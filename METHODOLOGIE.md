# Méthodologie, indicateurs et limites

## Sources examinées

- Fichier final `sales.pbix` : métadonnées de rapport extraites du composant `Report/Layout`.
- Quatre captures fournies par l’auteur, reproduites sans modification.
- README et inventaire des fichiers du dossier de formation.

Le fichier `report-structure.json` fournit un inventaire lisible des pages, types de visuels et noms de champs sélectionnés. Il ne contient ni formules DAX, ni requêtes Power Query, ni export des données.

## Dictionnaire des indicateurs

| Nom dans le rapport | Usage visible | Point à confirmer |
|---|---|---|
| Total Sales | Montant des ventes utilisé dans la carte et les graphiques | Formule, devise et contexte temporel de chaque visuel |
| Target | Objectif affiché à 7 M dans les captures | Période, périmètre et méthode de fixation |
| Total Margin % | Taux de marge par produit et dans la courbe annuelle | Définition des coûts, dénominateur et pondération |
| Order Quantity | Quantité affichée pour une catégorie | Règles de comptage et périmètre des commandes |
| YTD Sales | Cumul des ventes depuis le début de l’année | Calendrier, date de référence et formule |
| PY Total Sales | Comparaison avec l’année précédente | Décalage temporel et couverture comparable |
| Total Sales YoY % | Variation annuelle en pourcentage | Formule, base de comparaison et division par zéro |
| Count of Sales Orders | Nombre de commandes | Clé de commande et comptage distinct |
| Count of Sales Orders Line Items | Nombre de lignes de commande | Grain de ligne et règles de filtrage |

Aucune formule n’est reconstruite à partir du seul nom d’une mesure.

## Lecture des captures

Les captures sont des vues statiques de données de formation. Les valeurs arrondies des graphiques ne permettent pas de reconstituer tous les agrégats exacts. Le symbole $ ne précise pas USD, CAD ou une autre devise.

### Carte KPI et total des barres

- Carte : 9,74 M$ ; objectif : 7 M.
- Barres : 7,8 + 8,2 + 10,1 ≈ 26,1 M$.
- La définition du KPI contient `Total Sales`, `Order Date Year` et `Target`. Un affichage sur une période particulière du KPI est une hypothèse plausible, non validée par un recalcul.
- **Conséquence** : ne pas assimiler 9,74 M$ au total du graphique, ni publier un taux d’atteinte comme résultat validé avant d’aligner les contextes.

### Autres précautions d’interprétation

- Les proportions de l’infobulle Europe portent sur l’Europe, pas sur les ventes mondiales.
- Le 100 % d’Australia porte sur le contexte du groupe survolé.
- Un taux de marge élevé ne démontre pas une marge totale élevée sans examiner les ventes et volumes.
- La courbe intitulée « Sales Performance » utilise la mesure `Total Margin %` ; elle décrit donc un taux de marge et non des montants de ventes.
- La définition de Product Sales Details contient un filtre enregistré sur Accessories. Sa sélection doit être prise en compte dans les comparaisons.

## Vérifications non réalisées

La préparation de ce dépôt n’inclut pas l’audit des formules DAX, des requêtes Power Query, des relations et cardinalités, des données embarquées ou de l’actualisation dans Power BI Desktop. Les captures attestent de l’affichage, pas de la justesse exhaustive du modèle. Les causes des tendances et les gains métier ne sont pas établis.

## Contribution et cadre pédagogique

Le projet est présenté par l’auteur comme un travail réalisé dans sa formation. Le parcours d’origine fournit des données, des fichiers de leçons et des éléments de présentation. Ce dépôt documente le fichier final et les captures de l’auteur ; il n’attribue pas à celui-ci la création originale des données ou des exercices, et ne quantifie pas les adaptations personnelles par rapport à chaque leçon.
