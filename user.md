---
title: "user"
order: 7
in_menu: true
---
# La commande ``adduser`` 



- Ajoute un groupe au nom de l'utilisateur. Détermine un GID.

- Ajoute l'utilisateur dans le groupe de l'utilisateur.

- Détermine un UID pour l'utilisateur.

- UID et GID  utilisés par le système (et pas le login)

- Créer le répertoire personnel de l'utilisateur dans `/home`.

- `adduser` copie le fichier `/etc/skel` dans le répertoire de l'utilisateur qui contient :

	- `.bash_logout`
	- `.bashrc`
	- `.profile`
	
- Demande un mot de passe.

- Ajoute l'utilisateur au groupe "users"



```bash
sudo adduser titi
```



## La commande useradd



```bash
# useradd <options> login
```



- Sans options sur la ligne de commande c'est celles du fichier `/etc/default/useradd` qui seront appliquées.


| Option | Rôle |
| :--- | ---- |
| -m | Créer le répertoire personnel |
| -u | UID numérique de l'utilisateur (`login.defs`) |
| -g | Groupe principal - GID ou nom |
| -G | Groupes supplémentaires |
| -d | Chemin du répertoire personnel |
| -c | Commentaire |
| -k | Chemin du squelette si autre que `/etc/skel` |
| -s | Shell par défaut |


- Il faut créer un mot de passe pour le compte avec :


```bash
passwd toto
``` 