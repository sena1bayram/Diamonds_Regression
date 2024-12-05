# Diamond Price Regression Project 💎

Bu proje, elmasların fiziksel ve estetik özelliklerine dayalı olarak fiyatlarını tahmin etmek için farklı regresyon algoritmalarının performansını değerlendirmeyi amaçlamaktadır. Çalışmada **KNIME** ve **Python** araçları kullanılarak analiz gerçekleştirilmiştir.

---

## 📊 Veri Seti ve Özellikleri
Proje, **Diamonds veri seti** ile gerçekleştirilmiştir. Veri setindeki başlıca özellikler şunlardır:
- **Karat (carat):** Taşın ağırlığı
- **Kesim Kalitesi (cut):** Taşın işlenme kalitesi
- **Renk (color):** Taşın rengi
- **Temizlik (clarity):** Taşın berraklığı
- **Derinlik Oranı (depth):** Derinlik ve genişlik arasındaki oran
- **Masa (table):** Taşın üst düzey genişliği
- **Fiyat (price):** Taşın satış fiyatı (hedef değişken)

---

## ⚙️ Kullanılan Araçlar ve Yöntemler
### KNIME Workflows:
1. **Eksik Veri İşleme:** Eksik değerlerin temizlenmesi veya doldurulması
2. **Kategorik Verilerin Kodlanması:** "One to Many" yöntemi ile sayısal format dönüşümü
3. **Veri Bölme:** Eğitim ve test veri seti olarak ayrım
4. **Regresyon Algoritmaları:**
   - Doğrusal Regresyon
   - Polinomsal Regresyon
   - Rastgele Orman Regresyonu
   - Gradyan Destekli Ağaçlar
   - Basit Regresyon Ağacı
5. **Performans Ölçütleri:**
   - R² Skoru
   - Ortalama Mutlak Hata (MAE)
   - Ortalama Kare Hata (MSE)
   - Ortalama Yüzdelik Hata (MAPE)

### Python Uygulamaları:
1. **Veri Hazırlığı:** Eksik veri doldurma ve kategorik değişkenlerin kodlanması
2. **Farklı Regresyon Modellerinin Uygulanması:**
   - Doğrusal Regresyon
   - Polinomsal Regresyon
   - Rastgele Orman Regresyonu
   - Karar Ağacı Regresyonu
3. **Hiperparametre Optimizasyonu:** Model doğruluğunu artırmak için hiperparametrelerin ayarlanması
4. **Performans Karşılaştırmaları ve Görselleştirme:**
   - Scatter plotlar ve Line plotlar ile model sonuçlarının görselleştirilmesi

---

## 📈 Sonuçlar
### KNIME Performans Ölçütleri:
| Model                         | R² Skoru | MAE     | RMSE    |
|-------------------------------|----------|---------|---------|
| Lineer Regresyon              | 0.858    | 874.67  | 1478.18 |
| Polinomsal Regresyon          | 0.868    | 833.99  | 1427.60 |
| Rastgele Orman Regresyonu     | 0.882    | 760.67  | 1346.83 |
| Gradyan Destekli Ağaçlar      | 0.892    | 726.07  | 1289.59 |
| Basit Regresyon Ağacı         | 0.776    | 1028.03 | 1859.75 |

### Python Performans Ölçütleri:
| Model                         | R² Skoru | MAE     |
|-------------------------------|----------|---------|
| Lineer Regresyon              | 0.923    | 718.92  |
| Polinomsal Regresyon          | -5.81    | 534.37  |
| Rastgele Orman Regresyonu     | 0.972    | 319.50  |
| Karar Ağacı Regresyonu        | 0.960    | 390.82  |

**En İyi Model:** Rastgele Orman Regresyonu, yüksek doğruluğu (R² = 0.972) ve düşük hata payı (MAE = 319.50) ile en başarılı modeldir.

**En Kötü Model:** Polinomsal Regresyon, veri setine uyum sağlayamamış ve negatif R² skoru ile başarısız olmuştur.

---

## 🔧 Çalıştırma Adımları
### Gereksinimler:
- **Python 3.x**
- Gerekli Python kütüphaneleri:
  ```bash
  pip install numpy pandas matplotlib scikit-learn
