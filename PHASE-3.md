# Faz 3 — Backend Çekirdeği

---

## Bölüm 16 — Asenkron JavaScript
**Tahmini Süre: 1 hafta**

### Amaç
Backend'deki tüm I/O işlerinin async doğasını anlamak.

### Öğrenilecekler

- [ ] Sync vs async — blocking vs non-blocking
- [ ] Callback tabanlı async (eski yöntem, neden sorunlu)
- [ ] Callback hell nedir?
- [ ] Promise nedir? — 3 state: pending, fulfilled, rejected
- [ ] `.then()` / `.catch()` / `.finally()` zincirleme
- [ ] async / await syntax
- [ ] async fonksiyon her zaman Promise döndürür
- [ ] try / catch ile async hata yönetimi
- [ ] Promise.all — hepsi başarılı olursa
- [ ] Promise.allSettled — hepsi bitince (hata olsa da)
- [ ] Promise.race — ilk biten kazanır
- [ ] Promise.any — ilk başarılı kazanır
- [ ] Event loop — call stack, task queue, microtask queue
- [ ] Microtask vs macrotask (Promise vs setTimeout sırası)
- [ ] Seri await vs paralel await farkı (ve performans etkisi)
- [ ] Gereksiz await zinciri anti-pattern
- [ ] AbortController ile async iptal farkındalığı

### Ödevler

- [ ] Callback, Promise ve async/await ile aynı işi üç şekilde yaz
- [ ] Promise.all ile paralel istek farkını gözlemle
- [ ] Event loop sırası tahmin soruları çöz
- [ ] Seri vs paralel await ile zamanlama farkını ölç

### Mini Proje

**`fake-api-runner.js`**  
Gecikmeli işlemleri seri ve paralel çalıştıran mini simülasyon — zaman farkını logla.

### Çıkış Kriteri

- [ ] Async akışlarda neyin ne zaman çalışacağını daha iyi tahmin edebiliyorsun
- [ ] Paralel çalıştırma fırsatlarını görebiliyorsun
- [ ] Event loop'u basitçe açıklayabiliyorsun

---

## Bölüm 17 — Node.js, HTTP ve Express
**Tahmini Süre: 6–7 hafta**

### Amaç
HTTP'yi ve API'nin nasıl çalıştığını anlamak; Express ile sıfırdan çalışan bir backend kurmak.

---

### Aşama 1 — Node Temelleri

- [ ] Node.js runtime — V8 engine, libuv
- [ ] `process.env`, `process.argv`, `process.exit`
- [ ] `fs` modülü — readFile, writeFile, readdir (sync ve async)
- [ ] `path` modülü — join, resolve, dirname, extname
- [ ] `events` modülü — EventEmitter, on, emit
- [ ] Streams — Readable, Writable, Transform (temel bakış, neden önemli)
- [ ] `package.json` anatomy — name, version, scripts, dependencies, devDependencies, engines
- [ ] npm vs pnpm vs yarn farkındalığı
- [ ] `package-lock.json` ve `pnpm-lock.yaml` neden commit'lenir?
- [ ] dotenv — `.env` dosyası, `process.env`
- [ ] `.env.example` şablonu tutma alışkanlığı
- [ ] CommonJS (`require`) vs ESM (`import`) — fark ve geçiş
- [ ] `__dirname`, `__filename` (CommonJS) vs `import.meta.url` (ESM)
- [ ] Dev vs prod dependency ayrımı

---

### Aşama 2 — HTTP Temeli

- [ ] Request / response döngüsü — bir HTTP isteğinin anatomisi
- [ ] HTTP methods — GET, POST, PUT, PATCH, DELETE, HEAD, OPTIONS
- [ ] URL anatomy — protocol, host, port, path, query string, fragment
- [ ] Status code mantığı ve doğru kullanım
  - [ ] 2xx: 200 OK, 201 Created, 204 No Content
  - [ ] 3xx: 301, 302, 304
  - [ ] 4xx: 400, 401, 403, 404, 409, 422, 429
  - [ ] 5xx: 500, 502, 503
- [ ] Headers — Content-Type, Authorization, Accept, Cache-Control, custom headers
- [ ] Cookies — Set-Cookie, HttpOnly, Secure, SameSite, Path, Domain, Expires
- [ ] Request body — JSON, form-data, urlencoded
- [ ] HTTPS — TLS handshake temel mantığı
- [ ] CORS — neden var, preflight request, headers
- [ ] REST prensipleri — resource-based, stateless, uniform interface
- [ ] REST anti-pattern örnekleri
- [ ] Idempotency — GET, PUT, DELETE idempotent; POST değil
- [ ] HTTP/2 farkındalığı (multiplexing, header compression)

