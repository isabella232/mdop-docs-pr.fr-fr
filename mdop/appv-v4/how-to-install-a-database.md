---
title: Procédure pour installer une base de données
description: Procédure pour installer une base de données
author: dansimp
ms.assetid: 52e3a19d-b7cf-4f2c-8268-0f8361cc9766
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c5f42673c08744d17e1d2e0ef955ebed2848de18
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807082"
---
# Procédure pour installer une base de données


Vous pouvez utiliser la procédure suivante pour installer une base de données pour le déploiement de la virtualisation de l’application sur serveur si une base de données n’est pas encore disponible. En règle générale, dans un environnement de production, vous devez vous connecter à une base de données existante.

**Important**  Pour installer la base de données, vous devez utiliser un compte réseau doté des autorisations appropriées. Si votre organisation exige que seuls les administrateurs de base de données soient autorisés à créer et à effectuer des mises à jour de la base de données, des scripts permettent d’effectuer cette tâche.

 

**Pour installer une base de données**

1.  Naviguez jusqu’à l’emplacement du programme d’installation du système de virtualisation des applications sur le réseau, exécutez ce programme à partir du réseau ou copiez son annuaire vers l’ordinateur cible, puis double-cliquez sur **Setup.exe**.

2.  Dans la **page Bienvenue**, cliquez sur **suivant**.

3.  Dans la page **contrat de licence** , pour accepter le contrat de licence, cliquez sur **J’accepte les termes du**contrat de licence, puis cliquez sur **suivant**.

4.  Dans la page **informations d’inscription** , spécifiez le nom d' **utilisateur** et les informations de l' **organisation** , puis cliquez sur **suivant**.

5.  Dans la page **type d’installation** , sélectionnez **personnalisé** , puis cliquez sur **suivant**.

6.  Dans la page **configuration personnalisée** , désélectionnez tous les composants du système de virtualisation des applications, à l’exception du **serveur de virtualisation des applications**, puis cliquez sur **suivant**.

    **Remarques**  Si un composant est déjà installé sur l’ordinateur, vous devez le désélectionner sur l’écran de **configuration personnalisé** pour le désinstaller automatiquement.

     

7.  Dans la page **serveur de base de données** , tapez les mots de passe, attribuez un chemin d’installation, enregistrez les informations, puis cliquez sur **suivant**.

8.  Sélectionnez un nom pour la base de données, puis cliquez sur **suivant**.

    **Remarques**  Si l’erreur 25109 s’affiche lorsque vous essayez d’effectuer cette étape, vous avez configuré incorrectement les autorisations nécessaires pour l’installation de la base de données. Pour plus d’informations sur la configuration des autorisations SQL nécessaires, voir <https://go.microsoft.com/fwlink/?LinkId=132144> .

     

9.  Dans l’écran **serveur d’annuaire** , entrez le nom de domaine et les informations d’identification que les serveurs de virtualisation des applications et le service Web de gestion doivent utiliser pour accéder à votre contrôleur de domaine, enregistrer ces informations, puis cliquez sur **suivant**.

    **Remarques**  L’installation est par défaut celle du domaine de l’ordinateur actuel.

     

10. Sur la page **groupe administrateur** , entrez le nom d’un groupe qui disposera des privilèges d’administrateur, enregistrez les informations, puis cliquez sur **suivant**.

    **Remarques**  Vous pouvez également entrer les premiers caractères du nom d’un groupe disposant de privilèges d’administration, cliquez sur **suivant**, puis, dans l’écran **Sélectionner un groupe d’administrateurs** , sélectionnez le groupe dans la liste résultante. Enregistrez ces informations, puis cliquez sur **suivant**.

     

11. Sur la page **groupe de fournisseurs par défaut** , entrez le nom complet d’un groupe qui contrôlera l’accès aux applications, enregistrez les informations, puis cliquez sur **suivant**.

    **Remarques**  Vous pouvez également entrer les premiers caractères du nom d’un groupe qui contrôleront l’accès aux applications, cliquez sur **suivant**, puis, dans l’écran **Sélectionner le groupe du fournisseur par défaut** , sélectionnez le groupe dans la liste. Enregistrez ces informations, puis cliquez sur **suivant**.

     

12. Dans la page terminé de l' **Assistant Installation** , cliquez sur **Terminer**pour fermer l’Assistant.

    **Important**  Le processus d’installation peut prendre quelques minutes. Un message de statut clignote au-dessus de la zone de notification du bureau Windows, indiquant si l’installation a réussi.

     

## Rubriques connexes


[Procédure pour installer les serveurs et les composants système](how-to-install-the-servers-and-system-components.md)

 

 





