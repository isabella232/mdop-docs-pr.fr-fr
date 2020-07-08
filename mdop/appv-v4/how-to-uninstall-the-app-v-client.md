---
title: Procédure pour désinstaller App-V Client
description: Procédure pour désinstaller App-V Client
author: dansimp
ms.assetid: 07591270-9651-4bb5-a5b3-e0fc009bd9e2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: acb3f53b42027ff2c1b84fd2ab2bdde3c52f96de
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806741"
---
# Procédure pour désinstaller App-V Client


Suivez la procédure ci-dessous pour désinstaller le client de virtualisation des applications de l’ordinateur.

**Pour désinstaller le client de bureau de virtualisation des applications**

1.  Dans le panneau de configuration, double-cliquez sur **Ajout/suppression de programmes** (ou dans Windows Vista, **programmes et fonctionnalités**), puis double-cliquez sur **client de bureau Microsoft Application Virtualization**.

2.  Dans la boîte de dialogue qui s’affiche, cliquez sur **Oui** pour continuer le processus de désinstallation.

    **Important**  Le processus de désinstallation ne peut pas être annulé ou interrompu.

     

3.  Lorsqu’un message vous signale que l’application de barre des tâches du client de virtualisation des applications Microsoft doit être fermée, cliquez avec le bouton droit sur l’icône App-V dans la zone de notification et sélectionnez **quitter** pour fermer l’application. Cliquez ensuite sur **Réessayer** pour continuer le processus de désinstallation.

    **Important**  Vous pouvez voir un message indiquant qu’une ou plusieurs applications virtuelles sont utilisées. Fermez toutes les applications ouvertes et enregistrez vos données avant de continuer. Cliquez sur **OK** pour continuer le processus de désinstallation.

     

4.  Une barre de progression indique le temps restant. Lorsque cette étape est terminée, vous devez redémarrer l’ordinateur de manière à ce que tous les pilotes associés puissent être arrêtés pour achever le processus de désinstallation.

    **Remarques**  Les clés de Registre suivantes demeurent après la fin du processus de désinstallation:

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard "client" = dword: 00000000

    -   HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\SystemGuard\\SecKey

     

## Rubriques connexes


[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

 

 





