# Hayvan Sınıflandırma Projesi
Bu proje, VGG16, ResNet ve özelleştirilmiş bir CNN modeli kullanarak belirli hayvan türlerini sınıflandırmayı amaçlamaktadır. Üç farklı model denedikten sonra, en iyi sonuç veren VGG16 üzerinden çalışmalara devam edilmiştir.

Lütfen kodu Google Colab üzerinden çalıştırmak isteyen arkadaşlar şu adımları izlesin:
- **Çalışma zamanı > Çalışma zamanı türünü değiştir > v2-8 TPU** seçeneğini seçin.

## Veri Seti
Proje, "[Animals with Attributes 2](https://www.kaggle.com/rrebirrth/animals-with-attributes-2)" veri setini kullanmaktadır. Veri setinde 50 farklı hayvan türüne ait resimler bulunmaktadır. Ancak bu proje aşağıdaki 10 hayvan türüne odaklanmıştır:
- Collie
- Dolphin
- Elephant
- Fox
- Moose
- Rabbit
- Sheep
- Squirrel
- Giant Panda
- Polar Bear

Her bir sınıf için en fazla 650 resim kullanılmıştır. Gereksiz sınıflar ve fazla resimler temizlenmiştir.

---

## Veri Önİşleme
1. **Resim Boyutlandırma ve Normalizasyon**
   - Resimler 128x128 boyutuna getirilmiş ve piksel değerleri 255’e bölünerek normalize edilmiştir.

2. **Veri Ayrımı**
   - Veri seti, %70 eğitim ve %30 test olarak ayrılmıştır.

3. **Veri Artırma**
   - Veri artırma için şu dönüşüm teknikleri uygulanmıştır:
     - Döndürme (rotation)
     - Kaydırma (width/height shift)
     - Kesme (shear)
     - Yakınlaştırma (zoom)
     - Ayna yansıtma (horizontal flip)

---

## Kullanılan Modeller

### 1. **VGG16**
- **Özellikler**
  - ImageNet ile önceden eğitilmiş ağırlıklar kullanılmıştır.
  - Üst katmanlar dondurulmuş, son 4 katman ise eğitilebilir hale getirilmiştir.
  - Yeni tam bağlı katmanlar ve Dropout eklenmiştir.

- **Sonuçlar**
  - **Test Loss**: [Sonuç eklenmeli]
  - **Test Accuracy**: [Sonuç eklenmeli]

- **Model Kayıt**
  - Model, `vgg16_model.h5` dosyası olarak kaydedilmiştir.

### 2. **ResNet**
- **Özellikler**
  - Transfer Learning yaklaşımı ile kullanılmıştır.
  - ResNet modeli, benzer veri artırma teknikleriyle eğitilmiştir.

- **Sonuçlar**
  - **Test Loss**: [Sonuç eklenmeli]
  - **Test Accuracy**: [Sonuç eklenmeli]

- **Model Kayıt**
  - ResNet modeli bağlantısı: [ResNet Modeli](https://colab.research.google.com/drive/1niqPY9xY4ine64EW_ZKOWa3TOAoP6QBT?usp=sharing)

### 3. **CNN (Convolutional Neural Network)**
- **Özellikler**
  - Scratch (sıfırdan) bir CNN modeli tasarlanmış ve eğitilmiştir.

- **Sonuçlar**
  - **Test Loss**: [Sonuç eklenmeli]
  - **Test Accuracy**: [Sonuç eklenmeli]

- **Model Kayıt**
  - CNN modeli bağlantısı: [CNN Modeli](https://colab.research.google.com/drive/161oHfv6lYHywYd-1lLupzKIvKoB5RtDV?usp=sharing)

---

## Sonuçların Karşılaştırılması
1. Her model, test veri setinde ayrı ayrı değerlendirilmiştir.
2. Manipüle edilmiş test resimleri ve renk sabitliği uygulanmış test setleriyle çalışılmıştır.
3. **Sonuç Karşılaştırması**
   - Orijinal test seti ile manipüle edilmiş set arasında başarı farkı değerlendirilmiştir.
   - Renk sabitliği iyileştirmeleri rapor edilmiştir.

---

## Lisans
Bu proje MIT Lisansı altında kullanıma sunulmuştur.

