Giriş

Bu proje, metin tabanlı veriler üzerinde doğal dil işleme (NLP) teknikleri kullanarak çeşitli yapay zekâ modelleri geliştirmeyi amaçlamaktadır. Projede, veri indirme, ön işleme, vektörleştirme ve Word2Vec modelleri gibi adımlar uygulanacaktır.

Veri Seti Seçimi
Veri seti, Genius API üzerinden alınan Türkçe şarkı sözlerinden oluşmaktadır. Bu veri seti, şarkı sözlerinde tematik benzerlik ölçümü yapmak amacıyla kullanılacaktır.

Kurulum

Proje, aşağıdaki Python kütüphanelerine gereksinim duyar:

gensim
pandas
nltk
sklearn
matplotlib
seaborn
Kurulum için aşağıdaki komutu kullanabilirsiniz:

pip install gensim pandas nltk sklearn matplotlib seaborn
Veri Seti

Kaynak: Veri seti Genius API üzerinden alınmıştır.
Boyut: Veri seti 721 Türkçe şarkı sözünden oluşmaktadır.
Format: JSON formatında indirilmiştir.
Örnek Veri
Örnek bir şarkı sözü:

{
    "song": "Yavaş Yavaş",
    "lyrics": "Yavaş yavaş beni unut, çok geç olmadan, her şey geride kalsın"
}
Veri seti üzerinde uygulanan ön işleme adımlarında, şarkı sözlerinden önce gereksiz karakterler ve durak kelimeler (stop words) çıkarılmıştır.

Uygulanan Pre-processing Adımları

Veri seti üzerinde aşağıdaki ön işleme adımları uygulanmıştır:

Stop Word Removal: Gereksiz ve sık kullanılan kelimeler veri setinden çıkarılmıştır.
Tokenization: Şarkı sözleri kelimelere ayrılmıştır.
Lowercasing: Tüm metinler küçük harfe dönüştürülmüştür.
Lemmatization: Kelimeler kök halleriyle dönüştürülmüştür.
Stemming: Kelimeler köklerine indirgenmiştir.
Özel karakter temizliği: HTML etiketleri ve diğer özel karakterler temizlenmiştir.
Veri Seti Çıktıları

Temizlenmiş veri seti iki ayrı CSV dosyası olarak kaydedilmiştir:
lemmatized_data.csv
stemmed_data.csv
Bu dosyalar, GitHub repository'sinde yer almaktadır.
Zipf Yasası Analizi

Veri seti üzerine Zipf Yasası uygulanarak kelime sıklıklarının log-log grafikleri çizilmiştir. Bu grafikler, veri setinin dilsel özelliklerini ve kelime sıklığının dağılımını anlamamıza yardımcı olmuştur.

Vektörleştirme

Veri seti üzerinde TF-IDF ve Word2Vec yöntemleri ile vektörleştirme işlemi gerçekleştirilmiştir.

A. TF-IDF Vektörleştirme
Her iki veri seti için (lemmatized ve stemmed) TF-IDF vektörleştirme işlemi uygulanmıştır. Sonuçlar, şu şekilde kaydedilmiştir:

tfidf_lemmatized.csv
tfidf_stemmed.csv
B. Word2Vec Vektörleştirme
Gensim kütüphanesi kullanılarak, her iki veri seti için (lemmatized ve stemmed) toplamda 16 farklı Word2Vec modeli eğitilmiştir. Parametre setleri şu şekildedir:

CBOW model, pencere boyutu: 2, vektör boyutu: 100
Skipgram model, pencere boyutu: 2, vektör boyutu: 100
CBOW model, pencere boyutu: 4, vektör boyutu: 100
Skipgram model, pencere boyutu: 4, vektör boyutu: 100
CBOW model, pencere boyutu: 2, vektör boyutu: 300
Skipgram model, pencere boyutu: 2, vektör boyutu: 300
CBOW model, pencere boyutu: 4, vektör boyutu: 300
Skipgram model, pencere boyutu: 4, vektör boyutu: 300
Her modelin eğitimi sonrası elde edilen vektör çıktıları örnek olarak raporlanmıştır. Bu örneklerde, belirli kelimelerin vektör uzayındaki en yakın anlamlı kelimeleri paylaşılmıştır.

Sonuç ve Değerlendirme

Projede elde edilen sonuçlar, kullanılan veri setine ve uygulanan yöntemlere dayanarak değerlendirilecektir. Her modelin başarısı, kullanılan parametreler ve model çıktılarının benzerlik oranlarına göre karşılaştırılacaktır.

