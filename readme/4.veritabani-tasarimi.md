# 4.Veritabanı Tasarımı

Uygulamada PostgreSQL veritabanı kullanılmaktadır. Veritabanı yapısı oldukça sade tutulmuş ve yalnızca uygulamanın temel ihtiyacı olan kelime verilerinin saklanmasına odaklanılmıştır.

### words Tablosu

| Alan    | Açıklama                                  |
| ------- | ----------------------------------------- |
| id      | Her kelime için benzersiz kimlik numarası |
| english | İngilizce kelime                          |
| turkish | Türkçe karşılığı                          |

### Açıklama

Bu tablo, uygulamanın tüm kelime verisini içermektedir. Kelime kartları, quiz sistemi bu tablo üzerinden gelen veriler ile çalışmaktadır. Veriler backend tarafından çekilerek frontend’e dinamik olarak iletilmektedir.

Bu yapı sayesinde uygulama sabit veri yerine sürekli güncellenebilir ve genişletilebilir bir hale getirilmiştir.
