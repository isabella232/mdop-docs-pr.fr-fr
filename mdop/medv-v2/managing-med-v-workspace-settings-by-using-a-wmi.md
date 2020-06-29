---
title: Gestion des paramètres d'espace de travail MED-V à l'aide de WMI
description: Gestion des paramètres d'espace de travail MED-V à l'aide de WMI
author: dansimp
ms.assetid: 05a665a3-2309-46c1-babb-a3e3bbb0b1f9
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e74e6fa4944ce0dacd5503baec73044b231abe83
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811573"
---
# <span data-ttu-id="5acde-103">Gestion des paramètres d'espace de travail MED-V à l'aide de WMI</span><span class="sxs-lookup"><span data-stu-id="5acde-103">Managing MED-V Workspace Settings by Using a WMI</span></span>


<span data-ttu-id="5acde-104">Vous pouvez utiliser WMI (Windows Management Instrumentation) dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 pour gérer vos paramètres de configuration actuels.</span><span class="sxs-lookup"><span data-stu-id="5acde-104">You can use Windows Management Instrumentation (WMI) in Microsoft Enterprise Desktop Virtualization (MED-V) 2.0 to manage your current configuration settings.</span></span>

## <span data-ttu-id="5acde-105">Pour gérer les paramètres d’espace de travail MED-V avec un WMI</span><span class="sxs-lookup"><span data-stu-id="5acde-105">To manage MED-V workspace settings with a WMI</span></span>


<span data-ttu-id="5acde-106">Un outil de navigation WMI vous permet d’afficher et de modifier les paramètres dans un espace de travail MED-V.</span><span class="sxs-lookup"><span data-stu-id="5acde-106">A WMI browsing tool lets you view and edit the settings in a MED-V workspace.</span></span> <span data-ttu-id="5acde-107">Le fournisseur WMI est implémenté à l’aide de l’infrastructure d’extension du fournisseur WMI à partir de Microsoft .NET Framework 3,5.</span><span class="sxs-lookup"><span data-stu-id="5acde-107">The WMI provider is implemented by using the WMI Provider Extension framework from the Microsoft .Net Framework 3.5.</span></span>

<span data-ttu-id="5acde-108">Le fournisseur WMI est implémenté dans l’espace de noms **root\\microsoft\\medv** et implémente le **paramètre**de classe.</span><span class="sxs-lookup"><span data-stu-id="5acde-108">The WMI provider is implemented in the **root\\microsoft\\medv** namespace and implements the class **Setting**.</span></span> <span data-ttu-id="5acde-109">Le **paramètre** de classe contient des propriétés qui correspondent aux paramètres du Registre système sous la clé de Registre HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.</span><span class="sxs-lookup"><span data-stu-id="5acde-109">The class **Setting** contains properties that correspond to the settings in the system registry under the HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Medv registry key.</span></span>

<span data-ttu-id="5acde-110">**Attention**  Les outils de navigation WMI peuvent être utilisés pour supprimer ou modifier des classes et des instances.</span><span class="sxs-lookup"><span data-stu-id="5acde-110">**Caution** WMI browsing tools can be used to delete or modify classes and instances.</span></span> <span data-ttu-id="5acde-111">La suppression ou la modification de certaines classes et instances peut entraîner la perte de données importantes et provoquer une fonction de MED-V.</span><span class="sxs-lookup"><span data-stu-id="5acde-111">Deleting or modifying certain classes and instances can result in the loss of valuable data and cause MED-V to function unpredictably.</span></span>

 

<span data-ttu-id="5acde-112">Pour afficher et modifier les paramètres de configuration de MED-V, vous pouvez utiliser l’outil de navigation WMI de votre choix en procédant comme suit.</span><span class="sxs-lookup"><span data-stu-id="5acde-112">You can use your preferred WMI browsing tool to view and edit MED-V configuration settings by following these steps.</span></span>

