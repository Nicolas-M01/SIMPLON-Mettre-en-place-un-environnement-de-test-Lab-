# Mettre en place un environnement de test (Lab)  

## DAT (document d'architecture technique)  

## Schéma réseau, incluant les VM, l'Hyperviseur et les switchs virtuels  



---

## Tableau avec la liste des comptes utilisés pour l'administration et l'emplacement du gestionnaire de secrets contenant les mots de passe.

|Hostname|Compte|Compte|
|----|---|---|
|DC1 (Winserv2025)|Administrateur (admin domaine)||
|WIN11 (Windows11)|nicolocal ( admin local)|nmaertens (user domaine **nico.local**)|
|Debian13 (Debian13)|root|nico (sudoers group)|

---

## Diagramme de Gantt ou un Kanban de votre réalisation pour la partie gestion de projet.  

---


### Vérification des intégrités des images téléchargées avant l'installation  

:arrow_forward: **Windows 11 Intégrité**  
Ici les Hashes sont comparée en sha256 :  
<img width="1088" height="248" alt="Capture d'écran 2025-10-15 115632" src="https://github.com/user-attachments/assets/edd61804-39b6-4eeb-aae1-43b30b368741" />  

---

:arrow_forward: **Debian 13 Intégrité**  
Ici les hashes sont comparés en sha512 :  
<img width="1178" height="187" alt="Capture d'écran 2025-10-15 122532" src="https://github.com/user-attachments/assets/760f0c67-f5d1-4a07-be02-e58685a6c01a" />

---

:arrow_forward: **Windows Server 2025**  

Je n'ai pas trouvé le hash officiel de mon ISO, mais étant donné que j'ai téléchargé l'ISO sur le site officiel Microsoft, je dois avoir un ISO intègre.  
Néanmoins voici le hash de ma version téléchargée.  
<img width="1469" height="100" alt="Capture d'écran 2025-10-15 123837" src="https://github.com/user-attachments/assets/56d2e59c-9ed4-44b6-acba-fb6d8b1db11f" />





### Mises à jour réussies  
:arrow_forward: **Debian13**  
<img width="750" height="429" alt="Capture d'écran 2025-10-15 124340" src="https://github.com/user-attachments/assets/e1df0224-347d-4e90-856b-2cbc09396907" />  

---

:arrow_forward: **Windows Server 2025**  
<img width="507" height="309" alt="image" src="https://github.com/user-attachments/assets/e81573bc-a208-4d26-bdc9-dbb9c570de95" />  


---

:arrow_forward: **Windows 11 Intégrité**  
<img width="519" height="282" alt="image" src="https://github.com/user-attachments/assets/3f2aec9a-110a-46a1-8ce3-56ef203926ba" />


---

### le statut des services DNS et Web

:arrow_forward: **Status DNS sur Windows Serveur 2025**
<img width="866" height="342" alt="image" src="https://github.com/user-attachments/assets/f432ecd9-7433-4859-8f88-ca25df5369a4" />
<img width="465" height="112" alt="Capture d'écran 2025-10-15 165408" src="https://github.com/user-attachments/assets/6c7d1f51-d46f-4c3e-b8ee-cf59a9ea4d5b" />

---

:arrow_forward: **Status serveur Web Apache2 sur Debian 13**  
<img width="806" height="355" alt="Capture d'écran 2025-10-15 165743" src="https://github.com/user-attachments/assets/523993b5-c15a-4f1e-844b-6861fdbb07e7" />  

---

### connexions SSH et WinRM réussies (Connexion + commande whoami)  

* **Serveur SSH sur Debian 13**  
<img width="619" height="149" alt="image" src="https://github.com/user-attachments/assets/77f8dcd6-d5a4-4996-8d22-94aed061c592" />  
<img width="761" height="250" alt="image" src="https://github.com/user-attachments/assets/d4a82402-cd9a-4175-90f5-a31587331fd4" />  

