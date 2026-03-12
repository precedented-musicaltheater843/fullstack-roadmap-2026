# Faz 0 — Çalışma Temeli

---

## Bölüm 0 — Hazırlık, Ortam ve Çalışma Disiplini
**Tahmini Süre: 3–5 gün**

### Amaç
Ortamı kurmak, hata mesajı okumayı öğrenmek ve çalışmayı sürdürülebilir hale getirmek.

### Öğrenilecekler

- [ ] Node.js kurulumu ve sürüm kontrolü (nvm ile sürüm yönetimi)
- [ ] VS Code kurulumu ve temel verim ayarları
  - [ ] Prettier
  - [ ] ESLint
  - [ ] Error Lens
  - [ ] GitLens
- [ ] Terminal temel komutları
- [ ] Dosya / klasör mantığı
- [ ] Yorum satırları
- [ ] Basit markdown not tutma
- [ ] Hata mesajı okumaya alışma
- [ ] Console ile düşünme alışkanlığı

### Ödevler

- [ ] `node -v` ve `npm -v` doğrula
- [ ] 5 farklı `.js` dosyası oluştur ve Node ile çalıştır
- [ ] Kasıtlı syntax error üret, mesajı oku
- [ ] Bir `study-log.md` not dosyası aç

### Mini Proje

**`study-log.js`**  
Gün, konu, süre, not bilgilerini değişkenlerde tut ve çıktısını ver.

### Çıkış Kriteri

- [ ] Terminalden JS dosyası çalıştırabiliyorsun
- [ ] Hata alınca satırı ve nedeni kabaca bulabiliyorsun
- [ ] VS Code içinde yeni klasör / dosya / terminal akışını rahat kullanabiliyorsun

---

## Bölüm 0.5 — Git ve GitHub
**Tahmini Süre: 1 hafta**

### Amaç
Her projeyi versiyonlamak, branch kullanmak ve GitHub üzerinde düzenli ilerlemek.

### Öğrenilecekler

**Temel**
- [ ] Git nedir, neden gereklidir?
- [ ] repo / commit / branch / merge / remote
- [ ] `git init`
- [ ] `git status`
- [ ] `git add` / `git add -p` (kısmi staging)
- [ ] `git commit`
- [ ] `git log --oneline`
- [ ] `git diff` / `git diff --staged`
- [ ] `git restore` / `git reset` (soft, mixed, hard farkı)
- [ ] `git stash`

**GitHub**
- [ ] Remote ekleme
- [ ] push / pull / clone / fetch
- [ ] `README.md`
- [ ] `.gitignore`
- [ ] Issues / pull request farkındalığı
- [ ] GitHub Actions farkındalığı (ne işe yarar?)

**Branch İş Akışı**
- [ ] Feature branch mantığı
- [ ] Merge vs rebase farkındalığı
- [ ] Merge conflict çözümü
- [ ] Conventional commits formatı (`feat:`, `fix:`, `chore:` vb.)
- [ ] Küçük ama anlamlı commit alışkanlığı

### Ödevler

- [ ] Study-log projesini GitHub'a yükle
- [ ] Yeni branch aç, değişiklik yap, merge et
- [ ] `.env` ve `node_modules`'ü ignore et
- [ ] README yaz
- [ ] Conventional commit formatında 5 commit at

### Mini Proje

**`git-practice-repo`**  
En az 5 anlamlı commit, 2 branch, 1 conflict çözümü, 1 README.

### Çıkış Kriteri

- [ ] Yeni projede otomatik `git init` alışkanlığın var
- [ ] Branch açıp merge etmek seni korkutmuyor
- [ ] `.gitignore` neden kritik olduğunu biliyorsun
- [ ] Commit mesajlarını anlamlı ve tutarlı yazabiliyorsun

---

## Bölüm 0.7 — Web Temelleri Tazeleme
**Tahmini Süre: 1 hafta**

### Amaç
Web'in çekirdek parçalarını sağlamlaştırmak.

### Öğrenilecekler

