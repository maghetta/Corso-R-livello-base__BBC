---
title: Modulo 3
---

![modulo3](images/modulo3/modulo3.jpg)

<br>

## Argomenti

- *Data Frame in R*

- *Primi passi con i Grafici in R*

<br>
<br>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è e come si crea un *data frame* in R

- elencare almeno una differenza tra matrici e data frame in R

- caricare un data frame di dati di esempio (*mtcars*) nella console R 

- stampare a video nella console di R le prime o le ultime righe di un data frame

- ispezionare la struttura di un data frame

- creare un data frame in R

- selezionare gli elementi di un data frame (es. 1+ righe e/o 1+ colonne) utilizzando l'indice numerico di righe e colonne

- selezionare gli elementi di un data frame (es. 1+ righe e/o 1+ colonne) utilizzando il nome di righe e colonne

- selezionare una colonna di un data frame utilizzando il simbolo $

- selezionare un sottinsieme di dati di un data frame (es. 1+ righe o 1+ colonne) utilizzando un vettore logico

- riordinare le righe di un data frame (es. secondo valori crescenti o decrescenti di un dato vettore)
  
- creare uno scatterplot in R
  
- creare un barplot in R

- creare un grafico a torta in R

- esportare un grafico creato in R salvandolo come file di immagine sul PC

- modificare caratteristiche di un grafico, quali colore, etichette degli assi o simboli in uno scatterplot

- aggiungere una linea orizzontale o verticale ad un grafico

- aggiungere titolo o legenda ad un grafico

<br>

## Durata e programma dell'attività:

3 ore;

<table border="1" width="700">
	<tr>
		<td>[15']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
	</tr>
	<tr>
		<td>[50']</td>
		<td>Svolgimento del tutorial Data frame in R</td>		
	</tr>
	<tr>
		<td>[20']</td>
		<td>Sfide interattive sul contenuto del tutorial</td>		
	</tr>
	<tr>
	<td colspan="2">pausa 10'</td>
	</tr>
	<tr>
		<td>[45']</td>
		<td>Svolgimento del tutorial ABD Grafici in R</td>		
	</tr>
	<tr>
		<td>[30']</td>
		<td>Svolgimento sfida tremendissima (scorri questa pagina per trovarla)</td>		
	</tr>
	<tr>
		<td>[10']</td>
		<td>Spazio per domande e curiosità</td>		
	</tr>
</table>


<hr>

Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

<br>



1. Abbiamo conosciuto la terza classe di "oggetto" di R: le *Matrici*

A proposito: secondo te, posso avere colonne di classe diversa in una matrice? Perché (perché si o perché no)?

<br>

3. Qua e là tra i tutorial abbiamo anche conosciuto

diversi altri esempi di funzioni disponibili in R, quali: *matrix(), rownames(), colnames(), rowSums(), colSums(), ls(), cbind(), rbind()*

<hr>

## Svolgimento tutorial Data frame in R

<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Dataframe_in_R)

In questo tutorial imparerai a creare un data frame, selezionare da esso solo alcuni elementi di interesse, e ordinarlo in funzione di certe variabili.
Questo tipo di oggetto, che può ospitare dati eterogenei nelle sue diverse colonne, è il tipo di oggetto R di uso più comune poiché si presta 
ad immagazzinare la maggior parte dei set di dati con cui ci si possa trovare a lavorare. Dati di lavoro infatti spesso includono colonne di 
varia natura (ad esempio, sia dati di tipo numerico che di tipo categorico).


<hr>




<hr>

## Svolgimento tutorial Primi passi con i Grafici in R

<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/ABC_Grafici_in_R)

<hr>

<span style="color:red;">Sfida tremendissima</span>

**Premessa:**
<br>
Per poterti mettere alla prova con questa sfida tremendissima **ti servirà una console di R** installata sul tuo PC (ad esempio, quella integrata nell'interfaccia di *RStudio*).

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


Beh, già se sei arrivato a leggere fin qui ti faccio i complimenti per il coraggio e la tenacia!!!
