# Planifier, découper et piloter un Sprint — Blog des Lauréats

> **Atelier** : Planifier, découper et piloter un Sprint de développement  
> **Unité d'apprentissage** : UA.351.11 — Initiation à la démarche Agile et cadre Scrum  
> **Projet** : Blog des Lauréats — Solicode Tanger  
> **Apprenant** : Marwan bouhamid  
> **Encadrant** : ESSARRAJ Fouad  
> **Product Owner désigné dans le dépôt** : Groupe 1 (`docs/cadrage/note-cadrage.md`)  
> **Date** : 26 novembre 2026  
> **Version** : 1.0

> **Statut du document — simulation de planification.** Le dépôt documente un Sprint 1 actif et présente US-02 comme livrée, mais **aucun code source Laravel n'est présent** pour le vérifier. Ce document ne rapporte donc **aucune exécution réelle** : il propose un plan de sprint, un découpage technique et une simulation de Daily Scrum. Les heures indiquées sont des **estimations de planification**, pas des heures travaillées mesurées.

---

## 1. Contexte et statut du document

### 1.1 Objet de l'atelier

Cet atelier prolonge les deux ateliers précédents :

1. **Vision Produit et User Stories** : cinq User Stories validées avec critères d'acceptation.
2. **Créer, estimer et ordonner le Product Backlog** : dix stories estimées, priorisées en MoSCoW, avec une proposition de Sprint 1 à 8 Story Points.

Il répond à une question opérationnelle : *comment transformer une sélection de stories en un plan de travail exécutable, suivi et ajustable au quotidien ?*

Le document couvre cinq livrables :

- un **Sprint Goal** orienté valeur ;
- un **Sprint Backlog** sélectionné dans le backlog existant ;
- un **découpage en micro-tâches techniques de 1 à 3 heures** ;
- un **tableau Kanban** avec colonnes, règles de flux et limites WIP ;
- un **protocole de Daily Scrum** illustré par la simulation d'un blocage technique.

### 1.2 Documents de référence

| Source | Éléments réutilisés |
|---|---|
| `tutoriels/scrum/initiation-scrum/vision-besoins/vision-besoins.md` | US-01 et US-02, critères d'acceptation, valeur métier, MVP. |
| `tutoriels/scrum/initiation-scrum/product-backlog/product-backlog.md` | Backlog ordonné, estimations 5 SP et 3 SP, MoSCoW, DoR, DoD, sélection Sprint 1 à 8 SP. |
| `sprints/sprints.md` | Sprint 1 actif, objectif, branche `sprint1`, US-02 documentée comme livrée. |
| `docs/cadrage/note-cadrage.md` | Product Owner (Groupe 1), périmètre, contraintes, accessibilité. |
| `docs/cadrage/stack-technique.md` | Laravel, MySQL, Blade, tests PHPUnit/Pest, sécurité, responsive. |
| `rapport/chapitres/17 - Réalisation.md` | Route `/articles/{slug}`, `ArticleController`, `ArticleService`, gestion 404, architecture 2 couches. |
| `rapport/chapitres/15 - Diagramme de classes.md` | Entités `Article`, `Laureat`, `Categorie` ; attributs `slug`, `statut`, `publieLe`. |
| `rapport/chapitres/13 - Diagramme de cas d’utilisation.md` | Cas « Consulter la liste des articles » et « Lire le détail d'un article ». |
| `README.md` | Stack, architecture, organisation du dépôt. |

### 1.3 Statut du Sprint 1 dans le dépôt

| Constat | Conséquence pour ce document |
|---|---|
| `sprints/sprints.md` déclare un **Sprint 1 actif** : initialisation, cadrage et première fonctionnalité Laravel. | Le cadre du sprint existe déjà ; ce document en détaille le **périmètre fonctionnel proposé**. |
| L'atelier Product Backlog a proposé **US-02 + US-01 = 8 SP** pour ce Sprint 1. | Cette sélection est reprise **sans modification d'estimation**. |
| US-02 est documentée comme livrée au Sprint 1. | Les tâches T-01 à T-04 sont présentées comme **vérification et consolidation** si l'implémentation existe réellement ; le code étant absent, l'état n'est pas vérifiable ici. |
| Le dépôt est actuellement sur la branche `sprint0`, alors que la documentation déclare `sprint1` active. | **Prérequis** : vérifier et basculer sur la branche `sprint1` avant de démarrer. |
| Le dossier `issues/` est absent. | Aucun suivi de tâches existant à réutiliser ; le Kanban de ce document est une proposition. |

### 1.4 Ce que ce document n'est pas

- Ce n'est **pas un rapport d'exécution** : aucune tâche n'est déclarée réalisée.
- Ce n'est **pas une prévision de durée** : aucune durée de sprint, capacité ou vélocité n'est inventée.
- Ce n'est **pas une validation du Product Owner** : les choix de périmètre restent des propositions.
- Ce n'est **pas un engagement d'équipe** : la DoR et la DoD citées sont elles-mêmes des propositions de l'atelier précédent.

---

## 2. Cadre du sprint et point de départ

### 2.1 Product Goal et Vision Produit

Le dépôt ne contient **pas d'énoncé formel de Product Goal**. La Vision Produit de l'atelier précédent en tient lieu :

> **Pour les lauréats de Solicode Tanger qui souhaitent transmettre leur expérience, et pour les apprenants qui cherchent des exemples concrets de parcours professionnels, le Blog des Lauréats est une plateforme web communautaire qui centralise et valorise les témoignages des anciens apprenants sous forme d'articles lisibles et modérés.**

