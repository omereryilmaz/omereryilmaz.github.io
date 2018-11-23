---
layout: post
title: Microsoft Azure Mobile Services Nasıl Oluşturulur?
date: 2016-01-24 16:47
image: Mobileappolusturmak.jpg
comments: true
categories: [MicrosoftAzure, WindowsPhone]
---
<p style="text-align:justify;">
	<span style="color:#000000;">
		Bir önceki yazımızda <a style="color:#000000;" href="/azure-mobile-services-nedir/" target="_blank">Azure Mobil Service (Mobil Hizmet)</a>’in ne olduğuna değinmiştik. Bu yazımızda ise Mobil Hizmet’in oluşturulması ve kullanılmasını göreceğiz.
	</span>
</p>

<p style="text-align:justify;">
	<span style="color:#000000;">
		Öncelikle bu yazıdaki örneği uygulamak için Microsoft Azure hesabınız olması gerekmektedir. Burada Mobile Service oluşturup daha sonra da bu servis için oluşturulmuş örneğini de Visual Studio ile incelemeye çalışacağız.
	</span>
</p>

<p style="text-align:justify;">
	<span style="color:#000000;">Eğer bir Azure hesabınız varsa <a style="color:#000000;" href="https://manage.windowsazure.com">https://manage.windowsazure.com</a> adresinden girip işleme başlıyoruz.
	</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Karşınıza şekildeki gibi bir ekran çıkacak;</span>
</p>

<p style="text-align:center;">
    <img src="/images/mobilservices1.png"/>
</p>
<br>



<p style="text-align:justify;">
<span style="color:#000000;">Yeni Azure portalını kullanmak istiyorsak; <a style="color:#000000;" href="https://portal.azure.com">https://portal.azure.com</a> adresini kullanabiliriz.</span>
</p>

<p style="text-align:center;">
    <img src="/images/mobilservices2.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Her iki portal da şuan için kullanılabilir. Hizmetin başlatılmasına kadar ki kısımda ikisini de paralel olarak göstermeye çalışacağım ama daha sonraki aşamalarda bana daha kullanışlı geldiği için eski portal üzerinden devam edeceğim.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Yeni bir Mobile Service oluşturmak için aşağıdaki adımları takip ediyoruz;</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Sol taraftaki menüden MOBILE SERVICES’i seçip alt kısımdaki toolbar’dan NEW butonuna tıklıyoruz.</span>
</p> 	
<p style="text-align:center;">
    <img src="/images/mobilservices3.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Yeni portalda ise; +Yeni &gt; Web + Mobil &gt; Mobile App  adımlarını takip ederek aynı işlemleri gerçekleştirebiliriz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices4.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Açılan popup menüden CREATE’e tıklıyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices5.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Bu kısımda Mobile Service’imiz için detayları belirleyeceğiz. Ben URL kısmını “omerornek” olarak isimlendirdim. Database olarak da siz 20MB FREE olanını kullanabilirsiniz. Ben onu başka bir örneğimde kullandığım için burada çıkmamış. O yüzden başka yeni bir veritabanı oluşturacağım. Region olarak bize en yakın bölge North Europe’ı seçiyorum. Backend olarak da arka planda JavaScript ‘le çalışacağımı bildiriyorum.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices6.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Bu adımda veritabanımızın nerede barınacağını belirliyoruz. İstersek yeni bir server oluşturup onda barındırabiliriz. Benim daha önce oluşturğum server olduğu için veritabanım o server üzerinde barındıracağımı belirtip OK butonuna tıklıyoruz ve servisimiz oluşturulmaya başlıyor.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices7.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Oluşturduğumuz Mobil Servis’in durumu hazır olarak güncelenene kadar bekliyoruz. Bazen bu güncellemede sorun olabiliyor o yüzden çok uzun sürdüyse sayfamızı yenilemekte fayda var.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices8.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Mobile Service ‘imiz kullanıma hazır.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices9.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Ekranda görüldüğü üzere üst kısımda servisimizi kullanırken veya uygulumamızı inşa edereken kullanabileceğimiz özellikler (Dashboard, Data, v.s.), aşağı kısımdaki toolbar’da ise seçilen özelliğin eylemleri gerçekleştirebileceğimiz butonlar bulunmaktadır.</span>
