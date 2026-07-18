# ADA Wallet — TODO / Yapılacaklar

> Proje durumu ve geliştirme disiplini. Her "yapıldı" iş için commit atılır.

## ✅ Tamamlanan (16 Tem 2026)
- [x] README tutarsızlığı giderildi: "3 şehir" → "6 ilçe" (Lefkoşa, Girne, Gazimağusa, İskele, Güzelyurt, Lefke)
- [x] Yerel dev komutu `127.0.0.1`'e sabitlendi (`python3 -m http.server 8090 --bind 127.0.0.1`)
- [x] pitch.html'e scroll-reveal animasyonu eklendi (script.js'e dokunmadan, kendi script'i içinde)
- [x] pitch.html "3 şehir" → "6 ilçe" tutarlılığı sağlandı
- [x] Harita (#map) bölümü tamamen kaldırıldı (SVG + PNG + nav linki) — 6 ilçe bilgisi hero istatistiğine taşındı ("6 İlçe")

## 🔲 Sıradaki İşler
- [ ] Güvenlik: Formspree honeypot alanı ekle (spam koruması)
- [ ] Güvenlik: Google Fonts CDN gizlilik notu (SNI/ISP görünürlüğü) — yerel font'a geçiş değerlendir
- [ ] Kaliteli commit convention devamı (feat/docs/style/fix + changeset disiplini)
- [ ] pitch.html ↔ index.html görsel tema birliği kontrolü
- [ ] Mobil (responsive) test: index.html + pitch.html telefon genişliğinde
- [ ] Vercel deploy doğrulama (build command boş, output `.`)

## 📁 Değişiklik → Etki Haritası
| Dosya | Değişirse etkilenen | Etkilenmez |
|-------|--------------------|-----------|
| `style.css` | index.html | pitch.html |
| `script.js` | index.html | pitch.html |
| `index.html` | script.js, style.css, favicon.svg, Formspree endpoint | pitch.html |
| `pitch.html` | (kendi başına) | index.html, script.js, style.css |
| `favicon.svg` | index.html, pitch.html | — |

## 🔒 Güvenlik Notları
- README'deki iletişim formu `formspree.io/f/meebyvve` üzerinden — public HTML'de.
- Dev sunucusu `127.0.0.1`'e bağlı (dışarıdan erişim kapalı).
- Windows Firewall kuralı: port 80/8081/5432/5433/6379 gelen trafik engelli.

## 🧰 Dev Komutları (kaliteli kullanım)
```bash
# Yerel çalıştırma (sadece localhost)
python3 -m http.server 8090 --bind 127.0.0.1

# Git disiplini
git add -p            # satır satır ekle, gereksiz değişiklik girmez
git commit -m "type: kısa açıklama"
git push origin main

# Commit tipleri: feat / fix / docs / style / refactor / test / chore
```

## 📌 İletişim
- hello@adawallet.com · +90 533 966 88 77 · WhatsApp: wa.me/905339668877
