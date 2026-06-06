# M2 — Mémo exécutif de recommandation IA

**Étudiant·e** : [votre identifiant GitHub]  
**Équipe** : [identifiants GitHub des autres membres]  
**Spécialisation d'équipe** : Conformité KYC  
**Cas retenu (L3)** : [identifiant GitHub de l'auteur·e] — « Agent IA de pré-vérification des dossiers KYC »  
**Séance** : S04 — Atelier d'intégration : diagnostic et recommandation IA  
**Date limite** : remis pendant la séance S04, avant la présentation au DG

---

## En-tête du mémo

**À :** Directeur général, FinServ Québec  
**De :** [votre nom] · équipe : [membres listés en en-tête]  
**Objet :** Recommandation de premier déploiement d'agent IA  
**Date :** 3 juin 2026  
**Confidentialité :** Usage interne uniquement

---

## 1. Diagnostic — Rôle spécialisé recommandé

Nous recommandons de déployer en premier un agent IA de pré-vérification des dossiers KYC, agissant comme analyste KYC junior augmenté. Cet agent ne prend pas de décision réglementaire ou financière seul. Il analyse les dossiers clients, vérifie la complétude des informations, détecte les pièces manquantes, résume les risques et prépare une recommandation pour l’analyste humain.

Ce choix est prioritaire pour FinServ Québec, car l’organisation compte 12 personnes en conformité, dont 4 analystes traitant environ 1 200 dossiers par mois avec un délai actuel de 3 jours. Dans un contexte où l’entreprise perd 3 à 4 clients par semaine depuis le lancement d’un agent IA concurrent chez Patrimoine Nexio, réduire les délais de traitement KYC devient un levier concret pour améliorer l’expérience client tout en respectant les contraintes AMF et Loi 25.

---

## 2. Solution recommandée

Nous recommandons une solution SaaS spécialisée avec connecteur Salesforce natif, plutôt qu’un développement sur mesure. Le budget disponible de 300 K$ rend le SaaS réaliste, alors qu’un développement personnalisé coûterait minimalement 500 K$ à 800 K$ et prendrait environ 18 mois, ce qui est incompatible avec l’urgence du mandat.

La solution devrait être basée sur une plateforme canadienne ou hébergée au Canada, intégrée à Salesforce CRM et capable de traiter les documents KYC partiellement numérisés. Une option réaliste serait une combinaison de Microsoft Copilot Studio / Azure OpenAI avec hébergement canadien, connectée à Salesforce, avec supervision humaine obligatoire. Cette approche limite la charge sur l’équipe TI, déjà à 110 % de capacité, tout en permettant un POC en environ 6 semaines.

Le choix est justifié par trois critères : respect du budget, rapidité d’intégration grâce au connecteur Salesforce et conformité réglementaire plus facile à encadrer qu’une solution entièrement sur mesure.

---

## 3. Budget et ROI estimé

Budget proposé dans l’enveloppe de 300 K$ :

- Coût de déploiement : environ 200 K$ à 250 K$
- 80–120 K$ : licence SaaS et intégration Salesforce
- 60–80 K$ : formation des analystes et conseillers
- 60–80 K$ : tampon pour pilote, gouvernance, ajustements et conformité

Coût opérationnel annuel : environ 80 K$ à 120 K$ pour les licences, le support, les audits et l’amélioration continue.

ROI estimé à 12 mois :

Hypothèse 1 : FinServ traite 1 200 dossiers KYC par mois.

Hypothèse 2 : L’agent réduit le temps de préanalyse de 30 minutes à 10 minutes par dossier, soit un gain de 20 minutes par dossier.

Hypothèse 3 : Le coût chargé moyen d’un analyste conformité est estimé à 50 $/heure.

Calcul estimé :
1 200 dossiers × 20 minutes économisées = 400 heures économisées par mois.  
400 heures × 50 $ = 20 000 $ par mois.  
20 000 $ × 12 mois = 240 000 $ de valeur annuelle estimée.

À cela s’ajoute une valeur indirecte importante : réduction du délai de traitement de 3 jours à environ 1 jour, amélioration de l’expérience client et diminution du risque de perdre des clients au profit de concurrents plus rapides.

ROI estimé : si le projet coûte 250 K$ et génère 240 K$ de valeur annuelle directe, le retour financier direct est presque atteint en 12 mois. En incluant la réduction des pertes clients, le projet devient rentable dès la première année.

---

## 4. Contraintes réglementaires adressées

La recommandation respecte les exigences de l’AMF, car l’agent IA ne prend aucune décision finale. Il peut analyser, résumer, détecter des anomalies et alerter, mais un analyste humain conserve la responsabilité de valider le dossier. La supervision humaine demeure donc obligatoire dans la boucle décisionnelle.

Pour la Loi 25, la solution doit prévoir un registre de traitement, une traçabilité des actions de l’agent, une justification des recommandations et un hébergement au Canada ou au Québec lorsque possible. Les données personnelles financières ne doivent pas être utilisées pour entraîner un modèle externe sans consentement explicite. L’agent doit aussi citer ses sources dans les dossiers KYC pour assurer transparence, auditabilité et responsabilité.

Les décisions de design découlant de ces contraintes sont donc les suivantes : humain dans la boucle, journalisation complète, accès limité selon les rôles, hébergement canadien, consentement documenté et interdiction de validation automatique finale.

---

## 5. Plan de déploiement en 3 phases

| Phase | Contenu | Durée | Jalon de succès |
|-------|---------|-------|-----------------|
| Phase 1 — POC | Tester l’agent sur un sous-ensemble de 100 dossiers KYC standards provenant de Salesforce et de documents numérisés. Valider la capacité à détecter les pièces manquantes et à produire un résumé fiable. | 6 semaines | Réduction d’au moins 30 % du temps de préanalyse et précision minimale de 90 %. |
| Phase 2 — Pilote | Déploiement auprès de 2 analystes conformité et 5 conseillers volontaires. Mesure de l’adoption, de la satisfaction et des écarts entre recommandations IA et validations humaines. | 2 à 3 mois | Satisfaction utilisateur ≥ 80 %, précision ≥ 95 % sur les cas standards, aucun incident de conformité. |
| Phase 3 — Déploiement | Extension graduelle à toute l’équipe conformité. Formation, gouvernance active, tableau de bord de suivi, procédures d’escalade et audits mensuels. | 3 à 6 mois | Délai moyen KYC réduit de 3 jours à 1 jour et adoption par la majorité des analystes. |

---

## 6. Métriques de succès à 6 mois

| Type | Métrique | Valeur cible |
|------|----------|--------------|
| Technique | Précision des détections de pièces manquantes et anomalies KYC | ≥ 95 % sur les cas standards |
| Affaires | Délai moyen de traitement KYC | Réduction de 3 jours à 1 jour |
| Conformité | Dossiers validés avec supervision humaine et traçabilité complète | 100 % des dossiers traités par l’agent |

---

## 7. Clause go/no-go

Nous recommandons une décision go/no-go à la fin du POC de 6 semaines. Le projet doit être arrêté ou réorienté si l’agent n’atteint pas un niveau minimal de performance opérationnelle et réglementaire.

Indicateur : précision de l’agent sur la détection des pièces manquantes et anomalies KYC standards.  
Seuil d'arrêt : précision inférieure à 90 % ou gain de temps inférieur à 15 %.  
Date de décision : fin de la sixième semaine du POC.  
Action si seuil non atteint : suspendre le déploiement, réduire le périmètre aux dossiers les plus simples, renforcer la qualité des données et refaire un POC limité avant tout pilote.

Si les seuils sont atteints, nous recommandons de poursuivre vers un pilote contrôlé avec 2 analystes et 5 conseillers volontaires.

---

## Annexes (hors limite d'une page)

- **Annexe A** : Fiche d’opportunité agentique (`portfolio/S01_fiche_opportunite_agentique.md`)  
- **Annexe B** : Grille de sélection d'agents (`portfolio/M1_grille_selection_agents.md`)  
- **Annexe C** : Canevas de cas d’usage (`portfolio/L3_canevas_cas_usage_FinServ.md`)

Les annexes complètes sont documentées dans le fichier source `portfolio/Source annexe`.

---

*Divulgation IA : si des outils d'IA ont aidé à la rédaction de ce mémo, déclarez-les dans `ai-usage.md`.*
