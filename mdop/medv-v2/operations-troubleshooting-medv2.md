---
title: Résolution des problèmes d'opérations
description: Résolution des problèmes d'opérations
author: dansimp
ms.assetid: 948d7869-accd-44da-974f-93409234dee7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 126b5fae517c59914dcb7fb155ef4ad47278b5bd
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10804453"
---
# Résolution des problèmes d'opérations


Cette rubrique contient des informations que vous pouvez utiliser pour résoudre les problèmes de fonctionnement généraux dans Microsoft Enterprise Desktop Virtualization (MED-V) 2,0.

## Résoudre les problèmes liés aux opérations MED-V


Voici quelques problèmes rencontrés par les utilisateurs lorsqu’ils exécutent MED-V et des solutions pour vous aider à résoudre ces problèmes:

**Échec de la redirection de la documentation**. Ce problème se produit généralement lorsque le dossier Mes documents d’un utilisateur final pointe vers un emplacement réseau. Windows ne prend pas en charge la création d’un partage à partir d’un autre dossier partagé. Lorsqu’un lecteur ou un dossier est redirigé vers l’invité, RDP\\Windows Virtual PC crée un partage pour ce dossier. Par conséquent, si le dossier My documents sur l’hôte pointe déjà vers un partage, RDP\\Windows Virtual PC ne peut pas créer de partage d’un partage.

Ce problème peut également se produire lorsque les informations d’identification requises pour se connecter à la ressource réseau diffèrent des informations d’identification de domaine de l’utilisateur. MED-V est peut-être capable de détecter que des documents sont redirigés vers l’hôte, d’envoyer ces informations à l’invité, puis d’essayer de se reconnecter à la ressource réseau. Si les informations d’identification de l’utilisateur ne s’authentifient pas, MED-V peut ne plus essayer de s’authentifier.

**Solution**

Essayez l’une des solutions suivantes pour résoudre ce problème:

-   Définissez le répertoire racine de l’utilisateur dans Active Directory. L’invité et l’hôte doivent alors se connecter à la même ressource réseau.

-   Au lieu de rediriger le dossier Mes documents vers un chemin UNC, mappez-le à une lettre de lecteur (sur l’hôte, mappez un lecteur qui pointe vers la ressource du réseau). Le dossier Mes documents peut ensuite être configuré pour utiliser la lettre du lecteur à la place du chemin d’accès UNC. L’invité est alors redirigé vers ce même lecteur mappé comme prévu.

-   Créez un script de démarrage dans l’invité qui redirige le dossier Mes documents vers la ressource réseau et fournit des informations d’identification supplémentaires selon les besoins.

**Échec de la redirection d’URL**. Une URL que vous avez spécifiée pour la redirection de l’hôte vers l’invité n’est pas redirigée comme prévu ou renvoie un message d’erreur indiquant que le site Web n’existe pas.

**Solution**

