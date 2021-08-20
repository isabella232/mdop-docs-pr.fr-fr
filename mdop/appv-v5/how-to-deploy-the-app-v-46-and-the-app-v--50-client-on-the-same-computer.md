---
title: Déploiement d’App-V 4.6 et du client App-V 5.0 sur le même ordinateur
description: Déploiement d’App-V 4.6 et du client App-V 5.0 sur le même ordinateur
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.prod: w10
ms.openlocfilehash: f10f3d159c4724f3b486215b1169825bb029316d
ms.sourcegitcommit: 0132cd232b9c030820d95d91b71c4def0184400a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "11907227"
---
# <a name="how-to-deploy-the-app-v-46-and-the-app-v-50-client-on-the-same-computer"></a>Déploiement d’App-V 4.6 et du client App-V 5.0 sur le même ordinateur

**Remarque :** App-V 4.6 a quitté le support classique. L’exemple suivant suppose que le client App-V 4.6 SP3 est déjà installé.

Utilisez les informations suivantes pour installer le client App-V 5.0 (de préférence, avec les derniers Service Packs et correctifs logiciels) et le client App-V 4.6 SP3 sur le même ordinateur. Pour obtenir des versions, des conditions requises et d’autres informations de planification, voir [Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Pour déployer le client App-V 5.0 et le client App-V 4.6 sur le même ordinateur**

1.  Installez le client App-V 5.0 SP3 sur l’ordinateur qui exécute la version App-V 4.6 du client. Pour de meilleurs résultats, nous vous recommandons d’installer toutes les mises à jour disponibles sur le client App-V 5.0 SP3.

2.  Convertissez ou resserez progressivement les packages.

    -   Pour convertir les packages, utilisez le convertisseur de package App-V 5.0 et convertissez les packages requis au format de fichier App-V 5.0 (**.appv).**

    -   Pour ré-séquencer les packages, envisagez d’utiliser la dernière version de Sequencer pour obtenir de meilleurs résultats.

    Pour plus d’informations sur la publication de packages, voir [Comment publier un package à l’aide](how-to-publish-a-package-by-using-the-management-console-50.md)de la console de gestion .

3.  Déployer des packages sur les ordinateurs clients.

4.  Convertissez les points d’extension, selon vos besoins. Pour plus d'informations, voir les ressources suivantes:

    -   [Migration de points d'extension d'un package App-V 4.6 vers un package App-V 5.0 converti pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Migration de points d'extension d'un package App-V 4.6 vers un package App-V 5.0 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Comment convertir un package créé dans une version précédente d'App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Testez la réussite de vos packages App-V 5.0, puis supprimez les packages 4.6. Pour vérifier l’état utilisateur de vos ordinateurs clients, nous vous recommandons d’utiliser [la virtualisation](https://technet.microsoft.com/library/dn458947.aspx) de l’expérience utilisateur ou un autre outil de gestion de l’environnement utilisateur.

    **Vous avez une suggestion pour App-V**? Ajoutez ou votez sur les suggestions [ici.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème App-V ?** Utilisez le [forum TechNet App-V.](https://social.technet.microsoft.com/Forums/home?forum=mdopappv)

## <a name="related-topics"></a>Rubriques associées


[Planification d'une migration à partir d'une version précédente d'App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Déploiement d'App-V 5.0 Sequencer et Client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





