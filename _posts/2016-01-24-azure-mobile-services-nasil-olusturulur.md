---
layout: post
title: Microsoft Azure Mobile Services Nasıl Oluşturulur?
date: 2016-01-24 16:47
image: Mobileappolusturmak.jpg
comments: true
categories: [MicrosoftAzure, WindowsPhone]
---
<span style="color:#000000;">Bir önceki yazımızda <a style="color:#000000;" href="/azure-mobile-services-nedir/" target="_blank">Azure Mobil Service (Mobil Hizmet)</a>’in ne olduğuna değinmiştik. Bu yazımızda ise Mobil Hizmet’in oluşturulması ve kullanılmasını göreceğiz.</span>

<span style="color:#000000;">Öncelikle bu yazıdaki örneği uygulamak için Microsoft Azure hesabınız olması gerekmektedir. Burada Mobile Service oluşturup daha sonra da bu servis için oluşturulmuş örneğini de Visual Studio ile incelemeye çalışacağız.</span>

<span style="color:#000000;">Eğer bir Azure hesabınız varsa <a style="color:#000000;" href="https://manage.windowsazure.com">https://manage.windowsazure.com</a> adresinden girip işleme başlıyoruz.</span>

<span style="color:#000000;">Karşınıza şekildeki gibi bir ekran çıkacak;</span>

<a href="/images/mobilservices1.png" rel="attachment wp-att-574"><img class="alignnone wp-image-574" src="/images/mobilservices1.png" alt="mobilservices1" width="569" height="315" /></a>

&nbsp;

<span style="color:#000000;">Yeni Azure portalını kullanmak istiyorsak; <a style="color:#000000;" href="https://portal.azure.com">https://portal.azure.com</a> adresini kullanabiliriz.</span>

<a href="/images/mobilservices2.png" rel="attachment wp-att-575"><img class="alignnone wp-image-575" src="/images/mobilservices2.png" alt="mobilservices2" width="554" height="323" /></a>

&nbsp;

<span style="color:#000000;">Her iki portal da şuan için kullanılabilir. Hizmetin başlatılmasına kadar ki kısımda ikisini de paralel olarak göstermeye çalışacağım ama daha sonraki aşamalarda bana daha kullanışlı geldiği için eski portal üzerinden devam edeceğim.</span>

<span style="color:#000000;">Yeni bir Mobile Service oluşturmak için aşağıdaki adımları takip ediyoruz;</span>
<ol>
 	<li><span style="color:#000000;">Sol taraftaki menüden MOBILE SERVICES’i seçip alt kısımdaki toolbar’dan NEW butonuna tıklıyoruz.</span>
<a href="/images/mobilservices3.png" rel="attachment wp-att-576"><img class="alignnone wp-image-576" src="/images/mobilservices3.png" alt="mobilservices3" width="564" height="312" /></a><span style="color:#000000;">Yeni portalda ise; +Yeni &gt; Web + Mobil &gt; Mobile App  adımlarını takip ederek aynı işlemleri gerçekleştirebiliriz.</span>
<span style="color:#000000;"><a style="color:#000000;" href="/images/mobilservices4.png" rel="attachment wp-att-577"><img class="alignnone wp-image-577" src="/images/mobilservices4.png" alt="mobilservices4" width="566" height="281" /></a></span></li>
 	<li><span style="color:#000000;">Açılan popup menüden CREATE’e tıklıyoruz.</span><a href="/images/mobilservices5.png" rel="attachment wp-att-578"><img class="alignnone wp-image-578" src="/images/mobilservices5.png" alt="mobilservices5" width="568" height="281" /></a></li>
 	<li><span style="color:#000000;">Bu kısımda Mobile Service’imiz için detayları belirleyeceğiz. Ben URL kısmını “omerornek” olarak isimlendirdim. Database olarak da siz 20MB FREE olanını kullanabilirsiniz. Ben onu başka bir örneğimde kullandığım için burada çıkmamış. O yüzden başka yeni bir veritabanı oluşturacağım. Region olarak bize en yakın bölge North Europe’ı seçiyorum. Backend olarak da arka planda JavaScript ‘le çalışacağımı bildiriyorum.</span>
