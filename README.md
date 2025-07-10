# mnist-egitim-takibi
MNIST ile dropout ve early stopping uygulamalı model doğruluk/kayıp takibi
# 📊 MNIST Eğitim Takibi: Dropout & EarlyStopping ile

Bu projede, MNIST veri seti üzerinde çalışan bir yapay sinir ağı eğitimi sırasında modelin doğruluk (accuracy) ve kayıp (loss) değerleri grafikle izlenmektedir. Ayrıca:

- Aşırı öğrenmeyi önlemek için **Dropout** uygulanmıştır.
- Eğitim süreci, **EarlyStopping** ile erken durdurulmuştur.

## 🛠 Kullanılan Teknolojiler

- Python
- TensorFlow / Keras
- Matplotlib
- NumPy

## 🔬 Eğitim Yapısı

- Giriş: 784 boyutlu vektör (28x28 gri görüntü)
- Gizli Katmanlar:
  - Dense(128, ReLU)
  - Dropout(0.3)
  - Dense(64, ReLU)
- Çıkış: 10 sınıf, Softmax aktivasyon

## ⏱ Eğitim Süreci

- Eğitim epoch: 20 (EarlyStopping ile daha erken durabilir)
- Batch size: 128
- Kayıp fonksiyonu: `categorical_crossentropy`
- Optimizasyon: `adam`

## 📈 Görselleştirmeler

Notebook sonunda aşağıdaki grafikler üretilir:

- Eğitim vs Doğrulama Doğruluk Grafiği
- Eğitim vs Doğrulama Kayıp Grafiği

## 🖼️ Örnek Tahmin

Modelden test verisi için yapılan bir tahmin görselleştirilir:

```python
plt.title(f"Tahmin: 4, Gerçek: 4")
