# Farm Ads Clustering 🌾

Projekat za klasterovanje oglasa farmi korišćenjem različitih algoritama mašinskog učenja.

## 🚀 Pokretanje

### 1. Setup
```bash
# Kreiraj virtuelno okruženje
python3 -m venv .venv

# Aktiviraj ga
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows

# Instaliraj zavisnosti
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 2. Pokreni Jupyter Notebook
```bash
jupyter notebook farmadsclustering.ipynb
```

### 3. Pokretanje ćelija

- **Pokreni sve odjednom**: `Cell` → `Run All`
- **Ili pokreni redom**: `Shift + Enter` za svaku ćeliju

## 📂 Gde se čuvaju rezultati

Nakon izvršavanja, kreiraće se:

### `output/` folder - CSV i pickle fajlovi
- `clustering_results.csv` - Svi rezultati algoritama
- `data_clustered.csv` - Podaci sa klaster labelama
- `best_model.pkl` - Najbolji model
- `cluster_top_words.csv` - Top reči po klasterima

### `visualizations/` folder - Grafici (PNG)
- `viz_2d.png` - 2D vizualizacija
- `viz_3d.png` - 3D vizualizacija
- `elbow_method.png` - Elbow grafik
- `algorithm_comparison.png` - Poređenje algoritama
- `best_model_visualization.png` - Najbolji model

## 📊 Šta notebook radi

1. Učitava podatke (CSV sa kolonama `text` i `label`)
2. Pravi TF-IDF reprezentacije teksta
3. Primenjuje PCA, SVD, t-SNE redukciju
4. Testira K-Means, DBSCAN, Agglomerative, Mean Shift, BIRCH
5. Evaluira Silhouette, Davies-Bouldin, Calinski-Harabasz metrike
6. Čuva rezultate u `output/` i grafike u `visualizations/`

---

**Autor**: Lazar Dunjić 265/2021 