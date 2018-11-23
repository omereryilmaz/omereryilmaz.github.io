---
layout: post
title: Arduino ile Azure Mobile Services Bağlantısı IoT
date: 2016-01-31 21:37
image: arduino-azure.png
comments: true
categories: [Arduino, MicrosoftAzure, IoT]
---
<p style="text-align:justify;">
<span style="color:#000000;">Bu yazımda, Arduino ile aldığımız verileri bulut ortamına aktarmayı göstermeye çalışacağım. Yani bu yazıyla birlikte IoT konusuna da girmiş olacağız.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">IoT (Internet of Things = Nesnelerin İnterneti) adından da anlaşılacağı üzere fiziksel ağ üzerindeki nesnelerin; cihazlar, araçlar ve binalarda bulunan elektronik gömülü sistemler sayesinde birbiriyle bağlantı kurması ve veri alışverişi yapması olayıdır. 1970’lerden itibaren kurulan ATM’ler ilk IoT cihazları kabul edilmektedir. Günümüzde de bu tarz cihazların sayısı artmaya devam etmektedir. Cisco firmasının öngörüsüne göre 2020 yılında tüm dünyadaki IOT cihazlarının sayısı 50milyar’a ulaşması beklenmektedir[<a href="http://www.cisco.com/c/en/us/solutions/internet-of-things/overview.html" target="_blank">1</a>]. Bunun anlamı bir kaç yıl içerisinde IoT teknolojisi hayatımızın her alanına girmesi demektir. Örneğin internete bağlı buzdolabımızdaki yumurtanın bittiğinin tespit edilmesi ve otomatik olarak marketten yumurta siparişinin edilmesi, sağlık alanında kritik hastaların takibi ve olası kriz öncesi mühahale yapılarak yaşam kalitesinin arttırılması, araçlarımızdaki arızanın büyük boyutlara ulaşmadan tespiti gibi sınırı olmayan bir alan olarak görebiliriz.</span>
</p>
<p style="text-align:center;">
  <embed width="520" height="345"
  src="http://players.brightcove.net/2097119709001/NJOvFZMYl_default/index.html?videoId=4609490745001" 
  frameborder="0"/>
 
</p>
<p style="text-align:center;">
<span style="color:#000000;">Internet of Things Video<span style="color:#808080;">[</span><span style="color:#008080;"><a style="color:#008080;" href="http://www.forbes.com/sites/jacobmorgan/2014/05/13/simple-explanation-internet-things-that-anyone-can-understand" target="_blank">2</a></span><span style="color:#808080;">]</span></span></p>

<p style="text-align:justify;">
<span style="color:#000000;">Biz de bu yazımızda yapacağımız basit bir örnekle IoT dünyasına ufak bir adım atmış olacağız. Örneğimde Arduino Uno R3 ve internet bağlantısını gerçekleştirmek için de Ethernet Shield kullanacağım.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Arduino Uno hakkında kısa bir bilgi verecek olursak, üzerinde ATMEL firması tarafından geliştirilen Atmega328 mikrodenetleyicisi bulunmaktadır. Arduino üzerindeki programı yürüten asıl mikrodenetleyici budur. Program belleği 32KB olup, veri belleği ise 2KB’dır. Kart üzerinde bulunan diğer entegre ise Atmega16u2 ise USB bağlantısı için kullanılmaktadır. Ayrıca 14 adet dijital giriş/çıkış pini, 6 adet de analog giriş/çıkış pini bulunmaktadır.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Ethernet Shield ve kütüphanesi hakkında şu linkten ayrıntılı bilgiye ulaşabilirsiniz.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;"> <a href="https://www.arduino.cc/en/reference/ethernet" target="_blank">https://www.arduino.cc/en/reference/ethernet</a></span>
</p>

<p style="text-align:justify;"><span style="color:#000000;">Kodumuzu yazacağımız ortam ise Arduino için Java dilinde hazırlanmıştır. Kodlamada kullanılan kütüphaneler ise C ve C++ dillerinde yazılmıştır. Bu IDE’yi <span style="color:#008080;"><a style="color:#008080;" href="https://www.arduino.cc/en/Main/Software">https://www.arduino.cc/en/Main/Software</a> </span>adresinden indirip, bilgisayarınıza kurabilirsiniz.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Örneğimizdeki senaryo, oda ısısının ve neminin belli aralıklarla okunması ve bulut ortamına aktarılması olacak. Oda sıcaklığını ölçmek için DHT11 sensörünü, verilerimizi bulut ortamında barındırma işlemini ise <a href="/azure-mobile-services-nedir/" target="_blank">Azure Mobile Services</a>’i kullanacağım.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Eğer</span> <a href="/azure-mobile-services-nedir/" target="_blank">Azure Mobil Services</a> <span style="color:#000000;">'in oluşturulması hakkında bilgi sahibi değilseniz;</span> <a href="/azure-mobile-services-nasil-olusturulur/" target="_blank">Azure Mobil Services Nasıl Oluşturulur?</a><span style="color:#000000;"> yazımı okuyabilirsiniz.</span>
</p>

