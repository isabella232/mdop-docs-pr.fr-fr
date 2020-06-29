---
title: Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation
description: Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation
author: dansimp
ms.assetid: d8d11588-17c0-4bcb-a7e6-86b5e4ba7e1c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7164b3046671853216b870d68e651fed4fd84695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807230"
---
# <span data-ttu-id="32ead-103">Procédure pour configurer le serveur afin qu'il soit approuvé pour délégation</span><span class="sxs-lookup"><span data-stu-id="32ead-103">How to Configure the Server to be Trusted for Delegation</span></span>


<span data-ttu-id="32ead-104">Lorsque vous installez le logiciel serveur de gestion Microsoft Application Virtualization (App-V), vous pouvez choisir de l’installer à l’aide d’une architecture système distribuée.</span><span class="sxs-lookup"><span data-stu-id="32ead-104">When you install the Microsoft Application Virtualization (App-V) Management Server software, you can choose to install it by using a distributed system architecture.</span></span> <span data-ttu-id="32ead-105">Si vous installez la console, le service Web de gestion et la base de données sur des ordinateurs différents, vous devez configurer le serveur Internet Information Services (IIS) pour qu’il soit approuvé pour la délégation.</span><span class="sxs-lookup"><span data-stu-id="32ead-105">If you install the console, the Management Web Service, and the database on different computers, you must configure the Internet Information Services (IIS) server to be trusted for delegation.</span></span> <span data-ttu-id="32ead-106">Cela est nécessaire, car le service Web de gestion tente de se connecter au magasin de données App-V en utilisant les informations d’identification de l’administrateur d’application-V qui utilise la console.</span><span class="sxs-lookup"><span data-stu-id="32ead-106">This is necessary because the Management Web Service will attempt to connect to the App-V data store by using the credentials of the App-V administrator who is using the console.</span></span> <span data-ttu-id="32ead-107">Le serveur de base de données sur lequel est installé le magasin de données n’accepte pas les informations d’identification de l’administrateur du serveur IIS, sauf si le serveur IIS est configuré pour être approuvé pour la délégation, et le service Web de gestion ne sera pas en mesure de se connecter au magasin de données App-V.</span><span class="sxs-lookup"><span data-stu-id="32ead-107">The database server on which the data store is installed will not accept the administrator’s credentials from the IIS server unless the IIS server is configured to be trusted for delegation, and so the Management Web Service will not be able to connect to the App-V data store.</span></span>

<span data-ttu-id="32ead-108">**Remarques**  Si vous installez le logiciel serveur d’administration des applications sur un serveur unique et placez le magasin de données sur un serveur distinct, il existe une situation dans laquelle vous devez tout de même configurer le serveur pour qu’il soit approuvé pour la délégation, même si le service Web de gestion et la console de gestion se trouvent sur le même serveur.</span><span class="sxs-lookup"><span data-stu-id="32ead-108">**Note** If you install the App-V Management Server software on a single server and place the data store on a separate server, there is one situation in which you must still configure the server to be trusted for delegation even though the Management Web Service and Management Console are on the same server.</span></span> <span data-ttu-id="32ead-109">Cette situation se produit si vous devez vous connecter au service Web de gestion dans la console à l’aide de l’option **utiliser d’autres informations d’identification** .</span><span class="sxs-lookup"><span data-stu-id="32ead-109">This situation occurs if you need to connect to the Management Web Service in the console by using the **Use Alternate Credentials** option.</span></span>

 

