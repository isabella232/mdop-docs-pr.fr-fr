---
title: À propos de MBAM2.0 SP1
description: À propos de MBAM2.0 SP1
author: dansimp
ms.assetid: 5ba89ed8-bb6e-407b-82c2-e2e36dd1078e
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 73b92cd852d4f75f63f3dcba9f18167012b61401
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810025"
---
# À propos de MBAM2.0 SP1

Cette rubrique décrit les modifications apportées à l’administration et à l’analyse de BitLocker (MBAM) 2,0 Service Pack 1 (SP1). Pour obtenir une description générale de MBAM, reportez-vous à la rubrique [mise en route de MBAM 2,0](getting-started-with-mbam-20-mbam-2.md).

## <a href="" id="what-s-new-in-mbam-2-0-sp1"></a>Nouveautés de MBAM 2,0 SP1

Cette version de MBAM offre les nouvelles fonctionnalités et fonctionnalités suivantes.

### Prise en charge de Windows 8,1, Windows Server 2012 R2 et System Center 2012 R2 Configuration Manager

Microsoft BitLocker administration et analyse (MBAM) 2,0 Service Pack 1 (SP1) ajoute la prise en charge pour Windows 8,1, Windows Server 2012 R2 et System Center 2012 R2 Configuration Manager.

### Prise en charge de Microsoft SQL Server 2008 R2 SP2

Microsoft BitLocker administration et analyse (MBAM) 2,0 Service Pack 1 (SP1) ajoute la prise en charge de Microsoft SQL Server 2008 R2 SP2. Vous devez utiliser Microsoft SQL Server 2008 R2 ou une version ultérieure si vous exécutez Microsoft System Center Configuration Manager 2007 R2.

### Report de commentaires client

MBAM 2,0 SP1 inclut un ensemble de correctifs pour résoudre les problèmes détectés depuis la version d’administration et de surveillance de Microsoft BitLocker (MBAM) 2,0. Dans le cadre de ces modifications, le champ nom de l’ordinateur apparaît désormais dans les rapports sur les détails de conformité de l’ordinateur et BitLocker Enterprise lors de l’exécution de MBAM avec Microsoft System Center Configuration Manager 2007.

### Une exception de pare-feu doit être définie sur les ports du portail libre-service et sur le site Web d’administration et de surveillance.

Lorsque vous configurez le portail libre-service et le site Web d’administration et de surveillance, vous devez définir une exception de pare-feu pour autoriser les communications via les ports spécifiés. Auparavant, l’installation MBAM Server a ouvert les ports automatiquement dans le pare-feu Windows.

### L’emplacement des rapports MBAM a changé dans Configuration Manager

MBAM-XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX MBAM. Les noms de sous-dossiers représentent la langue des rapports dans le sous-dossier.

### Possibilité d’installer MBAM sur un serveur de site principal lors de l’installation d’MBAM avec Configuration Manager

Vous pouvez installer MBAM sur un serveur de site principal ou un serveur de site d’administration centrale lorsque vous installez MBAM avec la topologie intégrée de Configuration Manager. Auparavant, vous étiez obligé d’installer MBAM sur un serveur de site d’administration centrale.

**Important**  
Le serveur sur lequel vous installez MBAM doit être le serveur de niveau supérieur de votre hiérarchie.



L’installation de MBAM fonctionne différemment pour Microsoft System Center Configuration Manager 2007 et Microsoft System Center 2012 Configuration Manager comme suit:

-   **Configuration manager 2007** : Si vous installez MBAM sur un serveur de site principal qui fait partie d’une hiérarchie de gestionnaires de configuration plus volumineux et possède un serveur parent de site central, MBAM résout le serveur parent du site central et effectue toutes les actions d’installation sur ce serveur parent. Les actions d’installation incluent la vérification des éléments requis et l’installation des objets et des rapports du gestionnaire de configuration. Par exemple, si vous installez MBAM sur un serveur de site principal qui est un enfant d’un serveur parent de site central, MBAM installe tous les objets et rapports de configuration du serveur parent. Si vous installez MBAM sur le serveur parent, MBAM effectue toutes les actions d’installation sur ce serveur parent.

