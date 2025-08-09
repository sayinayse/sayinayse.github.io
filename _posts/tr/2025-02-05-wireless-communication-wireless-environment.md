---
title: "Kablosuz İletişim Temelleri: Kablosuz Ortamın Nitelikleri"
date: 2025-02-07T17:08:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

## Kablosuz İletim
Sinyali havadan iletmek harika bir fikir elbette, ama fazla unsurla al-veri var.

Peki ne gibi unsurları var bu işin? Mesela hangi fiziksel durumlardan etkilenir? 

Örneğin mühendis olarak Yozgat'a baz istasyonu dikip bir iletişim altyapısı kurmamız istendi. Bu iletişimin kalite ve servisine dair beklentiler sunuldu ve anlaşma yapıldı. Bu aşamada neleri hesap edip planlarız?  

Antenin dizaynı, sinyalin işlenip modüle edilmesi gibi adımları konumuzun kablosuz iletişim unsurları olmasından mütevellit geçiyorum, diyelim ki bu baz istasyonu dikildi ve artık sinyal gönderebiliyorum.

Bu sinyalin başına kablosuz iletim ortamında neler gelebilir?
1. Düz bir yüzeyden yansıyabilir (refraktasyon hali).  
2. Bir objenin içinden geçip iletim sürecini sürdürebilir.  
3. Bir yüzey üzerinde saçılabilir.  
4. Bir yüzeyin köşesine çarpıp difraksiyon (yön değiştirme) olabilir.

Bu soruları hakkıyla yanıtlamak ve sinyalinizin başına neler gelebileceğini tahmin edebilmek için matematiksel temsiller ile sinyali ve ortamı modellemeniz gerekiyor tabiî.

## Matematiksel Temsil 

Bu matematiksel temsil başlı başına büyük bir konu. Bir elektromanyetik dalganın matematiksel temsile indirgenmesi/modellenmesi hususundan devğil de konseptin kendisinden bahsediyorum büyük bir konu derken.


Russell'ın 20. yüzyıl başında ortaya attığı *berber* ya da *kendini içeren küme* paradoksu matematiksel ifadenin çelişkili ibareler içerebileceğini ortaya koyuyor. Hilbert bu paradoksların yarattığı çelişkinin ilgili paradoksların günlük dille ifade edilmesinden neşet ettiğini düşünerek matematiği sonlu bir küme olarak tarif ediyor. Yani temel amacı sonu olan bir aksiyomlar kümesi olarak matematik tanımı yapmak (aslına bakarsanız yapay zekânın çıkışı da buraya dayanıyor, insan düşüncesinin biçimsel/formal yapı olarak ifade edilebilirliği). Burada -Gödel öncesinde- var olan bir umut var *şeylerin* **tam** ve **tutarlı** olarak biçimselleştirilebileceği, formalize edilebilirliği üzerine. Gödel bir matematiksel ifadenin aynı anda **tam** ve **tutarlı** olamayacağını [ispat edince](https://en.wikipedia.org/wiki/G%C3%B6del%27s_incompleteness_theorems) buradaki keşif inancı hâlini sonlandırıyor tabiî. 


Yani somut bir örnekle açıklayacak olursam: **sıfıra bölme işlemi**. Bir sayının sıfıra bölünmesi işlemi bölme operasyonunda tanımlı değil. Yani her bölme operasyonu için *tutarlı* bir sonuç elde edemiyorum ta ki bir sayının 0'a bölümünü tanım gereği tanımsız ya da sonsuza eşleyip o sistemi, *tam* yapana değin.


Neyse, bu yazı [Tristram Shandy](https://books.googleusercontent.com/books/content?req=AKW5QacxDC2wq-puWTQWlCeAil63MS1xREIopv71GgmmN4qn0Sh7KmZwZShGuIEOnKGTauZ9ko4oIysD2d1PmKjr_x3bfT977rZKTyibxLxHKWDo85zIcSZcY7eBdiPWU-iYOTJCix0tAZd-1dos9FJM5M5rZN99shQXpRwDVeQgwuhxR718kV0f8bQjKHZTiq8NIAdqn9dxzV8frmN8gvtwlPRdKmfLT2zDh2mh4tNaWu0zt572rF4jFBeXLA_p4C2jfPdq3Zs9vFS9fddeZzTLjkeaHUCiLyskD1D-Sq-suausPqABaP4)'sel bir anlatıya dönüştü. Kaldığımız yeri kısaca özetleyip daha sonra devam etmek üzere diyeyim: 

Baz istasyonumuzu diktik. Antenimiz var. Hattâ işaretlerimizi kodlayabilmiş (1 ve 0'larla belirli kurallara göre temsil edebilir) hâldeyiz. Bize düşen artık bu kodlanmış sinyali kablosuz ortamda, havada, iletmek istiyoruz. 
Bu uğraşa girebilmek için tutarlı ve matematiksel bir temsil yaratmamız şart dedik[^not1].



[Kablosuz İletişim Temelleri: Bilgilendirme](/posts/wireless-communication-inform)

[^not1]: En son burada bırakmışım. Kağıt üzerinde karaladığım işlemleri düzgün ve anlaşılır hâle getirmek ve buraya öyle taşımak gerekecek. Şimdilik burada bırakıp karmaşık sayıların sağladığı temsiliyet TikTok'tan video izlemenizi sağlıyor gençler diyeceğim.