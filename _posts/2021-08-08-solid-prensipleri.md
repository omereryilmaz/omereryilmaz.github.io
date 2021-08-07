---
layout: post
title: SOLID Prensipleri
date: 2021-08-08 02:28
image: solid/solid-principles.png
comments: true
categories: [CSharp, ObjectOrientedProgramming]
tags: [solid-principles, solid-principles-in-csharp, solid-prensipleri-nelerdir, csharp-ile-solid-prensipleri,  single-responsibility-principle, open-closed-principle, liskovs-substitution-principle, interface-segregation-principle, dependency-inversion-principle]
---

SOLID prensipleri, yazılım tasarımı sorunlarının çoğuyla başa çıkmamızı sağlayan tasarım ilkeleridir.  Nesneye Yönelik Programlamada (`Object Oriented Programming` - OOP) yazılım tasarımının daha anlaşılır, esnek ve bakımı kolay hale getirmek için kullanılan prensiplerden oluşmaktadır. Bu prensipler ilk defa `Uncle Bob (Robert C. Martin)` tarafından derlenmiştir.

Hayattaki diğer prensiplerde olduğu gibi, her SOLID prensibi yanlış kullanılabilir. Dolayısıyla; anlaşılabilir, bakımı kolay ve esnek bir kod yerine, SOLID prensipleriyle daha kötü ve karmaşık kodlar elde edebilmek mümkündür. Bu nedenle, dikkatli bir şekilde düşünmek ve bu ilkeleri yalnızca gerektiğinde uygulamak; temiz bir kod yazmanın temel prensibidir.

&nbsp;

#### SOLID kısaltmasını oluşturan prensipler:

- **`S`** - [Single Responsibility Principle](http://omereryilmaz.com/single-responsibility-principle) - `Class'ların iyi tanımlanmış tek sorumlulukları olmalı.`
- **`O`** - Open / Closed Principle - `Class'lar genişlemeye açık, değişime kapalı olmalı.`
- **`L`** - Liskov Substitution Principle  - `Base class'tan türetilenler, base class yerine geçebilmeli.`
- **`I`** - Interface Segregation Principle  - `Küçük interface'ler oluşturularak, gereksiz metod kullanımının önüne geçilmeli.`
- **`D`** - Dependency Inversion Principle  - `Yüksek seviyedeki class'lar düşük seviyedeki class'lara bağımlı olmamalı.`

&nbsp;
&nbsp;

##### Kaynaklar
- [The Principles of OOD](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
- [Code Maze](https://code-maze.com/solid-principles/)
- [C-Sharp Corner](https://www.c-sharpcorner.com/UploadFile/damubetha/solid-principles-in-C-Sharp/)
- [DotNet Tricks](https://www.dotnettricks.com/learn/designpatterns/solid-design-principles-explained-using-csharp)