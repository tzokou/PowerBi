# Ouvrir et explorer le rapport

## Consultation rapide

Les captures et le README permettent de découvrir le projet sans installer Power BI. Pour explorer les visuels, télécharger `sales.pbix` depuis GitHub (bouton de téléchargement du fichier), puis l’ouvrir dans Power BI Desktop sur Windows. Si GitHub ne prévisualise pas le PBIX, cela n’empêche pas son téléchargement.

## Actualisation des sources

1. Récupérer les ressources du [dépôt pédagogique original](https://github.com/IterationInsights/Microsoft-Press-Introduction-to-Microsoft-Power-BI-V2).
2. Conserver la structure du dossier `Data`, y compris ses sous-dossiers et référentiels. Les fichiers Excel ne sont pas dupliqués dans ce dépôt.
3. Ouvrir le rapport et examiner les paramètres de sources et les étapes Source dans Power Query. Le parcours utilise initialement `C:\Introduction to Power BI` ; le fichier de l’auteur peut pointer vers un autre emplacement local.
4. Remplacer les chemins nécessaires par ceux de votre copie des ressources, puis appliquer les modifications et actualiser.
5. Vérifier les éventuelles erreurs de chargement, les filtres, la couverture temporelle et les totaux avant d’interpréter les résultats.

La procédure est un guide de reprise ; une actualisation complète n’a pas été exécutée lors de la préparation de ce dépôt. Aucune connexion à un service de production n’est nécessaire pour consulter les captures.

## Parcours de démonstration

- **Overview** : examiner les ventes par continent et les taux de marge. Sélectionner une année et un continent pour observer les changements.
- Survoler les barres géographiques pour explorer le détail par pays montré dans les captures.
- Examiner la catégorie Bikes : la capture fournie montre le taux de marge, la quantité et les options de détail.
- **Product Sales Details** : comparer ventes, YTD et année précédente. Le fichier inspecté contient un filtre enregistré sur Accessories ; le contrôler avant une démonstration globale.
- **Dax Demo** : parcourir les mesures réunies dans la table. Selon la configuration des pages, certaines vues techniques ou d’infobulle peuvent être masquées dans le parcours de lecture.

## Contrôles recommandés

- Aligner la période et les filtres de la carte KPI, de l’objectif et du graphique par continent.
- Renommer « Sales Performance » en « Taux de marge par année », puisque le visuel référence `Total Margin %`.
- Expliciter le code de devise, les règles de marge et la période de l’objectif.
- Vérifier les formules YTD et YoY sur une période de référence, y compris le traitement des périodes incomplètes et dénominateurs nuls.
