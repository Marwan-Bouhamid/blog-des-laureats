# Vision Produit et User Stories — Blog des Lauréats

> **Atelier** : Définir la vision produit et exprimer les besoins en User Stories  
> **Unité d'apprentissage** : UA.351.11 — Initiation à la démarche Agile et cadre Scrum  
> **Projet** : Blog des Lauréats — Solicode Tanger  
> **Apprenant** : Marwan bouhamid  
> **Encadrant** : ESSARRAJ Fouad  
> **Date** : 26 novembre 2026  
> **Version** : 1.0

---

## 1. Contexte de l'atelier

Cet atelier applique la démarche d'expression des besoins au projet technique **Blog des Lauréats**. Il ne reprend pas l'exemple générique de la TodoList : il part du dépôt réel, du cadrage existant, du diagramme de cas d'utilisation et du diagramme de classes du projet.

L'objectif est de produire une Vision Produit, deux Personas contrastés, des User Stories avec critères d'acceptation, puis de délimiter le MVP. Le document distingue systématiquement :

- les informations **vérifiées dans le dépôt** ;
- les **interprétations** raisonnables mais non confirmées ;
- les **hypothèses** sur les utilisateurs, à valider.

---

## 2. Introduction

Le Blog des Lauréats est une application web destinée à la communauté de Solicode Tanger. Les lauréats y partagent leurs parcours professionnels sous forme d'articles ; les apprenants actuels consultent ces retours d'expérience pour mieux comprendre les métiers, les spécialités et les trajectoires possibles.

Le dépôt documente déjà le contexte, le périmètre, les acteurs et les premiers cas d'utilisation. En revanche, il ne contient ni entretiens utilisateurs, ni statistiques d'usage, ni code applicatif permettant de vérifier l'état réel de l'implémentation. Les Personas et les priorités proposés ici sont donc des hypothèses de travail à confirmer par le Product Owner et par des retours d'utilisateurs.

---

## 3. Vision Produit

### 3.1 Énoncé de la vision

> **Pour les lauréats de Solicode Tanger qui souhaitent transmettre leur expérience, et pour les apprenants qui cherchent des exemples concrets de parcours professionnels, le Blog des Lauréats est une plateforme web communautaire qui centralise et valorise les témoignages des anciens apprenants sous forme d'articles lisibles et modérés. Là où ces témoignages restent dispersés et informels, elle offre un espace structuré et durable, dédié à la communauté de Solicode.**

### 3.2 Problème résolu

Le dépôt identifie explicitement le besoin de **centraliser les témoignages, les expériences et les réalisations des lauréats** afin de faciliter le partage de connaissances entre promotions et de renforcer la visibilité de la communauté (`docs/cadrage/note-cadrage.md`).

Trois difficultés découlent de ce besoin :

1. **Pour les apprenants** : les retours d'expérience sont difficiles à retrouver et ne sont pas toujours adaptés à leur niveau ou à leur spécialité.
2. **Pour les lauréats** : il n'existe pas d'espace dédié, simple et durable pour présenter leur parcours et leurs réalisations.
3. **Pour la communauté Solicode** : les contenus produits pendant la formation ne sont ni capitalisés ni valorisés dans un lieu unique.

### 3.3 Valeur apportée

| Bénéficiaire | Valeur attendue |
|---|---|
| Apprenant / visiteur | Découvrir des parcours concrets, comprendre les débouchés et trouver des modèles inspirants. |
| Lauréat contributeur | Partager son expérience, valoriser ses compétences et garder une trace durable de son parcours. |
| Communauté Solicode | Capitaliser les témoignages entre promotions et renforcer sa visibilité. |
| Administrateur | Garantir la qualité, la cohérence et la publication des contenus. |

### 3.4 Ce que la vision ne promet pas

La vision ne promet ni réseau social, ni messagerie, ni recommandations par intelligence artificielle, ni paiement en ligne. Ces éléments sont explicitement exclus du périmètre dans la note de cadrage. Elle ne promet pas non plus de recherche avancée dans le MVP : la recherche et le filtrage sont reportés aux évolutions futures (section 8).

---

## 4. Utilisateurs cibles

### 4.1 Acteurs retenus

