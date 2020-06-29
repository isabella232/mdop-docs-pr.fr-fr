---
title: Comment configurer les paramètres Web pour un espace de travail MED-V
description: Comment configurer les paramètres Web pour un espace de travail MED-V
author: dansimp
ms.assetid: 9a6cd28f-7e4f-468f-830a-7b1d9abd3af3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 770d3fa9a03c9754db86ca348390d0b916de6d5d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812132"
---
# <span data-ttu-id="9a171-103">Comment configurer les paramètres Web pour un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-103">How to Configure Web Settings for a MED-V Workspace</span></span>


<span data-ttu-id="9a171-104">Les sites Web qui peuvent être affichés uniquement dans les versions antérieures d’Internet Explorer et qui n’existent pas dans le système d’exploitation hôte peuvent être affichés dans les versions antérieures d’Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a171-104">Web sites that can only be displayed in older versions of Internet Explorer and that do not exist in the host operating system can be viewed in older versions of Internet Explorer within the MED-V workspace.</span></span> <span data-ttu-id="9a171-105">L’utilisateur n’a pas besoin d’ouvrir un navigateur dans l’espace de travail MED-V pour afficher les sites Web spécifiés.</span><span class="sxs-lookup"><span data-stu-id="9a171-105">The user does not need to open a browser in the MED-V workspace to view the specified Web sites.</span></span> <span data-ttu-id="9a171-106">L’utilisateur peut ouvrir un navigateur sur l’hôte et être automatiquement redirigé vers l’espace de travail MED-V et vice versa.</span><span class="sxs-lookup"><span data-stu-id="9a171-106">The user can open a browser on the host and automatically be redirected to the MED-V workspace and vice versa.</span></span>

<span data-ttu-id="9a171-107">Les procédures suivantes vous expliquent comment créer une liste de règles de navigation Web pour un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a171-107">The following procedures describe how you can set a list of Web browsing rules for a MED-V workspace.</span></span> <span data-ttu-id="9a171-108">Tous les sites inclus dans les règles peuvent être parcourus dans l’espace de travail MED-V ou sur l’hôte, tel qu’il est défini par l’administrateur.</span><span class="sxs-lookup"><span data-stu-id="9a171-108">All sites included in the rules can be browsed either in the MED-V workspace or on the host, as defined by the administrator.</span></span> <span data-ttu-id="9a171-109">Tous les sites non définis dans les règles sont parcourus à partir de l’environnement dans lequel ils ont été demandés.</span><span class="sxs-lookup"><span data-stu-id="9a171-109">All sites not defined within the rules are browsed from the environment in which they were requested.</span></span> <span data-ttu-id="9a171-110">Toutefois, vous pouvez également les configurer en tant que groupe, à parcourir dans l’espace de travail MED-V ou l’hôte.</span><span class="sxs-lookup"><span data-stu-id="9a171-110">However, you can configure them as a group as well, to be browsed in the MED-V workspace or the host.</span></span>

**<span data-ttu-id="9a171-111">Remarque</span><span class="sxs-lookup"><span data-stu-id="9a171-111">Note</span></span>**  
<span data-ttu-id="9a171-112">Les paramètres Web s’appliquent uniquement à Internet Explorer et à aucun autre navigateur.</span><span class="sxs-lookup"><span data-stu-id="9a171-112">Web settings are applied only to Internet Explorer and to no other browsers.</span></span>



<span data-ttu-id="9a171-113">Tous les paramètres Web sont configurés dans le module de **stratégie** sous l’onglet **Web** .</span><span class="sxs-lookup"><span data-stu-id="9a171-113">All Web settings are configured in the **Policy** module, on the **Web** tab.</span></span>

## <span data-ttu-id="9a171-114">Comment configurer les paramètres Web pour l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-114">How to Configure Web Settings for the MED-V Workspace</span></span>


**<span data-ttu-id="9a171-115">Pour configurer les paramètres Web pour l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-115">To configure Web settings for the MED-V workspace</span></span>**

