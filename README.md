Malware Analizi Veri Seti İşleme

Bu projede, bir malware analizi veri seti üzerinde derinlemesine veri ön işleme, analiz ve görselleştirme adımları gerçekleştirilmiştir.

İşlem Adımları

1. Veri Okuma
Veri seti, pandas kütüphanesi aracılığıyla CSV formatında okundu.
Toplam 34 sütun ve binlerce satırdan oluşan bu veri seti, malware analizine dair önemli bilgiler içermektedir.

2. Eksik Veri Doldurma
Eksik değerlerin veri setindeki etkisini azaltmak için bu değerler, ilgili sütunun ortalamasıyla dolduruldu.
Bu adım, makine öğrenimi modelinin performansını artırmak için kritiktir.

3. Normalizasyon
MinMaxScaler kullanılarak veri setindeki tüm değerler 0 ile 1 arasına ölçeklendirildi.
Bu işlem, özellikler arasındaki değerlerin aralığının dengelenmesi için gerçekleştirildi.

4. İstatistiksel Analiz
Veri setinin özet istatistikleri elde edildi.
Bu istatistikler, verinin dağılımı, merkezi eğilimi ve dağılımın yayılımı hakkında bilgi sağlar.

5. PCA (Ana Bileşenler Analizi)
Veri setinin boyutu, varyansın %95'i korunacak şekilde indirgendi.
Kümülatif varyans analizi ile optimal bileşen sayısı belirlendi.
Bu adım, makine öğrenimi modelleme aşamasında hesaplama süresini azaltmayı amaçlar.

6. Görselleştirmeler
Normalizasyon sonrası veri setinin histogramı ve box plot görselleştirmeleri oluşturuldu.
Bu görselleştirmeler, verinin dağılımını ve aykırı değerleri gözlemlemek için kullanılır.

Kullanılan Kütüphaneler
pandas: Veri manipülasyonu ve analizi için kullanıldı.
numpy: Sayısal hesaplamalar için kullanıldı.
matplotlib ve seaborn: Veri görselleştirme için kullanıldı.
sklearn.preprocessing: Veri ölçeklendirme ve normalizasyon işlemleri için kullanıldı.
sklearn.decomposition: PCA uygulaması için kullanıldı.
