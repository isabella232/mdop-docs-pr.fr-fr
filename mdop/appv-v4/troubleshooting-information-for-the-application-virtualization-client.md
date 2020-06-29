---
title: Informations pour résoudre les problèmes liés à Application Virtualization Client
description: Informations pour résoudre les problèmes liés à Application Virtualization Client
author: dansimp
ms.assetid: 260a8dad-847f-4ec0-b7dd-6e6bc52017ed
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c2ab332f5f3b7f8cdc40f6d35e8712d55028a60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806209"
---
# <span data-ttu-id="09acd-103">Informations pour résoudre les problèmes liés à Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="09acd-103">Troubleshooting Information for the Application Virtualization Client</span></span>


<span data-ttu-id="09acd-104">Cette rubrique contient des informations que vous pouvez utiliser pour résoudre divers problèmes sur le client Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="09acd-104">This topic includes information that you can use to troubleshoot various issues on the Application Virtualization (App-V) Client.</span></span>

## <span data-ttu-id="09acd-105">L’actualisation de la publication est très lente</span><span class="sxs-lookup"><span data-stu-id="09acd-105">Publishing Refresh Is Very Slow</span></span>


<span data-ttu-id="09acd-106">Si l’actualisation de la publication sur un ordinateur spécifique prend beaucoup plus de temps que prévu et si le client est configuré pour utiliser le paramètre **IconSourceRoot** , déterminez si **IconSourceRoot** contient une URL non valide.</span><span class="sxs-lookup"><span data-stu-id="09acd-106">If publishing refresh on a specific computer takes much longer than expected and if the client is configured to use the **IconSourceRoot** setting, determine whether **IconSourceRoot** contains a nonvalid URL.</span></span> <span data-ttu-id="09acd-107">Une URL non valide entraînera de longs retards lors de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="09acd-107">A nonvalid URL will cause very long delays during publishing refresh.</span></span>

## <span data-ttu-id="09acd-108">Les utilisateurs ne peuvent pas se connecter au serveur et passer en mode opérations hors connexion</span><span class="sxs-lookup"><span data-stu-id="09acd-108">Users Cannot Connect to the Server and Go into Disconnected Operations Mode</span></span>


<span data-ttu-id="09acd-109">Lorsque vous utilisez un serveur de gestion application-V configuré avec le protocole RTSP, si les utilisateurs ne parviennent pas à se connecter et sont dans le mode opérations déconnectées, déterminez si le certificat utilisé sur le serveur est valide.</span><span class="sxs-lookup"><span data-stu-id="09acd-109">When you are using an App-V Management Server configured with the RTSPS protocol, if the users are unable to connect and they go into disconnected operations mode, determine whether the certificate that is being used on the server is valid.</span></span> <span data-ttu-id="09acd-110">Si ce n’est pas le cas, les utilisateurs ne pourront pas se connecter et pourront y accéder en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="09acd-110">A nonvalid certificate will prevent users from connecting and will cause them to go into disconnected operations mode.</span></span>

## <a href="" id="users-experience-slow-performance-when-applications-are-not-fully-cached-"></a><span data-ttu-id="09acd-111">Les utilisateurs connaissent une dégradation des performances lorsque les applications ne sont pas entièrement mises en cache</span><span class="sxs-lookup"><span data-stu-id="09acd-111">Users Experience Slow Performance When Applications Are Not Fully Cached</span></span>


<span data-ttu-id="09acd-112">Lorsque les applications ne sont pas entièrement mises en cache, les utilisateurs peuvent occasionnellement découvrir des performances intermittentes ou intermittentes au démarrage ou à l’utilisation de l’application.</span><span class="sxs-lookup"><span data-stu-id="09acd-112">When applications are not fully cached, users might occasionally experience temporary slow or intermittent performance when they start or use the application.</span></span> <span data-ttu-id="09acd-113">Il peut y avoir plusieurs raisons à cela, par exemple lorsque le client App-V est dans le processus de chargement automatique d’une application ou lors du traitement d’une demande d’absence de séquence.</span><span class="sxs-lookup"><span data-stu-id="09acd-113">There are several possible reasons this can occur—for example, when the App-V Client is in the process of auto-loading an application or when an Out Of Sequence request is being processed.</span></span> <span data-ttu-id="09acd-114">Lorsque les applications sont entièrement mises en cache, ces problèmes ne se produiront plus.</span><span class="sxs-lookup"><span data-stu-id="09acd-114">When the applications are fully cached, these problems will no longer occur.</span></span>

## <a href="" id="error-displayed-after-an-update-is-removed-"></a><span data-ttu-id="09acd-115">Erreur affichée après la suppression d’une mise à jour</span><span class="sxs-lookup"><span data-stu-id="09acd-115">Error Displayed After an Update Is Removed</span></span>


<span data-ttu-id="09acd-116">Vous devez utiliser le format de commande Windows Installer 3,1 approprié pour supprimer une mise à jour du client App-V, comme suit:</span><span class="sxs-lookup"><span data-stu-id="09acd-116">You must use the correct Windows Installer 3.1 command format to remove an update from the App-V Client, as follows:</span></span>

