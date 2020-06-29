---
title: Authentification des utilisateurs MED-V
description: Authentification des utilisateurs MED-V
author: dansimp
ms.assetid: aaf96eb6-91d1-4f4d-9854-5fc73c7ae7ab
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 14c1e95a94f2da76b6b6c5ebd9d4cf14dcf839a7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810824"
---
# <span data-ttu-id="f5f29-103">Authentification des utilisateurs MED-V</span><span class="sxs-lookup"><span data-stu-id="f5f29-103">Authentication of MED-V End Users</span></span>


<span data-ttu-id="f5f29-104">L’authentification des utilisateurs finaux de Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 est un problème de sécurité important.</span><span class="sxs-lookup"><span data-stu-id="f5f29-104">The authentication of Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 end users is a very important security issue.</span></span> <span data-ttu-id="f5f29-105">Dans ce contexte, l’authentification consiste à vérifier l’identité de l’utilisateur final de MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5f29-105">In this context, authentication refers to verifying the identity of the MED-V end user.</span></span>

<span data-ttu-id="f5f29-106">La section suivante fournit des informations et des instructions sur l’authentification des utilisateurs finaux dans MED-V.</span><span class="sxs-lookup"><span data-stu-id="f5f29-106">The following section provides information and guidance about end-user authentication in MED-V.</span></span>

## <span data-ttu-id="f5f29-107">Authentification des utilisateurs dans MED-V</span><span class="sxs-lookup"><span data-stu-id="f5f29-107">User Authentication in MED-V</span></span>


<span data-ttu-id="f5f29-108">L’authentification dans MED-V se produit généralement à deux niveaux: lorsqu’un utilisateur accède d’abord à MED-V et chaque fois qu’il modifie son mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f5f29-108">Authentication in MED-V generally occurs at two levels: when a user first accesses MED-V and every time that they change their password.</span></span>

<span data-ttu-id="f5f29-109">En fonction de la manière dont vous avez configuré les paramètres MED-V pour l’authentification, l’utilisateur final est généralement invité à entrer son mot de passe lors de la première utilisation de MED-V ou lors de sa première tentative d’ouverture d’une application publiée.</span><span class="sxs-lookup"><span data-stu-id="f5f29-109">Depending on how you have configured MED-V settings for authentication, the end user is typically prompted at some point to enter their password, either the first time MED-V is started or the first time that they try to open a published application.</span></span>

<span data-ttu-id="f5f29-110">Vous pouvez contrôler plusieurs aspects de l’authentification des utilisateurs finaux, y compris les éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="f5f29-110">There are several aspects of end-user authentication that you can control, including the following:</span></span>

<span data-ttu-id="f5f29-111">Si les informations d’identification que l’utilisateur final entre sont stockées dans le gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="f5f29-111">Whether the credentials the end user enters are stored in Credential Manager</span></span>

<span data-ttu-id="f5f29-112">Quelle est la façon dont l’utilisateur final dispose de la possibilité d’entrer et d’enregistrer son mot de passe?</span><span class="sxs-lookup"><span data-stu-id="f5f29-112">In what manner the end user is presented with the option of entering and saving their password</span></span>

<span data-ttu-id="f5f29-113">En fonction du processus préféré de votre entreprise pour gérer l’authentification des utilisateurs finaux, vous pouvez spécifier si la mise en cache des informations d’identification se produit pour un espace de travail MED-V particulier.</span><span class="sxs-lookup"><span data-stu-id="f5f29-113">Depending on your company’s preferred process for managing end-user authentication, you can specify whether credential caching occurs for a particular MED-V workspace.</span></span> <span data-ttu-id="f5f29-114">La mise en cache des informations d’identification d’un utilisateur final est utile, car elles sont uniquement invitées une seule fois pour leur mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f5f29-114">Caching the credentials of an end user is helpful because they are only prompted one time for their password.</span></span> <span data-ttu-id="f5f29-115">Si l’utilisateur final n’est pas autorisé à enregistrer son mot de passe ou s’il ne le décide pas à chaque fois qu’il entame une nouvelle session MED-V, il doit le retaper.</span><span class="sxs-lookup"><span data-stu-id="f5f29-115">If the end user is not allowed to save their password or they decide not to, every time that they start a new MED-V session, they must enter it again.</span></span> <span data-ttu-id="f5f29-116">Par exemple, si MED-V est configuré pour démarrer lorsque l’utilisateur final se connecte à l’hôte mais que l’authentification est désactivée, l’utilisateur final est uniquement invité une fois pendant l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="f5f29-116">For example, if MED-V is configured to start when the end user logs on to the host but Authentication is disabled, the end user is only prompted one time during logon.</span></span> <span data-ttu-id="f5f29-117">Dans ce cas, les informations d’identification sont valides jusqu’à ce que l’utilisateur final se déconnecte de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5f29-117">In this case, credentials are valid until the end user logs off from the host.</span></span>

