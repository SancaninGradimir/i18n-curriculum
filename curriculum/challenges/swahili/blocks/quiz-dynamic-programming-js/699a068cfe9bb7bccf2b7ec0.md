---
id: 699a068cfe9bb7bccf2b7ec0
title: Test iz dinamičkog programiranja
challengeType: 8
dashedName: quiz-dynamic-programming-js
---

# --description--
Da biste položili kviz, morate tačno odgovoriti na najmanje 9 od 10 pitanja ispod.
# --quizzes--

## --quiz--

### --question--

#### --text--
Koje su dve ključne osobine koje moraju biti prisutne u problemu da bi dinamičko programiranje bilo efikasan pristup rešavanju?
#### --distractors--
Brzo vreme izvršavanja i minimalna potrošnja memorije

---

Rekurzivna sposobnost i iterativne petlje

---

Sekvencijalna obrada i paralelno računanje
#### --answer--
Preklapajući podproblemi i optimalna podstruktura
### --question--

#### --text--
Koja je glavna razlika između pristupa memoizaciji i tabulaciji u dinamičkom programiranju?
#### --distractors--
Memoizacija koristi hash tabele, dok tabulacija koristi nizove, što je efikasnije.

---

Memoizacija je brža, ali koristi više memorije i CPU ciklusa od tabulacije.

---

Memoizacija može da reši samo jednostavnije probleme od tabulacije.
#### --answer--
Memoizacija je pristup odozgo prema dole koji koristi rekurziju, dok tabulacija predstavlja pristup od dole ka gore koji koristi iteraciju.
### --question--

#### --text--
Zašto naivni rekursivni rešenja za probleme dinamičkog programiranja tipično imaju eksponencijalnu vremensku složenost?
#### --distractors--
Zato što koriste eksponencijalno mnogo memorijskog prostora za skladištenje varijabli.

---

Zato što zahtevaju sortiranje podataka u eksponencijalnom vremenu.

---

Zato što moraju da provere sve moguće permutacije unosa.
#### --answer--
Zato što svaki rekurzivni poziv se razdvaja na više granki, što uzrokuje ponovno izračunavanje istih podproblema.
### --question--

#### --text--
Šta znači optimalna podstruktura u kontekstu dinamičkog programiranja?
#### --distractors--
Algoritam mora da koristi najefikasniju dostupnu strukturu podataka.

---

Rešenje mora da minimizira i vremensku i prostornu kompleksnost istovremeno.

---

Problem mora imati jedinstveno i optimalno rešenje.
#### --answer--
Optimalno rešenje se može konstruisati iz optimalnih rešenja njegovih podproblema.
### --question--

#### --text--
Prilikom implementacije memoizacije, šta se dešava kada se funkcija pozove sa argumentima koji su već izračunati?
#### --distractors--
Funkcija ponovo izračunava rezultat kako bi osigurala tačnost.

---

Funkcija prosekuje stare i nove rezultate radi bolje preciznosti.

---

Greška je izbačena jer nisu dozvoljene duplikovane kalkulacije.
#### --answer--
Keširani rezultat se vraća odmah bez ponovnog izračunavanja.
### --question--

#### --text--
Koja je ključna prednost korišćenja tabulacije umesto memoizacije?
#### --distractors--
Tabulacija uvek zahteva manje memorije nego memoizacija.

---

Tabulacija može da razreši širi spektar problema.

---

Tabulisiranje je uvek lakše za implementaciju i razumevanje.
#### --answer--
Tabulacija izbegava režijski trošak rekurzije i pruža predvidljivo sekvencijalno izvršavanje.
### --question--

#### --text--
U rešenju dinamičkog programiranja od dna ka vrhu, zašto se osnovni slučajevi inicijalizuju prvi?
#### --distractors--
Za efikasnu alokaciju memorije za strukturu podataka.

---

Za sprečavanje beskonačnih petlji u algoritmu.

---

Radi poboljšanja vremenske složenosti algoritma.
#### --answer--
Pružiti osnovne vrednosti na kojima su izgrađeni svi veći podproblemi.
### --question--

#### --text--
Kako dinamičko programiranje transformiše vremensku složenost problema koji pokazuju preklapajuće podprobleme?
#### --distractors--
Od polinomialne do logaritamske složenosti efikasnom podelom problema.

---

Od kvadratične do linearne složenosti optimizacijom struktura petlji.

---

Smanjenje složenosti vremena sa linearnog na konstantno pomoću hash tabela.
#### --answer--
Od eksponencijalnog do polinomialnog, skladištanjem i ponovnim korišćenjem rešenja podproblema.
### --question--

#### --text--
Koji kompromis dinamičko programiranje obično pravi kako bi postiglo bolju složenost vremena?
#### --distractors--
Žrtvuje čitljivost koda radi bržeg izvršavanja.

---

Zahteva kompleksnije algoritme koje je teže održavati.

---

Ograničava veličinu problema koje je moguće rešiti.
#### --answer--
Koristi dodatni prostor za skladištenje međurezultata.
### --question--

#### --text--
U kojem scenariju dinamičko programiranje NEBIJE odgovarajući algoritamski pristup?
#### --distractors--
Kada problem zahteva pronalaženje optimalnog rešenja.

---

Kada se problem može razložiti na manje podprobleme.

---

Kada je potrebno minimalizovati složenost prostora.
#### --answer--
Kada su podproblemi nezavisni i ne preklapaju se.