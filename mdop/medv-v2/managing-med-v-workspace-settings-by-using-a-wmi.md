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
# Gestion des paramètres d'espace de travail MED-V à l'aide de WMI


Vous pouvez utiliser WMI (Windows Management Instrumentation) dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0 pour gérer vos paramètres de configuration actuels.

## Pour gérer les paramètres d’espace de travail MED-V avec un WMI


Un outil de navigation WMI vous permet d’afficher et de modifier les paramètres dans un espace de travail MED-V. Le fournisseur WMI est implémenté à l’aide de l’infrastructure d’extension du fournisseur WMI à partir de Microsoft .NET Framework 3,5.

Le fournisseur WMI est implémenté dans l’espace de noms **root\\microsoft\\medv** et implémente le **paramètre**de classe. Le **paramètre** de classe contient des propriétés qui correspondent aux paramètres du Registre système sous la clé de Registre HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\medv.

**Attention**  Les outils de navigation WMI peuvent être utilisés pour supprimer ou modifier des classes et des instances. La suppression ou la modification de certaines classes et instances peut entraîner la perte de données importantes et provoquer une fonction de MED-V.

 

Pour afficher et modifier les paramètres de configuration de MED-V, vous pouvez utiliser l’outil de navigation WMI de votre choix en procédant comme suit.

1.  Ouvrez l’outil de navigation WMI de votre choix avec des autorisations d’administrateur.

2.  Connectez-vous à l’espace de noms **root\\microsoft\\medv**.

3.  Énumérer les instances permettant de se connecter à l’instance en cours d’exécution. Vous voulez vous connecter à l’instance du **paramètre**de la classe.

    Une fenêtre de l' **éditeur d’objets** s’ouvre. Les paramètres de configuration de MED-V apparaissent sous forme de **Propriétés**.

Effectuez les étapes suivantes pour modifier un paramètre de configuration MED-V dans WMI.

1.  Dans la liste des **Propriétés** de la fenêtre de l' **éditeur d’objets** , double-cliquez sur le nom du paramètre de configuration que vous voulez modifier. Par exemple, pour modifier les informations de redirection d’URL MED-V, double-cliquez sur la propriété **UxRedirectUrls**.

    Une fenêtre d' **éditeur de propriété** s’ouvre.

2.  Modifiez la valeur afin de mettre à jour les informations de configuration. Par exemple, pour modifier les informations de redirection d’URL MED-V, ajoutez ou supprimez une adresse Web dans la liste.

3.  Enregistrez les paramètres de propriété mis à jour.

Lorsque vous avez terminé d’afficher ou de modifier les paramètres de configuration de MED-V, fermez l’outil navigation WMI.

**Important**  Dans certains cas, un redémarrage de l’espace de travail MED-V est requis pour que les modifications apportées aux paramètres de configuration MED-V soient prises en compte.

 

Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **Setting** .

``` syntax
[dynamic: ToInstance, provider("TroubleShooting, Version=2.0.392.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35"), singleton: DisableOverride ToInstance ToSubClass]
class Setting : ConfigValueProvider
{
                boolean UxSmartCardLogonEnabled = TRUE;
                [read] string User;
                [implemented] void Clear([in] string propertyName);
};
```

La classe **Setting** hérite de la classe **ConfigValueProvider** . Le code suivant montre le fichier MOF (Managed Object Format) qui définit la classe **ConfigValueProvider** .

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

## Rubriques connexes


[Gestion des paramètres de configuration d'espace de travail MED-V](managing-med-v-workspace-configuration-settings.md)

[Gérer les paramètres de l'espace de travail MED-V](manage-med-v-workspace-settings.md)

 

 





