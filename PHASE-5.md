# Faz 5 — Frontend

---

## Bölüm 21 — React, Frontend Engineering ve Erişilebilirlik
**Tahmini Süre: 8–9 hafta**

### Amaç
Sadece çalışan arayüz değil; sürdürülebilir, test edilebilir ve erişilebilir frontend kurmak.

---

### Aşama 1 — React Temeli

- [ ] JSX — nedir, nasıl derlenir?
- [ ] Component — fonksiyon component
- [ ] Props — parent'tan child'a veri
- [ ] Children prop
- [ ] Conditional rendering — `&&`, ternary, erken return
- [ ] List rendering — `.map()` ve `key` prop önemi
- [ ] `key` neden index kullanmamalı?
- [ ] useState
- [ ] Controlled input — value + onChange
- [ ] Event handling — onClick, onSubmit, onChange
- [ ] Form submit — `e.preventDefault()`
- [ ] Lifting state up
- [ ] Composition — component içine component

---

### Aşama 2 — Hooks ve Veri Akışı

- [ ] useEffect — side effect ne zaman çalışır?
- [ ] Dependency array — `[]`, `[dep]`, boş bırakmak
- [ ] Cleanup function — event listener, subscription temizleme
- [ ] Stale closure tuzağı
- [ ] useRef — DOM erişimi ve değer saklama (render tetiklemiyor)
- [ ] useReducer — karmaşık state için useState alternatifi
- [ ] useMemo — pahalı hesaplamayı memoize et
- [ ] useCallback — fonksiyon referansını memoize et
- [ ] Ne zaman optimizasyon gerekir, ne zaman erken optimizasyon?
- [ ] useContext — prop drilling'den kaçınma
- [ ] Context'in render performansına etkisi
- [ ] Custom hooks — mantığı yeniden kullanılabilir hale getir
- [ ] Veri çekme lifecycle: loading → data → error → empty
- [ ] Optimistic UI farkındalığı — cevap gelmeden güncelle

---

### Aşama 3 — Tailwind CSS

- [ ] Tailwind nedir? — utility-first CSS
- [ ] Neden Tailwind? — inline style'dan farkı, class birleşimi
- [ ] Kurulum — Vite veya Next.js ile
- [ ] Temel utility sınıflar:
  - [ ] Spacing — `p-4`, `m-2`, `px-6`, `py-2`, `gap-4`, `space-x-2`
  - [ ] Sizing — `w-full`, `h-screen`, `max-w-lg`, `min-h-0`
  - [ ] Flexbox — `flex`, `flex-col`, `items-center`, `justify-between`, `flex-1`
  - [ ] Grid — `grid`, `grid-cols-3`, `col-span-2`
  - [ ] Typography — `text-sm`, `text-lg`, `font-bold`, `text-center`, `leading-tight`
  - [ ] Colors — `bg-blue-500`, `text-gray-900`, `border-red-300`
  - [ ] Border — `border`, `rounded`, `rounded-lg`, `border-gray-200`
  - [ ] Shadow — `shadow`, `shadow-md`, `shadow-lg`
  - [ ] Opacity — `opacity-50`, `disabled:opacity-50`
  - [ ] Cursor — `cursor-pointer`, `cursor-not-allowed`
- [ ] Responsive prefix — `sm:`, `md:`, `lg:`, `xl:`
- [ ] State modifiers — `hover:`, `focus:`, `active:`, `disabled:`, `group-hover:`
- [ ] Dark mode — `dark:` prefix
- [ ] `clsx` / `cn` utility ile koşullu sınıf
- [ ] `tailwind.config.js` — tema genişletme, custom color, custom font
- [ ] Arbitrary values — `w-[342px]`, `text-[#ff6b6b]`
- [ ] `@apply` — Tailwind sınıflarını CSS'e çıkarma (ne zaman kullanılır)
- [ ] shadcn/ui Tailwind ile uyumu — neden birlikte çalışır

---

### Aşama 4 — Form ve İstemci Tarafı Kalitesi

- [ ] React Hook Form — register, handleSubmit, formState
- [ ] Zod ile form validation şeması
- [ ] `zodResolver` entegrasyonu
- [ ] Field-level error gösterimi
- [ ] Form UX — submit sırasında disable, pending spinner
- [ ] Server error gösterimi (form geneli hata)
- [ ] Toast / notification — ne zaman kullanılır, ne zaman abartılır
- [ ] Skeleton loading state
- [ ] Empty state (veri yok gösterimi)
- [ ] Retry state (hata sonrası tekrar dene butonu)
- [ ] Optimistic update ile form submit
- [ ] Multi-step form farkındalığı

---

### Aşama 5 — Frontend Engineering

