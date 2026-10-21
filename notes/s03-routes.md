# Session 03 - Routes, contrôleurs et layout

## Défi

URL produite par route('about') :
http://localhost:8000/a-propos

URL produite par route('posts.show', 'routes-et-controleurs') :
http://localhost:8000/posts/routes-et-controleurs

URL produite par route('posts.archive', 2025) :
http://localhost:8000/posts/archive/2025

Pourquoi /posts/archive/abc et /posts/article-inconnu répondent toutes deux 404, et quelle ligne de code en est 
responsable dans chaque cas ?
/posts/archive/abc répond 404 parce que le paramètre year doit être numérique. La ligne responsable est 
->whereNumber('year') dans routes/web.php.
/posts/article-inconnu répond 404 parce que l'article demandé n'existe pas. La ligne responsable est abort(404) 
dans la méthode show() de PostController.

Que se passe-t-il si une vue appelle route('posts.show') sans paramètre ?
Laravel déclenche une exception Missing required parameter parce que la route posts.show nécessite le paramètre 
slug.

