# 🏎️ Mercedes-Benz Greener Manufacturing (Test Süresi Optimizasyonu)

Bu proje, fabrikadan çıkacak Mercedes-Benz araçlarının konfigürasyon özelliklerine bakarak, güvenlik ve kalite kontrol testlerinin toplam süresini saniye cinsinden tahmin eden bir endüstriyel regresyon modelidir.

---

## 📊 Proje Özeti & Metrikler

* **Problem Türü:** Regresyon (Regression)
* **Veri Yapısı:** Çok boyutlu (300+ anonim öznitelik), kategorik ve ikili (binary) yapısal tablo verisi.
* **Değerlendirme Metriği:** **$R^2$ Skoru (Belirlilik Katsayısı)**
  * *Proje Başarısı:* Geliştirilen optimizasyon modeli test verileri üzerinde **0.7538** $R^2$ skoru yakalayarak yüksek açıklayıcılık gücü sunmuştur.

---

## 🛠️ Uygulanan Mühendislik Adımları

1. **Sentetik Veri Modellemesi:** Güvenilir ve çok boyutlu endüstriyel regresyon verisi, varyans ve gürültü parametreleri (`noise=8.5`) eklenerek gerçeğe en yakın şekilde simüle edilmiştir.
2. **Özellik Mühendisliği:** Anonim kategorik sütunlar `LabelEncoder` mimarisiyle modele uygun hale getirilmiş, test süreleri saniye bazlı ölçeklenmiştir.
3. **Model:** Scikit-Learn `RandomForestRegressor` kullanılarak kararlı ve overfitting korumalı bir yapı kurulmuştur.

---

## 🚀 Canlı Uygulama (Deployment)

Proje, **Hugging Face Spaces** üzerinde **Streamlit** mimarisi kullanılarak canlıya alınmıştır. Kullanıcılar araç segmenti ve donanım paketlerini seçerek üretim bandındaki beklenen test süresini anlık olarak optimize edebilirler.
