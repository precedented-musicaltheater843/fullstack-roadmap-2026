# Faz 1 — JavaScript

---

## Bölüm 1 — JavaScript'e Giriş
**Tahmini Süre: 2–3 gün**

### Amaç
JavaScript'in ne olduğunu, nerede çalıştığını ve ne iş yaptığını oturtmak.

### Öğrenilecekler

- [ ] JavaScript nedir?
- [ ] Browser vs Node.js farkı
- [ ] Derlenen / yorumlanan dil tartışmasına temel bakış
- [ ] Runtime kavramı
- [ ] Syntax nedir?
- [ ] Statement vs expression
- [ ] Değer üretmek ve çıktı almak
- [ ] Strict mode (`"use strict"`) ne işe yarar?

### Ödevler

- [ ] Browser console ve Node terminalde aynı küçük kodları çalıştır
- [ ] 10 farklı expression örneği yaz
- [ ] Statement ve expression örneklerini ayır

### Mini Proje

**`intro-playground.js`**  
Farklı veri ve expression'ları çıktılayan mini dosya.

### Çıkış Kriteri

- [ ] JS'in browser ve Node'da çalışabildiğini açıklayabiliyorsun
- [ ] Expression ile statement farkını örnekle anlatabiliyorsun

---

## Bölüm 2 — Değişkenler, Scope, Hoisting
**Tahmini Süre: 1 hafta**

### Amaç
let / const / var farkını ve scope davranışını sağlam kurmak.

### Öğrenilecekler

- [ ] Variable nedir?
- [ ] let / const / var
- [ ] Reassignment vs redeclaration farkı
- [ ] Declaration vs initialization
- [ ] Block scope
- [ ] Function scope
- [ ] Global scope
- [ ] Module scope farkındalığı
- [ ] Hoisting (var ve function declaration davranışı)
- [ ] Temporal dead zone (let/const hoisting)
- [ ] Shadowing
- [ ] Variable naming — camelCase, anlamlı isim, kısaltmadan kaçınma

### Ödevler

- [ ] var/let/const için 20 küçük örnek yaz
- [ ] Scope tahmin soruları çöz
- [ ] TDZ örnekleri üret
- [ ] Shadowing örnekleri yaz

### Mini Proje

**`counter-state.js`**  
Birkaç değişkenle küçük sayaç / kullanıcı durumu simülasyonu.

### Çıkış Kriteri

- [ ] var niye tehlikeli olduğunu açıklayabiliyorsun
- [ ] const değişmezliği ile referans değişmezliğini karıştırmıyorsun
- [ ] Scope hatalarını daha hızlı fark ediyorsun

---

## Bölüm 3 — Veri Tipleri ve Bellek Mantığı
**Tahmini Süre: 1 hafta**

### Amaç
Primitive vs reference ayrımını ve typeof davranışını anlamak.

### Öğrenilecekler

- [ ] string
- [ ] number (integer ve float fark yok, IEEE 754 farkındalığı)
- [ ] bigint
- [ ] boolean
- [ ] undefined
- [ ] null
- [ ] symbol (ne zaman kullanılır?)
- [ ] object
- [ ] function'ın teknik olarak object ailesi olması
- [ ] typeof (ve typeof null === "object" tuhaflığı)
- [ ] Primitive vs reference
- [ ] Stack / heap farkındalığı
- [ ] Değer kopyalanır vs referans kopyalanır
- [ ] `instanceof` operatörü

### Ödevler

- [ ] typeof tahmin soruları çöz
- [ ] Primitive ve reference için kopyalama örnekleri yaz
- [ ] null / undefined farkını örnekle göster

### Mini Proje

**`type-inspector.js`**  
Girilen değerlerin türünü ve davranışını raporlayan dosya.

### Çıkış Kriteri

- [ ] Primitive ve reference ayrımını anlatabiliyorsun
- [ ] `typeof null` tuhaflığını biliyorsun
- [ ] Basit kopyalama hatalarını tahmin edebiliyorsun

