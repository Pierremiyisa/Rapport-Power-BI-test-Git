# Rapport Power BI — test de versionnement Git (PBIP)

![Power BI](https://img.shields.io/badge/Power%20BI-PBIP-F2C811) ![Format](https://img.shields.io/badge/format-TMDL%20%2B%20PBIR-0077ff)

Projet d'essai : versionner un rapport Power BI avec Git grâce au format **Power BI Project (PBIP)**, qui enregistre le rapport et le modèle sémantique en fichiers texte (JSON et TMDL) comparables ligne à ligne.

## Structure
```
.
├── rapport-test-git.pbip              Point d'entrée : à ouvrir dans Power BI Desktop
├── rapport-test-git.Report/           Rapport (format PBIR : pages, visuels, thème)
│   ├── definition.pbir                Lien vers le modèle sémantique
│   └── definition/pages/…             Une page, un visuel texte
└── rapport-test-git.SemanticModel/    Modèle sémantique (TMDL)
    └── definition/                    model.tmdl, database.tmdl, cultures/
```

## Utilisation
1. Clonez le dépôt (GitHub Desktop ou `git clone`).
2. Ouvrez `rapport-test-git.pbip` dans Power BI Desktop (aperçu PBIP et stockage PBIR/TMDL activés dans Options › Fonctionnalités en préversion, selon votre version).
3. Modifiez, enregistrez, puis validez (commit) : chaque changement apparaît comme une différence de texte.

## Bonnes pratiques
- Ne versionnez pas `.pbi/localSettings.json` ni `.pbi/cache.abf` (déjà exclus par `.gitignore`).
- Un commit par modification lisible (« ajout de la page Ventes », « mesure CA mensuel »).

**Auteur :** Pierre Miyisa — data & business intelligence, Goma (RDC)
