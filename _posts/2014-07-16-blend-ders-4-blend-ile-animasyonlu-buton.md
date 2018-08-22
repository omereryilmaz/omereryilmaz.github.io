---
layout: post
title: Blend Ders-4 - Blend ile Animasyonlu Buton
date: 2014-07-16 16:25
image: blendbutonbaslik.jpg
comments: true
categories: [Blend, WPF, XAML]
---
<a href="/images/blendbutonbaslik.jpg"><img class="size-full wp-image-263 aligncenter" src="/images/blendbutonbaslik.jpg" alt="blendbutonbaslik" width="300" height="300" /></a>

&nbsp;

&nbsp;

<span style="color:#000000;">Blend ile ilgili serinin devamı niteliğindeki bu yazıda tasarımımıza uygun animasyonlu buton yapmaya calışacağız. Butonun, mouse işareti üzerine geldiğinde açılırken, üzerinden gittiğinde kapalı duruma gelmesini istiyoruz.</span>

<span style="color:#000000;">İlk önce ekrana bir <strong>Rectangle</strong> çizip buna buton özelliği veriyoruz. <strong>Rectangle</strong> ‘a buton özelliği vermek için; seçili haldeyken, </span>

<span style="color:#000000;"><strong>Tools &gt; Make Into Control...</strong> adımlarını takip ediyoruz.</span>

<a href="/images/blendbuton1.gif"><img class="alignnone size-full wp-image-264" src="/images/blendbuton1.gif" alt="blendbuton1" width="590" height="554" /></a>

&nbsp;

&nbsp;

&nbsp;

<span style="color:#000000;">Artık butonumuz oluşmuş durumda. Bu şekilde butonumuzun içerinde de çeşitli çizim ve resimler ekleyebiliriz. Ben butonumuzun ilk hali için projeye küçük bir resim dosyası dahil etmek istiyorum. Bunun için <strong>Projects</strong> bölümünden projemize sağ tıklayıp<strong> Exist New Item</strong> ‘e tıkladıktan sonra ilgili resmimizi seçip <strong>Aç</strong> diyoruz.</span>

<a href="/images/blendbuton2.gif"><img class="alignnone size-full wp-image-265" src="/images/blendbuton2.gif" alt="blendbuton2" width="593" height="530" /></a>

&nbsp;

<span style="color:#000000;">Projemize dahil ettiğimizi resmimizi butonun üzerine gelecek şekilde sürükleyip bırakıyoruz.</span>

<a href="/images/blendbuton3.gif"><img class="alignnone size-full wp-image-266" src="/images/blendbuton3.gif" alt="blendbuton3" width="485" height="391" /></a>

&nbsp;

<span style="color:#000000;">Butonumuz ilk haldeyken sadece üçgen resminin gözükmesini istiyoruz bunun için Button yazısının <strong>Opacity</strong> miktarını sıfırlıyoruz. Bu işlemi gerçekleştirmek için <strong>Content Prensenter</strong> seçili haldeyken;</span>

<a href="/images/blendbuton4.gif"><img class="alignnone size-full wp-image-267" src="/images/blendbuton4.gif" alt="blendbuton4" width="593" height="338" /></a>

&nbsp;

<span style="color:#000000;">Mouse imleci butonun üzerinde geldiğinde açılma animasyonun gerçekleşmesi için bir <strong>Trigger</strong> eklememiz gerekmektedir.</span>

<a href="/images/blendbuton5.gif"><img class="alignnone size-full wp-image-268" src="/images/blendbuton5.gif" alt="blendbuton5" width="594" height="421" /></a>

&nbsp;

<span style="color:#000000;">İmleç üzerinde olmadığında kapalı kalması içinde;</span>

<a href="/images/blendbuton6.gif"><img class="alignnone size-full wp-image-269" src="/images/blendbuton6.gif" alt="blendbuton6" width="553" height="426" /></a>

&nbsp;

<span style="color:#000000;">Bu şekilde animasyonlu buton stilimizi oluşturmuş olduk. Eğer istersek bu stilimizi birden fazla buton üzerinde de uygulayabiliriz. Bunun için;</span>

<a href="/images/blendbuton7.gif"><img class="alignnone size-full wp-image-270" src="/images/blendbuton7.gif" alt="blendbuton7" width="648" height="470" /></a>

&nbsp;

<span style="color:#000000;">Bu şekilde projemizdeki bütün butonların aynı stilde olmasını sağlayabiliriz. Çalışmamızın son hali aşağıdaki gibidir;</span>

<a href="/images/blendbuton8.gif"><img class="alignnone size-full wp-image-271" src="/images/blendbuton8.gif" alt="blendbuton8" width="517" height="344" /></a>
