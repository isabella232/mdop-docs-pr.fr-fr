---
title: Générer des rapports MBAM
description: Générer des rapports MBAM
author: dansimp
ms.assetid: 083550cb-8c3f-49b3-a30e-97d85374d2f4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: ccdc1a2cd69d8cc2e2c2823827f5ea43ad867a78
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810349"
---
# Générer des rapports MBAM


Lorsque vous installez Microsoft BitLocker administration et surveillance (MBAM) avec la topologie autonome, vous pouvez générer différents rapports pour contrôler l’utilisation et la conformité du chiffrement BitLocker. Les procédures décrites dans cette rubrique expliquent comment ouvrir le site Web d’administration et de contrôle, ainsi que les étapes nécessaires pour générer des rapports d’administration et de surveillance de BitLocker sur le respect de l’entreprise, sur les ordinateurs individuels et sur l’activité de récupération des clés. Pour plus d’informations sur les rapports MBAM, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).

**Remarques**  Pour exécuter les rapports, vous devez être membre du rôle de l' **utilisateur du rapport** sur les ordinateurs sur lesquels sont installés les rapports d’administration et de surveillance des fonctionnalités du serveur, de la conformité et de l’audit.

 

**Pour ouvrir le site Web d’administration et de surveillance**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance. L’URL par défaut du site Web d’administration et de surveillance est *http:// &lt; nomordinateur &gt; *.

    **Remarques**  Si theAdministration et le site Web de surveillance ont été installés sur un autre port que 80, vous devez spécifier le port dans l’URL (par exemple, *http:// &lt; nomordinateur &gt; : &lt; port &gt; *). Si vous avez spécifié un nom d’hôte pour theAdministration et qu’il est en cours d’installation, l’URL est *http:// &lt; hostname &gt; *.

     

2.  Dans le volet gauche, cliquez sur **rapports** , puis sélectionnez le rapport que vous souhaitez exécuter dans la barre de menus supérieure.

    Les données du client MBAM historique sont conservées dans la base de données de conformité pour référence historique en cas de perte ou de vol d’un ordinateur. Lors de l’exécution de rapports d’entreprise, nous vous recommandons d’utiliser les dates de début et de fin appropriées pour limiter les délais des rapports de une à deux semaines afin d’améliorer la précision des données de rapport.

    **Remarques**  Si SSRS n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM. Si vous accédez au portail du support technique et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché». Pour afficher l’État, cliquez sur **Afficher tout le contenu**.

     

**Pour générer un rapport de conformité d’entreprise**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud **rapports** dans le volet de navigation gauche, sélectionnez **rapport de conformité d’entreprise**, puis les filtres que vous souhaitez utiliser. Les filtres disponibles pour le rapport de conformité d’entreprise sont les suivants:

    -   **État de la conformité**. Utilisez ce filtre pour spécifier les types d’état de conformité (par exemple, conforme ou non conforme) du rapport.

    -   **État d’erreur**. Utilisez ce filtre pour spécifier les types d’état d’erreur (par exemple, aucune erreur ou erreur) du rapport.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport sélectionné.

    Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.

    **Remarques**  Le rapport de conformité d’entreprise est généré par un travail SQL qui s’exécute toutes les six heures. Par conséquent, lorsque vous affichez le rapport pour la première fois, il est possible que certaines données soient manquantes. Vous pouvez générer manuellement des données de rapport mises à jour à l’aide de SQL Management Studio. Dans la fenêtre **Explorateur d’objets** , développez l' **agent SQL Server**, développez **travaux**, cliquez avec le bouton droit sur le travail **CreateCache** , puis sélectionnez **Démarrer la tâche à l’étape....**

     

3.  Sélectionnez le nom d’un ordinateur pour afficher des informations relatives à l’ordinateur figurant dans le rapport de compatibilité de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

**Pour générer le rapport de conformité de l’ordinateur**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis sélectionnez le **rapport de conformité**de l’ordinateur. Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport sur l’ordinateur.

    Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.

3.  Sélectionnez le nom d’un ordinateur pour afficher des informations supplémentaires sur celui-ci dans le rapport de compatibilité de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

    **Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond aux exigences des paramètres de stratégie MBAM.

     

**Pour générer le rapport d’audit de clé de récupération**

1.  Sur le site Web d’administration et de surveillance, sélectionnez le nœud de **rapport** dans le volet de navigation gauche, puis sélectionnez le **rapport d’audit de récupération**. Sélectionnez les filtres du rapport d’audit de la clé de récupération. Les filtres disponibles pour les audits de clé de récupération sont les suivants:

    -   **Demandeur**. Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur du demandeur. Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur.

    -   **Demandeur**. Ce filtre permet aux utilisateurs de spécifier le nom d’utilisateur de la requête. La personne qui a appelé le support technique peut obtenir une clé de récupération.

    -   **Résultat**de la requête. Ce filtre permet aux utilisateurs de spécifier les types de résultats de requête (par exemple, succès ou échec) sur lesquels ils veulent baser le rapport. Par exemple, les utilisateurs peuvent souhaiter afficher les tentatives d’accès par clé en échec.

    -   **Type de clé**. Ce filtre permet aux utilisateurs de spécifier le type de clé (par exemple: mot de passe pour la clé de récupération ou hachage du mot de passe TPM) sur lequel il souhaite baser le rapport.

    -   **Date de début**. Ce filtre permet de définir la partie Date de début de la plage de dates à laquelle l’utilisateur souhaite rapporter.

    -   **Date de fin**. Ce filtre est utilisé pour définir la partie de la date de fin de la plage de dates à laquelle les utilisateurs veulent rapporter.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport.

    Les résultats peuvent être enregistrés dans différents formats, tels que HTML, Microsoft Word et Microsoft Excel.

## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM2.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-20-mbam-2.md)

 

 





