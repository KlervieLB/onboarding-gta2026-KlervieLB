# L3 — Canevas de cas d'usage IA

**Étudiant·e** : Klervie LE BAYON
**Séance** : S03 — Du cas d'usage au déploiement : structurer un projet IA 

## Cas d'usage choisi

**Secteur** : Finance / Services financiers.
**Processus ciblé** : Analyse automatisée du risque de crédit aux PME.

---

## Section 1 — Problème d'affaires précis

Les analystes consacrent en moyenne 4 à 6 heures à l'évaluation manuelle d'un dossier (collecte, calcul de ratios, vérification, rédaction), ce qui entraîne des délais de décision de 5 à 10 jours ouvrables. Le coût de l'inaction se traduit par une perte de clients au profit de fintechs capables de répondre en quelques heures, une expérience client dégradée ainsi qu'un risque d'erreurs humaines dans les calculs de ratios.

---

## Section 2 — Rôle spécialisé que l'agent orchestre

Analyste crédit senior spécialisé PME.

---

## Section 3 — Données nécessaires et disponibilité

Le déploiement s'appuie sur des données internes disponibles : les états financiers des demandeurs (PDF/numérique dans le CRM), l'historique des décisions de crédit sur 5 ans (base SQL) et les scores de bureaux de crédit (via API). Il nécessite également l'acquisition de données sectorielles de référence (Statistique Canada / BDC) et l'intégration de flux bancaires en temps réel via Open Banking dans le respect de la Loi 25.

---

## Section 4 — Solution IA proposée

Un agent LLM multimodal (ex. GPT-4o ou Claude Sonnet) combinant un OCR avec extraction structurée en JSON, un moteur de calcul de ratios déterministe par règles comptables et un système RAG basé sur les politiques de crédit internes. L'infrastructure cible est Azure OpenAI pour assurer l'hébergement canadien et la conformité SOC 2, opérant selon une architecture human-in-the-loop où l'analyste approuve la recommandation générée.

---

## Section 5 — Métriques de succès

| Type | Métrique | Valeur cible |
|---|---|---|
| Technique | Précision de la recommandation vs décision finale analyste | ≥ 85% |
| Technique | Temps de traitement automatisé d'un dossier standard | < 15 min |
| Affaires | Réduction du délai moyen de décision crédit | de 5 jours → 1 jour |
| Affaires | Capacité de traitement mensuelle (dossiers / analyste) | +40% |

---

## Section 6 — Risques et mitigations

**Risque principal** : Erreur de classification crédit (faux positif) où l'agent approuve un dossier qui aurait dû être refusé en raison d'une mauvaise interprétation des états financiers ou de données sectorielles périmées.
**Mitigation** : Maintien d'une validation humaine obligatoire pour tous les dossiers du POC, configuration d'un seuil de confiance minimal (≥90%) sous lequel le dossier est escaladé, et audit mensuel des dossiers approuvés face à leur performance réelle à 90 jours.

---

## Section 7 — Plan de déploiement phasé

| Phase | Périmètre | Durée estimée |
|---|---|---|
| POC | Dossiers de renouvellement de crédit < 250 K$ (faible risque, données complètes, décision historique connue). | 6 semaines |
| Pilote | Nouvelles demandes PME jusqu'à 1 M$ avec métriques formelles, gouvernance et formation des analystes. | 3 mois |
| Déploiement | Ensemble du portefeuille PME avec catégorisation par niveau de risque et intégration CRM complète. | 6 mois |

**Sponsor exécutif identifié** : Directeur-trice des risques (Chief Risk Officer).