---

### Aşama 3 — Express ile API

- [ ] `http` modülü ile ham server (bir kez dene, farkı hisset)
- [ ] Express kurulumu ve temel yapı
- [ ] `express.Router()` ile route organizasyonu
- [ ] Middleware kavramı — `(req, res, next)` zinciri
- [ ] Built-in middleware: `express.json()`, `express.urlencoded()`, `express.static()`
- [ ] `req` objesi: params, query, body, headers, cookies, ip
- [ ] `res` objesi: json, send, status, redirect, cookie, clearCookie
- [ ] Global error handling middleware (4 parametre: err, req, res, next)
- [ ] 404 handler
- [ ] Input validation — express-validator veya Zod
- [ ] Password hashing — bcrypt, salt rounds
- [ ] JWT — oluşturma, doğrulama, payload, expiry
- [ ] Auth middleware — Bearer token kontrolü
- [ ] Rate limiting — express-rate-limit
- [ ] Helmet — HTTP güvenlik başlıkları
- [ ] Structured logging — pino veya winston
- [ ] Request ID middleware
- [ ] nodemon / tsx ile hot reload
- [ ] supertest ile temel endpoint testi

---

### Aşama 4 — API Tasarımı ve Dokümantasyonu

- [ ] Resource isimlendirme — `/users`, `/users/:id/orders`
- [ ] Çoğul isimler, küçük harf, kebab-case
- [ ] Pagination — limit/offset ve cursor tabanlı
- [ ] Filtering — query params ile (`?status=active&role=admin`)
- [ ] Sorting — (`?sort=createdAt&order=desc`)
- [ ] Search — tam metin vs partial match
- [ ] Tutarlı response envelope: `{ data, error, meta }`
- [ ] 200 / 201 / 204 / 400 / 401 / 403 / 404 / 409 / 422 / 429 / 500 doğru kullanımı
- [ ] API versioning giriş
  - [ ] URL versioning (`/v1/users`)
  - [ ] Header versioning farkındalığı
  - [ ] Ne zaman v2 gerekir?
- [ ] OpenAPI / Swagger ile API dokümantasyonu
  - [ ] swagger-ui-express kurulumu
  - [ ] Temel endpoint dokümantasyonu (path, method, parameters)
  - [ ] Request ve response şemaları
  - [ ] Authentication tanımı

---

### Ödevler

- [ ] In-memory CRUD API yaz (DB olmadan)
- [ ] JWT ile korumalı route yap
- [ ] Pagination + filter + search ekle
- [ ] Global error handler yaz
- [ ] pino ile structured log ekle
- [ ] Swagger ile API'ni belgele
- [ ] supertest ile 5 endpoint testi yaz

### Mini Projeler

- [ ] `notes-rest-api` — CRUD, pagination, JWT auth
- [ ] `auth-api` — register, login, protected route
- [ ] `file-organizer-cli` — Node.js fs ile dosya yönetimi

### Çıkış Kriteri

- [ ] Express ile sıfırdan API kurabiliyorsun
- [ ] REST endpoint isimlendirmesinde daha bilinçlisin
- [ ] Middleware ve error handler akışını anlıyorsun
- [ ] Swagger ile API dokümantasyonu oluşturabiliyorsun

---

## Bölüm 18 — NestJS ve Backend Mimarisi
**Tahmini Süre: 7–8 hafta**

### Amaç
NestJS ile büyükçe backend kod tabanını düzenli kurmak ve mimari kararları anlamaya başlamak.

---

### Aşama 1 — Temel NestJS

- [ ] NestJS neden var? Express ile farkı
- [ ] CLI — `nest new`, `nest generate`
- [ ] Module / Controller / Provider üçlüsü
- [ ] Dependency Injection (DI) — neden önemli?
- [ ] Constructor injection
- [ ] Custom provider (`useClass`, `useValue`, `useFactory`)
- [ ] Request lifecycle — middleware → guard → interceptor → pipe → controller → interceptor → filter
- [ ] `@nestjs/config` ile config modülü
- [ ] Environment validation — Joi veya Zod ile env şeması

