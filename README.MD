# 🚀 Yaşar Abi'nin n8n Otomasyon Atölyesi

![n8n](https://img.shields.io/badge/n8n-Workflow-orange?style=for-the-badge&logo=n8n)
![GitHub](https://img.shields.io/badge/Open%20Source-Yes-green?style=for-the-badge&logo=github)
![Maintenance](https://img.shields.io/badge/Maintained-Yes-blue?style=for-the-badge)

Selamlar! 👋
Bu repository, **n8n** kullanarak geliştirdiğim otomasyon süreçlerini, botları ve entegrasyonları topladığım kişisel kütüphanemdir.

Amacım; finansal takip, kişisel asistanlık ve veri yönetimi gibi konularda işleri kolaylaştıran **açık kaynak** çözümler üretmek ve paylaşmaktır. Haftalık olarak yeni projeler eklemeye çalışıyorum.

---

## 📚 Proje Listesi

Buradaki klasörlere tıklayarak ilgili projenin detaylarına, kurulum rehberine ve `.json` dosyalarına ulaşabilirsiniz.

| ID | Proje Adı | Kategori | Durum |
| :--- | :--- | :--- | :--- |
| **001** | [**Binance Futures Telegram Bot**](./001_Binance_Telegram_Bot) | 💰 Finans / Trading | ✅ Yayında |
| **002** | *Yakında...* | ⏳ | 🚧 Hazırlanıyor |
| **003** | *Yakında...* | ⏳ | 🚧 Hazırlanıyor |

---

## 🛠️ Genel Kurulum Mantığı

Bu repodaki projeleri kullanmak için temel adımlar şöyledir (Her projenin kendi klasöründe detaylı rehber mevcuttur):

1.  **İndir:** İlgili projenin klasöründeki `.json` dosyasını bilgisayarınıza indirin.
2.  **İçe Aktar (Import):** n8n panelinizde sağ üstten `Import from File` seçeneği ile dosyayı yükleyin.
3.  **Kimlik Doğrulama (Credentials):** Workflow içindeki kırmızı uyarı veren node'lara (Telegram, Google Sheets, OpenAI vb.) kendi API anahtarlarınızı girin.
4.  **Aktifleştir:** Workflow'u `Active` konuma getirin.

---

## 🤝 Katkıda Bulunma

Projelerimi geliştirmek veya hata bildirmek isterseniz:
* Bir **Issue** açabilirsiniz.
* Projeyi **Fork**'layıp geliştirmeler yaptıktan sonra **Pull Request** gönderebilirsiniz.
* Ya da sadece bir ⭐ **Star** bırakarak destek olabilirsiniz!

---
*Bu repo [Yaşar Abi](https://github.com/YasarAbi) tarafından yönetilmektedir.*