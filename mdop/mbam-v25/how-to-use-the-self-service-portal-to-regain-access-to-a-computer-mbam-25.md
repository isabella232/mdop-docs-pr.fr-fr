---
title: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
description: Utilisation du portail libre-service pour accéder de nouveau à un ordinateur
author: dansimp
ms.assetid: 3c24b13a-d1b1-4763-8ac0-0b2db46267e3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: cde9c71a957a5270d69aa8388455895f1cb2432b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811915"
---
# Utilisation du portail libre-service pour accéder de nouveau à un ordinateur


Le portail libre-service est un site Web que les administrateurs informatiques configurent dans le cadre de leur déploiement de 2,5 d’administration et de surveillance de Microsoft. Le site Web permet aux utilisateurs finaux de pouvoir accéder de manière indépendante à leurs ordinateurs s’ils sont bloqués. Le portail libre-service ne nécessite aucune assistance de la part du personnel du support technique.

Les instructions suivantes sont rédigées du point de vue des utilisateurs finaux, mais les informations peuvent être utiles pour les administrateurs informatiques.

**Important**  Un utilisateur final doit avoir réussi à se connecter à l’ordinateur (pas à distance) au moins une fois pour pouvoir récupérer sa clé via le portail libre-service. Sinon, ils doivent utiliser le portail du support technique pour la récupération de clés.

 

Les utilisateurs finaux peuvent être confrontés aux verrouillages s’ils:

-   Oublier son mot de passe ou son code confidentiel

-   Modification des fichiers du système d’exploitation, du BIOS ou du module de plateforme sécurisée (TPM)

**Remarques**  Si l’administrateur informatique a configuré une période de temporisation de l’état de session IIS, un message s’affiche dans le portail libre-service de 60 secondes avant le délai d’expiration.

 

**Pour pouvoir utiliser le portail libre-service pour accéder à un ordinateur**

1.  Dans le champ **KeyId de récupération** , entrez au moins huit l’ID de clé bitlocker de 32 chiffres qui s’affiche dans l’écran de récupération BitLocker de votre ordinateur. Si les huit premiers chiffres correspondent à plusieurs clés, un message s’affiche et vous demande d’entrer tous les 32 chiffres de l’ID de la clé de récupération.

2.  Dans le champ **raison** , sélectionnez une raison pour votre demande de clé de récupération.

3.  Cliquez sur **obtenir la clé**. Votre clé de récupération BitLocker est affichée dans le champ **votre clé de récupération BitLocker** .

4.  Entrez le code de l' 48 sur l’écran de récupération BitLocker sur votre ordinateur pour accéder à l’ordinateur.



## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