Le Sprint Goal proposé doit être une **tranche visible de cette vision** : rendre les articles **lisibles et découvrables** par le public.

### 2.2 État du Product Backlog

| Indicateur | Valeur | Source |
|---|---|---|
| User Stories analysées | 10 (US-01 à US-10) | Atelier Product Backlog |
| Effort total | 47 SP (dont éléments différés) | Atelier Product Backlog |
| Périmètre MVP | 5 stories — 26 SP | Atelier Product Backlog |
| Sélection Sprint 1 proposée | US-02 + US-01 — 8 SP | Atelier Product Backlog, section 10 |
| Vélocité connue | **Aucune** | Aucun sprint terminé documenté |
| Durée de sprint fixée | **Aucune** | Non documentée dans le dépôt |

### 2.3 Périmètre retenu

| Élément | Valeur |
|---|---|
| **Sprint** | Sprint 1 — planification opérationnelle de l'incrément proposé |
| **Stories** | US-02 (5 SP) + US-01 (3 SP) |
| **Total Story Points** | **8 SP** |
| **Micro-tâches** | 8 tâches (T-01 à T-08) |
| **Total heures estimées** | **14 h** |
| **Objectif** | Offrir un premier parcours public complet : liste → détail |

### 2.4 Contraintes connues

- **Capacité inconnue** : aucun membre, horaire ou disponibilité n'est documenté. Le plan est un **périmètre**, pas un engagement calendaire.
- **Durée inconnue** : elle doit être décidée au Sprint Planning ; elle n'est pas inventée ici.
- **Code absent** : l'état réel de US-02 ne peut pas être vérifié.
- **Équipe individuelle** : le projet est présenté comme un projet technique individuel ; le Product Owner est le Groupe 1 et l'encadrant peut assurer la facilitation et la revue.
- **Branche** : travailler sur `sprint1` après vérification, pas sur `sprint0`.

---

## 3. Sprint Goal

### 3.1 Énoncé

> **Rendre le blog publiquement utile : permettre à un apprenant ou à un visiteur de découvrir la liste des articles publiés et d'en lire le détail confortablement, sur mobile comme sur ordinateur.**

### 3.2 Valeur utilisateur attendue

| Bénéficiaire | Valeur concrète |
|---|---|
| **Apprenant / visiteur** | Découvrir des parcours sans créer de compte et lire un témoignage dans de bonnes conditions. |
| **Lauréat** | Voir son article accessible publiquement dès qu'il est publié. |
| **Communauté Solicode** | Disposer d'un premier espace public de consultation, avant d'investir dans la contribution. |
| **Product Owner** | Valider la promesse la plus visible du produit avec un incrément démontrable. |

Le Sprint Goal ne promet **ni inscription, ni rédaction, ni modération** : il se concentre sur la **lecture publique**, qui est la valeur immédiatement démontrable.

### 3.3 Lien avec le Product Goal

La Vision Produit repose sur deux mouvements : **produire** un témoignage et **le rendre lisible**. Ce sprint livre le second mouvement, seul, de bout en bout. Il ne ferme pas encore la boucle complète du MVP (qui exige US-03, US-04 et US-06), mais il rend la promesse **visible et testable** par un utilisateur réel.

### 3.4 User Stories contributives

| ID | Titre | SP | Contribution au Sprint Goal |
|---|---|---|---|
| US-02 | Lire le détail d'un article | 5 | Délivre le contenu : titre, texte, auteur, catégorie, date, 404 maîtrisée. |
| US-01 | Consulter la liste des articles publiés | 3 | Rend le contenu découvrable et mène au détail. |
| | **Total** | **8** | |

### 3.5 Justification de la sélection

- **Cohérence de valeur** : les deux stories forment un parcours complet, de la découverte à la lecture. Aucune des deux ne suffit seule à démontrer la promesse.
- **Absence de dépendance bloquante** : ni US-01 ni US-02 ne requiert l'authentification, contrairement à US-03, US-04 et US-06.
- **Readiness** : US-02 est documentée (route, 404, responsive) et US-01 possède des critères d'acceptation testables ; les deux sont estimées et classées Must.
- **Taille maîtrisée** : 8 SP, soit le périmètre déjà proposé dans l'atelier Product Backlog, sans ajout de story.
- **Démonstrabilité** : l'incrément peut être montré en Sprint Review sans compte administrateur ni jeu de données complexe.

### 3.6 Ce que le Sprint Goal exclut explicitement

- La création de compte et la connexion (US-03).
- La rédaction, le brouillon et la soumission (US-04).
- La modération et la publication (US-06).
- Le suivi du statut (US-05), la recherche (US-07), la gestion des catégories (US-08).
- Les stories différées US-09 et US-10.

### 3.7 Critères de succès observables en Sprint Review

Sans affirmer que le sprint est exécuté, le succès se jugera ainsi :

1. La liste n'affiche **que** des articles publiés, avec titre, auteur, catégorie et date.
2. Un article publié s'ouvre via `/articles/{slug}` et affiche les cinq informations attendues.
3. Un slug inexistant ou un article non publié renvoie une **404** sans révéler le contenu.
4. La liste et le détail restent lisibles sur mobile et sur bureau, sans défilement horizontal.
5. L'état vide de la liste affiche un message explicite.
6. Les tests automatisés couvrant ces cas passent.

---

## 4. Sprint Backlog

### 4.1 Tableau de sélection

