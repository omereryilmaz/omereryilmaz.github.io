---
layout: post
title: Windows Phone WCF Kullanımı
date: 2014-04-23 23:30
image: wcf0.jpg
comments: true
categories: [WCF, WindowsPhone]
---
<p style="text-align:center;">
    <img src="/images/wcf0.jpg" />
</p>

<span style="color:#000000;"><strong>WCF nedir ?</strong></span>
<p style="text-align:justify;"><span style="color:#000000;">WCF (Windows Communication Foundation) Microsoft 'un servis yönelimli mimari için geliştirmiş olduğu bir framework 'tür. Kendi içerisinde kütüphaneler bulunur. Bu kütüphaneler yardımıyla servisler yazılabilir ve bu kütüphaneler kullanarak servis yönelimli mimari yazılımları geliştirmemize olanak sağlar.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Windows uygulamamızda uzaktaki bir sunucudan bir veri çekeceksek WCF kullanmamız gerekir.  Aynı şey Microsoft Sql Server 'daki veritabanımıza bağlanmak içinde geçerli. Fakat çoğu zaman bu bağlantıyı oluştururken sistemimizdeki ayarlar yüzünden bağlantı problemleri yaşanabiliyor.  Bu yazımızda karşılaştığım bir hatanın çözümüyle birlikte bir örnek üzerinde WCF kullanarak veritabanımızdaki verileri listelemeye çalışacağız.</span></p>
<span style="color:#000000;">Visual Studio 'yu <strong>Yönetici Olarak</strong> çalıştırıyoruz daha sonra</span>

<strong><span style="color:#000000;">File &gt; New &gt; Project</span></strong>

<p style="text-align:center;">
    <img src="/images/wcf1.jpg" />
</p>
<br><br>

<p style="text-align:justify;">
    <span style="color:#000000;">
        <strong>WCF &gt; WCF Service Application</strong> 'u seçip isimlendirmemizi kendimize göre yapıp, <strong>OK</strong> butonuna tıklıyoruz.
    </span>
</p>

<p style="text-align:justify;">
    <span style="color:#000000;">
    <strong>Solution Explorer</strong> 'daki <strong>IService.cs</strong> ve <strong>Service.svc</strong> dosyalarını siliyoruz.
    </span>
</p>

<p style="text-align:justify;">
    <span style="color:#000000;">
        Solution Explorer 'daki oluşturduğumuz WCF 'e (Ben WcfOmer ismini vermiştim)sağ tıklıyoruz, <strong>Add &gt; New Item</strong> diyoruz. Karşımıza gelen pencereden <strong>Data &gt; LINQ to SQL Classes</strong> ı seçip <strong>Name</strong> kısmınıda sınıfımızın ismini veriyoruz (TakimlarClases ismini verdim.) Add butonuna tıklıyoruz.
    </span>
</p>

<p style="text-align:center;">
    <img src="/images/wcf2.jpg"/>
</p>
<br><br>

<p style="text-align:justify;">
    <span style="color:#000000;">
        Server Explorer 'dan daha önce oluşturduğumuz database 'e tıklıyoruz. Eğer database 'imiz görünmüyorsa <strong>Connect to Database</strong> simgesine tıklarız.
    </span>
</p>

<p style="text-align:center;">
    <img src="/images/wcf3.jpg"/>
</p>
<br><br>

<p style="text-align:justify;"><span style="color:#000000;">Karşımıza çıkan <strong>Add Connection</strong> penceresinde <strong>Server name</strong> kısmına <strong>bilgisayarımızın ismini</strong>, <strong>Select or enter a database name</strong> kısmında ise kullanacağımız database 'i seçip<strong> OK</strong> 'e basıyoruz. Bu andan itibaren Server Explorer kısmında databaseimiz görünmüş olacak. Database 'in yanındaki küçük üçgene tıklayıp tablomuzu sürükleyerek resimdeki yere bırakıyoruz.</span></p>

<p style="text-align:center;">
    <img src="/images/wcf4.jpg" />
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Bundan sonraki aşamada ise wcf servisimizi ekleyeceğiz. Bunun için;</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Solution Explorer 'daki uygulamamızın üstünde sağ tıklayıp <strong>Add &gt; New Item &gt; Viusal C# &gt; WCF Service</strong></span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;"><strong>Name</strong> kısmına servisimizin ismini yazıp <strong>Add</strong> butonuna tıklıyoruz.</span>
</p>

<p style="text-align:center;">
    <img src="/images/wcf5.jpg"/>
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Karşımıza gelen interface sayfasında bendeki ismi <strong>ITakimService1.cs</strong> 'indeki kısmı şu şekilde değiştiriyoruz.</span>
</p>



<pre>
    <code>
        public interface ITakimService1
        {
        [OperationContract]
        List&lt;takimlar&gt; GetTumTakimlar();
        }
    </code>    
</pre>




<p style="text-align:justify;">
<span style="color:#000000;">&lt;&gt; bu aralığa tablomuzun ismini yazıp kaydediyoruz.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Sonra  Solution Explorer daki <strong>*.svc.cs</strong> dosyasına çift tıklayıp onda da şu değişiklikleri yapıyoruz.</span>
</p>

