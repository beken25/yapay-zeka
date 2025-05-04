Proje Adı: Şarkı Sözleri Tematik Analiz ve Vektörleştirme

1. Proje Hakkında
Bu proje, Türkçe şarkı sözlerini analiz etmek ve bu metinleri doğal dil işleme (NLP) yöntemleri kullanarak vektörleştirmek amacıyla geliştirilmiştir. Proje, şarkı sözlerinden tematik benzerlikleri ve kelime ilişkilerini incelemeyi hedefler. Yapılan işlemler arasında veri toplama, ön işleme (pre-processing), lemmatization ve stemming, vektörleştirme (TF-IDF ve Word2Vec) ve model eğitimi bulunmaktadır.

2. Projenin Amacı ve Kullanım Alanı
Bu proje, metin madenciliği ve doğal dil işleme tekniklerini kullanarak şarkı sözleri arasındaki benzerlikleri keşfetmek ve analiz etmeyi amaçlamaktadır. Proje, müzik analistleri, metin analistleri, araştırmacılar ve NLP alanında çalışanlar için faydalı olabilir. Kullanıcılar, bu projeyi farklı metin verileriyle de kullanarak benzer analizler yapabilir.

3. Proje İçeriği
Veri Toplama: Genius API kullanılarak şarkı sözleri verisi toplanmıştır.
Ön İşleme (Pre-Processing): Veri temizleme adımları (stop word removal, tokenization, lemmatization, stemming) uygulanmıştır.
Vektörleştirme: TF-IDF ve Word2Vec vektörleştirme yöntemleri uygulanmıştır.
Model Eğitim ve Değerlendirme: Word2Vec ve TF-IDF modelleri eğitilmiş ve sonuçlar karşılaştırılmıştır.
4. Gerekli Kütüphaneler ve Kurulum Talimatları
Bu projede kullanılan kütüphanelerin kurulumu için aşağıdaki adımları izleyebilirsiniz:

a. Gerekli Kütüphaneler:

pandas
nltk
gensim
zeyrek
scikit-learn
matplotlib
seaborn
requests
6. Veri Setinin Kullanılabilirliği
Veri Seti: Bu proje için kullanılan şarkı sözleri veri seti, şarkıcılar ve şarkı isimleriyle birlikte Genius API'den toplanmıştır.
Kullanım Amacı: Veri seti, şarkı sözleri arasındaki benzerlikleri analiz etmek, kelimelerin anlamlarını öğrenmek ve metin madenciliği çalışmaları yapmak için kullanılabilir. Ayrıca, NLP alanında deneysel çalışmalar yapmak isteyen araştırmacılar veya geliştiriciler için faydalıdır.
7. Modelin Değerlendirilmesi
Modelin doğruluğu, kullanılan veri setine ve uygulanan tekniklere bağlıdır. Burada, TF-IDF ve Word2Vec yöntemlerinin her ikisi de metin madenciliği için kullanışlıdır ve projede farklı amaçlar için kullanılabilir. Modelin başarısını değerlendirmek için vektörlerin benzerlikleri ve doğruluk oranları gözlemlenebilir.

