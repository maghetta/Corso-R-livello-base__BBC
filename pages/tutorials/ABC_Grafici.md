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

```