| ID | User Story | Valeur métier | MoSCoW | SP | Raison de la sélection |
|---|---|---|---|---|---|
| US-02 | Lire le détail d'un article | Élevée — cœur de la promesse | Must | 5 | Délivre le contenu et la valeur finale du parcours public. |
| US-01 | Consulter la liste des articles publiés | Élevée — point d'entrée | Must | 3 | Rend les articles découvrables et alimente le détail. |
| | **Total Sprint Backlog** | | | **8** | |

> Les estimations **5 SP et 3 SP sont reprises sans modification** de l'atelier Product Backlog. Aucune ré-estimation n'est proposée.

### 4.2 US-02 — Lire le détail d'un article

| Champ | Valeur |
|---|---|
| **ID** | US-02 |
| **Titre** | Lire le détail d'un article |
| **Acteur** | Apprenant / visiteur (persona Salma) |
| **MoSCoW** | Must Have |
| **Story Points** | 5 SP (inchangés) |
| **Origine** | Atelier Vision/Besoins ; documentée comme livrée au Sprint 1 |

**User Story complète** : *En tant qu'apprenante, je veux lire le détail d'un article afin de comprendre le parcours et les conseils d'un lauréat.*

**Valeur métier** : c'est le cœur de la promesse produit. L'article est le contenu qui transmet l'expérience et crée l'utilité pour l'apprenante.

**Critères d'acceptation** :
- **Étant donné** un article publié identifié par son slug, **quand** j'ouvre l'URL `/articles/{slug}`, **alors** le titre, le contenu, l'auteur, la catégorie et la date de publication sont affichés.
- **Étant donné** un slug inexistant ou un article non publié, **quand** j'ouvre son URL, **alors** une page d'erreur 404 est affichée et aucun contenu de l'article n'est révélé.
- **Étant donné** un écran mobile ou de bureau, **quand** je lis l'article, **alors** le contenu reste lisible sans défilement horizontal.

**Raison de la sélection** : story de référence du backlog (5 SP), elle constitue la valeur finale du parcours public et son périmètre est documenté dans `rapport/chapitres/17 - Réalisation.md`. Elle est déjà engagée dans le Sprint 1 documenté.

### 4.3 US-01 — Consulter la liste des articles publiés

| Champ | Valeur |
|---|---|
| **ID** | US-01 |
| **Titre** | Consulter la liste des articles publiés |
| **Acteur** | Apprenant / visiteur (persona Salma) |
| **MoSCoW** | Must Have |
| **Story Points** | 3 SP (inchangés) |
| **Origine** | Atelier Vision/Besoins |

**User Story complète** : *En tant qu'apprenante, je veux consulter la liste des articles publiés afin de découvrir les parcours des lauréats et choisir ceux qui m'intéressent.*

**Valeur métier** : la liste est le point d'entrée du blog. Sans elle, les articles existent mais restent difficiles à découvrir.

**Critères d'acceptation** :
- **Étant donné** des articles publiés et des articles en brouillon, **quand** j'ouvre la page de liste, **alors** seuls les articles publiés sont affichés, avec leur titre, leur auteur, leur catégorie et leur date de publication.
- **Étant donné** la liste affichée, **quand** je sélectionne un article, **alors** je suis dirigé vers la page de détail correspondante.
- **Étant donné** qu'aucun article n'est publié, **quand** j'ouvre la liste, **alors** un message explicite indique qu'aucun article n'est disponible.

**Raison de la sélection** : point d'entrée du produit, aucune dépendance d'authentification, readiness élevée. Elle transforme US-02 en parcours découvrable.

**Hypothèse de mise en œuvre à valider** : tri par date de publication décroissante et absence de pagination pour un volume initial faible. Ces choix ne figurent pas dans les critères d'acceptation ; ils doivent être confirmés au Sprint Planning.

### 4.4 Vérification de la Definition of Ready

La DoR utilisée est celle proposée dans l'atelier Product Backlog (11 critères). Elle n'a pas été formellement adoptée.

| # | Critère DoR | US-02 | US-01 |
|---|---|---|---|
| 1 | Format et acteur identifiés | OK | OK |
| 2 | Besoin et valeur explicites | OK | OK |
| 3 | Critères d'acceptation testables | OK | OK |
| 4 | Périmètre délimité | OK | **OK avec hypothèse** (tri, pagination) |
| 5 | Dépendances identifiées | OK — aucune | OK — aucune |
| 6 | Estimation Fibonacci | 5 SP | 3 SP |
| 7 | Priorité MoSCoW | Must | Must |
| 8 | Taille ≤ 8 SP | OK | OK |
| 9 | Ressources disponibles | **Réserve** — code absent du dépôt | OK — modèle et AC documentés |
| 10 | Contraintes non fonctionnelles | Responsive, 404, sécurité d'affichage | Responsive, état vide |
| 11 | Validation du Product Owner | **À confirmer** | **À confirmer** |

**Traitement des réserves** :

- **US-02, ressource** : la story est **prête pour la planification**, mais la première micro-tâche (T-01) vérifie l'existence et la conformité de l'implémentation. Si le code est déjà conforme, T-01 à T-04 deviennent des tâches de vérification et de consolidation ; toute réduction d'effort serait alors une **proposition de ré-estimation**, pas un acquis.
- **US-01, périmètre** : l'hypothèse de tri et d'absence de pagination est consignée ; elle ne bloque pas le démarrage, car les critères d'acceptation n'en dépendent pas.
- **Validation PO** : les deux stories restent des propositions tant que le Groupe 1 ne les a pas marquées « Prêtes ».

**Conséquence de planification** : si le Product Owner confirme que US-02 est déjà livrée et conforme, le Sprint Backlog se réduit à **US-01 (3 SP)** et T-01 à T-04 deviennent des **vérifications de non-régression**. Cette réduction est une proposition, pas une décision acquise.

