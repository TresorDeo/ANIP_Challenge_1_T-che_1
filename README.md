# ANIP Challenge 1 - Tâche 1 : ETL (Collecte, Nettoyage, Harmonisation)
**Auteur : Déo-Gratias ZINGUEDE**  
**Date : 1er Octobre 2025**  
**Date de Soumission : 2 Octobre 2025**

---

## Objectif
Ce projet répond à la **Tâche 1** de l'ANIP Challenge en créant un dataset unifié croisé avec :
- **Population par département** (évolution annuelle),
- **Taux de participation féminine au travail (Female Labor Rate)** par an,
- **PIB et PIB par habitant (GDP/GDP per capita)** par an,
- **Indicateurs sociaux et sportifs** (ex. : matchs CAN).

Le dataset est optimisé pour **Power BI**, avec une analyse exploratoire illustrant le lien entre les événements sportifs (CAN) et le développement (PIB, emploi, cohésion sociale).

---

## Livrables
1. **dataset_final_unifie.csv** : Dataset nettoyé et harmonisé (2010-2023).
2. **glossaire.csv** : Dictionnaire des variables avec métadonnées.
3. **etl_script.py** : Script Python complet (collecte, nettoyage, analyse).

---

## Méthodologie
### Collecte des Données
- **Sources** : UN WPP (population), WorldPop (départements), IMF WEO (PIB), UNCTAD (économie), Gender WB (emploi féminin), Sport Data (CAN/FIFA/CIO).
- **Période** : 2010-2023, avec focus 2020 pour WorldPop.
- **Enrichissement Sportif** : Intégration des participations du Bénin à la Coupe d'Afrique des Nations (CAN) depuis 2010 (ex. : 3 matchs en 2010, 5 en 2019).

### Nettoyage et Harmonisation
- Conversion en format long (`Year`, `Indicator`, `Value`, `Source`, `Region`, `Commune`).
- Filtrage : 2010-2023, gestion des NA, standardisation des unités (ex. : PIB en millions USD).
- Robustesse : Gestion des erreurs avec logs pour débogage.

### Analyse et Insights
- **Lien Sport-Développement** : Corrélation entre le nombre de matchs CAN et les indicateurs économiques/sociaux (PIB par habitant, taux d’emploi féminin).
- **Visualisation** : Heatmap des corrélations inclus dans `sport_dev_correlation.png`.

---

## Structure du Répertoire

ANIP_Challenge_Tache1/
│
├── dataset_final_unifie.csv    # Dataset final
├── glossaire.csv              # Glossaire des variables
├── etl_script.py             # Script Python
└── README.md                 # Ce fichier



## Remerciements
Merci à l'ANIP pour cette opportunité. Ce projet illustre mon expertise en ETL et analyse de données pour le développement socio-économique au Bénin.

**Contact** : [tresordeozinguede@gmail.com] 
**Soumis le** : 02/10/2025