---

### Aşama 2 — Environment Yönetimi

> Production'da en çok can yakan konulardan biri. Bu kısma dikkat.

- [ ] `.env` / `.env.development` / `.env.production` / `.env.test` ayrımı
- [ ] `@nestjs/config` ile `ConfigService` kullanımı
- [ ] Zod veya Joi ile env şeması — zorunlu değişken eksikse uygulama başlamasın
- [ ] Config namespace — `database.host`, `jwt.secret` gibi gruplandırma
- [ ] Secrets management farkındalığı — env'i commit etme, `.env.example` tut
- [ ] Farklı ortamlar için farklı değer: DB URL, log level, CORS origin
- [ ] `process.env` yerine `ConfigService` inject etmenin avantajı

---

### Aşama 3 — DTO, Validation, Pipe

- [ ] class-validator — decorator tabanlı validation
- [ ] class-transformer — plain object → class instance dönüşümü
- [ ] ValidationPipe global veya controller düzeyinde
- [ ] `whitelist: true`, `forbidNonWhitelisted: true` önemi
- [ ] Custom pipe
- [ ] Mapped types — PartialType, PickType, OmitType, IntersectionType
- [ ] Serialization — `@Exclude()`, `@Expose()`, ClassSerializerInterceptor
- [ ] Response DTO vs entity ayrımı

---

### Aşama 4 — Auth ve Yetki

- [ ] Guards — `@UseGuards()`, `canActivate`
- [ ] Interceptors — response transform, logging, timing
- [ ] Exception filters — custom exception şekillendirme
- [ ] passport-jwt entegrasyonu
- [ ] Access token / refresh token — iki token neden?
- [ ] Roles ve permissions
- [ ] RBAC (Role-Based Access Control)
- [ ] Permission-based access — daha granüler kontrol
- [ ] `@Roles()` decorator ile route bazlı kısıtlama
- [ ] Logout / token invalidation stratejileri (Redis blacklist)

---

### Aşama 5 — Veri Katmanı ve Organizasyon

- [ ] Feature module yapısı — her domain kendi modülünde
- [ ] Service katmanı — iş mantığı burada
- [ ] Repository yaklaşımı — veri erişimi soyutlama
- [ ] Use-case / Application service mantığı
- [ ] DTO (dışarıdan gelen veri) / Entity (DB satırı) / Domain model ayrımı
- [ ] Thin controller yaklaşımı — controller sadece yönlendirir
- [ ] Transaction farkındalığı — birden fazla operasyon atomik olmalı
- [ ] Swagger / OpenAPI — `@ApiTags`, `@ApiOperation`, `@ApiResponse`, `@ApiBearerAuth`

---

### Aşama 6 — Mimari Trade-off'lar

- [ ] Monolith nedir? Avantajları neler?
- [ ] Modular monolith — modüller arası bağımlılığı sınırla
- [ ] Microservice ne zaman erken optimizasyondur?
- [ ] Repository pattern ne zaman değer katar, ne zaman gereksiz katman?
- [ ] Clean architecture ne zaman faydalı, ne zaman aşırı mühendislik?
- [ ] Shared module büyüyünce ne olur?
- [ ] Circular dependency tehlikesi ve nasıl çözülür

---

### Ödevler

- [ ] Nest ile users + auth + roles modülü kur
- [ ] Global validation pipe kur
- [ ] Zod ile env validation ekle
- [ ] Swagger dokümantasyonu üret
- [ ] Controller / service / repository sorumluluklarını ayır
- [ ] Refresh token akışı implement et

### Mini Projeler

- [ ] `nest-auth-rbac-api`
- [ ] `task-management-api`

### Çıkış Kriteri

- [ ] Nest proje yapısını ezber değil mantıkla okuyabiliyorsun
- [ ] DI ve modül yapısının neden değerli olduğunu açıklayabiliyorsun
- [ ] Env validation ile uygulama hatalı config ile başlamıyor
- [ ] Basit mimari kararları bilinçli verebiliyorsun

---

## Bölüm 19 — Veritabanı: SQL, PostgreSQL ve ORM
**Tahmini Süre: 6–7 hafta**

### Amaç
Önce veritabanını anlamak, sonra ORM'i araç olarak kullanmak.

---

### Aşama 1 — SQL Temeli

