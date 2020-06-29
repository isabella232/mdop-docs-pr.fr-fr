---
title: Procédure pour ajouter un serveur
description: Procédure pour ajouter un serveur
author: dansimp
ms.assetid: 1f31678a-8edf-4d35-a812-e4a2abfd979b
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7d08b79bcbf34910ce357f39635431d11e3e99bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808724"
---
# <span data-ttu-id="ac526-103">Procédure pour ajouter un serveur</span><span class="sxs-lookup"><span data-stu-id="ac526-103">How to Add a Server</span></span>


<span data-ttu-id="ac526-104">Pour vous aider à gérer plus efficacement vos serveurs d’administration de la virtualisation de l’application, vous pouvez les organiser en groupes de serveurs.</span><span class="sxs-lookup"><span data-stu-id="ac526-104">To help you manage your Application Virtualization Management Servers more efficiently, organize them into server groups.</span></span> <span data-ttu-id="ac526-105">Après avoir créé un groupe de serveurs dans la console de gestion du serveur d’applications, vous pouvez utiliser la procédure suivante pour ajouter un serveur au groupe.</span><span class="sxs-lookup"><span data-stu-id="ac526-105">After you create a server group in the Application Virtualization Server Management Console, you can use the following procedure to add a server to the group.</span></span>

<span data-ttu-id="ac526-106">**Remarques**  Tous les serveurs d’un groupe de serveurs doivent être connectés au même magasin de données.</span><span class="sxs-lookup"><span data-stu-id="ac526-106">**Note** All servers in a server group must be connected to the same data store.</span></span>

 

**<span data-ttu-id="ac526-107">Pour ajouter un serveur à un groupe</span><span class="sxs-lookup"><span data-stu-id="ac526-107">To add a server to a group</span></span>**

1.  <span data-ttu-id="ac526-108">Cliquez sur le nœud **groupes de serveurs** dans le volet gauche pour développer la liste des groupes de serveurs.</span><span class="sxs-lookup"><span data-stu-id="ac526-108">Click the **Server Groups** node in the left pane to expand the list of server groups.</span></span>

2.  <span data-ttu-id="ac526-109">Cliquez avec le bouton droit sur le groupe de serveurs souhaité, puis sélectionnez **nouveau serveur de gestion des applications**.</span><span class="sxs-lookup"><span data-stu-id="ac526-109">Right-click the desired server group, and select **New Application Virtualization Management Server**.</span></span>

3.  <span data-ttu-id="ac526-110">Dans l' **Assistant Nouveau groupe de serveurs**, entrez le **nom d’affichage** et le nom d' **hôte DNS**.</span><span class="sxs-lookup"><span data-stu-id="ac526-110">In the **New Server Group Wizard**, enter the **Display Name** and the **DNS Host Name**.</span></span>

4.  <span data-ttu-id="ac526-111">Laissez les valeurs par défaut dans le champ **allocation de mémoire maximale** pour le cache du serveur et le champ d’avertissement d' **allocation de mémoire** pour spécifier le niveau d’avertissement de seuil.</span><span class="sxs-lookup"><span data-stu-id="ac526-111">Leave the default values in the **Maximum Memory Allocation** field for the server cache and the **Warn Memory Allocation** field to specify the threshold warning level.</span></span>

5.  <span data-ttu-id="ac526-112">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ac526-112">Click **Next**.</span></span>

6.  <span data-ttu-id="ac526-113">Dans la boîte de dialogue **mode de sécurité des connexions** , activez la case à cocher utiliser la **sécurité améliorée** pour sélectionner le mode de sécurité amélioré, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="ac526-113">In the **Connection Security Mode** dialog, check the **Use enhanced security** box to select enhanced security mode, if desired.</span></span> <span data-ttu-id="ac526-114">Le cas échéant, remplissez l' **Assistant Certificat** ou affichez les certificats existants.</span><span class="sxs-lookup"><span data-stu-id="ac526-114">If necessary, complete the **Certificate Wizard** or view existing certificates.</span></span>

7.  <span data-ttu-id="ac526-115">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="ac526-115">Click **Next**.</span></span>

8.  <span data-ttu-id="ac526-116">Dans la boîte de dialogue Paramètres de port de l' **application Virt** , sélectionnez la case d’option **utiliser le port par défaut** ou le **port personnalisé** de l’utilisateur, puis entrez le numéro de port personnalisé.</span><span class="sxs-lookup"><span data-stu-id="ac526-116">In the **App Virt Port Setting** dialog, select the **Use Default Port** or the **User Custom Port** radio button and enter the custom port number.</span></span>

9.  <span data-ttu-id="ac526-117">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="ac526-117">Click **Finish**.</span></span>

## <span data-ttu-id="ac526-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ac526-118">Related topics</span></span>


[<span data-ttu-id="ac526-119">Procédure pour créer un groupe de serveurs</span><span class="sxs-lookup"><span data-stu-id="ac526-119">How to Create a Server Group</span></span>](how-to-create-a-server-group.md)

[<span data-ttu-id="ac526-120">Procédure pour supprimer un serveur</span><span class="sxs-lookup"><span data-stu-id="ac526-120">How to Remove a Server</span></span>](how-to-remove-a-server.md)

 

 





