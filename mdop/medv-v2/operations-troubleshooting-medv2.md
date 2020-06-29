---
title: Résolution des problèmes d'opérations
description: Résolution des problèmes d'opérations
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804453"
---
# <span data-ttu-id="a2e42-103">Résolution des problèmes d'opérations</span><span class="sxs-lookup"><span data-stu-id="a2e42-103">Operations Troubleshooting</span></span>


<span data-ttu-id="a2e42-104">Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes de fonctionnement généraux dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.</span><span class="sxs-lookup"><span data-stu-id="a2e42-104">This topic includes information that you can use to help troubleshoot general operational issues in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0.</span></span>

## <span data-ttu-id="a2e42-105">Résoudre les problèmes liés aux opérations MED-V</span><span class="sxs-lookup"><span data-stu-id="a2e42-105">Troubleshooting Issues in MED-V Operations</span></span>


<span data-ttu-id="a2e42-106">Voici quelques problèmes rencontrés par les utilisateurs lorsqu’ils exécutent MED-V et des solutions pour vous aider à résoudre ces problèmes:</span><span class="sxs-lookup"><span data-stu-id="a2e42-106">The following are some issues end users might encounter when they run MED-V and solutions to help troubleshoot these issues:</span></span>

<span data-ttu-id="a2e42-107">**Échec de la redirection de la documentation**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-107">**Documentation Redirection Fails**.</span></span> <span data-ttu-id="a2e42-108">Ce problème se produit généralement lorsque le dossier Mes documents d’un utilisateur final pointe vers un emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="a2e42-108">This issue typically occurs when an end user’s My Documents folder points to a network location.</span></span> <span data-ttu-id="a2e42-109">Windows ne prend pas en charge la création d’un partage à partir d’un autre dossier partagé.</span><span class="sxs-lookup"><span data-stu-id="a2e42-109">Windows does not support creating a share from another shared folder.</span></span> <span data-ttu-id="a2e42-110">Lorsqu’un lecteur ou un dossier est redirigé vers l’invité, RDP\\Windows Virtual PC crée un partage pour ce dossier.</span><span class="sxs-lookup"><span data-stu-id="a2e42-110">When a drive or folder is redirected to the guest, RDP\\Windows Virtual PC creates a share for that folder.</span></span> <span data-ttu-id="a2e42-111">Par conséquent, si le dossier My documents sur l’hôte pointe déjà vers un partage, RDP\\Windows Virtual PC ne peut pas créer de partage d’un partage.</span><span class="sxs-lookup"><span data-stu-id="a2e42-111">Therefore, if the My Documents folder on the host is already pointing to a share, RDP\\Windows Virtual PC cannot create a share of a share.</span></span>

<span data-ttu-id="a2e42-112">Ce problème peut également se produire lorsque les informations d’identification requises pour se connecter à la ressource réseau diffèrent des informations d’identification de domaine de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2e42-112">Another possible cause of this issue is that the credentials that are required to connect to the network resource might differ from the user’s domain credentials.</span></span> <span data-ttu-id="a2e42-113">MED-V est peut-être capable de détecter que des documents sont redirigés vers l’hôte, d’envoyer ces informations à l’invité, puis d’essayer de se reconnecter à la ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="a2e42-113">MED-V might be detecting that documents are redirected on the host, send that information to the guest, and then try to reconnect the network resource.</span></span> <span data-ttu-id="a2e42-114">Si les informations d’identification de l’utilisateur ne s’authentifient pas, MED-V peut ne plus essayer de s’authentifier.</span><span class="sxs-lookup"><span data-stu-id="a2e42-114">If the user’s credentials do not authenticate, MED-V might stop trying to authenticate.</span></span>

**<span data-ttu-id="a2e42-115">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-115">Solution</span></span>**

<span data-ttu-id="a2e42-116">Essayez l’une des solutions suivantes pour résoudre ce problème:</span><span class="sxs-lookup"><span data-stu-id="a2e42-116">Try one of the following to resolve this issue:</span></span>

