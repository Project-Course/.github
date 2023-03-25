# Propagazione di fake news in social network

## Proposta project course

Le reti sociali sono strumenti pervasivi e utilizzati quotidianamente da miliardi di persone per interagire e scambiarsi informazioni. Come testimoniato da recenti eventi politici e sociali quali le elezioni americane del 2020, il ruolo delle fake news può essere determinante per polarizzare l’opinione pubblica ed influenzare l’opinione di intere comunità.

In questa tesi, lo/la studente implementerà e simulerà strategie per la diffusione di fake news in reti sociali descritte da dataset reali, e ricercherà le policy che portano al maggior tasso di “infezione” degli utenti. La tesi risponderà a domande quali

- Esistono utenti particolarmente “centrali” che devono essere attaccati prioritariamente perché aiutino la diffusione dell’infezione?
- Quanti utenti di tipo “bot” è necessario attivare, e come dovrebbero tali bot gestire la diffusione di fake news?
- Quali risultati si ottengono in reti sociali reali e simulate usando le policy sviluppate? Ci sono differenze sostanziali?

Possibile combinazione con research project o project course.

Composizione: 20% teoria - 50% sviluppo - 30% test

## Mail prof

Partendo da una mail di Francesco di qualche settimana fa (grazie!), alleghiamo un po' di materiale da leggere:

- [Paper di base](https://citeseerx.ist.psu.edu/document?repid=rep1&type=pdf&doi=beca05e54359339fe4eb03d231689aa6884534a8) da cui siamo partiti;
- [Paper nostro](https://www.mdpi.com/1999-5903/13/3/76) su modelli per simulare diffusione di fake news;
- [Codice GitHub](https://github.com/FraLotito/fakenews_simulator) del nostro simulatore (è un po’ più complicato di quello che serve a noi, ha anche una inutile al momento interfaccia grafica, quindi ti consiglio di implementarne uno da te, è molto semplice);
- [Qui](https://docs.google.com/document/d/1F7NS0BLR6AIVw97Ef6JwZF7SUcpo_KMXTiXYeWu4IIQ/edit?usp=sharing) ci sono delle note  e appunti su alcune idee che abbiamo avuto con altri colleghi in passato.

Ci sono anche dei paper interessanti collegati al topic, divisi per argomenti. Potrebbe essere uscito qualcosa di nuovo, nel dubbio consiglierei una breve ricerca online. Le parole chiave sono “influence maximization” (che è il framework algoritmico in cui ci poniamo, ovvero dato un grafo, scelgo il set di nodi che massimizza un processo, tipo un’epidemia). Oltre a influence maximization, a noi interessa l’aspetto temporale. Quindi andrei a vedere cosa si è detto nel campo di influence maximization su temporal networks. [Questo](https://arxiv.org/pdf/2010.09614.pdf) è un bel paper. Nota: non è detto che fare una “classifica” dei nodi secondo qualche criterio di importanza, e poi prendere i top-k nodi, sia il risultato migliore.

Esistono strade diverse: questi ([1](https://arxiv.org/pdf/2204.06250.pdf) e [2](https://www.sciencedirect.com/science/article/pii/S2665963821000415)) sono per esempio due lavori che conosco del prof. Iacca qui ad unitn, qui usano approcci evolutivi per trovare il set di nodi target.Oltre agli appunti e i paper, nel documento ci sono dei dataset di reti reali temporali. Quindi ci sono varie righe in ogni dataset, ogni riga sarà del tipo “Nodo A ha comunicato con Nodo B al tempo T”.
