---
title: Planification des applications à synchroniser avec UE-V1.0
description: Planification des applications à synchroniser avec UE-V1.0
author: dansimp
ms.assetid: c718274f-87b4-47f3-8ef7-5e1bd5557a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f2b04942588d0f6efad03d5e0249534cd325c09
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804212"
---
# <span data-ttu-id="114b8-103">Planification des applications à synchroniser avec UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="114b8-103">Planning Which Applications to Synchronize with UE-V 1.0</span></span>


<span data-ttu-id="114b8-104">La virtualisation de l’utilisation de Microsoft User (UE-V) utilise des modèles d’emplacement des paramètres (fichiers XML) qui définissent les paramètres capturés et appliqués par UE-V.</span><span class="sxs-lookup"><span data-stu-id="114b8-104">Microsoft User Experience Virtualization (UE-V) uses settings location templates (XML files) that define the settings that are captured and applied by UE-V.</span></span> <span data-ttu-id="114b8-105">UE-V inclut un ensemble de modèles d’emplacements de paramètres prédéfinis et permet également aux administrateurs de créer des modèles d’emplacement des paramètres personnalisés pour les applications tierces ou métier utilisées dans l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="114b8-105">UE-V includes a set of predefined settings location templates and also allows administrators to create custom settings location templates for third-party or line-of-business applications that are used in the enterprise.</span></span>

<span data-ttu-id="114b8-106">En tant qu’administrateur, lorsque vous déterminez quelles applications inclure dans votre solution UE-V, vous devez déterminer quels paramètres peuvent être personnalisés par les utilisateurs et comment et où l’application stocke les paramètres.</span><span class="sxs-lookup"><span data-stu-id="114b8-106">As an administrator, when you consider which applications to include in your UE-V solution, consider which settings can be customized by users, and how and where the application stores its settings.</span></span> <span data-ttu-id="114b8-107">Toutes les applications n’ont pas de paramètres qui peuvent être personnalisés ou personnalisés de façon régulière par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="114b8-107">Not all applications have settings that can be customized or that are routinely customized by users.</span></span> <span data-ttu-id="114b8-108">De plus, tous les paramètres d’application ne peuvent pas être déplacés en toute sécurité sur plusieurs ordinateurs ou environnements.</span><span class="sxs-lookup"><span data-stu-id="114b8-108">In addition, not all applications settings can safely roam across multiple computers or environments.</span></span> <span data-ttu-id="114b8-109">Synchroniser les paramètres qui répondent aux critères suivants:</span><span class="sxs-lookup"><span data-stu-id="114b8-109">Synchronize settings that meet the following criteria:</span></span>

-   <span data-ttu-id="114b8-110">Paramètres stockés dans des emplacements accessibles aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="114b8-110">Settings that are stored in user-accessible locations.</span></span> <span data-ttu-id="114b8-111">Par exemple, ne synchronisez pas les paramètres stockés dans la section system32 ou en dehors de la section HKCU du Registre.</span><span class="sxs-lookup"><span data-stu-id="114b8-111">For example, do not synchronize settings that are stored in system32 or outside HKCU section of the registry.</span></span>

-   <span data-ttu-id="114b8-112">Paramètres qui ne sont pas propres à l’ordinateur en particulier.</span><span class="sxs-lookup"><span data-stu-id="114b8-112">Settings that are not specific to the particular computer.</span></span> <span data-ttu-id="114b8-113">Par exemple, excluez les configurations réseau ou matérielles.</span><span class="sxs-lookup"><span data-stu-id="114b8-113">For example, exclude network or hardware configurations.</span></span>

-   <span data-ttu-id="114b8-114">Paramètres qui peuvent être synchronisés entre ordinateurs sans risque de corruption de données.</span><span class="sxs-lookup"><span data-stu-id="114b8-114">Settings that can be synchronized between computers without risk of corrupted data.</span></span> <span data-ttu-id="114b8-115">Par exemple, n’utilisez pas de paramètres stockés dans un fichier de base de données.</span><span class="sxs-lookup"><span data-stu-id="114b8-115">For example, do not use settings that are stored in a database file.</span></span>

## <span data-ttu-id="114b8-116">Modèles d’emplacement des paramètres inclus dans UE-V</span><span class="sxs-lookup"><span data-stu-id="114b8-116">Settings location templates that are included in UE-V</span></span>