-   **Gestionnaire de configuration de System Center 2012** : Si vous installez MBAM sur un serveur de site principal ou sur un serveur d’administration centrale, MBAM effectue toutes les actions d’installation sur ce serveur de site.

### <a href="" id="-------------configuration-manager-console-must-be-installed-on-the--computer-on-which-you-install-the-mbam-server"></a> La console Configuration Manager doit être installée sur l’ordinateur sur lequel vous installez le serveur MBAM

Lorsque vous installez MBAM avec la topologie intégrée de Configuration Manager, vous devez installer la console Configuration Manager sur le même ordinateur sur lequel MBAM sera installé. Si vous utilisez l’architecture recommandée, décrite dans la rubrique [mise en route-utilisez MBAM avec Configuration Manager](getting-started---using-mbam-with-configuration-manager.md), vous devez installer MBAM sur le serveur de site principal de Configuration Manager.

### Nouveaux paramètres de ligne de commande du programme d’installation pour la topologie intégrée de Configuration Manager

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre de ligne de commande</th>
<th align="left">Description</th>
<th align="left">Exemple</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>CM_SSRS_REMOTE_SERVER_NAME</p></td>
<td align="left"><p>Vous permet d’installer les rapports du gestionnaire de configuration sur un serveur SQL Server Reporting Services (SSRS) distant qui fait partie du site de Configuration Manager sur lequel MBAM est installé. Vous pouvez définir la valeur sur le nom de domaine complet du serveur de rôles de point SSRS distant.</p></td>
<td align="left"><p>MbamSetup.exe CM_SSRS_REMOTE_SERVER_NAME = ssrsServer. contoso. com</p></td>
</tr>
<tr class="even">
<td align="left"><p>CM_REPORTS_ONLY</p></td>
<td align="left"><p>Vous permet d’installer uniquement les rapports du gestionnaire de configuration, sans autres objets de Configuration Manager, tels que les éléments de base, de collection et de configuration.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Vous devez combiner ce paramètre avec le paramètre CM_REPORTS_COLLECTION_ID.</p>
</div>
<div>

</div>
<p>Valeurs de paramètre valides:</p>
<ul>
<li><p>Vrai</p></li>
<li><p>Faux</p></li>
</ul>
<p>Vous pouvez combiner ce paramètre à l’aide du paramètre CM_SSRS_REMOTE_SERVER_NAME si vous voulez installer les rapports uniquement sur un serveur de rôles de point de contrôle distant.</p>
<p>Si vous ne définissez pas le paramètre ou si vous lui attribuez la valeur false, le programme d’installation de MBAM installe tous les objets du gestionnaire de configuration, y compris les rapports.</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
<tr class="odd">
<td align="left"><p>CM_REPORTS_COLLECTION_ID</p></td>
<td align="left"><p>ID de collection existant qui identifie la collection pour laquelle les données de conformité de rapport seront affichées. Vous pouvez spécifier n’importe quel ID de collection. Vous n’êtes pas tenu d’utiliser l’ID de collection «MBAM pris en charge».</p></td>
<td align="left"><p>MbamSetup.exe CM_REPORTS_ONLY = true</p>
<p>CM_REPORTS_COLLECTION_ID = SMS00001</p></td>
</tr>
</tbody>
</table>



### Possibilité d’activer ou de désactiver le texte d’avis de portail libre-service

MBAM 2,0 SP1 vous permet de désactiver le texte de la note sur le portail libre-service. Auparavant, le texte d’avis affiché par défaut, et vous ne pouviez pas le désactiver.

**Pour désactiver le texte de la note**

