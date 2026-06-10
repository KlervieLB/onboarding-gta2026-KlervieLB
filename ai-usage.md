# Divulgation d'usage de l'IA — ai-usage.md

Remplissez ce fichier pour chaque milestone avant de soumettre. Si aucun outil IA n'a été utilisé, écrivez « Aucun » dans chaque section et signez. Obligatoire même en cas d'absence d'usage.

---

## 1. Outils utilisés

**Outil 1 :** Perplexity AI  
**Version / date d'accès :** Version Web (Pro), juin 2026

**Outil 2 :** Gemini  
**Version / date d'accès :** Advanced / Gemini 1.5 Pro, juin 2026

**Outil 3 :** IA intégrée GitHub Codespaces (GitHub Copilot Chat)  
**Version / date d'accès :** Extension VS Code, juin 2026

---

## 2. Ce qu'ils m'ont aidé à faire

* **Perplexity AI (Base de réflexion) :** Recherche de benchmarks sectoriels sur l'automatisation du KYC dans les PME financières et extraction d'exemples de structures de coûts/gains de temps réels pour crédibiliser les hypothèses d'affaires.
* **Gemini (Rédaction et structure) :** Structuration du mémo exécutif selon le format PRRP, formulation claire des arguments d'affaires et raffinement de la logique de valorisation de la rétention client (calcul du coût du churn).
* **IA intégrée Codespaces (Audit et Alignement) :** Validation technique de l'arborescence multi-agents, vérification de la cohérence de la pipeline séquentielle entre les scripts d'agents (`diagnostic.py`, `compliance.py`, etc.) et génération des squelettes de code pour simuler les points d'arrêt humains dans `app_v2.py`.

---

## 3. Sources et chiffres que j'ai vérifiés moi-même

* **Données du cas FinServ Québec :** J'ai validé manuellement que toutes les équations financières et opérationnelles utilisaises reprenaient strictement les contraintes du laboratoire : 4 ETP conformité, volume de 1 200 dossiers/mois, délai actuel de 3 jours, enveloppe budgétaire maximale de 300 K$ et coût de la phase de POC ciblé à 200 K$.
* **Cadre réglementaire :** Vérification des exigences de l'Autorité des marchés financiers (AMF) et des dispositions de la Loi 25 (Québec) concernant la non-délégabilité de la décision réglementaire à un algorithme et l'obligation d'hébergement local des données.

---

## 4. Ce que j'ai modifié ou rejeté

* **Rejet de l'automatisation totale :** L'IA proposait initialement d'approuver automatiquement et sans regard humain les 70 % de dossiers jugés "standards" pour maximiser le ROI. J'ai rejeté cette approche pour imposer une validation humaine obligatoire (Human-in-the-loop) sur 100 % des dossiers afin de respecter l'AMF.
* **Modification du modèle RH (Licenciements) :** L'agent financier de l'IA calculait un ROI basé sur la suppression pure et simple de 2 postes d'analystes. J'ai modifié ce raisonnement pour intégrer une réaffectation stratégique de ces employés vers les dossiers complexes et la gestion du churn client.
* **Arbitrage technologique (Sur-mesure vs SaaS) :** L'IA penchait pour le développement technique d'un grand modèle de langage propriétaire hébergé à l'interne. J'ai bloqué cette piste pour imposer une intégration SaaS existante (Salesforce Einstein), seule approche réaliste au vu du budget de 300 K$.

---

## 5. Déclaration de responsabilité

Je déclare que le contenu final reflète mon jugement personnel. Je suis responsable de l'exactitude, de la pertinence et du raisonnement — outil IA utilisé ou non.

**Nom :** Klervie LE BAYON  
**Date :** 10 juin 2026