**<span data-ttu-id="114b8-117">Les modèles d’emplacement des paramètres d’application UE-V</span><span class="sxs-lookup"><span data-stu-id="114b8-117">UE-V application settings location templates</span></span>**

<span data-ttu-id="114b8-118">Le logiciel d’installation de l’agent UE-V installe l’agent et inscrit un groupe par défaut de modèles d’emplacements des paramètres pour les applications Microsoft courantes.</span><span class="sxs-lookup"><span data-stu-id="114b8-118">The UE-V agent installation software installs the agent and registers a default group of settings location templates for common Microsoft applications.</span></span> <span data-ttu-id="114b8-119">Ces paramètres de capture des paramètres de capture d’emplacements pour les applications suivantes:</span><span class="sxs-lookup"><span data-stu-id="114b8-119">These settings location templates capture settings values for the following applications:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong><span data-ttu-id="114b8-120">Catégorie d’application</span><span class="sxs-lookup"><span data-stu-id="114b8-120">Application category</span></span></strong></th>
<th align="left"><strong><span data-ttu-id="114b8-121">Description</span><span class="sxs-lookup"><span data-stu-id="114b8-121">Description</span></span></strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114b8-122">Applications Microsoft Office 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-122">Microsoft Office 2010 applications</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-123">Microsoft Word 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-123">Microsoft Word 2010</span></span></p>
<p><span data-ttu-id="114b8-124">Microsoft Excel 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-124">Microsoft Excel 2010</span></span></p>
<p><span data-ttu-id="114b8-125">Microsoft Outlook 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-125">Microsoft Outlook 2010</span></span></p>
<p><span data-ttu-id="114b8-126">Microsoft Access 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-126">Microsoft Access 2010</span></span></p>
<p><span data-ttu-id="114b8-127">Microsoft Project 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-127">Microsoft Project 2010</span></span></p>
<p><span data-ttu-id="114b8-128">Microsoft PowerPoint 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-128">Microsoft PowerPoint 2010</span></span></p>
<p><span data-ttu-id="114b8-129">Microsoft Publisher 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-129">Microsoft Publisher 2010</span></span></p>
<p><span data-ttu-id="114b8-130">Microsoft Visio 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-130">Microsoft Visio 2010</span></span></p>
<p><span data-ttu-id="114b8-131">Microsoft SharePoint Workspace 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-131">Microsoft SharePoint Workspace 2010</span></span></p>
<p><span data-ttu-id="114b8-132">Microsoft InfoPath 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-132">Microsoft InfoPath 2010</span></span></p>
<p><span data-ttu-id="114b8-133">Microsoft Lync 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-133">Microsoft Lync 2010</span></span></p>
<p><span data-ttu-id="114b8-134">Microsoft OneNote 2010</span><span class="sxs-lookup"><span data-stu-id="114b8-134">Microsoft OneNote 2010</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="114b8-135">Options du navigateur (Internet Explorer 8, Internet Explorer 9 et Internet Explorer 10)</span><span class="sxs-lookup"><span data-stu-id="114b8-135">Browser options (Internet Explorer 8, Internet Explorer 9, and Internet Explorer 10)</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-136">Favoris, page d’accueil, onglets et barres d’outils.</span><span class="sxs-lookup"><span data-stu-id="114b8-136">Favorites, home page, tabs, and toolbars.</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114b8-137">Accessoires Windows</span><span class="sxs-lookup"><span data-stu-id="114b8-137">Windows accessories</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-138">Calculatrice, bloc-notes, WordPad.</span><span class="sxs-lookup"><span data-stu-id="114b8-138">Calculator, Notepad, WordPad.</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="114b8-139">Les paramètres d’application s’appliquent à l’application au démarrage de l’application.</span><span class="sxs-lookup"><span data-stu-id="114b8-139">Application settings are applied to the application when the application is started.</span></span> <span data-ttu-id="114b8-140">Ils sont enregistrés lors de la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="114b8-140">They are saved when the application closes.</span></span>

**<span data-ttu-id="114b8-141">UE-V-modèles d’emplacement des paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="114b8-141">UE-V Windows settings location templates</span></span>**

