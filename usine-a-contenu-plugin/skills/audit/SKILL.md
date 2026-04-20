---
name: audit
description: Analyser les contenus existants d'un site et leur performance pour identifier les quick wins SEO, les contenus à optimiser, à dépublier et les opportunités manquées. Se déclenche sur "audite mon site", "analyse mes contenus", "quels contenus performent", "qu'est-ce que je dois optimiser", ou depuis /usine-a-contenu:strategy.
---

# Skill — Audit

---

## Étape 1 — Expliquer les sources

```
Pour l'audit, voici ce que chaque source m'apporte :

📊 Google Analytics + Search Console (MCP ou CSV)
   → trafic, taux de rebond, requêtes, positions
   → Résultat : audit complet avec priorités basées sur des données réelles

🗺️  Sitemap XML (URL ou fichier uploadé)
   → structure du site, toutes les URLs indexées
   → Résultat : carte des contenus sans données de performance

📋 Arborescence manuelle (JSON, Sheet, liste)
   → structure partielle
   → Résultat : audit de structure uniquement

La combinaison GA4/GSC + sitemap donne l'audit le plus complet.
Tu as quoi sous la main ?
```

AskUserQuestion multiSelect :
- 📊 MCP GA4 + Search Console connectés
- 📁 Je colle mes exports CSV
- 🗺️ Je fournis l'URL de mon sitemap XML
- 📋 Je fournis mon arborescence
- 🔀 Combinaison de plusieurs sources

---

## Étape 2 — Collecte

**MCP connecté :** récupère automatiquement. Période par défaut : 90 derniers jours.
**CSV :** demande de coller le contenu.
**Sitemap :** charge depuis l'URL ou analyse le fichier uploadé.

---

## Étape 3 — Analyse

Identifie :
1. Contenus performants (trafic élevé, bonne position, bon CTR)
2. Quick wins (impressions élevées + CTR faible, positions 5-15, rebond anormal)
3. Contenus à rénover (trafic en déclin, contenu ancien sur sujet evergreen)
4. Contenus à dépublier ou fusionner (trafic quasi nul, duplication)
5. Opportunités manquées (requêtes avec impressions sans contenu dédié)
6. Maillage interne lacunaire

---

## Étape 4 — Livrable

```markdown
## Audit — [espace]
Date : [date] | Sources : [liste] | Période : [période]

### Synthèse
[3-4 phrases : état général, principaux constats]

### Contenus performants — à consolider
| Page | Trafic/mois | Position moy. | Action |

### Quick wins — impact rapide
| Page | Problème | Action | Effort |

### Contenus à rénover
| Page | Problème | Action |

### Contenus à dépublier ou fusionner
| Page | Raison | Action |

### Opportunités — sujets non couverts
| Requête / Sujet | Volume est. | Priorité |

### Maillage interne — lacunes
[Description]

### Priorités recommandées
1. [Action n°1]
2. [Action n°2]
3. [Action n°3]
```

---

## Étape 5 — Enregistrement

Sauvegarde dans MEMORY.md sous "## Audit — [date]".

> "Tu veux continuer avec l'analyse concurrentielle, créer des personas, ou passer au plan éditorial ?"
