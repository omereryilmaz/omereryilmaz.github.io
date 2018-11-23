---
layout: post
title: WordPress Zararlı Kod Tespiti
date: 2017-02-14 01:05
image: WordPress_Virus_Tespiti.jpg
comments: true
categories: [WordPress]
tags: [nulled tema nedir, Theme Authenticity Checker, waordpress backdoor, WordPress, wordpress antivirus, wordpress exploit scanner, wordpress malware plugin, wordpress malware tespiti, wordpress security, wordpress virüs eklentileri, wordpress virüs tespiti]
---
<p style="text-align:justify;">
Resmi WordPress temaları ve eklentilerinin yanısıra bu tarz eklenti ve temaları ücretsiz sağlayan bir çok site bulunmaktadır. Çoğu kişi de bilinçsiz bir şekilde ihtiyaçları doğrultusunda harici sitelerden bu tip temaları veya eklentileri kullanabilmektedirler. Peki onlara ne kadar güvenebiliriz? Bu çok büyük bir soru işaretidir. Çoğu tema ve eklentiler kötü niyetli kodlar eklenerek servis edilmektedirler. Bu zararlı kodların tespiti aşamasına geçmeden birkaç terimin üzerinden geçmekte fayda olacağı kanısındayım.
</p>

<p style="text-align:justify;">
Çoğu hacker’ın veya kötü niyetli kişilerin amacı websitenize malware (kötü amaçlı yazılım veya kod) bulaştırmaktır. Bu kötü amaçlı kodlar şunları içerebilir :
</p>
<ul style="text-align:justify;">
 	<li><strong>Pharma hack :</strong> Bir SEO saldırısı türüdür. Bazı sitelerin sizin siteniz üzerinden trafik kazanmaya çalışmasıdır. Bu sitenizin sansürlenmesine bile neden olabilir.</li>
 	<li><strong>Backdoor :</strong> FTP veya WordPress yönetici panelinizi istedikleri zaman erişmelerini sağlayan bir çeşit açık bir arka kapı bırakır.</li>
 	<li><strong>Kullanıcının zararlı dosya indirmesini sağlamak :</strong> Bu hackleme yönteminde websitenizi ziyaret eden kullanıcıları yanıltarak  zararlı kodlar içeren dosyaları bilgisayarlarına indirmelerini sağlar.</li>
 	<li><strong>Dosya ve veritabanı enjeksiyonları :</strong> Dosyalarınıza veya veritabanınıza, bilgisayar korsanlarının bir takım farklı şeyler yapmasını sağlayan kodu ekler.</li>
 	<li><strong>Kötü amaçlı yönlendirmeler :</strong> Ziyaretçileri veya kullanıcıları zararlı bir sayfaya yönlendirir.</li>
 	<li><strong>Kimlik avı :</strong> Kullanıcı adlarını, şifreleri, e-posta adreslerini ve diğer hassas bilgileri elde etmek için kullanılır [1].</li>
</ul>
<br>

<p style="text-align:justify;">
<strong>Nulled Tema veya Eklenti Nedir?</strong>
</p>
<p style="text-align:justify;">
Basitçe kırılmış veya hacklenmiş temalara verilen genel bir addır. Bu tür temaları servis edenler çoğunlukla gelir sağlamak için reklamlar veya backlinkler ekleyebilmektedir. Bunlar da çoğu zaman site sahibi böyle bir şeyin farkında olmadığından elde ettiği ücretsiz ürünün kendisi için bir nimet olarak düşünür. Buradan da anlaşılacağı üzere nulled tema ve eklentilerde çoğu zaman beklenenin dışında reklamlar, backlinkler ve sitenizin performansını kötü etkileyecek kodlar bulunmaktadır [2].
</p>
<br>
<blockquote>Bu uyarıyı yapmakta fayda görüyorum:

<strong>Asla nulled WordPress tema ve eklentilerine güvenmeyin!</strong></blockquote>
<br>

