---
title: Configuration de certificats pour prendre en charge le service de gestion Web App-V
description: Configuration de certificats pour prendre en charge le service de gestion Web App-V
author: dansimp
ms.assetid: b7960161-2c19-4cbf-a98a-d4b06f547dce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 23839e6fad79c1f10eb2416941396ad3c6f04d26
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809024"
---
# Configuration de certificats pour prendre en charge le service de gestion Web App-V


Le service de gestion de site Web de l’application doit être configuré pour prendre en charge les connexions SSL pour sécuriser la communication. Ce processus exige que le serveur Web ou l’ordinateur sur lequel le service de gestion est installé dispose d’un certificat délivré au service ou à l’ordinateur.

Les scénarios suivants montrent comment obtenir un certificat à cette fin:

1.  L’infrastructure de l’entreprise possède déjà une infrastructure à clé publique (PKI) qui publie automatiquement des certificats sur les ordinateurs.

2.  L’infrastructure de l’entreprise possède déjà une infrastructure PKI, même si elle n’émet pas automatiquement de certificats pour les ordinateurs.

3.  Aucune PKI n’est en place pour l’infrastructure de l’entreprise.

Dans chacun des scénarios ci-dessus, la méthode d’obtention d’un certificat est différente, mais le résultat final est le même. L’administrateur doit attribuer un certificat au site Web IIS par défaut et configurer le service de gestion des applications Web App-V pour exiger des communications sécurisées.

**Important**  Le nom du certificat doit correspondre au nom du serveur. Il est recommandé d’utiliser des noms de domaine complets (FQDN) pour le nom usuel du certificat.

 

App-V peut utiliser les serveurs IIS pour prendre en charge différentes configurations d’infrastructure. Pour plus d’informations sur la configuration des serveurs IIS pour la prise en charge des HTTPs, voir <https://go.microsoft.com/fwlink/?LinkId=151972> .

## Rubriques connexes


[Comment installer et configurer App-V Management Console pour un environnement plus sécurisé](how-to-install-and-configure-the-app-v-management-console-for-a-more-secure-environment.md)

 

 





