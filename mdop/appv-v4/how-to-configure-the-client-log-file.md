---
title: Procédure pour configurer le fichier journal du client
description: Procédure pour configurer le fichier journal du client
author: dansimp
ms.assetid: dd79f8ce-61e2-4dc8-af03-2a353554a1b2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 729089d683c5d102eb7eb45314583023d3362639
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807250"
---
# <span data-ttu-id="b3a7c-103">Procédure pour configurer le fichier journal du client</span><span class="sxs-lookup"><span data-stu-id="b3a7c-103">How to Configure the Client Log File</span></span>


<span data-ttu-id="b3a7c-104">Vous pouvez utiliser les procédures suivantes pour configurer le fichier journal du client de virtualisation des applications (App-V).</span><span class="sxs-lookup"><span data-stu-id="b3a7c-104">You can use the following procedures to configure the Application Virtualization (App-V) Client log file.</span></span>

**<span data-ttu-id="b3a7c-105">Pour modifier l’emplacement du fichier journal</span><span class="sxs-lookup"><span data-stu-id="b3a7c-105">To change the log file location</span></span>**

-   <span data-ttu-id="b3a7c-106">Modifiez la valeur de clé de Registre suivante pour spécifier le nouveau chemin d’accès au fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-106">Edit the following registry key value to specify the new path for the log file.</span></span> <span data-ttu-id="b3a7c-107">Après avoir modifié cette valeur, vous devez redémarrer le service **sftlist** .</span><span class="sxs-lookup"><span data-stu-id="b3a7c-107">You must restart the **sftlist** service after changing this value.</span></span> <span data-ttu-id="b3a7c-108">Ce lieu peut également être modifié de manière interactive après l’installation.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-108">This location can also be changed interactively after installation.</span></span>

    <span data-ttu-id="b3a7c-109">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span><span class="sxs-lookup"><span data-stu-id="b3a7c-109">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogFileName</span></span>

**<span data-ttu-id="b3a7c-110">Pour modifier le niveau de rapport du journal</span><span class="sxs-lookup"><span data-stu-id="b3a7c-110">To change the log reporting level</span></span>**

-   <span data-ttu-id="b3a7c-111">Par défaut, le type de messages qui sont écrits dans le journal inclut tous les événements de niveau de gravité 4 (information) ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-111">By default, the type of messages that are written to the log include all events of severity level 4 (Informational) or higher.</span></span> <span data-ttu-id="b3a7c-112">Le niveau de gravité est stocké dans la valeur de clé suivante.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-112">The severity level is stored in the following key value.</span></span> <span data-ttu-id="b3a7c-113">Définissez cette valeur de clé sur 5 pour activer la journalisation détaillée.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-113">Set this key value to 5 to enable verbose logging.</span></span> <span data-ttu-id="b3a7c-114">Utilisez la journalisation détaillée uniquement pour les courtes périodes lors de la résolution des problèmes, car elle génère un volume de messages de très grande taille et entraîne le remplissage rapide du journal.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-114">Use verbose logging only for short periods during troubleshooting because it will generate a very large volume of messages and cause the log to fill up quickly.</span></span>

    <span data-ttu-id="b3a7c-115">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span><span class="sxs-lookup"><span data-stu-id="b3a7c-115">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMinSeverity</span></span>

**<span data-ttu-id="b3a7c-116">Pour modifier la taille du journal</span><span class="sxs-lookup"><span data-stu-id="b3a7c-116">To change the log size</span></span>**

-   <span data-ttu-id="b3a7c-117">Dans Application Virtualization (App-V) 4,5, la taille du journal est contrôlée par la valeur de clé de Registre suivante.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-117">In Application Virtualization (App-V) 4.5, the log size is controlled by the following registry key value.</span></span> <span data-ttu-id="b3a7c-118">Cette valeur est définie par défaut sur 256Mo et définit la taille maximale (en Mo) à laquelle le journal peut s’étendre avant de procéder à la réinitialisation.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-118">This value defaults to 256MB and defines the maximum size, in MB, that the log can grow to before being reset.</span></span>

    <span data-ttu-id="b3a7c-119">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span><span class="sxs-lookup"><span data-stu-id="b3a7c-119">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogMaxSize</span></span>

    <span data-ttu-id="b3a7c-120">**Attention**  La valeur de cette clé de registre doit être définie sur une valeur supérieure à zéro pour garantir la réinitialisation du fichier journal.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-120">**Caution** This registry key value must be set to a value greater than zero to ensure the log file does get reset.</span></span>

     