1.  <span data-ttu-id="9a171-116">Cliquez sur l’espace de travail MED-V à configurer.</span><span class="sxs-lookup"><span data-stu-id="9a171-116">Click the MED-V workspace to be configured.</span></span>

2.  <span data-ttu-id="9a171-117">Activez la case à cocher **Parcourir la liste des URL définies dans le tableau ci-dessous** pour rediriger l’utilisateur vers un navigateur au sein de l’espace de travail ou de l’hôte MED-V, lorsque l’utilisateur navigue vers une URL qui est conforme aux règles Web spécifiées.</span><span class="sxs-lookup"><span data-stu-id="9a171-117">Select the **Browse the list of URLs defined in the following table** check box to redirect the user to a browser within the MED-V workspace or host, when the user browses to a URL that conforms to the Web rules specified.</span></span>

3.  <span data-ttu-id="9a171-118">Cliquez sur l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="9a171-118">Click one of the following:</span></span>

    -   <span data-ttu-id="9a171-119">**Dans l’espace de travail**, redirigez vers un navigateur dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a171-119">**In the Workspace**—Redirect to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="9a171-120">**Dans l’hôte**, redirigez vers un navigateur sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="9a171-120">**In the host**—Redirect to a browser on the host.</span></span>

4.  <span data-ttu-id="9a171-121">Cochez la case **Parcourir toutes les autres URL** pour rediriger toutes les URL exclues des règles Web vers l’espace de travail hôte ou MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a171-121">Select the **Browse all other URLs** check box to redirect all URLs excluded from the Web rules to the host or MED-V workspace.</span></span>

5.  <span data-ttu-id="9a171-122">Cliquez sur l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="9a171-122">Click one of the following:</span></span>

    -   <span data-ttu-id="9a171-123">**Dans l’espace de travail**, redirigez toutes les autres URL vers un navigateur dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="9a171-123">**In the Workspace**—Redirect all other URLs to a browser in the MED-V workspace.</span></span>

    -   <span data-ttu-id="9a171-124">**Dans l’hôte**, redirigez toutes les autres URL vers un navigateur sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="9a171-124">**In the host**—Redirect all other URLs to a browser on the host.</span></span>

6.  <span data-ttu-id="9a171-125">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="9a171-125">On the **Policy** menu, select **Commit**.</span></span>

## <span data-ttu-id="9a171-126">Comment ajouter une règle Web</span><span class="sxs-lookup"><span data-stu-id="9a171-126">How to Add a Web Rule</span></span>


**<span data-ttu-id="9a171-127">Pour ajouter une règle Web</span><span class="sxs-lookup"><span data-stu-id="9a171-127">To add a Web rule</span></span>**

1.  <span data-ttu-id="9a171-128">Activez la case à cocher **Parcourir la liste des URL définies dans le tableau ci-dessous** pour activer les règles de navigation Web.</span><span class="sxs-lookup"><span data-stu-id="9a171-128">Select the **Browse the list of URLs defined in the following table** check box to enable the Web browsing rules.</span></span>

2.  <span data-ttu-id="9a171-129">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="9a171-129">Click **Add**.</span></span>

    <span data-ttu-id="9a171-130">Une nouvelle règle Web est ajoutée.</span><span class="sxs-lookup"><span data-stu-id="9a171-130">A new Web rule is added.</span></span>

3.  <span data-ttu-id="9a171-131">Configurez les propriétés de la règle Web comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9a171-131">Configure the Web rule properties as described in the following table.</span></span>

