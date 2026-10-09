# 01 — Veritabanı Temelleri

> **Durum:** Başlangıç notu — ders ilerledikçe sınıfta işlenen ayrıntılar ve örnekler eklenecektir.

## Veritabanı Nedir?

Veritabanı; bilgilerin belirli bir düzen içinde saklanmasını, aranmasını, güncellenmesini ve birbiriyle ilişkilendirilmesini sağlayan veri yapısıdır.

Örneğin bir yemek sipariş sistemi için aşağıdaki bilgiler ayrı veri grupları hâlinde tutulabilir:

- Müşteriler
- Restoranlar
- Ürünler
- Siparişler
- Sipariş detayları
- Adresler

Bu verilerin tamamını tek bir tabloda tutmak yerine, doğru tablolara ayırıp aralarında ilişkiler kurmak daha sağlıklı bir veritabanı tasarımı oluşturur.

## Temel Kavramlar

### Tablo

Benzer türdeki verilerin satır ve sütunlar hâlinde saklandığı yapıdır.

Örnek bir `Musteriler` tablosu:

| MusteriID | Ad | Soyad | Telefon |
| --- | --- | --- | --- |
| 1 | Ayşe | Yılmaz | 05xx... |
| 2 | Mehmet | Kaya | 05xx... |

### Alan (Field)

Tablodaki sütunlara verilen isimdir.

Örnek:

- `MusteriID`
- `Ad`
- `Soyad`
- `Telefon`

### Kayıt (Record)

Tablodaki her satır bir kaydı temsil eder.

Örneğin tek bir müşteriye ait tüm bilgiler bir kayıttır.

## Birincil Anahtar — Primary Key

Bir tablodaki her kaydı **benzersiz** biçimde tanımlamak için kullanılan alandır.

Örneğin:

```text
MusteriID = 1
MusteriID = 2
MusteriID = 3
```

Birincil anahtarın temel amacı aynı isimde veya aynı özelliklere sahip kayıtlar bulunsa bile her kaydın ayrı olarak tanımlanabilmesini sağlamaktır.

### Neden Sadece İsim Kullanılmaz?

İki kişinin adı ve soyadı aynı olabilir. Bu nedenle:

```text
Ad = Hasan
```

gibi bir değer tek başına güvenilir bir benzersiz tanımlayıcı değildir.

Bunun yerine:

```text
MusteriID = 105
```

gibi benzersiz bir kimlik alanı kullanılabilir.

## Yabancı Anahtar — Foreign Key

Bir tablonun başka bir tablodaki kayda bağlanmasını sağlayan alandır.

Örneğin:

### Musteriler

| MusteriID | Ad |
| --- | --- |
| 1 | Ayşe |

### Siparisler

| SiparisID | MusteriID | Tarih |
| --- | --- | --- |
| 501 | 1 | 2026-10-09 |

Burada `Siparisler.MusteriID`, siparişin hangi müşteriye ait olduğunu gösterir.

## Tabloları Neden Ayırırız?

Aynı bilgiyi tekrar tekrar yazmak yerine ilişkili tablolara ayırmak:

- Veri tekrarını azaltır.
- Güncellemeyi kolaylaştırır.
- Hatalı ve tutarsız verileri azaltır.
- Sorgulamayı daha düzenli hâle getirir.
- Veritabanının büyüdükçe yönetilebilir kalmasına yardımcı olur.

## Gerçek Hayat Örneği — Sipariş Sistemi

Basit bir sipariş sistemi için şu tablolar düşünülebilir:

```text
Musteriler
Restoranlar
Urunler
Siparisler
SiparisDetaylari
```

İlişki mantığı kabaca şu şekilde olabilir:

```text
Musteriler
    │
    └──< Siparisler
              │
              └──< SiparisDetaylari >── Urunler
```

Buradaki amaç her bilgiyi ait olduğu yerde saklamaktır.

## Veri Türü Seçimi

Bir alan oluştururken o alanda hangi tür verinin saklanacağı belirlenmelidir.

Örnek:

| Alan | Uygun Veri Türü Mantığı |
| --- | --- |
| `MusteriID` | Sayısal / otomatik benzersiz değer |
| `Ad` | Kısa metin |
| `DogumTarihi` | Tarih / saat |
| `Fiyat` | Para birimi / ondalıklı sayı |
| `AktifMi` | Evet/Hayır |

Doğru veri türü seçmek hem veri doğruluğu hem de sorgular açısından önemlidir.

## Microsoft Access ile Bağlantısı

Bu derste Microsoft Access kullanılırken temel mantık şudur:

1. Veritabanı oluşturulur.
2. Tablolar tasarlanır.
3. Alanlar ve veri türleri belirlenir.
4. Birincil anahtarlar seçilir.
5. Gerekli tablolar arasında ilişkiler kurulur.
6. Veriler girilir.
7. İhtiyaca göre sorgular, formlar ve raporlar hazırlanır.

Access arayüzü kullanılan araçtır; asıl öğrenilmesi gereken konu verinin **neden o şekilde tasarlandığıdır**.

## Güvenlik Notu

Gerçek sistemlerde parola, ödeme veya kart verileri gibi hassas bilgiler sıradan metin alanlarına doğrudan kaydedilmemelidir. Özellikle ödeme bilgileri için güvenlik standartları ve ödeme sağlayıcılarının güvenli altyapıları kullanılmalıdır.

## Kısa Tekrar

- **Veritabanı:** Düzenli veri saklama ve yönetme yapısıdır.
- **Tablo:** Benzer türde verilerin tutulduğu yapıdır.
- **Alan:** Tablodaki sütundur.
- **Kayıt:** Tablodaki satırdır.
- **Primary Key:** Kaydı benzersiz tanımlar.
- **Foreign Key:** Tablolar arasında bağlantı kurar.
- **İlişkisel tasarım:** Aynı veriyi gereksiz yere tekrar etmek yerine doğru tablolara ayırmayı hedefler.

## Sonraki Güncelleme

Bir sonraki derste işlenen gerçek konu ve sınıf içi örnekler geldikçe bu not güncellenecek veya yeni numaralı ders notu oluşturulacaktır.