:arrow_forward: **Nico est dans le groupe Sudo**  
<img width="322" height="40" alt="Capture d'écran 2025-10-15 172633" src="https://github.com/user-attachments/assets/31fae145-c553-4651-9303-e82228ccfc4d" />  

:arrow_forward: **Je permets uniquement la connexion pour les membres du groupe "sudoers" et j'apporte de la sécurité dans la connexion SSH**  
<img width="172" height="36" alt="Capture d'écran 2025-10-15 175048" src="https://github.com/user-attachments/assets/51e6e346-7d50-400b-ae96-e92c309417af" />  
<img width="674" height="517" alt="image" src="https://github.com/user-attachments/assets/93cbec11-9367-4b2f-b0f4-75b9db7560b3" />  


:arrow_forward: **Je paramètre mon compte "Administrateur" de Windows Server 2025 pour me connecter à "nico" en ssh avec chiffrement asymétrique sans mot de passe**  
:arrow_forward: **Génération d'une paire de clés SSH en ed25519**  
<img width="719" height="426" alt="Capture d'écran 2025-10-15 185708" src="https://github.com/user-attachments/assets/40650d1c-e6ae-4809-9528-d9367cecfa3f" />  
:arrow_forward: **Vérification de la clé publique**  
<img width="990" height="41" alt="Capture d'écran 2025-10-15 185739" src="https://github.com/user-attachments/assets/0eac423f-0a02-4b53-b912-f60ccb757d84" />  
:arrow_forward: **Envoi de la clé publique sur le serveur SSH Debian 13 avec modif des droits au dossier ".ssh" et fichier "authorized_keys"**  
<img width="1015" height="240" alt="Capture d'écran 2025-10-15 185758" src="https://github.com/user-attachments/assets/f538a034-405e-44fc-bd80-675ba386d22b" />  
:arrow_forward: **Connexion réussie**  
<img width="868" height="316" alt="image" src="https://github.com/user-attachments/assets/12ca7d72-c6eb-4acf-abf4-ec2df0863f08" />  



---

* **Serveur WinRM sur Windows Server 2025**  
:arrow_forward: **Activation de WinRM sur le serveur AD (DC1) et vérification du status**  
<img width="615" height="145" alt="image" src="https://github.com/user-attachments/assets/176e288d-b6f3-4e9c-8e92-a8d0a4c6a79a" />  

:arrow_forward: **Paramétrage d'autorisation des groupes d'admin du domaine AD**  
<img width="993" height="591" alt="Capture d'écran 2025-10-15 192743" src="https://github.com/user-attachments/assets/c82017af-79e4-4986-8323-cadf65dafff6" />  

:arrow_forward: **Connexion réussie depuis un compte admin membre du groupe admin**  
<img width="606" height="191" alt="image" src="https://github.com/user-attachments/assets/a11bd987-6d68-485f-85b7-ec982c6232d4" />
<img width="847" height="204" alt="Capture d'écran 2025-10-15 193401" src="https://github.com/user-attachments/assets/5a34a964-d1b8-4a6c-bb63-cd5788b7593c" />  

:arrow_forward: **Connexion échouée depuis un compte user classique**  
<img width="992" height="170" alt="Capture d'écran 2025-10-15 194230" src="https://github.com/user-attachments/assets/74f36a18-da08-4fdb-a228-477bf34ff65a" />  

---

### Permissions et statut du partage SMB ou Samba  
:arrow_forward: **Permissions des dossiers partagés SMB**  
<img width="673" height="249" alt="image" src="https://github.com/user-attachments/assets/3fada9b0-b732-4397-9772-48b2b5580393" />

---

### le nombre d'utilisateurs contenus dans l'AD  
:arrow_forward: **Utilisateurs, Computers, Groups, OUs**  
<img width="677" height="157" alt="Capture d'écran 2025-10-16 103038" src="https://github.com/user-attachments/assets/fdf9d4cc-8fdd-40a5-aad5-b9c9ab9a7e78" />  