1.  Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez Internet Information Services (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et analysez les paramètres de l' &gt; &gt; application selfservice**.

2.  Dans la colonne **nom** , sélectionnez **DisplayNotice**, puis attribuez la valeur **false**.

### Possibilité de localiser l’instruction HelpdeskText qui pointe les utilisateurs vers d’autres informations de portail libre-service

Vous pouvez configurer une version localisée de l’instruction «HelpdeskText» du portail libre-service, qui indique aux utilisateurs finaux comment obtenir de l’aide sur le portail libre-service. Si vous configurez du texte localisé pour l’instruction, comme décrit dans les instructions ci-dessous, MBAM affiche la version localisée. Si MBAM ne trouve pas la version localisée, il affiche la valeur figurant dans le paramètre **HelpdeskText** .

**Pour afficher une version localisée de l’instruction HelpdeskText**

1.  Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez les services Internet (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et contrôle des paramètres de l' &gt; &gt; application selfservice**.

2.  Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .

3.  Dans le champ **nom** , tapez **HelpdeskText**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour le texte. Par exemple, pour créer une instruction HelpdeskText localisée en espagnol, vous nommerez le paramètre HelpdeskText \ _es-es. Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Dans le champ **valeur** , tapez le texte localisé que vous souhaitez afficher aux utilisateurs finaux.

### Possibilité de localiser le portail libre-service HelpdeskURL

Vous pouvez configurer une version localisée du portail libre-service HelpdeskURL pour l’afficher par défaut aux utilisateurs finaux. Si vous créez une version localisée, comme décrit dans les instructions ci-dessous, MBAM recherche et affiche la version localisée. Si MBAM ne trouve pas de version localisée, il affiche l’URL configurée pour le paramètre HelpDeskURL.

**Pour afficher un HelpdeskURL localisé**

1.  Sur le serveur sur lequel vous avez installé le portail libre-service, ouvrez les services Internet (IIS) et naviguez jusqu’à **sites &gt; Microsoft BitLocker administration et contrôle des paramètres de l' &gt; &gt; application selfservice**.

2.  Dans le volet **actions** , cliquez sur **Ajouter** pour ouvrir la boîte de dialogue Ajouter un **paramètre d’application** .

3.  Dans le champ **nom** , tapez **HelpdeskURL**\ _ &lt; *Language* &gt; , où &lt; *Language* &gt; correspond au code de langue approprié pour l’URL. Par exemple, pour créer une HelpdeskURL localisée en espagnol, vous nommerez le paramètre HelpdeskURL \ _es-es. Pour obtenir la liste des codes de langue valides que vous pouvez utiliser, voir référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947).

4.  Dans le champ **valeur** , tapez le HelpdeskURL localisé que vous souhaitez afficher aux utilisateurs finaux.

### Possibilité de localiser le texte d’avis du portail libre-service

Vous pouvez configurer le texte des notifications localisées pour qu’ils apparaissent par défaut aux utilisateurs finaux sur le portail libre-service. Le fichier notice.txt, qui affiche le texte de l’avis, se trouve dans le répertoire racine suivant:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

Pour afficher un texte d’avis localisé, vous devez créer un fichier notice.txt localisé et l’enregistrer sous un dossier de langue spécifique dans l’annuaire suivant:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

MBAM affiche le texte de l’avis en fonction des règles suivantes:

-   Si vous créez un fichier notice.txt localisé dans le dossier de langue approprié, MBAM affiche le texte du message localisé.

-   Si MBAM ne trouve pas de version localisée du fichier notice.txt, il affiche le texte dans le fichier de notice.txt par défaut.

-   Si MBAM ne trouve pas de fichier notice.txt par défaut, il affiche le texte par défaut dans le portail libre-service.

**Remarque**  
Si le navigateur d’un utilisateur final est défini pour une langue qui ne possède pas de sous-dossier de langue correspondant ou notice.txt, le texte qui se trouve dans le fichier notice.txt dans le répertoire racine suivant s’affiche:

&lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\



**Pour créer un fichier notice.txt localisé**

1.  Sur le serveur sur lequel vous avez installé le portail libre-service, créez un &lt; *language* &gt; dossier de langue dans l’annuaire suivant, où &lt; *Language* &gt; représente le nom de la langue localisée:

    &lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\

    **Remarque**  
    Certains dossiers de langue existent déjà et il n’est pas nécessaire d’en créer un. Si vous avez besoin de créer un dossier de langue, reportez-vous à la rubrique référence sur l' [API NLS (National Language Support)](https://go.microsoft.com/fwlink/?LinkId=317947) pour obtenir la liste des noms valides que vous pouvez utiliser pour le &lt; dossier *Language* &gt; .



2.  Créez un fichier notice.txt contenant le texte d’avis localisé.

3.  Enregistrez le fichier notice.txt dans le &lt; dossier *Language* &gt; . Par exemple, pour créer un fichier notice.txt localisé en espagnol, vous devez enregistrer le fichier notice.txt localisé dans le dossier suivant:

    &lt;Répertoire d’installation *de MBAM self-service* &gt; \\Self service Website\\es-es

## Mise à niveau vers MBAM 2,0 SP1


Vous pouvez effectuer une mise à niveau vers MBAM 2,0 SP1 à partir de n’importe quelle version antérieure de MBAM.

### Mise à niveau de l’infrastructure MBAM

Vous pouvez mettre à niveau l’infrastructure du serveur MBAM vers MBAM 2,0 SP1 comme suit:

**Remplacement manuel du serveur sur place**: vous devez désinstaller manuellement l’infrastructure du serveur MBAM existante, puis installer l’infrastructure du serveur MBAM 2,0 SP1. Vous n’avez pas besoin de supprimer les bases de données pour procéder à la mise à niveau. Au lieu de cela, vous sélectionnez les bases de données existantes, lesquelles la version précédente de MBAM a été créée. Le programme d’installation de la mise à niveau MBAM 2,0 SP1 effectue une migration vers MBAM 2,0 SP1.

**Mise à niveau du client distribué**: Si vous utilisez la topologie MBAM autonome, vous pouvez mettre à niveau les clients MBAM progressivement après l’installation de l’infrastructure de serveur MBAM 2,0 SP1.

Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM, les clients MBAM 1,0 ou 2,0 seront signalés au serveur MBAM 2,0 SP1 et stockeront les données de récupération, mais la conformité sera basée sur les stratégies disponibles pour la version du client MBAM actuellement installée. Pour activer la création de rapports sur les stratégies MBAM 2,0 SP1, vous devez mettre à niveau les ordinateurs clients vers MBAM 2,0 SP1. Vous pouvez mettre à niveau les ordinateurs client vers le client MBAM 2,0 SP1 sans désinstaller le client précédent, et le client va commencer à s’appliquer et à signaler, selon les stratégies 2,0 SP1 MBAM.

Pour plus d’informations sur la mise à niveau des serveurs MBAM, voir [mise à niveau à partir d’une version antérieure d’MBAM](upgrading-from-previous-versions-of-mbam.md).

### Mise à niveau du client MBAM vers MBAM 2,0 SP1

Pour mettre à niveau les ordinateurs des utilisateurs finaux vers le client MBAM 2,0 SP1, exécutez **MbamClientSetup.exe** sur chaque ordinateur client. Le programme d’installation met automatiquement à jour le client vers le client MBAM 2,0 SP1. Après l’installation, les ordinateurs clients n’ont pas besoin d’être redémarrés et le client MBAM 2,0 SP1 commence à s’appliquer et à rapporter des stratégies MBAM 2,0 SP1.

Si vous utilisez MBAM avec Configuration Manager, vous devez mettre à niveau les ordinateurs client MBAM vers MBAM 2,0 SP1.

Pour plus d’informations sur la mise à niveau des ordinateurs clients MBAM, voir [mise à niveau à partir d’une version antérieure d’MBAM](upgrading-from-previous-versions-of-mbam.md).

## Installation ou mise à niveau vers MBAM 2,0 SP1 avec Configuration Manager


Cette section décrit la configuration requise lors de l’installation d’MBAM 2,0 SP1 en tant que nouvelle installation ou en tant que mise à niveau vers une version antérieure de MBAM 2,0 SP1.

### Fichiers nécessaires pour l’installation d’MBAM 2,0 SP1 si vous utilisez MBAM avec Configuration Manager

Si vous installez MBAM pour la première fois et que vous utilisez MBAM 2,0 SP1 avec System Center Configuration Manager, vous devez créer ou modifier des fichiers MOF pour permettre à MBAM de fonctionner correctement avec Configuration Manager.

-   **fichier Configuration. mof**

    -   Si vous utilisez Configuration Manager 2007, vous devez modifier le fichier Configuration. mof en exécutant l’étape 3 à partir de la **mise à jour du fichier de configuration. mof si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007**, qui suit cet élément.

    -   Si vous utilisez System Center 2012 Configuration Manager, vous pouvez modifier le fichier Configuration. mof en suivant les instructions dans [modifier le fichier Configuration. mof](edit-the-configurationmof-file.md).

-   **fichier SMS \ _def. mof** : suivez les instructions de la procédure de [création ou de modification du fichier SMS \ _def. mof](create-or-edit-the-sms-defmof-file.md).

### Mettez à jour le fichier Configuration. mof si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007

Si vous effectuez une mise à niveau vers MBAM 2,0 SP1 et que vous utilisez MBAM avec Configuration Manager 2007, vous devez mettre à jour le fichier Configuration. mof pour vous assurer que MBAM 2,0 SP1 fonctionne correctement.

**Pour mettre à jour le fichier Configuration. mof:**

1.  Sur le serveur Configuration Manager, naviguez jusqu’à l’emplacement du fichier Configuration. mof:

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    Sur une installation par défaut, l’emplacement d’installation est%systemdrive%\\Program fichiers (x86) \\Microsoft Configuration Manager.

2.  Examinez le bloc de code que vous avez ajouté au fichier Configuration. mof et supprimez-le. Le bloc de code est semblable à celui présenté dans l’étape suivante.

3.  Copiez le bloc de code suivant, puis ajoutez-le au fichier Configuration. mof pour ajouter les classes MBAM requises suivantes au fichier:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL) 

    [Union, ViewSources{"select DeviceId, BitlockerPersistentVolumeId, BitLockerManagementPersistentVolumeId, BitLockerManagementVolumeType, DriveLetter, Compliant, ReasonsForNonCompliance, KeyProtectorTypes, EncryptionMethod, ConversionStatus, ProtectionStatus, IsAutoUnlockEnabled from Mbam_Volume"}, ViewSpaces{"\\\\.\\root\\microsoft\\mbam"}, dynamic, Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class Win32_BitLockerEncryptionDetails
    {
        [PropertySources{"DeviceId"},key]
        String     DeviceId;
        [PropertySources{"BitlockerPersistentVolumeId"}]
        String     BitlockerPersistentVolumeId;
        [PropertySources{"BitLockerManagementPersistentVolumeId"}]
        String     MbamPersistentVolumeId;
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        [PropertySources{"BitLockerManagementVolumeType"}]
        SInt32     MbamVolumeType;
        [PropertySources{"DriveLetter"}]
        String     DriveLetter;
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        [PropertySources{"Compliant"}]
        SInt32     Compliant;
        [PropertySources{"ReasonsForNonCompliance"}]
        SInt32     ReasonsForNonCompliance[];
        [PropertySources{"KeyProtectorTypes"}]
        SInt32     KeyProtectorTypes[];
        [PropertySources{"EncryptionMethod"}]
        SInt32     EncryptionMethod;
        [PropertySources{"ConversionStatus"}]
        SInt32     ConversionStatus;
        [PropertySources{"ProtectionStatus"}]
        SInt32     ProtectionStatus;
        [PropertySources{"IsAutoUnlockEnabled"}]
        Boolean     IsAutoUnlockEnabled;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
     [DYNPROPS]
    Class Win32Reg_MBAMPolicy
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate;
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

     [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy
    {
        KeyName="BitLocker policy";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [DYNPROPS]
    Class Win32Reg_MBAMPolicy_64
    {
        [key]
        string KeyName;

        //General encryption requirements
        UInt32    OsDriveEncryption;
        UInt32    FixedDataDriveEncryption;
        UInt32    EncryptionMethod;

        //Required protectors properties
        UInt32    OsDriveProtector;
        UInt32    FixedDataDriveAutoUnlock;
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        Uint32    MBAMPolicyEnforced;
        string    LastConsoleUser;
        datetime  UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        UInt32    MBAMMachineError;

        // Encoded computer name
        string    EncodedComputerName;
    };

    [DYNPROPS]
    Instance of Win32Reg_MBAMPolicy_64
    {
        KeyName="BitLocker policy 64";

        //General encryption requirements
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptOsDrive"),Dynamic,Provider("RegPropProv")]
        OsDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|ShouldEncryptFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveEncryption;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|EncryptionMethod"),Dynamic,Provider("RegPropProv")]
        EncryptionMethod;

        //Required protectors properties
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|OSVolumeProtectorPolicy"),Dynamic,Provider("RegPropProv")]
        OsDriveProtector;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE\\MDOPBitLockerManagement|AutoUnlockFixedDataDrive"),Dynamic,Provider("RegPropProv")]
        FixedDataDriveAutoUnlock;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Policies\\Microsoft\\FVE|FDVPassphrase"),Dynamic,Provider("RegPropProv")]
        FixedDataDrivePassphrase;

        //MBAM agent fields
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMPolicyEnforced"),Dynamic,Provider("RegPropProv")]
        MBAMPolicyEnforced;
         [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|LastConsoleUser"),Dynamic,Provider("RegPropProv")]
        LastConsoleUser;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|UserExemptionDate"),Dynamic,Provider("RegPropProv")]
        UserExemptionDate; //Registry value should be string in the format of yyyymmddHHMMSS.mmmmmmsUUU
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|MBAMMachineError"),Dynamic,Provider("RegPropProv")]
        MBAMMachineError;
        [PropertyContext("Local|HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\MBAM|EncodedComputerName"),Dynamic,Provider("RegPropProv")]
        EncodedComputerName;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,OperatingSystemSKU from Win32_OperatingSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_OperatingSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"OperatingSystemSKU"}]
        uint32     SKU;
    };

    # pragma namespace ("\\\\.\\root\\cimv2")
    # pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [Union, ViewSources{"select Name,PCSystemType from Win32_ComputerSystem"}, ViewSpaces{"\\\\.\\root\\cimv2"},
    dynamic,Provider("MS_VIEW_INSTANCE_PROVIDER")]
    class CCM_ComputerSystemExtended
    {
        [PropertySources{"Name"},key]
        string     Name;
        [PropertySources{"PCSystemType"}]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================

    ```

### Traduction de MBAM 2,0 SP1

MBAM 2,0 SP1 est désormais disponible dans les langues suivantes:

-   Anglais (États-Unis) en-US
-   Français (France) fr-FR
-   IT Italien (Italie)-IT
-   Allemand (Allemagne) de-DE
-   Espagnol, international (Espagne) es-ES
-   Coréen (Corée) ko-KR
-   Japonais (Japon) ja-JP
-   Portugais (Brésil) pt-BR
-   Russe (Russie) ru-RU
-   Chinois traditionnel zh-TW
-   Chinois simplifié zh-NC

## Obtention de technologies MDOP

MBAM 2,0 SP1 fait partie du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur le programme d’assurance logiciel Microsoft et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049) ( https://go.microsoft.com/fwlink/?LinkId=322049) .

## Rubriques connexes

[Notes de publication de MBAM2.0 SP1](release-notes-for-mbam-20-sp1.md)









