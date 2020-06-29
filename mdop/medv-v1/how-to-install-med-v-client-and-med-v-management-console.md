---
title: Comment installer le client MED-V et la console de gestion MED-V
description: Comment installer le client MED-V et la console de gestion MED-V
author: dansimp
ms.assetid: 8a5f3010-3a50-487e-99d8-e352e5cb51c6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 24a486cc7cf5534171f80b08dc93742e03cd4a0d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812083"
---
# Comment installer le client MED-V et la console de gestion MED-V


Les composants MED-V suivants sont inclus dans le package client. msi:

-   Client MED-V: logiciel MED-V qui doit être installé sur les ordinateurs clients pour exécuter des espaces de travail MED-V.

-   La console de gestion MED-V, l’outil d’administration que les administrateurs peuvent utiliser pour créer et gérer des images, des espaces de travail MED-V et des stratégies.

La console de gestion MED-V et le client MED-V sont tous deux installés à partir du package client MED-V. Toutefois, le client MED-V peut être installé indépendamment sans la console de gestion MED-V en désactivant la case à cocher **installer l’application de gestion Med-v** lors de l’installation.

**Remarque**  
Les clients MED-V et la console de gestion MED-V peuvent uniquement être installés sur des ordinateurs Windows 7, Windows Vista et Windows XP. Elles ne peuvent pas être installées sur les produits serveur.



**Remarque**  
N’installez pas le client MED-V à l’aide de la commande Windows **runas** .



**Pour installer le client MED-V**

1.  Connectez-vous en tant qu’utilisateur disposant de droits d’administrateur local sur l’ordinateur local.

2.  Exécutez le package MED-V. msi.

    Le package MED-V. msi est appelé *MED-V\_x.msi*, où *x* représente le numéro de version.

    Par exemple, *MED-V\_1.0.65.msi*.

3.  Lorsque l’écran d’accueil de l' **Assistant InstallShield** s’affiche, cliquez sur **suivant**.

4.  Sur l’écran **contrat de licence** , lisez le contrat de licence, cliquez sur **J’accepte les termes du contrat de licence**, puis cliquez sur **suivant**.

    L’écran **dossier de destination** s’affiche avec le dossier d’installation par défaut affiché.

    Le dossier d’installation par défaut est le répertoire dans lequel le système d’exploitation est installé.

    -   Pour modifier le dossier dans lequel vous souhaitez installer MED-V, cliquez sur **modifier**, puis recherchez un dossier existant.

5.  Cliquez sur **Suivant**.

6.  Dans l’écran **paramètres de med-v** , configurez l’installation de med-v comme suit:

    -   Activez la case à cocher **installer l’application de gestion MED-V** pour inclure le composant de gestion dans l’installation.

        **Remarque**  
        Les administrateurs de virtualisation de bureau de l’entreprise doivent installer l’application de gestion MED-V. Cette application est nécessaire pour la configuration des images de bureau et des espaces de travail MED-V.



~~~
-   Select the **Load MED-V when Windows starts** check box to start MED-V automatically on startup.

-   Select the **Add a MED-V shortcut to my desktop** check box to create a MED-V shortcut on your desktop.

-   In the **Server address** field, type the server address.

-   In the **Server port** field, type the server's port.

-   Select the **Server requires encrypted connections (https)** check box to work with https.

-   The default virtual machine images folder is displayed. The default installation folder is *%systemdrive%\\MED-V Images\\*. To change the folder where MED-V should be installed, click **Change**, and browse to an existing folder.
~~~

7. Cliquez sur **Suivant**.

8. Dans l’écran **prêt à installer le programme** , cliquez sur **installer**.

   L’installation du client MED-V démarre. Cela peut prendre quelques minutes et l’écran risque de ne pas afficher de texte. Lors de l’installation, plusieurs écrans de progression apparaissent. Si un message s’affiche, suivez les instructions fournies.

   Une fois l’installation terminée, l’écran **InstallShield terminé** s’affiche.

9. Cliquez sur **Terminer** pour fermer l’Assistant.

## Rubriques connexes


[Configurations prises en charge](supported-configurationsmedv-orientation.md)

[Listes de contrôle pour l'installation et la mise à niveau](installation-and-upgrade-checklists.md)









