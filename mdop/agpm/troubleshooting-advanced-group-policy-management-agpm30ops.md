---
title: Résolution des problèmes de la Gestion avancée des stratégies de groupe
description: Résolution des problèmes de la Gestion avancée des stratégies de groupe
author: dansimp
ms.assetid: f7ece97c-e9f8-4b18-8c7a-a615c98d5c60
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4815378a17a7c083501cfd7772e62415ec285237
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808202"
---
# Résolution des problèmes de la Gestion avancée des stratégies de groupe


Cette section répertorie les problèmes courants que vous pouvez rencontrer lors de l’utilisation de la gestion de la stratégie de groupe avancée (AGPM) pour gérer les objets de stratégie de groupe (GPO). Pour diagnostiquer des problèmes qui ne sont pas répertoriés ici, il est possible que l’Administrateur AGPM (contrôle total) utilise la journalisation et le suivi. Pour plus d’informations, voir [configurer la journalisation et le suivi](configure-logging-and-tracing-agpm30ops.md).

**Remarque**  
-   Pour plus d’informations sur la restauration d’une version antérieure d’un objet de stratégie de groupe en cas de problème, voir [restaurer une version précédente d’un objet de stratégie de groupe](roll-back-to-a-previous-version-of-a-gpo-agpm30ops.md).

-   Pour plus d’informations sur la récupération d’un sinistre en restaurant l’archive complète à partir d’une sauvegarde, voir [restaurer l’archive à partir d’une sauvegarde](restore-the-archive-from-a-backup.md).

 

## Quels problèmes rencontrez-vous?


