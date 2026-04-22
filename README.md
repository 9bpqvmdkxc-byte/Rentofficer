# 🚗 Rent A Car SaaS

Multi-tenant rent a car yönetim sistemi.

## ⚠️ Projenin Mevcut Durumu

✅ **Tamamlanan:**
- Veritabanı şeması (20+ tablo)
- Auth (login/register/logout) - NextAuth v5
- Multi-tenant middleware (URL izolasyonu)
- Landing page (paket gösterimi)
- Süper admin dashboard (firma listesi + istatistikler)
- Firma dashboard (istatistikler + hoş geldin)
- 9 UI componenti (Button, Card, Input, Select, Dialog, Table, Badge, Label, Textarea)

⏳ **Henüz yapılmadı:**
- Araç yönetimi (CRUD)
- Müşteri (cari) yönetimi
- Rezervasyon sistemi
- Sözleşme akışı
- Bakım takibi
- Hasar raporu
- Finans modülü
- Raporlar
- Şube ve kullanıcı yönetimi detayları

## 📋 Sistem Gereksinimleri

- **Node.js** 20.x+
- **PostgreSQL** 14.x+

## 🚀 Kurulum

```bash
# 1. Bağımlılıkları yükle
npm install

# 2. Environment'ı hazırla
cp .env.example .env
# .env içindeki DATABASE_URL ve AUTH_SECRET'ı düzenle
# AUTH_SECRET üretmek için: openssl rand -base64 32

# 3. PostgreSQL'de veritabanı oluştur
# psql -U postgres -c "CREATE DATABASE rentacar_saas;"

# 4. Veritabanı şemasını yükle
npm run db:generate
npm run db:push
npm run db:seed

# 5. Başlat
npm run dev
```

## 🔑 Test Giriş Bilgileri

### Platform Süper Admini
- **URL:** http://localhost:3000/login?type=superadmin
- **Email:** admin@rentacar-saas.com
- **Şifre:** admin123

### Demo Firma Admini
- **URL:** http://localhost:3000/login
- **Email:** admin@demo-rentacar.com
- **Şifre:** demo123
- **Panel:** http://localhost:3000/demo-rentacar

### Veya yeni firma kaydı
http://localhost:3000/register

## 🛠️ Komutlar

```bash
npm run dev              # Geliştirme
npm run build            # Production build
npm run db:studio        # Görsel DB editör
npm run db:seed          # Test verisi yükle
npm run db:push          # Şemayı DB'ye gönder
```

## 🎯 Sonraki Adım (Yeni Konuşmada)

Devamını yapmak için yeni bir konuşma aç ve şöyle başla:

> "Rent A Car SaaS projesinin devamını yapıyoruz.
>
> **Stack:** Next.js 15 (App Router) + PostgreSQL + Prisma + NextAuth v5 + Tailwind + shadcn/ui
>
> **Model:** Multi-tenant SaaS, `siteniz.com/[firma-slug]` yapısı
>
> **Tamamlanan:** Auth, landing, login/register, süper admin dashboard, firma dashboard, tüm DB şeması
>
> Bugün **Araç Yönetimi modülünü** ekleyeceğiz. `src/app/[companySlug]/vehicles/` altında:
> - Liste sayfası (filtrelemeli tablo)
> - Ekle/Düzenle sayfası
> - Detay sayfası (belgeler, fotoğraflar, bakım geçmişi)
> - API route'ları (GET/POST/PUT/DELETE, multi-tenant güvenli)
>
> Projeyi zip olarak yükleyeceğim, açıp devam et."

Sırayla şu modülleri isteyebilirsin:
1. Araç yönetimi
2. Müşteri (cari) yönetimi
3. Rezervasyon + takvim görünümü
4. Sözleşme (kiralama) akışı
5. Bakım takibi
6. Hasar raporu (görsel)
7. Finans modülü
8. Raporlar & dashboard grafikleri
9. Şube + kullanıcı yönetimi
10. Bildirimler & hatırlatıcılar

## 📝 Lisans

Özel