<p style="text-align:center;">
<img src="/images/wcf6.jpg" />
</p>
<br><br>

<pre>
    <code>
        public class TakimService1 : ITakimService1
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

        }
    </code>
</pre>
<br><br>

<p style="text-align:justify;"><span style="color:#000000;">Burada interface 'imizi implement edip tablodaki verilerimizi liste şeklinde döndürdük. Bu işlemi yaptıktan sonra kayıt edip Solution Explorer 'daki servis uygulamamıza sağ tıklayıp Build ederek herhangi bir hata olup olmadığını kontrol ediyoruz.</span></p>
&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Şimdi de oluşturduğumuz servisi phone uygulamamızla ilişkilendirmek için phone application ekliyoruz. Bunun için  Solution Explorer 'a sağ tıklayıp <strong>Add &gt; New Project</strong>..</span></p>

<p style="text-align:center;">
<img src="/images/wcf7.jpg"/>
</p>
<br><br>
<p style="text-align:justify;">
<span style="color:#000000;"><strong>Visual C# &gt;Windows Phone App</strong> deyip Name kısmında ismini belirledikten sonra <strong>OK</strong> butonuna tıklıyoruz..</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Şimdi ise oluşturduğumuz Phone App 'a Servisimizi ekleyelim, bunun için;</span>

<span style="color:#000000;">Solution Explorer 'da <strong>Refereces</strong> 'e sağ tıklayıp <strong>Add Service Reference</strong> 'ye tıklıyoruz.</span>
</p>

<p style="text-align:center;">
<img src="/images/wcf8.jpg"/>
</p>
<br><br>
<p style="text-align:justify;"><span style="color:#000000;">Karşımıza çıkan pencerede <strong>Discover </strong>(koyu kırmızı işaretli) butonuna tıklayıp oluşturduğumuz servisin gelmesini sağlarız. Servisimiz gelince <strong>Go</strong> butonuyla servisimizi çalıştırırız. Namespace kısmında servimize oluşturacağımız referansın ismini verip <strong>OK</strong> e tıklarız.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Artık veritabanımızdaki verilerileri rahattlıklar çekebiliriz. Şimdi ise verilerimizin görüntüleneceğin bileşenlerin bağlanması işlemini gerçekleştirelim. Bunun için Solution Explorer 'da <strong>*.xaml</strong> uzantılı dosyamızı(MainPage.xaml) açıyoruz.</span></p>

<span style="color:#000000;">&lt;phone:PhoneApplicationPage</span>

<span style="color:#000000;">..</span>

<span style="color:#000000;">&gt;</span>

<span style="color:#000000;">kısmının hemen ardına <strong>DataTemplate</strong> 'ımızı oluşturuyoruz..</span>


<pre>&lt;phone:PhoneApplicationPage.Resources&gt;
&lt;DataTemplate x:Key="StudentDataTemplate"&gt;
&lt;StackPanel Orientation="Horizontal"&gt;
&lt;TextBlock Margin="10" Text="{Binding id}"&gt;&lt;/TextBlock&gt;
&lt;TextBlock Margin="10" Text="{Binding takimad}"&gt;&lt;/TextBlock&gt;
&lt;/StackPanel&gt;
&lt;/DataTemplate&gt;
&lt;/phone:PhoneApplicationPage.Resources&gt;</pre>

<br><br>
<span style="color:#000000;">Listeleme yapacağımız listbox 'ı da <strong>Content Panel</strong> isimli <strong>Grid</strong> 'imizin içinde oluşturuyoruz.</span>


<pre>&lt;ListBox x:Name="listbox1" ItemsSource="{Binding}" ItemTemplate="{StaticResource StudentDataTemplate}" HorizontalAlignment="Center" Width="460" Margin="-2,108,-2,95" /&gt;</pre>

<br><br>
<span style="color:#000000;">Burada dikkat etmemiz gereken önemli yer <strong>ItemTemplate</strong> kısmının oluşturduğumuz <strong>datatemplate</strong> nin <span style="text-decoration:underline;">ismiyle aynı</span> olmasıdır.</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Verilerimizi uygulamamız yüklendiği anda listeletmek istiyoruz. Bunun için;</span>

<span style="color:#000000;">Solution Explorer dan <strong>MainPage.xaml.cs</strong> dosyasına çift tıklarız.</span>

<hr />


<pre>private void PhoneApplicationPage_Loaded(object sender, RoutedEventArgs e)
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

<span style="color:#000000;"><em>Additional information: The remote server returned ad error: Not found.</em>
<p style="text-align:center;">
    <img src="/images/wcf9.jpg"/>
</p>
<br><br>

<p style="text-align:justify;"><span style="color:#000000;">Bu hatanın sebebi Windows Phone için localhost un hiçbirşey ifade etmemesi ve dolayısıyla veritabanımızı bulamamasıdır. Çözümü ise localhost yerine ip adresimizle bağlantıyı sağlamak. Tabi bunun için de şu adımları uygulamamız gerekiyor.</span></p>
<p style="text-align:justify;"><span style="color:#000000;">Windows ayarlarımız resimdeki gibi olmalıdır. Bu ayarı yapabilmek için <strong>Denetim Masası &gt; Programlar ve Özellikler</strong>den sol taraftan <strong>Windows özelliklerini aç veya kapat</strong> 'ı tıklarız.</span></p>

