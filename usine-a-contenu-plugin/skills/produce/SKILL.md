---
name: produce
description: Produire un contenu complet à partir d'une idée validée. Applique le profil éditorial de l'espace actif. Supporte tous les formats. Se déclenche uniquement après validation explicite d'une idée, sur "rédige [format] sur [sujet]", "écris un article sur [sujet]", ou après un "go pour le n°X" en sortie de ideation.
---

# Skill — Produce

---

## Étape 1 — Contexte

Lis `CLAUDE.md` de l'espace actif : ton éditorial, audience, contraintes, mots-clés SEO.
Consulte `references/formats.md` pour les specs du format demandé.

---

## Étape 2 — Produire

Applique les specs du format et le profil éditorial de l'espace.

Règles : ton éditorial de l'espace (pas générique), mots-clés intégrés naturellement, valeur concrète, pas d'introduction vague, angle clair.

---

## Étape 3 — Enchaînements proposés

Après la production :
> "Tu veux que j'optimise ce contenu pour le SEO et le GEO ?"
→ Si oui, active `optimize`

> "Tu veux que je génère les métadonnées Ghost pour cet article ?"
→ Si oui, active `ghost-seo`

> "Tu veux publier ce contenu sur une plateforme ?"
→ Si oui, active `publisher`

---

## Étape 4 — Tracker & MEMORY.md

Mets automatiquement à jour le tracker de l'espace actif (`content-tracker.json`) :
- Si le sujet était dans `idées` : retire l'entrée correspondante
- Ajoute une entrée dans `contenus` avec `statut: "prêt"` et la date du jour

Puis demande :
> "Je note ce contenu dans la mémoire de l'espace ?"

Si oui, ajoute dans `MEMORY.md` :
```
[Titre] | [Format] | [Date] | Produit — en attente de publication
```