1.  <span data-ttu-id="5acde-113">Ouvrez l’outil de navigation WMI de votre choix avec des autorisations d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="5acde-113">Open your preferred WMI browsing tool with administrator permissions.</span></span>

2.  <span data-ttu-id="5acde-114">Connectez-vous à l’espace de noms **root\\microsoft\\medv**.</span><span class="sxs-lookup"><span data-stu-id="5acde-114">Connect to the namespace **root\\microsoft\\medv**.</span></span>

3.  <span data-ttu-id="5acde-115">Énumérer les instances permettant de se connecter à l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5acde-115">Enumerate the instances to connect to the running instance.</span></span> <span data-ttu-id="5acde-116">Vous voulez vous connecter à l’instance du **paramètre**de la classe.</span><span class="sxs-lookup"><span data-stu-id="5acde-116">You want to connect to the instance of the class **Setting**.</span></span>

    <span data-ttu-id="5acde-117">Une fenêtre de l' **éditeur d’objets** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5acde-117">An **Object Editor** window opens.</span></span> <span data-ttu-id="5acde-118">Les paramètres de configuration de MED-V apparaissent sous forme de **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="5acde-118">The MED-V configuration settings are listed as **Properties**.</span></span>

<span data-ttu-id="5acde-119">Effectuez les étapes suivantes pour modifier un paramètre de configuration MED-V dans WMI.</span><span class="sxs-lookup"><span data-stu-id="5acde-119">Perform the following steps to edit a MED-V configuration setting in the WMI.</span></span>

1.  <span data-ttu-id="5acde-120">Dans la liste des **Propriétés** de la fenêtre de l' **éditeur d’objets** , double-cliquez sur le nom du paramètre de configuration que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="5acde-120">In the list of **Properties** on the **Object Editor** window, double-click the name of the configuration setting you want to edit.</span></span> <span data-ttu-id="5acde-121">Par exemple, pour modifier les informations de redirection d’URL MED-V, double-cliquez sur la propriété **UxRedirectUrls**.</span><span class="sxs-lookup"><span data-stu-id="5acde-121">For example, to edit MED-V URL redirection information, double-click the property **UxRedirectUrls**.</span></span>

    <span data-ttu-id="5acde-122">Une fenêtre d' **éditeur de propriété** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="5acde-122">A **Property Editor** window opens.</span></span>

2.  <span data-ttu-id="5acde-123">Modifiez la valeur afin de mettre à jour les informations de configuration.</span><span class="sxs-lookup"><span data-stu-id="5acde-123">Edit the value to update the configuration information.</span></span> <span data-ttu-id="5acde-124">Par exemple, pour modifier les informations de redirection d’URL MED-V, ajoutez ou supprimez une adresse Web dans la liste.</span><span class="sxs-lookup"><span data-stu-id="5acde-124">For example, to edit MED-V URL redirection information, add or remove a web address in the list.</span></span>

3.  <span data-ttu-id="5acde-125">Enregistrez les paramètres de propriété mis à jour.</span><span class="sxs-lookup"><span data-stu-id="5acde-125">Save the updated property settings.</span></span>

<span data-ttu-id="5acde-126">Lorsque vous avez terminé d’afficher ou de modifier les paramètres de configuration de MED-V, fermez l’outil navigation WMI.</span><span class="sxs-lookup"><span data-stu-id="5acde-126">After you have finished viewing or editing MED-V configuration settings, close the WMI browsing tool.</span></span>

<span data-ttu-id="5acde-127">**Important**  Dans certains cas, un redémarrage de l’espace de travail MED-V est requis pour que les modifications apportées aux paramètres de configuration MED-V soient prises en compte.</span><span class="sxs-lookup"><span data-stu-id="5acde-127">**Important** In some cases, a restart of the MED-V workspace is required for changes to MED-V configuration settings to take effect.</span></span>

 

