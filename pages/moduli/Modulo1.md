---
title: Modulo 1
---

![modulo1](images/modulo1/modulo1.jpg)

<br>

## Argomenti

- Il linguaggio di programmazione R 

- Introduzione alla console di R
  
- Vettori e Fattori in R


<br>
<br>


## Obiettivi conoscitivi


Al termine di questa attività dovresti essere in grado di:
<br>

- descrivere cos'è la console interattiva di R (anche detto terminale)
- eseguire dei comandi nella console di R
- scrivere una riga di commento in un codice R
- utilizzare il terminale di R come una semplice calcolatrice
- descrivere cos'è una variabile
- creare una nuova variabile in R o assegnare un valore ad una variabile già esistente
- eseguire operazioni su variabili, come ad esempio la somma di due variabili di tipo numerico
- elencare almeno 3 tipi diversi di variabili
- creare una variabile di tipo carattere
- elencare i possibili valori per una variabile di tipo booleano
- verificare di che tipo è una data variabile
- effettuare la somma di tutti gli elementi di un vettore
- elencare gli operatori di confronto (logici) disponibili in R
- confrontare 2 variabili numeriche
- selezionare uno o più elementi da un vettore
- calcolare la media di un vettore numerico
- selezionare elementi di un vettore in base ad una condizione posta
- fornire qualche esempio di variabile categorica
- descrivere cos'è e come si crea un fattore in R
- distinguere una variabile categorica nominale da una variabile categorica ordinale
- confrontare variabili categoriche ordinali

<br>
<br>

## Durata e programma dell'attività:

3 ore;

<table border="1" width="700">
	<tr>
		<td>[20']</td>
		<td>R: una panoramica introduttiva (cosa è, diffusione, vantaggi)</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Svolgimento tutorial: Introduzione alla Console R</td>
	</tr>
	<tr>
		<td></td>td>
		<td>Sfide interattive sul contenuto del tutorial</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>[50']</td>
		<td>Svolgimento tutorial: Vettori in R</td>
	</tr>
	<tr>
		<td></td>td>
		<td>Sfide interattive sul contenuto del tutorial</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>	
	<tr>
		<td>[50']</td>
		<td>Svolgimento tutorial: Fattori in R</td>		
	</tr>	
	<tr>
		<td></td>td>
		<td>Sfide interattive sul contenuto del tutorial</td>		
	</tr>
</table>

<br>

## Introduzione all'attività del modulo

<br>

### Un passo indietro: perché imparare a programmare?

Programmare significa formalizzare un problema e descriverne la soluzione attraverso una sequenza di istruzioni che una macchina può interpretare ed eseguire. Un programma non è altro che una rappresentazione esplicita di un processo: una catena ordinata di operazioni logiche, matematiche o decisionali che trasformano dati in risultati.

Un linguaggio di programmazione funge da interfaccia tra il ragionamento umano e l’esecuzione automatica, permettendo di tradurre ipotesi, modelli e procedure in strumenti operativi. In questo senso, programmare non è semplicemente "dire al computer cosa fare", ma **rendere esplicito, verificabile e riutilizzabile un metodo di lavoro**.

Imparare a programmare è particolarmente rilevante nel percorso di un dottorato per diverse ragioni: <br>
- **Sviluppo del pensiero computazionale**
Programmare richiede di scomporre problemi complessi in sotto-problemi ben definiti, di ragionare in termini di flussi logici, condizioni e dipendenze. Questo tipo di approccio rafforza la capacità di analisi e di progettazione di soluzioni, competenze centrali nella ricerca scientifica indipendentemente dal dominio disciplinare.

- **Controllo consapevole degli strumenti digitali**
Gran parte della ricerca contemporanea si basa su software, algoritmi e pipeline di analisi. Conoscere la programmazione consente di andare oltre l’uso “a scatola nera” degli strumenti, comprendendone assunzioni, limiti e potenziali fonti di errore.

- **Automazione e scalabilità**
Procedure ripetitive, analisi iterative, aggiornamento di figure o tabelle possono essere automatizzati, riducendo drasticamente il tempo necessario e la probabilità di errore umano. Questo è cruciale quando i dati crescono in dimensione, complessità o frequenza di aggiornamento.

- **Riproducibilità e trasparenza scientifica**
Un’analisi descritta tramite codice è ispezionabile, versionabile e riproducibile. Programmare significa poter documentare in modo preciso ogni passaggio che porta da dati grezzi a risultati finali, un requisito sempre più centrale nella scienza aperta e nella valutazione della qualità della ricerca.

- **Flessibilità e autonomia**
Anche una competenza di base consente di adattare metodi esistenti a nuovi contesti, esplorare dati in modo più libero e costruire pipeline personalizzate, senza dipendere completamente da software preconfezionati.

In sintesi, imparare a programmare non è soltanto un obiettivo fine a sé stesso, ma anche uno strumento per pensare meglio i problemi oggetto di studio, lavorare in modo più efficiente e produrre risultati più solidi e affidabili.

<hr>
Il linguaggio di programmazione R
<hr>

![Pagina wiki R](images/modulo1/R_page.png)


- R è un linguaggio di programmazione *open source*, potente e gratuito, progettato specificamente per l’analisi statistica, la modellizzazione dei dati e la visualizzazione grafica.
- R è, insieme a Python, uno dei linguaggi più utilizzati nella ricerca accademica e scientifica e, più in generale, nella *data science*, grazie alla sua forte integrazione con metodi statistici e bio-statistici e con risorse di dati e annotazioni biomediche.

![Pagina wiki R](images/modulo1/R_page2.png)

- R è un software multipiattaforma, disponibile per sistemi Linux/UNIX, Windows e macOS.

![Pagina CRAN](images/modulo1/CRAN.png)

- R dispone di una comunità di sviluppatori e utenti estremamente ampia e attiva, che garantisce: <br>
- **migliaia di pacchetti aggiornati** (CRAN, Bioconductor),
- **ampio supporto** online (forum, mailing list, Q&A),
- **documentazione** dettagliata e buone pratiche consolidate.

___

## Svolgimento tutorial in R: "Introduzione alla Console R"
<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Introduzione_alla_Console_R)

## Svolgimento tutorial in R: "Vettori in R"
<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Vettori_in_R)

## Svolgimento tutorial in R: "Fattori in R"
<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Fattori_in_R)

