---
title: Modulo 3
---

![modulo3](/images/modulo3/modulo3.jpg)

<br>

## Argomenti di oggi

- *Data Frames in R, cioé il capitolo 5 del [corso di Introduzione a R di DataCamp](https://www.datacamp.com/courses/free-introduction-to-r)*

- *Grafici in R (vedi istruzioni nel box più in basso su questa stessa pagina)*

<br>
<br>

## Obiettivi conoscitivi di oggi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è e come si crea un data.frame in R

- elencare almeno una differenza tra matrici e data.frames in R

- caricare un data.frame di dati di esempio (*mtcars*) nella console R 

- stampare a video nella console di R le prime o le ultime righe di un data.frame

- ispezionare la struttura di un data.frame

- creare un data.frame in R

- selezionare gli elementi di un data.frame (es. 1+ righe e/o 1+ colonne) utilizzando l'indice numerico di righe e colonne

- selezionare gli elementi di un data.frame (es. 1+ righe e/o 1+ colonne) utilizzando il nome di righe e colonne

- selezionare una colonna di un data.frame utilizzando il simbolo $

- selezionare un sottinsieme di dati di un data.frame (es. 1+ righe o 1+ colonne) utilizzando un vettore logico

- riordinare le righe di un data.frame (es. secondo valori crescenti o decrescenti di un dato vettore)  

<br>

## Programma dell'attività di oggi

durata: 6 ore; modalità: presenza

<table border="1" width="700">
	<tr>
		<td>8:30-9:00</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>9:10-10:00</td>
		<td>Svolgimento corso R online (capitolo 5)</td>		
	</tr>
	<tr>
		<td>10:00-10:30</td>
		<td>Sfide interattive sul contenuto del capitolo 5</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>10:30-11:00</td>
		<td>Svolgimento del tutorial sui grafici in R (più in fondo su questa pagina)</td>		
	</tr>
	<tr>
		<td>11:00-12:00</td>
		<td>Svolgimento sfida tremendissima (vedi sotto)</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 45'</td>
	</tr>
	<tr>
		<td>12:45-14:00</td>
		<td>Svolgimento e invio prodotto di lavoro richiesto</td>		
	</tr>
	<tr>
		<td>14:00-14:30</td>
		<td>Conclusioni</td>		
	</tr>
</table>


<hr>

Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

<br>



1. Abbiamo visto un altro modo di accedere ad una console di R per fare i propri esercizi: la console di R del corso di DataCamp

![modulo3_datacamp](images/modulo3/dataCamp1.png)

- Sia l'editor di testo (riquadro in alto a dx della finestra di lavoro di DataCamp) che la console di R (riquadro in basso a dx della finestra di lavoro di DataCamp) possono essere usati anche per svolgere propri esercizi (ad esempio, per scrivere e testare il codice R richiesto come compito alla fine di ciascun modulo di PCTO).

- Ad esempio, nella foto allo schermo riportata qui sopra si può leggere nell'editor un testo indipendete dall'esercizio del corso di DataCamp.

- Per eseguire un codice a proprio piacimento e da te scritto nell'editor di DataCamp (riquadro in alto a dx) --> premi sul tasto "Run Code" e ne vedrai apparire il risultato nella console di R deella stessa schermata di DataCamp  (riquadro in basso a dx)

<br>

2. Abbiamo conosciuto il secondo tipo di "oggetto" di R: la matrice

![modulo3_datacamp](images/modulo3/dataCamp2.png)

A proposito: secondo te, posso avere colonne di classe diversa in una matrice? Perché (perché si o perché no)?

<br>

3. Abbiamo conosciuto il terzo tipo di "oggetto" di R: il fattore

![modulo3_datacamp](images/modulo3/dataCamp3.png)

A proposito, sapresti farmi un esempio di variabile fattoriale nominale? e un esempio di variabile fattoriale ordinale?


4. Qua e la tra i capitoli abbiamo anche conosciuto

diversi altri esempi di funzioni disponibili in R, quali: *matrix(), rownames(), colnames(), rowSums(), colSums(), ls(), mean(), factor(), levels(), summary(), cbind(), rbind()*

<hr>

## Svolgimento corso R online (capitolo 5)


- Nel capitolo 5 (*Data.Frames*) imparerai a creare un data frame, selezionare solo alcuni elementi di esso che ti interessano e ordinarlo in funzione di certe variabili. Questo tipo di oggetto, che può ospitare dati eterogenei nelle sue diverse colonne, è il tipo di oggetto R di uso più comune per immagazzinare la maggior parte dei set di dati con cui ci si può trovare a lavorare, che spesso includono colonne di varia natura (esempio, colonna di dati di tipo numerico alternata a colonna di dati categorici).


<hr>



Per riprendere il corso di R su DataCamp al capitolo 5 --> segui i passaggi illustrati nella [pagina web del Modulo 2](pages/moduli/modulo2.md) alla sezione intitolata

***

***Come riprendere il corso di Introduzione a R su DataCamp da dove lo si aveva interrotto***

<hr>

Grafici in R

<hr>

**Leggi attentamente** la guida su come creare grafici con R che trovi qui: [https://www.html.it/pag/67232/grafici-con-r/](https://www.html.it/pag/67232/grafici-con-r/)

Vedrai che la guida include dei **blocchi di codice R** (evidenziati come box su sfondo grigio nella guida): 

- esegui nella console R ciascuno di questi blocchi di codice e fai una foto allo schermo del risultato ottenuto


<hr>

<span style="color:red;">Sfida tremendissima</span>

**Premessa:**
<br>

Per risolvere questa sfida tremendissima **ti servirà una console di R**. Se non ne hai una installata in locale sul tuo PC, **puoi usare quella del corso di DataCamp**. Mentre NON andrà bene l'emulatore che trovi al link [https://rdrr.io/snippets/](https://rdrr.io/snippets/) perché manca di alcune funzioni.


Per dimostrarmi fin dove ti sei spinto nella soluzione di questa sfida, copia e in colla il **codice R da te generato** in un file di testo (possibilmente **un file di testo semplice**) e **inviamelo per email**, in modo che io possa eseguirlo in R e gustarmi il risultato! Usa delle **righe di commento** nel tuo codice per rispondere alle domande che troverai qua e la qui sotto.

<br>

**Pronti? Via!**

<br>

Sicuramente ti sarà capitato in questi anni complicati di vedere uno di quei grafici, in rete o in televisione, che fotografa la situazione in Italia delle vaccinazioni contro il Sars-CoV-2, cioé il virus responsabile della malattia covid-19.

Ebbene, questi dati sulle vaccinazioni effettuate in Italia, direttamente forniti dal Ministero della Salute, sono pubblicamente disponibili in rete e continuamente aggiornati, ad esempio su questa pagina GitHub ([https://github.com/italia/covid19-opendata-vaccini](https://github.com/italia/covid19-opendata-vaccini)).


La bellezza di R nel maneggiare file di dati è che sa andarseli a prendere anche direttamente dalla rete.

Per esempio, i dati più aggiornati sulle vaccinazioni effettuate in Italia sono disponibili in formato csv (comma-separated value) a questo link:

[https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv](https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv)


Li puoi caricare direttamente dalla rete in uno spazio di lavoro R con il seguente comando:

*urlcsv <- "[https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv](https://raw.githubusercontent.com/italia/covid19-opendata-vaccini/master/dati/anagrafica-vaccini-summary-latest.csv)"*

*X <- read.csv(url(urlcsv), header=1)*

1. Comincia la sfida eseguendo le 2 righe di codice qui sopra, così da creare il data.frame X nel tuo spazio di lavoro.

2. Utilizza almeno un paio di funzioni che hai appreso nel modulo di oggi per: ispezionare la struttura del data.frame X e stamparne a video le prime righe (**domanda tremendissima**: *quante variabili sono presenti in questo data.frame?*)

Crea un sottoinsieme di dati chiamato Xmf che contenga solo le colonne "m" e  "f" del data.frame X (**domanda tremendissima**: *che tipo di oggetto è l'oggetto Xmf che hai appena creato?*)

Assegna come nomi delle righe dell'oggetto Xmf i valori della colonna "eta" del data.frame X

Usa un operatore di confronto tra quelli che hai visto nel capitolo 2 del corso di DataCamp per vedere in quale fasce di età ci sono più vaccinati  tra le donne che tra gli uomini

Hai ancora energie??? Allora crea un altro sottoinsieme di dati chiamato Xaltro che contenga solo la colonna "db3" del data.frame X. Assegna come nomi al vettore Xaltro che hai appena creato i valori della colonna "eta" del data.frame X

Fai un grafico a torte di Xaltro (**domanda tremendissima**: quale fascia di età è più rappresentata nella categoria "db3" dei vaccinati ?)


Beh, già se sei arrivato a leggere fin qui ti faccio i complimenti per il coraggio e la tenacia!!! E non vedo l'ora di ricevere il tuo codice :)