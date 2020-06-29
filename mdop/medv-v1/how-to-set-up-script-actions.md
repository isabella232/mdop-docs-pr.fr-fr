---
title: Comment configurer des actions de script
description: Comment configurer des actions de script
author: dansimp
ms.assetid: 367e28f1-d8c2-4845-a01b-2fff9128ccfd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bfa264be447a0a8560e4af16ccaadc2ec1db3f6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804189"
---
# <span data-ttu-id="69a60-103">Comment configurer des actions de script</span><span class="sxs-lookup"><span data-stu-id="69a60-103">How to Set Up Script Actions</span></span>


<span data-ttu-id="69a60-104">L’éditeur d’actions de script permet à l’administrateur de créer des actions à effectuer lors de l’installation de l’espace de travail MED-V, ainsi que de définir l’ordre dans lequel ils sont exécutés.</span><span class="sxs-lookup"><span data-stu-id="69a60-104">The script actions editor allows the administrator to create actions to be performed during MED-V workspace setup, as well as to define the order in which they are performed.</span></span>

<span data-ttu-id="69a60-105">La liste suivante répertorie les actions qui peuvent être ajoutées au script de configuration du domaine:</span><span class="sxs-lookup"><span data-stu-id="69a60-105">The following is a list of actions that can be added to the domain setup script:</span></span>

-   <span data-ttu-id="69a60-106">**Redémarrez Windows**, puis redémarrez Windows.</span><span class="sxs-lookup"><span data-stu-id="69a60-106">**Restart Windows**—Restart Windows.</span></span>

-   <span data-ttu-id="69a60-107">**Joindre le domaine**: Si vous rejoignez un domaine, incluez cette action et configurez le nom d’utilisateur, le mot de passe, le nom de domaine complet, le nom de domaine NetBIOS et l’unité d’organisation (facultatif).</span><span class="sxs-lookup"><span data-stu-id="69a60-107">**Join Domain**—If joining a domain, include this action and configure the user name, password, fully qualified domain name, NetBIOS domain name, and organization unit (optional).</span></span>

-   <span data-ttu-id="69a60-108">**Vérifier la connectivité**: configurer un serveur auquel se connecter et vérifier que l’espace de travail MED-V peut se connecter à une ressource réseau (par exemple, le serveur de domaine).</span><span class="sxs-lookup"><span data-stu-id="69a60-108">**Check Connectivity**—Configure a server to connect to and verify that the MED-V workspace can connect to a network resource (such as the domain server).</span></span>

-   <span data-ttu-id="69a60-109">**Ligne de commande**: configurez un script dans l’espace de travail MED-V et entrez une ligne de commande incluant le chemin d’accès du script et les arguments du script.</span><span class="sxs-lookup"><span data-stu-id="69a60-109">**Command Line**—Configure a script in the MED-V workspace, and enter a command line that includes the path of the script and the script arguments.</span></span>

-   <span data-ttu-id="69a60-110">**Renommer l’ordinateur**: renommez l’ordinateur virtuel en fonction des paramètres définis.</span><span class="sxs-lookup"><span data-stu-id="69a60-110">**Rename Computer**—Rename the virtual machine computer based on the defined settings.</span></span>

-   <span data-ttu-id="69a60-111">**Désactiver la connexion automatique**, désactivez la connexion automatique Windows.</span><span class="sxs-lookup"><span data-stu-id="69a60-111">**Disable Auto-Logon**—Disable Windows Auto-Logon.</span></span> <span data-ttu-id="69a60-112">Cette action doit être ajoutée à la fin des scripts qui ajoutent l’ordinateur au domaine.</span><span class="sxs-lookup"><span data-stu-id="69a60-112">This action should be added at the end of scripts that add the computer to the domain.</span></span>

## <a href="" id="how-to-set-up-script-actions-"></a><span data-ttu-id="69a60-113">Comment configurer des actions de script</span><span class="sxs-lookup"><span data-stu-id="69a60-113">How to Set Up Script Actions</span></span>


**<span data-ttu-id="69a60-114">Pour configurer les actions de script</span><span class="sxs-lookup"><span data-stu-id="69a60-114">To set up script actions</span></span>**

