---
layout: post
title: WordPress Mail Gönderme (SMTP) Ayarı
date: 2014-07-30 02:30
image: mail_wp.jpg
comments: true
categories: [SMTP, WordPress]
---
<span style="color:#000000;">Bir çok sunucuda çeşitli güvenlik sorunları veya farklı sebebler yüzünden mail gönderimi engellenmiş olabiliyor. Bu yüzden ne admin parola sıfırlaması gönderilebiliyor ne de iletişim bölümünden ziyaretçilerimizin bizle olan iletişimi sağlanabiliyor. </span>
<p style="text-align:justify;"><span style="color:#000000;"><a href="/images/mail0.png"><span style="color:#000000;"><img class="size-full wp-image-289 aligncenter" src="/images/mail0.png" alt="mail0" width="463" height="105" /></span></a></span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bu sorun çeşitli sunucular kullanılarak giderilebiliyor. Bu yazımızda gmail sunucusunu kullanarak bu sorunun üstesinden geleceğiz.</span>
<span style="color:#000000;">Öncelikle bir gmail hesabımız olması gerekmektedir. Bu gmail hesabımızın güvenlik ayarlarının ise verdiğimiz linkten girilerek resimdeki gibi “<strong>Daha az güvenli uygulamaların Google Hesabı'na erişimi etkinleştirilmiş</strong>” şeklinde yapılandırılmış olması gerekmektedir.</span></p>
<a href="https://www.google.com/settings/security/lesssecureapps" target="_blank">https://www.google.com/settings/security/lesssecureapps</a>

<a href="/images/mail1.png"><img class="alignnone size-full wp-image-290" src="/images/mail1.png" alt="mail1" width="644" height="420" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Bundan sonraki aşamada ise başka yerden yapılan bağlantının güvenlik zaafı gibi algılanmasının önüne geçmektir. Eğer bu adımı yapmazsanız gmail şifrenizi sürekli sıfırlamanızı isteyecektir.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bu ayarı yapmak için Gmail hesabımızda sağ üst köşedeki dişli çark simgesini tıklayıp <strong>Ayarlar</strong> bölümüne giriyoruz.</span></p>
<a href="/images/mail3.png"><img class="alignnone size-full wp-image-292" src="/images/mail3.png" alt="mail3" width="256" height="322" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Ayarlar bölümünden <strong>Yönlendirme ve POP/IMAP</strong> sekmesini tıklıyoruz. Burada <strong>IMAP’i Etkinleştir</strong> ‘i seçip <strong>Değişiklikleri Kaydet</strong> butonuna tıklıyoruz.</span></p>
<a href="/images/mail4.png"><img class="alignnone size-full wp-image-293" src="/images/mail4.png" alt="mail4" width="707" height="380" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Gmail ‘deki ayarlarımız şimdilik bu kadar. Şimdi gelelim wordpress ayarlarımıza. </span>
<span style="color:#000000;">Sitemizden mail göndermek için bir SMTP plugin ‘ine ihtiyacımız var. Ben <strong>WP-Mail-SMTP</strong> isimli plugin ‘i kullandım. Bu plugin ‘i indiriyoruz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Aşağıdaki resimdeki gibi wordpress kontrol panelimizin Plugins sekmesinden pluginimizi aratıp, indiriyoruz.</span></p>
<a href="/images/mail5.gif"><img class="alignnone size-full wp-image-294" src="/images/mail5.gif" alt="mail5" width="671" height="429" /></a>

&nbsp;

<span style="color:#000000;">İndirdiğimiz pluginin <strong>Settings</strong> bölümüne giriyoruz.</span>

<a href="/images/mail6.png"><img class="alignnone size-full wp-image-295" src="/images/mail6.png" alt="mail6" width="446" height="609" /></a>
<p style="text-align:justify;"><span style="color:#000000;"><strong>From Email :</strong> Maillerin gönderilmesini istediğiniz mail adresini buraya yazıyorsunuz. Bu iş için yapılandırmış olduğunuz mail adresinizi yazarsanız çalışma ihtimali daha yüksek olur.</span></p>
<span style="color:#000000;"><strong>From Name :</strong> Sitenizin adını veya kendi adınızı yazabilirsiniz.</span>

<span style="color:#000000;">Diğer ayarlar resimde gösterildiği gibi yapılmalı. En son ve önemli kısım olan Username ve Password kısmı.</span>

<span style="color:#000000;"><strong>Username :</strong> Sitenizden mail gönderilmesi için yapılandırmış olduğunuz gmail adresinizi buraya yazıyorsunuz.</span>

<span style="color:#000000;"><strong>Password :</strong> Gmail hesabınızın şifresini yazıyorsunuz.</span>

<span style="color:#993300;">(Eklentiyi ben yazmadığımdan herhangi bir güvenlik açığından sorumlu olmadığımı belirtmek isterim.)</span>

<span style="color:#000000;">Bu işlemlerimizi <strong>Save Changes</strong> butonunu tıklayarak kaydediyoruz.</span>

<span style="color:#000000;">Daha sonra ise mail gönderdiğimizde doğrulama hatası almamak için aşağıdaki linke tıklayıp başka uygulamalardan erişime izin vermemiz gerekmektedir.</span>

<a href="https://accounts.google.com/DisplayUnlockCaptcha" target="_blank">https://accounts.google.com/DisplayUnlockCaptcha</a>

<a href="/images/mail2.png"><img class="alignnone size-full wp-image-291" src="/images/mail2.png" alt="mail2" width="651" height="184" /></a>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Mail gönderme işleminin çalışıp çalışmadığını yüklediğimiz pluginin Settings bölümünün aşağısındaki test bölümüne herhangi bir email adresimizi yazarak test edebiliriz. ( Yüksek ihtimal test mailiniz Gereksiz kutusuna düşecektir. )</span></p>
<a href="/images/mail7.png"><img class="alignnone size-full wp-image-296" src="/images/mail7.png" alt="mail7" width="579" height="173" /></a>

&nbsp;
