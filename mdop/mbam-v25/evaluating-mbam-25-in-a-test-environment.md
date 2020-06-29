---
title: Évaluation de MBAM2.5 dans un environnement de test
description: Évaluation de MBAM2.5 dans un environnement de test
author: dansimp
ms.assetid: 72959b7a-e55f-4797-91b3-5be23c8c2844
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 0d7ba8a62f5ddecf85fe56e04fc16a6bae374ba9
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809785"
---
# Évaluation de MBAM2.5 dans un environnement de test


Cette rubrique décrit comment configurer un environnement de test pour évaluer l’administration et la surveillance de l’utilisation de Microsoft BitLocker (MBAM) 2,5 dans la topologie d’intégration autonome ou System Center Configuration Manager.

## Évaluation de MBAM 2,5 à l’aide de la topologie autonome


Pour évaluer MBAM à l’aide de la topologie autonome, utilisez les informations du tableau suivant pour installer le logiciel serveur MBAM, puis configurez les fonctionnalités de MBAM Server dans votre environnement de test.

**Pour évaluer MBAM 2,5 à l’aide de la topologie autonome**

1. Avant l’installation d’MBAM, procédez comme suit:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Vérifiez que vous avez installé tous les logiciels requis.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Passez en revue les conditions préalables à l’utilisation de Windows PowerShell Si vous envisagez d’utiliser les applets de contrôle pour configurer MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</p></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez la base de données d’audit et de conformité avec la base de données de récupération.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Comment configurer les bases de données MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurer la fonctionnalité rapports.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Configuration des rapports MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez les applications Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Comment configurer les applications Web MBAM2.5</a></p></td>
   </tr>
   </tbody>
   </table>



3. Sur un ordinateur client, procédez comme suit:

   1.  Installez le client MBAM sur un ordinateur client.

   2.  Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.

   3.  Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à intervalles réguliers:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Remarque**  
       Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser les paramètres de clé de registre suivants uniquement dans un environnement de test.



   4.  Redémarrez le **service client de gestion BitLocker**.

## Évaluation de MBAM 2,5 à l’aide de la topologie d’intégration System Center 2012 Configuration Manager


Pour évaluer MBAM à l’aide de la topologie d’intégration de Configuration Manager, utilisez les informations du tableau suivant pour installer le logiciel serveur MBAM, puis configurez les fonctionnalités de MBAM Server dans votre environnement de test. Après avoir installé le client MBAM sur un ordinateur client, vous devez effectuer des étapes supplémentaires pour forcer le client MBAM à signaler l’état de l’ordinateur au MBAM plus rapidement.

**Pour évaluer MBAM 2,5 à l’aide de la topologie d’intégration System Center 2012 Configuration Manager**

1. Avant d’installer MBAM, passez en revue la configuration logicielle requise et la configuration prise en charge.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Vérifiez que vous avez installé tous les logiciels requis.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Passez en revue les conditions préalables à l’utilisation de Windows PowerShell Si vous envisagez d’utiliser les applets de contrôle pour configurer MBAM.</p></td>
   <td align="left"><p><a href="configuring-mbam-25-server-features-by-using-windows-powershell.md" data-raw-source="[Configuring MBAM 2.5 Server Features by Using Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md)">Configuration des composants du serveur MBAM2.5 à l'aide de Windows PowerShell</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Créez ou modifiez des fichiers. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Modifier le fichier Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Créer ou modifier le fichier Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté. Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez la base de données d’audit et de conformité avec la base de données de récupération.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Comment configurer les bases de données MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurer la fonctionnalité rapports.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Configuration des rapports MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez les applications Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Comment configurer les applications Web MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurez System Center Configuration Manager pour installer les objets Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. Sur un ordinateur client, procédez comme suit:

   1.  Installez le client MBAM et le client Configuration Manager sur un ordinateur client.

   2.  Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.

   3.  Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à intervalles réguliers:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Remarque**  
       Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser les paramètres de clé de registre suivants uniquement dans un environnement de test.



   4.  Redémarrez le **service client de gestion BitLocker**.

   5.  Dans le panneau de configuration, ouvrez **Configuration Manager**, puis cliquez sur l’onglet **actions** .

   6.  Sélectionnez **cycle d’inventaire matériel**, puis cliquez sur **Exécuter maintenant**. Cette étape exécute l’inventaire matériel en utilisant les nouvelles classes que vous avez importées dans vos fichiers. mof, puis envoie les données au serveur Configuration Manager.

   7.  Sélectionnez **récupération de la stratégie ordinateur & cycle d’évaluation**, puis cliquez sur **Exécuter maintenant** pour appliquer les objets de stratégie de groupe pertinents pour cet ordinateur client.



