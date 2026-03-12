# Faz 4 — Üretim Kalitesi

---

## Bölüm 20 — Auth, Güvenlik, Testing, System Design ve Observability
**Tahmini Süre: 7–9 hafta**

### Amaç
"Çalışıyor" seviyesinden "üretime daha yakın" seviyeye geçmek.

---

### Aşama 1 — Auth'un Gerçek Dünya Parçaları

- [ ] Register — validation, duplicate check, hash, email verify gönder
- [ ] Login — credentials kontrolü, token üret, son giriş kaydı
- [ ] Logout — token invalidation
- [ ] Access token — kısa ömürlü (15dk–1saat)
- [ ] Refresh token rotation — her kullanımda yeni refresh token
- [ ] Refresh token ailesini izleme (token reuse detection)
- [ ] Email verification — token üret, gönder, doğrula, süresi dol
- [ ] Forgot password — token üret, mail gönder
- [ ] Reset password — token doğrula, hash, eski tokenları geçersiz kıl
- [ ] Change password — mevcut şifre kontrolü
- [ ] Logout all devices — tüm refresh token'ları geçersiz kıl
- [ ] Session auth vs JWT trade-off — stateful vs stateless
- [ ] Cookie auth vs Bearer token trade-off — ne zaman hangisi
- [ ] OAuth 2.0 temeli — authorization code flow
- [ ] OIDC (OpenID Connect) — OAuth üzerine kimlik katmanı
- [ ] Google / GitHub login implementasyonu (Passport.js ile)
- [ ] Auth akışında UI + API + DB + Email koordinasyonu

---

### Aşama 2 — Güvenlik

- [ ] Password hashing — bcrypt, argon2 (ve salt neden önemli)
- [ ] Brute force koruması — rate limit + account lockout
- [ ] Rate limiting — IP bazlı, user bazlı, endpoint bazlı
- [ ] CSRF — ne zaman sorun, cookie auth'ta nasıl korunulur
- [ ] XSS — stored, reflected, DOM-based; CSP headers
- [ ] SQL injection — neden ORM korur, raw query tehlikesi
- [ ] NoSQL injection farkındalığı
- [ ] SSRF — server-side request forgery farkındalığı
- [ ] Path traversal farkındalığı
- [ ] Secure cookie — HttpOnly, Secure, SameSite=Strict/Lax
- [ ] CORS — allowOrigin, allowCredentials, allowMethods
- [ ] Input validation — her dış veri doğrulanmalı
- [ ] Output sanitization — HTML escape, DOMPurify gibi
- [ ] Secrets yönetimi — `.env` commit etme, secret manager farkındalığı
- [ ] HTTPS zorunluluğu — production'da HTTP olmamalı
- [ ] Security headers — helmet ile: X-Frame-Options, X-Content-Type-Options, HSTS
- [ ] Dependency audit — `npm audit`
- [ ] OWASP Top 10 — en azından tanı

---

### Aşama 3 — Test Stratejisi

- [ ] Test pyramid — çok unit, az entegrasyon, daha az e2e
- [ ] Unit test — tek fonksiyon / class, bağımlılıkları mock'la
- [ ] Integration test — birden fazla katman birlikte (DB dahil)
- [ ] E2E test — gerçek kullanıcı akışı, gerçek HTTP
- [ ] Happy path — işin doğru gittiği senaryo
- [ ] Sad path / error path — hatalı input, yetkisiz erişim, bulunamayan kaynak
- [ ] Edge case — boş liste, sıfır değer, maksimum limit
- [ ] Test fixture — sabit test verisi
- [ ] Factory — dinamik test verisi üreteci
- [ ] Test database — her test çalışmasından önce temizle
- [ ] Transaction rollback ile test izolasyonu
- [ ] Mock ne zaman gerekir — dış servis, email, ödeme
- [ ] Mock ne zaman zarar verir — orijinal davranışı saklar
- [ ] supertest ile API endpoint testi
- [ ] API sözleşmesini test etme — response şeması doğrulama
- [ ] Auth senaryosu testleri — korumalı route'a tokensız git
- [ ] Permission senaryosu testleri — yetersiz yetkiyle işlem dene
- [ ] Vitest veya Jest ile test kurulumu

---

### Aşama 4 — Backend Kalitesi

