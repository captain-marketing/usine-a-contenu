---
name: publish
description: Lancer le module Publication. Envoie un contenu produit vers WordPress, X, LinkedIn ou Instagram via les MCP connectés. Crée toujours des drafts, jamais de publication directe. Se déclenche sur "publish", "module publication", "publie ce contenu", "envoie sur [plateforme]", "prépare la publication".
---

# Usine à Contenu — Module Publication

Point d'entrée du module publication. Envoie un contenu produit vers une ou plusieurs plateformes. Crée toujours des drafts, jamais de publication directe.

---

## Étape 0 — Identifier l'espace et le contenu

Si l'espace n'est pas précisé, demande lequel utiliser.

Identifie le contenu à publier :
- Contenu produit dans la session en cours (priorité)
- Sinon : liste des contenus en attente depuis MEMORY.md > "Contenus produits"

---

## Étape 1 — État des connexions MCP

Vérifie quels MCP sont disponibles parmi : wordpress, typefully, ghost.

```
Plateformes disponibles :

[Si Typefully connecté]  ✅ Typefully → X, LinkedIn, Instagram (drafts)
[Si WordPress connecté]  ✅ WordPress → blog WordPress (draft ou planifié)
[Si Ghost connecté]      ✅ Ghost → blog Ghost (MCP communautaire)

[Si Typefully absent]    ⚠️  Typefully non connecté → X, LinkedIn, Instagram indisponibles
[Si WordPress absent]    ⚠️  WordPress non connecté → blog WordPress indisponible
[Si Ghost absent]        ⚠️  Ghost non connecté → blog Ghost indisponible

[Si au moins un manquant :]
💡 Pour connecter : Cowork > Personnaliser > Connecteurs.
   Typefully couvre X, LinkedIn et Instagram en une seule connexion.
   WordPress MCP est officiel et stable.
   Ghost est un MCP communautaire open source — à activer consciemment.

   Sans connexion, je prépare le contenu formaté pour que tu le colles toi-même.
```

---

## Étape 2 — Sélection des destinations

AskUserQuestion multiSelect — affiche uniquement les plateformes disponibles + fallbacks manuels :
- WordPress (draft)
- WordPress (publication planifiée)
- X — tweet ou thread
- LinkedIn
- Instagram
- Ghost
- Prépare le contenu formaté pour copier-coller manuel

---

## Étape 3 — Vérification de compatibilité

Vérifie la compatibilité format/plateforme. Si incompatibilité, propose les adaptations et soumet à validation avant d'envoyer.

Exemples de messages :
```
"Ce contenu est un article de [N] mots. Il n'est pas publiable directement sur X ou LinkedIn.
Je peux : créer un thread X / créer un post LinkedIn résumé / publier l'article sur WordPress."

"Ce contenu est un tweet. Trop court pour WordPress — je peux l'envoyer tel quel ou l'enrichir."
```

Consulte `references/platforms.md` pour les règles de compatibilité complètes.

---

## Étape 4 — Envoi et scheduling

### Via Typefully (X, LinkedIn, Instagram)
1. Demande la date et l'heure (ou "dès que possible dans la queue")
2. Envoie via MCP Typefully en mode draft
3. Fournis le lien vers le draft

### Via WordPress MCP
1. Draft ou publication planifiée ?
2. Si planifiée : date et heure ?
3. Envoie via MCP, fournis le lien vers le draft

### Via Ghost MCP
Même logique que WordPress. Rappelle le caractère communautaire du MCP. En cas d'erreur, bascule sur le fallback sans bloquer.

### Fallback manuel
Formate le contenu selon la plateforme cible (voir `references/platforms.md`), affiche prêt à copier-coller.

---

## Étape 5 — Confirmation et MEMORY.md

Résume : drafts créés, liens, dates prévues.

Met à jour MEMORY.md :
```
[Titre] | [Format] | [Date] | Draft créé — [Plateforme] — Publication prévue [date]
```
