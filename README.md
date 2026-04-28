# 🛒✨ E-Commerce Testing Project (C# & NUnit)

> 🚀 Test odaklı geliştirilmiş, hataların özellikle yerleştirildiği bir e-ticaret simülasyonu

---

## 🎯 Proje Amacı

Bu projede sıfırdan bir **e-ticaret sistemi** geliştirdim.  
Ama klasik bir sistem değil 👇

💥 Sistem içerisine **bilerek hatalar (bug)** yerleştirdim  
🧪 Amaç: Bu hataları farklı test türleri ile yakalamak  
📊 Böylece test süreçlerini gerçek senaryoya yakın şekilde deneyimledim  

---

## 🧠 Senaryo

Sistemde bir kullanıcı aşağıdaki işlemleri yapabilir:

- 🛍️ Ürün seçer  
- ➕ Sepete ekler  
- 📦 Sipariş verir  
- 💳 Ödeme yapar  

Ancak sistem kusursuz değil ❗  
👉 Testler sayesinde hatalar ortaya çıkarılır

---

## 🧱 Proje Yapısı

```bash
ECommerceApp/
 ├── Core/
 │    ├── Product.cs        🧾 Ürün modeli
 │    ├── Cart.cs           🛒 Sepet işlemleri
 │    ├── OrderService.cs   📦 Sipariş & ödeme
 │
 ├── Tests/
 │    ├── UnitTests/        🔬 Unit (White Box)
 │    ├── IntegrationTests/ 🔗 Integration
 │
 └── Program.cs             🚀 Entry point
```

---

## ⚙️ Kullanılan Teknolojiler

- 💻 C#
- ⚙️ .NET
- 🧪 NUnit

---

## 🧪 Test Yaklaşımları

### 🔬 Unit Test (White Box)

Kodun iç yapısını bilerek yazdığım testlerdir.

✔️ Amaç:
- İç mantığı doğrulamak  
- Hatalı logic’i yakalamak  

---

### ⚫ Black Box Test

Sistemin içini bilmeden sadece davranış test edilir.

✔️ Amaç:
- Kullanıcı açısından doğruluk  
- Input → Output kontrolü  

---

### ⚙️ Gray Box Test

Kısmi bilgi ile yapılan testlerdir.

✔️ Amaç:
- Kritik senaryolarda edge-case yakalamak  

---

### 🔗 Integration Test

Modüllerin birlikte çalışmasını test eder.

✔️ Amaç:
- Sistem akışının doğruluğunu kontrol etmek  

---

## 🧾 Test Senaryoları

| # | Senaryo | Sonuç |
|--|--------|------|
| 1 | Ürün sepete ekleniyor mu | ✅ |
| 2 | Sepet toplam fiyat doğru mu | ✅ |
| 3 | Negatif fiyatlı ürün eklenebilir mi | ❌ |
| 4 | Boş sepet ile sipariş verilebilir mi | ❌ |
| 5 | Ödeme sonrası sipariş oluşuyor mu | ❌ |
| 6 | Aynı ürün tekrar eklenince adet artıyor mu | ✅ |
| 7 | Sepetten ürün silinebiliyor mu | ✅ |
| 8 | Sipariş sonrası sepet temizleniyor mu | ❌ |
| 9 | Ödeme başarısızsa sipariş oluşuyor mu | ❌ |
|10 | Null ürün eklenirse sistem ne yapıyor | ❌ |

---

## 📊 Test Sonuç Raporu

### ❌ Başarısız Testler

| Test | Sebep |
|------|------|
| NegativePriceTest | Validasyon eksik |
| EmptyCartTest | Sepet kontrolü yok |
| PaymentFailureTest | Ödeme sonucu kontrol edilmiyor |
| NullProductTest | Null check yok |
| ClearCartAfterOrderTest | Sepet temizlenmiyor |

---

### ✅ Başarılı Testler

- ✔️ Ürün ekleme çalışıyor  
- ✔️ Ürün adedi artıyor  
- ✔️ Sepetten silme çalışıyor  
- ✔️ Temel hesaplama doğru  

---

## 🚀 Nasıl Çalıştırılır

```bash
git clone <repo-link>
cd ECommerceApp
dotnet test
```

---


## 📌 Sonuç

Bu proje:

✔️ Test türlerini uygulamalı olarak gösterir  
✔️ Gerçek hataları yakalamayı öğretir  
✔️ Test yazmanın önemini ortaya koyar  

❗ Ama bilinçli olarak hatalı bırakılmıştır  
