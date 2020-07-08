---
title: Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe
description: Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe
author: dansimp
ms.assetid: 79d03a2b-2586-4ca7-bbaa-bdeb0a694279
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: cd257691bf223baa5e2919d83fdbf53d34f271ac
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805280"
---
# Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe


Utilisez le modèle ADMX App-V 5,0 pour configurer les paramètres du client App-V 5,0 à l’aide du modèle ADMX et de la stratégie de groupe.

**Pour modifier la configuration du client App-V 5,0 à l’aide d’une stratégie de groupe**

1.  Pour modifier la configuration du client App-V 5,0, recherchez les fichiers **ADMXTemplate** disponibles avec App-v 5,0.

    **Remarques**  Utilisez le lien suivant pour télécharger les modèles App-V 5,0 **ADMX**: <https://go.microsoft.com/fwlink/p/?LinkId=393941> .

     

2.  Sur l’ordinateur sur lequel vous gérez la stratégie de groupe, en général le contrôleur de domaine, copiez le fichier template **. admx** dans le répertoire suivant: ** &lt; lecteur d’installation &gt; \ \ Windows \ \ PolicyDefinitions**.

    Ensuite, sur le même ordinateur, copiez le fichier **. adml** dans le répertoire suivant: ** &lt; InstallationDrive &gt; \ \ Windows \ \ POLICYDEFINITIONS \ \ en-US**.

3.  Une fois que vous avez copié les fichiers, ouvrez la console de gestion des stratégies de groupe, pour modifier les stratégies associées à vos clients App-v 5,0, accédez à stratégies de configuration de l' **ordinateur**  /  **Policies**  /  -application**modèles d’administration**  /  **System**  /  **-V**.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Déploiement d'App-V5.0](deploying-app-v-50.md)

[À propos des paramètres de configuration du client](about-client-configuration-settings.md)

 

 





