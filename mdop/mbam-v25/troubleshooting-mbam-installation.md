---
title: Résolution des problèmes d’installation de MBAM2.5
description: Découvrez comment résoudre les problèmes d’installation d’MBAM 2,5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: ed56a87496e09601c44028b7f948eda39143e8c0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804548"
---
# Résolution des problèmes d’installation de MBAM2.5

Cet article présente la procédure de résolution des problèmes d’installation de Microsoft BitLocker administration et de surveillance (MBAM) 2,5 dans une configuration autonome.

## Référencement des fichiers journaux de MBAM pour la résolution des problèmes

MBAM inclut la journalisation de l’installation du serveur, de l’installation du client et des événements. Cette journalisation devrait faire l’appel de la résolution des problèmes. 
 
### Fichiers journaux d’installation de MBAM Server

MBAMServerSetup.exe génère les fichiers journaux suivants dans le dossier% Temp% de l’utilisateur lors de l’installation d’MBAM:<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 numéros>. log**

MBAMServerSetup.exe enregistre les actions effectuées lors de l’installation d’MBAM et de la fonctionnalité MBAM Server.<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers # C1_0_MBAMServer.msi. log**

MBAMServerSetup.exe enregistre les actions supplémentaires effectuées lors de l’installation.

### Fichier journal d’installation du client MBAM

L’installation du client est enregistrée dans le fichier journal suivant dans le dossier% Temp% (ou un emplacement personnalisé, selon la façon dont le client a été installé): <br />**MSI \<five random characters\> . log**

Ce journal contient les actions effectuées lors de l’installation du client MBAM.
 
### Événement client MBAM-canal de journalisation

MBAM a des canaux de journalisation des événements séparés. Les fichiers du journal d’administration, de l’analyse et du fonctionnement se trouvent dans l’observateur d’événements, sous **applications et services consignent**  >  **Microsoft**  >  **Windows**  >  **MBAM**.

Le tableau suivant fournit une description succincte de chaque journal des événements.
 
|Journal des événements| Description|
|----------|-------|
|Microsoft-Windows-MBAM/admin|  Contient des messages d’erreur|
|Microsoft-Windows-MBAM/analyse|   Contient des informations de journalisation avancées|
|Microsoft-Windows-MBAM/opérationnel|    Contient des messages de réussite|

### MBAM-canal de journalisation des événements serveur

Les fichiers journaux sont situés dans l’observateur d’événements, sous **les journaux d’application et de service journaux**de  >  **Microsoft**  >  **Windows**  >  **MBAM**. Le tableau suivant inclut les journaux des événements serveur introduits dans MBAM 2,5:

|Journal des événements| Description|
|--------|-------------|
|Microsoft-Windows-MBAM/admin|  Contient des messages d’erreur|
|Microsoft-Windows-MBAM/analyse|   Contient des informations de journalisation avancées|
|Microsoft-Windows-MBAM/opérationnel|    Contient des messages de réussite|

### Journaux de service Web MBAM

Chaque journal de service Web MBAM écrit les informations de journalisation dans un fichier SVCLOG. Par défaut, chaque service Web écrit le fichier de suivi sous un dossier qui utilise son nom dans le dossier Solution\Logs de gestion C:\inetpub\Microsoft BitLocker.

Vous pouvez utiliser l’outil visionneuse de suivi des services (intégré à Microsoft Visual Studio) pour passer en revue les traces de svclog.

## Résolution des problèmes de chiffrement et de création de rapports

Cette section contient des informations permettant de résoudre les problèmes liés aux fonctionnalités du serveur, aux fonctionnalités client, aux paramètres de configuration et aux problèmes connus:
 
### Installation du client MBAM, paramètres de la stratégie de groupe

Déterminez si l’agent MBAM est installé sur l’ordinateur client. Lorsque MBAM est installé, il crée un service intitulé service du client de gestion BitLocker. Ce service est configuré pour démarrer automatiquement. Déterminez si le service est en cours d’exécution.

Assurez-vous que les paramètres de stratégie de groupe MBAM sont appliqués sur l’ordinateur client. La sous-clé de Registre suivante est créée si les paramètres de stratégie de groupe ont été appliqués sur l’ordinateur client: **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**

