# Faz 6 — Entegrasyon

---

## Bölüm 23 — Full-stack Entegrasyon ve Büyük Projeler
**Tahmini Süre: 6–8 hafta**

### Amaç
Şimdiye kadar öğrendiğin tüm parçaları tek üründe birleştirmek; modern full-stack araçları ve gerçek dünya senaryolarını öğrenmek.

---

### Aşama 1 — Full-stack Koordinasyon

- [ ] Next.js + NestJS auth akışı — cookie, token, redirect
- [ ] CORS tam yönetimi — credentials, origin, preflight
- [ ] File upload — multipart/form-data, S3/R2 farkındalığı
- [ ] Email gönderimi — Resend veya Nodemailer
- [ ] Queue ile async işler — ana thread'i bloke etme
- [ ] Webhook mantığı — dış servis seni çağırır, doğrula, işle
- [ ] Webhook signature doğrulama
- [ ] Audit log — kim ne yaptı, ne zaman
- [ ] Admin panel vs kullanıcı paneli ayrımı
- [ ] Permission kontrolü sadece frontend'de olmaz — backend'de de kontrol et
- [ ] Ödeme simülasyonu — Stripe farkındalığı
- [ ] Cron / schedule vs queue farkı

---

### Aşama 2 — WebSocket ve Gerçek Zamanlı İletişim

- [ ] WebSocket nedir? — HTTP'den farkı, full-duplex iletişim
- [ ] WebSocket handshake süreci
- [ ] Server-Sent Events (SSE) — tek yönlü, HTTP üzerinden
- [ ] WebSocket vs SSE — ne zaman hangisi?
  - [ ] SSE: bildirim, log stream, fiyat güncellemesi
  - [ ] WebSocket: chat, canlı işbirliği, oyun
- [ ] NestJS WebSocket Gateway — `@WebSocketGateway`, `@SubscribeMessage`
- [ ] Socket.io — WebSocket wrapper, reconnect, room, namespace
- [ ] Socket.io'nun NestJS entegrasyonu
- [ ] Client tarafında WebSocket — `useWebSocket` hook veya Socket.io client
- [ ] Bağlantı yönetimi — connected / disconnected state
- [ ] Yeniden bağlanma stratejisi
- [ ] Auth ile WebSocket — bağlantı sırasında token doğrulama
- [ ] Room / channel mantığı — sadece ilgili kullanıcıya mesaj
- [ ] Redis Pub/Sub ile yatay ölçekleme farkındalığı

**Socket.io vs Native WebSocket Karar Noktaları**
- [ ] Native WebSocket — tarayıcı built-in, hafif, düşük overhead
- [ ] Socket.io overhead — ekstra protokol katmanı, ~30KB client bundle
- [ ] Socket.io avantajları: otomatik reconnect, room/namespace, HTTP fallback (polling), event tabanlı API
- [ ] Socket.io dezavantajları: ekstra bağımlılık, native WebSocket'ten yavaş, Socket.io server zorunlu
- [ ] Ne zaman native WebSocket? — basit, performans kritik, tek yönlü veri akışı
- [ ] Ne zaman Socket.io? — room yönetimi, reconnect önemli, hızlı geliştirme öncelikli
- [ ] Socket.io v4 — HTTP long-polling fallback ne zaman devreye girer?

---

### Aşama 3 — Tip Güvenli API Katmanı

> Next.js + NestJS yazıyorsun; frontend ve backend arasındaki sözleşmeyi tip güvenli hale getirmenin yolları var.

**Shared Types**
- [ ] Shared type package — monorepo içinde `packages/types`
- [ ] Avantajı: frontend ve backend aynı tipi kullanır
- [ ] Dezavantajı: coupling artar, her değişiklik iki tarafı etkiler
- [ ] Ne zaman shared type mantıklı, ne zaman ayrı type daha iyi?

**OpenAPI → Kod Üretimi (Orval)**
- [ ] Orval nedir? — Swagger/OpenAPI şemasından TypeScript client üretir
- [ ] NestJS'in Swagger çıktısını kullanma
- [ ] Üretilen client — `useGetUsers`, `useCreateUser` gibi hook'lar
- [ ] React Query entegrasyonu ile üretilen hook'lar
- [ ] Avantajı: backend değişince frontend otomatik güncellenir
- [ ] Dezavantajı: build pipeline ekler, şemanın temiz olması gerekir
- [ ] `orval.config.ts` yapılandırması

**tRPC (Alternatif yaklaşım — farkındalık düzeyi)**
- [ ] tRPC nedir? — type-safe RPC, Next.js + Node için
- [ ] NestJS ile değil, Next.js full-stack (tek repo) için daha uygun
- [ ] Avantajı: sıfır kod üretimi, otomatik tip güvenliği
- [ ] Dezavantajı: NestJS ile doğal uyum yok, ayrı ekosistem
- [ ] Ne zaman tRPC, ne zaman Orval? — projeye göre karar ver

---

### Aşama 4 — Monorepo

- [ ] Monorepo nedir? — birden fazla uygulama tek repo'da
- [ ] Monorepo vs polyrepo trade-off
- [ ] Ne zaman monorepo mantıklı?
  - [ ] Shared types / utils / config
  - [ ] Full-stack (frontend + backend birlikte)
  - [ ] Design system paylaşımı
