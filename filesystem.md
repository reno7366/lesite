---
title: "FileSystem"
order: 8
in_menu: true
---
Le Système de fichiers ou File System définit l'organisation des données sur les différents supports de stockage.

Sur Linux on dit que tout est fichier, les données (images, programme) , les périphériques (clavier, souris ou carte wifi) ou les moyens de communication (sockets) sont dans des fichiers du FS.

L'arborescence de répertoire commence avec le root directory la racine ( / ).

![Arborescence de répertoire]({% link images/arborescence_linux.png %})

## 3 types de fichiers

* ordinaires
	* texte
	* image
	* audio
	* programme binaire compilé
	* scripts
	* base de données
	* bibliothèque de programme
	* etc.
* catalogues
	* les répertoires
		* contiennent d'autres répertoires, des fichiers normaux ou des fichiers spéciaux.
* spéciaux
	* mode bloc
		* permet l'accès à des périphériques de type bloc (dd usb, dd sata, etc...)
	* mode caractères
		* mode pile :  pour accéder au bloc n il faut d'abord accéder au bloc n-1.
	* mode FIFO
		* mode file : tubes ou pipes, permet l'échange de données entre processus (premier entré premier sortie)
	* mode socket
		* Permet la communication entre processus par protocoles réseau
	* liens symboliques


## Les chemins

1. Chemin absolue
	- démarre à la racine
	- traverse tous les répertoires jusqu'au répertoire rechercher
	- ne contient ni . ni ..
1. Chemin relatif
	- démarre dans le répertoire actuel (actif, pwd (print working directory))
	- peut contenir le . ou les ..
	- est le chemin le plus cours jusqu'à la destination

## Le bloc

Le bloc est constitué de plusieurs octets.
Le système de fichier détermine une taille en octets pour les blocs. 