Vérifiez que cette clé existe et qu’elle est remplie à l’aide de valeurs par paramètre de stratégie de groupe.

### Agent MBAM au cours de la période de délai initial

Le client MBAM ne démarre pas l’opération immédiatement après l’installation. Le délai initial d’un délai de 1 à 18 minutes avant le démarrage de l’agent MBAM est nécessaire. Outre le délai initial, il y a un délai d’au moins 90 minutes. (Le délai dépend des paramètres de stratégie de groupe qui sont configurés pour la fréquence de vérification de l’état du client.) Par conséquent, le délai total précédant l’opération de démarrage d’un client correspond au délai de *démarrage aléatoire*permettant de  +  *vérifier le délai de fréquence*.

Si les journaux des événements de fonctionnement et d’administration sont vides, le client n’a pas encore commencé l’opération et a atteint la période de délai mentionnée auparavant. Pour éviter ce délai, procédez comme suit:
 
1. Arrêtez le service du client de gestion BitLocker.

2. Sous HKEY_LOCAL_MACHINE la sous-clé de Registre **\software\microsoft\mbam** , créez la valeur de Registre **NoStartupDelay** , définissez son type sur **REG_DWORD**, puis définissez sa valeur sur **1**.

3. Sous **HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**, définissez les valeurs **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1**. Ces valeurs seront restaurées dans leurs paramètres d’origine après la mise à jour de la stratégie de groupe sur l’ordinateur.

4. Démarrez le service du client de gestion BitLocker.

Après le démarrage du service, si vous ouvrez une session locale sur l’ordinateur et qu’il n’y a pas d’erreurs, vous devriez recevoir une demande de chiffrer l’ordinateur dans une minute. Si vous ne recevez pas de requête, consultez les journaux d’administration MBAM pour toute erreur.

### L’ordinateur n’est pas équipé d’un module de plateforme sécurisée, ou le module de plateforme sécurisée n’est pas activé dans le BIOS.

Examinez le journal des événements d’administration MBAM. Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 12:31:10 PM
    Event ID:      9
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    The TPM hardware is missing.
    TPM is needed to encrypt the operating system drive with any TPM protector.

Ouvrez le module de gestion de la plateforme sécurisée (TPM. msc) et vérifiez que l’ordinateur dispose d’un appareil de plateforme sécurisée. Si TPM. msc ne montre pas d’appareil, ouvrez le gestionnaire de périphériques (devmgmt. msc) et recherchez un module de plateforme sécurisée sous dispositifs de sécurité. Si vous ne voyez pas d’appareil de module de plateforme sécurisée, il est possible que cela soit vrai pour l’une des raisons suivantes:

* Votre système ne possède pas de périphérique de module de plateforme sécurisée (TPM).

* Le périphérique TPM est désactivé dans le BIOS.

* Le module de plateforme sécurisée est activé dans le BIOS, mais la gestion du périphérique TPM à partir du système d’exploitation est désactivée dans le BIOS.

* Vous n’utilisez pas un pilote Microsoft pour le périphérique GPC. Passez en revue les périphériques qui sont répertoriés dans le gestionnaire de périphériques pour identifier le pilote de périphérique Microsoft GPC.

Si le module de plateforme sécurisée n’utilise pas le pilote C:\Windows\System32\tpm.sys, vous devez mettre à jour le pilote en sélectionnant le fichier C:\Windows\Inf\tpm.inf.

### Votre ordinateur ne possède pas de partition système valide

Examinez le journal des événements d’administration MBAM. Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:37 AM
    Event ID:      8
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTESTVM.xtremelabs.com
    Description:
    The system volume is missing.
    SystemVolume is needed to encrypt the operating system drive.

