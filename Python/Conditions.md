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
On peut les imbriquer ces bloc de code et tout ça c'est grâce au indentations : la touche tab de ton clavier :
![[keyboard.jpeg]]
Cela permet de les regrouper. Les tabs font en général 4 espaces : `    ` mais peuvent en faire autant que tu veux. Ce qui compte c'est que ces espaces doivent être de la même longueur tout du long d'un fichier.

### If
Pour traduire un **si** de la vraie vie on utilise donc le mot clé `if` puis une condition et un `:` à la fin de la ligne. Le bloc de code sera exécuté seulement si la condition est égale à `True`.
```py
question = input("Executer cette  action ? [yes/no] : ")
if question == "yes":
	print("Action effectuée !")
```
Ici, si l'utilisateur répond `yes`, le programme répond `Action effectuée !`. Si l'utilisateur répond autre chose, il ne se passe rien d'autre.

### Else
Littéralement traduit de l'anglais par "Sinon" on l'utilise de cette manière, après un bloc de code `if`. Son bloc est exécuté si la condition du dernier `if` n'a pas été remplie.
```py
question = input("Executer cette  action ? [yes/no] : ")
​if question == "yes":
	print("Action effectuée !")
else :
	print("Action annulée !")
```

### Elif
Un `elif` est la combinaison d'un `if` imbriqué dans un `else`.
Au lieu d'écrire un `else` puis un `if` :
```py
question = input("Executer cette  action ? [yes/no] : ")
​if question == "yes":
	print("Action effectuée !")
​else:
	if question == "no":
		print("Action annulée !")
```
On écrira :
```py
question = input("Executer cette  action ? [yes/no] : ")
​if question == "yes":
	print("Action effectuée !")
​elif question == "no":
	print("Action annulée !")
```

### Combinaison
Pour combiner ces 3 mots clés on l'écris dans un certain ordre sous peine d'erreurs :
```py
if condition_1:
	action_1()
elif condition_2:
	action_2()
elif condition_3:
	action_3()
else:
	action_par_defaut()
```

> [!CAUTION]
> Les conditions sont évaluées une par une. Si une d'elle est vérifié, donc égale à `True`, les conditions suivantes ne seront pas évaluées et le programme va "sauter" à la fin du bloc.

### Exercice 3 :
Crée un magasin virtuel. Lorsque l'on arrive dans le programme on choisi un budget puis un article à acheter. Si le budget n'est pas assez élevé, le programme s'arrête. Sinon le programme annonce que la transaction a réussi !

**Les articles :**
- Plante en pot : 7,50€
- Draps : 39,99 €
- Cookies : 2,50 €
- Calculatrice : 20,00 €
- Peluche : 11,50 €
- Sandwich au saumon : 3,21 €

> [!QUESTION]- Reponse
> ```py
> articles = {
> "Plante en pot": 7.50,
> "Draps": 39.99,
> "Cookies": 2.5,
> "Calculatrice": 20.0,
> "Peluche": 11.5,
> "Sandwich au saumon": 3.21
> }
> budget = float(input("Entrez votre budget : "))
> article = input("""
> Chosisez l'article qui vous plait :
> Plante en pot
> Draps
> Cookies
> Calculatrice
> Peluche
> Sandwich au saumon
> >>> """)
> if articles[article] <= budget:
> 	print("Transaction effectuée !")
> 	print("Il vous reste {budget - articles[article]} €")  # Facultatif
> else:
> 	print("Transaction annulée !")
> 	print("Il vous manque {articles[article] - budget} €")  # Facultatif
> ```

