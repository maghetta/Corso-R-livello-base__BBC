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
# È ideale per gestire dataset con più variabili, come un elenco di piante con relative informazioni
# su nome, tipo, altezza, ecc.



# Per creare un data frame in R, utilizziamo la funzione `data.frame()`, come nell'esempio che segue:

piante <- data.frame(
  Nome = c("Rosa", "Lavanda", "Girasole", "Tulipano", "Orchidea"),   # dato di tipo carattere
  Tipo = c("Arbusto", "Erbacea", "Erbacea", "Bulbosa", "Epifita"),   # dato di tipo categorico
  Altezza_cm = c(120, 60, 180, 40, 50),                              # dato di tipo numerico
  Perenne = c(TRUE, TRUE, FALSE, FALSE, TRUE)                        # dato di tipo logico
)

# Per ispezionare il contenuto di un data frame, possiamo utilizzare le funzioni `head()` e `tail()`
# per visualizzare rispettivamente le prime o le ultime righe

head(piante)  # Mostra le prime 6 righe (di default) del dataset

#--> domanda per te: prova ora a visualizzare le ultime 6 righe dello stesso data frame.

# Un'altra funzione utile per esaminare un data frame con cui stiamo lavorando è `str()`
# che ci restutisce una panoramica della sua struttura e composizione.
# Osserva ad esempio le informazioni restituite dal seguente comando:

str(piante)   # Fornisce informazioni sui tipi di dati contenuti in ogni colonna

# Analogamente a quanto visto in Estrazione di un sottoinsieme: selezionare solo le piante perenni
piante_perenni <- subset(piante, Perenne == TRUE)
piante_perenni  # Stampa il sottoinsieme delle piante perenni

# Ordinare il dataset in base all'altezza (in ordine crescente)
piante_ordinate <- piante[order(piante$Altezza_cm), ]
piante_ordinate  # Mostra il dataset ordinato per altezza

# Ordinare il dataset in base all'altezza in ordine decrescente
piante_ordinate_desc <- piante[order(-piante$Altezza_cm), ]
piante_ordinate_desc  # Mostra il dataset ordinato in ordine decrescente



```
