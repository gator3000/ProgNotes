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
À la place de `une_valeur` tu écriras soit un nombre, soit une chaîne de caractères (string) soit une variable, on y reviendra.
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
Il faut savoir que en python il n'y a pas besoin de spécifier le type de nos variables, seulement de leur affecter une valeur spécifié après le signe `=`. Exemple :
```py
ma_variable = "chaine de caractères"
ma_variable_2 = 3 #int > entier
ma_variable_3 = 2.069 # float > virgule flotante
```