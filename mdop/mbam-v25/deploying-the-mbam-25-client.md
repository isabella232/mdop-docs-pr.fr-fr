---
title: Déploiement du client MBAM2.5
description: Déploiement du client MBAM2.5
author: dansimp
ms.assetid: 0a96a0ee-f280-49d9-a244-88f4147fe9fd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 375af8966c8e66a58baec5065d065891187899fc
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811658"
---
# Déploiement du client MBAM2.5


Le logiciel client Microsoft BitLocker Administration and Analysis (MBAM) permet aux administrateurs d’appliquer et de surveiller le chiffrement de lecteur BitLocker sur les ordinateurs de l’entreprise. Le client BitLocker peut être intégré à une organisation en déployant le client par le biais d’un système de distribution de logiciels électronique, tel que les services de domaine Active Directory (AD FS), ou en chiffrant directement les ordinateurs clients dans le cadre du processus d’imagerie initial.

En fonction du moment où vous déployez le logiciel client d’administration et de surveillance de BitLocker, vous pouvez activer le chiffrement de lecteur BitLocker sur un ordinateur de votre organisation avant que l’utilisateur final ne reçoive l’ordinateur ou après la configuration de la stratégie de groupe et le déploiement du logiciel client MBAM à l’aide d’un système de déploiement de logiciels d’entreprise.

## Déployer le client MBAM sur un ordinateur portable ou de bureau


Après avoir configuré les paramètres de stratégie de groupe, vous pouvez utiliser un produit système de déploiement de logiciels d’entreprise tel que MicrosoftSystemCenter2012 ConfigurationManager ou les services de domaine Active Directory pour déployer les fichiers Windows Installer du client MBAM sur les ordinateurs cibles. Vous pouvez utiliser les fichiers MbamClientSetup.exe de la 32 ou de 64 bits ou les fichiers MBAMClient.msi 32 ou 64 bits, fourni avec le logiciel client MBAM. Pour plus d’informations sur le déploiement des paramètres de stratégie de groupe MBAM, voir [déploiement d’objets de stratégie de groupe MBAM 2,5](deploying-mbam-25-group-policy-objects.md).

**Remarques**  À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM. Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit.

 

[Déploiement du client MBAM pour ordinateur de bureau ou ordinateurs portables](how-to-deploy-the-mbam-client-to-desktop-or-laptop-computers-mbam-25.md)

## Déploiement du client MBAM dans le cadre d’un déploiement Windows


Dans les organisations sur lesquelles les ordinateurs sont reçus et configurés de manière centralisée, vous pouvez installer le client MBAM pour gérer le chiffrement de lecteur BitLocker sur chaque ordinateur avant d’y écrire des données utilisateur. L’avantage de ce processus est que chaque ordinateur est alors conforme à la norme de chiffrement du lecteur BitLocker. Cette méthode ne repose pas sur l’action de l’utilisateur, car l’administrateur l’a déjà crypté. Une supposition essentielle pour ce scénario est que la stratégie de l’organisation installe une image Windows d’entreprise avant que l’ordinateur ne soit remis à l’utilisateur. Si les paramètres de stratégie de groupe ont été configurés pour exiger un code confidentiel, les utilisateurs sont invités à définir un code confidentiel après réception de la stratégie.

[Comment activer BitLocker à l'aide de MBAM dans le cadre d'un déploiement Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

## Déploiement du client MBAM à l’aide d’une ligne de commande


Cette section explique comment installer le client MBAM à l’aide d’une ligne de commande.

[Déploiement du client MBAM àl'aide d'une ligne de commande](how-to-deploy-the-mbam-client-by-using-a-command-line.md)

## Autres ressources pour le déploiement du client MBAM


[Déploiement de MBAM2.5](deploying-mbam-25.md)



## Rubriques connexes


[Déploiement de MBAM2.5](deploying-mbam-25.md)

[Planification de MBAM2.5](planning-for-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





