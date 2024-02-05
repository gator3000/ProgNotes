[Retour](Summary)
___

### Inputs
Pour pimenter nos programmes on va utiliser les entrées de programme (`input`).
Grace à cette instruction, on va pouvoir demander à l'utilisateur une valeur :
```py
la_reponse = input("Ma question : ") # input prends la valeur entrée par l'utilisateur
print(la_reponse)  # Ici on print la  reponse entrée par l'utilisateur
```

> [!NOTE]
> L'instruction `input("question")` peut se résumer à un `print()` de "`question`" puis le programme va attendre que l'utilisateur entre une valeur et tape sur "Entrée". Il assignera la valeur toujours sous forme de string (même si c'est un nombre) que l'utilisateur a tapée à la variable à gauche du `=`.

Pour avoir un nombre à la sortie de `input` on utilise `int` ou `float`:
```py
# Code Valide
a = float(input("Donnez moi un nombre"))
b = float(input("Donnez moi un autre nombre"))
print("Voici le résultat de leur addition :")
print(a + b) # Si 2 et 3 entrés | Output : 5

# Code Invalide
a = input("Donnez moi un nombre")
b = input("Donnez moi un autre nombre")
print("Voici le résultat de leur addition :")
print(a + b) # Si 2 et 3 entrés | Output : 23
```


### Conditions
Les condition sont des valeurs Vraies ou Fausses.
Grâce à elles on peut faire des choix dans la vie. Par exemple : ***Si** il pleut, **Alors** je prend mon parapluie*.
On utilise alors des opérateurs :

| Opérateur | Effet | Exemple | Résultat | Exemple 2 | Résultat |
| :--: | :--: | :--: | :--: | :--: | :--: |
| `==` | "est égal ?" | `3 == 2` | `False` | `"3" == 3` | `False` |
| `!=` | "n'est pas égal ?" | `3 != 2` | `True` | `"hey" != "hey"` | `True` |
| `<` | "est plus petit ?" | `3 < 2` | `False` | `len("hey") < 2` | `False` |
| `>` | "est plus grand ?" | `3 > 3` | `False` | `100 > 105` | `True` |
| `<=` | "est plus petit ou égal ?" | `2 <= 2` | `True` | `len("nom") <= 15` | `True` |
| `>=` | "est plus grand ou égal ?" | `2 >= 2` | `True` | `5 >= 10` | `False` |
| `or` | "ou" | `True or False` | `True` | `False or False` | `False` |
| `and` | "et" | `True or False` | `False` | `True or True` | `True` |
| `` | " ?" | `` | `` | `` | `` |
Exemple :
```py
user_input = input("Ecrivez cette lettre > a : ")
ma_condition = user_input == "a"
print(ma_condition)
```


### Bloc de code ?

En python, lorsque que l'on regroupe des instructions après certains mots clés, on fait un bloc de code. 

![[th.jpeg|300]]
On peut les impriquer ces bloc de code et tout ça c'est grac au indentations : la touche tab de ton clavier : ![[keyboard.jpeg]]