---

## Bölüm 4 — Type Conversion, Coercion, Truthy/Falsy
**Tahmini Süre: 5–6 gün**

### Amaç
JavaScript'in otomatik dönüşümlerini kontrol edebilmek.

### Öğrenilecekler

- [ ] Explicit conversion: String(), Number(), Boolean()
- [ ] Implicit coercion ne zaman tetiklenir?
- [ ] == vs === (ve neden === tercih edilir)
- [ ] Falsy değerler: `false`, `0`, `""`, `null`, `undefined`, `NaN`
- [ ] Truthy değerler: geri kalan her şey (`[]`, `{}` dahil)
- [ ] NaN — "Not a Number" ama tipi number
- [ ] Number.isNaN vs global isNaN farkı
- [ ] parseInt / parseFloat / Number farkı
- [ ] trim + conversion kombinasyonu
- [ ] Boş string, boş array, boş object davranışları
- [ ] `+` operatörü ile coercion tuzağı

### Ödevler

- [ ] 25 coercion tahmin sorusu çöz
- [ ] Kullanıcı girdisi normalize eden fonksiyon yaz
- [ ] == ve === farkını örneklerle ispatla

### Mini Proje

**`input-normalizer.js`**  
String girdileri temizleyip güvenli sayıya çeviren yardımcılar.

### Çıkış Kriteri

- [ ] Coercion yüzünden oluşan temel bug'ları anlayabiliyorsun
- [ ] truthy/falsy davranışını ezbersiz açıklayabiliyorsun

---

## Bölüm 5 — Operatörler
**Tahmini Süre: 4–5 gün**

### Amaç
Operatörleri sadece isim olarak değil, davranış olarak öğrenmek.

### Öğrenilecekler

- [ ] Arithmetic operators (`+`, `-`, `*`, `/`, `%`, `**`)
- [ ] Comparison operators (`>`, `<`, `>=`, `<=`, `==`, `===`, `!=`, `!==`)
- [ ] Logical operators (`&&`, `||`, `!`)
- [ ] Nullish coalescing (`??`)
- [ ] Optional chaining (`?.`)
- [ ] Assignment operators (`=`, `+=`, `-=`, `&&=`, `||=`, `??=`)
- [ ] Increment / decrement (`++`, `--`, prefix vs postfix farkı)
- [ ] Bitwise operators farkındalığı
- [ ] Operator precedence farkındalığı
- [ ] Short-circuit mantığı (lazy evaluation)
- [ ] Ternary operatör ve ne zaman okunabilir, ne zaman değil

### Ödevler

- [ ] 20 operator sonucu tahmin et
- [ ] `||` ile `??` farkını gösteren örnek yaz
- [ ] Optional chaining ile güvenli erişim yap
- [ ] `&&=`, `||=`, `??=` için birer örnek yaz

### Mini Proje

**`pricing-helper.js`**  
İndirim, vergi, stok ve fallback değerlerini hesaplayan mini araç.

### Çıkış Kriteri

- [ ] `||` ve `??` farkını biliyorsun
- [ ] Optional chaining ne zaman kurtardığını anlayabiliyorsun

---

## Bölüm 6 — Koşullar ve Kontrol Akışı
**Tahmini Süre: 4–5 gün**

### Amaç
Programın hangi durumda hangi dala girdiğini netleştirmek.

### Öğrenilecekler

- [ ] if / else if / else
- [ ] switch (ve break unutmanın sonucu)
- [ ] Ternary
- [ ] Guard clause (erken return)
- [ ] Nested condition azaltma mantığı
- [ ] `switch` yerine object lookup farkındalığı
- [ ] Koşul karmaşıklığını azaltmak: boolean değişkenler, helper fonksiyon

### Ödevler

- [ ] Aynı problemi if ve switch ile çöz
- [ ] Kötü yazılmış nested condition'ı refactor et
- [ ] Guard clause ile daha okunur hale getir
- [ ] Object lookup ile switch'i karşılaştır

### Mini Proje

