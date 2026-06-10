# M2 — Mémo exécutif de recommandation IA

**Étudiant·e** : Klervie LE BAYON  
**Équipe initiale** : Lafa7183, Abdi23, Fka2026, Vincentl-uds  
**Spécialisation d'équipe** : Conformité KYC  
**Cas retenu (L3)** : « Agent IA de pré-vérification des dossiers KYC »  
**Séance** : S04 — Atelier d'intégration : diagnostic et recommandation IA  
**Date limite** : remis pendant la séance S04, avant la présentation au DG

---

## En-tête du mémo

**À :** Directeur général, FinServ Québec  
**De :** Klervie LE BAYON · équipe : Lafa7183, Abdi23, Fka2026, Vincentl-uds  
**Objet :** Recommandation de premier déploiement d'agent IA  
**Date :** 3 juin 2026  
**Confidentialité :** Usage interne uniquement

---

## 1. Diagnostic — Rôle spécialisé recommandé

Nous recommandons de déployer en priorité un agent IA de pré-vérification des dossiers KYC, positionné comme assistant de l’analyste conformité. Cet agent ne doit pas prendre de décisions réglementaires finales : il vérifie la complétude des dossiers, identifie les pièces manquantes, synthétise les risques et prépare une proposition de décision pour l’analyste humain.

Éléments clés :
- 12 collaborateurs conformité.
- 4 analystes traitent 1 200 dossiers par mois.
- Délai actuel de pré-analyse : 3 jours.
- Churn constaté : 3 à 4 clients perdus par semaine.
- Dossiers standards : 70-80 % du flux.

Enjeux prioritaires :
- réduire le délai de pré-analyse,
- renforcer la qualité des contrôles AMF,
- limiter les pertes de clientèle liées au temps de traitement.

---

## 2. Solution recommandée

La recommandation porte sur une solution hybride : un agent IA intégré à Salesforce, appuyé par un cockpit de supervision humaine et une traçabilité renforcée.

Ce choix est retenu parce qu’il combine :
- rapidité de déploiement,
- maîtrise réglementaire,
- faible charge TI relative,
- capacité à encadrer un POC mesurable.

Le modèle retenu :
- connecteur Salesforce natif,
- hébergement Canada / Québec ou fournisseur certifié local,
- supervision humaine obligatoire pour toute décision finale,
- gestion différenciée des dossiers standards et des dossiers complexes.

Cette approche est préférable à un développement 100 % interne, trop long et coûteux, et à une solution SaaS non structurée, moins contrôlable pour la conformité.

---

## 3. Budget et ROI estimé

Budget cible : 200 à 250 k$.

Répartition indicative :
- 100-130 k$ : plateforme IA et intégration Salesforce.
- 60-80 k$ : déploiement, tests et mise en production.
- 40-50 k$ : formation, gouvernance et pilotage.

### ROI direct

Hypothèses :
- 1 200 dossiers traités par mois.
- gain de 15 à 20 minutes par dossier.
- coût horaire moyen d’un analyste : 50 $.

Résultats estimés :
- 15 min × 1 200 = 300 h / mois → 15 000 $/ mois → 180 000$ / an.
- 20 min × 1 200 = 400 h / mois → 20 000 $/ mois → 240 000$ / an.

Le projet atteint un ROI direct proche du coût initial dès la première année.

### Valeur de rétention client

Hypothèse de churn : 3,5 clients perdus par semaine.
Valeur client moyenne : 15 000 $.
Impact annuel estimé : 2,73 M$.

Cette valeur illustre que le gain financier réel dépasse largement les seuls gains de productivité, en valorisant la rétention et l’expérience client.

---

## 4. Contraintes réglementaires adressées

Le dispositif respecte la posture AMF en maintenant l’humain comme décideur final. L’agent IA agit comme une aide à l’analyse, sans validation automatique finale.

Principes de conformité :
- supervision humaine pour toute décision finale,
- traçabilité de bout en bout des recommandations IA,
- registre de traitement conforme Loi 25,
- hébergement au Canada / Québec,
- accès restreint selon les rôles.

Mesures concrètes :
- journalisation complète (acteur, action, résultat, horodatage),
- comité de revue mensuel des cas limites,
- escalade automatique pour les dossiers PEP, montants élevés ou juridictions sensibles.

Ces mesures garantissent le respect des exigences AMF et de Loi 25 tout en permettant l’accélération des dossiers standards.

---

## 5. Plan de déploiement en 3 phases

| Phase | Contenu | Durée | Jalon de succès |
|-------|---------|-------|-----------------|
| Phase 1 — POC | Test sur 100 dossiers standards, intégration Salesforce, détection de pièces manquantes et synthèse de risques. | 6 semaines | Réduction de 30 % du temps de préanalyse et précision ≥ 90 %. |
| Phase 2 — Pilote | Déploiement auprès de 2 analystes conformité et 5 conseillers volontaires. Évaluation de l’adoption, de la qualité des recommandations et de la conformité. | 2-3 mois | Satisfaction ≥ 80 %, précision ≥ 95 % sur les cas standards, aucun incident de conformité. |
| Phase 3 — Déploiement | Extension progressive à l’ensemble de l’équipe conformité, gouvernance active, audits mensuels et tableau de bord. | 3-6 mois | Délai moyen KYC réduit à 1 jour et adoption majoritaire. |

---

## 6. Métriques de succès à 6 mois

