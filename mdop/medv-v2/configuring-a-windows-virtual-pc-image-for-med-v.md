---
title: Configuration d'une image Windows Virtual PC pour MED-V
description: Configuration d'une image Windows Virtual PC pour MED-V
author: dansimp
ms.assetid: d87a0df8-9e08-4d1e-bfb0-9dc3cebf0d28
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: 340754b33576651c8ba89c85f369c48c0a0ab957
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811982"
---
# Configuration d'une image Windows Virtual PC pour MED-V


Une fois que vous avez installé toutes les données que vous voulez inclure dans votre image MED-V, vous pouvez configurer l’image pour une utilisation dans la version 2,0 de Microsoft Enterprise Desktop Virtualization. Les rubriques de cette section fournissent des instructions pour configurer votre image MED-V de façon à ce qu’elle s’exécute pour la première fois avant de créer votre package d’espace de travail MED-V.

La première fois que le programme d’installation prépare l’espace de travail MED-V pour un utilisateur final. Le processus crée une machine virtuelle à partir de l’image empaquetée dans l’espace de travail MED-V, puis exécute la mini-installation de Windows sur l’ordinateur virtuel. Cela inclut l’exécution de scripts de configuration personnalisés et la première application de réalisation de l’installation, FtsCompletion.exe.

Suivez ces étapes pour configurer votre image MED-V pour l’exécution de la première fois:

1. En option, vous pouvez compacter le disque dur virtuel (VHD) pour récupérer l’espace libre sur le disque et réduire la taille du disque dur virtuel avant de poursuivre la configuration de l’image de PC virtuel Windows. Pour plus d’informations, voir [compactage du disque dur virtuel MED-V](compacting-the-med-v-virtual-hard-disk.md).

2. Personnalisez le processus de configuration d’une machine virtuelle.

3. Scellez l’image MED-V en utilisant Sysprep.

   **Personnalisation du processus de configuration d’une machine virtuelle**

4. Dans le cadre de la préparation de votre image pour une utilisation avec MED-V, vous pouvez configurer différents paramètres sur l’ordinateur virtuel, par exemple pour spécifier les paramètres d’exécution de Windows Update. Spécifiez tous les paramètres d’ordinateur virtuel nécessaires avant de créer le package d’espace de travail MED-V.

