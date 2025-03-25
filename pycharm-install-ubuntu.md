**Installation de PyCharm sur Ubuntu**

PyCharm est un IDE puissant pour le développement Python. Voici comment l’installer sur Ubuntu.

---

## **1. Télécharger PyCharm**

Rendez-vous sur le site officiel de JetBrains et téléchargez la version **PyCharm Community Edition** (gratuite) :
[👉 Télécharger PyCharm](https://www.jetbrains.com/pycharm/download/?section=linux)

Assurez-vous de télécharger la version **Linux**.

---

## **2. Extraction du fichier téléchargé**

Une fois le fichier téléchargé, ouvrez un terminal et accédez au dossier où il se trouve (par défaut, dans `~/Téléchargements` ou `~/Downloads`) :
```bash
cd ~/Téléchargements
```
Puis, décompressez l’archive :
```bash
tar -xvf pycharm-community-*.tar.gz
```
Cela va créer un dossier nommé **pycharm-community-xxxx.x** (avec le numéro de version).

---

## **3. Déplacer PyCharm vers `/opt/`**

Il est conseillé de déplacer le dossier extrait vers `/opt/` pour une installation propre :
```bash
sudo mv pycharm-community-xxxx.x /opt/
```
(Remplacez `pycharm-community-xxxx.x` par le nom exact du dossier extrait.)

---

## **4. Lancer PyCharm**

Accédez au dossier d’installation :
```bash
cd /opt/pycharm-community-xxxx.x/bin/
```
Puis exécutez PyCharm :
```bash
./pycharm.sh
```
L’assistant d’installation s’ouvrira. Suivez les instructions à l’écran pour finaliser la configuration.

---

## **5. Créer un raccourci pour PyCharm** (optionnel mais recommandé)

Pour éviter d’ouvrir le terminal à chaque lancement, vous pouvez créer un raccourci :

1. Ouvrez un terminal et exécutez :
   ```bash
   nano ~/.local/share/applications/pycharm.desktop
   ```
2. Copiez-collez ce contenu (en adaptant le chemin si nécessaire) :
   ```ini
   [Desktop Entry]
   Version=1.0
   Type=Application
   Name=PyCharm Community Edition
   Exec=/opt/pycharm-community-xxxx.x/bin/pycharm.sh
   Icon=/opt/pycharm-community-xxxx.x/bin/pycharm.svg
   Terminal=false
   Categories=Development;IDE;
   ```
3. Sauvegardez avec `CTRL+X`, puis `Y` et `Entrée`.
4. Rendez le fichier exécutable :
   ```bash
   chmod +x ~/.local/share/applications/pycharm.desktop
   ```

PyCharm apparaîtra maintenant dans le menu des applications ! 🚀