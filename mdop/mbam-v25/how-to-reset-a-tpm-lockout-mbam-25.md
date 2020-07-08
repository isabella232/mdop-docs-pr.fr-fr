---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: dd20a728-c52e-48e6-9f6c-1311c71dee74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f5aea277e80c54fb01d1a6c00b62f0c617d1ad12
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809887"
---
# Réinitialisation d'un verrouillage TPM


Cette rubrique explique comment utiliser le site Web d’administration et de contrôle (également appelé support technique) pour réinitialiser un verrouillage du TPM. Les verrouillages de TPM peuvent se produire si un utilisateur final entre trop de fois le code confidentiel incorrect. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.

À partir de la zone **gérer le module de plateforme sécurisée** du site Web d’administration et de surveillance, vous pouvez accéder au système de données de récupération de clés centralisées, qui fournit un fichier de mot de passe de propriétaire du TPM lorsque vous fournissez un ID d’ordinateur et un identificateur d’utilisateur associé.

Pour accéder à la zone gérer le module de plateforme sécurisée du site Web d’administration et de surveillance, vous devez disposer du rôle utilisateurs du support technique MBAM ou du rôle utilisateurs avancés du support technique MBAM. Ces rôles sont des groupes que les administrateurs créent dans Active Directory. Vous pouvez utiliser n’importe quel nom pour ces groupes. Pour plus d’informations, reportez-vous [à planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md#bkmk-helpdesk-roles).

Pour plus d’informations sur la propriété MBAM et TPM, voir [considérations relatives à la sécurité dans MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

**Pour réinitialiser un verrouillage du TPM**

1.  Ouvrez un navigateur Web, puis accédez au **site Web d’administration et de surveillance**.

2.  Dans le volet gauche, cliquez sur **gérer le TPM** pour ouvrir la page gérer le module de **plateforme sécurisée** .

3.  Entrez le nom de domaine complet de l’ordinateur et le nom de l’ordinateur.

4.  Entrez le nom d’utilisateur et le domaine d’ouverture de session Windows de l’utilisateur final pour récupérer le fichier de mots de passe du propriétaire du TPM.

    **Remarques**  Si vous vous trouvez dans le groupe utilisateurs du support technique avancé MBAM, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.

     

5.  Dans la liste des **fichiers de mots de passe du propriétaire du module de plateforme sécurisée** , sélectionnez une raison pour la demande, puis cliquez sur **valider**.

    MBAM renvoie l’une des valeurs suivantes:

    -   Message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant

    -   Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis

    Après l’extraction du mot de passe du propriétaire du TPM, le mot de passe propriétaire est affiché.

6.  Pour enregistrer le mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .

7.  Dans la zone **gérer le module de plateforme sécurisée** du **site Web d’administration et de surveillance**, sélectionnez l’option **réinitialisation du verrouillage du TPM** et indiquez le fichier de mot de passe du propriétaire du TPM.

    Le verrouillage du TPM est réinitialisé et l’accès de l’utilisateur final est restauré.

    **Important**  Ne donnez pas à la valeur de hachage du TPM ou au fichier de mot de passe du propriétaire du TPM les utilisateurs finaux. Les informations sur le TPM ne changent pas, ce qui donne aux utilisateurs finaux des risques en matière de sécurité.

     



## Rubriques connexes


[Gestion de BitLocker avec MBAM2.5](performing-bitlocker-management-with-mbam-25.md)

 

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam). 





