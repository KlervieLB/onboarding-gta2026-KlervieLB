# L3 — Canevas de cas d'usage IA

**Étudiant·e** : [Ton identifiant GitHub / Nom]
**Séance** : S03 — Du cas d'usage au déploiement : structurer un projet IA 

## Cas d'usage choisi

**Secteur** : Finance (Institution financière canadienne).
**Processus ciblé** : Analyse du risque de crédit pour les PME, incluant l'analyse des états financiers, le calcul des ratios et la génération d'une recommandation d'approbation ou de refus.

---

## Section 1 — Problème d'affaires précis

L'institution cherche à implanter un agent IA pour générer des gains de productivité et de temps dans l'analyse de crédit. Actuellement, les processus s'appuient sur des historiques de décisions de crédit qui reflètent les biais systémiques des analystes passés, ce qui expose l'institution à des risques réglementaires et à des pertes d'opportunités commerciales. De plus, une incapacité à adapter rapidement l'analyse lors de périodes de stress économique peut mener à l'augmentation du taux de défaut et à des pertes financières matérielles.

---

## Section 2 — Rôle spécialisé que l'agent orchestre ⭐

Agent d'analyse du risque de crédit PME.

---

## Section 3 — Données nécessaires et disponibilité

Le déploiement nécessite l'accès aux états financiers des PME et à l'historique des décisions de crédit de l'institution. Il faut également disposer de données macroéconomiques et de données d'entraînement rigoureusement validées pour assurer la représentation de différents secteurs, tailles d'entreprises (dont celles de moins de 3 ans), et minorités.

---

## Section 4 — Solution IA proposée

Un agent prédictif qui analyse les données financières pour générer des recommandations (approbation/refus). La solution est positionnée comme un outil d'augmentation, permettant à l'agent de gérer les dossiers répétitifs pendant que les analystes se concentrent sur les cas complexes. Elle intègre également un tableau de bord et un déclencheur automatique de révision humaine.

---

## Section 5 — Métriques de succès

| Type | Métrique | Valeur cible |
|---|---|---|
| Technique | Taux de défaut à 90 jours des dossiers approuvés par l'agent. | Maintien sous un seuil prédéfini déclenchant la révision automatique. |
| Affaires | Gains de temps individuels des analystes crédit. | Matérialisation démontrable de gains de productivité dès les premières semaines. |

---

## Section 6 — Risques et mitigations

**Risque principal** : L'utilisation de données d'entraînement non représentatives, ce qui amènerait l'agent à reproduire et amplifier des biais systémiques discriminatoires envers certains secteurs ou entreprises.
**Mitigation** : Réaliser un audit de biais obligatoire sur les données historiques avant le POC, constituer un jeu de validation représentatif et instaurer une revue humaine systématique des refus automatisés pendant les 6 premiers mois.

---

## Section 7 — Plan de déploiement phasé

| Phase | Périmètre | Durée estimée |
|---|---|---|
| POC | Cadrage initial incluant l'audit de biais sur les données historiques et la création d'un jeu de validation. | 4 à 6 semaines |
| Pilote | Intégration des analystes seniors comme co-concepteurs et mesure des gains de temps individuels. | 8 à 12 semaines |
| Déploiement | Déploiement continu avec tableau de bord mensuel, révisions humaines sur déclencheur, et recalibrage semestriel. | En continu |

**Sponsor exécutif identifié** : Le CRO (Chief Risk Officer).

