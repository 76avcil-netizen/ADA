# ADA Wallet

**Bir ada, tek cüzdan.** KKTC'nin tüm kahve dükkânlarında geçerli ön-ödemeli sadakat ve ödeme ağı.

Starbucks kartı mantığı — ama ada genelindeki tüm kafe ve kahve dükkânları için. Kullanıcı tek bir cüzdana kredi yükler, katılımcı kafede QR ile öder. Lefkoşa'dan Girne'ye, Mağusa'ya — aynı bakiye, aynı puan.

## Özellikler

- ☕ **Ön-ödemeli sanal cüzdan** — kredini yükle, ada genelinde harca
- 📱 **QR ile ödeme** — 2 saniyede, POS gerektirmez
- 🎁 **Ada-geneli puan** — hangi kafede olursan ol, ödül birikir
- 🗺️ **3 şehir ağı** — Lefkoşa, Girne, Mağusa
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
python3 -m http.server 8090
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

## İletişim

- ✉️ hello@adawallet.com
- 📞 +90 533 966 88 77
- 💬 WhatsApp: wa.me/905339668877

---

© 2026 ADA Wallet — Bir ada, tek cüzdan.
