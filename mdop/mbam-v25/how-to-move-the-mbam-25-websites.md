---
title: Comment déplacer les sites Web MBAM2.5
description: Comment déplacer les sites Web MBAM2.5
author: dansimp
ms.assetid: 71af9a54-c27b-408f-9d75-37c0d02e730e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa5bd8156810b3dccc1588b4dfd4cadd96fd22fb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811340"
---
# Comment déplacer les sites Web MBAM2.5


Utilisez ces procédures pour déplacer les sites Web MBAM suivants d’un ordinateur vers un autre, c’est-à-dire pour déplacer les fonctionnalités suivantes du serveur A vers le serveur B:

-   Site Web d’administration et de surveillance

-   Portail libre-service

**Important**  Lors de la configuration de ces deux sites Web, vous devez fournir la même chaîne de connexion, les URL de rapports, les comptes de groupe et le compte de domaine du pool d’applications de service Web que vous utilisez actuellement. Si vous n’utilisez pas les mêmes valeurs, vous ne pouvez pas accéder à certains serveurs. Pour obtenir les valeurs actuelles, utilisez la cmdlet Windows PowerShell **Get-MbamWebApplication** .

 

**Pour déplacer le site Web d’administration et de surveillance vers un autre serveur**

1.  Sur le serveur B, installez le logiciel serveur MBAM 2,5. Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité de **site Web Administration et analyse** .

    Vous pouvez également utiliser l’applet de contrôle Windows PowerShell **Enable-MbamWebApplication** pour configurer le site Web d’administration et de surveillance.

    Pour obtenir des instructions sur la configuration du site Web d’administration et de surveillance, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

**Pour déplacer le portail libre-service vers un autre serveur**

1.  Sur le serveur B, installez le logiciel serveur MBAM 2,5. Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonctionnalité de **portail libre-service** .

    Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamWebApplication** pour configurer le portail libre-service.

    Pour obtenir des instructions sur la configuration du site Web d’administration et de surveillance, voir [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

3.  Si les ordinateurs clients de votre organisation n’ont pas accès au réseau de distribution de contenu Microsoft, vous devez également déplacer les fichiers JavaScript. Pour plus d’informations, reportez-vous à la rubrique [configuration du portail libre-service lorsque les ordinateurs clients ne peuvent pas accéder au réseau de distribution de contenu Microsoft](how-to-configure-the-self-service-portal-when-client-computers-cannot-access-the-microsoft-content-delivery-network.md) .

4.  Personnaliser le portail libre-service pour votre organisation. Utilisez les instructions de la section [Personnalisation du portail libre-service de votre organisation](customizing-the-self-service-portal-for-your-organization.md) pour vérifier vos personnalisations actuelles et configurer des paramètres personnalisés sur le portail libre serveur sur le serveur B.



## Rubriques connexes


[Comment configurer les applications Web MBAM2.5](how-to-configure-the-mbam-25-web-applications.md)

[Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Déplacement des composants MBAM2.5 vers un autre serveur](moving-mbam-25-features-to-another-server.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