<a href="/images/mobilservices6.png" rel="attachment wp-att-579"><img class="alignnone wp-image-579" src="/images/mobilservices6.png" alt="mobilservices6" width="482" height="384" /></a></li>
 	<li><span style="color:#000000;">Bu adımda veritabanımızın nerede barınacağını belirliyoruz. İstersek yeni bir server oluşturup onda barındırabiliriz. Benim daha önce oluşturğum server olduğu için veritabanım o server üzerinde barındıracağımı belirtip OK butonuna tıklıyoruz ve servisimiz oluşturulmaya başlıyor.</span>
<a href="/images/mobilservices7.png" rel="attachment wp-att-580"><img class="alignnone wp-image-580" src="/images/mobilservices7.png" alt="mobilservices7" width="419" height="324" /></a></li>
 	<li><span style="color:#000000;">Oluşturduğumuz Mobil Servis’in durumu hazır olarak güncelenene kadar bekliyoruz. Bazen bu güncellemede sorun olabiliyor o yüzden çok uzun sürdüyse sayfamızı yenilemekte fayda var.</span>
<a href="/images/mobilservices8.png" rel="attachment wp-att-581"><img class="alignnone wp-image-581" src="/images/mobilservices8.png" alt="mobilservices8" width="584" height="315" /></a></li>
 	<li><span style="color:#000000;">Mobile Service ‘imiz kullanıma hazır.</span>
<a href="/images/mobilservices9.png" rel="attachment wp-att-582"><img class="alignnone wp-image-582" src="/images/mobilservices9.png" alt="mobilservices9" width="565" height="313" />
</a><span style="color:#000000;"><span style="color:#000000;">Ekranda görüldüğü üzere üst kısımda servisimizi kullanırken veya uygulumamızı inşa edereken kullanabileceğimiz özellikler (Dashboard, Data, v.s.), aşağı kısımdaki toolbar’da ise seçilen özelliğin eylemleri gerçekleştirebileceğimiz butonlar bulunmaktadır.</span></span>&nbsp;</li>
</ol>
<strong><span style="color:#000000;">Manage Keys:</span>
<a href="/images/mobilservices10.png" rel="attachment wp-att-583"><img class="alignnone wp-image-583" src="/images/mobilservices10.png" alt="mobilservices10" width="392" height="273" />
</a></strong>

<span style="color:#000000;">Microsoft Azure Mobile Services, API’ye erişeme sınırlandırmak için application key ve master key olmak üzere iki tane anahtar koda sahiptir. Tablolar ve API’ler sadece bu anahtar kodlara sahip uygulamaların isteklerine cevap verir. Ancak bu kodlar şifrelenmemiş olduğundan güvenli olarak görülmez. Bu yüzden bu servislere erişmeden önce kullanıcıların kimlik doğrulamasından geçmesi önemli bir konudur.</span>

<span style="color:#000000;">Master Key, yönetici erişimi için kullanılır ve bu key dağıtılan uygulamalarda kullanılmamalıdır.</span>

<span style="color:#000000;">Herhangi bir sorunda veya güvenlik endişesinde “regenerate” butonuna tıklayarak yeni bir key oluşturabiliriz. Ancak bu değişiklik bu servise erişen  diğer uygulamaların servise erişimini engelleyecektir. Bu yüzden çok gerekli olmadıkça değiştirilmemelidir. Değiştirildiği taktirde de uygulamalarımızdaki anahtar kodları güncellememiz gerekmektedir.</span>

&nbsp;

<span style="color:#000000;"><strong>Dashboard:</strong></span>
<span style="color:#000000;"> Mobil Service’imiz ve onunla ilgili depolama birimlerinin anlık kullanım durumlarını izleyebileceğimiz kısımdır.</span>

<span style="color:#000000;">Özelliklerden bazılarını kısaca açıkladıkdan sonra şimdide Microsoft’un Mobile Service örneklerinden birini indirip, onun üzerinden bir uygulama üzerinden bu hizmetin nasıl kullanabilineceğini anlamaya çalışalım.</span>
<ol>
 	<li><span style="color:#000000;">Hangi platformdaki örnek uygulamayla çalışacakcaksak onu seçiyoruz. Windows &gt; Create a new windows or windows phone app ‘a tıklıyoruz.</span>