| Type | Métrique | Valeur cible |
|------|----------|--------------|
| Technique | Précision de détection des pièces manquantes et anomalies | ≥ 95 % |
| Opérationnel | Délai moyen de préanalyse KYC | 1 jour |
| Conformité | Dossiers validés avec supervision humaine | 100 % |
| Commercial | Réduction du churn client | -30 % |

---

## 7. Clause go/no-go

La décision de passer à la phase pilote doit être prise à l’issue du POC de 6 semaines.

Critères :
- précision de détection ≥ 90 %,
- gain de temps net ≥ 15 % par dossier,
- exigence de gouvernance maintenue sans allongement du délai global.

Si ces critères ne sont pas atteints, le projet devra être suspendu ou réorienté vers un périmètre plus restreint avec un nouveau POC.

Si les critères sont atteints, lancement du pilote avec 2 analystes et 5 conseillers volontaires.

---

## 8. Architecture d'orchestration multi-agents et arbitrages humains

Cette section documente l'infrastructure technique développée sous GitHub Codespaces et la manière dont le pilotage humain a configuré la décision stratégique pour FinServ Québec.

### (1) Faiblesses de la version d'équipe initiale corrigées
Le travail initial réalisé avec mon équipe (Lafa7183, Abdi23, Fka2026, Vincentl-uds) a été audité et renforcé sur trois faiblesses majeures :
1. **Absence de quantification financière (ROI) :** Le premier mémo se contentait de bénéfices qualitatifs ("réduire les coûts"). Cette orchestration a forcé l'intégration stricte des métriques opérationnelles du cas (4 ETP, 1 200 dossiers/mois).
2. **Conformité déclarative non opérationnelle :** La version d'équipe demandait de "s'assurer de la conformité" de manière magique. L'orchestration actuelle l'opérationnalise par des barrières de code (Human-in-the-loop strict, journalisation).
3. **Flou sur l'arbitrage technologique :** La première version n'expliquait pas l'exclusion d'un développement sur mesure. L'orchestration a permis d'évaluer rationnellement le modèle SaaS.

### (2) Spécification technique de la séquence d'agents
L'infrastructure visible dans notre dépôt Codespaces repose sur un script d'orchestration (`app_v2.py`) distribuant le travail de manière modulaire à travers des agents et des configurations de prompts isolés :
Codespace Root
├── agents/
│   ├── diagnostic.py   --> Évalue le goulot d'étranglement (3 jours de délai)
│   ├── options.py      --> Compare les approches de déploiement (SaaS vs Sur-mesure)
│   ├── solution.py     --> Configure l'intégration Salesforce et l'architecture hybride
│   ├── compliance.py   --> Injecte les contraintes AMF et Loi 25
│   ├── finance.py      --> Calcule le ROI direct et la valeur de rétention client
│   └── writer.py       --> Formate et assemble le mémo exécutif final
├── prompts/
│   └── [diagnostic/options/solution/compliance/finance/writer].txt
├── config.py           --> Variables globales (300 K$ max, 1 200 dossiers, 4 ETP)
└── app_v2.py           --> Point d'entrée de la pipeline avec points d'arrêt humains

La séquence s'exécute de manière linéaire : `diagnostic` $\rightarrow$ `options` $\rightarrow$ `solution` $\rightarrow$ `compliance` $\rightarrow$ `finance` $\rightarrow$ `writer`. Chaque agent puise ses instructions métiers dans son fichier correspondant du dossier `/prompts`.

### (3) Points de contrôle et arbitrages de l'humain dans la boucle (Checkpoints)
Trois interventions humaines critiques ont été programmées dans `app_v2.py` pour rejeter ou modifier les comportements natifs de l'IA :
* **Arbitrage 1 (Fichier : `agents/compliance.py`) :** L'agent de conformité cherchait initialement à optimiser la rapidité en autorisant une validation 100 % automatisée (sans intervention humaine) pour 70 % des dossiers jugés "standards". **J'ai rejeté cette sortie** pour imposer une barrière technique stricte conforme à l'AMF : l'IA ne fait que de la pré-vérification ; le clic de validation finale reste l'apanage exclusif de l'analyste.
* **Arbitrage 2 (Fichier : `agents/finance.py`) :** L'agent financier calculait le ROI sur une pure logique de réduction de coûts en supprimant 2 postes d'analystes. **J'ai modifié cette hypothèse** dans le code pour réaffecter ces 2 ETP libérés vers la gestion des cas complexes et l'expérience client, transformant une logique de coupure budgétaire en levier de réduction du *churn* client (gain estimé de 2,73 M$).
* **Arbitrage 3 (Fichier : `agents/options.py`) :** L'agent d'options penchait vers une infrastructure LLM sur mesure construite en interne. **J'ai forcé le paramètre** vers un connecteur SaaS natif (Salesforce Einstein) afin de respecter le budget maximal de 300 K$ imposé dans `config.py` (le sur-mesure consommant l'enveloppe dès la phase de POC).

### (4) Angle créatif : L'agent comme "Tuteur de Conformité augmenté"
Une IA seule conçoit l'automatisation comme un outil brut de productivité (extraire des données pour aller plus vite). L'angle créatif apporté à cette orchestration consiste à programmer l'agent pour qu'il agisse comme un **Tuteur de Conformité augmenté**. 
Lorsqu'il détecte un document manquant ou une anomalie, l'agent ne se contente pas de lever un drapeau : il génère une note explicitative citant l'article de la Loi 25 ou la directive de l'AMF concernée. L'outil ne déqualifie pas le personnel de FinServ Québec ; au contraire, il devient un outil de formation continue automatisé permettant de faire monter rapidement en compétences les analystes juniors de l'organisation.
