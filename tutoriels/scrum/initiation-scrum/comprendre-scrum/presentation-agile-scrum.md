---
marp: true
theme: default
paginate: true
header: "Solicode N3 - Projet Imitation : Blog des lauréats"
footer: "Encadrant : ESSARRAJ Fouad | Solicode Tanger"
style: |
  section {
    font-family: Arial, sans-serif;
    background: #ffffff;
    color: #1f2937;
    padding: 60px 80px;
  }

  section h1 {
    font-size: 42px;
    color: #0338ab;
  }

  section h2 {
    color: #2563eb;
  }

  section h3 {
    color: #0338ab;
  }

  section.lead {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: left;
  }

  section.lead h1 {
    font-size: 58px;
    margin-bottom: 4px;
  }

  section.lead h3 {
    font-size: 26px;
    font-weight: normal;
    color: #2563eb;
    margin-top: 0;
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

  ul, ol {
    line-height: 1.5;
  }

  table {
    width: 100%;
    border-collapse: collapse;
    font-size: 23px;
  }

  th {
    background: #e8efff;
    color: #0338ab;
    text-align: left;
  }

  th, td {
    border: 1px solid #cbd5e1;
    padding: 8px 12px;
    vertical-align: top;
  }

  blockquote {
    border-left: 6px solid #2563eb;
    background: #f1f5ff;
    margin: 16px 0 0;
    padding: 8px 16px;
    font-size: 24px;
  }

  .flow {
    font-size: 24px;
    text-align: center;
    background: #f1f5ff;
    border: 1px solid #cbd5e1;
    border-radius: 8px;
    padding: 12px;
    margin: 16px 0;
  }

  .note {
    font-size: 22px;
    color: #475569;
  }
---

<!-- _class: lead -->
<!-- _paginate: false -->

# Agile & Scrum
### De la théorie à la pratique sur le projet Blog des Lauréats

- **Apprenant** : Marwan bouhamid
- **Encadrant** : ESSARRAJ Fouad
- **Établissement** : Solicode Tanger
- **Domaine** : Développement Web
- **Date** : 2026-11-26

<!--
Bonjour à toutes et à tous. J'espère que vous allez bien.

Aujourd'hui, je vais vous présenter un sujet important dans la gestion des projets informatiques : l'approche Agile et le cadre Scrum.

غادي نحاول نشرح ليكم شنو الفرق بين هاد المفاهيم، علاش كنستعملوهم، وكيفاش نقدروا نطبقوهم على notre projet technique, Blog des Lauréats.

Commençons !
-->

---

# Pourquoi une méthode ?

- Un projet informatique ne commence pas par l'écriture du code.
- Il faut clarifier : le besoin, l'équipe, les priorités et le suivi.
- Sans organisation claire : retards, bugs, problèmes de communication.
- Risque final : un produit qui ne répond pas aux besoins du client.
- D'où l'existence de plusieurs méthodes de gestion de projet.

<!--
Avant de commencer, خاصنا نفهمو علاش أصلاً كنحتاجو une méthode de gestion de projet.

فأي projet informatique، ماشي غير كنبدأو نكتبو le code مباشرة. خاصنا نعرفو شنو بغينا نبنيو، شكون غادي يخدم، شنو هي les priorités، وكيفاش غادي نتبعو التقدم ديال المشروع.

إلا ما كانتش عندنا organisation claire، ممكن نلقاو des retards, des bugs, des problèmes de communication، وفي الأخير نخرجو بواحد produit ما كيلبيش les besoins du client.

لهذا كاينين plusieurs méthodes باش ننظمو الخدمة ديالنا.
-->

---

# Le cycle en V

- Une approche **séquentielle** : chaque phase suit la précédente.
- Une phase doit être terminée avant de passer à la suivante.

<div class="flow">
Analyse des besoins → Conception → Développement → Tests → Validation
</div>

**Avantages** : organisation, clarté, documentation.

**Limites** : changement tardif coûteux, effet tunnel.

<!--
أول méthode عندنا هي le cycle en V.

هاد الطريقة كتخدم بطريقة séquentielle، يعني كل مرحلة كتجي من بعد المرحلة اللي قبل منها.

كنبدأو بـ l'analyse des besoins، من بعد la conception، ثم le développement، ومن بعد كنمشيو للاختبارات، وفي الأخير la validation.

يعني ببساطة، خاصنا نكملو مرحلة باش ننتاقلو للمرحلة اللي من بعدها.

هاد الطريقة عندها des avantages، بحال التنظيم والوضوح والتوثيق.

ولكن عندها حتى des limites. مثلاً، إلا اكتشفنا فالأخير أن العميل باغي يبدل شي حاجة، التغيير ممكن يكون مكلف وصعيب، حيث أغلب الخدمة دازت من قبل.

وهنا كنقدرو نواجهو ما يسمى بـ l'effet tunnel: العميل ما كيشوفش النتيجة الحقيقية حتى كيوصل المشروع لمراحل متقدمة أو للنهاية.
-->

---

# L'approche Agile

- Travailler par **petits cycles** (itérations courtes).
- Sortir un **résultat utilisable** à chaque cycle.
- Observer, écouter les retours, puis améliorer.
- S'adapter aux changements et détecter les problèmes tôt.
- **Agile ≠ absence de plan** : le plan est ajusté en continu.

> Exemple : commencer par « consulter un article », puis ajouter les autres fonctionnalités selon les priorités.

<!--
باش نتجاوزو بعض هاد المشاكل، كاينة l'approche Agile.

Agile هي approche qui permet de travailler par petits cycles، يعني ما كنستناوش حتى نساليو المشروع كامل باش نوريو النتيجة.

كنقسمو الخدمة لمراحل قصيرة، وفكل مرحلة كنحاولو نخرجو بشي résultat utilisable.

من بعد كنشوفو النتيجة، كنسمعو les retours، وكنحسنو الخدمة ديالنا.

مثلاً، فـ Blog des Lauréats، نقدروا نبدأو بميزة بسيطة بحال consulter un article، ومن بعد نزيدو fonctionnalités أخرى حسب les priorités.

إذن، Agile كتساعدنا نتأقلمو مع les changements ونكتاشفو المشاكل بكري.

ولكن خاصنا نفهمو واحد النقطة: Agile ماشي معناها نخدمو بلا plan. بالعكس، كاين التخطيط، ولكن كنقدرو نعدلوه حسب تطور المشروع.
-->

---

# Cycle en V vs Agile

| Critère | Cycle en V | Agile |
|---|---|---|
| Planification | Détaillée au départ | Progressive |
| Changements | Difficiles et coûteux | Intégrés, priorités ajustées |
| Livraison | Souvent à la fin | Incréments réguliers |
| Feedback client | Tardif | Continu |

<p class="note">Aucune méthode n'est « mauvaise » : tout dépend du contexte du projet.</p>

<!--
دابا نقدروا نقارنو بين le cycle en V و l'approche Agile.

فـ cycle en V، التخطيط كيكون غالباً من البداية، والتغييرات كتكون صعيبة ومكلفة نسبياً.

أما فـ Agile، كنخططو تدريجياً، وكنقدرو نبدلو les priorités حسب les besoins.

حتى طريقة livraison مختلفة: فـ cycle en V، غالباً كنستناو حتى النهاية، أما فـ Agile كنقدمو des incréments régulièrement.

هادشي ما كيعنيش أن cycle en V طريقة سيئة. كل méthode عندها contexte ديالها.

ولكن بالنسبة للمشاريع اللي فيها تغييرات مستمرة، Agile كتقدر تكون مناسبة أكثر.
-->

---

# Le Manifeste Agile

**2001 — quatre valeurs fondamentales**

| Valeur prioritaire | Plutôt que |
|---|---|
| Les individus et les interactions | les processus et les outils |
| Un logiciel opérationnel | une documentation exhaustive |
| La collaboration avec le client | la négociation contractuelle |
| L'adaptation au changement | le suivi rigide d'un plan |

<p class="note">Documentation et planning restent utiles : la priorité va à la collaboration, au résultat et à l'adaptation.</p>

<!--
فـ 2001، مجموعة من développeurs دارو ما يسمى بـ Le Manifeste Agile.

هاد manifeste فيه quatre valeurs principales.

La première : les individus et les interactions plutôt que les processus et les outils.
يعني التواصل بين الناس والتعاون مهمين أكثر من الاعتماد فقط على الأدوات.

La deuxième : un logiciel opérationnel plutôt qu'une documentation exhaustive.
يعني الأفضل يكون عندنا logiciel كيخدم فعلاً، ماشي غير documentation كبيرة بلا نتيجة عملية.

La troisième : la collaboration avec le client plutôt que la négociation contractuelle.
يعني خاصنا نبقاو على تواصل مع العميل وناخدو feedback ديالو.

La quatrième : l'adaptation au changement plutôt que le suivi rigide d'un plan.
يعني إلا تبدلات les besoins، خاصنا نكونو قادرين نتأقلمو.

وخاصنا نعرفو أن هاد القيم ما كتعنيش أننا نحيدو documentation أو planning، ولكن كتعطي الأولوية للتعاون والنتيجة والتكيف.
-->

---

# Scrum

- **Agile** = valeurs et principes.
- **Scrum** = cadre de travail pour appliquer ces principes.
- Trois responsabilités, cinq événements, trois artefacts.
- Scrum ne choisit ni les technologies ni la façon d'écrire le code.
- Il organise le travail et la collaboration de l'équipe.

| 3 responsabilités | 5 événements | 3 artefacts |
|---|---|---|
| Product Owner | Sprint | Product Backlog |
| Scrum Master | Sprint Planning | Sprint Backlog |
| Developers | Daily Scrum, Review, Retrospective | Increment |

<!--
دابا وصلنا لـ Scrum.

أول حاجة، خاصنا نفرقو بين Agile و Scrum.

Agile هي approche فيها valeurs et principes، أما Scrum فهو un cadre de travail كيعاوننا نطبقو هاد الأفكار بطريقة منظمة.

Scrum كيعتمد على ثلاثة éléments principaux : trois responsabilités، cinq événements، et trois artefacts.

وواحد الحاجة مهمة: Scrum ما كيحددش لينا شنو هي technologie اللي خاصنا نستعملو، ولا كيفاش خاصنا نكتبو le code.

هو كينظم طريقة العمل والتعاون داخل الفريق.
-->

---

# Les trois piliers de Scrum

| Pilier | Signification |
|---|---|
| **Transparence** | L'information est claire et comprise par toute l'équipe. |
| **Inspection** | Le travail et les résultats sont examinés régulièrement. |
| **Adaptation** | L'équipe ajuste sa façon de travailler si nécessaire. |

> Blog des Lauréats : suivre les tâches sur GitHub, faire des points réguliers, puis réajuster les priorités.

<p class="note">Les trois piliers fonctionnent ensemble.</p>

<!--
Scrum كيعتمد على ثلاثة piliers fondamentaux.

الأول هو la transparence، يعني المعلومات ديال المشروع خاصها تكون واضحة ومفهومة عند جميع أعضاء الفريق.

الثاني هو l'inspection، يعني خاصنا نراجعو العمل ديالنا والنتائج بانتظام باش نعرفو واش كلشي غادي مزيان.

الثالث هو l'adaptation، يعني إلا اكتشفنا شي problème أو شي حاجة خاصها التغيير، خاصنا نعدلو الطريقة ديال العمل.

مثلاً فـ Blog des Lauréats، نقدروا نستعملو GitHub باش نبينو les tâches، ونديرو مراجعة للتقدم، ومن بعد نبدلو les priorités إلا كان ضروري.

هاد الثلاثة خاصهم يخدمو مع بعضياتهم.
-->

---

# L'équipe Scrum

| Product Owner | Scrum Master | Developers |
|---|---|---|
| Maximise la valeur du produit | Facilite le processus Scrum | Réalise le produit |
| Gère et priorise le Product Backlog | Lève les obstacles | Organise le travail du Sprint |
| Décide « quoi » et « pourquoi » | Garantit le cadre et les événements | Garantit la qualité de l'incrément |

- Équipe **pluridisciplinaire** : toutes les compétences nécessaires.
- Équipe **auto-gérée** : elle décide comment répartir le travail.
- **Pas de chef hiérarchique** imposé par Scrum.

<!--
فـ Scrum، عندنا une équipe Scrum فيها trois responsabilités principales.

الأولى هي Product Owner، والثانية Scrum Master، والثالثة Developers.

كل واحد عندو مسؤوليات مختلفة، ولكن كاملين كيخدمو على نفس الهدف، اللي هو خلق de la valeur pour le produit.

الفريق خاصو يكون pluridisciplinaire، يعني فيه les compétences اللي محتاجها المشروع، ويكون auto-géré، يعني الأعضاء كينظمو الخدمة ديالهم وكيقررو كيفاش يقسمو العمل.

Scrum ما كيفرضش وجود chef hiérarchique داخل الفريق.
-->

---

# Le Product Owner

- Responsable de **maximiser la valeur du produit**.
- Gère le **Product Backlog** : liste ordonnée des besoins.
- Priorise les fonctionnalités selon leur importance pour l'utilisateur.
- Se concentre sur **quoi** construire et **pourquoi**, pas sur le code.

> Blog des Lauréats : priorité à « consulter un article », puis « soumettre un article » et « modérer les publications ».

<!--
أول مسؤولية هي Product Owner.

الـ Product Owner مسؤول على maximiser la valeur du produit، يعني كيحاول يضمن أن الفريق كيخدم على fonctionnalités اللي عندها أهمية كبيرة بالنسبة للمستخدم.

هو كذلك مسؤول على Product Backlog، يعني اللائحة المرتبة ديال الحاجات اللي ممكن نخدمو عليهم فالمشروع.

مثلاً، فـ Blog des Lauréats، ممكن يعطي الأولوية لميزة consulter un article، حيث الزائر خاصو يقدر يشوف المقالات بسهولة.

ومن بعد ممكن يعطي الأولوية لميزات أخرى بحال soumettre un article أو modérer les publications.

يعني باختصار، Product Owner كيركز على شنو خاصنا نبنيو وعلاش، ماشي كيفاش نكتبو le code.
-->

---

# Le Scrum Master

- **Pas un chef de projet**, pas un manager qui donne des ordres.
- Aide l'équipe à comprendre et à appliquer Scrum correctement.
- Aide à lever les **obstacles** qui bloquent la progression.
- Améliore la façon de travailler de l'équipe.
- Veille à ce que chaque événement ait un objectif clair.

> Le Scrum Master est un **facilitateur**.

<!--
ثاني مسؤولية هي Scrum Master.

الـ Scrum Master ماشي chef de projet وماشي manager كيعطي الأوامر للـ développeurs.

الدور ديالو هو يساعد الفريق يفهم ويطبق Scrum بطريقة صحيحة.

مثلاً، إلا كان الفريق عندو obstacle كيمنعو من التقدم، Scrum Master كيساعد باش يتجاوز هاد المشكل.

وكذلك كيساعد الفريق يحسن طريقة العمل ديالو، وكيحرص أن les événements ديال Scrum يكون عندهم هدف واضح.

يعني نقدروا نقولو أن Scrum Master هو facilitateur، كيساعد الفريق يخدم بطريقة فعالة.
-->

---

# Les Developers

- Réalisent l'**Increment** du produit.
- Organisent eux-mêmes le travail à l'intérieur du Sprint.
- Responsables de la **qualité** de ce qui est livré.
- Respectent la **Definition of Done**.

> Blog des Lauréats : modèle Article, routes, contrôleurs, vues Blade et tests.

<!--
ثالث مسؤولية هي les Developers.

هما الأشخاص اللي كيقومو بإنجاز le produit، ولكن الدور ديالهم ماشي غير يكتبو le code.

هما كذلك مسؤولين على تنظيم العمل داخل Sprint، وعلى جودة النتيجة اللي غادي يسلمو.

مثلاً، فـ Blog des Lauréats، يقدرو يخدمو على le modèle Article، les routes، les contrôleurs، les vues Blade، والاختبارات.

وخاصهم يتأكدو أن الخدمة كتوافق Definition of Done.

يعني المسؤولية ديالهم هي إنتاج un incrément utilisable avec la qualité attendue.
-->

---

# Les cinq événements Scrum

| Événement | Rôle | Durée / fréquence |
|---|---|---|
| **Sprint** | Période de réalisation d'un objectif | 1 mois maximum |
| **Sprint Planning** | Planifier le travail du Sprint | Début du Sprint |
| **Daily Scrum** | Synchroniser l'équipe | 15 min, chaque jour ouvré |
| **Sprint Review** | Inspecter le produit et collecter du feedback | Fin du Sprint |
| **Sprint Retrospective** | Améliorer la façon de travailler | Fin du Sprint |

<!--
دابا غادي نشوفو les cinq événements de Scrum.

أولاً، le Sprint، وهو الفترة اللي كيخدم فيها الفريق على تحقيق هدف معين. المدة ديالو شهر واحد أو أقل.

ثانياً، Sprint Planning، وفيه الفريق كيخطط شنو غادي يخدم خلال Sprint.

ثالثاً، Daily Scrum، وهو اجتماع قصير ديال 15 minutes كل يوم عمل، باش الفريق يراجع التقدم ديالو.

رابعاً، Sprint Review، وفيها كنشوفو شنو تحقق فـ Sprint وكنجمعو feedback.

وأخيراً، Sprint Retrospective، وفيها الفريق كيراجع كيفاش خدم، وشنو يقدر يحسن فالمستقبل.

هاد الأحداث كلها عندها أهداف مختلفة، وغادي نشرح بعضها بالتفصيل فالسلايدات الجاية.
-->

---

# Sprint Planning et Sprint Goal

**Trois questions auxquelles répond le Sprint Planning :**

| Question | Réponse |
|---|---|
| Pourquoi ce Sprint est-il important ? | **Sprint Goal** |
| Que peut-on réaliser ? | Éléments choisis dans le Product Backlog |
| Comment allons-nous le réaliser ? | Plan de travail → **Sprint Backlog** |

> Exemple : livrer une page de consultation d'article responsive.

<!--
فبداية كل Sprint، كنديرو Sprint Planning.

هاد الاجتماع كيجاوب على trois questions.

Première question : Pourquoi ce Sprint est important ?
الجواب كيكون هو Sprint Goal، يعني الهدف الرئيسي ديال Sprint.

Deuxième question : Qu'est-ce qu'on peut réaliser ?
هنا الفريق كيختار les éléments اللي يقدر يخدم عليهم من Product Backlog.

Troisième question : Comment on va réaliser ce travail ?
هنا كنحددو le plan de travail اللي غادي يكون داخل Sprint Backlog.

مثلاً، فـ Blog des Lauréats، ممكن يكون الهدف ديال Sprint هو تطوير صفحة consultation d'un article تكون responsive.

هاد المثال غير توضيحي باش نفهمو كيفاش كنحددو Sprint Goal.
-->

---

# Daily Scrum

- **15 minutes**, chaque jour ouvré.
- Les Developers se synchronisent et vérifient la progression vers le **Sprint Goal**.
- Chacun partage son avancement et ses éventuels obstacles.
- Ce n'est **pas** un rapport au manager.
- Les problèmes longs se règlent **après** la réunion, avec les personnes concernées.

> « J'ai terminé la route de consultation d'article, mais j'ai un problème avec l'affichage mobile. »

<!--
من بعد عندنا Daily Scrum.

هو اجتماع قصير كيكون لمدة 15 minutes، وكل يوم عمل، والهدف ديالو هو أن Developers يتواصلو ويشوفو واش باقيين متجهين نحو Sprint Goal.

مثلاً، واحد développeur يقدر يقول: « J'ai terminé la route de consultation d'article, mais j'ai un problème avec l'affichage mobile. »

يعني كيشارك التقدم ديالو والمشكل اللي لقا.

ولكن Daily Scrum ماشي اجتماع باش المدير يراقب كل واحد، وماشي ضروري نحلّو فيه جميع المشاكل.

إلا كان شي problème كيحتاج وقت، نقدروا نهضرو عليه من بعد مع الأشخاص المعنيين.
-->

---

# Sprint Review vs Sprint Retrospective

| | Sprint Review | Sprint Retrospective |
|---|---|---|
| **Focus** | Le produit | L'équipe et sa façon de travailler |
| **Objectif** | Montrer le résultat, collecter du feedback | Identifier ce qui marche et ce qu'il faut améliorer |
| **Résultat** | Backlog adapté | Actions d'amélioration concrètes |

**Pour retenir :**

- Review = on examine le **produit**.
- Retrospective = on examine la **façon de travailler** de l'équipe.

<!--
هنا عندنا جوج événements اللي ممكن يتخلطو على بعضياتهم: Sprint Review و Sprint Retrospective.

ولكن الفرق بيناتهم بسيط.

Sprint Review كتكون مركزة على le produit.

يعني كنشوفو شنو تدار فـ Sprint، كنقدمو النتيجة، وكنجمعو feedback من les parties prenantes.

مثلاً، نعرضو صفحة article على Product Owner وناخدو الملاحظات ديالو.

أما Sprint Retrospective فهي مركزة على l'équipe et sa manière de travailler.

يعني كنناقشو شنو خدم مزيان، شنو ما خدمش، وشنو خاصنا نحسنو فـ Sprint القادم.

مثلاً، ممكن نكتاشفو أن tests كيتدارو متأخر، ونتافقو نديروهم بشكل مستمر.

إذن، باش نتفكرو الفرق بسهولة:

Review = كنراجعو المنتج.

Retrospective = كنراجعو طريقة العمل ديال الفريق.
-->

---

# Les trois artefacts

| Artefact | Contenu | Engagement |
|---|---|---|
| **Product Backlog** | Liste ordonnée de tous les besoins du produit | Product Goal |
| **Sprint Backlog** | Travail choisi pour le Sprint + plan de réalisation | Sprint Goal |
| **Increment** | Résultat réel, utilisable, produit pendant le Sprint | Definition of Done |

<p class="note">Les engagements donnent un cap et un niveau de qualité communs.</p>

<!--
Scrum فيه trois artefacts principaux.

الأول هو Product Backlog، وهي اللائحة المرتبة ديال جميع الحاجات اللي ممكن نحتاجوها فالمشروع.

الثاني هو Sprint Backlog، وهو العمل اللي اختارو الفريق باش يخدم عليه فـ Sprint الحالي، مع الخطة ديال الإنجاز.

الثالث هو Increment، وهو النتيجة الفعلية اللي خرج بها الفريق وكتكون utilisable.

كل artefact عندو engagement ديالو.

Product Backlog مرتبط بـ Product Goal، Sprint Backlog مرتبط بـ Sprint Goal، وIncrement مرتبط بـ Definition of Done.

هاد engagements كيساعدونا نعرفو شنو هو الهدف وشنو هي النتيجة اللي وصلنا ليها.
-->

---

# Definition of Done et Increment

- La **Definition of Done** = critères qu'une fonctionnalité doit respecter pour être considérée comme terminée.
- Avoir écrit du code ne suffit pas.
- Si la fonctionnalité ne respecte pas la DoD, elle ne fait **pas** partie de l'Increment.

**Exemple pour une page article :**

- Titre, contenu et nom de l'auteur affichés.
- Affichage correct sur mobile et desktop.
- Cas « article introuvable » géré.
- Tests exécutés avec succès.

<!--
دابا غادي نشرحو واحد المفهوم مهم بزاف، وهو Definition of Done.

هي مجموعة ديال critères اللي خاص الخدمة تحترمهم باش نعتابروها terminée.

حيت ماشي أي حاجة كتبنا فيها le code معناها ساليناها.

مثلاً، فـ Blog des Lauréats، إلا خدمنا صفحة ديال article، خاصنا نتأكدو أن العنوان والمحتوى واسم الكاتب باينين، وأن الصفحة خدامة على mobile وdesktop، وأن حالة article غير موجود كتتعالج بطريقة صحيحة، وأن الاختبارات دازت.

هاد المعايير غير مثال مقترح للمشروع.

إلا كانت الخدمة ما كتوافقش Definition of Done، ما نعتابروهاش جزء من Increment.

يعني Definition of Done كتخلينا نتافقو على معنى كلمة « terminé »، وكتضمن واحد المستوى مشترك ديال الجودة.
-->

---

# Application au Blog des Lauréats

**Objectif** : permettre aux lauréats de partager leurs parcours et aux visiteurs de les consulter facilement.

- **Product Backlog** : consulter la liste des articles, lire un article, soumettre un article, modérer les publications.
- **Sprint Goal** : livrer une page de consultation d'article responsive.
- **Travail des Developers** : modèle Article, route, contrôleur, vue Blade, tests.
- **Vérification** : la Review confirme que le résultat respecte la Definition of Done.

<p class="note">Ces éléments sont des exemples illustratifs, pas des engagements officiels du projet.</p>

<!--
دابا وصلنا للتطبيق العملي ديال المفاهيم على projet technique ديالنا، Blog des Lauréats.

الهدف من المشروع هو permettre aux lauréats de partager leurs parcours et aux visiteurs de les consulter facilement.

باش نطبقو Scrum، نقدروا نحددو Product Backlog فيه plusieurs fonctionnalités، بحال consulter la liste des articles، lire un article، soumettre un article، et modérer les publications.

ومن بعد نختارو بعض العناصر اللي غادي نخدمو عليهم فـ Sprint معين.

مثلاً، نقدروا نحددو Sprint Goal وهو livrer une page de consultation d'article responsive.

الفريق يقدر يخدم على le modèle Article، la route، le contrôleur، la vue Blade، والاختبارات.

وفي الأخير، كنراجعو النتيجة وكنشوفو واش كتوافق Definition of Done.

مهم نوضح أن هاد العناصر هي أمثلة توضيحية لكيفاش يمكن تطبيق Scrum على المشروع، وماشي كلها engagements رسمية متفق عليها من طرف الفريق.
-->

---

# Conclusion

- **Agile** : approche pour s'adapter aux changements et avancer progressivement.
- **Scrum** : cadre organisé pour structurer le travail de l'équipe.
- Trois piliers, trois responsabilités, cinq événements, trois artefacts.
- L'objectif n'est pas seulement de terminer des tâches.
- L'objectif est de livrer un produit **utile**, avec de la **valeur** pour les utilisateurs.

<!--
Pour conclure، اليوم تعرفنا على الفرق بين l'approche Agile و le cadre Scrum.

شفنا أن Agile كتساعدنا نتأقلمو مع التغييرات ونخدمو بطريقة progressive، وScrum كيعطينا un cadre organisé باش ننظمو الخدمة ديال الفريق.

وتعرفنا كذلك على les trois piliers، les trois responsabilités، les cinq événements، et les trois artefacts.

وأهم حاجة هي أن الهدف ماشي غير نكملو les tâches، ولكن نخرجو بمنتج عندو قيمة وكيجاوب على les besoins des utilisateurs.
-->

---

<!-- _class: blank -->
<!-- _paginate: false -->
<!-- _header: "" -->
<!-- _footer: "" -->

# Merci

<!--
Voilà, c'est la fin de ma présentation.

Merci beaucoup pour votre attention.

Si vous avez des questions, je serai ravi d'y répondre.
-->
