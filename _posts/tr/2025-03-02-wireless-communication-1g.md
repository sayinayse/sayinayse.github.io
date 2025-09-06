---
title: "Kablosuz İletişim Temelleri: 1G"
date: 2025-03-02T17:06:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

## 1G

Birinci jenerasyon gezgin iletişim **Analog FDMA** **<span class="hover-term" data-tooltip="frequency division multiple access">frekans bölümlü çoklu erişim</span>** yapısını kullanılıyordu ve yalnızca **ses iletimi** için kullanılıyordu. 

Bu sistemin özelliği her kullanıcıya sabit bir frekans kanalı tahsis etmesi idi. 1980'leri 1G çağı olarak alacak olursak; henüz küresel bir iletişim/kanal tahsisi standardının olmadığı çağlar olarak niteleyebiliriz. Peki bu ne anlama geliyordu? Her ülke kendi frekans planını belirlediğinden ABD'de kullanılan bir telefon Avrupa'da kullanılamayabiliyordu (frekans bandlarının uyumlu olmamasından ötürü). Yani hem frekans modülasyonu hem de kanal bant genişlikleri ülkeden ülkeye değişebiliyordu kezâ bu da küresel bir sinyal formatı ve erişim yöntemi olmaması demek.

Neyse, en başta *American Mobile Phone Service* var idi; ardından *Advanced Mobile Phone Service* denildi ki kısaltmaları gördüğünüz üzere **AMPS** şeklinde ve eş.  

AMPS için ufak bir şema[^not]:  
![amps](/images/wireless-communication/amps.png){: .center }

Yaklaşık **800 MHz** civarında çalışıyordu.  

Aşağıda görüldüğü üzere **<span class="hover-term" data-tooltip="uplink">yukarı yönlü kanal</span>** ve **<span class="hover-term" data-tooltip="downlink">aşağı yönlü kanal</span>** için 25 MHz’lik iki adet bant tahsis edilmiş ve bu bantlar 20 kHz’lik alt kanallara bölünmüş[^not]:  

![amps-cell-bands](/images/wireless-communication/amps-cell-bands.png){: .center }

Ters yöndeki iletişimin (mobilden baz istasyonuna) yapısına da bakalım:  

> *Ekstra bilgi:* İnsan kulağı 16 Hz – 20 kHz arasındaki sesleri duyuyor. Erkek sesi frekans değeri 100 – 8500 Hz, kadın sesi ise 150 – 10000 Hz arasında.  

1G’de ise yaklaşık **3 kHz** civarını filtreden geçirmeyi uygun görmüşler. Bunları **30 kHz’lik bant genişliğine sahip alt kanallarda**, frekans modülasyonü kullanarak **800 MHz** dolaylarına bindirip baz istasyonuna yollamışlar. Baz istasyonunda ilgili alt kanal, ilgili erişim anında ilgili aboneye tahsis edildiğinden… vesaire vesaire[^not]:  

![amps-fdma](/images/wireless-communication/amps-fdma.png){: .center }

Bence artık [2G](/posts/wireless-communication-2g)’lik olduk.  

[Evrimsel Gelişim](/posts/wireless-communication-evolution)

[^not]: Görselleri hangi kaynaklardan aldığımı anımsamıyorum. Lokal makinemde tuttuğum notlarda olduğu şekliyle koymaktayım.