<a href="/images/mobilservices11.png" rel="attachment wp-att-584"><img class="alignnone wp-image-584" src="/images/mobilservices11.png" alt="mobilservices11" width="569" height="405" /></a></li>
 	<li><span style="color:#000000;">Uygulamamız için gerekli işlemler resimde gösterilmektedir. Uygulamızı yazımızın başında belirttiğimiz gibi Visual Studio ile açıp, çalıştıracağız. Bu yüzden eğer Visual Studio yoksa ilk adım olarak onu yüklemeliyiz. Daha sonra da uygulamızdaki verilerin kaydedileceği TodoItem Tablosunu oluşturmak için <strong>CREATE</strong> <strong>TODOITEM TABLE</strong> butonuna tıklıyoruz. En son olarak da uygulamamızın hangi programlama dilinde olacağını belirledikten sonra <strong>DOWNLOAD</strong> butonuna tıklayıp bizim için özel hazırlanmış örnek uygulamızı indiriyoruz.</span>
<a href="/images/mobilservices12.png" rel="attachment wp-att-585"><img class="alignnone wp-image-585" src="/images/mobilservices12.png" alt="mobilservices12" width="553" height="252" /></a></li>
 	<li><span style="color:#000000;">İndirdiğimiz uygulama dosyasındaki Solution’a tıklayıp Visual Studio ile açıyoruz.</span>
<a href="/images/mobilservices13.png" rel="attachment wp-att-586"><img class="alignnone wp-image-586" src="/images/mobilservices13.png" alt="mobilservices13" width="570" height="166" /></a></li>
 	<li><span style="color:#000000;">Uygulamamızı Visual Studio ile açtıktan sonra Solution’da sağ tıklayıp Build ediyoruz. Eğer uygulamamız için gerekli olan eksik veya yüklenmemiş Nuget paketleri varsa bu şekilde tespit edilip yüklenmesini sağlıyoruz.</span>
<a href="/images/mobilservices14.png" rel="attachment wp-att-587"><img class="alignnone wp-image-587" src="/images/mobilservices14.png" alt="mobilservices14" width="463" height="199" /></a></li>
 	<li><span style="color:#000000;">Solution’dan Windows uygulamasını seçip, çalıştırıyoruz.</span>
<a href="/images/mobilservices15.png" rel="attachment wp-att-588"><img class="alignnone wp-image-588" src="/images/mobilservices15.png" alt="mobilservices15" width="514" height="194" /></a><a href="/images/mobilservices16.png" rel="attachment wp-att-589"><img class="alignnone wp-image-589" src="/images/mobilservices16.png" alt="mobilservices16" width="530" height="237" /></a><span style="color:#000000;"><a style="color:#000000;" href="/images/mobilservices15.png" rel="attachment wp-att-588">
</a></span></li>
 	<li><span style="color:#000000;">Şimdi de ilk kaydımızı oluşturup, Azure’daki değişiklikleri kontrol edelim.</span>
<a href="/images/mobilservices17.png" rel="attachment wp-att-590"><img class="alignnone wp-image-590" src="/images/mobilservices17.png" alt="mobilservices17" width="539" height="210" />
</a><span style="color:#000000;">Azure &gt; Mobil Servisimizin İsmi &gt; Data &gt; Tablomuzun İsmi</span>
<a href="/images/mobilservices18.png" rel="attachment wp-att-591"><img class="alignnone wp-image-591" src="/images/mobilservices18.png" alt="mobilservices18" width="495" height="169" /></a></li>
</ol>
<span style="color:#000000;">Bu şekilde Mobile Service’imizin güzel bir şekilde çalıştığını görmüş olduk.</span>

<span style="color:#000000;">Mobil Servisin birkaç özelliğini görmek adına indirdiğimiz örneğin kaynak kodların bir kısmını inceleyecek olursak;</span>

<span style="color:#000000;">Örneğimizdeki App.xaml.cs ‘e baktığımızda oluşturulan MobileServiceClient nesnesindeki anahtarın, Azure’da oluşturduğumuz Mobil Servisimizin Manage Key’deki Application Key ile aynı olduğunu görebiliriz. Zaten daha öncede bu örneğim bizim için özel oluşturulduğunu söylemiştik.</span>

<span style="color:#000000;">Datamodel &gt; TodoItem.cs ‘e bakacak olursak;</span>
<a href="/images/mobilservices19.png" rel="attachment wp-att-592"><img class="alignnone wp-image-592" src="/images/mobilservices19.png" alt="mobilservices19" width="595" height="439" /></a>