| Acteur | Rôle | Besoin principal | Statut | Preuve dans le dépôt |
|---|---|---|---|---|
| **Lauréat contributeur** | Ancien apprenant de Solicode qui rédige, publie et gère ses articles. | Partager son parcours et valoriser son profil. | Acteur primaire | `README.md`, diagramme de cas d'utilisation, note de cadrage |
| **Apprenant / visiteur** | Apprenant actuel ou visiteur qui consulte les articles et les profils. | Découvrir des parcours et des conseils concrets. | Acteur primaire | `README.md`, diagramme de cas d'utilisation, note de cadrage |
| **Administrateur** | Gère les catégories et modère les publications. | Garantir la qualité et la conformité des contenus. | Acteur secondaire | Diagramme de cas d'utilisation, note de cadrage |

### 4.2 Acteurs évoqués mais non confirmés

Des versions antérieures du rapport, supprimées lors de la réorganisation des chapitres, mentionnaient également le **formateur** et le **recruteur** (carte d'empathie, cahier des charges, branche fonctionnelle). Ces acteurs ne figurent plus dans le diagramme de cas d'utilisation actuel ni dans la note de cadrage. Ils ne sont donc pas retenus comme cibles principales dans ce document ; leur réintégration éventuelle doit être validée par le Product Owner.

### 4.3 Limite méthodologique

Aucun entretien, questionnaire ou statistique d'usage n'est présent dans le dépôt. Les besoins ci-dessus sont déduits de la documentation fonctionnelle. Les Personas qui suivent sont donc des **personas de conception**, et non des portraits validés par des utilisateurs réels.

---

## 5. Personas

> **Convention de lecture** : les noms, âges, outils et habitudes sont fictifs. Les éléments marqués **(hypothèse)** doivent être validés. Les rôles et les besoins principaux sont, eux, adossés à la documentation du projet.

### 5.1 Persona 1 — Yassine, le lauréat contributeur

**Nom** : Yassine (fictif) — **Profil** : ancien apprenant de Solicode Tanger, aujourd'hui développeur junior **(hypothèse sur le métier exact)**.

| Dimension | Description |
|---|---|
| **Rôle** | Lauréat autorisé à rédiger, publier et administrer ses propres articles. |
| **Objectifs** | Raconter son parcours ; valoriser ses compétences auprès des recruteurs ; aider les apprenants ; conserver une trace durable de son expérience. |
| **Besoins et attentes** | Un éditeur simple ; la possibilité d'enregistrer un brouillon ; une soumission claire ; le suivi du statut de l'article ; une consultation confortable sur mobile. |
| **Problèmes et frustrations** | Ne pas savoir où publier ; disperser son témoignage sur les réseaux sociaux ; faire face à un outil trop technique ; ignorer si son article a été publié ou refusé. |
| **Contraintes** | Temps limité en dehors du travail **(hypothèse)** ; compétences rédactionnelles variables ; connexion parfois mobile **(hypothèse)**. |
| **Motivation** | Transmission, reconnaissance professionnelle et visibilité. |
| **Comportement pertinent** | Rédige par sessions courtes ; consulte l'état de ses articles ; partage le lien une fois publié **(hypothèse)**. |

> « Je veux raconter mon parcours simplement, sans que la technique me bloque. » — citation fictive illustrant le persona.

### 5.2 Persona 2 — Salma, l'apprenante

**Nom** : Salma (fictive) — **Profil** : apprenante actuelle à Solicode Tanger, en cours de spécialisation **(hypothèse sur le niveau)**.

| Dimension | Description |
|---|---|
| **Rôle** | Consulte et lit les articles publiés par les lauréats. |
| **Objectifs** | Comprendre les parcours possibles ; choisir une spécialité ; préparer son insertion professionnelle ; trouver des modèles concrets. |
| **Besoins et attentes** | Une liste claire des articles ; une lecture confortable sur mobile ; des contenus classés par catégorie ; des informations fiables sur l'auteur et son parcours. |
| **Problèmes et frustrations** | Conseils trop génériques ; informations éparpillées ; contenus trop techniques ou obsolètes ; difficulté à trouver un témoignage proche de son propre parcours. |
| **Contraintes** | Temps disponible limité entre les cours ; consultation principalement sur mobile **(hypothèse)** ; niveau de lecture technique variable. |
| **Motivation** | Réussir sa formation et construire un projet professionnel réaliste. |
| **Comportement pertinent** | Consulte les articles entre deux cours ; privilégie les contenus courts et concrets ; partage un article utile avec ses camarades **(hypothèse)**. |

> « Je cherche des exemples de personnes parties du même point que moi. » — citation fictive illustrant le persona.

### 5.3 Contraste entre les deux Personas

| Critère | Yassine (lauréat) | Salma (apprenante) |
|---|---|---|
| **Posture** | Producteur de contenu | Consommatrice de contenu |
| **Objectif dominant** | Transmettre et valoriser son parcours | Découvrir et s'orienter |
| **Bénéfice recherché** | Reconnaissance et visibilité | Guidage et inspiration |
| **Interaction clé** | Rédiger, soumettre, suivre le statut | Parcourir la liste, lire un article |
| **Contrainte principale** | Temps et simplicité de rédaction | Temps et lisibilité sur mobile |
| **Risque si le produit échoue** | Aucun espace pour publier son témoignage | Aucun contenu fiable à consulter |

Ce contraste est volontaire : il couvre les deux extrémités de la chaîne de valeur, la **production** et la **consultation** du contenu.

---

## 6. User Stories

### 6.1 Format et conventions

Chaque User Story respecte strictement la syntaxe :

> **En tant que** [type d'utilisateur], **je veux** [action ou besoin] **afin de** [bénéfice].

Les critères d'acceptation suivent le format Gherkin *Given / When / Then*, restitué en français : **Étant donné / Quand / Alors**. Chaque critère est observable et testable.

**Échelle de priorité utilisée :**

- **Haute** : indispensable à la valeur du MVP.
- **Moyenne** : importante, mais peut être livrée après le socle.
- **Basse** : utile, non bloquante.

### 6.2 User Story US-01 — Consulter la liste des articles publiés

| Champ | Valeur |
|---|---|
| **ID** | US-01 |
| **Titre** | Consulter la liste des articles publiés |
| **Persona** | Salma (apprenante) |
| **Priorité** | Haute |

**En tant qu'apprenante, je veux consulter la liste des articles publiés afin de découvrir les parcours des lauréats et choisir ceux qui m'intéressent.**

**Valeur métier** : la liste est le point d'entrée du blog. Sans elle, les articles existent mais restent difficiles à découvrir.

**Justification de la priorité** : sans liste accessible, la promesse de partage et de découverte n'est pas remplie.

**Critères d'acceptation :**

- **Étant donné** des articles publiés et des articles en brouillon, **quand** j'ouvre la page de liste, **alors** seuls les articles publiés sont affichés, avec leur titre, leur auteur, leur catégorie et leur date de publication.
- **Étant donné** la liste affichée, **quand** je sélectionne un article, **alors** je suis dirigé vers la page de détail correspondante.
- **Étant donné** qu'aucun article n'est publié, **quand** j'ouvre la liste, **alors** un message explicite indique qu'aucun article n'est disponible.

### 6.3 User Story US-02 — Lire le détail d'un article

| Champ | Valeur |
|---|---|
| **ID** | US-02 |
| **Titre** | Lire le détail d'un article |
| **Persona** | Salma (apprenante) |
| **Priorité** | Haute |

**En tant qu'apprenante, je veux lire le détail d'un article afin de comprendre le parcours et les conseils d'un lauréat.**

**Valeur métier** : c'est le cœur de la promesse produit. L'article est le contenu qui transmet l'expérience et crée l'utilité pour l'apprenante.

**Justification de la priorité** : cette fonctionnalité est la première cible du Sprint 1 et constitue la valeur minimale du blog.

**Critères d'acceptation :**

- **Étant donné** un article publié identifié par son slug, **quand** j'ouvre l'URL `/articles/{slug}`, **alors** le titre, le contenu, l'auteur, la catégorie et la date de publication sont affichés.
- **Étant donné** un slug inexistant ou un article non publié, **quand** j'ouvre son URL, **alors** une page d'erreur 404 est affichée et aucun contenu de l'article n'est révélé.
- **Étant donné** un écran mobile ou de bureau, **quand** je lis l'article, **alors** le contenu reste lisible sans défilement horizontal.

### 6.4 User Story US-03 — Créer un compte et se connecter

| Champ | Valeur |
|---|---|
| **ID** | US-03 |
| **Titre** | Créer un compte et se connecter |
| **Persona** | Yassine (lauréat) |
| **Priorité** | Moyenne |

**En tant que lauréat, je veux créer un compte et me connecter afin d'accéder à mon espace de rédaction.**

**Valeur métier** : l'authentification protège l'identité des auteurs et conditionne la contribution. Elle ne crée pas de valeur seule, mais elle rend possible la production de contenu.

**Justification de la priorité** : fonctionnalité habilitante, livrable juste avant la rédaction. Elle est indispensable au MVP, mais peut être regroupée avec US-04 dans un même incrément.

**Critères d'acceptation :**

- **Étant donné** un visiteur sur le formulaire d'inscription, **quand** il saisit un nom, un courriel et un mot de passe valides, **alors** un compte avec le rôle « lauréat » est créé et il est authentifié.
- **Étant donné** un compte existant, **quand** les identifiants saisis sont incorrects, **alors** l'accès est refusé et un message d'erreur explicite est affiché.
- **Étant donné** un visiteur non authentifié, **quand** il tente d'accéder à l'espace de rédaction, **alors** il est redirigé vers la page de connexion.

### 6.5 User Story US-04 — Rédiger et soumettre un article

| Champ | Valeur |
|---|---|
| **ID** | US-04 |
| **Titre** | Rédiger et soumettre un article |
| **Persona** | Yassine (lauréat) |
| **Priorité** | Haute |

**En tant que lauréat, je veux rédiger un article, l'enregistrer en brouillon puis le soumettre afin de partager mon parcours professionnel.**

**Valeur métier** : c'est la fonctionnalité qui alimente le blog et garantit sa durabilité. Sans contribution, le contenu ne se renouvelle pas.

**Justification de la priorité** : elle complète la chaîne de valeur avec la lecture et rend le produit réellement communautaire.

**Critères d'acceptation :**

- **Étant donné** un lauréat authentifié, **quand** il renseigne un titre, un contenu et une catégorie puis enregistre un brouillon, **alors** l'article est enregistré au statut « brouillon » et n'est visible que dans son espace personnel.
- **Étant donné** un brouillon complet, **quand** le lauréat le soumet, **alors** son statut passe à « en attente de publication » et il n'apparaît pas dans la liste publique.
- **Étant donné** un champ obligatoire manquant, **quand** le lauréat tente d'enregistrer ou de soumettre, **alors** des messages de validation s'affichent et aucun enregistrement incomplet n'est créé.

### 6.6 User Story US-05 — Suivre le statut de mes articles

| Champ | Valeur |
|---|---|
| **ID** | US-05 |
| **Titre** | Suivre le statut de mes articles |
| **Persona** | Yassine (lauréat) |
| **Priorité** | Moyenne |

**En tant que lauréat, je veux suivre le statut de mes articles afin de savoir s'ils sont en brouillon, en attente de publication ou publiés.**

**Valeur métier** : la transparence sur l'état de publication réduit l'incertitude et encourage la contribution.

**Justification de la priorité** : confort indispensable au contributeur, mais non bloquant pour une première mise en ligne.

**Critères d'acceptation :**

- **Étant donné** un lauréat authentifié possédant plusieurs articles, **quand** il ouvre son espace personnel, **alors** chaque article affiche son titre, son statut et, s'il est publié, sa date de publication.
- **Étant donné** un article en attente de publication, **quand** l'administrateur le publie, **alors** son statut devient « publié » et il apparaît dans la liste publique.
- **Étant donné** un article encore en brouillon, **quand** un visiteur ouvre la liste publique, **alors** cet article n'y figure pas.

### 6.7 Synthèse des User Stories

| ID | User Story | Persona | Priorité | Fonctionnalité MVP associée |
|---|---|---|---|---|
| US-01 | Consulter la liste des articles publiés | Salma | Haute | Liste publique |
| US-02 | Lire le détail d'un article | Salma | Haute | Page article |
| US-03 | Créer un compte et se connecter | Yassine | Moyenne | Authentification |
| US-04 | Rédiger et soumettre un article | Yassine | Haute | Espace de rédaction |
| US-05 | Suivre le statut de mes articles | Yassine | Moyenne | Espace personnel |

---

## 7. MVP — Périmètre de la première version utilisable

### 7.1 Définition retenue

Le MVP est la plus petite version du Blog des Lauréats qui permet de **fermer la boucle de valeur** : un lauréat s'inscrit, rédige et soumet un article ; un administrateur le publie ; un apprenant le découvre et le lit.

Une fonctionnalité n'est pas classée dans le MVP parce qu'elle existe déjà ou parce qu'elle est facile à coder, mais parce qu'elle est nécessaire à cette boucle.

### 7.2 Fonctionnalités essentielles

| # | Fonctionnalité | User Story | Justification | État documenté |
|---|---|---|---|---|
| 1 | Liste des articles publiés | US-01 | Point d'entrée et découverte du contenu. | Planifié (cas d'utilisation, note de cadrage) |
| 2 | Lecture du détail d'un article et gestion de la 404 | US-02 | Cœur de la valeur : transmettre le témoignage. | Documenté comme livré au Sprint 1 |
| 3 | Inscription et connexion des lauréats | US-03 | Protège l'identité et rend la contribution possible. | Planifié (note de cadrage) |
| 4 | Rédaction, brouillon et soumission d'un article | US-04 | Alimente le blog et garantit sa durabilité. | Planifié (cas d'utilisation, modèle Article) |
| 5 | Suivi du statut des articles | US-05 | Donne de la visibilité au contributeur. | Planifié (gestion des statuts) |
| 6 | Modération et publication par l'administrateur | Support de US-04 et US-05 | Aucun contenu ne devient public sans validation ; garantit la qualité. | Planifié (cas d'utilisation) |
| 7 | Référentiel de catégories existantes | Support de US-04 | L'article doit être classé ; la gestion complète des catégories peut attendre. | Modèle documenté (classe Catégorie) |

