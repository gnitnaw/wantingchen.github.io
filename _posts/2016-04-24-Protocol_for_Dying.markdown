---
layout: post
title:  "Traduction : Un protocole pour le décès (A Protocol for Dying), par Pieter Hintjens"
comments: true
analytics : true
category: Vie
tags: Hintjens
---

L'original de cet article est ici : [A Protocol for Dying](http://hintjens.com/blog:115)

[Pieter Hintjens](https://en.wikipedia.org/wiki/Pieter_Hintjens) est écrivain, programmeur et penseur,
qui a dépensé des décennies à construire de grands systèmes logiciels et des communautés en-ligne,
qu'il décrit comme des "système vivant".
Il est un expert du calcul distribué, 
et il a rédigé plus que 30 protocoles et système distribué.
Il a conçu AMQP en 2004, et il a fondé le projet de logiciel libre ZeroMQ en 2007.
Il est l'auteur de "ZeroMQ - Messaging for Many Applications" (O'Reilly), 
"Culture and Empire: Digital Revolution", et "The Psychopath Code".
En avril 2016, il a été diagnostiqué de métastase terminale d'un cancer précédent.

--------------------------------------------

<span style="color: blue"> Rédigé par Pieter Hintjens à 11h43, 22 avril, 2016.</span>

Voici mon dernier article. Peut-être je pourrais écrire plus, 
si j'ai encore le temps après.
Je concentrerai mon attention à la position la plus agréable au lit, 
la planification du traitement contre la douleur,
et les gens autour de moi.

Hier j'ai eu douze visiteurs, y compris mes jeunes enfants aimables.
On peut imaginer que c'est fatigant, 
mais l'interminable flux des amis et de la famille était comme être dans un confortable bain chaud alimenté en eau fraîche sans cesse.

J'étais un homme isolé et solitaire, et peut-être un peu autiste.
Je pensais seulement au travail, à la natation, à mes chats.
La notion que les gens inconnus à moi pouvaient prendre plaisir de ma compagnie était étrange pour moi.
Au moins mes œuvres, je trouvais, avaient la valeur.
Nous avons composé des générateurs de code en Cobol.
J'ai fait un éditeur de code que le personnel aimait bien, parce qu'il marchait gracieusement et pouvait exécuter partout.
J'ai fait de l'auto apprentissage en C et assembleur 8086 et j'ai composé des outils shareware dans les années 1990.

Au fil du temps j'ai appris que si on noue une petite conversation avec un inconnu,
la réponse vient avec un rayon de plaisir.
Petit à petit, ceci devenait ma drogue de choix,
comme une addiction graduelle au café.

Finalement ça était devenu la base et alors la cible de mon travail:
aller aux endroits étranges et rencontrer les gens inconnus.
J'aime bien les conférences parce qu'on n'a pas besoin d'excuse.
Tout le monde veut et espère parler.
Rarement je parle des sujets techniques.
On peut simplement lire le code si on veut.

Ainsi, je suis fier de mon œuvre réel, qui a été, pendant des décennies, 
de parler, d'écouter et d'échanger des connaissances avec les gens,
et alors synthétiser tout ceci et puis partager avec les autres.
Des milliers de conversations se sont ainsi faites à travers de l'Europe, de l'Amérique, de l'Afrique et de l'Asie.
Et je peux gagner toutes les louanges que les gens crédible me donnent, comme créatif ou brillant, etc.
Toutefois, les modèles et les théories que j'ai adaptés et documentés, 
sont toujours issues de l'expérience quotidienne avec d'autre gens.

Merci beaucoup pour tout ça, mes amis.
Quand je dis "je vous aime", ce n'est pas seulement un geste.
Vous m'avez littéralement alimenté professionnellement et intellectuellement.

Donc je voulais documenter un dernier modèle, 
qui est comment faire face au décès,
étant donné quelques connaissances d'avance.
Cette fois-ci je ne vais pas écrire un RFC (demande de commentaires). :)

### Comment cela s'est passé ###

