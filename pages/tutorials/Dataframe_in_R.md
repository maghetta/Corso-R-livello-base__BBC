---
title: Data frame in R
---

```markdown

# Introduzione ai data.frame in R
# ---------------------------------
# In R, un data.frame è una struttura dati simile a una tabella, dove le colonne possono contenere dati di tipo diverso (numerico, carattere, fattori, ecc.).
# È ideale per gestire dataset strutturati, come un elenco di piante con informazioni su nome, tipo, altezza, ecc.

# Creazione di un data.frame con informazioni su alcune piante da giardino
piante <- data.frame(
  Nome = c("Rosa", "Lavanda", "Girasole", "Tulipano", "Orchidea"),  # Colonna di caratteri
  Tipo = c("Arbusto", "Erbacea", "Erbacea", "Bulbosa", "Epifita"),   # Colonna di caratteri
  Altezza_cm = c(120, 60, 180, 40, 50),  # Colonna numerica
  Perenne = c(TRUE, TRUE, FALSE, FALSE, TRUE)  # Colonna logica (TRUE/FALSE)
)

# Visualizzare le prime righe del data.frame
head(piante)  # Mostra le prime 6 righe (di default) del dataset

# Visualizzare le ultime righe del data.frame
tail(piante)  # Mostra le ultime 6 righe (di default)

# Esaminare la struttura del data.frame
str(piante)   # Fornisce informazioni sui tipi di dati contenuti in ogni colonna

# Estrazione di un sottoinsieme: selezionare solo le piante perenni
piante_perenni <- subset(piante, Perenne == TRUE)
piante_perenni  # Stampa il sottoinsieme delle piante perenni

# Ordinare il dataset in base all'altezza (in ordine crescente)
piante_ordinate <- piante[order(piante$Altezza_cm), ]
piante_ordinate  # Mostra il dataset ordinato per altezza

# Ordinare il dataset in base all'altezza in ordine decrescente
piante_ordinate_desc <- piante[order(-piante$Altezza_cm), ]
piante_ordinate_desc  # Mostra il dataset ordinato in ordine decrescente



```
