# 🎲 Oyunla Matematik: Geritmetik Sayı Dizisi

> Aritmetik ve geometrik dizilerin birleşiminden oluşan **geritmetik sayı dizisi** formülünü iki oyunculu bir tahta oyunuyla öğren!

[![HTML](https://img.shields.io/badge/HTML-single--file-orange?logo=html5)](geritmetik-oyunu.html)
[![License](https://img.shields.io/badge/license-MIT-blue)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-web-brightgreen)](https://github.com/)

---

## 📖 Proje Hakkında

Bu proje, Lal Su Narinç'in **TÜBİTAK 2204-B 2021** yarışmasında bölge birincisi olan *"Geritmetik Sayı Dizisi ve Özellikleri"* başlıklı akademik çalışmasından esinlenerek geliştirilmiştir.

**Hedef kitle:** BİLSEM ÖYG öğrencileri  
**Amaç:** Öğrencilerin geritmetik dizi formülünü eğlenerek, rekabet ederek pekiştirmesi

---

## 🧮 Geritmetik Dizi Nedir?

Her terimi, bir önceki terimin **r katının d fazlasına** eşit olan sayı dizisidir:

```
a(n+1) = r · a(n) + d
```

### Genel Terim Formülü

```
a(n) = a₁ · r^(n-1) + d · ( (r^(n-1) - 1) / (r - 1) )
```

### Ardışık Farklar Dizisi

```
f(n) = r^(n-1) · [ a₁·(r-1) + d ]
```

Ardışık farklar dizisi, ortak çarpanı **r** olan bir **geometrik dizidir**.

### Örnek

`a₁ = 2, r = 3, d = 4` olan geritmetik dizi:

| n | 1 | 2 | 3 | 4 | 5 |
|---|---|---|---|---|---|
| a(n) | 2 | 10 | 34 | 106 | 322 |
| f(n) | — | 8 | 24 | 72 | 216 |

---

## 🎮 Oyun Nasıl Oynanır?

### Oyun Akışı

1. Oyun başladığında 4 değişken kartı rastgele belirlenir: **a₁**, **r**, **d**, **n**
2. Aktif oyuncu formülü kullanarak **Terim(n)** değerini hesaplar
3. Cevabı 60 saniye içinde girer
4. Her turun sonunda adım adım çözüm ekranı gösterilir
5. **50 adıma** ilk ulaşan oyuncu kazanır!

### Puanlama

| Durum | Adım |
|-------|------|
| ✅ Doğru cevap | **+5** |
| ❌ Yanlış cevap | **−2** |
| ⏰ Süre doldu | **−2** |
| 💡 Formül hatırlatıcı | **−1** |

### Değişken Aralıkları

| Değişken | Açıklama | Aralık |
|----------|----------|--------|
| `a₁` | İlk terim | [1, 5] |
| `r` | Geometrik oran / çarpan | [2, 4] |
| `d` | Aritmetik fark | [1, 5] |
| `n` | İstenen terim numarası | [2, 7] |

---

## 🚀 Kurulum ve Kullanım

Bu proje **saf HTML/CSS/JavaScript** ile yazılmıştır — herhangi bir kurulum, bağımlılık veya sunucu gerektirmez.

```bash
# Repoyu klonla
git clone https://github.com/kullanici-adi/geritmetik-oyunu.git

# Dosyayı tarayıcıda aç
open geritmetik-oyunu.html
# veya
double-click geritmetik-oyunu.html
```

---

## 🛠️ Teknik Detaylar

### Kullanılan Teknolojiler

| Teknoloji | Kullanım |
|-----------|----------|
| HTML5 | Yapı |
| CSS3 | Tasarım, animasyonlar |
| Vanilla JavaScript | Oyun mantığı |
| Google Fonts (Nunito) | Tipografi |

### Özellikler

- 📱 **Responsive** — mobil ve masaüstü uyumlu
- 🌐 **Offline** — internet bağlantısı gerektirmez
- 📦 **Single-file** — tek `.html` dosyası, sıfır bağımlılık
- ⚡ **Hızlı** — herhangi bir framework yok

### Proje Yapısı

```
geritmetik-oyunu/
│
├── geritmetik-oyunu.html   # Oyunun tamamı (tek dosya)
├── README.md               # Bu dosya
└── Geritmetik_Proje_Raporu.pdf  # Akademik proje raporu
```

---

## 📸 Ekran Görüntüleri

| Karşılama Ekranı | Oyun Ekranı |
|-----------------|-------------|
| Kurallar ve başlat butonu | Kartlar, zamanlayıcı, tahta |

| Formül Çözüm Ekranı | Oyun Tahtası |
|--------------------|-------------|
| Adım adım hesaplama | Yılan düzeninde 50 kare |

---

## 🧪 Formül Doğrulama

Oyundaki formülü elle doğrulamak için:

```
a₁ = 3,  r = 2,  d = 5,  n = 4

Geometrik kısım:  3 × 2^3 = 24
Toplam kısım:     5 × (2^3 - 1) / (2 - 1) = 5 × 7 = 35

Terim(4) = 24 + 35 = 59  ✓
```

---

## 📚 Akademik Referans

Bu projenin matematiksel temeli:

> Narinç, L. S. (2021). *Geritmetik Sayı Dizisi ve Özellikleri*.  
> TÜBİTAK 2204-B Ortaokul Öğrencileri Araştırma Projeleri Yarışması — **Bölge 1.si**

Detaylı matematiksel türetme ve ispat için [`Geritmetik_Proje_Raporu.pdf`](Geritmetik_Proje_Raporu.pdf) dosyasına bakınız.

---

## 🗓️ Geliştirme Süreci

```
Ocak    → Literatür taraması
Şubat   → Formüllerin türetilmesi ve ispatı
Mart    → Oyun tasarımı + Flutter prototipi
Nisan   → Web uygulamasına taşıma (HTML/CSS/JS)
```

---

## 🤝 Katkıda Bulunma

1. Bu repoyu fork'la
2. Yeni bir branch oluştur: `git checkout -b ozellik/yeni-ozellik`
3. Değişikliklerini commit'le: `git commit -m 'Yeni özellik eklendi'`
4. Branch'ini push'la: `git push origin ozellik/yeni-ozellik`
5. Pull Request aç

---

## 📄 Lisans

Bu proje MIT lisansı ile lisanslanmıştır. Detaylar için [LICENSE](LICENSE) dosyasına bakınız.

---

<div align="center">

**BİLSEM Matematik Projesi**  
Orijinal teorik içerik © Lal Su Narinç (2021)

</div>
