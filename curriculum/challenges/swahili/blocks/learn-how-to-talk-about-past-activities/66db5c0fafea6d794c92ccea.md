---
id: 66db5c0fafea6d794c92ccea
title: Vežba 58
challengeType: 19
dashedName: task-58
lang: en-US
---
<!--
AUDIO REFERENCE:
Linda: Da. Prilagođavanja navigacione trake i podnožja već su napravila veliku razliku.
-->

# --instructions--

Slušajte audio odgovor na pitanje ispod.

# --questions--

## --text--

Kako funkcionišu ažurirane karakteristike?

## --answers--

Havifanyi kazi ipasavyo kwenye vifaa vyote, na hii imeleta tofauti kubwa.

### --feedback--

Linda nije spomenula nikakve probleme u vezi tih korekcija.

---

Potrebno mu je više prilagođavanja da bi funkcionisao kako treba, a ovo nije napravilo nikakvu razliku.

### --feedback--

Linda hakutaja haja ya marekebisho zaidi.

---

Stvaraju nove probleme na korisničkom interfejsu, i ovo je donelo veliku razliku.

### --feedback--

Linda hakusema kuwa marekebisho yalisababisha matatizo mapya.

---

Vinafanya kazi vizuri na marekebisho yameleta tofauti kubwa.

## --video-solution--

4

# --explanation--

Ili kujua kama kitu kinafanya kazi vizuri, tafuta maneno au misemo inayoonyesha matokeo mazuri au maboresho.

Linda anatumia usemi `have already made a big difference`.

`Made a big difference` inaashiria mabadiliko muhimu au yanayoonekana. Wakati kitu kina `made a big difference` katika muktadha mzuri, kawaida ina maana kuwa mabadiliko hayo ni ya msaada au yenye ufanisi.

Dakle, odgovor Linde pokazuje da ažurirani elementi dobro funkcionišu i poboljšali su stanje.

# --scene--

```json
{
  "setup": {
    "background": "company2-center.png",
    "characters": [
      {
        "character": "Linda",
        "position": {
          "x": 50,
          "y": 0,
          "z": 1.4
        },
        "opacity": 0
      }
    ],
    "audio": {
      "filename": "B1_3-2.mp3",
      "startTime": 1,
      "startTimestamp": 15.66,
      "finishTimestamp": 19.46
    }
  },
  "commands": [
    {
      "character": "Linda",
      "opacity": 1,
      "startTime": 0
    },
    {
      "character": "Linda",
      "startTime": 1,
      "finishTime": 3.16,
      "dialogue": {
        "text": "Yes, the navigation bar and footer adjustments",
        "align": "center"
      }
    },
    {
      "character": "Linda",
      "startTime": 3.16,
      "finishTime": 4.6,
      "dialogue": {
        "text": "have already made a big difference,",
        "align": "center"
      }
    },
    {
      "character": "Linda",
      "opacity": 0,
      "startTime": 5.1
    }
  ]
}
```
