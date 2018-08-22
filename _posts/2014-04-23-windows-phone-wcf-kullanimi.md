---
layout: post
title: Windows Phone WCF Kullanımı
date: 2014-04-23 23:30
image: wcf0.jpg
comments: true
categories: [WCF, WindowsPhone]
---
<a href="/images/wcf0.jpg"><img class="size-full wp-image-148 aligncenter" src="/images/wcf0.jpg" alt="wcf0" width="400" height="400" /></a>

<span style="color:#000000;"><strong>WCF nedir ?</strong></span>
<p style="text-align:justify;"><span style="color:#000000;">WCF (Windows Communication Foundation) Microsoft 'un servis yönelimli mimari için geliştirmiş olduğu bir framework 'tür. Kendi içerisinde kütüphaneler bulunur. Bu kütüphaneler yardımıyla servisler yazılabilir ve bu kütüphaneler kullanarak servis yönelimli mimari yazılımları geliştirmemize olanak sağlar.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Windows uygulamamızda uzaktaki bir sunucudan bir veri çekeceksek WCF kullanmamız gerekir.  Aynı şey Microsoft Sql Server 'daki veritabanımıza bağlanmak içinde geçerli. Fakat çoğu zaman bu bağlantıyı oluştururken sistemimizdeki ayarlar yüzünden bağlantı problemleri yaşanabiliyor.  Bu yazımızda karşılaştığım bir hatanın çözümüyle birlikte bir örnek üzerinde WCF kullanarak veritabanımızdaki verileri listelemeye çalışacağız.</span></p>
<span style="color:#000000;">Visual Studio 'yu <strong>Yönetici Olarak</strong> çalıştırıyoruz daha sonra</span>

<strong><span style="color:#000000;">File &gt; New &gt; Project</span></strong>

[caption id="attachment_149" align="aligncenter" width="300"]<a href="/images/wcf1.jpg"><img class="size-medium wp-image-149" src="/images/wcf1-300x183.jpg" alt="Resmi büyütmek için tıklayın." width="300" height="183" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;

<span style="color:#000000;"><strong>WCF &gt; WCF Service Application</strong> 'u seçip isimlendirmemizi kendimize göre yapıp, <strong>OK</strong> butonuna tıklıyoruz.</span>

<span style="color:#000000;"><strong>Solution Explorer</strong> 'daki <strong>IService.cs</strong> ve <strong>Service.svc</strong> dosyalarını siliyoruz.</span>
<p style="text-align:justify;"><span style="color:#000000;">Solution Explorer 'daki oluşturduğumuz WCF 'e (Ben WcfOmer ismini vermiştim)sağ tıklıyoruz, <strong>Add &gt; New Item</strong> diyoruz. Karşımıza gelen pencereden <strong>Data &gt; LINQ to SQL Classes</strong> ı seçip <strong>Name</strong> kısmınıda sınıfımızın ismini veriyoruz (TakimlarClases ismini verdim.) Add butonuna tıklıyoruz.</span></p>


[caption id="attachment_150" align="aligncenter" width="300"]<a href="/images/wcf2.jpg"><img class="size-medium wp-image-150" src="/images/wcf2-300x182.jpg" alt="Resmi büyütmek için tıklayın." width="300" height="182" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;

<span style="color:#000000;">Server Explorer 'dan daha önce oluşturduğumuz database 'e tıklıyoruz. Eğer database 'imiz görünmüyorsa <strong>Connect to Database</strong> simgesine tıklarız.</span>

[caption id="attachment_151" align="aligncenter" width="300"]<a href="/images/wcf3.jpg"><img class="size-medium wp-image-151" src="/images/wcf3-300x257.jpg" alt="r" width="300" height="257" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Karşımıza çıkan <strong>Add Connection</strong> penceresinde <strong>Server name</strong> kısmına <strong>bilgisayarımızın ismini</strong>, <strong>Select or enter a database name</strong> kısmında ise kullanacağımız database 'i seçip<strong> OK</strong> 'e basıyoruz. Bu andan itibaren Server Explorer kısmında databaseimiz görünmüş olacak. Database 'in yanındaki küçük üçgene tıklayıp tablomuzu sürükleyerek resimdeki yere bırakıyoruz.</span></p>


