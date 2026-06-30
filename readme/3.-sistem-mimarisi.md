# 3. Sistem Mimarisi

Bu uygulama, modern web geliştirme prensiplerine uygun olarak üç katmanlı (three-tier architecture) bir yapı üzerine kurulmuştur. Bu yapı sayesinde frontend, backend ve veritabanı birbirinden bağımsız çalışmakta ve sistem daha düzenli, ölçeklenebilir ve sürdürülebilir hale gelmektedir.

### Mimari Yapı

Uygulama genel olarak aşağıdaki bileşenlerden oluşmaktadır:

* Frontend (Angular)
* Backend (Node.js + Express)
* Veritabanı (PostgreSQL)

```
Angular Frontend        ↓ HTTP RequestsNode.js / Express Backend API        ↓ SQL QueriesPostgreSQL Database
```

### Çalışma Mantığı

Kullanıcı uygulama üzerinde herhangi bir işlem yaptığında (örneğin kelime kartlarını görüntüleme veya quiz çözme), Angular frontend backend API’ye HTTP isteği gönderir. Backend bu isteği karşılayarak PostgreSQL veritabanına sorgu gönderir ve gerekli verileri alır. Daha sonra bu veriler geri döndürülür ve kullanıcı arayüzü güncellenir.

Bu yapı sayesinde veri akışı merkezi bir sistem üzerinden yönetilir ve uygulama daha güvenli ve düzenli bir hale gelir.
