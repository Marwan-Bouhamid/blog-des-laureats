---
marp: true
theme: default
paginate: true
size: 16:9
header: "Solicode N3 — Atelier Sprint Planning & Exécution"
footer: "Blog des Lauréats | Encadrant : ESSARRAJ Fouad"
style: |
  section {
    font-family: Arial, sans-serif;
    background: #ffffff;
    color: #1f2937;
    padding: 44px 62px;
  }

  section h1 {
    font-size: 37px;
    color: #0338ab;
  }

  section h2 {
    color: #2563eb;
  }

  section h3 {
    color: #0338ab;
    margin: 0 0 6px;
    font-size: 20px;
  }

  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
  }

  section.lead h1 {
    font-size: 48px;
    margin-bottom: 4px;
  }

  section.lead h3 {
    font-size: 23px;
    font-weight: normal;
    color: #2563eb;
    margin: 0 0 22px;
  }

  ul, ol {
    line-height: 1.38;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 19px;
  }

  th {
    background: #e8efff;
    color: #0338ab;
    text-align: left;
  }

  th, td {
    border: 1px solid #cbd5e1;
    padding: 5px 9px;
    vertical-align: top;
  }

  .small {
    font-size: 17px;
    color: #475569;
  }

  .quote {
    border-left: 5px solid #2563eb;
    background: #f1f5ff;
    padding: 10px 16px;
    font-size: 20px;
    font-style: italic;
    margin-top: 12px;
  }

  .two {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
    margin: 6px 0 14px;
  }

  .box {
    background: #f8fafc;
    border: 1px solid #dbe4f0;
    border-radius: 10px;
    padding: 10px 14px;
    font-size: 17px;
  }

  .box ul {
    margin: 5px 0 0;
    padding-left: 18px;
  }

  .box li {
    margin-bottom: 5px;
  }

  .compact table {
    font-size: 15.5px;
  }

  .compact th, .compact td {
    padding: 3px 6px;
  }

  .kanban {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 9px;
    margin-top: 10px;
  }

  .kcol {
    background: #f8fafc;
    border: 1px solid #dbe4f0;
    border-radius: 8px;
    padding: 7px;
    min-height: 330px;
  }

  .kcol h3 {
    font-size: 15px;
    margin: 0 0 8px;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .wip {
    font-size: 11px;
    background: #e8efff;
    color: #0338ab;
    border-radius: 10px;
    padding: 1px 6px;
  }

  .kcard {
    background: #ffffff;
    border: 1px solid #cbd5e1;
    border-left: 4px solid #2563eb;
    border-radius: 6px;
    padding: 5px 7px;
    margin-bottom: 6px;
    font-size: 12.5px;
    line-height: 1.25;
  }

  .kcard strong {
    color: #0338ab;
  }

  .kmeta {
    color: #64748b;
    font-size: 10.5px;
  }

  .blocked {
    border-left-color: #dc2626;
    background: #fef2f2;
  }

  .btag {
    color: #b91c1c;
    font-size: 10.5px;
    font-weight: bold;
  }

  .done {
    border-left-color: #16a34a;
  }

  .goal {
    border-left: 6px solid #0338ab;
    background: #eef4ff;
    padding: 18px 22px;
    font-size: 25px;
    font-weight: bold;
    color: #0338ab;
    line-height: 1.35;
    margin: 18px 0;
  }

  section.blank {
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    background: #111827;
    color: white;
  }

  section.blank h1 {
    font-size: 50px;
    color: white;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Planifier, découper et piloter un Sprint

### Blog des Lauréats — du Sprint Goal au Daily Scrum

- **Atelier** : UA.351.11 — Initiation à la démarche Agile et cadre Scrum
- **Apprenant** : Marwan bouhamid
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Date** : 26 novembre 2026

<!--
Présenter l'atelier : il transforme la sélection du Product Backlog en plan de sprint opérationnel.
Annoncer le fil : Sprint Goal, Sprint Backlog, micro-tâches, Kanban, Daily Scrum, blocage.
-->

---

# Objectifs de l'atelier

- **Formuler** un Sprint Goal clair, concis et orienté valeur.
- **Sélectionner** un Sprint Backlog cohérent avec le Product Backlog.
- **Découper** chaque story en micro-tâches de 1 à 3 heures.
- **Structurer** un Kanban avec colonnes, règles de flux et limites WIP.
- **Animer** un Daily Scrum de 15 minutes et traiter un blocage technique.

<p class="small">Cas pratique : Sprint 1 proposé du Blog des Lauréats — US-02 + US-01, 8 Story Points, 8 micro-tâches, 14 heures estimées.</p>

<!--
Insister sur la différence avec l'atelier précédent : ici, on passe du backlog à l'organisation quotidienne.
Tout est traçable dans la fiche technique et dans les ateliers Vision/Product Backlog.
-->

---

# Point de départ : du backlog au sprint

| Élément | Valeur | Source |
|---|---|---|
| User Stories analysées | 10 (US-01 à US-10) | Atelier Product Backlog |
| Effort total du backlog | 47 SP (dont différés) | Atelier Product Backlog |
| Périmètre MVP | 5 stories — 26 SP | Atelier Product Backlog |
| **Sélection Sprint 1** | **US-02 + US-01 — 8 SP** | Atelier Product Backlog, section 10 |
| Vélocité connue | **Aucune** | Aucun sprint terminé documenté |
| Durée de sprint fixée | **Aucune** | Non documentée |

<p class="small">Le plan est exprimé en scope (8 SP) et en heures de micro-tâches (14 h), jamais en jours calendaires inventés.</p>

<!--
Rappeler que le backlog contient 10 stories, mais que le sprint n'en prend que deux.
Un sprint n'absorbe pas le MVP : 8 SP contre 26 SP.
-->

---

# Statut du document : simulation de planification

<div class="two">
<div class="box">

### Ce que le dépôt documente

- Sprint 1 **actif** dans `sprints/sprints.md`
- US-02 présentée comme **livrée**
- Branche `sprint1` déclarée
- Architecture : contrôleur mince → `ArticleService`

</div>
<div class="box">

### Ce que le dépôt ne permet pas de vérifier

- **Aucun code Laravel** dans le dépôt
- Aucune base de données
- Aucune vélocité, aucune capacité
- Aucune durée de sprint

</div>
</div>

<p class="quote">Ce diaporama ne rapporte aucune exécution réelle. Il propose un plan, un découpage et une simulation de Daily Scrum.</p>

<p class="small">Prérequis : vérifier la branche de travail (`sprint1` selon la documentation, `sprint0` actuellement).</p>

<!--
Être transparent dès le départ : le code est absent, donc l'état réel de US-02 n'est pas vérifiable.
Les tâches T-01 à T-04 sont une vérification/consolidation, pas une affirmation que tout reste à faire.
-->

---

# Sprint Goal

<div class="goal">
Rendre le blog publiquement utile : permettre à un apprenant ou à un visiteur de découvrir la liste des articles publiés et d'en lire le détail confortablement, sur mobile comme sur ordinateur.
</div>

- **Pour qui ?** L'apprenant ou le visiteur qui cherche un parcours concret.
- **Quel bénéfice ?** Découvrir sans compte et lire dans de bonnes conditions.
- **Quel périmètre ?** US-02 (détail) + US-01 (liste), soit 8 SP.
- **Ce que le goal exclut ?** Inscription, rédaction, modération, recherche, profils.

<p class="small">Un seul objectif, deux stories complémentaires : la liste rend l'article découvrable, le détail délivre le contenu.</p>

<!--
Lire le Sprint Goal lentement. Vérifier qu'il tient en une phrase et qu'il ne liste pas des tâches techniques.
Il doit pouvoir être compris par le Product Owner sans lire le backlog.
-->

---

# Valeur attendue et lien avec la Vision

| Bénéficiaire | Valeur concrète |
|---|---|
| **Apprenant / visiteur** | Découvrir des parcours et lire un témoignage sans créer de compte |
| **Lauréat** | Voir son article accessible publiquement dès qu'il est publié |
| **Communauté Solicode** | Disposer d'un premier espace public de consultation |
| **Product Owner** | Valider la promesse la plus visible avec un incrément démontrable |

**Lien avec la Vision Produit** : la vision promet des articles **lisibles et découvrables**. Ce sprint livre cette moitié de la promesse, avant la contribution et la modération.

<p class="small">Le dépôt ne formalise pas de Product Goal distinct ; la Vision Produit en tient lieu.</p>

<!--
Ne pas prétendre que le MVP est terminé : il manque US-03, US-04 et US-06.
Ce sprint rend la promesse visible et testable, il ne ferme pas la boucle complète.
-->

---

# Sprint Backlog

<div class="compact">

| ID | User Story | Valeur métier | MoSCoW | SP | Raison |
|---|---|---|---|---|---|
| US-02 | Lire le détail d'un article | Élevée — cœur de la promesse | Must | 5 | Délivre le contenu et la valeur finale |
| US-01 | Consulter la liste des articles publiés | Élevée — point d'entrée | Must | 3 | Rend les articles découvrables |
| | **Total** | | | **8** | |

</div>

**Estimations reprises sans modification** de l'atelier Product Backlog.

- US-02 : route `/articles/{slug}`, 404, responsive, cinq informations affichées.
- US-01 : liste filtrée sur les publiés, état vide, lien vers le détail.

<p class="small">Aucune story ajoutée pour « remplir » le sprint ; aucune estimation modifiée sans justification.</p>

<!--
Montrer que le Sprint Backlog est un sous-ensemble strict du Product Backlog.
Les deux stories sont Must et forment un parcours complet.
-->

---

# Pourquoi ces deux stories ?

<div class="two">
<div class="box">

### Sélectionnées

- **US-02** : cœur de la promesse, documentée, story de référence à 5 SP
- **US-01** : point d'entrée, aucune dépendance d'authentification
- Ensemble : un parcours **liste → détail** démontrable
- Taille maîtrisée : **8 SP**

</div>
<div class="box">

### Écartées de ce sprint

- **US-03** : habilitante, mais élargit le goal
- **US-04** : non prête — statut « en attente » et éditeur non tranchés
- **US-06** : non prête — rôle administrateur non documenté
- **US-05** : dépend de US-03, US-04 et US-06

</div>
</div>

<p class="quote">Une story non prête n'entre pas dans le sprint « pour compléter » : elle retourne au raffinement.</p>

<!--
Appliquer la DoR : US-04 et US-06 ne sont pas prêtes, donc elles ne sont pas sélectionnées.
Ce n'est pas un manque d'ambition, c'est une décision de réduction de risque.
-->

---

# Vérification de la Definition of Ready

| Critère DoR | US-02 | US-01 |
|---|---|---|
| Format, acteur, valeur | OK | OK |
| Critères d'acceptation testables | OK | OK |
| Dépendances | Aucune | Aucune |
| Estimation et priorité | 5 SP — Must | 3 SP — Must |
| Ressources disponibles | **Réserve** : code absent | OK |
| Taille ≤ 8 SP | OK | OK |
| Validation du Product Owner | **À confirmer** | **À confirmer** |

<p class="small">US-01 : hypothèse de tri par date décroissante, sans pagination, à valider. US-02 : T-01 vérifie l'implémentation existante avant de conclure.</p>

<!--
La DoR n'est pas un tampon automatique : deux réserves sont explicitées.
La validation PO reste une proposition, pas un acquis.
-->

---

# Règle d'or du découpage

**Une micro-tâche = 1 à 3 heures, actionnable et vérifiable.**

1. **Durée courte** : 1 à 3 h ; au-delà, on découpe ; en dessous, on fusionne.
2. **Verbe concret** : « implémenter », « tester », « vérifier », jamais « avancer sur ».
3. **Résultat vérifiable** : un fichier, un test, un comportement observable.
4. **Test intégré** : quand c'est pertinent, la tâche inclut l'écriture ou l'exécution du test.
5. **Traçabilité** : chaque tâche est rattachée à une story et à un critère d'acceptation.

<p class="small">2 à 4 micro-tâches par story. Ici : 4 tâches pour US-02, 4 tâches pour US-01.</p>

<!--
Insister sur la différence entre une story (valeur, 5 SP) et une micro-tâche (action, 1-3 h).
Le découpage ne change pas le Story Point : il organise le travail.
-->

---

# Découpage US-02 — Lire le détail d'un article

<div class="compact">

| Task ID | Tâche technique | Description | Durée |
|---|---|---|---|
| T-01 | Vérifier route et contrôleur | Route `/articles/{slug}`, `ArticleController`, délégation à `ArticleService` | 1 h |
| T-02 | Récupérer l'article publié | Requête par `slug` + statut publié ; 404 si absent ou non publié | 2 h |
| T-03 | Finaliser la vue Blade | Titre, contenu, auteur, catégorie, date ; responsive ; échappement | 2 h |
| T-04 | Tester le détail et les erreurs | Publié affiché, slug inexistant → 404, brouillon → 404 | 2 h |
| | **Total US-02** | | **7 h** |

</div>

<p class="small">Chaque durée est justifiée dans la fiche technique (section 5.3) : vérification ciblée, requête + règle, cinq informations + responsive, quatre cas de test.</p>

<!--
Parcourir les tâches dans l'ordre : vérifier, implémenter, afficher, tester.
T-01 est une tâche de vérification, pas une réécriture automatique.
-->

---

# Découpage US-01 — Consulter la liste des articles publiés

<div class="compact">

| Task ID | Tâche technique | Description | Durée |
|---|---|---|---|
| T-05 | Déclarer route et méthode | Route GET de liste, méthode mince déléguant à `ArticleService` | 1 h |
| T-06 | Implémenter la liste des publiés | Filtre statut, auteur + catégorie, tri par date décroissante (hypothèse) | 2 h |
| T-07 | Créer la vue Blade et l'état vide | Titre, auteur, catégorie, date, lien détail, message si vide, responsive | 2 h |
| T-08 | Tester la liste et l'état vide | Publiés seulement, brouillons exclus, état vide, lien valide | 2 h |
| | **Total US-01** | | **7 h** |

</div>

<p class="small">Le tri et l'absence de pagination sont des hypothèses de mise en œuvre, pas des critères d'acceptation : ils doivent être validés au Sprint Planning.</p>

<!--
Signaler l'hypothèse de tri : elle ne bloque pas la story, mais elle doit être confirmée.
Les tests couvrent l'exclusion des brouillons, qui est le cœur de la règle métier.
-->

---

# Totaux : 8 Story Points, 14 heures

| Périmètre | Story Points | Micro-tâches | Heures estimées |
|---|---|---|---|
| US-02 | 5 | 4 | 7 h |
| US-01 | 3 | 4 | 7 h |
| **Sprint Backlog** | **8** | **8** | **14 h** |

**Story Points ≠ heures**

- Les SP mesurent la **taille relative** des stories.
- Les heures estiment les **micro-tâches** de ce découpage.
- Aucune formule de conversion : le rapport 8 SP / 14 h est propre à ce sprint.
- Les 14 h sont des **estimations de planification**, pas des heures travaillées.

<p class="quote">Changer le découpage changerait les heures, pas les Story Points.</p>

<!--
C'est le point le plus important à ne pas confondre.
Les SP restent 5 et 3 ; les heures dépendent du découpage et de l'équipe.
-->

---

# Kanban : quatre colonnes, un flux tiré

<div class="compact">

| Colonne | Rôle | Entrée | Sortie |
|---|---|---|---|
| **À faire** | Sprint Backlog ordonné | Story prête, sélectionnée au Planning | Tirage par le développeur, place WIP disponible |
| **En cours** | Travail actif | Limite WIP non atteinte | Code complet, auto-contrôle fait, tests écrits |
| **En test / Review** | Vérification qualité | Implémentation et tests prêts | AC vérifiés, tests verts, revue faite, DoD satisfaite |
| **Terminé** | Incrément visible | DoD satisfaite et fusion sur `sprint1` | Acceptation PO en Review, ou réouverture |

</div>

- **Tirer de la droite vers la gauche** : finir avant de commencer.
- **Aucun saut de colonne** : pas de passage direct de « À faire » à « Terminé ».
- **« Terminé » = DoD satisfaite**, pas « code écrit ».
- **Bloqué** est un marqueur, pas une colonne : la tâche reste visible et compte dans le WIP.

<!--
Expliquer pourquoi on ne crée pas de colonne « Bloqué » : elle masquerait le flux réel.
Le marqueur oblige à nommer la cause, le responsable et la prochaine action.
-->

---

# Limites WIP proposées

| Colonne | Limite | Justification |
|---|---|---|
| **À faire** | Pas de limite | File ordonnée par dépendances |
| **En cours** | **1** | Projet individuel : éviter le changement de contexte |
| **En test / Review** | **2** | Développeur + encadrant peuvent travailler sans accumulation |
| **Terminé** | Pas de limite | Reflète l'incrément validé |

**Quand une limite est atteinte :**

1. On ne démarre **pas** de nouvelle tâche.
2. On termine, on aide à relire, on fait avancer le flux.
3. Si un blocage dépasse le timebox, le facilitateur peut autoriser **explicitement** une tâche indépendante ; la dérogation est tracée.

<p class="small">Limites proposées : la taille et la capacité de l'équipe ne sont pas documentées ; elles doivent être validées au Sprint Planning.</p>

<!--
Les limites ne sont pas des règles universelles : elles dépendent du contexte.
Ici, le projet est individuel, donc 1 tâche active est déjà ambitieux.
-->

---

# Kanban peuplé — simulation de planification

<div class="kanban">
<div class="kcol">
<h3>À faire <span class="wip">5</span></h3>
<div class="kcard"><strong>T-04</strong> Tests du détail<br/><span class="kmeta">2 h · US-02</span></div>
<div class="kcard"><strong>T-05</strong> Route liste<br/><span class="kmeta">1 h · US-01</span></div>
<div class="kcard"><strong>T-06</strong> Service liste<br/><span class="kmeta">2 h · US-01</span></div>
<div class="kcard"><strong>T-07</strong> Vue liste<br/><span class="kmeta">2 h · US-01</span></div>
<div class="kcard"><strong>T-08</strong> Tests liste<br/><span class="kmeta">2 h · US-01</span></div>
</div>
<div class="kcol">
<h3>En cours <span class="wip">1 / 1</span></h3>
<div class="kcard blocked"><strong>T-03</strong> Vue Blade détail<br/><span class="kmeta">2 h · US-02</span><br/><span class="btag">BLOQUÉ — colonne publie_le absente</span></div>
</div>
<div class="kcol">
<h3>En test / Review <span class="wip">1 / 2</span></h3>
<div class="kcard"><strong>T-02</strong> Service détail<br/><span class="kmeta">2 h · US-02</span></div>
</div>
<div class="kcol">
<h3>Terminé <span class="wip">1</span></h3>
<div class="kcard done"><strong>T-01</strong> Vérification route<br/><span class="kmeta">1 h · US-02</span></div>
</div>
</div>

<p class="small">Instantané de simulation au moment du Daily Scrum de la section suivante. Il ne représente pas l'état réel d'un sprint exécuté.</p>

<!--
Lire le tableau : une tâche terminée, une en revue, une bloquée en cours, cinq à faire.
Le WIP est respecté (1/1 et 1/2), mais le blocage menace la suite de US-02.
-->

---

# Daily Scrum : 15 minutes, trois questions

<div class="two">
<div class="box">

### Cadre

- **15 minutes maximum**
- Chaque jour ouvré, heure fixe
- Debout, Sprint Goal et Kanban visibles
- Développeur(s), facilitateur, PO optionnel
- Sortie : Kanban à jour + blocages qualifiés

</div>
<div class="box">

### Les trois questions

1. **Qu'est-ce que j'ai réalisé** depuis le dernier Daily Scrum ?
2. **Qu'est-ce que je prévois de faire** ensuite ?
3. **Quels obstacles ou blocages** rencontrés ?

</div>
</div>

- Le but est d'**inspecter la progression vers le Sprint Goal** et d'**adapter le plan**.
- Un blocage est noté, pas résolu pendant la réunion : il reçoit un responsable et une prochaine action.
- Les discussions techniques approfondies se tiennent **après** le Daily.

<p class="small">Ces trois questions sont un format de facilitation pratique, pas une formulation imposée par le Scrum Guide.</p>

<!--
Le Daily n'est pas un rapport au manager : c'est une inspection du Sprint Goal.
Le timebox de 15 minutes protège le temps de travail.
-->

---

# Simulation : un blocage au Daily Scrum

<div class="compact">

| Participant | Hier / Progression | Aujourd'hui / Prochaine action | Blocage |
|---|---|---|---|
| **Développeur** — Marwan | T-01 terminé ; T-02 en revue | Finaliser T-03, puis T-04 | `SQLSTATE[42S22]` : colonne `publie_le` absente de la base locale |
| **Facilitateur** — rôle non nominativement attribué | WIP respecté (1/1, 1/2) | Timeboxer le diagnostic, mesurer l'impact, solliciter l'encadrant | Suivi ; décision si le timebox d'1 h est dépassé |
| **Product Owner** — Groupe 1 | Aucun changement de priorité | Confirmer que la date de publication reste obligatoire | Aucun blocage fonctionnel |

</div>

**Impact sur le Sprint Goal**

- US-02, AC n° 1 : la date de publication ne peut pas être affichée.
- T-04 : les tests du détail échouent.
- US-01, T-06 : le tri par date sera bloqué par la même colonne.
- Le Sprint Goal est **menacé**, pas encore perdu.

<p class="small">Simulation hypothétique, réaliste au regard de la stack Laravel/MySQL et du diagramme de classes (`publieLe`).</p>

<!--
Le blocage est technique, réparable, et ne remet pas en cause le périmètre.
Le Daily le rend visible au lieu de le laisser caché.
-->

---

# Résolution du blocage

| Étape | Action | Responsable | Timebox |
|---|---|---|---|
| 1 | Diagnostiquer : `php artisan migrate:status` + colonnes de `articles` | Développeur | 15 min |
| 2 | Appliquer la migration existante ou en créer une pour `publie_le` | Développeur | 30 min |
| 3 | Rejouer les tests T-04 et vérifier détail + liste | Développeur | 20 min |
| 4 | Retirer le marqueur `Bloqué`, déplacer T-03 en revue | Développeur + facilitateur | 10 min |
| 5 | Si > 1 h : solliciter l'encadrant, décider appui ou dérogation WIP pour T-05 | Facilitateur + encadrant | 15 min |

**Responsable du suivi** : le facilitateur.  
**Prochaine action** : diagnostic immédiat après le Daily.  
**Prochain point** : Daily suivant, ou point court si le blocage est levé.

<p class="small">Prévention : vérifier les migrations au Planning, ne jamais corriger la base manuellement, exécuter les tests avant la revue.</p>

<!--
La résolution a un responsable, un timebox et une prochaine action : c'est ce qui distingue un blocage traité d'un blocage signalé.
Le WIP est protégé : on ne démarre pas T-05 sans décision explicite.
-->

---

# Pilotage : quatre indicateurs, zéro vélocité inventée

| Indicateur | Ce qu'il mesure | Fréquence |
|---|---|---|
| **Heures restantes** | Effort restant sur les micro-tâches non terminées | Après chaque Daily |
| **Respect du WIP** | Tâches en cours / en revue vs limites | Après chaque Daily |
| **Blocages ouverts** | Nombre, âge, responsable | Après chaque Daily |
| **Conformité DoD** | Tâches en « Terminé » réellement conformes | À chaque passage |

| Périmètre | Heures initiales | Terminé (DoD) | Restant |
|---|---|---|---|
| US-02 | 7 h | 1 h (T-01) | 6 h |
| US-01 | 7 h | 0 h | 7 h |
| **Total** | **14 h** | **1 h** | **13 h** |

<p class="small">Instantané de simulation. T-02 en revue n'est pas comptée terminée. Aucun burndown calendaire : la durée du sprint n'est pas fixée.</p>

<!--
Ne pas calculer de vélocité : il n'y a pas d'historique.
Les heures restantes sont réestimées, pas mesurées comme du temps travaillé.
-->

---

# Risques et hypothèses à valider

| Risque / hypothèse | Impact | Mitigation |
|---|---|---|
| Durée du sprint non définie | Pas de planification calendaire | Décider au Sprint Planning |
| Capacité inconnue | 14 h ≠ engagement | Valider la disponibilité |
| US-02 documentée livrée, code absent | Tâches peut-être plus légères | T-01 vérifie ; ré-estimation proposée |
| Tri et pagination non spécifiés | Ambiguïté de mise en œuvre | Hypothèse : date décroissante, sans pagination |
| Schéma MySQL désaligné | Blocage type `publie_le` | Contrôle des migrations au Planning |
| Branche `sprint0` au lieu de `sprint1` | Mauvaise base de travail | Vérifier avant la première tâche |
| US-03, US-04, US-06 non prêtes | MVP retardé | Raffiner avant le prochain Planning |

<!--
Ces risques ne sont pas des excuses : chacun a une mitigation et un responsable.
Les deux plus structurants : l'absence de code et l'absence de durée/capacité.
-->

---

# Conclusion

- **Sprint Goal** : rendre le blog publiquement utile par la découverte et la lecture.
- **Sprint Backlog** : US-02 (5 SP) + US-01 (3 SP), sans modification d'estimation.
- **Découpage** : 8 micro-tâches de 1 à 2 h, 14 h estimées, tests intégrés.
- **Kanban** : 4 colonnes, flux tiré, marqueur `Bloqué`, WIP 1 en cours / 2 en revue.
- **Daily Scrum** : 15 minutes, 3 questions, inspection du Sprint Goal.
- **Blocage simulé** : `publie_le` absent, traité par migration versionnée avec responsable et timebox.

<p class="small">Aucune exécution réelle n'est affirmée. À valider : sélection et validation PO, durée et capacité, limites WIP, hypothèse de tri, état réel de US-02.</p>

<!--
Terminer sur la prudence : le plan est cohérent et traçable, mais il reste une proposition.
Ouvrir les questions.
-->

---

<!-- _class: blank -->
<!-- _paginate: false -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Merci

<!--
Merci de votre attention. Je suis disponible pour les questions.
-->
