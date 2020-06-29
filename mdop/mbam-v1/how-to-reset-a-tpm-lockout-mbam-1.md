---
title: Réinitialisation d'un verrouillage TPM
description: Réinitialisation d'un verrouillage TPM
author: dansimp
ms.assetid: 91ec6666-1ae2-4e76-9459-ad65c405f639
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: dde77a12e97d050777dac15d4106124ec111b3cd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804590"
---
# Réinitialisation d'un verrouillage TPM


La fonctionnalité de récupération de lecteur chiffrée de l’administration et de la surveillance de BitLocker (MBAM) englobe la capture et le stockage des données et la disponibilité des outils requis pour gérer le module de plateforme sécurisée (TPM). Cette rubrique traite de l’accès au système de données de récupération de clés centralisées dans le site Web d’administration des bits \ _admmon \ _tlanextref. Le système de données de récupération de clé peut fournir un fichier de mot de passe propriétaire du TPM lorsque l’identité de l’ordinateur et l’identificateur d’utilisateur associé sont fournis.

Un verrouillage du TPM peut se produire si un utilisateur entre un code confidentiel incorrect trop souvent. Le nombre de fois qu’un utilisateur peut entrer un code confidentiel incorrect avant que le verrouillage du TPM ne repose sur les spécifications du fabricant de l’ordinateur.

**Pour réinitialiser un verrouillage du TPM**

1.  Ouvrez le site Web d’administration MBAM.

2.  Dans le volet de navigation, sélectionnez **gérer le module de plateforme sécurisée**. Cette opération ouvre la page **gérer le module de plateforme sécurisée** .

3.  Entrez le nom de domaine complet (FQDN) de l’ordinateur et le nom de l’ordinateur. Entrez le domaine de connexion Windows de l’utilisateur et le nom d’utilisateur de l’utilisateur. Sélectionnez l’une des options prédéfinies dans la zone de liste déroulante **raison du demande de mot de passe de propriétaire du TPM** . Cliquez sur **Envoyer**.

4.  MBAM renverra l’une des valeurs suivantes:

    -   Message d’erreur s’il n’existe aucun fichier de mot de passe de propriétaire de TPM correspondant

    -   Fichier de mot de passe du propriétaire du TPM de l’ordinateur soumis

    **Remarques**  Si vous êtes un utilisateur expérimenté du support technique, les champs utilisateur et ID d’utilisateur ne sont pas obligatoires.

     

5.  Lorsque vous récupérez le mot de passe propriétaire, le mot de passe est affiché. Pour enregistrer ce mot de passe dans un fichier. TPM, cliquez sur le bouton **Enregistrer** .

6.  L’utilisateur doit exécuter la console de gestion du TPM et sélectionner l’option de **réinitialisation du verrouillage du TPM** et fournir le fichier de mot de passe du propriétaire du TPM pour réinitialiser le verrouillage du TPM.

## Rubriques connexes


[Gestion de BitLocker avec MBAM](performing-bitlocker-management-with-mbam.md)

 

 





