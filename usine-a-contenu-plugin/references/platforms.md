# Plateformes — Compatibilités et règles de publication

Référence lue par `publisher` et `publish.md`.

---

## Tableau de compatibilité

| Format produit | WordPress | Ghost | LinkedIn | X (tweet) | X (thread) | Instagram |
|----------------|-----------|-------|----------|-----------|------------|-----------|
| Article de blog | ✅ | ✅ | ⚠️ résumé | ❌ | ⚠️ extrait | ❌ |
| Newsletter | ✅ page | ⚠️ | ⚠️ résumé | ❌ | ⚠️ extrait | ❌ |
| Post LinkedIn | ❌ | ❌ | ✅ | ❌ | ❌ | ⚠️ adapté |
| Tweet | ❌ | ❌ | ❌ | ✅ | ✅ | ❌ |
| Thread X | ❌ | ❌ | ⚠️ résumé | ⚠️ 1er tweet | ✅ | ❌ |
| Post Instagram | ❌ | ❌ | ⚠️ adapté | ❌ | ❌ | ✅ |
| Script YouTube | ❌ | ❌ | ⚠️ résumé | ❌ | ❌ | ❌ |

**Légende :** ✅ natif | ⚠️ adaptation nécessaire | ❌ incompatible

---

## Règles par plateforme

### WordPress
- Format : HTML ou Markdown (selon config)
- Longueur : pas de limite pratique
- Images : uploadées séparément
- MCP : officiel, stable

### Ghost
- Format : Markdown ou HTML
- MCP : communautaire open source — tester en staging avant production
- Fallback recommandé : API Ghost Admin (documentation officielle)

### LinkedIn (via Typefully)
- Longueur max visible : ~220 caractères avant "voir plus" (première ligne décisive)
- Longueur totale recommandée : 150-300 mots
- Pas de liens dans le corps (pénalise la portée) — mettre en commentaire
- Hashtags : 3-5 maximum, en fin de post
- MCP : Typefully (Social Set ID à configurer dans l'espace)

### X — Tweet (via Typefully)
- Longueur : 280 caractères max
- Lien compte dans les caractères
- Images : jusqu'à 4

### X — Thread (via Typefully)
- Chaque tweet : 280 caractères max
- Numéroter (1/, 2/, etc.) ou laisser la numérotation automatique Typefully
- Dernier tweet : synthèse ou CTA + potentiel lien

### Instagram (via Typefully)
- Légende : 2200 caractères max, 150 recommandés pour la partie visible
- Hashtags : 5-15 en fin de légende ou premier commentaire
- L'image est obligatoire — signaler si absente
- Liens non cliquables dans la légende

---

## Notes de configuration

### Typefully
- Connexion MCP dans Cowork > Personnaliser > Connecteurs
- Social Set ID : à récupérer dans les paramètres Typefully de l'espace
- Couvre X, LinkedIn et Instagram avec une seule connexion

### WordPress MCP
- Nécessite l'URL du site, login et mot de passe applicatif
- MCP officiel — stable en production

### Ghost MCP
- MCP communautaire open source, non officiel
- Vérifier la compatibilité avec la version Ghost avant activation
- En cas d'erreur : utiliser l'API Ghost Admin directement
