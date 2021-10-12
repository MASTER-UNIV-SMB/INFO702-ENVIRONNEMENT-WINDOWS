# Environnement de Développement - INFO702 (Windows)
Tutoriel d'installation de l'environnement de développement WINDOWS INFO702

### 1 - Télécharger QT Open Source
https://download.qt.io/official_releases/qt/5.12/5.12.11/qt-opensource-windows-x86-5.12.11.exe

### 2 - Installer QT Open Source

Executez QT Open Source et installez le sur votre disque 

### 3 . Installer via Powershell (Admin)
Lancer un PowerShell en administrateur et executez cette commande :
```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```

Ensuite fermez et réexecutez un PowerShell en administrateur.

### 4 . Executez via Powershell (Admin)
Executez cette commande :
```choco install make```

Ensuite : 
```choco install mingw```

### 5 . Ajoutez dans les variables d'environnement 
Exécutez le raccourci : **WINDOWS + R** et tapez dans la fenêtre qui vient de s'ouvrir ```SystemPropertiesAdvanced.exe```

Une fenêtre s'ouvre cliquez sur **Variables d'environnement**, une autre fenêtre s'ouvre avec la liste des variables d'environnement.

![Path](https://i.imgur.com/nPng97i.png)

Cliquez sur **Path** et **Modifier**, une autre fenêtre s'ouvre

![Path](https://i.imgur.com/f7qhV5i.png)

Vous cliquez sur **Nouveau** et vous allez renseigner le **Dossier où vous avez installer QT** donc par exemple pour moi ce sera : ```D:\Developpement\QT\5.12.11\mingw73_64\bin```

**!! ATTENTION: NE PAS METTRE D'ACCENTS OU DE SYMBOLES DANS LE PATH**

Cliquez ensuite sur OK, validez et fermez l'éditeur d'environnement.

### 6 . Dans le projet

Ensuite rendez-vous sur votre Projet de TP, vous pouvez compiler simplement votre projet en faisant 
```qmake``` et ```make```
