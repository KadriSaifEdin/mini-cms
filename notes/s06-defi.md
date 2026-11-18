# Session 06 - Défi : publier et dépublier

La route posts.publication apparaît dans route:list avec le verbe PATCH : oui
Le bouton affiche « Publier » sur un brouillon et « Dépublier » sur un article publié : oui
published_at est rempli à la publication et vidé à la dépublication : oui
Le nouveau test passe et php artisan test est vert : oui (15 tests passés)

Pourquoi PATCH et pas PUT ni GET pour ce bouton ?
PATCH modifie une partie de la ressource : ici un seul champ, is_published (avec published_at). PUT remplace l'ensemble des champs du formulaire. Un GET ne doit jamais modifier de données : un robot, un préchargement ou un double clic pourrait publier ou dépublier l'article.