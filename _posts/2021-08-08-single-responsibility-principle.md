---
layout: post
title: Single Responsibility Principle (SRP)
date: 2021-08-08 13:10
image: solid/srp/single-responsibility.png
comments: true
categories: [CSharp, ObjectOrientedProgramming, SOLID]
tags: [solid-principles, solid-principles-in-csharp, csharp-ile-solid-prensipleri,  single-responsibility-principle, single-responsibility-principle-nedir, single-responsibility-principle-ornek, tek-sorumluluk-prensibi]
---

Bir yazılım projesinde tasarlanan sınıflar (class) ve yapılar (struct), bazen benzer görevleri yerine getirebilmektedir. Böyle durumlarda sınıfların hangi görevleri yerine getireceği konusunda karışıklıklar ortaya çıkabilmektedir. Single Responsibility Prensibine göre bu tarz karmaşanın önüne geçmek için sınıfların ve yapıların iyi tanımlanmış tek sorumluluğu olması gerekmektedir. Eğer bir sınıf birden fazla görevin yerine getirilmesinden sorumlu olursa, gelecekte bu sınıfın değişme ihtimalini de arttırmaktadır. Bu da yazılım tasarımının bozulacağı anlamına gelmektedir.

Bu çalışmada öncelikle SRP’ye uygun olmayan basit bir tasarımla başlanarak, onu SRP’ye uygun hale getirilmeye çalışılacaktır. Örnek olarak geometrik şekillerin çevresini hesaplayan ve bu şekillerin çevrelerinin toplamını ekrana yazdıran basit bir console uygulaması yapılacaktır. Başlangıç olarak örneğin UML diyagramı aşağıdaki gibidir;

![Single Responsibility Principle Example UML - 1](/images/solid/srp/srp-uml-1.png)

Şekil 1. Console uygulamasının SRP’den önceki halinin UML diyagramı

&nbsp;

`IShape` interface’i ve bunu implement eden `Square` ve `Rectangle` class’larının C# kodları aşağıdaki gibidir;

<script src="https://gist.github.com/omereryilmaz/1730cbede312f88791c7f35187d687ed.js"></script>

<script src="https://gist.github.com/omereryilmaz/63007ffdd3af638bf22714758dd465e3.js"></script>

<script src="https://gist.github.com/omereryilmaz/0a166eb3f01c59fdc6cc65fdf6f08e3a.js"></script>

&nbsp;

Bu sınıfları kullanarak işlem yapan `CalcTotalPerimeter` class’ının da kodları aşağıdaki gibidir;

<script src="https://gist.github.com/omereryilmaz/623e101613a3ee84a63f75d016e635f3.js"></script>

Yukarıdaki kod incelendiğinde şekillere ait çevreyi hesaplama metodu olan `CalcPerimeter`’ın çağırıldığı ve bu hesaplamalardan dönen değerleri de `totalPerimeter` değişkeninde toplandığını görülmektedir. Son olarak da hesaplanan toplam çevre değeri `PrintToConsole` metodu ile console’a yazdırılmaktadır. İlgili kodu test etmek için `Program` class’ındaki Main metoduna aşağıdaki kodlar eklenir;

<script src="https://gist.github.com/omereryilmaz/93c33c404467d941df3bf265b7028373.js"></script>

Ekran Çıktısı:

```
Total Perimeter: 30
```

Çıktı değerleri kontrol edildiğinde uygulamanın doğru çalıştığı görünmektedir. Ancak tasarımsal olarak sorunlar barındırmaktadır. `CalcTotalPerimeter` class’ı incelendiğinde hem toplam çevreyi hesaplamakla hem de sonuçları ekrana yazdırmakla görevlidir. Yani birden fazla sorumluluğa sahiptir. Bu durum sonuçları yazdırma gereksinimleri genişletilmek istenildiğinde veya aynı metodlar başka sınıflar içinde gerekli olduğu durumlarda karmaşaya yola açabilir. Sonucunda da tasarımda değişikliğe gidilmesi gerekebilir. 

Bu tasarım sorununu gidermek için yazdırma sorumluluğu başka bir sınıfa verilmesi gerekmektedir. Bunun için `PrintResult` isminde bir class oluşturularak, `CalcTotalPerimeter` içerisindeki yazdırma metodu bu class’a eklenir.

![Single Responsibility Principle Example UML - 2](/images/solid/srp/srp-uml-2.png)

Şekil 2. Console uygulamasının SRP’ye göre düzenlenmiş halinin UML diyagramı

&nbsp;

`PrintResult` class’ının C# kodu aşağıdaki gibidir;

<script src="https://gist.github.com/omereryilmaz/2cedfcf748bd8670a48e8815546149aa.js"></script>

&nbsp;

Bu şekilde class’ların sorumlulukları bire indirgenmiş oldu. `CalcTotalPerimeter` class’ı sadece şekillerin çevrelerinin toplanmasından sorumluyken; `PrintResult` class’ı da ilgili sonuçların yazdırılma işlerinden sorumlu olmuştur. Artık console’a ya da bir dosyaya yazdırma işlemi yaptırmak istediğimizde değişiklik yapacağımız sadece bir sorumlu class’ımız olmuş oldu.

İlgili kodu test etmek için `Program` class’ındaki `Main` metoduna aşağıdaki kodlar eklenir;

<script src="https://gist.github.com/omereryilmaz/98803e2f09175e2f82ce73eef7557789.js"></script>


Sonuç olarak class’lar sadece bir görevi yerine getirmeye çalıştığı için dağınık olmayan ve okunması kolay kod yapısı elde edildi. Bu sayede tasarıma, ilgili class’ların yeniden düzenlenebilme, yeni özellikler ilave edebilme gibi yetenekler kazandırılmış oldu. Yukarıdaki örnekte görüleceği üzere class’lardaki özellikler kolaylıkla değiştirilip, yeni bir özellikler (dosyaya yazdırma) eklenebildi. Ayrıca class’lar daha bağımsız bir hale geldi. Bu şekilde ileride olabilecek gereksinimler doğrultusunda eklenecek olan class'ların (örneğin şekillerin alanlarının toplamını hesaplama) sonuç çıktıları da aynı yazdırma metodlarını kullanarak yazdırılabilir.

Güzel tasarlanmış yazılım sistemleri meydana getirebilmek için okunabilir ve sürdürülebilir kod yazılması temel amaç edinilmelidir. Bu yüzden SRP’yi doğru bir şekilde ve yerinde uygulamak önem arz etmektedir. Yanlış kullanımlarda organizasyonu iyi yapılmamış küçük parçalardaki class’ların elde edilmesine neden olabilmektedir. Böyle sistemlerde ise kod bakımı ve değişiklikler masraflı hale gelmiş olur.

İlgili Örneğin Kaynak Kodları: [Github - Solid Principles](https://github.com/omereryilmaz/SolidPrinciples)



&nbsp;
&nbsp;

##### Kaynaklar
- [1] The Principles of OOD, http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod 
- [2] Robert C. Martin and Micah Martin, “Agile Principles, Patterns, and Practices in C#”, 2006.
- [3] Code Maze, https://code-maze.com/solid-principles/
- [4] Nesneye Yönelik Programlama, https://acikogretim.istanbul.edu.tr/
 