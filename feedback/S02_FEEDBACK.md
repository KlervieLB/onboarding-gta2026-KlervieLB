# Rétroaction automatisée -- S02 (Sélectionner des solutions IA : décision, opérations, productivité)

_Générée le 2026-05-28T17:35:24+00:00 -- Run `20260528T172647Z-afdf4262`_

Ce document est produit par un pipeline reproductible (vérification SQL déterministe + analyse LLM du brief et de la déclaration IA). Une revue humaine précède toujours sa publication. **À ce stade expérimental, aucune note ni étiquette de niveau n'est diffusée : l'objectif est purement formatif.**

---

## 1. Vérification automatique de la requête SQL

La vérification automatique n'a pas pu être réalisée (gate non applicable (type=text_artifact, must_run=False)).


## 2. Rétroaction pédagogique sur le brief

> Le livrable contient une bonne structure et la checklist attendue, mais la majorité des tableaux et des sections clés restent vides. Avant remise finale, complétez les contextes, remplissez la grille avec justifications chiffrées et ajoutez ai-usage.md.

### Observations par dimension

**Contexte organisationnel**
- Observation : Le document indique les sections « Contexte 1 — PME de 50 employés » et « Contexte 2 — Grande entreprise de 500+ employés » mais ne décrit pas le secteur, la maturité numérique, le budget ou l'équipe IT.
- Piste d'amélioration : Compléter chaque contexte par taille, secteur, maturité numérique, budget IA approximatif et composition de l'équipe IT, et expliquer en une phrase pourquoi ces éléments modifient la recommandation entre PME et grande entreprise.

**Justification criteres**
- Observation : La grille pour les 5 critères est présente mais toutes les cellules sont vides, sans justification chiffrée ni hypothèse vérifiable pour impact, faisabilité, coût ou risque.
- Piste d'amélioration : Remplir chaque cellule de la grille pour les trois agents et les deux contextes en fournissant une justification factuelle (chiffres, exigences techniques, estimation coût) pour chacun des quatre critères.

**Role specialise identifie**
- Observation : La ligne « 1. Rôle spécialisé orchestré » est incluse dans les tableaux mais les colonnes pour Brex, Einstein et Copilot sont vides.
- Piste d'amélioration : Nommer pour chaque agent un rôle métier précis (ex. « contrôleur financier augmenté ») et décrire en une phrase la valeur métier créée (effet sur revenus, coûts ou temps).

**Recommandation argumentee**
- Observation : Les sections « Recommandation pour la PME » et « Recommandation pour la grande entreprise » sont laissées en blanc, sans position ni analyse de compromis.
- Piste d'amélioration : Formuler une recommandation distincte par contexte (2–3 phrases chacune) appuyée sur les scores de la grille et expliciter pourquoi les autres options sont écartées (compromis valeur/risque/coût).

**Ai disclosure**
- Observation : La checklist rappelle « Mettez à jour `ai-usage.md` » mais le rendu ne contient pas le fichier ni de déclaration d'usage d'IA.
- Piste d'amélioration : Ajouter un fichier ai-usage.md indiquant les outils (ou « aucun »), l'étape d'utilisation, la validation humaine effectuée et les limites observées.

_Quelques points appellent une attention particulière lors de la prochaine itération : grille_incomplète, ai_usage_absent._

## 3. Déclaration d'utilisation de l'IA

> Le fichier soumis est le gabarit non rempli et ne contient pas d'informations sur l'utilisation d'IA. Veuillez compléter chaque section avec des détails précis (nom et version de l'outil, étape d'utilisation, validation humaine et limites observées).

**Sujets à ajouter ou expliciter pour la prochaine itération :**

- outils utilisés (nom + version/modèle)
- à quelle étape l'IA a été utilisée
- comment la sortie a été validée par l'humain
- limites ou erreurs observées

## 4. Pistes d'action pour la prochaine itération

- Réviser le brief en tenant compte des observations par dimension de la section 2.
- Compléter `ai-usage.md` en y ajoutant : outils utilisés (nom + version/modèle).
- Compléter `ai-usage.md` en y ajoutant : à quelle étape l'IA a été utilisée.
- Compléter `ai-usage.md` en y ajoutant : comment la sortie a été validée par l'humain.
- Compléter `ai-usage.md` en y ajoutant : limites ou erreurs observées.

---

## 5. Traçabilité

- **Run ID :** `20260528T172647Z-afdf4262`
- **Devoir :** `S02`
- **Étudiant·e :** `KlervieLB`
- **Commit analysé :** `7b7cb8c`
- **Audit (côté instructeur) :** `tools/instructor/feedback_pipeline/audit/20260528T172647Z-afdf4262/KlervieLB/`
- **Prompts (SHA-256) :**
  - `rubric_grader_system` : `505f32d1d8319d66...`
  - `ai_usage_grader_system` : `81cb7fdf89bda55a...`
- **Fournisseur (rubrique) :** `openai`
- **Fournisseur (IA-usage) :** `openai` (gpt-5-mini-2025-08-07)

_Ce feedback a été produit par un pipeline automatisé et **revu par l'équipe pédagogique avant publication**. Aucun chiffre ni étiquette de niveau n'est diffusé à ce stade expérimental : l'objectif est uniquement formatif. Ouvrez une issue dans ce dépôt pour toute question._
