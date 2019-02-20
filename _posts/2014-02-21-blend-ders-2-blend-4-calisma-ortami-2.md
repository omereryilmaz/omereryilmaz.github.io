---
layout: post
title: Blend Ders-2 - Blend 4 Çalışma Ortamı
date: 2014-02-21 20:53
image: ders2_1.jpg
comments: true
categories: [Blend, WPF]
---
<span style="color:#000000;text-align:justify;">Bu yazımızda Blend çalışma ortamını kısaca tanımaya çalışacağız.  Photoshop, Flash gibi programlara aşina olanların fazla zorlanmayacağı bir tasarıma sahiptir. Bu tür programların hiç birini kullanmamış olanların bile kolayca adapte olabileceğini düşünüyorum. </span>

<span style="color:#000000; text-align:justify;">Sözü fazla uzatmadan Blend ile ilk projemimizi oluşturmaya başlayalım. </span>

<p><span style="color:#000000; text-align:justify;">Microsoft Expression Blend 4 programımızı çalıştırıyoruz. Karşımıza şöyle bir ekran çıkacak ;</span></p>

<p style="text-align:center;">
<a href="/images/ders2_1.jpg"><img class="size-medium wp-image-56 aligncenter" src="/images/ders2_1.jpg" alt="ders2_1" width="251" height="300" /></a>
</p>

<p style="text-align:justify;"><span style="color:#000000;">Bu giriş penceresinden bahsedecek olursak, görüldüğü üzere üç kısımlı tab menüden oluşmaktadır. Bu menüden <strong>Projects</strong> kısmında <strong>New Project</strong> ile <strong>Yeni Proje</strong> veya <strong>Open Project</strong> ile kayıtlı herhangi bir proje açılır. <strong>Help</strong> menüsünden program ile ilgili yardımlara ulaşabilirsiniz. <strong>Samples</strong> kısmında ise bu programla yapılmış çeşitli hazır proje ve oyun örneklerine ulaşabilirsiniz.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Biz yeni bir proje yapacağımız için <strong>New Project</strong> 'e tıklıyoruz.</span></p>
<p style="text-align:center;"><img src="/images/ders2_2.jpg" alt="ders2_2" width="452" height="387" /></p>
<p style="text-align:justify;"><span style="color:#000000;">Karşımıza çıkan pencereden 1 numaralı<strong> Project types</strong> bölümünden proje tipini, 2 numaralı bölümde ne tür bir uygulama yapacağımızı, 3 numaralı bölümde ise projemizin ismi ve kayıt edildiği yer seçilir. Biz uygulamamızı <strong>WPF</strong> 'le yapacağımız için 1 numaralı bölümden <strong>WPF</strong> 'i, 2 numaralı bölümden ise <strong>WPF Application</strong> 'u seçeriz. 3 numaralı bölümde <strong>Name</strong> kısmına uygulamamızın adını girip, <strong>Location</strong> bölümünden ise kayıt edeceğimiz yerin seçimini yapıyoruz ve <strong>OK</strong> butonuna basıyoruz.</span></p>
<p style="text-align:center;"><a href="/images/ders2-3.jpg"><img src="/images/ders2-3.jpg" alt="ders2-3" width="300" height="180" /></a></p>

&nbsp;
<p style="text-align:center;"><span style="color:#000000;">Şimdi karşımıza çıkan ekranı biraz inceleyelim.</span></p>

<p style="text-align:center;"><a href="/images/ders2-3.jpg"><img src="/images/ders2-3.jpg" alt="ders2-3" width="311" height="689" /></a></p>

<p style="text-align:justify;"><span style="color:#000000;">1 numaralı bölümde basit ve kullanışlı Araçlar menüsü, 2 numaralı bölümde Kontroller, Stiller gibi çeşitli bileşenlerin bulunduğu alan bulunmaktadır. 3 numaralı bölümde ise Form 'umuz ve onun üzerine yerleştirğimiz bileşenlerin listesi bulunur.</span></p>

<p style="text-align:center;"><a href="/images/ders2-7.jpg"><img class="aligncenter" src="/images/ders2-7.jpg" alt="ders2-7" width="504" height="443" /></a></p>
<p style="text-align:justify;"><span style="color:#000000;">Orta kısımdaki alanda üzerinde çalışacağımız form alanı bulunur. Bu form alanının görüntüsünü de okla işaret edilen bölümden değiştire biliriz. İşaretlerden ilkine tıkladığımızda ekranda sadece form, ikinsicine tıkladığımızda sadece XAML kodları, üçüncüsüne tıkladığımızda ise hem formumuz hem de XAML kodlarımız olacaktır.</span></p>
<p style="text-align:center;"><a href="/images/ders2-4.jpg"><img  src="/images/ders2-4.jpg" alt="ders2-4" width="283" height="675" /></a></p>

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Bu kısmın <strong>Properties</strong> tab menüsünde seçili olan bileşenin özellikleri, <strong>Projects</strong> tab menüsünde ise projemizi oluşturan dosya listesi bulunmaktadır.</span></p>
<p style="text-align:center;"><a href="/images/ders2-5.jpg"><img src="/images/ders2-5.jpg" alt="ders2-5" width="391" height="317" /></a></p>
<p style="text-align:justify;"><span style="color:#000000;">Blend 'de oluşturduğumuz bir projeyi çalıştırma istersek yukarıdaki menüden <strong>Project &gt; Run Project</strong> veya ona karışılık gelen <strong>F5 </strong>,<strong> Ctrl+F5</strong> tuşları kullanılır.</span></p>
<p style="text-align:left;"><span style="color:#000000;">Projemizi bu haliyle çalıştırdığımızda karşımıza klasik ve boş bir Windows form görüntüsü gelecektir.</span></p>
<p style="text-align:center;"><a href="/images/ders2-6.jpg"><img class="alignnone size-full wp-image-68" src="/images/ders2-6.jpg" alt="ders2-6" width="397" height="300" /></a></p>

<address style="text-align:justify;"><span style="color:#000000;">Fazla ayrıntıya girmeden Blend çalışma ortamını yüzeysel olarak tanımış olduk. Ayrıntılı özelliklerin bir kısmını diğer yazılarımda örnekler üzerinde anlatmaya çalışacağım bu şekilde o özelliklerin  kolay anlaşılır ve kalıcı olacağını düşünüyorum. Bu yazıyı burada sonlandırıyorum.</span></address><address style="text-align:justify;"><span style="color:#000000;">                    </span><span style="color:#000000;">Bir sonraki yazımda ise Metro stilinde bir arayüz tasarlamayı anlatmaya çalışacağım. Görüşmek üzere..</span></address><address style="text-align:justify;"> </address>

