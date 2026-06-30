# 7.Kelime Kartları

#### Genel Bilgi

Kelime Kartları modülü, kullanıcıların İngilizce kelime dağarcığını geliştirmesini hedefleyen interaktif bir öğrenme bileşenidir. Bu modül, özellikle tekrar temelli öğrenme ile kullanıcıların kelimeleri daha kalıcı şekilde öğrenmesini amaçlamaktadır.

Sistem içerisinde kelimeler kartlar halinde kullanıcıya sunulmakta, kullanıcı kartın ön yüzünde yer alan kelimeyi görmekte ve kartı çevirdiğinde ingilizce karşılığını görüntüleyebilmektedir. Bu yöntem, klasik ezberleme yöntemlerine göre daha etkileşimli ve kullanıcı odaklı bir öğrenme deneyimi sağlamaktadır.

Ayrıca kullanıcı, kelimeler arasında ilerleyerek sürekli tekrar yapma imkânına sahip olmakta ve bu sayede öğrenme süreci daha verimli hale gelmektedir.

***

#### Sistem Mimarisi ve Çalışma Mantığı

Kelime kartları modülü, istemci–sunucu (client–server) mimarisi üzerine kurulmuştur. Frontend tarafında Angular kullanılırken, backend tarafında Node.js ile geliştirilmiş RESTful API bulunmaktadır. Veri yönetimi ise PostgreSQL veritabanı üzerinden gerçekleştirilmektedir.

Kullanılan temel veri akışı şu şekildedir:

1. Angular frontend kullanıcıdan gelen isteği oluşturur.
2. Bu istek REST API aracılığıyla Node.js backend’e iletilir.
3. Backend, PostgreSQL veritabanında yer alan **words** tablosundan gerekli kelime verilerini çeker.
4. Veriler JSON formatına dönüştürülerek frontend’e geri gönderilir.
5. Angular uygulaması bu verileri alarak kelime kartları şeklinde kullanıcıya sunar.

Bu yapı sayesinde frontend ile backend arasında net bir ayrım sağlanmış, sistemin ölçeklenebilirliği ve bakımı kolaylaştırılmıştır.

***

#### Kullanıcı Arayüzü ve Etkileşim

Kelime kartları arayüzü kullanıcı dostu olacak şekilde tasarlanmıştır. Kartlar ekranın ortasında gösterilir ve kullanıcı kart üzerine tıklayarak çevirme animasyonu ile diğer yüzü görüntüleyebilir. Bu etkileşimler sayesinde kullanıcılar sorunsuz bir deneyim yaşamaktadır.

***

#### Sağladığı Avantajlar

Kelime kartları modülü, geleneksel ezber yöntemlerine kıyasla daha aktif bir öğrenme süreci sunmaktadır. Kullanıcı sadece kelimeyi okumakla kalmayıp aynı zamanda aktif olarak tahmin yapma sürecine dahil olmaktadır.

Başlıca avantajları şunlardır:

* Aktif öğrenmeyi teşvik eder
* Tekrar yapmayı kolaylaştırır
* Öğrenme sürecini daha eğlenceli hale getirir
* Kısa süreli belleği uzun süreli belleğe dönüştürmeyi destekler

***

#### Özellikler

* İngilizce ve Türkçe kelime gösterimi
* Kart çevirme (flip) animasyonu
* PostgreSQL veritabanı entegrasyonu
* REST API üzerinden veri alışverişi
* Dinamik ve güncellenebilir veri yapısı

***

#### Ekran Görüntüsü

***

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>
