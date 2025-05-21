 Maske Takma Durumu Sınıflandırması



Bu proje, insanların yüzlerinde maske olup olmadığını ve maskeyi düzgün takıp takmadıklarını otomatik olarak tespit edebilen bir derin öğrenme modeli geliştirmeyi hedeflemektedir. Özellikle pandemi dönemlerinde kamu alanlarında güvenlik ve denetim amacıyla kullanılabilir.

Kullanılan Teknolojiler
Python programlama dili

TensorFlow ve Keras derin öğrenme kütüphaneleri

MobileNetV2 (Transfer Learning için)

Google Colab

Görselleştirme: Matplotlib, Seaborn

Grad-CAM (modelin hangi bölgeye dikkat ettiğini göstermek için)

Veri Seti
Veri seti üç ana sınıftan oluşmaktadır:

with_mask: Maske doğru takılmış

without_mask: Maske takılmamış

mask_weared_incorrect: Maske yanlış takılmış

Görseller bu klasörlerde saklanarak modele beslenir. Google Drive üzerinde /MyDrive/Python/Dataset/ dizininde tutulmalıdır.

Modelin Eğitimi
Görseller, ImageDataGenerator ile yeniden boyutlandırılır ve normalize edilir.

MobileNetV2 modeli kullanılarak, önceden eğitilmiş bir model temel alınır.

Üst katmanlara yeni sınıflandırıcı katmanlar eklenir.

Model, 3 sınıfı tanıyacak şekilde eğitilir.

Değerlendirme
Eğitim sonrasında:

Doğruluk oranı ölçülür.

Confusion matrix ve classification report ile modelin performansı değerlendirilir.

Grad-CAM ile Görselleştirme
Grad-CAM yöntemi ile modelin tahmin yaparken görselin hangi bölgelerine odaklandığı gösterilir. Bu, modelin kararlarını anlamak açısından önemlidir.

Kullanım
Proje Google Colab üzerinde açılır.

Google Drive bağlanarak veri seti yüklenir.

Kod adımları sırayla çalıştırılarak model eğitilir.

testimages klasörüne konulan yeni görseller üzerinde tahmin yapılır.

Tahmin sonucu ve Grad-CAM görselleştirmesi ekranda gösterilir.