1.  <span data-ttu-id="69a60-115">Dans l’onglet Configuration de l' **ordinateur virtuel** , cliquez sur **éditeur de script**.</span><span class="sxs-lookup"><span data-stu-id="69a60-115">On the **VM Setup** tab, click **Script Editor**.</span></span>

2.  <span data-ttu-id="69a60-116">Dans la boîte de dialogue **actions de script** , cliquez sur **Ajouter**, puis dans le sous-menu, cliquez sur les actions de votre choix.</span><span class="sxs-lookup"><span data-stu-id="69a60-116">In the **Script Actions** dialog box, click **Add**, and on the submenu, click the desired actions.</span></span>

3.  <span data-ttu-id="69a60-117">Configurez les actions comme décrit dans les tableaux suivants.</span><span class="sxs-lookup"><span data-stu-id="69a60-117">Configure the actions as described in the following tables.</span></span>

    <span data-ttu-id="69a60-118">**Remarques** 
     L’attribution d’un nom à un **ordinateur** est configurée dans l’onglet Paramètres de la **machine virtuelle** . Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span><span class="sxs-lookup"><span data-stu-id="69a60-118">**Note**
**Rename Computer** is configured in the **VM Settings** tab. For more information, see [How to Configure VM Computer Name Pattern Properties](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).</span></span>

     

~~~
**Note**  
To rename a computer, Windows must be restarted. It is recommended to add a Restart Windows action following a Rename Computer action.
~~~



4. <span data-ttu-id="69a60-119">Définissez l’ordre des actions en sélectionnant une action, puis en cliquant sur **monter** ou **descendre**.</span><span class="sxs-lookup"><span data-stu-id="69a60-119">Set the order of the actions by selecting an action and clicking **Up** or **Down**.</span></span>

5. <span data-ttu-id="69a60-120">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="69a60-120">Click **OK**.</span></span>

**<span data-ttu-id="69a60-121">Remarque</span><span class="sxs-lookup"><span data-stu-id="69a60-121">Note</span></span>**  
<span data-ttu-id="69a60-122">Lorsque vous exécutez le script de domaine de jointure, l’utilisateur connecté à l’ordinateur virtuel de l’espace de travail MED-V doit disposer de droits d’administrateur local.</span><span class="sxs-lookup"><span data-stu-id="69a60-122">When running the Join Domain script, for the script to work, the user logged into the MED-V workspace virtual machine must have local administrator rights.</span></span>



**<span data-ttu-id="69a60-123">Remarque</span><span class="sxs-lookup"><span data-stu-id="69a60-123">Note</span></span>**  
<span data-ttu-id="69a60-124">Lorsque vous exécutez le script de désactivation de la connexion automatique, il est recommandé de désactiver le compte invité local utilisé pour l’ouverture de session automatique une fois la configuration initiale terminée.</span><span class="sxs-lookup"><span data-stu-id="69a60-124">When running the Disable Auto-Logon script, it is recommended to disable the local guest account used for the auto-logon once the initial setup is complete.</span></span>



### <a href="" id="bkmk-joindomainproperties"></a>

