[Retour](Summary)
___
> [!CHECKPOINT]
> Jusqu’ici on a vu de types de variables simples [[Variables & calculs]].
Dans ce chapitre on va approfondir ce sujet et découvrir les itérables.

## Les types de Variables Simples
1. Entiers
2. Décimaux
3. Booléens

### Integers
Commençons par les entiers.
Ce sont donc des nombres entiers comme en mathématiques. À partir de maintenant, on les appellera les `int`ou `integers`. On peut effectuer tout les calculs des opérateurs présentés plus tôt [[Variables & calculs#I.1.2 Les Opérateurs]].
On peut convertir une chaîne de caractères en entier si le cœur t'en dis :
```py
print(int("36")*2)
# Output : 72
```

### Floats
Les décimaux que l'on appellera les `floats` se comportent pareils à l'exception du fait qu'ils peuvent avoir des virgules. On peut aussi effectuer tout les calculs des opérateurs présentés plus tôt [[Variables & calculs#I.1.2 Les Opérateurs]]. Et à partir d'une chaine, on utilise `float()` :
```py
print(float("2.3")*3)
# Output : 6.9
```

### Bool
Les booléens ou `bool` ou `boolean` sont un type de variable qui ne peut avoir que deux états `True`("vrai" en anglais) et `False` ("faux" en anglais). Il sera très utile dans un autre chapitre [[Conditions]].
```py
mon_bool = True
mon_bool = False
print(mon_bool)
# Output : False
```

## Les types de Variables Itérables
1. Chaines
2. Listes & Tuples
3. Sets et Dictionnaire

> [!DEFINITION]
> "Itérable" signifie qu'on va pouvoir les parcourir par itérations dans des [boucles](Boucles).

### Strings
On en à déjà beaucoup parlé de ces chaines de caractères qui se nomment `strings`. Pour les définir il faut mettre des guillemets ou des apostrophes ou encore des triple guillemets (pour des chaines sur plusieurs lignes (sinon cela va provoquer une erreur)) Les strings supportent deux opérateurs `*` et `+`. Tout nos types de variables peuvent être convertis en string :
```py
mon_str = """Hello
World
!"""
print(mon_str)
# Output : Hello
# World
# !

print("hello " + "world " + "!")
# Output : hello world !

print("hello world !" * 3)
# Output : hello world !hello world !hello world !

print(str(2.3)*2)
# Output : 2.32.3
```
On peut transformer une string en liste selon un certain caractère :
```py
ma_string = "ma grande phrase bien grande grandie à la grande"
# on va séparer chaque partie de la chaine au endroits ou le caractere " " se trouve.
ma_liste_de_mot = ma_string.split(" ")
print(ma_liste_de_mot)
# Output : ['ma', 'grande', 'phrase', 'bien', 'grande', 'grandie', 'à', 'la', 'grande']

print(ma_string.split("a"))
# Output : ['m', ' gr', 'nde phr', 'se biengr', 'nde gr', 'ndie à l', ' gr', 'nde']

ma_string.split("grand")  
# Output : ['ma ', 'e phrase bien', 'e ', 'ie à la ', 'e']
```

> [!REMARQUE]
> Le caractère utilisé n’apparaît donc pas dans les items de la liste !

### Listes
Pour stocker des informations dans un certain ordre, on utilisera des listes. Elles contiennent plusieurs valeurs, des `items` de types différent (ou pas) qui peuvent être utilisés grâce à leur indice mis entre `[0]`. Elles sont définies avec des `[]` autours des valeurs et des virgules entre les items.
> [!TIP]
> On peut créer une liste vide avec `ma_liste = list()`. Cette syntaxe set préférable par rapport a deux crochets Selon la [PEP8](https://python.doctor/page-pep-8-bonnes-pratiques-coder-python-apprendre).

```py
mon_test = [3, "Bonjour", 50.3] # On créer une liste avec 3 items
ma_liste = [] # On créer une liste vide
ma_liste.append(3) # On ajoute une valeur (3) à la liste
ma_liste.append("Hello") # "
ma_liste.append("World") # "

print(ma_liste)
# Output : [3, "Hello", "World"]

mon_entier = ma_liste[0] + 3
print(mon_entier)
# Output : 6

ma_chaine = ma_liste[2] + ma_liste[1]
print(ma_chaine)
# Output : WorldHello

del ma_liste[0]  # Supprime des items
print(ma_liste)
# Output : ["Hello", "World"]

print(len(ma_liste)) # Affiche le nombre d'items dans la liste
# Output : 2

print(ma_liste + mon_test)
# Output : [3, 'Bonjour', 50.3, "Hello", "World"]

print(mon_test * 3)
# Output : [3, 'Bonjour', 50.3, 3, 'Bonjour', 50.3, 3, 'Bonjour', 50.3]
```

> [!IMPORTANT]
> Vous avez surement remarqué mais `l'indice 0` correspond au premier item et `l'indice 1` correspond lui au deuxième item et non au premier.
> De manière générale, en programmation on compte à partir de zéro et pas de 1.

Pour joindre des strings dans une liste on utilise `join(list)`, un peu l'inverse de `.split()` :
```py
print(" ".join(['ma', 'grande', 'phrase', 'bien', 'grande', 'grandie', 'à', 'la', 'grande']))
# Output : 'ma grande phrase bien grande grandie à la grande'
```
### Tuples
Les tuples sont comme des listes mais ils ne peuvent pas être modifiés. Il sont définis avec des `()` et une virgule entre chaque item pour les séparer. Ils gardent leur ordre comme les listes puisque leur indice est basé sur leur position.
```py
mon_tuple = ("Hey", 3, True)
print(mon_tuple[1])
# Output : 3

mon_tuple[0] = False
# Output : TypeError: 'tuple' object does not support item assignment

del mon_tuple[2]
# Output : TypeError: 'tuple' object doesn't support item deletion

mon_tuple.append(2.5)
# Output : AttributeError: 'tuple' object has no attribute 'append'
```

### Sets
Les sets sont un type qui se définit avec des `{}` dont les items sont séparés avec des virgules. Dans un set, chaque élément doit être **unique** et **immuable**, c’est-à- dire qu'il ne peut pas être modifié. Les éléments n'ont pas d'**ordre** particulier.
On peut donc stocker des chaînes de caractères, des nombres et des tuples dans un set mais pas de listes ou de dictionnaires !
Les sets sont utiles pour **contrôler les doublons** et effectuer des opérations sur les ensembles comme les unions, les différences, les intersections, etc.
```py
my_empty_set = set()
my_set = {3, "Hey", 3, 2.5}
print(my_set)
# Output : {'Hey', 2.5, 3} # Remarquez que python à supprimé tout seul le doublon (3) et que l'ordre à changé

print(my_set[0])
# Output : TypeError: 'set' object is not subscriptable

my_set.add("Hello")  # On ajoute "Hello" à ce set
print(my_set)
# Output : {'Hey', 2.5, 3, 'Hello'}

my_set.discard("Hey")  # On enlève "Hey" à ce set
print(my_set)
# Output : {2.5, 'Hello', 3}
```

> [!CAUTION]
> /!\\ Lorsqu'un output est un erreur le programme s’arrête normalement mais afin de le voir jusqu'à la fin, je les ai ignorés.

Un set c'est en fait l'équivalent python d'un ensemble mathématique :

```py
a = {1, 2, 3}
b = {3, 4, 5}

print(a | b) # A union B
# Output : {4, 3, 5, 1, 2}

print(a & b) # A inter B
# Output : {3}

print(a - b) # différences de A sur B
# Output : {2, 1}

print(a ^ b) # différences entre A et B
# Output : {4, 2, 5, 1}
```

### Frozensets

Les frozensets sont exactement pareils que les sets sauf qu'ils ne peuvent pas êtres modifiés.
```py
fa = frozenset([1, 2, 3]) # on peut mettre entre parnthèses soit une liste soit un set soit un tuple

print(s)    # frozenset({1, 2, 3})
print(len(s))   # 3
print(s.add('bones')) # AttributeError: 'frozenset' object has no attribute 'add'
```


### Dictionnaires

Les dictionnaire aussi appelés `dicts` sont créés par `{}` ou `dict()`.Ce sont comme des tableau ou une clé correspond à une valeur.

| Keys | Values |
| ---- | ---- |
| `"proprio"` | `"Mme Martin"` |
| `"marque"` | `"BMW"` |
| `"model"` | `"325 i"` |
| `"annee"` | `1992` |
Se traduit par :
```py
my_dict = {"proprio": "Mme Martin", "marque": "BMW", "model": "325 i", "annee": 1992}

# On peut aussi écrire, les retours a la ligne ne comptent pas
my_dict_2 = {
"proprio": "Mme Martin",
"marque": "BMW",
"model": "325 i",
"annee": 1992
}
```
Pour récupérer un item d'un dictionnaire on met l'indice entre `["indice"]`.
```py
# On considaire le code ci-dessus

print(my_dict["marque"])
# Output : "BMW"

my_dict["couleur"] = "black"
print(my_dict)
# Output : {"proprio": "Mme Martin", "marque": "BMW", "model": "325 i", "annee": 1992, "couleur": "black"}
```
On peut récupérer les clés et les valeurs sous forme de liste :
```py
# On considaire le code ci-dessus

print(list(my_dict))
# Output : ['proprio', 'marque', 'model', 'annee', 'couleur']

print(list(my_dict.values()))
# Output : ['Mme Martin', 'BMW', '325 i', 1992, 'black']
```