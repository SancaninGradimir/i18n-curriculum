---
id: 67d301cc87b84eaa42bdcdbe
title: Šta je `tsconfig` fajl i zašto je važno da ga uključite u svoje TypeScript projekte?
challengeType: 19
dashedName: what-is-a-tsconfig-file-and-why-is-it-important-to-include-in-your-typescript-projects
---

# --description--

Podešavanja kompajlera TypeScript-a mogu se konfigurisati da odgovore potrebama vašeg projekta. Ta konfiguracija se nalazi u fajlu `tsconfig.json` u korenom direktorijumu vašeg projekta. Zapravo, bez njega, kompajler neće raditi osim ako mu direktno ne prosledite komandne zastavice (flags). Ali šta tačno radi ovaj fajl? Pa, hajde da pogledamo primer fajla:

```json
{
  "compilerOptions": {
    "rootDir": "./src",
    "outDir": "./prod",
    "lib": ["ES2023"],
    "target": "ES2023",
    "module": "ES2022",
    "moduleResolution": "Node",
    "esModuleInterop": true,
    "skipLibCheck": true,
    "strict": true
  },
  "exclude": ["test/"]
}
```

Ovo izgleda kao mnogo! Dakle, hajde da to rastavimo. Svojstvo ``compilerOptions`` će sadržati "srž" vaše konfiguracije – ovde kontrolišete kako se ponaša kompajler TypeScript-a. Gledajući taj ugnježdeni objekat…

`rootDir` i `outDir` govore TypeScriptu koji direktorijum sadrži vaše izvorni fajlove, i koji direktorijum bi trebalo da sadrži transpilovani JavaScript kod.

Atribut ``lib`` određuje koje definicije tipova kompajler koristi, i omogućava vam da uključite podršku za specifične ES verzije, DOM i više.

`module` i `moduleResolution` efikasno rade u sinergiji da upravljaju načinom na koji vaš paket koristi module - bilo CommonJS ili ECMAScript.

`esModuleInterop` omogućava glatku interoperabilnost između CommonJS i ES modula automatskim kreiranjem objekata prostora imena za uvoz, što olakšava korišćenje modula iz različitih sistema zajedno u vašim TypeScript projektima, a `skipLibCheck` opcija preskače validaciju `.d.ts` fajlova koji nisu referencirani uvozima u vašem kodu.

I na kraju dolazimo do `strict` režima. Neki bi mogli da argumentuju da TypeScript nije zaista koristan bez omogućenog ovog zastavice, jer uključuje prilično mnogo drugih provera, kao što je zahtev pravilnu obradu nullabilnih tipova, ili upozorava kada TypeScript ne može da izvede tip i vraća se na bilo koji.

Pre nego što završimo, kratka napomena o top-level svojstvu ``exclude`` - kada definišete direktorijum izvora, možda imate TypeScript kod van tog direktorijuma koji ne želite da se kompajlira kao deo vašeg produkcionog koda. Na primer, vaš test kod. Niz ``exclude`` govori kompajleru da ignoriše ove TypeScript fajlove tokom kompilacije, ali i dalje omogućava alatima kao što je Intellisense da otkriju potencijalne probleme.

Postoji mnogo drugih opcija kompajlera koje možete istražiti – preko 50! Podstičem vas da istražite dokumentaciju i eksperimentišete kako biste pronašli konfiguraciju koja odgovara potrebama vašeg projekta.
# --questions--

## --text--

Koje svojstvo u fajlu ``tsconfig.json`` utiče na ponašanje kompajlera?
## --answers--

`rootDir`

### --feedback--

Ovo svojstvo je objekat koji sadrži opcije za kompajler.
---

`compilerOptions`

---

`exclude`

### --feedback--

Ovo svojstvo je objekat koji sadrži opcije za kompajler.
---

`lib`

### --feedback--

Ovo svojstvo je objekat koji sadrži opcije za kompajler.
## --video-solution--

2

## --text--

Šta radi opcija ``strict`` u fajlu ``tsconfig.json``?
## --answers--

Proverava samo nullabilne tipove.
### --feedback--

Ova opcija omogućava različite provere, uključujući rukovanje nulabilnim tipovima.
---

It enforces the use of CommonJS modules.

### --feedback--

Ova opcija omogućava različite provere, uključujući rukovanje nulabilnim tipovima.
---

It toggles several type-checking options.

---

It excludes test files from compilation.

### --feedback--

Ova opcija omogućava različite provere, uključujući rukovanje nulabilnim tipovima.
## --video-solution--

3

## --text--

Koja je svrha niza ``exclude`` u fajlu ``tsconfig.json``?
## --answers--

Da se navedu fajlovi koje treba kompajlirati.
### --feedback--

Možete ovo koristiti da biste isključili test kod iz kompilacije.
---

To list additional libraries to include.

### --feedback--

Možete ovo koristiti da biste isključili test kod iz kompilacije.
---

To ignore certain files during compilation.

---

To define output directories for compiled files.

### --feedback--

Možete ovo koristiti da biste isključili test kod iz kompilacije.
## --video-solution--

3
