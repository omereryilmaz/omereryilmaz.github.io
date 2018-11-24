---
layout: post
title: Webcam'den Çizgi İzleyen Robot
date: 2015-01-01 15:57
image: webcam_robo.png
comments: true
categories: [CSharp, PICBasic]
---
<p style="text-align:justify;">
Projede C# ve PicBasic kullanılmıştır. Robotta PIC 16F877 bulunmaktadır. Proje, manuel ve otomatik olmak üzere iki modda çalışmaktadır. Manuel olduğunda  WinForm üzerindeki butonlarla ve klavye tuşları yardımıyla robotun hareketi sağlanmaktadır. Otomatik modda ise robotun kamerasından alınan görüntü bilgisayarda işleme uğratılıyor ve çizginin ekrandaki koordinatına göre robota komutlar gönderiliyor.
</p>

<span style="color:#000000;">Projenin kodlarındaki önemli yerleri inceleyecek olursak ;</span>

<span style="color:#000000;">C# 'da görüntü işleme için AForge kütüphanesini kullandım.</span>

<p style="text-align:justify;">
<span style="color:#000000;">Robotla iletişimi portlar aracılığıyla yaptığımız için kullanacağımız portu ve frekansını tanımlıyoruz;</span>
</p>
<address><span style="color:#000000;">SerialPort sp = new SerialPort();</span></address><address><span style="color:#000000;"> sp.PortName = "COM2";</span>
<span style="color:#000000;"> sp.BaudRate = 9600;</span>
<span style="color:#000000;"> sp.Open();</span></address>&nbsp;
<br>

<span style="color:#000000;">Sonra görüntü işleme kodlarımıza geçiyoruz;</span>

<address><span style="color:#000000;"> Bitmap image1 = (Bitmap)eventArgs.Frame.Clone();</span>
<span style="color:#000000;"> pictureBox1.Image = image;</span></address><address><span style="color:#000000;">// Euclidean Color Filterin yapıldığı yer</span></address><address><span style="color:#000000;">EuclideanColorFiltering filter = new EuclideanColorFiltering();</span></address><address><span style="color:#000000;"> // Algılanacak renk belirleniyor ve orta noktası belirleniyor. </span>
<span style="color:#000000;"> filter.CenterColor = new RGB(Color.FromArgb(8, 47, 114));</span>
<span style="color:#000000;"> filter.Radius = 50;</span></address><address><span style="color:#000000;"> // filtre çalıştırılıyor</span>
<span style="color:#000000;"> filter.ApplyInPlace(image1);</span></address><address><span style="color:#000000;">//Görüntü üzerinde algilanan rengi cevrcevelemek veya hedeflemek icin gerekli Methodlar</span>
<span style="color:#000000;"> cevresiniciz(image1);</span></address>&nbsp;

<p style="text-align:justify;">
<span style="color:#000000;">Daha sonra cevresiniciz metodunun içinde çizilen dikdörtgenin değerlerine göre porta sp.Write(" "); ile komutlar gönderiyoruz.</span>
</p>
<address><span style="color:#000000;"> if (objectX &gt;= 350)</span>
<span style="color:#000000;"> { </span>
<span style="color:#000000;"> yonLabel.Text = "Saga";</span>
<span style="color:#000000;"> sp.Write("d");</span>
<span style="color:#000000;"> }</span>
<span style="color:#000000;"> else if (objectX &lt;= 200 )</span>
<span style="color:#000000;"> { </span>
<span style="color:#000000;"> yonLabel.Text = "Sola";</span>
<span style="color:#000000;"> sp.Write("a");</span>
<span style="color:#000000;"> }</span>
<span style="color:#000000;"> //if (objectX &lt; 480 &amp;&amp; objectX &gt; 430)</span>
<span style="color:#000000;"> else</span>
<span style="color:#000000;"> { </span>
<span style="color:#000000;"> yonLabel.Text = "Ileri";</span>
<span style="color:#000000;"> sp.Write("w");</span>
<span style="color:#000000;"> }</span></address>&nbsp;
<br>
<p style="text-align:justify;"><span style="color:#000000;">PicBasic kısmında ise porta gönderilen komutu  Hserin 100,t1,[STR i1] yardımıyla alıyoruz. Bu komutun anlamı 100 milisaniye içinde cevap gelmezse t1 labeline git, cevap gelirse porttan gelen karakteri i değişkenine at. i değişkenine atılan karaktere göre de select case yardımıyla robotun ne yapacağını belirliyoruz. </span></p>
<p style="text-align:justify;"><span style="color:#000000;">Bu kısımdaki önemli ve anlaşılması zor olabilecek kısım ise PWM komutu olabilir. O komutun amacı ise robottaki motorların torkunu ayarlamaktır. </span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Kontrol Paneli (winform) :</strong></span></p>

<p style="text-align:center;">
<img src="/images/webcam_robo1.jpg" />
</p>
<br>
<p style="text-align:justify;"><span style="color:#000000;"><strong>Projenin Videosu :</strong></span></p>
<p style="text-align:center;"><iframe width="560" height="315" src="https://www.youtube.com/embed/CGDvk_nTW5k" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe></p>
&nbsp;

<strong><span style="color:#000000;">Projenin Kaynak Kodları :</span></strong>
<a href="https://github.com/omereryilmaz/Webcam-den-Cizgi-Takip-Eden-Robot" target="_blank"><span style="color:#008080;"><strong>https://github.com/omereryilmaz/Webcam-den-Cizgi-Takip-Eden-Robot</strong></span></a>
