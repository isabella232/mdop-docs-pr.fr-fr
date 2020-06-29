---
title: Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion
description: Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion
author: dansimp
ms.assetid: a4d078aa-ec54-4fa4-9463-bfb3b971d724
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 63ec965519bedef08b09c961dc5d1c90e1d8d694
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806048"
---
# Administration d'applications virtuelles App-V5.1 à l'aide de la console de gestion


Le serveur de gestion 5,1 de Microsoft Application Virtualization (App-V) vous permet de gérer les packages, groupes de connexion et accès aux packages dans votre environnement. Le serveur publie des icônes d’application, des raccourcis et des associations de types de fichiers sur des ordinateurs autorisés qui exécutent le client App-V 5,1. Un ou plusieurs serveurs de gestion partagent généralement un magasin de données commun pour la configuration et les informations de package.

Le serveur de gestion utilise les groupes AD DS (Active Directory Domain Services) pour gérer les autorisations de l’utilisateur et SQL Server doit être installé pour gérer la base de données et le magasin de données.

Étant donné que les serveurs de gestion diffusent les applications aux utilisateurs finaux à la demande, ces serveurs sont idéalement adaptés aux configurations système qui disposent de réseaux locaux fiables et à bande passante élevée. Le serveur de gestion comprend les composants suivants:

-   Serveur de gestion: utilisez le serveur de gestion pour gérer des packages et des groupes de connexion.

-   Serveur de publication: utilisez le serveur de publication pour déployer des packages sur des ordinateurs qui exécutent le client App-V 5,1.

-   Base de données de gestion: utilisez la base de données de gestion pour gérer l’accès au package et publier la synchronisation du serveur avec le serveur de gestion.

## Tâches de la console de gestion


Les tâches les plus courantes que vous pouvez effectuer avec la console de gestion de l’application-V 5,1 sont les suivantes:

-   [Comment se connecter à la console de gestion](how-to-connect-to-the-management-console-51.md)

-   [Comment ajouter ou mettre à jour des packages à l’aide de la console de gestion](how-to-add-or-upgrade-packages-by-using-the-management-console-51-gb18030.md)

-   [Comment configurer l’accès aux packages à l’aide de la console de gestion](how-to-configure-access-to-packages-by-using-the-management-console-51.md)

-   [Comment publier un package à l’aide de la console de gestion](how-to-publish-a-package-by-using-the-management-console-51.md)

-   [Comment supprimer un package dans la console de gestion](how-to-delete-a-package-in-the-management-console-51.md)

-   [Comment ajouter ou supprimer un administrateur à l’aide de la console de gestion](how-to-add-or-remove-an-administrator-by-using-the-management-console51.md)

-   [Comment inscrire et désinscrire un serveur de publication à l’aide de la console de gestion](how-to-register-and-unregister-a-publishing-server-by-using-the-management-console51.md)

-   [Comment créer un fichier de configuration personnalisé à l'aide de la console de gestion App-V5.1](how-to-create-a-custom-configuration-file-by-using-the-app-v-51-management-console.md)

-   [Comment transférer l'accès et les configurations vers une autre version d'un package à l'aide de la console de gestion](how-to-transfer-access-and-configurations-to-another-version-of-a-package-by-using-the-management-console51.md)

-   [Comment personnaliser les extensions d’applications virtuelles d’un groupe AD spécifique à l’aide de la console de gestion](how-to-customize-virtual-applications-extensions-for-a-specific-ad-group-by-using-the-management-console51.md)

-   [Comment afficher et configurer des applications et des extensions de l’application virtuelle par défaut à l’aide de la console de gestion](how-to-view-and-configure-applications-and-default-virtual-application-extensions-by-using-the-management-console-beta.md)

Les principaux éléments de la console de gestion de l’application-V 5,1 sont les suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Onglet de la console de gestion</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Onglet packages</p></td>
<td align="left"><p>Utilisez l' <strong> </strong> onglet packages pour ajouter ou mettre à niveau des packages.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Onglet groupes de connexion</p></td>
<td align="left"><p>Utilisez l' <strong> onglet groupes </strong> de connexions pour gérer les groupes de connexion.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Onglet serveurs</p></td>
<td align="left"><p>Utilisez l' <strong> </strong> onglet serveurs pour inscrire un nouveau serveur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Onglet administrateurs</p></td>
<td align="left"><p>Utilisez l' <strong> </strong> onglet administrateurs pour inscrire, ajouter ou supprimer des administrateurs dans votre environnement App-V 5,1.</p></td>
</tr>
</tbody>
</table>

 

**Important**  JavaScript doit être activé dans le navigateur qui ouvre la console de gestion Web.

 






## <a href="" id="other-resources-for-this-app-v-5-1-deployment-"></a>Autres ressources pour le déploiement de 5,1 App-V


-   [Guide de l’administrateur de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Opérations d'App-V5.1](operations-for-app-v-51.md)

 

 





