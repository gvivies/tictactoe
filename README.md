# Tic Tac Toe Game

## Etat actuel

Ce jeu implémente une version simplifiée du Morpion (ou Tic Tac Toe en anglais)

Il possède deux méthodes principales qui permettent à l'utilisateur :

1. move : choisir le prochain mouvement de l'utilisateur avec la position gagnante ou la première case vide.
2. winner : teste si un tableau a un gagnant, mais le test est fait seulement sur les lignes.

## Les évolutions

Il est demandé d'implémenter les deux prochaines évolutions dans cet ordre :

1. permettre à la méthode winner de vérifier aussi les colonnes et les diagonales.
2. permettre à la méthode move de retourner la position pour bloquer l'adversaire si le joueur n'a pas de position
   gagnante

## Quelques exemples pour mieux comprendre

Representation du Board : "012345678"

```
 0 | 1 | 2   
---|---|---
 3 | 4 | 5   
---|---|---
 6 | 7 | 8
```

### Exemples de boards avec un gagnant :

#### Cas 1 :

Pour la grille suivante :

```
   | O |    
---|---|---
   | O |    
---|---|---
 X | X | X
```

On a :

- Stringbuffer "-O--O-XXX"
- game.winner() = "X"
- game.move("O") = "0"

#### Cas 2 :

Pour la grille suivante :

```
 O | O | O   
---|---|---
 X |   |    
---|---|---
 X |   | X
```

On a :

- Stringbuffer "OOOX--X-X"
- game.winner() = "O"
- game.move("O") = "7"

### Exemples de boards avec un coup gagnant à jouer :

#### Cas 1 :

Pour la grille suivante :

```
 O | O |    
---|---|---
 X |   |    
---|---|---
 X |   | 
```

On a :

- Stringbuffer "OO-X--X--"
- game.winner() = "-"
- game.move("O") = 2

#### Cas 2 :

Pour la grille suivante :

```
   | O |    
---|---|---
   |   | O   
---|---|---
 X | X | 
```

On a :

- Stringbuffer "-O---OXX-"
- game.winner() = "-"
- game.move("X") = 8