</p>
<br>
<p style="text-align:justify;">
<strong><span style="color:#000000;">Manage Keys:</span></strong>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices10.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Microsoft Azure Mobile Services, API’ye erişimi sınırlandırmak için application key ve master key olmak üzere iki tane anahtar koda sahiptir. Tablolar ve API’ler sadece bu anahtar kodlara sahip uygulamaların isteklerine cevap verir. Ancak bu kodlar şifrelenmemiş olduğundan güvenli olarak görülmez. Bu yüzden bu servislere erişmeden önce kullanıcıların kimlik doğrulamasından geçmesi önemli bir konudur.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Master Key, yönetici erişimi için kullanılır ve bu key dağıtılan uygulamalarda kullanılmamalıdır.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Herhangi bir sorunda veya güvenlik endişesinde “regenerate” butonuna tıklayarak yeni bir key oluşturabiliriz. Ancak bu değişiklik bu servise erişen  diğer uygulamaların servise erişimini engelleyecektir. Bu yüzden çok gerekli olmadıkça değiştirilmemelidir. Değiştirildiği taktirde de uygulamalarımızdaki anahtar kodları güncellememiz gerekmektedir.</span>
</p>
<br>

<p><span style="color:#000000;"><strong>Dashboard</strong></span></p>
<p style="text-align:justify;">
<span style="color:#000000;"> Mobil Service’imiz ve onunla ilgili depolama birimlerinin anlık kullanım durumlarını izleyebileceğimiz kısımdır.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Özelliklerden bazılarını kısaca açıkladıkdan sonra şimdide Microsoft’un Mobile Service örneklerinden birini indirip, onun üzerinden bir uygulama üzerinden bu hizmetin nasıl kullanabilineceğini anlamaya çalışalım.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Hangi platformdaki örnek uygulamayla çalışacakcaksak onu seçiyoruz. Windows &gt; Create a new windows or windows phone app ‘a tıklıyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices11.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Uygulamamız için gerekli işlemler resimde gösterilmektedir. Uygulamızı yazımızın başında belirttiğimiz gibi Visual Studio ile açıp, çalıştıracağız. Bu yüzden eğer Visual Studio yoksa ilk adım olarak onu yüklemeliyiz. Daha sonra da uygulamızdaki verilerin kaydedileceği TodoItem Tablosunu oluşturmak için <strong>CREATE</strong> <strong>TODOITEM TABLE</strong> butonuna tıklıyoruz. En son olarak da uygulamamızın hangi programlama dilinde olacağını belirledikten sonra <strong>DOWNLOAD</strong> butonuna tıklayıp bizim için özel hazırlanmış örnek uygulamızı indiriyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices12.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">İndirdiğimiz uygulama dosyasındaki Solution’a tıklayıp Visual Studio ile açıyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices13.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Uygulamamızı Visual Studio ile açtıktan sonra Solution’da sağ tıklayıp Build ediyoruz. Eğer uygulamamız için gerekli olan eksik veya yüklenmemiş Nuget paketleri varsa bu şekilde tespit edilip yüklenmesini sağlıyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices14.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Solution’dan Windows uygulamasını seçip, çalıştırıyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices15.png"/>
</p>
<br>
<p style="text-align:center;">
    <img src="/images/mobilservices16.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Şimdi de ilk kaydımızı oluşturup, Azure’daki değişiklikleri kontrol edelim.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices17.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Azure &gt; Mobil Servisimizin İsmi &gt; Data &gt; Tablomuzun İsmi</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices18.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Bu şekilde Mobile Service’imizin güzel bir şekilde çalıştığını görmüş olduk.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Mobil Servisin birkaç özelliğini görmek adına indirdiğimiz örneğin kaynak kodların bir kısmını inceleyecek olursak;</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Örneğimizdeki App.xaml.cs ‘e baktığımızda oluşturulan MobileServiceClient nesnesindeki anahtarın, Azure’da oluşturduğumuz Mobil Servisimizin Manage Key’deki Application Key ile aynı olduğunu görebiliriz. Zaten daha öncede bu örneğim bizim için özel oluşturulduğunu söylemiştik.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Datamodel &gt; TodoItem.cs ‘e bakacak olursak;</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices19.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Buradaki TodoItem sınıfı mobil servisimiz tarafından kullanılan veritabanındaki tabloyu, içerisindeki property’ler ise kolonlarımızı temsil etmektedir. JsonProperty olarak nitelendirilen kısımdaki isimler birebir veritabanımızdaki tablo kolonlarının ismidir. Bunlar temsil edildikleri sınıf property isimleri ile aynı olmayabilir ve Azure Mobile Service’in temsil edildiği Entity kesinlikle bir Id ‘ye sahip olmalıdır. Eğer Id olmaz ise çalışmayacaktır.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Bu aşamada Azure Mobile Service’in mucize diye nitenlendirilebilecek bir özelliğine değinmeye çalışacağım. Yukarıda bahsettiğim TodoItem sınıfına yeni bir alan ekleyeceğim.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices20.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Kırmızı dikdörtgen ile belirtilmiş alanı ekledim. Daha sonra da veri eklenmesi sırasında varsayılan değer göndermesi için MainPage’deki InsertTodoItem fonksiyonuna</span>
