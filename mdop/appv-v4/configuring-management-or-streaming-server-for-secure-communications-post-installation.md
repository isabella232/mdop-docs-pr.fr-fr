---
title: Configuration de Management ou Streaming Server pour sécuriser les communications post-installation
description: Configuration de Management ou Streaming Server pour sécuriser les communications post-installation
author: dansimp
ms.assetid: 1062a213-470b-4ae2-b12f-b3e28a6ab745
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 2a2713f130809c431b7444f3e928a523838597a6
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809018"
---
# Configuration de Management ou Streaming Server pour sécuriser les communications post-installation


Si le certificat approprié n’a pas été approvisionné avant l’installation du serveur de gestion des applications-V ou du serveur de streaming d’applications-V, l’application-V peut être configurée pour une sécurité renforcée après l’installation initiale. Vous pouvez configurer le serveur de gestion de l’application-V par le biais de la console de gestion App-V. Toutefois, le serveur de streaming App-V est géré par le biais du Registre. Dans les deux cas, le certificat doit inclure l' *utilisation de la clé étendue* (EKU) appropriée pour l’authentification du serveur et le service réseau doit avoir accès en lecture à la clé privée.

## Dans cette section


<a href="" id="how-to-configure-management-server-security-post-installation"></a>[Procédure pour configurer la sécurité post-installation de Management Server](how-to-configure-management-server-security-post-installation.md)  
Fournit une procédure qui peut être effectuée après l’installation, à l’aide de la console de gestion des applications pour ajouter le certificat et configurer le serveur de gestion App-V pour une sécurité renforcée.

<a href="" id="how-to-configure-streaming-server-security-post-installation"></a>[Procédure pour configurer la sécurité post-installation de Streaming Server](how-to-configure-streaming-server-security-post-installation.md)  
Fournit une procédure qui peut être effectuée après l’installation, ajouter le certificat et configurer le serveur de streaming App-V pour renforcer la sécurité.

<a href="" id="troubleshooting-certificate-permission-issues"></a>[Résolution des problèmes d'autorisation de certificat](troubleshooting-certificate-permission-issues.md)  
Fournit des conseils de dépannage pour le moment où la clé privée n’a pas été configurée à l’aide de la liste de contrôle d’accès appropriée pour le service réseau.

 

 





