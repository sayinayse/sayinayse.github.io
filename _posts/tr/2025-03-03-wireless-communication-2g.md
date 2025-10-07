---
title: "Kablosuz İletişim Temelleri: 2G"
date: 2025-03-04T17:06:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

## 2G

[1G](/posts/wireless-communication-1g)’de ne yapıyorduk? Analog haberleşme ile her kullanıcı için frekans modülasyonlu kanallar ayırıyor ve ses sinyali doğrudan iletiyorduk. 

2G ile birlikte bu analog sinyalleri sayısal temsillerle ifade edip bu sayısal temsilleri iletmenin çok daha verimli olduğu görülüyor ve sayısal haberleşme kullanılıyor. Bu sayısal temsiller, aşağıdaki görselden görüleceği üzere[^not1], sürekli bir sinyalden (örneğin ses) belirli aralıkla alınan örneklerin ayrık bir dizi hâlinde tutulması ile elde ediliyor.  

![adc](/images/wireless-communication/analog-to-digital.png){: .center }

İşte [1G](/posts/wireless-communication-1g)’den 2G'ye geçişte gezgin iletişim açısından böyle devrimsel bir gelişme var. Üstelik 2G ile birlikte sadece ses sinyallerini değil metinleri de iletebilir hâle geliniyor: ([ilk SMS](https://www.vodafone.com/news/technology/25-anniversary-text-message)).

Böylece, 1990’ların başında 2G ortaya çıktı (sayısal haberleşmenin başlangıcını ise telgraf üzerinden Mors alfabesi ile iletişime kadar götürebiliriz), veri iletim hızı 300 kbps’a kadar çıkabiliyordu.  


### 2G'nin Getirdikleri

1. 2G ile farklı çoklu erişim metodları (**<span class="hover-term" data-tooltip="Time Division Multiple Access (TDMA)">zaman bölümlü çoklu erişim</span>**, **<span class="hover-term" data-tooltip="Code Division Multiple Access (CDMA)">kod bölümlü çoklu erişim</span>**) kullanıldı ki bu da verimi artırdı. 
2. Ayrıca analog frekans modülasyonu yerine daha gelişmiş sayısal modülasyon tipleri kullanıldı.  
3. Artık şifreleme yapılabilir hâle gelmişti. Daha doğrusu, şifreleme 2G ile birlikte standartlaştırılabilecek kolaylığa kavuştu. PEki 1G'de şifreleme neden daha zordu? Çünkü 1G tamamen analogtu, yani dümdüz ses sinyalini iletiyorduk bu ses sinyalini şifrelemek **<span class="hover-term" data-tooltip="frequency scrambling">frekans karıştırma</span>** gibi yöntemler var ise de bu işlem özel donanım gerektiriyor. 
4. Sayısal haberleşmenin bir diğer avantajı ise hata bulma ve düzeltme.  
5. Yeni bir servis eklendi: SMS. Yani sesin üzerine metin de kablosuz iletime dâhil edildi.  

----


<!--
Hâlâ küresel ölçekte bir standartlaşma yok:  
- Kuzey Amerika’da 2G olan sistem **<span class="hover-term" data-tooltip="Digital Advanced Mobile Phone System">D-AMPS</span>**, yani *Digital Advanced Mobile Phone System*.  
- Avrupa’da **<span class="hover-term" data-tooltip="Global System for Mobile Communications">GSM</span>**, yani *Global System for Mobile Communications*.  
- Japonya’da **<span class="hover-term" data-tooltip="Japanese Digital Cellular">JDC</span>**.  
- Birleşik Krallık'ta **Cordless Telephone 2**, eskiden 1G versiyonu **Cordless Telephone 1** olabilir mi, emin değilim.  

En yaygın ve “dişi geçen” GSM olduğundan, onunla devam edeceğiz.

#### <span class="hover-term" data-tooltip="Global System for Mobile Communications">GSM</span> / Mobil İletişim için Küresel Sistem

GSM’in bu versiyonu dört ana bileşenden oluşur:  
1. **Mobil istasyon**  
2. **<span class="hover-term" data-tooltip="Base Station Subsystem">Baz İstasyonu Alt Sistemi</span> (BSS)**  
3. **<span class="hover-term" data-tooltip="Network Subsystem">Ağ Alt Sistemi</span> (NS)**  
4. **Operasyon ve yürütme (O&M)**  

**BSS**:  
- Baz istasyonu/istasyonları (her hücre başına bir adet)  
- Ve bu baz istasyonlarını kontrol eden bir **Base Station Controller (BSC)**  
  - Hücresel devirler ve **<span class="hover-term" data-tooltip="Paging">sayfalama</span>** işlemleri ile ilgilenir  

**NS**:  
- Hücresel ağı **[[PSTN - Geleneksel Telefon Ağı]]**’na bağlar. [bkz](obsidian://open?vault=work&file=%C3%B6ylesine%2Fkablosuz%20ileti%C5%9Fim%20sistemleri%2Fgsm.png)  
- Farklı BSS’ler arasında hücresel devir olduğunda bu alt sistem ilgilenir.  
- Merkezi elemanı **<span class="hover-term" data-tooltip="Mobile Switching Center">Mobil Anahtarlama Merkezi</span> (MSC)**’dir; BSS’lerin BSC’si olarak düşünülebilir.  

#### GSM Bandı

Aşağıdaki figürden görüldüğü üzere, kullanıcıya ayrılan bant genişliği artırılmış ve taşıyıcı frekansı **800 MHz’lerden 900 MHz’lere** çıkarılmıştır (bkz. [[1G]]), böylece veri iletim oranı yükselmiştir.  

GÖRSEL 2

2G’deki çoklu erişim yapısını 1G ile kıyaslayabiliriz:  
- 1G’de insan sesi (~3 kHz) filtrelenip **30 kHz** analog frekans modülasyonu ile modüle edilip **800 MHz** taşıyıcıya bindirilip gönderiliyordu (bkz. [[1G]]).  
- 2G’de ise yine ~3 kHz civarındaki insan sesi alınır, **sayısallaştırılır**, 8 kullanıcıdan gelen veriler bir çerçeveye konur ve **GMSK** ile modüle edilip **200 kHz’lik** kanallarda erişime sunulur.  

GÖRSEL 3

Çoklu çerçeve yapısı oluşunca, çerçevelerin de bileşenleri olur:  
- Kullanıcı verisi  
- Hata kontrol bitleri (sayısal haberleşmenin nimetleri)  
- **TDMA kontrol bitleri**  

Böylece bir çoklu çerçeve **26 çerçeveden** oluşur: 24’ü trafik çerçevesi, 2 tanesi kontrol çerçevesi.  
Bu 24 trafik çerçevesinin her biri, 8 kullanıcıdan gelen slottan oluşur.  

GÖRSEL 4  

[[3G]]’lik olduk mu artık?

-->


[Evrimsel Gelişim](/posts/wireless-communication-evolution)

[^not1]: https://www.youtube.com/watch?v=OBcCZkCf-OI