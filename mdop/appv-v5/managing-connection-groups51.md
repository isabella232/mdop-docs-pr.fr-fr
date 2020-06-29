---
title: Gestion des groupes de connexion
description: Gestion des groupes de connexion
author: dansimp
ms.assetid: 22c9d3cb-7246-4173-9742-4ba1c24b0a6a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c89fab70fa13a66c2c27b8d014a5bac034f21bd3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805077"
---
# <span data-ttu-id="0bc5b-103">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-103">Managing Connection Groups</span></span>


<span data-ttu-id="0bc5b-104">Les groupes de connexions permettent aux applications d’un package d’interagir entre elles dans l’environnement virtuel, tout en restant isolément du système.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-104">Connection groups enable the applications within a package to interact with each other in the virtual environment, while remaining isolated from the rest of the system.</span></span> <span data-ttu-id="0bc5b-105">L’utilisation de groupes de connexion permet aux administrateurs de gérer les packages indépendamment et de ne pas pouvoir ajouter plusieurs fois la même application sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-105">By using connection groups, administrators can manage packages independently and can avoid having to add the same application multiple times to a client computer.</span></span>

<span data-ttu-id="0bc5b-106">**Remarques**  Dans certaines versions précédentes de App-V, les groupes de connexion étaient désignés sous le nom de composition de suite dynamique.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-106">**Note** In some previous versions of App-V, connection groups were referred to as Dynamic Suite Composition.</span></span>

 

**<span data-ttu-id="0bc5b-107">Contenu de cet article:</span><span class="sxs-lookup"><span data-stu-id="0bc5b-107">In this topic:</span></span>**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><a href="about-the-connection-group-virtual-environment51.md" data-raw-source="[About the Connection Group Virtual Environment](about-the-connection-group-virtual-environment51.md)"><span data-ttu-id="0bc5b-108">À propos de l’environnement virtuel du groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-108">About the Connection Group Virtual Environment</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-109">Décrit l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-109">Describes the connection group virtual environment.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="about-the-connection-group-file51.md" data-raw-source="[About the Connection Group File](about-the-connection-group-file51.md)"><span data-ttu-id="0bc5b-110">À propos du fichier de groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-110">About the Connection Group File</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-111">Décrit le fichier de groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-111">Describes the connection group file.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-create-a-connection-group51.md" data-raw-source="[How to Create a Connection Group](how-to-create-a-connection-group51.md)"><span data-ttu-id="0bc5b-112">Comment créer un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-112">How to Create a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-113">Décrit la création d’un groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-113">Explains how to create a new connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md" data-raw-source="[How to Create a Connection Group with User-Published and Globally Published Packages](how-to-create-a-connection-group-with-user-published-and-globally-published-packages51.md)"><span data-ttu-id="0bc5b-114">Comment créer un groupe de connexion avec des packages publiés par l’utilisateur et globalement</span><span class="sxs-lookup"><span data-stu-id="0bc5b-114">How to Create a Connection Group with User-Published and Globally Published Packages</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-115">Décrit la création d’un nouveau groupe de connexion contenant une combinaison de packages publiés pour l’utilisateur et publié globalement.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-115">Explains how to create a new connection group that contains a mix of packages that are published to the user and published globally.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><a href="how-to-delete-a-connection-group51.md" data-raw-source="[How to Delete a Connection Group](how-to-delete-a-connection-group51.md)"><span data-ttu-id="0bc5b-116">Comment supprimer un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-116">How to Delete a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-117">Décrit la suppression d’un groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-117">Explains how to delete a connection group.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="how-to-publish-a-connection-group51.md" data-raw-source="[How to Publish a Connection Group](how-to-publish-a-connection-group51.md)"><span data-ttu-id="0bc5b-118">Comment publier un groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="0bc5b-118">How to Publish a Connection Group</span></span></a></p></td>
<td align="left"><p><span data-ttu-id="0bc5b-119">Explique comment publier un groupe de connexions.</span><span class="sxs-lookup"><span data-stu-id="0bc5b-119">Explains how to publish a connection group.</span></span></p></td>
</tr>
</tbody>
</table>

 






## <span data-ttu-id="0bc5b-120">Autres ressources pour les groupes de connexion App-V 5,1</span><span class="sxs-lookup"><span data-stu-id="0bc5b-120">Other resources for App-V 5.1 connection groups</span></span>


-   [<span data-ttu-id="0bc5b-121">Opérations d'App-V5.1</span><span class="sxs-lookup"><span data-stu-id="0bc5b-121">Operations for App-V 5.1</span></span>](operations-for-app-v-51.md)

 

 





