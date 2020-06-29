---
title: Procédure pour configurer les autorisations des utilisateurs
description: Procédure pour configurer les autorisations des utilisateurs
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807225"
---
# <span data-ttu-id="76cf7-103">Procédure pour configurer les autorisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="76cf7-103">How to Configure User Permissions</span></span>


<span data-ttu-id="76cf7-104">Vous pouvez activer et désactiver certaines actions pour les utilisateurs ne disposant pas des droits d’administration en modifiant les valeurs clés sous la clé de Registre **autorisations** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions).</span><span class="sxs-lookup"><span data-stu-id="76cf7-104">You can enable and disable some actions for users who do not have administrative rights by editing the key values under the **Permissions** registry key (HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions).</span></span> <span data-ttu-id="76cf7-105">Cette clé est essentiellement conçue pour empêcher les utilisateurs de faire des erreurs plutôt que de fournir des informations de sécurité spéciales, car les utilisateurs disposant de droits d’administrateur peuvent modifier l’une de ces valeurs clé.</span><span class="sxs-lookup"><span data-stu-id="76cf7-105">This key is primarily designed to help prevent users from making mistakes rather than to provide any special security, because users with administrative rights can edit any of these key values.</span></span> <span data-ttu-id="76cf7-106">Les procédures suivantes sont des exemples de modification des valeurs de clé.</span><span class="sxs-lookup"><span data-stu-id="76cf7-106">The following procedures are examples of how to change the key values.</span></span> <span data-ttu-id="76cf7-107">Pour plus d’informations sur les clés et les clés de Registre clientes sur la virtualisation des applications (App-V), voir <https://go.microsoft.com/fwlink/?LinkId=121528> .</span><span class="sxs-lookup"><span data-stu-id="76cf7-107">For more information about the Application Virtualization (App-V) Client registry keys and values, see <https://go.microsoft.com/fwlink/?LinkId=121528>.</span></span>

**<span data-ttu-id="76cf7-108">Pour modifier les autorisations des utilisateurs</span><span class="sxs-lookup"><span data-stu-id="76cf7-108">To change user permissions</span></span>**

1.  <span data-ttu-id="76cf7-109">Pour permettre aux utilisateurs de choisir d’exécuter le client en mode hors connexion, définissez la valeur clé suivante sur 1:</span><span class="sxs-lookup"><span data-stu-id="76cf7-109">To enable the users to choose to run the client in offline mode, set the following key value to 1:</span></span>

    <span data-ttu-id="76cf7-110">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span><span class="sxs-lookup"><span data-stu-id="76cf7-110">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode</span></span>

2.  <span data-ttu-id="76cf7-111">Pour permettre aux utilisateurs d’afficher toutes les applications par le biais de l’interface utilisateur, définissez la valeur clé suivante sur 1.</span><span class="sxs-lookup"><span data-stu-id="76cf7-111">To enable the users to view all applications through the user interface, set the following key value to 1.</span></span> <span data-ttu-id="76cf7-112">Si vous définissez la valeur sur 0 (zéro), les utilisateurs peuvent voir uniquement les applications qui leur sont proposées.</span><span class="sxs-lookup"><span data-stu-id="76cf7-112">Setting the value to 0 (zero) allows the users to see only the applications that are available to them.</span></span>

    <span data-ttu-id="76cf7-113">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span><span class="sxs-lookup"><span data-stu-id="76cf7-113">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications</span></span>

## <span data-ttu-id="76cf7-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="76cf7-114">Related topics</span></span>


[<span data-ttu-id="76cf7-115">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="76cf7-115">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[<span data-ttu-id="76cf7-116">Autorisations d'accès utilisateur dans Application Virtualization Client</span><span class="sxs-lookup"><span data-stu-id="76cf7-116">User Access Permissions in Application Virtualization Client</span></span>](user-access-permissions-in-application-virtualization-client.md)

 

 





