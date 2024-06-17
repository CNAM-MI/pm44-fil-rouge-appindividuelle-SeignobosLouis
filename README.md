#Next Drink, client avec Ionic

#Demonstration vidéo
La démonstration vidéo de l'accéléromètre (non fini, mais usage fonctionnel) est disponible sur la vidéo de démonstration de l'accéléromètre.
La démonstration de l'intéraction client/serveur, avec un impact sur la BDD directement est disponible sur la vidéo de démonstration correspondante.

#Spécifité mobile
Usage de l'accéléromètre pour voter sur un sondage

#Fonctionnement Socket io
Le client envoie (emit) un message au serveur, le serveur traite la demande, effectue une requête à l'aide de Sequelize, puis renvoie le résultat depuis la connection socket io. 

Le backend a été écrit en TypeScript pour l'échange avec le client à l'aide de Socket.io. Globalement, il fonctionne de la manière suivante (voir vidéo dans dossier "demo video" pour plus de visuel) : Lorsque le serveur reçoit des messages de socket io, il exécute des fonctions avec Sequelize (ORM) pour intéragir avec la BDD qui est hébergé sur l'instance du VM ubuntu, elle même hébergée sur Oracle Cloud. Une fois la requête effectuée à l'aide de Sequelize, le résultat est renvoyé par "emit" depuis une connection socket entre le client et le serveur. Le client attend un certain type de message depuis la socket, puis le traite.

Toutes les requêtes ont été écrites côté back, mais ne sont pas toutes branchées côté front : -la création de compte, la connection à un compte, la création d'un sondage sont "branchées", sur l'application écrite avec "Ionic". 
Le reste n'a pas encore été "branché".

#RETEX IONIC
#Apprentissage
Ayant déjà utilisé Angular, la courbe d'apprentissage a plutôt été rapide pour utiliser Ionic. 

Aucune notion majeure vient se rajouter à l'apprentissage Ionic si ce n'est d'apprendre à utiliser Capacitor pour build le projet et l'utiliser en parallèle avec Android Studio.

Je n'ai pas eu le temps de développer la version iOS par manque de temps, cependant, très peu de code et de permissions sont à rajouter, ce qui en fait un avantage pour le mutliplateforme.

#Avantages
Réaliser des interfaces dynamiques, "agréables" visuellement et intuitives est très facile et rapide du fait des nombreux templates proposés sur la documentation officielle d'Ionic.
Utiliser des packages npm rend la création de fonctionnalités qui ne sont pas forcément proposées "directement" depuis Ionic très facile :
  Typiquement pour le color picker, je n'ai pas utilisé une fonctionnalité d'Ionic mais un package installé depuis npm, utilisable car Ionic utilise Angular, qui est une technologie web. 

Multiplateforme très facile, testé au tout début du projet depuis le tutoriel d'Ionic.
Performances sur android très honorables.

De ce fait, et en vue des difficultés qu'on pu exprimé mes collègues sur leurs technologies pour réaliser ce que j'ai pu faire côté "client" sur les vues, je pense que Ionic est l'une des meilleures solutions pour réaliser le projet. 

