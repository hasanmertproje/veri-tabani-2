# Ders 3 — Tavuk Dürüm Paket Servis Veritabanı Tasarımı

**Tarih:** 09.10.2026  
**Ders:** Veri Tabanı 2  
**Öğrenci:** Hasan Mert Koku  
**Öğrenci No:** 202551501055

## Aktivite Konusu

Ders sırasında, bir **tavuk dürüm paket servis programı** için gerekli veritabanı tablolarını belirlemek amacıyla Google Gemini'den yardım istendi.

Kullanılan temel istek özetle şu fikre dayanıyordu:

> Tavuk dürüm paket servis programı için veritabanı oluşturmak istiyorum. Gerekli tabloları ver.

Bu aktivitenin amacı, gerçek hayattaki bir paket servis sistemini veritabanı tablolarına dönüştürmeyi ve yapay zekâ tarafından verilen tablo önerilerini veritabanı tasarım mantığı açısından değerlendirmeyi öğrenmektir.

## Fotoğrafta Görülen Gemini Önerileri

Ders sırasında ekrana yansıtılan yanıtta ilk olarak aşağıdaki tablolar görülmüştür.

### 1. Müşteriler (`Customers`)

Sipariş veren kişilerin iletişim ve adres bilgilerini tutmak için önerilmiştir.

Fotoğrafta görülen alan örnekleri:

| Alan | Örnek Veri Türü | Açıklama |
| --- | --- | --- |
| `MusteriID` | int | Primary Key |
| `AdSoyad` | varchar | Müşteri adı ve soyadı |
| `Telefon` | varchar | Telefon numarası; benzersiz olması önerilmiş |
| `Adres` | text | Teslimat adresi |
| `KayitTarihi` | datetime | Müşteri kayıt tarihi |

### 2. Personeller (`Staff`)

Kasiyer, mutfak personeli ve paket serviste görev yapan kuryelerin bilgilerini tutmak için önerilmiştir.

Fotoğrafta görülen alan örnekleri:

| Alan | Örnek Veri Türü | Açıklama |
| --- | --- | --- |
| `PersonelID` | int | Primary Key |
| `AdSoyad` | varchar | Personelin adı ve soyadı |
| `Telefon` | varchar | Telefon numarası |
| `Gorev` | varchar | Örn. Kurye, Kasiyer, Usta |

### 3. Ürünler (`Products`)

Tavuk dürüm, içecek, tatlı ve yan ürünlerin sisteme kaydedilmesi için önerilmiştir.

Fotoğrafta bu tablonun başlığı ve `UrunID` alanının Primary Key olarak başladığı görülmektedir. Diğer alanlar fotoğrafta tam olarak okunamadığı için aşağıdaki bölümde ders çalışmasına uygun biçimde mantıksal olarak tamamlanmıştır.

---

## Aktivite İçin Düzenlenmiş Veritabanı Taslağı

Gemini'nin verdiği başlangıç fikri, paket servis sisteminin ihtiyaçları düşünülerek aşağıdaki şekilde düzenlenebilir.

### Müşteriler

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `MusteriID` | Otomatik Sayı | Primary Key |
| `AdSoyad` | Kısa Metin |  |
| `Telefon` | Kısa Metin | Numara olmasına rağmen matematiksel işlem yapılmayacağı için metin tutulabilir |
| `Adres` | Uzun Metin | Teslimat adresi |
| `KayitTarihi` | Tarih/Saat |  |

### Personeller

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `PersonelID` | Otomatik Sayı | Primary Key |
| `AdSoyad` | Kısa Metin |  |
| `Telefon` | Kısa Metin |  |
| `Gorev` | Kısa Metin | Kurye, Kasiyer, Usta vb. |

### Kategoriler

Ürünleri gruplamak için ayrı kategori tablosu kullanılabilir.

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `KategoriID` | Otomatik Sayı | Primary Key |
| `KategoriAdi` | Kısa Metin | Dürümler, İçecekler, Tatlılar vb. |

### Ürünler

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `UrunID` | Otomatik Sayı | Primary Key |
| `KategoriID` | Sayı | Foreign Key → `Kategoriler.KategoriID` |
| `UrunAdi` | Kısa Metin | Örn. Tavuk Dürüm |
| `Fiyat` | Para Birimi | Ürün satış fiyatı |
| `StoktaMi` | Evet/Hayır | Ürünün satışa açık olup olmadığı |

### Siparişler

