# Django

Django, prononcé "jango", est un framework web open source en Python. Il a été initialement publié en 2005 et tire son nom du célèbre guitariste de jazz Django Reinhardt. Django est devenu l'un des frameworks les plus populaires en raison de sa flexibilité, de sa sécurité et de sa simplicité d'utilisation.

## Introduction

Ce projet vise à fournir une brève présentation de Django, en mettant en évidence ses principales caractéristiques, son utilité et sa popularité dans le domaine du développement web.

### Caractéristiques principales

- **Flexibilité :** Django permet de développer aussi bien le front-end que le back-end des applications web.
- **Sécurité :** Django intègre des fonctionnalités de sécurité avancées pour protéger les applications contre les attaques.
- **Simplicité :** Les bibliothèques Python intégrées simplifient le processus de développement et accélèrent la mise en place des fonctionnalités.

### Utilisation

Ce framework est largement utilisé dans divers secteurs d'activité pour le développement d'applications web. Il convient aussi bien aux petites startups qu'aux grandes entreprises.

## Guide d'installation de Django

Ce guide explique comment installer Django sur votre système en utilisant un environnement virtuel pour isoler votre projet. Django est un framework web puissant pour le développement rapide d'applications web en Python.

### Prérequis

Avant d'installer Django, assurez-vous que vous avez Python installé sur votre système. Vous pouvez vérifier la version de Python avec la commande suivante :

```bash
# Windows
python --version 

# macOS ou Linux
python3 --version 
```

### 1. Créer le dossier du projet

Avant de télécharger Django, créez un environnement virtuel pour isoler votre projet des autres applications Python.

```bash

# Créez un nouveau répertoire pour votre projet
mkdir hello_django
cd hello_django
```

### 2. Créer et activer l'environnement virtuel

Créez un environnement virtuel et activez-le pour votre projet.

```bash

python -m venv venv    # Windows
python3 -m venv venv   # macOS ou Linux
```
> Créez un environnement virtuel

```bash
# Windows
.\\venv\\Scripts\\Activate
# macOS ou Linux
source ./venv/bin/activate
```
> Activez l'environnement virtuel

### 3. Installation de Django

Utilisez un fichier requirements.txt pour lister les packages nécessaires à votre projet, y compris Django.

```bash

# Créez un fichier requirements.txt
touch requirements.txt

# Ajoutez Django au fichier requirements.txt
echo "Django" >> requirements.txt

# Installez les packages listés dans requirements.txt
pip install -r requirements.txt
```

Une fois l'installation terminée, vous êtes prêt à commencer à développer votre application Django !

## Concepts de base de Django

Ce README explore les concepts fondamentaux de Django, notamment les différences entre un projet et une application, les vues et le mappage d'URL.

### Différences entre un projet et une application

| Project | Application |
|---------|-------------|
| Il ne peut y avoir qu’un seul projet. | Il peut y avoir de nombreuses applications dans le même projet. |
| Contient les paramètres ou applications nécessaires pour un site web spécifique. | Est l’un des composants du site web global. |
| Les projets ne sont pas utilisés dans d’autres projets. | Les applications peuvent être utilisées dans de multiples projets. |

### Vues

Les vues sont des composants des applications Django. Elles exécutent une fonction spécifique au sein de chaque application. Les vues contiennent le code nécessaire pour renvoyer une réponse spécifique à une demande, telle qu'un modèle ou une image. Elles peuvent également rediriger vers une autre page si nécessaire.

### Mappage d’URL

Dans Django, le mappage d’URL est appelé URLconf et sert de table des matières pour votre application. Lorsqu'il reçoit une demande d'URL, ce module recherche le lien approprié dans le projet, puis redirige la demande vers le fichier de vues contenu dans l'application. La vue traite ensuite la demande et effectue les opérations nécessaires.

À mesure que la structure de fichiers devient plus complexe, vous ajouterez des vues et des URL supplémentaires à votre application. La fonction URLconf joue un rôle clé en permettant de gérer et d'organiser facilement les URL au sein de l'application, tout en offrant une flexibilité pour changer les chemins racines sans risquer de casser l'application.

## Création du premier projet Django

Ce guide explique comment créer votre premier projet Django, ajouter l'application "Hello World", explorer la structure du projet, exécuter le serveur de développement et inscrire l'application auprès du projet.

### Créer un projet avec django-admin

Utilisez la commande suivante pour créer un projet Django :

```bash
django-admin startproject helloproject .
```

Assurez-vous d'inclure le point à la fin de la commande pour utiliser le dossier actif.
Explorer la structure du projet

Après avoir créé le projet, vous trouverez une structure de dossier comme suit :

```markdown

helloproject/
    manage.py
    helloproject/
        __init__.py
        asgi.py
        settings.py
        urls.py
        wsgi.py
```

Explorez les différents fichiers pour comprendre leur fonction dans le projet.
Exécuter le projet

Lancez le serveur de développement en utilisant la commande :

```bash

python manage.py runserver
```

