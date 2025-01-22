---
title: Vettori in R
---

```markdown
# Tutorial introduttivo all'oggetto vettore in R

# Tutorial R: Pianificazione dei Viaggi con i Vettori

# Introduzione
# Questo tutorial ti guiderà attraverso l'analisi della pianificazione dei tuoi viaggi 
# utilizzando i vettori in R. Imparerai a:
# - Creare e manipolare vettori
# - Assegnare nomi agli elementi
# - Effettuare calcoli aritmetici e confronti
# - Selezionare elementi specifici

# Creazione di vettori
# I vettori sono array monodimensionali che possono contenere dati numerici, 
# caratteri o logici. Utilizziamo la funzione `c()` per creare vettori.

# Esempi di vettori:
numeric_vettore <- c(1, 2, 3)
character_vettore <- c("a", "b", "c")

# Raccogliamo le distanze e i costi settimanali per diversi spostamenti:
vettore_distanze <- c(140, 50, 120, 300, 240) # in chilometri
vettore_costi <- c(30, 10, 50, 100, 80) # in euro

# Assegnazione dei nomi agli elementi
# Usiamo la funzione `names()` per etichettare gli elementi dei vettori con i giorni della settimana.
giorni <- c("Lunedì", "Martedì", "Mercoledì", "Giovedì", "Venerdì")
names(vettore_distanze) <- giorni
names(vettore_costi) <- giorni

# Calcolo dei costi totali giornalieri
# Dividiamo i costi per le distanze per ottenere il costo medio per chilometro.
costo_medio_km <- vettore_costi / vettore_distanze

# Calcolo delle distanze e dei costi totali settimanali
# Utilizziamo la funzione `sum()` per calcolare le somme totali.
totale_distanze <- sum(vettore_distanze)
totale_costi <- sum(vettore_costi)
costo_totale_medio <- totale_costi / totale_distanze

# Confronto tra giorni con costi più alti e più bassi
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
