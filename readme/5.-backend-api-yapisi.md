# 5. Backend (API Yapısı)

Backend tarafı Node.js kullanılarak geliştirilmiştir. Backend’in temel amacı frontend ile veritabanı arasında köprü görevi görmektir.

Uygulamada kullanıcı doğrulama sistemi bulunmamaktadır. Sistem sadece kelime verilerini sağlayan bir API yapısı olarak tasarlanmıştır.

### API Yapısı

Backend üzerinde oluşturulan endpoint’ler aşağıdaki gibidir:

#### GET /words

Veritabanında bulunan tüm kelime verilerini frontend’e gönderir. Bu endpoint kelime kartları ve quiz sistemi için kullanılmaktadır.



### API Çalışma Mantığı

Frontend tarafından gönderilen HTTP istekleri backend tarafından karşılanır. Backend bu istekleri PostgreSQL veritabanına SQL sorguları olarak iletir ve elde edilen sonuçları frontend’e geri döndürür. Bu yapı sayesinde frontend ve backend birbirinden bağımsız çalışabilir ve sistem daha esnek bir hale gelir.
