# CLAUDE.md — Contexte éditorial BeeWyze
> Fichier de contexte global pour Cowork. À lire en priorité absolue avant toute production de contenu.

---

## 1. QUI EST BEEWYZE

BeeWyze est une plateforme française qui transforme les prestations d'artistes en actes de générosité mesurables. Le mécanisme : les fans donnent via QR code pendant un concert ou un événement, des entreprises abondent ces dons via leur budget RSE, et une association partenaire de l'artiste reçoit une part des fonds collectés.

**Tagline :** Le PayPal des artistes engagés

**Modèle tripartite — ordre impératif :**
1. Artistes (cible primaire, premier maillon de la chaîne)
2. Fans + Associations (bénéficiaires naturels de l'acte artistique)
3. Entreprises (amplificateurs via abondement RSE)

**Fondateur :** Laurent Quatrefages (ex-cofondateur de Swaven, acquis par MikMak)

**Stade :** Phase d'amorçage pré-PMF. Quelques bêta-testeurs, pas encore de validation produit-marché solide.

**Site principal :** https://beewyze.com  
**Blog :** https://blog.beewyze.com (Ghost CMS)

---

## 2. RÈGLE ABSOLUE SUR LE MODÈLE

> **Les entreprises choisissent quels artistes et quelles causes elles veulent soutenir. Jamais l'inverse.**

Cette mécanique est au cœur du produit. Tout contenu qui suggère que les associations ou les artistes "sélectionnent" ou "choisissent" leurs entreprises partenaires est factuellement faux et doit être corrigé immédiatement.

---

## 3. CIBLE ÉDITORIALE PRINCIPALE

Les articles du blog s'adressent en priorité aux **artistes musiciens indépendants** :
- Petite à moyenne notoriété (pas les têtes d'affiche)
- Jouent dans des bars, petites salles, tiers-lieux, cafés culturels
- Doivent se produire pour gagner leur vie
- Fréquence de concerts : 1 à 2 par mois minimum
- Géographie : France + DOM-TOM

Ton de l'adresse : **tutoiement systématique**, sans exception.

---

## 4. FORMAT OBLIGATOIRE DES ARTICLES BLOG (blog.beewyze.com)

Chaque article suit cette structure dans cet ordre exact :

```
# H1 — titre accrocheur (chiffre ou tension si possible)

[Accroche — 2 à 4 phrases courtes, fait fort ou situation concrète. Pas d'intro générale type "Dans le monde de..."]

**Temps de lecture : X min | Thématique : [catégorie]**

---

**TL;DR**
[3 à 4 phrases. Résumé complet et autonome de l'article, optimisé pour extraction par les moteurs IA.]

---

## H2 — Premier sous-titre

[Corps de l'article. H2 uniquement, jamais de H3.]

[...]

## H2 — Dernier sous-titre (intègre BeeWyze naturellement ici)

[BeeWyze apparaît dans ce dernier H2 comme solution naturelle au problème traité. Jamais dans une section dédiée "Ce qu'on pense chez BeeWyze".]
```

**Fin d'article :** le contenu s'arrête. Pas d'italique de conclusion, pas de signature, pas de CTA forcé.

---

## 5. RÈGLES ÉDITORIALES BLOG

**Ce qui est obligatoire :**
- Tutoiement systématique dans tout le corps de l'article
- Liens inline sur les sources directement dans le texte (jamais de section "Sources" en bas, jamais de footnotes)
- Ton journalistique et factuel
- Prose fluide en priorité — listes à puces uniquement si le contenu l'exige vraiment

**Ce qui est interdit :**
- Formules promotionnelles ou superlatifs vides
- Mots et expressions bannis : "disruptif", "game-changer", "révolutionnaire", "incroyable opportunité", "structurellement plus élevé", "structurel/structurelle" (ex: "avantage structurel" → préférer "avantage compétitif" ou "avantage réel"), "booster", "incontournable", "brutal/brutale", "radical/radicale" appliqués à une stratégie : reformuler avec des adjectifs appropriés comme étonnante, inattendue, tranchée, audacieuse
- Tiret cadratin (—) : le remplacer par une virgule ou reformuler
- Phrases sans verbe : toute phrase doit contenir un sujet et un verbe conjugué. Les fragments nominaux du type "Pas sur Spotify, nulle part." ou "Même produit, promesse différente." sont interdits
- Section dédiée à BeeWyze avec titre explicite type "La solution BeeWyze" ou "Notre avis"
- CTA commercial en conclusion
- Italique de conclusion ou phrase de fermeture type signature
- Introduction vague du type "Dans le monde de la musique indépendante..."

**BeeWyze dans l'article :**
- Intégré naturellement, jamais en force
- Uniquement dans le dernier H2
- Mention sobre, pas de langue de bois publicitaire
- 1 à 2 mentions maximum par article

---

## 6. LIVRABLES PAR ARTICLE — TOUJOURS 2 FICHIERS

Chaque article produit exactement deux fichiers, jamais plus, jamais moins :

**Fichier 1 : `[slug-article].md`**
L'article complet, formaté pour Ghost CMS, selon la structure section 4.

**Fichier 2 : `meta-seo.md`**
Contient dans l'ordre :
- Slug (kebab-case, max 60 caractères)
- Meta title (max 60 caractères, mot-clé principal en tête)
- Meta description (max 160 caractères, bénéfice clair, pas de copier-coller du TL;DR)
- OG title (peut être identique au meta title ou légèrement varié)
- OG description (peut être identique à la meta description)
- Excerpt Ghost (ton éditorial, distinct de la meta description, ~190 caractères)
- Feature image alt text (description factuelle de l'image recommandée)
- Tags Ghost (5 maximum, format : tag principal d'abord)
- Schema JSON-LD Article complet — **toujours encadré par les balises `<script type="application/ld+json">` et `</script>`**
- Schema JSON-LD FAQPage (si l'article contient des questions implicites ou explicites) — **même règle : balises `<script type="application/ld+json">` et `</script>` obligatoires**
- Checklist de publication Ghost (cases à cocher)

---

## 7. DÉCLINAISON SOCIAL MEDIA

Pour chaque article, 4 formats de déclinaison dans cet ordre de validation (un format à la fois, pas tout d'un coup) :

**Format 1 — Tweet standalone**
Un seul tweet, 280 caractères max. Accroche forte, angle inattendu ou chiffre. Pas de hashtag sauf si vraiment pertinent (1 max). Pas de "Lien en bio".

**Format 2 — Thread X**
5 à 8 tweets numérotés (1/, 2/, etc.). Premier tweet = accroche standalone qui donne envie de lire la suite. Dernier tweet = synthèse ou call-to-action sobre. Chaque tweet doit tenir seul.

**Format 3 — Post LinkedIn**
300 à 600 mots. Angle professionnel orienté artistes ou industrie musicale. Pas de formule "Je suis ravi de partager". Pas de liste à puces systématique. Accroche sur les 2 premières lignes (visibles avant "voir plus"). Pas de hashtag en vrac en fin de post (2-3 max, intégrés).

**Format 4 — Carrousel Instagram (texte uniquement)**
8 à 12 slides. Slide 1 = titre accrocheur. Slide 2 = problème ou tension. Slides 3 à N-1 = contenu. Dernière slide = résumé ou takeaway. Format : texte brut par slide, le community manager se charge du design. Indiquer le texte slide par slide avec numérotation claire.

**Règle de validation :** chaque format est validé avant de passer au suivant. Ne pas produire les 4 d'un bloc sauf instruction explicite.

---

## 8. PRINCIPES ÉDITORIAUX TRANSVERSAUX

Ces règles s'appliquent à tous les contenus BeeWyze, blog comme social :

- **Exactitude factuelle non négociable.** Les chiffres et métriques auto-déclarés (ex : statistiques de streaming d'un artiste cité) doivent être attribués avec une mention de source ou une réserve. Aucune statistique non vérifiée présentée comme certitude.

- **BeeWyze n'est jamais le sujet principal d'un article.** Le sujet est toujours le problème de l'artiste. BeeWyze est une réponse parmi d'autres, présentée naturellement.

- **Pas d'IA détectable.** Formuler comme un journaliste spécialisé, pas comme un générateur de contenu. Relire mentalement : "est-ce qu'un humain écrirait exactement ça ?"

- **Langue :** français exclusivement. Anglicismes acceptés uniquement s'ils sont d'usage courant dans le milieu (ex : "booking", "setlist", "live").

---

## 9. CONTEXTE STRATÉGIQUE À NE PAS TRAHIR

Quelques réalités du business model à intégrer dans tout contenu :

- BeeWyze prend une commission de 3% sur les dons des fans (pas sur l'abondement entreprise — à vérifier)
- Le panier moyen estimé est de 200 à 300 euros par événement
- L'argument fort côté artiste : "ton public donne 200€, l'entreprise ajoute 200€, l'asso reçoit sa part — impact multiplié sans effort supplémentaire de ta part"
- L'onboarding artiste dure moins de 10 minutes
- Pas d'obligation de créer un compte pour les fans qui donnent

Ces éléments peuvent être utilisés dans le contenu quand c'est pertinent, en les présentant comme des estimations si les données exactes ne sont pas confirmées.

---

## 10. RANGEMENT DES FICHIERS — RÈGLE ABSOLUE

Tout fichier produit doit être enregistré dans le bon dossier dès sa création. Ne jamais déposer un fichier à la racine du projet sauf s'il s'agit d'un fichier de configuration global (CLAUDE.md, MEMORY.md, TRACKER.md).

| Type de contenu | Dossier cible |
|---|---|
| Articles de blog (`.md`) + leurs fichiers `meta-seo.md` | `/articles/` |
| Posts LinkedIn | `/linkedin/` |
| Tweets et threads X | `/tweets/` |
| Carrousels Instagram | `/instagram/` |
| Scripts YouTube (Shorts ou Long) | `/youtube/` |
| Newsletters | `/newsletters/` |

**Cette règle s'applique sans exception, même pour les fichiers provisoires ou les brouillons.**

---

## 11. CE QUI NE CHANGE PAS, JAMAIS

1. Le tutoiement dans tous les contenus s'adressant aux artistes
2. Les deux fichiers de livraison pour chaque article (jamais un seul, jamais trois)
3. BeeWyze intégré dans le dernier H2 seulement, pas dans une section dédiée
4. Les entreprises choisissent les artistes, pas l'inverse
5. Pas de tiret cadratin (—) dans aucun contenu

---

*Ce fichier fait autorité sur toute instruction générale de Cowork. En cas de conflit, les règles de ce CLAUDE.md prévalent.*