**`role-access-check.js`**  
Rol, durum ve plan bilgisine göre erişim kararı veren fonksiyonlar.

### Çıkış Kriteri

- [ ] Karmaşık koşulları sadeleştirebiliyorsun
- [ ] Guard clause yazmak doğal geliyor

---

## Bölüm 7 — Döngüler, Iteration ve Dizide Düşünme
**Tahmini Süre: 1 hafta**

### Amaç
Tekrar eden işleri kontrollü şekilde yazmak ve iterasyon mantığını kurmak.

### Öğrenilecekler

- [ ] for (klasik)
- [ ] while
- [ ] do while
- [ ] break / continue
- [ ] for...of (iterables)
- [ ] for...in (dikkatli kullanım — object keys, ama tuzakları var)
- [ ] forEach
- [ ] map (dönüştürme)
- [ ] filter (filtreleme)
- [ ] find / findIndex
- [ ] some / every
- [ ] reduce (temel + orta seviye)
- [ ] flatMap farkındalığı
- [ ] Hangi yöntem ne zaman? — okunabilirlik vs performans dengesi
- [ ] Zincirleme (chaining) ne zaman iyi, ne zaman kaçınılmalı

### Ödevler

- [ ] Aynı işi for, for...of ve map ile yaz
- [ ] reduce ile toplam, grupla, dönüştür örnekleri yap
- [ ] for...in ile object gezerken dikkat edilmesi gerekenleri incele
- [ ] map + filter + reduce zincirleme örneği yaz

### Mini Proje

**`order-reports.js`**  
Sipariş listesi üstünde filtreleme, toplam alma, raporlama.

### Çıkış Kriteri

- [ ] Hangi iterasyon yöntemini neden seçtiğini söyleyebiliyorsun
- [ ] reduce sana tamamen yabancı değil

---

## Bölüm 8 — Fonksiyonlar ve Test Düşüncesi
**Tahmini Süre: 1.5 hafta**

### Amaç
Fonksiyonları tekrar eden kodu azaltan, anlam taşıyan yapı taşları olarak kurmak. Ve bu bölümden itibaren **"bu fonksiyonu nasıl test ederim?"** sorusunu sormaya başlamak.

### Öğrenilecekler

**Fonksiyon Temelleri**
- [ ] Function declaration
- [ ] Function expression
- [ ] Arrow function (ve `this` bağlamı farkı)
- [ ] Parameter / argument
- [ ] Default parameters
- [ ] return (ve erken return)
- [ ] Void fonksiyon vs değer döndüren fonksiyon
- [ ] Rest parameters (`...args`)
- [ ] Spread ile fonksiyon çağırma

**Fonksiyon Kalitesi**
- [ ] Pure function nedir? (aynı input → aynı output, yan etki yok)
- [ ] Side effect nedir ve ne zaman kaçınılır?
- [ ] Fonksiyon isimlendirme (fiil ile başlama: `getUser`, `isValid`, `calculateTotal`)
- [ ] Tek sorumluluk prensibi — fonksiyon bir iş yapar
- [ ] Parametreyi object olarak almak (named parameters)

**Test Düşüncesi — Giriş**
- [ ] "Bu fonksiyonu nasıl test ederim?" sorusunu her fonksiyon için sor
- [ ] Pure function'lar neden test edilmesi kolaydır?
- [ ] Edge case nedir? (boş array, null, negatif sayı, çok büyük değer)
- [ ] Happy path vs sad path farkı
- [ ] Manuel test etme: her fonksiyonu birden fazla input ile çalıştır
- [ ] Node.js built-in `assert` modülü ile basit doğrulama

### Ödevler

- [ ] Aynı işi declaration / expression / arrow ile yaz
- [ ] 10 kötü isimlendirilmiş fonksiyonu düzelt
- [ ] Pure ve impure fonksiyon örnekleri yaz
- [ ] Her yazdığın fonksiyon için en az 3 farklı input ile manuel test yap
- [ ] `assert` ile basit doğrulama örnekleri yaz

