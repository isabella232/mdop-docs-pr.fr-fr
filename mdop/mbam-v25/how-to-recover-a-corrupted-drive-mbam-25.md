---
title: Récupération d'un lecteur endommagé
description: Récupération d'un lecteur endommagé
author: dansimp
ms.assetid: fa5b846b-dda6-4ae4-bf6c-39e4f1d8aa00
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fd9fd8a65d57cbfe965197fa26b57319ee046784
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809425"
---
# <span data-ttu-id="80095-103">Récupération d'un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="80095-103">How to Recover a Corrupted Drive</span></span>


<span data-ttu-id="80095-104">Vous pouvez utiliser cette procédure avec le site Web d’administration et de contrôle (également appelé support technique) pour récupérer un lecteur endommagé qui est protégé par BitLocker.</span><span class="sxs-lookup"><span data-stu-id="80095-104">You can use this procedure with the Administration and Monitoring Website (also referred to as the Help Desk) Website to recover a corrupted drive that is protected by BitLocker.</span></span> <span data-ttu-id="80095-105">Pour cela, vous devez effectuer les tâches indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="80095-105">To do this, you will complete the tasks outlined in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="80095-106">Tâche</span><span class="sxs-lookup"><span data-stu-id="80095-106">Task</span></span></th>
<th align="left"><span data-ttu-id="80095-107">Détails et informations supplémentaires</span><span class="sxs-lookup"><span data-stu-id="80095-107">Details and more information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80095-108">Créez un fichier de package de clé de récupération en accédant à la <strong> </strong> zone de récupération du lecteur sur le site Web d’administration et de surveillance.</span><span class="sxs-lookup"><span data-stu-id="80095-108">Create a recovery key package file by accessing the <strong>Drive Recovery</strong> area of the Administration and Monitoring Website.</span></span></p></td>
<td align="left"><p><span data-ttu-id="80095-109">Pour accéder à la <strong> zone de récupération du lecteur </strong> , vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle MBAM Advanced support Users.</span><span class="sxs-lookup"><span data-stu-id="80095-109">To access the <strong>Drive Recovery</strong> area, you must be assigned the MBAM Helpdesk Users role or the MBAM Advanced Helpdesk Users role.</span></span> <span data-ttu-id="80095-110">Il est possible que vous ayez attribué un nom différent aux rôles lorsque vous les avez créés.</span><span class="sxs-lookup"><span data-stu-id="80095-110">You may have given these roles different names when you created them.</span></span> <span data-ttu-id="80095-111">Pour plus d’informations, reportez-vous <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)"> à planification pour les comptes et groupes MBAM 2,5 </a> .</span><span class="sxs-lookup"><span data-stu-id="80095-111">For more information, see <a href="planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles" data-raw-source="[Planning for MBAM 2.5 Groups and Accounts](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles)">Planning for MBAM 2.5 Groups and Accounts</a>.</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="80095-112">Copiez le fichier de package sur l’ordinateur qui contient le lecteur endommagé.</span><span class="sxs-lookup"><span data-stu-id="80095-112">Copy the package file to the computer that contains the corrupted drive.</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="80095-113">Utiliser la <code>repair-bde</code> commande pour terminer le processus de récupération.</span><span class="sxs-lookup"><span data-stu-id="80095-113">Use the <code>repair-bde</code> command to complete the recovery process.</span></span></p></td>
<td align="left"><p><span data-ttu-id="80095-114">Pour éviter une perte de données potentielle, il est vivement recommandé de revoir la <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)"> commande Manage-bde </a> avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="80095-114">To avoid a potential loss of data, it is strongly recommended that you review the <a href="https://go.microsoft.com/fwlink/?LinkId=393567" data-raw-source="[Manage-bde](https://go.microsoft.com/fwlink/?LinkId=393567)">Manage-bde</a> command before using it.</span></span></p></td>
</tr>
</tbody>
</table>

 

**<span data-ttu-id="80095-115">Pour récupérer un lecteur endommagé</span><span class="sxs-lookup"><span data-stu-id="80095-115">To recover a corrupted drive</span></span>**

1.  <span data-ttu-id="80095-116">Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.</span><span class="sxs-lookup"><span data-stu-id="80095-116">Open a web browser and navigate to the **Administration and Monitoring Website**.</span></span>

