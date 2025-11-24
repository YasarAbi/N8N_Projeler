# 🤖 LinkedIn Auto-Reply Bot (n8n + Gemini AI)

> **Motto:** "Yoruma nokta koy, PDF'i DM atayım" devri bitti. "Yorum yaz, AI botum GitHub linkini yapıştırsın" devri başladı. 🚀

## 🎯 Projenin Amacı
LinkedIn'de algoritmayı manipüle etmek için yapılan manuel "Yoruma yaz, sana atayım" süreçlerini otomatize etmek ve bu esnada LinkedIn API kısıtlamalarını **"Browser Emulation"** yöntemiyle aşmak.

Bu proje; yorumları tarar ve **Google Gemini** entegrasyonu sayesinde her kullanıcıya **özel, dinamik ve esprili** bir yanıt vererek proje linkini paylaşır.

---

## ⚙️ Nasıl Çalışır? (The Magic)

LinkedIn'in pahalı ve kısıtlı resmi API'si yerine, bu bot **"Korsan Taksi"** usulü çalışır:

1.  **Veri Çekme (GET):** Tarayıcı oturumunuzu taklit ederek (cURL), gönderiye gelen yorumları çeker.
2.  **Analiz (Logic):**
    * Yorum "n8n" veya "Test" içeriyor mu?
    * Bu yoruma daha önce cevap vermiş miyim? (Stateless Control - Database tutmaz!)
    * Yorumu yazan kişi ben miyim? (Kendine cevap verme!)
3.  **AI Yanıt Üretimi (Gemini):** Google Gemini'ye kullanıcının ismini ve yorumunu gönderir, duruma uygun dinamik bir yanıt metni oluşturur.
4.  **Aksiyon (POST):** Yine tarayıcıyı taklit ederek yorumun altına yanıtı yapıştırır.
5.  **Döngü (Loop):** LinkedIn "Spam" filtresine takılmamak için yorumları 10'ar saniye arayla, tek tek işler.

---

## 🛠️ Kurulum ve Kullanım

### Gereksinimler
* **n8n** (Self-hosted veya Desktop versiyonu - `Execute Command` node'u için gerekli).
* **Docker** (n8n içinde `curl` yüklü olmalı).
* **Google Gemini API Key** (Ücretsiz alınabilir).

### Adım Adım Kurulum
1.  **Workflow'u İçe Aktar:** Repodaki `.json` dosyasını n8n'e import et.
2.  **Cookie Avı:**
    * LinkedIn'i tarayıcıda aç.
    * Herhangi bir gönderiye git, "İncele (Inspect)" -> "Network" sekmesini aç.
    * Yorumları yükle veya bir yorum at.
    * İsteklerden birine sağ tıkla -> `Copy as cURL (bash)`.
3.  **n8n Ayarı:**
    * Kopyaladığın cURL'ü workflow'daki `Input_Curl` (veya ilgili Set node) alanına yapıştır.
    * Kod, Cookie ve CSRF token'ı otomatik ayıklayacaktır.
4.  **Member ID:** `Code` node'u içindeki `MY_ID` değişkenine kendi LinkedIn ID'ni yaz (Böylece bot kendine cevap vermez).
5.  **Çalıştır:** "Execute Workflow" butonuna bas ve arkanı yaslan.

---

## ⚠️ Yasal Uyarı & Sorumluluk Reddi (Disclaimer)

Bu proje tamamen **eğitim ve deneysel (Ar-Ge)** amaçlıdır.

* **Cookie Süresi:** Tarayıcı oturumunuz kapandığında veya cookie süresi dolduğunda cURL komutunu yenilemeniz gerekir.
* **Hesap Güvenliği:** LinkedIn, otomatikleştirilmiş araçları sevmez. Bu botu aşırı agresif (çok hızlı veya binlerce yorum için) kullanmak hesabınızın kısıtlanmasına yol açabilir.
* **Sorumluluk:** Kullanımdan doğacak her türlü sorumluluk (Shadowban, kısıtlama vb.) kullanıcıya aittir.

---

## 🤝 Katkıda Bulun (Contribution)

"Bu regex daha temiz yazılırdı", "Cookie yenilemeyi otomatize ettim", "Docker imajını küçülttüm" diyen babayiğitler; **Fork** atın, **Pull Request** gönderin. Bu kaosu birlikte büyütelim!

---

**Developed by [Yaşar Karaali](https://www.linkedin.com/in/yasarkaraali)** | *Automation with Attitude* 😎