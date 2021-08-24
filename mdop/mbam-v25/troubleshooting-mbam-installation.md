---
title: Résolution des problèmes d’installation de MBAM 2.5
description: Présentation de la résolution des problèmes d’installation de MBAM 2.5.
author: Deland-Han
ms.reviewer: dcscontentpm
manager: dansimp
ms.author: delhan
ms.sitesec: library
ms.prod: w10
ms.date: 09/16/2019
ms.openlocfilehash: 6ea152792801c630fa365f37d1668d1a4d84b3a5
ms.sourcegitcommit: 3e0500abde44d6a09c7ac8e3caf5e25929b490a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2021
ms.locfileid: "11910629"
---
# <a name="troubleshooting-mbam-25-installation-problems"></a>Résolution des problèmes d’installation de MBAM 2.5

Cet article explique comment résoudre les problèmes d’installation de Microsoft BitLocker Administration and Monitoring (MBAM) 2.5 dans une configuration autonome.

## <a name="referring-mbam-log-files-for-troubleshooting"></a>Référence des fichiers journaux MBAM pour la résolution des problèmes

MBAM inclut la journalisation pour l’installation du serveur, l’installation du client et les événements. Cette journalisation doit être référente pour la résolution des problèmes. 
 
### <a name="mbam-server-installation-log-files"></a>Fichiers journaux d’installation du serveur MBAM

MBAMServerSetup.exe génère les fichiers journaux suivants dans le dossier %temp% de l’utilisateur lors de l’installation de MBAM :<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14 chiffres>.log**

MBAMServerSetup.exe journal des actions qui ont été prises lors de l’installation de MBAM et de l’installation des fonctionnalités serveur MBAM :<br /> **Microsoft_BitLocker_Administration_and_Monitoring_<14_numbers>_0_MBAMServer.msi.log**

MBAMServerSetup.exe journal des actions supplémentaires qui ont été prises pendant l’installation.

### <a name="mbam-client-installation-log-file"></a>Fichier journal d’installation du client MBAM

L’installation du client est enregistrée dans le fichier journal suivant dans le dossier %temp% (ou un emplacement personnalisé, selon la façon dont le client a été installé) : <br />**MSI \<five random characters\> .log**

Ce journal contient les actions entreprises lors de l’installation du client MBAM.
 
### <a name="mbam-client-event-logging-channel"></a>Canal de journalisation des événements du client MBAM

MBAM dispose de canaux de journalisation des événements distincts. Les fichiers journaux administrateur, analytique et opérationnel se trouvent dans l’Observateur d’événements, sous **Journaux**des applications et des services  >  **Microsoft**  >  **Windows**  >  **MBAM**.

Le tableau suivant fournit une brève description de chaque journal des événements.
 
|Journal des événements| Description|
|----------|-------|
|Microsoft-Windows-MBAM/Admin|  Contient des messages d’erreur|
|Microsoft-Windows-MBAM/Analytique|   Contient des informations de journalisation avancées|
|Microsoft-Windows-MBAM/Opérationnel|    Contient des messages de réussite|

### <a name="mbam-server-event-logging-channel"></a>Canal de journalisation des événements du serveur MBAM

Les fichiers journaux se trouvent dans l’Observateur d’événements, sous **Journaux**des applications et des services  >  **Microsoft**  >  **Windows**  >  **MBAM**. Le tableau suivant inclut les journaux des événements serveur introduits dans MBAM 2.5 :

|Journal des événements| Description|
|--------|-------------|
|Microsoft-Windows-MBAM/Admin|  Contient des messages d’erreur|
|Microsoft-Windows-MBAM/Analytique|   Contient des informations de journalisation avancées|
|Microsoft-Windows-MBAM/Opérationnel|    Contient des messages de réussite|

### <a name="mbam-web-service-logs"></a>Journaux du service web MBAM

Chaque journal du service web MBAM écrit les informations de journalisation dans un fichier SVCLOG. Par défaut, chaque service web écrit le fichier de suivi sous un dossier qui utilise son nom dans le dossier C:\inetpub\Microsoft BitLocker Management Solution\Logs.

