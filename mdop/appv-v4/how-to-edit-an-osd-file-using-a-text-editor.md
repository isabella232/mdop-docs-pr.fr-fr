---
title: Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte
description: Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte
author: dansimp
ms.assetid: f4263a1b-824f-49b9-8060-b8229c9d9960
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c83547b38cee7e91e8348689583e0542a88dab83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807109"
---
# <span data-ttu-id="a8735-103">Procédure pour modifier un fichier OSD à l'aide d'un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="a8735-103">How to Edit an OSD File Using a Text Editor</span></span>


<span data-ttu-id="a8735-104">Utilisez la procédure suivante pour modifier un fichier d’OSD (Open Software Descriptor) à l’aide d’un éditeur de texte.</span><span class="sxs-lookup"><span data-stu-id="a8735-104">Use the following procedure to edit an Open Software Descriptor (OSD) file by using a text editor.</span></span>

**<span data-ttu-id="a8735-105">Pour modifier un fichier OSD à l’aide d’un éditeur de texte</span><span class="sxs-lookup"><span data-stu-id="a8735-105">To edit an OSD file by using a text editor</span></span>**

1.  <span data-ttu-id="a8735-106">Ouvrez le fichier OSD à l’aide d’un éditeur de texte XML ou ASCII, par exemple le bloc-notes Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8735-106">Open the OSD file using any XML or ASCII text editor—for example, Microsoft Notepad.</span></span>

    <span data-ttu-id="a8735-107">**Remarques**  Avant de modifier le fichier OSD, lisez le schéma prescrit par le fichier XSD figurant dans le répertoire d’installation.</span><span class="sxs-lookup"><span data-stu-id="a8735-107">**Note** Before modifying the OSD file, read the schema prescribed by the XSD file in the install directory.</span></span> <span data-ttu-id="a8735-108">Il est possible que l’échec de la suivi de ce schéma génère des erreurs qui empêchent le démarrage correct d’une application séquencée.</span><span class="sxs-lookup"><span data-stu-id="a8735-108">Failing to follow this schema might introduce errors that prevent a sequenced application from starting successfully.</span></span>

     

2.  <span data-ttu-id="a8735-109">Modifiez le fichier OSD en utilisant votre éditeur de texte XML ou ASCII de votre choix, en adhérant au schéma prescrit et aux instructions suivantes:</span><span class="sxs-lookup"><span data-stu-id="a8735-109">Edit the OSD file using your XML or ASCII text editor of choice, adhering to the prescribed schema and the following guidelines:</span></span>

    1.  <span data-ttu-id="a8735-110">Assurez-vous que les éléments nommés sont imbriqués dans l' &lt; &gt; élément racine SOFTPKG.</span><span class="sxs-lookup"><span data-stu-id="a8735-110">Ensure that named elements are nested within the &lt;SOFTPKG&gt; root element.</span></span>

    2.  <span data-ttu-id="a8735-111">Vérifiez que les noms d’éléments sont en majuscules.</span><span class="sxs-lookup"><span data-stu-id="a8735-111">Ensure that element names are in all uppercase letters.</span></span>

    3.  <span data-ttu-id="a8735-112">Sachez que les valeurs d’attribut respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="a8735-112">Be aware that attribute values are case sensitive.</span></span>

    4.  <span data-ttu-id="a8735-113">Tapez soigneusement et observez les spécifications XML.</span><span class="sxs-lookup"><span data-stu-id="a8735-113">Type carefully, and observe the XML specifications.</span></span>

## <span data-ttu-id="a8735-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8735-114">Related topics</span></span>


[<span data-ttu-id="a8735-115">À propos de l'onglet OSD</span><span class="sxs-lookup"><span data-stu-id="a8735-115">About the OSD Tab</span></span>](about-the-osd-tab.md)

[<span data-ttu-id="a8735-116">Procédure pour modifier un fichier OSD</span><span class="sxs-lookup"><span data-stu-id="a8735-116">How to Edit an OSD File</span></span>](how-to-edit-an-osd-file.md)

[<span data-ttu-id="a8735-117">Éléments du fichier OSD</span><span class="sxs-lookup"><span data-stu-id="a8735-117">OSD File Elements</span></span>](osd-file-elements.md)

 

 





