---
title: Validation de la configuration des composants serveur de MBAM2.5
description: Validation de la configuration des composants serveur de MBAM2.5
author: dansimp
ms.assetid: f4983a33-ce18-4186-a471-dd6415940504
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f955e0b9ccb7952995574e4aa981674f7c7667fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812143"
---
# Validation de la configuration des composants serveur de MBAM2.5


Lorsque vous avez terminé le déploiement de la fonctionnalité serveur d’administration et de surveillance de BitLocker (MBAM 2,5), nous vous recommandons de valider le déploiement pour vous assurer que toutes les fonctionnalités ont bien été configurées. Utilisez la procédure qui correspond à la topologie (intégration autonome ou System Center Configuration Manager) que vous avez déployée.

## Validation du déploiement du serveur MBAM avec la topologie autonome


Procédez comme suit pour valider votre déploiement MBAM Server avec la topologie autonome.

**Pour valider un déploiement de serveur MBAM autonome**

1.  Sur chaque serveur sur lequel est déployée une fonctionnalité MBAM **Control Panel** , cliquez sur programmes &gt; **Programs** &gt; **et fonctionnalités**du panneau de configuration. Vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche dans la liste **programmes et fonctionnalités** .

    **Remarque**  
    Pour effectuer la validation, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2.  Sur le serveur sur lequel est configuré la base de données de récupération, ouvrez SQL Server Management Studio, puis vérifiez que la base de données **MBAM et de récupération** de la base de données est configurée.

3.  Sur le serveur sur lequel la base de données d’audit et de conformité est configurée, ouvrez SQL Server Management Studio, puis vérifiez que la **base de données d’état de conformité MBAM** est configurée.

4.  Sur le serveur sur lequel la fonctionnalité de création de rapports est configurée, ouvrez un navigateur Web contenant les informations d’identification d’administration et naviguez jusqu’au site «Accueil» du site SQL Server Reporting Services.

    L’emplacement d’accueil par défaut d’une instance de site SQL Server Reporting Services est le suivant:

    http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /reports.aspx

    Pour trouver l’URL réelle, utilisez l’outil Gestionnaire de configuration Reporting Services et sélectionnez les instances que vous avez spécifiées lors de l’installation.

5.  Confirmez qu’un dossier de rapports intitulé **Microsoft BitLocker administration et analyse** contient une source de données appelée **MaltaDataSource** ainsi que les dossiers de langue. La source de données contient des dossiers avec des noms qui représentent des langues (par exemple, en-US). Les rapports se trouvent dans les dossiers de langue.

    **Remarque**  
    Si SQL Server Reporting Services (SSRS) a été configuré en tant qu’instance nommée, l’URL doit ressembler à ce qui suit: http (s):// &lt; *MBAMReportsServerName* &gt; : &lt; *port* &gt; /Reports\_ &lt; *SSRSInstanceName*&gt;



~~~
**Note**  
If SSRS was not configured to use Secure Socket Layer (SSL), the URL for the reports will be set to HTTP instead of HTTPS when you install the MBAM Server. If you then go to the Administration and Monitoring Website (also known as Help Desk) and select a report, the following message appears: "Only Secure Content is Displayed." To show the report, click **Show All Content**.
~~~



6. Sur le serveur sur lequel la fonctionnalité de site Web Administration et contrôle est configurée, exécutez le **Gestionnaire de serveur**, accédez aux **rôles**, puis sélectionnez **serveur Web (IIS)** &gt; **Gestionnaire des services Internet (IIS**).

7. Dans **connexions**, accédez à * &lt; nom &gt; * de l’ordinateur et sélectionnez **sites** &gt; **administration et analyse de Microsoft BitLocker**. Vérifiez que les éléments suivants s’affichent:

   -   **MBAMAdministrationService**

   -   **MBAMComplianceStatusService**

   -   **MBAMRecoveryAndHardwareService**

8. Sur le serveur sur lequel sont configurés le site Web d’administration et de surveillance et le portail libre-service, ouvrez un navigateur Web contenant les informations d’identification d’administration.

