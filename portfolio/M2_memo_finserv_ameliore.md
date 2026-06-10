# M2 — Mémo exécutif de recommandation IA

**Étudiant·e** : KlervieLB ou Klervie LE BAYON  
**Équipe initiale ** : Lafa7183, Abdi23, Fka2026, Vincentl-uds  
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
- 15 min × 1 200 = 300 h / mois → 15 000 $ / mois → 180 000 $ / an.
- 20 min × 1 200 = 400 h / mois → 20 000 $ / mois → 240 000 $ / an.

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

## 8. Orchestration multi-agents et arbitrage humain dans la boucle

La méthodologie proposée repose sur quatre axes :
- diagnostic spécialisé,
- solution IA assistée,
- gouvernance réglementaire,
- arbitrage humain documenté.

Le pilotage du projet s’appuie sur un acteur IA pour la pré-vérification, un analyste humain pour la décision finale et un cockpit de gouvernance pour la traçabilité.

Hypothèses fondamentales :
- l’humain reste garant de la conformité AMF,
- la valeur économique repose sur la rétention client autant que sur la productivité,
- la documentation des recommandations IA est indispensable pour l’auditabilité.

Arbitrages clés :
- prioriser la conformité sur la vitesse pour les dossiers à risque élevé,
- accélérer les dossiers standards par l’automatisation,
- maintenir un comité mensuel de revue des cas limites.

Cette organisation garantit un modèle professionnel et aligné sur les exigences opérationnelles et réglementaires de FinServ.
