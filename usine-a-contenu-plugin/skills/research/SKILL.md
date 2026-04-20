---
name: research
description: Rechercher ce qui existe sur YouTube et Google sur une thématique donnée. Produit une synthèse des contenus trouvés, des angles dominants et des opportunités détectées. Utiliser ce skill dès que l'utilisateur veut explorer un sujet. Se déclenche sur "cherche ce qui se fait sur [sujet]", "trouve les meilleurs contenus sur [thème]", "qu'est-ce qui existe sur [sujet]", "recherche YouTube/Google sur [thème]".
---

# Skill — Research

Recherche sur YouTube et/ou Google les contenus existants sur une thématique.

---

## Étape 1 — Contexte

Lis `CLAUDE.md` de l'espace actif. Si non précisé, demande lequel utiliser.
Si la thématique est vague, demande une précision avant de lancer.

---

## Étape 2 — Recherche

### Google : 2 à 4 requêtes ciblées
- Types de contenus dominants, angles couverts, lacunes

### YouTube : 2 à 3 recherches
- Vidéos les plus vues, formats dominants, angles récurrents, ce qui manque

---

## Étape 3 — Synthèse

```
## Recherche : [thématique]
Espace : [nom] | Date : [date]

### Ce qui domine
[3-5 points]

### Ce qui manque
[2-4 angles sous-exploités]

### Opportunités détectées
[2-4 idées concrètes]

### Sources notables
[Sources/vidéos avec URL]
```

---

## Étape 4 — Transition

> "Tu veux que je parte de ces résultats pour te proposer des idées ?"

Si oui, active `ideation`.
