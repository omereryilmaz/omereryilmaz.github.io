---
layout: post
title: WordPress Zararlı Kod Tespiti
date: 2017-02-14 01:05
image: WordPress_Virus_Tespiti.jpg
comments: true
categories: [WordPress]
tags: [nulled tema nedir, Theme Authenticity Checker, waordpress backdoor, WordPress, wordpress antivirus, wordpress exploit scanner, wordpress malware plugin, wordpress malware tespiti, wordpress security, wordpress virüs eklentileri, wordpress virüs tespiti]
---
Resmi WordPress temaları ve eklentilerinin yanısıra bu tarz eklenti ve temaları ücretsiz sağlayan bir çok site bulunmaktadır. Çoğu kişi de bilinçsiz bir şekilde ihtiyaçları doğrultusunda harici sitelerden bu tip temaları veya eklentileri kullanabilmektedirler. Peki onlara ne kadar güvenebiliriz? Bu çok büyük bir soru işaretidir. Çoğu tema ve eklentiler kötü niyetli kodlar eklenerek servis edilmektedirler. Bu zararlı kodların tespiti aşamasına geçmeden birkaç terimin üzerinden geçmekte fayda olacağı kanısındayım.

Çoğu hacker’ın veya kötü niyetli kişilerin amacı websitenize malware (kötü amaçlı yazılım veya kod) bulaştırmaktır. Bu kötü amaçlı kodlar şunları içerebilir :
<ul>
 	<li><strong>Pharma hack :</strong> Bir SEO saldırısı türüdür. Bazı sitelerin sizin siteniz üzerinden trafik kazanmaya çalışmasıdır. Bu sitenizin sansürlenmesine bile neden olabilir.</li>
 	<li><strong>Backdoor :</strong> FTP veya WordPress yönetici panelinizi istedikleri zaman erişmelerini sağlayan bir çeşit açık bir arka kapı bırakır.</li>
 	<li><strong>Kullanıcının zararlı dosya indirmesini sağlamak :</strong> Bu hackleme yönteminde websitenizi ziyaret eden kullanıcıları yanıltarak  zararlı kodlar içeren dosyaları bilgisayarlarına indirmelerini sağlar.</li>
 	<li><strong>Dosya ve veritabanı enjeksiyonları :</strong> Dosyalarınıza veya veritabanınıza, bilgisayar korsanlarının bir takım farklı şeyler yapmasını sağlayan kodu ekler.</li>
 	<li><strong>Kötü amaçlı yönlendirmeler :</strong> Ziyaretçileri veya kullanıcıları zararlı bir sayfaya yönlendirir.</li>
 	<li><strong>Kimlik avı :</strong> Kullanıcı adlarını, şifreleri, e-posta adreslerini ve diğer hassas bilgileri elde etmek için kullanılır [1].</li>
</ul>
&nbsp;

<strong>Nulled Tema veya Eklenti Nedir?</strong>

Basitçe kırılmış veya hacklenmiş temalara verilen genel bir addır. Bu tür temaları servis edenler çoğunlukla gelir sağlamak için reklamlar veya backlinkler ekleyebilmektedir. Bunlar da çoğu zaman site sahibi böyle bir şeyin farkında olmadığından elde ettiği ücretsiz ürünün kendisi için bir nimet olarak düşünür. Buradan da anlaşılacağı üzere nulled tema ve eklentilerde çoğu zaman beklenenin dışında reklamlar, backlinkler ve sitenizin performansını kötü etkileyecek kodlar bulunmaktadır [2].

&nbsp;
<blockquote>Bu uyarıyı yapmakta fayda görüyorum:

<strong>Asla nulled WordPress tema ve eklentilerine güvenmeyin!</strong></blockquote>
&nbsp;

<strong>Kötü Amaçlı Kodların Tespiti</strong>

Bir şekilde tema veya eklentiyi bilgisayarınıza indirmişseniz olası trojan veya solucan tespiti için mutlaka öncesinde antivirüs programınızla taratınız. Eğer bir virüs programı kullanmıyorsanız aşağıdaki alternatif çözümleri de deneyebilirsiniz. Çünkü çoğu zaman bazı uygulamaların göremediği zararlı kodları bazıları tespit edebiliyor, bunun için alternatifleri de denemekte fayda var.

&nbsp;

<strong>VirusTotal</strong>

<a href="/images/virustotal_1.png" target="_blank"><img class="wp-image-744" src="/images/virustotal_1.png" width="410" height="298" /></a> Şekil 1. Virustotal.com

Virustotal.com adresi bu iş için pratik bir yöntemdir. Online olarak sitenizde yüklü olan tema ve eklentilerdeki zararlı kodların tespitinin yanı sıra sitenize henüz yüklememiş olduğunuz .zip uzantılı tema veya eklentinizde de zararlı kod tespitine yardımcı olur. Bilgisayarınıza indirdiğiniz dosyaları taratmak istiyorsanız “File” bölümünden, sitenizi taratmak istiyorsanız da “URL” bölümünden bu işleminizi kolayca gerçekleştirebilirsiniz. Şekil 2’de herhangi bir zararlı yazılımın tespit edilmediği sonuç görülmektedir.

[caption id="attachment_745" align="aligncenter" width="604"]<a href="/images/virustotal_2.png" target="_blank"><img class="wp-image-745" src="/images/virustotal_2.png" width="604" height="346" /></a> Şekil 2. Virustotal tarama sonucu[/caption]

Şekil 3’de ise zararlı temayla gelen eklentide zararlı bir kod tespit edilmiş.

[caption id="attachment_746" align="aligncenter" width="619"]<a href="/images/virustotal_3.png" target="_blank"><img class="wp-image-746" src="/images/virustotal_3.png" width="619" height="310" /></a> Şekil 3. Virustotal tarama sonucu[/caption]

