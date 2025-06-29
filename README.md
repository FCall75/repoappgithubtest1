# ini_WaveCare_Automatisation

### IDE

Je préconise d'utiliser Visual Studio Code avec l'extension [RobotFramework](https://marketplace.visualstudio.com/items?itemName=robocorp.robotframework-lsp)

### Environnement Virtuel

Pour lancer nos tests, nous utiliserons un environnement virtuel. Pour ce faire, nous devons tout d'abord le créer. Nous utiliserons la version stable [3.11.8 de Python](https://www.python.org/downloads/release/python-3118/) pour ce projet. Une fois Python installé, il faut récupérer le chemin d'accès de l'exécutable de Python sous le format suivant :

```js
C:\Users\{IDENTIFIANT}\AppData\Local\Programs\Python\Python311\python
```

Une fois ce chemin récupéré, nous pouvons l'utiliser dans le terminal de l'IDE afin de créer l'environnement virtuel :

```shell
C:\Users\{IDENTIFIANT}\AppData\Local\Programs\Python\Python311\python -m venv venv
```

***Attention*** : Il faut être dans le répertoire du projet !

Pour activer l'environnement virtuel, il s'agit de la commande suivante :

```shell
venv\Scripts\activate
```

**À noter que le dossier .vscode permet de lancer l'environnement virtuel à chaque test ou suite de tests.**

### Installation des librairies

Le fichier requirements-freeze.txt est une liste des dépendances Python avec leurs versions spécifiques. Chaque ligne de ce script représente un package Python avec sa version précise. Ces dépendances sont à installer à l'aide d'un gestionnaire de paquets tel que pip via la commande suivante :

```shell
py -m pip install -U pip setuptools wheel
```

```shell
py -m pip install -r requirements-freeze.txt
```

### UTILISATION

Pour lancer les tests en ligne de commande    

Prérequis l'environnement virtuel est activé

```
py -m robot --outputdir output --variable BROWSER:chrome --include tnr tests\testsuites

ou

robot -d output -v BROWSER:chrome -i tnr tests\testsuites

```
