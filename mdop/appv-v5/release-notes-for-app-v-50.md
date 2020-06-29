---
title: Notes de publication pour App-V5.0
description: Notes de publication pour App-V5.0
author: dansimp
ms.assetid: 68a6a5a1-4b3c-4c09-b00c-9ca4237695d5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: e49f6072d738b45afe25de24f2ee9a2d09d64a2e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804890"
---
# Notes de publication pour App-V5.0


**Pour rechercher un problème spécifique dans ces notes de publication, appuyez sur CTRL + F.**

Lisez attentivement ces notes de publication avant d’installer App-V 5,0.

Ces notes de publication contiennent des informations requises pour l’installation de l’application-V 5,0. Les notes de publication contiennent également des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents App-V 5,0, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## À propos de la documentation relative aux produits


Pour plus d’informations sur la documentation App-V 5,0, consultez la page d’accueil App-V 5,0 sur Microsoft TechNet.

## Fournir des commentaires


Vos commentaires vous intéressent sur App-V 5,0. Vous pouvez envoyer vos commentaires à <mdopdocs@microsoft.com> .

**Remarques**  Cette adresse de messagerie n’est pas un canal de support, mais vos commentaires nous aideront à planifier des changements ultérieurs dans la documentation et les versions de nos produits.

 

Pour obtenir les informations les plus récentes sur MDOP et les ressources de formation supplémentaires, voir la page d' [utilisation de MDOP](https://go.microsoft.com/fwlink/p/?LinkId=236032) .

Pour en savoir plus sur les nouvelles mises à jour ou pour nous faire part de vos commentaires, suivez-nous sur [Facebook](https://go.microsoft.com/fwlink/p/?LinkId=242445) ou [Twitter](https://go.microsoft.com/fwlink/p/?LinkId=242447).

## Problèmes connus avec App-V 5,0


Cette section contient des notes de publication relatives aux problèmes connus avec App-V 5,0.

### Impossible d’arrêter l’ajout de packages lors de l’utilisation des cmdlets PowerShell du serveur

Lorsque vous ajoutez un package à l’aide de PowerShell, il n’existe aucune méthode de fermeture pour ajouter de nouveaux packages.

Solution de contournement: pour arrêter l’ajout de packages, appuyez sur **entrée** après avoir ajouté le package final.

### <a href="" id="-------------app-v-5-0-client-rejects-packages-from-servers-whose-ssl-certificate-has-been-revoked"></a> Le client App-V 5,0 rejette les packages des serveurs dont le certificat SSL a été révoqué

Dans le cadre de l’utilisation du protocole HTTPs, le client App-V 5,0 refusera par défaut les packages des serveurs dont le certificat SSL a été révoqué. Ce comportement peut être désactivé à l’aide de la configuration en modifiant le paramètre **VerifyCertificateRevocationList** . L’application d’une nouvelle configuration pour ce paramètre n’est pas appliquée tant que le service App-V 5,0 n’est pas redémarré.

Solution de contournement: redémarrez le service App-V 5,0.

## Informations de copyright des notes de publication


Microsoft, Active Directory, ActiveX, Bing, Excel, Silverlight, SQLServer, Windows, MicrosoftIntune et WindowsPowerShell sont des marques commerciales du groupe de sociétés Microsoft. Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.








## Rubriques connexes


[À propos d'App-V5.0](about-app-v-50.md)

 

 





