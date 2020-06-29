---
title: Procédure pour configurer le comportement d'association de type de fichier et de raccourci
description: Procédure pour configurer le comportement d'association de type de fichier et de raccourci
author: dansimp
ms.assetid: d6fd1728-4de6-4066-b36b-d4837d593d40
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 84e3e0cdd43cfc26cf56f1b5ac72560b1c702ae6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807297"
---
# <span data-ttu-id="781a9-103">Procédure pour configurer le comportement d'association de type de fichier et de raccourci</span><span class="sxs-lookup"><span data-stu-id="781a9-103">How to Configure Shortcut and File Type Association Behavior</span></span>


<span data-ttu-id="781a9-104">La stratégie de publication de type raccourci et Association de types de fichier (FTA) est définie et contrôlée par le fichier XML de publication, qui est envoyé aux clients par un serveur de publication lors d’une opération d’actualisation de publication.</span><span class="sxs-lookup"><span data-stu-id="781a9-104">Shortcut and File Type Association (FTA) publishing policy is defined and controlled by the publishing XML file, which is sent to clients by a publishing server during a publishing refresh operation.</span></span> <span data-ttu-id="781a9-105">Lorsque le client reçoit ces informations, il ajoute les données nouvellement publiées relatives aux applications telles que les icônes et FTAs.</span><span class="sxs-lookup"><span data-stu-id="781a9-105">When the client receives this information, it adds any newly published data about applications such as the icons and FTAs.</span></span> <span data-ttu-id="781a9-106">Ensuite, elle supprime toutes les données de publication obsolètes.</span><span class="sxs-lookup"><span data-stu-id="781a9-106">Then, it removes any outdated publishing data.</span></span>

<span data-ttu-id="781a9-107">Dans l’App-V version 4,6, deux valeurs de clé de Registre ont été définies pour permettre aux administrateurs de contrôler ce comportement.</span><span class="sxs-lookup"><span data-stu-id="781a9-107">In App-V version 4.6, two registry key values have been defined to enable administrators to control this behavior.</span></span> <span data-ttu-id="781a9-108">Par défaut, les raccourcis créés localement à l’aide de la console client sont désormais conservés.</span><span class="sxs-lookup"><span data-stu-id="781a9-108">By default, shortcuts that are created locally by using the client console are now retained.</span></span>

## <span data-ttu-id="781a9-109">Comment modifier le raccourci et le comportement de FTA</span><span class="sxs-lookup"><span data-stu-id="781a9-109">How to Change Shortcut and FTA Behavior</span></span>


<span data-ttu-id="781a9-110">Deux nouvelles valeurs de Registre DWORD ont été définies pour la clé de registre de configuration du client, «FileTypePolicy» et «ShortcutPolicy».</span><span class="sxs-lookup"><span data-stu-id="781a9-110">Two new DWORD registry values have been defined for the client Configuration registry key, “FileTypePolicy” and “ShortcutPolicy”.</span></span> <span data-ttu-id="781a9-111">Ces valeurs de Registre DWORD ne sont pas présentes par défaut, mais peuvent être ajoutées manuellement.</span><span class="sxs-lookup"><span data-stu-id="781a9-111">These DWORD registry values are not present by default, but they can be added manually.</span></span> <span data-ttu-id="781a9-112">La clé de registre de configuration se trouve dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span><span class="sxs-lookup"><span data-stu-id="781a9-112">The Configuration registry key is located at HKEY\_LOCAL\_MACHINE\\SOFTWARE\\\[Wow6432Node\\\]Microsoft\\SoftGrid\\4.5\\Client\\Configuration.</span></span>

