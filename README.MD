# 🚀 Yaşar Abi'nin n8n Otomasyon Projeleri

![n8n](https://img.shields.io/badge/n8n-Automations-orange?style=for-the-badge&logo=n8n)
![GitHub](https://img.shields.io/badge/Open%20Source-Yes-green?style=for-the-badge&logo=github)

Selamlar! 👋
Bu repository, **n8n** kullanarak geliştirdiğim kişisel otomasyon süreçlerini, trading botlarını ve hayatı kolaylaştıran araçları içerir. Açık kaynak kültürüne katkı sağlamak amacıyla projelerimi burada paylaşıyorum.

İster direkt kullanın, ister kendi ihtiyaçlarınıza göre düzenleyin.

---

## 📂 Projeler Listesi

### 1. 🤖 Binance Futures Trading Bot (Telegram Entegreli)
Binance Vadeli İşlemler (Futures) hesabınızı Telegram üzerinden yönetmenizi sağlayan, güvenlik odaklı bir ticaret asistanı.

* **Dosya:** `Binance_Bot.json`
* **Özellikler:**
  * 📊 **Cüzdan & PNL Raporu:** Tek komutla toplam bakiye, marjin ve anlık kâr/zarar durumu.
  * 🚨 **Panik Butonu:** Acil durumlarda tüm açık pozisyonları anında Market fiyatından kapatma.
  * 🔐 **Kişisel Güvenlik:** Sadece yetkili Telegram kullanıcısından gelen komutları işleme alır.
  * 🧠 **Akıllı Emir:** Coin'e özel fiyat hassasiyetini (precision) otomatik hesaplar, API hatalarını önler.
  * 💰 **Multi-Asset Desteği:** Cüzdandaki USDT ve USDC bakiyelerini otomatik tarar.

---

## ⚙️ Nasıl Kullanılır?

1.  İlgili projenin `.json` dosyasını indirin.
2.  Kendi **n8n** panelinizde **"Import from File"** diyerek yükleyin.
3.  Workflow içindeki **Credentials** (API Anahtarları) alanlarını kendi bilgilerinizle doldurun.
4.  Varsa `Sticky Note` (Sarı notlar) içindeki özel ayarları (örn: Telegram kullanıcı adı) yapın.
5.  **Activate** butonuna basıp arkanıza yaslanın! 🚀

## ⚠️ Yasal Uyarı & Sorumluluk Reddi

Burada paylaşılan kodlar **eğitim ve kişisel kullanım** amaçlıdır.
* **Finansal Tavsiye Değildir:** Trading botları veya finansal araçlar kullanmak risk içerir.
* **Sorumluluk:** Bu yazılımları kullanarak yaptığınız işlemlerden doğabilecek kâr veya zarar tamamen kullanıcının sorumluluğundadır.
* API anahtarlarınızın güvenliğini sağlamak sizin sorumluluğunuzdadır.

---

⭐ **Projeleri beğendiyseniz sağ üstten Star vermeyi unutmayın!**