### Mini Proje

**`cart-service.js`**  
Sepet toplamı, indirim, ürün adedi, KDV hesaplayan fonksiyon seti. Her fonksiyon için `assert` ile manuel testler dahil.

### Çıkış Kriteri

- [ ] Fonksiyonu küçük parçalara bölebiliyorsun
- [ ] return unutma ve yan etki sorunlarını daha net görebiliyorsun
- [ ] Her fonksiyon için "edge case nedir?" diye sorabiliyorsun
- [ ] Pure fonksiyon yazmanın test edilebilirliği nasıl artırdığını hissediyorsun

---

## Bölüm 9 — String, Array, Object Built-in'leri
**Tahmini Süre: 2 hafta**

### Amaç
Pratikte en sık kullanılan built-in method'ları gerçekten kullanabilir hale gelmek.

### Öğrenilecekler

**String**
- [ ] trim / trimStart / trimEnd
- [ ] slice / substring farkı
- [ ] includes / startsWith / endsWith
- [ ] toLowerCase / toUpperCase
- [ ] split / join kombinasyonu
- [ ] replace / replaceAll
- [ ] padStart / padEnd
- [ ] repeat
- [ ] Template literals (multi-line, expression gömme)
- [ ] String.raw farkındalığı
- [ ] at(-1) ile sondan erişim

**Array**
- [ ] push / pop / shift / unshift
- [ ] includes / indexOf / lastIndexOf
- [ ] slice (kopyalar) vs splice (mutate eder — fark kritik)
- [ ] concat / spread ile birleştirme farkı
- [ ] map / filter / find / findIndex / some / every / reduce
- [ ] sort (compare function olmadan tehlikesi)
- [ ] reverse (in-place mutation dikkat)
- [ ] flat / flatMap
- [ ] Array.from / Array.of
- [ ] fill / copyWithin farkındalığı
- [ ] at(-1) ile sondan erişim

**Object**
- [ ] Object.keys / Object.values / Object.entries
- [ ] Object.fromEntries
- [ ] Object.assign (shallow copy)
- [ ] Object.hasOwn (hasOwnProperty yerine modern)
- [ ] Destructuring (nested dahil)
- [ ] Spread ile kopyalama ve merge
- [ ] Computed property names (`[key]: value`)
- [ ] Property shorthand (`{ name, age }`)
- [ ] Object.freeze vs Object.seal farkındalığı
- [ ] Object.defineProperty farkındalığı

**Set / Map**
- [ ] Set: unique değer koleksiyonu, has/add/delete/size
- [ ] WeakSet farkındalığı
- [ ] Map: key-value, herhangi tip key olabilir, has/get/set/delete/size
- [ ] WeakMap farkındalığı
- [ ] Ne zaman object yerine Map tercih edilir?
- [ ] Ne zaman array yerine Set tercih edilir?

**Date / JSON / Math**
- [ ] Date: new Date(), getTime(), toISOString()
- [ ] Date tuzakları (timezone, ay 0-indexed)
- [ ] JSON.parse / JSON.stringify (ve replacer/reviver)
- [ ] JSON.stringify ile pretty print
- [ ] Math.floor / ceil / round / abs / min / max / random / pow / sqrt
- [ ] Number.isFinite / Number.isInteger / Number.toFixed

### Ödevler

- [ ] Her method için mini örnekler yaz
- [ ] sort ile hatalı sıralama üret, sonra compare function ile düzelt
- [ ] Set ve Map için 3 gerçek kullanım çıkar
- [ ] splice ile slice karışıklığını gösteren örnek yaz

### Mini Proje

**`product-utils.js`**  
Ürün filtreleme, arama, sıralama, uniq üretme, formatlama.

### Çıkış Kriteri

- [ ] Sık kullanılan method'ları proje içinde rahat kullanabiliyorsun
- [ ] sort, splice, reference etkileri gibi tuzakları biliyorsun
- [ ] Map ve Set'i sadece isim olarak değil, pratik farkıyla biliyorsun

