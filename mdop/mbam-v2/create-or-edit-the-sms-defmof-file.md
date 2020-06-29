---
title: Créer ou modifier le fichier SMS \ _def. mof
description: Créer ou modifier le fichier SMS \ _def. mof
author: dansimp
ms.assetid: d1747e43-484e-4031-a63b-6342fe588aa2
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/04/2017
ms.openlocfilehash: 15f1d1a1c19cb9b19b7d83534e035d5410720ce9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810001"
---
# Créer ou modifier le fichier SMS \ _def. mof


Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof.

Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier.

Dans Configuration Manager 2007, le fichier existe déjà et vous n’avez plus qu’à le modifier. **Ne remplacez pas le fichier existant**.

Dans les sections ci-dessous, suivez les instructions correspondant à la version de Configuration Manager que vous utilisez.

**Pour créer le fichier SMS \ _def. mof pour SystemCenter2012 ConfigurationManager**

1.  Sur le serveur Configuration Manager, accédez à l’emplacement où vous voulez créer le fichier SMS \ _def. mof, par exemple le bureau.

2.  Créez un fichier texte appelé **SMS \ _def. mof** et copiez le code suivant pour remplir le fichier avec les classes sms \ _def. mof MBAM suivantes:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
    };
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")

    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0")]

    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;

        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;

        //MBAM agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser;
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };
    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  Importez le fichier **SMS \ _def. mof** en procédant comme suit:

    1.  Ouvrez la **console ConfigurationManager SystemCenter2012** et sélectionnez l’onglet **administration** .

    2.  Dans l’onglet **administration** , sélectionnez **paramètres du client**.

    3.  Cliquez avec le bouton droit sur **paramètres du client par défaut**, puis sélectionnez **Propriétés**.

    4.  Dans la fenêtre **paramètres par défaut** , sélectionnez **inventaire matériel**.

    5.  Cliquez sur **définir les classes**, puis sur **Importer**.

    6.  Dans le navigateur qui s’ouvre, sélectionnez votre fichier **. mof** , puis cliquez sur **ouvrir**. La fenêtre d' **importation de résumé** s’ouvre.

    7.  Dans la fenêtre **importation de résumé** , assurez-vous que l’option d’importation des classes d’inventaire matériel et des paramètres de classe est activée, puis cliquez sur **Importer**.

    8.  Dans la fenêtre **classes d’inventaire matériel** et la fenêtre **paramètres par défaut** , cliquez sur **OK**.

4.  Activez la classe **Win32 \ _Tpm** comme suit:

    1.  Ouvrez la **console ConfigurationManager SystemCenter2012** et sélectionnez l’onglet **administration** .

    2.  Dans l’onglet **administration** , sélectionnez **paramètres du client**.

    3.  Cliquez avec le bouton droit sur **paramètres du client par défaut**, puis sélectionnez **Propriétés**.

    4.  Dans la fenêtre **paramètres par défaut** , sélectionnez **inventaire matériel**.

    5.  Cliquez sur **définir des classes**.

    6.  Dans la fenêtre principale, faites défiler vers le bas, puis sélectionnez la classe **TPM (Win32 \ _Tpm)** .

    7.  Sous **TPM**, assurez-vous que la propriété **SpecVersion** est sélectionnée.

    8.  Dans la fenêtre **classes d’inventaire matériel** et la fenêtre **paramètres par défaut** , cliquez sur **OK**.

**Pour modifier le fichier SMS \ _def. mof pour Configuration Manager 2007**

1.  Sur le serveur Configuration Manager, accédez à l’emplacement du fichier **SMS \ _def. mof** :

    &lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv\\

    Sur une installation par défaut, l’emplacement d’installation est% systemdrive% C:\\Program Files (x86) \\Microsoft Configuration Manager.

