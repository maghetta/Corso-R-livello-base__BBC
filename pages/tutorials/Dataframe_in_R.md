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
# Nella maggior parte dei casi, è l'oggetto ideale per gestire set di dati, che spesso contengono 
# variabili di tipo diverso.


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

# 4. solo le piante perenni 




piante_perenni <- subset(piante, Perenne == TRUE)
piante_perenni  # Stampa il sottoinsieme delle piante perenni

# Ordinare il dataset in base all'altezza (in ordine crescente)
piante_ordinate <- piante[order(piante$Altezza_cm), ]
piante_ordinate  # Mostra il dataset ordinato per altezza

# Ordinare il dataset in base all'altezza in ordine decrescente
piante_ordinate_desc <- piante[order(-piante$Altezza_cm), ]
piante_ordinate_desc  # Mostra il dataset ordinato in ordine decrescente



```