<span data-ttu-id="f5f29-118">Le cas échéant, vous pouvez utiliser le gestionnaire d’informations d’identification pour supprimer les informations d’identification de l’utilisateur final stockées.</span><span class="sxs-lookup"><span data-stu-id="f5f29-118">If it is necessary, you can use Credential Manager to remove any stored end-user credentials.</span></span>

<span data-ttu-id="f5f29-119">Par défaut, le stockage des informations d’identification est désactivé, mais vous pouvez modifier ce paramètre à l’aide de l’une des méthodes suivantes:</span><span class="sxs-lookup"><span data-stu-id="f5f29-119">By default, credential storing is disabled, but you can change this setting through one of the following methods:</span></span>

<span data-ttu-id="f5f29-120">**Lors de la création du package d’espace de travail MED-V**.</span><span class="sxs-lookup"><span data-stu-id="f5f29-120">**While you are creating the MED-V workspace package**.</span></span> <span data-ttu-id="f5f29-121">Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).</span><span class="sxs-lookup"><span data-stu-id="f5f29-121">For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).</span></span>

<span data-ttu-id="f5f29-122">**Après avoir déployé l’espace de travail MED-V**.</span><span class="sxs-lookup"><span data-stu-id="f5f29-122">**After you have deployed the MED-V workspace**.</span></span> <span data-ttu-id="f5f29-123">Modifiez le paramètre de cmdlet UxCredentialCacheEnabled pour définir la clé de Registre Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="f5f29-123">Edit the MED-V cmdlet parameter UxCredentialCacheEnabled to set the Terminal Services registry key.</span></span> <span data-ttu-id="f5f29-124">Pour plus d’informations, consultez l’aide de Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="f5f29-124">For more information, see Windows PowerShell Help.</span></span>

<span data-ttu-id="f5f29-125">Après le déploiement d’un espace de travail MED-V, vous pouvez définir votre préférence pour l’authentification des utilisateurs finaux en modifiant la stratégie des services Terminal Server nommée DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="f5f29-125">After MED-V workspace deployment, you can set your preference for end-user authentication by modifying the Terminal Services policy named DisablePasswordSaving.</span></span> <span data-ttu-id="f5f29-126">DisablePasswordSaving indique si la case à cocher enregistrement du mot de passe s’affiche dans la fenêtre de dialogue du client RDP et si l’invite d’identification MED-V s’affiche.</span><span class="sxs-lookup"><span data-stu-id="f5f29-126">DisablePasswordSaving controls whether the password saving check box appears on the RDP client dialog window and whether the MED-V credential prompt is displayed.</span></span>

<span data-ttu-id="f5f29-127">Vous trouverez ci-après le chemin de stratégie de la stratégie des services Terminal Server nommée DisablePasswordSaving.</span><span class="sxs-lookup"><span data-stu-id="f5f29-127">Following is the policy path for the Terminal Services policy named DisablePasswordSaving.</span></span>

**<span data-ttu-id="f5f29-128">Regedit</span><span class="sxs-lookup"><span data-stu-id="f5f29-128">Regedit:</span></span>**

<span data-ttu-id="f5f29-129">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="f5f29-129">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Virtual Machine\\Policies\\DisablePasswordSaving</span></span>

