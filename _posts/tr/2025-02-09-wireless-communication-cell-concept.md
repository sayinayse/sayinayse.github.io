---
title: "Kablosuz İletişim Temelleri: Hücre Konsepti"
date: 2025-02-09T17:05:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

Hücre konsepti temelini belirli bir coğrafi alana dikilmiş bir adet vericinin bulunmasından alıyor ve fikir 1971'de Bell Lab'tan çıkıyor.

Evvelden mobil iletişim bir adet vericinin şifresiz biçimde veriyi **<span class="hover-term" data-tooltip="broadcast">genel yayın</span>**laması şeklinde gerçekleşiyordu.

Ticari anlamda ilk hücre japonlar tarafından inşa ediliyor 1979'da.

Buradaki fikir amiyane tabirle üst üste binme doğru düzgün tabirle girişim olmadan coğrafyanın bütününü kapsamak. Altıgenler. 

---

## Avantajlar
- Daha düşük güç harcanması (yayın yapılacak alanın kısıtlanmasından mütevellit).
- Sistem kapasitesini artırmaya olanak tanıması, komşu hücrelerde aynı frekans ile yayın yapılmasa da komşu olmayan hücrelerde aynı frekans ile yayın yapılabilir. -> **<span class="hover-term" data-tooltip="frequency reuse">frekans yeniden kullanımı</span>** konsepti.

## Dezavantajlar
- Hücreleri oluşturmanın bir maliyeti var elbette.
- Hücresel devir işlemi ve getirdiği operasyonel yük.
- Kullanıcıların lokasyonunu takip etmeyi gerektirir, arama ya da mesajları yönlendirmek için.
- Komşu hücreler arasında girişim olabilir.

---

## Yozgat[^not1]'a Mobil İletişim Altyapısı Götürecektik
Yozgat'ta mobil iletişim altyapısı kurmaktan bahsetmiştik [önceki yazıda](/posts/wireless-communication-wireless-environment). Kanala dair özelliklerden ve nelerle karşılaşabileceğimizin matematiksel olarak hesaplanması gereğinden bahsetmiş. Burada bir altıgen mimaride hücresel bir mobil altyapı dizayn etmek üzerine bahsedelim.

Dizayn parametrelerimi neler olabilir?
- **Bant Genişliği**: Her bir hücreye ayrılacak toplam bant genişliği belirlenmeli (Örn. 20 MHz).
- **Kullanıcı Başına Bant Genişliği Tahsisi**: Tek bir kullanıcıya ayrılacak kanal genişliği tanımlanmalı (Örn. 100 kHz).
- **Kanal Modeli ve **<span class="hover-term" data-tooltip="Path Loss">Yol Kaybı</span>** Katsayısı**: Seçilen kanal modeline ( ) göre yapılacak analiz sonucunda yol kaybı katsayısı belirlenmeli (Örn. 𝑔 = 2).
- **Kalite Hedefleri**: Hizmet kalitesini belirlemeli **<span class="hover-term" data-tooltip="signal to interference ratio">sinyal girişim oranı</span>** tanımlanmalıdır (Örn. sesli iletişim için 10 dB SIR hedefi).
- **Hücre Yarıçapı**: Altyapı yerleşiminde her bir hücrenin kapsama yarıçapı belirlenmeli (Örn. 200 m).
- **Frekans Yeniden Kullanım Politikası**: Komşu olmayan hücrelerde aynı frekansların tekrar kullanımı için bir plan gerekir
- **Kapasite Planlaması**: Seçilen bant genişliği, kullanıcı başına tahsis ve yeniden kullanım oranına göre sistemin toplam kapasitesi hedeflenmeli.
- **Girişim Yönetimi**: Eş kanal (Co-channel) ve komşu kanal (Adjacent channel) girişimlerinin sınırlandırılması için gerekli önlemler planlanmalıdır.

> İki tip girişimle karşılaşırız böyle bir hücresel mobil iletişim altyapısında:
1. **<span class="hover-term" data-tooltip="Co-channel Interference">Eş Kanal Girişimi</span>** aynı frekansı kullanan kanallar arası
2. **<span class="hover-term" data-tooltip="Adjacent Channel Interference">Komşu Kanallar Girişimi</span>** mükemmel filtrelerimiz yok, diğer frekanslardan gelen sinyalleri de geçirebiliyor alıcılarımız.

[Kablosuz İletişim Temelleri: Bilgilendirme](/posts/wireless-communication-inform)

[^not1]: https://onedio.com/haber/sabahattin-ali-nin-1927-yilinda-ogretmenlik-yaptigi-yozgat-hakkinda-yazdiklari-burasi-beni-cildirtacak-1260204



