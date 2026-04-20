---
name: ghost-seo
description: Générer toutes les métadonnées SEO pour publier un article sur Ghost CMS. Produit slug, title, excerpt, meta title, meta description, Schema Markup JSON-LD, og:title, og:description, liens internes suggérés et alt textes images. Se déclenche sur "/ghost-seo", "génère les métadonnées Ghost", "crée le fichier SEO", "prépare les métas pour Ghost".
---

# Skill — Ghost SEO

Génère un fichier markdown complet avec toutes les métadonnées SEO pour Ghost CMS.

---

## Ce que produit ce skill

Un fichier `[slug]-ghost-seo.md` dans le dossier de l'espace actif contenant :

1. **Slug** — URL optimisée, sans accents ni caractères spéciaux
2. **Title** — Le H1 de l'article
3. **Excerpt** — Résumé court pour les listings Ghost (150-200 caractères)
4. **Meta Title** — Balise title SEO (50-60 caractères)
5. **Meta Description** — Description SERP (140-155 caractères)
6. **Schema Markup JSON-LD** — Structuré en `BlogPosting`, avec balises `<script>`
7. **og:title** — Titre pour les partages sociaux (60-90 caractères)
8. **og:description** — Description pour les partages sociaux (120-150 caractères)
9. **Liens internes suggérés** — 3 à 5 suggestions avec contexte
10. **Alt textes des images** — Image principale + 2 images secondaires

Chaque élément dans un bloc de code pour copier-coller direct dans Ghost.

---

## Règles

- Compter précisément les caractères pour chaque champ limité
- Schema Markup : JSON valide avec balises `<script>` incluses
- Utiliser `[À COMPLÉTER]` pour les informations manquantes (URL finale, date de publication)
- Nom du fichier : `[slug]-ghost-seo.md`