**<span data-ttu-id="f5f29-130">Remarque</span><span class="sxs-lookup"><span data-stu-id="f5f29-130">Note</span></span>**  
<span data-ttu-id="f5f29-131">Les modifications que vous apportez à DisablePasswordSaving affectent uniquement l’invite RDP à une machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="f5f29-131">The changes that you make to DisablePasswordSaving only affect the RDP prompt to a virtual machine.</span></span>



<span data-ttu-id="f5f29-132">Le tableau suivant répertorie les différentes façons dont vous pouvez configurer vos paramètres pour le stockage des informations d’identification et les effets des différentes configurations:</span><span class="sxs-lookup"><span data-stu-id="f5f29-132">The following table lists the different ways you can configure your settings for credential storing and the effects of the different configurations:</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="f5f29-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5f29-133">Value</span></span></th>
<th align="left"><span data-ttu-id="f5f29-134">Configuration</span><span class="sxs-lookup"><span data-stu-id="f5f29-134">Configuration</span></span></th>
<th align="left"><span data-ttu-id="f5f29-135">Résultat</span><span class="sxs-lookup"><span data-stu-id="f5f29-135">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f29-136">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="f5f29-136">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f5f29-137">Désactivé</span><span class="sxs-lookup"><span data-stu-id="f5f29-137">Disabled</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="f5f29-138">L’invite MED-V est présentée et une case à cocher accepter est disponible et désactivée.</span><span class="sxs-lookup"><span data-stu-id="f5f29-138">The MED-V prompt is presented and a check box to accept is available and cleared.</span></span> <span data-ttu-id="f5f29-139">Si l’utilisateur final sélectionne la case à cocher, les informations d’identification sont mises en cache pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f5f29-139">If the end user selects the check box, credentials are cached for subsequent use.</span></span> <span data-ttu-id="f5f29-140">L’utilisateur final a également l’avantage d’être invité uniquement à l’expiration du mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f5f29-140">The end user also has the benefit of only being prompted when the password expires.</span></span></p>
<p></p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p><span data-ttu-id="f5f29-141">Si l’utilisateur n’a pas activé la case à cocher, l’invite du client Connexion Bureau à distance (RDC) est présentée à la place de l’invite MED-V et la case à cocher accepter est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f5f29-141">If the end user does not select the check box, the Remote Desktop Connection (RDC) Client prompt is presented instead of the MED-V prompt, and the check box to accept is cleared.</span></span> <span data-ttu-id="f5f29-142">Si l’utilisateur final sélectionne la case à cocher, les informations d’identification du client de RDC sont stockées pour une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f5f29-142">If the end user selects the check box, the RDC Client credential is stored for later use.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="f5f29-143">Important</span><span class="sxs-lookup"><span data-stu-id="f5f29-143">Important</span></span></strong><br/><p><span data-ttu-id="f5f29-144">RDC ne valide pas les informations d’identification à l’entrée de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f5f29-144">RDC does not validate credentials when the end user enters them.</span></span> <span data-ttu-id="f5f29-145">Si l’utilisateur final met en cache les informations d’identification par le biais de l’invite CBD, il est possible que des informations d’identification incorrectes soient stockées.</span><span class="sxs-lookup"><span data-stu-id="f5f29-145">If the end user caches the credentials through the RDC prompt, there is a risk that incorrect credentials might be stored.</span></span> <span data-ttu-id="f5f29-146">Dans ce cas, vous devez supprimer les informations d’identification incorrectes dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="f5f29-146">In this case, the incorrect credentials must be deleted in the Windows Credential Manager.</span></span></p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="f5f29-147">DisablePasswordSaving</span><span class="sxs-lookup"><span data-stu-id="f5f29-147">DisablePasswordSaving</span></span></p></td>
<td align="left"><p><strong><span data-ttu-id="f5f29-148">Activé</span><span class="sxs-lookup"><span data-stu-id="f5f29-148">Enabled</span></span></strong></p></td>
<td align="left"><div class="alert">
<strong><span data-ttu-id="f5f29-149">Remarque</span><span class="sxs-lookup"><span data-stu-id="f5f29-149">Note</span></span></strong><br/><p><span data-ttu-id="f5f29-150">Cette configuration est plus sécurisée, car elle ne permet pas aux informations d’identification de l’utilisateur final d’être mises en cache.</span><span class="sxs-lookup"><span data-stu-id="f5f29-150">This configuration is more secure because it does not allow end user credentials to be cached.</span></span></p>
</div>
<div>

