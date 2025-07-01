
# 🚀 Whaleswap AI – Demo Kullanım Akışı

Bu belge, Whaleswap AI platformunun temel kullanıcı yolculuğunu ve sistem etkileşim akışını özetler.

---

## 🧑‍💼 1. Kayıt & API Bağlantısı
- Kullanıcı platforma kayıt olur ve kullandığı borsa(lar) için API anahtarlarını girer (Binance / Bybit / Hyperliquid).
- API anahtarları AES ile şifrelenerek güvenli biçimde saklanır.

---

## 📈 2. Trader Analizi ve Kopyalama
- Kullanıcı, AI analiz motoru tarafından sıralanmış trader listesini görüntüler.
- Filtreleme (risk düzeyi, başarı oranı, işlem tipi vs.) yaparak uygun trader seçilir.
- “Copy Now” butonuyla seçilen trader’ın işlemleri gerçek zamanlı olarak kendi hesabına yansıtılır.

---

## 🛠 3. Copy Trade Terminali
- Kullanıcılar dilerse manuel olarak da işlem açabilir.
- İşlem tipi, kaldıraç, pozisyon büyüklüğü gibi ayarlar doğrudan terminal üzerinden yapılandırılır.
- Tüm işlemler doğrudan kullanıcıya ait API ile gerçekleşir — sistem cüzdan tutmaz.

---

## 📊 4. Portföy & Performans Takibi
- Anlık PnL, ROI, işlem geçmişi, varlık dağılımı ve trader bazlı kazanç analizleri gösterilir.
- Gerçek zamanlı grafikler WebSocket ile canlı güncellenir.

---

## 🔔 5. Bildirim & Uyarılar
- Kullanıcılar, pozisyon açılış/kapanış, PnL değişimi ve sinyaller hakkında Telegram bot üzerinden bilgilendirilir.
- Bot üzerinden temel sorgulamalar (günlük kazanç, açık işlem sayısı vs.) yapılabilir.

---

## 🧠 6. Arka Planda Çalışan Bileşenler
- Tüm veri akışı Kafka üzerinden dağıtılır, Redis ile kuyruklanır ve Celery işleyicileriyle analiz edilir.
- İşlem geçmişi, sinyaller ve kullanıcı davranışları MongoDB’de tutulur.
- Her servis Docker ile izole edilmiş, Kubernetes ile yatay ölçeklenebilir hale getirilmiştir.

---

## 📌 Not:
Demo ortamı ve kullanıcı paneli kaynak kodlara dahil değildir. Görsel ve teknik sunum amaçlıdır.
