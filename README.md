# TUSAŞ Proje Risk Simülatörü

> **Jet Eğitim Uçağı Geliştirmek İçin Bilinmeyeni Yönetmek**  
> Hacettepe Üniversitesi · Endüstri Mühendisliği · TUSAŞ İş Birliği

Interaktif bir proje risk simülatörü. Gerçek TUSAŞ proje verisine dayalı olarak aktivite gecikmelerinin proje süresine ve mali etkisine interaktif biçimde gösterir.

---

## 🚀 Canlı Demo

**GitHub Pages:** `https://<kullaniciadi>.github.io/tusas-risk-simulator`

---

## 📋 Özellikler

- **Adım 1 — Aktivite & Gecikme:** 8 farklı kritiklik seviyesindeki aktiviteden birini seçip gecikme girişi yaparak projeye yansımasını anlık görün
- **Adım 2 — Mali Etki Analizi:** Günlük ceza kaydırıcısıyla gecikmenin TL cinsinden maliyetini hesaplayın
- **Adım 3 — Sensitivity Analizi (Kaynak Kararı):** 30 günlük hızlandırma bütçenizi en verimli aktiviteye yönlendirin

---

## 🏗️ Kurulum

### GitHub Pages ile yayınlama (önerilen)

1. Bu repoyu GitHub'a yükleyin:
```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/<kullaniciadi>/tusas-risk-simulator.git
git push -u origin main
```

2. GitHub'da: **Settings → Pages → Source: main / (root)** seçin

3. Birkaç dakika içinde `https://<kullaniciadi>.github.io/tusas-risk-simulator` adresinde yayında!

### Lokal çalıştırma

```bash
# Python ile
python -m http.server 8000

# Node.js ile
npx serve .
```

Tarayıcıda `http://localhost:8000` adresini açın.

---

## 📁 Dosya Yapısı

```
tusas-risk-simulator/
├── index.html        # Ana uygulama (tek dosya, bağımlılık yok)
└── README.md         # Bu dosya
```

Tüm uygulama tek HTML dosyasında — harici JavaScript kütüphanesi veya build adımı gerekmez. Google Fonts CDN üzerinden yüklenir.

---

## 📊 Kullanılan Veri

Gerçek TUSAŞ askeri jet eğitim uçağı geliştirme projesinden alınan aktiviteler:

| Aktivite | Süre | Kritiklik İndeksi (CI) |
|---|---|---|
| System Requirements Review | 45 gün | %100 |
| Final Acceptance | 30 gün | %100 |
| Critical Design Review | 60 gün | %86.9 |
| First Metal Cut | 30 gün | %86.9 |
| Ground Vibration Test | 25 gün | %86.9 |
| Final Assembly Completion | 90 gün | %42.3 |
| Avionics Integration Start | 50 gün | %28.4 |
| Compliance Demo Review | 15 gün | %12.1 |

**Metodoloji:** CPM (3.099 gün) → PERT → Monte Carlo Simülasyonu (10.000 iterasyon, ortalama: 3.252 gün)

---

## 👥 Proje Ekibi

- Tuğçe Başaran
- Tarık Buğra Birinci
- Zeynep Kızkapan
- Koray Sarı

**Akademik Danışman:** Doç. Dr. Diclehan Tezcaner Öztürk

---

## 📄 Lisans

Bu proje akademik amaçlıdır. TUSAŞ proje verileri gizlilik kapsamındadır; simülatörde kullanılan değerler temsili niteliktedir.