[caption id="attachment_152" align="aligncenter" width="300"]<a href="/images/wcf4.jpg"><img class="size-medium wp-image-152" src="/images/wcf4-300x183.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="183" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;

<span style="color:#000000;">Bundan sonraki aşamada ise wcf servisimizi ekleyeceğiz. Bunun için;</span>

<span style="color:#000000;">Solution Explorer 'daki uygulamamızın üstünde sağ tıklayıp <strong>Add &gt; New Item &gt; Viusal C# &gt; WCF Service</strong></span>

<span style="color:#000000;"><strong>Name</strong> kısmına servisimizin ismini yazıp <strong>Add</strong> butonuna tıklıyoruz.</span>

[caption id="attachment_153" align="aligncenter" width="300"]<a href="/images/wcf5.jpg"><img class="size-medium wp-image-153" src="/images/wcf5-300x183.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="183" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;

<span style="color:#000000;">Karşımıza gelen interface sayfasında bendeki ismi <strong>ITakimService1.cs</strong> 'indeki kısmı şu şekilde değiştiriyoruz.</span>

&nbsp;
<pre class="lang:c# decode:true">public interface ITakimService1
{
[OperationContract]
List&lt;takimlar&gt; GetTumTakimlar();
}</pre>
&nbsp;

&nbsp;

<span style="color:#000000;">&lt;&gt; bu aralığa tablomuzun ismini yazıp kaydediyoruz.</span>

<span style="color:#000000;">Sonra  Solution Explorer daki <strong>*.svc.cs</strong> dosyasına çift tıklayıp onda da şu değişiklikleri yapıyoruz.</span>

<a href="/images/wcf6.jpg"><img class="size-medium wp-image-154 aligncenter" src="/images/wcf6-300x266.jpg" alt="wcf6" width="300" height="266" /></a>

&nbsp;

&nbsp;
<blockquote>
<pre class="lang:c# decode:true ">public class TakimService1 : ITakimService1
{
public TakimlarClassesDataContext Data { set; get; }
public TakimService1()
{
Data = new TakimlarClassesDataContext();
}
public List&lt;takimlar&gt; GetTumTakimlar()
{
return Data.takimlars.ToList();
}

}</pre>
&nbsp;</blockquote>
&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Burada interface 'imizi implement edip tablodaki verilerimizi liste şeklinde döndürdük. Bu işlemi yaptıktan sonra kayıt edip Solution Explorer 'daki servis uygulamamıza sağ tıklayıp Build ederek herhangi bir hata olup olmadığını kontrol ediyoruz.</span></p>
&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Şimdi de oluşturduğumuz servisi phone uygulamamızla ilişkilendirmek için phone application ekliyoruz. Bunun için  Solution Explorer 'a sağ tıklayıp <strong>Add &gt; New Project</strong>..</span></p>


[caption id="attachment_155" align="aligncenter" width="300"]<a href="/images/wcf7.jpg"><img class="size-medium wp-image-155" src="/images/wcf7-300x182.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="182" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;"><strong>Visual C# &gt;Windows Phone App</strong> deyip Name kısmında ismini belirledikten sonra <strong>OK</strong> butonuna tıklıyoruz..</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Şimdi ise oluşturduğumuz Phone App 'a Servisimizi ekleyelim, bunun için;</span>

<span style="color:#000000;">Solution Explorer 'da <strong>Refereces</strong> 'e sağ tıklayıp <strong>Add Service Reference</strong> 'ye tıklıyoruz.</span>