**<span data-ttu-id="b3a7c-121">Pour modifier le nombre de copies de sauvegarde</span><span class="sxs-lookup"><span data-stu-id="b3a7c-121">To change the number of backup copies</span></span>**

-   <span data-ttu-id="b3a7c-122">Lorsque le fichier journal atteint la taille maximale, une réinitialisation est imposée lors de l’écriture suivante du journal.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-122">When the log file reaches the maximum size, a reset is forced when the next write to the log occurs.</span></span> <span data-ttu-id="b3a7c-123">Une réinitialisation entraîne la création d’un nouveau fichier journal et l’ancien fichier est renommé comme sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-123">A reset causes a new log file to be created, and the old file is renamed as a backup.</span></span> <span data-ttu-id="b3a7c-124">Le paramètre de Registre suivant contrôle le nombre de copies de sauvegarde du fichier journal conservées lors de la réinitialisation du fichier.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-124">The following registry setting controls the number of backup copies of the log file that are kept when the file is reset.</span></span> <span data-ttu-id="b3a7c-125">La valeur par défaut est 4.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-125">The default value is 4.</span></span>

    <span data-ttu-id="b3a7c-126">HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span><span class="sxs-lookup"><span data-stu-id="b3a7c-126">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Configuration\\LogRolloverCount</span></span>

    <span data-ttu-id="b3a7c-127">Le format des noms de fichiers du journal de sauvegarde est le suivant: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** et repose sur l’heure de réinitialisation, en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="b3a7c-127">The format of the backup log file names is: **sftlog\_YYYYMMDD\_hhmmss-uuu.txt** and is based on the reset time, in Universal Coordinated Time (UTC).</span></span> <span data-ttu-id="b3a7c-128">Le tableau suivant répertorie les symboles utilisés lors de la création du nom de fichier et leurs descriptions.</span><span class="sxs-lookup"><span data-stu-id="b3a7c-128">The following table lists the symbols used in creating the file names and their descriptions.</span></span>

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left"><span data-ttu-id="b3a7c-129">Symbole</span><span class="sxs-lookup"><span data-stu-id="b3a7c-129">Symbol</span></span></th>
    <th align="left"><span data-ttu-id="b3a7c-130">Description</span><span class="sxs-lookup"><span data-stu-id="b3a7c-130">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b3a7c-131">MM</span><span class="sxs-lookup"><span data-stu-id="b3a7c-131">YYYY</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-132">année à 4 chiffres</span><span class="sxs-lookup"><span data-stu-id="b3a7c-132">4-digit year</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b3a7c-133">HAUTEUR</span><span class="sxs-lookup"><span data-stu-id="b3a7c-133">MM</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-134">mois de 2 chiffres (01 à 12)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-134">2-digit month (01–12)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b3a7c-135">UTER</span><span class="sxs-lookup"><span data-stu-id="b3a7c-135">DD</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-136">jour sur 2 chiffres du mois (01 à 31)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-136">2-digit day of the month (01–31)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b3a7c-137">hh</span><span class="sxs-lookup"><span data-stu-id="b3a7c-137">hh</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-138">heure (00 à 23)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-138">hour (00–23)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b3a7c-139">hauteur</span><span class="sxs-lookup"><span data-stu-id="b3a7c-139">mm</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-140">minutes (00 à 59)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-140">minutes (00–59)</span></span></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><span data-ttu-id="b3a7c-141">ss</span><span class="sxs-lookup"><span data-stu-id="b3a7c-141">ss</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-142">secondes (00 à 59)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-142">seconds (00–59)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><span data-ttu-id="b3a7c-143">uuu</span><span class="sxs-lookup"><span data-stu-id="b3a7c-143">uuu</span></span></p></td>
    <td align="left"><p><span data-ttu-id="b3a7c-144">millisecondes (000 – 999)</span><span class="sxs-lookup"><span data-stu-id="b3a7c-144">milliseconds (000–999)</span></span></p></td>
    </tr>
    </tbody>
    </table>

     

## <span data-ttu-id="b3a7c-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3a7c-145">Related topics</span></span>


[<span data-ttu-id="b3a7c-146">Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="b3a7c-146">How to Configure the App-V Client Registry Settings by Using the Command Line</span></span>](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

 

 





