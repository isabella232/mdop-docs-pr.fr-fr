---
title: Gestion des groupes de connexion
description: Gestion des groupes de connexion
author: dansimp
ms.assetid: 1a9c8f26-f421-4b70-b7e2-da8118e8198c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c2e57b9dbe56072e6049e8fabef5705c374d022c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805083"
---
# <span data-ttu-id="090f1-103">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-103">Managing Connection Groups</span></span>


<span data-ttu-id="090f1-104">Les groupes de connexions permettent aux applications d’un package d’interagir entre elles dans l’environnement virtuel, tout en restant isolément du système.</span><span class="sxs-lookup"><span data-stu-id="090f1-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="090f1-105">L’utilisation de groupes de connexion permet aux administrateurs de gérer les packages indépendamment et de ne pas pouvoir ajouter plusieurs fois la même application sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="090f1-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="090f1-106">**Remarques**  Dans les versions précédentes de App-V 5,0, les groupes de connexion étaient désignés sous le nom de composition de suite dynamique.</span><span class="sxs-lookup"><span data-stu-id="090f1-106">**Note** In previous versions of App-V 5.0, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="090f1-107">Contenu de cet article:</span><span class="sxs-lookup"><span data-stu-id="090f1-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment.md)"><span data-ttu-id="090f1-108">À propos de l’environnement virtuel du groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-109">Décrit l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="090f1-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file.md)"><span data-ttu-id="090f1-110">À propos du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-111">Décrit le fichier de groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="090f1-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group.md)"><span data-ttu-id="090f1-112">Comment créer un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-113">Décrit la création d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="090f1-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages.md)"><span data-ttu-id="090f1-114">Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement</span><span class="sxs-lookup"><span data-stu-id="090f1-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-115">Décrit la création d’un nouveau groupe de connexion contenant une combinaison de packages publiés pour l’utilisateur et publié globalement.</span><span class="sxs-lookup"><span data-stu-id="090f1-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group.md)"><span data-ttu-id="090f1-116">Comment supprimer un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-117">Décrit la suppression d’un groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="090f1-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group.md)"><span data-ttu-id="090f1-118">Comment publier un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="090f1-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="090f1-119">Explique comment publier un groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="090f1-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="090f1-120">Autres ressources pour les groupes de connexion App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="090f1-120">Other resources for App-V 5.0 connection groups</span></span>


-   [<span data-ttu-id="090f1-121">Opérations d'App-V5.0</span><span class="sxs-lookup"><span data-stu-id="090f1-121">Operations for App-V 5.0</span></span>](operations-for-app-v-50.md)

 

 





