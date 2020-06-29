---
title: Fichiers journaux d'Application Virtualization Sequencer
description: Fichiers journaux d'Application Virtualization Sequencer
author: dansimp
ms.assetid: 1a296544-eab4-46f9-82ce-3136f8b578af
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: d8cdf9dbc78ccdd03df5903ef4d42990099a2c53
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806618"
---
# <span data-ttu-id="91332-103">Fichiers journaux d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="91332-103">Log Files for the Application Virtualization Sequencer</span></span>


<span data-ttu-id="91332-104">Les fichiers journaux pour le Sequencer Application Virtualization (App-V) fournissent des informations détaillées sur les applications de séquençage, et peuvent être utiles lorsque vous vérifiez la fonctionnalité ou que vous rencontrez des problèmes.</span><span class="sxs-lookup"><span data-stu-id="91332-104">The log files for the Application Virtualization (App-V) Sequencer provide detailed information about sequencing applications, and they can be helpful when you are verifying functionality or when you are troubleshooting issues.</span></span>

<span data-ttu-id="91332-105">Le tableau suivant fournit des informations sur les fichiers journaux et leurs emplacements par défaut, qui sont créés lors de l’utilisation du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="91332-105">The following table provides information about the log files and their default locations, which are created when using the Sequencer.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="91332-106">Nom de fichier journal</span><span class="sxs-lookup"><span data-stu-id="91332-106">Log File Name</span></span></th>
<th align="left"><span data-ttu-id="91332-107">Description</span><span class="sxs-lookup"><span data-stu-id="91332-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91332-108">sft-seq-log.txt</span><span class="sxs-lookup"><span data-stu-id="91332-108">sft-seq-log.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91332-109">Fournit des informations générales sur le séquençage d’une application.</span><span class="sxs-lookup"><span data-stu-id="91332-109">Provides general information about sequencing an application.</span></span> <span data-ttu-id="91332-110">Utilisez ce journal comme point de départ pour la résolution des erreurs de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="91332-110">Use this log as a starting point for troubleshooting Sequencer errors.</span></span></p>
<p><span data-ttu-id="91332-111">Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="91332-111">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="91332-112">[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</span><span class="sxs-lookup"><span data-stu-id="91332-112">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><strong><span data-ttu-id="91332-113">sftbt.txt</span><span class="sxs-lookup"><span data-stu-id="91332-113">sftbt.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91332-114">Fournit des informations sur les tâches de redémarrage de l’ordinateur qui se produisent lors du redémarrage simulé du Sequencer.</span><span class="sxs-lookup"><span data-stu-id="91332-114">Provides information about computer restart tasks that occur during the Sequencer’s simulated restart.</span></span></p>
<p><span data-ttu-id="91332-115">Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="91332-115">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="91332-116">[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</span><span class="sxs-lookup"><span data-stu-id="91332-116">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong><span data-ttu-id="91332-117">SftCallBack.txt</span><span class="sxs-lookup"><span data-stu-id="91332-117">SftCallBack.txt</span></span></strong></p></td>
<td align="left"><p><span data-ttu-id="91332-118">Fournit des informations générales sur les processus utilisés lors du séquençage.</span><span class="sxs-lookup"><span data-stu-id="91332-118">Provides general information about processes used during sequencing.</span></span></p>
<p><span data-ttu-id="91332-119">Emplacement du fichier journal: <em> %windir%\Microsoft Application Virtualization Sequencer\Logs</span><span class="sxs-lookup"><span data-stu-id="91332-119">Log file location: <em>%windir%\Microsoft Application Virtualization Sequencer\Logs</span></span></em></p>
<p><span data-ttu-id="91332-120">[Valeur du jeton de modèle] Emplacement du fichier journal App-V 4.6: <em> %WINDIR%\Program Files\Microsoft Application Virtualization Sequencer\Logs </em> [valeur de jeton de modèle]</span><span class="sxs-lookup"><span data-stu-id="91332-120">[Template Token Value] App-V4.6 log file location: <em>%windir%\Program Files\Microsoft Application Virtualization Sequencer\Logs</em>[Template Token Value]</span></span></p></td>
</tr>
</tbody>
</table>

 

## <span data-ttu-id="91332-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="91332-121">Related topics</span></span>


[<span data-ttu-id="91332-122">Référence d'Application Virtualization Sequencer</span><span class="sxs-lookup"><span data-stu-id="91332-122">Application Virtualization Sequencer Reference</span></span>](application-virtualization-sequencer-reference.md)

 

 





