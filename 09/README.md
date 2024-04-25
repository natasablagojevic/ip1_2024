# KMeans 

- SSE = sum_i(sum_j(d(i, center)^2))

- funkcija koja pravi KS 
    - opadajuca je i na kraju je jednaka nuli 
    - inercija = 0 
    - ocekivali smo da stalno opada 
    - da li mozemo da izaberemo K, ali tako sto znamo da ce uvek da opada ==> NE!
        - sta nam se vise isplati? --> sa 2 na 3 jer se tu SSE mnogo smanjilo 
    - izaberemo K tako da nasa funkcija formira lakat ==> u nasem slucaju idelano je mozda K=3
        - pravilo lakta
    
- metrika koja ce da nam izabere najbolje klasterovanje
    - mera kvaliteta: SILHOUETTE_SCORE (senke)
    - SILUETA(i) = (b-a) / max(a, b)
        - a - prosecno rastojanje od istance i do svih ostalih instanci u klasteru 
        - b - koji joj je najblizi koji nije b, i uzmi prosek 
        - svakoj istanci su u proseku blize istance iz njenog klastera 
        - a = 0 ==> SILUETA ~ 1 (sto je ovo blize jedinici to je bolje) 
        - a = b ==> SILUETA ~ 0 (sto je ovo blize nuli to je gore)
        - instance unutar klastera su blizu, instance izmedju klastera su daleko    
        - b = 0 ==> SILUETA = -1 (cim vidimo da je nesto negativno, vidimo da nesto ne valja)

- gde postavljamo centroide
    - bolje je da ih stavimo daleko, nego da ih stavimo jedne pored drugih
    - brze cemo iskonvergirati, ako inicijalno izaberemo sto dalje centroide 
    - 