<span data-ttu-id="114b8-142">La virtualisation de l’interface utilisateur inclut les modèles d’emplacement des paramètres qui capturent les valeurs de paramètres pour les paramètres Windows suivants:</span><span class="sxs-lookup"><span data-stu-id="114b8-142">User Experience Virtualization includes settings location templates that capture settings values for the following Windows settings:</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="114b8-143">paramètres Windows</span><span class="sxs-lookup"><span data-stu-id="114b8-143">Windows settings</span></span></th>
<th align="left"><span data-ttu-id="114b8-144">Description</span><span class="sxs-lookup"><span data-stu-id="114b8-144">Description</span></span></th>
<th align="left"><span data-ttu-id="114b8-145">Appliquer le</span><span class="sxs-lookup"><span data-stu-id="114b8-145">Apply on</span></span></th>
<th align="left"><span data-ttu-id="114b8-146">État par défaut</span><span class="sxs-lookup"><span data-stu-id="114b8-146">Default state</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114b8-147">Arrière-plan du Bureau</span><span class="sxs-lookup"><span data-stu-id="114b8-147">Desktop background</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-148">Arrière-plan actuellement actif sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="114b8-148">Currently active desktop background.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-149">Connexion, déverrouiller, connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="114b8-149">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-150">Activé</span><span class="sxs-lookup"><span data-stu-id="114b8-150">Enabled</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="114b8-151">Options d’ergonomie</span><span class="sxs-lookup"><span data-stu-id="114b8-151">Ease of Access</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-152">Accessibilité et paramètres d’entrée, loupe, narrateur et clavier visuel.</span><span class="sxs-lookup"><span data-stu-id="114b8-152">Accessibility and input settings, magnifier, Narrator, and on-Screen keyboard.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-153">Connexion, déverrouiller, connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="114b8-153">Logon, unlock, remote connect.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-154">Désactivé</span><span class="sxs-lookup"><span data-stu-id="114b8-154">Disabled</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="114b8-155">Paramètres de bureau</span><span class="sxs-lookup"><span data-stu-id="114b8-155">Desktop settings</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-156">Paramètres du menu Démarrer et de la barre des tâches, options des dossiers, icônes du bureau par défaut, horloges supplémentaires et paramètres régionaux et linguistiques.</span><span class="sxs-lookup"><span data-stu-id="114b8-156">Start menu and Taskbar settings, Folder options, default desktop icons, additional clocks, and region and Language settings.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-157">Connexion uniquement.</span><span class="sxs-lookup"><span data-stu-id="114b8-157">Logon only.</span></span></p></td>
<td align="left"><p><span data-ttu-id="114b8-158">Désactivé</span><span class="sxs-lookup"><span data-stu-id="114b8-158">Disabled</span></span></p></td>
</tr>
</tbody>
</table>

 

<span data-ttu-id="114b8-159">L’arrière-plan du bureau Windows et les paramètres d’ergonomie sont appliqués lorsque l’utilisateur se connecte, lorsque l’ordinateur est déverrouillé ou lors d’une connexion à distance vers un autre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="114b8-159">The Windows desktop background and Ease of Access settings are applied when the user logs on, when the computer is unlocked, or upon remote connection to another computer.</span></span> <span data-ttu-id="114b8-160">L’agent enregistre ces paramètres lorsque l’utilisateur se déconnecte, lorsque l’ordinateur est verrouillé ou lorsqu’une connexion à distance est déconnectée.</span><span class="sxs-lookup"><span data-stu-id="114b8-160">The agent saves these settings when the user logs off, when the computer is locked, or when a remote connection is disconnected.</span></span> <span data-ttu-id="114b8-161">Par défaut, les paramètres d’arrière-plan du bureau Windows sont itinérants entre les ordinateurs utilisant la même version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="114b8-161">By default, Windows desktop background settings are roamed between computers of the same operating system version.</span></span>

<span data-ttu-id="114b8-162">Les paramètres de bureau et d’ergonomie de Windows sont appliqués lors de l’ouverture de session avant que le Bureau ne s’affiche à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="114b8-162">Windows desktop and Ease of Access settings are applied at logon before the desktop is presented to the user.</span></span> <span data-ttu-id="114b8-163">Pour optimiser l’ouverture de session, ces paramètres ne sont pas itinérants par défaut.</span><span class="sxs-lookup"><span data-stu-id="114b8-163">To optimize the logon experience, these settings are not roamed by default.</span></span> <span data-ttu-id="114b8-164">Les paramètres de bureau et d’ergonomie peuvent être activés en utilisant une stratégie de groupe, PowerShell et WMI.</span><span class="sxs-lookup"><span data-stu-id="114b8-164">Desktop and Ease of Access settings can be enabled by using Group Policy, PowerShell, and WMI.</span></span>