Techniquement, j'ai un cancer métastasé des voies biliaires dans les deux poumons.
Depuis février j'ai eu la toux sèche, la fatigue augmentée et la perte de concentration au travail.
En mars, mon père est décédé et nous nous sommes dépêchés de l'arranger.
Je toussais encore tous le temps.
Le 8 avril je suis allé chez mon oncologue et je lui ai dit que je n'allais pas bien. 
Elle a ordonné un CAT-scan urgent et des analyses de sang.

Le 13 avril, une bronchoscopie horrible et des biopsies.
Et puis le 15 avril, un TEP-scan.
Pour le 16 avril, il avait été prévu que je conduise à Eindhoven pour y donner un keynote à NextBuild.
Au contraire, je suis allé aux urgences à cause de la douleur explosive du côté des biopsies.
Je me suis enregistré et j'ai été donné des antibiotiques, qui réduit la douleur.
Et puis le 18 avril, mon oncologue a confirmé que c'est du cancer.
Je suis encore ici, et mes médecins réfléchissent quelle chimio je peux essayer.
C'est un cancer rare en Europe, avec peu de données solides.

Tous ce que nous comprenons est, cholangiocarcinoma ne répond pas bien à la chimiothérapie.
De plus, mon cancer est agressif et envahit vite.
Ensuite, j'ai déjà des clusters ailleurs dans mon corps.
Tout ceci, ce sont des données solides.

Ce jour-là, je l'ai dit au monde, et alors j'ai préparé le décès.

### S'adresser à une personne qui va mourir ###

Il peut s'avérer très étrange de parler une personne mourante (on la nomme "Bob").
Voici les choses principales que l'autre personne (on l'appelle "Alice") ne devrait pas dire à Bob :

- **"Accroche-toi! Il faut avoir de l'espoir! Tu dois lutter!"**
Il est prudent d'assumer que Bob lutte contre la maladie aussi durement que possible.
Si non, c'est le choix de Bob entièrement.  
- **"C'est tellement tragique. Je suis si triste. Ne meurs pas s'il vous plaît!"**
C'est ce que ma fille m'a dit une fois.
J'ai expliqué doucement qu'on ne peut jamais lutter contre la réalité.
La mort n'est pas une option.
Être fâché ou triste en face des faits, c'est du gaspillage de temps.  
- **"Tu peux vaincre ceci! On ne sait jamais!"**
C'est ce qu'Alice fait afin de exprimer son espoir.
L'espoir faux n'est pas un médicament réel,
contrairement à un produit efficace de chimiothérapie, ou un anti-douleur calmant.  
- **"Il y a cette guérison alternative dont les gent parlent."**
De telles remarques, dont j'ai eu seulement peu, heureusement, méritent un coup de marteau.
Même s'il y a une guérison miraculeuse, 
le coût et le stress (aux autres) de la chercher est un acte tellement égoïste et disproportionné,
avec une probabilité de réussite comparable à celle de la loterie.
On vit, et on meurt.  
- **"Lis ce chapitre de la Bible, ça t'aidera."**
C'est très rude, offensant, maladroit et aussi arrogant.
Si Bob veut des conseils religieux, il parlera à son prêtre.
Dans le cas contraire: territoire interdit!
C'est une autre offense qui encourt mon marteau.  
- **S'engager questionner hésitant est comme un harcèlement passif.** Par exemple,
demander à Bob de répondre à maintes reprises des petites choses comme "je t'ai réveillé?"
Probablement, Bob n'a pas l'état d'esprit pour un bavardage.
Il a envie d'avoir les gens qui restent près de lui physiquement, ou parlent des choses intéressantes (vois ci-dessous).

En outre, ne pleure pas au téléphone quand tu l'appelles.
Si tu sens que tu vas pleurer, raccroche le téléphone et attends pendant 10 minutes, puis rappelle-le.
La larme n'est pas de problème.
Pourtant, la menace d'auto apitoiement peut pousser Bob vers l'obscur.
J'avais appris à maîtriser mon émotion main souvent Bob est vulnérable.

Voici les choses qu'Alice peut évoquer pour rendre Bob heureux.

