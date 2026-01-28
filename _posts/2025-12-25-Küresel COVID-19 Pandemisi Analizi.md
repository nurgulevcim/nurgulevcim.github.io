---
title: "Econ-Küresel COVID-19 Pandemisi – Ülke ve Kıta Bazlı Analiz Raporu"
date: 2025-12-25
categories:
  - Data Analysis
  - Public Health
tags:
  - covid19
  - global-health
  - data-analysis
  - pandas
  - public-policy
excerpt: "Bu çalışma, küresel COVID-19 verileri kullanılarak pandeminin ülke ve kıta bazında nasıl farklılaştığını analiz etmektedir."
---

📊 **Küresel COVID-19 Pandemisi – Analiz Raporu**  

Bu çalışma, küresel COVID-19 veri seti kullanılarak pandeminin **ülke ve kıta bazında** yayılımını, ölüm oranlarını, test kapasitesini ve nüfus etkisini analiz etmektedir.

Araştırmanın temel amacı; toplam sayılarla görünmeyen **bölgesel eşitsizlikleri**, sağlık altyapısı farklarını ve test stratejilerinin vaka tespiti üzerindeki rolünü ortaya koymaktır.

---

## 🧹 1. Veri Hazırlama ve Metodoloji  

Veri seti; ülkeler ve kıtalar düzeyinde **toplam vaka, ölüm, iyileşme, test sayıları ve nüfus bilgilerini** içermektedir.

### Ön işleme adımları:
- Eksik *Deaths* ve *Recovered* değerleri 0 ile doldurulmuştur  
- *Tests* değişkenindeki eksik gözlemler medyan ile tamamlanmıştır  
- “All” (küresel toplam) ve kıta düzeyindeki kayıtlar ülke bazlı analizlerden çıkarılmıştır  
- Tüm analizler Python (Pandas, NumPy, Matplotlib) kullanılarak gerçekleştirilmiştir  

### Türetilen göstergeler:
- Ölüm Oranı (Fatality Rate)  
- İyileşme Oranı (Recovery Rate)  
- Milyon kişi başına vaka sayısı  

Bu adımlar sayesinde betimsel analizler, karşılaştırmalar ve korelasyon analizleri güvenilir biçimde uygulanabilmiştir.

---

## 📈 2. Küresel Betimsel İstatistikler  

Dünya genelinde:
- **Toplam vaka:** ≈ 2.11 milyar  
- **Toplam ölüm:** ≈ 21 milyon  
- **Toplam iyileşen:** ≈ 1.91 milyar  
- **Toplam test:** ≈ 7.08 milyar  

Bu toplamlar üzerinden hesaplanan oranlar:
- **Global ölüm oranı:** %0.99  
- **Global iyileşme oranı:** %90.42  

Genel görünüm, küresel ölçekte vakaların büyük bölümünün iyileşme ile sonuçlandığını göstermektedir.

---

## ⚖️ 3. Ülke Bazlı Ölüm ve İyileşme Oranları  

Ülkeler bazında hesaplanan oranlar, küresel ortalamalardan belirgin biçimde ayrışmaktadır:

| Gösterge | Ortalama | Medyan |
|---|---|---|
| Ölüm Oranı | %1.38 | %0.88 |
| İyileşme Oranı | %73.6 | %97.3 |

Bu fark, bazı ülkelerde **orantısız biçimde yüksek ölüm oranları** olduğunu ve pandeminin etkilerinin ülkeler arasında homojen olmadığını göstermektedir.

---

## 🌐 4. En Çok Etkilenen Ülkeler  

### Toplam vaka sayısına göre:
ABD, Hindistan ve büyük Avrupa ülkeleri öne çıkmaktadır.

### Toplam ölüm sayısına göre:
ABD, Brezilya ve Hindistan listenin üst sıralarında yer alırken, Latin Amerika ülkelerinin ölüm yükü dikkat çekicidir.

### Nüfusa oranla (vaka / milyon):
Küçük nüfuslu ülkeler üst sıralarda yer almakta; bu durum per-capita göstergelerin nüfus büyüklüğüne duyarlı olduğunu göstermektedir.

---

## 🌍 5. Kıtasal Karşılaştırmalar  

Kıta bazlı ölüm oranları pandeminin bölgesel etkilerini açık biçimde ortaya koymaktadır:

| Kıta | Ölüm Oranı |
|---|---|
| Africa | %2.01 |
| South America | %1.95 |
| North America | %1.29 |
| Europe | %0.83 |
| Asia | %0.70 |
| Oceania | %0.22 |

Afrika ve Güney Amerika, görece düşük vaka sayılarına rağmen en yüksek ölüm oranlarına sahiptir. Okyanusya ise erken önlemler sayesinde hem vaka hem ölüm oranlarında ayrışmaktadır.

---

## 🔗 6. Test, Nüfus ve Vaka Sayıları Arasındaki İlişkiler  

### Test sayısı ↔ Vaka sayısı
- **Korelasyon katsayısı:** r ≈ 0.84  

Daha fazla test yapan ülkelerin daha fazla vaka tespit ettiği görülmektedir.

### Nüfus ↔ Vaka sayısı
- **Korelasyon katsayısı:** r ≈ 0.37  

Nüfus büyüklüğü vaka sayısını kısmen açıklasa da tek başına belirleyici değildir.

---

## 📘 7. Genel Sonuçlar ve Çıkarımlar  

- Küresel ortalamalar pandeminin etkisini olduğundan daha homojen gösterebilmektedir  
- Test kapasitesi, tespit edilen vaka sayısında kritik rol oynamaktadır  
- Ölüm oranları, yalnızca vaka sayısıyla değil sağlık altyapısı ile de ilişkilidir  
- Pandemiye yönelik politikaların **bölgesel ve ülke-özel** tasarlanması gerekmektedir  

---

## 🧠 Son Değerlendirme  

Bu analiz, COVID-19 pandemisinin tek tip bir küresel deneyim olmadığını; aksine ülkeler ve kıtalar arasında ciddi farklılıklar barındırdığını göstermektedir.  
Veri, pandeminin yalnızca biyolojik değil, aynı zamanda **yapısal ve politik bir kriz** olduğunu açıkça ortaya koymaktadır.

---

🔗 **Proje Dosyaları**  
Bu analizde kullanılan notebook ve görseller GitHub’da yer almaktadır:

👉 https://github.com/nurgulevcim/covid19-global-country-continent-analysis

Hazırlayan: Nurgül Evcim

_Data Analyst
