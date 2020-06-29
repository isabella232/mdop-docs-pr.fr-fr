---
title: Exemples de configurations d'ordinateur virtuel
description: Exemples de configurations d'ordinateur virtuel
author: dansimp
ms.assetid: 5937601e-41ab-4ca2-8fa1-3c9154710cd6
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6b9fc7b1f88b2b30ea149fe73a387826fdbb2a66
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810644"
---
# Exemples de configurations d'ordinateur virtuel


Voici quelques exemples de configurations d’ordinateur virtuel typiques: une dans un espace de travail MED-V persistant et une dans un espace de travail revertible MED-V.

**Remarques**  Ces exemples ne sont pas destinés à une utilisation dans tous les environnements. Ajustez la configuration en fonction de votre environnement.

 

**Pour configurer une configuration de domaine standard dans un espace de travail MED-V permanent**

1.  Configurez Sysprep sur l’image de base pour créer un SID unique. Pour plus d’informations, reportez-vous à [la rubrique Création d’une image de PC virtuel pour MED-V](creating-a-virtual-pc-image-for-med-v.md#bkmk-howtoconfiguresysprepformedvimages).

2.  Dans l’onglet Configuration de l' **ordinateur virtuel** , activez la case à cocher **exécuter la configuration VM** .

3.  Dans la section modèle de nom de l' **ordinateur VM** , configurez le modèle du nom d’image de l’ordinateur. Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

4.  Cliquez sur **éditeur de script**, puis, dans la boîte de dialogue Éditeur de script de **configuration VM** , configurez les actions suivantes:

    1.  **Renommer ordinateur**

    2.  **Redémarrer Windows**

    3.  **Vérifier la connectivité**

    4.  **Joindre un domaine**

    5.  **Désactiver la connexion automatique**

    Pour plus d’informations, reportez-vous [à la rubrique Configuration d’actions de script](how-to-set-up-script-actions.md).

5.  Dans le menu **stratégie** , cliquez sur **valider**.

**Pour configurer une configuration standard dans un espace de travail revertible**

1.  Dans l’onglet Configuration de l’ordinateur **virtuel** , activez la case à cocher **Renommer l’ordinateur virtuel en fonction de votre modèle de nom d’ordinateur** .

2.  Dans la section modèle de nom de l' **ordinateur VM** , configurez le modèle du nom d’image de l’ordinateur. Pour plus d’informations, reportez-vous [à configuration des propriétés de modèle de nom d’ordinateur VM](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md).

3.  Dans le menu **stratégie** , cliquez sur **valider**.

## Rubriques connexes


[Comment configurer l'installation d'ordinateur virtuel pour un espace de travail MED-V](how-to-configure-the-virtual-machine-setup-for-a-med-v-workspacemedvv2.md)

[Comment configurer les propriétés du modèle de nom d'ordinateur virtuel](how-to-configure-vm-computer-name-pattern-propertiesmedvv2.md)

[Comment configurer des actions de script](how-to-set-up-script-actions.md)

 

 





