layout: single
title: "Piyasa-Social Media Algorithms & Consumer Behavior – Analysis Report"
date: 2025-11-22
categories: [piyasaarastirmalari1]
categories:
  - Piyasa_Arastirmalari
---

---

# 📊 Sosyal Medya Algoritmaları ve Tüketici Davranışı – Analiz Raporu

Bu çalışma, **“Impacto dos Algoritmos das Redes Sociais no Comportamento de Consumo”** veri seti kullanılarak,
sosyal medya algoritmalarının tüketicilerin satın alma kararları üzerindeki etkisini analiz etmektedir.

Araştırmanın temel amacı; algoritmik kişiselleştirme, fiyat dinamikleri, sosyal onay mekanizmaları ve influencer etkilerinin
tüketici davranışlarını nasıl şekillendirdiğini ölçmektir.

---

## 🧹 1. Veri Hazırlama ve Metodoloji

Veri seti, Portekizce olarak hazırlanmış Likert ölçekli anket yanıtlarından oluşmaktadır.  
İstatistiksel analiz yapılabilmesi için tüm Likert ifadeleri **1–5 arası sayısal ölçeğe** dönüştürülmüştür.

- **Kodlama şeması:**  
  (1) Kesinlikle Katılmıyorum … (5) Kesinlikle Katılıyorum  
- **Ön işleme adımları:**  
  - Kolon adlarındaki Unicode karakter sorunları temizlenmiştir  
  - Eksik veri kontrolü yapılmıştır  
  - Analizler Python (Pandas, Statsmodels) kullanılarak gerçekleştirilmiştir  

Bu adımlar sayesinde korelasyon, segmentasyon ve regresyon analizleri güvenilir biçimde uygulanabilmiştir.

---

## 📈 2. Betimsel İstatistikler (Ortalama Etki Düzeyleri)

En yüksek ortalamaya sahip ifadeler, sosyal medyanın fiyat algısı ve sosyal onay mekanizmalarındaki güçlü rolünü ortaya koymaktadır:

1. **Sosyal Onay:**  
   “Diğer tüketici yorumlarını dikkate alırım” (Ort. = 4.74)
2. **Fiyat Rekabeti:**  
   “Sosyal medyada daha iyi fiyat bulduğum için fiziksel mağazadan vazgeçtim” (Ort. = 4.72)
3. **Yerel Ticaret Potansiyeli:**  
   “Yerel mağazalar kişiselleştirilmiş reklam verseydi onlardan alışveriş yapardım” (Ort. = 4.69)
4. **Ekonomik Motivasyon:**  
   “Fiyat online alışverişte temel motivasyonumdur” (Ort. = 4.49)
5. **Algoritmik Farkındalık:**  
   “Algoritmalar zevklerimi ve tercihlerimi tanıyor” (Ort. = 4.29)

**Genel Değerlendirme:**  
Tüketiciler algoritmik kişiselleştirmenin farkındadır ve satın alma kararlarında
öncelikle fiyat avantajı ve diğer kullanıcı yorumlarını dikkate almaktadır.


---

## 🔥 3. Korelasyon Analizi (Davranışsal Yapılar)

Korelasyon ısı haritası, değişkenler arasındaki güçlü ilişkileri açık biçimde göstermektedir.

**Öne çıkan ilişkiler:**
- Algoritmalar tarafından “tanınma” algısı ↔ Kişiselleştirilmiş reklamların etkisi  
- Influencer tavsiyeleri ↔ Reklamlardan etkilenme düzeyi  
- Online alışverişin pratikliği ↔ Satın alma sıklığı  

Bu ilişkiler üç temel davranışsal yapıyı işaret etmektedir:

1. Algoritmik kişiselleştirme etkisi  
2. Influencer / sosyal onay etkisi  
3. Online alışveriş kolaylığı  

Bu yapılar, segmentasyon analizinde de tutarlı biçimde doğrulanmıştır.

---

## 🎯 4. Davranışsal Segmentasyon (K-Means)

K-Means kümeleme analizi sonucunda üç farklı tüketici segmenti belirlenmiştir:

### Segment 0 – *Bilinçli Değerlendirici* (n = 25)
Fiyat ve yorum odaklı, influencer etkisine daha mesafeli tüketiciler.

- Yorum ve değerlendirmelere yüksek önem verir  
- Fiyat karşılaştırmasına duyarlıdır  
- Influencer etkisi düşüktür  
- Rasyonel ve analitik alışveriş davranışı sergiler  

### Segment 1 – *Algoritma Etkisine Açık Alıcı* (n = 13)
Kişiselleştirilmiş reklam ve influencer önerilerinden güçlü biçimde etkilenen tüketiciler.

- Kişiselleştirilmiş reklamlara yüksek tepki verir  
- Influencer tavsiyeleri satın alma olasılığını artırır  
- Dijital içerik akışına duyarlıdır  
- “Kolay tetiklenen” tüketici profili  

### Segment 2 – *Pratik Online Tüketici* (n = 56)
En geniş segmenttir; temel motivasyon hız ve kolaylıktır.

- Ana motivasyon: pratiklik ve zaman tasarrufu  
- Online alışverişi kolay olduğu için tercih eder  
- Kişiselleştirme etkisi orta düzeydedir  
- Influencer etkisi görece düşüktür  


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

## 📘 6. Genel Sonuçlar ve Stratejik Çıkarımlar

- **Platform Değil Mekanizma:**  
  Kruskal–Wallis testleri, platformlar (Instagram, TikTok, YouTube) arasında anlamlı bir fark olmadığını göstermiştir *(p > 0.05)*.  
  Bu durum, etkinin platformdan ziyade **algoritmik kişiselleştirme mekanizmasından** kaynaklandığını ortaya koymaktadır.

- **Algoritmik Güven:**  
  Tüketicilerin algoritmalar tarafından “tanınma” hissi, satın alma dönüşümünü doğrudan artırmaktadır.

- **Segment Bazlı Strateji:**  
  Pazarlama yaklaşımları:
  - Influencer odaklı tüketiciler (Segment 1)
  - Fiyat ve pratiklik odaklı tüketiciler (Segment 2)  
  için ayrı ayrı tasarlanmalıdır.

---

## 🧠 Son Değerlendirme

Bu analiz, algoritmaların yalnızca teknik araçlar değil,  
tüketici kararlarını yaklaşık **%64 oranında açıklayan psikolojik yönlendiriciler** olduğunu göstermektedir.

## 🔗 Proje Dosyaları

Bu analizde kullanılan notebook ve görseller GitHub’da yer almaktadır:

👉 https://github.com/nurgulevcim/social-media-algorithmic-influence

Hazırlayan: **Nurgül Evcim**  
_Data Analyst
