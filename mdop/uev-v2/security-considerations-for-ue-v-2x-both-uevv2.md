---
title: Considérations relatives à la sécurité pour UE-V2.x
description: Considérations relatives à la sécurité pour UE-V2.x
author: dansimp
ms.assetid: 9d5c3cae-9fcb-4dea-bd67-741b3dea63be
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 8e24e9e37de11053663bb90974fabf2ff369aeca
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810691"
---
# Considérations relatives à la sécurité pour UE-V2.x


Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité relatives à la virtualisation de l’interface utilisateur de Microsoft (UE-V) 2,0, 2,1 et 2,1 SP1. Pour plus d’informations, suivez les liens fournis ici.

## Considérations en matière de sécurité pour la configuration d’UE-V


**Important**  Lorsque vous créez le partage de stockage des paramètres, limitez l’accès du partage aux utilisateurs qui ont besoin d’y accéder.

 

Étant donné que les packages de paramètres peuvent contenir des informations personnelles, vous devez veiller à les protéger aussi bien que possible. En général, procédez comme suit:

-   Limitez le partage aux seuls utilisateurs qui ont besoin d’y accéder. Créer un groupe de sécurité pour les utilisateurs qui ont Redirigé des dossiers sur un partage particulier et limiter l’accès à ces utilisateurs uniquement.

-   Lorsque vous créez le partage, masquez le partage en plaçant un $ après le nom du partage. Ce complément permet de masquer le partage dans les navigateurs informels et le partage n’est pas visible dans les emplacements réseau.

-   Octroiez aux utilisateurs uniquement le nombre minimum d’autorisations dont ils doivent disposer. Les tableaux suivants indiquent les autorisations requises.

    1.  Définissez les autorisations SMB au niveau du partage suivantes pour le dossier Setting Storage Location.

        | Compte d’utilisateur | Autorisations recommandées |
        | - | - |
        | Tout le monde | Aucune autorisation |
        |Groupe de sécurité d’UE-V | Contrôle total |

    2.  Définissez les autorisations de système de fichiers NTFS suivantes pour le dossier emplacement de stockage des paramètres.

        | Compte d’utilisateur | Autorisations recommandées | Folder |
        | - | - | - |
        | Créateur/propriétaire | Contrôle total | Sous-dossiers et fichiers uniquement|
        | Administrateurs de domaine | Contrôle total | Ce dossier, les sous-dossiers et les fichiers |
        | Groupe de sécurité des utilisateurs d’UE-V | Afficher le dossier/lire les données, créer des dossiers/ajouter des données | Ce dossier uniquement |
        | Tout le monde | Supprimer toutes les autorisations | Aucune autorisation |

    3.  Définissez les autorisations de SMB au niveau du partage suivantes pour le dossier du catalogue de modèles de paramètres.

        | Compte d’utilisateur | Recommander des autorisations |
        | - | - |
        | Tout le monde | Aucune autorisation |
        | Ordinateurs de domaine | Lire les niveaux d’autorisation |
        | Administrateurs | Niveaux d’autorisation en lecture/écriture |
         
    4.  Définissez les autorisations NTFS suivantes pour le dossier du catalogue de modèles de paramètres.

        | Compte d’utilisateur | Autorisations recommandées | Appliquer à |
        | - | - | - |
        | Créateur/propriétaire | Contrôle total | Ce dossier, les sous-dossiers et les fichiers |
        | Ordinateurs de domaine | Afficher le contenu du dossier et les autorisations de lecture | Ce dossier, les sous-dossiers et les fichiers|
        | Tout le monde| Aucune autorisation| Aucune autorisation|
        | Administrateurs| Contrôle total| Ce dossier, les sous-dossiers et les fichiers|

### Utiliser windowsserver2003 en tant que WindowsServer2003 pour héberger des partages de fichiers redirigés

Les fichiers de package de paramètres utilisateur contiennent des informations personnelles transférées entre l’ordinateur client et le serveur qui stocke les packages de paramètres. En raison de ce processus, vous devez vous assurer que les données sont protégées lors de leur déplacement sur le réseau.

Les données de paramètres utilisateur sont vulnérables aux menaces potentielles suivantes: interception des données lors de leur passage sur le réseau, falsification des données lors du passage sur le réseau et usurpation d’identité du serveur qui héberge les données.

Depuis Windows Server2003, plusieurs fonctionnalités du système d’exploitation Windows Server peuvent vous aider à sécuriser les données des utilisateurs:

-   **Kerberos** : Kerberos est standard dans toutes les versions de Microsoft Windows2000Server et de windowsserver2003, en commençant par WindowsServer2003. Kerberos vérifie le niveau de sécurité le plus élevé aux ressources réseau. NTLM authentifie uniquement le client; Kerberos authentifie le serveur et le client. Lorsque la valeur NTLM est utilisée, le client ne sait pas si le serveur est valide. Cette différence est particulièrement importante si le client échange des fichiers personnels avec le serveur, comme dans le cas des profils utilisateur errants. Kerberos fournit une meilleure sécurité que le protocole NTLM. Kerberos n’est pas disponible pour les systèmes d’exploitation 4,0 ou antérieurs de Microsoft WindowsNTServer.

