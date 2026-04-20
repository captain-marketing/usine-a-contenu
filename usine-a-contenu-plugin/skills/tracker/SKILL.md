---
name: tracker
description: Suivre l'état des contenus d'un espace. Affiche un tableau de bord complet (idées, en cours, prêts, publiés) et permet de gérer les tâches de contenu. Se déclenche sur "Où en sommes nous ?", "état des contenus", "qu'est-ce qui est en cours", "ajoute l'idée", "passe en cours", "marque comme publié", ou toute question sur l'avancement des contenus.
---

# Skill — Tracker de contenus

**Langue : toujours répondre en français.**

---

## Ce que tu fais

Ce skill gère le fichier `content-tracker.json` de l'espace actif. Il permet de consulter l'état des contenus et de le maintenir à jour.

Le fichier est toujours dans : `spaces/[identifiant-espace]/content-tracker.json`

---

## Commandes reconnues

### "Où en sommes nous ?" / "État des contenus" / "Tableau de bord"

Lis le fichier `content-tracker.json` de l'espace actif et affiche un résumé structuré :

```
📊 TABLEAU DE BORD — [Nom de l'espace]
Mis à jour le [date]

💡 IDÉES À TRAITER ([n])
→ [titre] — [tags si présents]

⚙️ EN COURS ([n])
→ [titre] — [format] — commencé le [date]

✅ PRÊT À PUBLIER ([n])
→ [titre] — [format] — [notes si présentes]

📢 PUBLIÉS ([n] ce mois / [total] total)
→ [titre] — [format] — publié le [date]
```

Si le fichier n'existe pas, propose de l'initialiser : `"Je ne trouve pas de tracker pour cet espace. Je l'initialise ?"` puis crée le fichier vide avec la structure de base (voir section Initialisation).

---

### "Ajoute l'idée : [titre]"

Ajoute une entrée dans le tableau `idées` du JSON :

```json
{
  "id": "[prochain id disponible]",
  "titre": "[titre fourni]",
  "format": null,
  "tags": [],
  "notes": "",
  "date_ajout": "[date du jour]"
}
```

Confirme : `"✅ Idée ajoutée : [titre]"`

---

### "Passe [titre] en cours" / "Je travaille sur [titre]"

1. Si le contenu est dans `idées` : le retire des idées et crée une entrée dans `contenus` avec `statut: "en cours"`
2. Si le contenu n'existe pas encore : crée directement l'entrée dans `contenus` avec `statut: "en cours"`

```json
{
  "id": "[prochain id]",
  "titre": "[titre]",
  "format": "[format si connu, sinon null]",
  "statut": "en cours",
  "plateforme": null,
  "notes": "",
  "date_creation": "[date du jour]",
  "date_publication": null,
  "tags": []
}
```

---

### "Marque [titre] comme prêt" / "C'est prêt"

Met à jour `statut` → `"prêt"` et ajoute une note si précisée.
Confirme : `"✅ [titre] marqué comme prêt à publier."`

---

### "Marque [titre] comme publié" / "[titre] est publié"

Met à jour `statut` → `"publié"` et `date_publication` → date du jour.
Confirme : `"✅ [titre] marqué comme publié le [date]."`

---

### "Supprime [titre]" / "Retire [titre]"

Retire l'entrée du JSON (idées ou contenus).
Demande confirmation avant : `"Tu veux vraiment supprimer [titre] du tracker ?"`

---

### "Ajoute une note sur [titre] : [note]"

Met à jour le champ `notes` de l'entrée correspondante.

---

## Mise à jour du fichier

Après chaque modification :
1. Mets à jour `_meta.derniere_mise_a_jour` avec la date du jour
2. Réécris le fichier JSON complet (propre, indenté à 2 espaces)

---

## Initialisation d'un nouvel espace

Quand `new-space` crée un espace, ce skill génère le fichier initial :

```json
{
  "_meta": {
    "description": "Gestionnaire de contenus [Nom de l'espace]",
    "derniere_mise_a_jour": "[date]",
    "statuts_possibles": ["idée", "en cours", "prêt", "publié"]
  },
  "contenus": [],
  "idées": [],
  "archive": []
}
```

---

## Intégration avec produce

Quand le skill `produce` termine la production d'un contenu, il met automatiquement à jour le tracker :
- Retire l'idée de `idées` si elle y était
- Crée une entrée dans `contenus` avec `statut: "prêt"` et la date du jour

---

## Règles générales

- Toujours lire le fichier JSON avant d'écrire pour ne pas écraser des données existantes
- En cas d'ambiguïté sur le titre (plusieurs correspondances), demander lequel
- Si le format n'est pas précisé, le laisser à `null` — ne pas inventer
- Archiver les contenus publiés depuis plus de 60 jours dans le tableau `archive` si demandé