Bir siparişin genel bilgilerini tutar.

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `SiparisID` | Otomatik Sayı | Primary Key |
| `MusteriID` | Sayı | Foreign Key → `Musteriler.MusteriID` |
| `KuryeID` | Sayı | Foreign Key → `Personeller.PersonelID`; boş bırakılabilir |
| `SiparisTarihi` | Tarih/Saat |  |
| `TeslimatAdresi` | Uzun Metin | Sipariş anındaki adres |
| `Durum` | Kısa Metin | Hazırlanıyor, Yolda, Teslim Edildi vb. |
| `ToplamTutar` | Para Birimi | Sipariş toplamı |

### Sipariş Detayları

Bir sipariş içerisinde birden fazla ürün bulunabileceği için ara tablo gerekir.

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `SiparisDetayID` | Otomatik Sayı | Primary Key |
| `SiparisID` | Sayı | Foreign Key → `Siparisler.SiparisID` |
| `UrunID` | Sayı | Foreign Key → `Urunler.UrunID` |
| `Adet` | Sayı | Sipariş edilen miktar |
| `BirimFiyat` | Para Birimi | Sipariş anındaki ürün fiyatı |

### Ödemeler

Ödeme bilgisini siparişten ayrı tutmak için kullanılabilir.

| Alan | Access'te Uygun Tür | Anahtar / Not |
| --- | --- | --- |
| `OdemeID` | Otomatik Sayı | Primary Key |
| `SiparisID` | Sayı | Foreign Key → `Siparisler.SiparisID` |
| `OdemeTuru` | Kısa Metin | Nakit, Kart vb. |
| `OdemeTutari` | Para Birimi |  |
| `OdemeTarihi` | Tarih/Saat |  |

> Güvenlik açısından banka/kredi kartı numarası, CVV gibi hassas kart bilgileri bu veritabanında tutulmamalıdır.

## Tablolar Arası İlişkiler

Önerilen temel ilişkiler:

```text
Musteriler (1) -------- (N) Siparisler
Personeller (1) ------- (N) Siparisler
Kategoriler (1) ------- (N) Urunler
Siparisler (1) -------- (N) SiparisDetaylari
Urunler (1) ----------- (N) SiparisDetaylari
Siparisler (1) -------- (N) Odemeler
```

Buradaki en önemli noktalardan biri **Siparişler ile Ürünler arasında doğrudan çoktan çoğa ilişki kurmak yerine `SiparisDetaylari` ara tablosunun kullanılmasıdır.**

## Örnek Senaryo

Bir müşteri aşağıdaki siparişi versin:

- 2 adet Tavuk Dürüm
- 1 adet Ayran

Bu durumda:

1. Müşteri bilgisi `Musteriler` tablosunda bulunur.
2. Yeni sipariş `Siparisler` tablosuna kaydedilir.
3. Tavuk dürüm için `SiparisDetaylari` tablosuna bir satır eklenir ve `Adet = 2` olur.
4. Ayran için `SiparisDetaylari` tablosuna ikinci bir satır eklenir ve `Adet = 1` olur.
5. Paket servise çıkan kurye `Siparisler.KuryeID` üzerinden siparişe bağlanabilir.
6. Ödeme bilgisi `Odemeler` tablosunda tutulabilir.

## Derste Öğrenilen / Pekiştirilen Noktalar

- Gerçek bir işletme senaryosu önce varlıklara ayrılabilir.
- Her varlık için ayrı tablo düşünülür.
- Her tabloda benzersiz bir Primary Key bulunmalıdır.
- Tablolar Foreign Key alanlarıyla birbirine bağlanabilir.
- Tek bir siparişte birden fazla ürün olabileceğinden sipariş detay tablosu gerekir.
- Telefon numarası gibi sayısal görünen ancak hesaplama yapılmayan bilgiler metin türünde saklanabilir.
- Yapay zekânın verdiği tablo önerileri doğrudan kabul edilmek yerine veritabanı mantığı açısından kontrol edilmelidir.
- Access kullanılırken SQL veri türleri yerine Access'in karşılıkları seçilmelidir.

## Aktivite Sonucu

Gemini, paket servis sistemi için gerekli temel varlıkların belirlenmesinde başlangıç noktası olarak kullanılmıştır. Daha sonra bu öneriler Primary Key, Foreign Key, tablo ilişkileri ve Access veri türleri açısından düzenlenerek ilişkisel bir veritabanı taslağına dönüştürülmüştür.

---

**Not:** Fotoğrafta açıkça okunmayan alanlar Gemini'nin birebir çıktısı olarak gösterilmemiş; ders aktivitesinin devamı niteliğinde mantıksal veritabanı tasarımı olarak ayrı bölümde hazırlanmıştır.
