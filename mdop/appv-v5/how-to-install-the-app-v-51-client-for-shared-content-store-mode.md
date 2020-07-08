---
title: Installation d'App-V5.1 Client pour le mode Magasin de contenu partagé
description: Installation d'App-V5.1 Client pour le mode Magasin de contenu partagé
author: dansimp
ms.assetid: 6f3ecb1b-b5b5-4ae0-8de9-b4ffdfd2c216
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a7ce8114a44762180bf9bb0240913dca50c55d31
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805437"
---
# Installation d'App-V5.1 Client pour le mode Magasin de contenu partagé


Utilisez la procédure suivante pour installer le client Microsoft Application Virtualization (App-V) 5,1 de façon à ce qu’il utilise le mode SCS (App-5,1 V) Shared content Store. Assurez-vous que toutes les conditions préalables requises sont installées sur l’ordinateur sur lequel vous envisagez d’installer. Utilisez le lien suivant pour afficher les [conditions préalables pour App-V 5,1](app-v-51-prerequisites.md).

**Remarques**  Avant d’effectuer cette procédure, si nécessaire, désinstallez les versions existantes du client App-V 5,1.

 

Pour plus d’informations sur le mode SCS, voir [magasin de contenus partagés dans Microsoft App-V 5,0-en coulisses](https://go.microsoft.com/fwlink/?LinkId=316879) ( https://go.microsoft.com/fwlink/?LinkId=316879) .

**Installer et configurer le client App-V 5,1 pour le mode SCS**

1.  Copiez les fichiers d’installation du client App-V 5,1 sur l’ordinateur sur lequel il est installé. Ouvrez une ligne de commande et à partir du répertoire où sont enregistrés les fichiers d’installation, tapez l’une des options suivantes, en fonction de la version du client que vous installez:

    -   Pour installer la version RDS du type de client App-V 5,1: **appv\_client\_setup\_rds.exe/SHAREDCONTENTSTOREMODE = 1/q**

    -   Pour installer la version standard du type de client App-V 5,1: **appv\_client\_setup.exe/SHAREDCONTENTSTOREMODE = 1/q**

        **Important**  Vous devez effectuer une installation silencieuse ou l’installation échouera.

         

2.  Une fois l’installation terminée, vous pouvez déployer des packages vers l’ordinateur exécutant le client et le contenu de tous les packages sera diffusé sur le réseau.

    Vous **avez une suggestion pour App-V**? Ajoutez ou Votez en fonction [de suggestions.](http://appv.uservoice.com/forums/280448-microsoft-application-virtualization) **Vous avez un problème lié à l’application-V?** Utilisez le [Forum TechNet App-V](https://social.technet.microsoft.com/Forums/home?forum=mdopappv).

## Rubriques connexes


[Planification du déploiement d'App-V5.1 Sequencer et Client](deploying-the-app-v-51-sequencer-and-client.md)

 

 





