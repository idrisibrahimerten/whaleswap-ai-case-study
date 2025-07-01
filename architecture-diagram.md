
# 🧱 Whaleswap AI – Sistem Mimarisi Açıklaması

Aşağıdaki diyagram, Whaleswap AI platformunun genel teknik mimarisini özetlemektedir. Bileşenler modüler, bulut uyumlu ve yüksek trafik işleyebilecek şekilde tasarlanmıştır.

---

## 📐 Temel Katmanlar

### 1. **Frontend**
- **React / Next.js** kullanılarak geliştirildi.
- Portföy takibi, trader listesi, kopyalama arayüzü ve canlı grafik bileşenlerini içerir.
- WebSocket ile canlı veri akışı sağlar.

### 2. **Backend Servisleri**
- Django & FastAPI kullanılarak modüler mikroservisler oluşturulmuştur.
- REST & GraphQL API’ler üzerinden frontend ile haberleşir.
- Kullanıcı işlemleri, API anahtar yönetimi ve portföy verisi burada yönetilir.

### 3. **Gerçek Zamanlı Veri Akışı**
- **Kafka** ile dağıtık mesajlaşma yapılır.
- **Redis + Celery** ile zamanlı görevler ve veri işleme gerçekleştirilir.
- Borsa verileri milisaniyelik hassasiyetle analiz edilerek yayınlanır.

### 4. **AI & Analitik Katmanı**
- **PyTorch / TensorFlow** ile geliştirilen modeller, trader davranışlarını analiz eder.
- AI modülü, geçmiş performansa göre trader puanı üretir.
- (Opsiyonel) ChatGPT ile açıklamalı sinyaller verilebilir.

### 5. **Veritabanı**
- **MongoDB (NoSQL)** kullanılır.
- Kullanıcılar, pozisyon geçmişi, sinyaller ve sistem günlükleri bu veritabanında saklanır.

### 6. **Güvenlik Katmanı**
- JWT Authentication
- AES şifreleme (API anahtarları için)
- Her işlem ve API çağrısı için detaylı loglama

### 7. **Bildirim & Entegrasyon**
- **Telegram Bot API** ile kullanıcıya anlık sinyal ve portföy güncellemeleri gönderilir.
- Kullanıcı komutlarıyla pozisyon sorgulama yapılabilir.

### 8. **Altyapı & DevOps**
- **Docker** ile containerize edilmiş servisler
- **Kubernetes** ile yük dengeleme ve otomatik ölçeklendirme
- **AWS (EC2, S3, Lambda)** üzerinde barındırma
- **CI/CD** akışları GitHub Actions ile yönetilir

---

## 📎 Not:
Bu açıklama, [architecture-diagram.png](architecture-diagram.png) görseline paralel olacak şekilde hazırlanmıştır. Kod paylaşımı yapılmamıştır.
