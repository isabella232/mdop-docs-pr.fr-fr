---
title: Générer des rapports MBAM
description: Générer des rapports MBAM
author: dansimp
ms.assetid: cdf4ae76-040c-447c-8736-c9e57068d221
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 7f0b5a4e984d7a609eab7204e67f46042992f586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810608"
---
# Générer des rapports MBAM


Microsoft BitLocker administration et surveillance (MBAM) génère divers rapports pour contrôler l’utilisation et la conformité du chiffrement BitLocker. Cette rubrique décrit comment ouvrir le site Web d’administration MBAM et générer des rapports MBAM sur le respect de la conformité d’entreprise, des ordinateurs individuels, de la compatibilité matérielle et de la récupération de clés. Pour plus d’informations sur les rapports MBAM, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-1.md).

**Remarques**  Pour exécuter les rapports, vous devez être membre du rôle **utilisateurs du rapport** sur les ordinateurs sur lesquels vous avez installé les fonctionnalités d’administration et de surveillance de la base de données de serveur d’administration et de conformité, ainsi que des rapports de conformité et d’audit.

 

**Pour ouvrir le site Web d’administration MBAM**

1.  Ouvrez un navigateur Web, puis accédez au site Web MBAM. L’URL par défaut du site Web *est &lt; http:// &gt; nomordinateur* du serveur d’administration et de contrôle Microsoft BitLocker.

    **Remarques**  Si le site Web MBAMadministration a été installé sur un autre port que le port 80, vous devez spécifier ce numéro de port dans l’URL. Par exemple, *http:// &lt; nomordinateur &gt; : &lt; port &gt; *. Si vous spécifiez un nom d’hôte pour le site Web MBAMadministration lors de l’installation, l’URL serait *http:// &lt; hostname &gt; *.

     

2.  Dans le volet de navigation, cliquez sur **rapports**. Dans le volet principal, cliquez sur l’onglet de votre type de rapport: **rapport de conformité d’entreprise**, rapport de conformité des **ordinateurs**, rapport **d’audit matériel**ou **rapport d’audit de récupération**.

    **Remarques**  Les données du client MBAM historique sont conservées dans la base de données de conformité. Ce risque de perte de données peut être requis en cas de perte ou de vol d’un ordinateur. Lors de l’exécution de rapports d’entreprise, vous devez utiliser les dates de début et de fin appropriées pour limiter les délais pour les rapports de une à deux semaines afin d’améliorer la précision des données de rapport.

     

**Pour générer un rapport de conformité d’entreprise**

1.  Sur le site Web MBAMadministration, cliquez sur **rapports** dans le volet de navigation, puis cliquez sur l’onglet **rapport de conformité d’entreprise** et sélectionnez les filtres appropriés pour votre rapport. Pour le rapport de conformité d’entreprise, vous pouvez définir les filtres suivants.

    -   **État de la conformité**. Utilisez ce filtre pour spécifier les types d’état de conformité (par exemple, conforme ou non conforme) à inclure dans le rapport.

    -   **État d’erreur**. Utilisez ce filtre pour spécifier les types d’état d’erreur (par exemple, aucune erreur ou erreur) à inclure dans le rapport.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport spécifié.

    Les résultats du rapport peuvent être enregistrés dans l’un des nombreux formats de fichier disponibles (par exemple, HTML, Microsoft Word et Microsoft Excel).

    **Remarques**  Le rapport de conformité d’entreprise est généré par un travail SQL qui s’exécute toutes les six heures. Dès lors que vous essayez d’afficher le rapport pour la première fois, il est possible que certaines données soient manquantes.

     

3.  Pour afficher des informations sur un ordinateur figurant dans le rapport de conformité informatique, sélectionnez le nom de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

**Pour générer le rapport de conformité de l’ordinateur**

1.  Sur le site Web MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport de conformité**de l’ordinateur. Utilisez le rapport de conformité de l’ordinateur pour rechercher le **nom d’utilisateur** ou le nom de l' **ordinateur**.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport sur l’ordinateur.

    Les résultats peuvent être enregistrés dans l’un des formats de fichier disponibles (par exemple, HTML, Microsoft Word et Microsoft Excel).

3.  Pour afficher des informations supplémentaires sur un ordinateur dans le rapport de conformité informatique, sélectionnez le nom de l’ordinateur.

4.  Sélectionnez le signe plus (+) en regard du nom de l’ordinateur pour afficher des informations sur les volumes présents sur l’ordinateur.

    **Remarques**  Un ordinateur client MBAM est considéré comme conforme si l’ordinateur répond aux exigences des paramètres de stratégie MBAM ou si le modèle matériel de l’ordinateur est défini sur incompatible. Par conséquent, lorsque vous affichez des informations détaillées sur les volumes de disque associés à l’ordinateur, les ordinateurs exemptés du chiffrement BitLocker en raison de la compatibilité matérielle peuvent être affichés comme conformes, même si leur état de chiffrement de volume est affiché comme non conforme.

     

**Pour générer le rapport d’audit de compatibilité matérielle**

1.  Sur le site Web MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport de vérification matérielle**. Sélectionnez les filtres appropriés pour le rapport d’audit de votre matériel. Le rapport de vérification matérielle fournit les filtres suivants disponibles:

    -   **Utilisateur (Domain\\User)**. Spécifie le nom de l’utilisateur qui a apporté une modification.

    -   **Changer de type**. Spécifie le type de modification que vous recherchez.

    -   **Date de début**. Spécifie la partie Date de début de la plage de dates dans laquelle vous souhaitez créer un rapport.

    -   **Date de fin**. Spécifie la partie de la date de fin de la plage de dates dans laquelle vous souhaitez créer un rapport.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport.

    Vous pouvez enregistrer les résultats dans différents formats de fichier (par exemple, HTML, Microsoft Word et Microsoft Excel).

**Pour générer le rapport d’audit de clé de récupération**

1.  Sur le site Web de MBAMadministration, sélectionnez le nœud de **rapport** dans le volet de navigation, puis sélectionnez le **rapport d’audit de récupération**. Sélectionnez les filtres du rapport d’audit de la clé de récupération. Les filtres disponibles pour les audits de clé de récupération sont les suivants:

    -   **Demandeur**. Spécifie le nom d’utilisateur du demandeur. Le demandeur est la personne du support technique qui a accédé à la clé pour le compte d’un utilisateur.

    -   **Demandeur**. Spécifie le nom d’utilisateur de la requête. La personne qui a appelé le support technique peut obtenir une clé de récupération.

    -   **Résultat** de la requête Spécifie les types de résultats de la requête, tels que: réussite ou échec. Par exemple, il est possible que vous souhaitiez afficher les tentatives d’accès par clé en échec.

    -   **Type de clé**. Spécifie le type de clé, par exemple: mot de passe de clé de récupération ou hachage du mot de passe TPM.

    -   **Date de début**. Spécifie la date de début dans la plage de dates.

    -   **Date de fin**. Spécifie la partie de la date de fin de la plage de dates.

2.  Cliquez sur **afficher le rapport** pour afficher le rapport.

    Vous pouvez enregistrer les résultats dans différents formats de fichier (par exemple, HTML, Microsoft Word et Microsoft Excel).

## Rubriques connexes


[Surveillance et création de rapports de la conformité BitLocker avec MBAM1.0](monitoring-and-reporting-bitlocker-compliance-with-mbam-10.md)

 

 





