<h1 align="center">Full-Stack Web Developer Roadmap</h1>

<p align="center">
  <strong>Backend first, proje odaklı, gerçekçi bir öğrenme yol haritası.</strong>
  <br />
  <em>"Her şeyi duydum" seviyesi değil, gerçekten iş üretebilir hale gelmek.</em>
</p>

<p align="center">
  <a href="#-neden-bu-roadmap">Neden?</a> •
  <a href="#-fazlar">Fazlar</a> •
  <a href="#-sureler">Süreler</a> •
  <a href="#-nasil-kullanilir">Kullanım</a> •
  <a href="#-katkida-bulun">Katkı</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Faz-8%20Bolum-blue?style=for-the-badge" alt="8 Faz">
  <img src="https://img.shields.io/badge/Sure-23--28%20Ay-green?style=for-the-badge" alt="23-28 Ay">
  <img src="https://img.shields.io/badge/Seviye-Junior%20→%20Mid-orange?style=for-the-badge" alt="Seviye">
  <img src="https://img.shields.io/badge/Dil-Turkce-red?style=for-the-badge" alt="Turkce">
</p>

---

## Bu Roadmap Nedir?

Bu roadmap seni tek başına "ünvan olarak senior" yapmaz.

Ama bunu disiplinle uygular, bol proje yapar, bakım / refactor / debug / production görürsen seni **güçlü bir full stack geliştirici çizgisine** sokar.

### Her modülde şu 5 şey vardır:

| # | Içerik | Açıklama |
|:-:|--------|----------|
| 1 | **Amaç** | Bu bölümden ne beklendiği |
| 2 | **Konular** | Checkbox listesi |
| 3 | **Ödevler** | Aktif pratik |
| 4 | **Mini Proje** | Ellerini kirletecek çıktı |
| 5 | **Çıkış Kriteri** | Geçmeden önce karşılaman gereken bar |

---

## Neden Bu Roadmap?

<table>
<tr>
<td width="50%">

### Başka Roadmaplerden Farkı

- Backend first yaklaşım
- Sadece teori değil, proje odaklı
- Gerçekçi süreler
- Çıkış kriterleri ile ilerleme kontrolü
- Modern 2026 teknolojileri

</td>
<td width="50%">

### Hedef Kitle

- Sıfırdan başlayan geliştiriciler
- Kariyer değisikligi yapanlar
- Kendini güncellemek isteyen juniorlar
- Sistematik öğrenme isteyenler

</td>
</tr>
</table>

---

## Öğrenme Sırası

```
JavaScript → TypeScript → Async/Node → NestJS → DB → Redis/Queue
→ Docker → Auth/Guvenlik/Testing → React/Next → Entegrasyon → Deploy
```

> **Neden bu sıra?**
> Önce veri, API, auth, hata yönetimi, veritabanı ve sistem mantığını kuruyorsun.
> Sonra frontend tarafında neyi neden yaptığını daha iyi anlıyorsun.

---

## Fazlar

| Faz | İçerik | Tahmini Süre | Döküman |
|:---:|--------|:------------:|:-------:|
| 0 | Çalışma Temeli | 2-3 hafta | [Başlat →](./PHASE-0.md) |
| 1 | JavaScript Temelleri | 5-6 ay | [Başlat →](./PHASE-1.md) |
| 2 | TypeScript | 1-1.5 ay | [Başlat →](./PHASE-2.md) |
| 3 | Backend Çekirdeği | 6-7 ay | [Başlat →](./PHASE-3.md) |
| 4 | Üretim Kalitesi | 2-2.5 ay | [Başlat →](./PHASE-4.md) |
| 5 | Frontend Geliştirme | 3.5-4.5 ay | [Başlat →](./PHASE-5.md) |
| 6 | Full Stack Entegrasyon | 1.5-2 ay | [Başlat →](./PHASE-6.md) |
| 7 | Deploy ve Operasyon | 1.5-2 ay | [Başlat →](./PHASE-7.md) |

<p align="center">
  <strong>Toplam Tahmini Süre: 23-28 ay</strong>
  <br />
  <em>(Haftada 15-20 saat gerçek çalışma ile)</em>
</p>

---

## Teknolojiler

<p align="center">
  <img src="https://skillicons.dev/icons?i=js,ts,nodejs,nestjs,postgres,redis,docker,react,nextjs,tailwind,git&theme=dark" alt="Teknolojiler" />
</p>

