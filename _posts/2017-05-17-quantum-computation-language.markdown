---
layout: post
title: Quantum Computation Language
image: qcl-image.jpg
date: 2017-05-17 01:08:21 +00:00
tags: [Kuantum, Yazılım, grover-algoritması, kuantum-bilgisayar-programlama, Kuantum-Bilgisayarlar, kuantum-hesaplama-dili, kuantum-programlama-dili, kuantum-simülasyon, qcl, quantum-computing, quantum-computing-language, quantum-programming-language, quantum-programming-language-for-windows]
categories: KuantumBilgisayarlar
---


<h3 style="text-align:center;"><span style="color:#333333;">QCL (Quantum Computation Language) Nedir?</span></h3>
<p style="text-align:center;"><span class="fontstyle2" style="color:#000000;">QCL (Kuantum Hesaplama Dili),  kuantum bilgisayarlar için mimariden bağımsız yüksek seviyeli bir programlama dilidir. Kuantum algoritmalarının eksiksiz uygulanmasını ve simülasyonunu sağlar[1].</span></p>
&nbsp;
<p style="text-align:center;">
<img class="aligncenter wp-image-917 size-full" src="/images/qcl-mimarisi.png" alt="" width="760" height="414" /></p>

&nbsp;
<p style="text-align:center;"><span style="color:#000000;"><strong> Şekil 1.</strong> QCL’nin Hibrit Mimarisi [2].</span></p>
<p style="text-align:center;"><span style="color:#000000;"><span class="fontstyle0">QCL dili C++ ile yazılmış yorumlayıcı program üzerinden kullanılabilmektedir. Kuantum arkaplanını taklit etmek için sayısal simülasyon kütüphanesini (libqc) kullanmaktadır. Bu program açık kaynak olarak geliştirilmiştir ve </span><span class="fontstyle0">http://tph.tuwien.ac.at/~oemer/qcl.html </span><span class="fontstyle0">adresinden temin edinilebilir. En son sürümü 0.6.4 versiyon numarasıyla 2014 yılında yayınlanmıştır.</span></span></p>


<hr />

