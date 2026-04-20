![Usine à Contenu — Plugin Cowork V5](assets/cover.png)

# Usine à Contenu

Plugin Claude Cowork pour produire du contenu multi-format avec modules stratégie et publication intégrés.

---

## Les 3 modules

### ⚙️ MODULE PRODUCTION — toujours actif
`research` → `watch` → `ideation` → `produce` → `optimize` → `ghost-seo`

### 📋 MODULE STRATÉGIE — optionnel
Commande : `/usine-a-contenu:strategy`
Skills : `audit` · `competitive` · `persona-builder`
MCP utiles : Google Analytics 4, Google Search Console, Google Sheets

### 📤 MODULE PUBLICATION — optionnel
Commande : `/usine-a-contenu:publish`
Skill : `publisher`
MCP utiles : Typefully (X, LinkedIn, Instagram), WordPress, Ghost (communautaire)

---

## Démarrage

1. Installer dans Cowork > Personnaliser > Plugins
2. `/usine-a-contenu:begin` — initialise et crée le premier espace
3. `/usine-a-contenu:new-space` — crée de nouveaux espaces à tout moment
4. Les skills de production se déclenchent automatiquement selon le contexte

---

## Connecteurs MCP recommandés

Tous optionnels. Le plugin fonctionne sans, avec fallbacks manuels.

| Connecteur | Module | Usage |
|------------|--------|-------|
| Google Analytics 4 | Stratégie | Audit de performance |
| Google Search Console | Stratégie | Audit SEO, requêtes |
| Google Sheets | Stratégie | Export plan éditorial |
| Typefully | Publication | X, LinkedIn, Instagram |
| WordPress | Publication | Blog WordPress |
| Ghost | Publication | Blog Ghost (communautaire) |

---

## Structure

```
usine-a-contenu/
├── .claude-plugin/plugin.json   (v3.0.0)
├── .mcp.json                     (config connecteurs)
├── commands/
│   ├── begin.md
│   ├── new-space.md
│   ├── strategy.md
│   └── publish.md
├── skills/
│   ├── research/      → veille YouTube + Google
│   ├── watch/         → surveillance de sources
│   ├── ideation/      → batch d'idées à valider
│   ├── produce/       → production tous formats
│   ├── optimize/      → SEO + GEO
│   ├── ghost-seo/     → métadonnées Ghost CMS
│   ├── audit/         → audit de contenus existants
│   ├── competitive/   → analyse concurrentielle
│   ├── persona-builder/ → création de personas
│   └── publisher/     → publication multi-plateformes
├── references/
│   ├── formats.md
│   ├── seo-geo.md
│   ├── persona-template.md
│   ├── persona-methods.md
│   └── platforms.md
└── spaces/            (créés automatiquement)
    └── [nom-espace]/
        ├── CLAUDE.md
        ├── MEMORY.md
        ├── sources.md
        └── personas/
```
