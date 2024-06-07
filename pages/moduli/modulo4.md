---
title: Modulo 4
---

Argomenti di oggi

Liste in R, cioé il capitolo 6 del corso di Introduzione a R di DataCamp

Come ottenere aiuto per codice R (vedi box dedicato qui sotto)

Come (installare e) caricare un pacchetto di R (vedi box dedicato qui sotto)

Obiettivi conoscitivi di oggi

Al termine di questa attività dovresti essere in grado di:

costruire una lista in R a partire da una serie di oggetti

assegnare nomi agli elementi di una lista

selezionare, in diversi modi,  gli elementi di una lista

aggiungere un nuovo elemento ad una lista

installare un pacchetto di R

trovare documentazione relativa all'uso di una funzione di R

cercare aiuto in rete per risolvere un problema di codice R

Programma dell'attività di oggi

durata: 6 ore; modalità: presenza

[8:30-9:30]	Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

[pausa 10']

[9:40-10:20]	Svolgimento corso R online (capitolo 6)

[10:20-10:50]	Sfide interattive sul contenuto del capitolo 6

[pausa 10']

[11:00-11:20]	Ottenere aiuto in R (vedi box qui sotto)

[11:20-11:40]	(Installare e) caricare un pacchetto R (vedi box qui sotto)

[11:40-12:10]	Sfide interattive

[pausa pranzo 40']

[12:50-13:30]	Altra sfida tremendissima

[13:40-14:30]	Svolgimento e invio prodotto di lavoro richiesto 

Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

1. Abbiamo conosciuto il quarto tipo di "oggetto" di R: il data.frame


A proposito, te li ricordi tutti i tipi di oggetti R che abbiamo conosciuto fin qui in questo corso introduttivo di R?

2. Abbiamo imparato i comandi base per fare un grafico in R

3. Qua e la tra i capitoli abbiamo anche conosciuto

diversi altri esempi di funzioni disponibili in R, quali: head(), tail(),  str(), data.frame(), subset(), order()

alcune funzioni utili per creare grafici come: plot(), barplot(), pie(), title(), lines(), box(), axis()

uno di tanti dataset di esempio (in particolare, mtcars) già pronti da caricare nello spazio di lavoro di R per esercitarsi

Svolgimento corso R online (capitolo 6)


Nel capitolo 6 (Liste) imparerai a creare e maneggiare una lista, selezionarne alcuni elementi o assegnare dei nomi ai suoi elementi. Contrariamente ai vettori, le liste in R possono contenere tipi di dato differenti tra loro. (a proposito: conosci un altro tipo di oggetto in R che ti permette di immagazzinare tipi diversi / non omogenei?)

**segnalazione di un errore nel capitolo 6!!!!**

Alla schermata "Creare una lista con i nomi (2)", nelle istruzioni dell'esercizio c'è un piccolo errore.

Dove dice:

Non dimenticarti di assegnare i nomi agli elementi della lista (i nomi da assegnare sono nome_film, attori e reviews).

Tu leggi come fosse scritto:

Non dimenticarti di assegnare i nomi agli elementi della lista (i nomi da assegnare sono nome_film, actors e reviews).

Per riprendere il corso di R su DataCamp al capitolo 5 --> segui i passaggi illustrati nella pagina web del Modulo 2 alla sezione intitolata

***Come riprendere il corso di Introduzione a R su DataCamp da dove lo si aveva interrotto***

Sfide interattive

Ottenere aiuto in R

Come abbiamo detto, R è un linguaggio molto ben documentato e supportato da una vasta e attiva comunità di utenti.

A questo link puoi trovare un guida (in inglese) che illustra i diversi modi per chiedere aiuto in R.

Qui di seguito riassumerò due approcci molto comuni:


Per trovare aiuto su come usare una data funzione di R ***di cui conosci il nome*** (esempio: per sapere quali argomenti la funzione si aspetta,  e quali parametri posso usare per modificarne il comportamento) posso accedere alla documentazione digitando nella console di R il comando:

?\<nome della funzione\>

es. ?row.names

NOTA: la documentazione di una funzione cui si accede come visto qui sopra (?\<nome_della_funzione\>) non è sempre di facile lettura. Ma non ti spaventare!!! E soprattutto, tra le tante informazioni disponibili, orientati in particolare su:

la sessione Description, ti fornisce una breve descrizione, in forma discorsiva, di cosa fa la data funzione

la sessione Arguments, ti illustra i diversi argomenti che prende in input la data funzione

la sessione Examples (in fondo alla pagina), ti illustra esempi di uso della data funzione


Alternativamente, e nel caso in cui non conosci già il nome della funzione R da usare per un dato scopo:

 

Puoi trovare aiuto in rete utilizzando un motore di ricerca (es. [https://www.google.com/](https://www.google.com/)), specificando con le giuste parole chiave il tuo dubbio / problema.

Prova ad esempio a cercare su Google:

come faccio a rinominare righe e colonne di un data.frame in R?

--> Sei soddisfatto del risultato? Hai trovato la risposta al tuo dubbio?

Meglio ancora se riesci a formulare la tua domanda in inglese: avrai accesso ad un numero ancor più vasto di documenti tecnici e discussioni in forum specializzati


Altra via, digitando nella console di R il comando: 

help.search() o il suo sinonimo ??

es. help.search("expression") o ??"expression"

Avrai in risposta un elenco di tutti i pacchetti R che contengono funzioni (riportati come nome_pacchetto::nome_funzione) nella cui documentazione è presente la/le parola/e chiave da te inserite per la ricerca di aiuto, insieme ad una minima descrizione di scopo della data funzione R.

(Installare e) caricare un pacchetto R

I pacchetti di R sono delle ulteriori collezioni di funzioni, rispetto alle funzioni di base già disponibili in qualunque console di R, dedicate a svolgere un certo compito.


Esistono al momento oltre 20,000 pacchetti di R disponibili per essere installati sul proprio PC, e caricati all'occorrenza nella  propria sessione di lavoro di R. L'elenco completo dei pacchetti si può trovare qui: Table of available packages, sorted by name

Per utilizzare un pacchetto di R sul nostro computer, ci servirà di seguire 2 passaggi:


installare il pacchetto sul nostro PC con la funzione R install.packages() 

es. install.packages("A3")	# nota il nome del pacchetto messo tra virgolette

NOTA 1: questo lo possiamo fare SOLO sulla nostra console R locale, dove abbiamo permessi adeguati

NOTA 2: questo passaggio sarà necessario solo la prima volta che usiamo un nuovo pacchetto


caricare il dato pacchetto nella propria sessione di lavoro di R,  con la funzione library():

es. library(A3)                             # nota il nome del pacchetto scritto senza virgolette

NOTA: questo passaggio sarà necessario ogni volta che vorremo utilizzare le funzioni di un dato pacchetto R nella nostra sessione di lavoro


Un paio di riferimenti utili:

Un comando utile per controllare quali pacchetti abbiamo caricato nella nostra sessione di lavoro è: sessionInfo()

Prova ad esempio a digitare il seguente comando di R nella console di R che utilizzi di solito:

sessionInfo()

Ogni pacchetto di R ha una pagina dedicata, dove è anche possibile scaricare la documentazione che ci insegna ad usarlo. Es.: fai click sul nome A3 nell'elenco di pacchetti che trovi a questo link (Table of available packages, sorted by name) per accedere alla pagina di documentazione del pacchetto A3

NOTA: per scoprire come installare e caricare pacchetti in R, avremmo anche potuto applicare quanto appena imparato. E cioé, chiedere a un motore di ricerca per trovare aiuto. Prova ad esempio a cercare su [https://www.google.com/](https://www.google.com/) la seguente combinazione di parole:

come caricare e installare pacchetti in R

oppure in inglese:

how to install / load packages in R

Ha funzionato la ricerca? Hai trovato risultati utili per risolvere il tuo dubbio (cioé, come installare e caricare pacchetti R)?


Suggerimento extra: se leggere la documentazione non ti piace, dai uno sguardo anche ai risultati della tua ricerca trovati tra i video. Ad esempio, su youtube puoi trovare tantissimi tutorial su vari aspetti di R, a diversi livelli di complessità. Qui c'è un esempio di questi video tutorial.

Sfida tremendissima

Premessa: 

Per risolvere questa sfida tremendissima ti servirà una console di R. Se stai lavorando da casa e non ne hai una installata in locale sul tuo PC, puoi usare quella del corso di DataCamp. 

Per dimostrarmi fin dove ti sei spinto nella soluzione di questa sfida, copia e incolla il codice R da te generato in un file di testo (possibilmente un file di testo semplice) e inviamelo per email, in modo che io possa eseguirlo in R e gustarmi il risultato! Usa delle righe di commento nel tuo codice per rispondere alle domande che troverai qua e la qui sotto.


Pronti? Via!

**********************************************************************************************

##  1. DATI

**********************************************************************************************

### Carica i dati presenti nel data.frame chiamato USArrests

# (suggerimento: USArrests è un altro dataset di esempio di R, si carica come caricavi nel modulo scorso il dataset mtcars)


### Ora stampa a video le prime 8 righe di questo data.frame 

# (suggerimento: per stamparne proprio 8 dovrai vedere la documentazione della funzione di R che ti verrà in mente di usare)


### Ora estrai la nona riga di questo data.frame


### Infine, estrai i valori riportati nelle colonne 2, 3, e 4 per le righe 5, 6 e 7 di questo data.frame

**********************************************************************************************


**********************************************************************************************

##  2. CREAZIONE DI UN GRAFICO DEI DATI

**********************************************************************************************

### Crea un plot della variabile 'Murder' del data.frame chiamato 'USArrests'. Fai in modo che nel grafico compaia un titolo in colore blu con su scritto "Omicidi nel 1973 negli USA per 100,000 abitanti" 

**********************************************************************************************