-   [Je ne peux pas accéder à une archive](#bkmk-access-an-archive)

-   [L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe](#bkmk-state-varies)

-   [Je ne parviens pas à modifier la connexion à un serveur AGPM](#bkmk-modify-archive-location)

-   [Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe](#bkmk-perform-task)

-   [Je ne peux pas utiliser un nom d’objet GPO particulier](#bkmk-use-particular-name)

-   [Je ne reçois pas de notifications par courrier électronique AGPM](#bkmk-email)

-   [Je ne peux pas utiliser le port 4600 pour le service AGPM](#bkmk-port)

-   [Le service AGPM ne démarre pas](#bkmk-not-start)

-   [Échec de l’installation de logiciels de stratégie de groupe](#bkmk-software-installation)

-   [Une erreur s’est produite lors de la restauration de l’archivage sur un nouveau serveur AGPM](#bkmk-error-on-restore)

### <a href="" id="bkmk-access-an-archive"></a>Je ne peux pas accéder à une archive

-   **Cause**: vous n’avez pas sélectionné le serveur et le port appropriés pour l’archive.

-   **Solution**:

    -   Si vous êtes un administrateur AGPM: voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm30ops.md).

    -   Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM. Voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-reviewer-agpm30ops.md).

-   **Raison**: le service AGPM n’est pas en cours d’exécution.

-   **Solution**:

    -   Si vous êtes un administrateur AGPM: démarrez le service AGPM. Pour plus d’informations, reportez-vous à [Démarrer et arrêter le service AGPM](start-and-stop-the-agpm-service-agpm30ops.md).

    -   Si vous n’êtes pas un administrateur AGPM: contactez un administrateur AGPM pour obtenir de l’aide.

### <a href="" id="bkmk-state-varies"></a>L’état de l’objet de stratégie de groupe varie selon les administrateurs de stratégie de groupe

-   **Raison**: d’autres administrateurs de stratégie de groupe ont sélectionné différents serveurs AGPM pour la même archive.

-   **Solution**:

    -   Si vous êtes un administrateur AGPM: voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm30ops.md).

    -   Si vous n’êtes pas un administrateur AGPM: Demandez les détails de connexion du serveur AGPM auprès d’un administrateur AGPM. Voir [configurer une connexion de serveur AGPM](configure-an-agpm-server-connection-reviewer-agpm30ops.md).

### <a href="" id="bkmk-modify-archive-location"></a>Je ne parviens pas à modifier la connexion à un serveur AGPM

-   **Raison**: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, le serveur AGPM a été configuré de manière centralisée à l’aide d’un modèle d’administration.

-   **Solution**:

    -   Si vous êtes un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, voir [configurer les connexions au serveur AGPM](configure-agpm-server-connections-agpm30ops.md).

    -   Si vous n’êtes pas un administrateur AGPM: si les paramètres sous l’onglet **serveur AGPM** ne sont pas disponibles, vous n’êtes pas obligé de modifier le serveur AGPM.

### <a href="" id="bkmk-perform-task"></a>Je ne parviens pas à changer le modèle par défaut ou à afficher, créer, modifier, renommer, déployer ou supprimer des objets de stratégie de groupe

-   **Cause**: vous n’avez pas reçu de rôle avec les autorisations requises pour effectuer les tâches ou tâches.

-   **Solution**:

    -   Si vous êtes un administrateur d’AGPM: voir [déléguer l’accès au niveau du domaine à l’archive et l'](delegate-domain-level-access-to-the-archive-agpm30ops.md) [accès délégué à un objet GPO individuel dans l’archive](delegate-access-to-an-individual-gpo-in-the-archive-agpm30ops.md). Les autorisations AGPM seront mises en cascade à partir du domaine vers tous les objets de stratégie de groupe actuellement présents dans l’archive. Pour plus d’informations sur les rôles pouvant exécuter une tâche et les autorisations nécessaires à l’exécution d’une tâche, voir l’aide de cette tâche.

    -   Si vous n’êtes pas un administrateur AGPM et que vous avez besoin d’autorisations ou de rôles supplémentaires: contactez un administrateur AGPM pour obtenir de l’aide. Sachez que si vous êtes un éditeur, vous pouvez commencer le processus de création d’un objet de stratégie de groupe, de déploiement d’un objet de stratégie de groupe ou de suppression d’un objet de stratégie de groupe à partir de l’environnement de production, mais un approbateur ou un administrateur AGPM doit approuver votre demande.

### <a href="" id="bkmk-use-particular-name"></a>Je ne peux pas utiliser un nom d’objet GPO particulier

-   **Cause**: le nom de l’objet de stratégie de groupe est déjà utilisé ou vous ne disposez pas des autorisations nécessaires pour le répertorier.

-   **Solution**:

    -   Si le nom de l’objet de stratégie de groupe s’affiche sous l’onglet **contrôlé**, non **contrôlé**ou **en attente** , sélectionnez un autre nom. Si un objet de stratégie de groupe qui a été déployé est renommé mais qu’il n’a pas encore été redéployé, il sera affiché sous son ancien nom dans l’environnement de production. Par conséquent, l’ancien nom est toujours utilisé. Redéploiement de l’objet de stratégie de groupe pour mettre à jour son nom dans l’environnement de production et libérer ce nom pour une utilisation par un autre objet de stratégie de groupe.

    -   Si le nom de l’objet GPO n’apparaît pas dans l’onglet **contrôlé**, non **contrôlé**ou **en attente** , il est possible que vous ne disposiez pas des autorisations nécessaires pour afficher l’objet GPO. Pour demander une autorisation, contactez un administrateur AGPM.

### <a href="" id="bkmk-email"></a>Je ne reçois pas de notifications par courrier électronique AGPM

-   **Raison**: un serveur de courrier électronique SMTP et une adresse de messagerie valides n’ont pas été fournis ou aucune action ne a été effectuée pour générer une notification par courrier électronique.

-   **Solution**:

    -   Si vous êtes un administrateur d’AGPM: pour les notifications par courrier électronique concernant les actions en attente envoyées par AGPM, un administrateur AGPM doit fournir un serveur de messagerie SMTP et des adresses de messagerie valides pour les approbateurs dans l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm30ops.md).

    -   Les notifications par courrier électronique sont générées uniquement lorsque l’éditeur, le réviseur ou un autre administrateur de stratégie de groupe qui ne dispose pas de l’autorisation nécessaire pour créer, déployer ou supprimer un objet GPO envoie une demande pour l’une de ces actions. Il n’y a aucune notification automatique d’approbation ou de rejet d’une demande.

### <a href="" id="bkmk-port"></a>Je ne peux pas utiliser le port 4600 pour le service AGPM

-   **Raison**: par défaut, le port sur lequel le service AGPM écoute est le port 4600.

-   **Solution**: si le port 4600 n’est pas disponible pour le service AGPM, modifiez la configuration de port sur le serveur AGPM pour utiliser un autre port, puis mettez à jour le port dans la connexion de serveur AGPM pour les clients AGPM. Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm30ops.md).

### <a href="" id="bkmk-not-start"></a>Le service AGPM ne démarre pas

-   **Raison**: vous avez modifié les paramètres du service AGPM dans le système d’exploitation sous outils et **services** **d’administration** .

-   **Solution**: modifiez les paramètres de la **gestion de stratégie de groupe avancée Microsoft-serveur** sous **programmes et fonctionnalités** dans le panneau de configuration. Pour plus d’informations, voir [modifier le service AGPM](modify-the-agpm-service-agpm30ops.md).

### <a href="" id="bkmk-software-installation"></a>Échec de l’installation de logiciels de stratégie de groupe

-   **Raison**: AGPM conserve l’intégrité des packages d’installation de logiciels de stratégie de groupe. Bien que les objets de stratégie de groupe soient modifiés hors connexion, les liens entre les packages en plus des informations client mises en cache sont conservés. Cela est normal.

-   **Solution**: lorsque vous modifiez un objet de stratégie de groupe hors connexion avec AGPM, configurez la mise à niveau de l’installation de logiciels de stratégie de groupe d’un package dans un autre objet de stratégie de groupe pour référencer l’objet de stratégie de groupe déployé et non la copie L’éditeur doit disposer d’une autorisation de **lecture** pour l’objet GPO déployé.

### <a href="" id="bkmk-error-on-restore"></a>Une erreur s’est produite lors de la restauration de l’archivage sur un nouveau serveur AGPM

-   **Raison**: pour des raisons de sécurité, le chiffrement qui protège le mot de passe entré sous l’onglet **délégation de domaine** entraîne l’échec du mot de passe si l’archive est déplacée vers un autre ordinateur.

-   **Solution**: entrez à nouveau et confirmez le mot de passe dans l’onglet **délégation de domaine** . Pour plus d’informations, voir [configurer une notification par courrier électronique](configure-e-mail-notification-agpm30ops.md).

 

 





