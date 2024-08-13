# BACKPROPAGATION BASED RL NETWORK

allora, 
scrivo in italiano che è meglio.

questa è l'idea: abbiamo un certo agente che deve interagire con l'enviroment e compiere delle azioni. Ma non esistono delle "azioni corrette", 
bensì solo degli "stati positivi" e "stati negativi". Dunque quando un agente riesce a raggiungere degli "stati positivi" gli possiamo concedere
un "reward" e quando invece raggiunge degli "stati negativi" gli possiamo dare una "penalities" (che equivale ad un reward negativo). Il nostro 
agente è (sotto il cofano) guidato da una certe rete neurale (di cui possiamo studiare e pensare la struttura, ma non è strettamente ciò di cui 
ci occupiamo oggi) che non ha però una "funzione obiettivo". Come mai? Semplice: se avessimo una funzione obiettivo non sarebbe RL (non è del tutto
vero ma era più per il meme). Oltre agli scherzi, il motivo è che se avessimo a priori la funzione obiettivo a cui vogliamo puntare sarebbe 
sufficiente usare quella e la nostra rete neurale saprebbe fare tutto, ed invece non è così; tuttavia man mano che l'agente si sposta questo
colleziona "reward" e "penalities". E da qui nasce l'idea: cos'è una funzione? Beh una funzione è qualcosa che mappa una certa X ad una certa Y,
dunque la scelta che l'agente compie (Y) basandosi sui suoi input (X) definisce una certa funzione (in un unico punto è vero, però noi quello che
facciamo è di fatto costruire la funzione corretta proprio "punto per punto"). Dunque costruiamo una struttura che, presa l'azione compiuta dall'agente, 
il reward che l'azione ha portato e l'output della rete neurale := F (che poiché usiamo una sigmoide sull'ultimo livello è definibile come una "funzione 
di probabilità") andiamo a costruire una versione della F che va più o meno a premiare (in base al reward positivo o negativo raccolto) l'azione compiuta.
E dunque man mano, passo dopo passo, possiamo "overfittare" le azioni corrette, esplorare il resto dell'enviroment ed allontanarci dalle cattive scelte.

Nei notebook sono presenti più cose. E' tutto ben documentato nei notebook ed in caso fosse utile lavorerò a migliorare la qualità della spiegazione.

