---
title: "Kablosuz İletişim Temelleri: İletim Temelleri"
date: 2025-02-06T12:17:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

## İletim Temelleri

### İletim Karakteristikleri

Kablosuz iletişimde üç temel iletim karakteristiğinden bahsedilebilir:

1. **<span class="hover-term" data-tooltip="Path Loss">Yol Kaybı</span>**  
   Bu, deterministik (belirlenimci) bir kayıptır ve gönderici ile alıcı arasındaki mesafeden kaynaklanır.

2. **<span class="hover-term" data-tooltip="Shadowing">Gölgelenme</span>** 

Gölgelenme rasgeledir[^not1], log-normal dağılım gösterir. Gönderici ile alıcı arasındaki engellerden kaynaklanır.

3. **<span class="hover-term" data-tooltip="Multipath Fading">Çoklu Yol Sönümlenmesi</span>** 

Bu tamamen rasgeledir. Sinyalin göndericiden çıktıktan sonra bir yerden yansıması, bir engelde sönümlenmesi, birden fazla farklı kuvvetteki kopyalarının farklı vakitlerde alıcıya varmasından kaynaklanır.

---


## **<span class="hover-term" data-tooltip="Orthogonal Frequency Divison Multiplexing">Ortogonal Frekans Bölümlü Çoğullama</span>**  

Temeli, bir bit akışını birden çok sinyalin gönderimi için bölüştürmektir.  
Bir kanalı tek bir iletime ayırmaktansa, darbantlı birden çok iletim oluşturmak.

Aşağıdaki görselde güzel bir analoji kurulmuş:  
![Ortogonallik](/images/wireless-communication/ofdm.png){: .center }

### Ortogonal frekans bölümlü çoğullamanın temel sorunu

**<span class="hover-term" data-tooltip="Inter symbol interference">Semboller arası girişim</span>** olabilir. Çünkü her bir alt taşıyıcıyı ayrı ayrı çözersin.


---

## Hücresel Ağ

Veri trafiği kapasitesi formülü ile başlayalım:

**Kapasite = Hücre Yoğunluğu × Spektrum Verimliliği × Ulaşılabilir Spektrum**

Birimlerle mühendislik dilinde açalım:

- **Kapasite**: Birim alan başına düşen trafik kapasitesi  
  *Birim:* bit/s (km² başına)  
- **Hücre Yoğunluğu**: Birim alan başına düşen hücre sayısı  
  *Birim:* hücre sayısı/km²  
- **Spektrum Verimliliği**: Bir hücrede kullanılan spektrumda birim zamanda elde edilen veri trafiği  
  *Birim:* bit/s × Hertz × hücre  
- **Ulaşılabilir Spektrum**: [Hertz](https://tr.wikipedia.org/wiki/Hertz#:~:text=Hertz%20birimi%2C%20ad%C4%B1n%C4%B1%20Heinrich%20Hertz,her%20saniye%2010%20kez%20tekrarlan%C4%B1r.)  sıklık birimi malûmunuz. Alman fizikçi Hertz'den gelme. Güzide dilimize özel isimlerin anlamsal transplantını yapamıyoruz. O yüzden hertz.


---

## Hücre Kapasitesini Artırmak

E peki bu G'lerin başındaki sayı arttıkça ne yapıyoruz?

Aslında yukarıdaki soru tam olarak aşağıda vereceğim yanıtın sorusu değil (eğer soruyu yukarıdaki gibi bırakırsam ...sonrasında - post[^not2] hoc safsatasına kurban gitmiş olurum. Doğru soru ile bir üstteki sorunun aynı temel-nedenlere farklı yollardan bağlı olma durumları var. Yani doğrudan aynı yanıtın sorusu değiller.)

Soruyu şöyle güncelleyeyim: *peki biz bu trafik kapasitesini nasıl artırıyoruz?*

- **Hücre sayısını artırmak**: belirli bir coğrafi alandaki hücre sayısını artırabiliyoruz, ki bu da daha fazla baz istasyonu dikmek oraya buraya.
- **Spektrum verimliliğini artırmak**: spektrum kullanabilme verimliliğimizi artırabiliyoruz, ki bu da aynı hücre içine daha çok verici/anten yerleştirmek oluyor. Tebrikler **<span class="hover-term" data-tooltip="multiple input multiple output">çoklu anten</span>**  sistemlerini[^not3] keşfettiniz.
- **Ulaşılabilir spektrumu artırmak**: ulaşılabilir spektrumu artırıyoruz. Bu da iletimi daha yüksek frekanslara taşımak demek. İşte G'ler arttıkça temelde artan bu.

E tabiî bu artırımların da farklı farklı maliyetleri var. Mesela kafana göre anten sayısını artırdığında çok daha fazla güç kullanman gerekebilir bir sinyali göndermen için. 

Ya da frekansı daha yüksek taşıyıcı sinyaller kullanabilirsin ama bu sefer gönderdiğin sinyaller yağmurla ve su molekülleri ile falan etkileşebilir (yani bunlar tarafından dağıtılabilir veya absorbe edilebilir). Gibi gibi.


[Kablosuz İletişim Temelleri: Bilgilendirme](/posts/wireless-communication-inform)


---

[^not1]: Rasgeleyi bilinçli yazdım: <https://www.veryansintv.com/rastgele-mi-rasgele-mi-tdkye-gore-nasil-yazilir>. Hâlâ bu şekilde kullanmakta beis görmeyen yayınevleri var (YKY).

[^not2]: **...sonrasında - post hoc safsatası:** kronolojik olarak art arda gerçekleşen iki olay arasında veri, delil ya da mantığa başvurmadan, sırf gerçekleşme sırasından kaynaklanan bir nedensellik bağı kurmaktan ileri gelir. Korelasyon biri bağımsız diğeri bağımlı iki değişken arasındaki ilişki olduğundan birbirleri ardındaki mekaznizmanın net olarak açıklanabilmesi önemli korelasyonda. Örneğin yazın dondurma tüketimi artar... Yazın evlilik sayısı da artar... O hâlde dondurmanın evliliğe neden olduğundan söz edebilir miyiz? Uğursuzlukla ilgili inançların birçoğu da kaynağını buradan alıyor.

[^not3]: Bunu nasıl kavramlaştıracağıma emin olamamıştım. Olduğu gibi çeviri ile çoklu giriş çoklu çıkış sistemleri denilebilir olsa da çoklu anten sistemlerinin kavramaya ve kullanmaya daha elverişli olduğunu gördüm yazarken. 