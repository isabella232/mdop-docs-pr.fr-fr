---
title: Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V
description: Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V
author: dansimp
ms.assetid: b50d0dfb-8d61-4543-9607-a29bbb1ed45f
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 9662bb8202285d51971eeea8beaef938b98ed6b0
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811477"
---
# Comment appliquer des paramètres de machine virtuelle à un espace de travail MED-V


Chaque espace de travail MED-V doit être associé à une image Microsoft Virtual PC. Les paramètres de l’ordinateur virtuel vous permettent d’affecter une image de PC virtuel et de définir d’autres propriétés d’ordinateur virtuel.

Tous les paramètres d’ordinateur virtuel sont configurés dans le module de **stratégie** sous l’onglet Paramètres de l' **ordinateur virtuel** .

**Pour appliquer les paramètres d’ordinateur virtuel à un espace de travail MED-V**

1.  Cliquez sur l’espace de travail MED-V à configurer.

2.  Configurez les propriétés de l’ordinateur virtuel comme décrit dans le tableau suivant.

3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés de la machine virtuelle**

Description de la propriété-paramètres de l' *ordinateur virtuel*

Image affectée

Image de l’ordinateur virtuel Microsoft réel affectée à l’espace de travail MED-V. Le menu fournit une liste de toutes les images Virtual PC disponibles. Les types d’image suivants se trouvent dans la liste des images **actives** :

-   **Images de test locales**: images de l’ordinateur local qui ne sont pas encore empaquetées. Ces noms d’image sont suivis du mot «test» entre parenthèses (test) et sont uniquement à des fins de test.

-   **Images compactées locales**: images empaquetées sur l’ordinateur local. Ces images sont suivies du mot «local» entre parenthèses (locales) et ne peuvent pas être téléchargées par les clients tant que l’administrateur ne les a pas chargées sur le serveur.

    Une image locale peut être sélectionnée si vous créez un package qui sera distribué au client par le biais d’un support amovible (par exemple, USB ou DVD).

-   **Images compactées sur le serveur**: les images qui se trouvent sur le serveur et peuvent être téléchargées par les clients. Cliquez sur Actualiser pour actualiser la liste des images.

    **Remarques**  Chaque image d’espace de travail MED-V ne peut être utilisée que par un seul utilisateur Windows.

     

Espace de travail permanent

Activez cette case à cocher pour configurer l’espace de travail MED-V comme permanent. Dans un espace de travail MED-V permanent, lorsque l’espace de travail MED-V est arrêté, les modifications et les ajouts apportées à l’espace de travail MED-V sont enregistrés dans l’espace de travail MED-V.

Pour un espace de travail de domaine MED-V, cette option doit être sélectionnée.

**Remarques**  Ce paramètre ne doit pas être modifié après le déploiement d’un espace de travail MED-V pour les utilisateurs.

 

Arrêter l’ordinateur virtuel lors de l’arrêt de l’espace de travail

Activez cette case à cocher pour éteindre l’ordinateur virtuel lors de l’arrêt de l’espace de travail MED-V. Si cette case à cocher est désactivée, à l’achèvement de chaque session, la machine virtuelle n’est pas arrêtée, mais prend une photo de l’ordinateur virtuel. Lors de l’initiation d’une nouvelle session, Windows démarre à partir de la capture d’une capture d’image (c’est-à-dire que Windows ne redémarre pas et qu’aucune connexion n’est requise).

**Remarques**  Cette propriété est activée uniquement si l’option **espace de travail est permanente** .

 

Connexion à Windows dans la VM à l’aide d’informations d’identification MED-V (SSO)

Activez cette case à cocher pour vous connecter à Windows sur l’ordinateur virtuel en utilisant les informations d’identification MED-V entrées lors de la connexion au client MED-V.

**Remarques**  Cette propriété est uniquement activée lorsque l’option **espace de travail est permanente** .

 

L’espace de travail est revertible

Activez cette case à cocher pour configurer l’espace de travail MED-V en tant que revertible. Dans un espace de travail MED-V de revertible, à l’achèvement de chaque session (autrement dit, lorsque l’utilisateur arrête l’espace de travail MED-V), l’espace de travail MED-V retrouve son état d’origine au cours du déploiement. Aucune modification ou aucun complément n’est enregistré dans l’espace de travail MED-V entre les sessions.

**Remarques**  Ce paramètre ne doit pas être modifié après le déploiement d’un espace de travail MED-V pour les utilisateurs.

 

Synchroniser le fuseau horaire de l’espace de travail avec un hôte

Activez cette case à cocher pour synchroniser le fuseau horaire dans l’espace de travail MED-V avec l’hôte.

La synchronisation fonctionne différemment selon que l’espace de travail MED-V est persistant ou revertible, comme suit:

-   Dans un espace de travail MED-V permanent, le fuseau horaire tente d’abord de se synchroniser avec le serveur. En cas d’échec, il se synchronise avec l’hôte.

-   Dans un espace de travail MED-V revertible, le fuseau horaire est synchronisé avec l’hôte.

*Paramètres de verrouillage*

Verrouiller l’espace de travail sur l’hôte de secours/veille prolongée

Activez cette case à cocher pour verrouiller automatiquement l’espace de travail MED-V lorsque l’ordinateur hôte passe en mode veille ou mise en veille prolongée.

Verrouiller l’espace de travail après

Activez cette case à cocher pour verrouiller l’espace de travail MED-V lorsque l’espace de travail MED-V est inactif pendant une durée spécifiée. Lorsque cette case est cochée, la case numérique est activée. Entrez le nombre de minutes d’inactivité avant de verrouiller l’espace de travail MED-V.

**Remarques**  Le temps d’inactivité fait référence aux applications d’espace de travail MED-V (pas aux applications hôtes).

 

*Paramètres de mise à jour d’image*

Conserver seulement

Activez cette case à cocher pour limiter le nombre de versions d’anciennes images à conserver.

Lorsque cette case est cochée, la case numérique est activée. Entrez le nombre d’anciennes versions à conserver.

Suggérer une mise à jour lorsqu’une nouvelle version est disponible

Activez cette case à cocher pour suggérer (mais pas forcée) une mise à jour lorsqu’une nouvelle version de l’image est disponible.

Les clients doivent utiliser le transfert de découpage lors du téléchargement d’images pour cet espace de travail

Activez cette case à cocher pour activer le transfert de découpage (pour plus d’informations, reportez-vous à la section [technologie de transfert de coupure med-v](med-v-trim-transfer-technology-medvv2.md)) lors du téléchargement d’images associées à cet espace de travail MED-v Si cette case à cocher est désactivée, l’image complète est téléchargée.

**Remarques**  Le transfert de découpage nécessite l’indexation du disque dur, ce qui peut prendre un certain temps. Il est recommandé d’utiliser le transfert de découpage lors de l’indexation du disque dur pour plus d’efficacité que le téléchargement de la nouvelle version d’image, par exemple lors du téléchargement d’une version d’image similaire à la version existante.

 

 

## Rubriques connexes


[Création d'une image MED-V](creating-a-med-v-image.md)

[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

 

 





