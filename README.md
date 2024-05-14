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
