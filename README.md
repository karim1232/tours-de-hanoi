# 🗼 Tours de Hanoï

Jeu des **Tours de Hanoï** en **Python**, avec un affichage graphique en **Turtle** et une résolution automatique animée.

**Le but :** déplacer tous les disques de la tour de gauche à la tour de droite. On déplace un seul disque à la fois, et un disque ne peut jamais être posé sur un disque plus petit.

## ✨ Fonctionnalités

- Plateau et disques dessinés avec Turtle (une couleur par disque)
- Coups saisis dans le terminal (tour de départ puis tour d'arrivée). Les coups interdits sont refusés avec un message
- **Annuler** le dernier coup
- **Abandonner** à tout moment
- **Chronomètre** et compteur de coups. On gagne si on finit en au plus `2ⁿ + n` coups (le minimum possible est `2ⁿ − 1`)
- **Solution animée** : l'algorithme récursif résout le jeu sous tes yeux
- **Tableaux de fin de partie**, par nombre de disques :
  - meilleurs scores (nombre de coups)
  - meilleurs temps
  - classement par temps de réflexion moyen par coup

## 🚀 Lancer

Il faut **Python 3**, sans rien installer de plus (Turtle est inclus dans Python).

```bash
python tours_de_hanoi.py
```

Clique dans la fenêtre pour commencer, puis réponds aux questions dans le terminal (de 1 à 7 disques).

## 🧠 L'algorithme récursif

Pour déplacer `n` disques de A vers C :
1. déplacer `n − 1` disques de A vers B (récursivement)
2. déplacer le plus grand disque de A vers C
3. déplacer les `n − 1` disques de B vers C (récursivement)

Cela donne la solution optimale en `2ⁿ − 1` coups.

## 📁 Organisation du code

| Partie | Contenu |
|---|---|
| Plateau | Représentation du plateau en listes, vérification des coups et de la victoire |
| Graphisme | Dessin du plateau, des disques, effacement |
| Jeu | Lecture des coups, boucle de jeu, chronomètre |
| Annulation | Historique des positions, retour au coup précédent |
| Scores | Sauvegarde et affichage des tableaux de scores, temps et classements |
| Solution | Résolution récursive et animation |

## 👤 Auteur

Karim Glelah