- **Les histoires de veilles aventures qu'ils ont partagées.**
Tu le te rappelles encore? Ah oui, je me rappelle... Comme c'était bien!  
- **Les détails cliniques.** 
Bob, qui est fixé au lit tout le temps, est probablement obsédé par le rituel des soins, 
le personnel, les médicaments, et surtout, sa maladie.
Plus bas, je discuterai les obligations de Bob concernant le partage de tout ceci.  
- **Aide Bob avec les détails techniques.**
Arranger toutes les choses de la vie est très compliqué et on a besoin de beaucoup de mains et cerveaux.  
- **"J'ai acheté ton livre."**
dans l'hypothèse que Bob est un écrivain comme moi.
Peut-être c'est de la flatterie, ou sincère, de toute façon ça va faire Bob sourire.

Avant tout, évite toute émotion autre que le bonheur, 
ne lui présente pas de problèmes additionnels.

### Devoir de Bob ###

Ce n'est pas toujours la responsabilité d'Alice.
Bob aussi a ses obligations sous ce protocole.
Y compris, au moins :

- **Soyez heureux.** 
Peut-être on trouve que c'est banal mais en fait c'est essentiel.
Si vous restez triste et dépressif, Alice toujours sera misérable quand elle parle avec vous.  
- **Évidemment, rangez vos affaires en ordre.**
J'avais déjà attendu mon décès il y a plusieurs années, 
alors me suis fait dispensable partout où je pouvais.
Pour ma famille, ce n'est pas possible.
Pour mes œuvres, bien-sûr, au fil des années je me suis rentré en tant qu'acteur critiqué de la communauté ZeroMQ.  
- **Éliminez autant de stress et frais que possible.**
Par exemple, l'euthanasie est licite en Belgique.
J'ai déjà demandé à mon médecin de la préparer 
(pas maintenant! Quand ce moment arrive...).
Et j'ai demandé aux gens de venir me dire adieu avant je meurs, pas après.
Pas d'obsèques.
Je vais donner mon corps à la université ici, si elle veut.  
- **Soyez réaliste.**
L'espoir n'est pas un médicament, comme j'ai expliqué.
Si vous allez négocier avec vos médecins, que ce soit pragmatique et à l'intérêt de tous.
J'ai dit les miens qu'ils peuvent essayer toute chimiothérapie expérimentale qu'ils souhaitent.
Ils pouvaient en obtenir des données,
et c'est la moindre récompense que je peux verser à un système qui ma donné une extension de vie de plus que cinq ans.  
- **Présumez le pire.**
Quand mon oncologue voyait mon scan, elle m'appelée tout de suite et me disait que,
pour sa part, il s'agissait du cancers.
J'ai raccroché le téléphone et puis, je l'ai dit aux enfants.
Le lendemain j'ai dit à leurs écoles, mon avocat, et mon notaire, d'expecter le pire.
Après dix jours, les biopsies l'ont confirmées.
Ça nous a donné dix jours plus pour nous chagriner, et plus de temps à préparer.  
- **Soyez honnête et transparent avec les autres.**
Il faut du temps au chagriner. 
Et c'est plus facile de le passer le décès de Bob s'ils peuvent parler avec lui.
Il n'y a aucune honte au décès, ce n'est pas un échec.

### Expliquez aux enfants ###

Mes enfants ont 12, 9, 5 ans. Tragique, etc., etc.
Ils grandiront sans leur père. C'est une réalité.
Pourtant ils grandiront avec moi dans leur ADN, 
dans les discours de conférence interminable au Youtube,
et dans mes mots.

Je leur ai déjà expliqué doucement, plusieurs fois pendant des années, comme ça:
Un jour, je serai parti. Peut-être bien loin au futur, peut-être bientôt.
Chacun va mourir, oui, mon petit Gregor, toi aussi.
C'est la vie.

Imagine que tu as une boîte de Lego, et alors tu construis une maison, et tu la conserves.
Et puis tu continues à construire de nouvelles maisons sans détruire les anciens.
Qu'est-ce qu'il va passer?
"La boite sera vide, papa."
Bien, oui.
Ensuite tu peux encore construire une nouvelle maison?
"Non, pas vraiment."
Ainsi nous sommes comme les maisons de Lego.
Quand nous mourons, nous tombons en pièces qui seront rendues à la boîte.
Nous mourons, et de nouveaux bébés peuvent naître.
C'est la roue de la vie.

