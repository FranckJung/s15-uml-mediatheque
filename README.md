# Projet médiathèque UML

## User stories & Routes

| User story | Méthode HTTP | Route | Contrôleur | Méthode |
| --- | --- | --- | --- | --- |
| En tant que **visiteur**, j'ai besoin d'**une page d'accueil** afin d'**accéder aux services de l'application** | `GET` | `/` | `MainController` | `index` |
| En tant que **visiteur**, j'ai besoin d'**un formulaire de contact** afin de **pouvoir poser des questions aux administrateurs** | `GET|POST` | `/contact` | `MainController` | `contact` |
| En tant que **visiteur**, j'ai besoin d'**un champ de recherche** afin de **trouver les médias correspondant à certains critères** | `GET` | `/search` | `MainController` | `search` |
| En tant que **visiteur**, j'ai besoin d'**une liste de médias** afin de **pouvoir faire mon choix parmi les médias disponibles** | `GET` | `/:media` | `MediaController` | `index` |
| En tant que **visiteur**, j'ai besoin d'**une fiche technique** afin d'**en savoir plus sur un média qui m'intéresse**. | `GET` | `/:media/:id` | `MediaController` | `show` |
| En tant que **visiteur**, j'ai besoin d'**un formulaire d'inscription** afin de **créer un compte** | `GET|POST` | `/signup` | `SecurityContoller` | `signup` |
| En tant que **visiteur**, j'ai besoin d'**un formulaire d'authentification** afin d'**accéder à mon compte** | `GET|POST` | `/login` | `SecurityController` | `login` |
| En tant que **membre inscrit**, j'ai besoin d'**un bouton de déconnexion** afin de **refermer mon compte** | `POST` | `/logout` | `SecurityController` | `logout` |
| En tant que **membre inscrit**, j'ai besoin d'**une page de profil** afin de **mettre à jour mes informations** | `GET|POST` | `/account` | `AccountController` | `index` |
| En tant que **membre inscrit**, j'ai besoin d'**un bouton dans la description de chaque média** afin d'**ajouter ce média au panier** | `POST` | `/:media/:id/rent` | `MediaController` | `rent` |
| En tant que **membre inscrit**, j'ai besoin d'**une liste des médias que j'ai ajoutés dans mon panier** afin de **réserver les médias dans cette liste** | `GET` | `/cart` | `CartController` | `index` |
| En tant que **membre inscrit**, j'ai besoin d'**un bouton "validation" sur la page "panier"** afin de **valider ma réservation** | `POST` | `/cart/validate` | `CartController` | `validate` |
| En tant que **membre inscrit**, j'ai besoin d'**une liste des médias que j'ai loués** afin de **gérer mes locations** | `GET` | `/account/media` | `AccountController` | `media` |
| En tant que **membre inscrit**, j'ai besoin d'**un lecteur multimédia** afin de **consulter chaque média que j'ai loué** | `GET` | `/:media/:id/read` | `MediaController` | `read` |
| En tant que **vendeur**, j'ai besoin d'**un formulaire de sortie de média** afin de **valider la sortie d'un média réservé par un membre** | `GET|POST` | `/rent/out` | `RentController` | `out` |
| En tant que **vendeur**, j'ai besoin d'**un formulaire de retour de média** afin de **valider le retour d'un média par un membre** | `GET|POST` | `/rent/in` | `RentController` | `in` |
| En tant qu'**administrateur**, j'ai besoin d'**une liste de tous les médias existants** afin d'**avoir accès aux fonctionnalités de modification des médias** | `GET` | `/admin/media` | `Admin\MainController` | `media` |
| En tant qu'**administrateur**, j'ai besoin d'**un formulaire d'ajout de média** afin d'**ajouter des nouveaux médias** | `GET|POST` | `/admin/:media/new` | `Admin\MediaController` | `new` |
| En tant qu'**administrateur**, j'ai besoin d'**un formulaire de modification de média** afin de **modifier des médias existants** | `GET|POST` | `/admin/:media/:id/update` | `Admin\MediaController` | `update` |
| En tant qu'**administrateur**, j'ai besoin d'**un bouton de suppression pour chaque média** afin de **supprimer ce média** | `POST` | `/admin/:media/:id/delete` | `Admin\MediaController` | `delete` |
| En tant qu'**administrateur**, j'ai besoin d'**une liste de tous les membres inscrits existants** afin d'**avoir accès aux fonctionnalités de modification des membres inscrits** | `GET` | `/admin/members` | `Admin\MainController` | `members` |
| En tant qu'**administrateur**, j'ai besoin d'**un formulaire d'ajout de membre** afin d'**ajouter des nouveaux membres** | `GET|POST` | `/admin/members/new` | `Admin\MediaController` | `new` |
| En tant qu'**administrateur**, j'ai besoin d'**un formulaire de modification de membre** afin de **modifier des membres existants** | `GET|POST` | `/admin/members/:id/update` | `Admin\MediaController` | `update` |
| En tant qu'**administrateur**, j'ai besoin d'**un bouton de suppression pour chaque membre** afin de **supprimer ce membre** | `POST` | `/admin/members/:id/delete` | `Admin\MediaController` | `delete` |