Copiez l'URL de votre serveur de développement dans votre navigateur pour vérifier que le projet fonctionne correctement.
Créer l'application Hello World

Utilisez la commande suivante pour créer l'application "Hello World" :

```bash

python manage.py startapp hello_world
```

La structure de dossier de l'application sera générée automatiquement.
Inscrire l'application auprès du projet

Modifiez le fichier settings.py dans le répertoire helloproject pour ajouter l'application à la liste INSTALLED_APPS.

```python

INSTALLED_APPS = [
    ...
    'hello_world.apps.HelloWorldConfig',
]
```
Félicitations !

Vous avez maintenant créé votre premier projet Django et ajouté votre première application "Hello World". Vous pouvez maintenant créer des vues et des URL pour ajouter des fonctionnalités supplémentaires à votre application.

## Comprendre les chemins et les vues dans Django

Ce README explique les concepts de base des chemins (ou routes) et des vues dans Django, et comment ils sont utilisés pour gérer les demandes utilisateur dans une application web.

### Chemins

Les chemins sont utilisés pour déterminer quelles informations doivent être affichées à l'utilisateur et comment l'utilisateur peut y accéder. Dans une application web, les demandes utilisateur sont effectuées par des actions telles que la navigation vers différentes URL, la saisie d'informations, la sélection d'un lien ou l'appui sur un bouton.

Dans Django, les chemins sont configurés à l'aide de `urlpatterns`. Ces modèles indiquent à Django ce qu'il doit rechercher dans l'URL demandée par l'utilisateur et déterminent la fonction à exécuter en réponse à la demande. Ces modèles sont regroupés dans un module Django appelé URLconf.

### Vues

Les vues déterminent les informations à retourner à l'utilisateur en réponse à une demande. Ce sont des fonctions ou des classes qui exécutent du code en réponse à la demande utilisateur. Elles retournent des réponses HTML ou d'autres types de réponses, comme une erreur 404.

Par exemple, une URL comme https://adventure-works.com/about peut exécuter une fonction appelée `about`, tandis que https://adventure-works.com/login peut exécuter une fonction appelée `authenticate`.

---

## Créer des chemins et des vues dans Django

Ouvrez `views.py` dans le dossier hello_world.
Remplacez le contenu actuel par le code suivant :

```python

from django.shortcuts import render
from django.http import HttpResponse

def index(request):
    return HttpResponse("Hello, world!")
```

La fonction index retourne "Hello, world!" en utilisant l'objet HttpResponse.
Créer la route

Une fois la vue créée, nous devons la mapper à l'URL appropriée.

Dans Visual Studio Code, créez un fichier nommé urls.py dans le dossier hello_world.
Ajoutez le code suivant dans `urls.py` :

```python

from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
]
```

Ce code définit un chemin vide qui appelle la fonction index de views.py.
Inscrire URLconf dans le projet

Pour que notre application puisse gérer les demandes utilisateur, nous devons inscrire URLconf dans le fichier urls.py principal.

Ouvrez `urls.py` dans le dossier helloproject.
Remplacez la ligne `from django.urls import path` par :

```python

from django.urls import include, path
```

Ajoutez la ligne suivante sous la liste urlpatterns :

```python

path('', include('hello_world.urls')),
```

Cela inclut notre URLconf dans le projet.
Exécuter votre première application

Dans la fenêtre de terminal de Visual Studio Code, exécutez la commande suivante pour démarrer le serveur :

```bash
python manage.py runserver
```

Ouvrez l'URL http://localhost:8000/ dans votre navigateur.
Vous devriez voir "Hello, world!" s'afficher dans la fenêtre de votre navigateur.

Félicitations ! Vous avez créé votre première application Django avec des chemins et des vues.

## Préparation à la partie 2 du workshop

### 1. Poser des questions

N'hésitez pas à poser des questions si la moindre explication de ce worshop n'a pas était clair. Je suis là pour vous aider à progresser dans votre apprentissage de Django.

### 2. Développer vos compétences en front-end

Poussez vos connaissances en front-end en pratiquant avec des technologies telles que HTML, CSS et JavaScript. Essayez de créer des scripts JavaScript de base pour rendre votre application web plus interactive.

### 3. Assurez-vous d'avoir un fichier requirements.txt à jour

Assurez-vous que votre fichier requirements.txt contienne toutes les dépendances nécessaires à votre projet Django. Mettez à jour ce fichier si vous avez ajouté de nouvelles dépendances ou effectué des changements dans votre environnement de développement.

### 4. Mettre en pratique vos compétences en Django

Profitez de cette période de préparation pour mettre en pratique vos compétences en Django. Révisez les concepts abordés dans la première partie du workshop et essayez de créer de nouvelles fonctionnalités pour améliorer votre projet.

### 5. Explorez de nouvelles ressources

Explorez de nouvelles ressources en ligne telles que des tutoriels, des documentations officielles et des forums de discussion pour approfondir vos connaissances en Django. Plus vous en saurez, plus vous serez préparé pour la suite du workshop.