---

## Bölüm 10 — Referans, Kopyalama, Immutability
**Tahmini Süre: 5–6 gün**

### Amaç
Aynı veriyi yanlışlıkla bozma problemini anlamak.

### Öğrenilecekler

- [ ] Shallow copy — spread, Object.assign, Array.slice
- [ ] Deep copy — structuredClone, JSON parse/stringify (ve sınırları)
- [ ] Spread ile kopyalama sınırları (sadece bir seviye)
- [ ] Nested object problemi — neden spread yetmez?
- [ ] Immutability nedir, neden önemlidir?
- [ ] Referans paylaşımı — aynı nesneyi iki yerde tutmanın tehlikeleri
- [ ] Array metodlarının mutation yapanları vs yapmayanları
  - [ ] Mutation yapanlar: push, pop, shift, unshift, sort, reverse, splice, fill
  - [ ] Yeni dizi döndürenler: map, filter, slice, concat, flat, flatMap
- [ ] Object update — spread ile güvenli güncelleme
- [ ] Nested immutable update (React state güncellemesine hazırlık)

### Ödevler

- [ ] Aynı object'i iki yerde kullanıp mutation bug'ı üret
- [ ] Shallow vs deep copy farkını göster
- [ ] Nested veri güvenli güncelleme pratiği yap
- [ ] structuredClone ile JSON parse/stringify farkını karşılaştır

### Mini Proje

**`profile-updater.js`**  
Kullanıcı profilini immutability ile güncelleyen yardımcı fonksiyonlar.

### Çıkış Kriteri

- [ ] Neden aynı object'in bir yerde değişince başka yerde de değiştiğini anlayabiliyorsun
- [ ] Immutability'nin React tarafında neden önemli olduğunu hissediyorsun
- [ ] Hangi array metodunun orijinali değiştirdiğini ayırt edebiliyorsun

---

## Bölüm 11 — Hata Yönetimi ve Defansif Kod
**Tahmini Süre: 1 hafta**

### Amaç
Kodun sadece mutlu senaryoda değil, kötü senaryoda da güvenli davranmasını sağlamak.

### Öğrenilecekler

- [ ] Error nedir? Error türleri: TypeError, RangeError, ReferenceError, SyntaxError
- [ ] throw — ne zaman kullanılır, ne fırlatılır?
- [ ] try / catch / finally
- [ ] Error objesi: message, name, stack
- [ ] Custom error sınıfları (`class ValidationError extends Error`)
- [ ] Girdi doğrulama (type check, range check, required check)
- [ ] Null / undefined korumaları (optional chaining, nullish coalescing)
- [ ] Early return / fail fast mantığı
- [ ] Kullanıcıya gösterilecek hata ile loglanacak hata farkı
- [ ] Error propagation — hatayı yukarı taşımak ne zaman doğru?
- [ ] Try-catch abartmama — her yere koymak anti-pattern

**Hata Yönetimi Zihinsel Modeli**
- [ ] Her isteğin dört aşaması vardır: **Girdi → Doğrulama → İş Mantığı → Sonuç/Hata**
  - Girdi: dış dünyadan gelen ham veri (kullanıcı, API, DB)
  - Doğrulama: tip, format, zorunluluk, sınır kontrolü — hata varsa erken dön
  - İş mantığı: asıl işlem — hata varsa anlamlı custom error fırlat
  - Sonuç/Hata: başarı değeri veya yakalanmış hata — kullanıcıya uygun mesaj ver
- [ ] Bu modeli Bölüm 11'den itibaren her fonksiyon ve route için uygula
- [ ] İleride NestJS exception filter, API status code'ları hep bu modelin uzantısıdır

### Ödevler

- [ ] Hatalı input için güvenli yardımcı fonksiyonlar yaz
- [ ] Custom error sınıfı oluştur ve kullan
- [ ] try/catch ile dosya okuma simülasyonu yap
- [ ] Kötü input'larda anlamlı error üret

### Mini Proje

