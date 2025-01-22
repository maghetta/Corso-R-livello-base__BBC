---
title: Vettori in R
---

```markdown
# Tutorial introduttivo all'oggetto di classe vettore in R

# Introduzione
# Questo tutorial ti guiderà nella scoperta dei vettori in R. Più precisamente, imparerai a:
# - Creare e manipolare vettori
# - Assegnare nomi agli elementi
# - Effettuare calcoli aritmetici e confronti
# - Selezionare specifici elementi di un vettore

# Creazione di vettori
# I vettori sono array monodimensionali che possono contenere dati di tipo numerico, 
# carattere o logico. 
# Per creare un vettore in R abbiamo a disposizione la funzione `c()`, versione essenziale che sta per `concatenate`.

# A proposito: in R, **una funzione** è un blocco di codice progettato per eseguire un compito specifico.
# Le funzioni sono strumenti fondamentali per ridurre la duplicazione del codice, migliorare la leggibilità
# e organizzare le operazioni in modo modulare. Una funzione in R si riconosce sintatticamente
# perché il suo nome è immediatamente seguito da parentesi tonde, che possono contenere eventuali argomenti
# da passare alla funzione. Ad esempio: `sum(7, 2)` restituisce la somma dei due numeri forniti come input.

# Esempi di vettori:
vettore_numerico <- c(1, 2, 3)
vettore_carattere <- c("a", "b", "c")

# Ad esempio, creiamo un vettore  delle distanze e uno dei costi settimanali per diversi spostamenti
# fatti durante un viaggio:
vettore_distanze <- c(140, 50, 120, 300, 240) # in chilometri
vettore_costi <- c(30, 10, 50, 100, 80) # in euro

# Assegnazione dei nomi agli elementi di un vettore
# Usiamo la funzione `names()` per assegnare un nome agli elementi di un vettore.
# Ad esempio, potremmo nominare gli elementi dei vettori appena creati con i giorni della settimana.
giorni <- c("Lunedì", "Martedì", "Mercoledì", "Giovedì", "Venerdì")
names(vettore_distanze) <- giorni
names(vettore_costi) <- giorni

# Operazioni con i vettori

# Dividiamo i costi per le distanze utilizzando l'operatore `/`. La divisione tra due vettori
# viene effettuata elemento per elemento, ovvero il primo elemento del primo vettore
# viene diviso per il primo elemento del secondo vettore, il secondo elemento per il secondo, e così via.
# Ad esempio, se `vettore_costi` è c(30, 10, 50) e `vettore_distanze` è c(140, 50, 120),
# il risultato sarà c(30/140, 10/50, 50/120).
costo_medio_km <- vettore_costi / vettore_distanze

#--> domanda per te: cosa succede invece in questo comando R?
vettore_costi / 5


# Utilizziamo ora la funzione `sum()` per calcolare le somme totali.
totale_distanze <- sum(vettore_distanze)
totale_costi <- sum(vettore_costi)
costo_totale_medio <- totale_costi / totale_distanze

# Per comprendere meglio le operazioni appena compiute, stampa a video
# il contenuto della variabile risultato
# Per stampare il contenuto di una variabile puoi usare la funzione `print()`
# dando come argomento il nome della variabile di cui vuoi stampare il contenuto.
# Alternativamente, puoi anche digitare semplicemente il nome della variabile e premere invio.

#--> domanda per te: prova a utilizzare la funzione `print()` per stampare a video
# il contenuto della variabile totale_distanze

# Operatori di Confronto applicati ai vettori

# Confrontiamo i giorni con costi più alti e più bassi
# Verifichiamo quale giorno ha il costo massimo e minimo.
giorno_costo_max <- giorni[which.max(vettore_costi)]
giorno_costo_min <- giorni[which.min(vettore_costi)]

# Selezione degli elementi dai vettori
# Usiamo gli indici o i nomi per selezionare elementi specifici.
distanze_metà_settimana <- vettore_distanze[2:4]
costi_metà_settimana <- vettore_costi[2:4]
distanze_inizio_settimana <- vettore_distanze[c("Lunedì", "Martedì", "Mercoledì")]
media_distanze_inizio <- mean(distanze_inizio_settimana)

# Selezione basata su condizioni
# Filtriamo i giorni con distanze superiori a 100 km.
vettore_selezione <- vettore_distanze > 100
giorni_distanze_lunghe <- vettore_distanze[vettore_selezione]

# Ripetiamo la selezione per i costi.
vettore_selezione <- vettore_costi > 50
giorni_costi_alti <- vettore_costi[vettore_selezione]

# Risultati finali
print("Costo medio per chilometro:")
print(costo_medio_km)
print("Totale distanze settimanali:")
print(totale_distanze)
print("Totale costi settimanali:")
print(totale_costi)
print("Giorno con costo massimo:")
print(giorno_costo_max)
print("Giorno con costo minimo:")
print(giorno_costo_min)
print("Media distanze inizio settimana:")
print(media_distanze_inizio)
print("Giorni con distanze lunghe:")
print(giorni_distanze_lunghe)
print("Giorni con costi alti:")
print(giorni_costi_alti)




```