-   <span data-ttu-id="a2e42-117">Définissez le répertoire racine de l’utilisateur dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a2e42-117">Set the user’s root directory inside Active Directory.</span></span> <span data-ttu-id="a2e42-118">L’invité et l’hôte doivent alors se connecter à la même ressource réseau.</span><span class="sxs-lookup"><span data-stu-id="a2e42-118">The guest and host should then connect to the same network resource.</span></span>

-   <span data-ttu-id="a2e42-119">Au lieu de rediriger le dossier Mes documents vers un chemin UNC, mappez-le à une lettre de lecteur (sur l’hôte, mappez un lecteur qui pointe vers la ressource du réseau).</span><span class="sxs-lookup"><span data-stu-id="a2e42-119">Instead of redirecting the My Documents folder to a UNC path, map it to a drive letter (on the host, map a drive that points to the network resource).</span></span> <span data-ttu-id="a2e42-120">Le dossier Mes documents peut ensuite être configuré pour utiliser la lettre du lecteur à la place du chemin d’accès UNC.</span><span class="sxs-lookup"><span data-stu-id="a2e42-120">The My Documents folder can then be set to use the drive letter instead of the UNC path.</span></span> <span data-ttu-id="a2e42-121">L’invité est alors redirigé vers ce même lecteur mappé comme prévu.</span><span class="sxs-lookup"><span data-stu-id="a2e42-121">The guest will then redirect to that same mapped drive as expected.</span></span>

-   <span data-ttu-id="a2e42-122">Créez un script de démarrage dans l’invité qui redirige le dossier Mes documents vers la ressource réseau et fournit des informations d’identification supplémentaires selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="a2e42-122">Create a startup script in the guest that redirects the My Documents folder to the network resource and provides additional credentials as needed.</span></span>

<span data-ttu-id="a2e42-123">**Échec de la redirection d’URL**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-123">**URL Redirection Fails**.</span></span> <span data-ttu-id="a2e42-124">Une URL que vous avez spécifiée pour la redirection de l’hôte vers l’invité n’est pas redirigée comme prévu ou renvoie un message d’erreur indiquant que le site Web n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="a2e42-124">A URL that you have specified for redirection from the host to the guest is not redirecting as intended or is returning an error message that indicates that the website does not exist.</span></span>

**<span data-ttu-id="a2e42-125">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-125">Solution</span></span>**

