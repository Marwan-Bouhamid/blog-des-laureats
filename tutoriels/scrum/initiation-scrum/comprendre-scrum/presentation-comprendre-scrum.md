---
marp: true
theme: default
paginate: true
size: 16:9
header: "Solicode N3 · Agile & Scrum"
footer: "Blog des Lauréats · Marwan Bouhamid"
style: |
  :root {
    --navy: #0b1f4b;
    --blue: #0338ab;
    --accent: #2563eb;
    --sky: #e8efff;
    --ink: #0f172a;
    --muted: #475569;
    --line: #cbd5e1;
    --amber: #b45309;
    --amber-bg: #fff7e6;
  }

  section {
    font-family: "Segoe UI", "Trebuchet MS", Arial, sans-serif;
    font-size: 20px;
    line-height: 1.35;
    color: var(--ink);
    background: #ffffff;
    padding: 40px 56px 46px;
  }

  header, footer {
    color: #64748b;
    font-size: 12px;
  }

  section h1 {
    font-size: 32px;
    color: var(--blue);
    margin: 0 0 14px;
    line-height: 1.1;
    letter-spacing: -0.3px;
  }

  section h2 {
    font-size: 22px;
    color: var(--navy);
    margin: 10px 0 6px;
  }

  section h3 {
    font-size: 18px;
    color: var(--blue);
    margin: 8px 0 4px;
  }

  section p {
    margin: 4px 0 8px;
  }

  section ul, section ol {
    margin: 4px 0 8px 1.1em;
    padding-left: 0.4em;
  }

  section li {
    margin: 3px 0;
  }

  section strong {
    color: var(--navy);
  }

  section em {
    color: var(--muted);
  }

  section a {
    color: var(--accent);
  }

  blockquote {
    border-left: 5px solid var(--accent);
    background: var(--sky);
    padding: 10px 14px;
    margin: 10px 0;
    border-radius: 0 8px 8px 0;
    color: var(--navy);
  }

  blockquote p {
    margin: 0;
  }

  table, section table {
    width: 100%;
    border-collapse: collapse;
    font-size: 16px;
    margin: 8px 0;
  }

  section table {
    display: table !important;
    width: 100% !important;
  }

  th {
    background: var(--navy);
    color: #ffffff;
    text-align: left;
    padding: 7px 9px;
    font-weight: 600;
  }

  td {
    border-bottom: 1px solid var(--line);
    padding: 6px 9px;
    vertical-align: top;
  }

  tr:nth-child(even) td {
    background: #f8fafc;
  }

  code {
    background: #eef2ff;
    color: #1e3a8a;
    padding: 1px 5px;
    border-radius: 4px;
    font-size: 0.9em;
  }

  pre {
    background: var(--navy);
    color: #e2e8f0;
    padding: 12px 16px;
    border-radius: 10px;
    font-size: 14px;
    line-height: 1.25;
    margin: 8px 0;
  }

  pre code {
    background: none;
    color: inherit;
    padding: 0;
    font-size: inherit;
  }

  .small {
    font-size: 0.82em;
  }

  .muted {
    color: var(--muted);
  }

  .accent {
    color: var(--accent);
    font-weight: 600;
  }

  .warn {
    color: var(--amber);
    font-weight: 600;
  }

  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 26px;
    align-items: start;
  }

  .columns-3 {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 14px;
  }

  .card {
    background: #f8fafc;
    border: 1px solid var(--line);
    border-top: 4px solid var(--accent);
    border-radius: 10px;
    padding: 12px 14px;
  }

  .card h3 {
    margin-top: 0;
  }

  .pill {
    display: inline-block;
    background: var(--sky);
    color: var(--blue);
    border-radius: 999px;
    padding: 2px 10px;
    font-size: 0.78em;
    font-weight: 600;
  }

  .callout {
    background: var(--amber-bg);
    border-left: 5px solid var(--amber);
    padding: 10px 14px;
    border-radius: 0 8px 8px 0;
  }

  .ok {
    color: #047857;
    font-weight: 600;
  }

  .no {
    color: #b91c1c;
    font-weight: 600;
  }

  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background: linear-gradient(135deg, #071a3d 0%, #0b2f73 55%, #1d4ed8 100%);
    color: #ffffff;
    padding: 64px 76px;
  }

  section.lead h1 {
    color: #ffffff;
    font-size: 44px;
    margin-bottom: 10px;
  }

  section.lead h2 {
    color: #bfdbfe;
    font-size: 23px;
    font-weight: 500;
  }

  section.lead p, section.lead li {
    color: #e2e8f0;
  }

  section.lead strong {
    color: #ffffff;
  }

  section.lead a {
    color: #bfdbfe;
  }

  section.lead header, section.lead footer {
    display: none;
  }

  section.lead .meta {
    margin-top: 22px;
    font-size: 16px;
    line-height: 1.55;
  }

  section.lead .meta strong {
    color: #93c5fd;
  }

  section.lead .rule {
    width: 90px;
    height: 4px;
    background: #60a5fa;
    border-radius: 2px;
    margin: 16px 0 20px;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Comprendre l'approche Agile et le cadre Scrum

## Application à mon Projet Technique — Blog des Lauréats

<div class="rule"></div>

<div class="meta">
<strong>Apprenant :</strong> Marwan Bouhamid<br>
<strong>Établissement :</strong> Solicode Tanger<br>
<strong>Encadrant :</strong> ESSARRAJ Fouad<br>
<strong>Formation :</strong> Solicode N3<br>
<strong>Date :</strong> 25 novembre 2026
</div>

<!--
ORAL EXPLANATION:
Bonjour à toutes et à tous. Je m'appelle Marwan Bouhamid, apprenant en N3 à Solicode Tanger. Je vais vous présenter les fondations de l'approche Agile et du cadre Scrum, puis les appliquer à mon projet technique, le Blog des Lauréats. L'objectif est de comprendre pourquoi ces méthodes existent et comment elles organisent concrètement le travail d'une équipe.
-->

---

# Introduction — Pourquoi une méthode ?

<div class="columns">
<div>

### Gérer un projet logiciel

- Définir le **périmètre** et les priorités.
- Planifier, coordonner et suivre le travail.
- Garantir la **qualité** et la livraison.
- Faire circuler l'information dans l'équipe.

</div>
<div>

### Sans organisation claire

- Besoins flous ou contradictoires.
- Retards et **effet tunnel**.
- Bugs découverts trop tard.
- Reprises coûteuses et client insatisfait.

</div>
</div>

> **Fil conducteur :** du cycle en V vers l'Agilité, puis Scrum, ses rôles, ses événements et ses artefacts — avec le Blog des Lauréats comme fil rouge.

<!--
ORAL EXPLANATION:
Avant de parler de Scrum, rappelons ce qu'est la gestion de projet : c'est l'ensemble des décisions et des pratiques qui permettent de livrer un logiciel utile, dans les délais et avec la qualité attendue. Sans méthode, chacun travaille dans son coin, les besoins changent sans être priorisés et les problèmes apparaissent au moment de la livraison. Cette présentation va donc suivre un fil conducteur : comprendre le problème du cycle en V, découvrir l'Agilité, puis structurer le travail avec Scrum.
-->

---

# L'approche traditionnelle : le cycle en V

<div class="columns">
<div>

### Les étapes

1. **Analyse des besoins** → cahier des charges.
2. **Conception** → architecture et modèles.
3. **Développement** → réalisation.
4. **Tests** → unitaires et intégration.
5. **Validation** → recette et livraison.

</div>
<div>

```text
Besoins
  \
   Spécifications
     \
      Conception
        \
         Développement
        /
       Tests unitaires
     /
   Tests d'intégration
 /
Recette & validation
```

</div>
</div>

<div class="columns">
<div>

**Avantages**
- Cadre clair et traçable.
- Documentation abondante.
- Adapté aux besoins stables ou réglementés.

</div>
<div>

**Limites**
- Retours utilisateurs tardifs.
- Changements coûteux.
- Effet tunnel et rigidité.

</div>
</div>

<!--
ORAL EXPLANATION:
Le cycle en V organise le projet en phases séquentielles. On commence par analyser les besoins, puis on conçoit, on développe, et on teste seulement à la fin. La branche gauche du V descend vers la réalisation, la branche droite remonte vers la validation. Ce modèle a des qualités : il est clair, traçable et rassurant. Mais son défaut majeur est l'effet tunnel : le client ne voit le produit qu'à la fin, alors que ses besoins ont peut-être changé entre-temps.
-->

---

# L'approche Agile : livrer par petits pas

**Agile** est une approche **itérative et incrémentale** : on apprend par cycles courts, avec des retours fréquents.

<div class="columns">
<div>

### Les principes clés

- **Itérer** : produire par cycles courts.
- **Incrémenter** : ajouter une valeur utilisable.
- **Feedback** : montrer tôt, écouter, ajuster.
- **Prioriser** : livrer d'abord ce qui compte.
- **S'adapter** : accueillir le changement.

</div>
<div>

```text
   Sprint ──► Incrément ──► Feedback
      ▲                        │
      └────── adapter ◄────────┘

   Sprint 1 → Sprint 2 → Sprint 3 → ...
```

</div>
</div>

> **Agile n'est pas l'absence de plan.** C'est un plan ajusté en continu grâce à ce que l'on apprend.

<!--
ORAL EXPLANATION:
L'Agilité propose de réduire le risque en découpant le projet en petits cycles. À chaque cycle, l'équipe livre un incrément réellement utilisable, le montre aux utilisateurs et utilise leurs retours pour décider de la suite. On ne cherche pas à tout prévoir au départ : on cherche à apprendre vite pour prendre de meilleures décisions. Attention, Agile ne signifie pas improviser : il y a toujours un plan, mais il évolue avec les faits.
-->

---

# Cycle en V vs Agile

| Critère | Cycle en V | Approche Agile |
|---|---|---|
| **Planification** | Détaillée en amont | Progressive, par itérations |
| **Changements** | Coûteux et formalisés | Attendus et priorisés |
| **Livraison** | En fin de projet | Incréments réguliers |
| **Tests** | Phase finale | À chaque itération |
| **Feedback** | Tardif | Continu |
| **Organisation** | Séquentielle | Équipe autonome et collaborative |

> **À retenir :** Agile conserve la planification et la documentation, mais les rend **utiles et évolutives**. Le cycle en V reste pertinent lorsque les besoins sont stables ou fortement réglementés.

<!--
ORAL EXPLANATION:
Ce tableau résume la rupture principale. Le cycle en V mise sur la prévision : on spécifie beaucoup, puis on exécute. L'Agilité mise sur l'adaptation : on planifie par petits pas et on ajuste avec le feedback. Il ne s'agit pas de dire qu'un modèle est mauvais dans l'absolu. Le cycle en V peut être adapté à certains contextes. Mais pour un projet web dont les besoins évoluent, l'Agilité réduit le risque de livrer quelque chose qui ne correspond plus au besoin.
-->

---

# Le Manifeste Agile : quatre valeurs

| Valeur | Explication simple | Exemple pour le Blog des Lauréats |
|---|---|---|
| **Individus et interactions** plutôt que processus et outils | Se parler et décider ensemble | Un Daily de 15 minutes plutôt que dix e-mails |
| **Logiciel opérationnel** plutôt que documentation exhaustive | Une fonctionnalité qui fonctionne vraiment | Une page article consultable plutôt qu'un cahier des charges de 50 pages |
| **Collaboration avec le client** plutôt que négociation contractuelle | Construire avec le client, pas contre lui | Montrer la maquette au Product Owner et l'ajuster |
| **Adaptation au changement** plutôt que suivi rigide d'un plan | Changer de priorité quand le besoin évolue | Ajouter le filtrage par catégorie si les visiteurs le demandent |

> Les éléments de droite gardent de la valeur : processus, documentation, contrat et plan restent utiles. Agile **privilégie** simplement la gauche.

<!--
ORAL EXPLANATION:
Le Manifeste Agile, publié en 2001, repose sur quatre préférences. Par exemple, une équipe qui se parle et décide rapidement est souvent plus efficace qu'une équipe bloquée par des outils mal adaptés. De même, un logiciel qui fonctionne a plus de valeur pour l'utilisateur qu'un document qui promet de le faire. Attention à la formulation : il ne s'agit pas de supprimer la documentation ou le contrat, mais de ne pas les placer au-dessus de la collaboration et du produit réel.
-->

---

# Scrum : un cadre léger pour les problèmes complexes

<div class="columns">
<div>

### Ce que Scrum propose

- Un **cadre léger** pour générer de la valeur.
- Des **solutions adaptatives** face à la complexité.
- Un fonctionnement fondé sur l'**empirisme**.
- Trois responsabilités, cinq événements, trois artefacts.
- Un cadre minimal : l'équipe choisit ses pratiques techniques.

</div>
<div>

| Agile | Scrum |
|---|---|
| Une approche, des valeurs et des principes | Un **cadre de travail** concret |
| « Pourquoi et comment penser » | « Comment organiser le travail » |
| Manifeste + 12 principes | Guide Scrum 2020 |
| Peut se décliner en Kanban, XP… | Une mise en œuvre parmi d'autres |

</div>
</div>

> **Scrum n'est pas toute l'Agilité.** C'est un moyen structuré de la pratiquer.

<!--
ORAL EXPLANATION:
Il est fréquent de confondre Agile et Scrum. Agile est une approche, portée par des valeurs et des principes. Scrum est un cadre de travail précis qui permet de mettre ces idées en pratique. Scrum ne dit pas quelle technologie utiliser ni comment coder : il définit des responsabilités, des événements et des artefacts pour rendre le travail visible et adaptable. On peut être agile avec Kanban ou XP ; Scrum est l'un des cadres possibles.
-->

---

# Les trois piliers de l'empirisme

| Pilier | Définition | Exemple pour le Blog des Lauréats |
|---|---|---|
| **Transparence** | L'information est visible et comprise par tous | Backlog, code et difficultés visibles sur GitHub |
| **Inspection** | Examiner régulièrement le produit et le travail | Revue de la page article, tests, Daily Scrum |
| **Adaptation** | Ajuster dès qu'un écart est détecté | Corriger une priorité ou lever un obstacle |

```text
Transparence ──► Inspection ──► Adaptation
      ▲                              │
      └──────── apprentissage ◄──────┘
```

> Sans transparence, l'inspection est faussée. Sans adaptation, l'inspection ne sert à rien.

<!--
ORAL EXPLANATION:
Scrum repose sur l'empirisme : on apprend par l'expérience et les faits, pas uniquement par la théorie. Pour cela, trois piliers doivent fonctionner ensemble. La transparence rend le travail visible ; l'inspection permet de comprendre où en est le produit ; l'adaptation permet de corriger la trajectoire. Si l'équipe cache ses difficultés, l'inspection devient inutile. Et si l'on inspecte sans jamais rien changer, le rituel devient une simple formalité.
-->

---

# L'équipe Scrum : trois responsabilités

<div class="columns-3">
<div class="card">

### Product Owner

- Maximiser la **valeur** du produit.
- Gérer et ordonner le **Product Backlog**.
- Communiquer le **Product Goal**.

</div>
<div class="card">

### Scrum Master

- Établir et faire vivre **Scrum**.
- **Coacher** l'équipe et l'organisation.
- Aider à **lever les obstacles**.

</div>
<div class="card">

### Developers

- Créer le **Sprint Backlog**.
- Garantir la **qualité**.
- Produire un **Incrément** utilisable.

</div>
</div>

- Un seul **objectif produit** partagé par toute l'équipe.
- Une équipe **pluridisciplinaire** : toutes les compétences nécessaires.
- Une équipe **auto-gérée** : elle décide de la répartition du travail.
- **Pas de sous-équipes ni de hiérarchie interne** imposée par Scrum.

> Scrum définit des **responsabilités**, pas des grades.

<!--
ORAL EXPLANATION:
L'équipe Scrum réunit trois responsabilités complémentaires. Le Product Owner porte la valeur et les priorités ; le Scrum Master veille à l'efficacité du cadre ; les Developers construisent l'incrément. Scrum ne crée pas de chef de projet au-dessus de l'équipe et n'impose pas de sous-équipes. L'équipe est pluridisciplinaire et auto-gérée : elle décide elle-même comment répartir le travail pour atteindre l'objectif commun.
-->

---

# Le Product Owner : responsable de la valeur

<div class="columns">
<div>

### Ses responsabilités

- **Maximiser la valeur** du produit.
- Développer et communiquer le **Product Goal**.
- Créer et clarifier les éléments du **Product Backlog**.
- **Ordonner** le backlog selon la valeur et le risque.
- S'assurer que le backlog est **transparent** et compris.

</div>
<div>

<div class="callout">

### Exemple — Blog des Lauréats

Le Product Owner pourrait prioriser d'abord la **consultation d'un article**, car elle apporte une valeur immédiate au visiteur.

La modération avancée peut attendre un sprint ultérieur.

Il ne dit pas aux développeurs **comment coder**.

</div>

</div>
</div>

> Le Product Owner est **une seule personne**, pas un comité. Il peut déléguer certaines tâches, mais reste **responsable final** du produit.

<!--
ORAL EXPLANATION:
Le Product Owner est responsable de la valeur du produit. Concrètement, il décide ce qui est le plus important et dans quel ordre. Sur le Blog des Lauréats, il peut choisir de commencer par la consultation d'un article, parce que c'est la fonctionnalité la plus visible pour le visiteur. Il ne s'agit pas d'un chef technique : le PO décide du quoi et du pourquoi, pas du comment. Et même s'il travaille avec d'autres, il reste le responsable final du produit.
-->

---

# Le Scrum Master : facilitateur du cadre

<div class="columns">
<div>

### Ce qu'il fait

- **Établit Scrum** tel que défini dans le Guide.
- **Coache** l'équipe en auto-gestion et pluridisciplinarité.
- Aide à identifier et à **lever les obstacles**.
- Veille à ce que les événements soient **utiles et à durée limitée**.
- Aide l'organisation à **comprendre Scrum**.

</div>
<div>

### Ce qu'il n'est pas

- <span class="no">✗</span> Un chef de projet qui distribue les tâches.
- <span class="no">✗</span> Un manager hiérarchique des développeurs.
- <span class="no">✗</span> Un simple secrétaire de réunion.

<div class="callout">

**Son objectif :** créer les conditions de la performance, pas décider à la place de l'équipe.

</div>

</div>
</div>

> Le Scrum Master est un **serviteur-leader** : il sert l'équipe et le cadre, sans autorité hiérarchique.

<!--
ORAL EXPLANATION:
Le Scrum Master est souvent mal compris. Ce n'est pas un chef de projet déguisé. Son rôle est de faire en sorte que Scrum fonctionne vraiment : il coache l'équipe, facilite les événements et aide à supprimer les obstacles. Par exemple, si l'environnement Laravel bloque les développeurs, il intervient pour débloquer la situation. Il n'a pas d'autorité hiérarchique sur l'équipe : il influence par le coaching et la facilitation.
-->

---

# Les Developers : ceux qui construisent l'Incrément

<div class="columns">
<div>

### Leurs responsabilités

- Créer le **Sprint Backlog**, le plan du Sprint.
- Instaurer la **qualité** en respectant la Definition of Done.
- **Adapter** leur plan chaque jour vers le Sprint Goal.
- Créer un **Incrément utilisable** à chaque Sprint.
- S'auto-organiser et se tenir mutuellement responsables.

</div>
<div>

### Exemples — Blog des Lauréats

- Modéliser `Article`, `Catégorie`, `Utilisateur`.
- Développer la route et le contrôleur de consultation.
- Construire la vue **Blade responsive**.
- Écrire les tests et gérer l'erreur **404**.
- Relire le code et vérifier l'**accessibilité**.

</div>
</div>

> Scrum ne dit pas **comment coder** : l'équipe choisit ses pratiques techniques et assume collectivement la qualité.

<!--
ORAL EXPLANATION:
Les Developers sont les personnes qui réalisent l'incrément. Ils ne se contentent pas d'exécuter des tâches : ils construisent le plan du Sprint, décident de l'organisation technique et s'engagent sur la qualité. Sur le Blog des Lauréats, cela peut être la modélisation des articles, la route de consultation, la vue Blade ou les tests. Scrum laisse l'équipe libre sur les pratiques techniques : l'important est de livrer un incrément qui respecte la Definition of Done.
-->

---

# Les cinq événements Scrum

| Événement | Question à laquelle il répond | Durée / rythme |
|---|---|---|
| **Sprint** | Quel cycle de valeur ? | ≤ 1 mois, conteneur des autres événements |
| **Sprint Planning** | Pourquoi, quoi, comment ? | Début du Sprint |
| **Daily Scrum** | Où en sommes-nous vers le Sprint Goal ? | 15 minutes, chaque jour ouvré |
| **Sprint Review** | Qu'avons-nous livré, et que faire ensuite ? | Fin du Sprint |
| **Sprint Retrospective** | Comment mieux travailler ? | Après la Review |

```text
|←────────────── Sprint (≤ 1 mois) ──────────────→|
   Planning ──► Daily × n ──► Review ──► Rétrospective
```

> Tous les événements ont lieu **dans le Sprint**. Ce ne sont pas des réunions de reporting.

<!--
ORAL EXPLANATION:
Scrum organise le travail autour de cinq événements. Le Sprint est le conteneur : c'est la période de travail, d'un mois maximum. À l'intérieur, on trouve la planification, le Daily, la revue et la rétrospective. Chaque événement a un objectif précis et une durée limitée. Le Sprint n'est pas une réunion : c'est le cadre dans lequel l'équipe crée l'incrément. Les quatre autres événements permettent d'inspecter et d'adapter le travail.
-->

---

# Sprint Planning et Sprint Goal

<div class="columns">
<div>

### Trois questions

1. **Pourquoi** ce Sprint est-il utile ?
   → le **Sprint Goal**.
2. **Que** peut-on réaliser ?
   → la sélection dans le Product Backlog.
3. **Comment** le travail sera-t-il fait ?
   → le plan dans le Sprint Backlog.

</div>
<div>

<div class="callout">

### Exemple hypothétique — Blog des Lauréats

**Sprint Goal :** « Livrer une page de consultation d'article, responsive et accessible, alimentée par des données de démonstration. »

**Critère de succès :** un visiteur ouvre un article de démonstration et voit son contenu sur mobile comme sur desktop.

</div>

</div>
</div>

> Le Sprint Goal donne une **direction commune**. Ce n'est pas une liste de tâches.

<!--
ORAL EXPLANATION:
La Sprint Planning répond à trois questions. Pourquoi ce Sprint est-il utile ? C'est le Sprint Goal. Qu'est-ce qu'on peut réaliser ? C'est la sélection des éléments du Product Backlog. Comment va-t-on le faire ? C'est le plan du Sprint Backlog. Le Sprint Goal est important : il donne une direction commune et permet à l'équipe de s'adapter sans perdre le cap. L'exemple présenté est hypothétique : il illustre la méthode, il ne s'agit pas d'un engagement officiel de l'équipe.
-->

---

# Daily Scrum : synchroniser, pas surveiller

<div class="columns">
<div>

### Objectif et cadre

- Inspecter la progression vers le **Sprint Goal**.
- **15 minutes**, chaque jour ouvré, même heure, même lieu.
- Réservé aux **Developers**.
- Adapter le **Sprint Backlog** si nécessaire.
- Favoriser l'entraide et la décision rapide.

</div>
<div>

### Ce n'est pas…

- <span class="no">✗</span> Un rapport de statut pour un manager.
- <span class="no">✗</span> Une réunion pour résoudre tous les problèmes.
- <span class="no">✗</span> Un moment pour détailler chaque tâche.

<div class="callout">

**Exemple :** « La route article fonctionne ; je bloque sur l'affichage mobile. Qui peut m'aider ? »

</div>

</div>
</div>

> Les problèmes se règlent **après** le Daily, avec les personnes concernées.

<!--
ORAL EXPLANATION:
Le Daily Scrum est un point court, debout, de quinze minutes. Son but est de synchroniser les Developers et d'inspecter la progression vers le Sprint Goal. Ce n'est pas une réunion où chacun rend des comptes à un manager. L'équipe partage les informations utiles, identifie les obstacles et décide de la suite. Si un problème demande plus de temps, il se règle après le Daily avec les personnes concernées, pour ne pas transformer le rituel en réunion interminable.
-->

---

# Sprint Review vs Sprint Retrospective

| Critère | Sprint Review | Sprint Retrospective |
|---|---|---|
| **Focus** | Le **produit** et le résultat | L'**efficacité** de l'équipe |
| **Participants** | Équipe Scrum + parties prenantes | Équipe Scrum |
| **Objectif** | Inspecter l'Incrément et adapter la suite | Améliorer la façon de travailler |
| **Entrée** | L'Incrément terminé | Le déroulement du Sprint |
| **Sortie** | Feedback et Product Backlog ajusté | Actions d'amélioration concrètes |
| **Exemple Blog** | Démo de la page article au Product Owner | « Nos tests arrivent trop tard » |

> **Review = regarder le produit. Rétrospective = regarder l'équipe.** Les deux sont nécessaires.

<!--
ORAL EXPLANATION:
La Review et la Rétrospective sont souvent confondues. La Sprint Review regarde le produit : on montre l'incrément aux parties prenantes, on recueille du feedback et on adapte la suite. La Rétrospective regarde l'équipe : on analyse comment le Sprint s'est déroulé et on choisit des actions pour améliorer la qualité et l'efficacité. Sur le Blog des Lauréats, la Review pourrait être une démonstration de la page article ; la Rétrospective pourrait porter sur le fait que les tests arrivent trop tard.
-->

---

# Les trois artefacts et leurs engagements

| Artefact | Rôle | Engagement |
|---|---|---|
| **Product Backlog** | Liste ordonnée de tout ce qui pourrait être fait | **Product Goal** |
| **Sprint Backlog** | Objectif du Sprint + éléments sélectionnés + plan | **Sprint Goal** |
| **Incrément** | Étape concrète vers le Product Goal, utilisable | **Definition of Done** |

```text
Product Backlog ──────► Product Goal
       │
       ▼
Sprint Backlog ───────► Sprint Goal
       │
       ▼
   Incrément ─────────► Definition of Done
```

> L'engagement rend l'artefact **transparent** : on sait ce que l'on vise et ce qui est réellement terminé.

<!--
ORAL EXPLANATION:
Scrum définit trois artefacts, chacun avec un engagement. Le Product Backlog est la liste ordonnée de ce qui pourrait être fait ; son engagement est le Product Goal, la vision à moyen terme. Le Sprint Backlog contient l'objectif du Sprint, les éléments sélectionnés et le plan ; son engagement est le Sprint Goal. Enfin, l'Incrément est ce qui est réellement produit ; son engagement est la Definition of Done. Ces engagements évitent de confondre une intention avec un résultat terminé.
-->

---

# Definition of Done et Incrément

<div class="columns">
<div>

### Pourquoi une Definition of Done ?

- C'est la **définition formelle de la qualité**.
- Elle s'applique à **chaque élément** de travail.
- Un élément non conforme **n'est pas** dans l'Incrément.
- L'Incrément doit être **utilisable** et apporter de la valeur.
- La DoD rend la **transparence vérifiable**.

</div>
<div>

<div class="callout">

### Exemple hypothétique — affichage d'un article

- Titre, auteur, date et contenu affichés.
- Article inexistant → page **404** claire.
- Responsive **375 px** et desktop.
- HTML sémantique, contrastes accessibles.
- Contenu échappé contre les injections **XSS**.
- Test manuel + test automatisé validés.

</div>

</div>
</div>

> « Done » n'est pas une opinion : c'est un **critère partagé et vérifiable**.

<!--
ORAL EXPLANATION:
La Definition of Done est ce qui permet de savoir si un travail est vraiment terminé. Sans elle, chacun peut avoir sa propre définition et le mot « fini » perd son sens. Sur le Blog des Lauréats, une page article peut être considérée comme terminée si elle affiche les bonnes informations, gère le cas d'un article inexistant, reste lisible sur mobile, protège contre les injections et passe les tests. L'Incrément doit être utilisable : un ensemble de morceaux de code non vérifiés n'est pas un incrément.
-->

---

# Application au Blog des Lauréats

**Faits vérifiés dans le dépôt :** périmètre et stack issus de `docs/cadrage` ; Sprint 1 documenté dans `sprints/sprints.md`.

| Élément | Exemple proposé pour le Blog des Lauréats |
|---|---|
| **Product Goal** | Permettre aux lauréats de partager leurs parcours et aux visiteurs de les consulter facilement. |
| **Product Backlog** | Consulter la liste des articles ; lire un article ; soumettre un article ; modérer les publications. |
| **Sprint Goal** | Livrer la consultation d'un article, responsive et accessible, avec des données de démonstration. |
| **Sprint Backlog** | Modèle `Article`, route, contrôleur + service, vue Blade, gestion 404, tests. |
| **Incrément** | Page article fonctionnelle avec titre, auteur, date, contenu et état 404. |
| **Definition of Done** | Affichage mobile/desktop, 404, protection XSS, tests validés, revue de code. |

> Ces exemples sont **illustratifs** : ils ne constituent pas des engagements validés par l'équipe.

<!--
ORAL EXPLANATION:
Voici comment appliquer Scrum au Blog des Lauréats. Les éléments de contexte sont réels : le périmètre et la stack viennent du dossier de cadrage, et le Sprint 1 est bien consacré au cadrage et à la consultation d'un article. En revanche, les exemples de Product Goal, de backlog, de Sprint Goal et de Definition of Done sont des illustrations pédagogiques. Ils montrent comment une équipe pourrait formuler ces éléments, mais ils ne doivent pas être présentés comme des engagements officiels déjà validés.
-->

---

# Conclusion

- **Agile** encourage l'adaptation et le feedback continu.
- **Scrum** organise le travail avec un cadre léger et explicite.
- Les **trois piliers** rendent le contrôle empirique possible.
- Les **trois responsabilités**, les **cinq événements** et les **trois artefacts** structurent l'équipe.
- L'**Incrément** et la **Definition of Done** rendent la valeur visible et vérifiable.

> Une équipe Scrum ne promet pas de tout prévoir : elle organise l'apprentissage pour livrer la **bonne valeur, au bon moment**.

<!--
ORAL EXPLANATION:
Pour conclure, l'Agilité n'est pas une mode : c'est une réponse au risque de livrer trop tard un produit qui ne correspond plus au besoin. Scrum apporte un cadre concret avec des rôles, des événements et des artefacts. Les trois piliers garantissent que l'équipe apprend des faits. Et la Definition of Done permet de distinguer ce qui est réellement terminé de ce qui reste une intention. La prochaine étape, pour moi, est d'appliquer ces notions au Sprint 1 du Blog des Lauréats.
-->

---

<!-- _class: lead -->
<!-- _paginate: false -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Merci pour votre attention

## Des questions ?

**Marwan Bouhamid** · Solicode Tanger  
Projet : Blog des Lauréats · Formation Solicode N3  
Encadrant : ESSARRAJ Fouad

<!--
ORAL EXPLANATION:
Merci pour votre attention. Je reste disponible pour répondre à vos questions, notamment sur la différence entre Agile et Scrum, sur le rôle du Product Owner ou sur la façon dont ces notions s'appliquent au Blog des Lauréats.
-->