[caption id="attachment_156" align="aligncenter" width="300"]<a href="/images/wcf8.jpg"><img class="size-medium wp-image-156" src="/images/wcf8-300x242.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="242" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]
<p style="text-align:justify;"><span style="color:#000000;">Karşımıza çıkan pencerede <strong>Discover </strong>(koyu kırmızı işaretli) butonuna tıklayıp oluşturduğumuz servisin gelmesini sağlarız. Servisimiz gelince <strong>Go</strong> butonuyla servisimizi çalıştırırız. Namespace kısmında servimize oluşturacağımız referansın ismini verip <strong>OK</strong> e tıklarız.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Artık veritabanımızdaki verilerileri rahattlıklar çekebiliriz. Şimdi ise verilerimizin görüntüleneceğin bileşenlerin bağlanması işlemini gerçekleştirelim. Bunun için Solution Explorer 'da <strong>*.xaml</strong> uzantılı dosyamızı(MainPage.xaml) açıyoruz.</span></p>
<span style="color:#000000;">&lt;phone:PhoneApplicationPage</span>

<span style="color:#000000;">..</span>

<span style="color:#000000;">&gt;</span>

<span style="color:#000000;">kısmının hemen ardına <strong>DataTemplate</strong> 'ımızı oluşturuyoruz..</span>

&nbsp;
<pre class="lang:c# decode:true">&lt;phone:PhoneApplicationPage.Resources&gt;
&lt;DataTemplate x:Key="StudentDataTemplate"&gt;
&lt;StackPanel Orientation="Horizontal"&gt;
&lt;TextBlock Margin="10" Text="{Binding id}"&gt;&lt;/TextBlock&gt;
&lt;TextBlock Margin="10" Text="{Binding takimad}"&gt;&lt;/TextBlock&gt;
&lt;/StackPanel&gt;
&lt;/DataTemplate&gt;
&lt;/phone:PhoneApplicationPage.Resources&gt;</pre>
&nbsp;

<span style="color:#000000;">Listeleme yapacağımız listbox 'ı da <strong>Content Panel</strong> isimli <strong>Grid</strong> 'imizin içinde oluşturuyoruz.</span>

&nbsp;
<pre class="lang:js decode:true ">&lt;ListBox x:Name="listbox1" ItemsSource="{Binding}" ItemTemplate="{StaticResource StudentDataTemplate}" HorizontalAlignment="Center" Width="460" Margin="-2,108,-2,95" /&gt;</pre>
<span style="color:#000000;">Burada dikkat etmemiz gereken önemli yer <strong>ItemTemplate</strong> kısmının oluşturduğumuz <strong>datatemplate</strong> nin <span style="text-decoration:underline;">ismiyle aynı</span> olmasıdır.</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Verilerimizi uygulamamız yüklendiği anda listeletmek istiyoruz. Bunun için;</span>

<span style="color:#000000;">Solution Explorer dan <strong>MainPage.xaml.cs</strong> dosyasına çift tıklarız.</span>

<hr />

&nbsp;
<pre class="lang:c# decode:true">private void PhoneApplicationPage_Loaded(object sender, RoutedEventArgs e)
{
TakimServiceReference1.TakimService1Client servisclient = new TakimServiceReference1.TakimService1Client();
servisclient.GetTumTakimlarCompleted += servisclient_GetTumTakimlarCompleted;
servisclient.GetTumTakimlarAsync();
}

void servisclient_GetTumTakimlarCompleted(object sender, TakimServiceReference1.GetTumTakimlarCompletedEventArgs e)
{
if (e.Result != null) {
listbox1.ItemsSource = e.Result;
}
}</pre>
&nbsp;

<hr />

&nbsp;

<span style="color:#000000;">Bu kodu ekleriz. Artık uygulamamız hazır ama bu şekilde çalıştırırsak şöyle bir hatayla karşılaşırız.</span>

<span style="color:#000000;"><em>CommunicationException was unhandled by user code başlığı altında An exception of type 'System.ServiceModel. CommunicationException' occurred in System.ServiceModel.ni.dll but was not handled in user code</em></span>

