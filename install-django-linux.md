**Installation de Django sur Ubuntu et création d'un projet**

### 1. Mise à jour du système
Avant d'installer quoi que ce soit, il est recommandé de mettre à jour les paquets existants :
```bash
sudo apt update && sudo apt upgrade -y
```

### 2. Installation de Python
Ubuntu inclut généralement Python, mais pour s'assurer qu'il est installé :
```bash
sudo apt install python3 -y
```

### 3. Configuration de Python
Pour s'assurer que la commande `python` pointe vers `python3`, installez le package suivant :
```bash
sudo apt install python-is-python3 -y
```

### 4. Installation de Virtualenv
Il est recommandé d'utiliser un environnement virtuel pour éviter les conflits entre les dépendances de différents projets :
```bash
sudo apt install python3-virtualenv -y
```

---

## **Création du projet Django**

### 1. Création de l'arborescence du projet
Il est conseillé d'organiser ses projets. Par exemple, créez un dossier principal pour Django et un sous-dossier pour l'application :
```bash
mkdir -p ~/django_projects/app1
cd ~/django_projects/app1
```

### 2. Ouverture du projet dans VSCode
Si vous utilisez VSCode, ouvrez votre projet avec la commande suivante :
```bash
code .
```

### 3. Création et activation d'un environnement virtuel
Dans le terminal de votre éditeur (ou depuis votre dossier de projet) :
```bash
virtualenv env
source env/bin/activate
```
Une fois activé, vous verrez le préfixe `(env)` avant votre invite de commande.

### 4. Installation de Django
Dans l’environnement virtuel activé, installez Django :
```bash
pip install django
```

### 5. Création d'un projet Django
Générez la structure de votre projet avec la commande suivante :
```bash
django-admin startproject myapp .
```

### 6. Démarrage du serveur de développement
Pour tester si tout fonctionne correctement, exécutez :
```bash
python manage.py runserver
```
Vous devriez voir une sortie indiquant que le serveur est actif. Ouvrez un navigateur et allez à l'adresse `http://127.0.0.1:8000/` pour voir la page d'accueil par défaut de Django.

---

## **Étapes suivantes**

- **Créer une application Django** :
  ```bash
  python manage.py startapp nom_de_l_app
  ```
- **Appliquer les migrations** :
  ```bash
  python manage.py migrate
  ```
- **Créer un superutilisateur** pour accéder à l'interface d'administration :
  ```bash
  python manage.py createsuperuser
  ```
- **Exécuter le serveur et accéder à l’interface d’administration** :
  ```bash
  python manage.py runserver
  ```
  Accédez à `http://127.0.0.1:8000/admin/` et connectez-vous avec le compte superutilisateur créé.

Avec ces étapes, vous avez un environnement Django fonctionnel sur Ubuntu ! 🚀