BitLocker nécessite une partition système pour activer le chiffrement ([chiffrement de lecteur BitLocker dans Windows 7: Forum aux questions](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM ne crée pas automatiquement la partition système. Vous pouvez utiliser l’utilitaire de préparation de lecteur BitLocker (bdehdcfg.exe) pour créer la partition système et déplacer les fichiers de démarrage requis.

Par exemple, vous pouvez utiliser la commande **% windir% \system32\bdeHdCfg.exe-Target par défaut-size 300 – quiet** pour préparer le lecteur en silence avant de déployer MBAM pour chiffrer les lecteurs. Cela nécessite un redémarrage. Vous pouvez également Scripter l’action si nécessaire. Le document suivant décrit l’outil de préparation du lecteur BitLocker:

[Description de l’outil de préparation du lecteur BitLocker](https://support.microsoft.com/help/933246)

### Les lecteurs ne sont pas mis en forme pour disposer d’un système de fichiers compatible

Consultez l' [article TechNet relatif à la configuration requise pour le système de fichiers pour BitLocker](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements).

### Conflit de stratégie de groupe

Vous verrez une entrée d’événement semblable à celle qui suit dans le journal des événements d’administration MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/25/2013 9:27:58 PM
    Event ID:      22
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Detected Fixed Data Drive volume encryption policies conflict.
    Check BitLocker and MBAM policies related to FDD drive protectors.

Vérifiez les paramètres de stratégie de groupe pour vérifier que vous n’avez pas de paramètre en conflit entre les paramètres de stratégie de groupe MBAM.

Vous devez configurer une stratégie de groupe à l’aide du modèle MDOP MBAM et non du modèle de chiffrement de lecteur BitLocker.

Exemple:

Sous paramètres de chiffrement de lecteur du système d’exploitation, vous avez sélectionné TPM en tant que protecteur, et vous pouvez également sélectionner **autoriser les codes confidentiels optimisés pour le démarrage**. Il s’agit de paramètres en conflit, car la protection GPC uniquement ne nécessite pas de code confidentiel. Par conséquent, vous devez désactiver le paramètre épingles améliorées.

### L’utilisateur a pu demander une exonération

Si vous avez activé l’ordinateur d’administration\Composants Templates\Windows Components\MDOP MBAM (gestion de BitLocker) \Client Management\Configure paramètre de stratégie d’exemption des utilisateurs, les utilisateurs pourront demander une exemption.

Par défaut, si l’utilisateur demande une exemption, l’exemption est valide pendant 7 jours, et l’utilisateur ne reçoit pas les invites de chiffrement au cours de cette période. (La valeur par défaut peut être augmentée ou réduite lors de la configuration de la stratégie.) Au terme de la période d’exemption, l’utilisateur est invité à chiffrer.

Vous verrez l’entrée suivante dans le journal des événements d’administration MBAM lorsqu’un ordinateur est soumis à une exemption d’utilisation:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 3:06:40 PM
    Event ID:      13
    Task Category: None
    Level:         Warning
    Keywords:      
    User:          SYSTEM
    Computer:      MBAMCLIENT.contoso.com
    Description:
    The user is exempt from encryption.

Si vous voulez remplacer manuellement l’exemption pour un ordinateur, procédez comme suit:
 
1. Définissez la valeur AllowUserExemption sur **0** sous la sous-clé de Registre suivante: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Supprimez toutes les valeurs de Registre sous la sous-clé de Registre suivante, à l’exception de **AgentVersion**, **EncodedComputerName**et **installed**:<br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM**

    **Remarques** Vous devez redémarrer l’agent MBAM pour que les modifications prennent effet.

Sachez qu’après avoir appliqué une stratégie de groupe à votre ordinateur, ces valeurs risquent de rétablir leurs paramètres d’origine.

### Problème WMI

MBAM utilise les méthodes de la classe win32_encryptablevolume pour gérer BitLocker. Si ce module n’est pas enregistré ou est endommagé, le client MBAM ne fonctionnera pas correctement et l’entrée d’événement suivante s’affichera dans le journal des événements d’administration MBAM:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          7/27/2013 11:18:51 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:      
    User:          SYSTEM
    Computer:      BITTEST.xtremelabs.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x80041016 
    Details:
    NULL

Par ailleurs, il est possible que les stratégies de récupération et de matériel ne s’appliquent pas à l’aide du code d’erreur 0x8007007e. Cela se traduit par «le module spécifié est introuvable».

Pour résoudre ce problème, vous devez réinscrire la classe **Win32_EncryptableVolume** à l’aide de la commande suivante:

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## Résoudre les problèmes de communication avec l’agent MBAM

Cette section contient des informations de dépannage pour les problèmes suivants liés à la communication avec l’agent MBAM:

### URL du service MBAM incorrecte

Si la valeur du service de vérification de conformité MBAM ou de récupération et de service matériel est incorrecte, une entrée d’événement semblable à la suivante apparaît dans le journal des événements d’administration MBAM sur l’ordinateur client:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:36 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:13:33 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0010
    Details:
    The remote endpoint was not reachable.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      4
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    An error occurred while sending encryption status data.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          8/3/2013 4:20:32 PM
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      Mbamclient.contoso.com
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803d0020
    Details:
    The endpoint address URL is invalid.

Vérifiez les valeurs de **KeyRecoveryServiceEndPoint** et **StatusReportingServiceEndpoint** sous la sous-clé de Registre suivante de l’ordinateur client: <br />
**HKEY_LOCAL_MACHINE \SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Par défaut, l’URL de KeyRecoveryServiceEndPoint (point de terminaison du service de récupération et de matériel MBAM) est au format suivant: <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Par défaut, l’URL de StatusReportingServiceEndpoint (point de terminaison du service de rapport d’État MBAM) est au format suivant:<br />
**http:// \<servername\> : \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> L’URL ne doit contenir aucun espace.

Si l’URL du service est incorrecte, vous devez corriger l’URL du service dans le paramètre de stratégie de groupe suivant:

**Configuration ordinateur**  >  **Politiques**  >  **Modèles**  >  d’administration **Composants Windows**  >  **MDOP MBAM (gestion de BitLocker)**  >  **Gestion**  >  des clients **Configurer les services de MBAM**

### Problème de connectivité affectant le serveur d’administration MBAM

L’agent MBAM ne sera pas en mesure de publier des mises à jour de la base de données s’il existe des problèmes de connectivité entre l’agent client et le serveur d’administration MBAM. Dans le cas présent, vous remarquerez les entrées d’échec de connectivité dans le journal des événements d’administration MBAM sur l’ordinateur client:

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 18:21:22
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.
 
    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          29-04-2014 23:06:48
    Event ID:      2
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    An error occurred while applying MBAM policies.
    Volume ID:\\?\Volume{871c5858-2467-4d0b-8c83-d68af8ce10e5}\ 
    Error code:
    0x803D0006 
    Details:
    The operation did not complete within the time allotted.

    Log Name:      Microsoft-Windows-MBAM/Admin
    Source:        Microsoft-Windows-MBAM
    Date:          02-09-2013 02:02:04
    Event ID:      18
    Task Category: None
    Level:         Error
    Keywords:     
    User:          SYSTEM
    Computer:      TESTLABS.CONTOSO.COM
    Description:
    Unable to connect to the MBAM Recovery and Hardware service.
    Error code:
    0x803D0010 
    Details:
    The remote endpoint was not reachable.

Vérifications de base:

* Vérifiez la connectivité de base en exécutant une commande ping sur le serveur d’administration MBAM. Vérifiez si vous pouvez vous connecter au port de service ou de site Web d’administration MBAM à l’aide de Telnet ou Portqry.

* Vérifiez que le service IIS s’exécute sur le serveur d’administration et de surveillance MBAM et que le service Web MBAM écoute sur le même port que celui configuré sur l’ordinateur client MBAM ( `netstat –ano | find "portnumber"` ).

* Vérifiez que le numéro de port configuré pour le site Web MBAM utilise le gestionnaire des services Internet (inetmgr). Assurez-vous que le numéro de port est identique au numéro de port sur lequel le client écoute. Vérifiez que le numéro de port n’est pas partagé par une autre application. Par exemple, une autre application sur le serveur ne doit pas utiliser le même port.

* S’il y a un pare-feu, assurez-vous que le port est ouvert dans le pare-feu ou le serveur proxy.

* Si la communication entre le client et le serveur est sécurisée, vérifiez que vous utilisez un certificat SSL valide.

* Vérifiez la connectivité réseau entre le serveur Web et le serveur de base de données sur lequel les données sont envoyées pour insertion. Vous pouvez vérifier la connectivité de base de données du serveur Web vers le serveur de base de données à l’aide de l’administrateur de sources de données ODBC. Des informations détaillées sur la résolution des problèmes de connexion au serveur SQL Server sont disponibles dans la [procédure de résolution des problèmes de connexion au moteur de base de données SQL Server](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### Résoudre les problèmes de connectivité

Assurez-vous que l’URL du service configuré sur le client est correcte. Copiez la valeur de l’URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**) du Registre et ouvrez-la dans Internet Explorer.

De même, copiez la valeur de l’URL pour StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE \software\policies\microsoft\fve\mdopbitlockermanagement**), puis ouvrez-la dans Internet Explorer.

> [!Note]
> Si vous ne parvenez pas à accéder à l’URL à partir de l’ordinateur client, vous devez tester la connectivité réseau de base entre le client et le serveur exécutant IIS. Voir points 1, 2, 3 et 4 dans la section précédente.

De plus, consultez les journaux d’application sur le serveur d’administration et de surveillance en cas d’erreur.

Vous pouvez effectuer une trace réseau concomitant entre le client et le serveur, puis examiner la trace pour déterminer la cause de l’échec de connexion entre l’agent client et le serveur d’administration MBAM.

> [!Note]
> Si vous pouvez accéder aux URL du service à partir de l’ordinateur client et qu’il y a des entrées d’erreur de connectivité dans les journaux des événements d’administration MBAM, cela peut être dû à un échec de connectivité entre le serveur d’administration et le serveur de base de données.

Si vous parvenez à parcourir les deux URL de service, et qu’il existe une connectivité entre le client et le serveur en cours d’exécution, le service IIS fonctionne. Toutefois, il est possible qu’il y ait un problème de communication entre le serveur qui exécute les services Internet et le serveur de base de données.

Les services MBAM peuvent ne pas être en mesure de se connecter au serveur de base de données en raison d’un problème de réseau ou d’un paramètre de chaîne de connexion de base de données incorrect. Passez en revue les journaux d’application sur le serveur d’administration et de surveillance. Des entrées d’erreur ou des avertissements provenant de sources ASP.NET 2.0.50727.0 similaires à ceux de l’entrée de journal suivante peuvent s’afficher:

    Log Name:      Application
    Source:        ASP.NET 2.0.50727.0
    Date:          7/11/2013 6:16:34 PM
    Event ID:      1310
    Task Category: Web Event
    Level:         Warning
    Keywords:      Classic
    User:          N/A
    Computer:      MBAM2-Admin.contoso.com
    Description:
    Event code: 100001
    Event message: SQL error occurred
    Event time: 7/11/2013 6:16:34 PM
    Event time (UTC): 7/11/2013 12:46:34 PM
    Event ID: 6615fb8eb9d54e778b933d5bb7ca91ed
    Event sequence: 2
    Event occurrence: 1
    Event detail code: 0 
    Application information:
        Application domain: /LM/W3SVC/2/ROOT/MBAMAdministrationService-1-130180202570338699
        Trust level: Full
        Application Virtual Path: /MBAMAdministrationService
        Application Path: C:\inetpub\Microsoft BitLocker Management Solution\Administration Service\
        Machine name: MBAM2-ADMIN 
    
    Process information:
        Process ID: 1940
        Process name: w3wp.exe
        Account name: NT AUTHORITY\NETWORK SERVICE 
    
    Exception information:
        Exception type: SqlException
        Exception message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server) 
    
    Request information:
        Request URL: 
        Request path: 
        User host address: 
        User: 
        Is authenticated: False
        Authentication Type: 
        Thread account name: NT AUTHORITY\NETWORK SERVICE 
    
    Thread information:
        Thread ID: 7
        Thread account name: NT AUTHORITY\NETWORK SERVICE
        Is impersonating: False
        Stack trace:    at System.Data.SqlClient.SqlInternalConnection.OnError(SqlException exception, Boolean breakConnection)
       at System.Data.SqlClient.TdsParser.ThrowExceptionAndWarning(TdsParserStateObject stateObj)
       at System.Data.SqlClient.TdsParser.Connect(ServerInfo serverInfo, SqlInternalConnectionTds connHandler, Boolean ignoreSniOpenTimeout, Int64 timerExpire, Boolean encrypt, Boolean trustServerCert, Boolean integratedSecurity, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.AttemptOneLogin(ServerInfo serverInfo, String newPassword, Boolean ignoreSniOpenTimeout, Int64 timerExpire, SqlConnection owningObject)
       at System.Data.SqlClient.SqlInternalConnectionTds.LoginNoFailover(String host, String newPassword, Boolean redirectedUserInstance, SqlConnection owningObject, SqlConnectionString connectionOptions, Int64 timerStart)
       at System.Data.SqlClient.SqlInternalConnectionTds.OpenLoginEnlist(SqlConnection owningObject, SqlConnectionString connectionOptions, String newPassword, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlInternalConnectionTds..ctor(DbConnectionPoolIdentity identity, SqlConnectionString connectionOptions, Object providerInfo, String newPassword, SqlConnection owningObject, Boolean redirectedUserInstance)
       at System.Data.SqlClient.SqlConnectionFactory.CreateConnection(DbConnectionOptions options, Object poolGroupProviderInfo, DbConnectionPool pool, DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionFactory.CreatePooledConnection(DbConnection owningConnection, DbConnectionPool pool, DbConnectionOptions options)
       at System.Data.ProviderBase.DbConnectionPool.CreateObject(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.UserCreateRequest(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionPool.GetConnection(DbConnection owningObject)
       at System.Data.ProviderBase.DbConnectionFactory.GetConnection(DbConnection owningConnection)
       at System.Data.ProviderBase.DbConnectionClosed.OpenConnection(DbConnection outerConnection, DbConnectionFactory connectionFactory)
       at System.Data.SqlClient.SqlConnection.Open()
       at System.Data.Linq.SqlClient.SqlConnectionManager.UseConnection(IConnectionUser user)
       at System.Data.Linq.SqlClient.SqlProvider.get_IsSqlCe()
       at System.Data.Linq.SqlClient.SqlProvider.InitializeProviderMode()
       at System.Data.Linq.SqlClient.SqlProvider.System.Data.Linq.Provider.IProvider.Execute(Expression query)
       at System.Data.Linq.DataContext.ExecuteMethodCall(Object instance, MethodInfo methodInfo, Object[] parameters)
       at Microsoft.Mbam.Server.ServiceCommon.KeyRecoveryModelDataContext.GetRecoveryKeyIds(String partialRecoveryKeyId, String reason)
       at Microsoft.Mbam.ApplicationSupportService.AdministrationService.GetRecoveryKeyIds(String partialRecoveryKeyId, String reasonCode)
    
    Custom event details:
        Application: MBAMAdministrationService
        Sql Server:
        Database: MBAM Recovery and Hardware
        Database: MBAM Compliance Status
        Sql ErrorCode: 5
        Error Message: A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections. (provider: Named Pipes Provider, error: 40 - Could not open a connection to SQL Server)

#### Causes possibles

##### Cause 1

L’administrateur a pu spécifier un nom de l’instance de base de données ou un nom de base de données non valide lors de l’installation des composants serveur d’administration et de surveillance.

Vous pouvez vérifier et corriger les chaînes de connexion de la base de données à l’aide de la console de gestion IIS. Pour ce faire, ouvrez le gestionnaire des services Internet et naviguez jusqu’à l’administration et à la surveillance de Microsoft BitLocker. Pour chaque service figurant sur le côté gauche, procédez comme suit pour modifier les chaînes de connexion de base de données:

1. Dans l' **affichage fonctionnalités**, double-sélectionnez **chaînes de connexion**.

2. Dans la page **chaînes de connexion** , sélectionnez la chaîne de connexion que vous souhaitez modifier.

3. Dans le volet **actions** , sélectionnez **modifier**.

4. Dans la boîte de dialogue **modifier la chaîne de connexion** , modifiez les propriétés que vous souhaitez modifier, puis sélectionnez **OK**.

##### Cause 2

Port SQL Server bloqué dans le pare-feu. Vérifiez le numéro de port sur lequel SQL Server est configuré pour l’écoute et assurez-vous que le port est ouvert dans le pare-feu entre le serveur d’administration et le serveur de base de données.

##### Cause 3

Liaisons TCP/IP incorrectes SQL Server. Vérifiez les liaisons TCP/IP SQL dans le gestionnaire de configuration SQL Server sur le serveur de base de données. MBAM doit être activé pour la connexion à la base de données par le biais de protocoles TCP/IP et de canaux nommés.

##### Cause 4

Le compte de service NT Nt\service ou le compte d’ordinateur du serveur d’administration MBAM ne disposent pas des autorisations nécessaires pour la connexion à la base de données SQL.

Lors de l’installation des composants de base de données sur le serveur de base de données, le programme d’installation crée deux groupes locaux: audit de la conformité MBAM et accès aux bases de données et de récupération MBAM.

Le compte de service NT Authority\Network, le compte d’ordinateur du serveur d’administration MBAM et l’utilisateur qui installe les composants de base de données sont ajoutés automatiquement à ces groupes.

Ces groupes disposent des autorisations requises sur la base de données au cours de l’installation. Tous les utilisateurs qui font partie de ce groupe reçoivent automatiquement les autorisations requises sur la base de données.

Le service Web n’est pas connecté au serveur de base de données en raison d’un problème d’autorisations si une ou plusieurs des conditions suivantes sont remplies:

* Les groupes mentionnés précédemment sont supprimés des groupes locaux sur le serveur de base de données.

* Le compte de service NT Nt\service et le compte d’ordinateur du serveur d’administration MBAM ne sont pas membres de ces groupes.

* Ces groupes ne disposent pas des autorisations requises sur la base de données.

Vous remarquerez les erreurs liées aux autorisations dans les journaux de l’application sur le serveur d’administration et de surveillance de MBAM si l’une des conditions précédentes est vraie. Dans ce cas, vous devez ajouter manuellement le compte de service NT Nt\service et le compte d’ordinateur du serveur d’administration MBAM, et leur accorder un rôle public au niveau du serveur sur le serveur de base de données SQL qui utilise SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### Examiner les journaux de service Web

Si aucun événement n’est consigné dans les journaux d’application sur le serveur d’administration MBAM, il est temps de passer en revue les journaux de service Web (. svclog) du service Web MBAM hébergé sur le serveur d’administration et de surveillance MBAM. Pour afficher le fichier journal, vous devez utiliser l’outil visionneuse de suivi de service (SvcTraceViewer.exe) https://msdn.microsoft.com/library/ms732023.aspx .

Vous devez examiner essentiellement les journaux de suivi de service de RecoveryandHardwareService et ComplianceStatusService. Par défaut, les journaux de service Web se trouvent dans le dossier Solution\Logs de gestion de C:\inetpub\Microsoft BitLocker. Là, chaque service écrit son fichier. svclog dans son propre dossier.

Examinez l’activité du journal de suivi des services pour toutes les entrées d’erreur ou d’avertissement. Par défaut, les entrées d’erreur sont mises en surbrillance en rouge. Sélectionnez la description d’erreur dans le volet droit de la visionneuse de suivi pour afficher des informations détaillées sur l’entrée d’erreur. Voici un exemple d’entrée d’erreur du journal de suivi:

    <E2ETraceEvent xmlns="http://schemas.microsoft.com/2004/06/E2ETraceEvent">
    <System xmlns="http://schemas.microsoft.com/2004/06/windows/eventlog/system">
    <EventID>15183</EventID>
    <Type>3</Type>
    <SubType Name="Error">0</SubType>
    <Level>2</Level>
    <TimeCreated SystemTime="2013-07-05T14:48:06.2821550Z" />
    <Source Name="Microsoft.Mbam.CoreService" />
    <Correlation ActivityID="{00000000-0000-0000-0000-000000000000}" />
    <Execution ProcessName="w3wp" ProcessID="4332" ThreadID="11" />
    <Channel />
    <Computer>XXXXXXXXXXX</Computer>
    </System>
    <ApplicationData>AddUpdateVolume: While executing sql transaction for add volume to store exception occurred Key Recovery Data Store processing error: Violation of UNIQUE KEY constraint 'UniqueRecoveryKeyId'. Cannot insert duplicate key in object 'RecoveryAndHardwareCore.Keys'. The duplicate key value is (8637036e-b379-4798-bd9e-5a0b36296de3).
    </ApplicationData>
    </E2ETraceEvent>

## Nouvelle installation ou reconfiguration de l’infrastructure MBAM

Pour réinstaller ou reconfigurer l’infrastructure MBAM, vous devez connaître les éléments suivants:

* Compte du pool d’applications

* Groupes MBAM (assistance technique avancée, groupe utilisateurs de rapports)

* URL des rapports MBAM

* Nom SQL Server et noms de base de données

* MBAM les comptes et les ReadOnly

### Compte du pool d’applications

Pour trouver le compte du pool d’applications, connectez-vous au serveur Web MBAM, ouvrez le **Gestionnaire des services Internet (IIS)**, puis sélectionnez **pools d’applications**:

![pools d’applications](images/troubleshooting-MBAM-installation-1.png)

Le nom de principal de service (SPN) doit être défini dans ce compte. Ce paramètre est important pour la fonctionnalité de MBAM.

### Groupes MBAM (support technique, avancé, groupe utilisateurs de rapports et URL des rapports)

![Groupes MBAM](images/troubleshooting-MBAM-installation-2.png)

Cela fournit des informations telles que le groupe assistance, le groupe assistance avancée, le groupe utilisateurs de rapports et l’URL des rapports MBAM. L’URL des rapports MBAM doit être fournie dans le programme d’installation d’MBAM et doit prendre la forme: http (s)://servername/ReportServer.

### Noms de nom et de base de données SQL Server

Pour savoir quels sont les noms et instances SQL Server hébergeant les DBs MBAM, connectez-vous au serveur Web MBAM (IIS) et naviguez jusqu’à la sous-clé de Registre suivante:

**HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit](images/troubleshooting-MBAM-installation-3.png)

Les parties mises en surbrillance sont des chaînes de connexion. Celles-ci doivent avoir le nom SQL Server, les noms de base de données et les instances (s’ils sont nommés).

### MBAM les comptes et les ReadOnly

Ces informations seront dans la base de données SQL Server, pour lesquelles nous avons déjà trouvé le nom du serveur Web.

#### Compte ReadWrite

1. Connectez-vous à SQL Management Studio.

2. Dans MBAM, cliquez avec le bouton droit sur **restauration et matériel**, sélectionnez **Propriétés**, puis sélectionnez **autorisations**.

Par exemple, le nom du compte laboratoire est **MBAMWrite**. Le pool d’applications et les comptes ReadWrite sont définis en tant que tels.

![SQL DB](images/troubleshooting-MBAM-installation-4.png)

![Propriétés de BDD](images/troubleshooting-MBAM-installation-5.png)

Accédez à **sécurité** , puis **Connectez** -vous dans SQL Management Studio. Naviguez jusqu’au compte affiché dans la capture d’écran précédente.

![Sécurité SQL](images/troubleshooting-MBAM-installation-6.png)

Cliquez avec le bouton droit sur les comptes, accédez à l’image **mappage des utilisateurs**et recherchez la base de données de récupération et de MBAM:

![Mappage utilisateur](images/troubleshooting-MBAM-installation-7.png)

#### Compte ReadOnly

Ouvrez le gestionnaire de configuration SQL Server Reporting Services sur le serveur SSRS. Sélectionnez **URL du gestionnaire de rapports**, puis parcourez les **URL**:

![Gestionnaire de rapports](images/troubleshooting-MBAM-installation-8.png)

Sélectionnez **administration et surveillance de Microsoft BitLocker**:

![Administration et analyse de BitLocker](images/troubleshooting-MBAM-installation-9.png)

Sélectionnez **MaltaDatasource**:

![Bases](images/troubleshooting-MBAM-installation-10.png)

![MaltaDatasource](images/troubleshooting-MBAM-installation-11.png)

MaltaDataSource doit avoir le nom de compte ReadOnly et doit être utilisé dans la configuration MBAM.

## Référence

Pour plus d’informations, consultez les articles suivants:

[Déploiement de MBAM 2,5 dans une configuration autonome](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
