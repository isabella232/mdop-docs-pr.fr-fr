---
title: Création ou modification des fichiers mof
description: Création ou modification des fichiers mof
author: dansimp
ms.assetid: 4d19d707-b90f-4057-a6e9-e4221a607190
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 5f59e9133dd25ecf45d16a5cb704d6ea00923d9e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811087"
---
# <span data-ttu-id="70e2e-103">Création ou modification des fichiers mof</span><span class="sxs-lookup"><span data-stu-id="70e2e-103">How to Create or Edit the mof Files</span></span>


<span data-ttu-id="70e2e-104">Avant d’installer Microsoft BitLocker administration et la surveillance (MBAM) avec Configuration Manager, vous devez modifier le fichier Configuration. mof.</span><span class="sxs-lookup"><span data-stu-id="70e2e-104">Before you install Microsoft BitLocker Administration and Monitoring (MBAM) with Configuration Manager, you need to edit the Configuration.mof file.</span></span> <span data-ttu-id="70e2e-105">Vous devez également modifier ou créer le fichier SMS \ _def. mof, en fonction de la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="70e2e-105">You also need to either edit or create the Sms\_def.mof file, depending on which version of Configuration Manager you are using.</span></span>

## <span data-ttu-id="70e2e-106">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="70e2e-106">Edit the Configuration.mof File</span></span>


<span data-ttu-id="70e2e-107">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez modifier le fichier Configuration. mof pour Microsoft System Center Configuration Manager 2007 et SystemCenter2012 ConfigurationManager.</span><span class="sxs-lookup"><span data-stu-id="70e2e-107">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to edit the Configuration.mof file for Microsoft System Center Configuration Manager 2007 and SystemCenter2012 ConfigurationManager.</span></span>

[<span data-ttu-id="70e2e-108">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="70e2e-108">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file.md)

## <a href="" id="create-or-edit-the-sms-def-mof-file"></a><span data-ttu-id="70e2e-109">Créer ou modifier le fichier SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="70e2e-109">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="70e2e-110">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker dans les rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="70e2e-110">To enable the client computers to report BitLocker compliance details in the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span> <span data-ttu-id="70e2e-111">Dans Configuration Manager 2007, le fichier existe déjà, vous devez donc modifier le fichier existant, mais pas le remplacer.</span><span class="sxs-lookup"><span data-stu-id="70e2e-111">In Configuration Manager 2007, the file already exists, so you need to edit, but not overwrite, the existing file.</span></span> <span data-ttu-id="70e2e-112">Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier.</span><span class="sxs-lookup"><span data-stu-id="70e2e-112">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span>

[<span data-ttu-id="70e2e-113">Créer ou modifier le fichier SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="70e2e-113">Create or Edit the Sms\_def.mof File</span></span>](create-or-edit-the-sms-defmof-file.md)

## <span data-ttu-id="70e2e-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="70e2e-114">Related topics</span></span>


[<span data-ttu-id="70e2e-115">Déploiement de MBAM avec Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="70e2e-115">Deploying MBAM with Configuration Manager</span></span>](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





