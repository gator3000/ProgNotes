[Retour](Summary)
___
# I.1 Variables et sorties

### I.1.0 Petite parenthèse :

> [!IMPORTANT]
> Lorsque il y a un `#` sur une ligne de code cela signifie que l'interpréteur ne va pas lire les caractères après le Hashtag sur cette ligne.
> Cela s'appelle un commentaire.

Avant tout, tu dois savoir une chose : pour afficher quelque chose, il faut utiliser une instruction : le print, sa syntaxe est la suivante : 
```py
print(une_valeur)
```

^ee7155

À la place de `une_valeur` tu écriras soit un nombre, soit une chaîne de caractères (string) soit une variable, on y reviendra [[Variables&calculs#Utilisons là maintenant.]].
> [!NOTE]
> pour écrire un nombre à virgule flottante (décimal) on utilisera le point : 
> ```py
> 3.4
> # Et pas 3,4
> ```

Par exemple, pour afficher un texte `Hello World !` ou un nombre (3,25) on écrira
```py
# Texte
print("Hello World !")
# Output : Hello World !
# Nombre
print(3.25)
# Output : 3.25
```

### I.1.1 Les Variables :

> [!DEFINITION]
> On peut considérer une variable comme une boite qui aurait un nom et une valeur.

Pour définir cette variable il faut un nom. Ce nom ne devra pas commencer par une majuscule ni un nombre. Il ne pourra pas non plus contenir autre chose que des lettres des chiffres et des `underscore`. Voici des exemples de noms de variables :
```py
# Nom valide et recomandé
ma_variable_1
# Noms valides mais à éviter
maVariable2
Ma_Variable3
# Nom invalide
4iemeVariable
```
En résumé : 
1. Pas de caractères spéciaux ou d'accents
2. Pas de chiffres au début
3. Pas de majuscules
4. Ecrite en "snake_case"
5. Plusieurs caractères sauf pour les variables de boucle et de convention mathématiques (ex : `x` et `y` pour des axes sur un repère)

![Description de trois types de mise en forme de nom](https://juniortoexpert.com/wp-content/uploads/naming-convention-snake-case-kebab-case-camel-case.png)


Maintenant qu'on a son nom, il nous faut une valeur.
Il faut savoir que en python il n'y a pas besoin de spécifier le type de nos variables, seulement de leur affecter une valeur spécifié après un signe `=`.
Exemple :
```py
ma_variable = "chaine de caractères"
ma_variable_2 = 3 #int > entier
ma_variable_3 = 2.069 # float > virgule flotante
```
Ça y est ! Nous avons déclaré notre première variable.

###### Utilisons là maintenant. 

Pour afficher la valeur d'une variable on se réfère à [[#^ee7155]].
Exemple :
```py
ma_variable = "Hello world !"
print(ma_variable)
# Output : Hello world !
```
Ici on définit `ma_variable` à un message et dans la deuxième ligne on récupère la valeur de `ma_variable` et on la donne à l'instruction `print()` qui l'affiche.

### I.1.2 Les Opérateurs :

Dans la vie les nombres on peut les additionner, multiplier... Et bien sur python, on peut aussi !
1. L'addition : `+`
2. La soustraction : `-`
3. La multiplication : `*`
4. La division : `/`
5. La division entière : `//` (renvoie le quotient de la division)
6. Le modulo : `%` (renvoie le reste de la division)

```py
3 + 6
# Output : 9
2 - 1
# Output : 1
5 * 2
# Output : 10
20 / 6
# Output : 3.3333333333333335
20 // 6
# Output : 3
20 // 6
# Output : 2
```

> [!CAUTION]
> Python n'est pas très précis quand il s'agit de chiffres à virgule

On peut aussi faire nos opérations avec des variables :
```py
example_num = 5
example_num2 = 6

print(example_num * 2)
# Output : 10

print(example_num // 2)
# Output : 2

print(example_num2 + example_num)
# Output : 11
```

> [!WARNING]
> Attention : si tu demandes à python d'opérer avec des chaînes de caractères même si a l’intérieur il n'y a que des nombre, il ne se passera pas ce que tu espère. Exemple : 
> ```py
> error_num = "27"
> error_num_2 = "3"
> number = 2
> print(error_num * number)
> # Output : 2727
> print(error_num + error_num_2)
> # Output : 273
> ```
Toutes les autres configurations donneront des erreurs

Pour des calculs composés il faut connaitre les priorités de calculs de python :
1. Ce qui est à l’intérieur des parenthèses : `3 * (2 + 3)` donnera `15` et non `9`.
2. Les multiplications et divisions (avec les modulo et divisons entières)
3. Enfin les additions et soustractions.
Le reste est exécuté dans l'ordre

### Exercice 1 :
Que donne ce programme ? 
```py
ma_variable = "50"
ma_variable_2 = 2
ma_variable_3 = "5"
print(ma_variable + (ma_variable_2 / 0.5 * ma_variable_3))
```