**HTML**
- [ ] Semantic HTML (header, nav, main, section, article, aside, footer)
- [ ] Form elemanları (input türleri, select, textarea, fieldset)
- [ ] label / input ilişkisi ve `for` attribute
- [ ] Button türleri (`type="button"`, `type="submit"`, `type="reset"`)
- [ ] Link vs button farkı ve ne zaman hangisi kullanılır
- [ ] `data-*` attribute farkındalığı
- [ ] Meta tags ve head yapısı

**CSS**
- [ ] Box model (margin, border, padding, content)
- [ ] display (block, inline, inline-block, flex, grid, none)
- [ ] position (static, relative, absolute, fixed, sticky)
- [ ] Flexbox (justify-content, align-items, gap, flex-wrap, flex-direction)
- [ ] Grid (grid-template-columns, grid-template-rows, grid-area, gap)
- [ ] Responsive mantık (media queries, breakpoints)
- [ ] rem / em / px / % / vw / vh farkı
- [ ] overflow / z-index temel mantığı
- [ ] CSS custom properties (değişkenler)
- [ ] Selector özgüllüğü (specificity) farkındalığı

**Web Temelleri**
- [ ] Browser request yaşam döngüsü (URL bar'a yazınca ne olur?)
- [ ] DNS nedir?
- [ ] Cookie, localStorage, sessionStorage farkı ve ne zaman hangisi
- [ ] Same-origin policy nedir?
- [ ] CORS nedir, neden var?
- [ ] HTTP vs HTTPS farkı (temel)

**Accessibility (A11y)**
- [ ] Semantic yapının ekran okuyucuyla ilişkisi
- [ ] Heading sırası (h1 → h2 → h3, atlamama)
- [ ] Form label zorunluluğu
- [ ] Keyboard erişilebilirliği (Tab, Enter, Escape, Space)
- [ ] Focus yönetimi ve görünür focus ring
- [ ] Color contrast farkındalığı
- [ ] aria-label / aria-describedby / role — sadece gerektiğinde kullan
- [ ] Alternatif metin (alt attribute)

### Ödevler

- [ ] Tam semantic HTML ile basit landing page yaz
- [ ] Form + label + validation message içeren sayfa yap
- [ ] Flex ve Grid ile iki ayrı layout kur
- [ ] Sadece klavye ile gezerek test et
- [ ] DevTools ile box model görselleştir

### Mini Proje

**`semantic-profile-page`**  
Responsive, semantic ve erişilebilir profil sayfası.

### Çıkış Kriteri

- [ ] Link ve button'ı bilinçsiz karıştırmıyorsun
- [ ] Basit responsive layout kurabiliyorsun
- [ ] Erişilebilirliğin sadece ekran okuyucu değil, ürün kalitesi konusu olduğunu biliyorsun
- [ ] CSS Flexbox ile temel layout sorunlarını çözebiliyorsun

---

## Faz 0 Köprüsü

### Bu fazda ne öğrendin?
Terminal, Git, temel web yapısı ve çalışma disiplini. Bunlar araçlar — asıl iş henüz başlamadı.

### Bu faz senden sonra ne açtı?
Git olmadan hiçbir proje yönetilemez. Terminal olmadan hiçbir araç çalıştırılamaz. Semantic HTML olmadan erişilebilir frontend yazılamaz. Sonraki her fazın temeli burada atıldı.

### Geliştiricilerin %80'inin yaptığı hata
- `.gitignore` olmadan `node_modules`'ü commit etmek
- Commit mesajlarını "fix", "update", "asdf" gibi anlamsız yazmak
- `div` soup — her şeyi `<div>` ile yazmak, semantic eleman kullanmamak

### Açık kaynak okuma görevi
VS Code'un GitHub reposuna git (`microsoft/vscode`). Herhangi bir `.md` dosyasını aç ve nasıl yazıldığına bak. Katkıda bulunma rehberini oku. Bir issue'ya göz at. Kod okumak zorunda değilsin — proje kültürünü hisset.
