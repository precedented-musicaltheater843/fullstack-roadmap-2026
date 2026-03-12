# Full-Stack Web Developer Roadmap — 2026

> **Backend-first, proje odaklı, gerçekçi bir yol haritası.**  
> Amaç: "Her şeyi duydum" seviyesi değil, gerçekten iş üretebilir hale gelmek.

---

## Bu Roadmap Nedir?

Bu roadmap seni tek başına "ünvan olarak senior" yapmaz.

Ama bunu disiplinle uygular, bol proje yapar, bakım / refactor / debug / production görürsen seni **güçlü bir full-stack geliştirici çizgisine** sokar.

Her modülde şu 5 şey vardır:

1. **Amaç** — Bu bölümden ne beklendiği
2. **Öğrenilecek konular** — Checkbox listesi
3. **Ödevler** — Aktif pratik
4. **Mini proje** — Ellerini kirleteceğin çıktı
5. **Çıkış kriteri** — Geçmeden önce karşılaman gereken bar

---

## Neden Bu Sıra?

Backend-first ilerliyorsun:

```
JavaScript → TypeScript → Async/Node → NestJS → DB → Redis/Queue
→ Docker → Auth/Güvenlik/Testing → React/Next → Entegrasyon → Deploy
```

Bu sıra şunun için iyi: Önce veri, API, auth, hata yönetimi, veritabanı ve sistem mantığını kuruyorsun. Sonra frontend tarafında neyi neden yaptığını daha iyi anlıyorsun.

> **Not — "Vanilla Browser JS" nerede?**  
> Bu roadmap core JavaScript'i (dil mantığı, async, OOP, modüller) Faz 1'de öğretir.  
> Browser platform tarafı ise iki yere dağılmıştır:  
> - **Faz 0** — Web temelleri: DOM mantığı, cookie/localStorage/sessionStorage, CORS, HTTP vs HTTPS  
> - **Faz 5** — Modern frontend: React ile event handling, form yönetimi, veri akışı  
>  
> "Vanilla DOM manipulation" (querySelector, addEventListener, fetch API) bilinçli olarak kapsam dışı bırakılmıştır — bu roadmap React/Next.js ile frontend yazmayı hedefler. DOM'u elle manipüle etmek yerine React'ın soyutlamasını kullanırsın. Eğer vanilla browser JS de öğrenmek istersen MDN'in [JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)'ı opsiyonel kaynak olarak önerilir.

---

## Ana Akış

| Faz | İçerik | Dosya |
|-----|--------|-------|
| Faz 0 | Çalışma temeli | [PHASE-0.md](./PHASE-0.md) |
| Faz 1 | JavaScript | [PHASE-1.md](./PHASE-1.md) |
| Faz 2 | TypeScript | [PHASE-2.md](./PHASE-2.md) |
| Faz 3 | Backend çekirdeği | [PHASE-3.md](./PHASE-3.md) |
| Faz 4 | Üretim kalitesi | [PHASE-4.md](./PHASE-4.md) |
| Faz 5 | Frontend | [PHASE-5.md](./PHASE-5.md) |
| Faz 6 | Entegrasyon | [PHASE-6.md](./PHASE-6.md) |
| Faz 7 | Deploy & Operasyon | [PHASE-7.md](./PHASE-7.md) |

Kaynaklar için: [RESOURCES.md](./RESOURCES.md)

---

## Tahmini Süreler

> Haftada **15–20 saat** gerçek çalışma ile:

| Faz | Süre |
|-----|------|
| Faz 0 — Çalışma temeli | 2–3 hafta |
| Faz 1 — JavaScript | 5–6 ay |
| Faz 2 — TypeScript | 1–1.5 ay |
| Faz 3 — Backend çekirdeği | 6–7 ay |
| Faz 4 — Üretim kalitesi | 2–2.5 ay |
| Faz 5 — Frontend | 3.5–4.5 ay |
| Faz 6 — Entegrasyon | 1.5–2 ay |
| Faz 7 — Deploy & Operasyon | 1.5–2 ay |
| **TOPLAM** | **~23–28 ay** |

> Bu "gerçekten sindirdim" temposudur. Daha hızlı gidebilirsin; ama çıkış kriterlerini karşılamıyorsan hızın önemi yok.

---

## Kullanım Kuralları

- Konu bitmeden sırf takvim yüzünden sonraki modüle geçme.
- Önce mantığı kur, sonra syntax hızlanır.
- Her bölümde küçük örnek + mini proje yap.
- Her proje Git ile yönetilir.
- Her modül sonunda kısa not çıkar:
  - Bu konu ne işe yarıyor?
  - En sık hangi hatayı yaptım?
  - Bunu gerçek projede nerede kullanırım?
- Kopyala-yapıştırla ilerleme; gerektiğinde referans bak ama kendin yaz.
- Öğrenme sırasında küçük tekrarlar normaldir; geri dönmek zayıflık değildir.

---

## Yasaklar

- [ ] Sadece video izleyip geçmek
- [ ] Framework'e çok erken kaçmak
- [ ] SQL bilmeden ORM'e güvenmek
- [ ] "Çalıştıysa tamamdır" diyip test yazmamak
- [ ] Auth ve güvenlik kısmını hafife almak
- [ ] Sadece mutlu senaryoyu kodlayıp error state yazmamak
- [ ] Debug etmeden çözümü doğrudan kopyalamak
- [ ] Her şeyi aynı anda öğrenmeye çalışmak

---

## Bilinçli Olarak Opsiyonel Bırakılanlar

Bu başlıklar değerlidir ama çekirdek yol için zorunlu değildir:

- Kubernetes
- GraphQL
- gRPC
- Kafka / event streaming derin seviye
- Microservices derin seviye
- Terraform / IaC
- Native mobile / React Native
- WebAssembly
- Deno / Bun derin seviye
- Storybook derin seviye
- Multi-region / edge mimari derin seviye

---

## Katkıda Bulunma

Bu roadmap toplulukla birlikte büyümeyi hedefliyor.

Eksik bir konu, hatalı bir sıralama veya eklenebilecek bir kaynak görürsen:

1. Repo'yu fork'la
2. Yeni bir branch aç (`git checkout -b feat/yeni-konu`)
3. Değişikliğini yap ve commit et
4. Pull Request aç — ne eklediğini ve neden gerekli olduğunu kısaca açıkla

Her katkı değerlidir. Büyük ekleme zorunlu değil; küçük bir kaynak, daha net bir açıklama veya eksik bir checkbox bile fark yaratır.

---

*Doğru sıra kısaca:*

```
JavaScript → TypeScript → Async → Node/HTTP → NestJS → PostgreSQL + ORM
→ Redis/Queue → Docker → Auth/Güvenlik/Testing → React → Next.js
→ Full-stack Entegrasyon → Deploy/Operasyon
```
