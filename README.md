# Veri Tabanı 2 — Ders Notları ve Uygulamalar

Bu depo, **Veri Tabanı 2** dersi kapsamında tutulan ders notlarını, ders içi aktiviteleri, uygulamaları, örnek veritabanı çalışmalarını ve yararlanılan kaynakları düzenli biçimde arşivlemek amacıyla hazırlanmıştır.

> Bu repository dönem boyunca güncellenecektir. Yeni konular işlendikçe ilgili ders notları ve sınıf içi çalışmalar uygun klasörlere eklenecektir.

## Öğrenci Bilgileri

| Bilgi | Değer |
| --- | --- |
| **Ad Soyad** | Hasan Mert Koku |
| **Öğrenci No** | 202551501055 |
| **Ders** | Veri Tabanı 2 |
| **Repository** | `veri-tabani-2` |

## Repository Amacı

Bu çalışmanın temel amaçları:

- Ders sırasında işlenen konuları düzenli ve tekrar edilebilir notlar hâline getirmek,
- Veritabanı tasarımıyla ilgili kavramları örneklerle pekiştirmek,
- Ders içi aktiviteleri ve uygulamaları ayrı olarak arşivlemek,
- Microsoft Access ve ilişkisel veritabanı mantığıyla yapılan çalışmaları belgelemek,
- Sınav ve uygulama çalışmalarında hızlı başvuru kaynağı oluşturmak,
- Dönem sonunda ders boyunca yapılan çalışmaların tek bir GitHub deposunda toplanmasını sağlamaktır.

## İçerik Yapısı

```text
veri-tabani-2/
├── README.md
├── ders-notlari/
│   ├── README.md
│   └── 01-veritabani-temelleri.md
├── ders-ici-aktiviteler/
│   └── README.md
└── kaynaklar/
    └── README.md
```

### `ders-notlari/`

Derslerde anlatılan teorik konular, önemli tanımlar, öğretim elemanının vurguladığı noktalar ve örnekler burada tutulur.

### `ders-ici-aktiviteler/`

Sınıfta yapılan uygulamalar, örnek senaryolar, tablo tasarımları, sorgular ve diğer pratik çalışmalar burada belgelenir.

### `kaynaklar/`

Ders sırasında veya ders dışında yararlanılan faydalı kaynaklar, dokümantasyon bağlantıları ve çalışma önerileri burada listelenir.

## Ders Kapsamında Takip Edilecek Konular

Dönem boyunca aşağıdaki başlıklar işlendikçe repository genişletilecektir:

- Veritabanı ve ilişkisel veritabanı kavramları
- Tablo, kayıt ve alan yapısı
- Birincil anahtar (Primary Key)
- Yabancı anahtar (Foreign Key)
- Tablolar arası ilişkiler
- Veri türleri ve doğru veri türü seçimi
- Veri bütünlüğü
- Normalizasyon mantığı
- Microsoft Access ile veritabanı oluşturma
- Sorgular
- Formlar
- Raporlar
- Gerçek hayat senaryolarının veritabanına dönüştürülmesi
- Güvenli biçimde saklanması gereken / saklanmaması gereken veriler

> Konu listesi dersin gerçek ilerleyişine göre güncellenecek; henüz işlenmeyen konular ders notu olarak gösterilmeyecektir.

## Kullanılan / Kullanılacak Araçlar

| Araç / Teknoloji | Kullanım Amacı |
| --- | --- |
| **Microsoft Access** | Veritabanı oluşturma, tablo, ilişki, sorgu, form ve rapor çalışmaları |
| **SQL** | Sorgulama mantığını ve temel veritabanı işlemlerini anlamak |
| **GitHub** | Ders notlarını ve uygulamaları sürüm kontrollü biçimde arşivlemek |
| **Markdown** | Ders dokümantasyonunu okunabilir ve düzenli tutmak |

## Notlandırma Sistemi

Ders notlarında mümkün olduğunca aşağıdaki yapı kullanılacaktır:

1. **Konu** — Derste işlenen ana başlık
2. **Tanım** — Kavramın kısa açıklaması
3. **Ders Notu** — Derste vurgulanan önemli noktalar
4. **Örnek** — Konunun gerçek hayat veya Access üzerinden örneği
5. **Dikkat Edilecek Noktalar** — Sık yapılan hatalar
6. **Ders İçi Aktivite** — Varsa ilgili uygulamanın bağlantısı
7. **Kısa Tekrar** — Sınav öncesi hızlı gözden geçirme bölümü

## Ders İçi Aktivite Formatı

Her aktivite mümkün olduğunca şu bilgilerle kaydedilecektir:

- Aktivite başlığı
- Tarih / hafta
- Amaç
- Verilen senaryo
- Yapılan işlemler
- Oluşturulan tablolar ve alanlar
- Kullanılan anahtarlar ve ilişkiler
- Sonuç
- Derste belirtilen önemli notlar

## Dosya Adlandırma Standardı

Dosyaların sıralı kalması için numaralı adlandırma kullanılacaktır.

```text
01-veritabani-temelleri.md
02-tablolar-ve-veri-turleri.md
03-primary-key-ve-iliskiler.md
```

Ders içi aktivitelerde de benzer bir düzen kullanılacaktır:

```text
01-ornek-veritabani-tasarimi.md
02-access-tablo-uygulamasi.md
```

## Haftalık İlerleme

| Hafta | Konu | Ders Notu | Aktivite | Durum |
| --- | --- | --- | --- | --- |
| 1 | Veritabanı temelleri | [Ders Notu](ders-notlari/01-veritabani-temelleri.md) | — | Başlandı |
| 2 | Eklenecek | — | — | Bekliyor |
| 3 | Eklenecek | — | — | Bekliyor |

Bu tablo her ders sonrasında güncellenecektir.

## Çalışma İlkeleri

- Derste anlatılmayan içerikler ders notuymuş gibi eklenmeyecektir.
- Örnekler mümkün olduğunca gerçek hayat senaryoları üzerinden açıklanacaktır.
- Veritabanı tasarımında gereksiz veri tekrarından kaçınılacaktır.
- Hassas bilgilerin veritabanında nasıl tutulması gerektiği güvenlik açısından ayrıca değerlendirilecektir.
- Ders içi uygulamalar teorik notlardan ayrı tutulacaktır.
- Yeni içerikler eklendikçe bu README ana indeks olarak güncellenecektir.

## Hızlı Erişim

- 📘 [Ders Notları](ders-notlari/README.md)
- 🧪 [Ders İçi Aktiviteler](ders-ici-aktiviteler/README.md)
- 🔗 [Kaynaklar](kaynaklar/README.md)

---

**Hasan Mert Koku**  
**Öğrenci No:** 202551501055  
**Ders:** Veri Tabanı 2
