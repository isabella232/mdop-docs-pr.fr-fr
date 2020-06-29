---
title: Comment installer MED-V Client
description: Comment installer MED-V Client
author: dansimp
ms.assetid: bfac6de7-d96d-4b3e-bd8b-183e051e53c8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b2e4468b15c0c196bf605b1b5d129ab38678ec74
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812209"
---
# Comment installer MED-V Client


Dans un scénario basé sur un package de déploiement, l’installation du client MED-V est incluse dans le package de déploiement et installée directement à partir du package.

**Important**  
Lors de l’utilisation d’un package de déploiement qui n’inclut pas d’image, assurez-vous que l’image est téléchargée sur le Web ou déplacée vers le dossier de préinstallation avant d’installer le package de déploiement.



**Pour installer un package de déploiement**

1.  Effectuez l'une des opérations suivantes:

    -   Téléchargez le package MED-V à partir du Web.

    -   Insérez le port USB ou DVD de déploiement dans le lecteur hôte.

2.  Si MED-V ne démarre pas automatiquement, double-cliquez sur MED-VAutoInstaller.exe.

    Une boîte de dialogue s’affiche, indiquant les composants déjà installés et ceux qui sont actuellement installés.

    **Remarque**  
    Si une version de Microsoft Virtual PC non prise en charge existe sur l’ordinateur hôte, un message s’affiche pour vous demander de désinstaller la version existante et de réexécuter le programme d’installation.



~~~
**Note**  
If an older version of the MED-V client exists, it will prompt you asking whether you want to upgrade.



Depending on the components that have been installed, you might need to reboot. If rebooting is necessary, a message appears notifying you that you must reboot.
~~~

3. Le cas échéant, redémarrez l’ordinateur.

   Lorsque l’installation est terminée, MED-V démarre et un message s’affiche, indiquant que l’installation est terminée.

4. Connectez-vous à MED-V en utilisant le nom d’utilisateur et le mot de passe suivants:

   -   Entrez le nom de domaine et le nom d’utilisateur, suivis du mot de passe de l’utilisateur autorisé à travailler avec MED-V.

       Exemple: "Domain \ _name \\user\ _name", "password"

## Rubriques connexes


[Comment configurer un package de déploiement](how-to-configure-a-deployment-package.md)

[Comment charger une image MED-V sur le serveur](how-to-upload-a-med-v-image-to-the-server.md)

[Référence des lignes de commande d'installation du client](client-installation-command-line-reference.md)









