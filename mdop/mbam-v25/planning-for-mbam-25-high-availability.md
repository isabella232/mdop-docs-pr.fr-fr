---
title: Planification de la haute disponibilité de MBAM2.5
description: Planification de la haute disponibilité de MBAM2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812059"
---
# <span data-ttu-id="36f89-103">Planification de la haute disponibilité de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="36f89-103">Planning for MBAM 2.5 High Availability</span></span>


<span data-ttu-id="36f89-104">Le contrôle et l’administration de BitLocker (MBAM) Microsoft BitLocker peuvent garantir une disponibilité élevée grâce à l’utilisation d’une ou de plusieurs des technologies suivantes, qui sont décrites dans les sections suivantes:</span><span class="sxs-lookup"><span data-stu-id="36f89-104">Microsoft BitLocker Administration and Monitoring (MBAM) can maintain high availability through use of one or more of the following technologies, which are described in the following sections:</span></span>

-   [<span data-ttu-id="36f89-105">Groupes de disponibilité SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="36f89-105">SQL Server AlwaysOn availability groups</span></span>](#bkmk-alwayson)

-   [<span data-ttu-id="36f89-106">Regroupement Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="36f89-106">Microsoft SQL Server clustering</span></span>](#bkmk-sql-clustering)

-   [<span data-ttu-id="36f89-107">Équilibrage de la charge réseau IIS</span><span class="sxs-lookup"><span data-stu-id="36f89-107">IIS Network Load Balancing</span></span>](#bkmk-load-balance)

-   [<span data-ttu-id="36f89-108">Mise en miroir de base de données dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="36f89-108">Database mirroring in SQL Server</span></span>](#bkmk-db-mirroring)

-   [<span data-ttu-id="36f89-109">Sauvegarder des bases de données MBAM à l’aide du service de cliché instantané de volume</span><span class="sxs-lookup"><span data-stu-id="36f89-109">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>](#bkmk-vss)

<span data-ttu-id="36f89-110">Utilisez les informations contenues dans les sections suivantes pour mieux comprendre les options de déploiement d’MBAM dans une configuration très disponible.</span><span class="sxs-lookup"><span data-stu-id="36f89-110">Use the information in the following sections to help you understand the options to deploy MBAM in a highly available configuration.</span></span>

## <a href="" id="bkmk-alwayson"></a><span data-ttu-id="36f89-111">Prise en charge des groupes de disponibilité SQL Server AlwaysOn</span><span class="sxs-lookup"><span data-stu-id="36f89-111">Support for SQL Server AlwaysOn availability groups</span></span>


<span data-ttu-id="36f89-112">MBAM vous permet de configurer et de gérer les groupes de disponibilités pour les bases de données dans Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36f89-112">MBAM enables you to configure and manage availability groups for the databases in Microsoft SQL Server.</span></span> <span data-ttu-id="36f89-113">Un groupe de disponibilité pour MBAM prend en charge un environnement de basculement dans lequel la base de données d’audit et de conformité et la base de données de récupération échouent ensemble plutôt que séparément.</span><span class="sxs-lookup"><span data-stu-id="36f89-113">An availability group for MBAM supports a failover environment where the Compliance and Audit Database and the Recovery Database fail over together rather than separately.</span></span>

<span data-ttu-id="36f89-114">Un groupe de disponibilité prend en charge un ensemble de bases de données principales en lecture/écriture et un à quatre ensembles de bases de données secondaires correspondantes.</span><span class="sxs-lookup"><span data-stu-id="36f89-114">An availability group supports a set of read/write primary databases and one to four sets of corresponding secondary databases.</span></span> <span data-ttu-id="36f89-115">Les bases de données secondaires peuvent éventuellement être mises à disposition d’autorisations en lecture seule, de quelques opérations de sauvegarde ou pour les deux.</span><span class="sxs-lookup"><span data-stu-id="36f89-115">Optionally, secondary databases can be made available for read-only permission, some backup operations, or for both.</span></span>

<span data-ttu-id="36f89-116">Pour plus d’informations sur la configuration des groupes de disponibilité, voir groupes de disponibilité [AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).</span><span class="sxs-lookup"><span data-stu-id="36f89-116">For information about how to set up availability groups, see [AlwaysOn Availability Groups](https://go.microsoft.com/fwlink/?LinkId=393277).</span></span>

## <a href="" id="bkmk-sql-clustering"></a><span data-ttu-id="36f89-117">Regroupement Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="36f89-117">Microsoft SQL Server clustering</span></span>


<span data-ttu-id="36f89-118">Vous pouvez exécuter la base de données d’audit et de conformité MBAM 2,5 et la base de données de récupération sur des ordinateurs exécutant des clusters SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36f89-118">You can run the MBAM 2.5 Compliance and Audit Database and the Recovery Database on computers that are running SQL Server clusters.</span></span>

## <a href="" id="bkmk-load-balance"></a><span data-ttu-id="36f89-119">Équilibrage de la charge réseau IIS</span><span class="sxs-lookup"><span data-stu-id="36f89-119">IIS Network Load Balancing</span></span>


<span data-ttu-id="36f89-120">Vous pouvez utiliser le service d’équilibrage de la charge réseau pour configurer un environnement hautement disponible pour les ordinateurs qui exécutent le site Web d’administration et de contrôle (également appelé support technique), le portail libre-service et les services Web déployés via Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="36f89-120">You can use Network Load Balancing to configure a highly available environment for computers that are running the Administration and Monitoring Website (also known as Help Desk), the Self-Service Portal, and the web services, which are deployed through Internet Information Services (IIS).</span></span>

### <span data-ttu-id="36f89-121">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="36f89-121">Prerequisites</span></span>

<span data-ttu-id="36f89-122">Avant de configurer l’équilibrage de charge, assurez-vous que vous remplissez les conditions préalables suivantes:</span><span class="sxs-lookup"><span data-stu-id="36f89-122">Before configuring load balancing, ensure that you have met the following prerequisites:</span></span>

-   <span data-ttu-id="36f89-123">Un équilibrage de charge doit être disponible.</span><span class="sxs-lookup"><span data-stu-id="36f89-123">A load balancer must be available.</span></span> <span data-ttu-id="36f89-124">Vous pouvez utiliser des équilibreurs de charge de Microsoft ou d’une autre société.</span><span class="sxs-lookup"><span data-stu-id="36f89-124">You can use load balancers from Microsoft or another company.</span></span> <span data-ttu-id="36f89-125">Pour plus d’informations sur la technologie de l’équilibrage de charge Microsoft, voir [créer une batterie de serveurs Web avec des serveurs IIS](https://go.microsoft.com/fwlink/?LinkId=393326).</span><span class="sxs-lookup"><span data-stu-id="36f89-125">For more information about Microsoft load balancer technology, see [Build a Web Farm with IIS Servers](https://go.microsoft.com/fwlink/?LinkId=393326).</span></span>

-   <span data-ttu-id="36f89-126">Au moins deux serveurs exécutent IIS et répondent à toutes les conditions préalables MBAM pour prendre en charge ses fonctionnalités Web, notamment ASP.NET MVC 4.</span><span class="sxs-lookup"><span data-stu-id="36f89-126">At least two servers are running IIS and have met all of the MBAM prerequisites to support its web features, including ASP.NET MVC 4.</span></span>

-   <span data-ttu-id="36f89-127">Les bases de données et rapports MBAM s’exécutent sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="36f89-127">MBAM databases and reports are running on a server.</span></span>

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> <span data-ttu-id="36f89-128">Modifications spécifiques à MBAM requises pour activer l’équilibrage de charge</span><span class="sxs-lookup"><span data-stu-id="36f89-128">MBAM-specific changes that are required to enable Load Balancing</span></span>

<span data-ttu-id="36f89-129">Effectuez les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="36f89-129">Complete the following tasks:</span></span>

1.  <span data-ttu-id="36f89-130">Enregistrez un nom de principal de service (SPN) pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web.</span><span class="sxs-lookup"><span data-stu-id="36f89-130">Register a Service Principal Name (SPN) for the virtual host name under the domain account that you are using for the web application pools.</span></span> <span data-ttu-id="36f89-131">Par exemple, si le nom d’hôte virtuel est mbamvirtual.contoso.com et que le compte de domaine utilisé pour les pools d’applications Web est contoso\\mbamapppooluser, la commande suivante enregistre le SPN de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="36f89-131">For example, if the virtual host name is mbamvirtual.contoso.com, and the domain account used for the web application pools is contoso\\mbamapppooluser, the following command registers the SPN appropriately.</span></span>

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  <span data-ttu-id="36f89-132">Configurez les fonctionnalités Web de MBAM suivantes:</span><span class="sxs-lookup"><span data-stu-id="36f89-132">Configure the following MBAM web features:</span></span>

    -   <span data-ttu-id="36f89-133">Sur chaque serveur qui héberge les fonctionnalités Web de MBAM, utilisez le même compte de domaine pour les informations d’identification d’administration de pool d’applications.</span><span class="sxs-lookup"><span data-stu-id="36f89-133">On each server that will host the MBAM web features, use the same domain account for the application pool administrative credentials.</span></span>

    -   <span data-ttu-id="36f89-134">Spécifiez un nom d’hôte qui correspond au nom d’hôte virtuel (nom DNS) du cluster d’équilibrage de charge.</span><span class="sxs-lookup"><span data-stu-id="36f89-134">Specify a host name that matches the virtual host name (DNS name) of the Load Balancing cluster.</span></span> <span data-ttu-id="36f89-135">Par exemple, lorsque vous installez MBAM sur un serveur appelé «NLB1» avec un nom d’hôte virtuel de **mbamvirtual.contoso.com**, assurez-vous que le nom d’hôte que vous spécifiez dans la cmdlet Windows PowerShell est **mbamvirtual.contoso.com**.</span><span class="sxs-lookup"><span data-stu-id="36f89-135">For example, when you install MBAM on a server called "NLB1" with a virtual host name of **mbamvirtual.contoso.com**, ensure that the host name that you specify in the Windows PowerShell cmdlet is **mbamvirtual.contoso.com**.</span></span>

3.  <span data-ttu-id="36f89-136">Si vous configurez les sites Web dans une batterie de serveurs Web avec un équilibreur de charge, vous devez configurer les sites Web pour qu’ils utilisent la même clé d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="36f89-136">If you are configuring the websites in a web farm with a load balancer, you must configure the websites to use the same machine key.</span></span>

    <span data-ttu-id="36f89-137">Pour plus d’informations, reportez-vous aux sections suivantes dans l' [élément machineKey (schéma de paramètres ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span><span class="sxs-lookup"><span data-stu-id="36f89-137">For more information, see the following sections in [machineKey Element (ASP.NET Settings Schema)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):</span></span>

    -   <span data-ttu-id="36f89-138">Explication de la clé d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="36f89-138">Machine Key Explained</span></span>

    -   <span data-ttu-id="36f89-139">Considérations en matière de déploiement de fermes Web</span><span class="sxs-lookup"><span data-stu-id="36f89-139">Web Farm Deployment Considerations</span></span>

    <span data-ttu-id="36f89-140">Pour obtenir des instructions sur la génération automatique d’une clé, voir [générer une clé d’ordinateur (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span><span class="sxs-lookup"><span data-stu-id="36f89-140">For instructions about how to automatically generate a key, see [Generate a Machine Key (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).</span></span>

<span data-ttu-id="36f89-141">Les informations relatives à l’équilibrage de charge s’appliquent également aux clusters d’équilibrage de charge réseau (NLB) IIS dans Windows Server 2012 ou Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="36f89-141">The information about Load Balancing also applies to IIS Network Load Balancing (NLB) clusters in Windows Server 2012 or Windows Server2008R2.</span></span> <span data-ttu-id="36f89-142">La fonctionnalité d’équilibrage de charge réseau d’IIS dans Windows Server 2012 est en général similaire à celle de Windows Server2008R2.</span><span class="sxs-lookup"><span data-stu-id="36f89-142">The IIS Network Load Balancing functionality in Windows Server 2012 is generally the same as in Windows Server2008R2.</span></span> <span data-ttu-id="36f89-143">Toutefois, certains détails de la tâche diffèrent dans Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="36f89-143">However, some task details are different in Windows Server 2012.</span></span> <span data-ttu-id="36f89-144">Pour plus d’informations sur les nouvelles méthodes de tâches, voir [tâches de gestion et navigation dans Windows server 2012 R2 Preview et Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span><span class="sxs-lookup"><span data-stu-id="36f89-144">For information about new ways to do tasks, see [Common Management Tasks and Navigation in Windows Server 2012 R2 Preview and Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).</span></span>

## <a href="" id="bkmk-db-mirroring"></a><span data-ttu-id="36f89-145">Mise en miroir de base de données dans SQL Server</span><span class="sxs-lookup"><span data-stu-id="36f89-145">Database mirroring in SQL Server</span></span>


<span data-ttu-id="36f89-146">MBAM prend en charge l’utilisation de la mise en miroir SQL Server, où la base de données d’audit et de conformité, ainsi que la base de données de récupération, sont mises en miroir à l’aide de deux instances de SQL Server pour chaque base de données.</span><span class="sxs-lookup"><span data-stu-id="36f89-146">MBAM supports the use of SQL Server mirroring, where the Compliance and Audit Database and the Recovery Database are mirrored by using two instances of SQL Server for each database.</span></span> <span data-ttu-id="36f89-147">Avant d’implémenter la mise en miroir, sachez que la mise en miroir est progressivement interrompue, en plus des groupes de disponibilité, décrits plus haut dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="36f89-147">Before implementing mirroring, be aware that mirroring is slowly being phased out, in favor of availability groups, which are discussed earlier in this topic.</span></span>

<span data-ttu-id="36f89-148">Pour implémenter la mise en miroir pour MBAM, vous devez spécifier les chaînes de connexion appropriées pour la configuration de la base de données en miroir à l’aide de l’applet de la cmdlet Windows PowerShell **Enable-MbamWebApplication** .</span><span class="sxs-lookup"><span data-stu-id="36f89-148">To implement mirroring for MBAM, you must specify the appropriate connection strings for the mirrored database configuration by using the **Enable-MbamWebApplication** Windows PowerShell cmdlet.</span></span> <span data-ttu-id="36f89-149">Pour plus d’informations sur les applets de MBAM 2,5 de Windows PowerShell, voir [Configuration des fonctionnalités du serveur 2,5 MBAM à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="36f89-149">For more information about the MBAM 2.5 Windows PowerShell cmdlets, see [Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).</span></span>

### <span data-ttu-id="36f89-150">Exemples d’implémentation de la mise en miroir SQL Server à l’aide de Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="36f89-150">Examples of implementing SQL Server mirroring by using Windows PowerShell</span></span>

<span data-ttu-id="36f89-151">Les exemples suivants illustrent la manière dont vous pouvez implémenter la mise en miroir SQL Server à l’aide d’applets de commande Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="36f89-151">The following examples show how you might implement SQL Server mirroring by using Windows PowerShell cmdlets.</span></span>

**<span data-ttu-id="36f89-152">Exemple1</span><span class="sxs-lookup"><span data-stu-id="36f89-152">Example 1</span></span>**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**<span data-ttu-id="36f89-153">Exemple2</span><span class="sxs-lookup"><span data-stu-id="36f89-153">Example 2</span></span>**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### <span data-ttu-id="36f89-154">Plus d’informations sur la mise en miroir SQL Server</span><span class="sxs-lookup"><span data-stu-id="36f89-154">More information about SQL Server mirroring</span></span>

<span data-ttu-id="36f89-155">Les liens suivants fournissent des informations supplémentaires sur la configuration de la mise en miroir SQL Server:</span><span class="sxs-lookup"><span data-stu-id="36f89-155">The following links provide more information about configuring SQL Server mirroring:</span></span>

-   [<span data-ttu-id="36f89-156">Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)</span><span class="sxs-lookup"><span data-stu-id="36f89-156">How to: Prepare a Mirror Database for Mirroring (Transact-SQL)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [<span data-ttu-id="36f89-157">Établir une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)</span><span class="sxs-lookup"><span data-stu-id="36f89-157">Establish a Database Mirroring Session Using Windows Authentication (SQL Server Management Studio)</span></span>](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a><span data-ttu-id="36f89-158">Sauvegarder des bases de données MBAM à l’aide du service de cliché instantané de volume</span><span class="sxs-lookup"><span data-stu-id="36f89-158">Backing up MBAM databases by using the Volume Shadow Copy Service (VSS)</span></span>


<span data-ttu-id="36f89-159">MBAM fournit un writer de service de cliché instantané de volume (VSS) appelé Microsoft BitLocker Administration and Management Writer.</span><span class="sxs-lookup"><span data-stu-id="36f89-159">MBAM provides a Volume Shadow Copy Service (VSS) writer, called the Microsoft BitLocker Administration and Management Writer.</span></span> <span data-ttu-id="36f89-160">Ce writer VSS facilite la sauvegarde de la base de données d’audit et de conformité et de la base de données de récupération.</span><span class="sxs-lookup"><span data-stu-id="36f89-160">This VSS writer facilitates the backup of the Compliance and Audit Database and the Recovery Database.</span></span>

<span data-ttu-id="36f89-161">Le writer VSS est inscrit sur chaque serveur sur lequel vous activez une application Web MBAM.</span><span class="sxs-lookup"><span data-stu-id="36f89-161">The VSS writer is registered on every server where you enable an MBAM web application.</span></span> <span data-ttu-id="36f89-162">Le writer VSS MBAM dépend du writer SQL Server VSS qui est inscrit dans le cadre de l’installation de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="36f89-162">The MBAM VSS writer depends on the SQL Server VSS Writer, which is registered as part of the Microsoft SQL Server installation.</span></span> <span data-ttu-id="36f89-163">Toute technologie de sauvegarde qui utilise des Writers VSS pour effectuer une sauvegarde peut découvrir le scripteur VSS MBAM.</span><span class="sxs-lookup"><span data-stu-id="36f89-163">Any backup technology that uses VSS writers to perform backup can discover the MBAM VSS writer.</span></span>



## <span data-ttu-id="36f89-164">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="36f89-164">Related topics</span></span>


[<span data-ttu-id="36f89-165">Planification du déploiement de MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="36f89-165">Planning to Deploy MBAM 2.5</span></span>](planning-to-deploy-mbam-25.md)

 

 
## <span data-ttu-id="36f89-166">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="36f89-166">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="36f89-167">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="36f89-167">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span>
- <span data-ttu-id="36f89-168">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="36f89-168">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




