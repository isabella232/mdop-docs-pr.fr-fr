---
title: Résolution des problèmes d'autorisation de certificat
description: Résolution des problèmes d'autorisation de certificat
author: dansimp
ms.assetid: 06b8cbbc-93fd-44aa-af39-2d780792d3c3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 728c35b9f51c8f2e18db8acd63708c70bb5d3100
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806214"
---
# Résolution des problèmes d'autorisation de certificat


Après l’installation de App-V 4.5, si la clé privée n’a pas été configurée à l’aide de la liste de contrôle d’accès correcte pour le service réseau, un événement est consigné dans le journal des événements Windows et une entrée est placée dans le `Sft-server.log` fichier.

## Messages d’erreur


### Windows Server2003

ID d’événement 36870: une erreur irrécupérable s’est produite lors d’une tentative d’accès à la clé privée d’informations d’identification du serveur SSL. Le code d’erreur renvoyé par le module cryptographique est 0x80090016.

### Windows Server 2008

ID d’événement 36870: une erreur irrécupérable s’est produite lors d’une tentative d’accès à la clé privée d’informations d’identification du serveur SSL. Le code d’erreur renvoyé par le module cryptographique est 0x8009030d.

## SFT-Server. log


Le message d’erreur suivant est placé dans le `sft-server.log` fichier situé dans le `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\logs` répertoire:

Le certificat n’a pas pu être chargé. Code d’erreur \ [-2146893043 \]. Assurez-vous que le compte de service réseau dispose de l’accès approprié au certificat et au fichier de clé privée correspondant.

 

 