- [ ] Turborepo — Next.js ekosisteminden, pipeline caching
  - [ ] `turbo.json` — pipeline tanımı
  - [ ] `build`, `lint`, `test` pipeline
  - [ ] Remote caching farkındalığı
- [ ] Nx — enterprise ölçekli, daha kapsamlı (farkındalık)
- [ ] Workspace — npm / pnpm workspaces
- [ ] `packages/` yapısı — shared kütüphaneler
  - [ ] `packages/types` — shared TypeScript types
  - [ ] `packages/ui` — shared component library
  - [ ] `packages/config` — shared ESLint, TypeScript config
- [ ] Monorepo'da versioning farkındalığı
- [ ] Internal package import — `@myapp/types`

---

### Aşama 5 — AI / LLM Entegrasyonu

> 2026 yılında AI özelliği ekleyebilmek, junior geliştiricilerden bile bekleniyor.

- [ ] LLM API'si nedir? — modele metin gönder, metin al
- [ ] OpenAI API — `chat/completions` endpoint'i
- [ ] Vercel AI SDK — Next.js ile entegrasyon için standart kütüphane
- [ ] `useChat` hook — sohbet arayüzü
- [ ] `streamText` — streaming response (token token gelir)
- [ ] Streaming neden önemli? — kullanıcı beklemez, anlık görür
- [ ] System prompt — modele rol ver
- [ ] Temperature, max_tokens gibi parametreler
- [ ] Tool calling farkındalığı — modelin fonksiyon çağırması
- [ ] RAG (Retrieval-Augmented Generation) farkındalığı
- [ ] Prompt injection riski — kullanıcı girdisini güvenli ilet
- [ ] AI özelliği için maliyet yönetimi — token sayımı, rate limit
- [ ] Anthropic Claude, Google Gemini API alternatifleri

**Prompt Güvenliği (Derinleştirilmiş)**
- [ ] Prompt injection nedir? — kullanıcı girdisi sistem prompt'unu manipüle ediyor
- [ ] Doğrudan prompt injection — kullanıcı "ignore previous instructions" gibi şeyler yazar
- [ ] Dolaylı prompt injection — LLM'in okuduğu bir belge içine zararlı talimat gizlendi
- [ ] Savunma: kullanıcı girdisini sistem prompt'a doğrudan enjekte etme
- [ ] Savunma: input validation — beklenen format dışındaki uzun/şüpheli girdileri reddet
- [ ] Savunma: output validation — LLM çıktısını da doğrula (hassas bilgi sızdı mı?)
- [ ] Savunma: least privilege — LLM'e gereksiz tool/yetki verme
- [ ] OWASP LLM Top 10 farkındalığı

**Token Maliyet Yönetimi**
- [ ] Token nedir? — yaklaşık 4 karakter = 1 token
- [ ] Input token vs output token fiyatlandırması (output genellikle daha pahalı)
- [ ] Maliyet hesaplama — `tiktoken` veya model provider'ın tokenizer aracı
- [ ] Sistem prompt maliyet etkisi — her istekte tekrar gönderilir
- [ ] `max_tokens` sınırı koymak — sınırsız output maliyeti patlatır
- [ ] Caching — aynı sistem prompt için prompt caching desteği (Anthropic, OpenAI)
- [ ] Rate limiting AI endpoint'ini — kullanıcı başına günlük limit
- [ ] Streaming ile maliyet kontrolü — kullanıcı iptal ederse token israfı

---

### Kapanış Projeleri
- [ ] Next.js + Vercel AI SDK ile basit chat arayüzü kur
- [ ] NestJS backend ile OpenAI API çağrısını proxy et (key güvenliği)
- [ ] Streaming response'u frontend'de göster
- [ ] Kullanıcı bazlı rate limiting ekle

---

### Kapanış Projeleri

- [ ] **`fullstack-todo`**  
  Next.js + NestJS + PostgreSQL + auth + Docker + deploy

- [ ] **`fullstack-blog`**  
  Kayıt/giriş, rol sistemi, kategori, yorum, admin panel, email doğrulama, Orval ile tip güvenli client

- [ ] **`realtime-notifications`**  
  WebSocket veya SSE ile gerçek zamanlı bildirim — Next.js + NestJS

- [ ] **`ai-chat-app`**  
  Vercel AI SDK + streaming + sistem prompt + NestJS proxy

- [ ] **`fullstack-saas`**  
  Monorepo (Turborepo), ekip/çalışma alanı, rol/izin, faturalama simülasyonu, queue, email, audit log, testler, deploy

- [ ] **`fullstack-ecommerce`**  
  Ürün, sepet, sipariş, ödeme simülasyonu, admin panel, worker, email bildirimi, rapor ekranı

### Çıkış Kriteri

- [ ] Tek başına tam ürün akışını kurgulayabiliyorsun
- [ ] Backend ve frontend auth koordinasyonunu kurabiliyorsun
- [ ] Queue, email, upload, permissions gibi gerçek parçaları bağlayabiliyorsun
- [ ] WebSocket veya SSE ile gerçek zamanlı özellik ekleyebiliyorsun
- [ ] Orval ile OpenAPI'den tip güvenli client üretebiliyorsun
- [ ] Monorepo kurabiliyorsun
- [ ] Basit bir AI özelliği entegre edebiliyorsun
