---
title: Procédure pour configurer la sécurité post-installation de Streaming Server
description: Procédure pour configurer la sécurité post-installation de Streaming Server
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807293"
---
# Procédure pour configurer la sécurité post-installation de Streaming Server


Configurez le serveur de streaming App-V pour renforcer la sécurité par le biais du Registre. Comme pour le serveur de gestion App-V, un certificat doit être correctement configuré avec l’identificateur EKU approprié pour l’authentification du serveur avant de terminer la procédure de post-installation suivante.

**Pour configurer la sécurité du serveur de diffusion après l’installation**

1.  Créez une console MMC, ajoutez le composant logiciel enfichable **certificats** et sélectionnez magasin de certificats de l' **ordinateur local**.

2.  Ouvrez les certificats **personnels** pour l’ordinateur, puis ouvrez le certificat approvisionné pour App-V.

3.  Dans l’onglet **Détails** , faites défiler vers le bas jusqu’à l’empreinte numérique et copiez le hachage dans le volet Détails.

4.  Ouvrez l’éditeur du Registre et naviguez jusqu’à `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .

5.  Modifiez la `X509CertHash` valeur, collez le hachage de l’empreinte numérique dans le champ valeur et supprimez tous les espaces. Cliquez sur **OK** pour accepter la modification.

6.  Dans l’éditeur du Registre, accédez à `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .

7.  Créez une nouvelle valeur **DWORD** nommée «322», puis entrez la valeur décimale 322 ou la valeur hexadécimale 142.

8.  Redémarrez le service de diffusion en continu.

## Rubriques connexes


[Procédure pour configurer la sécurité post-installation de Management Server](how-to-configure-management-server-security-post-installation.md)

[Résolution des problèmes d'autorisation de certificat](troubleshooting-certificate-permission-issues.md)

 

 





