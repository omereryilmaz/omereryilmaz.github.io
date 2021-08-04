---
layout: post
title: Çürüyen Yazılım Tasarımı (Rotting Design)
date: 2021-08-04 17:22
image: rot-design.png
comments: true
categories: [Genel, ObjectOrientedProgramming]
tags: [rotting-desigin, rot-software, code-smells, design-smells, curuyen-yazilim, curuyen-tasarim ]
---
<p style="text-align:justify;">
Jack Reeves 1992 yılında yaynladığı bir makalede, yazılım sistemi tasarımının kriterlerini karşılayan tek yazılım dökümantasyonun, kaynak kodları olduğu kavramını ortaya koydu [1]. Bu kavrama göre yazılım tasarımı, kaynak kodları temsil eden soyut bir kavram iken; UML (Unified Modelling Language) diyagramları ise  tasarımın parçalarını temsil etmektedir.

Yazılım büyüdükçe; tasarım, karmaşık hale gelme eğilimdindedir. Böyle bir durumun sonucunda; karmaşık, bakımı zor, modüllerin birbirine sıkı sıkıya bağlı, basit değişikliklerin bile gerçekleştirilmesinin çok zor olacağı bir kod yapısı ortaya çıkar.  Bu, yazılım tasarım sisteminin ve haliyle yazılım projesinin çürümesi anlamına gelmektedir.
</p>

&nbsp;

#### Yazılım Tasarımı Neden Çürür?
<p style="text-align:justify;">
Değişikliklere kolayca uyum sağlanamayan geliştirme ortamlarında; gereksinimler ilk tasarımın ön görmediği şekillerde değiştiğinde, yazılım sisteminin tasarımında bozulmalara neden olmaktadır. Çoğu zaman bu tarz değişikliklerinin veya eklemelerin hızlı bir şekilde yapılması istenildiğinde sistemin orijinal tasarımının bozulması önemsenmez. Ancak asıl yapıyı ihlal eden bu tarz değişiklikler devam ettikçe kod yapısını işin içinden çıkılmaz hale getirir. 
</p>

&nbsp;

#### Tasarım Kokuları (Design Smells)
<p style="text-align:justify;">
Robert ve ark. [2006] göre, zayıf bir şekilde tasarlanmış yazılımların yedi çürüme belirtisi bulunmaktadır. Bu belirtilerden herhangi biri ortaya çıktığında yazılımın çürüdüğü veya çürümeye başladığı anlaşılabilmektedir.
</p> 

- Katılık (Rigidity)
- Kırılganlık (Fragility)
-	Hareketsizlik (Immobility)
- Akışmazlık (Viscosity)
-	Gereksiz karmaşıklık (Needless complexity) 
-	Gereksiz tekrar (Needless repetition)
-	Bulanıklık (Opacity)

&nbsp;

###### Katılık (Rigidity)
<p style="text-align:justify;">
Yazılımın, basit yollarla bile değiştirilmesinin zor olma eğilimi göstermesidir. Yapılacak bir değişiklik, bağımlı modüllerde de değişiklikler yapılmasına neden oluyorsa, bu yazılım tasarımının katı olduğunu belirtir. Tasarım; değiştirilmesi gereken ne kadar modül veya bağımlı bileşen varsa o kadar katı olduğu anlamına gelmektedir.
</p>
&nbsp;

###### Kırılganlık (Fragility)
<p style="text-align:justify;">
Yazılımın, bir yerinde değişiklik yapıldığında buna tepki olarak birçok yerinde kırılma eğilimi göstermesidir. Genelde bu özelliğe sahip yazılımlarda sorunlar çözüldükçe daha fazla sorunlar çıkar. Sonuç olarak bir değişikliğin bile kolay bir şekilde tasarımı bozan durumlar, tasarımın kırılganlığına işaret etmektedir.
</p
>
&nbsp;

