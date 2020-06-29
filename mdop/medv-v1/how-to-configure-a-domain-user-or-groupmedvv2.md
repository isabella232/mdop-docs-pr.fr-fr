---
title: Comment configurer un utilisateur ou un groupe de domaine
description: Comment configurer un utilisateur ou un groupe de domaine
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812210"
---
# <span data-ttu-id="008f8-103">Comment configurer un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="008f8-103">How to Configure a Domain User or Group</span></span>


<span data-ttu-id="008f8-104">Les paramètres de déploiement vous permettent de contrôler les utilisateurs ou groupes qui peuvent accéder à l’espace de travail MED-V, ainsi que la durée de l’utilisation de l’espace de travail MED-V et la possibilité de les utiliser hors connexion.</span><span class="sxs-lookup"><span data-stu-id="008f8-104">The deployment settings enable you to control which users or groups can access the MED-V workspace, as well as how long the MED-V workspace can be utilized and whether it can be used offline.</span></span> <span data-ttu-id="008f8-105">Vous pouvez également configurer des règles supplémentaires pour contrôler l’accès entre l’espace de travail MED-V et l’hôte.</span><span class="sxs-lookup"><span data-stu-id="008f8-105">You can also configure additional rules to control access between the MED-V workspace and the host.</span></span>

<span data-ttu-id="008f8-106">Toutes les autorisations d’espace de travail MED-V sont configurées dans le module de **stratégie** sous l’onglet **déploiement** .</span><span class="sxs-lookup"><span data-stu-id="008f8-106">All MED-V workspace permissions are configured in the **Policy** module, on the **Deployment** tab.</span></span>

<span data-ttu-id="008f8-107">Pour permettre aux utilisateurs d’utiliser l’espace de travail MED-V, vous devez d’abord ajouter des utilisateurs ou groupes de domaine aux autorisations d’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-107">To allow users to utilize the MED-V workspace, you must first add domain users or groups to the MED-V workspace permissions.</span></span> <span data-ttu-id="008f8-108">Vous pouvez ensuite définir des autorisations pour chaque utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="008f8-108">You can then set permissions for each user or group.</span></span>

## <span data-ttu-id="008f8-109">Comment ajouter un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="008f8-109">How to Add a Domain User or Group</span></span>


**<span data-ttu-id="008f8-110">Pour ajouter un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="008f8-110">To add a domain user or group</span></span>**

1.  <span data-ttu-id="008f8-111">Dans la fenêtre **utilisateurs et groupes** , cliquez sur **Ajouter.**</span><span class="sxs-lookup"><span data-stu-id="008f8-111">In the **Users / Groups** window, click **Add.**</span></span>

2.  <span data-ttu-id="008f8-112">Dans la boîte de dialogue **entrer un nom d’utilisateur ou de groupe** , sélectionnez utilisateurs ou groupes de domaines en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="008f8-112">In the **Enter User or Group names** dialog box, select domain users or groups by doing one of the following:</span></span>

    -   <span data-ttu-id="008f8-113">Dans le champ **Entrez des noms d’utilisateur ou de groupe** , entrez un nom d’utilisateur ou de groupe qui existe dans le domaine ou en tant qu’utilisateur ou groupe local de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="008f8-113">In the **Enter User or Group names** field, type a user or group that exists in the domain or as a local user or group on the computer.</span></span> <span data-ttu-id="008f8-114">Puis cliquez sur **vérifier les noms** pour le résoudre au nom existant complet.</span><span class="sxs-lookup"><span data-stu-id="008f8-114">Then click **Check Names** to resolve it to the full existent name.</span></span>

    -   <span data-ttu-id="008f8-115">Cliquez sur **Rechercher** pour ouvrir la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** standard.</span><span class="sxs-lookup"><span data-stu-id="008f8-115">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="008f8-116">Sélectionnez ensuite utilisateurs ou groupes de domaines.</span><span class="sxs-lookup"><span data-stu-id="008f8-116">Then select domain users or groups.</span></span>

