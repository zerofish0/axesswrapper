# AxessWrapper

Un empaqueteur pour accéder à la vie scolaire depuis python. Utilisation de headers aléatoires. Pas de stockage des mots de passe (même en temps que variables, ils sont utilisés directement à l'initialisation)

## Dépendances

### beautifulsoup
Pour le parsing HTML

`pip install beautifulsoup4`

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

### Informations

`session.getInformations()`

Renvoie les informations de l'utilisateur sous la forme : 

```
{"name":"prenom_utilisateur",
"surname":"nom_utilisateur",
"status":"statut_utilisateur",
"etab":"etablissement_utilisateur"}
```

### Notes

`session.getGrades()`

Renvoie les notes de l'utilisateur sous la forme : 

```
{"matiere1" : {"average" : "average_note_of_the_user","details" : ["note 1","note 2"...]},
"matiere2" : {"average" : "average_note_of_the_user","details" : ["note 1","note 2"...]}
}

```

### Devoirs

`session.getHomeworks(date : str ("yyyy-mm-dd"))`

Renvoie les devoirs à faire pour la date donnée sous la forme : 

```
{matiere1 : [devoir1,devoir2...],
...
}
```

### Emploi du temps

`session.getPlanner(date : str ("dd/mm/yyyy"))`

Renvoie l'emploi du temps de la semaine correspondant à la date fournie, sous la forme : 

`{"lundi" : ["matiere1","matiere2"...], "mardi" : ["matiere1","matiere2"...]...}`

## ⚠️ Avertissement

Ce projet a été créé par **Zerofish0** à des **fins strictement éducatives et personnelles**.

Il s'agit d’un outil expérimental permettant d’interagir avec le site d’un établissement scolaire via des techniques de web scraping.

**Aucune affiliation ou approbation officielle n’existe** entre ce projet et l’établissement concerné.

L’auteur :
- n’encourage en aucun cas un usage contraire aux conditions générales d’utilisation du site concerné ;
- ne collecte, ne stocke ni ne traite aucune donnée personnelle ;
- décline toute responsabilité en cas d’usage abusif, non autorisé ou illicite de ce logiciel.

**L’utilisateur est seul responsable de ses actions**. Il lui revient de vérifier que l’utilisation de ce logiciel est conforme aux règles du site cible et à la législation en vigueur (notamment le RGPD et le Code pénal français).

En téléchargeant, exécutant ou modifiant ce logiciel, **vous acceptez expressément ces conditions**.


