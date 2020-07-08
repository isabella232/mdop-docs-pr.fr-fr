---
title: Utilisation du portail de support technique
description: Utilisation du portail de support technique
author: dansimp
ms.assetid: c27f7737-10c8-4164-9de8-57987292c89c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa8813fbe9a7b6980b656ecc673ac4ed618c4cf7
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811688"
---
# Utilisation du portail de support technique


Le site Web d’administration et de surveillance de MBAM, également appelé portail d’assistance technique, est une interface d’administration de BitLocker Drive Encryption qui est installée dans le cadre de l’infrastructure du serveur Microsoft BitLocker (MBAM). Les sections suivantes décrivent comment vous pouvez utiliser ce site Web pour passer en revue des rapports, récupérer les lecteurs des utilisateurs finaux et gérer les utilisateurs TPMs.

## <a href="" id="bkmk-reports"></a>Rapports


MBAM collecte des informations à partir d’Active Directory et d’ordinateurs clients, ce qui vous permet d’exécuter différents rapports pour contrôler l’utilisation et la conformité de BitLocker. À l’aide de la section **rapports** du site Web d’administration et de surveillance, vous pouvez générer des rapports sur les activités de conformité d’entreprise, d’ordinateur individuel et de récupération de clés. Pour obtenir une description de chaque rapport, voir [Présentation des rapports MBAM](understanding-mbam-reports-mbam-2.md).

**Pour accéder aux rapports**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de contrôle MBAM.

2.  Dans le volet gauche, sélectionnez **rapports** .

3.  Dans la barre de menus supérieure, sélectionnez le type de rapport que vous souhaitez générer. Pour enregistrer des rapports, cliquez sur le bouton **Exporter** dans la barre de menus rapports.

Pour plus d’informations sur l’exécution des rapports MBAM, voir [génération de rapports MBAM](how-to-generate-mbam-reports-mbam-2.md).

## <a href="" id="bkmk-drirec"></a>Récupération des lecteurs


La fonctionnalité de **récupération de lecteur** du site Web d’administration et de contrôle permet aux utilisateurs ayant des rôles d’administrateur spécifiques (par exemple, les utilisateurs du support technique) d’accéder aux données de clé de récupération collectées par le client MBAM. Ces données peuvent être utilisées pour accéder à un lecteur protégé par BitLocker lorsque BitLocker passe en mode de récupération. Pour obtenir des instructions sur la façon de récupérer un lecteur qui est en mode récupération, voir [Comment récupérer un lecteur en mode récupération](how-to-recover-a-drive-in-recovery-mode-mbam-2.md).

Vous pouvez également récupérer des lecteurs qui ont été déplacés ou qui sont endommagés:

-   [Récupération d'un lecteur déplacé](how-to-recover-a-moved-drive-mbam-2.md)

-   [Récupération d'un lecteur endommagé](how-to-recover-a-corrupted-drive-mbam-2.md)

Pour plus d’informations sur la façon de récupérer un lecteur protégé par BitLocker, voir exécution de la [gestion BitLocker avec mbam](performing-bitlocker-management-with-mbam-mbam-2.md).

## <a href="" id="bkmk-manatpm"></a>Gérer le TPM


La fonction de gestion des PUCEs du site Web d’administration et de contrôle donne aux utilisateurs de certains rôles d’administrateur (par exemple, «utilisateurs du support technique MBAM») l’accès aux données du TPM collectées par le client MBAM. Dans le cas d’un verrouillage de module de plateforme sécurisée, un administrateur peut utiliser le site Web d’administration et de surveillance pour récupérer le fichier de mot de passe nécessaire pour déverrouiller le TPM. Pour obtenir des instructions sur la réinitialisation d’un TPM après le verrouillage du TPM, voir [Comment réinitialiser un verrouillage du TPM](how-to-reset-a-tpm-lockout-mbam-2.md).

## <a href="" id="bkmk-helpdesk"></a> Tâches du support technique MBAM


Vous pouvez utiliser le site Web d’administration et de contrôle pour de nombreuses tâches d’administration, telles que la gestion du matériel protégé par BitLocker, la récupération de lecteurs et l’exécution de rapports. Par défaut, l’URL du site Web d’administration et de surveillance est http:// &lt; *MBAMAdministrationServername* &gt; , même si vous pouvez le personnaliser pendant le processus d’installation.

**Remarques**  Pour accéder aux diverses fonctionnalités proposées par le site Web d’administration et de surveillance, vous devez disposer des rôles appropriés associés à votre compte d’utilisateur. Pour plus d’informations sur la compréhension des rôles d’utilisateur, voir [Comment gérer les rôles d’administrateur de MBAM](how-to-manage-mbam-administrator-roles-mbam-2.md).

 

Pour trouver des informations sur les tâches que vous pouvez effectuer à l’aide du site Web d’administration et de contrôle, utilisez les liens suivants:

-   [Réinitialisation d'un verrouillage TPM](how-to-reset-a-tpm-lockout-mbam-2.md)

-   [Procédure de récupération d'un lecteur en mode de récupération](how-to-recover-a-drive-in-recovery-mode-mbam-2.md)

-   [Récupération d'un lecteur déplacé](how-to-recover-a-moved-drive-mbam-2.md)

-   [Récupération d'un lecteur endommagé](how-to-recover-a-corrupted-drive-mbam-2.md)

-   [Détermination de l'état de chiffrement BitLocker des ordinateurs perdus](how-to-determine-bitlocker-encryption-state-of-lost-computers-mbam-2.md)

 

 