- [ ] Component sınırları — ne kadar büyük, ne kadar küçük?
- [ ] Smart (container) vs presentational component ayrımı
- [ ] Feature-based klasörleme
- [ ] Barrel export (`index.ts`) ne zaman iyidir?
- [ ] UI kit / design system farkındalığı
- [ ] shadcn/ui — neden component'leri kopyalar (owned code)
- [ ] Component composition pattern — `<Card>`, `<Card.Header>`, `<Card.Body>`
- [ ] Semantic HTML — React içinde de geçerli
- [ ] Accessibility
  - [ ] Keyboard navigation — Tab sırası, focus görünürlüğü
  - [ ] Focus management — modal açılınca focus trap
  - [ ] `role`, `aria-label`, `aria-describedby` — sadece gerektiğinde
  - [ ] Dialog ve modal pattern — React Portal ile
  - [ ] Dropdown ve menu pattern
  - [ ] Tab widget pattern
  - [ ] Screen reader ile test etme farkındalığı
- [ ] Responsive tasarım — Tailwind breakpoints ile
- [ ] Render performansı
  - [ ] Re-render ne zaman olur?
  - [ ] React DevTools Profiler ile render ölçme
  - [ ] `React.memo` ne zaman kullanılır?
  - [ ] Key ile component reset trick

---

### Aşama 6 — State ve Server State

- [ ] Local state — component seviyesi
- [ ] Lifted state — parent seviyesi
- [ ] Context — uygulama geneli ama sık değişmeyen (tema, kullanıcı)
- [ ] Context performans tuzağı — her render tetiklenir
- [ ] Zustand — global state için hafif çözüm
  - [ ] Store oluşturma
  - [ ] Actions
  - [ ] Selectors (partial subscription)
  - [ ] Zustand ile devtools
- [ ] TanStack Query — server state yönetimi
  - [ ] `useQuery` — veri çekme, loading/error/data
  - [ ] `useMutation` — veri değiştirme
  - [ ] Query keys — cache anahtarları
  - [ ] Stale time / cache time
  - [ ] `queryClient.invalidateQueries` — cache geçersiz kıl
  - [ ] `refetchOnWindowFocus` davranışı
  - [ ] Optimistic update
  - [ ] Infinite query farkındalığı (infinite scroll)
  - [ ] QueryClient ile global hata handling

---

### Ödevler

- [ ] Form + validation + error + success durumlu sayfa yap
- [ ] Accessible modal / dialog kur (focus trap dahil)
- [ ] List / detail / filter / search içeren React sayfası yap
- [ ] TanStack Query ile server state yönet
- [ ] Klavye ile gezerek test yap
- [ ] Tailwind ile responsive dashboard layout yaz
- [ ] Zustand ile basit global state kur

### Mini Projeler

- [ ] `todo-react-app` — CRUD, filter, TanStack Query
- [ ] `dashboard-ui` — Tailwind, responsive, Zustand
- [ ] `settings-panel` — form, validation, server hata gösterimi

### Çıkış Kriteri

- [ ] Sadece güzel görünen değil, durumları düşünülmüş UI yapabiliyorsun
- [ ] Accessibility'yi sonradan eklenen süs sanmıyorsun
- [ ] Server state ve local state ayrımını daha iyi görüyorsun
- [ ] Tailwind ile hızlı ve tutarlı UI yazabiliyorsun
- [ ] Zustand ve TanStack Query'yi birlikte kullanabiliyorsun

---

## Bölüm 22 — Next.js, Testing ve Full-stack UI Patterns
**Tahmini Süre: 7–8 hafta**

### Amaç
Modern Next.js ile üretime daha yakın arayüzler ve kapsamlı test akışı kurmak.

---

### Aşama 1 — Next Temeli