4.  <span data-ttu-id="9a171-132">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="9a171-132">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="9a171-133">Propriétés Web de l’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-133">MED-V Workspace Web Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="9a171-134">Propriété</span><span class="sxs-lookup"><span data-stu-id="9a171-134">Property</span></span></th>
<th align="left"><span data-ttu-id="9a171-135">Description</span><span class="sxs-lookup"><span data-stu-id="9a171-135">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="9a171-136">Type</span><span class="sxs-lookup"><span data-stu-id="9a171-136">Type</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="9a171-137">Suffixe </strong> de domaine: accès à n’importe quelle adresse d’hôte se terminant par le suffixe spécifié dans la <strong> </strong> propriété Value et est défini en fonction de l’option définie dans navigation sur le <strong> Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="9a171-137">Domain suffix</strong>—Access to any host address ending with the suffix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="9a171-138">Préfixe IP </strong> : accès à toute adresse IP complète ou partielle dans la plage du préfixe spécifiée dans <strong> la </strong> propriété Value et définie en fonction de l’option définie dans navigation sur le <strong> Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="9a171-138">IP Prefix</strong>—Access to any full or partial IP address in the range of the prefix specified in the <strong>Value</strong> property and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
<li><p><strong><span data-ttu-id="9a171-139">Toutes les adresses locales </strong> : l’accès à toutes les adresses sans &#39;. &#39; et est défini d’après l’option définie dans navigation sur le <strong> Web </strong> .</span><span class="sxs-lookup"><span data-stu-id="9a171-139">All Local Addresses</strong>—Access to all addresses without a &#39;.&#39; and is set according to the option set in <strong>Web Browsing</strong>.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="9a171-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a171-140">Value</span></span></p></td>
<td align="left"><ul>
<li><p><span data-ttu-id="9a171-141">Si <strong> </strong> l’option suffixe de domaine est sélectionnée dans la <strong> </strong> propriété type, entrez un suffixe de domaine.</span><span class="sxs-lookup"><span data-stu-id="9a171-141">If <strong>Domain suffix</strong> is selected in the <strong>Type</strong> property, enter a domain suffix.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="9a171-142">Remarque</span><span class="sxs-lookup"><span data-stu-id="9a171-142">Note</span></span></strong><br/><ul>
<li><p><span data-ttu-id="9a171-143">Ne pas entrer &quot; \* &quot; avant le suffixe.</span><span class="sxs-lookup"><span data-stu-id="9a171-143">Do not enter &quot;\*&quot; before the suffix.</span></span></p></li>
<li><p><span data-ttu-id="9a171-144">Les suffixes de domaine prennent également en charge les alias.</span><span class="sxs-lookup"><span data-stu-id="9a171-144">Domain suffixes support aliases as well.</span></span></p></li>
</ul>
</div>
<div>

</div></li>
<li><p><span data-ttu-id="9a171-145">Si l’option préfixe IP est sélectionnée dans la <strong> </strong> propriété type, entrez une adresse IP complète ou partielle.</span><span class="sxs-lookup"><span data-stu-id="9a171-145">If IP Prefix is selected in the <strong>Type</strong> property, enter a full or partial IP address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>



## <span data-ttu-id="9a171-146">Comment supprimer une règle Web</span><span class="sxs-lookup"><span data-stu-id="9a171-146">How to Delete a Web Rule</span></span>


**<span data-ttu-id="9a171-147">Pour supprimer une règle Web</span><span class="sxs-lookup"><span data-stu-id="9a171-147">To delete a Web rule</span></span>**

1.  <span data-ttu-id="9a171-148">Dans le volet **Web** , sélectionnez la règle Web à supprimer.</span><span class="sxs-lookup"><span data-stu-id="9a171-148">In the **Web** pane, select the Web rule to delete.</span></span>

2.  <span data-ttu-id="9a171-149">Cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="9a171-149">Click **Remove**.</span></span>

    <span data-ttu-id="9a171-150">La règle Web est supprimée.</span><span class="sxs-lookup"><span data-stu-id="9a171-150">The Web rule is deleted.</span></span>

## <span data-ttu-id="9a171-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9a171-151">Related topics</span></span>


[<span data-ttu-id="9a171-152">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-152">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

[<span data-ttu-id="9a171-153">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="9a171-153">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)









