---
title: Créer ou modifier le fichier SMS \ _def. mof
description: Créer ou modifier le fichier SMS \ _def. mof
author: dansimp
ms.assetid: 0bc5e7d8-9747-4da6-a1b3-38d8f27ba121
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 272f597974e96efa0c742fecfe9488a4899fc695
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809810"
---
# <span data-ttu-id="a2646-103">Créer ou modifier le fichier SMS \ _def. mof</span><span class="sxs-lookup"><span data-stu-id="a2646-103">Create or Edit the Sms\_def.mof File</span></span>


<span data-ttu-id="a2646-104">Pour permettre aux ordinateurs clients de signaler les détails de conformité BitLocker par le biais des rapports du gestionnaire de configuration MBAM, vous devez créer ou modifier le fichier SMS \ _def. mof.</span><span class="sxs-lookup"><span data-stu-id="a2646-104">To enable the client computers to report BitLocker compliance details through the MBAM Configuration Manager reports, you have to create or edit the Sms\_def.mof file.</span></span>

<span data-ttu-id="a2646-105">Si vous utilisez SystemCenter2012 ConfigurationManager, vous devez créer le fichier.</span><span class="sxs-lookup"><span data-stu-id="a2646-105">If you are using SystemCenter2012 ConfigurationManager, you must create the file.</span></span> <span data-ttu-id="a2646-106">Créez le fichier sur le site de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="a2646-106">Create the file on the top-tier site.</span></span> <span data-ttu-id="a2646-107">Les modifications seront répliquées sur les autres sites de votre infrastructure.</span><span class="sxs-lookup"><span data-stu-id="a2646-107">The changes will be replicated to the other sites in your infrastructure.</span></span>

<span data-ttu-id="a2646-108">Dans Configuration Manager 2007, le fichier existe déjà et vous n’avez plus qu’à le modifier.</span><span class="sxs-lookup"><span data-stu-id="a2646-108">In Configuration Manager 2007, the file already exists, so you only have to edit it.</span></span> **<span data-ttu-id="a2646-109">Ne remplacez pas le fichier existant.</span><span class="sxs-lookup"><span data-stu-id="a2646-109">Do not overwrite the existing file.</span></span>**

<span data-ttu-id="a2646-110">Dans les sections ci-dessous, suivez les instructions correspondant à la version de Configuration Manager que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="a2646-110">In the following sections, complete the instructions that correspond to the version of Configuration Manager that you are using.</span></span>

**<span data-ttu-id="a2646-111">Pour créer le fichier SMS \ _def. mof pour SystemCenter2012 ConfigurationManager</span><span class="sxs-lookup"><span data-stu-id="a2646-111">To create the Sms\_def.mof file for SystemCenter2012 ConfigurationManager</span></span>**

1.  <span data-ttu-id="a2646-112">Sur le serveur Configuration Manager, accédez à l’emplacement où vous voulez créer le fichier SMS \ _def. mof, par exemple le bureau.</span><span class="sxs-lookup"><span data-stu-id="a2646-112">On the Configuration Manager Server, browse to the location where you have to create the Sms\_def.mof file, for example, the Desktop.</span></span>

2.  <span data-ttu-id="a2646-113">Créez un fichier texte appelé **SMS \ _def. mof** et copiez le code suivant pour remplir le fichier avec les classes sms \ _def. mof MBAM suivantes:</span><span class="sxs-lookup"><span data-stu-id="a2646-113">Create a text file called **Sms\_def.mof** and copy the following code to populate the file with the following Sms\_def.mof MBAM classes:</span></span>

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
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
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

