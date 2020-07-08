---
title: Procédure pour installer le client via la ligne de commande
description: Procédure pour installer le client via la ligne de commande
author: dansimp
ms.assetid: ed372403-64ff-48ff-a3cd-a46cad04a4d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: eca594e1399b4ca4f680f68efffcd011fdc5f042
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807061"
---
# Procédure pour installer le client via la ligne de commande


Les rubriques de cette section incluent des procédures permettant d’installer le client de bureau App-V (App-V) ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) en utilisant setup.exe ou setup.msi. Des droits d’administration sont requis pour exécuter un programme d’installation.

Vous pouvez utiliser des paramètres de ligne de commande facultatifs pour appliquer des paramètres de configuration spécifiques au client App-V lors de l’installation. Pour plus d’informations sur l’utilisation des paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md). Si vous avez appliqué des paramètres de Registre à un ordinateur avant de déployer un client, par exemple, à l’aide d’une stratégie de groupe, ces paramètres sont conservés et les paramètres de ligne de commande supplémentaires sont appliqués. Les valeurs des paramètres de ligne de commande remplacent toute valeur existante pour le même paramètre.

**Remarques**  Lorsque vous installez le client App-V pour une utilisation avec un cache en lecture seule, par exemple avec une implémentation de serveur VDI, vous devez définir le paramètre *AUTOLOADTARGET* sur None pour empêcher le client d’essayer de mettre à jour des applications lorsque le cache est en lecture seule.

 

Pour plus d’informations sur la définition de ces valeurs de paramètres après l’installation, voir [Comment configurer les paramètres du registre des clients App-v à l’aide de la ligne de commande](https://go.microsoft.com/fwlink/?LinkId=169355) ( https://go.microsoft.com/fwlink/?LinkId=169355) dans le guide des opérations d’application-v).

**Remarques**  Si un paramètre de configuration de l’ordinateur de l’utilisateur dépend du chemin d’installation du client, Notez que le client de virtualisation des applications (App-V) 4.5 copie ses fichiers d’installation dans un autre dossier que les versions précédentes. Par défaut, une nouvelle installation du client App-V 4.5 copie ses fichiers d’installation dans le dossier du client de la virtualisation de l’application C:\\Program Files\\Microsoft. Si une version antérieure du client est déjà installée, l’exécution du programme d’installation du client App-V 4,5 effectue une mise à niveau du client existant à l’aide du dossier d’installation existant.

 

\ [Valeur du jeton de modèle \]

**Remarques**  Pour App-version 4.6 ou ultérieure, lorsque le client App-V est installé, SFTLDR.DLL est copié dans l’annuaire Windows\\system32. Si le client App-V est installé sur un système 64 bits, SFTLDR\_WOW64.DLL est copié dans l’annuaire Windows\\SysWOW64.

 

\ [Valeur du jeton de modèle \]

## Dans cette section


Les rubriques suivantes expliquent comment installer le client de bureau App-V ou le client App-V pour les services Bureau à distance (auparavant services Terminal Server) en utilisant setup.exe ou setup.msi.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-exe"></a>[Procédure pour installer le client App-V Client à l'aide de setup.exe](how-to-install-the-app-v-client-by-using-setupexe-new.md)  
Fournit une procédure pas à pas pour l’installation du client App-V à l’aide du programme setup.exe.

<a href="" id="how-to-install-the-app-v-client-by-using-setup-msi"></a>[Procédure pour installer le client App-V Client à l'aide de setup.msi](how-to-install-the-app-v-client-by-using-setupmsi-new.md)  
Fournit des procédures pas à pas pour l’installation de logiciels requis et également du client App-V à l’aide du programme setup.msi.

## Rubriques connexes


[Paramètres de ligne de commande du programme d'installation d'Application Virtualization Client](application-virtualization-client-installer-command-line-parameters.md)

[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour publier une application virtuelle sur le client](how-to-publish-a-virtual-application-on-the-client.md)

[Procédure pour désinstaller App-V Client](how-to-uninstall-the-app-v-client.md)

 

 





