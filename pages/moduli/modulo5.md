---
title: Modulo 5
---

![modulo5](/images/modulo5/modulo5.jpg)

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
		<td>[30']</td>
		<td>Statistica descrittiva: una panoramica introduttiva</td>
	</tr>
	<tr>
	<td colspan="2">pausa 5'</td>
	</tr>
	<tr>
		<td>[15']</td>
		<td>tipi di grafici</td>		
	</tr>
	<tr>
		<td>[15']</td>
		<td>caricare tabelle di dati in R</td>		
	</tr>
	<tr>
		<td>[35']</td>
		<td>to be defined</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
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

### Statistica descrittiva: una panoramica introduttiva

In questa sezione, copriremo i seguenti argomenti:

- [Tipi di Variabili in Statistica]
- [Indicatori Statistici di una distribuzione di Dati]
- [Grafici di Base]

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

## Indicatori Statistici di una distribuzione di Dati






### Media, Mediana, Moda

La **media** è la somma di tutti i valori divisa per il numero di valori. La **mediana** è il valore centrale di un insieme di dati ordinato. La **moda** è il valore che appare più frequentemente nei dati.

### Varianza e Deviazione Standard

La **varianza** misura la dispersione dei dati intorno alla media. La **deviazione standard** è la radice quadrata della varianza e rappresenta la dispersione media dei valori dalla media.

### Grafici di Base

I grafici sono strumenti fondamentali per visualizzare i dati. Alcuni dei grafici di base in R includono il grafico a dispersione, il boxplot e l'istogramma.

# Principali Tipi di Grafico in Statistica Descrittiva con R

La statistica descrittiva utilizza vari tipi di grafici per rappresentare visivamente i dati. Ecco una panoramica dei principali tipi di grafico utilizzati, con esempi di codice R per ciascuno.

## 1. Istogramma

Un istogramma è utilizzato per rappresentare la distribuzione di una variabile numerica continua. Mostra la frequenza dei dati suddivisi in intervalli (bins).

### Esempio di Codice
```r
# Genera un set di dati casuale
set.seed(123)
data <- rnorm(100)

# Crea un istogramma
hist(data, main="Istogramma", xlab="Valori", ylab="Frequenza", col="blue", border="black")



## Esercizi

Prova a risolvere i seguenti esercizi utilizzando R. Puoi eseguire i comandi di R direttamente nel tuo ambiente di lavoro.

### Esercizio 1: Calcolo della Media e Mediana di un vettore numerico

Utilizza il seguente dataset per svolgere l'esercizio: `c(4, 8, 6, 5, 3, 8, 9, 7, 6, 8)`. Calcola la media, la mediana e la moda.

```r
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

# tipi di grafici
Alcuni tipi di grafici di uso comune per rappresentare distribuzioni di variabili numeriche, logiche o categoriche.
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
