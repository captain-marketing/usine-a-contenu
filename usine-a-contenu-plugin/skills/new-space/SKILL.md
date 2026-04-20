---
name: new-space
description: Créer un nouvel espace de travail dans le plugin Usine à Contenu. Lance un interview guidé pour configurer le profil éditorial, génère CLAUDE.md, MEMORY.md et sources.md. Se déclenche sur "new-space", "crée un espace", "nouveau projet", "nouveau client", "nouvel espace de travail".
---

# Usine à Contenu — Créer un espace de travail

**Langue : toujours répondre en français, quelle que soit la langue de l'utilisateur.**

Pose les questions **une par une**. L'utilisateur peut taper `/` pour passer une question.

---

## L'interview

### 1. Nom
> "Comment s'appelle ce projet ou client ?"

Génère un identifiant de dossier (minuscules, tirets, pas d'espaces ni d'accents). Exemple : "Captain Marketing" → `captain-marketing`. Confirme avant de continuer.

### 2. Description
> "En une phrase, c'est quoi ce projet ?"

### 3. Audience
> "À qui s'adresse ce contenu ?"

### 4. Formats prioritaires
AskUserQuestion multiSelect :
- 📝 Article de blog
- 📧 Newsletter
- 💼 Post LinkedIn
- 🐦 Tweet / Thread X
- 📸 Post Instagram
- 🎬 Script YouTube court
- 🎬 Script YouTube long

### 5. Ton éditorial
AskUserQuestion :
- Expert et direct
- Pédagogique et accessible
- Inspirant et narratif
- Professionnel et neutre
- Autre (je décris en chat)

### 6. Mots-clés SEO
> "Des mots-clés SEO prioritaires ? (tape / pour passer)"

### 7. Concurrents / sources de référence
> "Des concurrents à surveiller ou sources de référence ? (tape / pour passer)"

### 8. Contraintes
> "Des sujets à éviter ou règles particulières ? (tape / pour passer)"

---

## Création des fichiers

Crée `spaces/[identifiant]/` avec :

### CLAUDE.md
```markdown
# [Nom] — Profil éditorial

## Description
[Réponse 2]

## Audience cible
[Réponse 3]

## Formats prioritaires
[Formats sélectionnés]

## Ton éditorial
[Réponse 5]

## Mots-clés SEO prioritaires
[Réponse 6 ou "À définir"]

## Sources de référence et concurrents
[Réponse 7 ou "Aucun défini"]

## Contraintes
[Réponse 8 ou "Aucune"]

## Style éditorial
[Rempli si une Style Card a été générée — voir style-card.md]

## Rangement des fichiers — règle absolue
Tout fichier produit doit être sauvegardé dans le sous-dossier correspondant à son format. Ne jamais déposer un fichier à la racine de l'espace. Si aucun dossier ne correspond aux règles ci-dessous, demmander à l'utilisateur où ranger le fichier produit.

| Type de contenu | Dossier cible |
|---|---|
| Articles de blog + meta-seo.md | `articles/` |
| Posts LinkedIn | `linkedin/` |
| Tweets et threads X | `x/` |
| Carrousels Instagram | `instagram/` |
| Scripts YouTube | `scripts-video/` |
| Newsletters | `newsletters/` |

## Instructions
Lire ce fichier avant toute production.
Appliquer le ton éditorial et respecter les contraintes.
Si une Style Card est disponible dans cet espace, l'appliquer à toute production.
Consulter MEMORY.md pour éviter les doublons.
```

### MEMORY.md
```markdown
# Mémoire — [Nom]

_Dernière mise à jour : [date]_

## Idées validées en attente de production

## Contenus produits
<!-- Titre | Format | Date | Statut -->

## Sujets déjà traités

## Idées refusées

## Notes et retours
```

