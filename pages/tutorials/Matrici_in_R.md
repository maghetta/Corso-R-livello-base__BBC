---
title: Matrici in R
---

```markdown

### **Tutorial: Introduzione all'oggetto di classe `Matrice` in R**

#### **Che cos'è una matrice in R?**
# In R, una matrice è una collezione di elementi dello stesso tipo (numerico, carattere o logico) disposti in un numero fisso di righe e colonne.
# In questo tutorial lavoreremo con matrici bidimensionali, e prenderemo come spunto alcuni dischi famosi dei Pink Floyd

# Per creare una matrice in R, utilizziamo la funzione `matrix()`. Ecco un esempio:

matrix(1:9, byrow = TRUE, nrow = 3)

# **Il primo argomento** (`1:9`) rappresenta la sequenza di elementi da disporre nella matrice.
# **L'argomento `byrow`** specifica se riempire la matrice per riga (`TRUE`) o per colonna (`FALSE`)
# **L'argomento `nrow`** indica il numero di righe della matrice.

#### **Creiamo una matrice di esempio**
# Costruiamo ad esempio una matrice con i dati delle vendite di alcuni mitici album dei Pink Floyd.
# La nostra matrice avrà tre righe (una per ciascun album) e due colonne (vendite in Italia e nel mondo).

vendite_italia <- c(2.1, 2.5, 1.3)      # Vendite in Italia dei tre album, in milioni
vendite_mondo <- c(200, 240, 90.5)      # Vendite nel mondo dei tre album, in milioni

# Uniamo i dati in un unico vettore
vendite_totali <- c(vendite_italia, vendite_mondo)

#--> domande per te: che classe di oggetto ha la variabile `vendite_totali`? E quanto è lungo?

# Costruisci la matrice, disponendo gli elementi della variabile `vendite_totali` per riga
matrice_vendite <- matrix(vendite_totali, nrow = 3, byrow = FALSE,
                          dimnames = list(c("The Dark Side of the Moon", 
                                            "Wish You Were Here", 
                                            "Animals"), 
                                          c("Italia", "Mondo")))

#--> domanda per te: stampa a video la variabile `matrice_vendite`


#--> domandaccia per te: crea ora una aseconda matrice, chiamata `matrice_vendite_v2`, in cui nella prima colonna
#          ci siano le vendite degli album nel mondo, e nella seconda colonna le vendite in Italia

---

#### **Assegnare nomi alle righe e colonne**
Puoi aggiungere o modificare i nomi delle righe e delle colonne utilizzando le funzioni `rownames()` e `colnames()`.

rownames(matrice_vendite) <- c("The Dark Side of the Moon", "Wish You Were Here", "Animals")
colnames(matrice_vendite) <- c("Italia", "Mondo")

print(matrice_vendite)

---

#### **Calcolare i totali delle vendite per album**
Per calcolare i totali delle vendite, sommiamo i valori su ogni riga usando la funzione `rowSums()`.

totali_album <- rowSums(matrice_vendite)
totali_album

---

#### **Aggiungere una colonna con i totali delle vendite**
Possiamo aggiungere una colonna alla matrice con i totali calcolati.

matrice_completa <- cbind(matrice_vendite, Totale = totali_album)
print(matrice_completa)

---

#### **Unire matrici per riga**
Immaginiamo di avere una seconda matrice con le vendite di altri tre album dei Pink Floyd. Possiamo combinare le due matrici usando `rbind()`.

# Dati della seconda matrice
vendite_italia2 <- c(0.9, 1.0, 0.8)
vendite_mondo2 <- c(25, 30, 20)
vendite_totali2 <- c(vendite_italia2, vendite_mondo2)

# Costruisci la seconda matrice
matrice_vendite2 <- matrix(vendite_totali2, nrow = 3, byrow = FALSE,
                           dimnames = list(c("The Wall", "The Division Bell", "A Momentary Lapse of Reason"), 
                                           c("Italia", "Mondo")))

# Unisci le due matrici
matrice_completa2 <- rbind(matrice_completa, matrice_vendite2)
print(matrice_completa2)

---

#### **Calcolare i totali delle vendite per regione**
Usiamo la funzione `colSums()` per sommare le vendite in Italia e nel mondo.

totali_regioni <- colSums(matrice_completa2)
print(totali_regioni)

---

#### **Selezionare elementi specifici**
Possiamo selezionare righe o colonne specifiche con le parentesi quadre `[ ]`.


# Vendite nel mondo per tutti gli album
vendite_mondo_tutti <- matrice_completa2[, "Mondo"]

# Media delle vendite nel mondo
media_mondo <- mean(vendite_mondo_tutti)
media_mondo


---

#### **Aritmetica con le matrici**
Puoi eseguire operazioni aritmetiche direttamente sugli elementi delle matrici.


# Supponiamo che il costo di un disco in Italia e nel mondo sia 20 euro
prezzo_disco <- matrix(c(20, 20), nrow = 3, ncol = 2, byrow = TRUE)

# Numero stimato di dischi venduti
dischi_venduti <- matrice_completa2[, c("Italia", "Mondo")] / prezzo_disco
print(dischi_venduti)


---
