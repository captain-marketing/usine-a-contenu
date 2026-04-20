# Comment écrire avec l'IA sans que ça ressemble à de l'IA

**TL;DR :** L'IA écrit comme tout le monde parce qu'elle est entraînée pour être cohérente, pas distinctive. Un guide de style lui donne une cible précise : ta voix, ta structure, tes tournures. Sans ça, tu passes ton temps à corriger les mêmes défauts en boucle. Avec un guide de style, tu réduis le bruit et tu gardes le contrôle éditorial. Le template complet et le prompt d'entretien pour créer ton guide sont en fin d'article.

---

Tu demandes à l'IA de rédiger un article. Elle te rend quelque chose en moins d'une minute. C'est bien structuré, les phrases s'enchaînent proprement, le plan tient la route.

Et pourtant tu le relis, et tu sais immédiatement que tu ne peux pas publier ça.

Le ton est lisse. Les transitions sont scolaires. Il y a des "c'est ça.. mais pas ça" partout. Chaque paragraphe se termine sur une fausse profondeur philosophique qui ne mène nulle part. Et une intro qui contextualise pendant trois paragraphes avant d'arriver au sujet.

Tu passes alors vingt minutes à tout réécrire. Ce qui devait te faire gagner du temps t'en a en fait coûté. Et rebelote au prochain article.

Beaucoup de gens s'arrêtent là. Ils concluent que l'IA ne sait pas écrire, ou qu'ils sont mauvais en prompting. Mais le vrai problème est ailleurs : le modèle fait exactement ce pour quoi il a été entraîné. Il produit l'approximation la plus sûre, la plus moyenne, la probabilité d'une "bonne écriture". Sans indication précise, il converge vers quelque chose de très consensuel.

La solution n'est pas un meilleur prompt à chaque fois. C'est un guide de style : un système de référence réutilisable qui dit au modèle comment tu écris, toi, une bonne fois pour toutes.

---

## Ce qu'est vraiment un guide de style pour l'IA

Un guide de style traditionnel sert à harmoniser l'écriture d'une équipe. Quand dix personnes écrivent sur le même blog, tu as besoin de règles communes pour éviter les incohérences.

Un guide de style pour l'IA résout le problème inverse : le modèle est parfaitement cohérent dès le départ, et c'est précisément pour ça qu'il ne ressemble à personne. L'enjeu n'est pas de le rendre plus régulier, c'est de le pousser vers les idiosyncrasies qui font que ton écriture t'appartient.

La distinction essentielle à garder en tête : une instruction ponctuelle dit à l'IA *quoi faire* (rédige cet article, améliore cette intro, resserre ce paragraphe). Un guide de style est le système en dessous, qui dit à l'IA *comment sonner comme toi* pendant qu'elle le fait. C'est la différence entre donner une commande et donner un "état d'esprit".

La plupart des gens s'arrêtent aux adjectifs flatteurs : "mon style est clair, conversationnel, expert". C'est vrai, mais ça n'est pas suffisant pour changer le comportement du modèle. Il faut aller plus loin : comment tes articles ouvrent-ils ? À quelle vitesse tu arrives au point principal ? Quels types de phrases tu n'écrirais jamais ? Qu'est-ce qui te fait lever les yeux au ciel dans un texte généré par IA ?

---

## La structure : l'élément que l'IA rate le plus souvent

Si tu ne mets qu'une chose dans ton guide de style, mets la structure.

C'est là où l'IA décroche le plus facilement. Elle peut trouver un ton acceptable, elle peut éviter les tournures trop pompeuses si tu le lui demandes. Mais la façon dont les idées s'organisent, le mouvement d'un article, la vitesse à laquelle tu arrives au cœur du sujet, tout ça, elle l'infère très mal.

Un exemple concret. Pour une newsletter B2B sur le marketing, le schéma typique pourrait être :

1. Ouvrir sur un constat qui fait tilt : un chiffre, une situation reconnaissable, une friction réelle
2. Identifier pourquoi la solution évidente ne fonctionne pas
3. Présenter l'approche alternative avec un exemple vécu
4. Donner un framework ou une méthode directement utilisable
5. Terminer par une extension de l'idée, pas un résumé

Ce schéma n'est pas le seul possible, mais il correspond à une newsletter spécifique, avec ses lecteurs spécifiques. L'IA ne peut pas le deviner. Tu dois le lui écrire.

La plupart des guides de style pour IA que j'ai vus commencent par la voix. C'est compréhensible, mais c'est souvent moins utile qu'une description structurelle précise. La voix, tu peux l'affiner en relecture. Une structure mal posée, ça demande de tout reprendre.

