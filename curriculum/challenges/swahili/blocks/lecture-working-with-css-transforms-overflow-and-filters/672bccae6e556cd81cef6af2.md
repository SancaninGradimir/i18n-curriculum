---
id: 672bccae6e556cd81cef6af2
title: Je, Margin Collapsing ni Nini, na Inafanya Kazi Vipi?
challengeType: 19
dashedName: what-is-margin-collapsing
---

# --interactive--

Margin collapsing ni dhana msingi katika CSS ambayo mara nyingi huwatatiza wanaoanza katika ukuzaji wa mtandao.

Ova karakteristika nastaje kada vertikalne ivice susednih elemenata interaguju, stvarajući samo jednu ivicu koja je jednaka najvećoj od dve te ivice.

Kuelewa margin collapsing ni muhimu kwa udhibiti sahihi wa nafasi na mpangilio katika muundo wa mtandao. Hivyo, tuangalie jinsi margin collapsing inavyofanya kazi na kuchunguza baadhi ya hali za kawaida ambapo hutokea.

Katika CSS, wakati kingo mbili za wima zinapokutana, zitagongana, hii inamaanisha badala ya kujumlishwa, kando kubwa ndilo linalotawala na kuamua nafasi kati ya vipengele. Tabia hii inahusu tu kingo za wima (juu na chini) na si za usawa (kushoto na kulia). Hapa kuna mfano wa kuelezea dhana hii:

:::interactive_editor

```html
<style>
  .box1 {
    margin-bottom: 20px;
    background-color: lightblue;
  }
  .box2 {
    margin-top: 30px;
    background-color: lightgreen;
  }
</style>

<div class="box1">Box 1</div>
<div class="box2">Box 2</div>
```

:::

U ovom primeru, možete pretpostaviti da je ukupni prostor između `.box1` i `.box2` od 50 piksela (20 piksela plus 30). Međutim, zbog kolaps margina, stvarni prostor će biti od 30 piksela, što je veći razmak između ta dva.

Kama tulivyoona katika mfano uliopita, kingo za vipengele vinavyopakana zitagongana. Hii ni kesi rahisi kabisa ya margin collapsing. Tuchunguze zaidi hali ambapo margin collapsing inaweza kutokea.

Kingo pia zinaweza kugongana kati ya kipengele mzazi na mtoto wake wa kwanza au wa mwisho. Ikiwa hakuna mpaka, nafasi ya ndani, maudhui ndani ya mstari, au utulivu wa kuwatenganisha kingo za mzazi na mtoto, zitagongana.

:::interactive_editor

```html
<style>
  .parent {
    margin-top: 40px;
    background-color: lightyellow;
  }
  .child {
    margin-top: 30px;
    background-color: lightpink;
  }
</style>

<div class="parent">
  <div class="child">Child element</div>
</div>
```

:::

U ovom slučaju, možete pretpostaviti da dete ima prostor od 70 piksela odozgo (pikseli 40 plus 30). Međutim, ivice se sudaraju sa većom stranom od 40 piksela, i ona je korišćena.

Kama kipengele hakina maudhui, nafasi ya ndani, au mpaka, kingo zake za juu na chini zinaweza kugongana na kuwa kando moja.

:::interactive_editor

```html
<style>
  .empty-block {
    margin-top: 20px;
    margin-bottom: 10px;
    height: 0;
  }
  .next-block {
    background-color: lightgray;
  }
</style>

<div class="empty-block"></div>
<div class="next-block">Next block</div>
```

:::

Katika mfano huu, kingo za juu na chini za `empty-block` zinagongana na kuwa kando moja ya pikseli 20, kubwa zaidi kati ya hizo mbili.

Hapa kuna mfano wa kuzuia mgongano kwa kutumia nafasi ya ndani:

:::interactive_editor

```html
<style>
  .parent {
    margin-top: 40px;
    padding-top: 1px;
    background-color: lightyellow;
  }
  .child {
    margin-top: 30px;
    background-color: lightpink;
  }
</style>

<div class="parent">
  <div class="child">Child element</div>
</div>
```

:::

U ovom slučaju, unutrašnji prostor jednog piksela na roditelju sprečava koliziju ivica i stvara ukupni prostor od 71 piksela od vrha roditelja do vrha sadržaja deteta.

Razumeti kolaps margina je važno za pravilnu kontrolu rasporeda i razmaka u CSS. Iako ponekad može izazvati nepredvidive rezultate, radi se o karakteristici dizajniranoj da pruži bolji i stabilniji razmak u dokumentu. Znanjem kada se dešava kolaps margina i kako ga sprečiti kada je potrebno, možete kreirati očekivane i lako održive postavke u vašim web dizajnovima.

# --questions--

## --text--

U kom pravcu se događa kolizija sa obalom?

## --answers--

Samo granice jednakosti.

### --feedback--

Zamislite koje ivice (gore, dole, levo, desno) su pogođene ovim svojstvom.

---

Samo vertikalne ivice.

---

Profile za sve horizontalne i vertikalne rubove.

### --feedback--

Zamislite koje ivice (gore, dole, levo, desno) su utječene ovim svojstvom.

---

Obrici za elevaciju.

### --feedback--

Razmisli koje ivice (gore, dole, levo, desno) su pogođene ovom karakteristikom.

## --video-solution--

2

## --text--

Šta se dešava kada su dva susedna elementa različitih ivičnih vrednosti?

## --answers--

Kingo se generalizuje.

### --feedback--

Razmisli o kojoj je strani "pobedi" kada dođe do kolizije.

---

Mala strana se koristi.

### --feedback--

Zamislite koju stranu „pobedi“ kada dođe do sukoba.

---

Koristi se velika strana.

---

Koristi se prosek obe ivice.

### --feedback--

Zamisli koju stranu koja "pobedi" kada dođe do sudara/sukoba.

## --video-solution--

3

## --text--

Koje od sledećih NE SPREČAVA sudar uglom između roditelja i njihove prve dece?

## --answers--

Dodavanje `border` roditelju.

### --feedback--

Razmislite koji su faktori koji čine razdvajanje između roditelja i deteta.

---

Postaviti `padding-top: 1px;` za roditelja.

### --feedback--

Razmislite o kriterijumima koji određuju razmak između roditeljskog i detinjeg obala.

---

Koristi `display: inline-block;` za dete.

### --feedback--

Razmislite koji su kriterijumi koji formiraju razdvajanje između granica roditelja i deteta.

---

Da stavi `margin-top: 0;` za dete.

## --video-solution--

4