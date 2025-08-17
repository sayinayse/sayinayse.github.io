---
title: "Kablosuz İletişim Temelleri: Kanal Modelleri"
date: 2025-02-09T17:07:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

Kablosuz iletişimde kanal modelleri, ortamdan eklenen gürültüye ve kanalın yarattığı <span class="hover-term" data-tooltip="fading">sönümlenme</span> türüne göre değişiklik gösterir.

---

## <span class="hover-term" data-tooltip="Additive White Gaussian Noise (AWGN) Channel">Toplamalı Beyaz Gauss Gürültü Kanalı</span>

Şimdi sönümlenme olmadan bir iletim olduğunu düşünelim -> ki bu da verici ve alıcının aynı lokasyonda olduğu anlamına gelir. 

- Toplamalı çünkü sinyale bir gürültü *eklenir*.
- Beyaz Gaussian gürültü çünkü sinyale bütün *frekanslara eşit etki eden* bir gürültü eklenir.

Şimdi verici ve alıcı arasına bir mesafe soktuğumuz durumlara bakalım aşağıdaki alt bölümlerde.

---

## <span class="hover-term" data-tooltip="Slow-Varying Frequency-Flat Fading Channel">Yavaş Değişen Düz Sönümlü Kanal</span>

Bu senaryoda verici ve alıcı arasında <span class="hover-term" data-tooltip="interference loss">girişim kaybı</span> ve <span class="hover-term" data-tooltip="shadowing">gölgelenme</span> var. Bu etkiler, sinyalin gücünü azaltıyor.

Bkz: Sinyal İletiminde Kayıp Etkisi

---

## <span class="hover-term" data-tooltip="Slow-Varying Frequency-Selective Fading Channel">Yavaş Değişen Frekans Seçimli Sönümlü Kanal</span>

Hem yansımanın, hem saçılmanın , hem doğrudan görüş hattından gelen sinyalin olduğu kanallar. Çoklu yollardan gelen sinyal alıcıya ulaşıyor yani. Alıcının yerinin değişmesi yapıcı ya da yıkıcı sinyal değişimlerine sebep olabilir çünkü yansıyan da geliyor saçılan da.

Bu kanal, iki bileşeni birlikte değerlendiriyor:

1. **<span class="hover-term" data-tooltip="large-scale fading">geniş ölçekte sönümleme</span>** -> <span class="hover-term" data-tooltip="path loss">yol kaybı</span>, <span class="hover-term" data-tooltip="shadowing">gölgelenme</span>, <span class="hover-term" data-tooltip="interference Loss">girişim kayıpları</span> gibi göreceli olarak uzun mesafelerde baskın olan etkiler.

2.   
**<span class="hover-term" data-tooltip="small-scale fading">dar ölçekte sönümleme</span>**leri hesaba katar. -> <span class="hover-term" data-tooltip="Multipath Loss">çoklu yol</span>, ortam nesnelerinin yer değişimi gibi kısa mesafeli etkiler.  

> *<span class="hover-term" data-tooltip="Slow-Varying">slow varying</span>* Kanal zamanla çok değişmez.  
> *<span class="hover-term" data-tooltip="Frequency-Selective">frequency selective</span>* inyalin farklı frekans bileşenleri kanalda farklı etkilenir (vericiden gönderilen sinyalin frekansı değişince ortamda maruz kalacağı muamele de değişebilir).

---

## <span class="hover-term" data-tooltip="Fast-Varying Frequency-Selective Fading Channel">Hızlı Değişen Frekans Seçimli Sönümlü Kanal</span>


Bir önceki senaryoda vericinin, alıcının, ortamdaki nesnelerin birinin ya da birden fazlasının hareketli olduğu durumlarda karşılaştığımız iletim ortamına bu ismi vermişler. çünkü kanal *zamanla değişiyor.*

--- 

Özet: 
![channel-models](/images/wireless-communication/channel-models.png){: .center }

> **Not:** Burada bir alt not düşmek isterim. Diyelim kanalımız frekans seçimli fakat bizim sinyalimizin bant genişliği bu seçimli frekans aralığından daha dar. O zaman gönderdiğimiz sinyal *frekans seçimli olmayan* bir davranış gösterebilir. İlgili yardımcı görsel: 
![[frekans seçimli-seçimsiz.png]]
![channel-models1](/images/wireless-communication/channel-models1.png){: .center }

---

[Kablosuz İletişim Temelleri: Bilgilendirme](/posts/wireless-communication-inform)