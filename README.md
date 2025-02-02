# Documentation de `nsi_library`

## Introduction
`nsi_library` est une bibliothèque Python conçue pour faciliter l'apprentissage et la mise en pratique des concepts enseignés en NSI (Numérique et Sciences Informatiques) au lycée. Cette bibliothèque implémente des structures de données de base (piles, files, graphes) et des algorithmes classiques (tri, recherche, parcours de graphes, etc.).

## Installation
Pour utiliser cette bibliothèque après sa publication sur PyPI, exécutez la commande suivante :

```bash
pip install nsi_library
```

## Structures de données

### Pile
Une pile (LIFO : Last In, First Out) est une structure de données où le dernier élément inséré est le premier à être retiré.

#### Méthodes
- `est_vide()`: Vérifie si la pile est vide.
- `empiler(element)`: Ajoute un élément au sommet de la pile.
- `depiler()`: Retire et renvoie l'élément au sommet de la pile.
- `sommet()`: Renvoie l'élément au sommet de la pile sans le retirer.

#### Exemple d'utilisation
```python
pile = Pile()
pile.empiler(1)
pile.empiler(2)
print(pile.depiler())  # 2
print(pile.sommet())  # 1
```

---

### File
Une file (FIFO : First In, First Out) est une structure de données où le premier élément inséré est le premier à être retiré.

#### Méthodes
- `est_vide()`: Vérifie si la file est vide.
- `enfiler(element)`: Ajoute un élément à la fin de la file.
- `defiler()`: Retire et renvoie le premier élément de la file.

#### Exemple d'utilisation
```python
file = File()
file.enfiler(1)
file.enfiler(2)
print(file.defiler())  # 1
print(file.defiler())  # 2
```

---

### Graphe
Un graphe est une structure de données composée de sommets et d'arêtes qui relient ces sommets.

#### Méthodes
- `ajouter_sommet(sommet)`: Ajoute un sommet au graphe.
- `ajouter_arete(sommet1, sommet2)`: Ajoute une arête entre deux sommets.
- `voisins(sommet)`: Renvoie la liste des sommets voisins d'un sommet donné.

#### Exemple d'utilisation
```python
graphe = Graphe()
graphe.ajouter_arete("A", "B")
graphe.ajouter_arete("A", "C")
print(graphe.voisins("A"))  # ['B', 'C']
```

---

## Fonctions

### `sous_tableau(tableau, debut, fin)`
Renvoie une portion d'un tableau entre les indices `debut` (inclus) et `fin` (exclu).

#### Exemple d'utilisation
```python
tableau = [1, 2, 3, 4, 5]
print(sous_tableau(tableau, 1, 4))  # [2, 3, 4]
```

---

### `tri_insertion(tableau)`
Trie un tableau en utilisant l'algorithme de tri par insertion.

#### Exemple d'utilisation
```python
tableau = [5, 3, 2, 4, 1]
print(tri_insertion(tableau))  # [1, 2, 3, 4, 5]
```

---

### `recherche_dichotomique(tableau, valeur)`
Recherche une valeur dans un tableau trié en utilisant la méthode dichotomique.

#### Exemple d'utilisation
```python
tableau = [1, 2, 3, 4, 5]
print(recherche_dichotomique(tableau, 3))  # 2
```

---

### `fibonacci(n)`
Calcule le n-ième terme de la suite de Fibonacci (récursivement).

#### Exemple d'utilisation
```python
print(fibonacci(5))  # 5
```

---

### `factorielle(n)`
Calcule la factorielle de `n` récursivement.

#### Exemple d'utilisation
```python
print(factorielle(5))  # 120
```

---

### `parcours_profondeur(graphe, sommet)`
Effectue un parcours en profondeur sur un graphe à partir d'un sommet donné.

#### Exemple d'utilisation
```python
graphe = Graphe()
graphe.ajouter_arete("A", "B")
graphe.ajouter_arete("A", "C")
graphe.ajouter_arete("B", "D")
print(parcours_profondeur(graphe, "A"))  # {'A', 'B', 'C', 'D'}
```

---

### `parcours_largeur(graphe, sommet)`
Effectue un parcours en largeur sur un graphe à partir d'un sommet donné.

#### Exemple d'utilisation
```python
graphe = Graphe()
graphe.ajouter_arete("A", "B")
graphe.ajouter_arete("A", "C")
graphe.ajouter_arete("B", "D")
print(parcours_largeur(graphe, "A"))  # {'A', 'B', 'C', 'D'}
```

---

## Tests unitaires
Des tests unitaires sont inclus dans le fichier principal pour valider le bon fonctionnement des structures de données et des fonctions.

---

## Contribution
Les contributions sont les bienvenues. Créez une issue ou un pull request sur le [dépôt GitHub](https://github.com/votre_nom/nsi_library).

---

## Licence
Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus d'informations.