Cette erreur peut se produire en cas d’utilisation incorrecte ou incorrecte de caractères (par exemple, astérisque (\ *), dans les informations de redirection d’URL. Vérifiez la valeur de registre de redirection d’URL et corrigez toutes les erreurs.

La clé de Registre est appelée `RedirectUrls` et se trouve généralement à l’adresse suivante:

Computer\\HKEY\ _LOCAL \ _MACHINE \\SOFTWARE\\Microsoft\\MEDV\\v2\\UserExperience

**Icône dans la barre des tâches**. Par défaut, l’icône qui s’affiche dans la barre des tâches de l’utilisateur final pour les applications publiées et l’URL redirigée est l’icône du PC virtuel Windows. Si un utilisateur final ne connaît pas ce comportement par défaut, il peut devenir confus lorsque vous examinez la barre des tâches pour localiser son application.

**Solution**

Le seul moyen d’éviter ce comportement par défaut consiste à modifier les paramètres d’utilisateur pour les propriétés de la barre des tâches comme suit:

1.  Cliquez avec le bouton droit sur la barre des tâches, puis cliquez sur **Propriétés**.

2.  Dans la boîte de dialogue Propriétés de la **barre des tâches et du menu Démarrer** , cliquez sur l’onglet **barre des tâches** .

3.  Dans le menu déroulant de la zone **des boutons de la barre des tâches** , sélectionnez **ne jamais combiner**.

4.  Cliquez sur **OK**.

Les icônes correspondant aux applications publiées et aux URL redirigées sont affichées.

**Avertissement émis si le second utilisateur tente de se connecter ou si une machine virtuelle est en cours d’utilisation**. Un message d’avertissement est émis lorsqu’un utilisateur se connecte à un espace de travail MED-V alors qu’il continue à exécuter MED-V. L’avertissement est également émis si MED-V est démarré alors que l’ordinateur virtuel est utilisé (par exemple, si l’ordinateur virtuel a été démarré via le PC virtuel Windows dans le menu **Démarrer** ). Lorsque l’utilisateur final accepte le message d’avertissement, MED-V s’arrête.

**Solution**

Un utilisateur final doit vérifier que tous les autres utilisateurs sont déconnectés de MED-V avant d’essayer de se connecter. Cela garantit qu’aucune autre instance de MED-V n’est en cours d’exécution et que le PC virtuel Windows n’est pas dans le contrôle de l’ordinateur virtuel.

Des **bips audibles lors de la première configuration**. Occasionnellement, des bips sont audibles lorsque MED-V est lancé pour la première fois. Cela peut prêter à confusion pour un utilisateur final. Les bips sont émises par l’ordinateur virtuel lorsqu’il effectue certaines actions, telles que l’arrêt.

**Solution**

Vous pouvez arrêter le service bip en spécifiant la commande "net stop BEEP" au début de chaque séquence de démarrage de la machine virtuelle. Vous pouvez ou désactiver le service bip en spécifiant la commande «sc config bips start = disabled». Vous pouvez spécifier ces commandes avant de sceller l’image ou dans le cadre de Sysprep.

**Connexions réseau multiples créées pour les espaces de travail MED-V en mode Bridged**. Si la première fois que vous créez un espace de travail MED-V configuré pour le mode NAT, il ne crée qu’une seule connexion réseau dans l’ordinateur virtuel Windows. Toutefois, si la première fois que vous créez un espace de travail MED-V configuré pour le mode pont, il crée une connexion réseau distincte pour chaque carte réseau installée sur l’ordinateur, car MED-V ne peut pas identifier la carte réseau active. Cela permet également de s’assurer que les utilisateurs mobiles disposent toujours d’une carte réseau disponible pour les connexions câblées et sans fil.

**Solution**

Aucune.

L' **application MED-V ne répond pas pendant un certain temps lors de la fermeture**. Dans certains cas, une application MED-V ne répond plus lorsque vous tentez de la fermer.

**Solution**

Vous pouvez spécifier la durée pendant laquelle MED-V attend de fermer des applications qui ne répondent pas en définissant la clé de Registre WaitToKillAppTimeout dans l’ordinateur virtuel invité. Pour plus d’informations, reportez-vous [à la rubrique Comment augmenter le délai d’arrêt pour que les processus puissent s’arrêter correctement dans Windows XP](https://go.microsoft.com/fwlink/?LinkId=206819) ( https://go.microsoft.com/fwlink/?LinkId=206819) .

Le **fait de renommer un raccourci d’application publiée dans l’ordinateur virtuel invité ne modifie pas le nom publié dans l’hôte**. Lorsque vous publiez une application en créant un raccourci et renommez le raccourci dans l’ordinateur virtuel invité, le nom de l’application d’origine reste dans le menu **Démarrer** de l’hôte. Le programme continue de s’exécuter comme prévu, mais le programme conserve toujours le nom d’origine.

**Solution**

Aucune. Il s’agit d’un comportement connu de l’ordinateur virtuel Windows.

**Le déplacement d’un raccourci dans l’ordinateur virtuel invité ne met pas à jour l’emplacement du menu Démarrer de l’ordinateur hôte**. Les raccourcis d’application MED-V publiés sur le menu **Démarrer** de l’ordinateur hôte sont catalogués dans le registre. Si vous déplacez un raccourci vers une application dans un sous-dossier, le registre ne sera pas mis à jour pour refléter la modification.

**Solution**

Pour modifier l’emplacement d’un raccourci d’application MED-V, procédez comme suit:

1.  Lorsque MED-V est en cours d’exécution, ouvrez l’Explorateur Windows sur l’ordinateur virtuel d’invité MED-V.

2.  Accédez au répertoire «%ALLUSERSPROFILE%\\Start Menu\\Programs».

3.  Déplacez le raccourci de l’application dans les dossiers StartMenu ou programmes.

4.  Après un délai de 30 secondes, vérifiez que les raccourcis sont supprimés du menu **Démarrer** de l’ordinateur hôte.

5.  Replacez les raccourcis de l’application dans les nouveaux dossiers de programmes sous l’annuaire de Menu\\Programs de démarrage.

6.  Après une durée de 30 secondes, vérifiez que les raccourcis sont mis à jour dans le menu **Démarrer** de l’ordinateur hôte.

**Les applications publiées peuvent expirer après une période d’inactivité**. Dans certains cas, le délai imparti pour les applications publiées sera écoulé s’il est resté inactif pendant un certain temps. Cette situation se produit uniquement si la sécurité IPsec est activée et que l’espace de travail MED-V est configuré pour le mode NAT. Cette situation ne se produit pas s’il s’exécute en mode BRIDGEd.

**Solution**

Désactivez IPsec lorsque vous exécutez l’espace de travail MED-V en mode NAT.

**Le verrouillage d’une application publiée à la barre des tâches ignore MED-V**. Si un utilisateur final épingle une application publiée à la barre des tâches, puis ferme l’application, MED-V est ignoré lors de la prochaine ouverture de l’application à partir de l’icône de la barre des tâches. Au lieu de cela, l’application s’ouvre directement dans une fenêtre VMSAL.

**Solution**

Ne codez pas les applications publiées dans MED-V vers la barre des tâches.

## Rubriques connexes


[Meilleures pratiques de sécurité pour les opérations de MED-V](security-best-practices-for-med-v-operations.md)

[Résolution des problèmes de déploiement](deployment-troubleshooting.md)

 

 





