---
name: ideation
description: Analyser des résultats de recherche ou de veille et proposer un batch d'idées de contenu à valider. Arrêt forcé avant production. Se déclenche sur "propose-moi des idées", "donne-moi des idées sur [sujet]", "qu'est-ce que je pourrais faire comme contenu sur [thème]", ou en sortie de research et watch.
---

# Skill — Ideation

---

## Étape 1 — Contexte

Lis dans l'ordre :
1. `CLAUDE.md` de l'espace actif
2. `MEMORY.md` — sujets traités, idées refusées
3. Résultats de recherche/veille disponibles dans la session

---

## Étape 2 — Générer les idées

**5 à 8 idées numérotées.** Pour chaque :

```
**[N°] [Titre accrocheur]**
Format : [format recommandé]
Angle : [1-2 phrases]
Pourquoi maintenant : [lien avec recherche/veille ou pertinence SEO]
```

Règles : varier les formats, éviter les sujets déjà traités, adapter le ton de l'espace.

---

## Étape 3 — Arrêt forcé (obligatoire)

Termine **toujours** par :

> "Laquelle ou lesquelles tu veux développer ? Donne-moi le(s) numéro(s) et je produis."

**Ne jamais passer à `produce` sans validation explicite.**

---

## Étape 4 — Après validation

1. Propose d'enregistrer les idées validées dans `MEMORY.md`
2. Active `produce` avec l'idée, son format et son angle
