---
title: "Kablosuz İletişim Temelleri: Sinyal İletiminde Kayıp Etkisi"
date: 2025-02-09T17:06:30-04:00
categories:
  - Kablosuz Haberleşme
tags:
  - kablosuz iletişim
---

Sinyal/elektromanyetik dalga enerjisinin uzayda iletimi sırasında kaybettiği enerjiyi matematiksel olarak modelleyeceğiz/hesaplayacağız?

---

## Boş Uzay – Görüş Hattı – Free Space – LOS Modeli

Sinyal veya elektromanyetik dalga enerjisinin boş uzayda iletimi sırasında uğradığı **güç kaybını** modeller. Yani bu model, **<span class="hover-term" data-tooltip="Line-of-Sight">doğrudan görüş hattı</span>** ilerleyen bir dalganın kaybettiği gücü inceler. Bu güç kaybı nelere bağlıdır?

- Sinyalin çıkış gücü
- Kullanılan sinyalin **<span class="hover-term" data-tooltip="hayır sıklık demeyeceğim">frekansı</span>**
- İletim mesafesi (kaynağın hedefe uzaklığı)

Bu sözel ifadelerin matematiksel ifadesi:

![yol-kaybi](/images/wireless-communication/path-loss.png){: .center }


> **Not:** Birimlerle uğraşmak önemli. Burada desibel kullanımı lineer ölçekten logaritmik ölçeğe geçmek için. Böylece lineer ölçekte çarpma bölme fonksiyonlarıyla eylediklerini logaritmik ölçekte toplama çıkarma ile eyleyebilir ve kayıp-kazanç analizi yapabilirsin.


Tabii ki sinyaller genelde boş uzayda iletilmez, bu yüzden başka kayıp modelleri de vardır.

---


### Genel Işın İzleme - General Ray Tracing

Bu modelde:

- Yansımalar
- Dağılmalar
- **<span class="hover-term" data-tooltip="diffraction">Kırınımlar</span>**/yön değiştirim? 
hesaba katılır.

Hâlâ maxwell denkleriyle uğraşmaktan daha kolay. Farklı bileşen sayılarını hesaba katan ışın izleme modelleri olabilir:

1. *2-bileşenli ışın izleme*'de doğrudan görüş hattından gelen sinyal ile yerden sekip gelen sinyali hesaba katarsın.
2. diyelim ki *10-bileşenli izleme* yaptık. doğrudan görüş hattından gelen, yerden seken, yerden sekip başka bir yere çarpıp oradan seken... gibi gibi bileşenler de hesaba katılır.

---

### [Gerçek Hayat](https://www.youtube.com/watch?v=g8X0s_kGgCM&list=RDg8X0s_kGgCM&start_radio=1) 
Ama bu modeller hâlâ bir kablosuz iletişim sistemini modellemek için yeterli değil. Bu sebeptendir ki ne boş uzay sinyal kaybı hesabı ne de ışın izleme bir başına bu hesaplarda kullanılmaz.

Peki neler kullanılır?

Deneysel olarak belirlenmiş katsayı ve modellerle yürütülür: 

*okumura modeli*, *hata modeli*
Şehir ya da kırsal alanlarda belirli frekans aralıklarına sahip sinyallerin kayıplarını modelleyip bir  **<span class="hover-term" data-tooltip="cheat sheet">kopya kağıdı</span>** olarak sunulur. Bu hesaplar deney tabanlı metriklerin belirlenmesi ve bunlar üzerine analitik yaklaşım/hesapların yapılmasıyla sürdürülür.

Örnek olarak, iç mekanda 1200 hz sinyal duvara tosladığında 5-20 dbm güç kaybeder, pencereden geçtiğinde 3 kilo güç kaybına uğrar gibi. 

---

### Kayıp Modellerinin Genel Değerlendirmesi

- **Maxwell denklemleri:** Fazla karmaşık, pratik değil.
- **Doğrudan görüş hattı modeli:** Fazla basit.
- **Işın izleme modeli:** Çevreye dair ayrıntılı bilgi gerektirir.
- **Deneysel modeller:** Tüm ortamlar için genellenemez.
- **Basitleştirilmiş güç kaybı modelleri:** Sistem düzeyinde genel içgörü sağlar ancak detaylandırma gerekebilir.

---

### kayıplar: kapsam alanı vs. bant genişliği al-veri
Bir kere yüksek frekanslarda iletimi sağlamak için gerekli donanımsal altyapı hem üretim hem de kullanım açısından daha maliyetli. Ama daha fazla bilgi iletimi de yapmana olanak sağlıyor. Bu bir **<span class="hover-term" data-tooltip="tradeoff">al-ver dengesi</span>**.

Örneğin:  
**800 MHz** (1G civarı) bir sinyali iletmek, **3.5 GHz**’lik bir sinyali iletmeye kıyasla **~20 kat daha az güç** gerektiriyor.

Neyse biz devam edelim. Detaylarına girmeden bazı kavramları sıralayacağım. İhtiyaç durumunda derinlemesine bakılabilir.

---

### **<span class="hover-term" data-tooltip="Shadowing">Gölgelenme</span>** 
Bu model engellerle sönümlenen ve yoluna devam eden sinyali modellemek için kullanılır. Pratikte ise yine basitleştirilmiş hesabı kullanılır.

### Doppler Kayması
alıcının göndericeye referansla (ya da tam tersi) hareket ettiği durumlarda.

### **<span class="hover-term" data-tooltip="Multipath Fading">Çoklu Yol Sönümlenmesi</span>**

### **<span class="hover-term" data-tooltip="Delay Spread">Gecikme Yayılımı</span>**
Yansıyan yüzeeylerden alıcıya ulaşan yan sinyallerden kaynaklanır.

Bu sebeple iletim (sıklığı) oranı düşük tutulmak zorunda kalınabilir.

### **<span class="hover-term" data-tooltip="Coherent Bandwidth">Uyumlu Bant Genişliği</span>**
Tabiî sinyaller farklı yolak ve zamanlarda alıcıya ulaşabilrdiği için, alıcı tarafında sinyali işleyebilmek için sinyalin tutarlı kaldığı bir band genişliği/zaman aralığı üzerine hesaplar da yapılmalı.

Bu kavramdan bahsettikten sonra [kanal modelleri](/posts/wireless-communication-wireless-channel-models) üzerine konuşmak/düşünmek iyi olur.


[Kablosuz İletişim Temelleri: Bilgilendirme](/posts/wireless-communication-inform)