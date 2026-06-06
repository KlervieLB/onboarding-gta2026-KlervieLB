# L3 — Canevas de cas d'usage IA — FinServ Québec

**Étudiant·e** : Fka2026  
**Séance** : S04 — Atelier d’intégration : diagnostic et recommandation IA  
**Date limite** : 3 juin 2026

---

## Cas d'usage choisi

**Secteur** : Services financiers  
**Processus ciblé** : Pré-vérification des dossiers KYC pour FinServ Québec

---

## Section 1 — Problème d’affaires précis

Le processus de pré-vérification KYC prend en moyenne 3 jours pour environ 1 200 dossiers par mois. Ce délai retarde l’entrée en relation client, augmente le risque de perte de prospects et crée une charge importante pour les 4 analystes conformité de l’équipe.

La situation est critique dans un marché où FinServ perd 3 à 4 clients par semaine face à des concurrents plus rapides, comme Patrimoine Nexio.

---

## Section 2 — Rôle spécialisé que l'agent orchestre ⭐

Agent IA de pré-vérification KYC, équivalent à un analyste KYC junior augmenté.

Il analyse les dossiers, vérifie la complétude, identifie les pièces manquantes, repère les anomalies et prépare une recommandation formalisée pour validation humaine.

---

## Section 3 — Données nécessaires et disponibilité

- Dossiers clients dans Salesforce CRM
- Documents KYC numérisés
- Notes clients et alertes de conformité
- Règles internes AMF et politiques Loi 25
- Historique des décisions de validation conformité

Les données sont déjà présentes dans les systèmes existants et peuvent être exploitées via un connecteur Salesforce natif.

---

## Section 4 — Solution IA proposée

Déployer une solution SaaS spécialisée KYC avec un connecteur Salesforce natif et hébergement canadien. L’agent doit rester en supervision humaine permanente et ne jamais prendre de décision finale.

La plateforme analysée doit être capable de traiter des documents partiellement numérisés, d’extraire des informations KYC, de signaler les pièces manquantes et de générer un résumé de risques pour l’analyste.

---

## Section 5 — Métriques de succès

| Type | Métrique | Valeur cible |
|---|---|---|
| Technique | Précision de détection des pièces manquantes et anomalies KYC | ≥ 95 % sur les cas standards |
| Affaires | Délai moyen de traitement KYC | Réduction de 3 jours à 1 jour |
| Conformité | Dossiers traités avec supervision humaine et traçabilité | 100 % |

---

## Section 6 — Risques et mitigations

**Risque principal** : Validation ou pré-vérification incomplète par l’agent.

**Mitigation** : Maintenir un humain dans la boucle, fixer un seuil minimal de précision de 90 % pour le POC, et exiger une traçabilité complète de toutes les recommandations.

**Risque** : Non-conformité aux exigences Loi 25 et AMF.

**Mitigation** : Hébergement canadien, registre de traitement, accès limité par rôle, journalisation complète et consentement explicite pour l’usage des données.

**Risque** : Rejet par les analystes ou manque d’adoption.

**Mitigation** : Pilote avec volontaires, formation ciblée, communication sur le rôle d’assistant et décision finale toujours humaine.

---

## Section 7 — Plan de déploiement phasé

| Phase | Périmètre | Durée estimée | Jalon de succès |
|---|---|---|---|
| POC | 100 dossiers KYC standards, Salesforce + documents numérisés | 6 semaines | Gain de temps ≥ 30 % et précision ≥ 90 % |
| Pilote | 2 analystes conformité + 5 conseillers volontaires | 2 à 3 mois | Satisfaction ≥ 80 %, précision ≥ 95 %, aucun incident de conformité |
| Déploiement | Extension graduelle à toute l’équipe conformité | 3 à 6 mois | Délai KYC réduit à 1 jour et adoption majoritaire |

---

*Longueur cible : 300-400 mots. Remettez ce fichier complété sous `portfolio/L3_canevas_cas_usage_FinServ.md`.*
