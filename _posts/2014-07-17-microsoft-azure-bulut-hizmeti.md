---
layout: post
title: Microsoft Azure Bulut Hizmeti
date: 2014-07-17 16:22
image: cloud_baslik.jpg
comments: true
categories: [MicrosoftAzure, Cloud]
---
<a href="/images/cloud_baslik.jpg"><img class="size-full wp-image-279 aligncenter" src="/images/cloud_baslik.jpg" alt="cloud_baslik" width="300" height="300" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Microsoft Azure Bulut Hizmetleri çok katmanlı uygulamalar oluşturmaya, oluşturduğumuz bu uygulamaları kullanıma sunmaya ve yönetmeye imkan sağlayan bir teknolojidir. Bunun yanı sıra uygulamalarımız için çoklu roller de oluşturulabilir. Bahsettiğimiz bu bulut hizmeti uygulamalarını .NET, Node.js, PHP, Java, Python ve Ruby dilleri dahil olmak üzere hemen hemen tüm popüler dilleri kullanılarak geliştirilebiliriz. Ayrıca uygulamamıza Windows Azure Mobile Services ve Media Services gibi servisleri de entegre edebiliriz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bulut servisi, alt yapı ve onunla ilgili oluşacak sorunlarla ilgilenmek yerine kendimiz için asıl önemli konuya odaklanmamızı sağlar. Dolayısıyla da iş yükü ve zamandan tasarruf etmiş oluruz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bulut servisinde çalışan uygulamalarımızın stabilite kontrolünü yapmak için Microsoft Azure Yönetim Portalını kullanabiliriz. Bu şekilde uygulamalarımızdan gerçek zamanlı olarak haberdar olabiliriz. Bozulma ve hizmet kesintisi gibi durumlarda gerçek zamanlı haberdar olmak için de yapılandırabiliriz. Uygulamamıza gelen talepler doğrultusunda kaynakları otomatik olarak büyütmek için otomatik ölçeklendirme özelliğini kullanabiliriz. Bu otomatik ölçeklendirme sayesinde maliyet açısından büyük bir tasarruf sağlanacaktır. Olayın daha iyi anlaşılması açısından ÖSYM ‘nin sitesini örnek verebiliriz. Sadece belirli günlerde sınav sonuçlarının açıklandığı v.s sitenin ziyaret sayısı milyonlarla ifade edilirken başka günlerde bu sayının oldukça az olma olasılığı yüksektir. Bu gibi durumlarda sistemi en yüksek ziyaretçi kapasitesine göre hazırlanması gerekiyor buda sistemin yoğun kullanılmadığı durumlarda kaynak israfına neden olmaktadır.</span></p>
&nbsp;

&nbsp;

<span style="color:#000000;"><strong>Bulut Servisinin Oluşturulması ve Kullanıma Sunulması</strong></span>
<p style="text-align:justify;"><span style="color:#000000;">Bir bulut servisi oluşturmak için önce bir dizi kavramları anlamamız gerekmektedir. Bulut hizmetinin iki adet rolleri bulunmaktadır.  Bunlar;</span>
<span style="color:#000000;">- Web Role</span>
<span style="color:#000000;">- Worker Role</span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Web Role :</strong> Kendimize ait bir IIS web sunucusu ve bu sunucuda front-end web uygulaması veya mid-tier servis katmanı barındırmamıza imkan sağlar.</span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Worker Role :</strong> Host uygulamarını asenkron çalıştırabiliriz, genellikle kullanıcı girişinden ve etkileşiminden bağımsız uzun soluklu veri işleme görevleri gerçekleştirilebilinir.</span>
<span style="color:#000000;">Her bir rol örneğinin tanımlandığı dosya uzantısı <strong>*.csdef</strong>, bulut hizmeti yapılandırma ayarlarının bulunduğu dosyanın uzantısı <strong>*cscfg</strong>, rolün genel amacını belirten dosyanın uzantısı da <strong>*.cspkg</strong> 'dir.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Microsoft Azure ‘da yeni bir bulut hizmeti oluşturmak için Microsoft Azure Portalı ‘nda sol taraftaki <strong>Cloud Services</strong> sekmesini seçmeliyiz. Eğer ilk bulut hizmetimizi oluşturuyorsak karşımıza gelen pencerede <strong>Create a Cloud Service</strong> yazısı çıkacaktır. Bulut servisini bu yazıya tıklayarak veya aşağıdaki<strong> New</strong> ‘e tıklayarak oluşturabiliriz. Bu aşamadan sonra karşımıza iki seçenek çıkar; <strong>Quick Create</strong> (Hızlı oluşturma), <strong>Custom Create</strong> (Özel Oluşturma). Şekilde görüldüğü gibi özel oluşturma seçilir. URL ve bölge bilgisi girildikten sonra <strong>Create Cloud Service</strong> 'e tıklayarak yeni bir cloud hizmeti oluşturmuş olduk. </span></p>
<a href="/images/cloud1.gif"><img class="alignnone size-full wp-image-280" src="/images/cloud1.gif" alt="cloud1" width="536" height="447" /></a>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Quick Create</strong> seçeneğiyle oluşturduktan sonra uygulamamızın çalışması ve uygulamamızın  gerekli SSL sertifikaları için Windows Azure SDK ‘sını yüklemeliyiz. Bir sonraki adım ise uygulamayı sunacağımız ortama karar vermektir. Microsoft Azure bulut hizmetleri iki farklı sunum ortamı sunmaktadır. Bunlar, <strong>staging</strong> (evreleme) ve<strong> production</strong> (üretim) ‘dir.</span></p>
<a href="/images/cloud2.gif"><img class="alignnone size-full wp-image-281" src="/images/cloud2.gif" alt="cloud2" width="616" height="573" /></a>

<span style="color:#000000;">Eğer evreleme sunum ortamını kullanmak istiyorsak; </span>

<a href="/images/cloud3.gif"><img class="alignnone size-full wp-image-282" src="/images/cloud3.gif" alt="cloud3" width="616" height="573" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Yukarıdaki şekilde yeni bir evreleme sunum ortamını oluşturma sihirbazı sayfasını göstermektedir. Bu sayfada ortamın adını, servis paketini (*.cspkg) ve hizmet yapılandırma dosyasının (*.cscfg) konumları belirtilir. Uygulamamız bir veya daha fazla rol içeriyor olsa bile uygulama sunum ortamı seçimi vardır ama Microsoft Azure en fazla iki tane rol için yüzde 99,95 uptime garantisi vermektedir. </span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Custom Create</strong> seçeneği de Quick Create seçeneğine benzemektedir ama bu seçenek ile bir bulut servisi oluşturduğumuzda bulut servis paketini sunmanı da sağlar. </span></p>
<p style="text-align:justify;"><span style="color:#000000;">Ayrıca şu iki önemli konuya da dikkat etmemiz gerekmektedir :</span>
<span style="color:#000000;">- Windows kayıt defterini kullanmaktan kaçınmalıyız.</span>
<span style="color:#000000;">- Eğer web.config veya app.config dosyaları kullanıyorsak bunun yerine bir servis yapılandırma dosyası (*.cscfg) kullanmalıyız.</span></p>

<h4 style="text-align:justify;"><span style="color:#808080;">Kaynak : </span></h4>
<h5 style="color:#9a9797;"><span style="color:#808080;">Introducing Windows Azure – Mitch Tulloch</span></h5>
&nbsp;
