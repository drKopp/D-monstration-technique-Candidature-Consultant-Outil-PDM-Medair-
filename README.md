# Démonstration technique — Candidature Consultant Outil PDM (Medair)

> Réponse à l'appel à consultation **« Consultant Outil PDM »** — Recrutement d'un consultant pour le développement d'un outil automatisé d'analyse et de rapportage des enquêtes Post Distribution Monitoring (PDM).

Ce dépôt présente le travail réalisé pour démontrer ma compréhension des Termes de Référence et ma capacité à livrer l'outil demandé.

---

## 🎥 Démonstration vidéo

[**▶ Voir la vidéo de démonstration**](https://youtu.be/NmIuBX3p1Qw)

*(Remplacez ce lien par l'URL de votre vidéo — YouTube non répertorié, Loom, ou Google Drive avec partage activé.)*

La vidéo présente le cycle complet : de la soumission d'une enquête sur le terrain jusqu'à la génération du rapport PDM dans Excel.

---

## 📄 Le livrable contractuel : le classeur Excel

Conformément à la section 4.2 du TDR, le cœur du travail est un **classeur Excel autonome**, structuré en 9 onglets :

| Onglet | Rôle |
|---|---|
| `Guide` | Mode d'emploi de l'outil |
| `Config` | Paramètres (zones, secteurs, langue) |
| `Raw_Data` | Données brutes importées (Power Query) |
| `Data_Clean` | Données nettoyées et validées |
| `QC_Qualite` | Contrôle qualité : doublons, valeurs manquantes, incohérences |
| `Indicateurs` | Calcul automatique des indicateurs clés (satisfaction, utilisation des biens, redevabilité, protection et inclusion) |
| `Desagregation` | Désagrégation par sexe, âge, zone, localisation |
| `Dashboard` | Tableau de bord interactif : graphiques dynamiques, TCD, filtres et segments |
| `Rapport` | Résumé exécutif, tableau de synthèse, recommandations — exportable en PDF |

L'outil s'actualise automatiquement (bouton « Actualiser ») dès que de nouvelles données sont disponibles dans la source connectée, conformément à l'exigence d'« actualisation automatique des analyses après mise à jour des données ».

📎 [**Télécharger le classeur Excel**](LIEN_VERS_VOTRE_FICHIER_EXCEL)

---

## ⚙️ Le pipeline de démonstration (complément, hors périmètre du TDR)

Pour illustrer ma compréhension du flux de données complet — de la collecte terrain jusqu'au rapport final — j'ai construit un pipeline de démonstration :

```
KoboToolbox  →  n8n  →  Google Sheets  →  Excel (Power Query)
(collecte)      (traitement /       (stockage        (analyse,
                 nettoyage           intermédiaire)    indicateurs,
                 automatisé)                           dashboard,
                                                        rapport)
```

**Important — positionnement par rapport au TDR :**
Le cahier des charges de Medair ne demande pas d'outil d'automatisation externe de type n8n : le livrable contractuel attendu est un **classeur Excel autonome**, fonctionnant sans logiciel supplémentaire, avec formules optimisées et macros VBA si nécessaire — c'est exactement ce que fournit le classeur présenté ci-dessus.

Le pipeline KoboToolbox → n8n → Google Sheets est une **extension optionnelle** que j'ai développée en supplément, pour deux raisons :
1. Démontrer ma compréhension du cycle de vie complet des données PDM (de la collecte au rapport), et pas seulement de la partie Excel ;
2. Illustrer des pistes concrètes d'automatisation supplémentaire, si Medair souhaite aller au-delà du périmètre du TDR à l'avenir.

### Pistes d'amélioration envisageables (non développées, pour discussion future)
- **Alertes email automatiques** en cas d'anomalie détectée dans les données (doublons, valeurs manquantes critiques, incohérences)
- **Envoi automatique du rapport** (Excel/PDF) à intervalles définis (hebdomadaire, mensuel) aux responsables MEAL
- Notification (email ou messagerie interne) lors de chaque nouvelle soumission d'enquête

---

## 🔗 Correspondance avec les objectifs du TDR

| Exigence du TDR (section 4.2) | Où c'est démontré |
|---|---|
| Importation facile des données brutes, compatibilité Excel/CSV | Power Query — onglet `Raw_Data` |
| Détection des doublons, valeurs manquantes, contrôles de cohérence | Onglet `QC_Qualite` |
| Calcul automatique des indicateurs clés | Onglet `Indicateurs` |
| Désagrégation par sexe, âge, localisation | Onglet `Desagregation` |
| Tableau de bord interactif (graphiques, TCD, filtres, segments) | Onglet `Dashboard` |
| Rapport automatique exportable en PDF | Onglet `Rapport` |

---

## 📬 Contact

**Diriana**
*(email: dirianatins@gmail.com, +261343532728)*

