---
title: Configurer la sécurité de messagerie électronique pour AGPM
description: Configurer la sécurité de messagerie électronique pour AGPM
author: dansimp
ms.assetid: b9c48894-0a10-4d03-8027-50ed3b02485a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a384c2a21f912ca7ec55a5e4c74ca7062bfe864c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807729"
---
# Configurer la sécurité de messagerie électronique pour AGPM


Par défaut, les notifications par courrier électronique envoyées en raison d’actions dans la gestion de la stratégie de groupe avancée (AGPM) ne sont pas chiffrées et sont envoyées via le port SMTP 25. Toutefois, vous pouvez configurer la sécurité de messagerie pour AGPM en utilisant des paramètres de Registre pour spécifier l’utilisation du chiffrement SSL (Secure Sockets Layer) et le port SMTP à utiliser.

En chiffrant les notifications par courrier électronique AGPM, vous pouvez mieux protéger celles susceptibles de divulguer des informations sensibles sur la sécurité de votre organisation. Le chiffrement des notifications par courrier électronique est recommandé quand ils sont relayés par le biais de serveurs de messagerie distants, et peuvent être requis par certains règlements de conformité.

**Attention**  La modification incorrecte du registre pourrait endommager sérieusement votre système. Avant d’apporter des modifications au registre, il est recommandé de sauvegarder toutes les données importantes de votre ordinateur.

 

Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’Approbateur ayant créé l’objet de stratégie de groupe (GPO) utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans AGPM est requis pour effectuer ces procédures. Passez en revue les détails dans «autres considérations» dans cette rubrique.

**Pour configurer la sécurité de la messagerie électronique pour AGPM en utilisant les préférences de stratégie de groupe**

1.  Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet de stratégie de groupe qui s’applique à tous les serveurs AGPM pour lesquels vous souhaitez configurer la sécurité de messagerie électronique. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).

2.  Dans la fenêtre **éditeur de gestion des stratégies de groupe** , développez la section Configuration de l' **ordinateur**, **Préférences**, **Paramètres Windows**et dossiers **du Registre** .

3.  Dans l’arborescence de la console, cliquez avec le bouton droit sur **Registre**, pointez sur **nouveau**, cliquez sur **élément de collection**et tapez **sécurité de messagerie électronique AGPM**.

4.  Créer un élément de préférence Registre pour activer le chiffrement:

    1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur **sécurité des messages AGPM**, pointez sur **nouveau**, puis cliquez sur **élément Registre**.

    2.  Dans la boîte de dialogue **nouvelles propriétés de Registre** , sélectionnez l’action **mettre à jour** .

    3.  Pour **Hive**, sélectionnez **HKEY \ _LOCAL \ _MACHINE**.

    4.  Pour le **chemin d’accès**de la clé, tapez **SOFTWARE\\Microsoft\\AGPM**.

    5.  Pour **nom**de la valeur, tapez **EncryptSmtp**.

    6.  Pour **type de valeur**, sélectionnez **reg \ _DWORD**.

    7.  Pour **base**, sélectionnez **décimal**, et pour les données de la **valeur**, tapez **1** pour utiliser le chiffrement SSL, ou **0** pour permettre l’envoi du courrier sans chiffrement. Par défaut, le courrier électronique est envoyé sans chiffrement. Cliquez sur **OK**.

5.  Créer un élément de préférence Registre pour spécifier le port SMTP:

    1.  Dans l’arborescence de la console, cliquez avec le bouton droit sur **sécurité des messages AGPM**, pointez sur **nouveau**, puis cliquez sur **élément Registre**.

    2.  Dans la boîte de dialogue **nouvelles propriétés de Registre** , sélectionnez l’action **mettre à jour** .

    3.  Pour **Hive**, sélectionnez **HKEY \ _LOCAL \ _MACHINE**.

    4.  Dans la boîte de dialogue **chemin d’accès** de la clé, tapez **SOFTWARE\\Microsoft\\AGPM**.

    5.  Pour **nom**de la valeur, tapez **SmtpPort**.

    6.  Pour **type de valeur**, sélectionnez **reg \ _DWORD**.

    7.  Pour **base**, sélectionnez **décimal**et pour les **données**de la valeur, tapez un numéro de port pour le port SMTP. Par défaut, le port SMTP est le port 25 si le chiffrement n’est pas activé ou le port 587 si le chiffrement SSL est activé. Cliquez sur **OK**.

6.  Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** , puis archivez et déployez l’objet de stratégie de groupe. Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md).

### Autres éléments à prendre en considération

-   Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer les paramètres du Registre à l’aide des préférences de stratégie de groupe. Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)

### Références supplémentaires

-   [Configuration de la Gestion avancée des stratégies de groupe](configuring-advanced-group-policy-management-agpm40.md)

 

 





