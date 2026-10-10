# Veri Tabanı 2 — Ders Notları ve Uygulamalar

Bu depo, **Veri Tabanı 2** dersi kapsamında tutulan ders notlarını, ders içi aktiviteleri, uygulamaları, örnek veritabanı çalışmalarını ve yararlanılan kaynakları düzenli biçimde arşivlemek amacıyla hazırlanmıştır.

> Bu repository dönem boyunca güncellenecektir. Yeni konular işlendikçe ilgili ders notları ve sınıf içi çalışmalar uygun klasörlere eklenecektir.

## Öğrenci Bilgileri

| 
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
│   ├── README.md
│   ├── aktivite-sablonu.md
│   └── 03-tavuk-durum-paket-servis-veritabani.md
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
- Yapay zekâ tarafından önerilen veritabanı tasarımlarını değerlendirme
- Güvenli biçimde saklanması gereken / saklanmaması gereken veriler

> Konu listesi dersin gerçek ilerleyişine göre güncellenecek; henüz işlenmeyen konular ders notu olarak gösterilmeyecektir.

## Kullanılan / Kullanılacak Araçlar

| Araç / Teknoloji | Kullanım Amacı |
| --- | --- |
| **Microsoft Access** | Veritabanı oluşturma, tablo, ilişki, sorgu, form ve rapor çalışmaları |
| **Google Gemini** | Gerçek hayat senaryolarından tablo/alan önerileri almak ve önerileri veritabanı mantığı açısından değerlendirmek |
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
03-tavuk-durum-paket-servis-veritabani.md
```

## Haftalık İlerleme

| Hafta / Ders | Konu | Ders Notu | Aktivite | Durum |
| --- | --- | --- | --- | --- |
| 1 | Veritabanı temelleri | [Ders Notu](ders-notlari/01-veritabani-temelleri.md) | — | Başlandı |
| 2 | Eklenecek | — | — | Bekliyor |
| 3 | Tavuk dürüm paket servis sistemi için veritabanı tablolarının belirlenmesi; Gemini çıktısının değerlendirilmesi | — | [Ders 3 Aktivitesi](ders-ici-aktiviteler/03-tavuk-durum-paket-servis-veritabani.md) | Tamamlandı |

Bu tablo her ders sonrasında güncellenecektir.

## Ders 3 — Kısa Özet

Ders 3'te gerçek hayattaki bir **tavuk dürüm paket servis sistemi** veritabanı problemine dönüştürüldü. Google Gemini'den gerekli tablolar için başlangıç önerileri istendi. Ekrandaki yanıtta özellikle **Müşteriler**, **Personeller** ve **Ürünler** tabloları görüldü.

Aktivite kaydında bu başlangıç önerileri; Primary Key, Foreign Key, Access veri türleri ve tablo ilişkileri açısından düzenlenerek daha kapsamlı bir ilişkisel veritabanı taslağına dönüştürüldü.

➡️ [Ders 3 — Tavuk Dürüm Paket Servis Veritabanı Tasarımı](ders-ici-aktiviteler/03-tavuk-durum-paket-servis-veritabani.md)

## Çalışma İlkeleri

- Derste anlatılmayan içerikler ders notuymuş gibi eklenmeyecektir.
- Fotoğrafta veya ders kaydında açıkça görülmeyen AI çıktıları birebir ders çıktısı olarak gösterilmeyecektir.
- Yapay zekâdan alınan öneriler kontrol edilmeden doğru kabul edilmeyecektir.
- Örnekler mümkün olduğunca gerçek hayat senaryoları üzerinden açıklanacaktır.
- Veritabanı tasarımında gereksiz veri tekrarından kaçınılacaktır.
- Hassas bilgilerin veritabanında nasıl tutulması gerektiği güvenlik açısından ayrıca değerlendirilecektir.
- Ders içi uygulamalar teorik notlardan ayrı tutulacaktır.
- Yeni içerikler eklendikçe bu README ana indeks olarak güncellenecektir.

## Hızlı Erişim

- 📘 [Ders Notları](ders-notlari/README.md)
- 🧪 [Ders İçi Aktiviteler](ders-ici-aktiviteler/README.md)
- 🍗 [Ders 3 — Tavuk Dürüm Paket Servis Aktivitesi](ders-ici-aktiviteler/03-tavuk-durum-paket-servis-veritabani.md)
- 🔗 [Kaynaklar](kaynaklar/README.md)

---

**Hasan Mert Koku**  
**Öğrenci No:** 202551501055  
**Ders:** Veri Tabanı 2