`Msiexec /I {F82584A0-D706-4D2D-9BC1-7E6D8BE3BB0F} MSIPATCHREMOVE={BE3DD018-9A1F-40FD-9538-C0A995CBD254} /qb /l*v "Uninstall.log"`

<span data-ttu-id="09acd-117">L’utilisation de l’ancien format de commande `msiexec /package <GUID> /uninstall <GUID>` entraîne l’erreur 6003 «le client de virtualisation des applications n’a pas pu être démarré».</span><span class="sxs-lookup"><span data-stu-id="09acd-117">Using the older command format `msiexec /package <GUID> /uninstall <GUID>` will cause error 6003 "Application Virtualization client could not be started".</span></span>

## <span data-ttu-id="09acd-118">Code d’erreur 0A-0000E01E se produit lorsque vous essayez de démarrer une application</span><span class="sxs-lookup"><span data-stu-id="09acd-118">Error Code 0A-0000E01E Occurs When You Try to Start an Application</span></span>


<span data-ttu-id="09acd-119">Code d’erreur 0A-0000E01E indique que le package d’application séquencé est peut-être endommagé.</span><span class="sxs-lookup"><span data-stu-id="09acd-119">Error code 0A-0000E01E indicates that the sequenced application package might be corrupt.</span></span> <span data-ttu-id="09acd-120">La solution consiste à reséquencer le package.</span><span class="sxs-lookup"><span data-stu-id="09acd-120">The solution is to resequence the package.</span></span>

## <span data-ttu-id="09acd-121">Les utilisateurs ne peuvent pas accéder aux fichiers qu’ils ont créés sur le lecteur Q:</span><span class="sxs-lookup"><span data-stu-id="09acd-121">Users Cannot Access Files They Have Created on the Q: Drive</span></span>


<span data-ttu-id="09acd-122">Si les utilisateurs enregistrent des fichiers sur le lecteur **Q:** , ils ne peuvent pas les récupérer, car ils ne disposent pas de droits de lecture sur le lecteur.</span><span class="sxs-lookup"><span data-stu-id="09acd-122">If users save files to the **Q:** drive, they cannot retrieve them because they do not have read rights to the drive.</span></span> <span data-ttu-id="09acd-123">Les utilisateurs ne peuvent pas enregistrer des fichiers sur le lecteur **Q:** .</span><span class="sxs-lookup"><span data-stu-id="09acd-123">Users should not save files to the **Q:** drive.</span></span>

## <span data-ttu-id="09acd-124">L’utilisateur est invité à entrer une erreur 1D1</span><span class="sxs-lookup"><span data-stu-id="09acd-124">User Is Prompted with a 1D1 Error</span></span>


<span data-ttu-id="09acd-125">Lorsque l’URL de diffusion de fichier est définie de manière incorrecte dans le fichier d’OSD (Open Software Descriptor), le client App-V renvoie une erreur 1d1 au lieu d’une erreur «fichier introuvable».</span><span class="sxs-lookup"><span data-stu-id="09acd-125">When the file streaming URL is incorrectly set in the Open Software Descriptor (OSD) file, the App-V Client returns a 1d1 error instead of a “file not found” error.</span></span> <span data-ttu-id="09acd-126">Cette erreur indique que le démarrage de l’application a échoué et que l’utilisateur a été forcé de basculer en mode opérations hors connexion.</span><span class="sxs-lookup"><span data-stu-id="09acd-126">This error indicates that the application start failed and the user has been forced into disconnected operations mode.</span></span> <span data-ttu-id="09acd-127">Corrigez l’URL de diffusion du fichier.</span><span class="sxs-lookup"><span data-stu-id="09acd-127">Correct the file streaming URL.</span></span>

## <span data-ttu-id="09acd-128">Icônes incorrectes associées à certaines applications</span><span class="sxs-lookup"><span data-stu-id="09acd-128">Incorrect Icons Associated with Some Applications</span></span>


<span data-ttu-id="09acd-129">Lorsqu’une icône doit être utilisée dans une opération de publication, le client App-V détermine d’abord s’il possède déjà une copie mise en cache de l’icône, en consultant le cache d’icônes pour un élément dont le chemin source d’origine correspond au chemin d’accès de l’icône fournie à l’opération de publication.</span><span class="sxs-lookup"><span data-stu-id="09acd-129">When an icon is to be used in a publishing operation, the App-V Client first determines whether it already has a cached copy of the icon, by looking in the icon cache for an item whose original source path matches the path of the icon given to the publishing operation.</span></span> <span data-ttu-id="09acd-130">Si le client App-V trouve une correspondance, il utilise l’icône déjà mise en cache; dans le cas contraire, il télécharge la nouvelle icône dans le cache.</span><span class="sxs-lookup"><span data-stu-id="09acd-130">If the App-V Client finds a match, it will use the already-cached icon; otherwise, it will download the new icon into the cache.</span></span> <span data-ttu-id="09acd-131">Si le chemin d’accès à l’icône est un répertoire de travail ou s’il est réutilisé pour de nouvelles icônes ou packages, la recherche dans le cache peut sélectionner l’icône incorrecte d’une opération précédente.</span><span class="sxs-lookup"><span data-stu-id="09acd-131">If the path to the icon is a scratch directory or if it gets reused for new icons or packages, the lookup in the cache might pick the wrong icon from a previous operation.</span></span>

