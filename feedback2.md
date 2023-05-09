Le menu est accessible sans être connecté, il faudrait dans la vue header faire une condition avec Twig pour afficher le menu que si on est connecté (et avec une vérification sur le rôle).
Ne pas hésiter à regarder la documentation sur Twig et notamment sur la condition if (voir https://twig.symfony.com/doc/3.x/tags/if.html)
De la même manière toutes les vues sont disponible peu importe le rôle. Il faut penser à faire une vérification avant d'afficher les pages.
Attention il y a un problème avec la vue de l'erreur 404 (le fichier n'existe pas)