2.  Copiez le code suivant, puis ajoutez-le au fichier **SMS \ _def. mof** pour ajouter les classes MBAM requises suivantes au fichier:

    ``` syntax
    //===================================================
    // Microsoft BitLocker Administration and Monitoring 
    //===================================================

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32_BitLockerEncryptionDetails", NOFAIL)
    [ SMS_Report (TRUE),
      SMS_Group_Name ("BitLocker Encryption Details"),
      SMS_Class_ID ("MICROSOFT|BITLOCKER_DETAILS|1.0")]
    class Win32_BitLockerEncryptionDetails : SMS_Class_Template
    {
        [ SMS_Report (TRUE), key ]
        String     DeviceId;
        [ SMS_Report (TRUE) ]
        String     BitlockerPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        String     MbamPersistentVolumeId;
        [ SMS_Report (TRUE) ]
        //UNKNOWN = 0, OS_Volume = 1, FIXED_VOLUME = 2, REMOVABLE_VOLUME = 3
        SInt32     MbamVolumeType;
        [ SMS_Report (TRUE) ]
        String     DriveLetter;
        [ SMS_Report (TRUE) ]
        //VOLUME_NOT_COMPLIANT = 0, VOLUME_COMPLIANT = 1, NOT_APPLICABLE = 2
        SInt32     Compliant;
        [ SMS_Report (TRUE) ]
        SInt32     ReasonsForNonCompliance[];
        [ SMS_Report (TRUE) ]
        SInt32     KeyProtectorTypes[];
        [ SMS_Report (TRUE) ]
        SInt32     EncryptionMethod;
        [ SMS_Report (TRUE) ]
        SInt32     ConversionStatus;
        [ SMS_Report (TRUE) ]
        SInt32     ProtectionStatus;
        [ SMS_Report (TRUE) ]
        Boolean     IsAutoUnlockEnabled;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=32|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;

        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;

        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser;
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("Win32Reg_MBAMPolicy_64", NOFAIL)
    [ SMS_Report(TRUE),
      SMS_Group_Name("BitLocker Policy"),
      SMS_Class_ID("MICROSOFT|MBAM_POLICY|1.0"),
      SMS_Context_1("__ProviderArchitecture=64|uint32"),
      SMS_Context_2("__RequiredArchitecture=true|boolean")]
    Class Win32Reg_MBAMPolicy_64: SMS_Class_Template
    {
        [SMS_Report(TRUE),key]
        string KeyName;

        //General encryption requirements
        [SMS_Report(TRUE)]
        UInt32    OsDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveEncryption;
        [ SMS_Report (TRUE) ]
        UInt32    EncryptionMethod;

        //Required protectors properties
        [ SMS_Report (TRUE) ]
        UInt32    OsDriveProtector;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDriveAutoUnlock;
        [ SMS_Report (TRUE) ]
        UInt32    FixedDataDrivePassphrase;

        //MBAM Agent fields
        //Policy not enforced (0), enforced (1), pending user exemption request (2) or exempted user (3)
        [SMS_Report(TRUE)]
        Uint32    MBAMPolicyEnforced;
        [SMS_Report(TRUE)]
        string    LastConsoleUser;
        //Date of the exemption request of the last logged on user,
        //or the first date the exemption was granted to him on this machine.
        [SMS_Report(TRUE)]
        datetime  UserExemptionDate;
        //Errors encountered by MBAM agent.
        [ SMS_Report (TRUE) ]
        UInt32    MBAMMachineError;
        // Encoded Computer Name
        [ SMS_Report (TRUE) ]
        string    EncodedComputerName;
    };

    //Read Win32_OperatingSystem.SKU WMI property in a new class - because SKU is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_OperatingSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Operating System Ex"),
      SMS_Class_ID   ("MICROSOFT|OPERATING_SYSTEM_EXT|1.0") ]
    class CCM_OperatingSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
            string     Name;
        [SMS_Report (TRUE) ]
            uint32     SKU;
    };

    //Read Win32_ComputerSystem.PCSystemType WMI property in a new class - because PCSystemType is not available before Vista.
    #pragma namespace ("\\\\.\\root\\cimv2\\SMS")
    #pragma deleteclass("CCM_ComputerSystemExtended", NOFAIL)
    [ SMS_Report     (TRUE),
      SMS_Group_Name ("Computer System Ex"),
      SMS_Class_ID   ("MICROSOFT|COMPUTER_SYSTEM_EXT|1.0") ]
    class CCM_ComputerSystemExtended : SMS_Class_Template
    {
        [SMS_Report (TRUE), key ]
        string     Name;
        [SMS_Report (TRUE) ]
        uint16     PCSystemType;
    };

    //=======================================================
    // Microsoft BitLocker Administration and Monitoring end
    //=======================================================
    ```

3.  Modifiez la classe **Win32 \ _Tpm** comme suit:

    -   Définissez **SMS \ _REPORT** sur **true** dans les attributs de classe.

    -   Définissez **SMS \ _REPORT** sur **true** dans l’attribut de propriété **SpecVersion** .

## Rubriques connexes


[Création ou modification des fichiers mof](how-to-create-or-edit-the-mof-files.md)

[Déploiement de MBAM avec Configuration Manager](deploying-mbam-with-configuration-manager-mbam2.md)

 

 





