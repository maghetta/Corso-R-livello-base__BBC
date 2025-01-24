---
title: Modulo 2
---

![modulo2](images/modulo2/modulo2.jpg)

<br>

## Argomenti

- Matrici in R

<hr>

## Obiettivi conoscitivi

Al termine di questa attività dovresti essere in grado di:

- descrivere cos'è e come si crea una matrice in R

- assegnare i nomi alle righe e/o alle colonne di una matrice

- calcolare la somma degli elementi di ogni riga o di ogni colonna di una matrice numerica

- aggiungere una o più colonne ad una matrice

- aggiungere una o più righe ad una matrice

- ispezionare il contenuto del tuo spazio di lavoro (workspace)

- selezionare gli elementi di una matrice

- effettuare delle operazioni matematiche (es. +, -, /, \*) con matrici numeriche


## Durata e programma dell'attività:

2 ore;

<table border="1" width="700">
	<tr>
		<td>[30']</td>
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa</td>
        </tr>
	<tr>
		<td>[30']</td>
		<td>Esercizi</td>
	</tr>
	<tr>
		<td>[40']</td>
		<td>Svolgimento tutorial: Matrici in R</td>		
	</tr>
	<tr>
		<td>[20']</td>
		<td>Sfide interattive sul contenuto del tutprial</td>		
	</tr>
</table>


<br>

<hr>


### Ricapitolando: vediamo insieme cosa abbiamo imparato a fare la volta scorsa

1. Abbiamo cominciato ad usare la console di R


<table>
	<tr>
		<td><iframe src="https://rdrr.io/snippets/embed/" width="800" height="600"></iframe></td>
	</tr>
	<tr>
		<td>Emulatore della console di R disponibile gratuitamente online al link: <a href="https://rdrr.io/snippets/"><(https://rdrr.io/snippets/)</a></td>
	</tr>
</table>

Nota: 

- un editor di testo non è strettamente fondamentale. Puoi anche digitare i tuoi comandi R direttamente nella console interattiva e premere invio per eseguirli. Però i comandi digitati direttamente in console verranno dimenticati quando chiudi la sessione di lavoro.

- di solito un codice R per svolgere un certo obiettivo lo si costruisce avendo aperti davanti un editor di testo e la console di R. Sulla console di R puoi testare il comando (esempio: il comando per creare un vettore), una volta trovata la riga di codice che funziona, la puoi annotare nell'editor di testo per conservarla. E magari integrarla con una riga di commento che ne spieghi il senso. Il codice così costruito nell'editor di testo lo puoi salvare con un nome (es. "mio_primo_script.R") per conservarlo sul tuo PC. L'estensione del nome del file ".R" (in maiuscolo o in minuscolo) viene convenzionalmente usato per specificare che quel dato file di testo semplice contiene istruzioni scritte nel linguaggio R ed eseguibili se lette da un interprete R.


2. Abbiamo cominciato ad usare R in RStudio

![modulo1](images/modulo2/1_rstudiopanels.jpg)

<br>

Schema della interfaccia di lavoro su RStudio. Nella figura qui sopra (presa da [questo ebook di R della Prof.ssa Michela Cameletti](https://bookdown.org/michela_cameletti/sapf2021_rlab_appunti/intro.html)), sono indicate le funzioni principali dei quattro riquadri che compongono l'interfaccia.




3. **Abbiamo conosciuto l'utilizzo di base della console di R, come un semplice calcolatore**
Ad esempio, quanto fa: (1-(5-4))+\{2^10/2^7-(6-(3\*2-10\/5))\}  ?

4. **Abbiamo imparato a creare una variabilein R**

A proposito: cos'è una variabile? E come la creo in R?

5. **Abbiamo conosciuto i primi due tipi di "oggetto" di R: il vettore e il fattore**

A proposito: in cosa si somigliano e in cosa si differenziano, ad esempio, un vettore e un fattore?

E, sapresti fare un esempio di variabile fattoriale nominale? e un esempio di variabile fattoriale ordinale?

Una perla di saggezza: in R tutto è un oggetto (sia esso un vettore, un fattore, o... altri oggetti che conosceremo nelle prossime puntate). A proposito: i nomi di un vettore, che tipo di oggetto sono?

6. **Qua e là tra i capitoli abbiamo anche conosciuto**

- alcuni esempi di funzioni disponibili in R (quali: c(), class(), mean(), factor(), levels(), summary() )

- come riconoscere una funzione in un codice R (a proposito, come la riconosci una funzione? che caratteristica ha?)

- l'importanza delle parentesi e il loro diverso significato in R (quando hai visto una parentesi tonda? quando una parentesi quadra?)

- il simbolo "<-" (che chiamiamo di assegnazione) per creare una variabile (la scelta del nome di una variabile è obbligato o a piacere?)

- l'esistenza di "parole speciali" utilizzate in R, come ad esempio TRUE, FALSE, NA

<hr>


**Svolgimento del tutorial: Matrici in R**

<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Matrici_in_R)


- In questo tutorial imparerai come creare matrici e come effettuare operazioni di base su di esse. 

<hr>


<hr>