2.  <span data-ttu-id="80095-117">Dans le volet gauche, sélectionnez **récupération de lecteur** pour ouvrir la page **récupérer l’accès à un lecteur chiffré** .</span><span class="sxs-lookup"><span data-stu-id="80095-117">In the left pane, select **Drive Recovery** to open the **Recover access to an encrypted drive** page.</span></span>

3.  <span data-ttu-id="80095-118">Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final, la raison pour laquelle vous pouvez déverrouiller le lecteur et l’ID du mot de passe de récupération de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="80095-118">Enter the end user’s Windows log-on domain and user name, the reason for unlocking the drive, and the end user’s recovery password ID.</span></span>

    <span data-ttu-id="80095-119">**Remarques**  Si vous êtes membre du groupe Advanced support Users Access, vous n’êtes pas obligé d’entrer le nom de domaine ou le nom d’utilisateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80095-119">**Note** If you are a member of the Advanced Helpdesk Users access group, you do not have to enter the user’s domain name or user name.</span></span>

     

4.  <span data-ttu-id="80095-120">Cliquez sur **Envoyer**.</span><span class="sxs-lookup"><span data-stu-id="80095-120">Click **Submit**.</span></span> <span data-ttu-id="80095-121">La clé de récupération s’affiche.</span><span class="sxs-lookup"><span data-stu-id="80095-121">The recovery key will be displayed.</span></span>

5.  <span data-ttu-id="80095-122">Cliquez sur **Enregistrer**, puis sélectionnez **package de clé de récupération**.</span><span class="sxs-lookup"><span data-stu-id="80095-122">Click **Save**, and then select **Recovery Key Package**.</span></span> <span data-ttu-id="80095-123">Le package de clé de récupération sera créé sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="80095-123">The recovery key package will be created on your computer.</span></span>

6.  <span data-ttu-id="80095-124">Copiez le package de clé de récupération sur l’ordinateur sur lequel le lecteur est endommagé.</span><span class="sxs-lookup"><span data-stu-id="80095-124">Copy the recovery key package to the computer that has the corrupted drive.</span></span>

7.  <span data-ttu-id="80095-125">Ouvrez une invite de commandes avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="80095-125">Open an elevated command prompt.</span></span> <span data-ttu-id="80095-126">Pour cela, cliquez sur **Démarrer** , puis tapez `cmd` dans la zone de texte Rechercher dans les **programmes et fichiers** .</span><span class="sxs-lookup"><span data-stu-id="80095-126">To do this, click **Start** and type `cmd` in the **Search programs and files** text box.</span></span> <span data-ttu-id="80095-127">Cliquez avec le bouton droit sur **cmd.exe**et sélectionnez **exécuter en tant qu’administrateur**.</span><span class="sxs-lookup"><span data-stu-id="80095-127">Right-click **cmd.exe**, and select **Run as Administrator**.</span></span>

8.  <span data-ttu-id="80095-128">À l’invite de commandes, tapez ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="80095-128">At the command prompt, type the following:</span></span>

    `repair-bde <corrupted drive> <fixed drive> -kp <location of keypackage> -rp <recovery password>`

    <span data-ttu-id="80095-129">**Remarques**  Remplacez &lt; un *lecteur fixe* &gt; par un disque dur disponible dont l’espace disponible est supérieur ou égal à celui des données sur le disque endommagé.</span><span class="sxs-lookup"><span data-stu-id="80095-129">**Note** Replace &lt;*fixed drive*&gt; with an available hard disk drive that has free space equal to or larger than the data on the corrupted drive.</span></span> <span data-ttu-id="80095-130">Les données du lecteur endommagé sont récupérées et déplacées sur le disque dur spécifié.</span><span class="sxs-lookup"><span data-stu-id="80095-130">Data on the corrupted drive is recovered and moved to the specified hard disk drive.</span></span>

     


## <span data-ttu-id="80095-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80095-131">Related topics</span></span>


[<span data-ttu-id="80095-132">Gestion de BitLocker avec MBAM2.5</span><span class="sxs-lookup"><span data-stu-id="80095-132">Performing BitLocker Management with MBAM 2.5</span></span>](performing-bitlocker-management-with-mbam-25.md)

 
## <span data-ttu-id="80095-133">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="80095-133">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="80095-134">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="80095-134">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="80095-135">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="80095-135">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>
 





