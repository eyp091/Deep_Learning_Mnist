# Derin Öğrenme Yöntemleriyle MNIST Rakam Tanıma:

## Giriş:
- MNIST, el yazısı rakamların bulunduğu bir veri kümesidir ve makine öğrenimi ve derin öğrenme modellerinin eğitimi için sıkça kullanılır. Bu proje, MNIST veri kümesini kullanarak rakam tanıma problemi üzerinde bir derin öğrenme modeli oluşturmayı ve bu modelin performansını değerlendirmeyi amaçlamaktadır.

## Veri Kümesi ve Ön İşleme:
- MNIST veri kümesi, 0 ile 9 arasındaki rakamlardan oluşan 28x28 piksel boyutlarındaki siyah beyaz görüntülerden oluşur. Veri kümesi, 60.000 eğitim örneği ve 10.000 test örneği içerir. Öncelikle, veri kümesi TensorFlow kütüphanesi aracılığıyla yüklenir. Ardından, görüntüler 0 ila 1 arasında ölçeklenir ve düzleştirilir, yani her bir görüntü 28x28 piksel boyutundan tek boyutlu bir vektöre dönüştürülür.

## Model Mimarisi:
- Bu projede, derin öğrenme modeli oluşturmak için TensorFlow ve Keras kütüphaneleri kullanılmıştır. Model, tam bağlantılı (fully connected) katmanlardan oluşan bir sinir ağıdır. İlk katmanda 512 nöron, ikinci katmanda 128 nöron ve çıkış katmanında 10 nöron bulunur. Her katmanın aktivasyon fonksiyonu olarak sigmoid kullanılmıştır.

## Eğitim ve Değerlendirme:
- Model, eğitim veri kümesi üzerinde eğitilir ve ardından test veri kümesi üzerinde değerlendirilir. Eğitim sırasında, kayıp fonksiyonu olarak "binary crossentropy", optimize edici olarak "RMSprop" ve metrik olarak "accuracy" kullanılmıştır. Model 20 epoch boyunca eğitilmiş ve her bir epoch sonunda eğitim ve validasyon doğruluğu ile kayıp değerleri kaydedilmiştir.

## Performans Değerlendirme:
- Modelin performansı, karmaşıklık matrisi, sınıflandırma raporu ve doğruluk skoru gibi metrikler kullanılarak değerlendirilmiştir. Sınıflandırma raporu, her bir sınıf için hassasiyet, duyarlılık ve F1 skorunu gösterirken, karmaşıklık matrisi gerçek ve tahmin edilen sınıflar arasındaki ilişkiyi görselleştirir.

## Sonuçlar ve İyileştirme:
- Proje sonuçlarına göre, oluşturulan model yüksek doğruluk oranları elde etmiştir(%97.96). Ancak, modelin bazı sınıfları diğerlerine göre daha az doğru tahmin ettiği gözlemlenmiştir. Bu, modelin belirli sınıflar için daha fazla eğitilmesi veya modelin mimarisinin iyileştirilmesi gerekebileceğini göstermektedir.