- [ ] Next.js neden var? React'tan farkı
- [ ] App Router (v13+)
- [ ] `layout.tsx` — paylaşılan düzen
- [ ] `loading.tsx` — Suspense ile otomatik loading
- [ ] `error.tsx` — hata sınırı
- [ ] `not-found.tsx`
- [ ] Route segments — klasör yapısı = URL yapısı
- [ ] Dynamic routes — `[id]`, `[...slug]`
- [ ] Route groups — `(auth)`, `(dashboard)` (URL'yi etkilemez)
- [ ] Parallel routes farkındalığı
- [ ] Intercepting routes farkındalığı
- [ ] Metadata API — `generateMetadata`, static metadata
- [ ] `next/image` — otomatik optimizasyon
- [ ] `next/font` — layout shift olmadan font yükleme
- [ ] Environment variables — `NEXT_PUBLIC_` prefix kuralı
- [ ] Static rendering — build zamanı
- [ ] Dynamic rendering — request zamanı
- [ ] `revalidate` — ISR (Incremental Static Regeneration)
- [ ] Server component — default, async, veri doğrudan çeker
- [ ] Client component — `"use client"`, hook kullanabilir, state tutabilir
- [ ] Server vs client component sınırı
- [ ] Route handlers — `route.ts` — API endpoint
- [ ] Server Actions — form submit, mutation farkındalığı
- [ ] Middleware — `middleware.ts` — auth gate, redirect

---

### Aşama 2 — Auth ve Veri Entegrasyonu

- [ ] Cookie tabanlı auth ile Next entegrasyonu
- [ ] Middleware ile protected route
- [ ] Role-aware UI — server component'te kullanıcıyı kontrol et
- [ ] `cookies()` ve `headers()` server component'te kullanımı
- [ ] Next-auth / Auth.js farkındalığı
- [ ] Optimistic UI — TanStack Query ile
- [ ] Form submit akışları — server action vs client mutation
- [ ] Server error'ı güvenli gösterme — stack trace client'a gitmesin
- [ ] Backend-for-frontend (BFF) mantığı
- [ ] `fetch` ile server component'te veri çekme ve caching

---

### Aşama 3 — Frontend Testing ve MSW

**Vitest + React Testing Library**
- [ ] Vitest kurulumu Next.js ile
- [ ] RTL — `render`, `screen`, `fireEvent`, `userEvent`
- [ ] Sorgular — `getByRole`, `getByLabelText`, `getByText` (öncelik sırası)
- [ ] `queryBy` vs `getBy` vs `findBy` farkı
- [ ] `userEvent` neden `fireEvent`'ten daha iyi?
- [ ] Kullanıcı davranışına yakın test yazma
- [ ] Async test — `waitFor`, `findBy`
- [ ] Component testi — render + interact + assert
- [ ] Custom hook testi — `renderHook`

**MSW (Mock Service Worker)**
- [ ] MSW nedir? — ağ katmanında API mock
- [ ] Neden MSW? — gerçek fetch çağrısı, gerçekçi test
- [ ] MSW vs jest.mock farkı — network level vs module level
- [ ] Handler tanımlama — `http.get`, `http.post`
- [ ] `HttpResponse` ile response döndürme
- [ ] `server.use()` ile test bazlı override
- [ ] Hata senaryosu — 500, 404, network error
- [ ] MSW ile loading state testi
- [ ] MSW browser integration (geliştirme ortamında da kullanılabilir)

**Playwright — E2E Testing**
- [ ] Playwright kurulumu
- [ ] `page.goto`, `page.click`, `page.fill`, `page.getByRole`
- [ ] Assertions — `expect(page).toHaveURL`, `expect(locator).toBeVisible`
- [ ] Test dosyası yapısı
- [ ] Auth state ile test — storage state
- [ ] Login akışı testi
- [ ] Form submit ve sonuç kontrolü
- [ ] Protected route testi — yetkisiz erişim kontrolü
- [ ] Flaky test nedenleri ve nasıl önlenir
- [ ] Playwright trace viewer

---

### Aşama 4 — Performans ve Ürün Kalitesi

- [ ] Bundle analizi — `@next/bundle-analyzer`
- [ ] Gereksiz client component azaltma
- [ ] `next/image` ile image optimization
- [ ] Streaming — Suspense ile kısmi render
- [ ] Loading state kalitesi — skeleton, blur placeholder
- [ ] SEO — title, description, canonical, Open Graph
- [ ] `metadata` API ile statik ve dinamik meta
- [ ] `sitemap.ts` ile otomatik sitemap
- [ ] `robots.ts`
- [ ] Lighthouse ile performans ölçme
- [ ] Core Web Vitals — LCP, FID/INP, CLS farkındalığı

---

### Ödevler

- [ ] Next ile dashboard kur
- [ ] Protected route ve auth gate implement et
- [ ] MSW ile API mock'lanan 5 component testi yaz
- [ ] RTL ile 10 component testi yaz
- [ ] Playwright ile kritik kullanıcı akışını test et
- [ ] Error / loading / empty state'leri kasıtlı test et
- [ ] Bundle analyzer ile büyük dependency tespit et

### Mini Projeler

- [ ] `dashboard-next`
- [ ] `auth-portal`
- [ ] `admin-panel-next`

### Çıkış Kriteri

- [ ] Next.js'te veri ve render stratejisini bilinçli seçebiliyorsun
- [ ] MSW ile API bağımlılığı olmadan component test yazabiliyorsun
- [ ] Playwright ile kritik akışları test edebiliyorsun
- [ ] Modern Next.js yapısını korkmadan kurabiliyorsun
