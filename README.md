# DÉLIA

**Décodage · Étiquetage · Langues · Intelligence · Analyse**

Un jeu éducatif pour apprendre, en jouant, comment les machines lisent le langage humain ; de la découpe des mots aux grands modèles de langue, avec un focus rare sur les langues d'Afrique et le NLP à faibles ressources.

DÉLIA est une application web **mono-fichier**, **hors-ligne**, sans backend ni dépendance externe (hormis le chargement optionnel de Python). Tout tient dans un seul `index.html`.

---

## Table des matières

- [Aperçu](#aperçu)
- [Pourquoi DÉLIA](#pourquoi-délia)
- [Fonctionnalités](#fonctionnalités)
- [Contenu pédagogique](#contenu-pédagogique)
  - [Les 7 dossiers NLP](#les-7-dossiers-nlp)
  - [Chapitre Python](#chapitre-python)
  - [Chapitre Programmation orientée objet](#chapitre-programmation-orientée-objet)
  - [Les projets guidés](#les-projets-guidés)
  - [Le labo interactif](#le-labo-interactif)
- [Modes de jeu](#modes-de-jeu)
- [Types d'exercices](#types-dexercices)
- [Progression et motivation](#progression-et-motivation)
- [Détails techniques](#détails-techniques)
- [Installation et déploiement](#installation-et-déploiement)
- [Pour les enseignants](#pour-les-enseignants)
- [Confidentialité et données](#confidentialité-et-données)
- [Accessibilité](#accessibilité)
- [Chiffres clés](#chiffres-clés)
- [Feuille de route](#feuille-de-route)
- [Licence et crédits](#licence-et-crédits)

---

## Aperçu

DÉLIA enseigne le traitement automatique des langues (TAL / NLP) et la linguistique à travers un parcours progressif : une bouchée de théorie, une question interactive, un exemple concret, puis on recommence. Le joueur avance chapitre par chapitre, débloque des « boss » qui combinent plusieurs concepts, construit de vrais mini-outils dans des projets guidés, et peut coder pour de bon en Python directement dans le navigateur.

Le jeu vise un public large : étudiants en linguistique et en informatique, curieux du fonctionnement des IA de langage, enseignants cherchant un support interactif, et plus particulièrement les personnes intéressées par le NLP des langues africaines.

---

## Pourquoi DÉLIA

La plupart des ressources d'apprentissage du NLP sont anglophones et ignorent les langues à faibles ressources. DÉLIA prend le parti inverse :

- **Un dossier entier consacré aux langues africaines** : tons du yoruba, morphologie bantoue du swahili, écritures (n'ko, adlam, ajami, guèze), langues à faibles ressources.
- **Des exemples ancrés** tout au long du jeu : Ouagadougou, le FESPACO, Thomas Sankara, le mooré, le dioula, le bambara, le wolof.
- **Une approche honnête des limites** : biais des modèles, hallucinations, fertilité des tokens (pourquoi un texte en yoruba coûte plus cher qu'un texte en anglais), inégalités entre langues.

Le tout dans une interface pensée d'abord pour le mobile, jouable hors-ligne — un choix qui compte pour l'accès dans des contextes à connexion limitée.

---

## Fonctionnalités

- **Parcours guidé** de 48 unités réparties en 7 chapitres, avec déblocage progressif et carte de progression.
- **143 questions de NLP et de linguistique**, réparties en 7 dossiers d'une vingtaine de questions chacun.
- **Difficulté progressive** : chaque question a un niveau (facile / moyen / difficile) et les parties montent en difficulté.
- **Longueur de partie réglable** (8, 12 ou 20 questions).
- **Chapitre Python complet** (16 leçons) avec du vrai code exécuté dans le navigateur via Pyodide.
- **Chapitre Programmation orientée objet** (7 leçons).
- **7 projets guidés** où l'on construit un mini-outil de NLP fonctionnel.
- **Labo interactif** : 7 outils qui calculent en direct sur le texte de l'utilisateur.
- **Fiches de cours approfondies** pour chaque concept, avec exemples commentés et erreurs courantes.
- **Modes de jeu** : défi 60 secondes chronométré, duel local à deux joueurs.
- **Système de motivation** : 28 badges, série quotidienne, révision espacée des erreurs, défi du jour.
- **Correcteur orthographique** basé sur un dictionnaire de 20 000 mots français, intégré au projet correspondant.
- **Diplôme de fin de parcours** partageable, généré en image.
- **Partage de scores** en texte et en image (carte carrée).
- **Mode enseignant** : liens directs vers chaque activité.
- **Sauvegarde locale** de toute la progression, avec export / import pour changer d'appareil.

---

## Contenu pédagogique

### Les 7 dossiers NLP

Chaque dossier contient une vingtaine de questions graduées et se termine par un « boss » qui combine plusieurs concepts.

| Dossier | Concepts couverts |
|---------|-------------------|
| **Les bases** | Tokenisation, étiquetage morpho-syntaxique (POS), modèles n-grammes, distance d'édition (Levenshtein), plongements lexicaux (embeddings) |
| **Linguistique** | Phonologie (phonèmes, tons, paires minimales), morphologie (morphèmes, flexion/dérivation), syntaxe (arbres de dépendances, ambiguïté), pragmatique (implicatures, actes de langage) |
| **NLP** | Reconnaissance d'entités nommées (NER), TF-IDF, similarité cosinus, mécanisme d'attention |
| **Ouverture** | Expressions régulières, langues du monde (familles, écritures), normalisation (stemming vs lemmatisation), biais des modèles |
| **Langues africaines** | Tons (yoruba), écritures (n'ko, adlam, ajami, guèze), morphologie bantoue (classes nominales), langues à faibles ressources |
| **Modèles modernes** | Embeddings contextuels (BERT), pré-entraînement et fine-tuning, LLM, évaluation (précision, rappel, F1, perplexité, BLEU), transfert cross-lingue, prompting (zero/few-shot) |
| **Génération & fiabilité** | RAG (Retrieval-Augmented Generation), hallucinations, fertilité des tokens, désambiguïsation du sens, coréférence, seq2seq |

Chaque concept dispose d'une **fiche de cours** structurée en cinq parties : l'idée, comment ça marche, un exemple, pourquoi ça compte, et des liens « en savoir plus » (Wikipédia, cours Hugging Face, Jurafsky & Martin, Masakhane…).

### Chapitre Python

Un chapitre de **16 leçons** qui part de zéro et couvre les bases du langage, chacune ancrée dans un exemple NLP. Le code est écrit par l'utilisateur et **exécuté réellement dans le navigateur** grâce à Pyodide (Python compilé en WebAssembly), avec vérification automatique du résultat.

Leçons : variables et chaînes, nombres et calculs, conditions, boucle for, boucle while, listes, dictionnaires, fonctions, f-strings et formatage, tuples et ensembles, compréhensions, méthodes de chaînes, fichiers, modules (dont `Counter`), gestion des erreurs, module `re` (regex). Un projet final assemble le tout en un compteur de mots complet.

Chaque leçon dispose d'une **fiche approfondie** avec exemples commentés et section « erreurs courantes ».

### Chapitre Programmation orientée objet

Un chapitre séparé de **7 leçons** pour penser en objets : classe et objet, attributs, constructeur `__init__`, méthodes, méthode `__str__`, attributs de classe, héritage. Le projet final construit une classe `Tokeniseur` réutilisable.

### Les projets guidés

Sept projets, un par dossier, où l'on construit un vrai mini-outil étape par étape :

1. **Correcteur orthographique** — dictionnaire de 20 000 mots français, distance d'édition, classement par fréquence
2. **Annotateur de corpus** — étiquetage POS, arbre de dépendances, export au format CoNLL-U
3. **Moteur de recherche** — TF-IDF et similarité cosinus sur un corpus
4. **Nettoyeur de tweets** — regex pour liens, mentions, gestion des caractères non-ASCII
5. **Restaurateur de tons yoruba** — désambiguïsation, comparaison de fertilité des tokens
6. **Évaluateur de classifieur** — calcul de précision, rappel, F1 sur des données réelles
7. **Assistant RAG** — sélection de passages, écriture du prompt, détection d'hallucination

### Le labo interactif

Sept outils qui calculent en direct sur le texte tapé par l'utilisateur :

- **Tokeniseur** — découpage en tokens et en sous-mots
- **BPE pas à pas** — le véritable algorithme Byte-Pair Encoding, fusion par fusion, avec le corpus visible
- **Arbre de dépendances libre** — construction manuelle et export CoNLL-U
- **Attention** — visualisation des poids d'attention d'un mot vers les autres
- **Similarité cosinus** — comparaison de deux phrases en sac de mots
- **Distance de Levenshtein** — calcul et alignement lettre à lettre
- **Regex** — motif appliqué en direct sur un texte, correspondances surlignées

---

## Modes de jeu

- **Parcours** — le mode principal, progressif et guidé.
- **Entraînement** — accès libre aux 7 dossiers, tirage aléatoire de questions, sans déblocage imposé.
- **Défi 60 secondes** — questions en rafale, multiplicateurs de combo, une erreur coûte du temps.
- **Duel** — deux joueurs sur le même appareil, chacun son tour, avec bonus de rapidité.
- **Révision** — les questions ratées reviennent, triées des plus manquées aux moins manquées.
- **Défi du jour** — une question quotidienne, identique pour tous, qui entretient la série.

---

## Types d'exercices

DÉLIA utilise sept mécaniques d'interaction pour éviter la monotonie du QCM :

- **quiz** — choix multiple classique
- **tapword** — toucher le bon mot dans une phrase
- **multitap** — sélectionner plusieurs mots (ex. entités nommées)
- **deptree** — construire un arbre de dépendances en reliant les mots
- **buildword** — recomposer un mot à partir de ses sous-mots (BPE, morphèmes)
- **spoterror** — repérer l'erreur dans une sortie de modèle
- **codequiz** — écrire et exécuter du code Python dans une question

---

## Progression et motivation

- **28 badges** couvrant tous les aspects du jeu (premiers pas, sans-faute, boss vaincus, séries quotidiennes, projets, code, fiches lues…).
- **Série quotidienne** (streak) entretenue par une leçon ou un défi par jour.
- **Révision espacée** légère : chaque erreur augmente la probabilité de revoir la question.
- **Écran « ce que tu as travaillé »** en fin de dossier, avec les concepts clés.
- **Diplôme de fin de parcours** personnalisé et partageable.

---

## Détails techniques

- **Un seul fichier HTML** autonome, sans framework, sans build, sans dépendance à installer.
- **JavaScript vanilla** pour toute la logique de jeu et l'interface.
- **Pyodide** (chargé à la demande, uniquement à l'ouverture des chapitres de code) pour exécuter du Python réel dans le navigateur via WebAssembly.
- **Canvas HTML** pour la génération des images (diplôme, cartes de partage).
- **SVG** pour les arbres de dépendances et certaines visualisations.
- **localStorage** pour la sauvegarde de la progression, avec repli silencieux si le stockage est indisponible.
- **Dictionnaire de 20 000 mots français** intégré (classés par fréquence), pour le projet correcteur.
- **Conception mobile-first** : barre de navigation fixe, carrousels horizontaux, cibles tactiles larges.
- **Fonctionne hors-ligne** une fois la page chargée (hors premier chargement de Pyodide).

---

## Installation et déploiement

DÉLIA n'a aucune étape de compilation. Le fichier `index.html` se suffit à lui-même.

### En local

Ouvrir `index.html` dans un navigateur moderne. Remarque : ouvert directement depuis le disque (`file://`), certaines fonctions comme la sauvegarde locale ou le chargement de Python peuvent être bloquées par le navigateur. Pour un test complet, servir le fichier via un hébergement ou un serveur local.

### GitHub Pages

1. Déposer `index.html` à la racine du dépôt (via glisser-déposer pour éviter toute troncature).
2. Dans **Settings → Pages**, choisir la source **Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Le site est publié à `https://<utilisateur>.github.io/<dépôt>/`.

### Netlify

Glisser-déposer le fichier (renommé `index.html`) sur [app.netlify.com/drop](https://app.netlify.com/drop). Un compte gratuit rend le déploiement permanent.

> **Important** : le fichier doit s'appeler `index.html`, et être **uploadé** (glissé-déposé), jamais copié-collé dans l'éditeur web — un fichier de cette taille serait tronqué au collage, ce qui produit une page blanche.

---

## Pour les enseignants

Le mode enseignant génère des **liens directs** vers chaque activité, à envoyer aux élèves. Le jeu s'ouvre alors directement sur l'activité visée, sans passer par l'accueil :

- `#parcours` — le parcours guidé
- `#dossier=nlp` — un dossier précis (bases, linguistique, nlp, ouverture, afrique, modeles, generation)
- `#python` / `#poo` — les chapitres de code
- `#labo`, `#defi`, `#duel`, `#fiches` — les modes correspondants
- `#fiche=Attention` — une fiche de cours précise

La progression de chaque élève reste sur son propre appareil.

---

## Confidentialité et données

- **Aucune donnée envoyée** : tout se passe dans le navigateur.
- La progression (scores, badges, série, erreurs) est stockée **localement** via `localStorage`.
- Une fonction d'**export / import** permet de transférer sa progression d'un appareil à l'autre sous forme de code.
- Le nom saisi pour le diplôme reste local.

---

## Accessibilité

- Respect de `prefers-reduced-motion` (désactivation des animations pour les personnes sensibles au mouvement).
- Cibles tactiles larges, pensées pour le pouce.
- Contraste élevé du thème sombre.
- Sélecteur de longueur de partie pour adapter le rythme.

---

## Chiffres clés

| Élément | Quantité |
|---------|----------|
| Dossiers NLP | 7 |
| Questions NLP / linguistique | 143 |
| Unités du parcours | 48 |
| Projets guidés | 7 |
| Leçons Python | 16 |
| Leçons POO | 7 |
| Fiches de cours (NLP + Python + POO) | 57 |
| Outils du labo | 7 |
| Types d'exercices | 7 |
| Badges | 28 |
| Mots du dictionnaire correcteur | 20 000 |
| Dépendances externes | 0 (Pyodide chargé à la demande) |

---

## Feuille de route

Pistes envisagées pour les versions futures :

- Élargir chaque dossier vers 25-30 questions pour plus de variété entre les parties.
- Nouveaux types d'exercices visuels (glisser-déposer de morphèmes, exploration d'embeddings en 2D).
- Mode « exploration libre » des concepts sous forme de carte.
- Synthèse vocale pour la phonologie et les tons.
- Interface disponible en anglais (le contenu linguistique restant en français).
- Version PWA installable pour un usage hors-ligne complet.

---

## Licence et crédits

Projet éducatif personnel.

**Sources et ressources citées dans les fiches** : Wikipédia (FR), le cours de NLP de Hugging Face, *Speech and Language Processing* de Jurafsky & Martin, [Masakhane](https://www.masakhane.io/) (NLP pour les langues africaines), Lacuna Fund.

**Dictionnaire français** dérivé de données de fréquence lexicale ouvertes.

**Pyodide** — Python dans le navigateur, sous licence Mozilla Public License 2.0.

---

*DÉLIA — parce que le NLP ne parle pas qu'anglais.*