### sources.md
```markdown
# Sources de veille — [Nom]

_Dernière mise à jour : [date]_

## Sources actives

| Source | URL | Type | Fréquence | Dernière veille |
|--------|-----|------|-----------|-----------------|

## Sources à explorer

## Mots-clés de veille Google

## Chaînes YouTube à surveiller
```

### content-tracker.json

Crée également ce fichier pour le suivi des contenus :

```json
{
  "_meta": {
    "description": "Gestionnaire de contenus [Nom]",
    "derniere_mise_a_jour": "[date]",
    "statuts_possibles": ["idée", "en cours", "prêt", "publié"]
  },
  "contenus": [],
  "idées": [],
  "archive": []
}
```

### Sous-dossiers de contenu

Crée un sous-dossier pour chaque format sélectionné à l'étape 4, avec un `README.md` minimal dans chacun :

| Format sélectionné | Dossier à créer |
|--------------------|-----------------|
| 📝 Article de blog | `spaces/[identifiant]/articles/` |
| 📧 Newsletter | `spaces/[identifiant]/newsletters/` |
| 💼 Post LinkedIn | `spaces/[identifiant]/linkedin/` |
| 🐦 Tweet / Thread X | `spaces/[identifiant]/x/` |
| 📸 Post Instagram | `spaces/[identifiant]/instagram/` |
| 🎬 Script YouTube court | `spaces/[identifiant]/scripts-video/courts/` |
| 🎬 Script YouTube long | `spaces/[identifiant]/scripts-video/longs/` |

Crée toujours ce dossier commun, quelle que soit la sélection :
- `spaces/[identifiant]/assets/` — images, visuels, ressources partagées

Chaque dossier contient un `README.md` avec ce contenu :
```markdown
# [Nom du dossier] — [Nom du projet]

Ranger ici tous les contenus produits pour ce format.

Format du nom de fichier recommandé : `YYYY-MM-DD-titre-court.md`
```

---

## Étape Style Card — calibrage du style éditorial

Une fois les fichiers créés, propose systématiquement :

> "Pour que je produise du contenu dans ta voix exacte plutôt qu'un style générique, tu peux me donner des exemples de tes contenus existants. Je vais les analyser pour extraire tes patterns d'écriture et créer une Style Card appliquée à toutes les productions de cet espace.
>
> Tu as des exemples à me donner ? Articles, newsletters, posts LinkedIn — 3 à 7 exemples donnent les meilleurs résultats."

AskUserQuestion :
- ✅ Oui, je donne des exemples maintenant
- ⏭️ Je le ferai plus tard
- ❌ Non, le ton décrit suffit

### Si l'utilisateur donne des exemples

1. Demande de coller les contenus ou uploader les fichiers, et/ou fournir des URLs
2. Charge et lit tous les exemples (fichiers uploadés depuis `/mnt/user-data/uploads/` + URLs)
3. Analyse avec le skill `analyseur-style-editorial` — méthode complète : voix, structure, hooks, conclusions, rhétorique, syntaxe, vocabulaire
4. Produit la Style Card au format défini par l'analyseur
5. Sauvegarde dans `spaces/[identifiant]/style-card.md`
6. Ajoute dans la section `## Style éditorial` du `CLAUDE.md` de l'espace :
   ```
   Style Card disponible : spaces/[identifiant]/style-card.md
   Appliquer systématiquement à toute production de contenu pour cet espace.
   ```
7. Résume en 3-4 phrases les patterns les plus distinctifs détectés

### Si l'utilisateur veut le faire plus tard

Note dans `MEMORY.md` sous "Notes et retours" : `Style Card à générer — fournir des exemples de contenus pour calibrer le style éditorial`

---

## Confirmation finale

Résume en 4-5 lignes ce qui a été configuré (fichiers créés + dossiers générés), puis propose :

AskUserQuestion :
- 🔍 Lancer une recherche sur un sujet
- 👁️ Configurer des sources de veille
- ✍️ Produire un premier contenu directement
- ⏸️ C'est bon pour l'instant