<span style="color:#000000;"><em>Additional information: The remote server returned ad error: Not found.</em></span><a href="/images/wcf9wcferrornotfound.jpg"><img class="size-full wp-image-157 aligncenter" src="/images/wcf9wcferrornotfound.jpg" alt="wcf9WcfErrorNotFound" width="565" height="429" /></a>
<p style="text-align:justify;"><span style="color:#000000;">Bu hatanın sebebi Windows Phone için localhost un hiçbirşey ifade etmemesi ve dolayısıyla veritabanımızı bulamamasıdır. Çözümü ise localhost yerine ip adresimizle bağlantıyı sağlamak. Tabi bunun için de şu adımları uygulamamız gerekiyor.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Windows ayarlarımız resimdeki gibi olmalıdır. Bu ayarı yapabilmek için <strong>Denetim Masası &gt; Programlar ve Özellikler</strong>den sol taraftan <strong>Windows özelliklerini aç veya kapat</strong> 'ı tıklarız.</span></p>
<p style="text-align:justify;"><a href="/images/wcf10winc3b6zellikler.jpg"><img class="alignnone size-full wp-image-158" src="/images/wcf10winc3b6zellikler.jpg" alt="wcf10winözellikler" width="875" height="463" /></a></p>
&nbsp;

<span style="color:#000000;">Diğer adımda ise servisimizin kullandığı portu özel olarak açmamız gerekiyor. Bunun için ;</span>

<span style="color:#000000;"><strong>Denetim Masası &gt; Tüm Denetim Masası Öğeleri &gt; Windows Güvenlik Duvarı</strong> sol taraftan <strong>Gelişmiş Ayarlar</strong>a tıklarız.</span>

[caption id="attachment_159" align="aligncenter" width="300"]<a href="/images/wcf11portacma1.jpg"><img class="size-medium wp-image-159" src="/images/wcf11portacma1-300x129.jpg" alt="Resmi büyütmek için tıklayın." width="300" height="129" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]
<p style="text-align:justify;"><span style="color:#000000;">Karşımıza gelen pencerede<strong> Gelen Kurallar</strong>ı daha sonra da sağ taraftan <strong>Yeni Kural..</strong> a tıklayıp yeni kuralımızı port numaramızı ekleyerek oluştururuz.</span></p>


[caption id="attachment_160" align="aligncenter" width="300"]<a href="/images/wcf11portacma2.jpg"><img class="size-medium wp-image-160" src="/images/wcf11portacma2-300x241.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="241" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;">Bağlantı noktasını<strong> TCP veya UDP</strong> olarak seçip İleri deriz.</span>

&nbsp;

[caption id="attachment_161" align="aligncenter" width="300"]<a href="/images/wcf11portacma3.jpg"><img class="size-medium wp-image-161" src="/images/wcf11portacma3-300x243.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="243" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;">Servisimizin kullandığı port numarasını yazarak İleri deriz.</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Servisimizin kullandığı port numarasını öğrenmek için ;</span>

<span style="color:#000000;">Solution Explorer 'daki oluşturduğumuz servise sağ tıklayıp <strong>Properties</strong> 'e tıklarız.</span>

[caption id="attachment_163" align="aligncenter" width="300"]<a href="/images/wcf12portogrenme.jpg"><img class="size-medium wp-image-163" src="/images/wcf12portogrenme-300x134.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="134" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]
<p style="text-align:justify;"><span style="color:#000000;">Sol taraftaki menüden <strong>Web</strong> 'i seçeriz, <strong>Project Url</strong> Kısmında localhosttan sonra yazan port numaramızdır. Onu kopyalayıp Port açma kısmındaki yere yapıştırırız. <strong>İleri</strong> deriz. Sonraki pencerede de<strong> bağlantıya izin ver</strong> deyip <strong>İleri</strong> tıklarız.</span></p>


[caption id="attachment_162" align="aligncenter" width="300"]<a href="/images/wcf12portacma4.jpg"><img class="size-medium wp-image-162" src="/images/wcf12portacma4-300x243.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="243" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;">Burada Özel seçeneğini seçip İleri deriz. Sonraki pencerede Kuralımızın adını verip <strong>SON</strong> a tıklarız. Şuan portumuzu açtık ve gelen isteklere cevap vermesini sağladık.</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Şimdi de servisimizin ip adresimizi görmesini sağlamak için  <strong>IIExpress</strong> 'in <strong>config</strong> dosyasında bazı eklemeleri yapmamız gerekiyor.</span>