5. Avant de créer le package d’espace de travail MED-V, nous vous recommandons de désactiver les points de restauration sur l’ordinateur virtuel pour empêcher le disque de différenciation de croître. Pour plus d’informations, reportez-vous à la rubrique désactivation [et activation de la restauration du système dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=195927) ( https://go.microsoft.com/fwlink/?LinkId=195927) .

   **Remarque**  
   Vous pouvez configurer votre fichier Sysprep. inf pour désactiver les points de restauration lors de la première exécution du programme d’installation. Pour obtenir un exemple de définition de cette clé GuiRunOnce, voir l’exemple de fichier Sysprep. inf plus loin dans cette section.



6. Configurez le processus de configuration pour exécuter la mini-installation au lieu de l’accueil Windows par défaut. Vous devez exécuter l’outil Sysprep à l’aide du **mini-** commutateur ou activer la case à cocher **MiniSetup** dans l’interface utilisateur graphique. Pour plus d’informations, reportez-vous [à la section sceller l’image avec Sysprep](#bkmk-seal).

   **Appel lors de la première exécution du fichier de configuration**

   1.  Un exécutable appelé FtsCompletion.exe est inclus dans le cadre de l’installation de l’agent d’invité MED-V. Par défaut, il se trouve dans le lecteur système de votre image MED-V sous **Program Files-Microsoft Enterprise Desktop Virtualization**.

       **Important**  
       Lors de la dernière étape du processus de configuration pour la première fois, vous devez exécuter ce programme exécutable. L’utilisateur pour lequel le programme exécutable est appelé doit être membre du groupe d’administrateurs local de l’invité.



   2.  Vous pouvez décider de la façon dont vous souhaitez appeler ce programme exécutable, par exemple par le biais d’un script déployé avec l’espace de travail MED-V. Vous pouvez appeler cet exécutable en tant que dernière ligne de votre fichier Sysprep. inf. Pour obtenir un exemple illustrant comment appeler ce programme exécutable dans votre fichier Sysprep. inf, voir l’exemple de fichier plus loin dans cette section.

Une fois que vous avez terminé la personnalisation de votre image MED-V, vous êtes prêt à sceller l’image en utilisant Sysprep.

<a href="" id="bkmk-seal"></a>**Sceller l’image MED-V à l’aide de Sysprep**

1.  L’outil de préparation du système (Sysprep) est une technologie qui vous permet d’effectuer des installations basées sur une image à l’échelle du réseau en minimisant l’intervention d’un administrateur ou d’un informaticien.

2.  Dans un environnement MED-V, vous pouvez utiliser Sysprep pour affecter des ID de sécurité (SID) uniques et d’autres paramètres à chaque espace de travail MED-V lors du premier démarrage.

    **Remarque**  
    Pour plus d’informations sur l’utilisation de Sysprep, voir [référence technique de Sysprep](https://go.microsoft.com/fwlink/?LinkId=195930) ( https://go.microsoft.com/fwlink/?LinkId=195930) .



~~~
**Caution**  
When you use non-ASCII characters in the Sysprep.inf file, you must save the file by using the encoding appropriate for the characters entered. Windows XP expects the Sysprep.inf file to be encoded by using the code page for the language that you are targeting.

You must also make sure that the System Locale of the computers to which the MED-V workspace is deployed is set to handle the language specific characters that might be present in the Sysprep.inf file. To change the settings for the System Locale, follow these steps:

1.  To open Region and Language, click **Start**, click **Control Panel**, and then click **Region and Language**.

2.  Click the **Administrative** tab, and then click **Change System Locale** under **Language for non-Unicode programs**.

    If you are prompted for an administrator password or confirmation, type the administrator password or provide confirmation.

3.  Select your preferred language and then click **OK**.



**To configure Sysprep on the MED-V Guest Computer**

1.  Create a folder named *Sysprep* in the root of the MED-V image system drive.

2.  Download the deploy.cab file. For more information, see [Windows XP Service Pack 3 Deployment Tools](https://go.microsoft.com/fwlink/?LinkId=195928) From the Microsoft Download Center (https://go.microsoft.com/fwlink/?LinkId=195928).

3.  From the deploy.cab file, copy or extract the Setupmgr.exe, Sysprep.exe, and Setupcl.exe files to the Sysprep folder.

4.  In the Sysprep folder, run **Setup Manager** (Setupmgr.exe) to create a Sysprep.inf answer file.

    Or, you can create this file manually or use your company’s existing file. For more information, see [How to use the Sysprep tool to automate successful deployment of Windows XP](https://go.microsoft.com/fwlink/?LinkId=195929) (https://go.microsoft.com/fwlink/?LinkId=195929).

5.  Follow the **Setup Manager** wizard.

    **Important**  
    You must configure the MED-V guest to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.



    **Caution**  
    When you configure a proxy account for joining virtual machines to the domain, know that it is possible for an end user to obtain the proxy account credentials. Take all the necessary security precautions to minimize risk, such as limiting account user rights. For more information about security concerns when you configure a Windows Virtual PC image for MED-V, see [Security Best Practices for MED-V Operations](security-best-practices-for-med-v-operations.md).



    If end users must provide information during the first time setup process based on the parameters specified in the Sysprep.inf file, you must also specify that first time setup is run in **Attended** mode when you are creating your MED-V workspace package. If no information will be required from the end user, you can specify that first time setup is run in **Unattended** mode when you are creating your MED-V workspace package. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).

    Although you can specify any settings that you prefer, a MED-V best practice is that you create the Sysprep.inf file so that first time setup can be run in **Unattended** mode. This requires that you provide all of the required settings information as you continue through the **Setup Manager** wizard.

    **Caution**  
    If you have set a local policy or registry entry to include a service level agreement (SLA) in your image (VHD), you must specify that first time setup is run in **Attended** mode or first time setup will fail. Or, a MED-V best practice is to enforce the SLA through Group Policy later so that the SLA is displayed to the end user after first time setup is finished.



    **Note**  
    You can configure the MED-V workspace to set certain Sysprep.inf settings based on the configuration of the host and the identity of the end user. For more information, see [Create a MED-V Workspace Package](create-a-med-v-workspace-package.md).



6.  Seal the MED-V image.

    **Important**  
    We recommend that you make a backup copy of the MED-V image before sealing it.



    After you have completed all the steps in the **Setup Manager** wizard, you are ready to run Sysprep to seal the MED-V image.

**To run Sysprep**

1.  Run the System Preparation Tool (Sysprep.exe) from the *Sysprep* folder that you created when you configured Sysprep in the MED-V virtual machine.

2.  In the warning message box that appears, click **OK**.

3.  In the **Options** dialog box, select the **Don't reset grace period for activation** and **Use Mini-Setup** check boxes. Also, make sure that the **Shutdown mode** box is set to **Shut down**.

4.  Click **Reseal**. This removes identity information and clears event logs to prepare for first time setup.

5.  If you are not satisfied with the information listed in the confirmation message box that appears, click **Cancel** and then change the selections.

6.  Click **OK** to complete the system preparation process.

After you have run Sysprep on your MED-V image, the virtual machine shuts down and is ready for use in creating a MED-V workspace.
~~~

## Exemple


Voici un exemple de fichier Sysprep. inf.

``` syntax
;SetupMgrTag
[GuiUnattended]
    EncryptedAdminPassword=NO
    TimeZone=10
    OEMDuplicatorstring="MED_V v2 Host"
    AdminPassword="administrator"
    AutoLogon=Yes
    AutoLogonCount=1
    OEMSkipRegional=1
    OemSkipWelcome=1

[UserData]
    ProductKey=
    FullName="MED-V User"
    OrgName="Contoso"
    ComputerName=*

[Identification]
    JoinDomain=domain.corp.contoso.com
    DomainAdmin=UserName
    DomainAdminPassword=Password

[Networking]
    InstallDefaultComponents=Yes

[Branding]
    BrandIEUsingUnattended=Yes

[Proxy]
    Proxy_Enable=0
    Use_Same_Proxy=0

[Unattended]
    InstallFilesPath=C:\sysprep\i386
    TargetPath=\WINDOWS
    UpdateServerProfileDirectory=1
    OemSkipEula=Yes

[RegionalSettings]
    LanguageGroup=1
    Language=00000409

[GuiRunOnce]
    Command0="wmic /namespace:\\root\default path SystemRestore call Disable %SystemDrive%\"
    Command1="c:\Program Files\Microsoft Enterprise Desktop Virtualization\FtsCompletion.exe"

[sysprepcleanup]
```

## Rubriques connexes


[Créer un package d'espace de travail MED-V](create-a-med-v-workspace-package.md)

[Préparer une image MED-V](prepare-a-med-v-image.md)









