# Faz 7 — Deploy, Operasyon ve CI/CD

---

## Bölüm 24 — Deployment, Linux/Server Temelleri ve Sürekli Teslimat
**Tahmini Süre: 5–7 hafta**

### Amaç
Projeyi sadece kendi bilgisayarında değil, internette güvenli ve düzenli çalıştırmak.

---

### Aşama 1 — Deploy Temeli

- [ ] Domain nedir? — TLD, subdomain, DNS
- [ ] DNS nasıl çalışır? — A, CNAME, MX, TXT record
- [ ] DNS propagation
- [ ] HTTP vs HTTPS farkı
- [ ] SSL/TLS — sertifika, handshake temel mantığı
- [ ] Let's Encrypt ile ücretsiz SSL
- [ ] Environment variables production yönetimi
  - [ ] `.env` production'a commit edilmez
  - [ ] Platform environment variables (Vercel, Railway, Render)
  - [ ] Secret manager farkındalığı (AWS Secrets Manager, Doppler)
- [ ] Next.js deploy — Vercel, Netlify veya self-hosted
- [ ] NestJS API deploy — Railway, Render, VPS
- [ ] Cloud PostgreSQL — Neon, Supabase, Railway
- [ ] Rollback stratejisi — bir önceki versiyona dönme

---

### Aşama 2 — Linux / Server Temeli

- [ ] SSH ile bağlanma — `ssh user@ip`, SSH key ile bağlantı
- [ ] SSH key üretme ve `authorized_keys`
- [ ] Temel Linux komutları:
  - [ ] `pwd` / `ls -la` / `cd` / `mkdir -p` / `rm -rf`
  - [ ] `cat` / `less` / `tail -f` / `head`
  - [ ] `cp` / `mv`
  - [ ] `grep` — metin arama
  - [ ] `find` — dosya arama
  - [ ] `chmod` / `chown` — izin yönetimi
  - [ ] `df -h` / `du -sh` — disk kullanımı
  - [ ] `free -m` — bellek kullanımı
  - [ ] `top` / `htop` — sistem kaynakları
- [ ] Process nedir? — çalışan program
- [ ] PID — process identifier
- [ ] Port — hangi uygulama hangi portu dinliyor
- [ ] `lsof -i :3000` — port kullanan process
- [ ] `ps aux` — çalışan process'ler
- [ ] `kill` / `kill -9` farkı
- [ ] Servis log okuma — `journalctl`, `systemctl status`
- [ ] Dosya izinleri — rwx, 755, 644 ne demek?
- [ ] Crontab — zamanlı görev
- [ ] Reverse proxy kavramı — nginx public port → uygulama port
- [ ] Nginx temel config — server block, location, proxy_pass
- [ ] Firewall temel farkındalığı — UFW ile port açma/kapatma

---

### Aşama 3 — PM2 ve Node Operasyonu

- [ ] PM2 nedir? — Node.js process manager
- [ ] `pm2 start` / `stop` / `restart` / `delete`
- [ ] `pm2 logs` / `pm2 logs --lines 200`
- [ ] `pm2 monit` — canlı izleme
- [ ] `ecosystem.config.js` — multi-app config
- [ ] `pm2 startup` — sunucu yeniden başlayınca otomatik başlat
- [ ] `pm2 save`
- [ ] Cluster mode — CPU core sayısı kadar process
- [ ] Log rotation — `pm2-logrotate`
- [ ] Graceful shutdown — SIGTERM ile açık bağlantıları kapat

---

### Aşama 4 — Docker ile Production

> Faz 3'te geliştirme ortamı için Docker öğrendik. Burada production perspektifi.

- [ ] Multi-stage build — build stage + production stage
  - [ ] Build stage: `node:20` ile `npm ci`, `npm run build`
  - [ ] Production stage: `node:20-alpine` ile sadece dist kopyala
  - [ ] Image boyutu karşılaştır (büyük vs küçük)
- [ ] `node:alpine` — neden küçük image?
- [ ] Non-root user ile container çalıştırma (güvenlik)
- [ ] Health check — Dockerfile içinde
- [ ] Container registry — Docker Hub, GitHub Container Registry (GHCR)
- [ ] Image tag stratejisi — `latest`, git SHA, semantic version
- [ ] Docker Compose production farkı — geliştirme vs production compose
- [ ] Kubernetes farkındalığı — container orchestration, ne zaman gerekir

---

### Aşama 5 — CI/CD

- [ ] CI/CD nedir? — Continuous Integration / Continuous Deployment
- [ ] GitHub Actions temel yapısı:
  - [ ] Workflow dosyası — `.github/workflows/*.yml`
  - [ ] `on` — trigger (push, pull_request, schedule)
  - [ ] `jobs` ve `steps`
  - [ ] `uses` — action kullanımı
  - [ ] `run` — shell komutu
  - [ ] `env` ve `secrets`
- [ ] CI pipeline adımları:
  - [ ] Checkout
  - [ ] Node.js kurulumu
  - [ ] Dependency install
  - [ ] Lint
  - [ ] Type check
  - [ ] Test
  - [ ] Build
- [ ] CD pipeline adımları:
  - [ ] Docker image build
  - [ ] Registry'ye push
  - [ ] Deploy (SSH, API veya platform webhook)
