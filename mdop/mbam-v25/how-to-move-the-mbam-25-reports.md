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
# <span data-ttu-id="8d797-103">Déplacement des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d797-103">How to Move the MBAM 2.5 Reports</span></span>


<span data-ttu-id="8d797-104">Pour déplacer la fonctionnalité rapports d’un ordinateur vers un autre, procédez comme suit pour déplacer la fonctionnalité rapports du serveur A vers le serveur B.</span><span class="sxs-lookup"><span data-stu-id="8d797-104">Use these procedures to move the Reports feature from one computer to another, that is, to move the Reports feature from Server A to Server B.</span></span>

<span data-ttu-id="8d797-105">Les étapes principales pour le déplacement de la fonctionnalité de création de rapports sont les suivantes:</span><span class="sxs-lookup"><span data-stu-id="8d797-105">The high-level steps for moving the Reports feature are:</span></span>

1.  <span data-ttu-id="8d797-106">Arrêtez toutes les instances de l’MBAM site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8d797-106">Stop all instances of the MBAM Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="8d797-107">Installez le logiciel serveur MBAM 2,5 sur le serveur B et configurez la fonctionnalité rapports sur le serveur B.</span><span class="sxs-lookup"><span data-stu-id="8d797-107">Install the MBAM 2.5 Server software on Server B and configure the Reports feature on Server B.</span></span>

3.  <span data-ttu-id="8d797-108">Mettez à jour les données de connexion rapports sur les serveurs d’administration et de surveillance MBAM.</span><span class="sxs-lookup"><span data-stu-id="8d797-108">Update the reports connection data on the MBAM Administration and Monitoring servers.</span></span>

4.  <span data-ttu-id="8d797-109">Reprenez l’instance du site Web d’administration et de contrôle MBAM.</span><span class="sxs-lookup"><span data-stu-id="8d797-109">Resume the instance of the MBAM Administration and Monitoring Website.</span></span>

