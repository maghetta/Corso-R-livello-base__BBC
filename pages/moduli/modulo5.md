---
title: Modulo 5
---

![modulo5](/images/modulo5/modulo5.jpg)

<br>

## Argomenti di oggi

- Il progetto Bioconductor

- espressione genica e microarrays

- tutorial su Bioconducto

<br>
<br>

## Obiettivi conoscitivi di oggi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è il progetto Bioconductor

- trovare in rete e installare sul tuo PC un pacchetto R/Bioconductor

- caricare in una sessione di lavoro un pacchetto R/Bioconductor

- trovare la documentazione di uso per un pacchetto R/Bioconductor di interesse

- seguire le istruzioni fornite in un tutorial (codice commentato, con domande ed esercizi)

- descrivere cos'è una heatmap

<br>
<br>

## Programma dell'attività di oggi

durata: 6 ore; modalità: presenza

<table border="1" width="700">
	<tr>
		<td>8:30-9:30</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
		<td>9:30-10:20</td>
		<td>Sfide interattive su www.menti.com</td>
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>10:30-11:00</td>
		<td>Il progetto Bioconductor</td>		
	</tr>
	<tr>
		<td>11:00-11:20</td>
		<td>Inizio svolgimento tutorial su Bioconductor</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>11:30-12:00</td>
		<td>Fine svolgimento tutorial su Bioconductor</td>		
	</tr>
	<tr>
	<td colspan="2">pausa pranzo 50'</td>
	</tr>
	<tr>
		<td>12:50-14:00</td>
		<td>Svolgimento e invio prodotto di lavoro richiesto</td>		
	</tr>
	<tr>
		<td>14:00-14:20</td>
		<td>Sfide interattive</td>		
	</tr>
	<tr>
		<td>14:20-14:30</td>
		<td>Conclusioni e saluti: questo era l'ultimo dei 5 appuntamenti di questo percorso di PCTO: com'è andata?</td>		
	</tr>
</table>


## Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

1. **Abbiamo conosciuto il quinto ed ultimo tipo di "oggetto" di R: la lista**

![r_liste](/images/modulo5/r_liste.png)

2. **Abbiamo imparato come chiedere aiuto se abbiamo dubbi sul codice, in R o in rete**

![cmd](/images/modulo5/cmd.png)

ad esempio dalla console di R, con il simbolo ? seguito dal nome della funzione per cui vogliamo vedere la documentazione

![firefox](/images/modulo5/firefox.png)


Oppure direttamente ad un motore di ricerca, per sapere come fare una certa cosa in R. Approfittando dei tanti utenti R e dei tanti forum con argomenti e problemi di ogni tipo già affrontati e risolti, e documentati in rete.

<br>

3. **Abbiamo visto come installare e caricare nella propria sessione di lavoro un pacchetto R**

![cmd](/images/modulo5/cmd2.png)

installo un pacchetto, dei tanti disponibili nel repository di R, una sola volta sul mio PC con la funzione **install.packages()**

![cmd](/images/modulo5/cmd3.png)

Ogni volta che voglio utilizzare funzioni da un dato pacchetto, carico quel pacchetto nella mia sessione di lavoro R con la funzione *library()*

4. **Qua e la tra i capitoli abbiamo anche conosciuto**

- diversi altri esempi di funzioni disponibili in R, quali: *list(), names(), sessionInfo()* 

- un altro dei tanti dataset di esempio (in particolare, USArrests) già pronti da caricare nello spazio di lavoro di R per esercitarsi

- abbiamo visto l'importanza delle parentesi: \[], \[[]], () ... a proposito, sapresti dire ciascuno di questi tipi di parentesi quando si usa?

<br>

<hr>

## Il progetto Bioconductor

L'analisi statistica dei dati relativi a un fenomeno è un passaggio cruciale per qualsiasi ricercatore.

E' infatti necessario per formulare modelli funzionali e ipotesi di lavoro. 

L'ambiente statistico R e il progetto Bioconductor forniscono un sistema di strumenti (analitici, statistici, computazionali e grafici) molto potente per adempiere questo scopo, specialmente in ambito di analisi di dati genomici.

<br>

# CHE COS'È IL PROGETTO BIOCONDUCTOR

<br>

**Bioconductor**: software libero per l'analisi e l'interpretazione di dati genomici massivi
Bioconductor è un progetto aperto e partecipato che ha come obiettivo fornire strumenti per l'analisi e l'interpretazione di dati genomici. 

<br>

**Bioconductor** utilizza il <u>linguaggio di programmazione statistica **R** </u> ed è un progetto open-source e open-development. È open-source perché chiunque può leggere e modificare il codice di una funzione, ed è open-development perchè chiunque può contribuire e partecipare allo sviluppo del codice.

<br>

Il progetto **Bioconductor** ha una comunità di utenti molto attiva, una <u>documentazione approfondita</u>, diversi <u>forum di discussione dedicati</u> e viene costantemente aggiornato (la versione corrente è la 3.18, e una nuova versione viene rilasciata ogni 6 mesi).

<br>

<iframe src="https://www.bioconductor.org" width="800" height="600"></iframe>

<br>

# CHE COSA SI INTENDE PER PACCHETTO R/BIOCONDUCTOR

<br>

## Pacchetto R/Bioconductor: la app per la mia sessione di lavoro R


Il software sviluppato dal progetto **Bioconductor** è distribuito principalmente sotto forma di **pacchetti** compatibili con il linguaggio R. **Un pacchetto R/Bioconductor** è concettualmente simile ad una applicazione o app del cellulare: fornisce un insieme strutturato di codice, documentazione e/o dati per l'esecuzione di un certo scopo, ampliando così le funzionalità a disposizione dell'utente. 

