# 🦁 Animal Classification Model - Proje Özeti

Bu proje, 10 farklı hayvan türünü sınıflandırmak amacıyla bir derin öğrenme modeli oluşturmayı hedeflemektedir. **Toplamda 46 farklı sınıf** bulunmaktadır, ancak proje kapsamında **seçilen 10 sınıf** üzerinde çalışmalar yapılmıştır. Model, farklı hayvan türlerinin görüntülerini kullanarak bu türleri doğru bir şekilde tanıyabilen bir sınıflandırıcıdır. Projede, görüntü işleme, veri hazırlığı, model eğitimi ve model değerlendirmesi gibi adımlar yer almaktadır.

## 🐘 Kullanılan Kütüphaneler

- **Pandas**: Veri analizi ve manipülasyonu için.
- **NumPy**: Sayısal hesaplamalar için.
- **Matplotlib ve Seaborn**: Görselleştirme ve grafikler için.
- **Scikit-learn**: Veri setinin bölünmesi, etiket kodlama ve model değerlendirme için.
- **TensorFlow/Keras**: Derin öğrenme modelinin oluşturulması, eğitilmesi ve test edilmesi için.
- **Scikit-optimize**: Hiperparametre optimizasyonu için.

## 🦓 Veri Seti

Veri seti, 10 farklı hayvan türüne ait görüntülerden oluşmaktadır. **Her sınıftan 650 tane fotoğraf alınmıştır.** Her hayvan türü belirli etiketlerle tanımlanmıştır. Görüntüler, eğitim, doğrulama ve test setlerine ayrılmadan önce karıştırılmıştır. Görüntüler **224x224 piksel** boyutunda olup, **RGB renk formatında** işlenmiştir.

## 🦒 Adım Adım İşlemler

### 1. 🦝 Veri Hazırlama

- **Dosya Yollarının Alınması**: Veri setindeki tüm görüntü dosyalarının yolları ve etiketleri alınarak bir DataFrame'e dönüştürülmüştür.
- **Etiket Filtreleme**: Veri setindeki gereksiz etiketler ve dosyalar hariç tutulmuştur.
- **Karıştırma**: DataFrame rastgele karıştırılarak eğitim, doğrulama ve test setlerine bölünmüştür.

### 2. 🦔 Görüntü İşleme

- **Öznitelik Çıkarımı**: Her görüntü, yeniden boyutlandırılmış ve normalleştirilmiştir.
- **Normalizasyon**: Görüntü verileri [0, 1] aralığına normalleştirilmiştir.

### 3. 🦁 Etiket Kodlama

- **Label Encoding**: Etiketler sayısal değerlere dönüştürülmüştür.
- **One-Hot Encoding**: Modelin sınıflandırma işlemi için etiketler one-hot formatına çevrilmiştir.

### 4. 🐅 Model Oluşturma

- **Model Mimarisinin Tasarımı**: Derin bir sinir ağı kullanılarak bir model oluşturulmuştur. Modelde, birden fazla konvolüsyonel katman, BatchNormalization, MaxPooling, Dropout katmanları kullanılmıştır.
- **Hiperparametre Ayarı**: Hiperparametre optimizasyonu için GridSearchCV ve RandomizedSearchCV gibi teknikler kullanılmıştır.

### 5. 🐆 Model Eğitimi

- **Eğitim Süreci**: Model, eğitim ve doğrulama verileri üzerinde eğitilmiş ve en iyi performansı gösteren model kaydedilmiştir.
- **Callbacks**: Eğitim sırasında erken durdurma (EarlyStopping) ve öğrenme oranı azaltma (ReduceLROnPlateau) gibi callback fonksiyonları kullanılmıştır.

### 6. 🦄 Model Değerlendirmesi

- **Kayıp ve Doğruluk Grafikleri**: Eğitim süreci boyunca kayıp ve doğruluk değerleri görselleştirilmiştir.
- **Sınıflandırma Raporu**: Modelin doğruluğu, precision, recall ve F1-score gibi metriklerle değerlendirilmiştir.
- **Confusion Matrix**: Gerçek ve tahmin edilen sınıflar arasındaki ilişkileri görselleştiren bir confusion matrix oluşturulmuştur.

## 🐘 Sonuçlar

Model, test setlerinde yüksek doğruluk oranları elde etmiştir. Eğitim süreci boyunca kayıp değeri sürekli azalmış ve doğruluk değeri artmıştır. Model, özellikle `dolphin` ve `moose` sınıflarında doğru tahmin yaparken, `rabbit` sınıfında zayıf performans göstermektedir.

## 🦓 Kullanım

Bu proje, hayvan sınıflandırma üzerine yapılacak araştırmalar ve uygulamalar için bir temel oluşturmaktadır. Kullanıcılar, gerekli kütüphaneleri yükleyerek ve sağlanan kodu çalıştırarak modelin eğitimini ve değerlendirilmesini gerçekleştirebilirler.

### 🦒 Kaggle Linki
(https://www.kaggle.com/code/siladurtas/cnn-bootcamp)
