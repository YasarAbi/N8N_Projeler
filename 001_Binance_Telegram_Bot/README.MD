# 📈 Proje 001: Binance Futures Telegram Bot

![n8n Version](https://img.shields.io/badge/n8n-Workflow-orange?style=flat-square&logo=n8n)
![Status](https://img.shields.io/badge/Durum-Aktif-green?style=flat-square)

Bu klasör, **Binance Vadeli İşlemler (Futures)** hesabınızı Telegram üzerinden yönetmenizi sağlayan n8n workflow dosyasını ve dokümantasyonunu içerir.

## 📂 Dosya İçeriği

* **`Binance_Telegram_Bot.json`**: n8n'e import edilecek ana workflow dosyası.
* **`README.md`**: Şu an okuduğunuz dokümantasyon dosyası.

---

## 🔥 Özellikler

Bu bot ile şunları yapabilirsiniz:
1.  **Cüzdan Özeti:** `/start` veya butonlar aracılığıyla toplam bakiye, marjin ve kullanılabilir tutarı görüntüleme.
2.  **Anlık PNL Takibi:** Açık pozisyonların kâr/zarar durumunu emojilerle desteklenmiş rapor halinde alma.
3.  **Panik Butonu (Acil Kaçış):** Piyasada ters bir durum olduğunda `closePosition` komutu ile tüm işlemleri **Market** fiyatından anında kapatma.
4.  **Güvenlik Kontrolü:** Sadece tanımlı Telegram kullanıcısından gelen komutları işleme alma.
5.  **Hassas Hesaplama:** Coin'e özel fiyat hassasiyetini (precision) otomatik hesaplayarak API hatalarını önleme.

---

## ⚙️ Kurulum Adımları

### 1. Dosyayı İçe Aktarın
* n8n panelinizde sağ üstteki **"Import"** butonuna basın.
* Bu klasördeki `Binance_Telegram_Bot.json` dosyasını seçin.

### 2. Credential (Kimlik) Ayarları
Workflow yüklendiğinde bazı node'lar hata verebilir, çünkü kendi API anahtarlarınızı girmelisiniz:
* **Telegram Node'ları:** `Telegram Api` credential'ı oluşturup BotFather'dan aldığınız token'ı girin.
* **Binance Node'ları:** `Binance Api` credential'ı oluşturup Binance Futures API Key & Secret'ınızı girin.

### 3. Kullanıcı Ayarı (⚠️ Çok Önemli)
Botun başkası tarafından kullanılmasını engellemek için:
1. Workflow'un en başındaki **"Kullanıcı Kontrol"** (If Node) kutusuna çift tıklayın.
2. `Value 1` veya `Right Value` kısmında yazan `KullaniciAdi` değerini silin.
3. Yerine kendi **Telegram Kullanıcı Adınızı** (başında @ olmadan) yazın.

### 4. Aktifleştirme
* Her şeyi ayarladıktan sonra üstteki **"Active"** butonunu açın.
* Telegram botunuza `/start` yazarak test edin.

---

## ⚠️ Sorumluluk Reddi
Bu workflow eğitim amaçlı hazırlanmıştır. Finansal işlemler risk içerir. Yazılımı kullanarak yapacağınız işlemlerden doğabilecek kâr veya zarar tamamen kullanıcının sorumluluğundadır. Lütfen gerçek bakiyelerle işlem yapmadan önce küçük tutarlarla test ediniz.

---
*Bu proje [Yaşar Abi'nin n8n Projeleri](https://github.com/YasarAbi/N8N_Projeler) serisinin bir parçasıdır.*