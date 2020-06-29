---
title: Comment appliquer des paramètres réseau à un espace de travail MED-V
description: Comment appliquer des paramètres réseau à un espace de travail MED-V
author: dansimp
ms.assetid: 641f46b3-a56f-478a-823b-1d90aa1716b3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5a13227518945e74be9e4b3772af97eadbce3fc4
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811802"
---
# <span data-ttu-id="b706b-103">Comment appliquer des paramètres réseau à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b706b-103">How to Apply Network Settings to a MED-V Workspace</span></span>


<span data-ttu-id="b706b-104">Les administrateurs peuvent définir les paramètres réseau de chaque espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b706b-104">Administrators can define the network settings for each MED-V workspace.</span></span>

<span data-ttu-id="b706b-105">Tous les paramètres réseau sont configurés dans le module de **stratégie** sous l’onglet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="b706b-105">All network settings are configured in the **Policy** module, on the **Network** tab.</span></span>

**<span data-ttu-id="b706b-106">Pour appliquer les paramètres réseau à un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b706b-106">To apply network settings to a MED-V workspace</span></span>**

1.  <span data-ttu-id="b706b-107">Cliquez sur l’espace de travail MED-V à configurer.</span><span class="sxs-lookup"><span data-stu-id="b706b-107">Click the MED-V workspace to configure.</span></span>

2.  <span data-ttu-id="b706b-108">Dans le volet **réseau** , configurez les paramètres comme décrit dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b706b-108">In the **Network** pane, configure the settings as described in the following table.</span></span>

3.  <span data-ttu-id="b706b-109">Dans le menu **stratégie** , cliquez sur **valider**.</span><span class="sxs-lookup"><span data-stu-id="b706b-109">On the **Policy** menu, select **Commit**.</span></span>