<span style="color:#000000;"><em>C:UsersKullanıcıİsminizDocumentsIISExpressconfig</em></span>

<span style="color:#000000;">adresindeki <strong>applicationhost</strong> isimli text dosyasını açarız.</span>

<hr />

&nbsp;

&lt;site name="WcfOmer(1)" id="7"&gt;

&lt;application path="/" applicationPool="Clr4IntegratedAppPool"&gt;

&lt;virtualDirectory path="/" physicalPath="D:3.Sınıf - 2Bahar1-İleri Veri TabanıAlbumOrnekWcfOmerWpWcfOmer" /&gt;

&lt;/application&gt;

&lt;bindings&gt;

&lt;binding protocol="http" bindingInformation="*:58042:localhost" /&gt;

<strong>                   &lt;binding protocol="http" bindingInformation="*:58042:ipadresiniz" /&gt;</strong>

&lt;/bindings&gt;

&lt;/site&gt;

<hr />

&nbsp;

&nbsp;

<span style="color:#000000;">servisimizin olduğu kısmı bulup ip adresimizle bağlantı kurabilmesi için koyu renkli satırı ekliyoruz.</span>

<span style="color:#000000;">ip adresini öğrenmek için ;</span>

<span style="color:#000000;"><strong>Ağ ve Paylaşım Merkezini</strong> açarız karşımıza gelen pencereden</span>

[caption id="attachment_164" align="aligncenter" width="300"]<a href="/images/wcf13ipogrenme.jpg"><img class="size-medium wp-image-164" src="/images/wcf13ipogrenme-300x112.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="112" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;">Windows phone emulatör'ü tıklarız gelen pencereden ayrıntılara tıklarız. Buradaki <strong>Otomatik Yapılandırma IPv4</strong>  ip si.</span>

<span style="color:#000000;">Aynı ip adresimizi Servisimizin <strong> Project Url</strong> Kısmında <strong>localhost</strong> kısmının yerine yazarız.</span>

&nbsp;

[caption id="attachment_165" align="aligncenter" width="300"]<a href="/images/wcf14.jpg"><img class="size-medium wp-image-165" src="/images/wcf14-300x120.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="120" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

<span style="color:#000000;"><strong>Create Virtual Directory</strong> butonuna tıklarız.</span>

<span style="color:#000000;">Bu işlemi yaptıktan sonra localhost adresimizle oluşturduğumuz servisimizi iptal edip yerine ip adresimizle iletişime geçecek servisimizi tanımlarız.</span>

<a href="/images/wcf15servissilme.jpg"><img class="size-medium wp-image-166 aligncenter" src="/images/wcf15servissilme-300x252.jpg" alt="wcf15servissilme" width="300" height="252" /></a>

&nbsp;

&nbsp;
<p style="text-align:center;"><span style="color:#000000;"><strong>References &gt; Add Service Reference</strong></span></p>


[caption id="attachment_167" align="aligncenter" width="300"]<a href="/images/wcf16.jpg"><img class="size-medium wp-image-167" src="/images/wcf16-300x242.jpg" alt="Resmi büyütmek için üzerine tıklayın." width="300" height="242" /></a> Resmi büyütmek için üzerine tıklayın.[/caption]

&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Servis referansımızı ip adresimizle oluşturuyoruz. Eğer bu aşamada <strong>Go</strong> butonuna bastığınızda herhangi bir hata alıyorsanız servislerinizi ve visual studio 'yu kapatıp <strong>yönetici olarak tekrar çalışıtırınız</strong>.</span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>F5</strong> e basıp uygulamamızı çalıştırdığımızda verilerimizin listelendiğini görebilirsiniz.</span></p>
<a href="/images/wcf17.jpg"><img class="size-full wp-image-168 aligncenter" src="/images/wcf17.jpg" alt="wcf17" width="371" height="615" /></a>
