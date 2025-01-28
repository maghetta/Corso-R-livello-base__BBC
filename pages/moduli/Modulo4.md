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

4 ore;

<table border="1" width="700">
	<tr>
		<td>[35']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
	<td colspan="2">5'</td>
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Svolgimento corso R online (capitolo 6 del corso di DataCamp)</td>		
	</tr>
	<tr>
		<td>[30']</td>
		<td>Sfide interattive sul contenuto del capitolo 6</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[35']</td>
		<td>Ottenere aiuto in R (vedi box qui sotto)</td>		
	</tr>
	<tr>
		<td>[35']</td>
		<td>Pacchetti R: cosa sono, come si usano (vedi box qui sotto)</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[20']</td>
		<td>Spazio per domande e curiosità</td>		
	</tr>
	<tr>
		<td>[10']</td>
		<td>Conclusioni</td>		
	</tr>
</table>



## Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa



1. Abbiamo conosciuto il quarto tipo di "oggetto" di R: il data.frame

![modulo4_datacamp](images/modulo4/dataCamp1.png)


A proposito, te li ricordi tutti i tipi di oggetti R che abbiamo conosciuto fin qui in questo corso introduttivo di R?


2. Abbiamo imparato i comandi base per fare un grafico in R


3. Qua e la tra i capitoli abbiamo anche conosciuto

- diversi altri esempi di funzioni disponibili in R, quali: *head(), tail(),  str(), data.frame(), subset(), order()*

- alcune funzioni utili per creare grafici come: *plot(), barplot(), pie(), title(), lines(), box(), axis()*

- uno di tanti dataset di esempio (in particolare, *mtcars*) già pronti da caricare nello spazio di lavoro di R per esercitarsi


<hr>

## Svolgimento corso R online (capitolo 6)


Nel capitolo 6 (*Liste*) imparerai a creare e maneggiare una lista, selezionarne alcuni elementi o assegnare dei nomi ai suoi elementi. Contrariamente ai vettori, le liste in R possono contenere tipi di dato differenti tra loro. (a proposito: conosci un altro tipo di oggetto in R che ti permette di immagazzinare tipi diversi / non omogenei?)

**segnalazione di un errore nel capitolo 6!!!!**

Alla schermata " 
# Creare una lista con i nomi (2)
", nelle istruzioni dell'esercizio c'è un piccolo errore.

Dove dice:

*Non dimenticarti di assegnare i nomi agli elementi della lista (i nomi da assegnare sono nome_film, attori e reviews).*

Tu leggi come fosse scritto:

*Non dimenticarti di assegnare i nomi agli elementi della lista (i nomi da assegnare sono nome_film, <span style="color:red;">actors</span> e reviews).*

<hr>

Per riprendere il corso di R su DataCamp al capitolo 5 --> segui i passaggi illustrati pagina web del Modulo 2](pages/moduli/modulo2.md) alla sezione intitolata

***Come riprendere il corso di Introduzione a R su DataCamp da dove lo si aveva interrotto***

<hr>

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

 

- Puoi trovare aiuto in rete utilizzando un motore di ricerca (es. [https://www.google.com/](https://www.google.com/)), specificando con le giuste parole chiave il tuo dubbio / problema.

Prova ad esempio a digitare su Google il tuo dubbio. Meglio ancora se poni la richiesta in inglese: avrai accesso ad un numero ancor più vasto di documenti tecnici e discussioni in forum specializzati.
<br>
Ad esempio:

How do I rename rows and columns of a data.frame in R?

**--> Sei soddisfatto del risultato? Hai trovato la risposta al tuo dubbio?**


- Altra via, digitando nella console di R il comando: 

**help.search()** o il suo sinonimo **??**

es. help.search("names") o ??"names"

Avrai in risposta un elenco di tutti i pacchetti R che contengono funzioni (riportati come nome_pacchetto::nome_funzione) nella cui documentazione è presente la/le parola/e chiave da te inserite per la ricerca di aiuto, insieme ad una minima descrizione di scopo della data funzione R.

<hr>

## Pacchetti R: cosa sono, come si usano

- I pacchetti di R sono delle ulteriori collezioni di funzioni, rispetto alle funzioni di base già disponibili in qualunque console di R, dedicate a svolgere un certo compito.

![R-page](images/modulo4/R.png)

<br>
Esistono al momento oltre 20,000 pacchetti di R disponibili per essere installati sul proprio PC, e caricati all'occorrenza nella  propria sessione di lavoro di R. L'elenco completo dei pacchetti si può trovare qui: [Table of available packages, sorted by name](https://cloud.r-project.org/web/packages/available_packages_by_name.html)

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
