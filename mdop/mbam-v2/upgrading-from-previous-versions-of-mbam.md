---
title: Mise à niveau des versions précédentes de MBAM
description: Mise à niveau des versions précédentes de MBAM
author: dansimp
ms.assetid: 73b425cf-9cd9-4ebc-a35e-1b3bf18596ce
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: af45d193a5e8001288e70389ff220cb5d8269918
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810176"
---
# Mise à niveau des versions précédentes de MBAM


Vous pouvez mettre à niveau l’administration et la surveillance de Microsoft BitLocker (MBAM) vers MBAM 2.0, avec la topologie autonome ou la topologie de Configuration Manager, en procédant comme suit:

-   **Remplacement manuel du serveur sur place** : pour mettre à niveau le serveur MBAM, désinstallez MBAM manuellement à l’aide du programme d’installation ou du panneau de configuration, puis installez l’infrastructure MBAM 2.0. Vous n’avez pas besoin de supprimer les bases de données. La désinstallation du serveur MBAM 1,0 quitte les bases de données MBAM intactes. Si vous spécifiez les mêmes bases de données que MBAM 1,0, l’installation de MBAM 2.0 conserve les données 1,0 MBAM dans les bases de données et convertit les bases de données pour qu’elles fonctionnent avec MBAM 2.0.

-   **Mise à niveau du client distribué** : Si vous utilisez la topologie MBAM autonome, vous pouvez mettre à niveau les clients MBAM progressivement après l’installation de l’infrastructure du serveur MBAM 2,0. Le serveur MBAM 2,0 détecte la version du client existant et effectue les étapes requises pour effectuer une mise à niveau vers le client 2,0.

    Après avoir effectué la mise à niveau de l’infrastructure du serveur MBAM 2,0, les clients MBAM 1,0 continuent de signaler au serveur MBAM 2,0 les données de récupération par confiance, mais la conformité sera basée sur les stratégies de MBAM 1,0. Vous devez mettre à niveau des clients vers MBAM 2,0 pour que les ordinateurs clients signalent de manière précise la conformité par rapport aux stratégies 2,0 MBAM. Vous pouvez mettre à niveau les clients vers le client MBAM 2,0 sans désinstaller le client précédent, et le client doit commencer à appliquer et à signaler les stratégies 2,0 MBAM.

    Si vous utilisez MBAM avec Configuration Manager, vous devez mettre à niveau les clients 1,0 MBAM vers MBAM 2,0.

## Mise à niveau de MBAM à partir d’une architecture à deux serveurs


Utilisez les instructions suivantes pour effectuer une mise à niveau à partir d’une version précédente de MBAM lorsque vous utilisez une architecture à deux serveurs, où un serveur héberge les composants Microsoft SQL Server, et l’autre serveur héberge les services et sites Web.

**Pour mettre à niveau MBAM à partir d’une architecture à deux serveurs**

1.  Sur le serveur avec les fonctionnalités de SQL Server, dans le panneau de configuration, sélectionnez **programmes et fonctionnalités**, puis désinstallez l' **administration et la surveillance de Microsoft BitLocker**. La base de données de récupération et la base de données d’audit et de conformité restent inchangées.

2.  Exécutez **MBAMSetup.exe** pour la version MBAM 2,0, si vous le souhaitez, sélectionnez le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie d’intégration **autonome** ou **System Center Configuration Manager** , puis cliquez sur **suivant**.

5.  Dans la page **Sélectionner les fonctionnalités à installer** , décochez la case **serveur libre-service** et fonctionnalités du **serveur d’administration** et de surveillance, puis cliquez sur **suivant**.

6.  Attendez la fin de la vérification préalable, puis cliquez sur **suivant**. Si une prérequis manquante est détecté, résolvez les conditions préalables manquantes, puis cliquez **à nouveau sur vérifier les conditions préalables**.

7.  Sur la page **fournir le compte utilisé pour accéder à la base de données MBAM** , indiquez le nom de l’ordinateur qui hébergera les sites et services, puis cliquez sur **suivant**.

8.  Sur la page **configurer la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de récupération. Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et les informations de journalisation.

9.  Cliquez sur **Suivant** pour poursuivre.

10. Sur la page **configurer la conformité et la base de données d’audit** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stockera les données de conformité et d’audit.

11. Cliquez sur **Suivant** pour poursuivre.

12. Sur la page **configurer les rapports de conformité et d’audit** , spécifiez l’instance de SQL Server Reporting Services dans laquelle les rapports de conformité et d’audit seront installés, puis fournissez un compte d’utilisateur et un mot de passe de domaine pour accéder à la base de données d’audit et de conformité. Configurez le mot de passe de ce compte pour qu’il n’expire jamais. Le compte d’utilisateur peut accéder à toutes les données disponibles dans le groupe utilisateurs de reports MBAM.

13. Cliquez sur **Suivant** pour poursuivre.

14. Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**. Les mises à jour automatiques ne sont pas activées dans Windows. Si vous avez précédemment choisi d’utiliser Microsoft Update pour ce produit ou un autre produit, la page Microsoft Update ne s’affiche pas.

