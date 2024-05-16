# Pravila pridruzivanja 

- Veza izmedju atributa
- Prodavnica i atributi su nam proizvodi koje ljudi kupuju
    - Ako je neko kupio nesto, onda ce kupiti i nesto drugo
 
- Podrska: frekvencija/broj_skupap
- X < Y ==> sup(X) >= sup(Y) **antimonotonost**
  - jednako je kada : kad god imam maline javljaju se i jabuke
 
- minsup < X onda je on cest
- hocemo i da support i da confidence budu sto veca, odnosno sto bliza 1
  - sup in [0,1]
  - conf in [0,1]

# APRIORI ALGORITAM 

- ako je skup cest onda je i njegov podskup cest

# MERE KVALITETA PRAVILA PRIDRUZIVANJA

- Lift = conf(X -> Y) / sup(Y) = 1
  - Lift in [0, inf]
  - hocemo da bude sto veci
  - ako dobijemo da je malo, znamo da ko je uzeo jabuke nece uzeti maline
  - Lift = 1 nam je beskorisno, jer nisu dovoljno znacajne; kada dobijemo da je Lift = 1 to pravilo odbacujemo

- Lift = conf_posterier / conf_aprior
  - conf_posterior = zapravo pouzdanost conf(X -> Y) - sup(Y)
  - conf_aprior = conf(0 -> Y)
     - 0 je prazan skup
  - 