### 4.5 Stories non sélectionnées et raisons

| ID | SP | MoSCoW | État de préparation | Raison de la non-sélection |
|---|---|---|---|---|
| US-03 | 5 | Must | Partiellement prête — mécanisme d'authentification non tranché | Habilite la contribution, mais élargit le Sprint Goal et ajoute 5 SP ; à planifier avec US-04. |
| US-04 | 8 | Must | **Non prête** — statut « en attente » non validé, type d'éditeur non spécifié | Dépend de US-03 ; l'incertitude empêche un découpage fiable en tâches de 1 à 3 h. |
| US-05 | 3 | Should | Non prête — dépend de US-03, US-04 et US-06 | Aucun statut réel à afficher tant que le workflow de contribution n'existe pas. |
| US-06 | 5 | Must | **Non prête** — rôle administrateur non documenté, statut à valider | Dépend de US-04 ; sans contribution, la file de modération serait vide. |
| US-07 | 5 | Could | Estimée, hors objectif — dépend de US-08 | Recherche et filtres non nécessaires à un volume initial faible. |
| US-08 | 3 | Could | Proposée, hors objectif | Un référentiel de catégories initial suffit. |
| US-09 | 5 | Won't | Différée | Modification/suppression hors périmètre actuel. |
| US-10 | 5 | Won't | Différée | Profil public hors périmètre actuel. |

> **Règle appliquée** : une story non prête n'est pas intégrée « pour remplir » le sprint. US-04 et US-06 restent au backlog jusqu'à ce que les décisions manquantes soient prises.

### 4.6 Total du Sprint Backlog

| Indicateur | Valeur |
|---|---|
| Stories | 2 |
| Story Points | **8 SP** |
| Micro-tâches | 8 |
| Heures estimées | **14 h** |
| Dépendances externes | Aucune (hors état de la base et de la branche) |

---

## 5. Découpage en micro-tâches techniques

### 5.1 Règle d'or du découpage

Une micro-tâche doit respecter quatre conditions :

1. **Durée courte** : entre **1 et 3 heures**. Au-delà, elle est découpée ; en dessous, elle est probablement fusionnable.
2. **Actionnable** : elle commence par un verbe concret et produit un résultat vérifiable.
3. **Testable** : elle inclut, quand c'est pertinent, l'écriture ou l'exécution d'un test.
4. **Traçable** : elle est rattachée à une User Story et à un critère d'acceptation.

Chaque story est découpée en **4 micro-tâches**, conformément à la fourchette de 2 à 4 attendue.

### 5.2 US-02 — Découpage technique

| Task ID | Related User Story | Technical Task | Description | Estimated Duration |
|---|---|---|---|---|
| T-01 | US-02 | Vérifier la route et le contrôleur du détail | Contrôler la route GET `/articles/{slug}`, la méthode de `ArticleController` et la délégation à `ArticleService` ; consigner tout écart avec l'architecture 2 couches. | 1 h |
| T-02 | US-02 | Implémenter la récupération d'un article publié | Dans `ArticleService`, récupérer l'article par `slug` en filtrant sur le statut publié ; déclencher une 404 si l'article est absent ou non publié. | 2 h |
| T-03 | US-02 | Finaliser la vue Blade du détail | Afficher titre, contenu, auteur, catégorie et date de publication ; mise en page responsive Tailwind/Preline ; échappement des contenus. | 2 h |
| T-04 | US-02 | Tester le détail et les cas d'erreur | Écrire et exécuter les tests feature : article publié affiché, slug inexistant → 404, brouillon → 404, absence de débordement horizontal. | 2 h |
| | | **Total US-02** | | **7 h** |

### 5.3 Justification des durées — US-02

| Task ID | Justification de l'estimation |
|---|---|
| T-01 | Vérification ciblée de fichiers et de conventions déjà documentés, sans nouvelle logique métier. |
| T-02 | Une requête Eloquent, une règle de statut, une gestion de 404 et le câblage du service : périmètre court mais avec un cas négatif. |
| T-03 | Cinq informations à afficher, une mise en page responsive et une vérification visuelle sur deux tailles d'écran. |
| T-04 | Quatre cas de test, dont deux cas d'erreur, avec écriture, exécution et correction éventuelle. |

### 5.4 US-01 — Découpage technique

| Task ID | Related User Story | Technical Task | Description | Estimated Duration |
|---|---|---|---|---|
| T-05 | US-01 | Déclarer la route et la méthode de liste | Ajouter la route GET de la liste et une méthode mince dans le contrôleur, déléguant le traitement à `ArticleService`. | 1 h |
| T-06 | US-01 | Implémenter la liste des articles publiés | Dans `ArticleService`, filtrer sur le statut publié, charger l'auteur et la catégorie, trier par date de publication décroissante (hypothèse à valider). | 2 h |
| T-07 | US-01 | Créer la vue Blade de liste et l'état vide | Afficher titre, auteur, catégorie et date ; ajouter le lien vers `/articles/{slug}` ; prévoir le message d'état vide ; rendre la liste responsive. | 2 h |
| T-08 | US-01 | Tester la liste et l'état vide | Écrire et exécuter les tests feature : seuls les publiés apparaissent, les brouillons sont exclus, l'état vide s'affiche, le lien mène au détail. | 2 h |
| | | **Total US-01** | | **7 h** |

### 5.5 Justification des durées — US-01

