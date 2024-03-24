Projet Hub :

## Description :
**Hub** est une application qui aura pour but de conserver tous vos sites web, signets, flux d'informations et notes préférés de manière organisée;

## Méthodologie d'installation

### git clone
Pour récupérer le projet en local

```bash
git clone git@github.com:Guillaume-RICHARD/Hub.git
```

### Droits des dossiers de cache
Mettre les droits en écriture sur certains dossiers

```bash
sudo chmod -R 775 storage/logs
sudo chmod -R 775 bootstrap/cache
chmod -R 775 storage/framework
```

## Installation des dépendances PHP

```bash
composer update
```

## Variable d'environnement
Faire une copie du fichier d'environnement
```bash
cp .env.example .env
```
Puis modifier ce qu'il faut dans le nouveau fichier .env

### Connexion à la BDD
Modifier ceci :
```env
DB_DATABASE=laravel
DB_USERNAME=root
DB_PASSWORD=
```

En :
```env
DB_DATABASE=hub
DB_USERNAME=root
DB_PASSWORD=root
```

### Variables locale de développement
```env

```

### Générer la clé de Laravel

```bash
php artisan key:generate
```

## Génération de la BDD
On génère la BDD via les fichiers de migrations, et on injecte les données existant dans les seeders

```bash
php artisan migrate
php artisan db:seed
```
## Tableau des URLS

| Method | Name | URL |
|--------|------|-----|
| xxx    | xxx  | xxx |

## Contributing

Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Code of Conduct

In order to ensure that the Laravel community is welcoming to all, please review and abide by the [Code of Conduct](https://laravel.com/docs/contributions#code-of-conduct).

## Security Vulnerabilities

If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License

The Laravel framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