**Ce que tu peux mettre dans cette section :**

- Comment tes textes ouvrent-ils habituellement ? (friction, anecdote, chiffre, question directe ?)
- À quelle vitesse arrives-tu au point central ? (dès le premier paragraphe, après une mise en contexte courte ?)
- Quel mouvement suit l'argument ? (du concret vers l'abstrait ? de l'exemple vers la règle ?)
- Comment tes textes se terminent-ils ? (élan vers la prochaine idée, appel à l'action, question ouverte ?)

---

## Voix, ton et phrases : ce que l'IA ne devine pas

### La voix : aller au-delà des adjectifs

Une fois la structure posée, la voix. Ici, le piège est d'écrire des choses vraies mais inutiles.

"*Mon ton est conversationnel mais professionnel.*" Soit. Mais le modèle ne sait pas ce que ça veut dire pour toi. Il a des milliers d'exemples de "conversationnel mais professionnel" dans ses données d'entraînement.

Ce qui fonctionne, c'est de définir la voix avec des tensions et des limites : ce qu'elle est, ce qu'elle n'est pas.

Quelques exemples de formulations utiles :

- Direct, sans être abrasif
- Expert sans jamais être condescendant
- Humoristique par touches sèches, pas par blagues développées
- Vulnérabilité analytique : les doutes personnels servent à poser les enjeux, pas à se plaindre
- Critique des pratiques sans être moralisateur

La formulation "vulnérabilité analytique" vient d'un guide de style développé par l'équipe éditoriale d'Every.to, un média américain qui a intégré l'IA dans toute sa production éditoriale. Leur approche : ne pas se contenter d'adjectifs, mais nommer les tensions. C'est un réflexe à adopter.

**Ce que tu peux mettre dans cette section :**

- Cinq formulations qui décrivent la voix avec ses tensions (ce qu'elle est et ce qu'elle n'est pas)
- Le niveau de formalité (tutoiement ? vouvoiement ? selon le contexte ?)
- La place de l'humour (présent, rare, quel type ?)
- La température émotionnelle (froide et analytique, ou avec des enjeux personnels visibles ?)

### Les préférences au niveau des phrases

C'est la section la plus technique, et souvent celle qui améliore le plus vite la qualité des brouillons quand on écrit avec l'IA.

L'idée : décrire tes habitudes ligne par ligne. Longueur des phrases, ponctuation, niveau d'abstraction, mots que tu utilises systématiquement ou que tu évites.

Quelques exemples concrets tirés de guides qui fonctionnent :

**Préférer le concret à l'abstrait :**
- "Claude a ouvert cinq PRs (Pull Request) pendant que je buvais mon café" plutôt que "les workflows ont été optimisés"
- "400 € par mois remplaçant 4 000 € de prestataire" plutôt que "une solution rentable"
- "Gmail a bloqué 2 000 opérations email" plutôt que "on a rencontré des problèmes de scalabilité"

**Localiser les émotions dans le concret :**
Plutôt que "j'étais soulagé", dire "le soulagement se sentait physiquement, comme si la pression dans ma poitrine était descendue d'un cran". Ça s'applique moins à un blog B2B qu'à un essai personnel, mais le principe tient : les descriptions émotionnelles abstraites ne parlent à personne.

**Ce que tu peux mettre dans cette section :**

- Longueur de phrases que tu préfères (courtes et percutantes ? longues et sinueuses ?)
- Niveau d'abstraction toléré (exemples concrets systématiques, ou conceptualisation acceptée ?)
- Mots que tu utilises souvent (à donner au modèle comme vocabulaire préféré)
- Mots à éviter (le modèle a besoin de ta liste noire personnelle)

---

## Tournures signature et liste noire : le cœur du guide

### Les tournures signature

Chaque bonne écriture a des mouvements récurrents. Des façons de passer d'une idée à l'autre, des structures narratives qui reviennent, des pivots qui te ressemblent.

Nommer ces tournures est utile pour deux raisons. D'abord, ça donne au modèle une cible mécanique à reproduire. Ensuite, ça t'oblige à les identifier toi-même, et c'est souvent une surprise.

Trois exemples de tournures nommées pour un blog marketing :

**La Friction, le zoom arrière, le framework :** Commencer par un problème concret rencontré en pratique, prendre du recul pour le connecter à une logique plus large, puis atterrir sur une méthode utilisable. C'est le schéma classique du bon article de blog pratique.

**L'Écart de croyance :** Ouvrir sur ce que la plupart des gens croient, montrer pourquoi c'est faux ou incomplet, puis donner la vision corrigée. Fonctionne bien pour les sujets où il y a beaucoup de bruit et de mauvais conseils.

**L'analogie empruntée :** Importer un concept d'un autre domaine (psychologie, architecture, sport) pour éclairer une problématique marketing. Quand ça marche, c'est mémorable. Quand ça ne marche pas, ça sonne forcé, donc à utiliser avec discernement.

Tu n'as pas besoin d'en lister dix. Trois ou quatre tournures bien décrites valent mieux qu'une longue liste floue.

### La liste noire : souvent la section la plus utile du guide de style

Ne dis pas seulement au modèle ce que tu aimes. Dis-lui ce que tu détestes.

C'est contre-intuitif, mais la liste noire est souvent la section qui améliore le plus les brouillons. Les défauts de l'IA sont prévisibles : les mêmes constructions reviennent sur presque tous les modèles, quel que soit le sujet.

Voilà une liste de départ à personnaliser :

| Schéma | Solution |
|--------|----------|
| "Non seulement... mais aussi" | Formuler directement la deuxième idée |
| "Il est important de noter que" | Supprimer, aller au fait |
| Atténuateurs : "en fait", "peut-être", "juste" | Supprimer sauf utilité réelle |
| Intro qui pose le contexte sur trois paragraphes | Commencer par la friction ou l'enjeu |
| Conclusion qui résume ce qui précède | Terminer en prolongeant ou en ouvrant |
| Fausse profondeur finale ("Au bout du compte, c'est une question de...") | Couper |
| Questions rhétoriques servant de remplissage | Couper ou convertir en affirmation |
| "Dans le monde actuel du marketing digital" | Reformuler avec un fait concret |

Ta liste noire évoluera avec le temps. Commence avec cinq ou six éléments, et ajoute un nouveau chaque fois que tu fais la même correction deux fois de suite sur un brouillon IA.

---

## Comment construire ton guide de style IA (sans partir d'une page blanche)

Ne te prends pas la tête pour écrire ton guide de zéro. Laisse l'IA te faire passer l'entretien.

Beaucoup de gens sont meilleurs pour réagir que pour se décrire. C'est difficile d'expliquer sa voix à partir d'une page blanche. Il est plus facile de répondre à : "Laquelle de ces deux ouvertures te ressemble le plus ?" ou "Qu'est-ce qui te gêne dans ce paragraphe ?"

Le process en cinq étapes :

**1. Donne au modèle des exemples de ton écriture.** Trois à cinq textes que tu aimes vraiment : des articles ou posts qui capturent parfaitement ta voix. Si tu n'en as pas encore assez, donne-lui des textes d'auteurs que tu apprécies.

**2. Demande-lui de t'interviewer.** Demande-lui de te poser des questions une par une sur ton ton, ta structure, tes habitudes de phrases, tes anti-patterns. L'interview fait remonter des préférences que tu n'aurais pas formulées spontanément.

**3. Réagis à des exemples et non pas à des généralités.** Demande-lui de te proposer des variantes de phrases, des reformulations, des ouvertures alternatives. Et réagis : "celle-là est trop symétrique", "celle-là sonne trop corporate", "celle-là, c'est exactement ça". Les réactions concrètes valent plus que les descriptions abstraites.

**4. Demande-lui de synthétiser l'entretien en guide.** Une fois qu'il a assez de matière, il peut produire un premier jet couvrant les sections vues plus haut.

**5. Teste pendant une semaine, puis révise.** Utilise le guide sur de vrais brouillons. Note les corrections que tu fais encore. Affine les instructions qui sont encore trop vagues. Un bon guide de style se construit avec l'usage.

---

## Les trois niveaux d'investissement

Selon où tu en es avec l'IA dans ton workflow d'écriture, l'effort à mettre dans le guide varie.

**Niveau 1 — Guide de démarrage (20 minutes) :** Trois à cinq bullets sur la voix, une description de ta structure préférée, une liste noire de cinq patterns, deux ou trois exemples commentés. C'est suffisant pour commencer à obtenir de bons résultats. À garder dans un document et à coller dans la conversation quand tu en as besoin.

**Niveau 2 — Guide de travail :** Tu rédiges régulièrement avec l'IA et tu as remarqué des erreurs récurrentes. Tu ajoutes des préférences au niveau des phrases avec des exemples positifs et négatifs, des tournures signature nommées, une liste de vérification, des modèles structurels pour les formats que tu utilises le plus. Ce guide vit dans un projet Claude ou une instruction personnalisée du modèle que tu utilises, et il est lu en contexte à chaque conversation.

**Niveau 3 — Système composé :** L'IA est au cœur de ton workflow et tu veux que le système s'améliore à chaque usage. Le guide devient une partie d'une infrastructure plus large : des instructions intégrées dans des skills ou des agents, des vérifications automatisées qui scannent les brouillons avant publication, une boucle de feedback qui enrichit le guide après chaque correction. Tu n'as pas besoin de commencer là, mais c'est vers là qu'il faut progressivement aller.

---

## Ce qui fait la différence quand on écrit avec l'IA au quotidien

Quelques observations après des mois à utiliser ce type de guide dans une production éditoriale régulière.

**La spécificité bat la complétude.** Un guide court et très précis produit de meilleurs résultats qu'un guide exhaustif rempli de généralités. Si tu dois choisir, préfère dix instructions concrètes à trente vagues.

**La liste noire est sous-estimée.** La plupart des gens décrivent longuement ce qu'ils aiment et peu ce qu'ils détestent. Or c'est souvent la liste noire qui améliore le plus vite la qualité des brouillons. Ajoute un élément chaque fois que tu fais la même correction deux fois.

**Les exemples valent plus que les règles.** Un paragraphe qui trouve le bon ton apprend plus au modèle qu'un paragraphe d'explications abstraites. Mets des exemples dans chaque section si tu peux, y compris des contre-exemples commentés.

**Calibre le guide sur ce que tu écris vraiment.** La tentation est de faire un guide assez large pour couvrir tous tes formats. En général, ça l'affaiblit. Un article de blog, une newsletter et un post LinkedIn n'ont pas la même structure, le même rythme ni le même niveau de formalité. Si tu produis plusieurs formats régulièrement, envisage des sections distinctes pour chacun, ou des guides séparés. Un guide ancré dans des tâches réelles produit de meilleurs résultats qu'un guide conçu pour tout couvrir.

**Ne le rigidifie pas trop.** Traite le guide comme un règlement que le modèle doit suivre mécaniquement, et tu aplatis l'écriture d'une façon différente. L'objectif est de préserver ce qui compte, pas de transformer le modèle en machine à reproduire une formule. La règle qui prime sur toutes les autres reste : choisis l'approche qui sert le texte.

**Le guide n'élimine pas le jugement éditorial.** Un bon guide améliore les brouillons et réduit les corrections répétitives, mais il ne remplace pas le goût. Tu gardes le dernier mot, et c'est exactement ce qu'on cherche.

---

## Où stocker ton guide de style une fois créé

Un guide de style qui traîne dans un fichier texte que tu dois retrouver et coller manuellement à chaque conversation, ça finit par ne plus être utilisé. Pour qu'il fonctionne vraiment, il doit être lu automatiquement par le modèle à chaque session.

Dans **Claude**, tu peux le stocker dans un Projet : le guide est chargé en contexte à chaque conversation ouverte dans ce projet, sans aucune manipulation de ta part. C'est le niveau 2 du système décrit plus haut.

Dans **Cowork**, tu peux aller encore plus loin en l'intégrant directement dans un skill dédié à ta production éditoriale. Le guide devient alors une partie de l'infrastructure : il s'applique automatiquement à chaque contenu rédigé, sans que tu aies besoin d'y penser. C'est le niveau 3.

Dans les deux cas, le principe est le même : le guide doit vivre là où tu travailles, pas dans un onglet que tu oublies d'ouvrir.

---

## Le prompt et le template pour créer ton guide de style IA

Si tu veux créer ton guide rapidement, commence par l'instruction d'entretien ci-dessous. Elle demande à l'IA de te poser des questions avant d'écrire quoi que ce soit — c'est beaucoup plus efficace que de remplir un template à froid.

> *"Je veux que tu m'aides à créer un guide de style pour mon écriture.*
>
> *Ton rôle est de m'interviewer et d'extraire les informations dont tu auras besoin pour rédiger un guide de style utile : un document pratique qui aidera une IA à produire de l'écriture qui me ressemble, plutôt qu'un résumé flatteur de ma voix.*
>
> *Voici comment je veux que tu t'y prennes :*
>
> *1. Commence par me demander des exemples de mon écriture, ou des exemples d'une écriture que j'admire si je n'ai pas encore assez de textes à moi.*
> *2. Pose-moi une question à la fois, pas une liste d'un coup.*
> *3. Concentre-toi sur les spécificités : ton, structure, rythme des phrases, stratégies d'ouverture, métaphores, habitudes récurrentes, ce que je déteste dans la prose générée par IA, et les différences entre ce qui me ressemble et ce qui semble générique.*
> *4. Quand c'est utile, propose-moi de courts exemples, des comparaisons ou des reformulations alternatives, et demande-moi d'y réagir.*
> *5. Aide-moi à faire remonter mes préférences positives ET négatives. Je veux identifier ce que j'aime, mais aussi ce que je veux éviter.*
> *6. Après avoir rassemblé suffisamment de matière, synthétise la conversation en guide de style avec les huit sections du template ci-dessous.*
> *7. Garde le guide concret, spécifique et utilisable. Si quelque chose est trop vague pour modifier le comportement d'une IA, rends-le plus précis.*
>
> *Ne commence pas par rédiger le guide. Commence par m'interviewer."*

Une fois l'entretien terminé, demande-lui de produire le guide en suivant ce template :

---

**1. Voix et ton**
Comment cette écriture doit-elle se sentir à son meilleur ?
Rédige trois à cinq points qui décrivent la voix avec ses tensions et ses limites, au-delà des adjectifs flatteurs.
Exemples :
- Direct, sans être abrasif
- Expert sans jamais être condescendant
- Humoristique par touches sèches, pas par blagues développées
- Prêt à être honnête émotionnellement, sans être mélodramatique
- Spécifique et ancré plutôt que vague ou gonflé
À compléter aussi : niveau de formalité, température émotionnelle, place de l'humour, registre (reportorial, essayistique, intime, sceptique...).

**2. Structure**
Comment les textes dans ce style se déplacent-ils habituellement ?
Exemples :
- Ouvrir avec un détail concret, une scène ou un problème reconnaissable
- Arriver à l'argument central assez rapidement
- Aller de l'exemple vers l'idée, pas l'inverse
- Éviter les longues introductions de mise en contexte
- Terminer avec de l'élan plutôt qu'un résumé bien net

**3. Préférences au niveau des phrases**
Qu'est-ce qui fait qu'une phrase sonne juste dans cette voix ?
Exemples :
- Varier la longueur des phrases
- Préférer les phrases épurées et directes aux constructions trop symétriques
- Utiliser l'abstraction avec parcimonie
- Favoriser les noms et verbes concrets plutôt que le langage de cadrage vague
- Éviter de sonner trop poli ou trop satisfait de soi

**4. Tournures signature**
Qu'est-ce que cette voix fait particulièrement bien ?
Exemples :
- Commence par du concret et prend de la hauteur
- Utilise l'humour pour couper à travers l'abstraction
- Pivote de l'anecdote vers l'argument
- Laisse un peu de friction subsister au lieu de tout lisser

**5. Liste noire**
Que doit éviter le modèle ?

| Schéma | Solution |
|--------|----------|
| Constructions "pas X, mais Y" | Formuler Y directement, supprimer l'échafaudage |
| Atténuateurs : "en fait", "peut-être", "juste" | Supprimer sauf si vraiment utile |
| Intro traînante | Commencer avec de la tension ou des enjeux |
| Fin résumée | Terminer en prolongeant ou en recadrant |
| Fausse profondeur | Couper |
| Transitions génériques | Couper ou rendre spécifiques |
| Autorité sans source ("des études montrent") | Nommer l'étude ou supprimer |

**6. Exemples positifs**
Quels sont des exemples de cette voix qui fonctionne bien ?
À inclure : un paragraphe que tu aimes, une intro qui sonne juste, une phrase avec le bon rythme. Pour chacun, explique brièvement pourquoi ça fonctionne.

**7. Exemples négatifs**
Quels sont des exemples de cette voix qui rate ?
À inclure : des phrases générées par IA qui sonnent trop générique, des phrases trop symétriques ou trop polies, des ouvertures qui semblent mortes. Pour chacun, explique ce qui cloche.

**8. Liste de vérification avant publication**
Comment évaluer si le brouillon fonctionne ?
Exemples :
- Est-ce que ça ressemble à une vraie personne ou à une machine à résumés ?
- L'écriture est-elle trop lisse ?
- Le langage est-il assez spécifique ?
- Des schémas de la liste noire subsistent-ils dans le brouillon ?
- La fin préserve-t-elle de l'énergie, ou s'effondre-t-elle en résumé ?
- Est-ce ainsi que je dirais les choses ?

---

Une session d'entretien bien menée te donne un premier guide utilisable en moins d'une heure. Après, c'est l'usage qui l'affine.

Écrire avec l'IA sans que ça ressemble à de l'IA, ça s'apprend. Et comme beaucoup de choses qui s'apprennent, ça demande un système réutilisable, pas juste de la bonne volonté.

---

*Inspiré de "AI Style Guides" par Katie Parrott et Claude, publié sur Every.to*