___

**Esercizi**
<br>

1. Quale comando si può utilizzare in R per visualizzare il contenuto del proprio spazio di lavoro?

- *a. dir()*
- *b. read()*
- *c. ls()*
- *d. list()*


2. Il comando  c(1, TRUE,"A") genera in R un vettore di che tipo?

- *a. Numerico.*
- *b. Logico.* 
- *c. Carattere.*

<br>

3. Voglio estrarre da un vettore chiamato "compiti" composto da 24 elementi, i valori corrispondenti alle posizioni 3, 11, 15 e 21. Scrivi il comando R opportuno per farlo.

4. La funzione rep() di R genera ripetizioni di un dato vettore tante volte quanto specificato nel parametro times. Ad esempio: *rep( c(1,0,2), times=2)* genererà il seguente output:  *1 0 2 1 0 2*. Usa il comando *rep()* per generare il seguente vettore: *1 0 1 0 1 0 1 0 1 0 1 0*

5. Scrivi 3 righe di codice R che facciano quanto segue: (1) creare un vettore denominato "regioni" che contiene gli elementi "Sicilia", "Lombardia" e "Liguria"; (2) aggiungere a questo vettore l'elemento "Molise"; (3) stampare a video il contenuto del vettore regioni. 

6. Risolvi la seguente espressione in R: *-3 x 5<sup>6</sup> + 3<sup>2-2</sup> x 2<sup>2</sup> -(-2)<sup>2</sup>*. Quanto fa?

7. Crea un vettore denominato x con i seguenti elementi: *3,4,5,6,6,5,2,2,6,7,8,2,3,2,5,4,5,9*; Poi calcola la media e la lunghezza del vettore x.

8. Crea un fattore ordinato denominato *geografia* che contenga le seguenti valutazioni di uno studente in geografia nei tre anni delle scuole medie: *ottimo, buono, buono, discreto, ottimo, insufficiente, buono*



### Riferimenti utili

- <span style="color:blue;">Progetto R - sito ufficiale: [https://www.r-project.org/](https://www.r-project.org/)</span>
- <span style="color:blue;">Ebook del Prof. Federico Reali: [Note dal aboratorio di R del corso di Probabilità e Statistica Matematica - aa 2018/2019](https://thefreolo.github.io/book/primi-passi-con-r.html)</span>
