---
layout: post
title: Java Lambda Nedir?
date: 2017-02-08 19:36
image: java-lambda-nedir.jpg
comments: true
categories: [Java]
tags: [expression, Java, java 8 lambda expression, java 8 lambda nedir, lambda, lambda kullanımı, lambda nedir]
---
<p style="text-align:justify;">
Java, nesne-yönelimli programlamanın (object-oriented programming)  yazılım geliştirme için temel paradigma olduğu 1990’lı yıllarda nesne-yönelimli  bir programlama dili olarak tasarlanmıştır. Nesne-yönelimli programlamadan çok önce Lisp ve Scheme gibi fonksiyonel programlama dilleri olmasına rağmen akademik çevreler dışında pek rağbet görmemiştir. Son zamanlarda da fonksiyonel programlama önem kazanmıştır çünkü eşzamanlı ve olay güdümlü programlama için bu yöntem çok uygundur. Ama bu, nesne-yönelimli programlamanın kötü olduğu anlamına gelmemektedir. Aksine nesne-yönelimli programlamayla fonksiyonel programlamanın harmanlanması bu konuya daha da işlevsellik kazandırmaktadır. Örneğin programlama dilinin işlevsel ifadeler için uygun bir söz dizimi (syntax) varsa koleksiyon kütüphaneleri güçlü API’ler sunabilir. Java 8 ile gelen temel değişiklik fonksiyonel programlama yapılarının nesne-yönelimli yapının köklerine eklenmesidir [1].</p>
<p style="text-align:justify;">
Lambda ifadeleri de Java 8 ile birlikte gelen en büyük yenilik olarak görülmüştür. Ana amacı fonksiyonel programlamayı kolaylaştırarak kod geliştirmeyi veya yazmayı daha sade ve basit hale getirmeyi sağlamaktır [2]. Bir lambda ifadesi anonim bir fonksiyonun kısa bir şekilde gösterimi de diyebiliriz. Bir isme sahip değildir ancak parametre listesine, bir gövdeye ve bir dönüş tipine ayrıca da fırlatılabilecek istisnaların (exceptions) bir listesine sahiptir. Bu tanımı biraz daha anlaşılabilir olması adına açacak olursak;
</p>
<ul style="text-align:justify;">
 	<li>Anonimdir dedik çünkü bir metodun normalde sahip olacağı gibi belirgin bir isme sahip değildir.</li>
 	<li>Fonksiyondur dedik çünkü bir lambda belirli bir sınıfla bir metod gibi ilişkili değildir. Ancak bir metod gibi parametre listesi, bir gövdesi, bir dönüş tipi ve muhtemel fırlatılabilecek istisna listesine sahiptir.</li>
 	<li>Bir lambda ifadesi bir metodda argüman olarak geçirilebilir veya bir değişkende depolanabilir.</li>
 	<li>Yazımı kısadır, anonim sınıflar gibi basmakalıp uzun bir yazımı yoktur.</li>
</ul>
<p style="text-align:justify;">
Sonuç olarak kodumuzun daha net ve esnek olmasını sağlar. Örneğin lambda ifadesi kullanarak daha kısa bir şekilde özel bir Comparator nesnesi oluşturabilirsiniz [3].
</p>

<strong>Önce :</strong>
<pre>Comparator&lt;Elma&gt; agirlikOlarak = new Comparator&lt;Elma&gt;() {
public int compare(Elma e1, Elma e2){
return e1.getAgirlik().compareTo(e2.getAgirlik());
}
};</pre>
&nbsp;

<strong>Sonra (lambda ifadesiyle):</strong>
<pre>Comparator&lt;Elma&gt; agirlikOlarak =
(Elma e1, Elma a2) -&gt; e1.getAgirlik().compareTo(e2.getAgirlik());</pre>
&nbsp;
<p style="text-align:justify;">
Yukarıdaki kodların her ikisinde de Elma sınıfından üretilen nesnenin ağırlıkları karşılaştırılmaktadır. Görüldüğü üzere lambda ifadesi kullanılarak kod daha anlaşılır ve kısa hale getirilmiştir.
</p>

<p style="text-align:center;">
    <img src="/images/Lambda_ifadesi.jpg"/>
</p>
<p style="text-align:center;">
    <strong>Şekil 1.</strong> Bir lambda ifadesi parametrelereden, bir ok şeklinden ve bir gövdeden oluşmaktadır.
</p>
<br>

<ul style="text-align:justify;">
 	<li>Parametre listeleri : Buradaki iki “Elma”nın parametreleri, bir Comporator karşılaştırma metodu ile karşılaştırılır.</li>
 	<li>Lambda operatörü : Parametre listesini lambda’nın gövdesinden ayırır.</li>
 	<li>Lambda gövdesi : İki “Elma”nın ağırlıkları burada karşılaştırılır. Karşılaştırma sonucu da lambda’nın dönüş değeri olarak düşünülür.</li>
</ul>
<br>

<p style="text-align:justify;">
Bu şekildeki lambda syntax’ı Java tasarımcıları tarafından, C# ve Scala gibi benzer özellikleri taşıyan dillerde başarılı olduğu için seçilmiştir. Yukarıda da anlatıldığı üzere temel syntax;
</p>

<em>(Parametreler) -&gt; ifade</em>

Veya

<em>(Parametreler) -&gt; { ifadeler; }</em>

<br>

<strong>Lambda örnekleri :</strong>
<p style="text-align:center;">
    <img src="/images/java_lamdha_ornek.jpg"/>
</p>

<br><br>

<strong>Kaynakça:</strong>
<ul>
 	<li>[1] http://www.drdobbs.com/jvm/lambda-expressions-in-java-8/240166764</li>
 	<li>[2] https://www.tutorialspoint.com/java8/java8_lambda_expressions.htm</li>
 	<li>[3] Java 8 in Action</li>
</ul>