<p style="text-align:center;">
    <img src="/images/wcf10winozellikler.jpg"/>
</p>
<br><br>

<span style="color:#000000;">Diğer adımda ise servisimizin kullandığı portu özel olarak açmamız gerekiyor. Bunun için ;</span>

<span style="color:#000000;"><strong>Denetim Masası &gt; Tüm Denetim Masası Öğeleri &gt; Windows Güvenlik Duvarı</strong> sol taraftan <strong>Gelişmiş Ayarlar</strong>a tıklarız.</span>

<p style="text-align:center;">
    <img src="/images/wcf11portacma1.jpg"/>
</p>
<br><br>

<p style="text-align:justify;"><span style="color:#000000;">Karşımıza gelen pencerede<strong> Gelen Kurallar</strong>ı daha sonra da sağ taraftan <strong>Yeni Kural..</strong> a tıklayıp yeni kuralımızı port numaramızı ekleyerek oluştururuz.</span></p>

<p style="text-align:center;">
    <img src="/images/wcf11portacma2.jpg"/>
</p>
<br><br>

<span style="color:#000000;">Bağlantı noktasını<strong> TCP veya UDP</strong> olarak seçip İleri deriz.</span>

<p style="text-align:center;">
    <img src="/images/wcf11portacma3.jpg"/>
</p>
<br><br>


<span style="color:#000000;">Servisimizin kullandığı port numarasını yazarak İleri deriz.</span>

<span style="color:#000000;"> </span>

<span style="color:#000000;">Servisimizin kullandığı port numarasını öğrenmek için ;</span>

<span style="color:#000000;">Solution Explorer 'daki oluşturduğumuz servise sağ tıklayıp <strong>Properties</strong> 'e tıklarız.</span>

<p style="text-align:center;">
    <img src="/images/wcf12portogrenme.jpg"/>
</p>
<br><br>

<p style="text-align:justify;"><span style="color:#000000;">Sol taraftaki menüden <strong>Web</strong> 'i seçeriz, <strong>Project Url</strong> Kısmında localhosttan sonra yazan port numaramızdır. Onu kopyalayıp Port açma kısmındaki yere yapıştırırız. <strong>İleri</strong> deriz. Sonraki pencerede de<strong> bağlantıya izin ver</strong> deyip <strong>İleri</strong> tıklarız.</span></p>


<p style="text-align:center;">
    <img src="/images/wcf12portacma4.jpg"/>
</p>
<br><br>


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

<br><br>

<span style="color:#000000;">servisimizin olduğu kısmı bulup ip adresimizle bağlantı kurabilmesi için koyu renkli satırı ekliyoruz.</span>

<span style="color:#000000;">ip adresini öğrenmek için ;</span>

<span style="color:#000000;"><strong>Ağ ve Paylaşım Merkezini</strong> açarız karşımıza gelen pencereden</span>

<p style="text-align:center;">
    <img src="/images/wcf13ipogrenme.jpg"/>
</p>
<br><br>

<span style="color:#000000;">Windows phone emulatör'ü tıklarız gelen pencereden ayrıntılara tıklarız. Buradaki <strong>Otomatik Yapılandırma IPv4</strong>  ip si.</span>

<span style="color:#000000;">Aynı ip adresimizi Servisimizin <strong> Project Url</strong> Kısmında <strong>localhost</strong> kısmının yerine yazarız.</span>

<p style="text-align:center;">
    <img src="/images/wcf14.jpg"/>
</p>
<br><br>


<span style="color:#000000;"><strong>Create Virtual Directory</strong> butonuna tıklarız.</span>

<span style="color:#000000;">Bu işlemi yaptıktan sonra localhost adresimizle oluşturduğumuz servisimizi iptal edip yerine ip adresimizle iletişime geçecek servisimizi tanımlarız.</span>

<p style="text-align:center;">
    <img src="/images/wcf15servissilme.jpg"/>
</p>
<br><br>

<p style="text-align:center;"><span style="color:#000000;"><strong>References &gt; Add Service Reference</strong></span></p>

<p style="text-align:center;">
    <img src="/images/wcf16.jpg"/>
</p>
<br><br>


&nbsp;
<p style="text-align:justify;"><span style="color:#000000;">Servis referansımızı ip adresimizle oluşturuyoruz. Eğer bu aşamada <strong>Go</strong> butonuna bastığınızda herhangi bir hata alıyorsanız servislerinizi ve visual studio 'yu kapatıp <strong>yönetici olarak tekrar çalışıtırınız</strong>.</span></p>
<p style="text-align:justify;"><span style="color:#000000;"><strong>F5</strong> e basıp uygulamamızı çalıştırdığımızda verilerimizin listelendiğini görebilirsiniz.</span></p>

<p style="text-align:center;">
    <img src="/images/wcf17.jpg"/>
</p>