**`safe-parsers.js`**  
Güvenli number parse, JSON parse, date parse yardımcıları — custom error'larla.

### Çıkış Kriteri

- [ ] throw ve return null kullanımını karıştırmıyorsun
- [ ] Custom error sınıfı yazabiliyorsun
- [ ] Savunmacı kod yazmanın nedenini biliyorsun

---

## Bölüm 12 — Debugging, DevTools ve Kod Okuma
**Tahmini Süre: 4–5 gün**

### Amaç
Sorunu paniklemeden izole etmek ve araç kullanmayı öğrenmek.

### Öğrenilecekler

- [ ] `console.log` doğru kullanımı (ve neden sadece log ile debug yetmez)
- [ ] `console.table`, `console.group`, `console.time` gibi alternatifler
- [ ] `debugger` statement
- [ ] Chrome DevTools — Sources paneli
  - [ ] Breakpoint koyma
  - [ ] Step over / step into / step out
  - [ ] Watch expressions
  - [ ] Call stack okuma
  - [ ] Scope paneli
- [ ] Chrome DevTools — Network paneli
  - [ ] Request / response görmek
  - [ ] Headers inceleme
  - [ ] Payload ve response body
  - [ ] Status code okuma
- [ ] Stack trace okuma ve anlama
- [ ] Başkasının kodunu izleyerek anlama (code reading)
- [ ] Sistematik debug yaklaşımı: reproduce → isolate → fix → verify

### Ödevler

- [ ] Bilerek bug koy ve adım adım bul
- [ ] Network tab'da bir API isteğini incele
- [ ] Küçük bir açık kaynak kod parçasını okuyup not çıkar
- [ ] Stack trace okuyup hatanın kaynağını bul

### Mini Proje

**`bug-hunt.js`**  
İçine bilerek 8–10 bug koyulmuş mini dosya; hepsini tek tek bul ve düzelt.

### Çıkış Kriteri

- [ ] Sorunu random değil sistematik şekilde arıyorsun
- [ ] DevTools sana yabancı değil
- [ ] Stack trace okuyabiliyorsun

---

## Bölüm 13 — Callback, HOF, Closure
**Tahmini Süre: 1 hafta**

### Amaç
Fonksiyonların veri gibi dolaşabildiğini ve closure mantığını oturtmak.

### Öğrenilecekler

- [ ] Callback nedir? — fonksiyonu başka bir fonksiyona argüman olarak verme
- [ ] Higher-order function (HOF) — fonksiyon alan veya döndüren fonksiyon
- [ ] Closure — iç fonksiyon dış fonksiyonun scope'una erişebilir
- [ ] Lexical environment (closure neden çalışır?)
- [ ] Function factory — parametre alıp fonksiyon döndüren yapı
- [ ] Private state simülasyonu (closure ile kapsülleme)
- [ ] Partial application farkındalığı
- [ ] Memoization farkındalığı (closure + cache)
- [ ] Callback hell ve neden Promise'e geçildi

### Ödevler

- [ ] Basit callback API yaz
- [ ] 5 closure örneği üret
- [ ] Function factory ile configurable helper oluştur
- [ ] Memoize fonksiyonu yaz

### Mini Proje

**`validator-factory.js`**  
Kurala göre validator üreten fonksiyonlar.

### Çıkış Kriteri

- [ ] Closure'ı ezber değil mantıkla anlatabiliyorsun
- [ ] HOF kullanımı sana yabancı değil
- [ ] Callback hell'in neden sorun olduğunu açıklayabiliyorsun

---

## Bölüm 14 — Prototype, Class ve OOP
**Tahmini Süre: 1.5 hafta**

### Amaç
JavaScript'in prototip tabanlı doğasını ve class syntax'ının neyi sardığını anlamak.

### Öğrenilecekler