<span data-ttu-id="a2e42-126">Cette erreur peut se produire en cas d’utilisation incorrecte ou incorrecte de caractères (par exemple, astérisque (\ \*), dans les informations de redirection d’URL.</span><span class="sxs-lookup"><span data-stu-id="a2e42-126">This error can occur when there is a misspelling or incorrect use of characters, such as asterisk (\*), in the URL redirection information.</span></span> <span data-ttu-id="a2e42-127">Vérifiez la valeur de registre de redirection d’URL et corrigez toutes les erreurs.</span><span class="sxs-lookup"><span data-stu-id="a2e42-127">Check the registry value for URL redirection and correct any mistakes.</span></span>

<span data-ttu-id="a2e42-128">La clé de Registre est appelée `RedirectUrls` et se trouve généralement à l’adresse suivante:</span><span class="sxs-lookup"><span data-stu-id="a2e42-128">The registry key is called `RedirectUrls` and is typically located at:</span></span>

<span data-ttu-id="a2e42-129">Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span><span class="sxs-lookup"><span data-stu-id="a2e42-129">Computer\\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience</span></span>

<span data-ttu-id="a2e42-130">**Icône dans la barre des tâches**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-130">**Icon in Taskbar Misleading**.</span></span> <span data-ttu-id="a2e42-131">Par défaut, l’icône qui s’affiche dans la barre des tâches de l’utilisateur final pour les applications publiées et l’URL redirigée est l’icône du PC virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="a2e42-131">By default, the icon that appears in an end user’s taskbar for published applications and redirected URLs is the icon for Windows Virtual PC.</span></span> <span data-ttu-id="a2e42-132">Si un utilisateur final ne connaît pas ce comportement par défaut, il peut devenir confus lorsque vous examinez la barre des tâches pour localiser son application.</span><span class="sxs-lookup"><span data-stu-id="a2e42-132">If an end user is not aware of this default behavior, they can become confused when looking at the taskbar to locate their application.</span></span>

**<span data-ttu-id="a2e42-133">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-133">Solution</span></span>**

<span data-ttu-id="a2e42-134">Le seul moyen d’éviter ce comportement par défaut consiste à modifier les paramètres d’utilisateur pour les propriétés de la barre des tâches comme suit:</span><span class="sxs-lookup"><span data-stu-id="a2e42-134">The only way to avoid this default behavior is to change the user settings for the taskbar properties as follows:</span></span>

1.  <span data-ttu-id="a2e42-135">Cliquez avec le bouton droit sur la barre des tâches, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-135">Right-click the taskbar and then click **Properties**.</span></span>

2.  <span data-ttu-id="a2e42-136">Dans la boîte de dialogue Propriétés de la **barre des tâches et du menu Démarrer** , cliquez sur l’onglet **barre des tâches** .</span><span class="sxs-lookup"><span data-stu-id="a2e42-136">In the **Taskbar and Start Menu Properties** dialog box, click the **Taskbar** tab.</span></span>

3.  <span data-ttu-id="a2e42-137">Dans le menu déroulant de la zone **des boutons de la barre des tâches** , sélectionnez **ne jamais combiner**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-137">In the drop-down bar for the **Taskbar buttons** box, select **Never combine**.</span></span>

4.  <span data-ttu-id="a2e42-138">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-138">Click **OK**.</span></span>

<span data-ttu-id="a2e42-139">Les icônes correspondant aux applications publiées et aux URL redirigées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="a2e42-139">The expected icons for published applications and redirected URLs are displayed.</span></span>

<span data-ttu-id="a2e42-140">**Avertissement émis si le second utilisateur tente de se connecter ou si une machine virtuelle est en cours d’utilisation**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-140">**Warning Issued if Second User Attempts Log on or if Virtual Machine is in Use**.</span></span> <span data-ttu-id="a2e42-141">Un message d’avertissement est émis lorsqu’un utilisateur se connecte à un espace de travail MED-V alors qu’il continue à exécuter MED-V.</span><span class="sxs-lookup"><span data-stu-id="a2e42-141">A warning message is issued when a second user logs on to a MED-V workspace while a first user is still running MED-V.</span></span> <span data-ttu-id="a2e42-142">L’avertissement est également émis si MED-V est démarré alors que l’ordinateur virtuel est utilisé (par exemple, si l’ordinateur virtuel a été démarré via le PC virtuel Windows dans le menu **Démarrer** ).</span><span class="sxs-lookup"><span data-stu-id="a2e42-142">The warning is also issued if MED-V is started while the virtual machine is being used, for example, if the virtual machine was started through Windows Virtual PC on the **Start** menu.</span></span> <span data-ttu-id="a2e42-143">Lorsque l’utilisateur final accepte le message d’avertissement, MED-V s’arrête.</span><span class="sxs-lookup"><span data-stu-id="a2e42-143">When the end user accepts the warning message, MED-V shuts down.</span></span>

**<span data-ttu-id="a2e42-144">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-144">Solution</span></span>**

<span data-ttu-id="a2e42-145">Un utilisateur final doit vérifier que tous les autres utilisateurs sont déconnectés de MED-V avant d’essayer de se connecter.</span><span class="sxs-lookup"><span data-stu-id="a2e42-145">An end user must verify that all other users are logged off MED-V before they try to log on.</span></span> <span data-ttu-id="a2e42-146">Cela garantit qu’aucune autre instance de MED-V n’est en cours d’exécution et que le PC virtuel Windows n’est pas dans le contrôle de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="a2e42-146">This ensures that no other instance of MED-V is running and that Windows Virtual PC is not in control of the virtual machine.</span></span>

<span data-ttu-id="a2e42-147">Des **bips audibles lors de la première configuration**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-147">**Beeps Heard During First Time Setup**.</span></span> <span data-ttu-id="a2e42-148">Occasionnellement, des bips sont audibles lorsque MED-V est lancé pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="a2e42-148">Occasionally, beeps are heard while MED-V is running first time setup.</span></span> <span data-ttu-id="a2e42-149">Cela peut prêter à confusion pour un utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="a2e42-149">This can be confusing to an end user.</span></span> <span data-ttu-id="a2e42-150">Les bips sont émises par l’ordinateur virtuel lorsqu’il effectue certaines actions, telles que l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="a2e42-150">The beeps are originating from the virtual machine when it performs certain actions, such as shutting down.</span></span>

**<span data-ttu-id="a2e42-151">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-151">Solution</span></span>**

<span data-ttu-id="a2e42-152">Vous pouvez arrêter le service bip en spécifiant la commande "net stop BEEP" au début de chaque séquence de démarrage de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="a2e42-152">You can stop the beep service by specifying the "net stop beep" command at the beginning of each virtual machine start sequence.</span></span> <span data-ttu-id="a2e42-153">Vous pouvez ou désactiver le service bip en spécifiant la commande «sc config bips start = disabled».</span><span class="sxs-lookup"><span data-stu-id="a2e42-153">Or you can disable the beep service by specifying the “sc config beep start= disabled" command.</span></span> <span data-ttu-id="a2e42-154">Vous pouvez spécifier ces commandes avant de sceller l’image ou dans le cadre de Sysprep.</span><span class="sxs-lookup"><span data-stu-id="a2e42-154">You can specify these commands either before you seal the image or as part of Sysprep.</span></span>

<span data-ttu-id="a2e42-155">**Connexions réseau multiples créées pour les espaces de travail MED-V en mode Bridged**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-155">**Multiple Network Connections Created for MED-V Workspaces in BRIDGED Mode**.</span></span> <span data-ttu-id="a2e42-156">Si la première fois que vous créez un espace de travail MED-V configuré pour le mode NAT, il ne crée qu’une seule connexion réseau dans l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="a2e42-156">If first time setup is creating a MED-V workspace that is configured for NAT mode, it only creates a single network connection in Windows Virtual PC.</span></span> <span data-ttu-id="a2e42-157">Toutefois, si la première fois que vous créez un espace de travail MED-V configuré pour le mode pont, il crée une connexion réseau distincte pour chaque carte réseau installée sur l’ordinateur, car MED-V ne peut pas identifier la carte réseau active.</span><span class="sxs-lookup"><span data-stu-id="a2e42-157">However, if first time setup is creating a MED-V workspace that is configured for BRIDGED mode, it creates a separate network connection for each network adapter that is installed in the computer, because MED-V cannot determine which network adapter is active.</span></span> <span data-ttu-id="a2e42-158">Cela permet également de s’assurer que les utilisateurs mobiles disposent toujours d’une carte réseau disponible pour les connexions câblées et sans fil.</span><span class="sxs-lookup"><span data-stu-id="a2e42-158">This also ensures that roaming users always have a network adapter available for wired and wireless connections.</span></span>

**<span data-ttu-id="a2e42-159">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-159">Solution</span></span>**

<span data-ttu-id="a2e42-160">Aucune.</span><span class="sxs-lookup"><span data-stu-id="a2e42-160">None.</span></span>

<span data-ttu-id="a2e42-161">L' **application MED-V ne répond pas pendant un certain temps lors de la fermeture**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-161">**MED-V Application is Unresponsive for Too Long when Closing**.</span></span> <span data-ttu-id="a2e42-162">Dans certains cas, une application MED-V ne répond plus lorsque vous tentez de la fermer.</span><span class="sxs-lookup"><span data-stu-id="a2e42-162">In some instances, a MED-V application stops responding when it is trying to close.</span></span>

**<span data-ttu-id="a2e42-163">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-163">Solution</span></span>**

<span data-ttu-id="a2e42-164">Vous pouvez spécifier la durée pendant laquelle MED-V attend de fermer des applications qui ne répondent pas en définissant la clé de Registre WaitToKillAppTimeout dans l’ordinateur virtuel invité.</span><span class="sxs-lookup"><span data-stu-id="a2e42-164">You can specify the length of time that MED-V waits to close unresponsive applications by setting the WaitToKillAppTimeout registry key in the guest virtual machine.</span></span> <span data-ttu-id="a2e42-165">Pour plus d’informations, reportez-vous [à la rubrique Comment augmenter le délai d’arrêt pour que les processus puissent s’arrêter correctement dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .</span><span class="sxs-lookup"><span data-stu-id="a2e42-165">For more information, see [How To Increase Shutdown Time So That Processes Can Quit Properly in Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) (https://go.microsoft.com/fwlink/?LinkId=206819).</span></span>

<span data-ttu-id="a2e42-166">Le **fait de renommer un raccourci d’application publiée dans l’ordinateur virtuel invité ne modifie pas le nom publié dans l’hôte**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-166">**Renaming a Published Application Shortcut in the Guest Virtual Machine does not Change the Published Name in the Host**.</span></span> <span data-ttu-id="a2e42-167">Lorsque vous publiez une application en créant un raccourci et renommez le raccourci dans l’ordinateur virtuel invité, le nom de l’application d’origine reste dans le menu **Démarrer** de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="a2e42-167">When you publish an application by creating a shortcut and then rename the shortcut in the guest virtual machine, the original application name remains in the host **Start** menu.</span></span> <span data-ttu-id="a2e42-168">Le programme continue de s’exécuter comme prévu, mais le programme conserve toujours le nom d’origine.</span><span class="sxs-lookup"><span data-stu-id="a2e42-168">The program continues to run as expected, however the program will always retain the original name.</span></span>

**<span data-ttu-id="a2e42-169">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-169">Solution</span></span>**

<span data-ttu-id="a2e42-170">Aucune.</span><span class="sxs-lookup"><span data-stu-id="a2e42-170">None.</span></span> <span data-ttu-id="a2e42-171">Il s’agit d’un comportement connu de l’ordinateur virtuel Windows.</span><span class="sxs-lookup"><span data-stu-id="a2e42-171">This is a known behavior of Windows Virtual PC.</span></span>

<span data-ttu-id="a2e42-172">**Le déplacement d’un raccourci dans l’ordinateur virtuel invité ne met pas à jour l’emplacement du menu Démarrer de l’ordinateur hôte**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-172">**Moving a Shortcut in the Guest Virtual Machine does not Update the Location on the Host Computer Start Menu**.</span></span> <span data-ttu-id="a2e42-173">Les raccourcis d’application MED-V publiés sur le menu **Démarrer** de l’ordinateur hôte sont catalogués dans le registre.</span><span class="sxs-lookup"><span data-stu-id="a2e42-173">MED-V application shortcuts that are published to the host computer **Start** menu are cataloged in the registry.</span></span> <span data-ttu-id="a2e42-174">Si vous déplacez un raccourci vers une application dans un sous-dossier, le registre ne sera pas mis à jour pour refléter la modification.</span><span class="sxs-lookup"><span data-stu-id="a2e42-174">If you move an application shortcut into a subfolder, the registry is not updated to reflect the change.</span></span>

**<span data-ttu-id="a2e42-175">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-175">Solution</span></span>**

<span data-ttu-id="a2e42-176">Pour modifier l’emplacement d’un raccourci d’application MED-V, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="a2e42-176">Follow these steps to change the location of a MED-V application shortcut:</span></span>

1.  <span data-ttu-id="a2e42-177">Lorsque MED-V est en cours d’exécution, ouvrez l’Explorateur Windows sur l’ordinateur virtuel d’invité MED-V.</span><span class="sxs-lookup"><span data-stu-id="a2e42-177">When MED-V is running, open up Windows Explorer on the MED-V guest virtual machine.</span></span>

2.  <span data-ttu-id="a2e42-178">Accédez au répertoire «%ALLUSERSPROFILE%\\Start Menu\\Programs».</span><span class="sxs-lookup"><span data-stu-id="a2e42-178">Browse to the "%ALLUSERSPROFILE%\\Start Menu\\Programs" directory.</span></span>

3.  <span data-ttu-id="a2e42-179">Déplacez le raccourci de l’application dans les dossiers StartMenu ou programmes.</span><span class="sxs-lookup"><span data-stu-id="a2e42-179">Move the application shortcuts out of the startmenu or programs folders.</span></span>

4.  <span data-ttu-id="a2e42-180">Après un délai de 30 secondes, vérifiez que les raccourcis sont supprimés du menu **Démarrer** de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a2e42-180">After about 30 seconds, validate that the shortcuts are removed from the host computer **Start** menu.</span></span>

5.  <span data-ttu-id="a2e42-181">Replacez les raccourcis de l’application dans les nouveaux dossiers de programmes sous l’annuaire de Menu\\Programs de démarrage.</span><span class="sxs-lookup"><span data-stu-id="a2e42-181">Move the application shortcuts back in to the new program folders under the Start Menu\\Programs directory.</span></span>

6.  <span data-ttu-id="a2e42-182">Après une durée de 30 secondes, vérifiez que les raccourcis sont mis à jour dans le menu **Démarrer** de l’ordinateur hôte.</span><span class="sxs-lookup"><span data-stu-id="a2e42-182">After about 30 seconds, validate that the shortcuts are updated in the host computer **Start** Menu.</span></span>

<span data-ttu-id="a2e42-183">**Les applications publiées peuvent expirer après une période d’inactivité**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-183">**Published Applications can Time Out after Sitting Idle**.</span></span> <span data-ttu-id="a2e42-184">Dans certains cas, le délai imparti pour les applications publiées sera écoulé s’il est resté inactif pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="a2e42-184">In some cases, published applications will time out if they have sat idle for some time.</span></span> <span data-ttu-id="a2e42-185">Cette situation se produit uniquement si la sécurité IPsec est activée et que l’espace de travail MED-V est configuré pour le mode NAT.</span><span class="sxs-lookup"><span data-stu-id="a2e42-185">This situation only occurs if IPsec is enabled and the MED-V workspace is configured for NAT mode.</span></span> <span data-ttu-id="a2e42-186">Cette situation ne se produit pas s’il s’exécute en mode BRIDGEd.</span><span class="sxs-lookup"><span data-stu-id="a2e42-186">This situation does not occur if running in BRIDGED mode.</span></span>

**<span data-ttu-id="a2e42-187">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-187">Solution</span></span>**

<span data-ttu-id="a2e42-188">Désactivez IPsec lorsque vous exécutez l’espace de travail MED-V en mode NAT.</span><span class="sxs-lookup"><span data-stu-id="a2e42-188">Disable IPsec when you are running the MED-V workspace in NAT mode.</span></span>

<span data-ttu-id="a2e42-189">**Le verrouillage d’une application publiée à la barre des tâches ignore MED-V**.</span><span class="sxs-lookup"><span data-stu-id="a2e42-189">**Pinning a Published Application to the Taskbar Bypasses MED-V**.</span></span> <span data-ttu-id="a2e42-190">Si un utilisateur final épingle une application publiée à la barre des tâches, puis ferme l’application, MED-V est ignoré lors de la prochaine ouverture de l’application à partir de l’icône de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2e42-190">If an end user pins a published application to the taskbar and then closes the application, MED-V is bypassed the next time that the application is opened from the taskbar icon.</span></span> <span data-ttu-id="a2e42-191">Au lieu de cela, l’application s’ouvre directement dans une fenêtre VMSAL.</span><span class="sxs-lookup"><span data-stu-id="a2e42-191">Instead, the application opens directly in a VMSAL window.</span></span>

**<span data-ttu-id="a2e42-192">Solution</span><span class="sxs-lookup"><span data-stu-id="a2e42-192">Solution</span></span>**

<span data-ttu-id="a2e42-193">Ne codez pas les applications publiées dans MED-V vers la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="a2e42-193">Do not pin the applications published in MED-V to the taskbar.</span></span>

## <span data-ttu-id="a2e42-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2e42-194">Related topics</span></span>


[<span data-ttu-id="a2e42-195">Meilleures pratiques de sécurité pour les opérations de MED-V</span><span class="sxs-lookup"><span data-stu-id="a2e42-195">Security Best Practices for MED-V Operations</span></span>](security-best-practices-for-med-v-operations.md)

[<span data-ttu-id="a2e42-196">Résolution des problèmes de déploiement</span><span class="sxs-lookup"><span data-stu-id="a2e42-196">Deployment Troubleshooting</span></span>](deployment-troubleshooting.md)

 

 





