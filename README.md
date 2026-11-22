# Tours de Hanoï

Le jeu des tours de Hanoï en Python, avec un affichage graphique en Turtle et une résolution automatique animée.

Le but est de déplacer tous les disques de la tour de gauche à la tour de droite, un seul disque à la fois, sans jamais poser un disque sur un plus petit.

## Fonctionnalités

- Plateau et disques dessinés avec Turtle, une couleur par disque
- Coups tapés dans le terminal (tour de départ, puis tour d'arrivée) ; un coup interdit est refusé avec un message
- Annulation du dernier coup
- Abandon possible à tout moment
- Chronomètre et compteur de coups. On gagne si on termine en `2ⁿ + n` coups au maximum (le minimum possible est `2ⁿ − 1`)
- Solution animée : l'algorithme récursif résout le jeu sous tes yeux
- Tableaux de fin de partie pour chaque nombre de disques : meilleurs scores (en nombre de coups), meilleurs temps, et classement par temps de réflexion moyen par coup

## Lancer

Il suffit de Python 3, Turtle est déjà inclus.

```bash
python tours_de_hanoi.py
```

Clique dans la fenêtre pour commencer, puis réponds aux questions dans le terminal.

## L'algorithme récursif

Pour déplacer `n` disques de A vers C :
1. déplacer `n − 1` disques de A vers B (récursivement)
2. déplacer le plus grand disque de A vers C
3. déplacer les `n − 1` disques de B vers C (récursivement)

On obtient la solution optimale, en `2ⁿ − 1` coups.

## Organisation du code

| Partie | Contenu |
|---|---|
| Plateau | plateau représenté par des listes, vérification des coups et de la victoire |
| Graphisme | dessin du plateau et des disques, effacement |
| Jeu | lecture des coups, boucle de jeu, chronomètre |
| Annulation | historique des positions, retour au coup précédent |
| Scores | sauvegarde et affichage des tableaux de scores, de temps et de classement |
| Solution | résolution récursive et animation |

## Auteur

Karim Glelah
