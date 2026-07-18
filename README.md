# ADA Wallet

**Bir ada, tek cüzdan.** KKTC'nin tüm kahve dükkânlarında geçerli ön-ödemeli sadakat ve ödeme ağı.

Ön-ödemeli ada-geneli sadakat ağı — ada genelindeki tüm kafe ve kahve dükkânları için. Kullanıcı tek bir cüzdana kredi yükler, katılımcı kafede QR ile öder. Lefkoşa'dan Girne'ye, Mağusa'ya — aynı bakiye, aynı puan.

## Özellikler

- ☕ **Ön-ödemeli sanal cüzdan** — kredini yükle, ada genelinde harca
- 📱 **QR ile ödeme** — 2 saniyede, POS gerektirmez
- 🎁 **Ada-geneli puan** — hangi kafede olursan ol, ödül birikir
- 🗺️ **6 ilçe ağı** — Lefkoşa, Girne, Gazimağusa, İskele, Güzelyurt, Lefke
- 💼 **Kafe için** — ortak müşteri havuzu, nakit akışı, analitik

## İş Modeli

| Kanal | Açıklama |
|-------|----------|
| İşlem komisyonu | Her QR ödemede %2 |
| Kafe aboneliği | Pro plan ₺4.900/ay |
| Kredi bakiyesi (float) | Yüklenen bakiyenin kısa vadeli değeri (regülasyona bağlı) |

## Dosya Yapısı

```
ada-wallet/
├── index.html      # Landing page (kafe sahipleri + kullanıcılar)
├── pitch.html      # Yatırımcı sunumu (9 slayt)
├── style.css       # Ortak stiller (kahve çekirdeği teması)
├── script.js       # Nav, scroll reveal, sayaçlar, form
├── favicon.svg     # Kahve çekirdeği logosu
└── README.md
```

Landing ve pitch deck birbirine bağlı:
- Footer'dan **📊 Yatırımcı Sunumu** → `pitch.html`
- Pitch deck'ten **← Siteye dön** → `index.html`

## Yerel Çalıştırma

```bash
# kök dizinde
python3 -m http.server 8090 --bind 127.0.0.1
# tarayıcıda:
# http://localhost:8090/ada-wallet/index.html
# http://localhost:8090/ada-wallet/pitch.html
```

## Vercel Deploy

1. vercel.com → **Add New → Project**
2. **Import Git Repository** → `76avcil-netizen/ADA`
3. Framework: **Other** (statik HTML)
4. Build Command: (boş) · Output Directory: `.`
5. **Deploy**

İletişim formu **Formspree** (`f/meebyvve`) üzerinden çalışır — endpoint'i `index.html` içinde değiştirebilirsin.

## Gizlilik Notu

Sayfalar Google Fonts CDN (`fonts.googleapis.com`) üzerinden font yükler. HTTPS şifreli olsa da **SNI alanı düz metin** gider; yani ziyaretçinin ISP'i "hangi siteye girdiğini" (hostname) görür. Font CDN trafiği de bu kapsamdadır. Bunun etkisini azaltmak için:

- Font isteği `display=swap` ile **non-blocking** yüklenir (metin font yüklenmeden görünür).
- `preconnect` ile CDN handshake hızlandırılır.
- Tam gizlilik isteniyorsa fontlar ileride yerel (`/fonts/`) olarak gömülebilir (henüz yapılmadı).

## İletişim

- ✉️ hello@adawallet.com
- 📞 +90 533 966 88 77
- 💬 WhatsApp: wa.me/905339668877

---

© 2026 ADA Wallet — Bir ada, tek cüzdan.
