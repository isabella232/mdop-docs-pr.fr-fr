---
title: Comment configurer un utilisateur ou un groupe de domaine
description: Comment configurer un utilisateur ou un groupe de domaine
author: dansimp
ms.assetid: 055aba81-a9c9-4b98-969d-775e603becf3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c51da13808df657c1341572767c24860d9d5e8b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812210"
---
# Comment configurer un utilisateur ou un groupe de domaine


Les paramètres de déploiement vous permettent de contrôler les utilisateurs ou groupes qui peuvent accéder à l’espace de travail MED-V, ainsi que la durée de l’utilisation de l’espace de travail MED-V et la possibilité de les utiliser hors connexion. Vous pouvez également configurer des règles supplémentaires pour contrôler l’accès entre l’espace de travail MED-V et l’hôte.

Toutes les autorisations d’espace de travail MED-V sont configurées dans le module de **stratégie** sous l’onglet **déploiement** .

Pour permettre aux utilisateurs d’utiliser l’espace de travail MED-V, vous devez d’abord ajouter des utilisateurs ou groupes de domaine aux autorisations d’espace de travail MED-V. Vous pouvez ensuite définir des autorisations pour chaque utilisateur ou groupe.

## Comment ajouter un utilisateur ou un groupe de domaine


**Pour ajouter un utilisateur ou un groupe de domaine**

1.  Dans la fenêtre **utilisateurs et groupes** , cliquez sur **Ajouter.**

2.  Dans la boîte de dialogue **entrer un nom d’utilisateur ou de groupe** , sélectionnez utilisateurs ou groupes de domaines en effectuant l’une des opérations suivantes:

    -   Dans le champ **Entrez des noms d’utilisateur ou de groupe** , entrez un nom d’utilisateur ou de groupe qui existe dans le domaine ou en tant qu’utilisateur ou groupe local de l’ordinateur. Puis cliquez sur **vérifier les noms** pour le résoudre au nom existant complet.

    -   Cliquez sur **Rechercher** pour ouvrir la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** standard. Sélectionnez ensuite utilisateurs ou groupes de domaines.

3.  Cliquez sur **OK**.

    Les utilisateurs ou groupes du domaine sont ajoutés.

    **Remarque**  
    Les utilisateurs des domaines approuvés doivent être ajoutés manuellement.



~~~
**Warning**  
Do not run the management application from a computer that is part of a domain that is not trusted by the domain the server is installed on.
~~~



## Supprimer un utilisateur ou un groupe de domaine


**Pour supprimer un utilisateur ou un groupe de domaine**

1.  Dans la fenêtre **utilisateurs/groupes** , sélectionnez un utilisateur ou un groupe.

2.  Cliquez sur **supprimer**.

    L’utilisateur ou le groupe est supprimé.

## Définir des autorisations pour un utilisateur ou un groupe


**Pour définir des autorisations pour un utilisateur ou un groupe**

1.  Cliquez sur l’utilisateur ou le groupe pour lequel vous définissez les autorisations.

2.  Configurez les propriétés de l’espace de travail MED-V comme décrit dans le tableau suivant.

3.  Dans le menu **stratégie** , cliquez sur **valider**.

**Propriétés de déploiement d’espace de travail**

Description de propriété *générale*

Activer un espace de travail pour un &lt; utilisateur ou un groupe&gt;

Activez cette case à cocher pour activer l’espace de travail MED-V pour cet utilisateur ou groupe.

Espace de travail expire à cette date

Activez cette case à cocher pour affecter une date d’expiration aux autorisations définies pour cet utilisateur ou groupe.

Lorsque vous sélectionnez cette option, la zone de date est activée. Définissez la date et l’autorisation expire à la fin de la date spécifiée.

Le fonctionnement hors connexion est limité à

Activez cette case à cocher pour attribuer une période pendant laquelle la stratégie doit être actualisée pour cet utilisateur ou groupe. Lorsque cette case est cochée, la case période est activée. Définir le nombre de jours ou d’heures et à la fin de la période spécifiée, le groupe ou l’utilisateur ne peut pas se connecter si la stratégie n’est pas actualisée.

Options de suppression d’espace de travail

Cliquez pour définir les options de suppression d’espace de travail de MED-V. Pour plus d’informations, reportez-vous [à définition des options de suppression d’espace de travail MED-V](how-to-set-med-v-workspace-deletion-options.md).

*Transfert de données*

Support du presse-papiers entre l’hôte et l’espace de travail

Activez cette case à cocher pour autoriser les opérations de copie et de collage entre l’hôte et l’espace de travail MED-V.

Prise en charge du transfert de fichiers entre l’hôte et l’espace de travail

Activez cette case à cocher pour autoriser le transfert de fichiers entre les espaces de travail hôte et MED-V. Sélectionnez l’une des options suivantes dans la boîte de **transfert de fichiers** :

-   **Both**: permet de transférer des fichiers entre l’hôte et l’espace de travail MED-V.

-   **Hébergé sur un espace de travail**: permet de transférer des fichiers à partir de l’hôte vers l’espace de travail MED-V.

-   **Espace de travail à hôte**: permet de transférer des fichiers à partir de l’espace de travail MED-V vers l’hôte.

**Remarque**  
Si un utilisateur sans autorisation tente de transférer des fichiers, une fenêtre s’affiche et vous invite à entrer les informations d’identification d’un utilisateur disposant des autorisations pour effectuer le transfert de fichier.



**Important**  
Pour prendre en charge le transfert de fichiers dans Windows XP SP3, vous devez désactiver la synchronisation des fichiers hors connexion en modifiant le registre comme suit:

`REG ADD HKLM\software\microsoft\windows\currentversion\netcache /V Enabled /T REG_DWORD /F /D 0`



Avancé

Cliquez pour définir les options de transfert de fichier avancées. Pour plus d’informations, reportez-vous [à la rubrique définition des options de transfert de fichiers avancées](how-to-set-advanced-file-transfer-options.md).

*Contrôle de l’appareil*

Activer l’impression sur les imprimantes connectées à l’hôte

Activez cette case à cocher pour permettre aux utilisateurs d’imprimer à partir de l’espace de travail MED-V à l’aide de l’imprimante hôte.

**Remarque**  
L’impression est effectuée par les imprimantes définies sur l’hôte.



Activer l’accès au CD/DVD

Activez cette case à cocher pour autoriser l’accès à un CD ou un DVD à partir de cet espace de travail MED-V.



**Appartenances multiples**

1.  Si l’utilisateur fait partie d’un groupe et les autorisations sont appliquées à l’utilisateur ainsi qu’au groupe auquel il fait partie, toutes les autorisations sont appliquées.

2.  Si l’utilisateur est membre de deux groupes différents, les autorisations les moins restrictives sont appliquées.

## Rubriques connexes


[Utilisation de l'interface utilisateur de la console de gestion MED-V](using-the-med-v-management-console-user-interface.md)

[Création d'un espace de travail MED-V](creating-a-med-v-workspacemedv-10-sp1.md)

[Comment définir les options de suppression d'espace de travail MED-V](how-to-set-med-v-workspace-deletion-options.md)

[Comment définir les options de transfert de fichiers avancées](how-to-set-advanced-file-transfer-options.md)