15. Dans la page Résumé de l' **installation** , passez en revue les fonctionnalités qui seront installées, puis cliquez sur **installer** pour démarrer l’installation.

**Pour désinstaller les fonctionnalités d’administration et de surveillance du serveur et procéder à la mise à niveau**

1.  Sur l’ordinateur qui héberge les fonctionnalités d’administration et de surveillance du serveur, dans le panneau de configuration, sélectionnez **programmes et fonctionnalités**, puis désinstallez MBAM pour supprimer les services et sites Web déjà installés.

2.  Exécutez le **MBAMSetup.exe** pour la version 2,0, sélectionnez éventuellement le **programme d’amélioration**du produit, puis cliquez sur **Démarrer**.

3.  Lisez et acceptez le contrat de licence logiciel Microsoft, puis cliquez sur **suivant** pour continuer l’installation.

4.  Dans la page de sélection de la **topologie** , sélectionnez la topologie d’intégration **autonome** ou **System Center Configuration Manager** , puis cliquez sur **suivant**.

5.  Dans la **page Sélectionner les fonctionnalités à installer** , effacez les fonctionnalités de la **base de données de récupération** et **de la base de données d’audit et de** **conformité** et audit, puis cliquez sur **suivant**.

6.  Attendez la fin de la vérification préalable, puis cliquez sur **suivant**. Si une condition préalable manquante est détectée, vous devez d’abord résoudre les conditions préalables manquantes, puis cliquez sur **vérifier les conditions préalables**.

7.  Dans la page **configurer la sécurité du réseau** , choisissez si vous souhaitez utiliser le chiffrement SSL (Secure Socket Layer) pour les services et sites Web. Si vous décidez de chiffrer la communication, sélectionnez le certificat d’autorité de certification à utiliser pour le chiffrement.

    **Remarques**  Le certificat doit être créé avant cette étape pour vous permettre de le sélectionner dans cette page.

     

8.  Dans la page **configurer l’emplacement de la base de données d’état de conformité** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stocke les données de conformité et d’audit. Vous devez également spécifier l’emplacement où se trouvent les fichiers de base de données et les informations de journalisation.

9.  Cliquez sur **Suivant** pour poursuivre.

10. Dans la page **configurez l’emplacement de la base de données de récupération** , spécifiez le nom de l’instance SQL Server et le nom de la base de données qui stocke les données de récupération.

11. Cliquez sur **Suivant** pour poursuivre.

12. Dans la page **configurer les rapports de conformité et d’audit** , entrez l’URL de l’instance de rapport que vous avez configurée sur l’autre serveur. Utilisez le bouton **tester** pour vérifier que vous pouvez accéder au site.

13. Cliquez sur **Suivant** pour poursuivre.

14. Dans la page **configurer le portail libre-service** , entrez le numéro de port, le nom d’hôte, le nom du répertoire virtuel et le chemin d’installation du portail libre-service.

    **Remarques**  Le numéro de port que vous spécifiez doit être un numéro de port inutilisé sur le serveur d’administration et de surveillance sauf si vous spécifiez un nom d’en-tête d’hôte unique.

     

15. Sur la page **configurer le serveur d’administration et de surveillance** , spécifiez le répertoire virtuel souhaité pour le site Web du support technique.

16. Indiquez si vous souhaitez utiliser les mises à jour de Microsoft pour renforcer la sécurité de votre ordinateur, puis cliquez sur **suivant**. Cette étape n’active pas les mises à jour automatiques dans Windows. Si vous avez précédemment choisi d’utiliser Microsoft Update pour ce produit ou un autre produit, la page Microsoft Update ne s’affiche pas.

17. Dans la page Résumé de l' **installation** , passez en revue les fonctionnalités qui seront installées, puis cliquez sur **installer** pour démarrer l’installation.

18. Pour vérifier que la mise à niveau a réussi, vérifiez que vous pouvez joindre chaque site à partir d’un autre ordinateur du domaine.

## Mise à niveau du client MBAM sur les ordinateurs des utilisateurs finaux


Pour mettre à niveau les ordinateurs des utilisateurs finaux vers le client MBAM 2,0, exécutez **MbamClientSetup.exe** sur chaque ordinateur client. Le programme d’installation met automatiquement à jour le client vers le client MBAM 2,0. Vous pouvez installer le client MBAM via un système de distribution de logiciels électronique, des outils tels que les services de domaine Active Directory ou System Center Configuration Manager.

Pour valider la mise à niveau du client, procédez comme suit:

1.  Attendez la fin du cycle de création de rapports configuré, puis démarrez **SQL Server Management Studio** sur l’ordinateur SQL Server.

2.  Sur l’ordinateur SQL Server, démarrez **SQL Server Management Studio**.

3.  Vérifiez que la table **RecoveryAndHardwareCore. machines** contient une ligne montrant le nom de l’ordinateur de l’utilisateur final.

## Rubriques connexes


[Déploiement de MBAM2.0](deploying-mbam-20-mbam-2.md)

 

 





