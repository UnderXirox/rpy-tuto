
Installation du système d'impression
====================================
Par défaut, il n'y a pas de système d'impression installé sur le Pi.
Il faut en installer un afin d'ajouter une imprimante; puis imprimer.

Installation de CUPS
--------------------
Le système d'impression standards sur Unix, Linux et macOS est CUPS (Common Unix Printing System).

Depuis une fenêtre de terminal :

Mettre à jour la liste des paquets::

    sudo apt-get update

Installer CUPS::

    sudo apt-get install cups

Donner le droit à l'utilisateur pi de gérer les imprimantes::

    sudo usermod -a -G lpadmin pi

Ajout d'une imprimante
----------------------
La console d'administration est maintenant accessible en entrant l'adresse suivante dans le navigateur: ::

    http://localhost:631

.. image:: images/cups.jpg

Localhost, correspond à l'addresse locale.

- Cliquez sur **Ajout d'imprimantes et  de classes**
- Cliquez sur ajouter une imprimante et entrez le nom d'utilisateur (**pi**) et le mot de passe (**raspberry**)
- Cochez l'imprimante Brother HL-2250DN et cliquez continuer
- Cliquez à nouveau sur continuer

Maintenant il faut choisr le driver pour l'imprimante, choisisez Brother HL-2060 (compatible avec ce modèle). Puis continuer.

- Cliquez définir les options par défaut

L'imprimante est maintenant installée.