| Task ID | Justification de l'estimation |
|---|---|
| T-05 | Ajout d'une route et d'une méthode de contrôleur mince, sans logique métier. |
| T-06 | Requête filtrée, chargement de deux relations, tri proposé et exclusion explicite des brouillons. |
| T-07 | Quatre informations par article, un état vide, un lien de navigation et une mise en page responsive. |
| T-08 | Quatre cas de test, dont l'état vide et l'exclusion des brouillons, avec exécution. |

### 5.6 Totaux

| Périmètre | Story Points | Micro-tâches | Heures estimées |
|---|---|---|---|
| US-02 | 5 | 4 | 7 h |
| US-01 | 3 | 4 | 7 h |
| **Sprint Backlog** | **8** | **8** | **14 h** |

### 5.7 Story Points et heures ne se confondent pas

Les 8 SP expriment la **taille relative** des deux stories. Les 14 h expriment une **estimation opérationnelle des micro-tâches**. Il n'existe aucune règle de conversion entre les deux : le rapport observé (8 SP / 14 h) est propre à ce découpage et ne doit pas être réutilisé comme formule.

Les heures sont des **estimations initiales de planification**, pas des heures travaillées. Elles seront ajustées si le Sprint Planning révèle une capacité différente ou si US-02 s'avère déjà implémentée.

---

## 6. Tableau Kanban et limites WIP

### 6.1 Colonnes et règles d'entrée/sortie

| Colonne | Objectif | Une tâche peut y entrer quand… | Elle en sort quand… |
|---|---|---|---|
| **À faire** | Visualiser le Sprint Backlog ordonné | Elle est sélectionnée au Sprint Planning et satisfait la DoR | Le développeur la tire et une place WIP est disponible |
| **En cours** | Concentrer le travail actif | La limite « En cours » n'est pas atteinte | Le code est complet, l'auto-contrôle est fait et les tests sont écrits |
| **En test / Review** | Vérifier la qualité avant de déclarer terminé | L'implémentation et les tests sont prêts | Les critères d'acceptation sont vérifiés, les tests passent, la revue est faite et la DoD est satisfaite |
| **Terminé** | Rendre visible l'incrément | La DoD est satisfaite et la modification est intégrée sur `sprint1` | Le PO accepte en Sprint Review, ou la story est rouverte en cas de défaut |

**Règles de flux** :

1. **Tirer de la droite vers la gauche** : on termine ou on fait avancer une tâche avant d'en démarrer une nouvelle.
2. **Aucun saut de colonne** : une tâche ne passe pas directement de « À faire » à « Terminé ».
3. **Une seule tâche active par développeur** : la limite « En cours » l'impose.
4. **« Terminé » signifie DoD satisfaite**, pas « code écrit ».
5. **Une tâche bloquée reste dans sa colonne**, marquée `Bloqué` ; elle continue d'occuper sa place WIP.

### 6.2 Pourquoi un marqueur « Bloqué » plutôt qu'une colonne

Une colonne « Bloqué » donnerait l'illusion que le travail a avancé et masquerait la pression sur le flux. Le marqueur conserve la tâche à l'endroit où elle est réellement, compte dans le WIP et rend le blocage visible au Daily Scrum.

Chaque blocage doit indiquer :

- la **cause** (technique, décision, accès, donnée) ;
- le **responsable du déblocage** ;
- la **prochaine action** et son **délai** ;
- la **date de début** du blocage.

### 6.3 Limites WIP proposées

| Colonne | Limite proposée | Justification |
|---|---|---|
| **À faire** | Pas de limite | File ordonnée par dépendances ; la limiter n'apporterait pas de valeur. |
| **En cours** | **1** | Projet individuel : une seule tâche active évite le changement de contexte et rend l'avancement lisible. |
| **En test / Review** | **2** | Permet au développeur de préparer la suite pendant que l'encadrant relit, sans accumuler davantage. |
| **Terminé** | Pas de limite | La colonne reflète l'incrément validé. |

> **Statut** : ces limites sont des **propositions**. La taille et la capacité de l'équipe ne sont pas documentées ; elles doivent être validées au Sprint Planning. Si l'équipe s'avère plus nombreuse, la limite « En cours » pourra être relevée, mais jamais sans justification.

**Quand une limite est atteinte** :

1. On **ne démarre pas** de nouvelle tâche.
2. On **finit** ce qui est en cours ou on aide à faire avancer la revue.
3. Si une tâche est bloquée au-delà du timebox, le facilitateur peut autoriser **explicitement** le démarrage d'une tâche indépendante ; la dérogation est tracée et levée dès le déblocage.
4. Si le blocage persiste, il est escaladé au PO ou à l'encadrant ; le Sprint Goal est réévalué, pas contourné en silence.

### 6.4 Visualisation du tableau — simulation de planification

> **Instantané de simulation**, au moment du Daily Scrum de la section 8. Il ne représente **pas l'état réel** d'un sprint exécuté.

| À faire (5) | En cours (1/1) | En test / Review (1/2) | Terminé |
|---|---|---|---|
| **T-04** Tests du détail — 2 h — US-02<br/>**T-05** Route liste — 1 h — US-01<br/>**T-06** Service liste — 2 h — US-01<br/>**T-07** Vue liste — 2 h — US-01<br/>**T-08** Tests liste — 2 h — US-01 | **T-03** Vue Blade détail — 2 h — US-02<br/>`Bloqué` : colonne `publie_le` absente | **T-02** Service détail — 2 h — US-02 | **T-01** Vérification route — 1 h — US-02 |

**Lecture** : une tâche terminée, une en revue, une en cours mais bloquée, cinq encore à faire. Le WIP est respecté (1/1 et 1/2), mais le blocage de T-03 menace la suite de US-02.

---

## 7. Daily Scrum

