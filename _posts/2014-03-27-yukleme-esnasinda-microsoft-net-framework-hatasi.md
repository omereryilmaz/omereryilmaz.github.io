---
layout: post
title: MSSQL Server Microsoft .NET Framework hatası
date: 2014-03-27 23:32
image: sqlServer_logo.jpg
comments: true
categories: [Exception, MSSQLServer]
---


<span style="color:#000000;">Microsoft SQL Server 2012 'yi yükleme esnasında şöyle bir hatayla karşılaşmıştım;</span>

<p style="text-align:center;"><img src="/images/sql2012hata.png"  /></p>

<span style="color:#000000;"> </span>
<pre class="theme:github lang:default decode:true">Unhandled exception has occurred in your application. If you click Continue, the  application will ignore this error and attempt to continue. If you click Quit, the  application will close immediately.

An error occurred creating the configuration section handler for userSettings/Microsoft.SqlServer.Configuration.LandingPage.Properties.Settings: Could not load file or assembly 'System, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089' or one of its dependencies. Sistem belirtilen dosyayı bulamıyor.</pre>

<span style="color:#000000;">Bu hatanın sebebi var olan <strong>Microsoft_Corporation</strong> isimli dosyaymış. Bu dosyayı kaldırdığımızda hata da ortadan kalkıyor.</span>

<span style="color:#000000;">Bu dosyayı aşağıda belirtilen yerden</span>
<pre class="theme:github lang:default decode:true">c:users%kullanıcıadınız%appdatalocal</pre>
<span style="color:#000000;">ya da şu komutları kullanarak Başlat &gt; Çalıştır &gt; cmd</span>
<pre class="theme:github lang:default decode:true">rd /S C:Users%kullanıcıadınız%appdatalocalMicrosoft_Corporation</pre>
<span style="color:#000000;">silebilirsiniz.</span>

MsDos komutları ile ilgili ayrıntılı bilgi için ; <a href="https://tr.wikipedia.org/wiki/MS-DOS">Tıkla
</a>

<span style="color:#000000;"><span style="color:#ff0000;">Edit:</span> appdata dosyasının bulunamadığına dair mesaj aldım. Sebebi dosyanın gizli olmasıdır. Çözüm için aşağıdaki resimdeki adımları uygulayabilirsiniz.</span>

<p style="text-align:center;"><img src="/images/mELeUwf.png" /></p>
