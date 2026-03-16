# Dev/Soy Web Stüdyosu — Deployment Rehberi

## Klasör Yapısı

```
dso-studio/
│
├── devsoy-web.html          ← ANA SAYFA (domain root'a koy)
├── sitemap.html             ← Site haritası
├── ROADMAP.md               ← Proje yol haritası
├── DEVSOY_WEB_STUDIO_BRIEF.md ← Marka brief
│
├── demos/
│   ├── demo-butik.html      ← LUNE Butik Giyim
│   ├── demo-kirtasiye.html  ← KALEM&CO. Kırtasiye
│   ├── demo-spor.html       ← OBSIDIAN Spor Giyim
│   ├── demo-arac-parca.html ← DEMİR PARTS Araç Parça
│   └── demo-galeri.html     ← PHOS Sanat Galerisi
│
└── admin/
    ├── admin-butik.html
    ├── admin-kirtasiye.html
    ├── admin-spor.html
    ├── admin-arac-parca.html
    └── admin-galeri.html
```

---

## Deployment Seçenekleri

### Seçenek A — Netlify Drop (En Kolay, Ücretsiz)
1. https://app.netlify.com/drop adresine git
2. Tüm `dso-studio/` klasörünü sürükle-bırak
3. Netlify otomatik link verir → müşterilere paylaşılabilir

### Seçenek B — Vercel (Önerilen, Ücretsiz)
```bash
npm install -g vercel
cd dso-studio
vercel
# domain: devsoy.web veya özel domain ekle
```

### Seçenek C — Özel Domain ile (devsoy.web / devsoy.online/studio)
1. Domain satın al (ör. devsoy.web veya studio.devsoy.online)
2. Hosting: Netlify, Vercel, GitHub Pages (hepsi ücretsiz)
3. DNS ayarlarını hosting'e yönlendir
4. Dosyaları yükle

### Seçenek D — GitHub Pages (Ücretsiz)
```bash
# GitHub'da yeni repo oluştur: dso-studio
git init
git add .
git commit -m "Dev/Soy Web Stüdyosu v1.0"
git remote add origin https://github.com/KULLANICIADI/dso-studio.git
git push -u origin main
# Repo Settings → Pages → main branch → / (root)
# URL: kullaniciadi.github.io/dso-studio
```

---

## Resim / Asset Gereksinimleri

### ⚠️ Şu An Gerçek Resim Yok
Tüm görseller CSS gradient + emoji ile simüle edilmiştir.  
Gerçek görseller eklemek istersen:

| Dosya | Boyut | Açıklama | Klasör |
|-------|-------|----------|--------|
| `hero-bg.jpg` | 1920×1080 | Ana sayfa hero arka plan görseli | `images/` |
| `butik-hero.jpg` | 1200×800 | LUNE butik koleksiyon görseli | `images/` |
| `spor-hero.jpg` | 1200×800 | OBSIDIAN sporcu/giyim görseli | `images/` |
| `galeri-artwork.jpg` | 800×1000 | Phos galeri örnek eser | `images/` |
| `devsoy-team.jpg` | 800×600 | (Opsiyonel) Ekip fotoğrafı | `images/` |

> **Önemli:** Resim eklemek zorunlu değil. Şu haliyle tamamen işlevsel.

---

## Renk Referansı — Her Demo İçin

| Demo | Birincil | İkincil | Arka Plan |
|------|----------|---------|-----------|
| Butik (LUNE) | `#C1603A` Terrakota | `#B8935A` Altın | `#F9F4EC` Krem |
| Kırtasiye (KALEM&CO.) | `#FFD166` Sarı | `#FF6B6B` Mercan | `#1A1A2E` Koyu |
| Spor (OBSIDIAN) | `#C9A84C` Altın | `#FFFFFF` Beyaz | `#080808` Siyah |
| Araç Parça (DEMİR) | `#E8531A` Turuncu | `#F5C842` Sarı | `#1C2128` Çelik |
| Galeri (PHOS) | `#9B6B4A` Bakır | `#2E2E2A` Mürekkep | `#F8F5F0` Krem |
| Ana Sayfa | `#C9A84C` Altın | `#FFFFFF` Beyaz | `#080808` Siyah |

---

## Font Referansı

| Demo | Display Font | Body Font |
|------|-------------|-----------|
| Butik | Cormorant Garamond | Jost |
| Kırtasiye | Silkscreen | Space Grotesk |
| Spor | Bebas Neue | Raleway |
| Araç Parça | Barlow Condensed | Barlow |
| Galeri | Libre Baskerville | Outfit |
| Ana Sayfa | Playfair Display | Figtree |

Tüm fontlar Google Fonts CDN üzerinden yüklenir — internetsiz çalışmaz.  
Offline kullanım için fontları indir: https://fonts.google.com

---

## Gezinti Sistemi

Her demo ve admin sayfasının **altında sabit bir gezinti şeridi** vardır:

```
[DS Dev/Soy] | [👗 Butik] [✏️ Kırtasiye] [🏃 Spor] [⚙️ Araç] [🎨 Galeri] | [Admin →]
```

- Aktif demo rengiyle altı çizili gösterilir
- Admin sayfalarında demo ↔ admin geçişi butonla yapılır
- Ana sayfaya her zaman [DS Dev/Soy] butonu ile dönülür

---

## Müşteriye Sunum Akışı

1. `devsoy-web.html` aç → müşteri siteyi görür
2. "Portföyü Gör" bölümündeki demo linklerine tıkla → canlı demo
3. "Admin" butonuna tıkla → admin paneli göster
4. Alt gezinti çubuğu ile tüm demolar arası geçiş
5. WhatsApp ile teklif al

---

## Teknik Notlar

- Tüm dosyalar **saf HTML/CSS/JS** — framework yok, build adımı yok
- Fontlar ve ikonlar CDN (internet bağlantısı gerekli)
- Font Awesome 6.5 Free (fa-solid, fa-brands, fa-regular) kullanıldı
- Admin paneller backend gerektirmez — simülasyon modu (JS toast)
- Form gönderimi sadece toast gösterir, gerçek backend yok
- Tüm renkler CSS variables ile — tek dosyadan tema değiştirilebilir

---

*Dev/Soy Web Stüdyosu v1.0 — Kuzey Kıbrıs · devsoy.online*