<span data-ttu-id="5acde-128">Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **Setting** .</span><span class="sxs-lookup"><span data-stu-id="5acde-128">The following code shows the Managed Object Format (MOF) file that defines the **Setting** class.</span></span>

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

<span data-ttu-id="5acde-129">La classe **Setting** hérite de la classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="5acde-129">The **Setting** class inherits from the **ConfigValueProvider** class.</span></span> <span data-ttu-id="5acde-130">Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **ConfigValueProvider** .</span><span class="sxs-lookup"><span data-stu-id="5acde-130">The following code shows the Managed Object Format (MOF) file that defines the **ConfigValueProvider** class.</span></span>

``` syntax
[abstract]
class ConfigValueProvider
{
                [write] string DiagEventLogLevel;
                [write] boolean FtsAddUserToAdminGroupEnabled;
                [write] string FtsComputerNameMask;
                [write] sint32 FtsDeleteVMStateTimeout;
                [write] sint32 FtsDetachVfdTimeout;
                [write] string FtsDialogUrl;
                [write] sint32 FtsExplorerTimeout;
                [write] string FtsFailureDialogMsg;
                [write] string FtsLogFilePaths[];
                [write] sint32 FtsMaxPostponeTime;
                [write] sint32 FtsMaxRetryCount;
                [write] string FtsMode;
                [write] sint32 FtsNonInteractiveRetryTimeoutInc;
                [write] sint32 FtsNonInteractiveTimeout;
                [write] string FtsPostponeUtcDateTimeLimit;
                [write] string FtsRetryDialogMsg;
                [write] boolean FtsSetComputerNameEnabled;
                [write] boolean FtsSetJoinDomainEnabled;
                [write] boolean FtsSetMachineObjectOUEnabled;
                [write] boolean FtsSetRegionalSettingsEnabled;
                [write] boolean FtsSetUserDataEnabled;
                [write] string FtsStartDialogMsg;
                [write] sint32 FtsTaskCancelTimeout;
                [write] sint32 FtsTaskVMTurnOffTimeout;
                [write] sint32 FtsUpgradeTimeout;
                [write] boolean UxAppPublishingEnabled;
                [write] boolean UxAudioSharingEnabled;
                [write] boolean UxClipboardSharingEnabled;
                [write] boolean UxCredentialCacheEnabled;
                [write] sint32 UxDialogTimeout;
                [write] sint32 UxHideVmTimeout;
                [write] boolean UxLogonStartEnabled;
                [write] boolean UxPrinterSharingEnabled;
                [write] sint32 UxRebootAbsoluteDelayTimeout;
                [write] string UxRedirectUrls[];
                [write] boolean UxShowExit;
                [write] boolean UxSmartCardLogonEnabled;
                [write] boolean UxSmartCardSharingEnabled;
                [write] boolean UxUSBDeviceSharingEnabled;
                [write] string VmCloseAction;
                [write] sint32 VmGuestMemFromHostMem[];
                [write] sint32 VmGuestUpdateDuration;
                [write] string VmGuestUpdateTime;
                [write] sint32 VmHostMemToGuestMem[];
                [write] boolean VmHostMemToGuestMemCalcEnabled;
                [write] sint32 VmMemory;
                [write] boolean VmMultiUserEnabled;
                [write] string VmNetworkingMode;
                [write] sint32 VmTaskTimeout;
};
```

## <span data-ttu-id="5acde-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5acde-131">Related topics</span></span>


[<span data-ttu-id="5acde-132">Gestion des paramètres de configuration d'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5acde-132">Managing MED-V Workspace Configuration Settings</span></span>](managing-med-v-workspace-configuration-settings.md)

[<span data-ttu-id="5acde-133">Gérer les paramètres de l'espace de travail MED-V</span><span class="sxs-lookup"><span data-stu-id="5acde-133">Manage MED-V Workspace Settings</span></span>](manage-med-v-workspace-settings.md)

 

 





