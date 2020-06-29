---
title: Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V
description: Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807305"
---
# <span data-ttu-id="21996-103">Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V</span><span class="sxs-lookup"><span data-stu-id="21996-103">How to Configure Microsoft SQL Server Mirroring Support for App-V</span></span>


<span data-ttu-id="21996-104">Vous pouvez utiliser la procédure suivante pour configurer votre environnement Microsoft Application Virtualization (App-V) pour utiliser la mise en miroir de base de données Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21996-104">You can use the following procedure to configure your Microsoft Application Virtualization (App-V) environment to use Microsoft SQL Server database mirroring.</span></span> <span data-ttu-id="21996-105">La configuration de la mise en miroir de la base de données peut être utile pour les scénarios de reprise après sinistre et de reprise.</span><span class="sxs-lookup"><span data-stu-id="21996-105">Configuring database mirroring can help with disaster recovery and failover scenarios.</span></span> <span data-ttu-id="21996-106">App-V 4,5 SP2 prend en charge tous les modes de mise en miroir de la base de données actuellement disponibles pour Microsoft SQL Server 2005 et SQL Server 2008.</span><span class="sxs-lookup"><span data-stu-id="21996-106">App-V 4.5 SP2 supports all modes of database mirroring currently available for Microsoft SQL Server 2005 and SQL Server 2008.</span></span>

**<span data-ttu-id="21996-107">Remarque</span><span class="sxs-lookup"><span data-stu-id="21996-107">Note</span></span>**  
<span data-ttu-id="21996-108">Cette procédure est écrite pour les administrateurs habitués à configurer et à configurer les bases de données SQL Server et la mise en miroir de la base de données à l’aide de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21996-108">This procedure is written for administrators who are familiar with setting up and configuring SQL Server databases and database mirroring with Microsoft SQL Server, and therefore covers only the specific configuration settings that are unique to App-V.</span></span>



**<span data-ttu-id="21996-109">Pour configurer votre environnement App-V de façon à utiliser la mise en miroir de la base de données Microsoft SQL Server</span><span class="sxs-lookup"><span data-stu-id="21996-109">To configure your App-V environment to use Microsoft SQL Server database mirroring</span></span>**

