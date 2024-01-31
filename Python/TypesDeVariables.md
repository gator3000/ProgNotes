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

Les booléens ou `bool` ou `boolean` sont un type de variable qui ne peut avoir que deux états `True`("vrai" en anglais) et `False` ("faux" en anglais). Il sera très utile dans un autre chapitre [[Conditions]]
```py
mon_bool = True
mon_bool = False
print(mon_bool)
# Output : False
```


On en à déjà beaucoup parlé de ces chaines de caractères qui se nomment `strings`. Les strings supportent deux opérateurs `*` et `+`. Tout nos types de variables peuvent être convertis en string :
```py
print("hello " + "world " + "!")
# Output : hello world !

print("hello world !" * 3)
# Output : hello world !hello world !hello world !

print(str(2.3)*2)
# Output : 2.32.3
```
