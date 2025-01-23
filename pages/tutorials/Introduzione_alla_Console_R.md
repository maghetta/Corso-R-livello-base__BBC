---
title: Introduzione alla Console R
---

```markdown
# Tutorial introduttivo a R e all'uso della sua console interattiva

In questo breve tutorial vedremo:
- cos'è e come usare la console interattiva (o terminale interattivo) di R
- come utilizzare R come una calcolatrice
- cos'è una variabile e come crearla in R, o modificarne il valore
- quali sono i tipi principali di variabili che si possono incontrare

## Terminale Interattivo di R

R è spesso utilizzato tramite un terminale interattivo, noto anche come console R.
Il terminale interattivo è un ambiente in cui è possibile digitare comandi R e vedere immediatamente mostrati i risultati.
Questo è molto utile per testare rapidamente il codice e sperimentare.

Per avviare il terminale interattivo di R, è possibile:

1. Avviare R dall'icona corrispondente sul nostro PC
2. Avviare R da una finestra di terminale (o prompt dei comandi) e digitare `R` seguito da invio.
3. Avviare RStudio (un popolare ambiente di sviluppo integrato per R) e utilizzare la console R integrata nella sua interfaccia.

NOTA: tutte e tre le opzioni qui sopra riportate prevedono che tu abbia una versione di R installata e funzionante sul tuo PC.
Se poi scegliessi l'opzione #3, dovrai aver installato sul tuo PC anche RStudio.
Se così non fosse, puoi vedere come installare R e/o RStudio ad esempio [qui](https://rstudio-education.github.io/hopr/starting.html).
Una volta avviato il terminale interattivo, vedrete un prompt (solitamente `>`), dove potrete digitare i vostri comandi R.


## Uso di R come Calcolatrice

R può essere utilizzato per eseguire semplici operazioni aritmetiche. Ecco alcuni esempi:

```R
# Somma
3 + 5

# Sottrazione
10 - 4

# Moltiplicazione
6 * 7

# Divisione
20 / 4

# Potenza
2^3

# Radice quadrata
sqrt(16)
```

## Variabili e Assegnazione

In R, possiamo memorizzare i risultati delle operazioni in variabili. Una variabile è un contenitore con un nome che rappresenta un valore. Per assegnare il valore ad una variabile, in R si utilizza il simbolo `<-` (o `=`). 
Una variabile è un contenitore simbolico utilizzato per memorizzare un valore o un insieme di valori in un programma. In R, una variabile può contenere diversi tipi di dati come numeri, stringhe, vettori, matrici, liste o data frame.

Le variabili rendono il codice più flessibile e leggibile, permettendo di riferirsi ai dati senza conoscerne direttamente il valore specifico.

```R
# Assegnazione di un valore a una variabile
x <- 5

# Utilizzo della variabile in un'operazione
y <- x + 3

# Stampa del valore della variabile
print(y)
```

## Esempio

Rivediamo tutto insieme in un esempio:

```R
# Assegnazione di valori a variabili
a <- 10
b <- 2

# Operazioni aritmetiche
somma <- a + b
diffrenza <- a - b
prodotto <- a * b
quoziente <- a / b
potenza <- a^b
radice <- sqrt(a)

# Stampa dei risultati
print(paste("Somma:", somma))
print(paste("Differenza:", differenza))
print(paste("Prodotto:", prodotto))
print(paste("Quoziente:", quoziente))
print(paste("Potenza:", potenza))
print(paste("Radice quadrata:", radice))
```


## Principali Tipi di Variabili in R

1. **Variabili Numeriche**
   - **Interi**: Numeri senza decimali.
     ```R
     intero <- 10
     ```
   - **Numeri a virgola mobile (double)**: Numeri con decimali.
     ```R
     numerico <- 10.5
     ```

2. **Variabili Carattere (Stringhe)**
   - Sequenze di caratteri racchiuse tra virgolette.
     ```R
     stringa <- "Ciao, mondo!"
     ```

3. **Variabili Logiche (Boolean)**
   - Variabili che possono assumere solo due valori: `TRUE` o `FALSE`.
     ```R
     logico <- TRUE
     ```

# Stampa delle variabili
print(intero)   # ma anche, più semplicemente, prova a digitare il sul terminale il nome della variabile che vuoi stampare a video
```

## Conclusione
In questo tutorial, abbiamo visto come usare R come calcolatrice, abbiamo introdotto i concetti di variabile e assegnazione, e visto i principali tipi di variabile.
```
