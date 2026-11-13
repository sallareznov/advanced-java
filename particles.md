# Projet : Particules

Des particules colorées se déplacent en plein écran. Chacune part dans une direction
choisie au hasard, rebondit sur les bords de l'écran, et change de direction quand elle
en percute une autre.

![Aperçu de l'application](assets/particles/apercu.png)

Une vidéo d'une exécution est disponible ici : [demo.mp4](assets/particles/demo.mp4).
Elle fait référence : votre application doit se comporter de la même façon.

## Objectifs

Ce projet est un projet de **Java**, pas de JavaFX. À la fin, vous aurez pratiqué :

- la conception de plusieurs classes qui collaborent ;
- l'encapsulation (attributs privés, visibilité de paquetage, objets immuables) ;
- les collections et les streams ;
- les interfaces et les lambdas ;
- la séparation entre le **modèle** (la logique) et la **vue** (l'affichage).

Vous partez de zéro. Le sujet décrit ce que l'application doit faire et les règles à
respecter. Il ne donne ni la liste des classes ni les étapes à suivre : la conception et
l'organisation du travail vous reviennent.

## Ce que fait l'application

- L'application s'ouvre en plein écran, sur fond sombre, sans bouton ni panneau.
- Elle contient un nombre fixe de particules (150), créées au démarrage. Ce nombre ne change plus ensuite.
- Chaque particule est un disque de 8 pixels de rayon, d'une couleur tirée au hasard.
- Chaque particule démarre à un endroit libre (elle ne touche aucune autre particule), dans une
  direction tirée au hasard, à 150 pixels par seconde.
- Une particule rebondit sur les quatre bords de l'écran.
- Deux particules qui se touchent rebondissent l'une sur l'autre. Le choc est élastique et
  toutes les particules ont la même masse.
- La touche Espace met en pause et relance. La touche Échap quitte l'application.

## Règles à respecter

Ces règles font partie du sujet. Elles seront vérifiées.

1. **Deux paquetages : `model` et `view`.** Tout ce qui décide quelque chose (déplacement,
   rebonds, collisions, choix des couleurs) est dans `model`. Tout ce qui affiche est dans `view`.
2. **Aucun `import javafx` dans le paquetage `model`.** Le modèle doit pouvoir fonctionner
   sans fenêtre.
3. **Une particule n'est pas un cercle JavaFX.** La classe qui représente une particule
   n'hérite pas de `Circle`, ne contient pas de `Circle` et ne sait pas se dessiner.
   C'est la vue qui connaît le modèle, jamais l'inverse.
4. **Le modèle ne connaît pas la vue.** Aucune classe de `model` n'utilise une classe de `view`.
5. **Tous les attributs sont privés.** Aucun attribut `public`, aucune variable `static` modifiable.
6. **Les positions et les vitesses sont des vecteurs immuables.** Vous écrivez vous-même une
   classe de vecteur à deux dimensions : ses attributs sont `final` et chaque opération
   renvoie un nouveau vecteur. N'utilisez pas `Point2D` de JavaFX.
7. **Une particule ne peut pas être modifiée par n'importe qui.** Les méthodes qui changent
   sa position ou sa vitesse ne sont pas `public`. De même, la collection des particules ne
   doit pas pouvoir être modifiée depuis l'extérieur de la classe qui la possède.
8. **Pas de `instanceof`.**
9. **La partie JavaFX reste petite** : environ 150 lignes au total dans `view`. Si elle
   grossit, c'est que de la logique s'est glissée dans la vue.
10. **Un programme console.** En plus de l'application, vous fournissez un second `main` qui
    fait tourner la simulation sans ouvrir de fenêtre : il crée 100 particules, fait 1 000 pas
    de 1/60 de seconde, et affiche avant et après le nombre de particules, la vitesse moyenne
    et la somme des carrés des vitesses, calculées avec des **streams**.

## Critères de validation

Votre travail est correct si :

- l'application se comporte comme décrit plus haut ;
- après 1 000 pas, toutes les particules sont encore dans l'écran et leur nombre n'a pas changé ;
- deux particules lancées l'une vers l'autre sur la même ligne, avec les vitesses (100, 0) et
  (−40, 0), repartent avec les vitesses échangées : (−40, 0) et (100, 0) ;
- dans le programme console, le nombre de particules et la somme des carrés des vitesses sont
  identiques avant et après. Si la somme des carrés change, votre rebond est faux ;
- toutes les règles ci-dessus sont respectées.

## Ce que vous rendez

- Le projet Maven complet, qui se lance avec `mvn javafx:run`.
- Le programme console.
- Un court fichier `README.md` qui liste vos classes, avec une phrase par classe pour
  expliquer son rôle, et qui justifie vos choix de conception.

## Pour aller plus loin

Ces extensions sont facultatives.

- **Aller plus vite.** Comparer toutes les paires de particules devient lent avec plusieurs
  milliers de particules. Découpez le rectangle en cases et ne comparez que les particules
  de cases voisines. Rien ne doit changer dans `view`.
- **Plusieurs types de particules.** Une particule lourde (masse × 10), une particule fantôme
  qui traverse les autres, une particule collante qui absorbe celles qu'elle touche.
  Sans `instanceof` : c'est à chaque particule de dire comment elle se comporte.
- **Un compteur à l'écran.** Affichez le nombre de collisions depuis le démarrage, sans
  toucher au modèle.
