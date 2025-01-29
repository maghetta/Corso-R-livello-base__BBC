---
title: Liste in R
---

```markdown

## Introduzione alle liste in R

# In questo tutorial conoscerai l'ultimo tipo di oggetto fondamentale di R: le `liste`. Imparerai
# come crearle, e come manipolarle. Ad esempio come accedere ai suoi elementi, o npminarli.  
# Le liste in R sono oggetti flessibili che possono contenere come propri elementi diversi tipi di dati,
# inclusi vettori, matrici, data frame e persino altre liste.

## Creare una lista in R
# In R puoi creare una lista utilizzando il comando `list()`.
# Creiamo ad esempio una lista per organizzare gli ingredienti di una ricetta:

# Definiamo gli ingredienti principali come vettore
ingredienti <- c("Farina", "Uova", "Latte", "Zucchero", "Burro")

# Creiamo una matrice con le quantità degli ingredienti per 1 o 2 porzioni
quantita <- matrix(c(200, 2, 250, 100, 50, 400, 4, 500, 200, 100), 
                   nrow = 2, byrow = TRUE, 
                   dimnames = list(c("Dose 1", "Dose 2"), ingredienti))

# Creiamo un data frame con le informazioni nutrizionali per ogni ingrediente
# (per 100g):
info_nutrizionali <- data.frame(Ingrediente = ingredienti,
                                Calorie = c(364, 155, 42, 387, 717),
                                Proteine = c(10, 13, 3, 0, 1))

# Creiamo infine una lista che raccolga tutti questi dati:
ricetta <- list(ingredienti = ingredienti, 
                quantita = quantita, 
                info_nutrizionali = info_nutrizionali)

## Ispezionare una lista
# Analogamente a quanto visto con i data frame, possiamo utilizzare la funzione `str()`
# per ispezionare la struttura di una lista.

#--> domanda per te: prova ad applicare la funzione `str()` per ispezionare la struttura
# della lista *ricetta* appena creata.


## Nominare gli elementi di una lista
# Per dare un nome agli elementi di una lista, possiamo tornare ad utilizzare
# la funzione `names()` già incontrata con i `vettori` e i `fattori`.


## Selezione di elementi da una lista
# Possiamo accedere agli elementi della lista utilizzando sempre le parentesi `[]`,
# ma con una sintassi un pò diversa, che riflette la struttura delle liste.
# Vi ricordate quando abbiamo detto che tutto in R è un oggetto?
# Ecco, per accedere ad un elemento di una lista, dovremo utilizzare doppie parentesi `[[]]`

# Ad esempio, per accedere all'oggetto 


 o il simbolo $
print(ricetta[["ingredienti"]])  # Stampa il vettore degli ingredienti
print(ricetta$quantita)  # Stampa la matrice delle quantità

# Selezioniamo un singolo valore all'interno di un elemento della lista
print(ricetta$quantita[1, "Farina"])  # Quantità di farina nella prima dose

# Aggiungere un nuovo elemento alla lista
# Aggiungiamo il tempo di cottura della ricetta
ricetta_completa <- c(ricetta, tempo_cottura = 30)

# Stampiamo la struttura della nuova lista
str(ricetta_completa)



```
