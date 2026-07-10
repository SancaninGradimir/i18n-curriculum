---
id: 67d78c94b686ce3bddcaf8ab
title: Vežba 117
challengeType: 22
dashedName: task-117
lang: en-US
---

<!-- (Audio) Brian: It could save us time and resources. What about timelines? Which option is faster? -->

# --instructions--

Slušajte audio i dovršite sledeću rečenicu.

# --fillInTheBlank--

## --sentence--

`It could BLANK and resources. What about BLANK? Which option is faster?`

## --blanks--

`save us time`

### --feedback--

Maneno haya matatu pamoja yanamaanisha kupunguza muda unaohitajika kumaliza zoezi.

---

`timelines`

### --feedback--

Neno hili kwa wingi linahusu ratiba au tarehe za mwisho za kumaliza mradi.

# --explanation--

`Save us time` znači smanjiti vreme potrebno za završetak nečega i učiniti proces efikasnijim. Na primer:

`Using automation tools can save us time on repetitive tasks.` – Hii inamaanisha zana za automatisering husaidia kumaliza kazi kwa haraka zaidi.

`Timelines` zinahusu ratiba au tarehe za mwisho zinazoonyesha lini sehemu tofauti za mradi zinapaswa kumalizika. Kwa mfano:

`We need to adjust our timelines to finish the project on schedule.` – Hii inamaanisha kubadilisha tarehe za mwisho ili kuhakikisha mradi unamalizika kwa wakati. 

# --scene--

```json
{
  "setup": {
    "background": "company2-center.png",
    "characters": [
      {
        "character": "Brian",
        "position": {
          "x": 50,
          "y": 15,
          "z": 1.2
        },
        "opacity": 0
      }
    ],
    "audio": {
      "filename": "B1_13-3.mp3",
      "startTime": 1,
      "startTimestamp": 32.34,
      "finishTimestamp": 37.52
    }
  },
  "commands": [
    {
      "character": "Brian",
      "opacity": 1,
      "startTime": 0
    },
    {
      "character": "Brian",
      "startTime": 1,
      "finishTime": 6.18,
      "dialogue": {
        "text": "It could save us time and resources. What about timelines? Which option is faster?",
        "align": "center"
      }
    },
    {
      "character": "Brian",
      "opacity": 0,
      "startTime": 6.68
    }
  ]
}
```