> **Précision** : la modération (ligne 6) est portée par l'acteur secondaire **Administrateur**. Elle ne fait pas l'objet d'une des cinq User Stories retenues, centrées sur les deux Personas principaux, mais reste indispensable au parcours de valeur.

### 7.3 Parcours minimal couvert

1. Salma ouvre la liste des articles publiés et sélectionne un article (US-01, US-02).
2. Yassine crée son compte et se connecte (US-03).
3. Yassine rédige un article, l'enregistre en brouillon puis le soumet (US-04).
4. L'administrateur modère et publie l'article (fonctionnalité de support).
5. Yassine constate que son article est publié (US-05) et Salma peut désormais le lire.

### 7.4 Ce qui n'est pas nécessaire au MVP

- La recherche et le filtrage avancé : la liste suffit pour un volume initial faible.
- Les profils publics détaillés : le nom de l'auteur dans l'article suffit à la première version.
- La gestion complète des catégories : un référentiel préparé permet de démarrer.
- La modification d'un article déjà publié : le brouillon peut être corrigé avant soumission.
- La gestion des utilisateurs par l'administrateur : le volume initial ne la justifie pas.
- La version mobile native : le web responsive couvre le besoin initial.

> **À valider** : la frontière exacte du MVP et l'ordre des priorités relèvent d'une décision du Product Owner. Les propositions ci-dessus sont argumentées, mais ne constituent pas une décision d'équipe enregistrée dans le dépôt.

