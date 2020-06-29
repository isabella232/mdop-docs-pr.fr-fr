---
title: Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V
description: Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V
author: dansimp
ms.assetid: 6d069eb5-109f-460a-836a-de49473b7035
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: fb572442cd12bb32fc9406de65f05a3bf061f946
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807305"
---
# Procédure pour configurer la prise en charge de la mise en miroir de Microsoft SQL Server pour App-V


Vous pouvez utiliser la procédure suivante pour configurer votre environnement Microsoft Application Virtualization (App-V) pour utiliser la mise en miroir de base de données Microsoft SQL Server. La configuration de la mise en miroir de la base de données peut être utile pour les scénarios de reprise après sinistre et de reprise. App-V 4,5 SP2 prend en charge tous les modes de mise en miroir de la base de données actuellement disponibles pour Microsoft SQL Server 2005 et SQL Server 2008.

**Remarque**  
Cette procédure est écrite pour les administrateurs habitués à configurer et à configurer les bases de données SQL Server et la mise en miroir de la base de données à l’aide de Microsoft SQL Server.



**Pour configurer votre environnement App-V de façon à utiliser la mise en miroir de la base de données Microsoft SQL Server**

1.  Configurez la mise en miroir de la base de données SQL Server de la base de données App-V en suivant les recommandations standard pour la mise en miroir de la base de données. Pour obtenir des informations générales sur l’implémentation de la mise en miroir de la base de données Microsoft SQL Server, utilisez les liens suivants:

    -   **Microsoft SQL 2005**:[configuration de la mise en miroir de base de données](https://go.microsoft.com/fwlink/?LinkId=187478) (https://go.microsoft.com/fwlink/?LinkId=187478)

    -   **Microsoft SQL 2008**:[configuration de la mise en miroir de base de données](https://go.microsoft.com/fwlink/?LinkId=187477) (https://go.microsoft.com/fwlink/?LinkId=187477)

    De plus, vous pouvez trouver des informations pratiques recommandées en [matière de meilleures pratiques en matière de mise en miroir de la base de données](https://go.microsoft.com/fwlink/?LinkId=190270) ( https://go.microsoft.com/fwlink/?LinkId=190270) .

2.  Une fois la mise en miroir configurée, vérifiez que la base de données App-V affiche un état **(principal, synchronisé)** et que la base de données en miroir affiche un état **(miroir, synchronisé/restauré)**. Résoudre les problèmes de mise en miroir avant de passer à l’étape suivante. Pour plus d’informations sur la surveillance de l’État, voir [surveiller l’état de mise en miroir](https://go.microsoft.com/fwlink/?LinkId=190279) ( https://go.microsoft.com/fwlink/?LinkId=190279) .

3.  Sur l’ordinateur SQL Server qui héberge le miroir de la base de données App-v, créez le nom de connexion SQL Server pour le compte de service réseau du serveur de gestion des applications-v en utilisant le nom de compte ** &lt; Domain &gt; \\ &lt; ManagementServerHostName &gt; $ **.

4.  Installez le client natif Microsoft SQL Server sur le serveur de gestion App-V, puis sur l’ordinateur exécutant le service Web de gestion des applications-V s’il est installé sur un autre ordinateur. Si vous envisagez de faire en sorte que des serveurs d’administration d’applications supplémentaires se connectent à la base de données SQL en miroir pour l’équilibrage de charge, vous devez installer le client natif Microsoft SQL Server sur ces ordinateurs. Vous pouvez télécharger le client natif Microsoft SQL Server à partir de la page [Microsoft SQL server 2008 Feature Pack](https://go.microsoft.com/fwlink/?LinkId=187479) du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=187479) .

5.  Vérifiez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlservername** et assurez-vous qu’elle contient uniquement le nom d’hôte du serveur SQL Server. S’il inclut un nom d’instance (par exemple, *serverhostname\\instancename*), le nom de l’instance doit être supprimé.

    **Important**  
    Le serveur de gestion App-V utilise la bibliothèque de réseau TCP/IP pour communiquer avec le serveur SQL lorsque la mise en miroir de la base de données est activée, et par conséquent, les noms d’instances ne peuvent pas être utilisés. Les numéros de port doivent être spécifiés dans les clés de Registre à la place.



6.  Vérifiez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlserverport** et assurez-vous qu’elle contient le numéro de port utilisé pour SQL sur l’ordinateur SQL Server. Si vous utilisez une instance nommée, cette valeur de clé doit être définie sur le port utilisé pour l’instance nommée.

7.  Créez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverservername** en tant que REG \ _SZ puis définissez la valeur sur le nom d’hôte de SQL Server qui héberge le miroir.

8.  Créez la clé de Registre **HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\server\\sqlfailoverserverport** en tant que DWORD, puis définissez la valeur sur le numéro de port utilisé pour SQL sur l’ordinateur exécutant SQL Server pour héberger le miroir. Si vous utilisez une instance nommée pour le miroir, la valeur de cette clé doit être définie sur le numéro de port utilisé pour l’instance nommée.

9.  Sur l’ordinateur exécutant le service Web d’administration des applications-V, configurez le fichier texte UDL (Universal Data Link). Dans le répertoire d’installation de l’application-V, double-cliquez sur **SftMgmt. UDL** et spécifiez les valeurs suivantes:

    -   Dans l’onglet **fournisseur** , sélectionnez le fournisseur OLE DB fournisseur **SQL Server Native Client 10,0**.

    -   Cliquez sur **suivant** pour sélectionner l’onglet **connexion** . Dans la zone **nom du serveur** , entrez le nom du serveur SQL Server. Ensuite, activez la case à cocher **utiliser la sécurité intégrée à Windows NT**. Pour finir, cliquez sur la liste, **Sélectionnez la base de données**, puis sélectionnez le nom de la base de données App-V.

    -   Cliquez sur l’onglet **toutes** , puis sélectionnez le **partenaire entrée Failover**. Cliquez sur **modifier la valeur**, puis entrez le nom de serveur du serveur SQL de basculement. Cliquez sur **OK**.

    **Important**  
    Le système App-V utilise l’authentification Kerberos. Par conséquent, lorsque vous configurez la mise en miroir SQL où l’authentification Kerberos est activée sur le serveur SQL Server et que le service SQL Server s’exécute sous un compte d’utilisateur de domaine, vous devez configurer manuellement un SPN. Pour plus d’informations, consultez la section «lorsque le service SQL utilise un compte basé sur le domaine» dans l’article [configuration de l’administration d’App-V pour un environnement distribué](https://go.microsoft.com/fwlink/?LinkId=203186) ( https://go.microsoft.com/fwlink/?LinkId=203186) .



10. Pour vérifier que la mise en miroir de la base de données fonctionne correctement, testez le basculement et confirmez que le serveur de gestion de l’application-V continue de fonctionner correctement.

    **Important**  
    Procédez comme suit, puis suivez les recommandations standard de votre entreprise pour vous assurer que les opérations système ne sont pas interrompues en cas de panne.



~~~
After the failover has occurred successfully, as verified by using the SQL Server status monitoring information, right-click the **Applications** node in the App-V Management Console, and then select **Refresh**. The list of applications should display normally if the system is working correctly.
~~~

## Rubriques connexes


[Procédure pour effectuer des tâches d'administration dans Application Virtualization Server Management Console](how-to-perform-administrative-tasks-in-the-application-virtualization-server-management-console.md)









