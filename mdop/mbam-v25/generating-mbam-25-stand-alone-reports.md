---
title: Génération des rapports MBAM2.5 autonomes
description: Génération des rapports MBAM2.5 autonomes
author: dansimp
ms.assetid: 0ec623ff-5155-4906-aef2-20cdc0f84667
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: e1c6b33de26cce5d9ad8d20461dbe0ea0f138c78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809767"
---
# Génération des rapports MBAM2.5 autonomes


Lorsque vous configurez l’administration et la surveillance de Microsoft BitLocker (MBAM) avec la topologie autonome, vous pouvez générer des rapports pour contrôler l’utilisation et la conformité du chiffrement de lecteur BitLocker. Cette rubrique contient les procédures suivantes:

-   [Pour ouvrir le site Web d’administration et de surveillance](#bkmk-openadmin)

-   [Pour générer un rapport de conformité d’entreprise](#bkmk-enterprise)

-   [Pour générer un rapport de conformité ordinateur](#bkmk-computercomp)

-   [Pour générer un rapport d’audit de clé de récupération](#bkmk-recoverykey)

Pour obtenir une description des rapports autonomes, voir [Présentation des rapports MBAM 2,5 autonomes](understanding-mbam-25-stand-alone-reports.md).

**Remarques**  Pour exécuter les rapports, vous devez être membre du groupe **MBAM des utilisateurs du rapport** , que vous configurez dans les services de domaine Active Directory (AD FS). Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

 

<a href="" id="bkmk-openadmin"></a>**Pour ouvrir le site Web d’administration et de surveillance**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance. L’URL par défaut du site Web d’administration et de surveillance est la suivante:

    *http (s):// &lt; MBAMAdministrationServerName &gt; : &lt; port &gt; /helpdesk*

2.  Dans le volet de gauche, cliquez sur **rapports**. Dans la barre de menus supérieure, sélectionnez le rapport que vous souhaitez exécuter.

    Les données du client MBAM sont conservées dans la base de données d’audit et de conformité pour référence historique en cas de perte ou de vol d’un ordinateur. Lors de l’exécution de rapports d’entreprise, nous vous recommandons d’utiliser les dates de début et de fin appropriées pour limiter les délais des rapports de une à deux semaines afin d’améliorer la précision des données de rapport.

    Après avoir généré un rapport, vous pouvez enregistrer les résultats dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.

    **Remarques**  Configurer SQL Server Reporting Services (SSRS) pour utiliser le protocole SSL (Secure Sockets Layer) avant de configurer le site Web d’administration et de surveillance. Si, pour une raison quelconque, SSRS n’est pas configuré pour utiliser SSL, l’URL des rapports sera définie sur HTTP au lieu de HTTPs lorsque vous configurez le site Web d’administration et de surveillance. Si vous accédez au site Web Administration et surveillance et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché». Pour afficher l’État, cliquez sur **Afficher tout le contenu**.

     

<a href="" id="bkmk-enterprise"></a>**Pour générer un rapport de conformité d’entreprise**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud **rapports** dans le volet de navigation gauche, sélectionnez **rapport de conformité d’entreprise**, puis les filtres que vous souhaitez utiliser. Les filtres disponibles pour le rapport de conformité d’entreprise sont les suivants:

    -   **État de la conformité**. Utilisez ce filtre pour spécifier les types d’état de conformité du rapport (par exemple, conforme ou non conforme).

    -   **État d’erreur**. Utilisez ce filtre pour spécifier les types d’état d’erreur du rapport (par exemple, aucune erreur ou erreur).

2.  Cliquez sur **afficher le rapport** pour afficher le rapport sélectionné.

3.  Sélectionnez le nom d’un ordinateur pour afficher des informations relatives à l’ordinateur figurant dans le rapport de compatibilité de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

<a href="" id="bkmk-computercomp"></a>**Pour générer un rapport de conformité ordinateur**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis cliquez sur **rapport de conformité d’ordinateur**. Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport de conformité de votre ordinateur.

3.  Sélectionnez le nom d’un ordinateur pour afficher des informations supplémentaires sur celui-ci dans le rapport de compatibilité de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

    **Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond à la configuration requise des paramètres de stratégie de groupe MBAM.

<a href="" id="bkmk-recoverykey"></a>**Pour générer un rapport d’audit de clé de récupération**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis cliquez sur **rapport d’audit de récupération**. Sélectionnez les filtres du rapport d’audit de la clé de récupération. Les filtres disponibles pour les audits de clé de récupération sont les suivants:

    -   **Utilisateur du support technique**. Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur du demandeur. Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur final.

    -   **Utilisateur final**. Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur de la requête. La demande est l’utilisateur final ayant appelé le support technique pour obtenir une clé de récupération.

    -   **Résultat**de la requête. Ce filtre permet aux utilisateurs de spécifier les types de résultats de requête (par exemple, succès ou échec) sur lesquels ils veulent baser le rapport. Par exemple, les utilisateurs peuvent souhaiter afficher les tentatives d’accès par clé en échec.

    -   **Type de clé**. Ce filtre permet aux utilisateurs de spécifier le type de clé (par exemple, un mot de passe pour la clé de récupération ou le hachage du mot de passe du TPM) sur lequel il souhaite baser le rapport.

    -   **Date de début**. Ce filtre permet de définir la partie Date de début de la plage de dates à laquelle l’utilisateur souhaite rapporter.

    -   **Date de fin**. Ce filtre est utilisé pour définir la partie de la date de fin de la plage de dates à laquelle les utilisateurs veulent rapporter.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport.



## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM2.5](monitoring-and-reporting-bitlocker-compliance-with-mbam-25.md)

[Présentation des rapports autonomes MBAM2.5](understanding-mbam-25-stand-alone-reports.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





