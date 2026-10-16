# Cycle de vie d'une requête vers /heure

1. `public/index.php` reçoit la requête HTTP.
2. `vendor/autoload.php` charge les classes de Composer.
3. `bootstrap/app.php` initialise l'application Laravel.
4. Laravel traite la requête et consulte les routes déclarées dans `routes/web.php`.
5. La route `/heure` exécute sa closure et prépare l'heure et la date.
6. `resources/views/heure.blade.php` affiche les données transmises grâce à Blade.
7. Laravel renvoie la réponse HTML au navigateur.