3.  <span data-ttu-id="008f8-117">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="008f8-117">Click **OK**.</span></span>

    <span data-ttu-id="008f8-118">Les utilisateurs ou groupes du domaine sont ajoutés.</span><span class="sxs-lookup"><span data-stu-id="008f8-118">The domain users or groups are added.</span></span>

    **<span data-ttu-id="008f8-119">Remarque</span><span class="sxs-lookup"><span data-stu-id="008f8-119">Note</span></span>**  
    <span data-ttu-id="008f8-120">Les utilisateurs des domaines approuvés doivent être ajoutés manuellement.</span><span class="sxs-lookup"><span data-stu-id="008f8-120">Users from trusted domains should be added manually.</span></span>



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## <span data-ttu-id="008f8-121">Supprimer un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="008f8-121">How to Remove a Domain User or Group</span></span>


**<span data-ttu-id="008f8-122">Pour supprimer un utilisateur ou un groupe de domaine</span><span class="sxs-lookup"><span data-stu-id="008f8-122">To remove a domain user or group</span></span>**

1.  <span data-ttu-id="008f8-123">Dans la fenêtre **utilisateurs/groupes** , sélectionnez un utilisateur ou un groupe.</span><span class="sxs-lookup"><span data-stu-id="008f8-123">In the **Users / Groups** window, select a user or group.</span></span>

2.  <span data-ttu-id="008f8-124">Cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="008f8-124">Click **Remove**.</span></span>

    <span data-ttu-id="008f8-125">L’utilisateur ou le groupe est supprimé.</span><span class="sxs-lookup"><span data-stu-id="008f8-125">The user or group is deleted.</span></span>

## <span data-ttu-id="008f8-126">Définir des autorisations pour un utilisateur ou un groupe</span><span class="sxs-lookup"><span data-stu-id="008f8-126">How to Set Permissions for a User or a Group</span></span>


**<span data-ttu-id="008f8-127">Pour définir des autorisations pour un utilisateur ou un groupe</span><span class="sxs-lookup"><span data-stu-id="008f8-127">To set permissions for a user or a group</span></span>**

1.  <span data-ttu-id="008f8-128">Cliquez sur l’utilisateur ou le groupe pour lequel vous définissez les autorisations.</span><span class="sxs-lookup"><span data-stu-id="008f8-128">Click the user or group for which you are setting the permissions.</span></span>

2.  <span data-ttu-id="008f8-129">Configurez les propriétés de l’espace de travail MED-V comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="008f8-129">Configure the MED-V workspace properties as described in the following table.</span></span>

3.  <span data-ttu-id="008f8-130">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="008f8-130">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="008f8-131">Propriétés de déploiement d’espace de travail</span><span class="sxs-lookup"><span data-stu-id="008f8-131">Workspace Deployment Properties</span></span>**

<span data-ttu-id="008f8-132">Description de propriété *générale*</span><span class="sxs-lookup"><span data-stu-id="008f8-132">Property Description *General*</span></span>

<span data-ttu-id="008f8-133">Activer un espace de travail pour un &lt; utilisateur ou un groupe&gt;</span><span class="sxs-lookup"><span data-stu-id="008f8-133">Enable Workspace for &lt;user or group&gt;</span></span>

<span data-ttu-id="008f8-134">Activez cette case à cocher pour activer l’espace de travail MED-V pour cet utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="008f8-134">Select this check box to enable the MED-V workspace for this user or group.</span></span>

<span data-ttu-id="008f8-135">Espace de travail expire à cette date</span><span class="sxs-lookup"><span data-stu-id="008f8-135">Workspace expires on this date</span></span>

<span data-ttu-id="008f8-136">Activez cette case à cocher pour affecter une date d’expiration aux autorisations définies pour cet utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="008f8-136">Select this check box to assign an expiration date for the permissions set for this user or group.</span></span>

<span data-ttu-id="008f8-137">Lorsque vous sélectionnez cette option, la zone de date est activée.</span><span class="sxs-lookup"><span data-stu-id="008f8-137">When selected, the date box is enabled.</span></span> <span data-ttu-id="008f8-138">Définissez la date et l’autorisation expire à la fin de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="008f8-138">Set the date, and permissions will expire at the end of the date specified.</span></span>

<span data-ttu-id="008f8-139">Le fonctionnement hors connexion est limité à</span><span class="sxs-lookup"><span data-stu-id="008f8-139">Offline work is restricted to</span></span>

