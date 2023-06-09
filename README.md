# Village-green

# Projet fil rouge de formation Développeur web et web mobile

# 1- Présentation du projet

# _1.1- Expression des besoins :_

Le projet est un site e-commerce de vente de matériel de musique (instruments, accessoires etc…). Il doit comporter un panier avec la possibilité de passer des commandes.
L’administrateur devra pouvoir gérer le site complètement, aussi bien la partie client que la partie commandes.
Le client aura la possibilité de pouvoir trouver des produits selon les différentes catégories proposées.

# _1.2- Mise en place du cahier des charges :_

Selon le cahier des charges, un administrateur doit pouvoir accéder à toutes les commandes selon leur statut (en retard, annulée etc…) et en gérer la modification. Il doit aussi avoir la possibilité d’ajouter de nouveaux produits, de modifier ou de supprimer ceux existants.
Le client pourra ajouter des produits dans le panier et passer des commandes. Il pourra également donner une note à son expérience sur le site par l’intermédiaire d’un formulaire seulement si la commande possède un statut particulier.
Seul un client possédant un compte et étant connecté aura accès à toutes les fonctionnalités du site, comme ajouter des produits au panier ou voir le récapitulatif des ses commandes effectuées par exemple. 

# _1.3- Fonctionnalités :_

Concernant la gestion du site, l’objectif du projet est de créer un tableau de bord qui pourra permettre aux administrateurs de gérer les produits, les commandes, les comptes d’utilisateurs et son propre compte admin.

# _1.4- Droits Admin/Clients :_

_Côté Admin :_

-	Gestion des clients : L’administrateur pourra supprimer des clients (D). 

-	Gestion des Admins : L’administrateur pourra créer, lire, modifier et supprimer son compte d’amin (CRUD).

-	Gestion des Produits : L’administrateur pourra créer, lire, modifier et supprimer des produits (CRUD).

-	Gestion des Commandes : L’administrateur pourra créer, lire, modifier et supprimer des commandes (CRUD).

_Côté Client :_

-	Panier : Le client pourra ajouter des produits au panier, supprimer tout ou partie de celui-ci, modifier la quantité des produits déjà ajoutés (CRUD).

-	Evaluation : Si une commande possède le statut ‘terminée’, le client aura la possibilité de laisser une évaluation sous forme d’étoiles à attribuer de 0 à 5 (CRD).

-	Gestion de son compte : Le client pourra créer et modifier son compte client (CRU).

-	Message : Le client aura la possibilité d’envoyer un message (C).


# _1.5- Technologies utilisées_

- HTML
- CSS
- Javascript
- PHP
- Mysql
- Looping

# 2- La base de données

# _2.1- Le MCD_

A l’aide du logiciel de modélisation conceptuelle de données ‘Looping’, j’ai commencé par réaliser le MCD (Modèle Conceptuel de Données) en suivant les demandes du cahier des charges.

