# AxessWrapper

Un empaqueteur pour accéder à la vie scolaire depuis python. Utilisation de headers aléatoires. Pas de stockage des mots de passe (même en temps que variables, ils sont utilisés directement à l'initialisation)

## Dépendances

### beautifulsoup
Pour le parsing HTML
`pip install beautifulsoup4'

### requests
Pour les requêtes
`pip install requests`

## Usage

Créez un nouveau script python, placez axess.py dans le même dossier. Puis initialisez l'instance avec : 
```
import axess
session = axess.Axess(username,password,verbose = False)
```

puis, pour utilisez les diverses méthodes : 
`session.method(args)`

## Points d'accès 

Les instances de Axess ont plusieurs méthodes : 

`session.getInformations()`
Renvoie les informations de l'utilisateur sous la forme : {a compléter}

`session.getGrades()`
Renvoie les notes de l'utilisateur sous la forme : {}

`session.getHomeworks(date : str ("yyy-mm-dd"))`
Renvoie les devoirs à faire pour la date donnée sous la forme : {}

`session.getPlanner(date : str ("dd/mm/yyyy"))`
Renvoie l'emploi du temps de la semaine correspondant à la date fournie, sous la forme : 
`{"lundi" : ["matiere1","matiere2"...], "mardi" : ["matiere1","matiere2"...]...}`
