# Session 02 - Git et GitHub

Réponses rédigées avec mes propres mots, puis comparées au corrigé de la page.

## 1. Index et commit

Réponse : L’index est une zone où l’on prépare les modifications avant de les enregistrer. 
Le commit permet d’enregistrer ces modifications dans l’historique du projet.

## 2. Branche et tag

Réponse : Une branche permet de continuer le développement du projet. Un tag permet d’identifier un commit précis, par exemple la version lab-01.

## 3. Le fichier .env

Réponse : Le fichier .env ne doit pas être publié sur GitHub, car il peut contenir des informations sensibles, comme les mots de passe et les paramètres de connexion à 
la base de données. On l’ajoute au fichier .gitignore.

## 4. Le dossier vendor/

Réponse : Le dossier vendor/ contient les bibliothèques installées par Composer. Il peut être recréé avec la commande composer install, donc il n’est généralement pas 
nécessaire de le publier sur GitHub.

## 5. Git Credential Manager

Réponse : Git Credential Manager permet de gérer les informations d’authentification utilisées pour se connecter à des services comme GitHub. Il facilite la connexion 
et évite de saisir les informations d’authentification à chaque opération.