Vous pouvez utiliser l’outil visionneuse de suivi de service (partie Microsoft Visual Studio) pour passer en revue les traces de svclog.

## <a name="troubleshooting-encryption-and-reporting-issues"></a>Résolution des problèmes de chiffrement et de rapport

Cette section contient des informations de dépannage pour les fonctionnalités serveur, les fonctionnalités client, les paramètres de configuration et les problèmes connus :
 
### <a name="mbam-client-installation-group-policy-settings"></a>Installation du client MBAM, paramètres de stratégie de groupe

Déterminez si l’agent MBAM est installé sur l’ordinateur client. Lorsque MBAM est installé, il crée un service nommé Service client de gestion BitLocker. Ce service est configuré pour démarrer automatiquement. Déterminez si le service est en cours d’exécution.

Assurez-vous que les paramètres de stratégie de groupe MBAM sont appliqués sur l’ordinateur client. La sous-clé de Registre suivante est créée si les paramètres de stratégie de groupe ont été appliqués sur l’ordinateur client : **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Vérifiez que cette clé existe et qu’elle est remplie à l’aide de valeurs par paramètres de stratégie de groupe.

### <a name="mbam-agent-in-the-initial-delay-period"></a>Agent MBAM au cours de la période de retard initiale

Le client MBAM ne démarre pas l’opération immédiatement après l’installation. Il existe un délai aléatoire initial de 1 à 18 minutes avant que l’agent MBAM démarre son opération. En plus du délai initial, il y a un délai d’au moins 90 minutes. (Le délai dépend des paramètres de stratégie de groupe configurés pour la fréquence de vérification de l’état du client.) Par conséquent, le délai total avant qu’un client démarre l’opération est un retard de démarrage aléatoire *du*délai de vérification de  +  *la fréquence du client*.

Si les journaux des événements opérationnels et d’administration sont vides, le client n’a pas encore démarré l’opération et se trouve dans la période de retard mentionnée précédemment. Si vous souhaitez ignorer le délai, suivez les étapes suivantes :
 
1. Arrêtez le service client de gestion BitLocker.

2. Sous la ** sous-cléHKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM** registre, créez la valeur de Registre **NoStartupDelay,** définissez son type sur **REG_DWORD,** puis définissez sa valeur sur **1**.

3. Sous **HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**, définissez les valeurs **ClientWakeupFrequency** et **StatusReportingFrequency** sur **1**. Ces valeurs revenir à leurs paramètres d’origine une fois les mises à jour de stratégie de groupe mises à jour sur l’ordinateur.

4. Démarrez le service client de gestion BitLocker.

Après le démarrage du service, si vous vous connectez localement sur l’ordinateur et qu’il n’y a aucune erreur, vous devez recevoir une demande de chiffrement de l’ordinateur dans un délai d’une minute. Si vous ne recevez pas de demande, vous devez consulter les journaux de l’administrateur MBAM pour les entrées d’erreur.

### <a name="computer-does-not-have-a-tpm-device-or-the-tpm-device-is-not-enabled-in-the-bios"></a>L’ordinateur n’a pas de périphérique de TPM ou n’est pas activé dans le BIOS.

Examinez le journal des événements de l’administrateur MBAM. Vous verrez une entrée d’événement semblable à ce qui suit dans le journal des événements de l’administrateur MBAM :

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

Ouvrez la gestion du TPM (tpm.msc) et vérifiez si l’ordinateur dispose d’un appareil TPM. Si tpm.msc n’affiche pas d’appareil, ouvrez le Gestionnaire de périphériques (devmgmt.msc) et recherchez un module de plateforme fiable sous Périphériques de sécurité. Si vous ne voyez pas d’appareil de module de plateforme de confiance, cela peut être vrai pour l’une des raisons suivantes :

* Votre système ne comprend pas de module de plateforme de confiance (TPM/Sécurité).

* Le périphérique de TPM est désactivé dans le BIOS.

* Le périphérique de TPM est activé dans le BIOS, mais la gestion de l’appareil du TPM à partir du paramètre du système d’exploitation est désactivée dans le BIOS.

