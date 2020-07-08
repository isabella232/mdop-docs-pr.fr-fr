---
title: Procédure pour configurer la sécurité post-installation de Management Server
description: Procédure pour configurer la sécurité post-installation de Management Server
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807306"
---
# Procédure pour configurer la sécurité post-installation de Management Server


Utilisez la console de gestion App-V pour ajouter le certificat et configurer le serveur de gestion App-V pour une sécurité renforcée. Vous pouvez utiliser la procédure suivante pour configurer la sécurité après l’installation.

**Pour configurer la sécurité du serveur de gestion après l’installation**

1.  Ouvrez la console de gestion App-V, puis connectez-vous au **service de gestion** avec les privilèges d’administrateur d’application-v.

2.  Développez le serveur, développez **groupes de serveurs**, puis sélectionnez le groupe de serveurs approprié avec lequel le serveur de gestion a été enregistré.

3.  Cliquez avec le bouton droit sur l’objet serveur de gestion, puis sélectionnez **Propriétés**.

4.  Dans l’onglet **ports** , cliquez sur **certificat de serveur** , puis terminez l’Assistant pour sélectionner le certificat configuré correctement.

    **Remarques**  Si aucun certificat n’est affiché dans l’Assistant, un certificat n’a pas été approvisionné ou le certificat répond aux exigences de App-V.

     

5.  Cliquez sur **suivant** pour passer à la page de l' **Assistant Bienvenue** sur le certificat.

6.  Sélectionnez le certificat approprié dans l’écran **certificats disponibles** .

7.  Cliquez sur **Terminer**.

8.  Une fois l’Assistant terminé, effacez **RTSP** comme port d’écoute disponible. Cela empêche les connexions d’être effectuées via un canal de communication non sécurisé.

9.  Cliquez sur **appliquer**, puis redémarrez le service **serveur d’applications virtuelles Microsoft** . Pour effectuer cette tâche, utilisez le composant logiciel enfichable MMC du service.

## Rubriques connexes


[Procédure pour configurer la sécurité post-installation de Streaming Server](how-to-configure-streaming-server-security-post-installation.md)

[Résolution des problèmes d'autorisation de certificat](troubleshooting-certificate-permission-issues.md)

 

 





