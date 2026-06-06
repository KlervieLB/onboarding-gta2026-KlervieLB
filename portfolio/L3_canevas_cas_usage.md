# L3 — Canevas de cas d'usage IA

**Étudiant·e** : Klervie LE BAYON
**Séance** : S03 — Du cas d'usage au déploiement : structurer un projet

## Cas d'usage choisi

[cite_start]**Secteur** : Finance (Institution financière canadienne)[cite: 48].
[cite_start]**Processus ciblé** : Analyse du risque de crédit pour les PME, incluant l'analyse des états financiers, le calcul des ratios et la génération d'une recommandation d'approbation ou de refus[cite: 48].

---

## Section 1 — Problème d'affaires précis

[cite_start]L'institution cherche à implanter un agent IA pour générer des gains de productivité et de temps dans l'analyse de crédit[cite: 58, 63]. [cite_start]Actuellement, les processus s'appuient sur des historiques de décisions de crédit qui reflètent les biais systémiques des analystes passés, ce qui expose l'institution à des risques réglementaires et à des pertes d'opportunités commerciales[cite: 48]. [cite_start]De plus, une incapacité à adapter rapidement l'analyse lors de périodes de stress économique peut mener à l'augmentation du taux de défaut et à des pertes financières matérielles[cite: 48].

---

## Section 2 — Rôle spécialisé que l'agent orchestre ⭐

[cite_start]Agent d'analyse du risque de crédit PME[cite: 48].

---

## Section 3 — Données nécessaires et disponibilité

[cite_start]Le déploiement nécessite l'accès aux états financiers des PME et à l'historique des décisions de crédit de l'institution[cite: 48]. [cite_start]Il faut également disposer de données macroéconomiques et de données d'entraînement rigoureusement validées pour assurer la représentation de différents secteurs, tailles d'entreprises (dont celles de moins de 3 ans), et minorités[cite: 48].

---

## Section 4 — Solution IA proposée

[cite_start]Un agent prédictif qui analyse les données financières pour générer des recommandations (approbation/refus)[cite: 48]. [cite_start]La solution est positionnée comme un outil d'augmentation, permettant à l'agent de gérer les dossiers répétitifs pendant que les analystes se concentrent sur les cas complexes[cite: 62]. [cite_start]Elle intègre également un tableau de bord et un déclencheur automatique de révision humaine[cite: 49, 50].

---

## Section 5 — Métriques de succès

| Type | Métrique | Valeur cible |
|---|---|---|
| Technique | [cite_start]Taux de défaut à 90 jours des dossiers approuvés par l'agent[cite: 49]. | [cite_start]Maintien sous un seuil prédéfini déclenchant la révision automatique[cite: 50]. |
| Affaires | [cite_start]Gains de temps individuels des analystes crédit[cite: 63]. | [cite_start]Matérialisation démontrable de gains de productivité dès les premières semaines[cite: 58, 63]. |

---

## Section 6 — Risques et mitigations

[cite_start]**Risque principal** : L'utilisation de données d'entraînement non représentatives, ce qui amènerait l'agent à reproduire et amplifier des biais systémiques discriminatoires envers certains secteurs ou entreprises[cite: 48].
[cite_start]**Mitigation** : Réaliser un audit de biais obligatoire sur les données historiques avant le POC, constituer un jeu de validation représentatif et instaurer une revue humaine systématique des refus automatisés pendant les 6 premiers mois[cite: 48].

---

## Section 7 — Plan de déploiement phasé

| Phase | Périmètre | Durée estimée |
|---|---|---|
| POC | [cite_start]Cadrage initial incluant l'audit de biais sur les données historiques et la création d'un jeu de validation[cite: 48]. | (Non spécifié) |
| Pilote | [cite_start]Intégration des analystes seniors comme co-concepteurs et mesure des gains de temps individuels dès les premières semaines[cite: 61, 63]. | (Non spécifié) |
| Déploiement | [cite_start]Déploiement continu avec tableau de bord mensuel, révisions humaines sur déclencheur, et recalibrage semestriel du modèle[cite: 48, 49, 50]. | (En continu avec recalibrage aux 6 mois) [cite_start][cite: 50]. |

[cite_start]**Sponsor exécutif identifié** : Le CRO (Chief Risk Officer)[cite: 59].