<span data-ttu-id="8d797-110">**Remarques**  Pour exécuter les exemples de scripts Windows PowerShell figurant dans cette rubrique, vous devez mettre à jour la stratégie d’exécution Windows PowerShell pour permettre l’exécution de scripts.</span><span class="sxs-lookup"><span data-stu-id="8d797-110">**Note** To run the example Windows PowerShell scripts in this topic, you must update the Windows PowerShell execution policy to enable scripts to be run.</span></span> <span data-ttu-id="8d797-111">Pour obtenir des instructions, voir [exécution de scripts Windows PowerShell](https://technet.microsoft.com/library/ee176949.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8d797-111">See [Running Windows PowerShell Scripts](https://technet.microsoft.com/library/ee176949.aspx) for instructions.</span></span>

 

**<span data-ttu-id="8d797-112">Arrêter le site Web d’administration et de surveillance de MBAM</span><span class="sxs-lookup"><span data-stu-id="8d797-112">Stop the MBAM Administration and Monitoring Website</span></span>**

-   <span data-ttu-id="8d797-113">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console Gestionnaire des services Internet (IIS) pour arrêter le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8d797-113">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to stop the Administration and Monitoring Website.</span></span>

    <span data-ttu-id="8d797-114">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour entrer une commande semblable à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="8d797-114">To automate this procedure, you can use Windows PowerShell to enter a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Stop-Website "Microsoft BitLocker Administration and Monitoring"
    ```

**<span data-ttu-id="8d797-115">Installez le logiciel serveur MBAM et exécutez l’Assistant Configuration de MBAM Server sur le serveur B</span><span class="sxs-lookup"><span data-stu-id="8d797-115">Install MBAM Server software and run the MBAM Server Configuration wizard on Server B</span></span>**

1.  <span data-ttu-id="8d797-116">Installez le logiciel serveur MBAM sur le serveur B. Pour obtenir des instructions, consultez [installer le logiciel serveur MBAM 2,5](installing-the-mbam-25-server-software.md).</span><span class="sxs-lookup"><span data-stu-id="8d797-116">Install the MBAM Server software on Server B. For instructions, see [Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md).</span></span>

2.  <span data-ttu-id="8d797-117">Sur le serveur B, démarrez l’Assistant Configuration de MBAM Server, cliquez sur **ajouter de nouvelles fonctionnalités**, puis sélectionnez uniquement la fonction **rapports** .</span><span class="sxs-lookup"><span data-stu-id="8d797-117">On Server B, start the MBAM Server Configuration wizard, click **Add New Features**, and then select only the **Reports** feature.</span></span>

    <span data-ttu-id="8d797-118">Vous pouvez également utiliser l’applet de cmdlet Windows PowerShell **Enable-MbamReport** pour configurer les rapports.</span><span class="sxs-lookup"><span data-stu-id="8d797-118">Alternatively, you can use the **Enable-MbamReport** Windows PowerShell cmdlet to configure the Reports.</span></span>

    <span data-ttu-id="8d797-119">Pour obtenir des instructions sur la configuration des rapports, voir [Configuration des rapports 2,5 de MBAM](how-to-configure-the-mbam-25-reports.md).</span><span class="sxs-lookup"><span data-stu-id="8d797-119">For instructions on how to configure the Reports, see [How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md).</span></span>

**<span data-ttu-id="8d797-120">Mettre à jour les données de connexion rapports sur le serveur d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="8d797-120">Update the reports connection data on the Administration and Monitoring Server</span></span>**

1.  <span data-ttu-id="8d797-121">Sur le serveur qui exécute la fonctionnalité rapports, utilisez la console Gestionnaire des services Internet (IIS) pour mettre à jour l’URL du rapport.</span><span class="sxs-lookup"><span data-stu-id="8d797-121">On the server that is running the Reports feature, use the Internet Information Services (IIS) Manager console to update the Reports URL.</span></span>

2.  <span data-ttu-id="8d797-122">Développez le centre d' **administration et de contrôle Microsoft BitLocker**, puis sélectionnez le nœud du **support technique** .</span><span class="sxs-lookup"><span data-stu-id="8d797-122">Expand **Microsoft BitLocker Administration and Monitoring**, and then select the **HelpDesk** node.</span></span>

3.  <span data-ttu-id="8d797-123">Dans la section **gestion** de l' **affichage fonctionnalités**, sélectionnez **éditeur de configuration**.</span><span class="sxs-lookup"><span data-stu-id="8d797-123">In the **Management** section of the **Features View**, select **Configuration Editor**.</span></span>

4.  <span data-ttu-id="8d797-124">Dans le champ **section** , sélectionnez **appSettings**.</span><span class="sxs-lookup"><span data-stu-id="8d797-124">In the **Section** field, select **appSettings**.</span></span>

5.  <span data-ttu-id="8d797-125">Sélectionnez la ligne de **collection** , puis cliquez sur le bouton «points de suspension» **(...)** dans l’extrémité droite du volet pour ouvrir l' **éditeur de collection**.</span><span class="sxs-lookup"><span data-stu-id="8d797-125">Select the **Collection** row, and then click the "ellipses" button **(…)** at the far right of the pane to open the **Collection Editor**.</span></span>

6.  <span data-ttu-id="8d797-126">Dans l' **éditeur de collection**, sélectionnez la ligne qui contient **Microsoft. mbam. reports. URL**et mettez à jour la valeur pour **Microsoft. mbam. reports. URL** pour refléter le nom de serveur pour le serveur B.</span><span class="sxs-lookup"><span data-stu-id="8d797-126">In the **Collection Editor**, select the row that contains **Microsoft.Mbam.Reports.Url**, and update the value for **Microsoft.Mbam.Reports.Url** to reflect the server name for Server B.</span></span>

    <span data-ttu-id="8d797-127">Si vous avez précédemment configuré la fonctionnalité rapports sur une instance nommée de SQL Server Reporting Services, ajoutez ou mettez à jour le nom de l’instance dans l’URL, par exemple:</span><span class="sxs-lookup"><span data-stu-id="8d797-127">If you previously configured the Reports feature on a named instance of SQL Server Reporting Services, add or update the name of the instance to the URL, for example:</span></span>

    `http://$SERVERNAME$/ReportServer_$SQLSRSINSTANCENAME$/Pages....)`

7.  <span data-ttu-id="8d797-128">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande du serveur d’administration et de surveillance similaire à l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="8d797-128">To automate this procedure, you can use Windows PowerShell to run a command on the Administration and Monitoring Server that is similar to the following code example.</span></span>

    ``` syntax
    PS C:\> Set-WebConfigurationProperty '/appSettings/add[@key="Microsoft.Mbam.Reports.Url"]' -PSPath "IIS:\\sites\Microsoft Bitlocker Administration and Monitoring\HelpDesk" -Name "Value" -Value "http://$SERVERNAME$/ReportServer[_$SRSINSTANCENAME$]/Pages/ReportViewer.aspx?/Microsoft+BitLocker+Administration+and+Monitoring/"
    ```

    <span data-ttu-id="8d797-129">À l’aide des descriptions figurant dans le tableau suivant, remplacez les valeurs dans l’exemple de code par des valeurs qui correspondent à votre environnement.</span><span class="sxs-lookup"><span data-stu-id="8d797-129">Using the descriptions in the following table, replace the values in the code example with values that match your environment.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="8d797-130">Paramètre</span><span class="sxs-lookup"><span data-stu-id="8d797-130">Parameter</span></span></th>
    <th align="left"><span data-ttu-id="8d797-131">Description</span><span class="sxs-lookup"><span data-stu-id="8d797-131">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="8d797-132">$SERVERNAME $</span><span class="sxs-lookup"><span data-stu-id="8d797-132">$SERVERNAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8d797-133">Nom du serveur sur lequel les rapports ont été déplacés.</span><span class="sxs-lookup"><span data-stu-id="8d797-133">Name of the server to which the Reports were moved.</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="8d797-134">$SRSINSTANCENAME $</span><span class="sxs-lookup"><span data-stu-id="8d797-134">$SRSINSTANCENAME$</span></span></p></td>
    <td align="left"><p><span data-ttu-id="8d797-135">Nom de l’instance de SQL Server Reporting Services vers laquelle les rapports ont été déplacés.</span><span class="sxs-lookup"><span data-stu-id="8d797-135">Name of the instance of SQL Server Reporting Services to which the Reports were moved.</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

**<span data-ttu-id="8d797-136">Reprendre l’instance du site Web d’administration et de surveillance</span><span class="sxs-lookup"><span data-stu-id="8d797-136">Resume the instance of the Administration and Monitoring Website</span></span>**

1.  <span data-ttu-id="8d797-137">Sur le serveur qui exécute le site Web d’administration et de surveillance, utilisez la console du gestionnaire des services Internet (IIS) pour démarrer le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="8d797-137">On the server that is running the Administration and Monitoring Website, use the Internet Information Services (IIS) Manager console to start the Administration and Monitoring Website.</span></span>

2.  <span data-ttu-id="8d797-138">Pour automatiser cette procédure, vous pouvez utiliser Windows PowerShell pour exécuter une commande similaire à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="8d797-138">To automate this procedure, you can use Windows PowerShell to run a command that is similar to the following:</span></span>

    ``` syntax
    PS C:\> Start-Website "Microsoft BitLocker Administration and Monitoring"
    ```

    <span data-ttu-id="8d797-139">**Remarques**  Pour exécuter cette commande, vous devez ajouter le module IIS pour Windows PowerShell à l’instance actuelle de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8d797-139">**Note** To run this command, you must add the IIS module for Windows PowerShell to the current instance of Windows PowerShell.</span></span>

     



## <span data-ttu-id="8d797-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8d797-140">Related topics</span></span>


[<span data-ttu-id="8d797-141">Configuration des rapports MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="8d797-141">How to Configure the MBAM 2.5 Reports</span></span>](how-to-configure-the-mbam-25-reports.md)

[<span data-ttu-id="8d797-142">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="8d797-142">Configuring MBAM 2.5 Server Features by Using Windows PowerShell</span></span>](configuring-mbam-25-server-features-by-using-windows-powershell.md)

[<span data-ttu-id="8d797-143">Déplacement des composants MBAM2.5 vers un autre serveur</span><span class="sxs-lookup"><span data-stu-id="8d797-143">Moving MBAM 2.5 Features to Another Server</span></span>](moving-mbam-25-features-to-another-server.md)

 
## <span data-ttu-id="8d797-144">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="8d797-144">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="8d797-145">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="8d797-145">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="8d797-146">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="8d797-146">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





