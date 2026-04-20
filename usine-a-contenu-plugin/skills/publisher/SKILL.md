---
name: publisher
description: Orchestrer la publication d'un contenu produit vers une ou plusieurs plateformes. Vérifie les MCP disponibles, adapte le format si nécessaire, crée des drafts uniquement. Activé par produce après production d'un contenu, ou depuis /usine-a-contenu:publish.
---

# Skill — Publisher

---

## Étape 1 — Identifier le contenu et l'espace

- Contenu de la session en cours (priorité)
- Sinon : liste les contenus en attente depuis MEMORY.md

---

## Étape 2 — Vérifier les MCP disponibles

Vérifie parmi : typefully, wordpress, ghost.

```
[Si Typefully connecté]  ✅ X, LinkedIn, Instagram disponibles via Typefully
[Si WordPress connecté]  ✅ WordPress disponible
[Si Ghost connecté]      ✅ Ghost disponible (MCP communautaire)
[Si absent]              ⚠️  [Plateforme] non disponible → fallback manuel proposé
```

---

## Étape 3 — Sélection des destinations

Consulte `references/platforms.md` pour les compatibilités format/plateforme.

Si incompatibilité détectée :
> "Ce contenu est un [format X]. Voici ce que je peux faire pour [plateforme Y] : [options]. Laquelle tu choisis ?"

**Attendre la validation avant d'envoyer.**

---

## Étape 4 — Publication

### Typefully (X, LinkedIn, Instagram)
1. Demande la date/heure ou "dans la queue"
2. Envoie via MCP en mode draft
3. Fournis le lien vers le draft Typefully

### WordPress
1. Draft ou planifié ? Si planifié : date/heure ?
2. Envoie via MCP
3. Fournis le lien vers le draft WordPress

### Ghost
1. Même logique que WordPress
2. Rappelle le caractère communautaire en cas de première utilisation
3. En cas d'erreur MCP : bascule sur fallback sans bloquer

### Fallback manuel
Formate le contenu selon les specs de `references/platforms.md`, affiche pour copier-coller.

---

## Étape 5 — MEMORY.md

```
[Titre] | [Format] | [Date] | Draft — [Plateforme] — Publication prévue [date]
```