- [ ] Tutarlı response envelope — `{ data, error, meta, requestId }`
- [ ] Request ID — her isteğe UUID ata, loglara ekle
- [ ] Structured logging — JSON formatında: level, message, requestId, userId, duration
- [ ] Correlation ID — servisler arası istek takibi
- [ ] Health check endpoint — `/health` — DB ve Redis bağlantısını kontrol et
- [ ] Readiness vs liveness probe farkındalığı
- [ ] Graceful shutdown — açık bağlantıları kapat, kuyrukları boşalt
- [ ] Swagger / OpenAPI temizliği — her endpoint belgelenmiş olmalı
- [ ] API versioning kararları — ne zaman breaking change?
- [ ] Pagination stratejisi — offset vs cursor büyük tablolarda
- [ ] Idempotent endpoint — aynı isteği iki kez göndermek güvenli mi?

---

### Aşama 5 — Observability

- [ ] Log level — DEBUG / INFO / WARN / ERROR / FATAL ne zaman hangisi
- [ ] Sentry — hata yakalama, stack trace, context
- [ ] Sentry kullanıcı context'i ekleme
- [ ] Monitoring mantığı — metrik toplama (Prometheus farkındalığı)
- [ ] Uptime takibi — UptimeRobot veya Better Uptime
- [ ] Temel metrikler — istek sayısı, hata oranı, response time
- [ ] Latency / p50 / p95 / p99 kavramları — ortalama neden yanıltıcı
- [ ] Hata sınıflandırma — beklenen (400) vs beklenmeyen (500)
- [ ] Alert — ne zaman bildirim gönderilmeli?
- [ ] Debug log production'da kapalı olmalı

---

### Aşama 6 — Performans

- [ ] N+1 sorgu — nasıl oluşur, nasıl tespit edilir, nasıl düzeltilir
- [ ] Index etkisi — EXPLAIN ANALYZE ile ölç
- [ ] Payload küçültme — sadece gerekli alanları gönder
- [ ] `select` ile sadece gerekli sütunları çek
- [ ] Pagination — 10.000 kayıt döndürme
- [ ] Streaming farkındalığı — büyük dosya / veri akışı
- [ ] Cache trade-off — ne cache'lenir, ne zaman geçersiz kılınır
- [ ] Gereksiz serialization / deserialization
- [ ] Memory leak farkındalığı — event listener cleanup, closure tuzakları
- [ ] CPU-bound işlerin ayrı ele alınması — worker thread farkındalığı
- [ ] Database connection pool boyutu

---

### Aşama 7 — System Design Farkındalığı

> Bu aşamada uzman olmak değil, teknik kararları düşünmeye başlamak hedefleniyor.

**Temel Kavramlar**
- [ ] Scalability — vertical (daha güçlü sunucu) vs horizontal (daha fazla sunucu)
- [ ] Load balancer — round-robin, least connections
- [ ] Stateless servis — neden ölçeklenmesi kolay
- [ ] Database replication — read replica farkındalığı
- [ ] CDN — statik içerik, edge caching
- [ ] Cache katmanlarının mimarideki yeri — client, CDN, uygulama, DB
- [ ] CAP teoremi farkındalığı — Consistency, Availability, Partition tolerance

**Pratik Tasarım Soruları**
- [ ] URL shortener tasarımı — klasik başlangıç sorusu
- [ ] Bildirim sistemi nasıl çalışır?
- [ ] Rate limiter nasıl tasarlanır?
- [ ] Feed sistemi nasıl tasarlanır? (timeline)
- [ ] Dosya upload servisi nasıl tasarlanır?
- [ ] Bottleneck nerede oluşur ve nasıl fark edilir?

**Pratik**
- [ ] NeetCode — System Design bölümüne göz at
- [ ] ByteByteGo YouTube kanalından 5 video izle
- [ ] "System Design Interview" kitabı 3. bölüme kadar oku

---

### Ödevler

- [ ] Email verify + forgot/reset akışı implement et
- [ ] Cookie auth ve Bearer auth artı/eksi listesi çıkar
- [ ] Unit + integration + e2e test yaz
- [ ] Sentry bağla ve test et
- [ ] `/health` endpoint ekle
- [ ] N+1 örneği oluştur ve düzelt
- [ ] URL shortener kağıt üzerinde tasarla

### Mini Projeler

- [ ] `production-ready-auth-api`
- [ ] `permissioned-admin-api`

### Çıkış Kriteri

- [ ] Auth işini sadece login endpoint'i sanmıyorsun
- [ ] Güvenlik başlıklarını bağlam içinde biliyorsun
- [ ] Test katmanlarını kurabiliyorsun
- [ ] Hata ve performans takibi için araç ekleyebiliyorsun
- [ ] Bir sistemi tasarlarken "ne nerede durur?" diye sormaya başlıyorsun
