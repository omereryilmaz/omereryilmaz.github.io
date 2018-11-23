---
layout: post
title: TypeScript Nedir?
date: 2017-02-25 16:21
image: typescript_nedir.png
comments: true
categories: [JavaScript, TypeScript]
tags: [ecmascript nedir, neden typescript, neden typescript kullanmalıyız, tsc nedir, TypeScript, typescript amacı nedir, typescript avantajları, typescript özellikleri, typescript derleyicisi nedir, typescript language service nedir, typescript nedir, typescript vs javascript]
---
<p style="text-align:justify;">
TypeScript, Microsoft çalışanı Anders Hejlsberg (C# tasarımcısı) tarafından tasarlanan açık kaynaklı programlama dilidir. TypeScript hem dil hem de araçlar kümesidir. TypeScript, JavaScript’in ek özellikler almış hali de denilebilir (Şekil 1). İstemci tarafında (client-side) veya sunucu tarafında (server-side) çalışabilen JavaScript uygulamaları geliştirmek için kullanılabilir.
</p>
<p style="text-align:center;">
    <img src="/images/typescript_javascript.png"/>
</p>
<p style="text-align:center;">Şekil 1. TypeScript ve JavaScript</p>
<br>

<p style="text-align:justify;">
Kavramsal olarak JavaScript’i daha kolay ve güvenli bir şekilde yazmamızı sağlayan “sanal editör” olarak da düşünebiliriz. Büyük ve karmaşık kod yapısına sahip projelerde verimliliği arttırır. Uzun JavaScript satırlarını daha az komutla ifade etmemizi sağlar. Nedeni ise JavaScript’in fonksiyonel olmasına karşın TypeScript’in nesne yönelimli olmasıdır. Bunun yanı sıra TypeScript kodunu anlamak daha kolaydır. Eğer JavaScript biliyorsanız bunu TypeScript’de de kolayca kullanabilirsiniz. Yani var olan JavaScript kodlarınızı TypeScript dosyanızın içersine ekleyip derleyebilirsiniz.
</p>
<p style="text-align:justify;">
JavaScript büyük iş veya projeler için kullanıldığında belirli zorluklar ortaya çıkarmaktadır. C#, Java ve C++ gibi statik olarak derlenen diller, geliştiricinin derleme işlemi sırasında hata denetimi gerçekleştirirken, JavaScript ise çalıştırılıncaya kadar bu hata denetimini gerçekleştiremez. Microsoft, TypeScript ile birlikte derleme aşamasında hata denetimi yapılabilen bir JavaScript sunmayı amaçlamıştır.
</p>
<br>

<h3>TypeScript Özellikleri :</h3>
<ul style="text-align:justify;">
 	<li>Typescript, JavaScript'in temel yapı taşlarını benimser. Dolayısıyla, yalnızca TypeScript'i kullanmak için JavaScript'i öğrenmeniz yeterlidir. Tüm TypeScript kodunun çalıştırılması için JavaScript diline dönüştürülmesi gerekir.</li>
 	<li>TypeScript, diğer JS kütüphenelerini destekler. Derlenmiş TypeScript, herhangi bir JavaScript kodunda tüketilebilir. TypeScript ile oluşan JavaScript kodu mevcut tüm JavaScript frameworkleri, araçları ve kütüphanelerini yeniden kullanabilir.</li>
 	<li>JavaScript, TypeScript’tir. Bunun anlamı .js uzantılı herhangi bir dosya .ts olarak yeniden adlandırabilir ve diğer TypeScript dosyalarıyla derlenebilir.</li>
 	<li>TypeScript portatiftir. TypeScript, tarayıcılar, aygıtlar ve işletim sistemleri arasında taşınabilir. JavaScript’in çalıştığı herhangi bir ortamda çalışabilir. TypeScript’in çalışması için sanal makineye (VM) veya özel bir runtime çalışma ortamına ihtiyacı yoktur.</li>
</ul>
<br>

<h3>TypeScript ve ECMAScript</h3>
<p style="text-align:justify;">
ECMAScript, bir script dili standartıdır. Yayınlanmış 6 sürüm bulunmaktadır. Standartın 6. Versiyonuna “Harmony” kod adı verilmiştir. TypeScript, EcmaScript6 standartına sahiptir. Ayrıca temel dil özellikleri ECMAScript5 standartından yani JavaScript’in resmi şartnamesinden uyarlanmıştır (Şekil 2).
</p>
<p style="text-align:center;">
    <img src="/images/typescript1.png"/>
</p>
<p style="text-align:center;">
	Şekil 2. TypeScript'i oluşturan standartlar ve özellikler
</p>
<br>



<h3>Neden TypeScript?</h3>
<p style="text-align:justify;">
TypeScript, CoffeScript ve Dart programlama dilleri gibi diğer muadillerinden üstün olup, JavaScript’in gelişmiş bir türevidir. Bunun yanı sıra CoffeScript ve Dart gibi diller kendi başlarına yeni dillerdir ve kendilerine özgü yürütme ortamlarına ihtiyaç duyarlar.
</p>
<p style="text-align:justify;">
TypeScript'in çok popüler hale gelmesinin bir başka nedeni de Google Angular 2’dir. AngularJS’nin yeni sürümü resmi olarak JavaScript yerine tür denetimi (Type Checking) yeteneğinden dolayı TypeScript’i kullanacak şekilde uyarlanmıştır.
</p>
<br>

<h4>TypeScript’in avantajları:</h4>
<p style="text-align:justify;">
<strong>Derleme</strong>: JavaScript’i test etmek için çalıştırılması gerekir. Bu, bir hatanın olması durumunda tüm kodu kontrol etmek anlamına gelmektedir. Dolayısıyla, kodda hatalar bulmaya çalışmak için saatler harcamanız gerekir. TypeScript transpiler, hata denetimi özelliğini sağlar. Bu, komut dosyasının çalıştırılmadan önce hataları görmemize yardımcı olur.
</p>
<p style="text-align:justify;">
<strong>Güçlü Statik Tipleme</strong>: TypeScript, <strong>TLS</strong> (TypeScript Dil Servisi) aracılığıyla isteğe bağlı bir statik tipleme ve tür önerme sistemi ile birlikte gelir. TLS, herhangi bir tip tanımlanmamış değişkeni aldığı değere göre anlamlandırabilir
</p>
<p style="text-align:justify;">
TypeScript, sınıflar, arayüzler gibi  <strong>Nesneye Dayalı Programlama</strong> kavramlarını destekler.
</p>
<br>

<h3>TypeScript Bileşenleri</h3>
<p style="text-align:justify;">
TypeScript üç bileşene sahiptir (Şekil 3):
<br>
<p style="text-align:center;">
<img src="/images/typescript_cycle.png" />
</p>
<p style="text-align:center;">
	Şekil 3. TypeScript'i oluşturan bileşenler
</p>
<br>
<p style="text-align:justify;">
<strong>Dil:</strong> Sözdizimi(syntax), anahtar sözcükler (keywords) ve ek açıklamalardan oluşur.
</p>
<p style="text-align:justify;">
<strong>TypeScript Derleyicisi:</strong> TypeScript Derleyicisi (tsc), TypeScript’te yazılmış komutları JavaScript karşılığına çevirir.
</p>
<p style="text-align:justify;">
<strong>TypeScript Dil Servisi:</strong> Dil servisi, ifade tamamlama, kod formatlama, özetleme, renklendirme gibi tipik editör işlemlerinin gerçekleşmesini sağlar.
</p>
<br><br>

<strong>Kaynakça:</strong>
<ul>
 	<li>[1] typescriptlang.org</li>
 	<li>[2] en.wikipedia.org</li> 	
	<li>[3] TypeScript Tutorial Book</li> 
	<li>[4] Tony de Araujo - TypeScript in Plain Language Book</li> 
</ul>

