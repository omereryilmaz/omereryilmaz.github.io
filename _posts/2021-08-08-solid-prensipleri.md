---
layout: post
title: SOLID Prensipleri
date: 2021-08-08 02:28
image: solid/solid-principles.png
comments: true
categories: [CSharp, ObjectOrientedProgramming, SOLID]
tags: [solid-principles, solid-principles-in-csharp, solid-prensipleri-nelerdir, csharp-ile-solid-prensipleri,  single-responsibility-principle, open-closed-principle, liskovs-substitution-principle, interface-segregation-principle, dependency-inversion-principle]
---

SOLID prensipleri, yazılım tasarımı sorunlarının çoğuyla başa çıkmamızı sağlayan tasarım ilkeleridir.  Nesneye Yönelik Programlamada (`Object Oriented Programming` - OOP) yazılım tasarımının daha anlaşılır, esnek ve bakımı kolay hale getirmek için kullanılan prensiplerden oluşmaktadır. Bu prensipler ilk defa `Uncle Bob (Robert C. Martin)` tarafından derlenmiştir.

Hayattaki diğer prensiplerde olduğu gibi, her SOLID prensibi yanlış kullanılabilir. Dolayısıyla; anlaşılabilir, bakımı kolay ve esnek bir kod yerine, SOLID prensipleriyle daha kötü ve karmaşık kodlar elde edebilmek mümkündür. Bu nedenle, dikkatli bir şekilde düşünmek ve bu ilkeleri yalnızca gerektiğinde uygulamak; temiz bir kod yazmanın temel prensibidir.

&nbsp;

#### SOLID kısaltmasını oluşturan prensipler:

- **`S`** - [Single Responsibility Principle](http://omereryilmaz.com/single-responsibility-principle) - `Class'ların iyi tanımlanmış tek sorumlulukları olmalı.`
- **`O`** - [Open / Closed Principle](https://github.com/omereryilmaz/SOLIDPrinciplesInCSharp) - `Class'lar genişlemeye açık, değişime kapalı olmalı.`
- **`L`** - [Liskov Substitution Principle](https://github.com/omereryilmaz/SOLIDPrinciplesInCSharp)  - `Base class'tan türetilenler, base class yerine geçebilmeli.`
- **`I`** - [Interface Segregation Principle](https://github.com/omereryilmaz/SOLIDPrinciplesInCSharp)  - `Küçük interface'ler oluşturularak, gereksiz metod kullanımının önüne geçilmeli.`
- **`D`** - [Dependency Inversion Principle](https://github.com/omereryilmaz/SOLIDPrinciplesInCSharp)  - `Yüksek seviyedeki class'lar düşük seviyedeki class'lara bağımlı olmamalı.`

&nbsp;

SOLID prensipleri ile ilgili basit örnekler için [SOLIDPrinciplesInCSharp](https://github.com/omereryilmaz/SOLIDPrinciplesInCSharp) GitHub reposunu inceleyebilirsiniz.

&nbsp;
&nbsp;

##### Kaynaklar
- [1] The Principles of OOD, http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod 
- [2] Robert C. Martin and Micah Martin, “Agile Principles, Patterns, and Practices in C#”, 2006.
- [3] Code Maze, https://code-maze.com/solid-principles/