###### Hareketsizlik (Immobility)
<p style="text-align:justify;">
Yazılımda, diğer sistemlerde faydalı olabilecek modüller içerdiğinde hareketsizlik eğilimi gösterir. Bu bileşenleri orjinal yerinden ayırmak risklidir ve çok çaba gerektirir. Modüllerin arasındaki ilişki derecesine de `coupling` adı verilmektedir. 
</p>

&nbsp;

###### Akışmazlık (Viscosity)
<p style="text-align:justify;">
Akışmazlık belirtisi iki formda ortaya çıkmaktadır: ortamın ve yazılımın akışmazlığı. Ortamın akışmazlığı, geliştirme yapılan ortamın yavaş ve verimsiz olduğu durumlarda ortaya çıkar. Bu gibi durumların ortaya çıkması, çoğunlukla alınan görevin bir an önce yapılabilmesi için yazılım orijinal tasarımı gözardı edilmesiyle olur. Yazılımın akışmazlığında ise geliştiriciler tasarımı koyuyan zor yöntemler yerine kendilerine daha kolay yöntemleri tercih edebilmektedirler. Bu şekilde de yazılım tasarımının orijinal felsefesi gözardı edilmiş olur. Her iki durumda da akışmazlık olan bir proje, yazılım tasarımın korunmasının zor olduğu bir projedir. Sonuç olarak tasarımı korurken geliştirmeyi kolaylaştıracak; sistemler ve proje ortamları oluşturmak gerekmektedir.
</p>
&nbsp;

###### Gereksiz Karmaşıklık (Needless Complexity)
<p style="text-align:justify;">
Bir tasarım; hali hazırda kullanışlı olmayan öğeler içerdiğinde, gereksiz bir karmaşıklık ortaya çıkabilmektedir. Birçok beklenmedik duruma hazırlanmak, tasarımı hiç kullanılmayan yapılarla dolu hale getirir. Kullanılmayan bu yapılar, yazılım tasarımsal olarak ağırlığını da arttırır. Sonuç olarak ortaya; karmaşık ve anlaşılması zor hale gelen bir yazılım ortaya çıkar.
</p>

&nbsp;

###### Gereksiz Tekrar (Needless Repetition)
<p style="text-align:justify;">
Yeterince soyutlama yapılmayan yazılımlarda gereksiz kod tekrarları kaçınılmazdır. Kod tekrarının çok olması sistemdeki gereksiz kod fazlalığını arttırır. Gereksiz kod fazlalıkları da sistemin anlaşılmasını ve bakımını zorlaştırır. 
</p>

&nbsp;

###### Bulanıklık (Opacity)
<p style="text-align:justify;">
Bulanıklık, kodun okuması ve anlaşılmasının zor olma eğiliminde olduğunu belirtir. Zamanla gelişen kod daha bulanık hale gelme eğilimdedir. Bulanıklığı minimumda tutarak; açık ve anlaşılabilir kod yazmak ise sürekli çaba gerektiren bir eylemdir.
</p>

&nbsp;

#### Çürümelerden Kaçınmak
<p style="text-align:justify;">
Robert C. Martin’in 2000 yılında yazılım tasarımı sorunlarının çoğuyla başa çıkmamızı sağlayan <a href="http://omereryilmaz.com/solid-prensipleri" target="_blank">SOLID prensipleri</a>'ni tanıttı. Bu prensipler göz önüne alınarak oluşturulan tasarımlar çürümeyi minimuna indirirerek; tasarımı daha anlaşılır, esnek ve bakımı kolay hale getirir.
</p>

&nbsp;
&nbsp;

##### Kaynaklar
- [1] Jack W. Reeves, “What is Software Design?”, 1992 C++ Journal. 
- [2] Robert C. Martin and Micah Martin, “Agile Principles, Patterns, and Practices in C#”, 2006.
- [3] Alex Atomei, 2020, “Rotting Design”, https://www.cognizantsoftvision.com/blog/rotting-design/


