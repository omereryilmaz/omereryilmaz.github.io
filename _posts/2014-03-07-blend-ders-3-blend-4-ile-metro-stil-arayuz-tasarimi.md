---
layout: post
title: Blend Ders-3 - Blend 4 ile Metro Stil Arayüz Tasarımı
date: 2014-03-07 19:18
image: metrologo.jpg
comments: true
categories: [Blend, WPF, XAML]
---
<p style="text-align:justify;"><span style="color:#000000;">Bu yazımızda etkili bir tasarım için uyulması gereken metotlara değindikten sonra basit metro arayüz tasarımı yapmaya çalışacağız.</span></p>
<a href="/images/metrologo1.jpg"><img class="size-full wp-image-107 aligncenter" src="/images/metrologo1.jpg" alt="metrologo" width="200" height="200" /></a>
<p style="text-align:justify;"><span style="color:#000000;text-align:justify;line-height:1.5em;">Tasarım konusunda alanımızda farklılık yaratmak istiyorsak öncelikle bir takım hususları göz önünde bulundurarak işe başlamalıyız. Bunlar yapacağımız yazılım hangi konuyla alakalı, hangi teknoloji üzerinde kullanacağımız ve hangi renkleri kullanacağımız gibi başlıklara ayırabiliriz. Bu hususlardan renkler konusu bazen bizim zevkimize kalınca ortaya renk cümbüşü tarzında bir şeyler çıkma olasılığı yüksek oluyor. Benim tavsiyem tek renk tonu üzerinden gidilmesi veya renklerin birbirine uyumlu olmasıdır. Bu tasarımımıza ciddiyet ve profesyonellik katacaktır.</span></p>
Bir önceki yazımızda yeni wpf projesi oluşturulmasına değinmiştik. Yeni projemizi oluşturduktan sonra kendimize özel form tasarımı yapmak için sol taraftaki<strong> Objects and Timeline</strong> bölümünden <strong>Window</strong> 'u seçiyoruz. Sonra sağ taraftaki <strong>Properties</strong> bölümüne geçiyoruz.</span></p>
<a href="/images/ders3_1brush.jpg"><img class="size-full wp-image-87 aligncenter" src="/images/ders3_1brush.jpg" alt="ders3_1brush" width="292" height="143" /></a>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Brushes</strong> kısmındaki 1 numaralı bölümde<strong> Background</strong> 'a tıklayıp daha sonra 2 numaralı bölümdeki <strong>No brush</strong> 'a tıklayoruz.</span></p>
<p style="text-align:center;"><a href="/images/ders3_2appe.jpg"><img class="alignnone size-full wp-image-88" src="/images/ders3_2appe.jpg" alt="ders3_2appe" width="293" height="211" /></a></p>
<span style="color:#000000;"><strong>Apperance</strong> kısmından <strong>AllowsTransparency</strong> 'i seçili hale getirip formumuza transparan özelliği veriyoruz.</span>   <a href="/images/ders3_3rec.jpg"><img class="size-full wp-image-89 aligncenter" src="/images/ders3_3rec.jpg" alt="ders3_3rec" width="296" height="126" /></a>   <span style="color:#000000;"><strong>Tools</strong> menüsünden <strong>Rectangle</strong> 'ı seçip formumuzun ilk halini çiziyoruz.</span>   <a href="/images/ders3_4recoval.jpg"><img class="alignnone size-full wp-image-90 aligncenter" src="/images/ders3_4recoval.jpg" alt="ders3_4recoval" width="454" height="332" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Çizdiğimiz dikdörtgeni seçili haldeyken kırmızı halka içerisinde gösterdiğimiz noktalarından tutup köşelerine oval bir görüntü kazandırabiliriz.</span></p>
<a href="/images/ders3_5opacity.jpg"><img class="size-full wp-image-91 aligncenter" src="/images/ders3_5opacity.jpg" alt="ders3_5opacity" width="298" height="168" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Oluşturduğumuz formun saydamlık ayarını ise <strong>Properties &gt; Appearance</strong> bölümündeki <strong>Opacity</strong> 'den ayarlıyoruz. Bu ayar 0% 'a yaklaştıkça seçili bileşenin saydamlığını arttıracaktır.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Biz metro stilinde bir arayüz yapacağımız için <strong>Opacity 100%</strong> , <strong>RadiusX 0</strong> ve <strong>RadiusY 0</strong> olacaktır.</span></p>
<a href="/images/ders3_6stroke.jpg"><img class="size-full wp-image-92 aligncenter" src="/images/ders3_6stroke.jpg" alt="ders3_6stroke" width="289" height="329" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Form arkaplanı olarak çizdiğimiz Dikdörtgenin renk ayarlarını <strong>Brush</strong> kısmından <strong>Fill : #FFFFF</strong>, <strong>Stroke: #515151</strong> olacak şekilde ayarlıyoruz.</span></p>

