---
layout: post
title: TFS-2 - Team Foundation Server Nedir? Ne işe yarar?
date: 2014-07-13 17:37
image: tfs_nedir.png
comments: true
categories: [ALM]
---
<p style="text-align:justify;">Team Foundation Server, Microsoft ‘un düzenli proje geliştirmek için ürettiği bir ürün ailesidir. Bir önceki yazımızda TFS ‘nin bir <a href="/alm-application-lifecycle-management-nedir/">ALM (Application Lifecycle Management)</a> aracı olduğunu söylemiştik ama TFS ‘nin sadece kaynak kodu kontrol eden bir mekanizma olarak düşünülmemelidir. Dolayısıyla burada işin içerisine metodojiler, süreçler, ekipler ve seçilen sürece göre iş kalemleri girmektedir.</p>
<br>
<p style="text-align:center;">
    <img src="/images/tfs_diagram.png"/>
</p>
<br>

<p style="text-align:justify;">TFS ‘ye nereden sonra ihtiyaç duyuluyor ve TFS ‘yle neler yapabiliriz sorusuna bir örnekle cevaplandırmaya çalışalım. Bir projeyi tek başımıza yaparken kaynak kod paylaşma gibi zorunluluğumuz yoktur ama iş hayatında projeler en az iki kişilik ekiplerle yapılacağından kaynak kod ekip ile paylaşılmalıdır. Kaynak kodun paylaşılması flash bellek veya herhangi bir depolama birimiyle yapılabilir. Ama bu şekildeki paylaşımda revizyonlar sırasında karmaşaya neden olabilir veya yapılacak değişikliklerden önceki sürümlere ulaşım git gide imkansızlaşacaktır. Ekip çalışmalarındaki bu karmaşıklığın önlenmesi için TFS ‘nin Kaynak Kod Sunucusu kullanılabilir. Bu şekilde kodu her gönderdiğimizde bir önceki sürümü ezmez ve değişikliklerimizden önceki herhangi bir sürüme ulaşabiliriz.</p>
<br>

<h2>TFS ‘de diğer yapılabilecekler:</h2>
<ul>
    <li>Proje yönetimi (Project Managment)</li>
    <li>Gereksinim Yönetimi (Requerements Managment)</li>
    <li>Test Yönetimi (Test Case Managment)</li>
    <li>Build Otomasyon (Build Automation)</li>
    <li>Raporlama İşlemleri (Reporting)</li>
    <li>Versiyon Kontrolü (Version Control)</li>
</ul>
<br>

<p style="text-align:justify;"> Tüm bunların üstüne bir proje geliştirmek istersek. Projeye süreç şablonu veriyoruz ve bu şablona göre hareket edeceğim diyoruz. Dolayısıyla ilgili sürece dahil olan alanlar otomatik olarak arka planda bizim adımıza oluşturulmuş oluyor. Bu işleme <strong>Process Template</strong> denir.</p>
<br>

<p style="text-align:justify;">
<strong> Lab Managment</strong> ‘ta ise test işlemlerimizi gerçekleştiririz. Bütün bu bahsettiklerimizi yaparken Visual Studuio ortamında ayrılmamıza gerek yoktur. Visual Studio 2012 ‘yle birlikte TFS ‘nin tüm özellkileri hazır bir şekilde geliyor. Ayrıca TFS ‘de Office entegrasyonu da söz konusudur. Pek çok analizi TFS ortamından çekip Excel ortamında raporlayabiliriz. Ekip halinde bir proje geliştiriyorsak sadece kaynak kodundan bahsedemeyiz. Örneğin projeye yeni bir özellik katacaksak bunun tartışması olabilir, bir hata bildirimi var ise bu hata bildiriminin takibi olabilir, projenin çeşitli aşamalarında oluşturulmuş dokümantasyonları olabilir yani ekip çalışmasının gereği olan pek çok belge ve süreç vardır. Bu noktada da TFS ile <strong>Share Point</strong> etkileşimi devreye girer. TFS, Share Point sayesinde işbirliği merkezine dönüşmüş olur.
</p>