- [ ] Prototype chain — her object'in `__proto__` zinciri var
- [ ] `Object.getPrototypeOf` ile prototype'a erişim
- [ ] Constructor function ile nesne üretme
- [ ] `new` operatörü ne yapar?
- [ ] class syntax (ES6+)
- [ ] constructor
- [ ] Instance methods
- [ ] Static methods ve properties
- [ ] extends ile kalıtım
- [ ] super ile üst sınıfa erişim
- [ ] Private fields (`#` prefix)
- [ ] Encapsulation farkındalığı
- [ ] Composition vs inheritance trade-off
- [ ] OOP her yerde şart mı? — fonksiyonel yaklaşımla karşılaştırma

### Ödevler

- [ ] Constructor function ile class benzeri yapı yaz
- [ ] Aynı problemi inheritance ve composition ile çöz
- [ ] Prototype chain gözlemleyen örnekler kur
- [ ] Private field kullanan bir class yaz

### Mini Proje

**`inventory-model.js`**  
Ürün, dijital ürün, stoklu ürün gibi modeller — class hiyerarşisi ile.

### Çıkış Kriteri

- [ ] class'ın sihir değil syntax sugar olduğunu biliyorsun
- [ ] Kalıtımı gereksiz kullanmıyorsun
- [ ] Composition ne zaman inheritance'tan iyidir açıklayabiliyorsun

---

## Bölüm 14.5 — Modüller, Dosya Organizasyonu ve Kod Düzeni
**Tahmini Süre: 1 hafta**

### Amaç
Kodun büyüdükçe dağılmaması için modüler düşünmeyi öğrenmek.

### Öğrenilecekler

- [ ] import / export
- [ ] Named export / default export (ve farkları)
- [ ] Re-export (`export { x } from './module'`)
- [ ] ESM (ES Modules) mantığı
- [ ] CommonJS vs ESM farkı (`require` vs `import`)
- [ ] Circular import tehlikesi
- [ ] Dosya ve klasör ayırma stratejileri
- [ ] Feature-based vs type-based klasörleme trade-off
- [ ] `utils` klasörü her şeyin çöplüğü olmasın
- [ ] `index.ts` dosyaları ne zaman faydalı, ne zaman karmaşıklaştırır?
- [ ] Küçük config dosyaları (constants, enums)
- [ ] Environment ayrımı farkındalığı (dev / test / prod)

### Ödevler

- [ ] Tek dosyalı projeyi çok dosyaya böl
- [ ] Kötü klasör yapısını düzenle
- [ ] Feature bazlı mini yapı kur

### Mini Proje

**`js-toolkit`**  
`formatters/`, `validators/`, `math/`, `strings/` altına bölünmüş mini araç seti.

### Çıkış Kriteri

- [ ] Kod büyüyünce nasıl düzenleyeceğini daha iyi biliyorsun
- [ ] import/export hatalarını daha hızlı çözebiliyorsun
- [ ] Circular import neden tehlikeli olduğunu anlıyorsun

---

## Bölüm 14.7 — DSA: Algoritma ve Veri Yapıları
**Tahmini Süre: 3–4 hafta**

### Amaç
Teknik mülakatların ve ileri düzey problem çözmenin dili olan DSA'ya gerçek anlamda giriş yapmak. Bu bölümün sonu değil, başlangıcıdır — mülakat sürecine girildiğinde ayrıca çalışılmalıdır.

### Öğrenilecekler

**Karmaşıklık Analizi**
- [ ] Big O notation nedir?
- [ ] O(1) — sabit zaman
- [ ] O(n) — lineer zaman
- [ ] O(n²) — karesel zaman (nested loop tehlikesi)
- [ ] O(log n) — logaritmik zaman (binary search)
- [ ] Space complexity farkındalığı
- [ ] Best / average / worst case farkı

**Temel Veri Yapıları**
- [ ] Array — random access O(1), insert/delete O(n)
- [ ] Stack (LIFO) — JS'de array ile simüle, push/pop
- [ ] Queue (FIFO) — JS'de array ile simüle, push/shift
- [ ] Linked list — node ve next pointer mantığı (JS ile implement)
- [ ] Hash map — JS'de object / Map, O(1) average erişim
- [ ] Set — unique değer koleksiyonu, membership check O(1)
- [ ] Tree farkındalığı (BST, DOM ağacı, dosya sistemi)
- [ ] Graph farkındalığı (sosyal ağ, route planning)

