# M1 — Grille de sélection et évaluation de solutions IA

---

## Contexte 1 — PME de 50 employés

PME montréalaise de services-conseils en ressources humaines (RH) avec une maturité numérique intermédiaire (suite Microsoft 365 déjà en place, pas de CRM formel, comptabilité sur QuickBooks). Son budget IA est de 20 000 $/an maximum avec une équipe IT limitée à un seul responsable informatique à temps partiel et aucun développeur dédié. L'entreprise détient des données clients hautement sensibles (dossiers RH) et est pleinement soumise à la Loi 25 (Québec).

| Critère | Brex | Salesforce Einstein | Microsoft Copilot 365 |
|---|---|---|---|
| **1. Rôle spécialisé orchestré** | Directeur financier (CFO) virtuel[cite: 4]. | Directeur commercial / analyste prédictif des ventes[cite: 4]. | Adjoint administratif universel[cite: 4]. |
| **2. Impact d'affaires** _(1-5 + justification)_ | **5/5** - Critique : comble un poste inexistant en offrant une gouvernance financière en temps réel impossible autrement pour cette PME sans CFO dédié[cite: 4]. | **2/5** - Faible : sans CRM structuré ni données historiques d'opportunités, les prédictions seront non fiables et l'agent sous-utilisé[cite: 4]. | **4/5** - Élevé : gain de productivité immédiat pour 100 % des employés (rédaction, résumés, analyse Excel) visible dès la première semaine[cite: 4]. |
| **3. Faisabilité PME** _(1-5 + justification)_ | **4/5** - Bonne : intégration native avec QuickBooks et cartes corporate Brex en moins de 2 semaines, sans compétences IT requises[cite: 4]. | **1/5** - Très faible : exige un CRM Salesforce existant avec des données propres sur 12+ mois et un coût d'implémentation de 80-150 K$ hors budget[cite: 4]. | **5/5** - Excellente : suite Microsoft 365 déjà présente, activation en 1 clic admin, formation minimale via licences M365 Business Premium[cite: 4]. |
| **4. Coût estimé** _(annuel/TCO)_ | ~12 000 - 18 000 $/an tout inclus. TCO bas limité au coût d'abonnement et aux cartes Brex, sans intégration complexe[cite: 4]. | ~25 000 $/an (licences seules) + 80-150 K$ d'implémentation CRM. TCO de 100-170 K$ l'an 1, totalement hors budget[cite: 4]. | ~7 200 $/an (50 employés x 30 $/mois). Si M365 existe déjà, le surcoût net se situe entre 3 000 et 6 000 $/an[cite: 4]. |
| **5. Risque principal** _(et mitigation)_ | Risque de dépendance à un seul fournisseur pour la fonction financière. **Mitigation** : export mensuel des données et vérification humaine trimestrielle par un comptable externe[cite: 4]. | Risque : biais de prédiction majeur sans données suffisantes (faux signaux). **Mitigation** : N/A (non recommandé et exclu dans ce contexte)[cite: 4]. | Risque Loi 25 lié au traitement de données RH sensibles par l'IA (serveurs hors QC possibles). **Mitigation** : configurer Microsoft Purview et activer la résidence des données au Canada[cite: 4]. |

### Recommandation pour la PME

Il est recommandé de déployer Microsoft Copilot 365 en priorité absolue, car il s'active sur l'infrastructure Microsoft 365 déjà existante pour offrir un gain de productivité immédiat à toute l'équipe avec un TCO maîtrisé[cite: 4]. Brex sera déployé en deuxième priorité pour combler l'absence de CFO interne grâce à son intégration native rapide avec QuickBooks[cite: 4]. Salesforce Einstein est totalement exclu puisque l'entreprise ne possède ni le CRM ni les données requises, rendant le projet techniquement et financièrement infaisable[cite: 4].

---

## Contexte 2 — Grande entreprise de 500+ employés

