# 8. Quiz Sistemi

#### Genel Bilgi

Quiz sistemi, kullanıcıların İngilizce kelime öğrenme sürecini ölçmek, pekiştirmek ve değerlendirmek amacıyla geliştirilmiş interaktif bir test modülüdür. Bu sistemde kullanıcıya Türkçe kelimeler rastgele veya belirli bir algoritmaya göre sunulmakta ve bu kelimelerin doğru İngilizce karşılığını çoktan seçmeli seçenekler arasından seçmesi beklenmektedir.

Bu yapı sayesinde kullanıcılar yalnızca yeni kelimeler öğrenmekle kalmaz, aynı zamanda mevcut bilgilerini test ederek eksik oldukları alanları da tespit edebilirler. Quiz sistemi, öğrenme sürecini pasif bir yapıdan aktif bir değerlendirme sürecine dönüştürerek daha kalıcı bir öğrenme deneyimi sağlar.

***

#### Çalışma Mantığı ve Sistem Akışı

Quiz modülü, frontend ve backend arasında REST API üzerinden haberleşen bir mimari yapıya sahiptir. Kelime verileri PostgreSQL veritabanında yer alan **words** tablosundan alınmaktadır.

Sistemin çalışma akışı şu şekildedir:

1. Angular tabanlı frontend, quiz başlatma isteğini backend’e gönderir.
2. Node.js tabanlı backend, veritabanından rastgele veya filtrelenmiş kelimeleri çeker.
3. Alınan kelimeler üzerinden çoktan seçmeli seçenekler oluşturulur.
4. Doğru cevap ile birlikte yanlış seçenekler sistem tarafından hazırlanır.
5. Oluşturulan soru JSON formatında frontend’e gönderilir.
6. Kullanıcı soruyu cevapladıktan sonra cevap doğru/yanlış olarak değerlendirilir.

Bu yapı sayesinde quiz sistemi tamamen dinamik hale getirilmiş ve her kullanımda farklı soru setleri oluşturulması sağlanmıştır.

***

#### Soru Yapısı ve İçerik Üretimi

Quiz soruları, veritabanından çekilen kelimeler kullanılarak dinamik şekilde oluşturulmaktadır. Her soru için:

* Bir adet doğru cevap
* Birden fazla yanlış seçenek
* İngilizce hedef kelime

bulunmaktadır.

Yanlış seçenekler genellikle diğer kelimeler arasından rastgele seçilerek oluşturulur. Bu yöntem, kullanıcıların sadece ezber yapmasını engelleyip gerçek öğrenme seviyesini ölçmeyi amaçlamaktadır.

***

#### API ve Backend Yapısı

Quiz sistemi backend tarafında REST prensiplerine uygun şekilde geliştirilmiştir. Temel endpoint yapısı aşağıdaki gibidir:

* GET /api/quiz/start → Yeni quiz oturumu başlatır
* GET /api/quiz/question → Yeni soru getirir
* POST /api/quiz/answer → Kullanıcının cevabını değerlendirir<br>

***

#### Kullanıcı Arayüzü ve Etkileşim

Quiz arayüzü sade ve kullanıcı odaklı olacak şekilde tasarlanmıştır. Kullanıcıya her seferinde tek bir soru gösterilir ve dört seçenekli çoktan seçmeli bir yapı sunulur.

Arayüzdeki temel özellikler şunlardır:

* Soru ve seçeneklerin net şekilde gösterimi
* Seçim sonrası anlık geri bildirim (doğru/yanlış)

Bu yapı sayesinde kullanıcılar dikkat dağılmadan odaklanarak test çözebilmektedir.

***

#### Sağladığı Avantajlar

Quiz sistemi, öğrenme sürecini ölçülebilir hale getirir. Bu sayede kullanıcı hangi kelimeleri bildiğini ve hangilerinde eksik olduğunu net şekilde görebilir.

Başlıca avantajları şunlardır:

* Bilgi ölçme ve değerlendirme imkânı sağlar
* Öğrenilen kelimelerin pekişmesini destekler
* Tekrar motivasyonunu artırır
* Aktif öğrenme sürecini destekler

***

#### Ekran Görüntüsü

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>