Ad esempio, se installo sul mio cellulare la app *Instagram* estendo la gamma di funzioni a mia disposizione nel senso che ora dal mio cellulare posso anche: accedere al mio account Istagram oppure crearne uno, scorrere le pagine della mia rete di connessioni, caricare o commentare una foto, etc. 

In modo del tutto simile, se carico in una sessione di lavoro R il pacchetto R/Bioconductor [GEOquery](http://www.bioconductor.org/packages/release/bioc/html/GEOquery.html) posso interrogare l'archivio pubblico di dati di microarray Gene Expression Omnibus (GEO) del National Center for Biotechnology Information (NCBI), una risorsa ricca e varia, e ottenere direttamente nella mia sessione di lavoro R i dati di espressione che mi interessa analizzare. GEOquery è il ponte tra GEO e la mia sessione di lavoro R.

La versione corrente di **Bioconductor** (**versione 3.18**, a Febbraio 2024) esistono **oltre 2200 pacchetti** a disposizione della comunità scientifica biomedica. Questi pacchetti sono raggruppati in **4 tipologie principali**: 

- **software** - implementano analisi particolari o altre funzionalità, ad es. metodi per interrogare banche dati presenti sul Web o importare formati di file comuni in oggetti R

- **annotazione** - contengono dati che possono essere utili per interpretare i risultati di un'analisi, ad esempio: mappatura tra identificativi di diverse banche dati biologiche come "BRCA1" (da HUGO) e "ENSG00000012048" (da Ensembl); o anche, descrizione delle coordinate genomiche di esoni, trascritti o geni di interesse.

- **dati sperimentali** - contengono insiemi di dati biologici curati che possono essere utili per esercitazioni e tutorial.

- **procedure complete di analisi** - riassumono i flussi di lavoro comuni, ad es. il pacchetto SimpleSingleCell per analisi di espressione dati di RNA-seq a singola cella. 

Questa collezione di pacchetti può essere navigata per parola chiave sulla pagina [Bioconductor BioCViews](https://www.bioconductor.org/packages/release/BiocViews.html#___Software), in maniera del tutto simile a come cercheresti una app per un certo scopo su *Play Store* o su *Apple Store*.

<br>

<iframe src="https://www.bioconductor.org/packages/release/BiocViews.html#___Software" width="800" height="600"></iframe>

<br>

# COME SI USA UN PACCHETTO R/BIOCONDUCTOR

## I punti cardinali: pagina web e 'vignettes' del pacchetto 

Ogni **pacchetto R/Bioconductor** ha una **pagina web** ad esso dedicata sul sito del progetto Bioconductor: [http://www.bioconductor.org/](http://www.bioconductor.org/). Se già si conosce il nome del pacchetto di interesse, il modo più veloce per raggiungerne la pagina web dedicata è una ricerca del tipo "*NomeDelPacchetto Bioconductor*" su un motore di ricerca, ad esempio su Google. 

<span style="color:red;">*************             Seguendo quanto appena detto, riusciresti a trovare la pagina web del pacchetto GEOquery?              *************</span>

Ogni **pagina web di un dato pacchetto R/Bioconductor** mostra **come installare il pacchetto** stesso sul proprio computer con 2-3 righe di codice che si possono direttamente copiare e incollare nella propria sessione di lavoro R. Si noti che, in maniera del tutto simile all'esempio della app sul cellulare di prima, l'installazione di un pacchetto è necessaria solo la prima volta. Una volta installato, il pacchetto sarà pronto all'uso sul nostro computer, basterà caricarlo all'occorrenza nella sessione di lavoro di R ( con il comando R: *library(NomePacchetto)* ).

Ogni **pagina web di un dato pacchetto R/Bioconductor** contiene inoltre una o più **vignettes**, cioè documenti che forniscono una descrizione accurata e operativa del pacchetto. Questa documentazione è disponibile in varie forme: molti sono dei veri e propri tutorial che illustrano esempi di uso o dimostrano come un particolare compito può essere realizzato con il software di quel pacchetto. Altri documenti forniscono una panoramica più generale del pacchetto, come l'elenco delle funzioni in esso contenute e le loro specifiche.

Altra informazione utile presente sulla **pagina web di un dato pacchetto R/Bioconductor** è la lista delle **dipendenze**, cioè la lista di altri pacchetti, R o Bioconductor, che il dato pacchetto si aspetta di trovare installati sul vostro computer per poter funzionare.

<br>

<iframe src="https://www.bioconductor.org/packages/release/bioc/html/GEOquery.html" width="800" height="1200"></iframe>

<br>


<hr>

# WHAT'S NEXT

**Ti stava piacendo e vorresti continuare a "giocare" con R?**

Qui di seguito un paio di corsi di R gratuiti e disponibili online dall'ottimo progetto [Software Carpentry](https://software-carpentry.org/lessons/)  (corsi in inglese):

*Programming with R*, disponibile qui: [http://swcarpentry.github.io/r-novice-inflammation/](http://swcarpentry.github.io/r-novice-inflammation/)

*R for Reproducible Scientific Analysis*, disponibile qui: [http://swcarpentry.github.io/r-novice-gapminder/](http://swcarpentry.github.io/r-novice-gapminder/)


E poi c'è la pagina dei **manuali di R**, ricchi di esempi ed esercizi, a vari livelli di difficoltà: 

[https://cran.r-project.org/manuals.html](https://cran.r-project.org/manuals.html)

Per lo più questi manuali sono disponibili in inglese, ma ne esistono anche alcuni in altre lingue, compreso l'italiano:

[https://cran.r-project.org/other-docs.html#nenglish](https://cran.r-project.org/other-docs.html#nenglish) (scorri la pagina in basso per trovare i manuali disponibili in italiano)