<span data-ttu-id="008f8-140">Activez cette case à cocher pour attribuer une période pendant laquelle la stratégie doit être actualisée pour cet utilisateur ou groupe.</span><span class="sxs-lookup"><span data-stu-id="008f8-140">Select this check box to assign a time period in which the policy must be refreshed for this user or group.</span></span> <span data-ttu-id="008f8-141">Lorsque cette case est cochée, la case période est activée.</span><span class="sxs-lookup"><span data-stu-id="008f8-141">When selected, the time period box is enabled.</span></span> <span data-ttu-id="008f8-142">Définir le nombre de jours ou d’heures et à la fin de la période spécifiée, le groupe ou l’utilisateur ne peut pas se connecter si la stratégie n’est pas actualisée.</span><span class="sxs-lookup"><span data-stu-id="008f8-142">Set the number of days or hours, and at the end of the specified time period, the user or group will not be able to connect if the policy is not refreshed.</span></span>

<span data-ttu-id="008f8-143">Options de suppression d’espace de travail</span><span class="sxs-lookup"><span data-stu-id="008f8-143">Workspace deletion options</span></span>

<span data-ttu-id="008f8-144">Cliquez pour définir les options de suppression d’espace de travail de MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-144">Click to set the MED-V workspace deletion options.</span></span> <span data-ttu-id="008f8-145">Pour plus d’informations, reportez-vous [à définition des options de suppression d’espace de travail MED-V](how-to-set-med-v-workspace-deletion-options.md).</span><span class="sxs-lookup"><span data-stu-id="008f8-145">For more information, see [How to Set MED-V Workspace Deletion Options](how-to-set-med-v-workspace-deletion-options.md).</span></span>

*<span data-ttu-id="008f8-146">Transfert de données</span><span class="sxs-lookup"><span data-stu-id="008f8-146">Data Transfer</span></span>*

<span data-ttu-id="008f8-147">Support du presse-papiers entre l’hôte et l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="008f8-147">Support clipboard between host and Workspace</span></span>

<span data-ttu-id="008f8-148">Activez cette case à cocher pour autoriser les opérations de copie et de collage entre l’hôte et l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-148">Select this check box to enable copying and pasting between the host and the MED-V workspace.</span></span>

<span data-ttu-id="008f8-149">Prise en charge du transfert de fichiers entre l’hôte et l’espace de travail</span><span class="sxs-lookup"><span data-stu-id="008f8-149">Support file transfer between the host and Workspace</span></span>

<span data-ttu-id="008f8-150">Activez cette case à cocher pour autoriser le transfert de fichiers entre les espaces de travail hôte et MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-150">Select this check box to enable transferring files between the host and MED-V workspace.</span></span> <span data-ttu-id="008f8-151">Sélectionnez l’une des options suivantes dans la boîte de **transfert de fichiers** :</span><span class="sxs-lookup"><span data-stu-id="008f8-151">Select one of the following options from the **File Transfer** box:</span></span>

-   <span data-ttu-id="008f8-152">**Both**: permet de transférer des fichiers entre l’hôte et l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-152">**Both**—Enable transferring files between the host and the MED-V workspace.</span></span>

-   <span data-ttu-id="008f8-153">**Hébergé sur un espace de travail**: permet de transférer des fichiers à partir de l’hôte vers l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-153">**Host to Workspace**—Enable transferring files from the host to the MED-V workspace.</span></span>

-   <span data-ttu-id="008f8-154">**Espace de travail à hôte**: permet de transférer des fichiers à partir de l’espace de travail MED-V vers l’hôte.</span><span class="sxs-lookup"><span data-stu-id="008f8-154">**Workspace to Host**—Enable transferring files from the MED-V workspace to the host.</span></span>

**<span data-ttu-id="008f8-155">Remarque</span><span class="sxs-lookup"><span data-stu-id="008f8-155">Note</span></span>**  
<span data-ttu-id="008f8-156">Si un utilisateur sans autorisation tente de transférer des fichiers, une fenêtre s’affiche et vous invite à entrer les informations d’identification d’un utilisateur disposant des autorisations pour effectuer le transfert de fichier.</span><span class="sxs-lookup"><span data-stu-id="008f8-156">If a user without permissions attempts to transfer files, a window will appear prompting him to enter the credentials of a user with permissions to perform the file transfer.</span></span>



