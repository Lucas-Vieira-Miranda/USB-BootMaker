# USB-BootMaker

Script PowerShell simple et efficace pour créer une clé USB bootable à partir d’une image ISO Windows ou Linux.  
Il automatise le formatage, le montage et la copie du contenu ISO, avec la possibilité d’ajouter des fichiers personnalisés.  
Un outil idéal pour les techniciens, administrateurs et passionnés IT.

---

## 🚀 Fonctionnalités

- Détection interactive du périphérique USB  
- Formatage sécurisé en FAT32 ou NTFS selon la taille du fichier ISO  
- Montage automatique de l’image ISO avec PowerShell natif  
- Copie complète des fichiers ISO vers la clé USB  
- Ajout facultatif de fichiers personnalisés (scripts, drivers, outils)  
- Éjection propre du volume à la fin de l’opération

---

## 📦 Stack technique

- PowerShell 5.1 ou supérieur (Windows)  
- Utilisation des modules `Storage` et `DiskImage`  
- Scripting CLI sans dépendances externes  
- Support des images ISO Windows et Linux

---

## 📋 Prérequis

- Windows 10 ou supérieur avec PowerShell 5.1+  
- Droits administrateur (nécessaires pour manipuler les disques)  
- Clé USB avec espace suffisant  
- Fichier ISO valide (Windows ou Linux)

---

## ⚙️ Installation et lancement

1. **Cloner le dépôt**  
   
       git clone https://github.com/tonpseudo/usb-bootmaker.git
       cd usb-bootmaker

2. **Lancer le script PowerShell en mode administrateur**  
   
       .\usb-bootmaker.ps1 -ISOPath "C:\Images\Windows10.iso" -DriveLetter "E" -CustomFiles "C:\MesScripts"

3. **Paramètres**  
- `-ISOPath` : chemin complet vers l’image ISO à déployer  
- `-DriveLetter` : lettre assignée à la clé USB (exemple : "E")  
- `-CustomFiles` *(optionnel)* : dossier contenant des fichiers à copier en plus sur la clé USB

---

## ⚠️ Attention

- Le formatage effacera **toutes les données** présentes sur la clé USB sélectionnée.  
- Veille à bien choisir la lettre de lecteur correcte pour éviter toute perte de données.  
- Exécute toujours le script en mode administrateur.

---

## 🧪 Exemple d’utilisation

       .\usb-bootmaker.ps1 -ISOPath "D:\ISO\Ubuntu.iso" -DriveLetter "F"

       .\usb-bootmaker.ps1 -ISOPath "C:\ISOs\Win10.iso" -DriveLetter "G" -CustomFiles "C:\Outils\Drivers"

---

## 📜 Licence

Ce projet est sous licence MIT — fais-en bon usage et contribue si tu veux !
