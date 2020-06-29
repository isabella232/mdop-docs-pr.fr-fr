---
title: Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur
description: Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur
ms.assetid: 498d50c7-f13d-4fbb-8ea1-b959ade26fdf
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/21/2016
ms.openlocfilehash: 354db96223e623a7cd0416cb49ad67eb4d8f7162
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805527"
---
# Déploiement de l’application-V 4,6 et du client App-V 5,1 sur le même ordinateur

**Remarque:** App-V 4,6 a quitté le support technique standard.

Utilisez les informations ci-dessous pour installer le client Microsoft Application Virtualization (App-V) 5,1 (de préférence avec les derniers Service Packs et correctifs) et le client App-V 4.6 SP2 ou le client App-V 4.6 S3 sur le même ordinateur. Pour plus d’informations sur les versions prises en charge, les configurations requises et d’autres informations de planification, voir [planification de la migration à partir d’une version antérieure d’App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md).

**Pour déployer le client App-V 5,1 et le client App-V 4,6 sur le même ordinateur**

1.  Installez la version suivante du client App-V sur l’ordinateur exécutant App-V 4,6.

    -   [Microsoft Application Virtualization 4,6 Service Pack 3](https://www.microsoft.com/download/details.aspx?id=41187)

2.  Installez le client App-V 5,1 sur l’ordinateur exécutant la version App-V 4,6 SP3 du client. Pour obtenir de meilleurs résultats, nous vous recommandons d’installer toutes les mises à jour disponibles sur le client App-V 5,1.

3.  Convertissez ou réexécutez progressivement les packages.

    -   Pour convertir les packages, utilisez le convertisseur de package App-V 5,1, puis convertissez les packages requis au format App-V 5,1 (**. AppV**).

    -   Pour réorganiser les packages, envisagez d’utiliser la dernière version du Sequencer pour obtenir de meilleurs résultats.

    Pour plus d’informations sur les packages de publication, voir [Comment publier un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-51.md).

4.  Déploiement de packages sur les ordinateurs clients.

5.  Convertissez les points d’extension selon vos besoins. Pour plus d’informations, voir les ressources suivantes :

    -   [Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 converti pour tous les utilisateurs sur un ordinateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-a-converted-app-v-51-package-for-all-users-on-a-specific-computer.md)

    -   [Migration de points d'extension d'un package App-V4.6 vers un package App-V5.1 pour un utilisateur spécifique](how-to-migrate-extension-points-from-an-app-v-46-package-to-app-v-51-for-a-specific-user.md)

    -   [Comment convertir un package créé dans une version précédente d'App-V](how-to-convert-a-package-created-in-a-previous-version-of-app-v51.md)

6.  Testez la réussite de vos packages App-V 5,1, puis supprimez les packages 4,6. Pour vérifier l’état de l’utilisateur sur vos ordinateurs clients, nous vous recommandons d’utiliser [la virtualisation de l’interface utilisateur](https://technet.microsoft.com/library/dn458947.aspx) ou un autre outil de gestion de l’environnement des utilisateurs.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Planification d'une migration à partir d'une version précédente d'App-V](planning-for-migrating-from-a-previous-version-of-app-v51.md)

[Planification du déploiement d'App-V5.1 Sequencer et Client](deploying-the-app-v-51-sequencer-and-client.md)

 

 





