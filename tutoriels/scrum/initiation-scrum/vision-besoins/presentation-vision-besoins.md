---
marp: true
theme: default
paginate: true
size: 16:9
header: "Solicode N3 — Atelier Vision Produit et User Stories"
footer: "Blog des Lauréats | Encadrant : ESSARRAJ Fouad"
style: |
  section {
    font-family: Arial, sans-serif;
    background: #ffffff;
    color: #1f2937;
    padding: 50px 70px;
  }

  section h1 {
    font-size: 40px;
    color: #0338ab;
  }

  section h2 {
    color: #2563eb;
  }

  section h3 {
    color: #0338ab;
    margin: 0 0 6px;
    font-size: 22px;
  }

  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
  }

  section.lead h1 {
    font-size: 54px;
    margin-bottom: 4px;
  }

  section.lead h3 {
    font-size: 25px;
    font-weight: normal;
    color: #2563eb;
    margin: 0 0 24px;
  }

  ul, ol {
    line-height: 1.45;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 21px;
  }

  th {
    background: #e8efff;
    color: #0338ab;
    text-align: left;
  }

  th, td {
    border: 1px solid #cbd5e1;
    padding: 6px 10px;
    vertical-align: top;
  }

  .small {
    font-size: 19px;
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
    gap: 24px;
    margin: 8px 0 22px;
  }

  .box {
    background: #f8fafc;
    border: 1px solid #dbe4f0;
    border-radius: 10px;
    padding: 12px 16px;
    font-size: 19px;
  }

  .box ul {
    margin: 6px 0 0;
    padding-left: 20px;
  }

  .box li {
    margin-bottom: 7px;
  }

  .chain {
    display: flex;
    align-items: stretch;
    gap: 10px;
    margin: 22px 0 18px;
  }

  .step {
    flex: 1;
    background: #eef4ff;
    border: 1px solid #c7d8f5;
    border-radius: 10px;
    padding: 14px;
    text-align: center;
  }

  .step strong {
    display: block;
    color: #0338ab;
    font-size: 23px;
  }

  .step span {
    font-size: 18px;
    color: #475569;
  }

  .arrow {
    display: flex;
    align-items: center;
    font-size: 30px;
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
    font-size: 52px;
    color: white;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Vision Produit & User Stories

### Blog des Lauréats — de l'idée aux besoins utilisateurs

- **Atelier** : UA.351.11 — Initiation à la démarche Agile et cadre Scrum
- **Apprenant** : Marwan bouhamid
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Date** : 26 novembre 2026

<!--
Présenter l'atelier : il applique la méthode au projet réel Blog des Lauréats, et non à l'exemple TodoList.
Annoncer le fil : vision, personas, user stories, MVP.
-->

---

# Le projet en bref

| Élément | Description |
|---|---|
| **Produit** | Plateforme web communautaire du Blog des Lauréats |
| **Public** | Lauréats de Solicode Tanger et apprenants actuels |
| **Problème** | Des témoignages utiles, mais dispersés et peu structurés |
| **Promesse** | Centraliser et valoriser les parcours sous forme d'articles lisibles et modérés |
| **Acteurs** | Lauréat contributeur, apprenant/visiteur, administrateur |

<p class="small">Source : README, note de cadrage et diagramme de cas d'utilisation du dépôt.</p>

<!--
Rappeler le contexte Solicode. Le problème est documenté : centraliser les témoignages pour les partager entre promotions.
Ne pas parler technique ici : le sujet est le besoin utilisateur.
-->

---

# Pourquoi une Vision Produit ?

- Donne un **cap commun** à l'équipe et au Product Owner.
- Aide à **prioriser** les fonctionnalités.
- Guide les **choix fonctionnels** et évite la dérive du périmètre.
- Reste stable, même lorsque les solutions techniques changent.

> **Formule de référence** : Pour [utilisateurs] qui [besoin], le [produit] est [catégorie] qui [bénéfice]. Contrairement à [alternative], il [différenciation].

<!--
La vision n'est pas un cahier des charges détaillé : elle explique pourquoi le produit existe et pour qui.
Elle sert de filtre : une fonctionnalité qui ne sert pas la vision n'entre pas dans le MVP.
-->

---

# Vision Produit

> **Pour les lauréats de Solicode Tanger qui souhaitent transmettre leur expérience, et pour les apprenants qui cherchent des exemples concrets de parcours professionnels, le Blog des Lauréats est une plateforme web communautaire qui centralise et valorise les témoignages des anciens apprenants sous forme d'articles lisibles et modérés.**

- **Centraliser** : un espace unique au lieu de témoignages dispersés.
- **Valoriser** : donner de la visibilité aux parcours et aux compétences.
- **Durer** : conserver les expériences pour les promotions suivantes.

<p class="small">La vision ne promet ni réseau social, ni messagerie, ni paiement, ni recommandation par IA : ces éléments sont hors périmètre.</p>

<!--
Lire l'énoncé lentement. Insister sur les deux publics : celui qui produit le contenu et celui qui le consomme.
La différenciation est l'ancrage dans la communauté Solicode et la modération des contenus, pas une supériorité technique.
-->

---

# Utilisateurs cibles

| Acteur | Rôle | Besoin principal | Statut |
|---|---|---|---|
| **Lauréat contributeur** | Rédige, publie et gère ses articles | Partager son parcours et valoriser son profil | Primaire |
| **Apprenant / visiteur** | Consulte les articles et les profils | Découvrir des parcours concrets | Primaire |
| **Administrateur** | Modère les articles et gère les catégories | Garantir la qualité des contenus | Secondaire |

<p class="small">Le formateur et le recruteur apparaissent dans d'anciens documents supprimés ; ils ne figurent plus dans le diagramme de cas d'utilisation actuel. Leur réintégration reste à valider.</p>

<!--
Distinguer acteurs primaires et secondaire. L'administrateur ne produit pas de valeur directement, mais il sécurise la publication.
Signaler honnêtement que formateur et recruteur ne sont pas confirmés dans l'état actuel du dépôt.
-->

---

# Persona 1 — Yassine, le lauréat contributeur

| Dimension | Description |
|---|---|
| **Profil** | Ancien apprenant de Solicode, développeur junior (hypothèse) |
| **Objectifs** | Transmettre son parcours, valoriser ses compétences, aider les apprenants |
| **Besoins** | Éditeur simple, brouillon, soumission, suivi du statut, confort mobile |
| **Frustrations** | Témoignages dispersés, outils complexes, statut de publication inconnu |
| **Contraintes** | Temps limité, compétences rédactionnelles variables (hypothèses) |
| **Motivation** | Transmission, reconnaissance et visibilité professionnelle |

<p class="quote">« Je veux raconter mon parcours simplement, sans que la technique me bloque. » — citation fictive</p>

<!--
Yassine représente la production de contenu. Son parcours critique : s'inscrire, rédiger, soumettre, suivre le statut.
Rappeler que le nom et les habitudes sont fictifs : aucun entretien utilisateur n'est présent dans le dépôt.
-->

---

# Persona 2 — Salma, l'apprenante

| Dimension | Description |
|---|---|
| **Profil** | Apprenante actuelle à Solicode Tanger (niveau : hypothèse) |
| **Objectifs** | Comprendre les parcours, choisir une spécialité, préparer son insertion |
| **Besoins** | Liste claire, lecture mobile, catégories, informations fiables sur l'auteur |
| **Frustrations** | Conseils génériques, informations éparpillées, contenus obsolètes |
| **Contraintes** | Temps entre les cours, consultation mobile, niveau technique variable |
| **Motivation** | Réussir sa formation et construire un projet professionnel réaliste |

<p class="quote">« Je cherche des exemples de personnes parties du même point que moi. » — citation fictive</p>

<!--
Salma représente la consultation. Son parcours critique : ouvrir la liste, choisir un article, le lire confortablement.
Le contraste avec Yassine est volontaire : produire versus consommer, reconnaissance versus orientation.
-->

---

# User Stories : structure et utilité

**Format canonique :**

> **En tant que** [type d'utilisateur], **je veux** [action ou besoin] **afin de** [bénéfice].

**Pourquoi ce format ?**

- Il replace le besoin du point de vue de l'**utilisateur**, pas de la technique.
- Il rend chaque fonctionnalité **testable** grâce aux critères d'acceptation.
- Il permet de **prioriser** et de découper le travail en incréments.

<p class="small">Une User Story n'est pas une tâche technique : « créer une table SQL » n'est pas une User Story.</p>

<!--
Expliquer la différence entre besoin utilisateur et tâche de réalisation.
Les critères d'acceptation transforment la story en contrat vérifiable.
-->

---

# Les cinq User Stories majeures

| ID | User Story | Persona | Priorité |
|---|---|---|---|
| **US-01** | Consulter la liste des articles publiés | Salma | Haute |
| **US-02** | Lire le détail d'un article | Salma | Haute |
| **US-03** | Créer un compte et se connecter | Yassine | Moyenne |
| **US-04** | Rédiger et soumettre un article | Yassine | Haute |
| **US-05** | Suivre le statut de mes articles | Yassine | Moyenne |

<p class="small">Chaque story est rattachée à un persona et à une fonctionnalité du MVP. Les priorités sont des propositions à valider par le Product Owner.</p>

<!--
Parcourir les cinq stories : deux pour la consultation, trois pour la contribution.
US-03 est une story habilitante : elle ne crée pas de valeur seule, mais rend US-04 possible.
-->

---

# Critères d'acceptation — exemples

<div class="two">
<div class="box">

### US-02 · Lire un article

- Article publié → titre, contenu, auteur, catégorie et date affichés.
- Slug inconnu ou article non publié → page 404, aucun contenu révélé.
- Mobile ou bureau → lecture sans défilement horizontal.

</div>
<div class="box">

### US-04 · Rédiger et soumettre

- Brouillon enregistré → visible uniquement dans l'espace du lauréat.
- Article soumis → statut « en attente », absent de la liste publique.
- Champ obligatoire manquant → erreurs affichées, aucun enregistrement.

</div>
</div>

<p class="small">Format Gherkin : Étant donné / Quand / Alors. Chaque critère est observable et testable.</p>

<!--
Montrer que les critères sont concrets : on peut les vérifier sans interprétation.
Le statut « en attente de publication » est une proposition pour matérialiser la modération ; il doit être validé.
-->

---

# MVP — Fonctionnalités essentielles

| Fonctionnalité | US | Pourquoi elle est essentielle |
|---|---|---|
| Liste des articles publiés | US-01 | Point d'entrée et découverte du contenu |
| Lecture du détail + 404 | US-02 | Cœur de la valeur : transmettre le témoignage |
| Inscription et connexion | US-03 | Rend la contribution possible et protège l'auteur |
| Rédaction, brouillon, soumission | US-04 | Alimente le blog et garantit sa durabilité |
| Suivi du statut | US-05 | Donne de la visibilité au contributeur |

<p class="small">Socle de support : modération et publication par l'administrateur, référentiel de catégories existantes.<br/>
Parcours minimal : s'inscrire → rédiger → soumettre → publier → lire.</p>

<!--
Le MVP n'est pas « tout ce qui existe déjà » : c'est le plus petit parcours qui ferme la boucle de valeur.
La modération est une fonction de support indispensable : sans elle, aucun contenu ne devient public.
-->

---

# Hors MVP — Évolutions futures

| Fonctionnalité | Pourquoi elle attend |
|---|---|
| Recherche et filtrage par catégorie | Utiles quand le volume d'articles augmente |
| Profils publics des lauréats | L'auteur est déjà visible dans l'article |
| Gestion complète des catégories | Un référentiel initial suffit au lancement |
| Modification d'articles publiés | Le brouillon peut être corrigé avant soumission |
| Gestion des utilisateurs par l'admin | Le volume initial ne la justifie pas |
| Version Android native (NativePHP) | Le web responsive couvre le besoin initial ; à arbitrer |

<p class="small">Hors périmètre explicite : messagerie, paiement, réseau social complexe, recommandation par IA, synchronisation externe.</p>

<!--
Justifier le report par la valeur, pas par la difficulté technique.
Signaler la contradiction entre la note de cadrage (mobile natif exclu) et la stack technique (NativePHP) : décision à prendre.
-->

---

# De la vision au MVP

<div class="chain">
<div class="step"><strong>Vision</strong><span>Pourquoi ?</span></div>
<div class="arrow">→</div>
<div class="step"><strong>Personas</strong><span>Pour qui ?</span></div>
<div class="arrow">→</div>
<div class="step"><strong>User Stories</strong><span>Quoi ?</span></div>
<div class="arrow">→</div>
<div class="step"><strong>MVP</strong><span>Combien ?</span></div>
</div>

- Chaque User Story se rattache à un persona identifié.
- Chaque fonctionnalité du MVP répond à un besoin utilisateur documenté.
- Une fonctionnalité sans lien avec la vision sort du périmètre ou attend une version future.

<!--
Insister sur la traçabilité : rien dans le MVP ne doit être là « parce que c'est facile » ou « parce que c'est déjà codé ».
C'est ce fil qui permet de défendre les choix devant le Product Owner.
-->

---

# Conclusion

- **Vision** : centraliser et valoriser les parcours des lauréats pour la communauté Solicode.
- **Personas** : deux besoins contrastés, produire un témoignage et en consulter un.
- **User Stories** : cinq besoins majeurs, quinze critères d'acceptation testables.
- **MVP** : un parcours complet, de l'inscription à la lecture, sans fonctionnalités de confort.

<p class="small">À valider avec le Product Owner : l'ordre des priorités, la frontière du MVP et le statut « en attente de publication ».<br/>
Les personas et leurs habitudes sont des hypothèses : aucun entretien utilisateur n'est disponible dans le dépôt.</p>

### Merci de votre attention.

<!--
Terminer sur la prudence méthodologique : le travail est adossé au dépôt, mais les personas et priorités restent à valider.
Ouvrir les questions.
-->
