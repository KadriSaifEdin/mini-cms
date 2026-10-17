# Cycle de vie d'une requête vers /heure

1. Le navigateur : envoie une requête HTTP GET /heure pour demander l'affichage de l'heure et de la date.

2. public/index.php : constitue le point d'entrée de l'application web et charge vendor/autoload.php, l'autoloader de Composer.

3. vendor/autoload.php : charge automatiquement les classes PHP nécessaires au fonctionnement de l'application.

4. bootstrap/app.php :  initialise l'application Laravel et configure notamment le chargement des routes web.

5. routes/web.php : contient la définition de la route /heure. Le routeur identifie cette route et exécute la closure associée.

6. resources/views/heure.blade.php : la closure transmet à cette vue les données préparées, notamment l'heure et la date. Blade utilise ces données pour générer le HTML.

7. La réponse HTTP : Laravel renvoie le HTML généré au navigateur, qui affiche la page contenant l'heure et la date.