3.  <span data-ttu-id="a2646-114">Importez le fichier **SMS \ _def. mof** en procédant comme suit:</span><span class="sxs-lookup"><span data-stu-id="a2646-114">Import the **Sms\_def.mof** file by doing the following:</span></span>

    1.  <span data-ttu-id="a2646-115">Ouvrez la **console ConfigurationManager SystemCenter2012** et sélectionnez l’onglet **administration** .</span><span class="sxs-lookup"><span data-stu-id="a2646-115">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="a2646-116">Dans l’onglet **administration** , sélectionnez **paramètres du client**.</span><span class="sxs-lookup"><span data-stu-id="a2646-116">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="a2646-117">Cliquez avec le bouton droit sur **paramètres du client par défaut**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a2646-117">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="a2646-118">Dans la fenêtre **paramètres par défaut** , sélectionnez **inventaire matériel**.</span><span class="sxs-lookup"><span data-stu-id="a2646-118">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="a2646-119">Cliquez sur **définir les classes**, puis sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="a2646-119">Click **Set Classes**, and then click **Import**.</span></span>

    6.  <span data-ttu-id="a2646-120">Dans le navigateur qui s’ouvre, sélectionnez votre fichier **. mof** , puis cliquez sur **ouvrir**.</span><span class="sxs-lookup"><span data-stu-id="a2646-120">In the browser that opens, select your **.mof** file, and then click **Open**.</span></span> <span data-ttu-id="a2646-121">La fenêtre d' **importation de résumé** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="a2646-121">The **Import Summary** window opens.</span></span>

    7.  <span data-ttu-id="a2646-122">Dans la fenêtre **importation de résumé** , assurez-vous que l’option d’importation des classes d’inventaire matériel et des paramètres de classe est activée, puis cliquez sur **Importer**.</span><span class="sxs-lookup"><span data-stu-id="a2646-122">In the **Import Summary** window, ensure that the option to import both hardware inventory classes and class settings is selected, and then click **Import**.</span></span>

    8.  <span data-ttu-id="a2646-123">Dans la fenêtre **classes d’inventaire matériel** et la fenêtre **paramètres par défaut** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2646-123">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

4.  <span data-ttu-id="a2646-124">Activez la classe **Win32 \ _Tpm** comme suit:</span><span class="sxs-lookup"><span data-stu-id="a2646-124">Enable the **Win32\_Tpm** class as follows:</span></span>

    1.  <span data-ttu-id="a2646-125">Ouvrez la **console ConfigurationManager SystemCenter2012** et sélectionnez l’onglet **administration** .</span><span class="sxs-lookup"><span data-stu-id="a2646-125">Open the **SystemCenter2012 ConfigurationManager console** and select the **Administration** tab.</span></span>

    2.  <span data-ttu-id="a2646-126">Dans l’onglet **administration** , sélectionnez **paramètres du client**.</span><span class="sxs-lookup"><span data-stu-id="a2646-126">On the **Administration** tab, select **Client Settings**.</span></span>

    3.  <span data-ttu-id="a2646-127">Cliquez avec le bouton droit sur **paramètres du client par défaut**, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="a2646-127">Right-click **Default Client Settings**, and then select **Properties**.</span></span>

    4.  <span data-ttu-id="a2646-128">Dans la fenêtre **paramètres par défaut** , sélectionnez **inventaire matériel**.</span><span class="sxs-lookup"><span data-stu-id="a2646-128">In the **Default Settings** window, select **Hardware Inventory**.</span></span>

    5.  <span data-ttu-id="a2646-129">Cliquez sur **définir des classes**.</span><span class="sxs-lookup"><span data-stu-id="a2646-129">Click **Set Classes**.</span></span>

    6.  <span data-ttu-id="a2646-130">Dans la fenêtre principale, faites défiler vers le bas, puis sélectionnez la classe **TPM (Win32 \ _Tpm)** .</span><span class="sxs-lookup"><span data-stu-id="a2646-130">In the main window, scroll down, and then select the **TPM (Win32\_Tpm)** class.</span></span>

    7.  <span data-ttu-id="a2646-131">Sous **TPM**, assurez-vous que la propriété **SpecVersion** est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a2646-131">Under **TPM**, ensure that the **SpecVersion** property is selected.</span></span>

    8.  <span data-ttu-id="a2646-132">Dans la fenêtre **classes d’inventaire matériel** et la fenêtre **paramètres par défaut** , cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="a2646-132">In both the **Hardware Inventory Classes** window and the **Default Settings** window, click **OK**.</span></span>

**<span data-ttu-id="a2646-133">Pour modifier le fichier SMS \ _def. mof pour Configuration Manager 2007</span><span class="sxs-lookup"><span data-stu-id="a2646-133">To edit the sms\_def.mof file for Configuration Manager 2007</span></span>**