**<span data-ttu-id="b706b-110">Propriétés du réseau d’espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b706b-110">MED-V Workspace Network Properties</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="b706b-111">Propriété</span><span class="sxs-lookup"><span data-stu-id="b706b-111">Property</span></span></th>
<th align="left"><span data-ttu-id="b706b-112">Description</span><span class="sxs-lookup"><span data-stu-id="b706b-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b706b-113">Propriétés TCP/IP</span><span class="sxs-lookup"><span data-stu-id="b706b-113">TCP/IP Properties</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="b706b-114">Utiliser l’adresse IP de l’hôte (NAT) </strong> : l’espace de travail utilisera la traduction d’adresses réseau pour partager l’adresse IP de l’hôte pour le trafic sortant.</span><span class="sxs-lookup"><span data-stu-id="b706b-114">Use host's IP address (NAT)</strong>—The workspace will use NAT to share the host's IP for outgoing traffic.</span></span></p></li>
<li><p><strong><span data-ttu-id="b706b-115">Utiliser une adresse IP différente de celle de l’hôte (pont) </strong> : l’espace de travail MED-V dispose de sa propre adresse réseau, généralement obtenue par le biais du protocole DHCP.</span><span class="sxs-lookup"><span data-stu-id="b706b-115">Use different IP address than host (Bridge)</strong>—The MED-V workspace will have its own network address, usually obtained via DHCP.</span></span></p></li>
</ul>
<p><span data-ttu-id="b706b-116">Activez la case <strong> à cocher mapper plusieurs cartes dans l’espace de travail </strong> lorsque l’ordinateur hôte est doté de plusieurs cartes.</span><span class="sxs-lookup"><span data-stu-id="b706b-116">Select the <strong>Map multiple adapters into Workspace</strong> check box when the host computer has multiple adapters.</span></span> <span data-ttu-id="b706b-117">Nous vous recommandons de l’utiliser lorsque l’hôte passe d’un réseau à un autre à l’aide de différentes cartes.</span><span class="sxs-lookup"><span data-stu-id="b706b-117">It is recommended to use this configuration when the host moves between different networks using different adapters.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="b706b-118">Serveur DNS</span><span class="sxs-lookup"><span data-stu-id="b706b-118">DNS Server</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="b706b-119">Ne pas modifier </strong> : les paramètres DNS définis dans l’ordinateur virtuel de l’espace de travail MED-V ne seront pas modifiés.</span><span class="sxs-lookup"><span data-stu-id="b706b-119">Don't change</strong>—DNS settings that are set within the MED-V workspace virtual machine will not be changed.</span></span></p></li>
<li><p><strong><span data-ttu-id="b706b-120">Utiliser l’adresse DNS de l’hôte </strong> : les paramètres DNS de l’espace de travail MED-V seront synchronisés pour correspondre aux paramètres de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="b706b-120">Use Host's DNS address</strong>—MED-V workspace DNS settings will be synchronized to match the host's settings.</span></span> <span data-ttu-id="b706b-121">La synchronisation DNS est dynamique.</span><span class="sxs-lookup"><span data-stu-id="b706b-121">The DNS synchronization is dynamic.</span></span> <span data-ttu-id="b706b-122">Il est synchronisé périodiquement avec l’hôte de sorte que, s’il est modifié sur l’hôte, il change dynamiquement dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="b706b-122">It is synchronized periodically with the host so that if it is changed on the host, it will change dynamically in the MED-V workspace.</span></span></p></li>
<li><p><strong><span data-ttu-id="b706b-123">Utiliser des adresses DNS spécifiques </strong> : l’espace de travail MED-V utilisera un DNS spécifique, tel qu’il est spécifié.</span><span class="sxs-lookup"><span data-stu-id="b706b-123">Use specific DNS addresses</strong>—The MED-V workspace will use a specific DNS, as specified.</span></span></p>
<p><span data-ttu-id="b706b-124">Dans les <strong> </strong> champs principal et <strong> secondaire </strong> , entrez les adresses DNS principales et secondaires.</span><span class="sxs-lookup"><span data-stu-id="b706b-124">In the <strong>Primary</strong> and <strong>Secondary</strong> fields, enter the primary and secondary DNS addresses.</span></span></p>
<p><span data-ttu-id="b706b-125">Cochez la <strong> case Ajouter les adresses DNS de l’hôte </strong> pour ajouter l’hôte aux adresses DNS configurées.</span><span class="sxs-lookup"><span data-stu-id="b706b-125">Select the <strong>Append Host's DNS addresses</strong> check box to append the host to the configured DNS addresses.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="b706b-126">Affecter des suffixes DNS</span><span class="sxs-lookup"><span data-stu-id="b706b-126">Assign DNS Suffixes</span></span></p></td>
<td align="left"><ul>
<li><p><strong><span data-ttu-id="b706b-127">Attribuez les suffixes suivants </strong> : activez cette case à cocher pour attribuer des suffixes DNS spécifiques; dans la zone, entrez un ou plusieurs suffixes séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="b706b-127">Assign the following suffixes</strong>—Select this check box to assign specific DNS suffixes; in the box, enter a suffix or multiple suffixes separated by commas.</span></span></p></li>
<li><p><strong><span data-ttu-id="b706b-128">Ajouter des suffixes </strong> d’hôte: activez cette case à cocher pour ajouter les suffixes d’hôte à l’adresse DNS.</span><span class="sxs-lookup"><span data-stu-id="b706b-128">Append host suffixes</strong>—Select this check box to append the host suffixes to the DNS address.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="b706b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b706b-129">Related topics</span></span>


[<span data-ttu-id="b706b-130">Création d'un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="b706b-130">Creating a MED-V Workspace</span></span>](creating-a-med-v-workspacemedv-10-sp1.md)

[<span data-ttu-id="b706b-131">Utilisation de l'interface utilisateur de la console de gestion MED-V</span><span class="sxs-lookup"><span data-stu-id="b706b-131">Using the MED-V Management Console User Interface</span></span>](using-the-med-v-management-console-user-interface.md)

 

 





