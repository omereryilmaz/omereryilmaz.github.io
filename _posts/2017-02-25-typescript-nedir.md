---
layout: post
title: TypeScript Nedir?
date: 2017-02-25 16:21
image: TypeScript-Nedir.png
comments: true
categories: [JavaScript, TypeScript]
tags: [ecmascript nedir, neden typescript, neden typescript kullanmalıyız, tsc nedir, TypeScript, typescript amacı nedir, typescript avantajları, typescript özellikleri, typescript derleyicisi nedir, typescript language service nedir, typescript nedir, typescript vs javascript]
---
TypeScript, Microsoft çalışanı Anders Hejlsberg (C# tasarımcısı) tarafından tasarlanan açık kaynaklı programlama dilidir. TypeScript hem dil hem de araçlar kümesidir. TypeScript, JavaScript’in ek özellikler almış hali de denilebilir (Şekil 1). İstemci tarafında (client-side) veya sunucu tarafında (server-side) çalışabilen JavaScript uygulamaları geliştirmek için kullanılabilir.
<p style="text-align:center;">
<a href="/images/typescript-and-javascript.png" target="_blank"><img class="wp-image-766 size-medium" src="/images/typescript-and-javascript.png" width="300" height="300" /></a>
<p>Şekil 1. TypeScript ve JavaScript</p>
</p>

Kavramsal olarak JavaScript’i daha kolay ve güvenli bir şekilde yazmamızı sağlayan “sanal editör” olarak da düşünebiliriz. Büyük ve karmaşık kod yapısına sahip projelerde verimliliği arttırır. Uzun JavaScript satırlarını daha az komutla ifade etmemizi sağlar. Nedeni ise JavaScript’in fonksiyonel olmasına karşın TypeScript’in nesne yönelimli olmasıdır. Bunun yanı sıra TypeScript kodunu anlamak daha kolaydır. Eğer JavaScript biliyorsanız bunu TypeScript’de de kolayca kullanabilirsiniz. Yani var olan JavaScript kodlarınızı TypeScript dosyanızın içersine ekleyip derleyebilirsiniz.

JavaScript büyük iş veya projeler için kullanıldığında belirli zorluklar ortaya çıkarmaktadır. C#, Java ve C++ gibi statik olarak derlenen diller, geliştiricinin derleme işlemi sırasında hata denetimi gerçekleştirirken, JavaScript ise çalıştırılıncaya kadar bu hata denetimini gerçekleştiremez. Microsoft, TypeScript ile birlikte derleme aşamasında hata denetimi yapılabilen bir JavaScript sunmayı amaçlamıştır.

&nbsp;
<h3><strong>TypeScript Özellikleri :</strong></h3>
<ul>
 	<li>Typescript, JavaScript'in temel yapı taşlarını benimser. Dolayısıyla, yalnızca TypeScript'i kullanmak için JavaScript'i öğrenmeniz yeterlidir. Tüm TypeScript kodunun çalıştırılması için JavaScript diline dönüştürülmesi gerekir.</li>
 	<li>TypeScript, diğer JS kütüphenelerini destekler. Derlenmiş TypeScript, herhangi bir JavaScript kodunda tüketilebilir. TypeScript ile oluşan JavaScript kodu mevcut tüm JavaScript frameworkleri, araçları ve kütüphanelerini yeniden kullanabilir.</li>
 	<li>JavaScript, TypeScript’tir. Bunun anlamı .js uzantılı herhangi bir dosya .ts olarak yeniden adlandırabilir ve diğer TypeScript dosyalarıyla derlenebilir.</li>
 	<li>TypeScript portatiftir. TypeScript, tarayıcılar, aygıtlar ve işletim sistemleri arasında taşınabilir. JavaScript’in çalıştığı herhangi bir ortamda çalışabilir. TypeScript’in çalışması için sanal makineye (VM) veya özel bir runtime çalışma ortamına ihtiyacı yoktur.</li>
</ul>
&nbsp;
<h3><strong>TypeScript ve ECMAScript</strong></h3>
ECMAScript, bir script dili standartıdır. Yayınlanmış 6 sürüm bulunmaktadır. Standartın 6. Versiyonuna “Harmony” kod adı verilmiştir. TypeScript, EcmaScript6 standartına sahiptir. Ayrıca temel dil özellikleri ECMAScript5 standartından yani JavaScript’in resmi şartnamesinden uyarlanmıştır (Şekil 2).

[caption id="attachment_767" align="aligncenter" width="600"]<a href="/images/typescript_1.png"><img class="wp-image-767 size-full" src="/images/typescript_1.png" width="600" height="200" /></a> Şekil 2. TypeScript ve ECMAScript[/caption]

&nbsp;
<h3><strong>Neden TypeScript?</strong></h3>
TypeScript, CoffeScript ve Dart programlama dilleri gibi diğer muadillerinden üstün olup, JavaScript’in gelişmiş bir türevidir. Bunun yanı sıra CoffeScript ve Dart gibi diller kendi başlarına yeni dillerdir ve kendilerine özgü yürütme ortamlarına ihtiyaç duyarlar.

TypeScript'in çok popüler hale gelmesinin bir başka nedeni de Google Angular 2’dir. AngularJS’nin yeni sürümü resmi olarak JavaScript yerine tür denetimi (Type Checking) yeteneğinden dolayı TypeScript’i kullanacak şekilde uyarlanmıştır.

&nbsp;
<h4><strong>TypeScript’in avantajları:</strong></h4>
<strong>Derleme</strong>: JavaScript’i test etmek için çalıştırılması gerekir. Bu, bir hatanın olması durumunda tüm kodu kontrol etmek anlamına gelmektedir. Dolayısıyla, kodda hatalar bulmaya çalışmak için saatler harcamanız gerekir. TypeScript transpiler, hata denetimi özelliğini sağlar. Bu, komut dosyasının çalıştırılmadan önce hataları görmemize yardımcı olur.

<strong>Güçlü Statik Tipleme</strong>: TypeScript, <strong>TLS</strong> (TypeScript Dil Servisi) aracılığıyla isteğe bağlı bir statik tipleme ve tür önerme sistemi ile birlikte gelir. TLS, herhangi bir tip tanımlanmamış değişkeni aldığı değere göre anlamlandırabilir

TypeScript, sınıflar, arayüzler gibi  <strong>Nesneye Dayalı Programlama</strong> kavramlarını destekler.

&nbsp;
<h3><strong>TypeScript Bileşenleri</strong></h3>
TypeScript üç bileşene sahiptir (Şekil 3):

[caption id="attachment_768" align="aligncenter" width="600"]<a href="/images/typescript-cycle.png"><img class="wp-image-768 size-full" src="/images/typescript-cycle.png" width="600" height="200" /></a> Şekil 3. TypeScript Bileşenleri[/caption]

<strong>Dil:</strong> Sözdizimi(syntax), anahtar sözcükler (keywords) ve ek açıklamalardan oluşur.

<strong>TypeScript Derleyicisi:</strong> TypeScript Derleyicisi (tsc), TypeScript’te yazılmış komutları JavaScript karşılığına çevirir.

<strong>TypeScript Dil Servisi:</strong> Dil servisi, ifade tamamlama, kod formatlama, özetleme, renklendirme gibi tipik editör işlemlerinin gerçekleşmesini sağlar.

&nbsp;

&nbsp;
<h4><strong>Kaynakça</strong></h4>
<span style="font-size:small;">typescriptlang.org
en.wikipedia.org
TypeScript Tutorial Book
Tony de Araujo - TypeScript in Plain Language Book
</span>

