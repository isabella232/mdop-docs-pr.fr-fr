---
title: À propos de MBAM2.5 SP1
description: À propos de MBAM2.5 SP1
author: dansimp
ms.assetid: 6f12e605-44e6-4646-9c20-aee89c8ff0b7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 09/27/2016
ms.openlocfilehash: 41e47e1561629c00d30b45ad2dcd94f37753af5b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810163"
---
# À propos de MBAM2.5 SP1


MBAM 2,5 SP1 fournit une interface d’administration simplifiée pour le chiffrement de lecteur BitLocker. BitLocker fournit une protection améliorée contre le vol de données ou l’exposition des données pour les ordinateurs perdus ou volés. BitLocker chiffre toutes les données stockées sur le système d’exploitation Windows, ainsi que les disques et les lecteurs de données configurés.

## Présentation de MBAM


MBAM 2,5 SP1 offre les fonctionnalités suivantes:

-   Permet aux administrateurs d’automatiser le processus de cryptage des volumes sur les ordinateurs clients au sein de l’entreprise.

-   Permet aux responsables de la sécurité de déterminer rapidement l’état de conformité de chaque ordinateur ou même de l’entreprise.

-   Fournit un rapport centralisé et une gestion du matériel avec Microsoft System Center Configuration Manager.

-   Réduit la charge de travail de l’assistance technique pour aider les utilisateurs finaux à utiliser le code confidentiel BitLocker et les requêtes de clé de récupération.

-   Permet aux utilisateurs finaux de récupérer des appareils chiffrés indépendamment via le portail libre-service.

-   Permet aux responsables de la sécurité d’auditer facilement l’accès pour récupérer des informations clés.

-   Permet aux utilisateurs de Windows d’entreprise de continuer à travailler en tout lieu et de garantir la protection des données d’entreprise.

MBAM applique les options de stratégie de chiffrement BitLocker que vous avez définies pour votre entreprise, surveille la conformité des ordinateurs clients avec ces stratégies et signale l’état de chiffrement de l’ordinateur de l’entreprise et de la personne. De plus, MBAM vous permet d’accéder aux informations de clé de récupération lorsque les utilisateurs oublient leur code confidentiel ou leur mot de passe, ou lorsque leurs enregistrements de BIOS ou de démarrage changent.

Les groupes suivants peuvent être intéressés par l’utilisation de MBAM pour gérer BitLocker:

-   Administrateurs, responsables de la sécurité informatique et responsables de la conformité chargés de veiller à ce que les données confidentielles ne soient pas divulguées sans autorisation.

-   Administrateurs responsables de la sécurité informatique de bureaux distants ou de succursales

-   Administrateurs responsables des ordinateurs clients exécutant Windows

