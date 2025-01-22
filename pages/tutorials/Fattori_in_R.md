---
title: Fattori in R
---

```markdown

## Tutorial introduttivo all'oggetto di classe fattore in R

# Questo tutorial ti guiderà nella scoperta dei fattori in R. Più precisamente, imparerai a:
# - Riconoscere tipi di dati per i quali è utile ricorrere ai fattori
# - Creare e manipolare fattori, ordinati e non
# - Selezionare specifici elementi di un fattore


## Introduzione ai Fattori

# Certe volte i dati che ci troviamo ad analizzare possono essere raggruppati in un certo numero di categorie.
# Per esempio, i film possono essere raggruppati per genere (commedia, horror, avventura...).
# In R, le `variabili di tipo categorico` sono salvate in oggetti di classe `fattore`,
# cioè speciali vettori caratterizzati dalla presenza di `livelli`
# (ossia, le categorie presenti nella variabile categorica considerata). 

# Quindi, il termine `fattore` si riferisce ad un particolare tipo di oggetto utilizzato
# per immagazzinare variabili di tipo categorico. La differenza tra una variabile di tipo categorico
# e una variabile di tipo continuo consiste nel fatto che la variabile categorica può appartenere
# a un numero limitato di categorie. Una variabile di tipo continuo, al contrario, può assumere infiniti valori.

# Permettere a R di sapere se sta operando su variabili di tipo categorico o continuo è molto importante siccome i modelli statistici che utilizzerai in futuro trattano i due tipi di variabile in modo molto diverso.

# Un buon esempio di una variabile categorica è il genere del film. Un film può essere "Commedia", "Horror" o "Avventura". In questo caso, "Commedia", "Horror" e "Avventura" sono i tre possibili valori che la variabile categorica "genere" può assumere e a ogni osservazione sarà assegnato uno dei tre possibili valori.

### Creare un Fattore

# Per creare un fattore in R si utilizza la funzione `factor()`. La prima cosa da fare è creare un vettore che contiene tutte le osservazioni che appartengono a un numero limitato di categorie. Per esempio, `vettore_genere` contiene il genere di 5 differenti film:

```r
# Vettore genere
vettore_genere <- c("Commedia", "Horror", "Avventura", "Commedia", "Horror")

# Converti vettore_genere in un fattore
fattore_vettore_genere <- factor(vettore_genere)

# Stampa fattore_vettore_genere
fattore_vettore_genere 
```

### Tipi di Variabili Categoricali

# Esistono due tipi di variabili categoriche: le variabili categoriche nominali e le variabili categoriche ordinali.

# Una variabile categorica nominale è una variabile che non è possibile ordinare naturalmente. Per esempio, pensa alla variabile categorica `vettore_animali` contenente le categorie "Elefante", "Giraffa", "Asino" e "Cavallo". In questo caso è abbastanza difficile ordinare le categorie.

# In senso opposto, le variabili categoriche ordinali hanno un ordine naturale. Considera la variabile categorica `vettore_gradimento` con le categorie "Basso", "Medio" e "Alto". Qui è abbastanza ovvio che, in un certo senso, "Medio" si trova sopra a "Basso" e "Alto" si trova sopra a "Medio".

### Cambiare i Livelli dei Fattori

# Quando ispezioni un nuovo dataset, noterai spesso che contiene fattori con diversi livelli. Tuttavia, alcune volte ti capiterà di voler cambiare il nome di questi livelli per ragioni di chiarezza (o altro). R ti permette di effettuare questa operazione utilizzando la funzione `levels()`:

```r
# Codice per costruire factor_vettore_genere
vettore_genere <- c("C", "H", "A", "C", "H")
factor_vettore_genere <- factor(vettore_genere)

# Specifica i livelli di factor_vettore_genere
levels(factor_vettore_genere) <- c("Avventura", "Commedia", "Horror")

factor_vettore_genere
```

### Ottenere un Sommario di un Fattore

# Alla fine di questo corso una delle tue funzioni preferite sarà `summary()`. Questa funzione ti permetterà di ottenere un'overview del contenuto di una variabile:

```r
# Crea factor_vettore_genere
vettore_genere <- c("C", "H", "A", "C", "H")
factor_vettore_genere <- factor(vettore_genere)
levels(factor_vettore_genere) <- c("Avventura", "Commedia", "Horror")

# Genera sommario per vettore_genere
summary(vettore_genere)

# Genera sommario per factor_vettore_genere
summary(factor_vettore_genere)
```

### Fattori Ordinali

# Diciamo che sei a capo di un gruppo che valuta il gradimento dei corsi e vuoi classificare il livello di gradimento come "Basso", "Medio" o "Alto". Salvi i risultati in `vettore_gradimento`.

```r
# Crea vettore_gradimento
vettore_gradimento <- c("Medio","Basso","Basso","Medio","Alto")

# Converti vettore_gradimento in un fattore ordinale
factor_vettore_gradimento <- factor(vettore_gradimento, ordered = TRUE, levels = c("Basso", "Medio", "Alto"))

# Stampa factor_vettore_gradimento
factor_vettore_gradimento
```

### Confrontare Due Fattori Ordinali

# Il fatto che `factor_vettore_gradimento` è ordinale ci permette di comparare i suoi elementi. Per effettuare il confronto, utilizza semplicemente gli operatori già conosciuti nei capitoli precedenti.

```r
# Valore del fattore per il secondo corso
da2 <- factor_vettore_gradimento[2]

# Valore del fattore per il quinto corso
da5 <- factor_vettore_gradimento[5]

# Il secondo corso è più gradito del quinto?
da2 > da5
```

---

Spero che questo tutorial ti sia utile! Se hai altre domande o hai bisogno di ulteriori chiarimenti, fammi sapere! 😊


```