**<span data-ttu-id="69a60-125">Joindre les propriétés de domaine</span><span class="sxs-lookup"><span data-stu-id="69a60-125">Join Domain Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a60-126">Propriété</span><span class="sxs-lookup"><span data-stu-id="69a60-126">Property</span></span></th>
<th align="left"><span data-ttu-id="69a60-127">Description</span><span class="sxs-lookup"><span data-stu-id="69a60-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-128">Informations d’identification à utiliser lors de la connexion de l’ordinateur virtuel au domaine</span><span class="sxs-lookup"><span data-stu-id="69a60-128">Credentials to use when joining the VM to the domain</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-129">Sélectionnez l’une des informations d’identification suivantes à utiliser lors de la connexion de l’ordinateur virtuel au domaine:</span><span class="sxs-lookup"><span data-stu-id="69a60-129">Select one of the following credentials to use when joining the VM to the domain:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="69a60-130">Utilisez les informations d’identification MED-V </strong> (informations d’identification de l’utilisateur final).</span><span class="sxs-lookup"><span data-stu-id="69a60-130">Use MED-V credentials</strong>—The end-user credentials.</span></span></p></li>
<li><p><strong><span data-ttu-id="69a60-131">Utilisez les informations d’identification suivantes </strong> : les informations d’identification spécifiées; entrez un nom d’utilisateur et un mot de passe dans les champs correspondants.</span><span class="sxs-lookup"><span data-stu-id="69a60-131">Use the following credentials</strong>—The credentials specified; enter a user name and password in the corresponding fields.</span></span></p></li>
</ul>
<div class="alert">
<strong><span data-ttu-id="69a60-132">Remarque</span><span class="sxs-lookup"><span data-stu-id="69a60-132">Note</span></span></strong><br/><p><span data-ttu-id="69a60-133">Les informations d’identification que vous entrez sont visibles par tous les utilisateurs de l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="69a60-133">The credentials you enter are visible to all MED-V workspace users.</span></span> <span data-ttu-id="69a60-134">Il est déconseillé de fournir des informations d’identification d’administrateur de domaine.</span><span class="sxs-lookup"><span data-stu-id="69a60-134">It is not recommended to provide domain administrator credentials.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-135">Domaine à joindre</span><span class="sxs-lookup"><span data-stu-id="69a60-135">Domain to join</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-136">Sélectionnez l’un des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="69a60-136">Select one of the following:</span></span></p>
<ul>
<li><p><strong><span data-ttu-id="69a60-137">Utilisez le nom de domaine utilisé lors du démarrage de l’espace de travail </strong> , rejoignez le domaine entré par l’utilisateur final lors de la connexion au client MED-V.</span><span class="sxs-lookup"><span data-stu-id="69a60-137">Use the domain name utilized in starting the Workspace</strong>—Join the domain entered by the end user when logging into the MED-V client.</span></span></p>
<p><span data-ttu-id="69a60-138">Pour définir le mappage de NetBIOS sur les noms de domaine complets, cliquez sur <strong> table de mappage de domaine global </strong> .</span><span class="sxs-lookup"><span data-stu-id="69a60-138">To define the mapping from NetBIOS to fully qualified domain names, click <strong>Global domain mapping table</strong>.</span></span> <span data-ttu-id="69a60-139">Dans la table de mappage de domaine global, cliquez sur <strong> ajouter </strong> , entrez un <strong> nom de domaine NetBIOS </strong> et un <strong> nom de domaine complet </strong> , puis cliquez sur <strong> OK </strong> .</span><span class="sxs-lookup"><span data-stu-id="69a60-139">In the global domain mapping table, click <strong>Add</strong>, enter a <strong>NetBIOS domain name</strong> and a <strong>Fully qualified domain name</strong>, and click <strong>OK</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="69a60-140">Utiliser le nom de domaine suivant </strong> : Rejoignez le domaine spécifié; entrez un nom de domaine et un nom de domaine NetBIOS dans les champs correspondants.</span><span class="sxs-lookup"><span data-stu-id="69a60-140">Use the following domain name</strong>—Join the domain specified; enter a domain name and NetBIOS domain name in the corresponding fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-141">Unité d’organisation</span><span class="sxs-lookup"><span data-stu-id="69a60-141">Organization Unit</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-142">Une unité d’organisation (UO) pourra être spécifiée pour joindre l’ordinateur à une UO spécifique.</span><span class="sxs-lookup"><span data-stu-id="69a60-142">An organization unit (OU) may be specified to join the computer to a specific OU.</span></span> <span data-ttu-id="69a60-143">Le format doit suivre un nom distinctif d’unité d’organisation: UO = &lt; unité d’organisation &gt; , &lt; contrôleur &gt; de domaine (par exemple, UO = QATest, DC = il, DC = MED-V, DC = com).</span><span class="sxs-lookup"><span data-stu-id="69a60-143">The format must follow an OU distinguished name: OU=&lt;Organization Unit&gt;,&lt;Domain Controller&gt; (for example, OU=QATest, DC=il, DC=MED-V, DC=com).</span></span></p>
<div class="alert">
<strong><span data-ttu-id="69a60-144">Warning</span><span class="sxs-lookup"><span data-stu-id="69a60-144">Warning</span></span></strong><br/><p><span data-ttu-id="69a60-145">Une seule unité d’organisation de niveau est prise en charge, comme le montre l’exemple ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="69a60-145">Only a single level OU is supported as is shown in the example above.</span></span></p>
</div>
<div>
 