<p style="text-align:justify;">
<strong>Kötü Amaçlı Kodların Tespiti</strong>
</p>
<p style="text-align:justify;">
Bir şekilde tema veya eklentiyi bilgisayarınıza indirmişseniz olası trojan veya solucan tespiti için mutlaka öncesinde antivirüs programınızla taratınız. Eğer bir virüs programı kullanmıyorsanız aşağıdaki alternatif çözümleri de deneyebilirsiniz. Çünkü çoğu zaman bazı uygulamaların göremediği zararlı kodları bazıları tespit edebiliyor, bunun için alternatifleri de denemekte fayda var.
</p>
<br>

<p style="text-align:justify;">
<strong>VirusTotal</strong>
</p>

<p style="text-align:center;">
    <img src="/images/virustotal1.png"/>
</p>
<p style="text-align:center;">
    Şekil 1. Virustotal.com
</p>
<br>

<p style="text-align:justify;">
Virustotal.com adresi bu iş için pratik bir yöntemdir. Online olarak sitenizde yüklü olan tema ve eklentilerdeki zararlı kodların tespitinin yanı sıra sitenize henüz yüklememiş olduğunuz .zip uzantılı tema veya eklentinizde de zararlı kod tespitine yardımcı olur. Bilgisayarınıza indirdiğiniz dosyaları taratmak istiyorsanız “File” bölümünden, sitenizi taratmak istiyorsanız da “URL” bölümünden bu işleminizi kolayca gerçekleştirebilirsiniz. Şekil 2’de herhangi bir zararlı yazılımın tespit edilmediği sonuç görülmektedir.
</p>
<p style="text-align:center;">
    <img src="/images/virustotal2.png"/>
</p>
<p style="text-align:center;">
    Şekil 2. Virustotal tarama 
</p>
<br>

<p style="text-align:justify;">
Şekil 3’de ise zararlı temayla gelen eklentide zararlı bir kod tespit edilmiş.
</p>

<p style="text-align:center;">
    <img src="/images/virustotal3.png"/>
</p>
<p style="text-align:center;">
    Şekil 3. Virustotal tarama sonucu
</p>
<br>


<p style="text-align:justify;">
<strong>Eklentilerle de zararlı kod tespiti yapılabilmektedir.</strong>
</p>

<p style="text-align:center;">
<strong>1.Sucuri Security</strong>
</p>
<p style="text-align:center;">
    <img src="/images/sucurisecu.png"/>
</p>
<p style="text-align:center;">
    Şekil 4. Sucuri Security yönetim paneli
</p>
<br>

<p style="text-align:justify;">
Sucuri en bilindik güvenlik ve zararlı kod tespiti yapabilen WordPress eklentilerinden bir tanesidir. Websitenize yüklenen dosyalarınızı oluşruturulan karaliste doğrultusunda izlemenizi, güvenlikle ilgili bildirimler almanızı sağlayan çeşitli özellikleri bulunmaktadır.  Ücretsiz olarak <a href="https://sitecheck.sucuri.net">https://sitecheck.sucuri.net</a> adresinden de web sitenizi taratabilirsiniz. Ayrıca eklentide belirli bir ücret karşılığında websitenizi daha güvenli hale getirmek için güvenlik duvarı seçeneği de sunmaktadır.
</p>
<p style="text-align:justify;">
Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins/sucuri-scanner/">Sucuri Security Eklentisi</a></strong>].
</p>
<br>

<p style="text-align:justify;">
<strong>2.Exploit Scanner</strong>
</p>
<p style="text-align:justify;">
Exploit Scanner web sitenizin dosyalarını ve veritabanı tarayabilir, zararlı kod tespiti yapabilir. Websitenizi hacker saldırılarına karşı koruyamaz veya süpheli dosyaları silemez. Zararlı kod varlığından şüpheli bir dosya tespit edildiğinde bunun onarımını veya imhasını elle yapmalısınız.
</p>
<p style="text-align:justify;">
Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins/exploit-scanner/">Exploit Scanner Eklentisi</a></strong>].
</p>
<p style="text-align:center;">
    <img src="/images/exploitscanner.png"/>
</p>
<p style="text-align:center;">
    Şekil 5. Exploit Scanner yönetim paneli