1.  <span data-ttu-id="a2646-134">Sur le serveur Configuration Manager, accédez à l’emplacement du fichier **SMS \ _def. mof** :</span><span class="sxs-lookup"><span data-stu-id="a2646-134">On the Configuration Manager Server, browse to the location of the **sms\_def.mof** file:</span></span>

    <span data-ttu-id="a2646-135">&lt;CMInstallLocation &gt; \\Inboxes\\clifiles.src\\hinv</span><span class="sxs-lookup"><span data-stu-id="a2646-135">&lt;CMInstallLocation&gt;\\Inboxes\\clifiles.src\\hinv</span></span>\\

    <span data-ttu-id="a2646-136">Sur une installation par défaut, l’emplacement d’installation est% systemdrive% C:\\Program Files (x86) \\Microsoft Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="a2646-136">On a default installation, the installation location is %systemdrive% \\Program Files (x86)\\Microsoft Configuration Manager.</span></span>

2.  <span data-ttu-id="a2646-137">Copiez le code suivant, puis ajoutez-le au fichier **SMS \ _def. mof** pour ajouter les classes MBAM requises suivantes au fichier:</span><span class="sxs-lookup"><span data-stu-id="a2646-137">Copy the following code, and then append it to **Sms\_def.mof** file to add the following required MBAM classes to the file:</span></span>

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
        [ SMS_Report (TRUE) ]
        String     NoncomplianceDetectedDate;
        [ SMS_Report (TRUE) ]
        String     EnforcePolicyDate;
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

3.  <span data-ttu-id="a2646-138">Modifiez la classe **Win32 \ _Tpm** comme suit:</span><span class="sxs-lookup"><span data-stu-id="a2646-138">Modify the **Win32\_Tpm** class as follows:</span></span>

    -   <span data-ttu-id="a2646-139">Définissez **SMS \ _REPORT** sur **true** dans les attributs de classe.</span><span class="sxs-lookup"><span data-stu-id="a2646-139">Set **SMS\_REPORT** to **TRUE** in the class attributes.</span></span>

    -   <span data-ttu-id="a2646-140">Définissez **SMS \ _REPORT** sur **true** dans l’attribut de propriété **SpecVersion** .</span><span class="sxs-lookup"><span data-stu-id="a2646-140">Set **SMS\_REPORT** to **TRUE** in the **SpecVersion** property attribute.</span></span>

    <span data-ttu-id="a2646-141">Vous **avez une suggestion pour MBAM**?</span><span class="sxs-lookup"><span data-stu-id="a2646-141">**Got a suggestion for MBAM**?</span></span> <span data-ttu-id="a2646-142">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="a2646-142">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> <span data-ttu-id="a2646-143">Vous **avez un problème avec mbam**?</span><span class="sxs-lookup"><span data-stu-id="a2646-143">**Got a MBAM issue**?</span></span> <span data-ttu-id="a2646-144">Utiliser le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a2646-144">Use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>

## <span data-ttu-id="a2646-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2646-145">Related topics</span></span>


[<span data-ttu-id="a2646-146">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="a2646-146">MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology</span></span>](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)

[<span data-ttu-id="a2646-147">Modifier le fichier Configuration.mof</span><span class="sxs-lookup"><span data-stu-id="a2646-147">Edit the Configuration.mof File</span></span>](edit-the-configurationmof-file-mbam-25.md)

[<span data-ttu-id="a2646-148">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</span><span class="sxs-lookup"><span data-stu-id="a2646-148">MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies</span></span>](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)

 

 
## <span data-ttu-id="a2646-149">Vous avez une suggestion pour MBAM?</span><span class="sxs-lookup"><span data-stu-id="a2646-149">Got a suggestion for MBAM?</span></span>
- <span data-ttu-id="a2646-150">Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)</span><span class="sxs-lookup"><span data-stu-id="a2646-150">Add or vote on suggestions [here](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring).</span></span> 
- <span data-ttu-id="a2646-151">Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span><span class="sxs-lookup"><span data-stu-id="a2646-151">For MBAM issues, use the [MBAM TechNet Forum](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).</span></span>




