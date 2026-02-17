# Medical Data Visualizer

Projet réalisé dans le cadre du cursus **Data Analysis with Python** de freeCodeCamp.

L’objectif est d’analyser et de visualiser des données médicales issues d’examens cliniques.  
Le projet utilise **Pandas**, **Matplotlib** et **Seaborn** pour explorer les relations entre les mesures corporelles, les marqueurs biologiques et la présence de maladies cardiovasculaires.

---

## 📊 Objectifs du projet

À partir du fichier `medical_examination.csv`, le programme doit :

### ✔️ Préparation des données
- Ajouter une colonne `overweight` basée sur l’IMC (BMI > 25 → 1).
- Normaliser les colonnes `cholesterol` et `gluc` (1 → 0, >1 → 1).
- Nettoyer les données pour supprimer les valeurs incohérentes :
  - `ap_lo` ≤ `ap_hi`
  - taille et poids dans les percentiles 2.5% à 97.5%

### ✔️ Visualisation 1 : Catplot
Créer un graphique catégoriel montrant, pour chaque variable :
- cholesterol  
- gluc  
- smoke  
- alco  
- active  
- overweight  

… les répartitions selon `cardio = 0` et `cardio = 1`.

### ✔️ Visualisation 2 : Heatmap
Créer une carte de corrélation :
- calcul de la matrice de corrélation
- masque triangulaire supérieur
- affichage annoté avec Seaborn

---

## 📁 Structure du projet

```
medical_data_visualizer.py   # Fonctions draw_cat_plot() et draw_heat_map()
medical_examination.csv      # Dataset médical
main.py                      # Script pour exécuter les tests
test_module.py               # Tests unitaires freeCodeCamp
catplot.png                  # Graphique catégoriel généré
heatmap.png                  # Carte de corrélation générée
README.md                    # Documentation du projet
```

---

## 🚀 Exécution

### Installer les dépendances
```bash
pip install -r requirements.txt
```

### Générer les visualisations
```bash
python3 main.py
```

Les fichiers `catplot.png` et `heatmap.png` seront créés automatiquement.

---

## 🧠 Exemple d’utilisation

```python
from medical_data_visualizer import draw_cat_plot, draw_heat_map

fig1 = draw_cat_plot()
fig2 = draw_heat_map()
```

---

## 📚 Source du dataset

Dua, D. and Graff, C. (2019).  
UCI Machine Learning Repository — Medical Examination Dataset.

---

##  Auteur

**Honnygloire MBOMBOTO TO HOUNDA**  
