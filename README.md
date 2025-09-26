# Meyve ve Sebze Sınıflandırma (CNN)

## 📌 Projenin Amacı
Bu projenin amacı, derin öğrenme yöntemlerini kullanarak farklı meyve ve sebzelerin görüntülerini sınıflandırmaktır. Görüntü tabanlı sınıflandırma sayesinde tarım, perakende ve gıda endüstrisinde ürün tanıma ve kalite kontrol süreçlerinin otomatikleştirilmesi hedeflenmektedir.

## 📂 Veri Seti Hakkında
Proje kapsamında kullanılan veri seti, çeşitli meyve ve sebze sınıflarına ait görüntülerden oluşmaktadır.  
- Görseller **etiketli** şekilde sınıflara ayrılmıştır (ör. elma, muz, domates vb.).  
- Eğitim, doğrulama ve test setleri olacak şekilde ayrıştırılmıştır.  
- Görseller farklı açılardan ve ışık koşullarında çekilmiştir, bu da modeli daha genellenebilir hale getirmektedir.

## 🛠 Kullanılan Yöntemler
- **Veri Ön İşleme:**  
  - Görseller yeniden boyutlandırıldı.  
  - Normalizasyon ve veri artırma (augmentation) uygulandı.  

- **Modelleme:**  
  - Convolutional Neural Network (CNN) mimarisi denendi.  
  - Transfer learning için **EfficientNetB0** tabanlı model kullanıldı.  

- **Eğitim:**  
  - Model, `categorical_crossentropy` kayıp fonksiyonu ve `Adam` optimizasyon algoritması ile eğitildi.  
  - Erken durdurma (early stopping) ve model kaydetme (checkpoint) teknikleri kullanıldı.  

## 📊 Elde Edilen Sonuçlar
- **Sıfırdan CNN modeli:**  
  - Eğitim doğruluğu: %95+  
  - Doğrulama doğruluğu: ~%61  
  - Test doğruluğu: **%60**  

- **EfficientNetB0 (Transfer Learning):**  
  - Eğitim doğruluğu: ~%80  
  - Doğrulama doğruluğu: ~%81–83  
  - Test doğruluğu: **%75**  

> 📌 Sonuç olarak, transfer learning yöntemi sıfırdan eğitilen CNN’e göre çok daha yüksek doğruluk ve genelleme başarısı sağlamıştır.
kaggle link = https://www.kaggle.com/code/naciyenur/fruits-and-vegetables-cnn
