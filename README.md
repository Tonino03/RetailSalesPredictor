# 💻 PC & Laptop RetailSalesPredictor- Regression Analysis

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-2.1+-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.3+-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.8+-013243?style=for-the-badge)

**RetailSalesPredictor** è un framework di analisi predittiva progettato per stimare il volume di vendita dei dispositivi mobile. Il progetto integra tecniche di regressione avanzata, clustering e data engineering per estrarre insight strategici da un dataset di 50.000 record estratti da Kaggle.

---

## 🎯 Obiettivi dell'Analisi
Il sistema affronta tre sfide critiche nel settore retail tech:
- **Predictive Modeling:** Stima accurata della variabile `Quantity Sold` basata sulle specifiche hardware.
- **Market Segmentation:** Identificazione di cluster omogenei di prodotti tramite l'algoritmo **K-Means**.
- **Feature Impact:** Analisi dell'influenza di componenti (RAM, ROM, SSD) sul successo commerciale.

---

## 🚀 Funzionalità Chiave

### 🧹 Data Engineering & Smart Cleaning
- **Normalizzazione Unità:** Conversione dinamica di stringhe eterogenee (GB/TB) in valori numerici scalabili.
- **Imputazione Avanzata:** Gestione dei valori mancanti (NaN) per SSD e Core Specification tramite logica condizionale basata su Brand e Categoria Prodotto.

### 📊 Exploratory Data Analysis (EDA)
- **Statistical Profiling:** Studio delle distribuzioni tramite Violin Plot e BoxPlot per mitigare l'impatto degli outlier.
- **Correlation Mapping:** Utilizzo di matrici di correlazione per evidenziare i legami tra specifiche tecniche e pricing.

### 🧠 Architettura Predittiva & Pipeline
- **Clustering-as-a-Feature:** Integrazione dei cluster generati dal K-Means come variabili di input per potenziare i regressori.
- **Benchmarking:** Valutazione comparativa tra modelli di Ensemble Learning e istanze basate sulla distanza (KNN).

---

## 🛠️ Stack Tecnologico & Architettura

L'analisi segue una pipeline modulare: **Cleaning → EDA → Clustering → Regression**.

| Componente | Tecnologia | Descrizione |
| :--- | :--- | :--- |
| **Language** | **Python** | Core logic per l'elaborazione dei dati. |
| **Data Processing** | **Pandas / Numpy** | Manipolazione di dataset di grandi dimensioni. |
| **Machine Learning**| **Scikit-Learn** | Pipeline di modellazione, clustering e metriche. |
| **Visualization**| **Seaborn / Matplotlib** | Plotting statistico e analisi visiva dei residui. |

---

## 📈 Performance & Risultati

Il modello **HistGradientBoosting** ha dimostrato la massima precisione, minimizzando l'errore quadratico medio.

| Modello | MAE | RMSE | $R^2$ Score |
| :--- | :--- | :--- | :--- |
| **HistGradientBoosting** | **3.99** | **5.00** | **0.749** |
| Random Forest Regressor | 4.06 | 5.10 | 0.738 |
| KNN Regressor (k=11) | 4.17 | 5.21 | 0.726 |

---

## 🧠 Logica Tecnica & Sfide Risolte

### Clustering Pre-Regressione
Per migliorare la precisione, ho implementato il **Metodo del Gomito (Elbow Method)** per determinare il numero ottimale di cluster. L'aggiunta del cluster ID alle feature ha permesso ai modelli di catturare relazioni non lineari specifiche per fascia di mercato.

### Ottimizzazione KNN
L'efficacia del KNN è stata garantita tramite l'applicazione di un **StandardScaler**. Senza la normalizzazione, variabili con scale diverse (es. Prezzo vs RAM) avrebbero distorto il calcolo della distanza euclidea.

---

## 🔧 Setup & Installazione
1. Clonare la repository: `git clone https://github.com/Tonino03/progetto-data-mining.git`
2. Installare le dipendenze: `pip install -r requirements.txt`
3. Eseguire il notebook `Data_Mining_Project.ipynb` in ambiente Jupyter o Google Colab.

---

## 👥 Contributors
Progetto realizzato in collaborazione da:
* **[Antoniopio Giurranna](https://github.com/Tonino03)** 
* **[Samuele Ferraro](https://github.com/samueleferraro)**
* **[Francesco D'Angelo](https://github.com/Vuot00)** 
