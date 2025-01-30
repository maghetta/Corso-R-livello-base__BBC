---
title: ABC Grafici in R
---

```markdown
# Tutorial: Creazione di Grafici Base in R

# R offre molte funzioni per creare grafici base, utili per visualizzare i dati.
# Questo tutorial introduce le basi per creare e personalizzare grafici in R.
# In particolare, esploreremo le funzioni `plot()`, `barplot()`, `hist()`, `pie()` e `boxplot()`.
# Inoltre, vedremo alcuni esempi su come personalizzare i grafici modificando colori, legende e stili.

# 1. Funzione plot
# La funzione plot() è molto versatile e consente di creare diversi tipi di grafici.
# Di default, viene usata per scatter plot (grafici a dispersione).

# Esempio: Scatter plot
x <- 1:10
y <- x^2
plot(x, y, main = "Scatter plot", xlab = "X", ylab = "Y", col = "blue", pch = 19)

# Modifiche principali:
# - main: titolo del grafico
# - xlab, ylab: etichette degli assi
# - col: colore dei punti
# - pch: stile dei punti

#--> domande per te: prova a modificare il grafico appena fatto come segue:

#...a.) ripeti il grafico modificando il colore dei punti da blu a verde
# A proposito: puoi stampare l'intero elenco dei 657 colori a tua disposizione digitando `colors()`

#...b.) ripeti il grafico modificando l'aspetto dei punti, da pallino pieno a triangolino pieno.
# Per farlo ti sarà utile sapere che il parametro da modificare nel comando del plot per modificare
# l'aspetto dei punti è `pch` (`plotting character`), e che questo parametro può assumere valori da 0 a 25,
# ognuno associato ad un diverso simbolo per rappresentare i punti nel plot.
# A proposito: puoi visualizzare l'intero elenco dei 26 caratteri di plot a tua disposizione digitando `?pch`

#...c.) ripeti il grafico modificando sia il contenuto del titolo (da "Scatter plot" a "Primo plot"), che
#      il colore (da nero a turchese).
# Lascio a te di dedurre, guardando gli argomenti del comando `plot()` appena digitato, quale argomento
# dovrai modificare per cambiare il titolo al grafico come richiesto. 
# Invece, per modificarne il colore, ti sarà utile sapere che l'argomento che ti permette di modificare
# il colore del titolo è: `col.main`

#...d.) ripeti il grafico modificando l'aspetto dei punti, in modo che compaiano connessi da una linea
# Per farlo, ti sarà utile sapere che il paramentro per modificare l'aspetto del tracciamento dei dati
# si chiama `type`, e può assumere tra gli altri i seguenti valori:
# - "p": stampa i singoli punti (default)
# - "l": stampa linee
# - "b": (che sta per *both*) stampa punti connessi da linee
# - "o": stampa punti sormontati da linee
# - "n": Non stampa nulla riguardo i punti, mentre stampa gli assi e il sistema di coordinate in accordo con i dati.
#        Si usa ad esempio nel caso si vogliano aggiungere poi gli ulteriori dettagli del plot con funzioni specifiche
#        come `points()`, `lines()` ecc. 


# Qualche altra informazione utile 


# 2. Funzione barplot
# La funzione barplot() è usata per creare grafici a barre.

# Esempio: Grafico a barre
values <- c(4, 7, 9, 6)
names <- c("A", "B", "C", "D")
barplot(values, names.arg = names, main = "Grafico a barre", col = "red", border = "black")

# Modifiche principali:
# - names.arg: nomi delle barre
# - col: colore delle barre
# - border: colore del bordo

# 3. Funzione hist
# La funzione hist() è utilizzata per creare istogrammi.

# Esempio: Istogramma
set.seed(123)
data <- rnorm(1000)
hist(data, main = "Istogramma", xlab = "Valori", col = "lightblue", border = "darkblue")

# Modifiche principali:
# - col: colore delle colonne
# - border: colore dei bordi
# - xlab: etichetta dell'asse x

# 4. Funzione pie
# La funzione pie() crea grafici a torta.

# Esempio: Grafico a torta
slices <- c(40, 30, 20, 10)
labels <- c("A", "B", "C", "D")
pie(slices, labels = labels, main = "Grafico a torta", col = rainbow(length(slices)))

# Modifiche principali:
# - labels: etichette delle sezioni
# - col: colori delle sezioni

# 5. Funzione boxplot
# La funzione boxplot() è usata per creare box plot.

# Esempio: Box plot
group1 <- rnorm(50, mean = 5)
group2 <- rnorm(50, mean = 7)
data <- list(Group1 = group1, Group2 = group2)
boxplot(data, main = "Box plot", col = c("orange", "green"), names = c("Gruppo 1", "Gruppo 2"))

# Modifiche principali:
# - col: colori delle scatole
# - names: nomi dei gruppi

# Personalizzazione generale
# I grafici possono essere ulteriormente personalizzati con:

# Aggiungere una legenda:
legend("topright", legend = c("Gruppo 1", "Gruppo 2"), fill = c("orange", "green"))

# Modificare i margini:
par(mar = c(5, 5, 4, 2))

# Salvare i grafici in un file:
png("grafico.png")
plot(x, y, main = "Scatter plot salvato", xlab = "X", ylab = "Y", col = "blue", pch = 19)
dev.off()

# Puoi continuare ad esplorare la funzione `plot()` e altre funzioni grafiche ad esempio nel capitolo 12
# `Graphical procedures` del [Manuale in formato PDF **Introduction to R**](href="https://cran.r-project.org/doc/manuals/r-release/R-intro.pdf)
```
