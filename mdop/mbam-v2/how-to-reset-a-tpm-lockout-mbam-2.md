---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: 20719ab2-18ae-4d3b-989a-539341909816
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 6453473ec09c2033346c7e464c08dbfdfe046d47
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810925"
---
# Réinitialisation d'un verrouillage TPM


La fonctionnalité de récupération de lecteur chiffrée de l’administration et de la surveillance de BitLocker (MBAM) englobe la capture et le stockage des données ainsi que la disponibilité des outils nécessaires pour gérer le module de plateforme sécurisée (TPM). Cette rubrique décrit comment accéder au système de données de récupération de clés centralisées dans le site Web d’administration et de surveillance, qui peut fournir un fichier de mots de passe de propriétaire du TPM lorsqu’un ID d’ordinateur et un identificateur d’utilisateur associé sont fournis.

Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que les verrouillages du TPM ne varient d’un fabricant au fabricant.

Vous pouvez réinitialiser un verrouillage du TPM uniquement si MBAM possède le module de plateforme sécurisée.

**Pour réinitialiser un verrouillage du TPM**

1.  Ouvrez un navigateur Web, puis accédez au site Web d’administration et de surveillance.

2.  Dans le volet de navigation gauche, sélectionnez **gérer le TPM** pour ouvrir la page gérer le module de **plateforme sécurisée** .

3.  Entrez le nom de domaine complet de l’ordinateur et le nom de l’ordinateur, puis entrez le domaine de connexion Windows de l’utilisateur et le nom d’utilisateur de l’utilisateur pour récupérer le fichier de mot de passe du propriétaire du module de plateforme sécurisée.

4.  Dans la liste des **fichiers de mots de passe du propriétaire du module de plateforme sécurisée** , sélectionnez une raison pour la demande, puis cliquez sur **valider**.

    MBAM renvoie l’une des valeurs suivantes:

    -   Un message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant

    -   Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis

    **Remarque**  
    Si vous êtes un utilisateur expérimenté du support technique, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.



~~~
After the TPM owner password is retrieved, the owner password is displayed.
~~~

5. Pour enregistrer le mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .

   L’utilisateur exécutera la console de gestion du module de plateforme sécurisée, sélectionner l’option de **réinitialisation du verrouillage du TPM** et fournir le fichier de mot de passe du propriétaire du TPM pour réinitialiser le verrouillage du TPM.

   **Important**  
   Les administrateurs du support technique ne doivent pas donner à la valeur de hachage du TPM ou au fichier de mot de passe du propriétaire du TPM les utilisateurs finaux. Les informations sur le TPM ne changent pas, ce qui peut entraîner un risque de sécurité si le fichier est fourni aux utilisateurs finaux.



## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam-mbam-2.md)