</p>
<br>
<p style="text-align:justify;">
Eklentinizi kurup, etkinleştirdikten sonra “Run the Scan” butonuna basıp tarama işlemini başlatabilirsiniz.
</p>
<br>

<p style="text-align:justify;">
<strong>3.AntiVirus</strong>
</p>
<p style="text-align:justify;">
AntiVirus websitenizin tema dosyalarında tarama yaparak kötü amaçlı kodları tespit edebilen ücretsiz bir WordPress eklentisidir. Ayrıca herhangi bir kötü amaçlı kodun tespitinde e-posta yoluyla bilgilendirilme yoluna da gidebilme seçeneği sunmaktadır.
</p>
<p style="text-align:justify;">
Eklenti yalnızca geçerli temayı taramaktadır. Yüklü diğer temalarda tarama işlemi gerçekleştirmez. Zaten güncellenmemiş eski temaları barındırmanız güvenlik açıklarına sebep olabileceğinden kaldırmanız önerilmektedir.
</p>
<p style="text-align:justify;">
Eklentiyi bu adresten temin edebilirsiniz [<a href="https://wordpress.org/plugins/antivirus/"><strong>AntiVirus Eklentisi</strong></a>].
</p>

<p style="text-align:center;">
    <img src="/images/antivirus.png"/>
</p>
<p style="text-align:center;">
    Şekil 6. AntiVirus yönetim paneli
</p>
<br>
<p style="text-align:justify;">
Şekil 6’da görüldüğü üzere temamızı manuel olarak da otomatik olarak da taramamıza imkan sağlamaktadır. Temamızın günlük olarak taranmasını istiyorsak ilgili kutucuğu işaretleyip mail adresimizi yazdıktan sonra “Değişiklikleri Kaydet” butonuna tıklamalıyız.
</p>
<br>

<p style="text-align:justify;">
<strong>4.TAC (Theme Authenticity Checker)</strong>
</p>
<p style="text-align:justify;">
Ücretsiz temalarda backlink ekleme çok yaygın bir tekniktir. Theme Authenticity Checker (Tema Özgünlük Denetleyicisi) eklentisi sayesinde bu kodları kolaylıkla bulabilirsiniz.
</p>

<p style="text-align:justify;">
Eklentiyi bu adresten temin edebilirsiniz [<strong><a href="https://wordpress.org/plugins-wp/tac/">TAC Eklentisi</a></strong>].
</p>
<p style="text-align:center;">
    <img src="/images/tac1.png"/>
</p>
<p style="text-align:center;">
    Şekil 7. TAC yönetim paneli
</p>
<br>

<p style="text-align:justify;">
Şekil 7’de görüldüğü üzere yüklü TAC eklentimiz “Görünüm” menüsü altına gelmektedir. Buradan eklentimize tıklayarak mevcut temalarınızda özgünlük taraması işlemini gerçekleştirebilirsiniz.
</p>
<br>

<p style="text-align:center;">
    <img src="/images/tac2.png"/>
</p>
<p style="text-align:center;">
    Şekil 8. TAC tarama sonuçları
</p>
<br>

<p style="text-align:justify;">
Şekil 8’de görüldüğü üzere tarama işlemi tamamlanmış ve temaların bir tanesinde link tespit edilmiş.
</p>
<br>


<p style="text-align:justify;">
<strong>4.Kendiniz</strong>
</p>

<p style="text-align:justify;">
Aslında antimalware ve benzeri eklentilerin sayısı oldukça fazladır. Ama asıl önemli olan kriter güvenliğin kendi elinizde olmasıdır. Siz hata yapmadığınız müddetçe saldırıya maruz kalmanız çok nadirdir. Güvenmediğiniz kaynaklardan tema ve eklentileri yüklemeyerek, WordPress sürümünüzü güncel tutarak websitenizin güvenliğini bir nebzede olsa sağlamış olursunuz.
</p>
<br><br>
<p class=""><strong>Kaynakça :</strong></p>
[1] https://www.elegantthemes.com/blog/tips-tricks/how-to-scan-your-wordpress-website-for-hidden-malware

[2] http://wordpress.stackexchange.com/questions/232041/what-are-nulled-themes