-   **IPSec** : le protocole IPSec fournit une authentification au niveau du réseau, l’intégrité des données et le chiffrement. IPsec vérifie les points suivants:

    -   Les données itinérantes sont sûres de la modification des données lorsque les données sont en cours de routage.

    -   Les données itinérantes sont sûres de l’interception, de l’affichage ou de la copie.

    -   Les données itinérantes ne sont pas accessibles par les parties non authentifiées.

-   **Signature SMB** : le protocole d’authentification par bloc de messages serveur (SMB) prend en charge l’authentification des messages, qui empêche le message actif et les attaques par homme-au-milieu. La signature SMB fournit cette authentification en plaçant une signature numérique dans chaque SMB. La signature numérique est alors vérifiée par le client et le serveur. Pour pouvoir utiliser la signature SMB, vous devez d’abord l’activer ou l’exiger sur le client SMB et le serveur SMB. Notez que la signature SMB impose une pénalité en termes de performances. Il n’utilise pas encore plus de bande passante réseau, mais il utilise davantage de cycles UC sur le client et côté serveur.

### Toujours utiliser le système de fichiers NTFS pour les volumes qui contiennent des données utilisateur

Pour la configuration la plus sécurisée, configurez les serveurs qui hébergent les fichiers de paramètres d’UE-V de façon à utiliser le système de fichiers NTFS. Contrairement au système de fichiers FAT, NTFS prend en charge les listes de contrôle d’accès discrétionnaires (DACL) et les listes de contrôle d’accès système (SACL). Les DACL et les SACL contrôlent les utilisateurs autorisés à effectuer des opérations sur un fichier, ainsi que les événements déclenchant la journalisation des actions exécutées sur un fichier.

### Ne comptez pas sur le système EFS pour chiffrer les fichiers des utilisateurs lors de leur transmission via le réseau

Lorsque vous utilisez le système de fichiers EFS pour chiffrer des fichiers sur un serveur distant, les données chiffrées ne sont pas chiffrées lors du transit sur le réseau. elle est uniquement chiffrée lorsque celle-ci est stockée sur le disque.

Ce processus de chiffrement n’est pas applicable lorsque votre système inclut la sécurité du protocole Internet (IPsec) ou WebDAV (Web Distributed Authoring and Versioning). IPsec chiffre les données lors de leur transport via un réseau TCP/IP. Si le fichier est chiffré avant d’être copié ou déplacé vers un dossier WebDAV sur un serveur, il reste chiffré lors de la transmission et est stocké sur le serveur.

### Permettre à l’agent UE-V de créer des dossiers pour chaque utilisateur

Pour vous assurer que UE-V fonctionne de façon optimale, créez uniquement le partage racine sur le serveur et laissez l’agent UE-V créer des dossiers pour chaque utilisateur. UE-V crée ces dossiers utilisateur avec la sécurité appropriée.

Cette configuration d’autorisation permet aux utilisateurs de créer des dossiers pour le stockage des paramètres. UE-V agent crée et sécurise un dossier de package de paramètres pendant qu’il s’exécute dans le contexte de l’utilisateur. Les utilisateurs bénéficient d’un contrôle total sur leur dossier de package de paramètres. Les autres utilisateurs n’héritent pas de l’accès à ce dossier. Vous n’avez pas besoin de créer et de sécuriser des annuaires utilisateurs individuels. L’agent qui s’exécute dans le contexte de l’utilisateur le fait automatiquement.

**Remarques**  Une sécurité supplémentaire peut être configurée quand un serveur Windows est utilisé pour le partage de stockage de paramètres. UE-V peut être configuré pour vérifier que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier où sont stockés les packages de paramètres. Pour activer une sécurité supplémentaire, utilisez la commande suivante:

1.  Ajoutez _DWORD la clé de Registre RepositoryOwnerCheckEnabled `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Définissez la valeur de la clé de Registre sur *1*.

Lorsque ce paramètre de configuration est en place, l’agent UE-V vérifie que le groupe Administrateurs local ou l’utilisateur actuel est le propriétaire du dossier de package de paramètres. Si ce n’est pas le cas, l’agent UE-V n’autorise pas l’accès au dossier.

 

Si vous devez créer des dossiers pour les utilisateurs, vérifiez que vous disposez des autorisations appropriées.

Nous vous recommandons vivement de ne pas créer de dossiers avant la précréation. Au lieu de cela, indiquez à l’agent UE-V de créer le dossier pour l’utilisateur.

### Vérifiez que les autorisations appropriées permettent d’enregistrer les paramètres d’UE-V 2 dans un répertoire de base ou un annuaire personnalisé

Si vous redirigez les paramètres d’UE-V vers le répertoire de base d’un utilisateur ou un annuaire d’Active Directory (AD) personnalisé, assurez-vous que les autorisations sur le répertoire sont définies correctement pour votre organisation.






## Rubriques connexes


[Informations techniques de référence sur UE-V2.x](technical-reference-for-ue-v-2x-both-uevv2.md)

 

 





