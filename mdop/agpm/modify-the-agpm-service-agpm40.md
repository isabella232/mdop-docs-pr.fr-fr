---
title: Modifier le service AGPM
description: Modifier le service AGPM
author: dansimp
ms.assetid: 3239d088-bb86-4ec4-bc56-dbe8f1c710f5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: be39b170ef4cdc14c0f447bb6bd09a4ea92c82fe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808330"
---
# Modifier le service AGPM


Le service AGPM est un service Windows agissant en tant que proxy de sécurité, gérant l’accès client aux objets de stratégie de groupe (GPO) dans l’environnement d’archivage et de production du domaine. Si ce service est arrêté ou désactivé, les clients AGPM ne peuvent pas effectuer d’opérations via le serveur. Vous pouvez modifier le chemin d’archive, le compte de service AGPM et le port sur lequel le service AGPM écoute.

**Attention**  Ne modifiez pas les paramètres du service AGPM via les outils et **services** **d’administration** du système d’exploitation. Cela peut empêcher le démarrage du service AGPM.

 

Un compte d’utilisateur membre du groupe administrateurs de domaine et ayant accès au serveur AGPM (l’ordinateur sur lequel est installé le serveur de gestion de la stratégie de groupe Microsoft Advanced) est requis pour effectuer cette procédure. Par ailleurs, vous devez fournir les informations d’identification du compte de service AGPM pour pouvoir exécuter cette procédure.

**Pour modifier le service AGPM**

1.  Sur l’ordinateur sur lequel est installé Microsoft Advanced Group Policy Management-Server, cliquez sur **Démarrer**, **panneau de configuration**, **programmes**et **programmes et fonctionnalités**.

2.  Cliquez avec le bouton droit sur **gestion de stratégie de groupe avancée Microsoft-serveur**, puis cliquez sur **modifier**.

3.  Cliquez sur **suivant**, puis sur **modifier**.

4.  Suivez les instructions pour configurer le service AGPM:

    1.  Dans la boîte de dialogue **path Archive** , entrez le nouvel emplacement de l’archivage relatif au serveur AGPM ou confirmez le chemin d’accès actuel de l’archivage, puis cliquez sur **suivant**.

        **Important**  Le chemin d’accès d’archive peut pointer vers un dossier sur le serveur AGPM ou un autre emplacement, mais l’espace disponible doit être suffisant pour stocker tous les objets de stratégie de groupe et les données d’historique gérés par ce serveur AGPM.

         

    2.  Dans la boîte de dialogue **compte de service AGPM** , entrez les informations d’identification d’un compte de service sous lequel le service AGPM sera exécuté, puis cliquez sur **suivant**.

        **Important**  La modification de l’installation efface les informations d’identification du compte de service AGPM. Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.

        Le compte de service AGPM doit disposer d’un accès complet aux objets de stratégie de groupe qu’il doit gérer et bénéficier d’une autorisation **de connexion en tant que service** . S’il s’agit de gérer les objets de stratégie de groupe sur un domaine unique, vous pouvez créer le compte système local pour le contrôleur de domaine principal du compte de service AGPM.

        S’il s’agit de gérer des objets de stratégie de groupe sur plusieurs domaines ou si un serveur membre sera le serveur AGPM, vous devez configurer un autre compte en tant que compte de service AGPM, car le compte système local d’un contrôleur de domaine ne peut pas accéder aux objets de stratégie de groupe sur d’autres domaines.

         

    3.  Dans la boîte de dialogue **Archiver le propriétaire** , entrez le nom d’utilisateur d’un administrateur AGPM (contrôle total) ou d’un groupe d’administrateurs AGPM, puis cliquez sur **suivant**.

        **Remarques**  La modification de l’installation efface les informations d’identification pour le propriétaire de l’archivage. Vous devez entrer de nouveau les informations d’identification, mais elles ne sont pas obligées de correspondre aux informations d’identification utilisées lors de l’installation d’origine.

         

    4.  Dans la boîte de dialogue **configuration du port** , tapez un nouveau port sur lequel le service AGPM écoute ou confirme le port actuellement sélectionné, puis cliquez sur **suivant**.

        **Remarques**  Par défaut, le service AGPM écoute sur le port 4600.

        Si vous configurez manuellement les exceptions de port ou que les règles configurent les exceptions de port, vous pouvez désactiver la case à cocher **Ajouter une exception de Port au pare-feu** .

         

5.  Cliquez sur **modifier**, et une fois l’installation terminée, cliquez sur **Terminer**.

6.  Si vous avez modifié le port sur lequel écoute le service AGPM, modifiez le port dans la connexion de serveur AGPM pour chaque administrateur de stratégie de groupe. (Pour plus d’informations, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm40.md).)

7.  Répétez cette opération pour chaque serveur AGPM sur lequel les modifications de configuration doivent être appliquées.

### Références supplémentaires

-   [Gestion du service AGPM](managing-the-agpm-service-agpm40.md)

 

 