</div></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-checkconnectivityproperties"></a>

**<span data-ttu-id="69a60-146">Vérifier les propriétés de connectivité</span><span class="sxs-lookup"><span data-stu-id="69a60-146">Check Connectivity Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a60-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="69a60-147">Property</span></span></th>
<th align="left"><span data-ttu-id="69a60-148">Description</span><span class="sxs-lookup"><span data-stu-id="69a60-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-149">Adresse IP</span><span class="sxs-lookup"><span data-stu-id="69a60-149">IP Address</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-150">Adresse IP du serveur sur lequel vous vérifiez la connexion.</span><span class="sxs-lookup"><span data-stu-id="69a60-150">The IP Address of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-151">Port</span><span class="sxs-lookup"><span data-stu-id="69a60-151">Port</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-152">Port du serveur sur lequel vous vérifiez la connexion.</span><span class="sxs-lookup"><span data-stu-id="69a60-152">The port of the server that you are verifying connection to.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-153">Délai d’expiration dépassé</span><span class="sxs-lookup"><span data-stu-id="69a60-153">Timeout</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-154">Nombre de secondes d’attente avant le dépassement du délai d’une réponse.</span><span class="sxs-lookup"><span data-stu-id="69a60-154">The number of seconds to wait for a response before timing out.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a href="" id="bkmk-commandlineproperties"></a>

