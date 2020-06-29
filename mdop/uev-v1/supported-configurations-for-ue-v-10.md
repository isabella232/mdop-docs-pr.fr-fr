---
title: Configurations prises en charge pour UE-V1.0
description: Configurations prises en charge pour UE-V1.0
author: dansimp
ms.assetid: d90ab83e-741f-48eb-b1d8-a64cb9259f7a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a84514317de8a4cfd9df9c94a9a130933b00874a
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811225"
---
# Configurations prises en charge pour UE-V1.0


La virtualisation de l’interface utilisateur de Microsoft (UE-V) prend en charge les configurations décrites ci-dessous.

**Remarques**  Microsoft prend en charge le Service Pack actuel et, dans certains cas, le Service Pack précédent. Pour savoir comment accéder aux délais de prise en charge de votre produit, voir les [Service Packs pris en charge](https://go.microsoft.com/fwlink/p/?LinkId=31975). Pour plus d’informations sur la politique de support du support Microsoft, voir FAQ sur la politique de support [Microsoft](https://go.microsoft.com/fwlink/p/?LinkId=31976).

 

## Configurations prises en charge pour les agents UE-V et UE-V Generator


Le tableau suivant répertorie les systèmes d’exploitation qui prennent en charge le générateur de virtualisation des utilisateurs et l’agent de virtualisation de l’utilisation de l’utilisateur.

<table>
<colgroup>
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
<col width="20%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Système d’exploitation</strong></th>
<th align="left"><strong>Édition</strong></th>
<th align="left"><strong>Service Pack</strong></th>
<th align="left"><strong>Architecture système</strong></th>
<th align="left"><strong>Microsoft .NET Framework</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Plus de.</p></td>
<td align="left"><p>Edition intégrale, entreprise ou édition professionnelle</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (générateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2008R2</p></td>
<td align="left"><p>Standard, entreprise, centre de données ou serveur Web</p></td>
<td align="left"><p>SP1</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 3,5 SP1</p>
<p>.NET Framework 4 (générateur)</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Windows8</p></td>
<td align="left"><p>Edition entreprise ou professionnel</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>32bits ou 64bits</p></td>
<td align="left"><p>.NET Framework 4 ou .NET Framework 3,5 SP1 (agent)</p>
<p>.NET Framework 4 (générateur)</p></td>
</tr>
<tr class="even">
<td align="left"><p>Windows Server2012</p></td>
<td align="left"><p>Standard ou Datacenter</p></td>
<td align="left"><p>None</p></td>
<td align="left"><p>64 bits</p></td>
<td align="left"><p>.NET Framework 4 ou .NET Framework 3,5 SP1 (agent)</p>
<p>.NET Framework 4 (générateur)</p></td>
</tr>
</tbody>
</table>

 

Il n’existe aucune exigence spéciale en RAM qui est spécifique à UE-V.

L’installation de l’agent UE-V nécessite des privilèges d’administration et nécessite un redémarrage de l’ordinateur pour que l’agent UE-V puisse s’exécuter.

**Important**  La fonction synchroniser vos paramètres de Windows 8 doit être désactivée pour permettre à UE-V de fonctionner correctement. La synchronisation des paramètres avec Windows 8 et UE-V entraîne un comportement de synchronisation inattendus.

 

### <a href="" id="requirements-for-the-offline-files-feature-"></a>Configuration requise pour la fonctionnalité fichiers hors connexion

L’agent UE-V peut synchroniser les paramètres utilisateur pour les ordinateurs qui ne sont pas toujours connectés au réseau d’entreprise, comme un ordinateur portable ou des ordinateurs situés sur des bureaux distants, ainsi que des ordinateurs qui sont toujours connectés au réseau d’entreprise, tels que des serveurs Windows qui hébergent des sessions VDI (Virtual Desktop interface).

La configuration par défaut d’UE-V utilise la fonctionnalité fichier hors connexion Windows pour synchroniser les paramètres. Les fichiers hors connexion permettent de s’assurer que les paramètres de l’utilisateur sont disponibles même lorsque l’ordinateur quitte le réseau d’entreprise. Les modifications apportées aux paramètres sont synchronisées automatiquement avec l’emplacement de stockage des paramètres lorsque la connexion au réseau d’entreprise est rétablie. Les fichiers hors connexion permettent également de s’assurer que les paramètres de l’utilisateur sont disponibles pour les ordinateurs situés dans un bureau distant doté d’une connexion lente ou limitée.

Pour synchroniser les paramètres des ordinateurs qui quittent occasionnellement le réseau d’entreprise, la fonctionnalité fichiers hors connexion doit être activée et démarrée avant le début du déploiement de l’agent UE-V. La fonctionnalité fichiers en mode hors connexion est activée par défaut sur le réseau de fichiers. Cette fonctionnalité est désactivée par défaut dans Windows Server2008R2, Windows Server 2012 et Windows 8. Si la fonctionnalité fichiers en mode hors connexion n’est pas activée, la synchronisation des paramètres d’UE-V échoue.

-   **Windows7**

    La fonctionnalité fichiers en mode hors connexion est activée par défaut dans Windows 7. Le cas échéant, les fichiers hors connexion peuvent être activés à l’aide de la commande suivante à l’invite de commandes avec élévation de privilèges:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows8**

    La fonctionnalité fichiers en mode hors connexion est désactivée par défaut dans Windows 8 version. Les fichiers hors connexion peuvent être activés sur Windows 8 à l’aide de la commande suivante à l’invite de commandes avec élévation de privilèges:

    ``` syntax
    sc config CscService start=auto
    ```

-   **Windows Server 2008 R2 et Windows Server 2012**

    La fonctionnalité fichiers hors connexion n’est pas installée par défaut sur Windows Server 2008 R2 ou Windows Server 2012. Pour que vous puissiez activer la fonctionnalité fichiers en mode hors connexion, le module expérience de bureau doit être installé. Il s’agit d’un composant serveur facultatif qui inclut la fonctionnalité fichiers en mode hors connexion. Une fois l’installation terminée, démarrez la fonctionnalité fichiers en mode hors connexion avec les commandes suivantes à l’invite de commandes avec élévation de privilèges:

    ``` syntax
    sc config csc start= system
    ```

    ``` syntax
    sc config cscservice start= auto
    ```

L’ordinateur doit être redémarré pour que les paramètres soient synchronisés.

### Synchronisation pour les ordinateurs disposant de connexions toujours disponibles

Lorsque vous utilisez UE-V sur des ordinateurs qui sont toujours connectés au réseau d’entreprise, par exemple un ordinateur Windows Server hébergeant des sessions VDI, les fichiers hors connexion doivent être désactivés.

Lorsque l’agent UE-V est configuré pour synchroniser les paramètres sans utiliser de fichiers hors connexion, le serveur de stockage des paramètres est considéré comme un partage réseau standard. Les paramètres sont synchronisés lorsque le réseau est disponible. Dans cette configuration, l’agent UE-V peut être configuré pour envoyer une notification si l’importation des paramètres d’application est retardée.

Si la fonctionnalité fichiers en mode hors connexion ne sera pas utilisée, vous devez désactiver le comportement par défaut de UE-V avant ou pendant le déploiement de l’agent UE-V. Pour désactiver les fichiers hors connexion pour UE-V, effectuez l’une des opérations suivantes:

-   Avant de déployer l’agent UE-V, activez la case à cocher «ne pas utiliser les fichiers hors connexion» du paramètre de stratégie de groupe UE-V.

-   Lors de l’installation d’UE-V, définissez le paramètre AgentSetup.exe `SyncMethod = None` à l’invite de commandes ou dans un fichier de commandes. Pour plus d’informations sur le déploiement de l’agent, voir [déploiement de l’agent UE-V](deploying-the-ue-v-agent.md).

Si vous désactivez le paramètre fichiers en mode hors connexion pour UE-V et que vous ne spécifiez pas le paramètre **PowerSchool** lors de l’installation, l’installation de l’agent UE-v échoue. Vous pouvez également désactiver les fichiers hors connexion avec PowerShell ou WMI. Pour plus d’informations sur les commandes WMI et PowerShell, voir [gestion de l’agent et des packages d’UE-V 1,0 avec PowerShell et WMI](managing-the-ue-v-10-agent-and-packages-with-powershell-and-wmi.md).

L’ordinateur doit être redémarré pour que les paramètres soient synchronisés.

### Conditions préalables pour la fonctionnalité PowerShell d’UE-V

Pour pouvoir activer et utiliser PowerShell version 2,0 ou une version ultérieure, vous 3,5 devez activer la fonctionnalité PowerShell d’UE-V de l’agent.

### Conditions préalables pour la prise en charge du générateur UE-V

Installez le générateur UE-V sur l’ordinateur utilisé pour créer des modèles d’emplacement des paramètres personnalisés. Ces applications doivent être installées sur l’ordinateur pour que les paramètres soient itinérants. Vous devez être membre du groupe Administrateurs sur l’ordinateur exécutant le logiciel UE-V Generator. Par ailleurs, UE-V Generator doit être installé sur un ordinateur qui utilise un système de fichiers NTFS. Le logiciel de générateur UE-V nécessite .NET Framework version 4. Pour plus d’informations, consultez [planification du déploiement de modèles personnalisés pour UE-V 1,0](planning-for-custom-template-deployment-for-ue-v-10.md).

## Rubriques connexes


[Planification pour UE-V1.0](planning-for-ue-v-10.md)

[Préparation de votre environnement pour UE-V](preparing-your-environment-for-ue-v.md)

[Déploiement d'UE-V1.0](deploying-ue-v-10.md)

Configurations prises en charge pour la virtualisation de l’utilisation des utilisateurs avec [le déploiement de l’emplacement de stockage des paramètres pour UE-V 1,0](deploying-the-settings-storage-location-for-ue-v-10.md)

[Installation du Générateur UE-V](installing-the-ue-v-generator.md)

[Déploiement de l'agent UE-V](deploying-the-ue-v-agent.md)

 

 





