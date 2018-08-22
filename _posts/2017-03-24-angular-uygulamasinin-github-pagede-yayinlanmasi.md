---
layout: post
title: Angular Uygulamasının GitHub Page'de Yayınlanması
date: 2017-03-24 01:06
image: angular-github-page.jpg
comments: true
categories: [Angular, GitHub]
tags: [angular-cli, angular-cli-ghpages, angular-cli-nedir, angular-github-deploy, Angular-github-hosting, angular-github-pages, angular-github-yükleme, angular-video-anlatım, cli-nedir, GitHub]
---
<p style="text-align:center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/b5HbOyRKw8Q" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></p>

<h2>Angular CLI</h2>
Angular CLI, Angular uygulamalar için oluşturulmuş ember-cli temeline dayanan bir CLI'dır (<em>Command Line Interface CLI, Command Line User-Interface olarak da bilinir. Kullanıcının veya istemcinin ardışık olarak komutlar göndererek etkileşim kurmasını sağlar.</em>). Angular uygulamalarını başlangıç durumununa getiren (initialize), iskelet yapısınının oluşturulmasını sağlayan (scaffold) ve bakım işlemlerinin yapılmasını (maintain) kolaylaştıran bir araçtır. Bilindiği üzere bir Angular uygulamasını ayağa kaldırmak biraz zahmetli bir iştir. Bu zahmetli işi bir kaç komut satırıyla bizim yerimize yapıp uygulamanın ayağa kaldırılmasını sağlar.

Angular CLI ve uygulamanın bağımlılıkları (dependencies) için Node 4 veya daha üst sürümüyle birlikte NPM 3 veya daha üst sürümünün bilgisayarınızda kurulu olması gerekmektedir.

Bu yazımızda Angular CLI yardımıyla bir Angular 2 uygulaması oluşturup bunu Github üzerinde bir web sayfası olarak yayınlamaya çalışacağız.
<h2>Angular CLI ile Angular Uygulamasının Oluşturulması</h2>
<ol>
 	<li>Comand Prompt’la hangi klasöre projemizi oluşturacaksak cd komutuyla o klasöre gidiyoruz.</li>
</ol>
<p style="text-align:center;"><strong><span style="color:#008080;">cd C:AngularOrnekler</span></strong></p>

<ol start="2">
 	<li>“<strong><span style="color:#008080;">npm install -g angular-cli</span></strong>” Angular-Cli ‘ı indiriyoruz.</li>
 	<li>“<span style="color:#008080;"><strong>ng new angular-ornek</strong></span>” komutuyla ilgili klasöre projemizi oluşturuyoruz.</li>
 	<li>“<strong><span style="color:#008080;">cd angular-ornek</span></strong>” komutuyla projemizin bulunduğu klasöre gidiyoruz.</li>
 	<li>“<strong><span style="color:#008080;">ng serve</span></strong>” komutuyla projemizi test etmek için çalıştırıyoruz.</li>
</ol>
&nbsp;
<h2>Projenin GitHub’a uygun hale getirilmesi</h2>
<ol>
 	<li>“<span style="color:#008080;"><strong>cd angular-ornek</strong></span>” ile projemizin klasörüne gidip, yine console üzerinde “<strong><span style="color:#008080;">code .</span></strong>” komutunu çalıştırıp, projenin visual code’da açılmasını sağlıyoruz.</li>
 	<li>Projemizin github üzerinden yayınlanabilmesi için gh-pages branch’ı oluşturmamız lazım, projemiz bu branch üzerinden yayın yapacak. Bunun için aşağıdaki kodu çalıştırırız;</li>
</ol>
<p style="text-align:center;"><strong><span style="color:#008080;">npm i -g angular-cli-ghpages</span></strong></p>

<ol start="3">
 	<li>Package.json içerisine şu satırı ekliyoruz;</li>
</ol>
"scripts": { <strong><span style="color:#008080;">"deploy": "ng build -sm -ec -bh /repo ismi/ &amp; ngh --no-silent"</span></strong>,...

<strong>NOT :</strong> 3.maddedeki repo ismini daha önceden github sayfanızda oluşturduğunuz repository ismi olacak.

&nbsp;
<h2><strong>Projenin GitHub’a yüklenmesi</strong></h2>
<a href="/images/angular-github-gizli.png"><img class="aligncenter size-full wp-image-840" src="/images/angular-github-gizli.png" alt="" width="441" height="231" /></a>
<ol>
 	<li>Öncelikle yukarıdaki resimdeki gösterilen “<strong><span style="color:#008080;"> .git</span> </strong>“ dosyasını siliyoruz.</li>
 	<li>“<strong> <span style="color:#008080;">git init</span> </strong>” komutuyla git işlemini başlatıyoruz.</li>
 	<li>“ <strong><span style="color:#008080;">git add .</span></strong> “ komutuyla yeni veya modifiye edilmiş dosyaları göndermek için hazırlıyoruz.</li>
 	<li>“ <strong><span style="color:#008080;">git commit -m "My first commit"</span></strong> “ ilk commit’imizi oluşturuyoruz.</li>
 	<li>" <strong><span style="color:#008080;">git remote add origin https://githubrepoadresi.git</span></strong> " komutunu çalıştırıp github bağlantısını oluşturuyoruz.</li>
 	<li>“ <span style="color:#008080;"><strong>git remote</strong></span> “ yazıp var olan bağlantıların listesini görebiliriz.</li>
 	<li>" <strong><span style="color:#008080;">git push -u origin master</span></strong> " komutuyla projemizin tüm dosyalarını( -u ) github a gönderiyoruz.</li>
</ol>
&nbsp;
<h2><strong>Angular Sayfasının GitHub’a Deploy Edilmesi</strong></h2>
<ol>
 	<li>“ <strong><span style="color:#008080;">npm run deploy</span></strong> “ komutuyla deploy işlemini başlatıyoruz.</li>
 	<li>Bu işlem sona erdiğinde sayfamız yayınlanmış olacaktır. Sayfamızın linkine ise Github &gt; Settings bölümünden ulaşabiliriz.</li>
</ol>
<p style="text-align:center;"><a href="/images/angular-github-pages.png">
</a> <a href="/images/angular-github-settings.png"><img class="aligncenter size-full wp-image-842" src="/images/angular-github-settings.png" alt="" width="993" height="111" /></a></p>
<p style="text-align:center;"><img class="aligncenter size-full wp-image-841" src="/images/angular-github-pages.png" alt="" width="528" height="245" /></p>
<strong>NOT: </strong>Uygulamamızı deploy ettikten sonra herhangi bir güncelleme yaptıysak; bu güncellemenin sayfamızda gerçekleşmesi için öncelikle yaptığımız değişikliği commit etmemiz ve “<strong><span style="color:#008080;"> npm run deploy</span></strong> ” komutunu tekrardan çalıştırarak deploy işlemini tekrarlamamız gerekmektedir (Yapılan değişiklikler birkaç dakika sonra sayfaya yansıyacaktır).

<strong>Kaynak Kodlar : </strong><a href="https://github.com/omreryilmaz/angular-ornek"><strong>https://github.com/omreryilmaz/angular-ornek</strong></a>

<strong>Demo : </strong><a href="https://omreryilmaz.github.io/angular-ornek/"><strong>https://omreryilmaz.github.io/angular-ornek/</strong></a>

&nbsp;

<strong>Kaynakça:</strong>
<ul>
 	<li>[1] https://en.wikipedia.org/wiki/Command-line_interface</li>
 	<li>[2] https://www.npmjs.com/package/angular-cliL</li> 	
</ul>