<h5><span style="color:#333333;">Fill: Nesnemizin rengi.</span></h5>
<h5><span style="color:#333333;">Stroke: Nesnemizin etrafındaki çizginin rengi.</span></h5>
<p style="text-align:justify;"><span style="color:#000000;">Formumuza logomuzu ve program ismi ve sürüm bilgileri üzerinde bulunduracağımız başlık kısmı ekliyoruz. Bunun için yine <strong>Tools</strong> kısmından <strong>Rectangle</strong> 'ı seçip başlık kısmımızı oluşturuyoruz.</span></p>


[caption id="attachment_93" align="aligncenter" width="300"]<a href="/images/ders3_7baslik.jpg"><img class="size-medium wp-image-93 " src="/images/ders3_7baslik-300x136.jpg" alt="ders3_7baslik" width="300" height="136" /></a> Resmi büyütmek için tıklayınız.[/caption]
<p style="text-align:justify;"><span style="color:#000000;">Oluşturduğumuz başlık kısmı ile arkaplandaki dikdörtgenin çevresinin aynı renkte olmasına dikkat edelim.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bu işlemden sonra oluşturduğumuz nesnelere isimlerini verelim. <strong>Object and Timeline</strong> bölümünde arkaplan için çizdiğim dikdörtgene tıklayıp sağ üst bölümdeki <strong>Name</strong> kısmına arkaplan, başlık dikdörtgenine de baslik yazip enter 'a basıyoruz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Programımız çalıştığında başlığa tıklayıp sürükleye bilmek için baslik nesnemiz seçili haldeyken sağ taraftaki <strong>Properties</strong> bölümünden;</span></p>
<a href="/images/ders3_8drag.jpg"><img class="size-medium wp-image-94 aligncenter" src="/images/ders3_8drag-300x174.jpg" alt="ders3_8drag" width="300" height="174" /></a>
<p style="text-align:justify;"><span style="color:#000000;">1 numaralı yıldırım sembollü yere tıklayıp, 2 numaralı <strong>MouseLeftButtonDown</strong> isimli yere iki kere tıklarız. Gelen kod bölümüne ;</span></p>

<pre class="lang:c# decode:true" title="Form sürükleme komutu">private void baslik_MouseLeftButtonDown(object sender, System.Windows.Input.MouseButtonEventArgs e)
        {
        	// TODO: Add event handler implementation here.
			DragMove();
        }</pre>
<span style="color:#000000;">kodunu yazalım.</span> <span style="color:#000000;">Daha sonra tekrar xaml.cs kısmından tasarımımızı yaptığımız .xaml bölümüne geçelim.</span> <span style="color:#000000;">Şimdi logomuzu ya da herhangi bi resmi (50x50px boyutunda) tutup sürükleyip formumuzun üstüne bırakıyoruz.</span> <a href="/images/ders3_8logo.jpg"><img class="size-medium wp-image-95 aligncenter" src="/images/ders3_8logo-300x202.jpg" alt="ders3_8logo" width="300" height="202" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Şimdi de logomuzun yanına programımızın ismini ve versiyon bölümünü yazmak için <strong>Tools</strong> menüsünden <strong>TextBlock</strong> 'u seçip logomuzun yanında konumlandırıyoruz.</span></p>


[caption id="attachment_96" align="aligncenter" width="300"]<a href="/images/ders3_10baslikyazi.jpg"><img class="size-medium wp-image-96 " src="/images/ders3_10baslikyazi-300x77.jpg" alt="ders3_10baslikyazi" width="300" height="77" /></a> Resmi büyütmek için tıklayınız.[/caption]
<p style="text-align:justify;"><span style="color:#000000;">Konumlandırdığımız 2 numaralı bölümde başlığımızı yazıyoruz ve 3 numaralı bölümden ise fontumuzu ve boyutlandırmamızı yapıyoruz. Aynı işlemleri yaparak şekilde görüldüğü gibi ekstra bilgiler de eklenebilir. Bu işlemleri yaptıktan sonra <strong>F5</strong> 'e basıp metro stilindeki formumuzun ilk halini elde etmiş olduk.</span></p>
<p style="text-align:justify;"><a href="/images/ders3_11formson.png"><img class="alignnone size-full wp-image-97" src="/images/ders3_11formson.png" alt="ders3_11formson" width="610" height="413" /></a></p>
<em style="line-height:1.5em;"><span style="color:#000000;">Bir sonraki yazımızda buton stilleri oluşturmaya başlayıp, formumuza uygun butonları tasarlamaya çalışacağız. Görüşmek üzere..</span></em>