### 7.1 Objectif

Le Daily Scrum est une **inspection quotidienne de la progression vers le Sprint Goal**, suivie d'une **adaptation du plan de travail**. Ce n'est pas un rapport hiérarchique, ni une réunion de résolution de problèmes.

### 7.2 Organisation

| Élément | Proposition |
|---|---|
| **Durée** | **15 minutes maximum** |
| **Fréquence** | Chaque jour ouvré, à une heure fixe décidée par l'équipe |
| **Format** | Debout, même lieu ou même canal, Sprint Goal et Kanban visibles |
| **Participants** | Développeur(s) ; facilitateur (rôle non nominativement attribué dans le dépôt) ; PO optionnel ; observateurs silencieux |
| **Sortie** | Kanban à jour, blocages identifiés avec responsable et prochaine action, plan de la journée |
| **Après la réunion** | Les discussions techniques approfondies se tiennent hors du Daily, avec les personnes concernées |

### 7.3 Les trois questions rituelles

1. **Qu'est-ce que j'ai réalisé depuis le dernier Daily Scrum ?**
2. **Qu'est-ce que je prévois de faire ensuite ?**
3. **Quels obstacles ou blocages rencontrés ?**

Chaque réponse est reliée à une tâche du Kanban et, si possible, au Sprint Goal. Une réponse du type « j'ai avancé sur le projet » n'est pas exploitable : elle doit nommer la tâche et son état.

> **Précision** : ces trois questions sont un **format de facilitation pratique**. Le Scrum Guide ne les impose pas mot pour mot ; l'équipe peut les adapter tant que l'inspection et l'adaptation restent au centre.

### 7.4 Règles de facilitation

- Le facilitateur **timeboxe** chaque intervention et garantit que le Sprint Goal reste le fil conducteur.
- Un blocage est **noté**, pas résolu pendant la réunion ; il reçoit un responsable et une prochaine action.
- Le Kanban est mis à jour **avant ou pendant** le Daily, pas après.
- Si une tâche est bloquée, elle est marquée `Bloqué` et reste visible dans sa colonne.
- Le Daily ne sert pas à détailler les solutions techniques : un « parking » est ouvert après la réunion.

### 7.5 Adaptation au projet individuel

Le projet est individuel. Le Daily peut donc réunir le développeur et le facilitateur (encadrant), avec le PO en point d'étape. Il reste utile :

- il force une **revue quotidienne du Kanban** ;
- il rend les blocages visibles avant qu'ils ne consomment la fin de sprint ;
- il documente les décisions et les dérogations WIP.

Même sans blocage, le créneau de 15 minutes est maintenu : c'est un rituel de pilotage, pas une réunion exceptionnelle.

---

## 8. Simulation d'un blocage technique

### 8.1 Nature de la simulation

> **Simulation hypothétique.** Le dépôt ne contient ni code source ni base de données. Le blocage décrit ci-dessous est **réaliste au regard de la stack documentée** (Laravel, MySQL, Eloquent, migrations) et du diagramme de classes (`publieLe`), mais il n'est **pas observé** dans le dépôt.

**Scénario** : lors de la finalisation de la vue Blade du détail (T-03), le développeur constate une erreur SQL :

```text
SQLSTATE[42S22]: Column not found: 1054 Unknown column 'publie_le' in 'order clause'
```

La colonne de date de publication n'existe pas dans la base locale : une migration est absente ou n'a pas été appliquée.

### 8.2 Daily Scrum simulé

| Participant | Hier / Progression | Aujourd'hui / Prochaine action | Blocage |
|---|---|---|---|
| **Développeur** — Marwan bouhamid | T-01 terminé : route et contrôleur vérifiés. T-02 envoyé en revue. | Finaliser T-03 (vue Blade du détail), puis T-04 (tests). | Erreur SQL `Unknown column 'publie_le'` à l'ouverture du détail ; la date de publication ne peut pas être affichée. |
| **Facilitateur / Scrum Master** — rôle non nominativement attribué | Suivi du Kanban : WIP respecté (1/1, 1/2). | Timeboxer le diagnostic, mesurer l'impact sur le Sprint Goal, organiser l'appui de l'encadrant. | Suivi du blocage ; décision si le timebox d'une heure est dépassé. |
| **Product Owner** — Groupe 1 | Aucun changement de priorité demandé. | Confirmer que la date de publication reste obligatoire dans l'affichage. | Aucun blocage fonctionnel : la correction du schéma relève de l'équipe. |

### 8.3 Impact sur le Sprint Goal

| Élément impacté | Effet |
|---|---|
| **US-02, AC n° 1** | La date de publication ne peut pas être affichée : le critère n'est pas satisfait. |
| **US-02, T-04** | Les tests du détail échouent ou ne peuvent pas être écrits complètement. |
| **US-01, T-06** | Le tri par date de publication sera bloqué par la même colonne absente. |
| **Sprint Goal** | La lecture reste possible en partie, mais l'incrément n'est pas conforme aux critères d'acceptation. Le Sprint Goal est **menacé**, pas encore perdu. |
| **Valeur produit** | Un article sans date reste lisible, mais la promesse de traçabilité des parcours est dégradée. |

**Gravité** : élevée pour le sprint, moyenne pour le produit. Le blocage est technique et réparable ; il ne remet pas en cause le périmètre.

### 8.4 Plan de résolution