4. Dans la console Configuration Manager, procédez comme suit:

   1.  Dans le volet de navigation, cliquez avec le bouton droit sur **MBAM prises en charge**, cliquez sur **mettre à jour l’appartenance**, puis sur **Oui** pour forcer l’ordinateur client à signaler son appartenance immédiatement.

   2.  Dans le volet de navigation, cliquez sur **MBAM systèmes pris en charge** pour vérifier que l’ordinateur client apparaît dans la collection.

5. Sur l’ordinateur client, dans le panneau de configuration, rouvrez **Configuration Manager** , puis procédez comme suit:

   1.  Cliquez sur l’onglet **actions** , puis réexécutez l’extraction de la **stratégie ordinateur & cycle d’évaluation**.

   2.  Cliquez sur l’onglet **configurations** , sélectionnez le planning de référence BitLocker, puis cliquez sur **évaluer**.

6. Dans la console Configuration Manager, vérifiez que l’ordinateur client apparaît sur le rapport de conformité de l’entreprise: comme suit:

   1.  Dans le volet de navigation, sélectionnez l’espace de travail **analyse** .

   2.  Dans l’arborescence de la console, développez **vue d’ensemble** des rapports de &gt; **rapport** &gt; **Reports** &gt; **MBAM**.

   3.  Sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet résultats.

## Évaluation de MBAM 2,5 à l’aide de System Center Configuration Manager 2007 Integration Topology


Pour évaluer MBAM à l’aide de la topologie d’intégration de Configuration Manager, procédez de la même façon pour installer et configurer MBAM dans votre environnement de test lorsque vous utilisez un environnement de production. Après avoir installé le client MBAM sur un ordinateur client, suivez la procédure supplémentaire décrite dans cette rubrique pour permettre au client MBAM de commencer à signaler l’état de l’ordinateur pour MBAM plus rapidement.

**Pour évaluer MBAM à l’aide de la topologie de l’intégration 2007 de Configuration Manager**

1. Avant l’installation d’MBAM, procédez comme suit:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Vérifiez que vous avez installé tous les logiciels requis.</p></td>
   <td align="left"><p><a href="mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md" data-raw-source="[MBAM 2.5 Server Prerequisites for Stand-alone and Configuration Manager Integration Topologies](mbam-25-server-prerequisites-for-stand-alone-and-configuration-manager-integration-topologies.md)">Conditions préalables pour le serveur MBAM2.5 pour les topologies Intégration Configuration Manager et autonome</a></p>
   <p><a href="mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md" data-raw-source="[MBAM 2.5 Server Prerequisites that Apply Only to the Configuration Manager Integration Topology](mbam-25-server-prerequisites-that-apply-only-to-the-configuration-manager-integration-topology.md)">Conditions préalables pour le serveur MBAM2.5 qui s'appliquent uniquement à la topologie Intégration Configuration Manager</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Vérifiez le matériel, la RAM et d’autres spécifications nécessaires.</p></td>
   <td align="left"><p><a href="mbam-25-supported-configurations.md" data-raw-source="[MBAM 2.5 Supported Configurations](mbam-25-supported-configurations.md)">Configurations prises en charge par MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Créez ou modifiez des fichiers. mof.</p></td>
   <td align="left"><p><a href="edit-the-configurationmof-file-mbam-25.md" data-raw-source="[Edit the Configuration.mof File](edit-the-configurationmof-file-mbam-25.md)">Modifier le fichier Configuration.mof</a></p>
   <p><a href="create-or-edit-the-sms-defmof-file-mbam-25.md" data-raw-source="[Create or Edit the Sms_def.mof File](create-or-edit-the-sms-defmof-file-mbam-25.md)">Créer ou modifier le fichier Sms_def.mof</a></p></td>
   </tr>
   </tbody>
   </table>



