---
layout: post
title: Windows 'ta dig komutu kullanımı
date: 2014-04-02 18:00
image: dig0windows.jpg
comments: true
categories: [Windows, Network]
---
<span style="color:#000000;"><a href="/images/dig0windows.jpg"><span style="color:#000000;"><img class="size-full wp-image-134 aligncenter" alt="dig0windows" src="/images/dig0windows.jpg" width="300" height="300" /></span></a></span>

&nbsp;

<span style="color:#000000;">Windows 'ta <strong>dig</strong></span><span style="color:#000000;"> komutunu çalıştırabilmek için sistemimize çeşitli kurulum ve yüklemeler yapmamız gerekiyor.</span>

<strong><span style="color:#ff0000;">Adım 1:</span></strong>
<span style="color:#008080;"><strong><a href="ftp://ftp.isc.org/isc/bind9/9.5.0-P2/" target="_blank"><span style="color:#008080;">ftp://ftp.isc.org/isc/bind9/9.5.0-P2/</span></a></strong></span>
<span style="color:#000000;">adresinden <strong>BIND9.5.0-P2.zip</strong></span><span style="color:#000000;"> uzantılı dosyayı indiriyoruz.</span>

<strong><span style="color:#ff0000;">Adım 2:</span></strong>
<span style="color:#000000;">İndirdiğimiz *.zip dosyasını herhangi bir yere çıkartıyoruz.</span>

<strong><span style="color:#ff0000;">Adım 3:</span></strong>

<span style="color:#000000;"><a href="/images/dig1.jpg"><span style="color:#000000;"><img alt="dig1" src="/images/dig1.jpg" width="111" height="26" /></span></a></span>
<span style="color:#000000;">Dosyadan <strong>vcredist_x86</strong> isimli dosyayı çift tıklayıp yüklenmesini sağlıyoruz.</span>

<strong><span style="color:#ff0000;">Adım 4:</span></strong>

<span style="color:#000000;"><a href="/images/dig2.jpg"><span style="color:#000000;"><img class="alignnone size-full wp-image-136" alt="dig2" src="/images/dig2.jpg" width="593" height="154" /></span></a></span>

<span style="color:#000000;">resimde görülen<strong><span style="color:#ff6600;"> libbind9.dll<span style="color:#000000;">,</span> libdns.dll<span style="color:#000000;">,</span> libeay32.dll<span style="color:#000000;">,</span> libisc.dll<span style="color:#000000;">,</span> libisccc.dll<span style="color:#000000;">,</span> libisccfg.dll<span style="color:#000000;">,</span> liblwres.dll</span></strong> ve <strong><span style="color:#ff6600;">dig.exe</span></strong> dosyalarını kopyalayıp <span style="color:#145151;"><strong>C:WindowsSystem32</strong></span> klasörüne yapıştırınız.</span>

<strong><span style="color:#000000;">Eğer işletim sisteminiz 64 bit ise aynı dosyaları <span style="color:#145151;">C:WindowsSysWOW64</span> klasörüne kopyalayınız.</span></strong>

<span style="color:#ff0000;"><strong>Adım 5:</strong> </span>
<span style="color:#000000;"><strong><span style="color:#145151;"> Başlat &gt; Çalıştır &gt; cmd</span></strong> yazıp enter a basarak Komut İstemi 'ne giriniz.</span>
<span style="color:#000000;"><strong><span style="color:#145151;">&gt;dig</span></strong> yazıp enter a bastığımızda komutumuz çalışır hale gelmiş olacaktır.</span>

<a href="/images/dig3.jpg"><img class="size-full wp-image-137 aligncenter" alt="dig3" src="/images/dig3.jpg" width="673" height="198" /></a>

&nbsp;

&nbsp;
