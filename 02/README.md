# Nedelja 2

- tekst, grafovi (mreze, internet), tabelarno, signali, slike/video

- na osnovu tipa podatka imamo razlicite stvari 

- =, != (za ID mogu to da kazem) --- razlicitost (imensi)
	- Primer: ID

- <, <=, >, >= () --- uredjenost (redni) + prethodni
	- Primer: osnovne studije < master studije < doktorske studije

- +, - () --- aditivni (intervalni) + prethodni
	- Primer: 29.02 < 10.03 (mozemo da oduzimamo datume i da ima smisla)

- *, / --- multiplikativni (razmerni) + prethodni
 - Primer: - kada mozemo da kazemo da je nesto duplo vise

- Biljke:
	- X - predstavljaju podaci 
	- Y - predstavljaju podatke koje trebamo predvideti
	- klasifikacija
	- nadgledano ucenje

```
	TEMPERATURA - vrsimo neko predvidjanje tako sto hocemo da predvidimo kakva
	ce temperatura biti u narednom periodu

	- predstavlja neki broj
	- treba da pogodim Y na osnovu podataka iz X
	- predstavlja problem regresije (predvidjamo numericku stvar)
	- nadgledano ucenje
	
	- temperaturu izrazavamo u: C, K, F
	- K(kelvin) - osnovna mera, ima fiksnu nulu i ide u plus 
```

- **klasterovanje** - grupisanje na osnuvu necega = spada u nenadgledano ucenje i tu nemamo tacan odgovor

- podaci: asimetricni, diskretni, kontinualni
```
	Predstavljanje teksta u tabeli:

				boja  i 	pesma 	mama
	rec1	1			0			0				0
	rec2	0			1			1				0
	rec3	0			1			0				1

	- gledamo koliko puta se ponavlja odredjena rec ili slovo u reci/recenici
```

#### Zadatak1

```
	- starost u godinama = diskretni (jer gledamo samo 7 godina, a ne 7.5), razmerni 
	- vreme u AM i PM
	- osvetljenost merena ljudskom procenom = redni, diskretni, kvalitativni 
	- uglovi mereni u stepenima = razmerno, neprekidno. kvalitativan
	- ISBN brojevi knjiga = diskretni, imenski, kvalitativan
	- rang u vojsci = redni, diskretni, kvalitativan
	- broj u garderobi = diskretno, imenski, kvalitativan 
```

#### TF-DF matrice 

- ne zelimo da imamo sum(modifikacija bilo koje vrednosti, nije uvek outlajer)
- elementi van granice (zavisi u kojoj situaciji su oni pozeljni, a u kojoj nisu)

#### IBM SPSS Modeler 