# Grup5
Beklenen Gol (xG) Oranları ile Lig Başarısı Arasındaki İlişki Analizi

Proje Açıklaması

Bu projede, 2023/2024 Süper Lig sezonuna ait futbol takımı performans verileri kullanılarak, beklenen gol (xG - Expected Goals) metriği ile takımların lig başarısı (puan ve sıralama) arasındaki ilişki incelenmiştir.

Amaç, yalnızca skorlar üzerinden değil, takımların maç içindeki hücum üretkenliğini ölçen daha ileri düzey istatistiksel bir metrik olan xG verilerini kullanarak gerçek başarıyı daha doğru modellemek ve analiz etmektir.

Kullanılan Yöntemler
1. Veri Toplama ve Hazırlık
xG verileri: Mackolik.com

Lig puan durumu: Türkiye Futbol Federasyonu (TFF)

Birleştirilerek .csv formatında veri seti oluşturuldu.

2. Veri Temizleme
Kategorik/sayısal veri ayrımı (select_dtypes)

Tekrarlayan kayıtlar (.duplicated(), drop_duplicates())

Eksik veri kontrolü (missingno ve .isnull())

3. Keşifsel Veri Analizi (EDA)
Bar grafikleri, boxplotlar ve scatter plotlar ile:

Puan dağılımı

Gol/xG oranı → Bitiricilik oranı

Yediği gol/xGA oranı → Kaleci performansı

xG farkı (xG - xGA) ile sıralama ilişkisi

4. Makine Öğrenmesi:
Algoritma: Doğrusal Regresyon (Linear Regression)

Kütüphane: scikit-learn

Amaç: xG üzerinden lig puanı tahmini yapmak

Performans Metrikleri:

R² Skoru: 0.98

MAE: 1.59

RMSE: 1.70

Özet Sonuçlar
xG ile puan arasında güçlü ve pozitif bir ilişki tespit edilmiştir.

Model, xG verileriyle takım puanlarını oldukça yüksek doğrulukla tahmin edebilmektedir.

xG değeri yüksek olup düşük puan alan takımlar, genellikle bitiricilik zayıflığı, şanssızlık veya bireysel hatalar nedeniyle bu durumu yaşamıştır.

xG, tek başına yeterli değildir; xGA, kaleci performansı gibi savunma metrikleriyle birlikte değerlendirilmelidir.
