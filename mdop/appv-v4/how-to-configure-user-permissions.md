---
title: Procédure pour configurer les autorisations des utilisateurs
description: Procédure pour configurer les autorisations des utilisateurs
author: dansimp
ms.assetid: 54e69f46-b028-4ad1-9b80-f06ef5c8f559
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3c2581a9f9dddcbc63682d356c777a24222dd62f
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807225"
---
# Procédure pour configurer les autorisations des utilisateurs


Vous pouvez activer et désactiver certaines actions pour les utilisateurs ne disposant pas des droits d’administration en modifiant les valeurs clés sous la clé de Registre **autorisations** (HKEY \ _LOCAL \ _MACHINE \\software\\microsoft\\softgrid\\4.5\\client\\permissions). Cette clé est essentiellement conçue pour empêcher les utilisateurs de faire des erreurs plutôt que de fournir des informations de sécurité spéciales, car les utilisateurs disposant de droits d’administrateur peuvent modifier l’une de ces valeurs clé. Les procédures suivantes sont des exemples de modification des valeurs de clé. Pour plus d’informations sur les clés et les clés de Registre clientes sur la virtualisation des applications (App-V), voir <https://go.microsoft.com/fwlink/?LinkId=121528> .

**Pour modifier les autorisations des utilisateurs**

1.  Pour permettre aux utilisateurs de choisir d’exécuter le client en mode hors connexion, définissez la valeur clé suivante sur 1:

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ToggleOfflineMode

2.  Pour permettre aux utilisateurs d’afficher toutes les applications par le biais de l’interface utilisateur, définissez la valeur clé suivante sur 1. Si vous définissez la valeur sur 0 (zéro), les utilisateurs peuvent voir uniquement les applications qui leur sont proposées.

    HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\Client\\Permissions\\ViewAllApplications

## Rubriques connexes


[Procédure pour configurer les paramètres de registre du client App-V Client à l'aide de la ligne de commande](how-to-configure-the-app-v-client-registry-settings-by-using-the-command-line.md)

[Autorisations d'accès utilisateur dans Application Virtualization Client](user-access-permissions-in-application-virtualization-client.md)

 

 





