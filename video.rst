
Installation et configuration d'un lecteur video
================================================
Le Raspberry Pi est tout à fait apte à lire des video en full HD (1080p).
On peut facilement l'utiliser pour afficher des vidéo d'une clé USB sur sa télévision.

Il n'y a malheueusement pas de lecteur vidéo déjà installé sur le Pi. Mais on va y remédier.

Installation de OMXPlayer
-------------------------
Le lecteur vidéo OMXplayer permet d'exploiter les performance vidéo du Pi.

Dans la console : ::

    sudo apt-get install omxplayer

OMXPlayer peut être utilisé depuis la console, pour plus d'info consulter son manuel : ::

    man omxplayer



Installation de TBOPlayer
-------------------------
TBOPlayer est une interface graphique simplifiant l'utilisation d'OMXPlayer. Il permet de lire des vidéo sans utiliser la ligne de commande.

Il n'est pas disponible sur les dépots standards (apt-get). Il faut l'installer depuis git: ::

    cd ~ && wget https://github.com/KenT2/tboplayer/tarball/master -O - | tar xz &&
    cd KenT2-tboplayer-* && chmod +x setup.sh && ./setup.sh

Utilisation de TBOPlayer
------------------------


Le paramètre ``-b`` permet de créer un arrière plan noir et ainsi d'éliminer les bandes non couvertes par la vidéo.

Forcer l'audio sur le HDMI
--------------------------
Il est possible que, bien que le port HDMI soit selectioné comme sortie audio, il n'ait aucun son.

L'opération suivante peut corriger ce problème :

Editer le fichier /boot/config.txt et supprimer le # pour rendre active la ligne hdmi_device=2. ::

    sudo nano /boot/config.txt



====== ===========
Ctrl-x Quitter nano
o      Enregistrer
====== ===========