9. Naviguez jusqu’au site Web suivant pour vérifier qu’il se charge correctement:

   -   HTTPS (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /helpdesk/: confirmez chacun des liens pour la navigation et les rapports

   -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /selfservice/

   **Remarque**  
   Il est supposé que vous avez configuré les fonctionnalités serveur sur le port par défaut sans chiffrement réseau. Si vous avez configuré les fonctionnalités du serveur sur un autre port ou répertoire virtuel, modifiez les URL pour inclure le port approprié, par exemple:

   http (s):// &lt; *nom d’hôte* &gt; : &lt; *port* &gt; /helpdesk/

   http (s):// &lt; *nom d’hôte* &gt; : &lt; *port* &gt; / &lt; *VirtualDirectory*&gt;/

   Si les fonctionnalités du serveur étaient configurées avec le chiffrement réseau, modifiez http://sur https://.



10. Accédez aux services Web suivants pour vérifier qu’ils se chargent correctement. Une page s’ouvre pour indiquer que le service est en cours d’exécution, mais que la page n’affiche aucune métadonnée.

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMAdministrationService/AdministrationService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMUserSupportService/UserSupportService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMComplianceStatusService/StatusReportingService.svc

    -   http (s):// &lt; *MBAMAdministrationServerName* &gt; : &lt; *port* &gt; /MBAMRecoveryAndHardwareService/CoreService.svc

## Validation du déploiement du serveur MBAM avec la topologie d’intégration de Configuration Manager


Procédez comme suit pour valider votre déploiement MBAM avec la topologie d’intégration de Configuration Manager. Suivez la procédure de validation qui correspond à la version de Configuration Manager que vous utilisez.

### <a href="" id="validating-the-mbam-server-deployment-with-system-center-2012-configuration-manager-"></a>Validation du déploiement du serveur MBAM avec System Center 2012 Configuration Manager

Suivez ces étapes pour valider votre déploiement MBAM Server lorsque vous utilisez MBAM avec System Center 2012 Configuration Manager.

**Pour valider un déploiement d’intégration de Configuration Manager MBAM serveur – System Center 2012 Configuration Manager**

1.  Sur le serveur sur lequel System Center 2012 Configuration Manager est déployé, ouvrez **programmes et fonctionnalités** dans **le panneau**de configuration, puis vérifiez que la fonctionnalité **administration et analyse de BitLocker Microsoft** s’affiche.

    **Remarque**  
    Pour valider la configuration, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2.  Dans la console Configuration Manager, cliquez sur collections de périphériques **et** de l’espace de travail de gestion des éléments &gt; **Device Collections**et vérifiez qu’une nouvelle collection appelée **MBAM les ordinateurs pris en charge** est affichée.

3.  Dans la console Configuration Manager, cliquez sur **analyse** des rapports de rapports d’espace de travail de &gt; **Reporting** &gt; **Reports** &gt; **MBAM**.

4.  Vérifiez que le dossier **MBAM** contient des sous-dossiers avec des noms qui représentent différentes langues et que les rapports suivants apparaissent dans chaque sous-dossier de langue:

    -   Compatibilité de l’ordinateur BitLocker

    -   Tableau de bord de conformité de BitLocker Enterprise

    -   Détails de la conformité à l’entreprise BitLocker

    -   Résumé de conformité de BitLocker Enterprise

5.  Dans la console Configuration Manager, cliquez sur éléments de base de la configuration des **ressources et** de la conformité &gt; **Compliance Settings** &gt; **Configuration Baselines**, puis vérifiez que la **protection BitLocker** de base de la configuration est répertoriée.

6.  Dans la console Configuration Manager, cliquez sur éléments de configuration de éléments **et de conformité** des espaces de travail et &gt; **Compliance Settings** &gt; **Configuration Items**Vérifiez que les nouveaux éléments de configuration suivants s’affichent:

    -   Protection des lecteurs de données fixes BitLocker

    -   Protection des lecteurs du système d’exploitation BitLocker

### Validation du déploiement du serveur MBAM avec Configuration Manager 2007

Suivez ces étapes pour valider votre déploiement MBAM Server lorsque vous utilisez MBAM avec Configuration Manager 2007.

**Pour valider un déploiement d’intégration de Configuration Manager MBAM serveur – Configuration Manager 2007**

1.  Sur le serveur sur lequel Configuration Manager 2007 est déployé, ouvrez **programmes et fonctionnalités** dans le panneau de configuration, puis vérifiez que le **volet** **administration et analyse de BitLocker Microsoft** s’affiche.

    **Remarque**  
    Pour valider la configuration, vous devez utiliser un compte de domaine disposant d’informations d’identification d’administrateur local sur chaque serveur.



2.  Dans la console Configuration Manager, cliquez sur **base de données de site &lt; SiteCode &gt;  -  &lt; NomServeur &gt; , &lt; SiteName &gt; ), gestion de l’ordinateur**, puis vérifiez qu’une nouvelle collection appelée MBAM les **ordinateurs pris en charge** est affichée.

3.  Dans la console Configuration Manager **, cliquez sur** &gt; dossiers de **Reporting Services** &gt; rapport ** \\\\ &lt; ServerName &gt; ** Report services &gt; **Report Folders** &gt; **MBAM**.

    Vérifiez que le dossier **MBAM** contient des sous-dossiers avec des noms qui représentent différentes langues et que les rapports suivants apparaissent dans chaque sous-dossier de langue:

    -   Compatibilité de l’ordinateur BitLocker

    -   Tableau de bord de conformité de BitLocker Enterprise

    -   Détails de la conformité à l’entreprise BitLocker

    -   Résumé de conformité de BitLocker Enterprise

4.  Dans la console Configuration Manager, cliquez sur configurations de configuration de la gestion de la **configuration souhaitées** &gt; **Configuration Baselines**, puis vérifiez que la **protection BitLocker** de base de la configuration est répertoriée.

5.  Dans la console Configuration Manager, cliquez sur éléments de configuration de la **gestion des configurations souhaités** &gt; **Configuration Items**, puis vérifiez que les éléments suivants sont affichés:

    -   Protection des lecteurs de données fixes BitLocker

    -   Protection des lecteurs du système d’exploitation BitLocker



## Rubriques connexes


[Configuration des composants du serveur MBAM2.5](configuring-the-mbam-25-server-features.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).