- [ ] Tablo, satır, sütun, schema kavramları
- [ ] Primary key / foreign key
- [ ] one-to-one / one-to-many / many-to-many ilişki türleri
- [ ] SELECT — sütun seçimi, alias
- [ ] INSERT / UPDATE / DELETE
- [ ] WHERE — koşullar, AND / OR / NOT
- [ ] ORDER BY — ASC / DESC
- [ ] LIMIT / OFFSET — pagination
- [ ] LIKE / ILIKE — pattern matching
- [ ] INNER JOIN / LEFT JOIN / RIGHT JOIN / FULL OUTER JOIN
- [ ] CROSS JOIN farkındalığı
- [ ] Aggregate functions — COUNT, SUM, AVG, MIN, MAX
- [ ] GROUP BY / HAVING
- [ ] Subquery — SELECT içinde SELECT
- [ ] CTE (Common Table Expression) — `WITH` farkındalığı
- [ ] DISTINCT
- [ ] COALESCE — null güvenli fallback
- [ ] CASE WHEN farkındalığı

---

### Aşama 2 — PostgreSQL Özellikleri

- [ ] PostgreSQL kurulumu (local veya Docker ile)
- [ ] `psql` ile terminal kullanımı
- [ ] Schema mantığı — public schema, custom schema
- [ ] Index nedir? — B-tree default, hash, GIN, GiST farkındalığı
- [ ] Unique constraint
- [ ] Check constraint
- [ ] Not null constraint
- [ ] Default değerler
- [ ] `SERIAL` / `BIGSERIAL` / `UUID` primary key seçimi
- [ ] Timestamp — `timestamptz` vs `timestamp` farkı
- [ ] Transaction — BEGIN / COMMIT / ROLLBACK
- [ ] Isolation level farkındalığı — Read Committed, Repeatable Read, Serializable
- [ ] Migration mantığı — up / down, geri alınabilir değişiklik
- [ ] EXPLAIN / ANALYZE ile sorgu planı okuma
- [ ] Deadlock farkındalığı
- [ ] Connection pooling (PgBouncer farkındalığı)
- [ ] JSON / JSONB column farkındalığı

---

### Aşama 3 — Data Modeling

- [ ] Domain modelleme — kullanıcı, oturum, rol, ürün, sipariş
- [ ] Soft delete — `deletedAt` timestamp ile
- [ ] Nullable alanların dikkatli tasarımı
- [ ] Audit alanları — `createdAt`, `updatedAt`, `createdBy`
- [ ] Relation tasarımı — junction table (many-to-many)
- [ ] Normalizasyon farkındalığı (1NF, 2NF, 3NF temel)
- [ ] Denormalization ne zaman yapılır?
- [ ] Pagination için doğru sıralama alanı seçme
- [ ] Cursor pagination — offset'in büyük tablolarda yavaşlaması
- [ ] Enum — DB enum vs uygulama katmanında string enum trade-off

---

### Aşama 4 — ORM Seçimi ve Kullanımı

> **Ana amaç:** Önce SQL öğren, sonra tek bir ORM'yi derin öğren.

**Prisma**
- [ ] Prisma schema — model, field, relation tanımlama
- [ ] `prisma migrate dev` / `prisma migrate deploy`
- [ ] Prisma client — findMany, findUnique, create, update, delete, upsert
- [ ] where, select, include, orderBy, skip, take
- [ ] Relation queries — nested read ve write
- [ ] Transaction — `$transaction`
- [ ] Raw query — `$queryRaw`, `$executeRaw`
- [ ] Prisma Studio farkındalığı

**Drizzle (alternatif)**
- [ ] Schema-first yaklaşım
- [ ] Query builder mantığı
- [ ] Migrations
- [ ] SQL'e yakınlığı

**Her iki ORM için ortak disiplin**
- [ ] SQL'i ORM altında kaybetmeme — ORM'in ürettiği SQL'i gör
- [ ] N+1 sorgu problemi — include vs ayrı query
- [ ] select ile sadece gerekli sütunları çek
- [ ] Seed verisi yazma
- [ ] Test için ayrı test DB veya transaction rollback

---

### Ödevler

- [ ] Saf SQL ile 30 sorgu yaz (JOIN'li, aggregate'li)
- [ ] 5 tablo ilişkili küçük şema tasarla ve kağıda çiz
- [ ] Prisma ile migration çalıştır
- [ ] Index ekleyip EXPLAIN ANALYZE farkını gözlemle
- [ ] Transaction gereken bir akış implement et
- [ ] N+1 örneği oluştur, include ile düzelt

