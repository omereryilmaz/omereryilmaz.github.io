---
layout: post
title: TFS-2 - Team Foundation Server Nedir? Ne işe yarar?
date: 2014-07-13 17:37
image: tfs_nedir.png
comments: true
categories: [TFS]
---
<span style="color:#000000;">Team Foundation Server, Microsoft ‘un düzenli proje geliştirmek için ürettiği bir ürün ailesidir. Bir önceki yazımızda TFS ‘nin bir ALM (Application Lifecycle Management) aracı olduğunu söylemiştik ama TFS ‘nin sadece kaynak kodu kontrol eden bir mekanizma olarak düşünülmemelidir. Dolayısıyla burada işin içerisine metodojiler, süreçler, ekipler ve seçilen sürece göre iş kalemleri girmektedir.</span>

<a href="/images/tfs_diagram.png"><img class="size-full wp-image-245 aligncenter" src="/images/tfs_diagram.png" alt="tfs_diagram" width="550" height="356" /></a>
<p style="text-align:justify;"><span style="color:#000000;"> TFS ‘ye nereden sonra ihtiyaç duyuluyor ve TFS ‘yle neler yapabiliriz sorusuna bir örnekle cevaplandırmaya çalışalım. Bir projeyi tek başımıza yaparken kaynak kod paylaşma gibi zorunluluğumuz yoktur ama iş hayatında projeler en az iki kişilik ekiplerle yapılacağından kaynak kod ekip ile paylaşılmalıdır. Kaynak kodun paylaşılması flash bellek veya herhangi bir depolama birimiyle yapılabilir. Ama bu şekildeki paylaşımda revizyonlar sırasında karmaşaya neden olabilir veya yapılacak değişikliklerden önceki sürümlere ulaşım git gide imkansızlaşacaktır. Ekip çalışmalarındaki bu karmaşıklığın önlenmesi için TFS ‘nin Kaynak Kod Sunucusu kullanılabilir. Bu şekilde kodu her gönderdiğimizde bir önceki sürümü ezmez ve değişikliklerimizden önceki herhangi bir sürüme ulaşabiliriz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;"> TFS ‘de diğer yapılabilecekler:</span>
<span style="color:#000000;"> - Project Managment (Proje yönetimi)</span>
<span style="color:#000000;"> - Requerements Managment (Gereksinim Yönetimi)</span>
<span style="color:#000000;"> - Test Case Managment (Test Case Yönetimi)</span>
<span style="color:#000000;"> - Build Automation (Build Otomasyon)</span>
<span style="color:#000000;"> - Reporting (Raporlama İşlemleri)</span>
<span style="color:#000000;"> - Version Control (Versiyon Kontrolü)</span></p>
<p style="text-align:justify;"><span style="color:#000000;"> Tüm bunların üstüne bir proje geliştirmek istersek. Projeye süreç şablonu veriyoruz ve bu şablona göre hareket edeceğim diyoruz. Dolayısıyla ilgili sürece dahil olan alanlar otomatik olarak arka planda bizim adımıza oluşturulmuş oluyor. Bu işleme <strong>Process Template</strong> denir.</span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong> Lab Managment</strong> ‘ta ise test işlemlerimizi gerçekleştiririz.</span>
<span style="color:#000000;"> Bütün bu bahsettiklerimizi yaparken Visual Studuio ortamında ayrılmamıza gerek yoktur. Visual Studio 2012 ‘yle birlikte TFS ‘nin tüm özellkileri hazır bir şekilde geliyor. Ayrıca TFS ‘de Office entegrasyonu da söz konusudur. Pek çok analizi TFS ortamından çekip Excel ortamında raporlayabiliriz.</span>
<span style="color:#000000;"> Ekip halinde bir proje geliştiriyorsak sadece kaynak kodundan bahsedemeyiz. Örneğin projeye yeni bir özellik katacaksak bunun tartışması olabilir, bir hata bildirimi var ise bu hata bildiriminin takibi olabilir, projenin çeşitli aşamalarında oluşturulmuş dokümantasyonları olabilir yani ekip çalışmasının gereği olan pek çok belge ve süreç vardır. Bu noktada da TFS ile <strong>Share Point</strong> etkileşimi devreye girer. TFS, Share Point sayesinde işbirliği merkezine dönüşmüş olur.</span></p>
