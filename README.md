# Chaines-de-Markov-et-page-Rank-de-Google

Chaînes de Markov et page Rank de Google



Leonardo CORREIA-MENDES / Groupe 3A BUT3
Diego PENICAUD-BERNAL / Groupe 3A BUT3
Aidan CRISTINI / Groupe 3A BUT3

Définition mathématique chaîne de Markov	2
Histoire et fondements des chaînes de Markov	2
Exemple de Modèle de Markov observable & caché	2
Modèle Markov observable :	2
Modèle Markov caché :	3
Définition mathématique PageRank	3
Histoire et fondements du PageRank	3
Fonctionnements de l’algorithme PageRank	3
Exemples de l’algorithme PageRank	3

Définition mathématique chaîne de Markov : 

Une chaîne de Markov est un modèle mathématique, basé sur des graphes, utilisé pour représenter des systèmes dans lesquels l’état futur dépend uniquement de l’état actuel, et non des états passés. Dit autrement, toute l’information est contenue dans l’état présent. Pour prédire l’état suivant, il suffit de connaître le dernier état, sans se soucier de la séquence d’états antérieurs.

Histoire et fondements des chaînes de Markov : 

Les chaînes de Markov apparaissent en 1906 grâce au mathématicien russe Andreï Markov. L’idée ne naît pas dans le vide : Markov voulait répondre à une controverse avec son collègue Pavel Nekrasov. Celui-ci affirmait que la loi des grands nombres, un des résultats centraux de la théorie des probabilités, ne pouvait s’appliquer que si les variables étaient indépendantes. Markov s’oppose fermement à cette vision. Pour le contredire, il entreprend de montrer qu’il est possible d’obtenir les mêmes résultats sans indépendance stricte, à condition que les dépendances soient bien structurées.
Par ce travail, Markov réussit à démontrer que Nekrasov avait tort : l’indépendance n’est pas nécessaire pour obtenir des résultats probabilistes fondamentaux. Cette volonté de réfuter une idée reçue est directement à l’origine du concept de chaîne de Markov.
Au milieu du XXᵉ siècle, des probabilistes comme Doeblin et Feller précisent les théorèmes de convergence. Puis les chaînes de Markov deviennent un outil central en mathématiques appliquées, donnant naissance à des méthodes comme le Monte Carlo par chaînes de Markov (MCMC), utilisées en physique, statistique et informatique.

Exemple de Modèle de Markov observable & caché
Modèle Markov observable :
Considérons la situation qui suit :
Vous êtes enfermés chez vous un jour de pluie, et vous aimeriez déterminer le temps qu’il fera lors des cinq prochains jours. mesure stationnaire
Comme vous n’êtes pas météorologue, vous vous simplifiez la tâche en faisant l’hypothèse que la météo suit un modèle de Markov: le temps qu’il fait au jour J dépend uniquement du temps qu’il fait au jour J-1.
Pour simplifier encore plus, vous considérez qu’il y a seulement trois temps possibles: soleil, nuages ou pluie.
En se basant sur les observations des derniers mois, vous établissez le diagramme de transitions suivant :
La matrice de transition associée est

Comme le temps d’un jour dépend uniquement du temps qu’il a fait la veille, il suffit de multiplier les probabilités (pour rappel il pleut aujourd’hui):

P (Soleil, Soleil, Pluie, Nuages, Nuages, Soleil | Pluie) 
= P(Soleil | Pluie)P(Soleil | Soleil)P(Pluie | Soleil)P(Nuages | Pluie)P(Soleil | Nuages)
= 0,35 x 0,35 x 0,4 x 0,45 x 0,4
= 0,0088

Modèle Markov caché : 
Supposons maintenant qu’un psychopathe de la météo vous a enfermé dans une pièce sans fenêtre avec seulement un ordinateur et une lampe. Chaque jour, la lampe s’allume d’une certaine couleur en fonction de la météo. Votre kidnappeur vous fournit la matrice d’observation suivante :


Par exemple s’il pleut, la lampe a 70% de chances d’être verte et 30% de chances d’être bleue.
Vous pourrez rentrer chez vous si vous déterminez le temps qu’il fera lors des cinq prochains jours uniquement en vous basant sur la couleur de la lampe. Vous construisez alors un modèle de Markov caché.
Vous restez enfermé 5 jours et vous relevez les couleurs suivantes:
   bleu, bleu, rouge, vert, rouge.
Vous vous souvenez qu’il pleuvait le jour précédant votre enfermement, vous pouvez donc rédiger un tableau montrant la combinaison qui a la plus forte probabilité d’être réalisée :




Définition mathématique PageRank : 

Le PageRank est un algorithme mathématique utilisé par Google pour évaluer l’importance des pages web. Sa formule de base, développée par Larry Page et Sergey Brin, repose sur des concepts de théorie des graphes et de probabilités, notamment les chaînes de Markov.

Histoire et fondements du PageRank : 
Le procédé de Pagerank de classement des pages web de Google est à l’origine du succès fulgurant du moteur de recherche le plus utilisé dans le monde. 
Le Pagerank influence les résultats de recherche en réponse à une requête utilisateur en évaluant la pertinence thématique du contenu par rapport à la recherche de l’utilisateur.

Le procédé de Pagerank de classement des pages web de Google a été créé par deux jeunes étudiants de l’université de Stanford : Larry Page et Sergey Brin. En 1996, au cœur de la Silicon Valley, ces deux visionnaires cherchaient un moyen d’organiser les informations sur le web de manière plus intelligente. Le Pagerank, qui tire son nom de Larry Page, repose sur une idée simple mais brillante : toutes les pages web ne se valent pas, et leur importance dépend en grande partie des liens qu’elles reçoivent d’autres pages.  
Fonctionnements de l’algorithme PageRank : 
Exemples de l’algorithme PageRank : 
