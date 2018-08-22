---
layout: post
title: Microsoft SQL Server 'ı Manual Olarak Silmek
date: 2014-03-30 17:43
image: sqlServer_logo.jpg
comments: true
categories: [MSSQLServer]
---
<span style="color:#000000;"><a href="/images/sqlServer_logo.jpg"><span style="color:#000000;"><img class="size-full wp-image-116 aligncenter" src="/images/sqlServer_logo.jpg" alt="sqlServer_logo" width="319" height="262" /></span></a></span>
<p style="text-align:justify;"><span style="color:#000000;">Daha önce sisteminize MSSQL server kurmuşsanız ve bir başka sürümünü yüklemek istediğinizde çoğunlukla başarılı bir sonuca ulaşamayabiliyorsunuz. Bunun nedeni daha önce kurmuş olduğunuz sürümün dosya ve kayıt defteri kalıntılarının yenileriyle çakışması diyebiliriz. Sistemden programı tam anlamıyla kaldırdığımızı düşünsekte, programla alakalı bir kaç dosya kalabiliyor. </span></p>
<span style="color:#800000;"><strong>Öncelikle databaselerinizin backup 'larını almayı unutmayın!</strong></span>

<span style="color:#000000;">Kalıntıların temizlenmesi için ;</span>

<strong><span style="color:#000000;"><span style="color:#003366;">1)</span> </span><span style="color:#000000;">Denetim Masası &gt; Programlar ve Özellikleri</span></strong>
<span style="color:#000000;">Burada Microsoft SQL Server 'la alakalı bütün programları siliyoruz. </span>
<span style="color:#000000;">Bazıları silinmemekte direnecektir, silinmeyenleri 3ncü adımdan sonra tekrar silmeyi deneyiniz.</span>

<span style="color:#000000;"><strong><span style="color:#003366;">2)</span> </strong>Başlat menüsünden <strong>SQL Configuration Manager</strong> 'dan bütün <strong>SQL Servis</strong> ve yapılandırmasını <strong>Disable</strong> yapıyoruz.</span>

<span style="color:#000000;"><strong><span style="color:#003366;">3)</span></strong>Windows kayıt defterindeki (Registry) SQL Server kayıtlarını siliyoruz. Wndows kayıt defterine girmek için;</span>
<span style="color:#000000;"><strong>Başlat &gt; Çalıştır</strong> 'a <strong>Regedit</strong> yazıp enter 'a basıyoruz.</span>

<a href="/images/kayitdefteri.jpg"><img class="alignnone size-medium wp-image-128" src="/images/kayitdefteri.jpg" alt="kayitdefteri" width="300" height="155" /></a>
<strong><span style="color:#000000;">Aşağıda belirtilen yoldaki kayıtları siliyoruz..</span></strong>
<span style="color:#000000;">HKEY_LOCAL_MACHINESYSTEM &gt; CurrentControlSet &gt; Services &gt; MSSQLServer</span>
<span style="color:#000000;">HKEY_LOCAL_MACHINESYSTEM &gt; CurrentControlSet &gt; Services &gt; SQLServerAgent</span>
<span style="color:#000000;">HKEY_LOCAL_MACHINESYSTEM &gt; CurrentControlSet &gt; Services &gt; MSSQLServerADHelper</span>
<span style="color:#000000;">HKEY_LOCAL_MACHINESYSTEM &gt; CurrentControlSet &gt; Services &gt; ReportServer</span>

<strong><span style="color:#000000;">Kayıt defterindeki SQL Configuration kayıtlarını da siliyoruz</span></strong>
<span style="color:#000000;">HKEY_LOCAL_MACHINE &gt; SOFTWARE &gt; Microsoft &gt; MSSQLServer</span>
<span style="color:#000000;">HKEY_LOCAL_MACHINE &gt; Software &gt; Microsoft &gt; Microsoft SQL Server</span>

<strong><span style="color:#000000;">Eğer Windows 64 bit olan sisteme SQL 'in 32 bitlik sürümünü yüklemişseniz aşağıda belirtilen kayıtları da silin.</span></strong>
<span style="color:#000000;">HKEY_LOCAL_MACHINE &gt; SOFTWARE &gt; WOW6432node &gt; Microsoft &gt; MSSQLServer</span>
<span style="color:#000000;">HKEY_LOCAL_MACHINE &gt; SOFTWARE &gt; WOW6432node &gt; Microsoft &gt; Microsoft SQL Server</span>

<span style="color:#000000;">Daha önce Denetim Masası &gt; Programlar ve Özellikleri 'nden silemediğiniz Microsoft SQL Server 'la alakalı programları tekrar silmeyi deneyin.</span>

<span style="color:#000000;">C:Program Files ve C:Program Files (x86) 'daki Microsoft SQL Server klasörünü de sildikten sonra sisteminizi yeniden başlatın.</span>
