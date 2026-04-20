---
name: persona-builder
description: Créer des fiches personas structurées à partir de sources variées. Format fixe pour permettre aux skills ideation et produce de s'y référer de façon fiable. Se déclenche sur "crée un persona", "définis mon audience", "qui sont mes lecteurs", "fais une fiche persona pour [prénom]", ou depuis /usine-a-contenu:strategy.
---

# Skill — Persona Builder

---

## Étape 1 — Choisir les sources

Consulte `references/persona-methods.md` pour les instructions de traitement par type de source.

```
Quelles sources as-tu pour construire ce persona ?
```

AskUserQuestion multiSelect :
- 📞 Transcriptions d'appels clients / interviews
- ⭐ Avis clients (Google, Trustpilot, Amazon, etc.)
- 🔴 Reddit / forums / commentaires
- 📋 Interviews ou formulaires
- 🔍 Recherche web (comportements de l'audience)
- 💡 Description intuitive (je sais qui c'est)

---

## Étape 2 — Collecte selon les sources

**Transcriptions / interviews :** demande de coller le texte ou de décrire les éléments clés.

**Avis clients :** demande les avis (copier-coller ou URL). Analyse les patterns récurrents, les formulations exactes, les frustrations et les résultats obtenus.

**Reddit / forums :** demande les URLs ou extraits. Identifie le vocabulaire utilisé, les questions récurrentes, les objections.

**Recherche web :** lance des recherches sur les comportements et problématiques de l'audience. S'appuie sur `CLAUDE.md` pour le contexte.

**Intuitif :** pose 5 questions guidées (problème principal, niveau de maturité, objection principale, canal préféré, résultat désiré).

---

## Étape 3 — Construire la fiche

Format fixe à respecter (pour compatibilité avec `ideation` et `produce`) :

```markdown
## Persona — [Prénom fictif]

### Profil
- **Âge approximatif :** [tranche]
- **Rôle / fonction :** [titre ou situation]
- **Secteur :** [secteur ou contexte]
- **Maturité sur le sujet :** [débutant / intermédiaire / expert]
- **Rapport au digital :** [natif / à l'aise / limité]

### Objectifs principaux
[2-3 points concrets]

### Douleurs et frustrations
[2-4 points — formulés comme le persona le dirait]

### Objections fréquentes
[2-3 points — les freins avant d'agir ou d'acheter]

### Formulations exactes
> "[Verbatim 1 — extrait ou reconstitution fidèle]"
> "[Verbatim 2]"
> "[Verbatim 3]"

### Canaux préférés
[Où il consomme de l'information, dans quel ordre]

### Ce qui résonne avec lui
[Ton, angles, formats, preuves qui fonctionnent]

### Ce qui ne fonctionne pas
[Ce qui le fait décrocher ou le laisse froid]

### Instructions pour la production
- [Règle 1 — ex: toujours partir d'un problème concret]
- [Règle 2 — ex: éviter le jargon technique]
- [Règle 3 — ex: inclure un exemple chiffré]
```

---

## Étape 4 — Enregistrement

Sauvegarde dans `spaces/[espace]/personas/[prenom].md`.

Met à jour MEMORY.md : `Persona créé : [Prénom] — [date]`

> "Tu veux créer un autre persona ou passer au plan éditorial ?"