1.  <span data-ttu-id="21996-110">Configurez la mise en miroir de la base de données SQL Server de la base de données App-V en suivant les recommandations standard pour la mise en miroir de la base de données.</span><span class="sxs-lookup"><span data-stu-id="21996-110">Set up SQL Server database mirroring of the App-V database following your standard business practices for database mirroring.</span></span> <span data-ttu-id="21996-111">Pour obtenir des informations générales sur l’implémentation de la mise en miroir de la base de données Microsoft SQL Server, utilisez les liens suivants:</span><span class="sxs-lookup"><span data-stu-id="21996-111">Use the following links for general information about implementing Microsoft SQL Server database mirroring:</span></span>

    -   <span data-ttu-id="21996-112">**Microsoft SQL 2005**:[configuration de la mise en miroir de base de données](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span><span class="sxs-lookup"><span data-stu-id="21996-112">**Microsoft SQL 2005**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)</span></span>

    -   <span data-ttu-id="21996-113">**Microsoft SQL 2008**:[configuration de la mise en miroir de base de données](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span><span class="sxs-lookup"><span data-stu-id="21996-113">**Microsoft SQL 2008**—[Setting Up Database Mirroring](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)</span></span>

    <span data-ttu-id="21996-114">De plus, vous pouvez trouver des informations pratiques recommandées en [matière de meilleures pratiques en matière de mise en miroir de la base de données](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .</span><span class="sxs-lookup"><span data-stu-id="21996-114">In addition, you can find Best Practices information in [Database Mirroring Best Practices and Performance Considerations](https://go.microsoft.com/fwlink/?LinkId=190270) (https://go.microsoft.com/fwlink/?LinkId=190270).</span></span>

2.  <span data-ttu-id="21996-115">Une fois la mise en miroir configurée, vérifiez que la base de données App-V affiche un état **(principal, synchronisé)** et que la base de données en miroir affiche un état **(miroir, synchronisé/restauré)**.</span><span class="sxs-lookup"><span data-stu-id="21996-115">After mirroring has been set up, verify that the App-V database shows a status of **(Principal, Synchronized)**, and the mirrored database shows a status of **(Mirror, Synchronized / Restoring)**.</span></span> <span data-ttu-id="21996-116">Résoudre les problèmes de mise en miroir avant de passer à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="21996-116">Resolve any mirroring issues before proceeding to the next step.</span></span> <span data-ttu-id="21996-117">Pour plus d’informations sur la surveillance de l’État, voir [surveiller l’état de mise en miroir](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .</span><span class="sxs-lookup"><span data-stu-id="21996-117">For additional information about monitoring the status, see [Monitoring Mirroring Status](https://go.microsoft.com/fwlink/?LinkId=190279) (https://go.microsoft.com/fwlink/?LinkId=190279).</span></span>

3.  <span data-ttu-id="21996-118">Sur l’ordinateur SQL Server qui héberge le miroir de la base de données App-v, créez le nom de connexion SQL Server pour le compte de service réseau du serveur de gestion des applications-v en utilisant le nom de compte \*\* &lt; Domain &gt; \\ &lt; ManagementServerHostName &gt; $ \*\*.</span><span class="sxs-lookup"><span data-stu-id="21996-118">On the SQL Server computer that hosts the mirror of the App-V database, create the SQL Server Login for the network service account of the App-V Management Server by using the account name **&lt;domain&gt;\\&lt;ManagementServerHostName&gt;$**.</span></span>

4.  <span data-ttu-id="21996-119">Installez le client natif Microsoft SQL Server sur le serveur de gestion App-V, puis sur l’ordinateur exécutant le service Web de gestion des applications-V s’il est installé sur un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="21996-119">Install the Microsoft SQL Server Native Client on the App-V Management Server, and on the computer running the App-V Management Web Service if installed on a different computer.</span></span> <span data-ttu-id="21996-120">Si vous envisagez de faire en sorte que des serveurs d’administration d’applications supplémentaires se connectent à la base de données SQL en miroir pour l’équilibrage de charge, vous devez installer le client natif Microsoft SQL Server sur ces ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="21996-120">If you plan to have additional App-V Management Servers connect to the mirrored SQL database for load balancing, you must install the Microsoft SQL Server Native Client on those computers as well.</span></span> <span data-ttu-id="21996-121">Vous pouvez télécharger le client natif Microsoft SQL Server à partir de la page [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .</span><span class="sxs-lookup"><span data-stu-id="21996-121">You can download the Microsoft SQL Server Native Client from the [Microsoft SQL Server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) page in the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=187479).</span></span>

5.  <span data-ttu-id="21996-122">Vérifiez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** et assurez-vous qu’elle contient uniquement le nom d’hôte du serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21996-122">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerName** and make sure that it contains only the host name of the SQL Server.</span></span> <span data-ttu-id="21996-123">S’il inclut un nom d’instance (par exemple, *serverhostname\\instancename*), le nom de l’instance doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="21996-123">If it includes an instance name, for example *serverhostname\\instancename*, the instance name must be removed.</span></span>

    **<span data-ttu-id="21996-124">Important</span><span class="sxs-lookup"><span data-stu-id="21996-124">Important</span></span>**  
    <span data-ttu-id="21996-125">Le serveur de gestion App-V utilise la bibliothèque de réseau TCP/IP pour communiquer avec le serveur SQL lorsque la mise en miroir de la base de données est activée, et par conséquent, les noms d’instances ne peuvent pas être utilisés.</span><span class="sxs-lookup"><span data-stu-id="21996-125">The App-V Management Server uses the TCP/IP networking library to communicate with the SQL Server when database mirroring is enabled, and therefore instance names cannot be used.</span></span> <span data-ttu-id="21996-126">Les numéros de port doivent être spécifiés dans les clés de Registre à la place.</span><span class="sxs-lookup"><span data-stu-id="21996-126">The port numbers must be specified in the registry keys instead.</span></span>



6.  <span data-ttu-id="21996-127">Vérifiez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** et assurez-vous qu’elle contient le numéro de port utilisé pour SQL sur l’ordinateur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21996-127">Check the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLServerPort** and make sure that it contains the port number that is used for SQL on the SQL Server computer.</span></span> <span data-ttu-id="21996-128">Si vous utilisez une instance nommée, cette valeur de clé doit être définie sur le port utilisé pour l’instance nommée.</span><span class="sxs-lookup"><span data-stu-id="21996-128">If you are using a named instance this key value must be set to the port that is used for the named instance.</span></span>

7.  <span data-ttu-id="21996-129">Créez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** en tant que REG \ _SZ puis définissez la valeur sur le nom d’hôte de SQL Server qui héberge le miroir.</span><span class="sxs-lookup"><span data-stu-id="21996-129">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerName** as REG\_SZ and then set the value to the host name of the SQL Server that hosts the mirror.</span></span>

8.  <span data-ttu-id="21996-130">Créez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** en tant que DWORD, puis définissez la valeur sur le numéro de port utilisé pour SQL sur l’ordinateur exécutant SQL Server pour héberger le miroir.</span><span class="sxs-lookup"><span data-stu-id="21996-130">Create the registry key **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Softgrid\\4.5\\Server\\SQLFailoverServerPort** as DWORD and then set the value to the port number that is used for SQL on the computer that is running SQL Server to host the mirror.</span></span> <span data-ttu-id="21996-131">Si vous utilisez une instance nommée pour le miroir, la valeur de cette clé doit être définie sur le numéro de port utilisé pour l’instance nommée.</span><span class="sxs-lookup"><span data-stu-id="21996-131">If you are using a named instance for the mirror this key value must be set to the port number that is used for the named instance.</span></span>

9.  <span data-ttu-id="21996-132">Sur l’ordinateur exécutant le service Web d’administration des applications-V, configurez le fichier texte UDL (Universal Data Link).</span><span class="sxs-lookup"><span data-stu-id="21996-132">On the computer that is running the App-V Management Web Service, configure the Universal Data Link (UDL) text file.</span></span> <span data-ttu-id="21996-133">Dans le répertoire d’installation de l’application-V, double-cliquez sur **SftMgmt. UDL** et spécifiez les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="21996-133">In the directory where App-V is installed, double-click **SftMgmt.udl** and specify the following values:</span></span>

    -   <span data-ttu-id="21996-134">Dans l’onglet **fournisseur** , sélectionnez le fournisseur OLE DB fournisseur **SQL Server Native Client 10,0**.</span><span class="sxs-lookup"><span data-stu-id="21996-134">On the **Provider** tab, select the OLE DB provider **SQL Server Native Client 10.0**.</span></span>

    -   <span data-ttu-id="21996-135">Cliquez sur **suivant** pour sélectionner l’onglet **connexion** . Dans la zone **nom du serveur** , entrez le nom du serveur SQL Server.</span><span class="sxs-lookup"><span data-stu-id="21996-135">Click **Next** to select the **Connection** tab. In the **Server Name** box, enter the server name of the SQL Server.</span></span> <span data-ttu-id="21996-136">Ensuite, activez la case à cocher **utiliser la sécurité intégrée à Windows NT**.</span><span class="sxs-lookup"><span data-stu-id="21996-136">Next, select **Use Windows NT Integrated Security**.</span></span> <span data-ttu-id="21996-137">Pour finir, cliquez sur la liste, **Sélectionnez la base de données**, puis sélectionnez le nom de la base de données App-V.</span><span class="sxs-lookup"><span data-stu-id="21996-137">Finally, click the list **Select the database**, and then select the App-V database name.</span></span>

    -   <span data-ttu-id="21996-138">Cliquez sur l’onglet **toutes** , puis sélectionnez le **partenaire entrée Failover**.</span><span class="sxs-lookup"><span data-stu-id="21996-138">Click the **All** tab, and then select the entry **Failover Partner**.</span></span> <span data-ttu-id="21996-139">Cliquez sur **modifier la valeur**, puis entrez le nom de serveur du serveur SQL de basculement.</span><span class="sxs-lookup"><span data-stu-id="21996-139">Click **Edit Value**, and then enter the server name of the failover SQL Server.</span></span> <span data-ttu-id="21996-140">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="21996-140">Click **OK**.</span></span>

    **<span data-ttu-id="21996-141">Important</span><span class="sxs-lookup"><span data-stu-id="21996-141">Important</span></span>**  
    <span data-ttu-id="21996-142">Le système App-V utilise l’authentification Kerberos.</span><span class="sxs-lookup"><span data-stu-id="21996-142">The App-V system uses Kerberos authentication.</span></span> <span data-ttu-id="21996-143">Par conséquent, lorsque vous configurez la mise en miroir SQL où l’authentification Kerberos est activée sur le serveur SQL Server et que le service SQL Server s’exécute sous un compte d’utilisateur de domaine, vous devez configurer manuellement un SPN.</span><span class="sxs-lookup"><span data-stu-id="21996-143">Therefore, when you configure SQL mirroring where Kerberos Authentication is enabled on the SQL Server and the SQL Server service runs under a domain user account, you must manually configure an SPN.</span></span> <span data-ttu-id="21996-144">Pour plus d’informations, consultez la section «lorsque le service SQL utilise un compte basé sur le domaine» dans l’article [configuration de l’administration d’App-V pour un environnement distribué](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .</span><span class="sxs-lookup"><span data-stu-id="21996-144">For more information, see “When SQL Service Uses Domain-Based Account” in the article [Configuring App-V Administration for a Distributed Environment](https://go.microsoft.com/fwlink/?LinkId=203186) (https://go.microsoft.com/fwlink/?LinkId=203186).</span></span>



10. <span data-ttu-id="21996-145">Pour vérifier que la mise en miroir de la base de données fonctionne correctement, testez le basculement et confirmez que le serveur de gestion de l’application-V continue de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="21996-145">To verify that database mirroring is running correctly, test the failover and confirm that the App-V Management Server continues to function correctly.</span></span>

    **<span data-ttu-id="21996-146">Important</span><span class="sxs-lookup"><span data-stu-id="21996-146">Important</span></span>**  
    <span data-ttu-id="21996-147">Procédez comme suit, puis suivez les recommandations standard de votre entreprise pour vous assurer que les opérations système ne sont pas interrompues en cas de panne.</span><span class="sxs-lookup"><span data-stu-id="21996-147">Proceed with care, and follow your standard business practices to ensure that system operations are not disrupted in the event of a failure.</span></span>



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## <span data-ttu-id="21996-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="21996-148">Related topics</span></span>


[<span data-ttu-id="21996-149">Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console</span><span class="sxs-lookup"><span data-stu-id="21996-149">How to Perform Administrative Tasks in the Application Virtualization Server Management Console</span></span>](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