**Remarques**  BitLocker n’est pas expliqué en détail dans cette documentation MBAM. Pour plus d’informations, voir [vue d’ensemble du chiffrement de lecteur BitLocker](https://go.microsoft.com/fwlink/p/?LinkId=225013).

 

## <a href="" id="what-s-new-in-mbam-2-5-sp1"></a>Nouveautés de MBAM 2,5 SP1


Cette section décrit les nouvelles fonctionnalités de MBAM 2,5 SP1.

### Langues récemment prises en charge pour le client MBAM 2,5 SP1

Les langues supplémentaires suivantes sont désormais prises en charge dans MBAM 2,5 SP1 pour le client MBAM uniquement, y compris le portail libre-service:

Tchèque (République tchèque) CS-CZ

Danois (Danemark) da-DK

Néerlandais (Pays-Bas) NL-NL

FI (Finlande)-FI

Grec (Grèce) El-GR

Hongrois (Hongrie) HU-HU

Norvégien, Bokmål (Norvège) NB-non

Polonais (Pologne) PL-PL

Portugais (Portugal) pt-PT

Slovaque (Slovaquie) SK-SK

Slovène (Slovénie) SL-SI

Suédois (Suède) sv-SE

Turc (Turquie) TR-TR

Pour obtenir la liste de toutes les langues prises en charge pour les clients et serveurs dans MBAM 2,5 et MBAM 2,5 SP1, voir [MBAM 2,5 configurations prises en charge](mbam-25-supported-configurations.md).

### Prise en charge de Windows 10

MBAM 2,5 SP1 ajoute la prise en charge de Windows 10 et de Windows Server 2016, en plus des logiciels pris en charge dans les versions antérieures d’MBAM.

Windows 10 est pris en charge dans MBAM 2,5 et MBAM 2,5 SP1.

### Prise en charge de Microsoft SQL Server 2014 SP1

MBAM 2,5 SP1 ajoute la prise en charge de Microsoft SQL Server 2014 SP1, en plus des mêmes logiciels pris en charge dans les versions antérieures d’MBAM.

### MBAM n’est plus fourni avec MSI distinct

À partir de MBAM 2,5 SP1, un MSI distinct n’est plus inclus dans le produit MBAM. Toutefois, vous pouvez extraire le MSI du fichier exécutable (. exe) qui est inclus dans le produit.

### MBAM peut OwnerAuth mot de passe de confiance sans être propriétaire du TPM

Auparavant, si MBAM ne possédait pas le TPM, le TPM OwnerAuth n’a pas pu être de confiance dans la base de données MBAM. Pour configurer MBAM de façon à ce qu’il s’agit du TPM et enregistrer les mots de passe, vous devez désactiver la mise en service automatique du TPM et effacer le TPM de l’ordinateur client.

Dans Windows 8 et versions ultérieures, MBAM 2,5 SP1 peut désormais avoir pour tiers de confiance les mots de passe OwnerAuth sans être propriétaire du TPM. Lors du démarrage d’un service, les requêtes MBAM pour voir si le TPM est déjà détenu et, si tel est le cas, il sollicite les mots de passe du système d’exploitation. Le mot de passe est alors dans la base de données MBAM. De plus, la stratégie de groupe doit être définie pour empêcher la suppression locale du OwnerAuth.

Dans Windows 7, MBAM doit avoir le module de plateforme sécurisée pour que les informations sur le TPM OwnerAuth automatiquement dans la base de données MBAM. Si MBAM ne possède pas le TPM et la sauvegarde Active Directory (AD) du TPM est configurée par le biais de la stratégie de groupe, vous devez utiliser les applets de commande d' **importation de données MBAM Active Directory (AD)** pour copier le TPM OWNERAUTH d’AD dans la base de données MBAM. Il s’agit de cinq nouvelles applets de commande PowerShell qui préremplissent les bases de données MBAM avec les informations de récupération de volume et de propriétaire du TPM stockées dans Active Directory.

Pour plus d’informations, consultez [considérations relatives à la sécurité de MBAM 2,5](mbam-25-security-considerations.md#bkmk-tpm).

### MBAM peut automatiquement déverrouiller le TPM après un verrouillage

Sur les ordinateurs exécutant le module de plateforme sécurisée 1,2, vous pouvez maintenant configurer MBAM pour qu’il déverrouille automatiquement le TPM en cas de verrouillage. Si la fonctionnalité de réinitialisation automatique de verrouillage de TPM est activée, MBAM peut détecter qu’un utilisateur est verrouillé, puis obtenir le mot de passe OwnerAuth de la base de données MBAM pour déverrouiller automatiquement le TPM pour l’utilisateur.

Cette fonctionnalité doit être activée côté serveur et dans une stratégie de groupe du côté client. Pour plus d’informations, consultez [considérations relatives à la sécurité de MBAM 2,5](mbam-25-security-considerations.md#bkmk-autounlock).

### Prise en charge des protections de mot de passe numérique compatibles FIPS

Dans MBAM 2.5, la prise en charge des clés de récupération de BitLocker conformes à la norme FIPS (Federal Information Processing Standard) sur les appareils exécutant le système d’exploitation Windows 8,1 est ajoutée. Toutefois, Windows n’a pas implémenté de clés de récupération compatibles FIPS dans Windows 7. C’est pourquoi les appareils Windows 7 et Windows 8 ont toujours requis un protecteur de l’agent de récupération de données (DRA) pour la récupération.

L’équipe Windows dispose de clés de récupération compatibles FIPS conformes à un correctif et MBAM 2,5 SP1 lui a également ajouté une prise en charge.

**Remarques**  Les ordinateurs clients qui exécutent le système d’exploitation Windows8 requièrent toujours un protecteur de DRA puisque le correctif n’a pas été transféré vers ce système d’exploitation. Pour télécharger et installer le correctif BitLocker pour les ordinateurs Windows 7 et Windows 8, voir [package de correctif 2 pour l’administration et la 2,5 surveillance de BitLocker](https://support.microsoft.com/kb/3015477) . Pour plus d’informations sur l’utilisation de DRA, voir [utilisation d’agents de récupération de données avec BitLocker](https://go.microsoft.com/fwlink/?LinkId=393557).

 

Pour activer la conformité FIPS au sein de votre organisation, vous devez configurer les paramètres de stratégie de groupe FIPS (Federal Information Processing Standard). Pour obtenir des instructions de configuration, voir [paramètres de stratégie de groupe BitLocker](https://go.microsoft.com/fwlink/?LinkId=393560).

### Personnaliser le message de récupération de pré-démarrage et l’URL avec le nouveau paramètre de stratégie de groupe

Un nouveau paramètre de stratégie de groupe, configurer un message de récupération pour la **prédémarrage et une URL**, vous permet de configurer un message de récupération personnalisé ou de spécifier une URL qui s’affiche dans l’écran de récupération avant démarrage de BitLocker lorsque le lecteur se bloque. Ce paramètre est uniquement disponible sur les ordinateurs clients exécutant Windows 10.

Si vous activez ce paramètre de stratégie, vous pouvez sélectionner l’une de ces options pour le message de récupération avant démarrage:

-   **Utiliser un message de récupération personnalisé**: sélectionnez cette option pour inclure un message personnalisé dans l’écran de récupération de BitLocker avant démarrage.

-   **Utiliser une URL de récupération personnalisée**: sélectionnez cette option pour remplacer l’URL par défaut qui s’affiche dans l’écran de récupération de BitLocker avant démarrage.

-   **Utiliser le message de récupération par défaut et l’URL**: sélectionnez cette option pour afficher le message et l’URL de récupération de BitLocker par défaut dans l’écran de récupération de BitLocker avant démarrage. Si vous avez précédemment configuré un message de récupération personnalisé ou une URL et que vous souhaitez rétablir le message par défaut, vous devez activer cette stratégie et sélectionner cette option.

Le nouveau paramètre de stratégie de groupe se trouve dans le nœud d’objet GPO suivant: stratégies de **Configuration ordinateur** &gt; **Policies** &gt; **modèles d’administration** &gt; **composants Windows** &gt; **MBAM (gestion de BitLocker)** &gt; **lecteur du système d’exploitation**. Pour plus d’informations, reportez-vous [à planification des exigences relatives aux stratégies de groupe MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### MBAM a ajouté une prise en charge du chiffrement d’espace utilisé.

Dans MBAM 2,5 SP1, si vous activez le chiffrement d’espace utilisé via la stratégie de groupe BitLocker, le client MBAM le respecte.

Ce paramètre de stratégie de groupe est appelé **appliquer le type de chiffrement de lecteur sur les lecteurs du système d’exploitation** et il se trouve dans le nœud d’objet GPO suivant: **Configuration ordinateur** &gt; **modèles d’administration** &gt; **composants Windows** &gt; lecteurs du système d’exploitation **BitLocker Drive Encryption** &gt; **Operating System Drives**. Si vous activez cette stratégie et sélectionnez le type de chiffrement en tant qu' **espace utilisé uniquement pour le chiffrement**, MBAM honorera la stratégie et BitLocker cryptera uniquement l’espace disque utilisé sur le volume.

Pour plus d’informations, reportez-vous [à planification des exigences relatives aux stratégies de groupe MBAM 2,5](planning-for-mbam-25-group-policy-requirements.md).

### Prise en charge du client MBAM pour les disques durs chiffrés

MBAM prend en charge BitLocker sur les disques durs chiffrés qui satisfont les exigences de spécification TCG pour Opal ainsi que les normes IEEE 1667. Lorsque BitLocker est activé sur ces appareils, il génère des clés et effectue des tâches de gestion sur le lecteur chiffré. Pour plus d’informations, voir [disque dur chiffré](https://technet.microsoft.com/library/hh831627.aspx) .

### La configuration de la délégation n’est plus nécessaire lors de l’inscription des SPN

La configuration requise pour la délégation contrainte de noms d’application (SPN) que vous enregistrez pour le compte du pool d’applications n’est plus nécessaire dans MBAM 2,5 SP1. Néanmoins, il est toujours requis pour MBAM 2,5.

### Activer BitLocker à l’aide de MBAM dans le cadre d’un déploiement Windows

Dans MBAM 2,5 SP1, vous pouvez utiliser un script PowerShell pour configurer les clés de récupération de lecteur et de confiance de BitLocker sur le serveur MBAM.

Pour plus d’informations, reportez-vous [à la rubrique activation de BitLocker à l’aide de MBAM dans le cadre d’un déploiement Windows](how-to-enable-bitlocker-by-using-mbam-as-part-of-a-windows-deploymentmbam-25.md)

### Le portail libre-service peut être personnalisé à l’aide de PowerShell ou de l’Assistant de personnalisation SSP.

À compter du MBAM 2,5 SP1, le portail libre-service peut être configuré à l’aide de l’Assistant de personnalisation et à l’aide de PowerShell. Découvrez [Comment configurer les applications Web MBAM 2,5](how-to-configure-the-mbam-25-web-applications.md).

### Le navigateur Web ne s’exécute plus involontairement en tant qu’administrateur

Dans le cas d’un problème lié à MBAM 2,5, les liens d’aide de l’outil de configuration du serveur peuvent s’ouvrir dans les fenêtres de navigateur avec des droits d’administrateur. Ce problème a été résolu dans MBAM 2,5 SP1.

### Il n’est plus nécessaire de télécharger les fichiers JavaScript pour configurer le portail libre-service lorsque le CDN n’est pas accessible

Dans MBAM 2,5 et les versions antérieures, les fichiers jQuery utilisés pour la configuration du portail libre-service doivent être téléchargés à partir du réseau de distribution de contenu à l’avance si les clients qui accèdent au portail libre-service ne disposent pas d’un accès à Internet. Dans MBAM 2,5 SP1, tous les fichiers JavaScript sont inclus dans le produit, c’est pourquoi le téléchargement est inutile.

### Les rapports peuvent être ouverts dans le générateur de rapports 3,0

Dans MBAM 2,5 SP1, les rapports ont été mis à jour avec le schéma de langue de définition de rapport le plus récent, ce qui permet aux utilisateurs d’ouvrir et de personnaliser les rapports dans le générateur de rapports 3,0 et de les enregistrer immédiatement sans endommager le fichier de rapport.

### Nouvelles cmdlets PowerShell

Les nouvelles cmdlets PowerShell pour MBAM 2,5 SP1 vous permettent de configurer et de gérer différentes fonctionnalités MBAM, notamment des bases de données, des rapports et des applications Web. Chaque fonctionnalité possède une applet de cmdlet PowerShell correspondante que vous pouvez utiliser pour activer ou désactiver des fonctionnalités, ou pour obtenir des informations sur la fonctionnalité.

Les applets de commande suivantes ont été implémentées pour MBAM 2,5 SP1:

-   Ecriture-MbamTpmInformation

-   Ecriture-MbamRecoveryInformation

-   Lecture-ADTpmInformation

-   Lecture-ADRecoveryInformation

-   Ecriture-MbamComputerUser

Les paramètres suivants ont été implémentés dans les applets de commande Enable-MbamWebApplication et test-MbamWebApplication pour MBAM 2,5 SP1:

-   DataMigrationAccessGroup

-   TpmAutoUnlock

Pour plus d’informations sur les applets de contrôle, voir [considérations relatives à la sécurité dans MBAM 2,5](mbam-25-security-considerations.md) et aide sur l' [applet de contrôle Microsoft BitLocker administration et analyse](https://technet.microsoft.com/library/dn720418.aspx).

### L’agent MBAM détecte le mode de présentation

L’agent MBAM peut détecter lorsque l’ordinateur est en mode de présentation et éviter d’appeler l’interface utilisateur MBAM à ce moment-là.

### Service agent MBAM désormais configuré pour utiliser le démarrage différé

Après l’installation, le service va désormais définir le service d’agent MBAM pour qu’il utilise le démarrage différé, ce qui réduit le temps nécessaire au démarrage de Windows.

### Les volumes de données fixes verrouillés s’indiquent désormais comme conformes

La logique de calcul de la conformité pour les volumes «données fixes figées» a été modifiée pour signaler les volumes comme «conformes», mais avec l’état de la protection et l’état de cryptage «inconnu» Auparavant, les volumes verrouillés ont été signalés comme «non conformes», un état de protection de «chiffré», un état de chiffrement «inconnu» et un détail d’état de conformité «une erreur inconnue».


## Obtention de technologies MDOP


MBAM fait partie du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie du programme Microsoft Software Assurance. Pour plus d’informations sur le programme Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP?](https://go.microsoft.com/fwlink/?LinkId=322049).

## Notes de publication de MBAM 2,5 SP1


Pour plus d’informations et des informations de dernière minute qui ne sont pas incluses dans cette documentation, voir [notes de publication pour MBAM 2,5 SP1](release-notes-for-mbam-25-sp1.md).

## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring) 
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).

## Rubriques connexes


[Microsoft BitLocker Administration and Monitoring2.5](index.md)

[Prise en main de MBAM2.5](getting-started-with-mbam-25.md)

 

 





