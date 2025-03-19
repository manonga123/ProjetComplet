Pour créer ton premier projet Laravel, voici les étapes de base :  

### 1️⃣ **Installer Laravel**  
Assure-toi d'avoir **PHP**, **Composer**, et **Node.js** installés.  

- **Installer Composer** (si ce n'est pas fait) :  
  [Télécharge Composer](https://getcomposer.org/download/) et installe-le.  

- **Installer Laravel via Composer** :  
  Ouvre un terminal et exécute :  
  ```sh
  composer create-project laravel/laravel mon-projet
  ```
  Remplace `mon-projet` par le nom de ton projet.  

### 2️⃣ **Configurer l’application**  
Va dans le dossier de ton projet :  
```sh
cd mon-projet
```
Copie le fichier `.env.example` et renomme-le en `.env` :  
```sh
cp .env.example .env
```
Génère la clé de l’application :  
```sh
php artisan key:generate
```

### 3️⃣ **Lancer le serveur**  
Démarre le serveur intégré avec :  
```sh
php artisan serve
```
Puis, ouvre **http://127.0.0.1:8000** dans ton navigateur.

### 4️⃣ **Créer une route et une vue simple**  
Modifie `routes/web.php` pour ajouter une route :  
```php
use Illuminate\Support\Facades\Route;

Route::get('/hello', function () {
    return view('hello');
});
```
Crée un fichier `resources/views/hello.blade.php` :  
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>Bonjour Laravel</title>
</head>
<body>
    <h1>Bienvenue sur Laravel !</h1>
</body>
</html>
```
Visite **http://127.0.0.1:8000/hello** pour voir ta page.

### 5️⃣ **Configurer la base de données (optionnel)**  
Modifie `.env` pour définir ta connexion à MySQL :  
```ini
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=mon_projet
DB_USERNAME=root
DB_PASSWORD=
```
Puis, applique les migrations :  
```sh
php artisan migrate
```

---

Tu es prêt à commencer ton projet Laravel ! Besoin d'aide pour un projet spécifique ?



//cmd ilaina

composer require fruitcake/laravel-cors
