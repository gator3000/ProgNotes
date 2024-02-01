[Retour](Summary)
___
> [!CHECKPOINT]
> Jusqu’ici on a vu de types de variables simples [[Variables&calculs]].
Dans ce chapitre on va approfondir ce sujet et découvrir les itérables.

## Les types de Variables Simples
1. Entiers
2. Décimaux
3. Booléens


Commençons par les entiers.
Ce sont donc des nombres entiers comme en mathématiques. À partir de maintenant, on les appellera les `int`ou `integers`. On peut effectuer tout les calculs des opérateurs présentés plus tôt [[Variables&calculs#I.1.2 Les Opérateurs]].
On peut convertir une chaîne de caractères en entier si le cœur t'en dis :
```py
print(int("36")*2)
# Output : 72
```


Les décimaux que l'on appellera les `floats` se comportent pareils à l'exception du fait qu'ils peuvent avoir des virgules. On peut aussi effectuer tout les calculs des opérateurs présentés plus tôt [[Variables&calculs#I.1.2 Les Opérateurs]]. Et à partir d'une chaine, on utilise `float()` :
```py
print(float("2.3")*3)
# Output : 6.9
```

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

Pour stocker des informations dans un certain ordre, on utilisera des listes. Elles contiennent plusieurs valeurs, des `items` de types différent (ou pas) qui peuvent être utilisés grâce à leur indice mis entre `[]`. Elles sont définies avec des `[]` autours des valeurs et des virgules entre les items.
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

Les sets sont des types assez pratiques qui se définissent avec des `{}` dont les items sont séparés avec des virgules. L'ordre des valeurs n'a pas d'importance et un set ne peut pas stocker plusieurs fois la même valeur.
```py
my_empty_set = set()
my_set = {3, "Hey", 3, 2.5}
print(my_set)
# Output : {'Hey', 2.5, 3} # Remarquez que python à supprimé tout seul le doublon (3) et que l'ordre à changé

print(my_set[0])
# Output : TypeError: 'set' object is not subscriptable

my_set.add("Hello")  # On ajoute "Hello" a ce set
print(my_set)
# Output : {'Hey', 2.5, 3, 'Hello'}
```

> [!CAUTION]
> Erreurs != Terminal