| Étape | Action | Responsable | Délai (timebox) |
|---|---|---|---|
| 1 | Diagnostiquer : `php artisan migrate:status`, puis inspecter les colonnes de la table `articles`. | Développeur | 15 min |
| 2 | Si la migration existe mais n'est pas appliquée : l'exécuter. Si elle est absente : créer une migration ajoutant `publie_le` (nullable), puis l'exécuter. | Développeur | 30 min |
| 3 | Rejouer les tests de T-04 et vérifier l'affichage du détail et de la liste. | Développeur | 20 min |
| 4 | Mettre à jour le Kanban : retirer le marqueur `Bloqué`, déplacer T-03 vers « En test / Review ». | Développeur + facilitateur | 10 min |
| 5 | Si le blocage persiste au-delà d'une heure : arrêter, solliciter l'encadrant et décider soit d'un appui, soit d'une dérogation WIP pour démarrer T-05 (indépendante). | Facilitateur + encadrant | 15 min |

**Responsable du suivi** : le facilitateur.  
**Prochaine action** : le développeur exécute l'étape 1 immédiatement après le Daily et rend compte à l'étape suivante.  
**Prochain point** : Daily suivant, ou point court si le blocage est levé avant.

### 8.5 Prévention

1. **Vérifier le schéma au Sprint Planning** : comparer les migrations avec le diagramme de classes (`statut`, `publieLe`, `slug`).
2. **Ajouter « migrations à jour » à la checklist de démarrage** et à la DoD (le critère 12 de la DoD proposée le prévoit déjà).
3. **Exécuter les tests avant de passer en revue**, pas après.
4. **Ne jamais corriger la base manuellement** : toute correction passe par une migration versionnée.
5. **Consigner le blocage** dans le Kanban et dans le compte rendu du Daily, même après résolution.

### 8.6 Ce que la simulation démontre

- Le Daily Scrum **révèle** le blocage au lieu de le laisser caché.
- Le blocage est **qualifié** (cause, impact, gravité) avant d'être résolu.
- La résolution a un **responsable**, un **timebox** et une **prochaine action**.
- Le WIP est **protégé** : on ne démarre pas une nouvelle tâche sans décision explicite.
- Le Sprint Goal est **réévalué**, pas contourné.

---

## 9. Pilotage et suivi du sprint

### 9.1 Indicateurs proposés

| Indicateur | Ce qu'il mesure | Fréquence | Source |
|---|---|---|---|
| **Heures restantes estimées** | Effort restant sur les micro-tâches non terminées | Après chaque Daily | Kanban |
| **Respect du WIP** | Nombre de tâches en cours et en revue vs limites | Après chaque Daily | Kanban |
| **Blocages ouverts** | Nombre, âge et responsable des blocages | Après chaque Daily | Kanban + Daily |
| **Conformité DoD** | Tâches en « Terminé » satisfaisant réellement la DoD | À chaque passage en Terminé | Revue + tests |
| **Couverture des AC** | Chaque critère d'acceptation possède au moins un test | Avant la Sprint Review | Tests + revue |

Aucune **vélocité** n'est calculée : le projet n'a pas d'historique de sprints terminés. Aucun **burndown calendaire** n'est produit : la durée du sprint n'est pas fixée.

### 9.2 Instantané de suivi — simulation

| Périmètre | SP | Heures initiales | Terminé (DoD) | Restant | Tâches terminées |
|---|---|---|---|---|---|
| US-02 | 5 | 7 h | 1 h (T-01) | 6 h | 1 / 4 |
| US-01 | 3 | 7 h | 0 h | 7 h | 0 / 4 |
| **Total** | **8** | **14 h** | **1 h** | **13 h** | **1 / 8** |

**Lecture** : T-02 est en revue mais **n'est pas comptée terminée** tant que la DoD n'est pas satisfaite. T-03 est bloquée et conserve ses 2 h restantes. Cet instantané est une **simulation**, pas un relevé d'heures travaillées.

### 9.3 Règles de mise à jour

- Le Kanban est mis à jour **au moins une fois par jour**, avant le Daily.
- Une tâche ne passe en « Terminé » que si la DoD est vérifiée.
- Un blocage est daté et doté d'un responsable dès qu'il est signalé.
- Toute dérogation WIP est consignée avec sa justification et sa durée.
- Les heures restantes sont réestimées si une tâche révèle un périmètre différent ; l'écart est expliqué.

### 9.4 Lien avec la Sprint Review

La Sprint Review (atelier suivant) vérifiera l'incrément par rapport au Sprint Goal et aux critères d'acceptation. Le pilotage de ce document prépare cette revue : il ne la remplace pas et ne préjuge pas de son résultat.

---

## 10. Risques, hypothèses et points à valider

| # | Risque / hypothèse | Impact | Mitigation proposée | Responsable |
|---|---|---|---|---|
| 1 | Durée du sprint non définie | Planification calendaire impossible | Décider de la durée au Sprint Planning ; le plan reste exprimé en scope et en heures de tâches | PO + équipe |
| 2 | Capacité et disponibilité inconnues | Les 14 h ne sont pas un engagement | Valider la capacité avant de confirmer le Sprint Backlog | PO + équipe |
| 3 | US-02 documentée livrée mais code absent | T-01 à T-04 peuvent être plus légères ou déjà faites | Vérifier l'implémentation en T-01 ; toute réduction est une proposition de ré-estimation | Développeur + PO |
| 4 | Tri et pagination de la liste non spécifiés | Ambiguïté de mise en œuvre | Hypothèse : tri par date décroissante, pas de pagination ; valider au Planning | PO |
| 5 | Schéma MySQL désaligné avec le diagramme de classes | Blocage de type `publie_le` | Contrôle des migrations au Planning ; correction par migration versionnée | Développeur |
| 6 | Processus de revue non formalisé | Qualité inégale | Revue par l'encadrant ou un pair avant fusion ; à formaliser | Équipe |
| 7 | Branche `sprint0` au lieu de `sprint1` | Travail sur une mauvaise base | Vérifier la branche avant la première tâche | Développeur |
| 8 | Projet individuel : facteur de bus | Blocage en cas d'absence | Documentation, revue par l'encadrant, commits réguliers | Équipe |
| 9 | US-03, US-04 et US-06 non prêtes | Le MVP ne peut pas avancer au sprint suivant sans raffinement | Raffiner le statut « en attente » et le rôle administrateur avant le prochain Planning | PO + équipe |
| 10 | Aucune CI documentée | Tests exécutés manuellement | Exécuter la suite localement avant chaque passage en revue | Développeur |

