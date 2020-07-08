---
title: Configuration de certificats pour prendre en charge la diffusion en continu sécurisée
description: Configuration de certificats pour prendre en charge la diffusion en continu sécurisée
author: dansimp
ms.assetid: 88dc76d8-7745-4729-92a1-af089c921244
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 9376634a1b9843f46dba4cd452e672cc9e535226
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809029"
---
# Configuration de certificats pour prendre en charge la diffusion en continu sécurisée


Par défaut, le service App-V s’exécute sous le compte service réseau. Toutefois, vous pouvez créer un compte de service dans les services de domaine Active Directory et remplacer le compte de service réseau par le compte de domaine Active Directory.

Le contexte de sécurité en vertu duquel le service s’exécute est important pour la configuration des communications sécurisées améliorées. Ce contexte de sécurité doit disposer d’autorisations de lecture pour la clé privée du certificat. Lorsqu’une *demande de signature de certificat* (CSR) PKCS \ #10 est générée pour le serveur App-V, *il est appelé* et une clé privée est générée. La clé privée est sécurisée, avec les autorisations accordées uniquement aux comptes système et administrateur.

Vous devez modifier les listes de contrôle d’accès (ACL) sur la clé privée pour autoriser la gestion de l’application-V ou du serveur de diffusion en continu à utiliser la clé privée pour une communication sécurisée TLS correcte.

## Obtention et installation d’un certificat


Les scénarios d’obtention et d’installation d’un certificat pour App-V sont les suivants:

-   Infrastructure à clé publique (PKI) interne.

-   Certificat tiers délivrant une autorité de certification (CA).

    **Remarques**  Si vous avez besoin d’obtenir un certificat auprès d’une autorité de certification tierce, suivez la documentation disponible sur le site Web de cette autorité de certification.

     

Si une infrastructure PKI a été déployée, contactez les administrateurs d’infrastructure à clé publique pour obtenir un certificat conforme aux exigences décrites dans cette rubrique. Si aucune infrastructure PKI n’est disponible, utilisez une autorité de certification tierce pour obtenir un certificat valide.

Pour obtenir des instructions détaillées sur l’obtention et l’installation d’un certificat, voir <https://go.microsoft.com/fwlink/?LinkId=151969> .

## Rubriques connexes


Configuration de certificats pour la prise en charge de la diffusion en continu sécurisé de [la modification des autorisations de clé privée pour le serveur de gestion ou le serveur de diffusion](how-to-modify-private-key-permissions-to-support-management-server-or-streaming-server.md)

 

 