* Vous n’utilisez pas de pilote Microsoft pour l’appareil du TPM. Examinez les appareils répertoriés dans le Gestionnaire de périphériques pour identifier le pilote de périphérique du TPM Microsoft.

Si le périphérique de TPM n’utilise pas le pilote C:\Windows\System32\tpm.sys, vous devez mettre à jour le pilote en sélectionnant le fichier C:\Windows\Inf\tpm.inf.

### <a name="computer-does-not-have-a-valid-system-partition"></a>L’ordinateur n’a pas de partition SYSTÈME valide

Examinez le journal des événements de l’administrateur MBAM. Vous verrez une entrée d’événement semblable à ce qui suit dans le journal des événements de l’administrateur MBAM :

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

BitLocker nécessite une partition SYSTEM pour activer le chiffrement ( Chiffrement de lecteur[BitLocker dans Windows 7 : Questions fréquemment posées](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_partitions)).

MBAM ne crée pas automatiquement la partition système. Vous pouvez utiliser l’utilitaire de préparation de lecteur BitLocker (bdehdcfg.exe) pour créer la partition système et déplacer les fichiers de démarrage requis.

Par exemple, vous pouvez utiliser la commande **%windir%\system32\bdeHdCfg.exe -target default -size 300 –quiet** pour préparer le lecteur en mode silencieux avant de déployer MBAM pour chiffrer les lecteurs. Cela nécessite un redémarrage. Vous pouvez également scripter l’action si nécessaire. Le document suivant décrit l’outil de préparation du lecteur BitLocker :

