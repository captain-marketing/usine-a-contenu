---
name: strategy
description: Lancer le module Stratégie. Propose un audit de contenus existants, une analyse concurrentielle, la création de personas et un plan éditorial 3-12 mois. Chaque étape est optionnelle. Se déclenche sur "strategy", "module stratégie", "fais un audit", "analyse mes concurrents", "crée des personas", "fais un plan éditorial".
---

# Usine à Contenu — Module Stratégie

Point d'entrée du module stratégie. Guide l'utilisateur à travers l'audit, l'analyse concurrentielle, la création de personas et le plan éditorial. Toutes les étapes sont optionnelles.

---

## Étape 0 — Identifier l'espace actif

Si non précisé, demande lequel utiliser avant de continuer.

---

## Étape 1 — État des connexions MCP

Vérifie quels MCP sont disponibles parmi : google-analytics, google-search-console, google-sheets.
Affiche un message adapté :

```
Le module Stratégie peut utiliser ces outils :

[Si GA4 connecté]      ✅ Google Analytics connecté
[Si GA4 absent]        ⚠️  Google Analytics non connecté
[Si GSC connectée]     ✅ Search Console connectée
[Si GSC absente]       ⚠️  Search Console non connectée
[Si Sheets connecté]   ✅ Google Sheets connecté
[Si Sheets absent]     ⚠️  Google Sheets non connecté

[Si au moins un manquant :]
💡 Pour connecter : Cowork > Personnaliser > Connecteurs.
   Les MCP officiels Google sont disponibles directement dans la liste.
   Sans connexion, tu pourras coller tes exports CSV manuellement.

Tu veux connecter des outils maintenant, ou on continue ?
```

AskUserQuestion :
- ✅ On continue avec ce qu'on a
- 🔌 Je veux d'abord connecter (explique-moi comment)

---

## Étape 2 — Choix des étapes

```
Le module Stratégie comporte 4 étapes. Fais celles dont tu as besoin.

1. Audit de l'existant
2. Analyse concurrentielle
3. Création de personas
4. Plan éditorial 3-12 mois
```

AskUserQuestion multiSelect :
- 📊 Audit de l'existant
- 🔍 Analyse concurrentielle
- 👤 Création de personas
- 📅 Plan éditorial
- ✅ Toutes dans l'ordre
- ↩️ Aucune — retour à la production

Lance les skills sélectionnés dans l'ordre : `audit` → `competitive` → `persona-builder` → plan éditorial.

---

## Étape finale — Plan éditorial

Disponible si au moins une étape précédente a été réalisée.

S'appuie sur ce qui est disponible dans MEMORY.md : résultats d'audit, fiches personas, analyse concurrentielle.

### Export du plan

```
[Si Sheets connecté]
📊 Google Sheets — tableau interactif, modifiable et partageable
📁 Fichier CSV
📝 Markdown dans Cowork

[Si Sheets absent]
📊 Google Sheets — non disponible
   (Connecte le MCP Google Sheets dans Personnaliser > Connecteurs)
📁 Fichier CSV
📝 Markdown
```

Enregistre toujours le plan dans MEMORY.md de l'espace, quel que soit le format choisi.

### Format du plan éditorial

```markdown
## Plan éditorial — [espace]
Période : [date] → [date + 12 mois]
Basé sur : [sources utilisées]

### Mois 1-3 — Quick wins et contenus piliers
| Sujet | Format | Angle | Mot-clé cible | Mois | Priorité | Persona cible |

### Mois 4-6 — Développement thématique
[même tableau]

### Mois 7-9 — Approfondissement et conversion
[même tableau]

### Mois 10-12 — Révision et nouveaux angles
[même tableau]

### Logique du plan
[3-4 phrases expliquant les priorités et l'influence des personas]
```
