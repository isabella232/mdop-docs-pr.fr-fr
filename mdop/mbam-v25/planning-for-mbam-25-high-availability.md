---
title: Planification de la haute disponibilité de MBAM2.5
description: Planification de la haute disponibilité de MBAM2.5
author: dansimp
ms.assetid: 1e29b30c-33f1-4a52-9442-8c1391f0049c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 20c304f669cfe9e1484be47dea1b9fcc917aea2c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812059"
---
# Planification de la haute disponibilité de MBAM2.5


Le contrôle et l’administration de BitLocker (MBAM) Microsoft BitLocker peuvent garantir une disponibilité élevée grâce à l’utilisation d’une ou de plusieurs des technologies suivantes, qui sont décrites dans les sections suivantes:

-   [Groupes de disponibilité SQL Server AlwaysOn](#bkmk-alwayson)

-   [Regroupement Microsoft SQL Server](#bkmk-sql-clustering)

-   [Équilibrage de la charge réseau IIS](#bkmk-load-balance)

-   [Mise en miroir de base de données dans SQL Server](#bkmk-db-mirroring)

-   [Sauvegarder des bases de données MBAM à l’aide du service de cliché instantané de volume](#bkmk-vss)

Utilisez les informations contenues dans les sections suivantes pour mieux comprendre les options de déploiement d’MBAM dans une configuration très disponible.

## <a href="" id="bkmk-alwayson"></a>Prise en charge des groupes de disponibilité SQL Server AlwaysOn


MBAM vous permet de configurer et de gérer les groupes de disponibilités pour les bases de données dans Microsoft SQL Server. Un groupe de disponibilité pour MBAM prend en charge un environnement de basculement dans lequel la base de données d’audit et de conformité et la base de données de récupération échouent ensemble plutôt que séparément.

Un groupe de disponibilité prend en charge un ensemble de bases de données principales en lecture/écriture et un à quatre ensembles de bases de données secondaires correspondantes. Les bases de données secondaires peuvent éventuellement être mises à disposition d’autorisations en lecture seule, de quelques opérations de sauvegarde ou pour les deux.

Pour plus d’informations sur la configuration des groupes de disponibilité, voir groupes de disponibilité [AlwaysOn](https://go.microsoft.com/fwlink/?LinkId=393277).

## <a href="" id="bkmk-sql-clustering"></a>Regroupement Microsoft SQL Server


Vous pouvez exécuter la base de données d’audit et de conformité MBAM 2,5 et la base de données de récupération sur des ordinateurs exécutant des clusters SQL Server.

## <a href="" id="bkmk-load-balance"></a>Équilibrage de la charge réseau IIS


Vous pouvez utiliser le service d’équilibrage de la charge réseau pour configurer un environnement hautement disponible pour les ordinateurs qui exécutent le site Web d’administration et de contrôle (également appelé support technique), le portail libre-service et les services Web déployés via Internet Information Services (IIS).

### Conditions préalables

Avant de configurer l’équilibrage de charge, assurez-vous que vous remplissez les conditions préalables suivantes:

-   Un équilibrage de charge doit être disponible. Vous pouvez utiliser des équilibreurs de charge de Microsoft ou d’une autre société. Pour plus d’informations sur la technologie de l’équilibrage de charge Microsoft, voir [créer une batterie de serveurs Web avec des serveurs IIS](https://go.microsoft.com/fwlink/?LinkId=393326).

-   Au moins deux serveurs exécutent IIS et répondent à toutes les conditions préalables MBAM pour prendre en charge ses fonctionnalités Web, notamment ASP.NET MVC 4.

-   Les bases de données et rapports MBAM s’exécutent sur un serveur.

### <a href="" id="-------------mbam-specific-changes-that-are-required-to-enable-load-balancing"></a> Modifications spécifiques à MBAM requises pour activer l’équilibrage de charge

Effectuez les tâches suivantes:

1.  Enregistrez un nom de principal de service (SPN) pour le nom d’hôte virtuel sous le compte de domaine que vous utilisez pour les pools d’applications Web. Par exemple, si le nom d’hôte virtuel est mbamvirtual.contoso.com et que le compte de domaine utilisé pour les pools d’applications Web est contoso\\mbamapppooluser, la commande suivante enregistre le SPN de manière appropriée.

    `Setspn -s http//mbamvirtual contoso\mbamapppooluser`

    `Setspn -s http//mbamvirtual.contoso.com contoso\mbamapppooluser`

2.  Configurez les fonctionnalités Web de MBAM suivantes:

    -   Sur chaque serveur qui héberge les fonctionnalités Web de MBAM, utilisez le même compte de domaine pour les informations d’identification d’administration de pool d’applications.

    -   Spécifiez un nom d’hôte qui correspond au nom d’hôte virtuel (nom DNS) du cluster d’équilibrage de charge. Par exemple, lorsque vous installez MBAM sur un serveur appelé «NLB1» avec un nom d’hôte virtuel de **mbamvirtual.contoso.com**, assurez-vous que le nom d’hôte que vous spécifiez dans la cmdlet Windows PowerShell est **mbamvirtual.contoso.com**.

3.  Si vous configurez les sites Web dans une batterie de serveurs Web avec un équilibreur de charge, vous devez configurer les sites Web pour qu’ils utilisent la même clé d’ordinateur.

    Pour plus d’informations, reportez-vous aux sections suivantes dans l' [élément machineKey (schéma de paramètres ASP.net)](https://msdn.microsoft.com/library/vstudio/w8h3skw9.aspx):

    -   Explication de la clé d’ordinateur

    -   Considérations en matière de déploiement de fermes Web

    Pour obtenir des instructions sur la génération automatique d’une clé, voir [générer une clé d’ordinateur (IIS 7)](https://technet.microsoft.com/library/cc772287.aspx).

Les informations relatives à l’équilibrage de charge s’appliquent également aux clusters d’équilibrage de charge réseau (NLB) IIS dans Windows Server 2012 ou Windows Server2008R2. La fonctionnalité d’équilibrage de charge réseau d’IIS dans Windows Server 2012 est en général similaire à celle de Windows Server2008R2. Toutefois, certains détails de la tâche diffèrent dans Windows Server 2012. Pour plus d’informations sur les nouvelles méthodes de tâches, voir [tâches de gestion et navigation dans Windows server 2012 R2 Preview et Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371).

## <a href="" id="bkmk-db-mirroring"></a>Mise en miroir de base de données dans SQL Server


MBAM prend en charge l’utilisation de la mise en miroir SQL Server, où la base de données d’audit et de conformité, ainsi que la base de données de récupération, sont mises en miroir à l’aide de deux instances de SQL Server pour chaque base de données. Avant d’implémenter la mise en miroir, sachez que la mise en miroir est progressivement interrompue, en plus des groupes de disponibilité, décrits plus haut dans cette rubrique.

Pour implémenter la mise en miroir pour MBAM, vous devez spécifier les chaînes de connexion appropriées pour la configuration de la base de données en miroir à l’aide de l’applet de la cmdlet Windows PowerShell **Enable-MbamWebApplication** . Pour plus d’informations sur les applets de MBAM 2,5 de Windows PowerShell, voir [Configuration des fonctionnalités du serveur 2,5 MBAM à l’aide de Windows PowerShell](configuring-mbam-25-server-features-by-using-windows-powershell.md).

### Exemples d’implémentation de la mise en miroir SQL Server à l’aide de Windows PowerShell

Les exemples suivants illustrent la manière dont vous pouvez implémenter la mise en miroir SQL Server à l’aide d’applets de commande Windows PowerShell.

**Exemple1**

``` syntax
Enable-MbamWebApplication -AdministrationPortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -AdvancedHelpdeskAccessGroup “MyDomain\AdvancedUserGroup” -HelpdeskAccessGroup “MyDomain\StandardUserGroup” -ReportsReadOnlyAccessGroup "MyDomain\ReportUserGroup" -ReportUrl "https://MyReportServer/ReportServer" -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

**Exemple2**

``` syntax
Enable-MbamWebApplication -SelfServicePortal -ComplianceAndAuditDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer; Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Compliance Status";' -RecoveryDBConnectionString 'Integrated Security=SSPI;Data Source=MyDatabaseServer;I Failover Partner=myMirrorServerAddress;Initial Catalog="MBAM Recovery and Hardware";' -Port 443 -WebServiceApplicationPoolCredential (Get-Credential) -Certificate (dir cert:\LocalMachine\My\E2A7EA5533890D6567E40DFC46F53B3D31D6B689)
```

### Plus d’informations sur la mise en miroir SQL Server

Les liens suivants fournissent des informations supplémentaires sur la configuration de la mise en miroir SQL Server:

-   [Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Établir une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377)

## <a href="" id="bkmk-vss"></a>Sauvegarder des bases de données MBAM à l’aide du service de cliché instantané de volume


MBAM fournit un writer de service de cliché instantané de volume (VSS) appelé Microsoft BitLocker Administration and Management Writer. Ce writer VSS facilite la sauvegarde de la base de données d’audit et de conformité et de la base de données de récupération.

Le writer VSS est inscrit sur chaque serveur sur lequel vous activez une application Web MBAM. Le writer VSS MBAM dépend du writer SQL Server VSS qui est inscrit dans le cadre de l’installation de Microsoft SQL Server. Toute technologie de sauvegarde qui utilise des Writers VSS pour effectuer une sauvegarde peut découvrir le scripteur VSS MBAM.



## Rubriques connexes


[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

 

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).