---

## 8. Évolutions futures — Hors MVP

| Fonctionnalité | Pourquoi elle est reportée | Source | Statut |
|---|---|---|---|
| Recherche plein texte | Utile lorsque le nombre d'articles augmente ; non bloquante au lancement. | Note de cadrage (« recherche des articles ») | À planifier |
| Filtrage par catégories | Améliore la découverte, mais la liste initiale reste exploitable. | Note de cadrage | À planifier |
| Gestion des catégories (CRUD administrateur) | Un référentiel initial suffit pour le MVP. | Note de cadrage, cas d'utilisation | À planifier |
| Profils publics des lauréats | Enrichit la valorisation des parcours ; l'article affiche déjà l'auteur. | Note de cadrage | À planifier |
| Modification et suppression d'articles publiés | Le workflow brouillon → soumission → publication suffit au départ. | Cas d'utilisation | À planifier |
| Gestion des utilisateurs par l'administrateur | Nécessaire avec la croissance, pas pour une première version. | Note de cadrage | À planifier |
| Version Android en lecture (NativePHP) | Le web responsive couvre le besoin initial. | `docs/cadrage/stack-technique.md` | À arbitrer (voir ci-dessous) |

### 8.1 Points de contradiction à arbitrer

- **Mobile natif** : la note de cadrage classe les « applications mobiles natives » hors périmètre, tandis que la stack technique prévoit une version Android en lecture via NativePHP. Les deux documents ne peuvent pas être vrais simultanément ; une décision du Product Owner est nécessaire.
- **Version de Laravel** : le `README.md` mentionne Laravel 12, le chapitre « Réalisation » mentionne Laravel 13. Cette divergence n'affecte pas la Vision Produit, mais doit être corrigée dans la documentation technique.