Grande entreprise québécoise d'assurance collective comptant 620 employés répartis sur 3 bureaux (Montréal, Québec, Toronto). Elle dispose d'une infrastructure robuste avec Salesforce CRM (déployé depuis 4 ans, 180 utilisateurs actifs), un ERP SAP, Microsoft 365 E3, et une équipe IT de 12 personnes. Le budget IA approuvé est de 2,5 M$ sur 3 ans sous une gouvernance stricte (6 niveaux d'approbation, conformité AMF/LPRPDE/Loi 25, et DPO nommé).

| Critère | Brex | Salesforce Einstein | Microsoft Copilot 365 |
|---|---|---|---|
| **1. Rôle spécialisé orchestré** | Contrôleur financier junior / analyste FP&A[cite: 4]. | Directeur des ventes augmenté / analyste CRM[cite: 4]. | Adjoint exécutif universel (résumés ComEx, analyse Excel actuariel, rapports FR/EN)[cite: 4]. |
| **2. Impact d'affaires** _(1-5 + justification)_ | **2/5** - Limité : un CFO, une équipe FP&A et un ERP SAP sont déjà en place. Sans intégration avec SAP, la valeur marginale est faible et fait doublon[cite: 4]. | **5/5** - Très élevé : 180 commerciaux utilisent déjà le CRM. Einstein peut augmenter de 25-35 % le taux de conversion des opportunités, impactant directement le CA[cite: 4]. | **4/5** - Élevé : gain de productivité transversal pour les 620 employés, forte valeur en rédaction bilingue et synthèses de réunions multi-équipes[cite: 4]. |
| **3. Faisabilité grande entreprise** _(1-5 + justification)_ | **1/5** - Très faible : conçu pour les PME/startups et incompatible avec SAP ERP. Aucune API native et gouvernance financière complexe non supportée[cite: 4]. | **5/5** - Excellente : Salesforce est déjà implanté avec 4 ans d'historique de données propres. S'active en add-on via une équipe IT interne compétente[cite: 4]. | **4/5** - Bonne : M365 E3 est déjà présent, mais requiert un upgrade vers E5 ou l'achat d'add-ons Copilot, en plus de gérer la gouvernance Loi 25[cite: 4]. |
| **4. Coût estimé** _(licences + intégration + formation)_ | N/A (non pertinent). Le coût de transition de SAP vers Brex serait prohibitif (500 K$+) ; la solution ne doit pas être déployée[cite: 4]. | ~180-220 K$/an (licences). Intégration : 30-50 K$. Formation : 20 K$. TCO de l'année 1 évalué entre 250 et 290 K$ pour un ROI estimé à 18 mois[cite: 4]. | ~225 K$/an (500 utilisateurs x 37,50 $/mois). Intégration et gouvernance Purview : 40-60 K$. Formation : 30 K$. TCO de l'année 1 estimé entre 300 et 350 K$[cite: 4]. |
| **5. Risque principal** _(et mitigation)_ | Risque de fragmentation des données financières s'il est déployé en parallèle du système SAP centralisé. **Mitigation** : Ne pas déployer[cite: 4]. | Risque de biais algorithmique dans le scoring et discrimination de profils clients (enjeu AMF). **Mitigation** : audit trimestriel du modèle et supervision humaine obligatoire sur les contrats > 100 K$[cite: 4]. | Risque Loi 25 sur les données hautement sensibles (polices, clients, employés). **Mitigation** : déploiement de Microsoft Purview, résidence des données au Canada configurée et validation par le DPO[cite: 4]. |

### Recommandation pour la grande entreprise

La priorité stratégique est d'implanter Salesforce Einstein, car l'organisation possède déjà le CRM avec 4 ans de données propres et 180 utilisateurs actifs, permettant un add-on rapide avec un impact commercial direct (hausse de 25-35 % des conversions)[cite: 4]. Microsoft Copilot 365 sera déployé en parallèle pour la productivité transversale, mais débutera par un pilote restreint de 50 utilisateurs afin de valider la conformité stricte à la Loi 25[cite: 4]. Brex est définitivement exclu en raison de son incompatibilité technique avec l'ERP SAP et des risques de fragmentation des données financières[cite: 4].

---

## Synthèse — ce que la grille révèle

Le critère qui a fait basculer les deux décisions est la faisabilité organisationnelle et l'intégration aux systèmes existants, plutôt que la simple puissance technique des outils[cite: 4]. Salesforce Einstein est objectivement l'agent le plus sophistiqué pour l'analyse prédictive, mais il obtient un score de 1/5 en faisabilité pour la PME (faute de CRM) et de 5/5 pour la grande entreprise qui possède l'historique de données nécessaire[cite: 4]. Cela démontre qu'il n'existe pas de « meilleur agent en absolu » : la sélection d'une solution IA dépend entièrement de l'infrastructure en place et du contexte réglementaire local (comme la Loi 25 et les exigences de l'AMF au Québec), qui transforment radicalement les scores de risque et de faisabilité par rapport au marché américain[cite: 4].

---