<span data-ttu-id="781a9-113">Il existe quatre valeurs de stratégie définies dans le tableau ci-dessous, qui s’appliquent aux deux valeurs de clé de registre.</span><span class="sxs-lookup"><span data-stu-id="781a9-113">There are four policy values defined in the following table and these apply to both registry key values.</span></span> <span data-ttu-id="781a9-114">La liste suivante indique les valeurs numériques des paramètres du Registre et le comportement appliqué aux types de fichiers ou aux raccourcis d’une opération d’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="781a9-114">The following list shows the numeric values for the registry settings, and the behavior applied to file types or shortcuts on a publishing refresh operation.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="781a9-115">Nom</span><span class="sxs-lookup"><span data-stu-id="781a9-115">Name</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-116">Type</span><span class="sxs-lookup"><span data-stu-id="781a9-116">Type</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-117">Données (exemples)</span><span class="sxs-lookup"><span data-stu-id="781a9-117">Data (Examples)</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-118">Description</span><span class="sxs-lookup"><span data-stu-id="781a9-118">Description</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="781a9-119">FileTypePolicy</span><span class="sxs-lookup"><span data-stu-id="781a9-119">FileTypePolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-120">DWORD</span><span class="sxs-lookup"><span data-stu-id="781a9-120">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-121">Par défaut = 0X2 (App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="781a9-121">Default=0x2 (App-V 4.6)</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-122">(0x0)-«ClientOnly»-supprimer tous les éléments existants de la même source d’informations de publication et conserver uniquement les éléments ajoutés localement</span><span class="sxs-lookup"><span data-stu-id="781a9-122">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items that are added locally</span></span></p>
<p><span data-ttu-id="781a9-123">(0x1) – "ServerOnly": supprimez tous les éléments obsolètes de la même source d’informations de publication et des éléments ajoutés localement, et ajoutez les nouveaux éléments.</span><span class="sxs-lookup"><span data-stu-id="781a9-123">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items that are added locally, and add the new items</span></span></p>
<p><span data-ttu-id="781a9-124">(0X2)-«ClientAndServer»-supprimer tous les éléments obsolètes de la même source d’informations de publication, conserver les éléments ajoutés localement et ajouter les nouveaux éléments (par défaut en cas de non-présentation pour App-V 4,6)</span><span class="sxs-lookup"><span data-stu-id="781a9-124">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present for App-V 4.6)</span></span></p>
<p><span data-ttu-id="781a9-125">(0x3) – "tout changer"-apporter des modifications aux types de fichiers ou aux raccourcis</span><span class="sxs-lookup"><span data-stu-id="781a9-125">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="781a9-126">ShortcutPolicy</span><span class="sxs-lookup"><span data-stu-id="781a9-126">ShortcutPolicy</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-127">DWORD</span><span class="sxs-lookup"><span data-stu-id="781a9-127">DWORD</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-128">Par défaut = 0X2</span><span class="sxs-lookup"><span data-stu-id="781a9-128">Default=0x2</span></span></p></td>
<td align="left"><p><span data-ttu-id="781a9-129">(0x0)-«ClientOnly»-supprimer tous les éléments existants de la même source d’informations de publication et conserver uniquement les éléments ajoutés localement</span><span class="sxs-lookup"><span data-stu-id="781a9-129">(0x0) – “ClientOnly”- remove any existing items from the same publishing information source, and keep only items added locally</span></span></p>
<p><span data-ttu-id="781a9-130">(0x1) – "ServerOnly"-supprimer tous les éléments obsolètes de la même source d’informations de publication et des éléments ajoutés localement, et ajouter les nouveaux éléments</span><span class="sxs-lookup"><span data-stu-id="781a9-130">(0x1) – “ServerOnly” - remove any outdated items from the same publishing information source and any items added locally, and add the new items</span></span></p>
<p><span data-ttu-id="781a9-131">(0X2)-«ClientAndServer»-supprimer tous les éléments obsolètes de la même source d’informations de publication, conserver les éléments ajoutés localement et ajouter les nouveaux éléments (par défaut en cas de non-présentation)</span><span class="sxs-lookup"><span data-stu-id="781a9-131">(0x2) – “ClientAndServer”- remove any outdated items from the same publishing information source, keep items added locally, and add the new items (default if not present)</span></span></p>
<p><span data-ttu-id="781a9-132">(0x3) – "tout changer"-apporter des modifications aux types de fichiers ou aux raccourcis</span><span class="sxs-lookup"><span data-stu-id="781a9-132">(0x3) – “NoChange” - make no changes to file types or shortcuts</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="781a9-133">**Remarques**  Les valeurs de texte font référence aux valeurs des attributs XML dans le fichier XML de publication.</span><span class="sxs-lookup"><span data-stu-id="781a9-133">**Note** The text values refer to the values for the XML attributes in the publishing XML file.</span></span><span data-ttu-id="781a9-134">Vous pouvez définir ces valeurs manuellement si vous avez implémenté une solution de publication HTTP personnalisée.</span><span class="sxs-lookup"><span data-stu-id="781a9-134"> You can set these values manually if you have implemented a custom HTTP publishing solution.</span></span>

 

 

 