<span style="color:#000000;"><strong>todoItem.YeniAlan = "yeni alan denemesi";</strong></span>
<span style="color:#000000;">kodunu ekliyoruz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices21.png"/>
</p>
<br>


<p style="text-align:justify;">
<span style="color:#000000;">Yaptığımız işlem tamamen veritabanımızdan bağımsız ve veritabanı tasarımına uymayan bir işlemdir. Dolayısıyla uygulamamızın çalıştırıldığında hata vermesi bekleyebiliriz.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Uygulamamızı çalıştırdığımızda ise hata vermeden çalıştığını görebiliriz.</span>
</p>
<p style="text-align:center;">
    <img src="/images/mobilservices22.png"/>
</p>
<br>
<p style="text-align:center;">
    <img src="/images/mobilservices23.png"/>
</p>
<br>

<span style="color:#000000;">Kırmızıyla belirtilen kısımda görüldüğü gibi yeni bir kolon oluşturmuş.</span>

<p style="text-align:justify;">
<span style="color:#000000;">Bu özellik sayesinde uygulama geliştirme işlemi inanılmaz şekilde kolaylaştırılmış oluyor. Çünkü görüldüğü üzere kodumuzdaki herhangi bir değişiklikte daha alt katmanda bulunan veritabanımız hatasız uyum sağlamış ve bizim yerimize arkaplandaki bu ayarlamaları yapmış oluyor. Biz kendi uygulamamızla uğraşırken Microsoft Azure bu işlemleri bizim yerimize yaparak hem zamandan tasarruf etmemizi hem de sadece uygulamamıza yoğunlaşmamızı sağlıyor.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Aslında bu durum pratikte çok kullanışlı olsa da uygulamamızın ileri aşamalarında veri kirliliğine neden olabileceğine de değinmekte fayda var. Örneğin uygulamamızı geliştirip market ortamına koyduğumuz da bu özelliğin başımıza dert açmasını önlemek için;</span>
</p>

<p style="text-align:center;">
    <img src="/images/mobilservices24.png"/>
</p>
<br>

<p style="text-align:justify;">
<span style="color:#000000;">Mobile Service’imizin Configure kısmına gelip, “<strong>ENABLE DYNAMIC SCHEMA</strong>” özelliğini “<strong>OFF</strong>” konumuna getirmeliyiz.</span>
</p>