&nbsp;

<strong>Eklentilerle de zararlı kod tespiti yapılabilmektedir.</strong>

<strong>1.Sucuri Security</strong>

[caption id="attachment_751" align="aligncenter" width="648"]<a href="/images/sucurisecurity.png"><img class="wp-image-751 size-large" src="/images/SucuriSecurity-1024x499.png" width="648" height="316" /></a> Şekil 4. Sucuri Security yönetim paneli[/caption]

&nbsp;

Sucuri en bilindik güvenlik ve zararlı kod tespiti yapabilen WordPress eklentilerinden bir tanesidir. Websitenize yüklenen dosyalarınızı oluşruturulan karaliste doğrultusunda izlemenizi, güvenlikle ilgili bildirimler almanızı sağlayan çeşitli özellikleri bulunmaktadır.  Ücretsiz olarak <a href="https://sitecheck.sucuri.net">https://sitecheck.sucuri.net</a> adresinden de web sitenizi taratabilirsiniz. Ayrıca eklentide belirli bir ücret karşılığında websitenizi daha güvenli hale getirmek için güvenlik duvarı seçeneği de sunmaktadır.

Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins/sucuri-scanner/">Sucuri Security Eklentisi</a></strong>].

&nbsp;

<strong>2.Exploit Scanner</strong>

Exploit Scanner web sitenizin dosyalarını ve veritabanı tarayabilir, zararlı kod tespiti yapabilir. Websitenizi hacker saldırılarına karşı koruyamaz veya süpheli dosyaları silemez. Zararlı kod varlığından şüpheli bir dosya tespit edildiğinde bunun onarımını veya imhasını elle yapmalısınız.

Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins/exploit-scanner/">Exploit Scanner Eklentisi</a></strong>].

[caption id="attachment_752" align="aligncenter" width="550"]<a href="/images/exploitscanner_1.png"><img class="wp-image-752" src="/images/exploitscanner_1.png" width="550" height="363" /></a> Şekil 5. Exploit Scanner yönetim paneli[/caption]

Eklentinizi kurup, etkinleştirdikten sonra “Run the Scan” butonuna basıp tarama işlemini başlatabilirsiniz.

&nbsp;

<strong>3.AntiVirus</strong>

AntiVirus websitenizin tema dosyalarında tarama yaparak kötü amaçlı kodları tespit edebilen ücretsiz bir WordPress eklentisidir. Ayrıca herhangi bir kötü amaçlı kodun tespitinde e-posta yoluyla bilgilendirilme yoluna da gidebilme seçeneği sunmaktadır.

Eklenti yalnızca geçerli temayı taramaktadır. Yüklü diğer temalarda tarama işlemi gerçekleştirmez. Zaten güncellenmemiş eski temaları barındırmanız güvenlik açıklarına sebep olabileceğinden kaldırmanız önerilmektedir.

Eklentiyi bu adresten temin edebilirsiniz [<a href="https://wordpress.org/plugins/antivirus/"><strong>AntiVirus Eklentisi</strong></a>].

[caption id="attachment_753" align="aligncenter" width="536"]<a href="/images/antivirus_1.png"><img class="wp-image-753" src="/images/antivirus_1.png" width="536" height="360" /></a> Şekil 6. AntiVirus yönetim paneli[/caption]

Şekil 6’da görüldüğü üzere temamızı manuel olarak da otomatik olarak da taramamıza imkan sağlamaktadır. Temamızın günlük olarak taranmasını istiyorsak ilgili kutucuğu işaretleyip mail adresimizi yazdıktan sonra “Değişiklikleri Kaydet” butonuna tıklamalıyız.

&nbsp;

<strong>4.TAC (Theme Authenticity Checker)</strong>

Ücretsiz temalarda backlink ekleme çok yaygın bir tekniktir. Theme Authenticity Checker (Tema Özgünlük Denetleyicisi) eklentisi sayesinde bu kodları kolaylıkla bulabilirsiniz.

Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins-wp/tac/">TAC Eklentisi</a></strong>].

[caption id="attachment_754" align="aligncenter" width="534"]<a href="/images/tac_1.png"><img class="wp-image-754" src="/images/tac_1.png" width="534" height="397" /></a> Şekil 7. TAC yönetim paneli[/caption]

Şekil 7’de görüldüğü üzere yüklü TAC eklentimiz “Görünüm” menüsü altına gelmektedir. Buradan eklentimize tıklayarak mevcut temalarınızda özgünlük taraması işlemini gerçekleştirebilirsiniz.

[caption id="attachment_755" align="aligncenter" width="548"]<a href="/images/tac_2.png"><img class="wp-image-755" src="/images/tac_2.png" width="548" height="426" /></a> Şekil 8. TAC tarama sonuçları[/caption]

Şekil 8’de görüldüğü üzere tarama işlemi tamamlanmış ve temaların bir tanesinde link tespit edilmiş.

&nbsp;

<strong>4.Kendiniz</strong>

Aslında antimalware ve benzeri eklentilerin sayısı oldukça fazladır. Ama asıl önemli olan kriter güvenliğin kendi elinizde olmasıdır. Siz hata yapmadığınız müddetçe saldırıya maruz kalmanız çok nadirdir. Güvenmediğiniz kaynaklardan tema ve eklentileri yüklemeyerek, WordPress sürümünüzü güncel tutarak websitenizin güvenliğini bir nebzede olsa sağlamış olursunuz.

&nbsp;
<p class=""><strong>Kaynakça :</strong></p>
[1] https://www.elegantthemes.com/blog/tips-tricks/how-to-scan-your-wordpress-website-for-hidden-malware

[2] http://wordpress.stackexchange.com/questions/232041/what-are-nulled-themes
