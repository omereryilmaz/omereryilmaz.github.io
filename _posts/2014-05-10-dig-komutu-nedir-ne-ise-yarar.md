---
layout: post
title: dig Komutu nedir? Ne işe yarar?
date: 2014-05-10 19:24
image: dig001.jpg
comments: true
categories: [Windows, Network]
---
<a href="/images/dig001.jpg"><img class="size-full wp-image-196 aligncenter" src="/images/dig001.jpg" alt="dig001" width="250" height="250" /></a>

<span style="color:#000000;">dig 'in açılımı Domain Information Groper yani Alan adı Bilgi Yoklayıcı' dır.</span>
<p style="text-align:justify;"><span style="color:#000000;">Adından da anlaşılacağı üzere alan adı sorgulamalarında kullanılmaktadır. Bu komut sayesinde DNS zehirlenmesinin olup olmadığı anlaşılabilir. dig komutunu Windows işletim sistemlerinde kullanabilmek için bir takım yüklemeler ve ayarlar yapmamız gerekmektedir. Bununla ilgili bilgi sahibi olmanız açısından Windows ' ta dig komutu kullanımı yazımı incelemenizi öneriyorum.</span></p>
<span style="color:#000000;">Bütün yükleme ve ayarlarımızı yaptıktan sonra artık dig komutumuzu çalıştırabiliriz. </span>

<span style="color:#000000;">Kullanımı en basit haliyle şu şekildedir: <strong>&gt;dig www.siteadi.com</strong></span>

<span style="color:#000000;"><strong>Başlat &gt; Çalıştır &gt; cmd</strong> yazıp enter a basarak Komut İstemi ‘ne giriniz.</span>

<span style="color:#000000;">Windows 8 ve 8.1 kullanıcıları ise Komut istemine ulaşmak için Metro Arayüze girip arama kısmını cmd yazıp enter 'a basmaları yeterli olacaktır.</span>

<span style="color:#000000;">Komut istemine girdikten sonra;</span>
<pre class="lang:batch decode:true"> dig www.google.com</pre>
<a href="/images/dig11.jpg"><img class="alignnone size-full wp-image-193" src="/images/dig11.jpg" alt="dig1" width="591" height="324" /></a> <span style="color:#000000;">Karşımıza çıkan verilerde IN A 64.15.117.248 makine adına karşılık gelen IP adresidir.</span> <span style="color:#000000;">IP adresine karşılık gelen makine adresini bulmak için de </span> <strong><span style="color:#000000;">dig -x ipadresi</span></strong> <span style="color:#000000;">Örneğin 64.15.117.248 IP adresine karşılık gelen makine adına bakalım, bunun için;</span>
<pre class="lang:batch decode:true ">dig -x 64.15.117.248</pre>
&nbsp;

<a href="/images/dig21.jpg"><img class="alignnone size-full wp-image-194" src="/images/dig21.jpg" alt="dig2" width="589" height="324" /></a>

&nbsp;

&nbsp;

<span style="color:#000000;">dig sorgumuzu *.txt uzantılı dosyaya aktarmak istiyorsak;</span>
<pre class="lang:batch decode:true ">dig www.google.com &gt;D:digtext.txt</pre>
&nbsp;

<a href="/images/dig31.jpg"><img class="alignnone size-full wp-image-195" src="/images/dig31.jpg" alt="dig3" width="595" height="386" /></a>

<span style="color:#000000;">Başka bir DNS sunucusu üzerinden sorgulamamızı yapmak için;</span>
<pre class="lang:batch decode:true  crayon-selected">dig @8.8.8.8 www.twitter.com</pre>
&nbsp;

<span style="color:#000000;"> </span>
<p style="text-align:justify;"><span style="color:#000000;">Bu şekilde Google 'ın DNS 'si üzerinden gerçekleştirdik. Aslında bu şekilde DNS zehirlenmesi tespitinin de yapılması mümkündür. DNS zehirlenmesi, tespiti ve zehirlenmenin engellemesi konusuna bir başka yazımda ayrıntılı olarak değineceğim.</span></p>
