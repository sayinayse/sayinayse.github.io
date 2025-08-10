---
title: "Yanlışlıkla Açığa Çıkan Gizli Belgeler: Güvenli Dizinleme"
date: 2025-02-07T17:08:30-04:00
categories:
  - Çeşitli Yazılar
tags:
  - bilgi güvenliği
---

## Arama Motorları

Arama motorları yalnızca herkese açık bilgileri bulup istemcisine getirmez. Bazen yanlış yapılandırılmış sistem ve ihmaller, gizli belgelerin de **<span class="hover-term" data-tooltip="indexing">dizinlenme</span>**sine sebep olabilir. Çok sayıda arama motoru var; bazıları belirli görevler için özelleşmiş. Örneğin, [shodan](https://www.shodan.io/) internet ağına bağlı cihazlarla ilgili sorgular yapabileceğin bir arama motoru. Burada sunucuların türlerini, sürümlerini ya da bir web sunucusu sürümünün kaç sunucu tarafından ve hangi ülkelerde çalıştırıldığını sorgulayabilir ve görebilirsin. Ya da [exploit-db](https://www.exploit-db.com/) ile spesifik bir uygulama için zafiyet sorgusu yapabilirsin. 

### Problem ne?
Peki burada sorun ne? Arama motorları gelişmiş sorgu parametreleri sunarak kullanıcıların belirli dosya tiplerini, anahtar kelimeleri veya unutulmuş açık içerikleri bulmasına imkân verebilir (örneğin Google dorking, Google hacking). Bu yöntem, düzgün yapılandırılmamış ve güvenlik önlemleri alınmamış sistemlerde erişilmesi istenmeyen, gizli içeriklerin açığa çıkmasına sebep olabilir.

Örneğin aşağıdaki sorgu, docdroid.net üzerinde “confidential” kelimesi geçen PDF dosyalarını listeliyor:

```console
site:docdroid.net "confidential" filetype:pdf
```

Yaptığım test sırasında, uluslararası bir organizasyonun “Confidential” ibaresi taşıyan bir katılımcı listesine dâhil olmak üzere üzerinde gizlilik ibaresi bulunan birçok dosyaya rastladım.
Buradaki sorun, yalnızca yetkililerin erişebilmesi gereken dosyaların arama motoru tarafından **<span class="hover-term" data-tooltip="indexing">dizinlenmesi</span>**dir.

### Örnek

Bahis olunan bu **<span class="hover-term" data-tooltip="indexing">dizinlenme</span>** hatası nedeniyle World Economic Forum Annual Meeting 2023 başlıklı, "Confidential" ibaresi taşıyan bir belgeye eriştim.
Belgede katılımcı isimleri ve e-posta adresleri bulunuyordu, ancak PDF üzerinde bu bilgiler görsel olarak siyah kutularla kapatılmıştı (ve gözden kaçan e-posta adresi de mevcuttu). Zaten bu tip görsel kapatmalar yapılsa da metni tamamen kaldırmadığı için teknik olarak geri kazanılabiliyor çoğu zaman.

Aşağıda belgenin kişisel verilerden tamamen arındırılmış, yalnızca başlık ve “Confidential” uyarısını içeren ilk sayfa görüntüsü yer almakta:

![Belge](/images/secure-indexing/redacted-confidential-file.png)

### Ne yapmalı?
Peki bu sızıntının (ve benzerlerinin) nedeni nedir ve önlemek için neler yapılabilir?

1. Yanlış robots.txt yapılandırması yapmamalı ---> Tarayıcıların bu belgelere erişiminin engellenmesi gerekir.
2. HTTP başlıkları eksik olmamalı --->  `x-robots-tag: noindex`eklenmeli.
3. **<span class="hover-term" data-tooltip="Public bucket">Açık erişimli depolama alan</span>**larında yanlış erişim yönetimi yapılmamalı.
4. Yanlış yöntemle gizleme işlemi yapılması ---> Görsel kapatma yerine metnin dosyadan kaldırılmalı ya da geri çıkarılamayacak şekilde kapatılmalı. 