2. Installez le logiciel serveur MBAM, puis configurez les fonctionnalités de votre choix.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Tâche</th>
   <th align="left">Où obtenir des instructions</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Installez le logiciel serveur MBAM sur chaque serveur sur lequel vous voulez configurer une fonctionnalité de MBAM Server.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Vous pouvez installer les bases de données sur un ordinateur distant SQL Server à l’aide de Windows PowerShell ou d’un package d’application de couche de données (DAC) exporté. Pour plus d’informations sur les packages DAC, voir <a href="https://technet.microsoft.com/library/ee210546.aspx" data-raw-source="[Data-tier Applications](https://technet.microsoft.com/library/ee210546.aspx)"> applications à couches de données </a> .</p>
   </div>
   <div>

   </div></td>
   <td align="left"><p><a href="installing-the-mbam-25-server-software.md" data-raw-source="[Installing the MBAM 2.5 Server Software](installing-the-mbam-25-server-software.md)">Installation du logiciel serveur MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez la base de données d’audit et de conformité avec la base de données de récupération.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-databases.md" data-raw-source="[How to Configure the MBAM 2.5 Databases](how-to-configure-the-mbam-25-databases.md)">Comment configurer les bases de données MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurer la fonctionnalité rapports.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-reports.md" data-raw-source="[How to Configure the MBAM 2.5 Reports](how-to-configure-the-mbam-25-reports.md)">Configuration des rapports MBAM2.5</a></p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Configurez les applications Web.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-web-applications.md" data-raw-source="[How to Configure the MBAM 2.5 Web Applications](how-to-configure-the-mbam-25-web-applications.md)">Comment configurer les applications Web MBAM2.5</a></p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Configurez System Center Configuration Manager pour installer les objets Configuration Manager.</p></td>
   <td align="left"><p><a href="how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md" data-raw-source="[How to Configure the MBAM 2.5 System Center Configuration Manager Integration](how-to-configure-the-mbam-25-system-center-configuration-manager-integration.md)">Comment configurer l'intégration de MBAM2.5 à System Center Configuration Manager</a></p></td>
   </tr>
   </tbody>
   </table>



3. Sur un ordinateur client, procédez comme suit:

   1.  Installez le client MBAM sur un ordinateur client.

   2.  Appliquez les objets de stratégie de groupe MBAM à l’ordinateur.

   3.  Définissez les clés de Registre suivantes pour forcer le client MBAM à se réveiller plus rapidement et à des intervalles plus courts:

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement
       "ClientWakeupFrequency"=dword:00000001
       "StatusReportingFrequency"=dword:00000001
       ```

       ``` syntax
       [HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM]
       "NoStartupDelay"=dword:00000001
       ```

       **Remarque**  
       Comme ces clés réactivent le client MBAM toutes les minutes, nous vous recommandons d’utiliser ces paramètres de clé de Registre uniquement dans un environnement d’évaluation.



   4.  Redémarrez le **service client de gestion BitLocker**.

   5.  Dans le panneau de configuration, ouvrez **Configuration Manager**, puis cliquez sur l’onglet **actions** .

   6.  Sélectionnez **récupération de la stratégie ordinateur & cycle d’évaluation**, puis cliquez sur **Exécuter maintenant** pour appliquer les objets de stratégie de groupe pertinents pour cet ordinateur client.

   7.  Sélectionnez **cycle d’inventaire matériel**, puis cliquez sur **Exécuter maintenant**. Cette étape exécute l’inventaire matériel en utilisant les nouvelles classes que vous avez importées dans vos fichiers. mof, puis envoie les données au serveur Configuration Manager.

4. Dans la console Configuration Manager, procédez comme suit:

   1.  Dans le volet de navigation, cliquez avec le bouton droit sur **MBAM prises en charge**, cliquez sur **mettre à jour l’appartenance**, puis sur **Oui** pour forcer l’ordinateur client à signaler son appartenance immédiatement.

   2.  Dans le volet de navigation, cliquez sur **MBAM systèmes pris en charge** pour vérifier que l’ordinateur client apparaît dans la collection.

5. Sur l’ordinateur client, dans le panneau de configuration, rouvrez **Configuration Manager** , puis procédez comme suit:

   1.  Cliquez sur l’onglet **actions** , puis réexécutez l’extraction de la **stratégie ordinateur & cycle d’évaluation**.

   2.  Cliquez sur l’onglet **configurations** , sélectionnez le planning de référence BitLocker, puis cliquez sur **évaluer**.

6. Dans la console Configuration Manager, vérifiez que l’ordinateur client apparaît sur le rapport de conformité d’entreprise, comme suit.

   1.  Dans le volet de navigation, développez **Computer Management** Reporting &gt; **Reporting** &gt; **services Reporting Services Reporting Services** &gt; ** &lt; nom du serveur &gt; MBAM**.

   2.  Dans le nœud **MBAM** , sélectionnez le dossier qui représente la langue dans laquelle vous souhaitez afficher les rapports, puis sélectionnez le rapport dans le volet résultats.


## Rubriques connexes


[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)


## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).