**<span data-ttu-id="008f8-157">Important</span><span class="sxs-lookup"><span data-stu-id="008f8-157">Important</span></span>**  
<span data-ttu-id="008f8-158">Pour prendre en charge le transfert de fichiers dans Windows XP SP3, vous devez désactiver la synchronisation des fichiers hors connexion en modifiant le registre comme suit:</span><span class="sxs-lookup"><span data-stu-id="008f8-158">To support file transfer in Windows XP SP3, you must disable offline file synchronization by editing the registry as follows:</span></span>

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



<span data-ttu-id="008f8-159">Avancé</span><span class="sxs-lookup"><span data-stu-id="008f8-159">Advanced</span></span>

<span data-ttu-id="008f8-160">Cliquez pour définir les options de transfert de fichier avancées.</span><span class="sxs-lookup"><span data-stu-id="008f8-160">Click to set the advanced file transfer options.</span></span> <span data-ttu-id="008f8-161">Pour plus d’informations, reportez-vous [à la rubrique définition des options de transfert de fichiers avancées](how-to-set-advanced-file-transfer-options.md).</span><span class="sxs-lookup"><span data-stu-id="008f8-161">For more information, see [How to Set Advanced File Transfer Options](how-to-set-advanced-file-transfer-options.md).</span></span>

*<span data-ttu-id="008f8-162">Contrôle de l’appareil</span><span class="sxs-lookup"><span data-stu-id="008f8-162">Device Control</span></span>*

<span data-ttu-id="008f8-163">Activer l’impression sur les imprimantes connectées à l’hôte</span><span class="sxs-lookup"><span data-stu-id="008f8-163">Enable printing to printers connected to the host</span></span>

<span data-ttu-id="008f8-164">Activez cette case à cocher pour permettre aux utilisateurs d’imprimer à partir de l’espace de travail MED-V à l’aide de l’imprimante hôte.</span><span class="sxs-lookup"><span data-stu-id="008f8-164">Select this check box to enable users to print from the MED-V workspace using the host printer.</span></span>

**<span data-ttu-id="008f8-165">Remarque</span><span class="sxs-lookup"><span data-stu-id="008f8-165">Note</span></span>**  
<span data-ttu-id="008f8-166">L’impression est effectuée par les imprimantes définies sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="008f8-166">The printing is performed by the printers defined on the host.</span></span>



<span data-ttu-id="008f8-167">Activer l’accès au CD/DVD</span><span class="sxs-lookup"><span data-stu-id="008f8-167">Enable access to CD / DVD</span></span>

<span data-ttu-id="008f8-168">Activez cette case à cocher pour autoriser l’accès à un CD ou un DVD à partir de cet espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="008f8-168">Select this check box to allow access to a CD or DVD drive from this MED-V workspace.</span></span>



**<span data-ttu-id="008f8-169">Appartenances multiples</span><span class="sxs-lookup"><span data-stu-id="008f8-169">Multiple Memberships</span></span>**

1.  <span data-ttu-id="008f8-170">Si l’utilisateur fait partie d’un groupe et les autorisations sont appliquées à l’utilisateur ainsi qu’au groupe auquel il fait partie, toutes les autorisations sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="008f8-170">If the user is part of a group and permissions are applied to the user as well as to the group they are part of, all permissions are applied.</span></span>

2.  <span data-ttu-id="008f8-171">Si l’utilisateur est membre de deux groupes différents, les autorisations les moins restrictives sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="008f8-171">If the user is a member of two different groups, the least restrictive permissions are applied.</span></span>

## <span data-ttu-id="008f8-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="008f8-172">Related topics</span></span>


[<span data-ttu-id="008f8-173">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="008f8-173">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="008f8-174">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="008f8-174">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="008f8-175">Comment définir les options de suppression d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="008f8-175">How to Set MED-V Workspace Deletion Options</span></span>](how-to-set-med-v-workspace-deletion-options.md)

[<span data-ttu-id="008f8-176">Comment définir les options de transfert de fichiers avancées</span><span class="sxs-lookup"><span data-stu-id="008f8-176">How to Set Advanced File Transfer Options</span></span>](how-to-set-advanced-file-transfer-options.md)