**<span data-ttu-id="69a60-155">Propriétés de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="69a60-155">Command-Line Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a60-156">Propriété</span><span class="sxs-lookup"><span data-stu-id="69a60-156">Property</span></span></th>
<th align="left"><span data-ttu-id="69a60-157">Description</span><span class="sxs-lookup"><span data-stu-id="69a60-157">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-158">Path</span><span class="sxs-lookup"><span data-stu-id="69a60-158">Path</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-159">Chemin d’accès de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="69a60-159">The path of the command line.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-160">Arguments</span><span class="sxs-lookup"><span data-stu-id="69a60-160">Arguments</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-161">Arguments de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="69a60-161">Command-line arguments.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-162">Attendre la fin</span><span class="sxs-lookup"><span data-stu-id="69a60-162">Wait for exit</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-163">Activez la case à cocher pour attendre un retour avant de poursuivre avec les actions de script.</span><span class="sxs-lookup"><span data-stu-id="69a60-163">Select the check box to wait for a return before continuing with the script actions.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-164">Erreur Échec</span><span class="sxs-lookup"><span data-stu-id="69a60-164">Fail on error</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-165">Activez cette case à cocher si le retour est différent de la valeur spécifiée.</span><span class="sxs-lookup"><span data-stu-id="69a60-165">Select this check box if the return is anything but the value specified.</span></span></p>
<p><span data-ttu-id="69a60-166">Entrez la valeur indiquant la réussite de la commande.</span><span class="sxs-lookup"><span data-stu-id="69a60-166">Enter the value that will indicate the command as a success.</span></span></p>
<p><span data-ttu-id="69a60-167">Par défaut: <strong> 0</span><span class="sxs-lookup"><span data-stu-id="69a60-167">Default: <strong>0</span></span></strong></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-168">Effectuer une seule fois</span><span class="sxs-lookup"><span data-stu-id="69a60-168">Perform only once</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-169">Activez cette case à cocher pour exécuter la ligne de commande une seule fois.</span><span class="sxs-lookup"><span data-stu-id="69a60-169">Select this check box to run the command line only once.</span></span> <span data-ttu-id="69a60-170">Si le script échoue ou est annulé, cette commande n’est pas réexécutée.</span><span class="sxs-lookup"><span data-stu-id="69a60-170">If the script fails or is canceled, this command will not be performed again.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-171">La ligne de commande suivante entraîne un redémarrage de Windows dans l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="69a60-171">This command line causes a restart of Windows in the Workspace</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-172">Activez cette case à cocher si la ligne de commande entraîne un redémarrage après achèvement.</span><span class="sxs-lookup"><span data-stu-id="69a60-172">Select this check box if the command line causes a restart after completion.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-173">Autoriser les interactions</span><span class="sxs-lookup"><span data-stu-id="69a60-173">Allow interaction</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-174">Activez cette case à cocher si la commande nécessite une interaction utilisateur.</span><span class="sxs-lookup"><span data-stu-id="69a60-174">Select this check box if the command will require user interaction.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-175">Message de progression</span><span class="sxs-lookup"><span data-stu-id="69a60-175">Progress message</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-176">Message à afficher à l’utilisateur lorsque la commande est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="69a60-176">Message to be displayed to the user while the command is running.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-177">Message d’échec</span><span class="sxs-lookup"><span data-stu-id="69a60-177">Failure message</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-178">Message à afficher à l’utilisateur en cas d’échec de la commande.</span><span class="sxs-lookup"><span data-stu-id="69a60-178">Message to be displayed to the user if the command fails.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="69a60-179">Lors de la configuration de l’action de ligne de commande, plusieurs variables peuvent être utilisées comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="69a60-179">When configuring the command-line action, several variables can be used as defined in the following table.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="69a60-180">Paramètre</span><span class="sxs-lookup"><span data-stu-id="69a60-180">Parameter</span></span></th>
<th align="left"><span data-ttu-id="69a60-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="69a60-181">Value</span></span></th>
<th align="left"><span data-ttu-id="69a60-182">Description</span><span class="sxs-lookup"><span data-stu-id="69a60-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-183">%MEDVUser%</span><span class="sxs-lookup"><span data-stu-id="69a60-183">%MEDVUser%</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-184">Nom d’utilisateur authentifié.</span><span class="sxs-lookup"><span data-stu-id="69a60-184">An authenticated user name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-185">Nom d’utilisateur authentifié MED-V.</span><span class="sxs-lookup"><span data-stu-id="69a60-185">MED-V authenticated user name.</span></span> <span data-ttu-id="69a60-186">Le nom d’utilisateur et le mot de passe peuvent être utilisés dans le script de configuration de l’ordinateur virtuel du domaine.</span><span class="sxs-lookup"><span data-stu-id="69a60-186">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-187">%MEDVPassword%</span><span class="sxs-lookup"><span data-stu-id="69a60-187">%MEDVPassword%</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-188">Un mot de passe authentifié.</span><span class="sxs-lookup"><span data-stu-id="69a60-188">An authenticated password.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-189">Mot de passe authentifié MED-V.</span><span class="sxs-lookup"><span data-stu-id="69a60-189">MED-V authenticated password.</span></span> <span data-ttu-id="69a60-190">Le nom d’utilisateur et le mot de passe peuvent être utilisés dans le script de configuration de l’ordinateur virtuel du domaine.</span><span class="sxs-lookup"><span data-stu-id="69a60-190">The user name and password can be used in the join domain VM setup script.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="69a60-191">%MEDVDomain%</span><span class="sxs-lookup"><span data-stu-id="69a60-191">%MEDVDomain%</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-192">Domaine configuré.</span><span class="sxs-lookup"><span data-stu-id="69a60-192">Configured domain.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-193">Domaine configuré dans l’authentification MED-V.</span><span class="sxs-lookup"><span data-stu-id="69a60-193">The domain configured in the MED-V authentication.</span></span> <span data-ttu-id="69a60-194">Il peut être utilisé sur le script de configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="69a60-194">It can be used on the VM setup script.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="69a60-195">%DesiredMachineName%</span><span class="sxs-lookup"><span data-stu-id="69a60-195">%DesiredMachineName%</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-196">Nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="69a60-196">Computer name.</span></span></p></td>
<td align="left"><p><span data-ttu-id="69a60-197">Nom d’ordinateur unique configuré dans l’application de gestion.</span><span class="sxs-lookup"><span data-stu-id="69a60-197">The unique computer name configured in the management application.</span></span> <span data-ttu-id="69a60-198">Il peut être utilisé dans le script de configuration de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="69a60-198">It can be used in the VM setup script.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="69a60-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="69a60-199">Related topics</span></span>


[<span data-ttu-id="69a60-200">Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="69a60-200">How to Configure the Virtual Machine Setup for a MED-V Workspace</span></span>](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[<span data-ttu-id="69a60-201">Comment configurer les propriétés du modèle de nom d'ordinateur virtuel</span><span class="sxs-lookup"><span data-stu-id="69a60-201">How to Configure VM Computer Name Pattern Properties</span></span>](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

 

 





