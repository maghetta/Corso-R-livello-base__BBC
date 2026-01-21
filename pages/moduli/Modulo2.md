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
		<td>Ricapitolando: vediamo insieme cosa abbiamo imparato a fare fin qui</td>
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


### Ricapitolando: vediamo insieme cosa abbiamo imparato a fare fin qui
1. Abbiamo cominciato ad usare la console di R

2. Abbiamo cominciato ad usare R in RStudio

3. **Abbiamo conosciuto l'utilizzo di base della console di R, come un semplice calcolatore**
Ad esempio, quanto fa: (1-(5-4))+\{2^10/2^7-(6-(3\*2-10\/5))\}  ?

4. **Abbiamo imparato a creare una variabilein R**

A proposito: cos'è una variabile? E come la creo in R?

5. **Abbiamo conosciuto i primi due tipi di "oggetto" di R: il vettore e il fattore**

A proposito: in cosa si somigliano e in cosa si differenziano, ad esempio, un vettore e un fattore?

E, sapresti fare un esempio di variabile fattoriale nominale? e un esempio di variabile fattoriale ordinale?

Una perla di saggezza: in R tutto è un oggetto (sia esso un vettore, un fattore, o... altri oggetti che conosceremo nelle prossime puntate). A proposito: i nomi di un vettore, che tipo di oggetto sono?

6. **Qua e là tra i tutorial abbiamo anche conosciuto**

- alcuni esempi di funzioni disponibili in R (quali: ls(), c(), class(), mean(), factor(), levels(), summary() )

- come riconoscere una funzione in un codice R (a proposito, come la riconosci una funzione? che caratteristica ha?)

- l'importanza delle parentesi e il loro diverso significato in R (quando hai visto una parentesi tonda? quando una parentesi quadra?)

- il simbolo "<-" (che chiamiamo di assegnazione) per creare una variabile (la scelta del nome di una variabile è obbligato o a piacere?)

- l'esistenza di "parole speciali" utilizzate in R, come ad esempio TRUE, FALSE, NA

<hr>


**Svolgimento del tutorial: Matrici in R**

<br>Puoi visualizzare o scaricare il tutorial da [qui](https://maghetta.github.io/Corso-R-livello-base__BBC/Matrici_in_R)


- In questo tutorial imparerai come creare matrici e come effettuare operazioni di base su di esse. 

___

**Esercizi**
<br>

1. Scrivi un comando in R per creare una matrice di 3 righe e 5 colonne, denominata M,
	che contenga i numeri interi da 16 a 30

2. Nomina righe e colonne della matrice M che hai appena creato, utilizzando le prime
   	tre lettere minuscole e le prime cinque maiuscole dell'alfabeto, rispettivamente.

3. Scrivi il comando R utile per estrarre la 3a riga dalla matrice M sopra creata

4. Scrivi il comando per estrarre le prime 2 righe e le colonne 1 e 3 dalla matrice M

5. Sapresti scrivere due comandi alternativi per estrarre le colonne 1, 2 e 5 dalla matrice M?
  
6. Decidi se la seguente affermazione è VERA o FALSA:
<br>*Le matrici in R possono contenere dati di tipo diverso (es. numeri e testo), purchè in colonne diverse*

7. che risultato da il seguente comando in R applicato a due matrici M1 e M2?
<br>*rbind(M1, M2)*

8. se G è una matrice numerica, come fai in R a moltiplicare per 2 tutti i suoi valori?

9. con quale dei seguenti comandi di R puoi aggiungere il vettore V come nuova colonna di una matrice M?
	- *M <- rbind(V,M)*
	- *M <- c(V, M)*
	- *M <- cbind(M, V)*
	- *nessuno di questi*

10. La funzione dim() di R ti permette di conoscere le dimensioni di un oggetto multidimensionale, come ad esempio una matrice (che ha due dimensioni). Considerando la seguente matrice: *m <- matrix(-31:100, ncol=6)*, applica la funzione dim() alla matrice m per vedere che dimensioni ha. Poi, calcola il valore medio della sua 5a riga.