### 8.2 Fonctionnalités explicitement hors périmètre

Conformément à la note de cadrage, les éléments suivants ne font pas partie du produit, même à terme, sauf décision contraire :

- messagerie instantanée ;
- paiement et abonnements en ligne ;
- réseau social complexe ;
- recommandations par intelligence artificielle ;
- synchronisation avec des plateformes externes.

---

## 9. Conclusion

La Vision Produit du Blog des Lauréats tient en une idée : **transformer des expériences individuelles en ressources utiles pour toute la communauté Solicode**.

Les deux Personas montrent que le produit doit réussir deux parcours complémentaires : permettre à un lauréat de publier simplement son témoignage, et permettre à un apprenant de le trouver et de le lire confortablement. Les cinq User Stories retenues couvrent cette chaîne, de la consultation à la soumission, avec des critères d'acceptation testables.

Le MVP proposé reste volontairement resserré : liste, lecture, authentification, rédaction, suivi du statut et modération. Les fonctions de confort — recherche, filtrage, profils publics, gestion avancée — sont reportées. Cette délimitation devra être confirmée par le Product Owner avant d'alimenter le Product Backlog.

---

## 10. Sources et hypothèses

### 10.1 Preuves vérifiées dans le dépôt

| Source | Informations utilisées |
|---|---|
| `README.md` | Description du projet, cibles (lauréats, apprenants), stack, application déployée en ligne. |
| `docs/cadrage/note-cadrage.md` | Contexte, objectif SMART, périmètre In-Scope / Out-of-Scope, parties prenantes, contraintes, risques. |
| `docs/cadrage/stack-technique.md` | Exigences de sécurité, responsive, version Android en lecture via NativePHP. |
| `rapport/chapitres/13 - Diagramme de cas d’utilisation.md` | Acteurs (Apprenant, Lauréat, Administrateur) et cas d'utilisation. |
| `rapport/chapitres/15 - Diagramme de classes.md` | Entités Laureat, Article, Categorie ; statut de l'article ; date de publication. |
| `rapport/chapitres/17 - Réalisation.md` | Route `/articles/{slug}`, gestion de la 404, architecture MVC. |
| `rapport/chapitres/7 - Méthode SCRUM.md` | Objectif du Sprint 1 et travaux documentés. |
| `sprints/sprints.md` | Sprint 1 actif : consultation d'un article, gabarit Blade responsive, gestion 404. |
| `presentations/presentation.md` | Métadonnées du projet (apprenant, encadrant, établissement). |
| Historique Git (fichiers supprimés) | Ancienne carte d'empathie et ancien cahier des charges mentionnant formateur et recruteur. |

