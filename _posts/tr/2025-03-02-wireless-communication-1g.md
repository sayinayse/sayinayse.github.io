---
title: "Kablosuz İletişim Temelleri: 1G"
date: 2025-03-02T17:06:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

## 1G

**Analog FDMA** **<span class="hover-term" data-tooltip="frequency division multiple access">frekans bölümlü çoklu erişim</span>** kullanılıyordu ve yalnızca **ses iletimi** yapılıyordu.  

Analog FDMA olması hasebiyle global bir standardı yoktu. Amerika’daki cihazın Avrupa sınırlarında çalışmaması gayet doğaldı.  

En başta *American Mobile Phone Service* idi; ardından *Advanced Mobile Phone Service* denildi ki kısaltmaları gördüğünüz üzere **AMPS** şeklinde ve eş.  

AMPS için ufak bir şema:  
![amps](/images/wireless-communication/amps.png){: .center }

Yaklaşık **800 MHz** civarında çalışıyordu.  

Aşağıda görüldüğü üzere **<span class="hover-term" data-tooltip="uplink">yukarı yönlü kanal</span>** ve **<span class="hover-term" data-tooltip="downlink">aşağı yönlü kanal</span>** için 25 MHz’lik iki adet bant tahsis edilmiş ve bu bantlar 20 kHz’lik alt kanallara bölünmüş:  

![amps-cell-bands](/images/wireless-communication/amps-cell-bands.png){: .center }

Ters iletişimin (mobilden baz istasyonuna) yapısına da bakalım:  

> *Ekstra bilgi:* İnsan kulağı 16 Hz – 20 kHz arasındaki sesleri duyar. Erkek sesi frekans değeri 100 – 8500 Hz, kadın sesi ise 150 – 10000 Hz arasında.  

1G’de ise yaklaşık **3 kHz** civarını filtreden geçirmeyi uygun görmüşler. Bunları **30 kHz’lik bant genişliğine sahip alt kanallarda**, frekans modülasyonü kullanarak **800 MHz** dolaylarına bindirip baz istasyonuna yollamışlar. Baz istasyonunda ilgili alt kanal, ilgili erişim anında ilgili aboneye tahsis edildiğinden… vesaire vesaire:  

![amps-fdma](/images/wireless-communication/amps-fdma.png){: .center }

Bence artık [2G](/posts/wireless-communication-2g)’lik olduk.  

[Evrimsel Gelişim](/posts/wireless-communication-evolution)