<h3 style="text-align:center;"><span style="color:#333333;">Yorumlayıcının Çalıştırılması (Windows İçin):</span></h3>
<p style="text-align:center;"><span class="fontstyle0">
</span><span class="fontstyle2" style="color:#000000;">Dil Linux’a uyumlu çıkarıldığı için Windows’da çalışması bazı özel ayarların yapılması gerekmektedir. Bunun için öncelikle Cygwin aracının indirilmesi (https://cygwin.com) ve kurulum sırasında da aşağıda belirtilen paketlerin seçilip indirilmesi gerekmektedir[3].</span></p>
<p style="text-align:left;"><span class="fontstyle2"><strong>Yükleme esnasında seçilip indirilmesi istenen paketler:</strong></span></p>
<p style="text-align:left;"><span class="fontstyle2">
<span style="color:#000000;">Devel altındaki..</span></span></p>

<ul>
 	<li><span class="fontstyle0" style="color:#000000;">bison</span></li>
 	<li><span class="fontstyle0" style="color:#000000;">flex</span></li>
 	<li><span class="fontstyle0" style="color:#000000;">gcc-g++</span></li>
 	<li><span class="fontstyle0" style="color:#000000;">libreadline-devel</span></li>
 	<li><span class="fontstyle0" style="color:#000000;">make</span></li>
</ul>
<p style="text-align:left;"><span class="fontstyle0" style="color:#000000;">
Graphics altındaki..</span></p>

<ul>
 	<li style="text-align:left;"><span class="fontstyle0" style="color:#000000;">libplotter-devel</span></li>
</ul>
<p style="text-align:left;"><span class="fontstyle0">
<span style="color:#000000;">Libs altındaki..</span>
</span></p>

<ul>
 	<li style="text-align:left;"><span class="fontstyle0" style="color:#000000;">libncurses-devel
</span></li>
 	<li style="text-align:left;"><span class="fontstyle0" style="color:#000000;">libX11-devel</span></li>
 	<li style="text-align:left;"><span class="fontstyle0" style="color:#000000;">libXt-devel
</span></li>
</ul>
&nbsp;

<span class="fontstyle0" style="color:#000000;">Web altındaki..</span>
<ul>
 	<li><span class="fontstyle0" style="color:#000000;">wget</span></li>
</ul>
<p style="text-align:center;"><span style="color:#000000;"><span class="fontstyle0">İndirme ve yükleme işlemi tamamlandıktan sonra Cygwin programı yönetici modda açılıp, aşağıda belirtilen komutlar çalıştırılır. (Bu komutlar o andaki mevcut QCL sürümlerine göre değişiklik gösterebilir.)</span> Aşağıdaki komutlar,  <span class="fontstyle0">QCL kaynak kodları bilgisayara indirir ve sıkıştırılmış halde olan dosyayı indirildiği dizine çıkarır.</span></span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">$ wget http://tph.tuwien.ac.at/~oemer/tgz/qcl-0.6.4.tgz
$ tar xvzf qcl-0.6.4.tgz</pre>
&nbsp;
<p style="text-align:center;"><span style="color:#000000;">Daha sonra  i<span class="fontstyle0">ndirilen QCL kaynak kodu aşağıdaki komutlar kullanılarak derlenir.</span></span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">$ cd qcl-0.6.4
$ make</pre>
&nbsp;
<p style="text-align:center;"><span class="fontstyle0"><span style="color:#000000;">QCL yorumlayıcısını/simülatörünü çalıştırmak içinde aşağıdaki komut kullanılır.</span>
</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">$ ./qcl</pre>
&nbsp;
<p style="text-align:center;"><span class="fontstyle0" style="color:#000000;">QCL çalıştığında komut satırında aşağıdakine benzer bir çıktının elde edileceği görülecektir.</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">QCL Quantum Computation Language (64 qubits, seed 1494298832)
[0/64] 1 |0&gt;
qcl&gt;</pre>
<h6></h6>
<h6></h6>

<hr />

&nbsp;
<h3 style="text-align:center;"><span class="fontstyle0"><span style="color:#333333;">QCL ‘deki Bazı Önemli Noktalar</span>
</span></h3>
<ul>
 	<li><span class="fontstyle0"><strong><span style="color:#000000;">Veri Tipleri ve Değişkenler</span></strong></span></li>
</ul>
<p style="text-align:center;"><a href="/images/qcl-veritipi.png"><img class="aligncenter size-full wp-image-890" src="/images/qcl-veritipi.png" alt="" width="491" height="166" /></a></p>
<p style="text-align:center;"><span style="color:#000000;"><strong>Tablo 1:</strong> Klasik veri tipleri</span></p>
<p style="text-align:left;"><span style="color:#000000;"><span class="fontstyle3">
</span><strong><span class="fontstyle0">Örnek: </span></strong></span><span class="fontstyle3"><span style="color:#000000;">Bir değişkenin tanımlanması.</span>
</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; int a; //degiskenin tanimlanmasi
qcl&gt; a=17; //degiskene deger atanmasi
qcl&gt; print a; //degiskenin ekrana basilmasi</pre>
&nbsp;
<ul>
 	<li style="text-align:left;"><strong><span class="fontstyle0" style="color:#000000;"> Operatörler </span></strong></li>
</ul>
<p style="text-align:center;"><a href="/images/qcl-op.png"><img class="aligncenter size-full wp-image-889" src="/images/qcl-op.png" alt="" width="449" height="473" /></a></p>
<p style="text-align:center;"><span class="fontstyle0" style="color:#000000;"><strong> Tablo 2:</strong> QCL operatörler </span></p>

<ul>
 	<li style="text-align:left;"><span style="color:#000000;"><strong> <span class="fontstyle0">Fonksiyonlar</span> </strong></span></li>
</ul>
<p style="text-align:center;"><a href="/images/qcl-func.png"><img class="aligncenter size-full wp-image-888" src="/images/qcl-func.png" alt="" width="643" height="250" /></a></p>
<p style="text-align:center;"><span class="fontstyle0" style="color:#000000;"><strong> Tablo 3:</strong> QCL Aritmatik fonksiyonlar </span></p>
<p style="text-align:left;"><span style="color:#000000;"><strong> <span class="fontstyle0">Örnek: </span></strong><span class="fontstyle2">Bir sayının logaritmasının hesaplanması ( log</span><span class="fontstyle2">2 </span></span><span class="fontstyle2"><span style="color:#000000;">32 = 5 )</span>
</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">qcl&gt; print log(32,2);
: 5</pre>
&nbsp;
<ul>
 	<li><span style="color:#000000;"><strong>Diğer Fonksiyonlar</strong></span></li>
</ul>
<p style="text-align:center;"><a href="/images/qcl-other-func.png"><img class="aligncenter size-full wp-image-892" src="/images/qcl-other-func.png" alt="" width="780" height="211" /></a></p>
<p style="text-align:center;"><span class="fontstyle0" style="color:#000000;"><strong> Tablo 4:</strong> QCL diğer fonksiyonlar </span></p>

<ul>
 	<li style="text-align:left;"><span class="fontstyle0" style="color:#000000;"><strong>Girdi (Input)</strong></span></li>
</ul>
<span style="color:#000000;"><span class="fontstyle2">Konsoldan girdi değerleri “input” komutuyla alınır.
</span></span>

<span class="fontstyle0"><span style="color:#000000;"><strong>Örnek:</strong></span>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; int sayi;
qcl&gt; input "Bir sayi giriniz : ",sayi;
? Bir sayi giriniz : 35</pre>
&nbsp;
<ul>
 	<li><span style="color:#000000;"><strong> <span class="fontstyle0">Çıktı (Output)</span></strong></span></li>
</ul>
<span class="fontstyle2"><span style="color:#000000;">Çıktılar ekrana “print” komutuyla basılır. Virgülle ayrılmış ifade veya değişkenlerin listesini konsol ekranına yazdırır.</span>
</span>

<span class="fontstyle0"><span style="color:#000000;"><strong>Örnek:</strong></span>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; int i=3; real x=pi; complex z=(0,1); boolean b;
qcl&gt; print i,x,z,b;
: 3 3.14159 (0,1) false</pre>
&nbsp;
<ul>
 	<li><strong><span class="fontstyle0" style="color:#000000;"> Koşullu İfadeler (If - else)</span></strong></li>
</ul>
<span class="fontstyle2"><span style="color:#000000;">Koşullu ifadeler klasik programlama dillerinde olduğu gibi “if - else” komutlarıyla</span>
<span style="color:#000000;">gerçekleştirilir.</span></span>

<span class="fontstyle2">
</span><span class="fontstyle0"><strong><span style="color:#000000;">Örnek:</span></strong>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">qcl&gt; int a=1; int b=2;
if (a==b) {print "a esittir b ye.";} else {print "a esit degildir b ye.";}
: a esit degildir b ye.</pre>
&nbsp;
<ul>
 	<li><strong><span class="fontstyle0" style="color:#000000;"> Döngüler</span></strong></li>
</ul>
<span class="fontstyle1"><span style="color:#000000;">Döngüler “for” komutuyla oluşturulur. For içerisinde integer bir sayaç tanımlanır ve bu sayaç süresince ilgili bloğun tekrar tekrar çalıştırılması sağlanır.</span>
</span>

<span class="fontstyle0"><span style="color:#000000;"><strong>Örnek:</strong></span>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; int i;
qcl&gt; for i=10 to 0 step -2 {print "sayi : ",i;}
: sayi : 10
: sayi : 8
: sayi : 6
: sayi : 4
: sayi : 2
: sayi : 0</pre>
&nbsp;
<ul>
 	<li><span style="color:#000000;"> <span class="fontstyle0"><strong>Koşullu Döngüler</strong></span></span></li>
</ul>
<span style="color:#000000;"><span class="fontstyle2">Döngüler koşul sağlandığı müddetçe devam ettirilir. Bu durum “until” veya “while” komutuyla sağlanır. “until” de önce ilgili blok çalıştırılır sonra koşul kontrol ettirilir, “while” da ise önce koşul kontrol edilir sonra blok çalıştırılır.
</span></span>

<span class="fontstyle0"><strong><span style="color:#000000;">Örnek:</span></strong>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">qcl&gt; {print "i degeri : ",i," oldu."; i=i-1;}until i==0;
: i degeri : 5 oldu.
: i degeri : 4 oldu.
: i degeri : 3 oldu.
: i degeri : 2 oldu.
: i degeri : 1 oldu.</pre>
<span style="color:#000000;">veya</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">while i&gt;0 {print "i degeri : ",i," oldu."; i=i-1;};
: i degeri : 5 oldu.
: i degeri : 4 oldu.
: i degeri : 3 oldu.
: i degeri : 2 oldu.
: i degeri : 1 oldu.</pre>
&nbsp;

<hr />

&nbsp;
<p style="text-align:center;"><strong><span class="fontstyle0" style="color:#000000;">Kuantum Depolama ve Kayıtçılar (Registers)</span></strong></p>
<p style="text-align:center;"><span class="fontstyle2" style="color:#000000;">Kuantum bilgisayarlarda olduğu gibi QCL’de de en küçük depolama birimi <strong>qubit</strong>’tir. QCL’de qubit formatında değişken tanımlanması klasik programlamadaki pointer’lar gibi bellekten alan tahsisiyle gerçekleştirilmektedir. Simülasyon ortamı olarak 32 veya 64 qubitlik alan tahsisi etmemize imkan sağlamaktadır. Bu değişken tanımı ve alan tahsisi işlemi için “<strong>qureg</strong>” komutu kullanılmaktadır. “<strong>dump</strong>” komutu ise değişkenimizin bra-ket notasyonunda ekrana basılmasını sağlar. </span></p>
<p style="text-align:center;"><a href="/images/qcl-bloch-kuresi.png"><img class="aligncenter wp-image-895" src="/images/qcl-bloch-kuresi.png" alt="" width="337" height="295" /></a></p>
<p style="text-align:center;"><a href="/images/qcl-1-qubit.png"><img class="aligncenter wp-image-896" src="/images/qcl-1-qubit.png" alt="" width="276" height="39" /></a></p>
<p style="text-align:center;"><span style="color:#000000;"><strong>Şekil 2.</strong> Bloch küresi üzerinde bir qubit'in durumu</span></p>
<span class="fontstyle0"><span style="color:#000000;"><strong>Örnek:</strong></span>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">qcl&gt; qureg x[1]; // 1 qubitlik x isminde alan ayir
qcl&gt; dump; // x degiskenini braket notasyonunda ekrana bas.
: STATE: 1 / 64 qubits allocated, 63 / 64 qubits free
1 |0&gt;</pre>
&nbsp;

&nbsp;

<hr />

&nbsp;
<p style="text-align:center;"><span style="color:#000000;"><strong> <span class="fontstyle0">Kapılar</span></strong></span></p>
<p style="text-align:center;"><span class="fontstyle1" style="color:#000000;">Kuantum bilgisayarlar kapılar tersinebilir (reversible) özelliklidir. Yani bir girdi için aldığımız sonuca, aynı işlemi uyguladığımızda başlangıçtaki girdi değerini elde edebilir. Örneğin, ket 0 ifadesine bir Not kapısı uyguladık diyelim; Not (|0&gt;) = |1&gt; elde ederiz. Daha sonra elde ettiğimiz sonuç olan ket 1’e tekra Not kapısı uygularsak Not(|1&gt;) = |0&gt; ket 0’ı yani başlangıçtaki durumu elde etmiş oluruz.</span></p>
<span class="fontstyle1">
</span><span style="color:#000000;"><span class="fontstyle0"><strong>Bazı önemli kapılar</strong>
</span></span>
<ul>
 	<li><span class="fontstyle0" style="color:#000000;"><strong>Pauli Kapıları:</strong></span></li>
</ul>
<p style="text-align:center;"><span style="color:#000000;">X, Y ve Z Pauli kapıları, Bloch küresinde(Şekil 2) sırasıyla x,y ve z eksenleri etrafında döndürmelere <span class="fontstyle1">karşılık gelmektedir. Matrissel gösterim şekilleri aşağıdaki gibidir.</span> </span></p>
<p style="text-align:center;"><a href="/images/qcl-pauli-gates.png"><img class="aligncenter wp-image-897" src="/images/qcl-pauli-gates.png" alt="" width="239" height="114" /></a></p>
<p style="text-align:center;"><span style="color:#000000;"><strong>Şekil 3</strong>. Pauli Kapılarının matrissel gösterimi</span></p>
<p style="text-align:left;"><span class="fontstyle0"><span style="color:#000000;"><strong>Örnek:</strong></span>
</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; qureg a[1];
qcl&gt; dump;
: STATE: 1 / 64 qubits allocated, 63 / 64 qubits free
1 |0&gt;
qcl&gt; Not(a);
[1/64] 1 |1&gt;</pre>
<span class="fontstyle1"><span style="color:#000000;">Tersinebilir (reversible) özelliği</span>
</span>
<pre class="theme:dark-terminal toolbar:1 lang:default decode:true">qcl&gt; Not(a);
[1/64] 1 |0&gt;</pre>
&nbsp;
<ul>
 	<li><span class="fontstyle0"><span style="color:#000000;"><strong>Hadamard Kapısı:</strong></span></span></li>
</ul>
<span class="fontstyle2" style="color:#000000;">Bu kapı qubitleri süperpozisyon durumuna getirmektedir. Aşağıda gösterildiği gibi H matrisi ile ifade edilmektedir. </span>
<p style="text-align:center;">
<a href="/images/qcl-hadamard-gate.png"><img class="aligncenter size-full wp-image-898" src="/images/qcl-hadamard-gate.png" alt="" width="219" height="80" /></a></p>
<p style="text-align:center;"><span style="color:#000000;"><strong>Şekil 4.</strong> Hadamard kapısının matrissel ifadesi</span></p>
<p style="text-align:center;">
<a href="/images/qcl-hadamard-one-qubit.png"><img class="aligncenter size-full wp-image-899" src="/images/qcl-hadamard-one-qubit.png" alt="" width="207" height="83" /></a></p>
<p style="text-align:center;"><span style="color:#000000;"><strong>Şekil 5.</strong> Hadamard kapısının Ket 0 ve Ket 1'e etkisi</span></p>
<p style="text-align:left;"><span style="color:#000000;"><strong>Örnek:</strong></span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">qcl&gt; qureg a[1]; // 1 qubitlik degisken tanimla
qcl&gt; dump; // bra-ket notasyonunda goster
: STATE: 1 / 64 qubits allocated, 63 / 64 qubits free
1 |0&gt;
qcl&gt; H(a); // a degiskenine Hadamard uygula
[1/64] 0.70711 |0&gt; + 0.70711 |1&gt;</pre>
&nbsp;

<hr />

&nbsp;
<p style="text-align:center;"><span style="color:#000000;"><strong>Mevcut Kütüphane ve Algoritmaların Çalıştırılması</strong></span></p>
<p style="text-align:center;"><span style="color:#000000;">QCL ile birlikte birkaç tane kütüphane ve hazır yazılmış algoritmalar gelmektedir. Bu kütüphaneler QCL'nin bulunduğu dizinde lib klasörü altında bulunmaktadır (Benim bilgisayarımda bulunduğu yer C:qcllib). Buradaki kütüphaneleri kodumuza dahil edip kullanabilmek için aşağıdaki komutları uygulamamız gerekmektedir.</span></p>
<p style="text-align:left;"><span style="color:#000000;"><strong>Örnek:</strong> Mevcut Grover arama algoritmasının çalıştırılması.</span></p>

<pre class="theme:dark-terminal toolbar:1 lang:default decode:true ">omer@OMR ~
$ cd qcl-0.6.4 //qcl nin bulundugu dizine git

omer@OMR ~/qcl-0.6.4
$ ./qcl //qcl yi calistir
QCL Quantum Computation Language (64 qubits, seed 1494971969)
[0/64] 1 |0&gt;
qcl&gt; include "grover.qcl"; //grover isimli kutuphaneyi dahil et
qcl&gt; grover(50); //grover kutuphanesinde bulunan grover() fonk. calistir
: 6 qubits, using 4 iterations
: measured 50</pre>
&nbsp;

<hr />

&nbsp;

<strong>Kaynakça:</strong>
<ul>
 	<li>[1] Bernhard Omer. Mar 27 2014. http://tph.tuwien.ac.at/~oemer/qcl.html</li>
 	<li>[2] Bernhard Omer. Jan 20 2000. Quantum Programming in QCL</li>
 	<li>[3] Brian Pursley. Dec 20 2015. https://blog.cinlogic.com/2015/12/20/running-qcl-quantum-computationlanguage-on-windows/</li>
</ul>