### 10.2 Interprétations soutenues mais non confirmées

- Le besoin de centralisation est explicite ; l'idée que les témoignages sont aujourd'hui « dispersés sur les réseaux sociaux » est une interprétation du contexte, non une donnée mesurée.
- Les priorités Haute / Moyenne et la frontière du MVP sont des propositions argumentées, à valider par le Product Owner.
- Le statut intermédiaire « en attente de publication » est proposé pour matérialiser la modération ; le diagramme de classes ne mentionne explicitement que les statuts brouillon et publié.
- L'ordre des User Stories suppose que la consultation et la rédaction sont plus critiques que le suivi du statut.

### 10.3 Hypothèses à valider

- Les noms, âges, métiers, niveaux d'étude, habitudes de navigation et équipements des Personas sont fictifs.
- On suppose que les apprenants consultent majoritairement sur mobile et que les lauréats disposent de peu de temps pour rédiger.
- On suppose qu'un volume initial faible d'articles rend la recherche et le filtrage non prioritaires.
- On suppose que l'administrateur est une personne de l'équipe pédagogique ou du groupe projet ; ce rôle n'est pas nominativement défini dans le dépôt.

### 10.4 Informations manquantes

- Entretiens, questionnaires ou statistiques sur les utilisateurs réels.
- Product Backlog et dossier `issues/` : mentionnés dans le README et les sprints, mais absents du dépôt.
- Code source de l'application Laravel : absent de ce dépôt, donc l'état réel de l'implémentation n'est pas vérifiable ici.
- Validation formelle du MVP, des priorités et des statuts par le Product Owner.
- Décision sur les acteurs formateur et recruteur.
- Arbitrage sur la version mobile native et sur la version de Laravel.

> **Conclusion sur la fiabilité** : les éléments fonctionnels de ce document sont adossés à la documentation du dépôt. Les portraits, les priorités et la frontière du MVP sont des propositions de travail explicitement signalées comme telles ; ils ne doivent pas être présentés comme des décisions validées.
