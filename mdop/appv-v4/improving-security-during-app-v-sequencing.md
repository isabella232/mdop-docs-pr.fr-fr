---
title: Amélioration de la sécurité lors du séquencement d'App-V
description: Amélioration de la sécurité lors du séquencement d'App-V
author: dansimp
ms.assetid: f30206dd-5749-4a27-bbaf-61fc21b9c663
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ba97c334c4ac9a928fee3d69c265c12e82e43619
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806674"
---
# <span data-ttu-id="0e852-103">Amélioration de la sécurité lors du séquencement d'App-V</span><span class="sxs-lookup"><span data-stu-id="0e852-103">Improving Security During App-V Sequencing</span></span>


<span data-ttu-id="0e852-104">L’empaquetage d’applications pour le séquençage représente la plus grande tâche en cours dans une infrastructure App-V.</span><span class="sxs-lookup"><span data-stu-id="0e852-104">Packaging applications for sequencing is the largest ongoing task in an App-V infrastructure.</span></span> <span data-ttu-id="0e852-105">Dans la mesure où cette tâche est en cours, vous devez soigneusement envisager la création de stratégies et de procédures à suivre lors du séquençage d’applications.</span><span class="sxs-lookup"><span data-stu-id="0e852-105">Because this task is ongoing, you should carefully consider creating policies and procedures to follow when sequencing applications.</span></span> <span data-ttu-id="0e852-106">Dans App-V 4.5 lors du séquençage, vous pouvez capturer des listes de contrôle d’accès (ACL) sur les ressources de fichier de l’application virtualisée.</span><span class="sxs-lookup"><span data-stu-id="0e852-106">In App-V4.5, during sequencing, you can capture Access Control Lists (ACLs) on the file assets of the virtualized application.</span></span>

## <span data-ttu-id="0e852-107">Analyse antivirus sur le Sequencer</span><span class="sxs-lookup"><span data-stu-id="0e852-107">Virus Scanning on the Sequencer</span></span>


<span data-ttu-id="0e852-108">Il est recommandé d’installer le logiciel de numérisation sur l’ordinateur de séquençage, puis de détecter la recherche de virus et de programmes malveillants dans l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e852-108">It is a best practice to install the scanning software on the sequencing computer and then scan the computer for viruses and malware.</span></span> <span data-ttu-id="0e852-109">Une fois que l’ordinateur de séquençage est scanné et ne dispose pas de virus et de programmes malveillants, désactivez le logiciel de numérisation, y compris le logiciel antivirus et de détection de logiciels malveillants, sur l’ordinateur de séquençage avant de séquencer les applications.</span><span class="sxs-lookup"><span data-stu-id="0e852-109">After the sequencing computer is scanned and free of any viruses or malware, disable the scanning software, including all antivirus and malware detection software, on the sequencing computer before sequencing any applications.</span></span> <span data-ttu-id="0e852-110">Cela accélère le processus de séquençage et empêche les composants logiciels d’analyse d’être détectés lors du séquençage et inclus dans le package d’application virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0e852-110">This speeds the sequencing process and prevents the scanning software components from being detected during sequencing and included in the virtual application package.</span></span>

## <span data-ttu-id="0e852-111">Capture d’ACL sur des fichiers (NTFS)</span><span class="sxs-lookup"><span data-stu-id="0e852-111">Capturing ACLs on Files (NTFS)</span></span>


<span data-ttu-id="0e852-112">Le Sequencer capture les autorisations NTFS (listes de contrôle d’accès (ACL) pour les fichiers surveillés lors de la phase d’installation du séquençage.</span><span class="sxs-lookup"><span data-stu-id="0e852-112">The Sequencer captures NTFS permissions (the ACLs) for the files that are monitored during the sequencing installation phase.</span></span> <span data-ttu-id="0e852-113">(Avant la publication de App-V 4.5, les ACL n’ont pas été capturées dans le cadre du processus de séquençage.) Cette nouvelle fonctionnalité permet à certaines applications d’être exécutées pour les utilisateurs disposant d’un niveau d’autorisation faible, qui nécessiteraient normalement des privilèges d’administration.</span><span class="sxs-lookup"><span data-stu-id="0e852-113">(Before the release of App-V4.5, ACLs were not captured as part of the sequencing process.) This new feature enables certain applications to run for users with a low level of permission that would normally require Administrative privileges.</span></span>

<span data-ttu-id="0e852-114">Cette fonctionnalité permet également aux ingénieurs de Sequencer de capturer les paramètres de sécurité identifiés par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="0e852-114">This feature also enables the sequencing engineer to capture the security settings identified by the vendor.</span></span> <span data-ttu-id="0e852-115">Le non-respect des paramètres recommandés par le fournisseur risque de laisser l’application ouverte aux attaques ou abus par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0e852-115">Failing to apply the settings recommended by the vendor could leave the application open to attack or misuse by users.</span></span> <span data-ttu-id="0e852-116">Pour plus d’informations sur l’utilisation ou non du déploiement d’une application avec des listes de Contrã’le d’accès ouvertes, reportez-vous au groupe de support de votre application ou au revendeur de logiciels.</span><span class="sxs-lookup"><span data-stu-id="0e852-116">For information about whether or not you should deploy an application with open ACLs, refer to your application support group or the software vendor.</span></span>

<span data-ttu-id="0e852-117">**Important**  Même si le Sequencer capture les listes de contrôle d’accès (ACL) NTFS lors de l’analyse de la phase d’installation du séquençage, il n’enregistre pas les listes de contrôle d’accès pour le registre.</span><span class="sxs-lookup"><span data-stu-id="0e852-117">**Important** Although the sequencer captures the NTFS ACLs while monitoring the installation phase of sequencing, it does not capture the ACLs for the registry.</span></span> <span data-ttu-id="0e852-118">Les utilisateurs disposent d’un accès complet à toutes les clés de Registre pour les applications virtuelles à l’exception des services.</span><span class="sxs-lookup"><span data-stu-id="0e852-118">Users have full access to all registry keys for virtual applications except for services.</span></span> <span data-ttu-id="0e852-119">Toutefois, si un utilisateur modifie le registre d’une application virtuelle, cette modification est stockée à un emplacement spécifique ( `uservol_sftfs_v1.pkg` ) et ne peut pas être affectée par d’autres utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="0e852-119">However, if a user modifies the registry of a virtual application, that change is stored in a specific location (`uservol_sftfs_v1.pkg`) and won’t affect other users.</span></span>

 

<span data-ttu-id="0e852-120">Pendant la phase d’installation, un ingénieur de séquençage peut modifier les autorisations par défaut des fichiers si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0e852-120">During the installation phase, a sequencing engineer can modify the default permissions of the files if necessary.</span></span> <span data-ttu-id="0e852-121">Une fois le processus de séquençage terminé, mais avant de l’enregistrer, vous pouvez choisir d’appliquer des descripteurs de sécurité qui ont été capturés lors de la phase d’installation.</span><span class="sxs-lookup"><span data-stu-id="0e852-121">After the sequencing process is complete, but before saving the package, the sequencing engineer can then choose to enforce security descriptors that were captured during the installation phase.</span></span> <span data-ttu-id="0e852-122">Il est recommandé de mettre en œuvre des descripteurs de sécurité s’il n’y a aucune autre solution pour que l’application s’exécute correctement une fois virtualisé.</span><span class="sxs-lookup"><span data-stu-id="0e852-122">It is a best practice to enforce security descriptors if no other solution allows the application to run properly once virtualized.</span></span>

 

 