<span data-ttu-id="32ead-110">Le type de délégation que vous pouvez utiliser dépend du niveau de fonctionnement du domaine que vous avez configuré dans votre infrastructure services de domaine Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="32ead-110">The type of delegation that you can use depends on the Domain Functional Level that you have configured in your Active Directory Domain Services (ADDS) infrastructure.</span></span> <span data-ttu-id="32ead-111">Le tableau suivant répertorie les types de délégation qui peuvent être configurés pour chaque niveau fonctionnel de domaine pour App-V.</span><span class="sxs-lookup"><span data-stu-id="32ead-111">The following table lists the types of delegation that can be configured for each Domain Functional Level for App-V.</span></span> <span data-ttu-id="32ead-112">Les instructions détaillées suivent le tableau.</span><span class="sxs-lookup"><span data-stu-id="32ead-112">Detailed instructions follow the table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="32ead-113">Niveau fonctionnel du domaine</span><span class="sxs-lookup"><span data-stu-id="32ead-113">Domain Functional Level</span></span></th>
<th align="left"><span data-ttu-id="32ead-114">Niveaux de délégation disponibles</span><span class="sxs-lookup"><span data-stu-id="32ead-114">Delegation Levels Available</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="32ead-115">Windows 2000 natif</span><span class="sxs-lookup"><span data-stu-id="32ead-115">Windows 2000 native</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="32ead-116">Aucune délégation (par défaut)</span><span class="sxs-lookup"><span data-stu-id="32ead-116">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="32ead-117">Délégation sans contraintes</span><span class="sxs-lookup"><span data-stu-id="32ead-117">Unconstrained delegation</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="32ead-118">Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32ead-118">Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="32ead-119">Aucune délégation (par défaut)</span><span class="sxs-lookup"><span data-stu-id="32ead-119">No delegation (default)</span></span></p></li>
<li><p><span data-ttu-id="32ead-120">Délégation sans contraintes ¹</span><span class="sxs-lookup"><span data-stu-id="32ead-120">Unconstrained delegation¹</span></span></p></li>
<li><p><span data-ttu-id="32ead-121">Délégation contrainte (utiliser des protocoles Kerberos uniquement)</span><span class="sxs-lookup"><span data-stu-id="32ead-121">Constrained delegation (Use Kerberos Only Protocols)</span></span></p></li>
<li><p><span data-ttu-id="32ead-122">Délégation contrainte (utiliser n’importe quel protocole d’authentification) ¹</span><span class="sxs-lookup"><span data-stu-id="32ead-122">Constrained delegation (Use any authentication protocol) ¹</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="32ead-123">¹ non recommandée.</span><span class="sxs-lookup"><span data-stu-id="32ead-123">¹ Not recommended.</span></span>

## <span data-ttu-id="32ead-124">Pour configurer la délégation sans contraintes lorsque le niveau de fonctionnalité du domaine est Windows 2000 natif</span><span class="sxs-lookup"><span data-stu-id="32ead-124">To configure unconstrained delegation when the Domain Functional Level is Windows 2000 native</span></span>


<span data-ttu-id="32ead-125">Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="32ead-125">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="32ead-126">Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="32ead-126">Click **Start**, **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="32ead-127">Développez domaine, puis développez le dossier ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32ead-127">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="32ead-128">Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="32ead-128">In the right pane, right-click the computer name for the Web server, and then click **Properties**.</span></span>

4.  <span data-ttu-id="32ead-129">Dans l’onglet **général** , assurez-vous que la case à cocher **approuver l’ordinateur pour la délégation** est activée.</span><span class="sxs-lookup"><span data-stu-id="32ead-129">On the **General** tab, ensure that the **Trust computer for delegation** check box is selected.</span></span>

5.  <span data-ttu-id="32ead-130">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="32ead-130">Click **OK**.</span></span>

## <span data-ttu-id="32ead-131">Pour configurer la délégation sans contraintes lorsque le niveau de fonctionnalité du domaine est Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32ead-131">To configure unconstrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="32ead-132">Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="32ead-132">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="32ead-133">Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="32ead-133">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="32ead-134">Développez domaine, puis développez le dossier ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32ead-134">Expand domain, and expand the Computers folder.</span></span>

3.  <span data-ttu-id="32ead-135">Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, sélectionnez **Propriétés**, puis cliquez sur l’onglet **délégation** .</span><span class="sxs-lookup"><span data-stu-id="32ead-135">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="32ead-136">Cliquez pour sélectionner **approuver cet ordinateur pour la délégation à tout service (Kerberos uniquement)**.</span><span class="sxs-lookup"><span data-stu-id="32ead-136">Click to select **Trust this computer for delegation to any service (Kerberos only)**.</span></span>

5.  <span data-ttu-id="32ead-137">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="32ead-137">Click **OK**.</span></span>

## <span data-ttu-id="32ead-138">Pour configurer la délégation contrainte lorsque le niveau de fonctionnalité du domaine est Windows Server 2003, Windows Server 2008 ou Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="32ead-138">To configure constrained delegation when the Domain Functional Level is Windows Server 2003, Windows Server 2008, or Windows Server 2008 R2</span></span>


<span data-ttu-id="32ead-139">Sur le contrôleur de domaine du domaine de votre serveur Web, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="32ead-139">On the domain controller for your Web server’s domain, complete the following steps.</span></span>

****

1.  <span data-ttu-id="32ead-140">Cliquez sur **Démarrer**, sur **Outils d’administration**, puis sur **utilisateurs et ordinateurs Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="32ead-140">Click **Start**, click **Administrative Tools**, and then click **Active Directory Users and Computers**.</span></span>

