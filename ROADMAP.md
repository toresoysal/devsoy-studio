# Dev/Soy Web Stüdyosu — Proje Yol Haritası

> **Dev/Soy Danışmanlık** bünyesinde açılan **Dev/Soy Web Stüdyosu**,  
> Kuzey Kıbrıs'ın ilk portföy-odaklı web tasarım stüdyosudur.  
> Domain: `devsoy.web` (veya `dsostudio.com`)

---

## 🗺 Genel Yapı

```
dso-studio/
│
├── ROADMAP.md                   ← Bu dosya
├── DSO_STUDIO_BRIEF.md          ← Konsept & marka brief
│
├── devsoy-web.html              ← Stüdyo ana sayfası (müşteri yönlendirme)
│
├── demos/
│   ├── demo-butik.html          ← Sıcak lüks butik
│   ├── demo-kirtasiye.html      ← Eğlenceli kırtasiye (piksel-at)
│   ├── demo-spor.html           ← Aşırı lüks spor giyim
│   ├── demo-arac-parca.html     ← Endüstriyel araç parça
│   └── demo-galeri.html         ← Sanat galerisi
│
└── admin/
    ├── admin-butik.html
    ├── admin-kirtasiye.html
    ├── admin-spor.html
    ├── admin-arac-parca.html
    └── admin-galeri.html
```

---

## 📅 Sprint Planı

### Sprint 0 — Temel & Döküman (1 gün)
- [x] ROADMAP.md hazırla
- [x] DSO_STUDIO_BRIEF.md hazırla
- [ ] Ortak CSS değişkenleri & token sistemi kararlaştır

### Sprint 1 — Demo Siteler (5–7 gün)
| # | Site | Estetik Yüz | Durum |
|---|------|-------------|-------|
| 1 | Butik Giyim | Sıcak Lüks | ✅ Üretildi |
| 2 | Kırtasiye | Piksel-at / Eğlenceli | ✅ Üretildi |
| 3 | Spor Giyim | Aşırı Lüks | ✅ Üretildi |
| 4 | Araç Parça | Endüstriyel Güç | ✅ Üretildi |
| 5 | Galeri | Minimal Sanat | ✅ Üretildi |

### Sprint 2 — Admin Paneller (5–7 gün)
| # | Panel | Özellikler | Durum |
|---|-------|------------|-------|
| 1 | Butik Admin | Ürün listesi, fiyat, stok, görsel | ✅ |
| 2 | Kırtasiye Admin | Kategori, ürün, kampanya | ✅ |
| 3 | Spor Admin | Koleksiyon, beden, renk yönetimi | ✅ |
| 4 | Araç Admin | Marka/model filtre, stok takibi | ✅ |
| 5 | Galeri Admin | Eser yükleme, sergi yönetimi | ✅ |

### Sprint 3 — Dev/Soy Web Stüdyosu Ana Sayfası (3 gün)
- [ ] Hero bölümü (stüdyo kimliği)
- [ ] Hizmetler grid'i (web tasarım, marka kimliği, SEO, sosyal medya…)
- [ ] Demo showcase — 5 örnek siteye yönlendirme
- [ ] Müşteri referans alanı (placeholder)
- [ ] İletişim / teklif formu
- [ ] Footer (devsoy.online bağlantısı)

### Sprint 4 — Sunum & Müşteri Paketi (2 gün)
- [ ] Müşteriye sunulacak PDF brief hazırla
- [ ] Her demo için QR kod üret
- [ ] Demo linkleri Instagram story formatına dönüştür
- [ ] Fiyat listesi sayfası tasarla

---

## 🎨 Estetik Yüz Sistemi

Dev/Soy Web Stüdyosu **3 estetik yüz** sunar ve her projeyi bu yüzlerden birine yerleştirir:

### Yüz 1: SICAK (Warm & Premium)
> *Butik giyim, restoran, otel, kozmetik*
- Krem / krem beyaz arka plan
- Terrakota ve altın aksanlar
- Serif tipografi (Cormorant, Playfair)
- Organik şekiller, ılık fotoğraflar

### Yüz 2: AŞIRI LÜKS (Ultra Luxury)
> *High-end moda, spor lüks, emlak, yat kiralama*
- Siyah / koyu arka plan
- Altın, platin aksan
- Condensed + ince serif kombinasyonu
- Geometrik kompozisyon, beyaz boşluk

### Yüz 3: PİKSEL-AT (Playful Digital)
> *Kırtasiye, çocuk ürünleri, teknoloji, oyun*
- Canlı renkler, kontrast çiftler
- Pixel / retro + modern sans-serif
- Eğimli bölümler, confetti elementler
- Animasyon ağırlıklı

---

## 🛠 Teknik Stack (Her Demo İçin)

```
- Saf HTML5 + CSS3 + Vanilla JS
- Google Fonts (Google CDN)
- Font Awesome 6 (CDN)
- Hiçbir framework bağımlılığı yok
- Tüm görseller: CSS gradient / SVG / emoji tabanlı
- Responsive: mobile-first
```

---

## 💼 Servis Kataloğu (devsoy.web sitesinde gösterilecek)

| Hizmet | Açıklama | Süre |
|--------|----------|------|
| Kurumsal Web Sitesi | 5–10 sayfa, mobil uyumlu | 2–3 hafta |
| E-Ticaret Sitesi | Ürün yönetimi + ödeme entegrasyonu | 3–5 hafta |
| Marka Kimliği | Logo, renk paleti, tipografi rehberi | 1 hafta |
| Sosyal Medya Tasarımı | Post şablonları, story, highlight | 3–5 gün |
| SEO & İçerik | Sayfa optimizasyonu, meta yapı | Süregelen |
| Bakım & Destek | Güncelleme, hosting desteği | Aylık |

---

## 📌 Notlar

- Tüm demo siteler `demos/` klasöründe, adminler `admin/` klasöründe
- Admin paneller tamamen bağımsız HTML dosyaları (backend gerektirmez)
- Müşteriye sunum: tarayıcıda doğrudan aç, Canva'ya export, WhatsApp paylaşım
- Her demo için admin paneli ayrı link olarak sunulabilir
- `devsoy.web` domain alındığında tüm dosyalar tek klasör olarak Vercel/Netlify'a atılır

---

*Son güncelleme: Dev/Soy Web Stüdyosu v1.0 — Kuzey Kıbrıs'ın dijital yüzü*