[Description de l’outil de préparation du lecteur BitLocker](https://support.microsoft.com/help/933246)

### <a name="drives-are-not-formatted-to-have-a-compatible-file-system"></a>Les lecteurs ne sont pas formatés pour avoir un système de fichiers compatible

Consultez [l’article TechNet pour savoir comment le système de fichiers est requis pour BitLocker.](https://docs.microsoft.com/previous-versions/windows/it-pro/windows-7/ee449438(v=ws.10)?redirectedfrom=MSDN#bkmk_hsrequirements)

### <a name="group-policy-conflict"></a>Conflit de stratégie de groupe

Vous verrez une entrée d’événement semblable à ce qui suit dans le journal des événements de l’administrateur MBAM :

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

Vérifiez vos paramètres de stratégie de groupe pour vous assurer qu’il n’y a pas de paramètre conflictuelle parmi les paramètres de stratégie de groupe MBAM.

Vous devez configurer la stratégie de groupe à l’aide du modèle MBAM MDOP et non du modèle de chiffrement de lecteur BitLocker.

Par exemple :

Sous les paramètres de chiffrement du lecteur du système d’exploitation, vous avez sélectionné le TPM comme logiciel de protection, et vous avez également sélectionné Autoriser les **pinn améliorés au démarrage.** Il s’agit de paramètres conflictuelles, car la protection TPM uniquement ne nécessite pas de code confidentiel. Par conséquent, vous devez désactiver le paramètre de pin pin amélioré.

### <a name="user-may-have-requested-an-exemption"></a>L’utilisateur a peut-être demandé une exemption

Si vous avez activé le paramètre Configuration ordinateur\Modèles d’administration\Composants Windows\MDOP MBAM (Gestion BitLocker)\Gestion du client\Configurer le paramètre de stratégie d’exemption utilisateur, les utilisateurs auront la possibilité de demander une exemption.

Par défaut, si l’utilisateur demande une exemption, l’exemption sera valide pendant 7 jours et l’utilisateur ne recevra pas d’invites de chiffrement pendant cette période. (La valeur par défaut peut être augmentée ou diminuée pendant la configuration de la stratégie.) Une fois la période d’exonération terminée, l’utilisateur est invité à chiffrer.

Vous verrez l’entrée suivante dans le journal des événements de l’administrateur MBAM lorsqu’un ordinateur est sous exemption utilisateur :

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

Si vous souhaitez remplacer manuellement l’exemption utilisateur pour un ordinateur, suivez les étapes suivantes :
 
1. Définissez la valeur AllowUserExemption sur **0** sous la sous-clé de Registre suivante : <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

2. Supprimez toutes les valeurs de Registre sous la sous-clé de Registre suivante à l’exception de **AgentVersion,** **EncodedComputerName**et **Installed**:<br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM**

    **Remarque** Vous devez redémarrer l’agent MBAM pour que les modifications prennent effet.

Sachez qu’après avoir appliqué la stratégie de groupe à l’ordinateur, ces valeurs peuvent revenir à leurs paramètres d’origine.

### <a name="wmi-issue"></a>Problème WMI

MBAM utilise les méthodes de la classe win32_encryptablevolume pour gérer BitLocker. Si ce module n’est pas enregistré ou endommagé, le client MBAM ne fonctionne pas correctement et vous verrez l’entrée d’événement suivante dans le journal des événements de l’administrateur MBAM :

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

En outre, vous pouvez remarquer que les stratégies de récupération et de matériel ne s’appliquent pas avec le code d'0x8007007e. Cela se traduit par « The specified module could not be found ».

Pour résoudre ce problème, vous devez réenregistrer **la classe win32_encryptablevolume** à l’aide de la commande suivante :

```cmd
mofcomp c:\Windows\System32\wbem\win32_encryptablevolume.mof
```

## <a name="troubleshooting-mbam-agent-communication-issues"></a>Résolution des problèmes de communication de l’agent MBAM

Cette section contient des informations de dépannage pour les problèmes suivants liés à la communication de l’agent MBAM :

### <a name="incorrect-mbam-service-url"></a>URL de service MBAM incorrecte

Si la valeur du service d’état de conformité MBAM ou du service de récupération et de matériel est incorrecte, vous verrez une entrée d’événement semblable à celle-ci dans le journal des événements d’administration MBAM sur l’ordinateur client :

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

Vérifiez les valeurs **de KeyRecoveryServiceEndPoint** et **StatusReportingServiceEndpoint** sous la sous-clé de Registre suivante sur l’ordinateur client : <br />
**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**

Par défaut, l’URL de KeyRecoveryServiceEndPoint (point de terminaison du service de récupération et de matériel MBAM) est au format suivant : <br />
**http:// \<servername\> : \<port\> /MBAMRecoveryAndHardwareService/CoreService.svc**

Par défaut, l’URL de StatusReportingServiceEndpoint (point de terminaison du service de rapports d’état MBAM) est au format suivant :<br />
**http:// : \<servername\> \<port\> /MBAMComplianceStatusService/StatusReportingService.svc**

> [!Note]
> Il ne doit y avoir aucun espace dans l’URL.

Si l’URL du service est incorrecte, vous devez corriger l’URL du service dans le paramètre de stratégie de groupe suivant :

**Configuration de l’ordinateur**  >  **Stratégies**  >  **Modèles d’administration**  >  **Windows composants**  >  **MDOP MBAM (BitLocker Management)**  >  **Gestion des clients**  >  **Configurer MBAM Services**

### <a name="connectivity-issue-that-affects-the-mbam-administration-server"></a>Problème de connectivité affectant le serveur d’administration MBAM

L’agent MBAM ne pourra pas publier de mises à jour dans la base de données en cas de problèmes de connectivité entre l’agent client et le serveur d’administration MBAM. Dans ce cas, vous remarquerez les entrées d’échec de connectivité dans le journal des événements d’administration MBAM sur l’ordinateur client :

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

Vérifications de base :

* Vérifiez la connectivité de base en pingant le serveur d’administration MBAM par nom et adresse IP. Vérifiez si vous pouvez vous connecter au site web d’administration mbam ou au port de service à l’aide de telnet ou portqry.

* Vérifiez que le service IIS est en cours d’exécution sur le serveur d’administration et de surveillance MBAM et que le service web MBAM est à l’écoute sur le même port que celui configuré sur l’ordinateur client MBAM ( `netstat –ano | find "portnumber"` ).

* Vérifiez que le numéro de port configuré pour le site web MBAM utilise le Gestionnaire des iis (inetmgr). Assurez-vous que le numéro de port est identique au numéro de port sur lequel le client écoute. Assurez-vous que le numéro de port n’est pas partagé par une autre application. Par exemple, une autre application sur le serveur ne doit pas utiliser le même port.

* S’il existe un pare-feu, assurez-vous que le port est ouvert dans le pare-feu ou le serveur proxy.

* Si la communication entre le client et le serveur est sécurisée, assurez-vous que vous utilisez un certificat SSL valide.

* Vérifiez la connectivité réseau entre le serveur web et le serveur de base de données vers lequel les données sont envoyées pour insertion. Vous pouvez vérifier la connectivité de la base de données entre le serveur web et le serveur de base de données à l’aide de l’administrateur de source de données ODBC. Des informations détaillées SQL Server résolution des problèmes de connexion sont disponibles dans La résolution des problèmes de connexion [au SQL Server Moteur de base de données](https://social.technet.microsoft.com/wiki/contents/articles/2102.how-to-troubleshoot-connecting-to-the-sql-server-database-engine.aspx).

#### <a name="troubleshooting-the-connectivity-issue"></a>Résolution du problème de connectivité

Assurez-vous que l’URL du service configurée sur le client est correcte. Copiez la valeur de l’URL de KeyRecoveryServiceEndPoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**) à partir du Registre et ouvrez-la dans Internet Explorer.

De même, copiez la valeur de l’URL de StatusReportingServiceEndpoint (**HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\FVE\MDOPBitLockerManagement**), puis ouvrez-la dans Internet Explorer.

> [!Note]
> Si vous ne pouvez pas accéder à l’URL à partir de l’ordinateur client, vous devez tester la connectivité réseau de base entre le client et le serveur qui exécute IIS. Voir les points 1, 2, 3 et 4 dans la section précédente.

En outre, examinez les journaux des applications sur le serveur d’administration et de surveillance pour les éventuelles erreurs.

Vous pouvez effectuer une trace réseau simultanée entre le client et le serveur, et examiner le suivi pour déterminer la cause de l’échec de connexion entre l’agent client et le serveur d’administration MBAM.

> [!Note]
> Si vous pouvez parcourir les URL de service à partir de l’ordinateur client et qu’il existe des entrées d’erreur de connectivité dans les journaux des événements d’administration MBAM, cela peut être dû à une défaillance de la connectivité entre le serveur d’administration et le serveur de base de données.

Si vous pouvez parcourir les deux URL de service et qu’il existe une connectivité entre le client et le serveur en cours d’exécution, IIS fonctionne. Toutefois, il peut y avoir un problème de communication entre le serveur qui exécute IIS et le serveur de base de données.

Les services MBAM risquent de ne pas pouvoir se connecter au serveur de base de données en raison d’un problème réseau ou d’un paramètre de chaîne de connexion de base de données incorrect. Examinez les journaux des applications sur le serveur d’administration et de surveillance. Vous pouvez voir des entrées d’erreur ou des avertissements provenant de la source ASP.NET 2.0.50727.0 qui ressemblent à l’entrée de journal suivante :

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

#### <a name="possible-causes"></a>Causes possibles

##### <a name="cause-1"></a>Cause 1

L’administrateur a peut-être spécifié un nom d’instance de base de données/nom de base de données non valide lors de l’installation des composants serveur d’administration et de surveillance.

Vous pouvez vérifier et corriger les chaînes de connexion de base de données à l’aide de la console de gestion IIS. Pour ce faire, ouvrez le Gestionnaire des services Internet et accédez à Microsoft BitLocker Administration and Monitoring. Pour chaque service répertorié sur le côté gauche, suivez ces étapes pour modifier les chaînes de connexion de base de données :

1. Dans **l’affichage des**fonctionnalités, double-sélectionnez **chaînes de connexion.**

2. Dans la page **Chaînes de** connexion, sélectionnez la chaîne de connexion à modifier.

3. Dans le **volet Actions,** sélectionnez **Modifier.**

4. Dans la **boîte de dialogue Modifier la chaîne** de connexion, modifiez les propriétés à modifier, puis sélectionnez **OK.**

##### <a name="cause-2"></a>Cause 2

SQL Server port bloqué dans le pare-feu. Vérifiez le numéro de port vers lequel SQL Server est configuré pour écouter et assurez-vous que le port est ouvert dans le pare-feu entre le serveur d’administration et le serveur de base de données.

##### <a name="cause-3"></a>Cause 3

Liaisons TCP/IP SQL serveur incorrects. Vérifiez SQL liaisons TCP/IP dans Gestionnaire de configuration SQL Server sur le serveur de base de données. MBAM requiert que les protocoles TCP/IP et Canaux nommés soient activés pour se connecter à la base de données.

##### <a name="cause-4"></a>Cause 4

Le compte d’autorité NT\service réseau ou le compte d’ordinateur du serveur d’administration MBAM ne sont pas autorisés à se connecter à la base de données SQL réseau.

Lors de l’installation des composants de base de données sur le serveur de base de données, le programme d’installation crée deux groupes locaux : MBAM Compliance Auditing DB Access et MBAM Recovery et Hardware DB Access.

Le compte NT Authority\Network Service, le compte d’ordinateur du serveur d’administration MBAM et l’utilisateur qui installe les composants de base de données sont automatiquement ajoutés à ces groupes.

Ces groupes se sont vu accorder les autorisations requises sur la base de données pendant l’installation. Tous les utilisateurs qui font partie de ce groupe reçoivent automatiquement les autorisations requises sur la base de données.

Le service web peut ne pas se connecter au serveur de base de données en raison d’un problème d’autorisations si une ou plusieurs des conditions suivantes sont vraies :

* Les groupes mentionnés précédemment sont supprimés des groupes locaux sur le serveur de base de données.

* Le compte d’autorité NT\service réseau et le compte d’ordinateur du serveur d’administration MBAM ne sont pas membres de ces groupes.

* Ces groupes ne sont pas autorisés sur la base de données.

Vous remarquerez les erreurs liées aux autorisations dans les journaux des applications sur le serveur d’administration et de surveillance MBAM si l’une des conditions précédentes est vraie. Dans ce cas, vous devez ajouter manuellement le compte d’autorité NT\Service réseau et le compte d’ordinateur du serveur d’administration MBAM et leur accorder un rôle public à l’échelle du serveur sur le serveur de base de données SQL qui utilise SQL Server Management Studio ( https://msdn.microsoft.com/library/aa337562.aspx) .

#### <a name="review-the-web-service-logs"></a>Consulter les journaux du service web

Si aucun événement n’est journalisé dans les journaux des applications sur le serveur d’administration MBAM, il est temps de passer en revue les journaux du service web (.svclog) du service web MBAM qui est hébergé sur le serveur d’administration et de surveillance MBAM. Vous devez utiliser l’outil Visionneuse de suivi de service (SvcTraceViewer.exe) pour https://msdn.microsoft.com/library/ms732023.aspx afficher le fichier journal.

Vous devez principalement examiner les journaux de suivi des services de RecoveryandHardwareService et ComplianceStatusService. Par défaut, les journaux du service web se trouvent dans le dossier C:\inetpub\Microsoft BitLocker Management Solution\Logs. Chaque service écrit alors son fichier .svclog sous son propre dossier.

Examinez l’activité dans le journal de suivi des services pour les entrées d’erreur ou d’avertissement. Par défaut, les entrées d’erreur sont mises en surbrillable en rouge. Sélectionnez la description de l’erreur dans le volet droit de la visionneuse de suivi pour afficher des informations détaillées sur l’entrée d’erreur. Voici un exemple d’entrée d’erreur à partir du journal de suivi :

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

## <a name="re-installation-or-reconfiguration-of-mbam-infrastructure"></a>Nouvelle installation ou reconfiguration de l’infrastructure MBAM

Pour réinstaller ou reconfigurer l’infrastructure MBAM, vous devez connaître les points suivants :

* Compte du pool d’applications

* Groupes MBAM (helpdesk, advanced, report users group)

* URL des rapports MBAM

* SQL Server et noms de base de données

* Comptes MBAM ReadWrite et ReadOnly

### <a name="application-pool-account"></a>Compte du pool d’applications

Pour trouver le compte du pool d’applications, connectez-vous au serveur web MBAM, ouvrez **Internet Information Services (IIS),** puis sélectionnez Pools d’applications : ****

![pools d’applications.](images/troubleshooting-MBAM-installation-1.png)

Le nom principal de service (SPN) doit être définie dans ce compte. Ce paramètre est très important pour les fonctionnalités de MBAM.

### <a name="mbam-groups-helpdesk-advanced-report-users-group-and-reports-url"></a>Groupes MBAM (Helpdesk, Advanced, Report Users Group and Reports URL)

![Groupes MBAM.](images/troubleshooting-MBAM-installation-2.png)

Cette page fournit des informations telles que groupe d’aide, groupe d’aide avancée, groupe Utilisateurs de rapports et URL de rapports MBAM. L’URL des rapports MBAM doit être fournie dans le programme d’installation de MBAM et doit être : http(s)://servername/ReportServer.

### <a name="sql-server-name-and-database-db-names"></a>SQL Server et noms de base de données (DB)

Pour trouver les SQL Server et instances hébergeant les DB MBAM, connectez-vous au serveur Web MBAM (IIS) et accédez à la sous-clé de Registre qui s’y trouve :

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MBAM Server\Web**

![Regedit.](images/troubleshooting-MBAM-installation-3.png)

Les parties mises en surbrill ouest sont des chaînes de connexion. Celles-ci doivent avoir le SQL Server, les noms de base de données et les instances (s’ils sont nommés).

### <a name="mbam-readwrite-and-readonly-accounts"></a>Comptes MBAM ReadWrite et ReadOnly

Ces informations se trouveront dans la base SQL Server de données, pour laquelle nous avons déjà trouvé le nom à partir du serveur web.

#### <a name="readwrite-account"></a>Compte ReadWrite

1. Connectez-vous au SQL Management Studio.

2. Cliquez avec le bouton **droit sur Récupération MBAM et matériel,** sélectionnez **Propriétés,** puis **sélectionnez Autorisations.**

Par exemple, le nom du compte d’atelier **est MBAMWrite**. Les comptes De pool d’applications et ReadWrite sont définies pour être identiques.

![SQL DB.](images/troubleshooting-MBAM-installation-4.png)

![Propriétés de la DB.](images/troubleshooting-MBAM-installation-5.png)

Accédez **à Sécurité,** puis **connectez-vous** SQL Management Studio. Accédez au compte illustré dans la capture d’écran précédente.

![SQL Sécurité.](images/troubleshooting-MBAM-installation-6.png)

Cliquez avec le bouton droit sur les comptes, cliquez sur **Mappage**des utilisateurs des propriétés et recherchez la base de données matérielle et de récupération MBAM :

![Mappage utilisateur.](images/troubleshooting-MBAM-installation-7.png)

#### <a name="readonly-account"></a>Compte ReadOnly

Ouvrez SQL Server Reporting Services Configuration Manager sur le serveur SSRS. Sélectionnez **l’URL du**Gestionnaire de rapports, puis parcourez les **URL**:

![Gestionnaire de rapports.](images/troubleshooting-MBAM-installation-8.png)

Sélectionnez **Microsoft Bitlocker Administration and Monitoring**:

![Administration et surveillance de Bitlocker.](images/troubleshooting-MBAM-installation-9.png)

Sélectionnez **MalteDatasource**:

![DBs.](images/troubleshooting-MBAM-installation-10.png)

![MalteDatasource.](images/troubleshooting-MBAM-installation-11.png)

MalteDataSource doit avoir le nom de compte ReadOnly et doit être utilisé dans le programme d’installation de MBAM.

## <a name="reference"></a>Référence

Pour plus d’informations, consultez les articles suivants :

[Déploiement de MBAM 2.5 dans une configuration autonome](https://support.microsoft.com/help/3046555)

[Microsoft BitLocker Administration and Monitoring 2.5](https://docs.microsoft.com/microsoft-desktop-optimization-pack/mbam-v25/)
