---
layout: post
title: Microsoft Azure Web Site Hizmeti
date: 2014-07-15 13:17
image: azureweb0.jpg
comments: true
categories: [MicrosoftAzure, WebSite]
---
<a href="/images/azureweb0.jpg"><img class="size-full wp-image-250 aligncenter" src="/images/azureweb0.jpg" alt="azureweb0" width="300" height="300" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Windows Azure Website Servisi web uygulamalar oluşturabileceğimiz güvenli ve esnek bir platformdur. Ayrıca kolay ve kullanışlı bir portala sahiptir. CakePHP, DasBlog, .DotNetNuke, WordPress gibi popüler birçok web çözümlerine imkan sağlamaktadır. Eğer kendimiz bir websitesini sıfırdan oluşturmak istiyorsak ücretsiz olan Web Matrix aracını yükleyerek bu işlemi gerçekleştirebiliriz. Web Matrix, ASP.NET, PHP, HTML5, CSS3, ve Node gibi en son teknoloji olan web teknolojilerini destekleyen bir web geliştirme aracıdır. Bütün bunları yaparken geliştirme ortamı olarak Visual Studio ‘yu kullanmak istersek de Windows Azure SDK ‘yı yüklememiz gerekmektedir. </span></p>
<p style="text-align:justify;"><span style="color:#000000;"> Yeni bir websitesi oluşturduğumuzda çoğunlukla bir veritabanına da ihtiyaç duyarız. Bu ihtiyacı karşılamak içinde SQL veritabanı ya da MySQL veritabanı oluşturmayı tercih edebiliriz. Ayrıca Team Foundation Service, CodePlex, GitHub, veya Bitbucket gibi kaynak denetimi sağlayan platformları da desteklemektedir.</span></p>
&nbsp;

&nbsp;

<span style="color:#000000;"><strong>Web Sitesi Oluşturmak için;</strong></span>

<a href="/images/azure-web1.jpg"><img class="size-medium wp-image-251 aligncenter" src="/images/azure-web1.jpg" alt="azure-web1" width="300" height="166" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Yeni bir websitesi oluşturmak için yukarıdaki resimde görünen Microsoft Azure portalından sol taraftan Web Sites sekmesini tıklayıp karşımıza gelen pencereden CREATE A WEB SITE veya +NEW ‘e tıklarız.</span></p>
&nbsp;

<a href="/images/azure-web2.jpg"><img class="size-medium wp-image-252 aligncenter" src="/images/azure-web2.jpg" alt="azure-web2" width="300" height="166" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">COMPUTE &gt; WEB SITE adımları takip edilmeli. URL kısmına oluşturduğumuz web sitesine ulaşmak için kullanacağımız adresi yazmalıyız. Buraya yazdığımız adres kullanıma uygun durumdaysa şekildeki gibi yeşil onay işareti çıkacaktır. Web Hosting Plan ‘ı olduğunu gibi bırakıyoruz. REGION bölümünde ise hangi coğrafi bölgedeki serverı kullanmak istiyorsak o seçilir. Burada tavsiye edilen bizim konumuza en yakın server olmasıdır. </span></p>
<p style="text-align:justify;"><span style="color:#000000;"> Web sitemizi oluştururken QUICK CREATE seçeneğini seçersek ek yapılandırma ayarları olmadan oluşturmamızı sağlar. Yeni veya daha önce oluşturulmuş bir veritabanını kullanarak web sitesi oluşturmak istiyorsak CUSTON CREATE seçeneği seçilmeli. Eğer ben bunların hiç biriyle uğraşamam herşey hazır olsun diyorsak FROM GALERY seçeneğine tıklayıp Microsoft Azure Galeriden kendimize uygun bir platformu seçeriz.</span></p>
&nbsp;

<span style="color:#000000;"><a href="/images/azure-web3.jpg"><span style="color:#000000;"><img class="size-medium wp-image-253 aligncenter" src="/images/azure-web3.jpg" alt="azure-web3" width="300" height="166" /></span></a></span>

<span style="color:#000000;">Ben örneği WordPress ile yapacağım için WordPress ‘i seçiyorum ve aşağıdaki okla ileriyi tıklıyoruz. </span>

&nbsp;

<span style="color:#000000;"><a href="/images/azure-web4.jpg"><span style="color:#000000;"><img class="size-medium wp-image-254 aligncenter" src="/images/azure-web4.jpg" alt="azure-web4" width="300" height="166" /></span></a></span>

<span style="color:#000000;">Karşımıza gelen pencereden ilgili yerleri dolduruyoruz. Deployment Settings bölümünü olduğu gibi bırakıyoruz. </span>

&nbsp;

<span style="color:#000000;"><a href="/images/azure-web5.jpg"><span style="color:#000000;"><img class="size-medium wp-image-255 aligncenter" src="/images/azure-web5.jpg" alt="azure-web5" width="300" height="166" /></span></a></span>

<span style="color:#000000;">Otomatik oluşturduğu database adını ve bulunduğu coğrafi bölgeyi gösteriyor. Aşağıda, belirtilen yasal koşulları kabul edip onay butonuna tıklarız.</span>

&nbsp;

<span style="color:#000000;"><a href="/images/azure-web6.jpg"><span style="color:#000000;"><img class="size-medium wp-image-256 aligncenter" src="/images/azure-web6.jpg" alt="azure-web6" width="300" height="166" /></span></a></span>

<span style="color:#000000;">Kısa sürede web sitemiz yayına girmiş olacak. Websitemizin durumunu STATUS bölümünden kontrol edebiliriz. </span>

&nbsp;

<a href="/images/azure-web8.jpg"><img class="size-medium wp-image-257 aligncenter" src="/images/azure-web8.jpg" alt="azure-web8" width="300" height="166" /></a>

<span style="color:#000000;">Oluşturduğumuz adrese internet tarayıcımızla girdiğimizde WordPress ‘in kurulmuş olduğunu görebiliriz. Buradaki ilgili alanları doldurup web sitemizi hazır hale getirmiş oluruz. </span>

&nbsp;

<span style="color:#000000;">Microsoft Azure konusuyla ilgili çalışmalarımızı, paralel olarak yürüttüğümüz <span style="color:#008080;"><a title="RoslynComu" href="http://roslyncomu.wordpress.com/category/microsoft-azure/" target="_blank"><span style="color:#008080;">RoslynComu</span></a></span> adresinden de takip edebilirsiz.</span>

&nbsp;
<h5><span style="color:#808080;">Kaynaklar :</span>
<span style="color:#808080;">Introducing Windows Azure - Mitch Tulloch</span></h5>