### Mini Projeler

- [ ] `postgres-playground` — saf SQL egzersizleri
- [ ] `inventory-db-api` — NestJS + Prisma
- [ ] `order-service` — transaction, ilişkili yazma

### Çıkış Kriteri

- [ ] SQL yazmadan ORM'e güvenmiyorsun
- [ ] İlişkili veri modelleyebiliyorsun
- [ ] Migration mantığını anlıyorsun
- [ ] Prisma'da temel CRUD rahat ve N+1'i engelleyebiliyorsun

---

## Bölüm 19.5 — Redis, Cache ve Background Jobs
**Tahmini Süre: 3–4 hafta**

### Amaç
Gerçek backend projelerinde çok sık çıkan cache, rate-limit store, queue ve worker mantığını öğrenmek.

---

### Aşama 1 — Redis Temeli

- [ ] Redis nedir? — in-memory key-value store
- [ ] Neden hızlı? — disk yerine RAM
- [ ] Persistence — RDB ve AOF farkındalığı
- [ ] Key / value yapısı
- [ ] Expire / TTL — süresi dolan veri
- [ ] Veri yapıları:
  - [ ] String — set, get, incr, decr
  - [ ] Hash — hset, hget, hgetall
  - [ ] List — lpush, rpush, lpop, rpop
  - [ ] Set — sadd, smembers, sismember
  - [ ] Sorted Set (ZSet) — zadd, zrange (leaderboard gibi senaryolar)
- [ ] Cache ne zaman kullanılır?
- [ ] Ne cache'lenmez? (kullanıcıya özel, sık değişen, kritik finansal)
- [ ] Cache invalidation stratejileri — TTL, event-driven, manual

---

### Aşama 2 — Pratik Redis Kullanımı

