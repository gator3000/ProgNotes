[Retour](Summary)
___

Il faut savoir qu'en programmation, les développeurs sont des flemmards.
Pour répéter une action on utilise les boucles, il y en a de 2 sortes:
- `while`
- `for`
`while` utilise les conditions et `for` permet de parcourir des itérables en résumé.

Beaucoup de manuels et livres te feront commencer par les boucles for mais je vais être original la dessus et on va commencer avec les boucles `while`, qui me semblent plus bas niveau.


### While

Les boucles `while` peuvent se traduire par `répéter tant que c'est vrai:` en français compréhensible par la majorité.
On les utilisent comme ceci :
```py
a = "default"
while a != "ok":
	a = input("Faire ceci ? [ok]")
```
Ici comme `a != "ok"` au début du programme on rentre dans la boucle. Si j'avais écrit `a = "ok"` à la place de la valeur par défaut, le programme n'aurais rien sorti.
Ensuite on demande à l'utilisateur d'écrire `ok` pour valider une action. Le programme ne finira jamais si l'utilisateur n'écrit pas `ok` dans l'input puisque à chaque tour de boucle on redéfinis la valeur de `a` à l'entrée utilisateur.

Voici un exemple plus poussé :
```py
cmd = "default"
while cmd != "exit":
	cmd = input("/etc/udev $ ")
	if cmd == "exit":
		print("La prise de commande est terminée !")
```


### For
Le deuxième type de boucle, `for`, plus poussé, sert soit à prendre chaque itérations d'un itérable par exemple une liste :
```py
list = ["Hello", "World", "!"]
for e in list:
	print(e)
# Output : Hello
# World
# !
```
