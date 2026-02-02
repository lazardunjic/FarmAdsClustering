# 📊 Farm Ads Text Clustering

Ovaj projekat se bavi **nenadgledanim klasterovanjem tekstualnih oglasa** iz skupa podataka **Farm-Ads**, sa ciljem otkrivanja prirodne grupisanosti dokumenata bez korišćenja labela tokom treniranja.

Rad je realizovan u okviru predmeta **Istraživanje podataka 2** na Matematičkom fakultetu.

---

## 🧠 Cilj projekta

- Ispitati da li algoritmi klasterovanja mogu automatski grupisati oglase po tematici  
- Uporediti različite reprezentacije teksta i algoritme klasterovanja  
- Evaluirati kvalitet klastera pomoću standardnih metrika  
- Analizirati interpretabilnost dobijenih grupa  

---

## 📁 Skup podataka

**Farm-Ads dataset**
- 4143 tekstualna oglasa  
- Oglasi su tematski povezani sa poljoprivredom ili nisu  
- Originalne oznake se koriste **samo za evaluaciju**, ne za treniranje  

---

## ⚙️ Obrada podataka

Primijenjeni koraci:

- TF-IDF vektorizacija (više konfiguracija)  
- Count Vectorizer  
- Redukcija dimenzionalnosti:
  - PCA  
  - Truncated SVD (LSA)  
- Dodavanje statističkih atributa teksta (dužina, broj reči, itd.)

Ukupno korišćeno **6 skupova atributa**.

---

## 🤖 Korišćeni algoritmi

Testirano je **8 konfiguracija klasterovanja**:

- K-Means (K=3 i K=10)  
- Agglomerative Clustering (Ward, Complete)  
- DBSCAN (2 podešavanja)  
- Mean Shift  
- BIRCH  

Ukupno: **48 eksperimenata** (8 algoritama × 6 reprezentacija).

---

## 📏 Metrike evaluacije

Kvalitet klastera meren je pomoću:

- **Silhouette Score**  
- **Davies–Bouldin Index**  
- **Calinski–Harabasz Score**

---

## 🏆 Glavni rezultat

Najbolji balans performansi postignut je sa:

**K-Means (K=3) + Count Vectorizer**

Model pokazuje visoku separaciju i kompaktnost klastera, uz dobru interpretabilnost dobijenih grupa.

---

## 🛠 Tehnologije

- Python  
- scikit-learn  
- NumPy  
- pandas  
- matplotlib / seaborn  

---

## 📌 Napomena

Projekat demonstrira kompletan tok rada nad tekstualnim podacima:  
**sirov tekst → vektorizacija → redukcija dimenzija → klasterovanje → evaluacija → interpretacija.**

---

## ✍ Autor

**Lazar Dunjić 265/2021**