<span style="color:#000000;"> <strong>1. Devrenin Kurulması:</strong></span>
<span style="color:#000000;"> Malzemeler:</span>
<ul>
 	<li><span style="color:#000000;">Arduino UNO R3</span></li>
 	<li><span style="color:#000000;">Ethernet Shield</span></li>
 	<li><span style="color:#000000;">DHT11 ısı ve nem sensörü</span></li>
 	<li><span style="color:#000000;">1 adet 10K direnç</span></li>
 	<li><span style="color:#000000;">5 adet kablo (Tasarımınıza göre sayı değişebilir.)</span></li>
</ul>
&nbsp;

<span style="color:#000000;">DHT11 ısı ve nem sensörü:</span>
<p style="text-align:center;">
    <img src="/images/dht11.png"/>
</p>
<br><br>

<span style="color:#000000;">Devre prototipi:</span>
<p style="text-align:center;">
    <img src="/images/dht11-arduino_bb.png"/>
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">DHT11’in kullanım klavuzunda bellirttiği şekilde devreye bağlantısını gerçekleştiriyoruz. DHT11’in ikinici bacağını yani veri bacağını Arduino’nun 2 numaralı dijital girişine bağlıyoruz. </span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">(Şekildeki devreyi Fritzing programıyla oluşturdum. Fritzing programını</span> <a href="http://fritzing.org/download/">http://fritzing.org/download/</a> <span style="color:#000000;">bu adresten ücretsiz olarak temin edebilirsiniz.)</span>
</p>
<br><br>


<p style="text-align:justify;">
<span style="color:#000000;"><strong>2. </strong></span><span style="color:#000000;"><strong>Kodun yazılması ve Arduino’ya yüklenmesi:</strong></span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Öncelikle DHT11’in kütüphanesini indirip, C:Program Files (x86)Arduinolibraries ‘deki kütüphane klasörümüze kopyalıyoruz. Daha sonra bu kütüphanemizi include komutuyla kodumuza dahil ediyoruz.</span>
</p>

<p style="text-align:justify;">
<a href="/images/dht11.rar" target="_blank">DHT11 Kütüphanesini İndir.</a>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Sensördeki değerleri serial monitor’de görüntülemek için aşağıdaki kodu Arduino’ya yükleyelim.</span>
</p>
<pre class="lang:c decode:true">// omereryilmaz.com Arduino ile Azure Baglantisi

#include &lt;dht11.h&gt; // DHT11 kütüphanesini dahil ediyoruz.
#define dataPIN 2 // dataPIN olarak Dijital 2'yi belirliyoruz.

dht11 DHT11;

void setup()
{
  Serial.begin(9600); // Seri iletişimi başlatıyoruz.
}

void loop()
{
  Serial.println("n");
  // Sensörün okunup okunmadığını konrol ediyoruz.
  // kontrol 0 ise sorunsuz okunuyor demektir.
  int kontrol = DHT11.read(dataPIN);

  if(kontrol==0){
  // Sensörden gelen verileri serial monitörde yazdırıyoruz.
  Serial.print("Nem (%): ");
  Serial.println((float)DHT11.humidity, dataPIN);

  Serial.print("Sicaklik (Celcius): ");
  Serial.println((float)DHT11.temperature, dataPIN);
  }
  else{
    Serial.print("Sensor Okunmuyor.");
    }
  // 2 saniye bekliyoruz.
  delay(2000);

}
</pre>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Serial monitor’ü açmak için kırmızı işaretli yeri tıklamamız yeterli;</span>
</p>

<p style="text-align:center;">
    <img src="/images/arduino-azure1.png"/>
</p>
<br><br>



<span style="color:#000000;">Serial Monitor;</span>

<p style="text-align:center;">
    <img src="/images/arduino-azure2.png"/>
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Eğer adımları doğru şekilde yaptıysak yukarıdaki şekildekine benzer ekran çıktısı almamız gerekiyor. Buradaki önemli noktalardan biri seri iletişimi başlattığımız değer, serial monitordeki baud değeriyle aynı olması gerekiyor.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;"><strong>Baud:</strong> Seri haberleşmede iletişim hızının ifade edildiği bir değerdir.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;"> <strong>Baud rate:</strong> Uzak iletişim ve elektronikte kullanılan saniyedeki atım oranını gösteren birimdir.</span> [<a href="https://tr.wikipedia.org/wiki/Baud" target="_blank">3</a>]
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Bu aşamadan sonra artık verilerimizi bulut ortamına aktarabiliriz. Bunun için öncelikler Azure hesabımıza giriş yapıp bir Mobile Service oluşturmamız gerekmektedir. Bu işlemi önceki yazımızda göstermiştik.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Mobile Servisimiz ile alakalı şuan için bize lazım olan bilgiler;</span>
</p>
<ul>
 	<li><span style="color:#000000;"><strong>server:</strong> Mobile Service URL</span></li>
 	<li><span style="color:#000000;"><strong>table_name:</strong> Mobil Service’de oluşturduğumuz tablo ismi</span></li>
 	<li><span style="color:#000000;"><strong>app_key:</strong> Manage Keys’deki Application Keys</span></li>
</ul>

<p style="text-align:center;">
    <img src="/images/arduino-azure3.jpg"/>
</p>
<br><br>

<p style="text-align:center;">
    <img src="/images/arduino-azure4.jpg"/>
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Resimlerdeki gibi Arduino’ya Ethernet Shield’i ilave edip, daha önceki devre prototipiyle aynı olacak şekildeki bağlantılarımızı güncelliyoruz.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Devremizi tamamladıktan sonra Arduino’yu bilgisayara bağlayıp aşağıdaki kodu yükleyelim. Kodu yükledikten sonra internet bağlantısını gerçekleştirip uygulamamızı çalışmasını serial monitorden veya Azure &gt; Mobil Services &gt; “Mobil Servisimizin İsmi” &gt; Data kısmından gelen verilerimizi görebiliriz.</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Senaryomuz şu şekilde gerçekleşecek; İlk önce belirlediğimiz mac adresine göre Ethernet Shield başlatılacak, Arduino DHT11 sensöründen aldığı değerleri Ethernet Shield aracılığıyla ilgili adresteki mobil servisimize gönderecek. Ben uygulamanın basitliği açısından her 5 saniyede verinin gönderilmesini istedim. Tabiki bu tarz birşey veritabanını gereksiz bir şekilde şişmesine neden olacaktır. Bunu önlemek için sadece değerlerin değiştiği zamanlar verinin gönderilmesi sağlanabilir. Bu şekilde gereksiz aynı verinin gönderilmesi engellenmiş olurdu veya daha farklı senaryolar da düşünebilirsiniz orası sizin algoritmanıza kalmış.</span>
</p>

<pre class="lang:c decode:true ">// omereryilmaz.com Arduino ile Azure Baglantisi

#include &lt;SPI.h&gt;
#include &lt;Ethernet.h&gt;
#include &lt;dht11.h&gt; // DHT11 kütüphanesini dahil ediyoruz.
#define dataPIN 2 // dataPIN olarak Dijital 2'yi belirliyoruz.
dht11 DHT11;

// Ethernet shield MAC adresi tanimliyoruz.
byte mac[] = { 0xDE, 0xAD, 0xBE, 0xEF, 0xFE, 0xED };

// Azure Mobile Service adresi
const char *server = "omerarduino.azure-mobile.net";

// Azure Mobile Service tablo ismi
const char *table_name = "omerev";

// Azure Mobile Service Application Key
// Dashboard kisminda alt tarafta 'Manage Keys'
const char *app_key = "UYgmWZxxxxxxxxxxxxxxxxxx";

char* jsonKodu = "";


EthernetClient client;

char buffer[64];

void send_request(int sicaklik, int nem)
{


  if (client.connect(server, 80)) {
    Serial.println("-----------------------");
    Serial.print("Sicaklik (Celcius): ");
    Serial.println(sicaklik);
    Serial.print("Nem (%): ");
    Serial.println(nem);
    Serial.println("-----------------------");
    // POST URI
    //tirnak icindeki %s yerine table_name i yaz, buffer degiskenine at
    sprintf(buffer, "POST /tables/%s HTTP/1.1", table_name);
    //bufferdaki post islemini baslat
    client.println(buffer);

    // Host basligini tanimla
    sprintf(buffer, "Host: %s", server);
    client.println(buffer);

    // Azure Mobile Services application key
    sprintf(buffer, "X-ZUMO-APPLICATION: %s", app_key);
    client.println(buffer);


    //verinin json olarak gonderilecegini belirtiyoruz
    client.println("Content-Type: application/json");

    jsonKodu = "{"sensor_tipi":"Oda_isi_nem" ,"sicaklik": %d,"nem": %d}";
    // POST edilecek veriler
    sprintf(buffer, jsonKodu, sicaklik, nem);

    // Icerik uzunlugu
    client.print("Content-Length: ");
    client.println(strlen(buffer));

    // Basliklarin sonu
    client.println();

    // Istek govdesi
    client.println(buffer);

  } else {
    Serial.println("Baglanti Hatasi! :(");
  }
}

/*
** Yanit bekleniyor
*/

void wait_response()
{
  while (!client.available()) {
    if (!client.connected()) {
      return;
    }
  }
}

/*
** Yanit okunuyor ve yigina ekleniyor
*/

void read_response()
{
  bool print = true;

  while (client.available()) {
    char c = client.read();
    // Sadece ilk satir basina kadar yazdir
    if (c == 'n')
      print = false;
    if (print)
      Serial.print(c);
  }
   Serial.println(""); //bosluk
}

/*
** Baglantiyi kapat
*/

void end_request()
{
  client.stop();
}


void setup() {
  Serial.begin(9600);
  Serial.println("Seri iletisim baslatildi.");
  while (!Serial) {
    ; // serial port baglantsi icin bekle
    Serial.println("Seri iletisim hata.");
  }

  Serial.println("Ethernet ayarlari yapiliyor..");

  if (Ethernet.begin(mac) == 0) {
    delay(100);
    Serial.println("Ethernet Hatasi");
    for (;;) ; //sonsuz dongu prog kitle
  }
  //ethernet shield'in başlatılması (initialize) icin bekletiliyor
  delay(1000);
  Serial.println("Ethernet ayarlari yapildi.");

}

void loop() {

  int kontrol = DHT11.read(dataPIN);

  if(kontrol==0){
    int sicak = (int)DHT11.temperature;
    int ne = (int)DHT11.humidity;
    send_request(sicak,ne);
    wait_response();
    read_response();
    end_request();
  }
  else{
    Serial.print("Sensor Okunmuyor.");
    }

  delay(5000); //5 saniye bekletiyoruz.
}</pre>

<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Kodumuzdaki önemli noktalardan bahsedecek olursak;</span>
</p>
<p style="text-align:justify;">
<span style="color:#000000;">Bir önceki koda ilave olarak kulladığımız kütüphaneler; SPI ve Ethernet.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">byte mac[] = { 0xDE, 0xAD, 0xBE, 0xEF, 0xFE, 0xED };</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Bu kodu ethernet shield’e mac adresi atamak için kullanıyoruz. Bazı ethernet shield’lerde bu adres üzerinde yazılı olarak gelmesine karşılık bazılarında gelmiyor. Bu yüzden mac standartlarına uygun kendi belirlediğimiz bir adresi de atayabiliriz.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;"> jsonKodu = "{"sensor_tipi":"Oda_isi_nem" ,"sicaklik": %d,"nem": %d}";</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;"> Bu kodda ise verilerimizi Json formatında gönderiyoruz. “kolon_ismi1:veri1, kolon_ismi2:veri2” şeklindeki tanımlama mevcuttur. İki noktadan önceki kısım kolon adımnı sonraki kısım isi o kolona aktarılacak veriyi temsil etmektedir.</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;">Eğer adımları başarılı bir şekilde gerçekleştirdiysek;</span>
</p>

<p style="text-align:justify;">
<span style="color:#000000;"> Serial Monitor;</span>
</p>

<p style="text-align:center;">
    <img src="/images/arduino-azure6.png"/>
</p>
<br><br>

<p style="text-align:center;">
    <img src="/images/arduino-azure7.png"/>
</p>
<br><br>

<p style="text-align:justify;">
<span style="color:#000000;">Yukarıdaki resimde görüldüğü gibi verilerimizi bulut ortamına aktarmış olduk.</span>
</p>
<br><br>
<strong>Kaynakça:</strong>
<ul>
 	<li>[1] http://www.cisco.com/c/en/us/solutions/internet-of-things/overview.html</li>
 	<li>[2] http://www.forbes.com/sites/jacobmorgan/2014/05/13/simple-explanation-internet-things-that-anyone-can-understand</li>
 	<li>[3] https://tr.wikipedia.org/wiki/Baud</li>
</ul>
