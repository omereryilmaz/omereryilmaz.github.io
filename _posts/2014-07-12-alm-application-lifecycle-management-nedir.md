---
layout: post
title: TFS-1 - ALM - Application Lifecycle Management Nedir ?
date: 2014-07-12 18:28
image: alm_nedir.png
comments: true
categories: [ALM]
---

<p style="text-align:justify;"><a href="/tfs-2-team-foundation-server-nedir-ne-ise-yarar/">TFS (Team Foundation Server)</a> konusuna başlamadan önce ALM ‘den biraz bahsetmemiz gerekiyor. Çünkü ALM ‘yi anladıktan sonra TFS konusunu daha da irdeleyebiliriz. Sonuç olarak TFS ‘de zaten bir ALM aracıdır.</p>
<br>


<h1>ALM Nedir ?</h1>
<p style="text-align:justify;">ALM ‘nin açılımı Application Lifecycle Management ‘dir yani Türkçe karşılığı Uygulama Yaşam Döngüsü Yönetimi ‘dir. Bir uygulamanın geliştirilmesi, büyümesi, geliştirdikten sonra müşteriden gelen feed backlere göre daha da farklılaştırılması ve yaşamını daha uzun süre devam ettirilmesi için bakımı yapılması gerekir. Bahsedilen bu işler için devamlılık arz eden bir sürece ihtiyaç vardır. ALM bunu karşılayan bir konsepttir. Aslında buradaki asıl amaç yazılım kalitesinin arttırılması ve maliyetlerin düşürülme çabasıdır.</p>

<p style="text-align:center;">
    <img src="/images/almnedir2.png"/>
</p>

<br>
<p style="text-align:justify;"> ALM içerisinde önemli yapı taşlarını barındırmaktadır. Örneğin; taleplerin yönetilmesi, ürünün yazılımsal anlamda mimarisinin çıkarılması, tasarlanması, kodlanması, test edilmesi, yaşayan süreçlerin incelenmesi, incelenme sonucunda ürünün iyileştirilmesi, bu iyileştirmeler sonucunda da yeni versiyonların çıkarılması gibi bu tarz kavramların yönetilmesini kolaylaştıran metodojilere sahiptir.</p>

<p style="text-align:justify;"> Ayrıca ALM, bir uygulamanın yaşamını tool (araç) ve process (süreç) ile destekler.</p>

<p style="text-align:justify;"><strong> Tool :</strong> İnsanların daha verimli olmasını sağlar. Böylece daha hızlı ve erken bir zamanda ürün çıkarılabilir.</p>

<p style="text-align:justify;"><strong> Process :</strong> Ürünün daha kaliteli olması noktasında izlenecek metolojileri sağlar.</p>

<p style="text-align:justify;">Yazılım metodojileri ALM 'nin ufak bir parçası olarak düşünülebilir.</p>
<br>

<h2>Yazılım Metodolojilerinden bazıları :</h2>

<p style="text-align:justify;">Waterfall, Scrum, XP (eXtreme Programing), TDD (Test – Driven Development), FDD (Feature-Driven Development), Lean, Agile, Prototype, Incremental, Iterative, V-Model, Spiral, Cleanroom, RAD(Rapid Application Development), DSDM(Dynamic System Development Model), RUP (IBM Rational Unified Model).</p>

<br>
<h2>Şekilde görüldüğü gibi ALM üç ayrı bölüme ayrılabilir;</h2>

<p style="text-align:center;">
    <img src="/images/alm_alanlari.jpg"/>
</p>

<p style="text-align:justify;">Uygulama yaşam döngüsü aslında bir fikirle başlar. Örneğin, "Şu uygulamayı neden yapmıyoruz?" gibi ve daha sonra uygulama oluşturulur. Sonraki olay uygulamanın üretime girdiği dağıtım aşamasıdır. En sonunda da uygulamanın iş değerinin kalmadığı tespiti edilir ve uygulama yaşam sonuna ulaşır. Dolayısıyla da hizmetten çıkarılır.</p>
<br>

<h2>ALM araçları ve yayınlayan firmalar:</h2>

<p style="text-align:center;">
    <table id="table-omer">
    <tr>
        <th>ALM Aracı İsmi</th>
        <th>Yayınlayan Firma</th>
    </tr>
    <tr>
        <td>Team Foundation Server</td>
        <td>Microsoft</td>
    </tr>
    <tr>
        <td>Endevor</td>
        <td>CA Technologies</td>
    </tr>
    <tr>
        <td>Centro comercial Moctezuma</td>
        <td>Francisco Chang</td>
    </tr>
    <tr>
        <td>FogBugz</td>
        <td>Fog Creek Software</td>
    </tr>
    <tr>
        <td>FusionForge</td>
        <td>FusionForge</td>
    </tr>
    <tr>
        <td>GeneXus	GeneXus</td>
        <td>Artech</td>
    </tr>
    <tr>
        <td>HP Application Lifecycle Management</td>
        <td>HP Software Division</td>
    </tr>
    <tr>
        <td>Coverity Development Testing Platform</td>
        <td>Coverity</td>
    </tr>
    <tr>
        <td>IBM Rational solution for Collaborative Lifecycle Management</td>
        <td>IBM</td>
    </tr>
    <tr>
        <td>IBM Rational Team Concert</td>
        <td>IBM</td>
    </tr>
    <tr>
        <td>Mylyn</td>
        <td>Eclipse Foundation</td>
    </tr>
    <tr>
        <td>Parasoft Concerto, Parasoft Development Testing Platform</td>
        <td>Parasoft</td>
    </tr>
    <tr>
        <td>Protecode System 4</td>
        <td>Protecode</td>
    </tr>
    <tr>
        <td>Pulse</td>
        <td>Genuitec</td>
    </tr>
    <tr>
        <td>SAP Solution Manager</td>
        <td>SAP</td>
    </tr>
    <tr>
        <td>StarTeam</td>
        <td>Borland</td>
    </tr>
    <tr>
        <td>TestTrack</td>
        <td>Seapine Software</td>
    </tr>
    <tr>
        <td>uberSVN</td>
        <td>WANdisco</td>
    </tr>
    <tr>
        <td>workspace.com</td>
        <td>Workspace Software</td>
    </tr>
    </table>
</p>

<strong>Kaynakça:</strong>
<ul>
 	<li>[1] en.wikipedia.org</li>
 	<li>[2] Burak Selim Şenyurti</li> 	
    <li>[3] David Chappell - Microsoft</li> 	
</ul>