## <span data-ttu-id="09acd-132">Les utilisateurs sont invités à entrer leurs informations d’identification lors du démarrage d’une application.</span><span class="sxs-lookup"><span data-stu-id="09acd-132">Users Are Prompted for Credentials When Starting an Application</span></span>


<span data-ttu-id="09acd-133">Si un utilisateur tente de démarrer une application virtuelle à laquelle l’administrateur système a restreint l’accès, il est possible qu’il soit invité à entrer les informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="09acd-133">If a user attempts to start a virtual application to which the system administrator has restricted access, the user might be prompted to enter credentials.</span></span> <span data-ttu-id="09acd-134">L’utilisateur doit taper le nom d’utilisateur et le mot de passe d’un compte qui est autorisé à lancer l’application, puis appuyez sur entrée.</span><span class="sxs-lookup"><span data-stu-id="09acd-134">The user should type the user name and password for an account that has permission to launch the application and then press ENTER.</span></span>

## <span data-ttu-id="09acd-135">Échec de l’actualisation de publication après la mise à niveau du client App-V vers la version 4,5</span><span class="sxs-lookup"><span data-stu-id="09acd-135">Publishing Refresh Fails After Upgrading the App-V Client to Version 4.5</span></span>


<span data-ttu-id="09acd-136">Si le répertoire de données utilisateur a été placé auparavant dans un emplacement standard (%*ALLUSERSPROFILE*%\\Documents\\SoftGrid Client\\Users\\%*nom_utilisateur*%), les utilisateurs ne disposant pas des droits d’administrateur sur l’ordinateur constateront que l’actualisation de publication échoue après la mise à niveau du client App-V.</span><span class="sxs-lookup"><span data-stu-id="09acd-136">If the user data directory was previously placed in a non-standard location (%*AllUsersProfile*%\\Documents\\SoftGrid Client\\Users\\%*username*%), users who do not have administrator privileges on the computer will find that publishing refresh fails after the App-V Client is upgraded.</span></span> <span data-ttu-id="09acd-137">Lors de la mise à niveau, le répertoire de données global du client App-V et tous ses sous-répertoires sont configurés avec des droits d’accès restreints pour les administrateurs uniquement.</span><span class="sxs-lookup"><span data-stu-id="09acd-137">During the upgrade, the App-V Client global data directory and all its subdirectories are configured with restricted access rights for administrators only.</span></span> <span data-ttu-id="09acd-138">Pour éviter ce problème, vous pouvez modifier le répertoire des données utilisateur avant de procéder à la mise à niveau afin qu’il ne s’agit pas d’un sous-répertoire du répertoire global Data.</span><span class="sxs-lookup"><span data-stu-id="09acd-138">You can avoid this problem by changing the user data directory before upgrading so that it is not a subdirectory of the global data directory.</span></span>

## <span data-ttu-id="09acd-139">Redémarrage requis après l’installation</span><span class="sxs-lookup"><span data-stu-id="09acd-139">Reboot Required After Install Failure</span></span>


<span data-ttu-id="09acd-140">Si l’installation du client échoue pour une raison quelconque et si des tentatives ultérieures d’installation du client échouent, consultez le journal du programme d’installation Windows pour savoir si le message d’erreur «sftplay Fail, erreur = possède 1072 au» s’affiche.</span><span class="sxs-lookup"><span data-stu-id="09acd-140">If the client install fails for any reason and if subsequent attempts to install the client also fail, check the Windows Installer log to see whether it shows an error “sftplay failed, error=1072”.</span></span> <span data-ttu-id="09acd-141">Si tel est le cas, redémarrez l’ordinateur avant d’essayer de réinstaller le client.</span><span class="sxs-lookup"><span data-stu-id="09acd-141">If so, restart the computer before trying to install the client again.</span></span>

## <span data-ttu-id="09acd-142">Réparer une application virtuelle endommagée</span><span class="sxs-lookup"><span data-stu-id="09acd-142">Repairing a Corrupted Virtual Application</span></span>


<span data-ttu-id="09acd-143">Si, pour une raison quelconque, un package d’application virtuelle installé à l’aide d’un fichier MSI (Windows Installer Package) est endommagé, réinstallez le package.</span><span class="sxs-lookup"><span data-stu-id="09acd-143">If for any reason a virtual application package installed using a Windows Installer Package (MSI) file becomes corrupted, reinstall the package.</span></span> <span data-ttu-id="09acd-144">La fonction de réparation disponible dans le programme d’installation Windows n’entraîne pas la mise à jour des volumes utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="09acd-144">The Repair function available in the Windows Installer will not update the user volumes.</span></span>

## <span data-ttu-id="09acd-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="09acd-145">Related topics</span></span>


[<span data-ttu-id="09acd-146">Référence d'Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="09acd-146">Application Virtualization Client Reference</span></span>](application-virtualization-client-reference.md)

 

 





