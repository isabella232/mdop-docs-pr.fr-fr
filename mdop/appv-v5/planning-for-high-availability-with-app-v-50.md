---
title: Planification de la haute disponibilité avec App-V5.0
description: Planification de la haute disponibilité avec App-V5.0
author: dansimp
ms.assetid: 6d9a6492-23f8-465c-82e5-49c863594156
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: ebf586de7cae19d40d76c9c0c845f93e7bd9021b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805017"
---
# Planification de la haute disponibilité avec App-V5.0


Microsoft Application Virtualization 5,0 (App-V 5,0) les configurations système peuvent utiliser des options qui permettent de maintenir un niveau élevé de service disponible.

Utilisez les informations contenues dans les sections suivantes pour mieux comprendre les options de déploiement d’App-V 5,0 dans une configuration hautement disponible.

-   [Prise en charge du regroupement Microsoft SQL Server](#bkmk-sqlcluster)

-   [Prise en charge de l’équilibrage de charge réseau IIS](#bkmk-iisloadbal)

-   [Prise en charge des serveurs de fichiers en cluster lors de l’exécution du mode SCS](#bkmk-clusterscsmode)

-   [Prise en charge de la mise en miroir Microsoft SQL Server](#bkmk-sqlmirroring)

-   [Prise en charge de Microsoft SQL Server toujours activé](#bkmk-sqlalwayson)

## <a href="" id="bkmk-sqlcluster"></a>Prise en charge du regroupement Microsoft SQL Server


Vous pouvez exécuter la base de données de gestion App-V et la base de données de création de rapports sur des ordinateurs exécutant des clusters Microsoft SQL Server. Toutefois, vous devez les installer à l’aide de scripts.

Pour obtenir des instructions, reportez-vous à la rubrique [déploiement de la base de données App-V à l’aide de scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).

## <a href="" id="bkmk-iisloadbal"></a>Prise en charge de l’équilibrage de charge réseau IIS


Vous pouvez utiliser le service d’équilibrage de la charge réseau d’Internet Information Services (IIS) pour configurer un environnement hautement disponible pour les ordinateurs exécutant les services de gestion, de publication et de création de rapports de l’application-V 5. x.

Pour plus d’informations sur la configuration d’IIS et de l’équilibrage de charge réseau pour les ordinateurs exécutant les systèmes d’exploitation Windows Server, voir les rubriques suivantes:

-   Fournit des informations sur la configuration d’Internet Information Services (IIS) 7,0.

    Garantir [une disponibilité et une évolutivité élevées-ARR et NLB](https://go.microsoft.com/fwlink/?LinkId=316369) (https://go.microsoft.com/fwlink/?LinkId=316369)

-   Configuration de Microsoft Windows Server

    [Équilibrage de charge réseau](https://go.microsoft.com/fwlink/?LinkId=316370) ( https://go.microsoft.com/fwlink/?LinkId=316370) .

    Ces informations s’appliquent également aux clusters d’équilibrage de charge réseau IIS (NLB) dans Windows Server 2008, Windows Server2008R2 ou Windows Server2012.

    **Remarques**  La fonctionnalité d’équilibrage de charge réseau IIS dans Windows Server2012 est généralement la même que dans Windows Server2008R2. Toutefois, certains détails de la tâche sont modifiés dans Windows Server2012. Pour plus d’informations sur les nouvelles manières de procéder, voir [tâches de gestion courantes et navigation dans Windows server 2012 R2 Preview et Windows server 2012](https://go.microsoft.com/fwlink/?LinkId=316371) ( https://go.microsoft.com/fwlink/?LinkId=316371) .

     

## <a href="" id="bkmk-clusterscsmode"></a>Prise en charge des serveurs de fichiers en cluster lors de l’exécution du mode SCS


L’exécution de App-V 5,0 en mode de partage de contenu (SCS) avec des serveurs de fichiers groupés est prise en charge.

Les étapes suivantes peuvent être utilisées pour activer cette configuration:

-   Configurez App-V 5,0 pour qu’il s’exécute en mode SCS du client. Pour plus d’informations sur la configuration du mode SCS App-V 5,0, voir [Comment installer le client App-v 5,0 pour le mode magasin de contenu partagé](how-to-install-the-app-v-50-client-for-shared-content-store-mode.md).

-   Configurez le cluster de serveurs de fichiers configuré à la fois dans le mode de mise à l’échelle Microsoft Server2012 et le mode pre **2012** avec un réseau San virtuel.

Les étapes suivantes peuvent être utilisées pour valider la configuration:

1.  Ajoutez un package sur le serveur de publication. Pour plus d’informations sur l’ajout d’un package, voir [comment ajouter ou mettre à niveau des packages à l’aide de la console de gestion](how-to-add-or-upgrade-packages-by-using-the-management-console-beta-gb18030.md).

2.  Effectuez une actualisation de publication sur l’ordinateur exécutant le client App-V 5,0 et ouvrez une application.

3.  Basculer entre les nœuds de cluster pour la publication et l’actualisation des flux de travail pour garantir le fonctionnement correct du basculement.

Pour plus d’informations sur la configuration des clusters de basculement de Windows Server, voir les rubriques suivantes:

-   [Liste de contrôle: créer un serveur de fichiers groupés](https://go.microsoft.com/fwlink/?LinkId=316372) ( https://go.microsoft.com/fwlink/?LinkId=316372) .

-   [Utiliser des volumes partagés de cluster dans un cluster de basculement Windows Server 2012](https://go.microsoft.com/fwlink/?LinkId=316373) ( https://go.microsoft.com/fwlink/?LinkId=316373) .

## <a href="" id="bkmk-sqlmirroring"></a>Prise en charge de la mise en miroir Microsoft SQL Server


À l’aide de la mise en miroir de Microsoft SQL Server, où la base de données App-V 5,0 Management Server est mise en miroir à l’aide de deux instances SQL Server, les bases de données du serveur de gestion des applications-V 5,0 sont prises en charge.

Pour plus d’informations sur la configuration de la mise en miroir de Microsoft SQL Server, voir les rubriques suivantes:

-   [Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=316375) (https://go.microsoft.com/fwlink/?LinkId=316375)

-   [Établir une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=316377) (https://go.microsoft.com/fwlink/?LinkId=316377)

Les étapes suivantes peuvent être utilisées pour valider la configuration:

1.  Lancez une session de mise en miroir Microsoft SQL Server.

2.  Sélectionnez **basculement** pour désigner une nouvelle instance principale de Microsoft SQL Server.

3.  Vérifiez que le serveur de gestion App-V 5,0 continue de fonctionner comme prévu après le basculement.

Vous pouvez modifier la chaîne de connexion sur le serveur de gestion pour inclure le **partenaire de basculement = &lt; Server2 &gt; **. Cette option n’est utile que lorsque le principal sur le miroir a basculé sur le secondaire et que l’ordinateur exécutant le client App-V 5,0 effectue une nouvelle connexion (par exemple, après un redémarrage).

Procédez comme suit pour modifier la chaîne de connexion afin d’inclure le **partenaire de basculement = &lt; Server2 &gt; **:

**Important**  Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.

 

1.  Connectez-vous au serveur de gestion et ouvrez **regedit**.

2.  Accédez à **HKEY \ _LOCAL \ _MACHINE**  \\  **logiciel**  \\  **Microsoft**  \\  **AppV**  \\  **Server**  \\  **ManagementService**.

3.  Modifiez la valeur **gestion \ _SQL \ _CONNECTION \ _STRING** par le **partenaire de basculement = &lt; Server2 &gt; **.

4.  Redémarrez le service de gestion à l’aide de la console IIS.

    **Remarques**  La mise en miroir de la base de données se trouve sur la liste des fonctionnalités du moteur de base de données déconseillé pour Microsoft SQL Server2012 en raison de la fonctionnalité **AlwaysOn** disponible dans Microsoft sql Server 2012.

     

Pour plus d’informations, cliquez sur l’un des liens suivants:

-   [Procédure: préparation d’une base de données miroir pour la mise en miroir (Transact-SQL)](https://go.microsoft.com/fwlink/?LinkId=394235) ( https://go.microsoft.com/fwlink/?LinkId=394235) .

-   [Procédure: configurer une session de mise en miroir de base de données (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394236) ( https://go.microsoft.com/fwlink/?LinkId=394236) .

-   [Etablissez une session de mise en miroir de la base de données à l’aide de l’authentification Windows (SQL Server Management Studio)](https://go.microsoft.com/fwlink/?LinkId=394237) ( https://go.microsoft.com/fwlink/?LinkId=394237) .

-   [Fonctionnalités du moteur de base de données déconseillées dans SQL Server 2012](https://go.microsoft.com/fwlink/?LinkId=394238) ( https://go.microsoft.com/fwlink/?LinkId=394238) .

## <a href="" id="bkmk-sqlalwayson"></a>Prise en charge de Microsoft SQL Server toujours sur la configuration


La base de données du serveur de gestion de l’application-V 5,0 prend en charge les déploiements sur des ordinateurs exécutant Microsoft SQL Server avec la configuration **toujours active** .

## Rubriques connexes


[Envisager de déployer App-V](planning-to-deploy-app-v.md)

 

 





