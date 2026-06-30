---
layout: single
title: "E-commerce Customer Behavior – Analysis Report"
date: 2025-11-22
categories:
  - Piyasa_Arastirmalari
---

---

# 📊 E-ticaret Müşteri Davranışı Analizi -Rapor

Bu çalışma, **IEcommerce_Consumer_Behavior_Analysis_Data.csv** veri seti kullanılarak, bir e-ticaret veri seti üzerinden müşteri davranışlarını anlamak, segmentlere ayırmak ve segment bazında stratejik içgörüler üretmek amacıyla oluşturuldu. Analizde, alışveriş sıklığı (Frequency), toplam harcama (Monetary) ve davranışsal değişkenler birlikte incelendi.


---

## 🧹 1. Veri Hazırlama ve Temizleme

Veri içindeki para birimi sembolleri temizlenerek Purchase_Amount sayısal formata dönüştürüldü. Sosyal medya etkisi ve reklam etkileşimi bilgilerindeki eksikler "None" olarak dolduruldu. Böylece segmentasyon ve davranış analizi için veri tutarlı hâle getirildi.
 
- **Ön işleme adımları:**  
  - Kolon adlarındaki Unicode karakter sorunları temizlenmiştir  
  - Eksik veri kontrolü yapılmıştır  
  - Analizler Python (Pandas, Statsmodels) kullanılarak gerçekleştirilmiştir  

Bu adımlar sayesinde korelasyon, segmentasyon ve regresyon analizleri güvenilir biçimde uygulanabilmiştir.

---

## 📈 2. FM Segmentasyonu

FM segmentasyonu, müşterilerin alışveriş sıklığı (F) ve harcama düzeyi (M) üzerinden üçer gruba ayrılmasıyla oluşturuldu.
Örneğin:
•	33 → En sık alışveriş yapan + en çok harcayan
•	11 → En az alışveriş yapan + en az harcayan
•	13 → Az alışveriş yapıp yüksek tutarda harcayan
Bu yapı, müşteri değerini anlamak için güçlü bir temel sağladı.


---

## 🔥 3. Davranış Analizleri

Her FM segmenti için davranış kalıplarını incelemek amacıyla çubuk grafikler oluşturuldu.
→ Discount Sensitivity
Düşük değer segmentlerinin daha çok indirimle motive olduğu görüldü.
Yüksek değer segmentlerinde indirim beklentisi daha düşüktü.
→ Purchase Channel
Bazı segmentlerin web ağırlıklı, bazılarının ise mobil uygulama üzerinden alışveriş yaptığı belirgin şekilde ayrıştı.
Bu durum kanal bazlı pazarlama için kritik bir veri sunuyor.
→ Device Usage
Cihaz kullanımında segmentler arasında ciddi farklar gözlendi.
Örneğin bazı segmentler tablet ağırlıklı alışveriş yaparken diğerleri tamamen mobil ağırlıklıydı.
→ Category Preference
Segmentlere göre kategori davranışları belirgin şekilde farklılaştı.
Bu içgörü, kampanya planlama ve ürün önerileri için değerli.
→ Brand Loyalty
Bazı segmentler düşük harcamalarına rağmen yüksek sadakat gösterdi.
Bazıları ise yüksek harcamaya rağmen düşük sadakatteydi → churn riski yüksek.
→ Ads Engagement
Reklamlara verilen tepkiler segment bazlı incelendiğinde, bazı yüksek değer segmentlerinin reklamlara beklenenden daha açık olduğu görüldü.
→ Social Media Influence
Sosyal medya belirli segmentlerde güçlü bir etkileyici faktörken, bazı segmentlerde tamamen etkisizdi.


---

## 🎯 4. Genel Değerlendirme

Bu analiz, e-ticaret için şu stratejik sorulara yanıt veriyor:
•	Hangi segmentler yüksek değerli müşteriler?
•	Kimler indirim bağımlısı?
•	Kim hangi kanaldan alışveriş yapıyor?
•	Hangi segment sosyal medya üzerinden etkileniyor?
•	Sadık ama düşük harcayan “fırsat segmentleri” hangileri?
•	Reklam hedeflemeleri kimlere yapılmalı?
Bu sonuçlar, CRM, hedefleme, öneri sistemleri ve pazarlama stratejileri için güçlü bir temel oluşturuyor.


---

## 📉 5. Algoritma Etkisi Endeksi ve Nedensel Analiz

Algoritma algısını ölçen beş madde birleştirilerek **Algoritma Etkisi Endeksi** oluşturulmuştur.  
Faktör analizi, endeksin **tek boyutlu bir yapı** sergilediğini doğrulamıştır.

### Regresyon Analizi Sonuçları

Kurulan doğrusal regresyon modeli istatistiksel olarak anlamlıdır  
*(F(1,92) = 161.1, p < 0.001)*.

- **Açıklanan varyans (R²):** 0.637  
  → Satın alma kararlarındaki varyansın yaklaşık **%64’ü** açıklanmaktadır.  
- **Standartlaştırılmamış katsayı (B):** 1.03  
  → Algoritma etkisindeki 1 birimlik artış, satın alma kararı üzerinde 1.03 birimlik artış yaratmaktadır.  
- **Standartlaştırılmış katsayı (β):** 0.80  
  → Etki büyüklüğünün **çok güçlü** olduğunu göstermektedir.


---


## 🔗 Proje Dosyaları

Bu analizde kullanılan notebook ve görseller GitHub’da yer almaktadır:

👉 GitHub https://github.com/nurgulevcim/ecommerce-customer-segmentation


Hazırlayan: **Nurgül Evcim**  
_Data Analyst
