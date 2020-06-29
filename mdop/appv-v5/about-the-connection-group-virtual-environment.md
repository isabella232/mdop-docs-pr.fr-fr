---
title: À propos de l’environnement virtuel du groupe de connexion
description: À propos de l’environnement virtuel du groupe de connexion
author: dansimp
ms.assetid: 535fa640-cbd9-425e-8437-94650a70c264
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2bd93c9e7acbf7bbf3f9da506d5d95b8df09e1f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806079"
---
# <span data-ttu-id="8c56c-103">À propos de l’environnement virtuel du groupe de connexion</span><span class="sxs-lookup"><span data-stu-id="8c56c-103">About the Connection Group Virtual Environment</span></span>


**<span data-ttu-id="8c56c-104">Contenu de cet article:</span><span class="sxs-lookup"><span data-stu-id="8c56c-104">In this topic:</span></span>**

-   [<span data-ttu-id="8c56c-105">Déterminer la priorité du package</span><span class="sxs-lookup"><span data-stu-id="8c56c-105">How package priority is determined</span></span>](#bkmk-pkg-priority-deter)

-   [<span data-ttu-id="8c56c-106">Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions</span><span class="sxs-lookup"><span data-stu-id="8c56c-106">Merging identical package paths into one virtual directory in connection groups</span></span>](#bkmk-merged-root-ve-exp)

## <a href="" id="bkmk-pkg-priority-deter"></a><span data-ttu-id="8c56c-107">Déterminer la priorité du package</span><span class="sxs-lookup"><span data-stu-id="8c56c-107">How package priority is determined</span></span>


<span data-ttu-id="8c56c-108">L’environnement virtuel et son état actuel sont associés au groupe de connexions, et non aux packages individuels.</span><span class="sxs-lookup"><span data-stu-id="8c56c-108">The virtual environment and its current state are associated with the connection group, not with the individual packages.</span></span> <span data-ttu-id="8c56c-109">Si un package App-V est supprimé du groupe de connexion, l’État qui existait dans le cadre du groupe de connexion n’est pas migré avec le package.</span><span class="sxs-lookup"><span data-stu-id="8c56c-109">If an App-V package is removed from the connection group, the state that existed as part of the connection group will not migrate with the package.</span></span>

<span data-ttu-id="8c56c-110">Si le même package fait partie de deux groupes de connexion différents, vous devez indiquer le groupe de connexions qu’il doit utiliser.</span><span class="sxs-lookup"><span data-stu-id="8c56c-110">If the same package is a part of two different connection groups, you have to indicate which connection group App-V should use.</span></span> <span data-ttu-id="8c56c-111">Par exemple, vous pouvez avoir deux packages dans un groupe de connexion, qui définissent chacun la même valeur DWORD Registry.</span><span class="sxs-lookup"><span data-stu-id="8c56c-111">For example, you might have two packages in a connection group that each define the same registry DWORD value.</span></span>

<span data-ttu-id="8c56c-112">Le groupe de connexion utilisé est basé sur l’ordre dans lequel un package s’affiche à l’intérieur du document XML **AppConnectionGroup** :</span><span class="sxs-lookup"><span data-stu-id="8c56c-112">The connection group that is used is based on the order in which a package appears inside the **AppConnectionGroup** XML document:</span></span>

-   <span data-ttu-id="8c56c-113">Le premier package a la priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8c56c-113">The first package has the highest precedence.</span></span>

-   <span data-ttu-id="8c56c-114">Le deuxième package a la deuxième priorité la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="8c56c-114">The second package has the second highest precedence.</span></span>

<span data-ttu-id="8c56c-115">Prenez en considération la section exemple suivant:</span><span class="sxs-lookup"><span data-stu-id="8c56c-115">Consider the following example section:</span></span>

```xml
<appv:Packages><appv:PackagePackageId="A8731008-4523-4713-83A4-CD1363907160"VersionId="E889951B-7F30-418B-A69C-B37283BC0DB9"/><appv:PackagePackageId="1DC709C8-309F-4AB4-BD47-F75926D04276"VersionId="01F1943B-C778-40AD-BFAD-AC34A695DF3C"/><appv:PackagePackageId="04220DCA-EE77-42BE-A9F5-96FD8E8593F2"VersionId="E15EFFE9-043D-4C01-BC52-AD2BD1E8BAFA"/></appv:Packages>
```

<span data-ttu-id="8c56c-116">Supposez que la même valeur DWORD ABC (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region) est définie dans les premier et troisième packages, par exemple:</span><span class="sxs-lookup"><span data-stu-id="8c56c-116">Assume that same DWORD value ABC (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region) is defined in the first and third package, such as:</span></span>

-   <span data-ttu-id="8c56c-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5</span><span class="sxs-lookup"><span data-stu-id="8c56c-117">Package 1 (A8731008-4523-4713-83A4-CD1363907160): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5</span></span>

-   <span data-ttu-id="8c56c-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 10</span><span class="sxs-lookup"><span data-stu-id="8c56c-118">Package 3 (04220DCA-EE77-42BE-A9F5-96FD8E8593F2): HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=10</span></span>

<span data-ttu-id="8c56c-119">Dans la mesure où Package 1 apparaît en premier, l’environnement virtuel de AppConnectionGroup aura la valeur DWORD unique de 5 (HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region = 5).</span><span class="sxs-lookup"><span data-stu-id="8c56c-119">Since Package 1 appears first, the AppConnectionGroup's virtual environment will have the single DWORD value of 5 (HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region=5).</span></span> <span data-ttu-id="8c56c-120">Cela signifie que les applications virtuelles dans le package 1, le package 2 et le package 3 verront tous la valeur 5 lors de la recherche de HKEY \ _LOCAL \ _MACHINE \\software\\contoso\\finapp\\region.</span><span class="sxs-lookup"><span data-stu-id="8c56c-120">This means that the virtual applications in Package 1, Package 2, and Package 3 will all see the value 5 when they query for HKEY\_LOCAL\_MACHINE\\software\\contoso\\finapp\\region.</span></span>

<span data-ttu-id="8c56c-121">Les autres ressources de l’environnement virtuel sont résolues de façon similaire, mais le cas échéant, c’est que les collisions se produisent dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8c56c-121">Other virtual environment resources are resolved similarly, but the usual case is that the collisions occur in the registry.</span></span>

## <a href="" id="bkmk-merged-root-ve-exp"></a><span data-ttu-id="8c56c-122">Fusion de chemins de package identiques dans un répertoire virtuel dans les groupes de connexions</span><span class="sxs-lookup"><span data-stu-id="8c56c-122">Merging identical package paths into one virtual directory in connection groups</span></span>


<span data-ttu-id="8c56c-123">Si au moins deux packages d’un groupe de connexion contiennent des chemins d’accès identiques, les chemins d’accès sont fusionnés dans un répertoire virtuel unique à l’intérieur de l’environnement virtuel du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="8c56c-123">If two or more packages in a connection group contain identical directory paths, the paths are merged into a single virtual directory inside the connection group virtual environment.</span></span> <span data-ttu-id="8c56c-124">Cette fusion des chemins d’accès permet à une application dans un même package d’accéder aux fichiers d’un autre package.</span><span class="sxs-lookup"><span data-stu-id="8c56c-124">This merging of paths allows an application in one package to access files that are in a different package.</span></span>

<span data-ttu-id="8c56c-125">Lorsque vous supprimez un package d’un groupe de connexions, les applications de ce package supprimé ne peuvent plus accéder aux fichiers figurant dans les packages restants du groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="8c56c-125">When you remove a package from a connection group, the applications in that removed package are no longer able to access files in the remaining packages in the connection group.</span></span>

<span data-ttu-id="8c56c-126">L’ordre dans lequel l’application-V recherche le nom d’un fichier dans le groupe de connexion est spécifié par l’ordre dans lequel les packages App-V apparaissent dans le fichier manifeste de groupe de connexion.</span><span class="sxs-lookup"><span data-stu-id="8c56c-126">The order in which App-V looks up a file’s name in the connection group is specified by the order in which the App-V packages are listed in the connection group manifest file.</span></span>

<span data-ttu-id="8c56c-127">L’exemple suivant montre l’ordre et la relation d’une recherche de nom de fichier dans un groupe de connexion pour le **package a et le** **package B**.</span><span class="sxs-lookup"><span data-stu-id="8c56c-127">The following example shows the order and relationship of a file name lookup in a connection group for **Package A** and **Package B**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="8c56c-128">Package A</span><span class="sxs-lookup"><span data-stu-id="8c56c-128">Package A</span></span></th>
<th align="left"><span data-ttu-id="8c56c-129">Package B</span><span class="sxs-lookup"><span data-stu-id="8c56c-129">Package B</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="8c56c-130">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="8c56c-130">C:\Windows\System32</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c56c-131">C:\Windows\System32</span><span class="sxs-lookup"><span data-stu-id="8c56c-131">C:\Windows\System32</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="8c56c-132">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="8c56c-132">C:\AppTest</span></span></p></td>
<td align="left"><p><span data-ttu-id="8c56c-133">C:\AppTest</span><span class="sxs-lookup"><span data-stu-id="8c56c-133">C:\AppTest</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="8c56c-134">Dans l’exemple ci-dessus, lorsqu’une application virtualisée tente de rechercher un fichier spécifique, le package A recherche d’abord un chemin de fichier correspondant.</span><span class="sxs-lookup"><span data-stu-id="8c56c-134">In the example above, when a virtualized application tries to find a specific file, Package A is searched first for a matching file path.</span></span> <span data-ttu-id="8c56c-135">Si aucun chemin d’accès correspondant n’est trouvé, le package B est recherché en utilisant les règles de mappage suivantes:</span><span class="sxs-lookup"><span data-stu-id="8c56c-135">If a matching path is not found, Package B is searched, using the following mapping rules:</span></span>

-   <span data-ttu-id="8c56c-136">Si un fichier nommé **test.txt** existe dans la même hiérarchie de dossiers virtuels dans les deux packages d’application, le premier fichier correspondant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8c56c-136">If a file named **test.txt** exists in the same virtual folder hierarchy in both application packages, the first matching file is used.</span></span>

-   <span data-ttu-id="8c56c-137">Si un fichier nommé **bar.txt** existe dans la hiérarchie des dossiers virtuels d’un package d’application, mais pas dans l’autre, le premier fichier correspondant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="8c56c-137">If a file named **bar.txt** exists in the virtual folder hierarchy of one application package, but not in the other, the first matching file is used.</span></span>






## <span data-ttu-id="8c56c-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c56c-138">Related topics</span></span>


[<span data-ttu-id="8c56c-139">Gestion des groupes de connexion</span><span class="sxs-lookup"><span data-stu-id="8c56c-139">Managing Connection Groups</span></span>](managing-connection-groups.md)

 

 





