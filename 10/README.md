# Hijerarhijsko klasterovanje

- spaja dva najbliza klastera 
- rastojanje izmedju dva klastera:
    - ili da uzmemo prosecno rastojanje
    - ili da uzmemo od prve instance ili da uzmemo od druge istance 

- najblize - (min = single) 
- najmanje - (max = complete)
- prosecno

- **Dendogram** - graf koji predstavlja hijerarhijsko klasterovanje
    - da idemo na gore efikasnije je, imamo manje kombinacija  ---> O(n^2)
    - ako bismo isli na dole imali bismo vise kombinacija da delimo 2^n ---> 

- trebamo normalizovati podatke jer koristimo rastojanja, kako bi svaki atribut imao jednak doprinos 

- **cildern_** = kako vrsimo hijerarhijsko klasterovanje, redosled kojim spajamo
    - ne mozemo da nacrtamo dendogram na osnovu ovoga, jer nemamo visinu 

- **labels_** = koliko instanci pripada kom klasteru

- **linkage(X)**


- kako da izaberemo koliko klastera hocemo? 
    - 

<href src="https://github.com/odenipinedo/Python/blob/master/datacamp/cluster%20analysis%20in%20Python.ipynb">

# DBSCAN

- gledamo gustinu i racunamo na to da klasteri mogu da imaju sum 

- **epsilon** - predstavlja epsilon okolinu 
- **min_samples**
    - uzmi svaku instancu i pogledaju u njenoj epsilon okolini koliko imas suseda i obelezimo tacku koja je u jezgru naseg klastera
    - da bi bilo na granici treba da bude blizu centra 
    - 