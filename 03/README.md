# Nedelja 3

#### Mere bliskosti i razlicitosti 

- neki atribut koji nije numericki (kategoricki)
  - merimo rastojanje izmedju npr. dva imena : Pera i Maja 
  - kategoricki i redni 
  - osnovne < master < doktorske (mozemo da pridruzimo nivoe i da vidimo kolika je bliskost)

  - Euklitsko rastojanje, Menhetn rastojanje, Rastojanje Minkoskog
  - Hamingovo rastojanje = brojanje razlika samo
  - Zakardov koeficijent = drugo 

```

duzina | sirina
----------------
   7   |   4000
   9   |   5000 
       |
       |
       |


```

#### Standardizacija 
- za neki atribut X, mogu da izracunam njegovu medijanu i standardnu devijaciju 

```
      X - mi
Z = ----------
      sigma^2

mi_Z = 0
sigma_Z = 1

```


#### Normalizacija

- hocu da dovedem X na segment [0, 1]

```
      X - min
Z = ------------
      max - min 

```

- autlajeri 


- ako imamo binarne atribute:
  - radimo **BINARIZACIJU** 
  
```
npr. imamo atribut boja:

crvena  plava  zelena 
  1       0      0
  0       1      0
  0       0      1

```


|crvena | plava | zelena|
|------ |-------|-------|
|  1    |   0   |    0  |
|  0    |   1   |    0  |
|  0    |   0   |    1  |


- koliko su dva organizma slicna:
  - odsustvo nekog gena 


```
0 | 0 | 1 | 1 | 0   <- covek 1
0 | 1 | 0 | 1 | 0   <- covek 2

```
  - kako poredimo dva coveka
    - bitne su nam razlike


<br>


- SMC 
  - $3/5$
  - $2/5$ 

- Zakardov koeficijent 
  - retki - retke reci koje ce se javljati skoro nigde (javlja ce se u nekom dokumentu)
    - postoje dosta reci na osnovu kojih su razliciti, a postoji neka rec po kojoj su slicni

##### Zadatak 1

- azijski slonovi: tezina, visina, 

##### Zadatak 3

- da transformisemo iz mere slicnosti [0, 1] na meru razlicitosti [0, inf) => -log (0, +inf)


#### BINARIZACIJA 
- Transformacija atributa u jedan ili vise binarnih atributa

#### DISKRETIZACIJA
- transformacija neprekidnog atributa u kategoricki atribut

```
         / mala
velicina - srednja
         \ velika 


|-----|----------|-----|

```

- ako imamo veliki broj jednih ucionica npr. malih 

- hocemo da svaka kategorija sadrzi jednak broj instanci 

# KLASIFIKACIJA

- stvrstavanje instance u neku kategoriju odnosno klasu 


```
        X           Y
|----------------|----|
|                |    |
|                |    |
|                |    |

```

- obucavamo model da moze da predvidi kojoj klasi neki slog pripada kojoj klasi 

- imamo novu instancu o kojo ne znamo nista, i na osnovu nje zelim da predvidim kojoj klasi ce da pripada
- na osnovu podataka iz X hocu da naucim neke principe po kojoj cu klasifikovati svaku novu narednu instancu 
- kako da procenim da mi je model dobar?
    - ako je tacan odgovor +1, ako je netacan odgovor onda nista, pa saberem te vrednosti => **accuracy = (broj_tacno_predvidjenih)/(ukupan_broj_instanci)**
    

- podatke **X** i **Y** delimo na dva dela: **TRENING** i **TEST**
    - **TRENING** - na osnovu koga se pravi model
        - podesavamo model
    - **TEST** - podaci na osnovu koga testiram model da li je dobar, da li dobro generalizuje odnosno da li dobro radi sa podacima koje nikada nije video
        - gledamo koliko dobro model radi 


## DRVETA ODLUCIVANJA 
- donosimo odluku na osnovu vrednosti nekih atributa 

```
              age < 30 
        / yes           \ no

    eat pizza?            exercises 

   / yes     \ no       / yes    \ no

UNFIT         FIT      FIT        UNFIT

```

- na osnovu kog atributa cu ici kroz stablo nam govori **MERA NECISTOCE**
  - mere koje mere necistocu:
    - Ginijev indeks
    - Entropija 
    - Greska klasifikacije

  - **cista** = koja je raspodela klasa na osnovu podskupa kog gledamo 
    - najgora opcija je da ako imam klase sa 50-50% i ne treba tako da ih pravim
    - hocu da pravim cvorove tako da dobijam cistu stvar 
    - jedna instanca je ucek cista

- hocu da na donosenju odluke budem 100% siguran 

- acc na trening skupu je 1 ; 
  - nikad ne zelim da stignem do ovoga, jer ce uciti napamet 

- hocu da nadjem pravilo ili pravila koja vaze generalno
  
- meni cilj nije trening skup, vec test skup jer on treba da generalizuje stvari 