<span data-ttu-id="114b8-165">UE-V ne prend pas en charge l’itinérance des paramètres entre les systèmes d’exploitation utilisant des langues différentes.</span><span class="sxs-lookup"><span data-stu-id="114b8-165">UE-V does not support the roaming of settings between operating systems with different languages.</span></span> <span data-ttu-id="114b8-166">Par exemple, la synchronisation entre l’anglais et l’allemand n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="114b8-166">For example, synchronization between English and German is not supported.</span></span> <span data-ttu-id="114b8-167">La langue de tous les ordinateurs sur lesquels UE-V est itinérante doit correspondre aux paramètres de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="114b8-167">The language of all computers to which UE-V roams the user settings must match.</span></span>

<span data-ttu-id="114b8-168">**Remarques**  Si vous modifiez les modèles d’emplacement des paramètres fournis par Microsoft, la virtualisation de l’utilisation de l’utilisateur peut ne pas fonctionner correctement pour le groupe de paramètres Windows ou application désigné.</span><span class="sxs-lookup"><span data-stu-id="114b8-168">**Note** If you change the settings location templates that are provided by Microsoft, User Experience Virtualization might not work properly for the designated application or Windows settings group.</span></span>

 

## <a href="" id="prevent-unintentional-user-settings-configuration-"></a><span data-ttu-id="114b8-169">Empêcher la configuration involontaire des paramètres utilisateur</span><span class="sxs-lookup"><span data-stu-id="114b8-169">Prevent unintentional user Settings configuration</span></span>


<span data-ttu-id="114b8-170">La virtualisation de l’utilisation de l’utilisateur vérifie la nouvelle information sur les paramètres utilisateur et télécharge ces informations en conséquence à partir d’un emplacement de stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="114b8-170">User Experience Virtualization checks for new user settings information, and downloads that information accordingly from a settings storage location.</span></span> <span data-ttu-id="114b8-171">Ensuite, il applique les paramètres à l’ordinateur local dans les cas suivants:</span><span class="sxs-lookup"><span data-stu-id="114b8-171">Then, it applies the settings to the local computer in the following cases:</span></span>

-   <span data-ttu-id="114b8-172">Chaque fois qu’une application est lancée et dispose d’un modèle UE-V enregistré.</span><span class="sxs-lookup"><span data-stu-id="114b8-172">Every time an application is launched that has a registered UE-V template.</span></span>

-   <span data-ttu-id="114b8-173">Lorsqu’un utilisateur ouvre une session sur son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="114b8-173">When a user logs on to their computer.</span></span>

-   <span data-ttu-id="114b8-174">Lorsqu’un utilisateur déverrouille son ordinateur.</span><span class="sxs-lookup"><span data-stu-id="114b8-174">When a user unlocks their computer.</span></span>

-   <span data-ttu-id="114b8-175">Lorsqu’une connexion est établie à un ordinateur de bureau distant sur lequel UE-V est installé.</span><span class="sxs-lookup"><span data-stu-id="114b8-175">When a connection is made to a remote desktop computer that has UE-V installed.</span></span>

<span data-ttu-id="114b8-176">Si UE-V est installé sur l’ordinateur A et l’ordinateur B et si les paramètres souhaités pour l’application se trouvent sur l’ordinateur A, l’ordinateur a doit d’abord ouvrir et fermer l’application.</span><span class="sxs-lookup"><span data-stu-id="114b8-176">If UE-V is installed on computer A and computer B, and the desired settings for the application are on computer A, then computer A must open and close the application first.</span></span> <span data-ttu-id="114b8-177">Si une application est ouverte et fermée sur l’ordinateur B d’abord, les paramètres de l’application sur l’ordinateur A seront configurés de la même manière que les paramètres de l’application sur l’ordinateur B.</span><span class="sxs-lookup"><span data-stu-id="114b8-177">If an application is opened and closed on computer B first, then the application settings on computer A will be configured to be the same as the application settings on computer B.</span></span>

<span data-ttu-id="114b8-178">Ce scénario s’applique également aux paramètres Windows.</span><span class="sxs-lookup"><span data-stu-id="114b8-178">This scenario also applies to Windows settings.</span></span> <span data-ttu-id="114b8-179">Si les paramètres Windows sur l’ordinateur B doivent être identiques aux paramètres Windows sur l’ordinateur A, l’utilisateur doit d’abord se connecter et se déconnecter de l’ordinateur A.</span><span class="sxs-lookup"><span data-stu-id="114b8-179">If the Windows settings on computer B should be the same as the Windows settings on computer A, then the user should logon and logoff computer A first.</span></span>

