# Mettre en place un environnement de test (Lab)  

## DAT (document d'architecture technique)  

### Un schéma réseau, incluant les VM, l'Hyperviseur et les switchs virtuels  



---

### Un tableau avec la liste des comptes utilisés pour l'administration et l'emplacement du gestionnaire de secrets contenant les mots de passe.

|Hostname|Compte|Compte|
|----|---|---|
|DC1 (Winserv2025)|Administrateur||
|WIN11 (Windows11)|nicolocal||
|deian13 (Debian13)|root|nico|

---

### Un Diagramme de Gantt ou un Kanban de votre réalisation pour la partie gestion de projet.  

---

### La présentation des éléments suivants, avec captures d'écran  

#### Vérification des intégrités des images téléchargées avant l'installation  

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





#### Mises à jour réussies  
:arrow_forward: **Debian13**  
<img width="750" height="429" alt="Capture d'écran 2025-10-15 124340" src="https://github.com/user-attachments/assets/e1df0224-347d-4e90-856b-2cbc09396907" />  

---

:arrow_forward: **Windows Server 2025**  
<img width="507" height="309" alt="image" src="https://github.com/user-attachments/assets/e81573bc-a208-4d26-bdc9-dbb9c570de95" />  


---

:arrow_forward: **Windows 11 Intégrité**  
<img width="519" height="282" alt="image" src="https://github.com/user-attachments/assets/3f2aec9a-110a-46a1-8ce3-56ef203926ba" />


---

#### le statut des services DNS et Web



#### connexions SSH et WinRM réussies (Connexion + commande whoami)  
#### Permissions et statut du partage SMB ou Samba  
#### le nombre d'utilisateurs contenus dans l'AD  