<span style="color:#000000;">Buradaki TodoItem sınıfı mobil servisimiz tarafından kullanılan veritabanındaki tabloyu, içerisindeki property’ler ise kolonlarımızı temsil etmektedir. JsonProperty olarak nitelendirilen kısımdaki isimler birebir veritabanımızdaki tablo kolonlarının ismidir. Bunlar temsil edildikleri sınıf property isimleri ile aynı olmayabilir ve Azure Mobile Service’in temsil edildiği Entity kesinlikle bir Id ‘ye sahip olmalıdır. Eğer Id olmaz ise çalışmayacaktır.</span>

<span style="color:#000000;">Bu aşamada Azure Mobile Service’in mucize diye nitenlendirilebilecek bir özelliğine değinmeye çalışacağım. Yukarıda bahsettiğim TodoItem sınıfına yeni bir alan ekleyeceğim.</span>
<a href="/images/mobilservices20.png" rel="attachment wp-att-593"><img class="alignnone wp-image-593" src="/images/mobilservices20.png" alt="mobilservices20" width="590" height="438" /></a>

&nbsp;

<span style="color:#000000;">Kırmızı dikdörtgen ile belirtilmiş alanı ekledim. Daha sonra da veri eklenmesi sırasında varsayılan değer göndermesi için MainPage’deki InsertTodoItem fonksiyonuna</span>
<span style="color:#000000;"><strong>todoItem.YeniAlan = "yeni alan denemesi";</strong></span>
<span style="color:#000000;">kodunu ekliyoruz.</span>
<a href="/images/mobilservices21.png" rel="attachment wp-att-594"><img class="alignnone wp-image-594" src="/images/mobilservices21.png" alt="mobilservices21" width="604" height="449" /></a>

&nbsp;

<span style="color:#000000;">Yaptığımız işlem tamamen veritabanımızdan bağımsız ve veritabanı tasarımına uymayan bir işlemdir. Dolayısıyla uygulamamızın çalıştırıldığında hata vermesi bekleyebiliriz.</span>

<span style="color:#000000;">Uygulamamızı çalıştırdığımızda ise hata vermeden çalıştığını görebiliriz.</span>
<a href="/images/mobilservices22.png" rel="attachment wp-att-595"><img class="alignnone wp-image-595" src="/images/mobilservices22.png" alt="mobilservices22" width="560" height="366" />
</a>

<span style="color:#000000;">Veritabanı kısmına bakacak olursak;</span>
<a href="/images/mobilservices23.png" rel="attachment wp-att-596"><img class="alignnone wp-image-596" src="/images/mobilservices23.png" alt="mobilservices23" width="554" height="269" /></a>

&nbsp;

<span style="color:#000000;">Kırmızıyla belirtilen kısımda görüldüğü gibi yeni bir kolon oluşturmuş.</span>

<span style="color:#000000;">Bu özellik sayesinde uygulama geliştirme işlemi inanılmaz şekilde kolaylaştırılmış oluyor. Çünkü görüldüğü üzere kodumuzdaki herhangi bir değişiklikte daha alt katmanda bulunan veritabanımız hatasız uyum sağlamış ve bizim yerimize arkaplandaki bu ayarlamaları yapmış oluyor. Biz kendi uygulamamızla uğraşırken Microsoft Azure bu işlemleri bizim yerimize yaparak hem zamandan tasarruf etmemizi hem de sadece uygulamamıza yoğunlaşmamızı sağlıyor.</span>

<span style="color:#000000;">Aslında bu durum pratikte çok kullanışlı olsa da uygulamamızın ileri aşamalarında veri kirliliğine neden olabileceğine de değinmekte fayda var. Örneğin uygulamamızı geliştirip market ortamına koyduğumuz da bu özelliğin başımıza dert açmasını önlemek için;</span>
<a href="/images/mobilservices24.png" rel="attachment wp-att-597"><img class="alignnone wp-image-597" src="/images/mobilservices24.png" alt="mobilservices24" width="471" height="323" />
</a>

<span style="color:#000000;">Mobile Service’imizin Configure kısmına gelip, “<strong>ENABLE DYNAMIC SCHEMA</strong>” özelliğini “<strong>OFF</strong>” konumuna getirmeliyiz.</span>