<span data-ttu-id="114b8-180">Si les paramètres d’utilisateur souhaités sont appliqués dans un ordre incorrect, ils peuvent être récupérés en effectuant une opération de restauration pour la configuration de l’application ou de l’application spécifique sur l’ordinateur sur lequel les paramètres ont été écrasés.</span><span class="sxs-lookup"><span data-stu-id="114b8-180">If the desired user settings are applied in the wrong order, they can be recovered by performing a restore operation for the specific application or Windows configuration on the computer on which the settings were overwritten.</span></span> <span data-ttu-id="114b8-181">Pour plus d’informations, reportez-vous à [restauration des paramètres d’application et de fenêtre synchronisés avec UE-V 1,0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="114b8-181">For more information, see [Restoring Application and Windows Settings Synchronized with UE-V 1.0](restoring-application-and-windows-settings-synchronized-with-ue-v-10.md).</span></span>

## <span data-ttu-id="114b8-182">Modèles d’emplacement des paramètres d’UE-V personnalisés</span><span class="sxs-lookup"><span data-stu-id="114b8-182">Custom UE-V settings location templates</span></span>


<span data-ttu-id="114b8-183">Vous pouvez créer des modèles d’emplacement des paramètres personnalisés à l’aide du générateur UE-V.</span><span class="sxs-lookup"><span data-stu-id="114b8-183">You can create custom settings location templates by using the UE-V Generator.</span></span> <span data-ttu-id="114b8-184">Après avoir créé et testé un modèle d’emplacement des paramètres personnalisés dans un environnement de test, vous pouvez déployer les modèles d’emplacement des paramètres sur les ordinateurs de l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="114b8-184">After you create and test a custom settings location template in a test environment, you can deploy the settings location templates to computers in the enterprise.</span></span> <span data-ttu-id="114b8-185">Les modèles d’emplacement des paramètres personnalisés doivent être déployés avec une infrastructure de déploiement existante, telle que la méthode de distribution de logiciels d’entreprise (ESD), avec des préférences ou en configurant un catalogue de modèles de paramètres UE-V.</span><span class="sxs-lookup"><span data-stu-id="114b8-185">Custom settings location templates must be deployed with an existing deployment infrastructure, such as enterprise software distribution (ESD) method, with preferences, or by configuring an UE-V settings template catalog.</span></span> <span data-ttu-id="114b8-186">Les modèles déployés avec une stratégie de groupe ou par ESD doivent être enregistrés à l’aide de la version WMI ou PowerShell d’UE-V.</span><span class="sxs-lookup"><span data-stu-id="114b8-186">Templates that are deployed with ESD or Group Policy must be registered by using UE-V WMI or PowerShell.</span></span> <span data-ttu-id="114b8-187">Pour plus d’informations sur les modèles d’emplacement des paramètres personnalisés, voir [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="114b8-187">For more information about custom settings location templates, see [Planning for Custom Template Deployment for UE-V 1.0](planning-for-custom-template-deployment-for-ue-v-10.md).</span></span>

<span data-ttu-id="114b8-188">Pour savoir si une application métier doit être synchronisée, voir [liste de contrôle pour évaluer les applications métier pour UE-V 1,0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span><span class="sxs-lookup"><span data-stu-id="114b8-188">For guidance on whether a line-of-business application should be synchronized, see [Checklist for Evaluating Line-of-Business Applications for UE-V 1.0](checklist-for-evaluating-line-of-business-applications-for-ue-v-10.md).</span></span>

## <span data-ttu-id="114b8-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="114b8-189">Related topics</span></span>


[<span data-ttu-id="114b8-190">Planification pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="114b8-190">Planning for UE-V 1.0</span></span>](planning-for-ue-v-10.md)

[<span data-ttu-id="114b8-191">Planification du déploiement de modèle personnalisé d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="114b8-191">Planning for Custom Template Deployment for UE-V 1.0</span></span>](planning-for-custom-template-deployment-for-ue-v-10.md)

[<span data-ttu-id="114b8-192">Déploiement d'UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="114b8-192">Deploying UE-V 1.0</span></span>](deploying-ue-v-10.md)

 

 





