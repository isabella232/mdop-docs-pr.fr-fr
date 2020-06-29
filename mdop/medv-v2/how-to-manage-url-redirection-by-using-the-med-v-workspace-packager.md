---
title: Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V
description: Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V
author: dansimp
ms.assetid: 1a8d25af-479f-42d3-bf5f-c7fd974bbf8c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 88167923e3bd47f2a3b0b3ada5e818715740dbe3
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810782"
---
# <span data-ttu-id="fcb36-103">Comment gérer la redirection d'URL à l'aide du Gestionnaire de package de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb36-103">How to Manage URL Redirection by Using the MED-V Workspace Packager</span></span>


<span data-ttu-id="fcb36-104">Vous pouvez utiliser le gestionnaire de package d’espace de travail MED-V pour gérer la redirection d’URL dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb36-104">You can use the MED-V Workspace Packager to manage URL redirection in the MED-V workspace.</span></span>

**<span data-ttu-id="fcb36-105">Pour gérer la redirection d’adresse Web dans un espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb36-105">To manage web address redirection in a MED-V workspace</span></span>**

1.  <span data-ttu-id="fcb36-106">Pour ouvrir le **Gestionnaire de package de l’espace de travail MED-v**, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **Microsoft Enterprise Desktop Virtualization**, puis sur **med-v Workspace**.</span><span class="sxs-lookup"><span data-stu-id="fcb36-106">To open the **MED-V Workspace Packager**, click **Start**, click **All Programs**, click **Microsoft Enterprise Desktop Virtualization**, and then click **MED-V Workspace Packager**.</span></span>

2.  <span data-ttu-id="fcb36-107">Dans le volet principal de l' **empaquetage de l’espace de travail MED-V** , cliquez sur **gérer la redirection Web**.</span><span class="sxs-lookup"><span data-stu-id="fcb36-107">On the **MED-V Workspace Packager** main panel, click **Manage Web Redirection**.</span></span>

3.  <span data-ttu-id="fcb36-108">Dans la fenêtre **gérer la redirection Web** , vous pouvez taper, coller ou importer une liste d’URL redirigées vers Internet Explorer dans l’espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="fcb36-108">In the **Manage Web Redirection** window, you can type, paste, or import a list of the URLs that are redirected to Internet Explorer in the MED-V workspace.</span></span>

    **<span data-ttu-id="fcb36-109">Remarque</span><span class="sxs-lookup"><span data-stu-id="fcb36-109">Note</span></span>**  
    <span data-ttu-id="fcb36-110">La redirection d’URL dans MED-V ne prend en charge que les protocoles HTTP et HTTPs.</span><span class="sxs-lookup"><span data-stu-id="fcb36-110">URL redirection in MED-V only supports the protocols HTTP and HTTPS.</span></span> <span data-ttu-id="fcb36-111">MED-V ne fournit pas de prise en charge pour FTP ou tout autre protocole.</span><span class="sxs-lookup"><span data-stu-id="fcb36-111">MED-V does not provide support for FTP or any other protocols.</span></span>



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



4. <span data-ttu-id="fcb36-112">Cliquez sur **Enregistrer sous...**</span><span class="sxs-lookup"><span data-stu-id="fcb36-112">Click **Save as…**</span></span> <span data-ttu-id="fcb36-113">pour enregistrer les fichiers de redirection d’URL mis à jour dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="fcb36-113">to save the updated URL redirection files in the specified folder.</span></span> <span data-ttu-id="fcb36-114">MED-V crée un fichier de Registre qui contient les informations de redirection d’URL mises à jour.</span><span class="sxs-lookup"><span data-stu-id="fcb36-114">MED-V creates a registry file that contains the updated URL redirection information.</span></span> <span data-ttu-id="fcb36-115">Déployez la clé de Registre mise à jour à l’aide d’une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="fcb36-115">Deploy the updated registry key by using Group Policy.</span></span> <span data-ttu-id="fcb36-116">Pour plus d’informations sur l’utilisation d’une stratégie de groupe, voir [installation de logiciels de stratégie de groupe](https://go.microsoft.com/fwlink/?LinkId=195931) ( https://go.microsoft.com/fwlink/?LinkId=195931) .</span><span class="sxs-lookup"><span data-stu-id="fcb36-116">For more information about how to use Group Policy, see [Group Policy Software Installation](https://go.microsoft.com/fwlink/?LinkId=195931) (https://go.microsoft.com/fwlink/?LinkId=195931).</span></span>

   <span data-ttu-id="fcb36-117">MED-V crée également un script Windows PowerShell dans le dossier spécifié que vous pouvez utiliser pour recréer le package d’espace de travail MED-V mis à jour.</span><span class="sxs-lookup"><span data-stu-id="fcb36-117">MED-V also creates a Windows PowerShell script in the specified folder that you can use to re-create the updated MED-V workspace package.</span></span>

## <span data-ttu-id="fcb36-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fcb36-118">Related topics</span></span>


[<span data-ttu-id="fcb36-119">Comment ajouter ou supprimer des informations de redirection des URL dans un espace de travail MED-V déployé</span><span class="sxs-lookup"><span data-stu-id="fcb36-119">How to Add or Remove URL Redirection Information in a Deployed MED-V Workspace</span></span>](how-to-add-or-remove-url-redirection-information-in-a-deployed-med-v-workspace.md)

[<span data-ttu-id="fcb36-120">Gérer la redirection d'URL MED-V</span><span class="sxs-lookup"><span data-stu-id="fcb36-120">Manage MED-V URL Redirection</span></span>](manage-med-v-url-redirection.md)









