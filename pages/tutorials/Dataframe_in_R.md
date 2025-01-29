---
title: Data frame in R
---

```markdown

# Introduzione ai data.frame in R
# ---------------------------------

# In questo tutorial apprenderai cosa caratterizza l'oggetto data frame in R, come crearne uno,
# come selezionare solo le parti di interesse e come ordinarlo in funzione di certe variabili.


# In R, un data frame è una struttura dati simile ad una tabella, dove le colonne possono contenere dati
# di tipo diverso (ad esempio, numerico, categorico, logico, ecc.).
# Nella maggior parte dei casi, è l'oggetto ideale per gestire set di dati, che spesso effettivamente
# contengono variabili di tipo diverso, organizzati in colonne (variabili) e righe (osservazioni).


# Per creare un data frame in R, utilizziamo la funzione `data.frame()`, come nell'esempio che segue,
# dove creerai un data frame che contiene un elenco di piante con relative informazioni
# su nome, tipo, altezza e altro:

piante <- data.frame(
  Nome = c("Rosa", "Lavanda", "Girasole", "Tulipano", "Orchidea"),   # dato di tipo carattere
  Tipo = c("Arbusto", "Erbacea", "Erbacea", "Bulbosa", "Epifita"),   # dato di tipo categorico
  Altezza_cm = c(120, 60, 180, 40, 50),                              # dato di tipo numerico
  Perenne = c(TRUE, TRUE, FALSE, FALSE, TRUE)                        # dato di tipo logico
)

## Ispezionare il contenuto

# Per ispezionare il contenuto di un data frame, possiamo utilizzare le funzioni `head()` e `tail()`
# per visualizzarne rispettivamente le prime o le ultime righe.

head(piante)  # Mostra le prime 6 righe (di default) del dataset

#--> domanda per te: prova ora a visualizzare le ultime 6 righe dello stesso data frame.

# Un'altra funzione utile per esaminare un data frame con cui stiamo lavorando è `str()`
# che ci restutisce una panoramica della sua struttura e composizione.
# Osserva ad esempio le informazioni restituite dal seguente comando:

str(piante)   #--> domanda per te: quali informazioni ottieni?


## Nominare righe e colonne
# Anche nel caso di data frame, possiamo attribuire nomi sia alle colonne che alle righe
# di un data frame, sia mentre lo creiamo (come nell'esempio qui sopra,
# dove abbiamo direttamente nominato le colonne nel comando `data.frame()`),
# sia successivamente ricorrendo alle funzioni `rownames()` o `colnames()`

# Come già visto, i comandi `rownames()` e `colnames()` possono essere usati sia per
# visualizzare i nomi rispettivamente di righe e colonne, sia per modificarli.

#--> domanda per te: le righe del data frame *piante* hanno dei nomi?

# --> domanda per te: utilizzando la funzione `rownames()`, attribuisci alle
# righe del data frame *piante* le prime cinque lettere minuscole dell'alfabeto.

# --> domanda per te: utilizzando la funzione `colnames()`, modifica
# il nome della 3a colonna del data frame *piante* da `Altezza_cm` a `Altezza`


## Selezione di elementi di interesse

# Analogamente a quanto visto con gli oggetti di R appresi nei precedenti tutorial,
# potrai estrarre un sottoinsieme di dati di interesse, specificando opportunamente
# tra le parentesi `[]` le righe e le colonne di tuo interesse. 

# --> domande per te: Applicando le modalità gia usate per estrarre sottoinsiemi
# di dati dall'oggetto matrice, prova ora a scrivere i comandi R opportuni per
# selezionare dal data frame *piante*:

# 1. le prime 3 righe e tutte le colonne

# 2. solo le colonne 1, 2 e 5

# 3. solo l'altezza della pianta corrispondente al 4° rigo

# 4. i primi 3 valori della variabile "Nome"

# 5. solo le piante perenni 


# Oltre ai modi già visti per estrarre elementi
# basati su indici numerici delle posizioni
# e/o i nomi delle righe o colonne di interesse,
# per i data frame in R esiste una scorciatoia nel caso
# in cui vogliamo estrarre una variabile (cioé, una colonna).
# La sintassi accorciata specifica il nome della colonna
# da estrarre dopo il simbolo `$`, come ad esempio:

piante$Perenne

#--> domanda per te: prova ora ad estrarre, utilizzando
# la sintassi con il simbolo `$`, la colonna `Nome` dal
# data frame *piante*.


# Da ultimo, per estrarre un sottoinsieme di dati
# da un data frame, possiamo usare la funzione R `subset()`.
# Se volessimo ad esempio utilizzare questa via per
# estrarre dal data frame *piante* il sottoinsieme delle
# piante perenni, potremmo usare il seguente comando:

piante_perenni <- subset(piante, Perenne == TRUE)

# Nel comando qui sopra:
# - Il **primo argomento**: specifica il data frame da cui
#    si vuole estrarre un sottoinsieme di elementi
# - Il **secondo argomento**: specifica una condizione su
#    cui voler operare la selezione di elementi

#--> domanda per te: stampa a video il contenuto della
# variabile *piante_perenni* per osservare il
# risultato della funzione `subset()`.

#--> domanda per te: prova ora a utilizzare la funzione `subset()`
#  per selezionare dal data frame *piante* il sottoinsieme di piante
#  con altezza superiore a 50 cm.

## Riordinare un data frame secondo i valori di una variabile

# Durante un'analisi di dati, può tornare utile ordinare
# le informazioni a disposizione sulla base di una certa variabile
# contenuta nel set di dati (ad esempio, nel caso di un data frame
# di risultati di un test statistico, potrebbe essere utile
# riordinare i dati per significatività creascente).
# In R, questa operazione può essere effettuata utilizzando
# la funzione `order()`. Questa funzione prende in input un vettore
# e restituisce in output l'ordine da dare agli
# elementi di questo vettore, ossia il modo
# in cui gli elementi dovrebbero essere disposti,
# affinchè questi risultino ordinati in ordine crescente (default).
# Ad esempio, utilizziamo la funzione `order()` per ordinare
# in modo crescente i valori della colonna *Altezza* del data frame *piante*:

order(piante$Altezza)  # ordine numerico crescente

# usiamolo ora per ordinare i valori della colonna *Nome*:

order(piante$Nome)     # ordine alfabetico

# usiamolo infine per ordinare i valori della colonna *Perenne* in ordine decrescente:

order(piante$Perenne, decreasing=TRUE)     # ordine alfabetico

#--> domanda per te: cosa rappresentano i numeri che ottieni in output
# dai comandi digitati qui sopra?

#--> domanda per te: prova a combinare selezione con `[]`
# e il risultato della funzione `order()` per stampare a video
# il data frame *piante* riordinato in base all'altezza (in ordine crescente)

```
