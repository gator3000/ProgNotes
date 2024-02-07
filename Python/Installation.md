[Retour](Summary)
___

> [!NOTE]
> J'utilise moi même linux (Debian 12 pour etre précis). Si il semble que mes exemples & corrections ne fonctionnent pas pour votre système d'exploitation, veuillez me le signialer. Normalement, ça n'arrivera pas car comme dit dans l'[Introduction](Introduction), un des point forts de python est de fonctionner de la même façon quel que soit l'OS.
## 0.2.1 Windows
Pour Windows, il y a trois manières :

1. Désinstalle Windows et viens sous linux :).
   Nan, plus serieusement :
2. Sinon installe un IDE, par exemple **PyCharm** par ce [site](https://pycharm-community-edition.fr.softonic.com/).
3. Il faut aller sur le [site officiel de python](https://www.python.org/downloads/windows/) et cliquer sur le lien pour télécharger la première version qui apparaît dans la section *Stable releases*. Maintenant, aller tout en bas du site et cliquez sur le lien commençant pas **Windows installer** qui correspond à ton architecture (*64 -bit* ou *32 -bit* (si tu ne sais pas, télécharge le *64 -bit*)).Ensuite, exécute le fichier que tu viens de télécharger et clique sur ***Install Now*** si tu ne sais que faire. Sinon fait ce que bon te semble :).

## 0.2.2 Linux

Sur linux, rien de plus simple, python est déjà installé sur votre ordinateur !
Si par malheur, ça ne serait pas fait par défaut, tu dois écrire dans ton terminal :
```sh
sudo apt update && sudo apt upgrade
```

De toute façon pour vérifier la version de python, tu écriras :
```sh
python3 -V
```
et ton shell te répondra la version de python installé sous la forme :
`Python 3.11.2`

Si la version est inferieure à la 3.11, je te reconduis ici [[Installation#0.2.2 Linux]]

## 0.2.3 Mac OS X

Comme sur linux, python est déjà installé par défaut !