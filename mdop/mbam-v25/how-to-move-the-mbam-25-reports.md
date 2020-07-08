---
title: Déplacement des rapports MBAM2.5
description: Déplacement des rapports MBAM2.5
author: dansimp
ms.assetid: c8223656-ca9d-41c8-94a3-64d07a6b99e9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 1cdef260b4381671a1b9de66565ece0b70876200
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804194"
---
# Déplacement des rapports MBAM2.5


Pour déplacer la fonctionnalité rapports d’un ordinateur vers un autre, procédez comme suit pour déplacer la fonctionnalité rapports du serveur A vers le serveur B.

Les étapes principales pour le déplacement de la fonctionnalité de création de rapports sont les suivantes:

1.  Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.

2.  Installez le logiciel serveur MBAM 2,5 sur le serveur B et configurez la fonctionnalité rapports sur le serveur B.

3.  Mettez à jour les données de connexion rapports sur les serveurs d’administration et de surveillance MBAM.

4.  Reprenez l’instance du site Web d’administration et de contrôle MBAM.

**Remarques**  Pour exécuter les exemples de scripts Windows PowerShell figurant dans cette rubrique, vous devez mettre à jour la stratégie d’exécution Windows PowerShell pour permettre l’exécution de scripts. Pour obtenir des instructions, voir [exécution de scripts Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .

 

**Arrêter le site Web d’administration et de surveillance de MBAM**

-   Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console Gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.

    Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B**

1.  Installez le logiciel serveur MBAM sur le serveur B. Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).

2.  Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonction **rapports** .

    Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamReport** pour configurer les rapports.

    Pour obtenir des instructions sur la configuration des rapports, voir [Configuration des rapports 2,5 de MBAM](how-to-configure-the-mbam-25-reports.md).

**Mettre à jour les données de connexion rapports sur le serveur d’administration et de surveillance**

1.  Sur le serveur qui exécute la fonctionnalité rapports, utilisez la console Gestionnaire des services Internet (IIS) pour mettre à jour l’URL du rapport.

2.  Développez le centre d' **administration et de contrôle Microsoft BitLocker**, puis sélectionnez le nœud du **support technique** .

3.  Dans la section **gestion** de l' **affichage fonctionnalités**, sélectionnez **éditeur de configuration**.

4.  Dans le champ **section** , sélectionnez **appSettings**.

5.  Sélectionnez la ligne de **collection** , puis cliquez sur le bouton «points de suspension» **(...)** dans l’extrémité droite du volet pour ouvrir l' **éditeur de collection**.

6.  Dans l' **éditeur de collection**, sélectionnez la ligne qui contient **Microsoft. mbam. reports. URL**et mettez à jour la valeur pour **Microsoft. mbam. reports. URL** pour refléter le nom de serveur pour le serveur B.

    Si vous avez précédemment configuré la fonctionnalité rapports sur une instance nommée de SQL Server Reporting Services, ajoutez ou mettez à jour le nom de l’instance dans l’URL, par exemple:

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande du serveur d’administration et de surveillance similaire à l’exemple de code suivant.

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    À l’aide des descriptions figurant dans le tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Paramètre</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>$SERVERNAME $</p></td>
    <td align="left"><p>Nom du serveur sur lequel les rapports ont été déplacés.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>$SRSINSTANCENAME $</p></td>
    <td align="left"><p>Nom de l’instance de SQL Server Reporting Services vers laquelle les rapports ont été déplacés.</p></td>
    </tr>
    </tbody>
    </table>

     

**Reprendre l’instance du site Web d’administration et de surveillance**

1.  Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.

2.  Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    **Remarques**  Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.

     



## Rubriques connexes


[Configuration des rapports MBAM2.5](how-to-configure-the-mbam-25-reports.md)

[Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[Déplacement des composants MBAM2.5 vers un autre serveur](moving-mbam-25-features-to-another-server.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