2.  <span data-ttu-id="32ead-141">Développez domaine, puis développez le dossier ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="32ead-141">Expand domain, and then expand the Computers folder.</span></span>

3.  <span data-ttu-id="32ead-142">Dans le volet droit, cliquez avec le bouton droit sur le nom de l’ordinateur du serveur Web, sélectionnez **Propriétés**, puis cliquez sur l’onglet **délégation** .</span><span class="sxs-lookup"><span data-stu-id="32ead-142">In the right pane, right-click the computer name for the Web server, select **Properties**, and then click the **Delegation** tab.</span></span>

4.  <span data-ttu-id="32ead-143">Cliquez pour sélectionner **approuver cet ordinateur pour la délégation aux services spécifiés uniquement**.</span><span class="sxs-lookup"><span data-stu-id="32ead-143">Click to select **Trust this computer for delegation to specified services only**.</span></span>

5.  <span data-ttu-id="32ead-144">Vérifiez que l’option **utiliser le protocole Kerberos uniquement** est sélectionnée, puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="32ead-144">Ensure that **Use Kerberos only** is selected, and then click **OK**.</span></span>

6.  <span data-ttu-id="32ead-145">Cliquez sur le bouton **Ajouter** .</span><span class="sxs-lookup"><span data-stu-id="32ead-145">Click the **Add** button.</span></span> <span data-ttu-id="32ead-146">Dans la boîte de dialogue **Ajouter des services** , cliquez sur **utilisateurs ou ordinateurs**, puis recherchez ou tapez le nom de Microsoft SQL Server qui dispose du magasin de données App-V et recevez les informations d’identification de l’utilisateur à partir d’IIS.</span><span class="sxs-lookup"><span data-stu-id="32ead-146">In the **Add Services** dialog box, click **Users or Computers**, and then browse to or type the name of the Microsoft SQL server that has the App-V data store and is to receive the users credentials from IIS.</span></span> <span data-ttu-id="32ead-147">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="32ead-147">Click **OK**.</span></span>

7.  <span data-ttu-id="32ead-148">Dans la liste **services disponibles** , sélectionnez le service MSSQLSvc qui indique le numéro de port sur lequel Microsoft SQL Server accepte les connexions pour la base de données App-V (le port par défaut est 1433).</span><span class="sxs-lookup"><span data-stu-id="32ead-148">In the **Available Services** list, select the MSSQLSvc service that lists port number on which the Microsoft SQL Server is accepting connections for the App-V database (the default port is 1433).</span></span> <span data-ttu-id="32ead-149">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="32ead-149">Click **OK**.</span></span>

### <span data-ttu-id="32ead-150">Étapes supplémentaires pour configurer IIS 7 pour la délégation contrainte</span><span class="sxs-lookup"><span data-stu-id="32ead-150">Additional steps to configure IIS 7 for constrained delegation</span></span>

<span data-ttu-id="32ead-151">Si vous exécutez le service Web de gestion sur un serveur IIS 7, vous devez effectuer les étapes suivantes pour définir la variable *useAppPoolCredentials* de services Internet (IIS) sur true.</span><span class="sxs-lookup"><span data-stu-id="32ead-151">If you are running the Management Web Service on an IIS 7 server, you must complete the following steps to set the IIS 7 *useAppPoolCredentials* variable to True.</span></span>

1.  <span data-ttu-id="32ead-152">Ouvrez une fenêtre d’invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="32ead-152">Open an elevated Command Prompt window.</span></span> <span data-ttu-id="32ead-153">Pour ouvrir une fenêtre d’invite de commandes avec élévation de privilèges, cliquez sur **Démarrer**, sur **tous les programmes**, sur **accessoires**, cliquez avec le bouton droit sur **invite de commandes**, puis cliquez sur **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="32ead-153">To open an elevated Command Prompt window, click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="32ead-154">Accédez à%windir%\\system32\\inetsrv.</span><span class="sxs-lookup"><span data-stu-id="32ead-154">Navigate to %windir%\\system32\\inetsrv.</span></span>

3.  <span data-ttu-id="32ead-155">Tapez **appcmd.exe définir config-section: System. webServer/Security/Authentication/WindowsAuthentication-useAppPoolCredentials: true**, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="32ead-155">Type **appcmd.exe set config -section:system.webServer/security/authentication/windowsAuthentication -useAppPoolCredentials:true**, and then press ENTER.</span></span>

 

 





