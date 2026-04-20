---
name: watch
description: Surveiller des sources définies et produire un digest des nouveaux contenus publiés. Deux modes : veille manuelle immédiate et veille planifiée détectée à l'ouverture de session. Se déclenche sur "surveille [source]", "qu'est-ce qu'a publié [source]", "fais une veille sur [source]". Se déclenche aussi automatiquement si des sources planifiées sont en retard.
---

# Skill — Watch

---

## Mode 1 — Veille manuelle

1. Extrais l'URL ou le nom depuis la demande
2. Charge le contenu (30 derniers jours par défaut)
3. Produis le digest :

```
## Veille : [source]
URL : [url] | Période : [dates] | Espace : [nom] | Date : [aujourd'hui]

### Publications récentes
[Titre | Format | Date | Résumé 1 ligne]

### Points notables
[2-4 observations]

### Idées déclenchées
[1-3 idées pour l'espace actif]
```

4. Propose de mettre à jour la date dans `sources.md`

---

## Mode 2 — Veille planifiée

Au démarrage de session, lis `sources.md`. Si des sources sont en retard sur leur fréquence :

> "La veille planifiée est en retard sur [N] source(s) : [liste]. Tu veux que je la fasse maintenant ?"

C'est une proposition, pas un blocage.

---

## Ajouter une source planifiée

Si l'utilisateur veut une surveillance régulière, ajoute dans `sources.md` : nom, URL, type, fréquence, date de dernière veille = aujourd'hui.