</div></td>
</tr>
</tbody>
</table>



<span data-ttu-id="f5f29-151">Par défaut, l’installation de MED-V définit une clé de Registre dans l’invité pour supprimer l’invite «mot de passe sur le point d’expirer».</span><span class="sxs-lookup"><span data-stu-id="f5f29-151">By default, the MED-V installation sets a registry key in the guest to suppress the "password about to expire" prompt.</span></span> <span data-ttu-id="f5f29-152">L’utilisateur final est invité à entrer un mot de passe pour la modification du mot de passe sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="f5f29-152">The end user is only prompted for a password change on the host.</span></span> <span data-ttu-id="f5f29-153">Les informations d’identification mises à jour sur l’hôte sont transmises à l’invité.</span><span class="sxs-lookup"><span data-stu-id="f5f29-153">Credentials that are updated on the host are passed to the guest.</span></span>

**<span data-ttu-id="f5f29-154">Vigilance</span><span class="sxs-lookup"><span data-stu-id="f5f29-154">Caution</span></span>**  
<span data-ttu-id="f5f29-155">Si vous utilisez une stratégie de groupe dans votre environnement, sachez qu’elle peut remplacer la clé de Registre à l’origine de la réapparition des invites de mot de passe.</span><span class="sxs-lookup"><span data-stu-id="f5f29-155">If you use Group Policy in your environment, know that it can override the registry key causing the password prompts from the guest to reappear.</span></span>



### <span data-ttu-id="f5f29-156">Problèmes de sécurité liés à l’authentification</span><span class="sxs-lookup"><span data-stu-id="f5f29-156">Security Concerns with Authentication</span></span>

<span data-ttu-id="f5f29-157">Même si la mise en cache des informations d’identification de l’utilisateur final offre une meilleure utilisation de l’utilisateur, vous devez connaître les risques liés.</span><span class="sxs-lookup"><span data-stu-id="f5f29-157">Even though caching the end user’s credentials provides the best user experience, you must be aware of the risks involved.</span></span>

<span data-ttu-id="f5f29-158">Lorsque la mise en cache des informations d’identification est activée, les informations d’identification de domaine de l’utilisateur final sont stockées dans un format réversible dans le gestionnaire d’informations d’identification Windows.</span><span class="sxs-lookup"><span data-stu-id="f5f29-158">When credential caching is enabled, the end user’s domain credential is stored in a reversible format within the Windows Credential Manager.</span></span> <span data-ttu-id="f5f29-159">Par conséquent, un attaquant peut écrire un outil qui s’exécute comme un processus de niveau système ou un processus utilisateur final, et qui récupère les informations d’identification de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="f5f29-159">As a result, an attacker could write a tool that runs as either a system level process or an end user process and that retrieves the end user's credentials.</span></span> <span data-ttu-id="f5f29-160">Vous pouvez limiter ce risque uniquement en définissant DisablePasswordSaving sur **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="f5f29-160">You can only lessen this risk by setting DisablePasswordSaving to **Enabled**.</span></span>

<span data-ttu-id="f5f29-161">Ce problème existe lorsque l’authentification MED-V est désactivée, mais que le paramètre de stratégie des services Terminal Server est activé.</span><span class="sxs-lookup"><span data-stu-id="f5f29-161">This same concern exists when MED-V authentication is disabled but the Terminal Services policy setting is enabled.</span></span>

## <span data-ttu-id="f5f29-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5f29-162">Related topics</span></span>


[<span data-ttu-id="f5f29-163">Meilleures pratiques de sécurité pour les opérations de MED-V</span><span class="sxs-lookup"><span data-stu-id="f5f29-163">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)









