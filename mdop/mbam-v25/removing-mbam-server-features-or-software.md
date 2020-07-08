---
title: Suppression du logiciel ou des composants serveur de MBAM
description: Suppression du logiciel ou des composants serveur de MBAM
author: dansimp
ms.assetid: 5212ba3f-124d-43c5-824a-608e9a192e86
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 2e6e57c3d2a62a4e01242ade7a82a7bfa551da83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810878"
---
# Suppression du logiciel ou des composants serveur de MBAM


Ces instructions expliquent comment supprimer des logiciels et des fonctionnalités de Microsoft BitLocker administration et de la surveillance (MBAM). Si vous supprimez les fonctionnalités de MBAM Server, seules les fonctionnalités configurées sont supprimées du serveur et non du logiciel de serveur MBAM. Si vous supprimez le logiciel serveur MBAM, le logiciel et les fonctionnalités de MBAM Server que vous avez configurées sur ce serveur sont supprimés.

**Remarques**  Pour empêcher la suppression accidentelle de données, MBAM ne propose aucun mécanisme de suppression des bases de données. vous devez le faire manuellement.

 

## <a href="" id="bkmk-removeserverfeatures"></a>Suppression des fonctionnalités du serveur MBAM


Vous pouvez utiliser l’une des méthodes suivantes pour supprimer les fonctionnalités du serveur MBAM que vous avez configurées:

-   Assistant Configuration de MBAM Server

-   Cmdlets Windows PowerShell

### Utilisation de l’Assistant Configuration de MBAM Server pour supprimer des fonctionnalités

Suivez ces instructions pour utiliser l’Assistant Configuration de MBAM Server pour supprimer les fonctionnalités du serveur MBAM configurées d’un serveur.

**Pour supprimer les fonctionnalités d’MBAM à l’aide de l’Assistant**

1.  Sur le serveur sur lequel vous voulez supprimer des composants, sélectionnez **MBAM Server Configuration** pour ouvrir l’Assistant Configuration.

2.  Cliquez sur **Supprimer les fonctionnalités**, sélectionnez les fonctionnalités à supprimer, puis cliquez sur **suivant**. Une page de **Résumé** affiche les fonctionnalités que vous avez sélectionnées pour suppression.

3.  Cliquez sur **supprimer** pour commencer à supprimer les fonctionnalités, puis cliquez sur **Fermer**.

### Utilisation de Windows PowerShell pour supprimer des fonctionnalités

Suivez les étapes ci-dessous pour supprimer les fonctionnalités de MBAM Server à l’aide d’applets de commande Windows PowerShell.

**Pour supprimer les fonctionnalités d’MBAM à l’aide de Windows PowerShell**

1.  Avant de supprimer des fonctionnalités, reportez-vous à [Configuration des fonctionnalités du serveur MBAM 2,5 à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md) pour consulter les conditions préalables à l’utilisation de Windows PowerShell.

2.  Utilisez les applets de commande suivantes pour supprimer les fonctionnalités du serveur MBAM:

    -   Disable-MbamReport

    -   Disable-MbamWebApplication

    -   Disable-MbamCMIntegration

    Pour obtenir de l’aide sur les applets de contrôle Windows PowerShell, tapez cmdlet **Get-Help** &lt; *cmdlet* &gt; ou consultez la page Automation de l’application [Microsoft Desktop Optimization avec Windows PowerShell](https://go.microsoft.com/fwlink/?LinkId=393498) pour les applets de MBAM Windows PowerShell.

## Suppression du logiciel serveur MBAM


Procédez comme suit pour supprimer le logiciel serveur MBAM et toutes les fonctionnalités MBAM Server que vous avez configurées sur ce serveur.

**Pour supprimer le logiciel serveur MBAM**

1.  Sur le serveur sur lequel vous souhaitez désinstaller le logiciel serveur MBAM, exécutez **MBAMserversetup.exe** pour démarrer l’Assistant de configuration de l’administration et de la surveillance de BitLocker.

2.  Sélectionnez **désinstaller**, puis suivez les invites restantes pour terminer le processus de désinstallation du logiciel serveur MBAM.



## Rubriques connexes


[Déploiement de MBAM2.5](deploying-mbam-25.md)

 

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).



