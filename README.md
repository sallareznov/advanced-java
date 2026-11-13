# Java avancé : projets

Ce dépôt contient les sujets des projets du cours de Java avancé.
Chaque sujet est décrit dans son propre fichier.

| | Projet | Sujet | Points | En une phrase |
|---|---|---|---|---|
| 🟦 Obligatoire | Particules | [particles.md](particles.md) | 8 | Des particules colorées se déplacent en plein écran et rebondissent entre elles. |
| 🟦 Obligatoire | Wa-Tor | [wator.md](wator.md) | 6 | Des thons et des requins vivent, se reproduisent et se mangent sur une planète recouverte d'eau. |
| 🟧 Au choix | Carrefour | [traffic.md](traffic.md) | 6 | Des voitures, des bus et des camions traversent un carrefour réglé par des feux. |
| 🟧 Au choix | Donjon | [dungeon.md](dungeon.md) | 6 | Un héros dirigé au clavier ramasse une clé, combat des monstres et cherche la sortie. |
| 🟧 Au choix | Serpent | [snake.md](snake.md) | 6 | Le jeu du serpent, avec quatre aliments qui ont chacun un effet différent. |
| 🟧 Au choix | Poursuite | [chase.md](chase.md) | 6 | Une proie dirigée au clavier fuit des prédateurs qui calculent le chemin le plus rapide avec l'algorithme de Dijkstra. |

🟦 Particules et Wa-Tor sont **obligatoires**.

🟧 Pour le troisième projet, vous en choisissez **un seul** parmi Carrefour, Donjon, Serpent et
Poursuite, ou vous proposez un sujet libre (voir ci-dessous).
Poursuite est le plus difficile des quatre : il demande d'écrire l'algorithme de Dijkstra.

## Notation

Les projets sont notés sur **20 points** au total :

- **Particules : 8 points** ;
- **Wa-Tor : 6 points** ;
- **Troisième projet : 6 points.** Vous avez le choix entre cinq possibilités :
  - le projet **Carrefour** ;
  - le projet **Donjon** ;
  - le projet **Serpent** ;
  - le projet **Poursuite** ;
  - un **sujet libre**, que vous proposez vous-même. Il doit être validé par l'enseignant
    avant que vous ne commenciez, et il respecte les règles communes ci-dessous.

## Règles communes à tous les projets

- **Vous partez de zéro.** Aucun code de départ n'est fourni, et la liste des classes à écrire
  n'est pas donnée : la conception fait partie du travail.
- **Ce sont des projets de Java, pas de JavaFX.** JavaFX sert uniquement à afficher. Toute la
  logique est écrite en Java, dans des classes qui ne connaissent pas JavaFX.
- **Deux paquetages au minimum** : `model` pour la logique, `view` pour l'affichage.
  Aucun `import javafx` dans `model`.
- **Le code est en anglais** : noms de classes, de méthodes, de variables et commentaires.
