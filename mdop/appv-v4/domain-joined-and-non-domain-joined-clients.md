---
title: Clients joints au domaine et non joints au domaine
description: Clients joints au domaine et non joints au domaine
author: dansimp
ms.assetid: a935dc98-de60-45f3-ab74-2444ce082e88
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: c4385ab3f26bb867dd649fe768e1500c9d015ffa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808873"
---
# Clients joints au domaine et non joints au domaine


Le client de bureau App-V peut être configuré pour autoriser la connexion à un réseau, qu’il s’agisse d’un domaine ou d’un autre domaine.

## Clients liés à un domaine


Les clients appartenant à un domaine, mais en dehors du réseau interne, peuvent communiquer avec l’infrastructure App-V via une connexion VPN. Lorsque vous souhaitez offrir aux utilisateurs la possibilité de quitter le réseau interne tout en continuant à communiquer dans une infrastructure App-V, votre environnement nécessite une configuration très légère. Dans la mesure où les utilisateurs font déjà partie du domaine, il vous suffit de vérifier que les informations d’identification mises en cache sont prises en charge sur le client. Il s’agit de la configuration par défaut, et les modifications apportées à ce paramètre peuvent être effectuées à partir de stratégies de groupe.

Comme indiqué dans le guide des pratiques recommandées pour l’application-V, l’utilisateur tente d’envoyer son ticket utilisateur à l’infrastructure App-V pour l’authentification. Si le ticket est arrivé à expiration, il revient à utiliser NTLM et aux informations d’identification mises en cache sur l’ordinateur. Pour autoriser l’itinérance, les administrateurs doivent s’assurer que le serveur de publication qui est consulté en interne est disponible au même nom de manière externe pour que les noms soient résolus correctement.

## Clients non liés à un domaine


Les clients qui ne sont pas connectés au domaine et qui doivent communiquer dans l’infrastructure App-V doivent être configurés pour s’assurer que l’authentification auprès de l’infrastructure App-V est réussie. Le client de bureau App-V n’autorise pas le processus de mise à jour de la publication, de sorte que le client doit être configuré pour présenter les informations d’identification appropriées au serveur de gestion de l’application-V.

Le serveur de publication qui est configuré pour l’actualisation de la publication à partir du client autre qu’un domaine joint, exige que le nom externe auquel les clients accèdent soit configuré en tant que nom commun ou autre nom (SAN) sur le certificat du serveur de publication.

## Rubriques connexes


[Comment affecter les informations d’identification appropriées pour Windows Vista](how-to-assign--the-proper-credentials-for-windows-vista.md)

[Comment affecter les informations d’identification appropriées pour Windows XP](how-to-assign--the-proper-credentials-for-windows-xp.md)

 

 





