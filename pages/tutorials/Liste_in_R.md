---
title: Liste in R
---

```markdown

# Introduzione alle liste in R
# Le liste in R sono oggetti flessibili che possono contenere diversi tipi di dati, inclusi vettori, matrici, data frame e persino altre liste.

# Creiamo una lista a tema cucina per organizzare gli ingredienti di una ricetta

# Definiamo gli ingredienti principali come vettore
ingredienti <- c("Farina", "Uova", "Latte", "Zucchero", "Burro")

# Creiamo una matrice con le quantità degli ingredienti per due porzioni
quantita <- matrix(c(200, 2, 250, 100, 50, 400, 4, 500, 200, 100), 
                   nrow = 2, byrow = TRUE, 
                   dimnames = list(c("Dose 1", "Dose 2"), ingredienti))

# Creiamo un data frame con le informazioni nutrizionali per ogni ingrediente
info_nutrizionali <- data.frame(Ingrediente = ingredienti,
                                Calorie = c(364, 155, 42, 387, 717),
                                Proteine = c(10, 13, 3, 0, 1))

# Creiamo la lista che raccoglie tutti questi dati
ricetta <- list(ingredienti = ingredienti, 
                quantita = quantita, 
                info_nutrizionali = info_nutrizionali)

# Stampiamo la lista per verificare la struttura
print(ricetta)

# Selezionare elementi da una lista
# Possiamo accedere agli elementi della lista utilizzando i doppi apici [[]] o il simbolo $
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
