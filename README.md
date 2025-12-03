# 🚀 Période de retour vers le futur
**Projet : Analyse des pluies extrêmes et périodes de retour dans un contexte de réchauffement climatique**

---

## 📌 Contexte  
Selon **Météo-France**, *le réchauffement climatique ne bouleverse pas seulement les températures : il modifie aussi la fréquence, l’intensité et la répartition des précipitations en France.*  
Dans une France à **+4 °C**, les pluies intenses se renforceraient, avec **+15 % en moyenne** et jusqu’à **+20 % sur la moitié nord**, aggravant le risque d’inondation, notamment en zones urbaines.

Ce projet s’inscrit dans le cadre du **Hackathon 2025 : “Le climat en données”**.

---

## 🔍 Problématiques scientifiques  
1. **Identification des pluies extrêmes sur la période historique**  
   - Analyse de l’apport des données **CPRCM** et comparaison avec différents modèles et les observations **COMEPHORE** et **SAFRAN**.  
2. **Analyse des données horaires vs quotidiennes**  
   - Comparaison des occurrences de pluies extrêmes avec les observations historiques.  
3. **Impact du réchauffement climatique sur les intensités à période de retour équivalente**  
   - Évaluation pour différents horizons de la **TRACC** et comparaison des résultats avec les données CPRCM (1h / 24h / quotidien).  

---

## 💼 Problématique métier  
- **Question clé :**  
  À quel type de pluies faut-il se préparer dans le futur ?  

- **Proposition de valeur :**  
  Aider et accompagner les territoires à renforcer leur résilience et assurer la pérennité du système assurantiel.

---

## ✅ Solution proposée  
### **Description et fonctionnalités**  
- Offre d’accompagnement **Territoires et Prévention**, enrichie d’un diagnostic du risque de ruissellement en fonction des scénarios climatiques.  
- Offre de **formation** pour les élus et agents.  

### **Usage des données**  
- Estimation des **périodes de retour** des pluies extrêmes.  
- **Sources et nature des données :** *(à compléter)*.  

### **Méthodologie**  
- Extraction des **maxima annuels**.  
- Ajustement via une loi de probabilité **GEV (Gumbel)**.

---

## 🌱 Impact envisagé  
- **Objectifs :**  
  - Renforcer la collaboration entre assureurs et collectivités.  
  - Intégrer le changement climatique dans les politiques d’urbanisation.  
  - Améliorer la connaissance des impacts climatiques.  

- **Usagers visés :**  
  Collectivités, élus, agents → **Sensibilisation et résilience territoriale**.

---

## 📂 Ressources
### Les données
Les données sout fournies via un S3. 
Toutes les informations pour le téléchargement sont [ici](https://guides.data.gouv.fr/guide-du-participant-au-hackathon-le-climat-en-donnees/ressources-du-hackathon/donnees)

Pour les télécharger en python, il est possible d'utiliser les librairies `requests` ou `wget`

### Préparation des données
Pour le calcul des périodes de retours, il faut extraire le max annuel des précipitations.
A partir des données fournies, du code SQL ou pandas basique permet d'obtenir ces informations. 

### Calcul de la période de retour
En entrée de ces calculs, il faut avoir 2 colonnes :
- l'année
- le max de précipitation en mm

Ensuite, une loi de Gumbel est ajustée à partir de ces données pour calculer la période de retour.

Les calculs ont été réalisés à l'aide d'un fichier Excel, disponible [ici](src/calculateur_periode_retour.xlsx)

A noter, que ce sont des formules simples qui pourraient être codés en Python.


### Résultats
Tableaux des périodes de retour selon :
- Types de modèles
- Scénarios climatiques / Historique
- Pas de temps (horaire / quotidien)

Graphiques de visualisation des périodes de retour :




---