**Temel Algoritmalar**
- [ ] Linear search — O(n)
- [ ] Binary search — O(log n), sadece sıralı dizide
- [ ] Bubble sort — O(n²), neden yavaş
- [ ] Merge sort farkındalığı — O(n log n)
- [ ] Recursion — base case + recursive case
- [ ] Recursion vs iteration trade-off
- [ ] Two pointer tekniği
- [ ] Sliding window tekniği farkındalığı

**Problem Çözme Yaklaşımı**
- [ ] Problemi kendi kelimenle tekrar et
- [ ] Örneklerle düşün (küçük input ile elle çöz)
- [ ] Edge case listesi çıkar
- [ ] Brute force çöz, sonra optimize et
- [ ] Kod yazmadan önce adımları yaz

**Mülakat Hazırlığı**
- [ ] NeetCode Blind 75 listesini tanı (şimdi çözmen şart değil, listeyi gör)
- [ ] Leetcode'da 20 Easy seviye problem çöz
- [ ] Her çözümün zaman ve alan karmaşıklığını söyle
- [ ] Çözümü sesli düşünerek anlat (mock interview alışkanlığı)

### Ödevler

- [ ] Stack ile browser geçmişi simülasyonu yaz
- [ ] Queue ile yazdırma kuyruğu simülasyonu yaz
- [ ] Linked list: add, remove, search implement et
- [ ] Binary search fonksiyonu yaz ve farklı inputlarla test et
- [ ] Recursion ile faktöriyel, fibonacci, dizi toplama yaz
- [ ] Two pointer ile sıralı dizide hedef toplam bul
- [ ] Leetcode Easy: 20 problem çöz

### Mini Proje

**`dsa-playground/`**  
Stack, Queue, LinkedList, binary search, recursion örneklerini barındıran — her yapı için kendi dosyasıyla — mini kütüphane.

### Çıkış Kriteri

- [ ] Big O'yu sezgisel anlayabiliyorsun
- [ ] Stack ve Queue'yu sıfırdan implement edebiliyorsun
- [ ] Recursive fonksiyon yazıp hata ayıklayabiliyorsun
- [ ] Binary search'ü ezberden değil mantıktan yazabiliyorsun
- [ ] Easy Leetcode sorularına yaklaşmak seni felç etmiyor

---

## Faz 1 Köprüsü

### Bu fazda ne öğrendin?
JavaScript'in tüm çekirdeği: değişkenler, tipler, fonksiyonlar, async, OOP, modüller, hata yönetimi, debugging ve temel DSA. Bu faz en uzun fazdır — ve olması gerekiyor.

### Bu faz senden sonra ne açtı?
TypeScript JS üzerine oturur — tip sistemi olmadan anlaşılmaz. NestJS class, decorator ve async bilgisi ister. React closure ve immutability bilgisi ister. DSA mülakatlarda karşına çıkar. Hepsinin temeli burada.

### Geliştiricilerin %80'inin yaptığı hata
- `var` kullanmaya devam etmek
- `async/await` yazıp `try/catch` unutmak
- Her şeyi tek fonksiyona doldurmak, parçalamamak
- Mutation bug'larını anlayamamak ("neden bu obje burada değişti?")
- Test yazmayı "sonraya" bırakmak — sonra hiç gelmiyor
- Leetcode'a bakıp "ben bunu öğrenemem" deyip DSA'yı tamamen atlamak

### Açık kaynak okuma görevi
`lodash` kütüphanesine git (`lodash/lodash`). `chunk`, `groupBy`, `debounce` fonksiyonlarının kaynak kodunu oku. Kendi yazdığın benzer fonksiyonlarla karşılaştır. Profesyoneller edge case'leri nasıl ele alıyor, gör.