<details>
<summary><strong>Tum Teknoloji Listesi</strong></summary>

### Diller ve Runtimelar
- JavaScript (ES6+)
- TypeScript
- Node.js

### Backend
- NestJS
- Express.js
- REST API Design
- PostgreSQL
- Redis
- Message Queues (BullMQ)
- Prisma / Drizzle ORM

### Frontend
- React 19
- Next.js 15+
- TanStack Query
- Zustand / Jotai
- Tailwind CSS
- Zod

### DevOps ve Tools
- Docker
- GitHub Actions
- Nginx
- Linux Basics

### Testing
- Jest / Vitest
- Testing Library
- MSW
- Playwright / Cypress

</details>

---

## Nasıl Kullanılır

### Kurallar

| # | Kural |
|:-:|-------|
| 1 | Konu bitmeden sirf takvim yüzünden sonraki modüle geçme |
| 2 | Önce mantığı kur, sonra syntax hızlanır |
| 3 | Her bölümde küçük örnek + mini proje yap |
| 4 | Her proje Git ile yönetilir |
| 5 | Kopyala yapıştırla ilerleme kendin yaz |
| 6 | Geri dönmek zayıflık değildir |

### Her Modül Sonunda

```
- Bu konu ne işe yarıyor?
- En sık hangi hatayı yaptım?
- Bunu gerçek projede nerede kullanırım?
```

---

## Yasaklar

> Bunları yapma.

- [ ] Sadece video izleyip geçmek
- [ ] Framework'e çok erken kaçmak
- [ ] SQL bilmeden ORM'e güvenmek
- [ ] "Çalıştıysa tamamdır" diyip test yazmamak
- [ ] Auth ve güvenlik kısmını hafife almak
- [ ] Sadece mutlu senaryoyu kodlayıp error state yazmamak
- [ ] Debug etmeden çözümü doğrudan kopyalamak
- [ ] Her şeyi aynı anda öğrenmeye çalışmak

---

## Opsiyonel Konular

<details>
<summary>Bu başlıklar değerlidir ama çekirdek yol için zorunlu değildir</summary>

- Kubernetes
- GraphQL
- gRPC
- Kafka / Event Streaming
- Microservices (derin seviye)
- Terraform / IaC
- Native Mobile / React Native
- WebAssembly
- Deno / Bun (derin seviye)
- Storybook (derin seviye)
- Multi-region / Edge Mimari

</details>

---

## Kaynaklar

Tüm kaynaklar için: **[RESOURCES.md](./RESOURCES.md)**

### Öneriler

| Kaynak | Tur | Link |
|--------|-----|------|
| javascript.info | Dökümantasyon | [Ziyaret Et](https://javascript.info) |
| Node.js Docs | Resmi Dökümanlar | [Ziyaret Et](https://nodejs.org/docs) |
| NestJS Docs | Framework | [Ziyaret Et](https://docs.nestjs.com) |
| React Docs | Resmi Dökümanlar | [Ziyaret Et](https://react.dev) |
| Next.js Docs | Framework | [Ziyaret Et](https://nextjs.org/docs) |

---

## Katkida Bulun

Bu roadmap toplulukla birlikte büyumeyi hedefliyor.

Eksik bir konu, hatalı bir sıralama veya eklenebilecek bir kaynak görürsen:

```bash
# 1. Repo'yu fork'la
# 2. Yeni bir branch aç
git checkout -b feat/yeni-konu

# 3. Değişikliğini yap ve commit et
git commit -m "feat: yeni konu eklendi"

# 4. Pull Request aç
```

> Her katkı değerlidir. Büyük ekleme zorunlu değil; küçük bir kaynak, daha net bir açıklama veya eksik bir checkbox bile fark yaratır.

---

## Yıldız Geçmişi

<p align="center">
  <em>Eğer bu roadmap faydalı olduysa, bir yıldız bırakmanı çok isterim!</em>
</p>

<p align="center">
  <a href="https://github.com/14metehan53/fullstack-roadmap-2026/stargazers">
    <img src="https://img.shields.io/github/stars/14metehan53/fullstack-roadmap-2026?style=social" alt="GitHub Stars">
  </a>
</p>

---

## Lisans

Bu proje [MIT Lisansi](./LICENSE) altinda lisanslanmıştır.

---

<p align="center">
  <sub>Built with mass of mass of coffee by <a href="https://github.com/14metehan53">@14metehan53</a> and AI.</sub>
</p>
