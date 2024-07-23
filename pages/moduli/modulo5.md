---
title: Modulo 5
---

![modulo5](images/modulo5/modulo5.jpg)

<br>

## Argomenti

- cenni di statistica descrittiva

- caricamento e ispezione di dati in R

- tipi di grafici di uso comune per la rappresentazione grafica di dati

<br>
<br>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- caricare una tabella di dati di interesse dal proprio PC (esempio, da un file excel o testo semplice formattato in colonne)

- scrivere comandi R per calcolare indicatori statistici descrittivi di variabili numeriche (media, mediana, deviazione standard)

- scrivere comandi R per calcolare indicatori statistici descrittivi di variabili categoriche e logiche

- scegliere un tipo di grafico adatto per visualizzare distribuzioni di variabili di interesse

- scrivere comandi R per rappresentare graficamente una distribuzione di variabili (numeriche, logiche o categoriche)

- seguire le istruzioni fornite in un tutorial (codice commentato, con domande ed esercizi)

- elencare e descrivere almeno tre tipi di grafici di uso comune per rappresentare distribuzioni di variabili numeriche, logiche o categoriche

<br>
<br>

## Durata e programma dell'attività:

4 ore;


<table border="1" width="700">
	<tr>
		<td>[20']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
		<td>[50']</td>
		<td>Statistica descrittiva: una panoramica introduttiva</td>
	</tr>
	<tr>
	<td colspan="2">pausa 5'</td>
	</tr>
	<tr>
		<td>[30']</td>
		<td>esercizi</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 15'</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>to be defined</td>
	</tr>
	<tr>
		<td>[30']</td>
		<td>Sfide interattive</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
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

1. **Abbiamo conosciuto il quinto ed ultimo tipo di "oggetto" di R: la lista**

![r_liste](images/modulo5/r_liste.png)

2. **Abbiamo imparato come chiedere aiuto se abbiamo dubbi sul codice, in R o in rete**

![cmd](images/modulo5/cmd.png)

ad esempio dalla console di R, con il simbolo ? seguito dal nome della funzione per cui vogliamo vedere la documentazione

![firefox](images/modulo5/firefox.png)


Oppure direttamente ad un motore di ricerca, per sapere come fare una certa cosa in R. Approfittando dei tanti utenti R e dei tanti forum con argomenti e problemi di ogni tipo già affrontati e risolti, e documentati in rete.

<br>

3. **Abbiamo visto come installare e caricare nella propria sessione di lavoro un pacchetto R**

![cmd](images/modulo5/cmd2.png)

installo un pacchetto, dei tanti disponibili nel repository di R, una sola volta sul mio PC con la funzione **install.packages()**

![cmd](images/modulo5/cmd3.png)

Ogni volta che voglio utilizzare funzioni da un dato pacchetto, carico quel pacchetto nella mia sessione di lavoro R con la funzione *library()*

4. **Qua e la tra i capitoli abbiamo anche conosciuto**

- diversi altri esempi di funzioni disponibili in R, quali: *list(), names(), sessionInfo()* 

- un altro dei tanti dataset di esempio (in particolare, USArrests) già pronti da caricare nello spazio di lavoro di R per esercitarsi

- abbiamo visto l'importanza delle parentesi: \[], \[[]], () ... a proposito, sapresti dire ciascuno di questi tipi di parentesi quando si usa?

<br>

<hr>

### Statistica descrittiva: una panoramica introduttiva

In questa sezione, copriremo i seguenti argomenti:

- Statistica descrittiva: scopi e modalità
- Tipi di Variabili in Statistica
- Indicatori Principali della Statistica Descrittiva
- Distribuzioni di Frequenza Assolute e Relative
- Principali Tipi di Grafico usati in Statistica Descrittiva
- Importare Dati in R: Diversi Formati e Modi Possibili


## Tipi di Variabili in Statistica

In statistica, le variabili si classificano in diversi tipi in base alla natura dei dati che rappresentano e al tipo di misurazione. Conoscere la tipologia di dati con cui si sta lavorando è essenziale per scegliere i giusti metodi di analisi statistica e per una corretta interpretazione dei risultati.Ecco una panoramica dei principali tipi di variabili:

# 1. Variabili Qualitative (o Categoriali)
Queste variabili descrivono categorie o attributi distinti e non numerici.

- **Nominali**: Le categorie non hanno un ordine intrinseco. Esempi includono il colore degli occhi (blu, verde, marrone), il genere (maschio, femmina), e il tipo di veicolo (auto, moto, bici).
- **Ordinali**: Le categorie hanno un ordine intrinseco, ma le distanze tra le categorie non sono misurabili. Esempi includono i livelli di istruzione (scuola elementare, media, superiore, università) e i livelli di soddisfazione (soddisfatto, neutro, insoddisfatto).

# 2. Variabili Quantitative (o Numeriche)
Queste variabili rappresentano quantità misurabili e possono essere numeri con significato matematico.

- **Discrete**: Possono assumere solo valori distinti e separati (tipicamente numeri interi). Esempi includono il numero di figli in una famiglia, il numero di studenti in una classe, e il numero di macchine vendute.
- **Continue**: Possono assumere qualsiasi valore in un intervallo continuo e possono essere frazionarie. Esempi includono l'altezza, il peso, e il tempo.

# 3. Variabili Dicotomiche e Logiche
Queste sono un tipo speciale di variabili nominali che hanno solo due categorie. Esempi includono il risultato di un test (passato/fallito) e la presenza o assenza di una caratteristica (sì/no). Un caso particolare di variabile dicotomica è rappresentato dalle variabili logiche (TRUE/FALSE). Queste ultime sono immediatamente interpretabili e trattabili come numeriche da R (1/0).


## Indicatori Principali della Statistica Descrittiva

La statistica descrittiva si avvale di diversi indicatori per riassumere e descrivere le caratteristiche principali di un insieme di dati. Ecco una panoramica degli indicatori più comuni e degli esempi su come calcolarli in R.

# 1. Media
La media aritmetica è la somma di tutti i valori divisa per il numero di valori. È un indicatore della tendenza centrale dei dati.

```
# Genera un set di dati
data <- c(2, 4, 6, 8, 10)

# Calcola la media
mean_value <- mean(data)
print(mean_value)  # Output: 6
```

# 2. Mediana
La mediana è il valore che separa la metà superiore dei dati dalla metà inferiore. È meno sensibile ai valori anomali rispetto alla media.

```
# Genera un set di dati
data <- c(2, 4, 6, 8, 10)

# Calcola la mediana
median_value <- median(data)
print(median_value)  # Output: 6
```

# 3. Deviazione Standard
La deviazione standard misura la dispersione dei dati rispetto alla media. Un valore elevato indica che i dati sono molto dispersi.

```
# Genera un set di dati
data <- c(2, 4, 6, 8, 10)

# Calcola la deviazione standard
sd_value <- sd(data)
```

# 4. Distribuzione di Frequenza
La distribuzione di frequenza mostra come i dati sono distribuiti tra diverse categorie o intervalli.

```
# Genera un set di dati
data <- c(18 ,19 , 20 , 30 , 29 , 28 , 21 , 22 , 23 , 27 , 26 , 25 , 24 , 25 , 26, 24 , 23 , 22 , 27 , 28 , 21 , 24 , 25 , 25 , 27 , 19 , 21 , 28 , 29, 28)

# Calcola la distribuzione di frequenza
frequency_distribution <- table(data)
print(frequency_distribution)
# Output:
# data
# 18 19 20 21 22 23 24 25 26 27 28 29 30 
# 1  2  1  3  2  2  3  4  2  3  4  2  1 
```

# Una funzione di R utile per un riepilogo dei dati: summary()

La funzione summary() in R è uno strumento potente e versatile che fornisce un riepilogo statistico dei principali indicatori di un set di dati. È particolarmente utile per ottenere rapidamente una panoramica delle caratteristiche di un dataset e per individuare eventuali valori anomali o pattern interessanti.

# Cosa Fa summary()

Quando si applica la funzione summary() a un dataset, essa restituisce i seguenti indicatori statistici per ciascuna variabile:

- **Valore Minimo (Min.)**: Il valore più basso nel dataset.
- **Primo Quartile (1st Qu.)**: Il valore al 25-esimo percentile.
- **Mediana (Median)**: Il valore al 50-esimo percentile.
- **Media (Mean)**: La media aritmetica dei valori.
- **Terzo Quartile (3rd Qu.)**: Il valore al 75-esimo percentile.
- **Valore Massimo (Max.)**: Il valore più alto nel dataset.

Per le variabili categoriche, summary() restituisce un conteggio delle occorrenze di ciascun livello.

# Perché È Utile

- **Rapida Panoramica**: Fornisce un riepilogo conciso delle principali statistiche descrittive.
- **Identificazione di Outliers**: Facilita l'individuazione di valori anomali.
- **Verifica di Dati Mancanti**: Indica la presenza di valori mancanti.

Di sequito un esempio di utilizzo della funzione summary() con un semplice dataset:

```
# Creazione di un dataset di esempio
data <- data.frame(
  age = c(23, 25, 31, 35, 42, 58, 60, 22, 30, 40),
  salary = c(50000, 60000, 80000, 55000, 120000, 70000, 75000, 65000, 62000, 58000)
)

# Applicazione della funzione summary()
summary_stats <- summary(data)
print(summary_stats)
```

## Distribuzioni di Frequenza Assolute e Relative

# Distribuzione di Frequenza Assoluta
La distribuzione di frequenza assoluta è una tabulazione che mostra il numero di occorrenze di ciascun valore o intervallo di valori in un dataset. È utile per capire come i dati sono distribuiti in termini di conteggio.

# Distribuzione di Frequenza Relativa
La distribuzione di frequenza relativa, invece, esprime la frequenza assoluta come una frazione o una percentuale del totale. È utile per confrontare distribuzioni di dataset di dimensioni diverse, poiché normalizza i dati rispetto al totale.

# Utilità
- **Comprensione della Distribuzione dei Dati**: Permette di visualizzare come i dati sono distribuiti e individuare pattern o anomalie.
- **Confronto di Dataset**: Le frequenze relative facilitano il confronto tra dataset di dimensioni diverse.
- **Base per Altre Analisi**: Costituiscono il punto di partenza per calcolare ulteriori statistiche descrittive o per visualizzazioni grafiche come istogrammi.

# Un paio di funzioni di R utile per calcolare frequenze assolute e relative: table() e prop.table()
Ecco un esempio di come calcolare e visualizzare le distribuzioni di frequenza assolute e relative in R:

```
# Creazione di un dataset di esempio
data <- c(2, 3, 3, 4, 4, 4, 5, 5, 5, 5, 6, 6, 7)

# Calcolo della distribuzione di frequenza assoluta
freq_abs <- table(data)
print(freq_abs)

# Calcolo della distribuzione di frequenza relativa
freq_rel <- prop.table(freq_abs)
print(freq_rel)
```


## Principali Tipi di Grafico usati in Statistica Descrittiva

I grafici sono strumenti fondamentali per visualizzare i dati. La statistica descrittiva utilizza vari tipi di grafici per rappresentare visivamente i dati.  Ogni tipo di grafico ha il suo specifico uso e può fornire diverse prospettive sui dati analizzati. Qui di seguito una panoramica dei principali tipi di grafico utilizzati nella statistica descrittiva con R. con esempi di codice R per ciascuno:


# 1. Istogramma
Un istogramma è utilizzato per rappresentare la distribuzione di una variabile numerica continua. Mostra la frequenza dei dati suddivisi in intervalli (bins).

```
# Genera un set di dati casuale
set.seed(123)	# questa funzione serve ad assicurare che tutti noi lavoreremo con gli stessi numeri (*)
data <- rnorm(100)

# Crea un istogramma
hist(data, main="Istogramma", xlab="Valori", ylab="Frequenza", col="blue", border="black")
```
(*) La funzione set.seed(), ad esempio **set.seed(123)**,  Imposta il seme del generatore di numeri casuali a 123. Questo significa che ogni volta che esegui il codice con lo stesso seme (123), otterrai la stessa sequenza di numeri casuali. Questo è particolarmente utile per garantire la riproducibilità dei risultati nelle analisi e nei test.
 Imposta il seme del generatore di numeri casuali a 123. Questo significa che ogni volta che esegui il codice con lo stesso seme (123), otterrai la stessa sequenza di numeri casuali. Questo è particolarmente utile per garantire la riproducibilità dei risultati nelle analisi e nei test.

# 2. Grafico a Barre
Un grafico a barre è utilizzato per rappresentare la frequenza o la percentuale di categorie di dati qualitativi.

```
# Genera dati categoriali
categories <- c("A", "B", "C", "D")
values <- c(10, 23, 15, 8)

# Crea un grafico a barre
barplot(values, names.arg=categories, main="Grafico a Barre", xlab="Categorie", ylab="Frequenza", col="lightblue")
```


# 3. Boxplot
Un boxplot è utilizzato per visualizzare la distribuzione di una variabile numerica continua attraverso i suoi quartili. È utile per identificare i valori anomali.

```
# Genera un set di dati casuale
set.seed(123)
data <- rnorm(100)

# Crea un boxplot
boxplot(data, main="Boxplot", ylab="Valori", col="lightgreen")
```

# 4. Grafico a Dispersione (Scatter Plot)
Un grafico a dispersione è utilizzato per visualizzare la relazione tra due variabili numeriche.

```
# Genera due set di dati correlati
set.seed(123)
x <- rnorm(100)
y <- 2 * x + rnorm(100)

# Crea un grafico a dispersione
plot(x, y, main="Grafico a Dispersione", xlab="Variabile X", ylab="Variabile Y", col="red", pch=19)
```

# 5. Grafico a Torta
Un grafico a torta è utilizzato per rappresentare la proporzione di diverse categorie di dati qualitativi.

```
# Genera dati categoriali
slices <- c(10, 23, 15, 8)
labels <- c("A", "B", "C", "D")

# Crea un grafico a torta
pie(slices, labels=labels, main="Grafico a Torta", col=rainbow(length(slices)))
```

# Importare Dati in R: Diversi Formati e Modi Possibili
## Introduzione
R offre diverse funzioni per importare dati da vari formati di file. Di seguito vengono illustrati i modi più comuni per leggere tabelle di dati in R, con esempi di codice per ciascun formato.

## 1. Importare Dati da un File CSV

Il formato CSV (Comma-Separated Values) è uno dei formati più comuni per l'archiviazione e lo scambio di dati tabulari. In R, si utilizza la funzione `read.csv()`.

```
# Importare dati da un file CSV
data_csv <- read.csv("path/to/yourfile.csv")
head(data_csv)
```


2. Importare Dati da un File TSV
Il formato TSV (Tab-Separated Values) utilizza il tab come delimitatore. In R, si può usare la funzione read.table() specificando il delimitatore.

```
# Importare dati da un file TSV
data_tsv <- read.table("path/to/yourfile.tsv", sep="\t", header=TRUE)
head(data_tsv)
```


3. Importare Dati da un File Excel
Per leggere file Excel (.xls o .xlsx), si può utilizzare il pacchetto readxl.
<br>
<small> Per un file excel da usare come esempio, scarica <a href="https://cdn.who.int/media/docs/default-source/child-growth/child-growth-standards/indicators/length-height-for-age/lhfa_girls_0-to-13-weeks_zscores.xlsx?sfvrsn=a2c6650e_11" download>questo file ("lhfa_girls_0-to-13-weeks_zscores.xlsx")</a> sul tuo PC che riporta i dati della <a href="https://www.who.int/tools/child-growth-standards/standards/length-height-for-age">World Health Organization (WHO)</a> su peso e altezza di bambine tra 0 e 13 settimane. </small>


```
# Installare e caricare il pacchetto readxl
install.packages("readxl")
library(readxl)

# Importare dati da un file Excel
data_excel <- read_excel("path/to/yourfile.xlsx", sheet = 1)	# es. adatta con il path al file "lhfa_girls_0-to-13-weeks_zscores.xlsx"
head(data_excel)
```

4. Importare Dati da un File di Testo con Delimitatore Personalizzato
Se si ha un file di testo con un delimitatore diverso da virgola o tab, si può utilizzare la funzione read.table() specificando il delimitatore corretto.

```
# Importare dati da un file di testo con delimitatore personalizzato
data_custom <- read.table("path/to/yourfile.txt", sep=";", header=TRUE)
head(data_custom)
```

5. Importare Dati da una Connessione URL
È possibile importare dati direttamente da una URL che punta a un file CSV.

```
# Importare dati da una URL
url <- "http://example.com/yourfile.csv"
data_url <- read.csv(url)
head(data_url)
```



## Esercizi

Prova a risolvere i seguenti esercizi utilizzando R. Puoi eseguire i comandi di R direttamente nel tuo ambiente di lavoro.

# Esercizio 1: Calcolo della Media e Mediana di un vettore numerico

Utilizza il seguente dataset per svolgere l'esercizio: `c(4, 8, 6, 5, 3, 8, 9, 7, 6, 8)`. Calcola la media, la mediana e la moda.

```
# Esercizio 1
data <- c(4, 8, 6, 5, 3, 8, 9, 7, 6, 8)

# Calcola la media
media <- mean(data)
cat("Media:", media, "\n")

# Calcola la mediana
mediana <- median(data)
cat("Mediana:", mediana, "\n")

# Calcola la moda
moda <- function(x) {
  uniqx <- unique(x)
  uniqx[which.max(tabulate(match(x, uniqx)))]
}
cat("Moda:", moda(data), "\n")


<br>

<br>

# caricare tabelle di dati in R

<br>

...

<br>
...

<br>

...

<br>

<iframe src="https://it.wikipedia.org/wiki/Statistica_descrittiva" width="800" height="600"></iframe>

<br>

## Contenuti in via di definizione---


...

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
