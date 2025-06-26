# API Blog Personnel - Laravel

## Description

Cette API Laravel fournit un système de publication pour un blog personnel, incluant :

* gestion des utilisateurs (authentification JWT)
* gestion des articles
* gestion des catégories
* gestion des commentaires
* fonctionnalités de pagination
* recherche textuelle des articles

L’API est développée en utilisant **Laravel** avec Eloquent ORM.

---

## Fonctionnalités

* Authentification par JWT (Laravel Sanctum ou Laravel Passport)
* CRUD complet sur les articles
* CRUD complet sur les catégories
* Ajout, édition et suppression de commentaires
* Pagination des résultats d’articles
* Recherche textuelle plein texte sur les titres et contenus
* Gestion des rôles (par exemple `admin`, `auteur`, `lecteur`)

---

## Stack technique

* PHP 8.x
* Laravel 11.x
* MySQL ou PostgreSQL
* Eloquent ORM
* JWT (Sanctum/Passport)

---

## Installation

1. **Cloner le dépôt**

```bash
git clone https://github.com/votre-utilisateur/api-blog-laravel.git
cd api-blog-laravel
```

2. **Installer les dépendances**

```bash
composer install
```

3. **Copier le fichier d’environnement**

```bash
cp .env.example .env
```

4. **Générer la clé d’application**

```bash
php artisan key:generate
```

5. **Configurer la base de données**
   Éditer le fichier `.env` avec vos paramètres :

```dotenv
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=blogdb
DB_USERNAME=root
DB_PASSWORD=
```

6. **Lancer les migrations**

```bash
php artisan migrate
```

7. **Installer et configurer JWT**

* Avec Sanctum

```bash
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate
```

* Ou avec Passport

```bash
composer require laravel/passport
php artisan migrate
php artisan passport:install
```

8. **Lancer le serveur**

```bash
php artisan serve
```

---

## Endpoints principaux

* `POST /api/register` : inscription d’un utilisateur
* `POST /api/login` : connexion d’un utilisateur
* `GET /api/articles` : lister les articles (avec pagination)
* `GET /api/articles/search?q=motcle` : rechercher des articles
* `GET /api/articles/{id}` : voir un article
* `POST /api/articles` : créer un article
* `PUT /api/articles/{id}` : mettre à jour un article
* `DELETE /api/articles/{id}` : supprimer un article
* `GET /api/categories` : lister les catégories
* `POST /api/comments` : ajouter un commentaire
* `GET /api/articles/{id}/comments` : lister les commentaires d’un article

---

## Tests

Lancer les tests avec :

```bash
php artisan test
```

---

## Sécurité

* Authentification par token JWT
* Protection CSRF pour le panel admin (si applicable)
* Validation stricte des entrées

---

## Contribuer

1. Forker le projet
2. Créer une branche
3. Soumettre une pull request

---

## License

Ce projet est sous licence MIT.

---