![MCD](https://github.com/cedric-chimot/Village-green/assets/106061524/909e54a1-e488-45ed-bcab-b4263c43a9ce)

Dans ce MCD, on peut voir des Entités contenant chacune des attributs. Entre chaque Entité, on retrouve des relations ou associations (Verbe) qui expliquent et précisent comment les Entités sont reliées entre elles (Les ovales avec leurs « pattes » qui se rattachent aux Entités). Enfin, des cardinalités qui sont les petits chiffres au-dessus des « pattes ». Le MCD a été modifié plusieurs fois afin d’intégrer au mieux les différentes fonctionnalités du site, notamment les reviews.

# _2.2- Le MLD_

Du MCD, toujours grâce à Looping, j’ai pu élaborer le MLD, qui est le Modèle Logique de Données. Le MLD transforme les entités en tables avec ses attributs et transformes les associations en clés primaire et clés étrangères. Comme dans l’exemple ci-dessous.

![MLD](https://github.com/cedric-chimot/Village-green/assets/106061524/bf944573-3baa-41dc-8633-f048515b80c6)

# _2.3- Dictionnaire de données_

Pour rester dans un vocabulaire conceptuel il a fallu créer un dictionnaire de données, celui-ci regroupe toutes les données et le vocabulaire commun qui figureront dans le projet et le MCD.

![dico](https://github.com/cedric-chimot/Village-green/assets/106061524/16f91e7a-1cbe-4742-92d7-1dcb9b76af58)

# 3- Le projet en détail

# _3.1 Page d'accueil_

La page d'accueil du site :

![home-village](https://github.com/cedric-chimot/Village-green/assets/106061524/39927801-8492-4361-a0f8-5c4de37393bd)
![home1-village](https://github.com/cedric-chimot/Village-green/assets/106061524/fc051876-cd38-421e-b9c2-a6e25731c1f3)

Il y a une Navbar pour naviguer sur chaque page, L'icône utilisateur pour afficher l'identifiant de la personne connectée, se connecter, s'inscrire ou se déconnecter. Les images étaient fournies dans le dossier d'exercice avec le cahier des charges. Au niveau "catégories", chaque image renvoie à la page de la catégrie correspondante.

# _3.2 Section "à propos"_

![apropos-village](https://github.com/cedric-chimot/Village-green/assets/106061524/232acf60-3259-481e-8225-7181afbb7153)
![apropos1-village](https://github.com/cedric-chimot/Village-green/assets/106061524/40de372f-a7c0-4370-aaf2-8209ff48821f)

On peut trouver une requête dans la section ‘à propos’ afin d’afficher sur la page dédiée les derniers commentaires postés par les clients.

# _3.3 Les produits_

La liste des produits :

![produits-village](https://github.com/cedric-chimot/Village-green/assets/106061524/9677ac4b-4c48-44b1-8245-16a70dd254ca)

Il y a un bouton pour ajouter au panier. Si l'utilisateur n'est pas connecté il ne peut pas ajouter d'articles au panier et il est renvoyé sur la page de login.

# _3.4 Les commandes_

_- Le panier :_

Ici le récapitulatif des produits dans le panier.

![panier-village](https://github.com/cedric-chimot/Village-green/assets/106061524/51c00524-f2aa-487a-864e-f0ce32a106b1)

On a la possibilité de valider le panier, ce qui nous reverra sur la page de validation de commande ci-après, ou l'on peut également supprimer tout ou partie des articles dans le panier.

_- Les commandes :_

_Validation de commande ->_

Lorsqu'on clique sur le bouton "passer la commande", on arrive sur cette page :

![commandes1-village](https://github.com/cedric-chimot/Village-green/assets/106061524/9c7c31bc-9dc0-4848-b5a4-06dbe32f3114)

Il y a un récapitulaif des articles dans le panier. On doit ensuite compléter le formulaire avec toutes nos coordonnées pour pouvoir enfin valider la commande.

_Récapitulatif des commandes passées ->_

Une fois la commande passée, on la retrouve sur la page regroupant toutes les commandes effectuées : 

![commandes-village](https://github.com/cedric-chimot/Village-green/assets/106061524/e2771d52-2750-47a0-b23b-07ab75053b02)

Par défaut, le statut de la commande est "en attente". L'admin pourra en changer le statut lorsque celle-ci aura éé traitée. Le client pourra alors donner son avis si la commande est complètement validée.

_Avis sur les commandes passées ->_

L’idée avec cette fonction était de permettre aux clients de laisser leur avis sur leur expérience sur le site à la suite d’une commande. L’utilisateur devra bien entendu être connecté au site s’il veut accéder au récapitulatif de ses commandes et laisser une appréciation.
On commencera donc par créer un formulaire. Il est accessible depuis le récapitulatif des commandes en appuyant sur le bouton ‘Donner votre avis’. Ce bouton est paramétré de façon qu’un commentaire ne puisse être donné que si la commande est complètement terminée. Le bouton d’accès au formulaire sera bloqué si le statut de la commande est autre que terminé.

![avis-village](https://github.com/cedric-chimot/Village-green/assets/106061524/eaf0d32f-ea1d-428d-95b1-1fd2e018cbe0)

Une fonction Javascript permet de créer une animation sur les étoiles dans le formulaire. Au survol, celles-ci changent de couleur. En cliquant dessus, la couleur se fixe et tant que le formulaire n'est pas validé on peut changer sa note en cliquant sur n'importe quelle étoile.

Une fois que le client à valider le formulaire, le commentaire s’affiche en dessous, il trouvera également tous les avis qu’il a déjà posté.

![avis1-village](https://github.com/cedric-chimot/Village-green/assets/106061524/06259c04-65db-48ef-b472-749bbbfbfa89)

# _3.5 Dashboard administrateur_

_- Accueil admin :_

Sur cette page, l'admin peut voir toutes les informations concernant le site et en gérer les options.

![dashboard-village](https://github.com/cedric-chimot/Village-green/assets/106061524/7fdd27e2-0da0-4160-922a-1d713417d132)

_- Gestion des admins :_

L'admin peut voir tous les comptes admins créés mais ne peut que modifier son compte personnel et ses informations pas celui des autres admins.

![dashboard1-village](https://github.com/cedric-chimot/Village-green/assets/106061524/4aedc77b-e274-4869-bb39-9fec653986c7)

_- Gestion des produits :_

Il y a ici un formulaire pour ajouter des produits.

![dashboard2-village](https://github.com/cedric-chimot/Village-green/assets/106061524/f84f6c23-6421-4b19-96c3-c5a37627ead0)
![dashboard5-village](https://github.com/cedric-chimot/Village-green/assets/106061524/6f442599-cebc-4ef2-849d-d7eb1aa19be4)

L'admin peut les supprimer ou les modifier.

_- Gestion des commandes :_

Suivant le cahier des charges, il était demandé de pouvoir assurer une gestion des commandes suivant leur statut. Pour ce faire, j’ai décidé de créer un CRUD (Create, Read, Update, Delete).
La partie Create se fait du côté du client lorsque celui-ci valide une commande. Le Read consistera à afficher les données des commandes sur une page, la partie modification Update ainsi que la suppression Delete seront liés à l’ID d’une commande en particulier pour que ne soit mis à jour que la commande concernée.

![dashboard3-village](https://github.com/cedric-chimot/Village-green/assets/106061524/63fcd97b-2ad2-4173-a439-f63214c39988)

Dans le Dashboard, on pourra voir les commandes selon leur statut, ci-dessus par exemple la page recensant les commandes passées par les utilisateurs. Une liste déroulante affichera divers statuts (en attente, terminée etc...) que l'admin pourra modifier.

_- Gestion des utilisateurs :_

L'admin peut voir tous les inscrits sur le site et supprimer leur compte s'il le faut.

![dashboard4-village](https://github.com/cedric-chimot/Village-green/assets/106061524/250f5f33-395e-4350-9e55-883e838d07cd)

# 4- Conclusion

Cette formation m’a permis de découvrir un nouveau métier et m’a permis également d’apprécier cette découverte. J’ai eu la chance de développer un projet depuis le début en mode From Scratch, c’est-à-dire, de la découverte du cahier des charges à la conception en passant par le développement de celui-ci. Cela a été très formateur.