- [ ] API response cache — pahalı sorgu sonuçlarını cache'le
- [ ] Session store (stateless JWT'ye alternatif)
- [ ] Rate limit store — request sayacı
- [ ] Email verification token saklama
- [ ] Password reset token saklama
- [ ] Idempotency key store — aynı isteği iki kez işleme
- [ ] Pub/Sub farkındalığı — gerçek zamanlı mesajlaşma için
- [ ] Redis'te atomic operasyonlar (MULTI/EXEC)

---

### Aşama 3 — Queue / Job Sistemi

- [ ] Queue nedir? — FIFO işleme kuyruğu
- [ ] Producer / consumer (worker) ayrımı
- [ ] Neden queue? — ana thread'i bloke etmeme, hata toleransı, retry
- [ ] Delayed jobs — belirli süre sonra çalıştır
- [ ] Retry — başarısız job'ı tekrar dene
- [ ] Backoff — artan bekleme süresi (exponential backoff)
- [ ] Dead-letter queue — çok kez başarısız olan job'lar
- [ ] Job idempotency — aynı job iki kez çalışsa zararsız olmalı
- [ ] Concurrency — aynı anda kaç worker?
- [ ] Queue senaryoları: email, bildirim, rapor, image işleme, webhook retry

---

### Aşama 4 — BullMQ

- [ ] Queue oluşturma
- [ ] Worker tanımlama
- [ ] Job ekleme (add, addBulk)
- [ ] Job seçenekleri — delay, priority, attempts, backoff
- [ ] Job durumları — waiting, active, completed, failed, delayed
- [ ] Event listeners — completed, failed, progress
- [ ] Retry stratejisi — `attempts` ve `backoff`
- [ ] Concurrency ayarı
- [ ] Ayrı worker process — `worker.ts` ayrı bir Node süreci
- [ ] BullMQ Board (monitoring UI) farkındalığı

---

### Ödevler

- [ ] Redis ile basit cache katmanı kur
- [ ] Login denemeleri için Redis tabanlı rate limit sayacı yap
- [ ] BullMQ ile email job kuyruğu oluştur
- [ ] Başarısız job için exponential backoff kurgula
- [ ] Dead-letter queue örneği yap

### Mini Projeler

- [ ] `email-queue-service`
- [ ] `report-generator-worker`

### Çıkış Kriteri

- [ ] Redis'i sadece "hızlı DB" gibi düşünmüyorsun
- [ ] Queue gerektiren işleri ayırt edebiliyorsun
- [ ] Worker mantığı sana yabancı değil
- [ ] BullMQ ile retry stratejisi kurabiliyorsun

---

## Bölüm 19.7 — Docker Temeli
**Tahmini Süre: 1.5–2 hafta**

### Amaç
"Bende çalışıyor" sorununu ortadan kaldırmak. Container mantığını ve günlük geliştirme akışında Docker'ı kullanabilmek.

---

### Aşama 1 — Container Kavramı

- [ ] Docker nedir, neden gereklidir?
- [ ] Container nedir? — yalıtılmış süreç
- [ ] VM (sanal makine) vs container farkı
- [ ] Image nedir? — şablon
- [ ] Container nedir? — çalışan image örneği
- [ ] Docker Hub — hazır image'ler
- [ ] Layer mantığı — her Dockerfile satırı bir katman
- [ ] Union filesystem farkındalığı

---

### Aşama 2 — Temel Komutlar

- [ ] `docker pull` — image indir
- [ ] `docker build -t isim:tag .` — image oluştur
- [ ] `docker run` — container başlat
  - [ ] `-d` detached mode
  - [ ] `-p` port mapping
  - [ ] `-e` environment variable
  - [ ] `-v` volume mount
  - [ ] `--name` container adı
  - [ ] `--rm` çıkışta sil
- [ ] `docker ps` / `docker ps -a`
- [ ] `docker stop` / `docker start` / `docker restart`
- [ ] `docker rm` / `docker rmi`
- [ ] `docker logs` / `docker logs -f`
- [ ] `docker exec -it` — çalışan container'a gir
- [ ] `docker inspect` — container detayları
- [ ] `docker images`
- [ ] `docker network ls` farkındalığı

---

### Aşama 3 — Dockerfile Yazma

- [ ] `FROM` — base image
- [ ] `WORKDIR` — çalışma dizini
- [ ] `COPY` vs `ADD` farkı
- [ ] `RUN` — build zamanı komut
- [ ] `CMD` vs `ENTRYPOINT` farkı
- [ ] `EXPOSE` — port bildirimi (zorunlu değil, dokümantasyon)
- [ ] `ENV` — environment variable
- [ ] `ARG` — build-time argument
- [ ] `.dockerignore` — `node_modules`, `.env` hariç tut
- [ ] Layer cache optimizasyonu — `package.json` kopyala, `npm install`, sonra kod kopyala
- [ ] Multi-stage build — build aşaması + production aşaması

---

### Aşama 4 — Docker Compose

- [ ] `docker-compose.yml` / `docker compose` (v2) yapısı
- [ ] services, image, build, ports, volumes, environment, depends_on
- [ ] Named volumes vs bind mounts
- [ ] Networks — servisler arası iletişim
- [ ] `docker compose up` / `down` / `up --build` / `down -v`
- [ ] `docker compose logs -f`
- [ ] PostgreSQL container ile çalışma — data volume zorunluluğu
- [ ] Redis container ile çalışma
- [ ] `healthcheck` — servisin hazır olduğunu bekle
- [ ] `env_file` — compose'da .env kullanımı
- [ ] Override dosyaları — `docker-compose.override.yml`

---

### Aşama 5 — Geliştirme Akışı

- [ ] NestJS uygulamasını Dockerize etme
- [ ] Volume ile kod değişikliklerini container'a yansıtma (hot reload)
- [ ] Tüm geliştirme ortamını tek `docker compose up` ile kaldırma
- [ ] Test ortamı için ayrı compose farkındalığı

---

### Ödevler

- [ ] PostgreSQL ve Redis'i Docker Compose ile kaldır
- [ ] Basit Node.js uygulaması için Dockerfile yaz
- [ ] Multi-stage Dockerfile ile production image oluştur
- [ ] Tüm geliştirme ortamını compose ile çalıştır
- [ ] `docker exec` ile container içine gir, process ve log incele

### Mini Proje

**`docker-dev-environment`**  
NestJS API + PostgreSQL + Redis — tek `docker compose up` ile ayağa kalkan geliştirme ortamı.

### Çıkış Kriteri

- [ ] Docker Compose ile geliştirme ortamını sıfırdan kurabiliyorsun
- [ ] Image ve container farkını açıklayabiliyorsun
- [ ] Dockerfile yazabiliyorsun
- [ ] "Bende çalışıyor ama sende çalışmıyor" sorununu container ile çözebiliyorsun
- [ ] Multi-stage build ile küçük production image oluşturabiliyorsun
