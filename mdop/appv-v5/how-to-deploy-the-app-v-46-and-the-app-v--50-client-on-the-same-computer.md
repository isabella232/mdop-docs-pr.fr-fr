---
title: Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur
description: Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur
ms.assetid: 5b7e27e4-4360-464c-b832-f1c7939e5485
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.date: 06/21/2016
ms.openlocfilehash: 38e77ce6ce6c0dba7c67f6c0dfa5c9e263e07e20
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805533"
---
# Déploiement de l’application-V 4,6 et du client App-V 5,0 sur le même ordinateur

**Remarque:** App-V 4,6 a quitté le support technique standard. L’exemple suivant suppose que le client App-V 4,6 SP3 est déjà installé.

Utilisez les informations suivantes pour installer le client App-V 5,0 (de préférence, avec les derniers Service Packs et correctifs) et le client App-V 4.6 SP3 sur le même ordinateur. Pour plus d’informations sur les versions prises en charge, les configurations requises et d’autres informations de planification, voir [planification de la migration à partir d’une version antérieure d’App-V](planning-for-migrating-from-a-previous-version-of-app-v.md).

**Pour déployer le client App-V 5,0 et le client App-V 4,6 sur le même ordinateur**

1.  Installez le client App-V 5,0 SP3 sur l’ordinateur exécutant la version App-V 4,6 du client. Pour obtenir de meilleurs résultats, nous vous recommandons d’installer toutes les mises à jour disponibles sur le client App-V 5,0 SP3.

2.  Convertissez ou réexécutez progressivement les packages.

    -   Pour convertir les packages, utilisez le convertisseur de package App-V 5,0, puis convertissez les packages requis au format App-V 5,0 (**. AppV**).

    -   Pour réorganiser les packages, envisagez d’utiliser la dernière version du Sequencer pour obtenir de meilleurs résultats.

    Pour plus d’informations sur les packages de publication, voir [Comment publier un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-50.md).

3.  Déploiement de packages sur les ordinateurs clients.

4.  Convertissez les points d’extension selon vos besoins. Pour plus d’informations, voir les ressources suivantes :

    -   [Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 converti pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-50-package-for-all-users-on-a-specific-computer.md)

    -   [Migration de points d'extension d'un package App-V4.6 vers un package App-V5.0 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-50-for-a-specific-user.md)

    -   [Comment convertir un package créé dans une version précédente d'App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v.md)

5.  Testez la réussite de vos packages App-V 5,0, puis supprimez les packages 4,6. Pour vérifier l’état de l’utilisateur sur vos ordinateurs clients, nous vous recommandons d’utiliser [la virtualisation de l’interface utilisateur](https://technet.microsoft.com/library/dn458947.aspx) ou un autre outil de gestion de l’environnement des utilisateurs.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Planification d'une migration à partir d'une version précédente d'App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)

[Déploiement d'App-V5.0 Sequencer et Client](deploying-the-app-v-50-sequencer-and-client.md)

 

 





