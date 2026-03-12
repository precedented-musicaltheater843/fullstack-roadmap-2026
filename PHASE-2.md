# Faz 2 — TypeScript

---

## Bölüm 15 — TypeScript
**Tahmini Süre: 4–6 hafta**

### Amaç
TypeScript'i "tip yazmak" değil, hatayı erkenden yakalayan tasarım aracı olarak öğrenmek.

---

### Aşama 1 — Temel

- [ ] TS neden var? JS ile farkı ne?
- [ ] Type annotation
- [ ] Type inference (TS'nin otomatik tip çıkarımı)
- [ ] Primitive types: string, number, boolean, null, undefined, symbol
- [ ] Union types (`string | number`)
- [ ] Literal types (`"admin" | "user"`)
- [ ] Type alias (`type UserId = string`)
- [ ] Interface (`interface User { ... }`)
- [ ] Type alias vs interface farkı ve ne zaman hangisi
- [ ] Optional property (`name?: string`)
- [ ] Readonly (`readonly id: number`)
- [ ] Narrowing (typeof, instanceof, in, custom type guard)
- [ ] unknown vs any — neden any tehlikeli
- [ ] never — tükenen union, ulaşılamaz kod
- [ ] void — değer döndürmeyen fonksiyon

---

### Aşama 2 — Veri Modelleme

- [ ] Array types (`string[]`, `Array<string>`)
- [ ] Tuple (`[string, number]`)
- [ ] Enum — neden genellikle union tercih edilir
- [ ] Function types — parametre ve return type
- [ ] Object types — inline ve interface
- [ ] Intersection types (`A & B`)
- [ ] Discriminated union (tagged union pattern)
- [ ] Index signature (`[key: string]: unknown`)
- [ ] API response modelleme
- [ ] Utility types
  - [ ] `Partial<T>`
  - [ ] `Required<T>`
  - [ ] `Pick<T, K>`
  - [ ] `Omit<T, K>`
  - [ ] `Record<K, V>`
  - [ ] `Exclude<T, U>`
  - [ ] `Extract<T, U>`
  - [ ] `ReturnType<T>`
  - [ ] `Awaited<T>`
  - [ ] `Parameters<T>`
  - [ ] `NonNullable<T>`
- [ ] Generics — `<T>` parametre kavramı
- [ ] Generic constraints (`T extends SomeType`)
- [ ] Generic functions ve generic interfaces
- [ ] Conditional types farkındalığı (`T extends U ? X : Y`)
- [ ] Template literal types farkındalığı

---

### Aşama 3 — Gerçek Proje Kullanımı

- [ ] tsconfig.json temel ayarlar
  - [ ] `strict: true` — neden açılmalı
  - [ ] `target`, `module`, `lib`
  - [ ] `outDir`, `rootDir`
  - [ ] `paths` (path alias)
  - [ ] `baseUrl`
  - [ ] `esModuleInterop`
  - [ ] `skipLibCheck`
- [ ] Declaration files (`.d.ts`) farkındalığı
- [ ] `@types/*` paketleri ne işe yarar?
- [ ] Zod ile runtime validation + type inference (`z.infer<typeof schema>`)
- [ ] Zod vs TypeScript: derleme zamanı vs çalışma zamanı
- [ ] JS projeyi TS'ye kademeli taşıma (`allowJs`, `checkJs`)
- [ ] Prisma / Drizzle ile otomatik type safety
- [ ] Shared types: ne zaman faydalı, ne zaman aşırı coupling
- [ ] `as const` kullanımı
- [ ] Non-null assertion operator (`!`) — ne zaman ve neden riskli

---

### Ödevler

- [ ] any kullanmadan küçük servis yaz
- [ ] Zod ile kayıt formu şeması kur
- [ ] Discriminated union ile Result pattern yaz
- [ ] JS mini projelerinden birini TS'ye geçir
- [ ] Utility types ile mevcut type'ları türet

### Mini Projeler

- [ ] `typed-api-client.ts`
- [ ] `result-pattern.ts`
- [ ] `validation-schema.ts`

### Çıkış Kriteri

- [ ] any'e refleks olarak gitmiyorsun
- [ ] Zod ve TypeScript'in görev farkını biliyorsun
- [ ] TypeScript ile veri modelleme yapabiliyorsun
- [ ] tsconfig'i baştan ayarlayabiliyorsun

---

## Faz 2 Köprüsü

### Bu fazda ne öğrendin?
TypeScript ile statik tip güvenliği, veri modelleme, generics ve runtime validation. JS'i TS'ye geçirmenin nasıl yapıldığını gördün.

### Bu faz senden sonra ne açtı?
NestJS tamamen TypeScript üzerine kurulu — decorator'lar, DTO'lar, generic repository'ler hepsi buradaki bilgiyle okunur. Prisma'nın ürettiği tipler, Zod şemaları, API response modelleme — bunların hepsi TypeScript bilgisi ister. Frontend'de de `useQuery<User[]>` gibi generic kullanımlar doğal gelecek.

### Geliştiricilerin %80'inin yaptığı hata
- `any` ile "çalıştırdım geçti" demek — TS'yi devre dışı bırakmak
- Her yere `interface` yazmak, `type alias` neden farklı bilmemek
- `Partial<T>` yerine her alanı tek tek `?` yapmak
- Zod'u sadece form validation için bilmek, API response parse etmek için kullanmamak
- `strict: false` ile başlayıp alışkanlık edinmek — en baştan `strict: true`

### Açık kaynak okuma görevi
`trpc` veya `zod` kütüphanesinin GitHub reposuna git. `src/` klasörüne bak. Tipler nasıl tanımlanmış, generic'ler nasıl kullanılmış? Anlamasan da olur — sadece gerçek kütüphane kodunda TypeScript'in nasıl göründüğünü hisset.
