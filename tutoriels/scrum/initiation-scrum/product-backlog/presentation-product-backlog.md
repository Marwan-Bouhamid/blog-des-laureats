---
marp: true
theme: default
paginate: true
size: 16:9
header: "Solicode N3 — Atelier Product Backlog"
footer: "Blog des Lauréats | Encadrant : ESSARRAJ Fouad"
style: |
  section {
    font-family: Arial, sans-serif;
    background: #ffffff;
    color: #1f2937;
    padding: 46px 64px;
  }

  section h1 {
    font-size: 38px;
    color: #0338ab;
  }

  section h2 {
    color: #2563eb;
  }

  section h3 {
    color: #0338ab;
    margin: 0 0 6px;
    font-size: 21px;
  }

  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
  }

  section.lead h1 {
    font-size: 50px;
    margin-bottom: 4px;
  }

  section.lead h3 {
    font-size: 24px;
    font-weight: normal;
    color: #2563eb;
    margin: 0 0 22px;
  }

  ul, ol {
    line-height: 1.4;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 20px;
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
    font-size: 18px;
    color: #475569;
  }

  .quote {
    border-left: 5px solid #2563eb;
    background: #f1f5ff;
    padding: 9px 15px;
    font-size: 19px;
    font-style: italic;
    margin-top: 10px;
  }

  .two {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 22px;
    margin: 6px 0 16px;
  }

  .box {
    background: #f8fafc;
    border: 1px solid #dbe4f0;
    border-radius: 10px;
    padding: 10px 14px;
    font-size: 18px;
  }

  .box ul {
    margin: 5px 0 0;
    padding-left: 18px;
  }

  .box li {
    margin-bottom: 5px;
  }

  .compact table {
    font-size: 16px;
  }

  .compact th, .compact td {
    padding: 3px 7px;
  }

  .chain {
    display: flex;
    align-items: stretch;
    gap: 8px;
    margin: 18px 0 14px;
  }

  .step {
    flex: 1;
    background: #eef4ff;
    border: 1px solid #c7d8f5;
    border-radius: 10px;
    padding: 10px 8px;
    text-align: center;
  }

  .step strong {
    display: block;
    color: #0338ab;
    font-size: 19px;
  }

  .step span {
    font-size: 16px;
    color: #475569;
  }

  .arrow {
    display: flex;
    align-items: center;
    font-size: 26px;
    color: #2563eb;
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

# Créer, estimer et ordonner le Product Backlog

### Blog des Lauréats — de la User Story à l'incrément priorisé

- **Atelier** : UA.351.11 — Initiation à la démarche Agile et cadre Scrum
- **Apprenant** : Marwan bouhamid
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Date** : 26 novembre 2026

<!--
Présenter l'atelier : il applique la démarche au projet réel Blog des Lauréats, pas à l'exemple TodoList.
Annoncer le fil : backlog, estimation, priorisation, MVP, DoR/DoD.
-->

---

# Objectifs de l'atelier

- **Expliquer** le rôle du Product Backlog et du Product Owner.
- **Estimer** l'effort relatif en Story Points avec la suite de Fibonacci.
- **Ordonner** les User Stories selon la valeur et les dépendances.
- **Prioriser** avec MoSCoW et isoler le MVP de la sélection d'un sprint.
- **Formaliser** une Definition of Ready et une Definition of Done vérifiables.

<p class="small">Fil conducteur : dix User Stories du Blog des Lauréats, cinq reprises de l'atelier Vision/Besoins et cinq propositions documentées.</p>

<!--
Insister sur la distinction entre les livrables : fiche technique détaillée et diaporama de synthèse.
Tout ce qui est présenté ici est traçable dans la fiche ou dans le dépôt.
-->

---

# Contexte projet : Blog des Lauréats

| Élément | Description |
|---|---|
| **Produit** | Plateforme web communautaire de Solicode Tanger |
| **Public** | Lauréats contributeurs, apprenants, visiteurs |
| **Problème** | Des témoignages utiles, mais dispersés et peu structurés |
| **Promesse** | Centraliser et valoriser les parcours sous forme d'articles modérés |
| **Acteurs** | Lauréat, apprenant/visiteur, administrateur |
| **Stack** | Laravel, MySQL, Blade, Tailwind CSS, Alpine.js |

<p class="small">Sources : README, note de cadrage, diagramme de cas d'utilisation et diagramme de classes.</p>

<!--
Rappeler le contexte Solicode. Le besoin est documenté : centraliser les témoignages entre promotions.
Ne pas entrer dans la technique : le sujet de la slide est la valeur produit.
-->

---

# Qu'est-ce qu'un Product Backlog ?

**Définition** : liste **ordonnée** et **évolutive** de tout ce qui est nécessaire pour améliorer le produit.

- **Ordonné** : le plus important en haut.
- **Émergent** : il s'enrichit et se réordonne en continu.
- **Unique** : source de vérité des changements du produit.
- **Mixte** : User Stories, tâches techniques, bugs, dettes, risques.

**Pourquoi le raffiner en continu ?**

- Réduire l'incertitude et découper les grosses stories.
- Ré-estimer après chaque apprentissage.
- Garder le haut du backlog prêt pour le Sprint Planning.

<p class="quote">Exemple : le statut « en attente de publication » doit être tranché avant de pouvoir engager la modération.</p>

<!--
Un backlog n'est pas un cahier des charges figé : il vit.
Le raffinement n'est pas une réunion administrative, c'est le moment où l'équipe réduit le risque.
-->

---

# Product Backlog vs Sprint Backlog

| Critère | Product Backlog | Sprint Backlog |
|---|---|---|
| **Propriétaire** | Product Owner | Developers |
| **Horizon** | Tout le produit | Un seul sprint |
| **Contenu** | Tous les besoins, y compris différés | Stories sélectionnées + plan |
| **Granularité** | Grossière en bas, fine en haut | Découpée en tâches |
| **Évolution** | Continu | Figé pendant le sprint |
| **Engagement** | **Product Goal** | **Sprint Goal** |
| **Exemple** | US-01 à US-10 | US-02 + US-01 (8 SP) |

<p class="small">Le Sprint Backlog est un sous-ensemble du Product Backlog, jamais l'inverse.</p>

<!--
Le Product Backlog dit quoi et pourquoi ; le Sprint Backlog dit ce qui est fait maintenant et comment.
Un élément du Sprint Backlog qui n'existe pas dans le Product Backlog est une anomalie de gouvernance.
-->

---

# Rôle du Product Owner

- **Possède et ordonne** le Product Backlog.
- **Maximise la valeur** du produit : chaque choix d'ordre sert la valeur, pas la facilité.
- **Exprime les besoins** de façon compréhensible par l'équipe.
- **Arbitre le périmètre** : MVP, reports, exclusions.
- **Valide la readiness** avant l'engagement en sprint.
- **Ne décide pas** de la solution technique : le « comment » appartient aux Developers.

<p class="small">Dans le dépôt, le Product Owner est désigné comme « Groupe 1 » (note de cadrage). Les priorités de ce diaporama restent des propositions à valider.</p>

<!--
Distinguer le rôle Scrum du rôle réel dans ce projet individuel : l'apprenant analyse, mais la décision de priorisation revient au PO désigné ou à l'encadrant.
-->

---

# Story Points : une estimation relative

**Un Story Point mesure un effort relatif, pas une durée.**

| Dimension prise en compte | Exemple Blog des Lauréats |
|---|---|
| **Complexité technique** | Authentification, rôles, autorisations (US-03) |
| **Volume de travail** | Formulaire, validation, workflow de statuts (US-04) |
| **Incertitude** | Statut « en attente » absent du diagramme de classes |
| **Risque** | Sécurité des accès, régression sur la page article |

**Pourquoi pas des heures ?**

- La solution n'est pas entièrement connue à l'avance.
- L'équipe n'a ni vélocité ni historique de sprints terminés.
- Les interruptions et la disponibilité ne sont pas maîtrisées.

<p class="quote">8 SP ne signifie pas « deux fois plus long » que 4 SP : la story est plus grande et plus incertaine.</p>

<!--
La question n'est pas « combien de temps », mais « quelle taille par rapport à ce que nous savons déjà estimer ».
Aucune conversion en heures ni en jours n'est proposée dans cet atelier.
-->

---

# L'échelle de Fibonacci retenue

| Valeur | Signification | Exemple dans le projet |
|---|---|---|
| **1** | Très petite, quasi certaine | Correction de libellé |
| **2** | Petite, bien comprise | Champ d'affichage simple |
| **3** | Modérée, périmètre clair | US-01, US-05, US-08 |
| **5** | Moyenne, règles ou sécurité | US-02, US-03, US-06 |
| **8** | Grande, plusieurs règles | US-04 |

**Deux principes :**

- Les **écarts** entre valeurs forcent la discussion : hésiter entre 3 et 5 oblige à expliciter le risque.
- **8 SP = seuil d'alerte** : au-delà, la story doit être découpée.

<p class="small">US-02 (lire un article) sert de story de référence à 5 SP : route, service, vue Blade, 404 et responsive.</p>

<!--
L'échelle n'est pas une échelle linéaire : elle traduit une incertitude croissante.
La story de référence donne un ancrage commun à l'équipe.
-->

---

# Estimation des User Stories

<div class="compact">

| ID | User Story | SP | MoSCoW |
|---|---|---|---|
| US-01 | Consulter la liste des articles publiés | 3 | Must |
| US-02 | Lire le détail d'un article | 5 | Must |
| US-03 | Créer un compte et se connecter | 5 | Must |
| US-04 | Rédiger et soumettre un article | 8 | Must |
| US-05 | Suivre le statut de mes articles | 3 | Should |
| US-06 | Modérer et publier les articles | 5 | Must |
| US-07 | Rechercher et filtrer les articles | 5 | Could |
| US-08 | Gérer les catégories | 3 | Could |
| US-09 | Modifier ou supprimer un article | 5 | Won't |
| US-10 | Consulter le profil public d'un lauréat | 5 | Won't |
| | **Total** | **47** | |

</div>

<p class="small">US-01 à US-05 : reprises de l'atelier Vision/Besoins. US-06 à US-10 : propositions adossées aux cas d'utilisation et à la note de cadrage.</p>

<!--
Parcourir la colonne SP, pas les stories une par une.
Signaler que US-09 et US-10 sont estimées à titre indicatif : elles sont hors périmètre actuel.
-->

---

# Pourquoi ces estimations ?

<div class="two">
<div class="box">

### US-04 · 8 SP

- Formulaire complet + validation serveur
- Workflow brouillon → soumis
- Contrôle de propriété
- Rattachement à une catégorie
- Plusieurs règles métier combinées

</div>
<div class="box">

### US-02 · 5 SP

- Route `/articles/{slug}`
- Contrôleur mince + classe Service
- Gestion sémantique du 404
- Vue Blade responsive
- **Story de référence**

</div>
</div>

<div class="two">
<div class="box">

### US-01 · 3 SP

- Lecture seule
- Filtre sur le statut publié
- État vide explicite
- Aucune authentification

</div>
<div class="box">

### US-06 · 5 SP

- File de modération
- Publication et dépublication
- Autorisation par rôle
- Cohérence de la liste publique

</div>
</div>

<p class="small">Estimations initiales raisonnées, sans session d'équipe ni vélocité : propositions à confirmer par planning poker.</p>

<!--
Justifier par la complexité, pas par une durée.
Rappeler que US-02 est documentée comme livrée, mais que le code est absent du dépôt : l'estimation porte sur le périmètre complet.
-->

---

# Product Backlog ordonné

<div class="compact">

| Rang | ID | User Story | SP | Priorité |
|---|---|---|---|---|
| 1 | US-02 | Lire le détail d'un article | 5 | Must |
| 2 | US-01 | Consulter la liste des articles publiés | 3 | Must |
| 3 | US-03 | Créer un compte et se connecter | 5 | Must |
| 4 | US-04 | Rédiger et soumettre un article | 8 | Must |
| 5 | US-06 | Modérer et publier les articles | 5 | Must |
| 6 | US-05 | Suivre le statut de mes articles | 3 | Should |
| 7 | US-07 | Rechercher et filtrer les articles | 5 | Could |
| 8 | US-08 | Gérer les catégories | 3 | Could |
| 9 | US-09 | Modifier ou supprimer un article | 5 | Won't |
| 10 | US-10 | Consulter le profil public d'un lauréat | 5 | Won't |

</div>

**Ordre = valeur → dépendances → readiness.**

<p class="small">US-04 (8 SP) passe avant US-08 (3 SP) : la priorité ne suit jamais la taille. US-06 suit US-04 car on ne modère que ce qui a été soumis.</p>

<!--
Expliquer les trois critères d'ordre.
Montrer deux exemples de dépendance : US-03 avant US-04, US-04 avant US-06.
-->

---

# MoSCoW : quatre catégories

| Catégorie | Signification | Conséquence |
|---|---|---|
| **Must Have** | Indispensable au produit initial utilisable | Sans elle, le MVP n'a pas de sens |
| **Should Have** | Importante mais reportable | Prévue après le socle |
| **Could Have** | Amélioration utile, non essentielle | Traitée si le contexte le permet |
| **Won't Have (this time)** | Exclue du périmètre actuel | Pourra être reconsidérée |

**Trois règles d'usage :**

- Une story appartient à **une seule** catégorie.
- « Won't » signifie **différé**, pas « abandonné ».
- Les éléments hors périmètre du produit sont distingués des reports.

<!--
MoSCoW n'est pas un simple étiquetage : c'est une décision de périmètre.
Ne pas confondre « Won't Have this time » (report) et hors périmètre (messagerie, paiement, IA).
-->

---

# MoSCoW — Must Have (26 SP)

| ID | User Story | SP | Pourquoi Must |
|---|---|---|---|
| US-01 | Consulter la liste des articles publiés | 3 | Point d'entrée : sans liste, rien n'est découvrable |
| US-02 | Lire le détail d'un article | 5 | Cœur de la valeur : transmettre le témoignage |
| US-03 | Créer un compte et se connecter | 5 | Rend la contribution possible et protège l'auteur |
| US-04 | Rédiger et soumettre un article | 8 | Alimente le blog et garantit sa durabilité |
| US-06 | Modérer et publier les articles | 5 | Sans modération, rien ne devient public |

<p class="quote">Les cinq Must forment le MVP : ils ferment la boucle de valeur, de l'inscription à la lecture.</p>

<!--
Insister sur US-06 : la modération n'est pas un confort, c'est la condition de publication.
Sans elle, US-04 produit des articles qui restent invisibles.
-->

---

# MoSCoW — Should, Could, Won't

| Catégorie | ID | User Story | SP | Justification |
|---|---|---|---|---|
| **Should** | US-05 | Suivre le statut de mes articles | 3 | Confort du contributeur, non bloquant |
| **Could** | US-07 | Rechercher et filtrer les articles | 5 | Utile quand le volume augmente |
| **Could** | US-08 | Gérer les catégories | 3 | Un référentiel initial suffit |
| **Won't** | US-09 | Modifier ou supprimer un article | 5 | Le brouillon peut être corrigé avant soumission |
| **Won't** | US-10 | Consulter le profil public d'un lauréat | 5 | L'auteur est déjà visible dans l'article |

<p class="small">Hors périmètre du produit : messagerie, paiement, réseau social, recommandations IA, synchronisation externe, mobile natif (à arbitrer).</p>

<!--
Expliquer la divergence assumée : US-05 était dans le MVP de l'atelier précédent, mais sa propre justification la décrit comme non bloquante.
Cette divergence doit être arbitrée par le PO.
-->

---

# MVP — le plus petit parcours qui ferme la boucle

<div class="chain">
<div class="step"><strong>US-03</strong><span>S'inscrire</span></div>
<div class="arrow">→</div>
<div class="step"><strong>US-04</strong><span>Rédiger, soumettre</span></div>
<div class="arrow">→</div>
<div class="step"><strong>US-06</strong><span>Modérer, publier</span></div>
<div class="arrow">→</div>
<div class="step"><strong>US-01</strong><span>Découvrir</span></div>
<div class="arrow">→</div>
<div class="step"><strong>US-02</strong><span>Lire</span></div>
</div>

**Périmètre MVP : 5 stories — 26 Story Points**

- Une fonctionnalité est Must parce que la boucle casse sans elle, pas parce qu'elle est facile.
- **Hors MVP** : US-05, US-07, US-08, US-09, US-10.

<p class="small">Le MVP n'est pas « tout ce qui existe déjà » ni « tout ce qui est simple à coder ».</p>

<!--
Faire parcourir la chaîne de valeur : sans US-06, le contenu soumis n'atteint jamais le public.
Sans US-01, l'article publié reste introuvable.
-->

---

# Sprint 1 proposé vs MVP

| Périmètre | Stories | SP | Statut |
|---|---|---|---|
| **MVP** | US-01, US-02, US-03, US-04, US-06 | 26 | Proposition à valider |
| **Sprint 1 proposé** | US-02 + US-01 | 8 | Proposition, non engagement |

**Pourquoi cette sélection ?**

- **US-02** est déjà documentée comme livrée au Sprint 1.
- **US-01** ne dépend d'aucune authentification : readiness immédiate.
- La paire **liste + détail** forme un incrément démontrable en Sprint Review.
- US-03, US-04 et US-06 (18 SP) dépendent de décisions non tranchées.

<p class="small">Aucune capacité, durée ou vélocité n'est supposée. Si le Sprint 1 reste strictement documenté, la sélection se réduit à US-02 (5 SP).</p>

<!--
Distinguer clairement MVP et Sprint 1 : un sprint ne doit pas absorber tout le MVP.
Signaler que le code étant absent du dépôt, l'incrément réel de US-02 doit être vérifié en revue.
-->

---

# Definition of Ready — prêt à démarrer

| Critère | Vérification concrète |
|---|---|
| **Format et acteur** | Les trois clauses sont présentes ; l'acteur figure dans le diagramme de cas d'utilisation |
| **Besoin et valeur** | Le PO reformule la valeur sans relire la story |
| **Critères testables** | Un test peut être écrit directement depuis chaque critère |
| **Périmètre et dépendances** | Inclusions, exclusions et dépendances listées ; aucun blocage |
| **Estimation** | Valeur ∈ {1, 2, 3, 5, 8}, consensus d'équipe, aucune heure |
| **Priorité** | Une catégorie MoSCoW renseignée par le PO |
| **Taille** | ≤ 8 SP, sinon découpage |
| **Ressources** | Routes, modèles, maquettes et règles disponibles |
| **Contraintes** | Sécurité, responsive et accessibilité identifiées |
| **Validation PO** | Statut « Prête » explicite, daté et attribué |

<p class="small">Une story qui échoue à la DoR retourne au raffinement ; elle n'entre pas dans le Sprint Backlog.</p>

<!--
Insister sur la vérifiabilité : « la story est claire » n'est pas un critère.
Chaque ligne doit pouvoir être cochée par une personne qui n'a pas participé à la rédaction.
-->

---

# Definition of Done — réellement terminé

| Critère | Vérification concrète |
|---|---|
| **Critères d'acceptation** | Démonstration en Sprint Review + tests nommés d'après les critères |
| **Tests automatisés** | Suite PHPUnit/Pest au vert, aucune régression |
| **Architecture** | Contrôleur mince, logique dans un Service, pas de requête dans la vue |
| **Sécurité** | Auth, autorisation, CSRF, XSS, SQLi, validation serveur vérifiés |
| **Responsive et accessibilité** | Mobile, tablette, bureau ; clavier, contrastes, HTML sémantique (WCAG 2.2) |
| **Cas d'erreur** | 404, accès refusé et validation échouée testés |
| **Bugs** | Aucun bug bloquant ou critique ouvert |
| **Revue de code** | Relecture par un pair ou le formateur avant fusion |
| **Documentation** | README, docs ou rapport mis à jour si le comportement change |
| **Intégration** | Fusion sur la branche `sprintN`, application démarrée, migrations à jour |

<p class="small">« Le code est écrit » n'est pas « terminé ». Une story hors DoD n'est pas comptée dans l'incrément.</p>

<!--
La DoD est un standard collectif, pas une négociation story par story.
Le processus de revue de code est proposé : aucun processus formel n'est documenté dans le dépôt.
-->

---

# DoR vs DoD

| Definition of Ready | Definition of Done |
|---|---|
| Avant le développement | Après le développement |
| Vérifie qu'une story est prête | Vérifie que le travail respecte la qualité |
| Porte sur la clarté et la préparation | Porte sur l'implémentation et la qualité |
| Utilisée au raffinement et au Planning | Utilisée pendant le sprint et en Review |
| Échec → retour au backlog | Échec → retour au Sprint Backlog |
| Responsabilité : PO avec l'équipe | Responsabilité : Developers |

<p class="quote">La DoR protège l'entrée du sprint ; la DoD protège la sortie. Ensemble, elles empêchent de démarrer flou et de finir incomplet.</p>

<!--
Ne pas présenter les deux comme des formalités : ce sont deux points de contrôle du même flux.
Un échec DoR coûte moins cher qu'un échec DoD.
-->

---

# Conclusion

- **Product Backlog** : 10 stories ordonnées, 47 Story Points, une seule source de vérité.
- **Estimation** : Fibonacci 1–2–3–5–8, effort relatif, aucune conversion en heures.
- **MoSCoW** : 5 Must (26 SP), 1 Should, 2 Could, 2 Won't.
- **MVP** : la boucle complète, de l'inscription à la lecture.
- **Sprint 1** : US-02 + US-01 (8 SP), proposition distincte du MVP.
- **Qualité** : DoR et DoD formalisées, vérifiables, à adopter par l'équipe.

<p class="small">À valider : frontière du MVP, classement de US-05, statut « en attente », rôle administrateur, et adoption de la DoR/DoD. Les estimations sont des propositions, pas des mesures.</p>

<!--
Terminer sur la prudence méthodologique : tout est traçable dans le dépôt, mais les décisions de périmètre restent au PO.
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
