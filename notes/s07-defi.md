# Session 07 - Défi : articles de la même catégorie

La section « Dans la même catégorie » apparaît sous un article publié qui a une 
catégorie : oui
L'article affiché n'apparaît pas dans sa propre section : oui
Un brouillon de la même catégorie n'apparaît pas : oui
La page s'ouvre sans LazyLoadingViolationException : oui
Le nouveau test passe et php artisan test est vert : oui (20 tests passés)

Combien de requêtes SQL charge la section, et pourquoi pas une par carte ?
La section charge 4 requêtes : une pour les articles de la catégorie, puis une pour les 
auteurs, une pour les catégories et une pour les tags. Ce nombre reste le même quel que 
soit le nombre de cartes, grâce à with('user', 'category', 'tags'), qui charge chaque 
relation d'un coup pour tous les articles. Sans with(), trois cartes ajouteraient 9 
requêtes (3 relations pour chacune), et la page lèverait LazyLoadingViolationException, 
car les articles sont chargés à plusieurs.