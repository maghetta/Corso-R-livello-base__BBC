---
title: Modulo 4
---

![modulo4](images/modulo4/modulo4.jpg)

<br>

## Argomenti

- Liste in R, cioé il capitolo 6 del corso di Introduzione a R di DataCamp

- Come ottenere aiuto per codice R (vedi box dedicato qui sotto)

- Come (installare e) caricare un pacchetto di R (vedi box dedicato qui sotto)



## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- costruire una lista in R a partire da una serie di oggetti

- assegnare nomi agli elementi di una lista

- selezionare, in diversi modi,  gli elementi di una lista

- aggiungere un nuovo elemento ad una lista

- installare un pacchetto di R

- trovare documentazione relativa all'uso di una funzione di R

- cercare aiuto in rete per risolvere un problema di codice R




## Durata e programma dell'attività:

2 ore;

<table border="1" width="700">
	<tr>
		<td>[20']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Svolgimento del tutorial *Liste in R*</td>		
	</tr>
	<tr>
		<td>[20']</td>
		<td>Sfide interattive sul contenuto del capitolo 6</td>		
	</tr>
	<tr>
		<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>[15']</td>
		<td>Ottenere aiuto in R</td>		
	</tr>
	<tr>
		<td>[15']</td>
		<td>Pacchetti R: cosa sono, come si usano</td>		
	</tr>
</table>



## Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa



1. Abbiamo conosciuto il quarto tipo di "oggetto" di R: il *data frame*

A proposito, te li ricordi tutti i tipi di oggetti R che abbiamo conosciuto fin qui in questo corso introduttivo di R?


2. Abbiamo imparato i comandi base per fare un grafico in R


3. Qua e la tra i capitoli abbiamo anche conosciuto

- diversi altri esempi di funzioni disponibili in R, quali: *head()*, *tail()*,  *str()*, *data.frame()*, *subset()*, *order()*

- alcune funzioni utili per creare grafici come: *plot()*, *barplot()*, *pie()*, *title()*, *lines()*, *box()*, *axis()*

- uno di tanti dataset di esempio (in particolare, *mtcars*) già pronti da caricare nello spazio di lavoro di R per esercitarsi


<hr>

## Svolgimento del tutorial: Liste in R

In questo tutorial imparerai a creare e maneggiare una lista, selezionarne alcuni elementi o assegnare dei nomi ai suoi elementi. Contrariamente ai vettori, le liste possono contenere come elementi tipi di dato differenti tra loro (a proposito: conosci un altro tipo di oggetto in R che ti permette di immagazzinare tipi diversi / non omogenei di dato?)

<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Liste_in_R)



## Ottenere aiuto in R

Come abbiamo detto, R è un linguaggio molto ben documentato e supportato da una vasta e attiva comunità di utenti.

A [questo link](https://www.r-project.org/help.html) puoi trovare un guida (in inglese) che illustra i diversi modi per chiedere aiuto in R.

Qui di seguito riassumerò due approcci molto comuni:


Per trovare aiuto su come usare una data funzione di R ***di cui conosci il nome*** (esempio: per sapere quali argomenti la funzione si aspetta,  e quali parametri posso usare per modificarne il comportamento) posso accedere alla documentazione digitando nella console di R il comando:

**?\<nome della funzione\>**

*es. ?row.names*

NOTA: la documentazione di una funzione cui si accede come visto qui sopra (?\<nome_della_funzione\>) non è sempre di facile lettura. Ma non ti spaventare!!! E soprattutto, tra le tante informazioni disponibili, orientati in particolare su:

la sessione *Description*, ti fornisce una breve descrizione, in forma discorsiva, di cosa fa la data funzione

la sessione *Arguments*, ti illustra i diversi argomenti che prende in input la data funzione

la sessione *Examples* (in fondo alla pagina), ti illustra esempi di uso della data funzione


Alternativamente, e nel caso in cui non conoscessi già il nome della funzione R da usare per un dato scopo:

 

- Puoi trovare aiuto in rete utilizzando un motore di ricerca (es. [https://www.google.com/](https://www.google.com/)), specificando con le giuste parole chiave il tuo dubbio / problema. Prova ad esempio a cercare nel tuo motore di ricerca preferito quanto segue:

*How do I rename rows and columns of a data.frame in R?*

Nota: Se poni la richiesta in inglese, avrai accesso ad un numero ancor più vasto di documenti tecnici e discussioni in forum specializzati per trovare la risposta che cerchi.


**--> Sei soddisfatto del risultato? Hai trovato la risposta al tuo dubbio?**


- Altra via, digitando nella console di R il comando: 

**help.search()** o il suo sinonimo **??**

es. help.search("names") o ??"names"

Avrai in risposta un elenco di tutti i pacchetti R che contengano funzioni nella cui documentazione è presente la/le parola/e chiave da te inserite per la ricerca di aiuto, insieme ad una minima descrizione di scopo della data funzione R. Nell'elenco vedrai le funzioni di possibile interesse forniti in risposta al tuo quesito indicati in questo formato: *nome_pacchetto::nome_funzione*

<hr>

## Pacchetti R: cosa sono, come si usano

Uno dei punti di forza del linguaggio e ambiente di sviluppo *R* è la vasta disponibilità di pacchetti, #
ovvero raccolte di funzioni, dati e documentazione che estendono le capacità di base del linguaggio.

I pacchetti in R consentono di eseguire operazioni avanzate senza dover scrivere codice da zero, 
offrendo strumenti e funzioni già pronte all’uso, applicabili in diversi contesti come analisi statistiche, 
machine learning, visualizzazione grafica e molto altro.
Esistono decine di migliaia di pacchetti R, che possono essere installati e caricati facilmente 
tramite il portale [*CRAN* (*Comprehensive R Archive Network*)](https://cran.r-project.org/), oppure da [*Bioconductor*](https://www.bioconductor.org/), un progetto che sviluppa, 
mantiene aggiornati e rende disponibili pacchetti specifici per l’analisi di dati biomedici. 
Altri pacchetti possono essere scaricati da repository alternativi o direttamente da sviluppatori indipendenti.

L’uso dei pacchetti rende R estremamente flessibile e adatto a una vasta gamma di applicazioni, sia in ambito scientifico che professionale.

![R-page](images/modulo4/R.png)

<br>
I pacchetti di R disponibili dal *CRAN* per essere installati sul proprio PC, e caricati all'occorrenza nella propria sessione di lavoro di R sono elencati [qui](https://cloud.r-project.org/web/packages/available_packages_by_name.html)
I pacchetti di R disponibili dal progetto *Bioconductor* per essere installati sul proprio PC, e caricati all'occorrenza nella propria sessione di lavoro di R sono elencati [qui](https://www.bioconductor.org/packages/release/BiocViews.html#___Software)

<br>
<br>

Per utilizzare un pacchetto di R sul nostro computer, seguire 2 passaggi:


1. **installare il pacchetto sul nostro PC** con la funzione R **install.packages()**

```
# Esempio:
install.packages("A3") 		# nota il nome del pacchetto messo tra virgolette
```

NOTA 1: questo lo possiamo fare SOLO sulla nostra console R locale, dove abbiamo permessi adeguati

NOTA 2: questo passaggio sarà necessario solo la prima volta che usiamo un nuovo pacchetto


2. **caricare il dato pacchetto nella propria sessione di lavoro** di R,  con la funzione **library()**:

```
# Esempio:
library(A3)                 # nota il nome del pacchetto scritto senza virgolette
```

NOTA: questo passaggio sarà necessario ogni volta che vorremo utilizzare le funzioni di un dato pacchetto R nella nostra sessione di lavoro


Un paio di riferimenti utili:

- Un comando utile per controllare quali pacchetti abbiamo caricato nella nostra sessione di lavoro è: sessionInfo()

Prova ad esempio a digitare il seguente comando di R nella console di R che utilizzi di solito:

```
sessionInfo()
```

- Ogni pacchetto di R ha una pagina dedicata, dove è anche possibile scaricare la documentazione che ci insegna ad usarlo. Es.: fai click sul nome A3 nell'elenco di pacchetti che trovi a questo link [Table of available packages, sorted by name](https://cloud.r-project.org/web/packages/available_packages_by_name.html) per accedere alla pagina di documentazione del pacchetto A3

NOTA: per scoprire come installare e caricare pacchetti in R, avremmo anche potuto applicare quanto appena imparato. E cioé, chiedere a un motore di ricerca per trovare aiuto. Prova ad esempio a cercare su [https://www.google.com/](https://www.google.com/) la seguente combinazione di parole:

come caricare e installare pacchetti in R

oppure in inglese:

how to install / load packages in R

Ha funzionato la ricerca? Hai trovato risultati utili per risolvere il tuo dubbio (cioé, come installare e caricare pacchetti R)?


Suggerimento extra: se leggere la documentazione non ti piace, dai uno sguardo anche ai risultati della tua ricerca trovati tra i video. Ad esempio, su youtube puoi trovare tantissimi tutorial su vari aspetti di R, a diversi livelli di complessità. Qui c'è un esempio di questi video tutorial.


<br>

## Esempio di installazione ed uso di un pacchetto R

**Premessa:**
Per eseguire il codice di esempio qui di seguito, **ti servirà una console di R**. Ad esempio, quella fornita da **RStudio**.

In questo esempio, utilizzeremo il pacchetto dplyr per dimostrare come caricare un pacchetto e applicare alcune delle sue funzioni per la manipolazione dei dati.

## Installazione del Pacchetto
Se non hai già installato il pacchetto dplyr, puoi farlo con il comando **install.packages()**. Questa operazione deve essere eseguita solo una volta.

```
# Installazione del pacchetto dplyr (da eseguire una sola volta)
install.packages("dplyr")
Caricamento del Pacchetto
Una volta installato, puoi caricare il pacchetto dplyr utilizzando library().
```

```
# Caricamento del pacchetto dplyr
library(dplyr)
Uso delle Funzioni di dplyr
Utilizziamo il pacchetto dplyr per eseguire alcune operazioni di manipolazione dei dati. Useremo il dataset integrato mtcars per questo esempio.
```

```
# Visualizzazione delle prime righe del dataset mtcars
head(mtcars)
Filtraggio dei Dati
Filtriamo le auto con almeno 6 cilindri.
```

```
# Filtraggio delle auto con almeno 6 cilindri
mtcars_6_cyl <- filter(mtcars, cyl >= 6)
head(mtcars_6_cyl)
Selezione delle Colonne
Selezioniamo solo le colonne mpg (miglia per gallone) e hp (potenza del motore).
```

```
# Selezione delle colonne mpg e hp
mtcars_mpg_hp <- select(mtcars, mpg, hp)
head(mtcars_mpg_hp)
Ordinamento dei Dati
Ordiniamo le auto in base alla potenza del motore (hp) in ordine decrescente.
```

```
# Ordinamento delle auto per potenza del motore in ordine decrescente
mtcars_sorted <- arrange(mtcars, desc(hp))
head(mtcars_sorted)
```
