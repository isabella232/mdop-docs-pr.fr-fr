---
title: Comment déployer un espace de travail MED-V manuellement
description: Comment déployer un espace de travail MED-V manuellement
author: dansimp
ms.assetid: 94bfb209-2230-49b6-bb40-9c6ab088dbf4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 3f13d06e2232681f87df7a71b9a3ef3269b4f9ce
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812258"
---
# Comment déployer un espace de travail MED-V manuellement


Dans certains cas, vous voudrez peut-être déployer votre espace de travail MED-V manuellement, par exemple, si votre entreprise n’utilise pas de système électronique de distribution de logiciels pour déployer des applications.

Cette section fournit des instructions sur le déploiement manuel d’un espace de travail MED-V.

**Pour déploiement manuel d’un espace de travail MED-V**

1.  Copiez toutes les applications prérequises et les fichiers de package d’espace de travail MED-V sur un lecteur partagé ou sur un DVD. Voici la liste des applications et fichiers nécessaires.

    -   **PC virtuel Windows**. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    -   **Ajouts et mises à jour de l’ordinateur virtuel Windows**. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    -   **Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation).

        **Warning**  
        Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL. Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.



~~~
-   **MED-V Workspace Installer, VHD, and Setup Executable** – created with the **MED-V Workspace Packager**. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    **Important**  
    The compressed VHD file (.medv) and the Setup executable program (setup.exe) must be in the same folder as the MED-V workspace installer.
~~~



2. Installez les éléments suivants dans l’ordre indiqué. L’utilisateur final peut exécuter cette tâche manuellement ou vous pouvez créer un script pour installer les éléments suivants:

   -   Le PC virtuel Windows et les mises à jour et ajouts de PC virtuelles. Un redémarrage de l’ordinateur est requis.

   -   Agent hôte MED-V.

       **Remarque**  
       S’il est en cours d’exécution, Internet Explorer doit être redémarré pour pouvoir terminer l’installation de l’agent hôte MED-V.



~~~
-   The MED-V workspace package.

    Install the MED-V workspace by running the setup.exe program that is included in the MED-V workspace package files.
~~~

3. Pour la première fois.

   Après l’installation de l’espace de travail MED-V, vous avez la possibilité de démarrer MED-V. L’agent hôte MED-V est alors démarré. Vous pouvez démarrer MED-V à ce moment ou démarrer l’agent hôte MED-V plus tard pour terminer la première configuration.

   Pour démarrer l’agent hôte MED-V, cliquez sur **Démarrer**, sur **tous les programmes**, sur **virtualisation de bureau de Microsoft**, puis sur agent d' **hébergement med-v**.

## Rubriques connexes


[Déploiement d'un espace de travail MED-V via un système de distribution électronique de logiciels](how-to-deploy-a-med-v-workspace-through-an-electronic-software-distribution-system.md)

[Comment déployer un espace de travail MED-V dans une image Windows7](how-to-deploy-a-med-v-workspace-in-a-windows-7-image.md)

[Déploiement du package d'espace de travail MED-V](deploying-the-med-v-workspace-package.md)