Cependant, j'ai trouvé qu'ils se sentent bien lorsqu'ils voient leurs parents heureux et relaxé 
(pas à cause des anti-douleurs),
et quand ils disent au-revoir pendant les semaines.
Je suis si reconnaissant que je ne meurs pas brusquement, et je ne perds pas mon esprit.

Et j'avais dit à mes enfants d'apprendre à nager, faire du vélo, patiner et tirer.
À cuisiner, à voyager et à camper.
À utiliser les technologies sans peur.
Gregor a joué Minecraft quand il avait 3 ans, avec le clavier dans la main gauche, et la souris dans la main droite.
Quand Noemie avait 7 ans, elle a appris à tirer avec un pistolet.
Ils peuvent parler plusieurs langues.
Ils sont confiants et peuvent apprendre rapidement, comme leur père.

Toute le monde doit comprendre la signification du décès.
Accepter sa propre mortalité est une compétence-clé de l'être un humain.
On s'efforce de vivre, bien sûr.
Quand c'est fini, on embrasse la fin.
Je suis heureux que je peux apprendre cette leçon à mes enfants,
une leçon que je n'ai jamais eu.

### Euthanasie ###

Finalement, je suis si content que je n'ai jamais quitté la Belgique.
C'est un pays qui permet le décès sur demande, 
pour les malades qui sont terminals ou ont une qualité de la vie souffrante terrible.
Il faut l'avis de 3 médecins, un psychiatre, 
et une période attendante de quatre semaines; 
Dans le premier cas, l'opinion d'un médecin suffira.

Mon père l'a choisi et il est décédé le mardi de Pâques.
Plusieurs de nous étaient avec lui.
C'était un processus simple et paisible.
Il a été endormi par une première injection, en tombant dans une coma.
Et puis la deuxième a arrêté son cœur.
C'était une bonne façon de mourir, c'est ce que j'ai déjà voulu, 
bien que je ne savais pas encore que j'étais malade en ce moment.

Je suis choqué que, en 2016, il y a seulement peu de pays qui la permettent,
et les autres appliquent encore les tortures barbare de la décadence et de l'échec.
C'est particulièrement pertinent pour le cancer, qui est la cause majeure du décès.
Si votre juridiction interdit l'euthanasie,
prenez le temps pour faire du lobbyisme pour la droit de mourir dans la dignité.

### Mon sentiment pour tous ###

Je n'ai jamais été une personne craintive.

Ma dernière presque-collision avec la mort m'a laissée si indifférent sur le concept entier de risque professionnel et sociale,
ainsi je suis devenu le caractère prédateur qu'Allen Ding décrit si bien.
Ça c'est calmé après la fin de notre projet "Game of Thrones".
Je n'étais vraiment comme ça, 
je suis juste devenu une telle personne afin de faire fonctionner les choses étant donné les circonstances.

Après avoir eu plusieurs années pour me préparer, 
et après avoir vu l'assemblage d'un grand nombre de plans délicats au cours de ces années,
me laisse profondément satisfait.
Depuis 2011 je suis devenu un tireur expert de pistolet, 
j'ai appris moi-même à jouer du piano 
(et j'ai aussi composé beaucoup de petites pièces),
j'ai vu mes enfants grandir à devenir des êtres heureuses et pétillants, 
j'ai écrit trois livres,
j'ai guidé la communauté de ZeroMQ jusqu’à un niveau d'auto-fiabilité serein.
Un Bob peut demander plus?
 
Les membres du personnel d'ici sont aimables.
Je n'ai rien à plaindre, 
et je veux seulement exprimer ma gratitude à tous mes amis pour les années de plaisir que vous me l'avez donné, 
ma médicaments, qui m'ont gardé vivant et motivé.

Merci!

### Pensez à mes enfants ###

Je vous en prie d'utiliser cet article pour ajouter vos histoires.
Si vous en avez ailleurs, vous pouvez aussi m'envoyer, 
copiez/collez comme un commentaire.
N'hésitez pas d'écrire en néerlandais ou français si elles sont votre langue maternelle.
J'aurais bien aimé un endroit unique où mes enfants peuvent venir et lire ce que les autres disent au sujet de leur père.

Beaucoup de gens m'ait demandé mon adresse de PayPal : ph@imatix.com,
afin de faire un don au bénéfice de mes enfants.