- [ ] Environment bazlı pipeline — staging vs production
- [ ] Secrets — `secrets.GITHUB_TOKEN`, özel secretlar
- [ ] Branch koruma — main'e doğrudan push yasak, PR + CI zorunlu
- [ ] Migration adımı ne zaman çalışır? — deploy öncesi mi, sonrası mı?
- [ ] Başarısız deploy — ne olur, nasıl rollback yapılır?
- [ ] Deployment strategy farkındalığı — blue/green, rolling, canary

**Veritabanı Migration Stratejisi CI/CD'de**
- [ ] Migration ne zaman çalışmalı? — deploy öncesi mi, sonrası mı?
- [ ] Deploy öncesi migration riski — yeni migration eski kod ile uyumsuz olabilir
- [ ] Deploy sonrası migration — eski kod yeni şemayı bilmiyor; kısa süre tutarsızlık
- [ ] Expand/contract pattern — en güvenli yöntem
  - [ ] Expand: yeni sütun ekle (eski kod çalışmaya devam eder)
  - [ ] Deploy: yeni kodu deploy et (her iki sütunu da kullanır)
  - [ ] Contract: eski sütunu kaldır (artık kullanılmıyor)
- [ ] Zero-downtime migration için backward-compatible değişiklikler yap
- [ ] `NOT NULL` sütun eklemenin tehlikesi — önce nullable, sonra doldur, sonra NOT NULL
- [ ] Migration rollback — down migration'ı da yaz, test et
- [ ] Production'da migration çalıştırmadan önce staging'de test et
- [ ] Büyük tabloda migration — LOCK tehlikesi, `pg_repack` farkındalığı

---

### Aşama 6 — Gözlem ve Bakım

- [ ] Sentry kurulumu ve production'a bağlama
- [ ] Sentry source map upload — minified kod yerine orijinal stack trace
- [ ] Uptime monitoring — UptimeRobot, Better Uptime
- [ ] `/health` endpoint — DB ve Redis bağlantısı kontrol
- [ ] Temel alertler — downtime, yüksek hata oranı
- [ ] Cron job takibi — çalıştı mı, ne kadar sürdü?
- [ ] Production log okuma — structured log + grep
- [ ] Incident sonrası brefing — ne oldu, neden oldu, tekrar olmasın
- [ ] Teknik borç listesi tutma — birikmesin

---

### Ödevler

- [ ] Frontend ve backend'i ayrı deploy et
- [ ] PM2 ile API'yi ayağa kaldır
- [ ] GitHub Actions ile lint + test + build pipeline kur
- [ ] SSH ile sunucuya bağlan, log oku, process kontrol et
- [ ] Health check ve uptime monitor ekle
- [ ] Multi-stage Dockerfile ile production image oluştur
- [ ] Nginx ile reverse proxy kur

### Mini Proje

**`deployment-playbook.md`**  
Kendi projelerini deploy ederken izleyeceğin adım adım rehber. Her adım, komutlarıyla birlikte.

### Çıkış Kriteri

- [ ] Projeyi internete çıkarabiliyorsun
- [ ] Hata olduğunda nereye bakacağını biliyorsun
- [ ] Basit CI/CD akışı kurabiliyorsun
- [ ] Server tarafı sana tamamen kara kutu gelmiyor
- [ ] Production için optimize edilmiş Docker image oluşturabiliyorsun
- [ ] Nginx ile reverse proxy kurabiliyorsun

---

## Faz 7 Köprüsü — Roadmap Sonu

### Bu fazda ne öğrendin?
Deploy, Linux, PM2, Docker production, CI/CD, database migration stratejisi ve observability. Projen artık internette, izleniyor ve bakımı yapılıyor.

### Bu faz senden sonra ne açtı?
Roadmap bitti — ama öğrenme bitmedi. Şu anda elimde olan şey gerçek projelerde kullanılabilir, savunulabilir, üretime yakın bir full-stack geliştirici profiline karşılık geliyor.

Bundan sonra ilerleyeceğin yerler:
- Gerçek bir projede çalışmak — ekip, code review, PR süreci
- Open source katkısı — küçük bir bug fix bile çok şey öğretir
- Sistem tasarımı daha derin — NeetCode, ByteByteGo, gerçek vaka çalışmaları
- İş mülakatları — DSA + system design + take-home project
- Seçmeli derinleşme — Kubernetes, GraphQL, event sourcing, platform engineering

### Geliştiricilerin %80'inin yaptığı hata
- Projeyi "çalışıyor" deyip hiç izlememek — Sentry'ye bakmamak, log okumamak
- CI/CD kurup test koşmayı atlamak — pipeline hızlansa da güven sağlamıyor
- Production'da `.env` dosyasını direkt sunucuya kopyalamak
- Database migration'ı test etmeden production'a uygulamak
- Deploy playbook yazmamak — "ben biliyorum zaten" demek, 6 ay sonra unutuluyor
- Graceful shutdown yazmamak — deploy sırasında açık istekler kesilir

### Açık kaynak okuma görevi
Kendi deploy ettiğin bir servisin GitHub Actions workflow dosyasına bak. Gerçek bir açık kaynak projenin (örn. `vercel/next.js`, `nestjs/nest`, `prisma/prisma`) `.github/workflows/` klasörünü incele. CI pipeline'ları nasıl kurulmuş? Test, lint, build hangi sırayla? Release nasıl yönetiliyor?

---

*Bu roadmap'i tamamladıysan: tebrikler. Ünvan değil, gerçek yetkinlik kazandın.*