---

## 11. Conclusion

Le plan proposé tient en une phrase : **livrer un parcours public de lecture, de la liste au détail, en 8 Story Points et 8 micro-tâches de 14 heures estimées.**

Les points structurants sont les suivants :

- **Sprint Goal** : rendre le blog publiquement utile par la découverte et la lecture des articles publiés.
- **Sprint Backlog** : US-02 (5 SP) + US-01 (3 SP), repris du backlog sans modification d'estimation.
- **Découpage** : 4 tâches par story, toutes entre 1 et 2 heures, avec tests intégrés.
- **Kanban** : quatre colonnes, flux tiré, marqueur `Bloqué`, WIP proposé à 1 en cours et 2 en revue.
- **Daily Scrum** : 15 minutes, trois questions, inspection du Sprint Goal et escalade des blocages.
- **Blocage simulé** : colonne `publie_le` absente, diagnostiquée et traitée par migration versionnée, avec responsable et timebox.

Les limites sont explicites : aucune exécution réelle n'est rapportée, aucune durée de sprint ni capacité n'est inventée, et les décisions de périmètre restent au Product Owner.

---

## 12. Sources, traçabilité et checklist de validation

### 12.1 Documents inspectés

| Source | Informations utilisées |
|---|---|
| `README.md` | Stack Laravel/MySQL/Blade, architecture 2 couches, organisation. |
| `docs/cadrage/note-cadrage.md` | Product Owner, périmètre, contraintes, accessibilité, risques. |
| `docs/cadrage/stack-technique.md` | Sécurité, responsive, tests PHPUnit/Pest, NativePHP. |
| `sprints/sprints.md` | Sprint 1 actif, objectif, branche `sprint1`, US-02 documentée livrée. |
| `sprints/readme.md` | Gouvernance des sprints, branche `sprint[N]`. |
| `tutoriels/scrum/initiation-scrum/vision-besoins/vision-besoins.md` | US-01, US-02, critères d'acceptation, valeur, MVP. |
| `tutoriels/scrum/initiation-scrum/product-backlog/product-backlog.md` | Backlog, 5 SP / 3 SP, MoSCoW, DoR, DoD, sélection Sprint 1. |
| `tutoriels/scrum/initiation-scrum/product-backlog/presentation-product-backlog.md` | Cohérence des chiffres et conventions Marp. |
| `rapport/chapitres/13 - Diagramme de cas d’utilisation.md` | Cas de consultation de la liste et du détail. |
| `rapport/chapitres/15 - Diagramme de classes.md` | `Article`, `Laureat`, `Categorie`, `slug`, `statut`, `publieLe`. |
| `rapport/chapitres/17 - Réalisation.md` | `/articles/{slug}`, `ArticleController`, `ArticleService`, 404, MVC. |
| État Git | Branche courante `sprint0`, branches `sprint0`/`sprint1`/`main`, absence de code applicatif. |

### 12.2 Faits, hypothèses et simulations

| Élément | Statut |
|---|---|
| US-01 et US-02, AC, valeur, 5 SP et 3 SP | **Faits** repris des ateliers précédents. |
| Sélection Sprint 1 à 8 SP | **Proposition** de l'atelier Product Backlog, non validée par le PO. |
| Sprint 1 actif et US-02 livrée | **Documenté** dans `sprints/sprints.md`, non vérifiable sans code. |
| Découpage en 8 micro-tâches et 14 h | **Estimation de planification** proposée. |
| Colonnes Kanban et limites WIP 1/2 | **Proposition** à valider. |
| Blocage `publie_le` | **Simulation hypothétique**, réaliste mais non observée. |
| Instantané du Kanban et heures restantes | **Simulation**, pas un état réel. |
| Durée du sprint, capacité, vélocité | **Non définies** ; aucune valeur inventée. |

### 12.3 Checklist de validation de l'atelier

- [x] Sprint Goal clair, concis et orienté valeur.
- [x] Sprint Backlog sélectionné dans le backlog existant.
- [x] Stories complètes avec valeur, MoSCoW, SP, AC et justification.
- [x] DoR vérifiée ; stories non prêtes écartées avec explication.
- [x] 2 à 4 micro-tâches par story.
- [x] Chaque micro-tâche entre 1 et 3 heures, avec justification.
- [x] Totaux par story et pour le Sprint Backlog.
- [x] Story Points et heures distingués.
- [x] Colonnes Kanban avec règles d'entrée et de sortie.
- [x] Limites WIP justifiées et conduite en cas de saturation.
- [x] Tableau Kanban visualisé et identifié comme simulation.
- [x] Daily Scrum de 15 minutes avec les trois questions.
- [x] Blocage technique simulé, impacté, résolu avec responsable et suivi.
- [x] Aucune exécution de sprint affirmée.
- [x] Hypothèses et points à valider explicitement identifiés.
