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

On en à déjà beaucoup parlé de ces chaines de caractères qui se nomment `strings`. Les strings supportent deux opérateurs `*` et `+`. Tout nos types de variables peuvent être convertis en string :
```py
print("hello " + "world " + "!")
# Output : hello world !

print("hello world !" * 3)
# Output : hello world !hello world !hello world !

print(str(2.3)*2)
# Output : 2.32.3
```

Pour stocker des informations dans un certain ordre, on utilisera des listes. Elles contiennent plusieurs valeurs, des `items` de types différent (ou pas) qui peuvent être utilisés grâce à leur indice.
```py
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

del ma_liste[0]
print(ma_liste)
# Output : ["Hello", "World"]
```