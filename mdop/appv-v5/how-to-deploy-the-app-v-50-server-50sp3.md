---
title: Comment déployer le serveur App-V5.0
description: Comment déployer le serveur App-V5.0
author: dansimp
ms.assetid: 4f8f16af-7d74-42b4-84b8-b04ce668225d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b94bab16349751aacf0aca0f8c2e5ac5a6ae6da7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805532"
---
# Comment déployer le serveur App-V5.0


Utilisez la procédure suivante pour installer le serveur App-V 5,0. Pour plus d’informations sur le déploiement du serveur App-V 5,0 SP3, voir [à propos de App-v 5,0 SP3](about-app-v-50-sp3.md#bkmk-migrate-to-50sp3).

**Avant de commencer:**

-   Vérifiez que vous avez installé les logiciels requis. Voir la [Configuration requise pour App-V 5,0](app-v-50-prerequisites.md).

-   Passez en revue la section serveur de [considérations relatives à la sécurité dans App-V 5,0](app-v-50-security-considerations.md).

-   Spécifiez un port sur lequel chaque composant sera hébergé.

-   Ajoutez des règles de pare-feu pour permettre aux demandes entrantes d’accéder aux ports spécifiés.

-   Si vous utilisez des scripts SQL, au lieu du programme d’installation Windows, pour configurer la base de données de gestion ou la base de données de création de rapports, vous devez exécuter les scripts SQL avant d’installer le serveur de gestion ou le serveur de rapports. Découvrez [comment déployer les bases de données App-V à l’aide de scripts SQL](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md).

**Pour installer le serveur App-V 5,0**

1. Copiez les fichiers d’installation de App-V 5,0 Server sur l’ordinateur sur lequel vous voulez l’installer.

2. Démarrez l’installation de l’App-V 5,0 Server en cliquant avec le bouton droit sur le **appv\_server\_setup.exe** en tant qu’administrateur, puis cliquez sur **installer**.

3. Passez en revue et acceptez les termes du contrat de licence, puis indiquez si vous souhaitez activer les mises à jour Microsoft.

4. Dans la page de **sélection des fonctionnalités** , sélectionnez tous les composants suivants.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Composant</th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Serveur de gestion</p></td>
   <td align="left"><p>Fournit les fonctionnalités de gestion globales de l’infrastructure App-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Base de données de gestion</p></td>
   <td align="left"><p>Facilite le déploiement de la base de données pour la gestion d’App-V.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Serveur de publication</p></td>
   <td align="left"><p>Fournit des fonctionnalités d’hébergement et de streaming pour les applications virtuelles.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Serveur de création de rapports</p></td>
   <td align="left"><p>Fournit App-V 5,0 Reporting Services.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>Base de données de création de rapports</p></td>
   <td align="left"><p>Facilite le déploiement de la base de données pour la création de rapports App-V.</p></td>
   </tr>
   </tbody>
   </table>

     

5. Dans la page emplacement de l' **installation** , acceptez l’emplacement par défaut où les composants sélectionnés seront installés ou modifiez l’emplacement en entrant un nouveau chemin dans la ligne emplacement de l' **installation** .

6. Dans la page de **création de base de données de gestion** initiale, configurez la **base de données** **Microsoft SQL Server instance** and Management Server en sélectionnant l’option appropriée ci-dessous.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Méthode</th>
   <th align="left">Ce que vous devez faire</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Vous utilisez une instance de Microsoft SQL Server personnalisée.</p></td>
   <td align="left"><p>Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</p>
   <p>Utilisez la mise en forme <strong> InstanceName </strong> . L’emplacement d’installation supposé est l’ordinateur local.</p>
   <p>Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Vous utilisez un nom de base de données personnalisé.</p></td>
   <td align="left"><p>Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</p>
   <p>Le nom de la base de données doit être unique ou l’installation échoue.</p></td>
   </tr>
   </tbody>
   </table>

     

7. Dans la page **configurer** , acceptez la valeur par défaut **utiliser cet ordinateur local**.

   **Remarque**  
   Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles. Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.

     

8. Dans la page de **création de base de données initiale de création de rapports** , configurez l' **instance SQL Server** et la **base de données du serveur** de création de rapports en sélectionnant l’option appropriée ci-dessous.

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Méthode</th>
   <th align="left">Ce que vous devez faire</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Vous utilisez une instance de Microsoft SQL Server personnalisée.</p></td>
   <td align="left"><p>Sélectionnez <strong> utiliser l’instance personnalisée </strong> , puis tapez le nom de l’instance.</p>
   <p>Utilisez la mise en forme <strong> InstanceName </strong> . L’emplacement d’installation supposé est l’ordinateur local.</p>
   <p>Non pris en charge: nom du serveur utilisant l’instance de nom de serveur <strong> ServerName </strong> &lt; &gt; </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>Vous utilisez un nom de base de données personnalisé.</p></td>
   <td align="left"><p>Sélectionnez <strong> configuration personnalisée </strong> et tapez le nom de la base de données.</p>
   <p>Le nom de la base de données doit être unique ou l’installation échoue.</p></td>
   </tr>
   </tbody>
   </table>

     

9. Dans la page **configurer** , acceptez la valeur par défaut: **Utilisez cet ordinateur local**.

   **Remarque**  
   Si vous installez le serveur de gestion et la base de données de gestion côte à côte, certaines options de cette page ne sont pas disponibles. Dans ce cas, les options appropriées sont sélectionnées par défaut et ne peuvent pas être modifiées.

     

10. Sur la page **configurer** (configuration du serveur de gestion), spécifiez les éléments suivants:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Élément à configurer</th>
    <th align="left">Description et exemples</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Entrez le groupe d’annonces disposant des autorisations nécessaires pour gérer l’environnement App-V.</p></td>
    <td align="left"><p>Par exemple: MyDomain\MyUser</p>
    <p>Après l’installation, vous pouvez ajouter des utilisateurs ou des groupes supplémentaires à l’aide de la console de gestion. Toutefois, les groupes de distribution globale et les groupes de distribution AD DS (Active Directory Domain Services) ne sont pas pris en charge. <strong> </strong> <strong> </strong> Pour effectuer cette action, vous devez utiliser les groupes locaux de domaine ou universels.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</p></td>
    <td align="left"><p>Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</p></td>
    <td align="left"><p>Par exemple: <strong> 12345</strong></p>
    <p>Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</p></td>
    </tr>
    </tbody>
    </table>

     

11. Dans la **page Configuration du** **serveur de publication** , spécifiez les éléments suivants:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Élément à configurer</th>
    <th align="left">Description et exemples</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Spécifiez l’URL du service de gestion.</p></td>
    <td align="left"><p>Example<a href="http://localhost:12345" data-raw-source="http://localhost:12345">http://localhost:12345</a></p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de publication.</p></td>
    <td align="left"><p>Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</p></td>
    <td align="left"><p>Par exemple: 54321</p>
    <p>Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</p></td>
    </tr>
    </tbody>
    </table>

     

12. Dans la page **Report Server** , spécifiez les éléments suivants:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Élément à configurer</th>
    <th align="left">Description et exemples</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Nom du site Web </strong> : spécifiez le nom personnalisé qui sera utilisé pour exécuter le service de création de rapports.</p></td>
    <td align="left"><p>Si vous n’avez pas de nom personnalisé, n’apportez aucune modification.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Liaison de port </strong> : spécifiez un numéro de port unique qui sera utilisé par App-V.</p></td>
    <td align="left"><p>Par exemple: 55555</p>
    <p>Vérifiez que le port spécifié n’est pas utilisé par un autre site Web.</p></td>
    </tr>
    </tbody>
    </table>

     

13. Pour démarrer l’installation, cliquez sur **installer** dans la page **prêt** , puis cliquez sur **Fermer** dans la page **terminé** .

14. Pour vérifier que la configuration s’est déroulée correctement, ouvrez un navigateur Web, puis tapez l’URL suivante:

    **http:// &lt; Nom de l’ordinateur du serveur de gestion &gt; : &lt; numéro de port du service de gestion &gt; /Console.html**.

    Par exemple: **http://localhost:12345/console.html** . Si l’installation a réussi, la console de gestion App-V est affichée sans erreur.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Déploiement d'App-V5.0](deploying-app-v-50.md)

[Comment installer les bases de données de gestion et de rapports sur des ordinateurs distincts des services de gestion et de rapports](how-to-install-the-management-and-reporting-databases-on-separate-computers-from-the-management-and-reporting-services.md)

[Comment installer le serveur de publication sur un ordinateur distant](how-to-install-the-publishing-server-on-a-remote-computer.md)

[Déploiement du serveur App-V5.0 à l'aide d'un script](how-to-deploy-the-app-v-50-server-using-a-script.md)

[Activation de la création de rapports sur App-V5.0 Client à l'aide de PowerShell](how-to-enable-reporting-on-the-app-v-50-client-by-using-powershell.md)

 

 





