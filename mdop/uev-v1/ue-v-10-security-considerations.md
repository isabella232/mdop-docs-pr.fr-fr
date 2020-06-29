---
title: Considérations sur la sécurité relatives à UE-V1.0
description: Considérations sur la sécurité relatives à UE-V1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810290"
---
# Considérations sur la sécurité relatives à UE-V1.0


Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité relatives à la virtualisation de l’utilisation de Microsoft. Pour plus d’informations, suivez les liens fournis ici.

## Considérations en matière de sécurité pour la configuration d’UE-V


**Lorsque vous créez le partage de stockage des paramètres, limitez l’accès du partage aux utilisateurs qui ont besoin d’y accéder.**

Étant donné que les packages de paramètres peuvent contenir des informations personnelles, vous devez veiller à les protéger aussi bien que possible. En général, procédez comme suit:

-   Limitez le partage aux seuls utilisateurs qui ont besoin d’y accéder. Créer un groupe de sécurité pour les utilisateurs qui ont Redirigé des dossiers sur un partage particulier et limiter l’accès à ces utilisateurs uniquement;

-   Lorsque vous créez le partage, masquez le partage en plaçant un $ après le nom du partage. Cela permet de masquer le partage dans les navigateurs informels et le partage ne sera pas visible dans les emplacements réseau.

-   Octroiez aux utilisateurs uniquement le volume minimum d’autorisations nécessaires. Les autorisations nécessaires sont indiquées dans les tableaux ci-dessous.

    1.  Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier Setting Storage Location:

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left">Compte d’utilisateur</th>
        <th align="left">Autorisations recommandées</th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p>Tout le monde</p></td>
        <td align="left"><p>Aucune autorisation</p></td>
        </tr>
        <tr class="even">
        <td align="left"><p>Groupe de sécurité d’UE-V</p></td>
        <td align="left"><p>Contrôle total</p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### Utiliser Windows Server 2003 ou un serveur ultérieur pour héberger des partages de fichiers redirigés

Les fichiers de package de paramètres utilisateur contiennent des informations personnelles transférées entre l’ordinateur client et le serveur qui stocke les packages de paramètres. Pour cette raison, vous devez vous assurer que les données sont protégées lors de leur déplacement sur le réseau.

Les données de paramètres utilisateur sont vulnérables aux menaces potentielles suivantes: interception des données lors de leur passage sur le réseau. falsification des données lors du passage sur le réseau; et l’usurpation d’identité du serveur qui héberge les données.

Plusieurs fonctionnalités de Windows Server 2003 et versions ultérieures peuvent vous aider à sécuriser les données des utilisateurs:

-   **Kerberos** : Kerberos est standard pour toutes les versions de Windows 2000 et de windows Server 2003 et versions ultérieures. Kerberos vérifie le niveau de sécurité le plus élevé aux ressources réseau. NTLM authentifie uniquement le client; Kerberos authentifie le serveur et le client. Lorsque la valeur NTLM est utilisée, le client ne sait pas si le serveur est valide. Ceci est particulièrement important si le client échange des fichiers personnels avec le serveur, comme c’est le cas pour les profils itinérants. Kerberos fournit une meilleure sécurité que le protocole NTLM. Kerberos n’est pas disponible dans la version 4,0 ou les systèmes d’exploitation de version antérieure de Windows NT.

-   **IPSec** : le protocole IPSec fournit une authentification au niveau du réseau, l’intégrité des données et le chiffrement. IPsec vérifie les points suivants:

    -   Les données itinérantes sont sûres de la modification des données lors de l’itinéraire.

    -   Les données itinérantes sont sûres de l’interception, de l’affichage ou de la copie.

    -   Les données itinérantes ne sont pas accessibles par les parties non authentifiées.

-   **Signature SMB** : le protocole d’authentification par bloc de message serveur (SMB) prend en charge l’authentification des messages qui empêche les messages actifs et les attaques de type «homme-au-milieu». La signature SMB fournit cette authentification en plaçant une signature numérique dans chaque SMB. La signature numérique est alors vérifiée par le client et le serveur. Pour pouvoir utiliser la signature SMB, vous devez d’abord l’activer ou l’exiger sur le client SMB et le serveur SMB. Notez que la signature SMB impose une pénalité en termes de performances. Il n’utilise pas encore plus de bande passante réseau, mais il utilise davantage de cycles UC sur le client et côté serveur.

### Toujours utiliser le système de fichiers NTFS pour les volumes qui contiennent des données d’utilisateurs

Pour la configuration la plus sécurisée, configurez les serveurs qui hébergent les fichiers de paramètres d’UE-V de façon à utiliser le système de fichiers NTFS. Contrairement à FAT, le système NTFS prend en charge les listes de contrôle d’accès discrétionnaire (DACL) et les listes de contrôle d’accès (SACL). Les DACL et les SACL contrôlent les utilisateurs autorisés à effectuer des opérations sur un fichier, ainsi que les événements déclenchant la journalisation des actions exécutées sur un fichier.

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a>Ne pas s’appuyer sur le système EFS pour chiffrer les fichiers des utilisateurs lors de leur transmission via le réseau

Lorsque vous utilisez le système de fichiers EFS pour chiffrer les fichiers sur un serveur distant, les données chiffrées ne sont pas chiffrées lors du transit sur le réseau. Elle est uniquement chiffrée lorsque celle-ci est stockée sur le disque.

Il existe des exceptions à cette configuration lorsque votre système inclut le protocole IPsec (Internet Protocol Security) ou WebDAV (Web Distributed Authoring and Versioning). IPsec chiffre les données lors de leur transport via un réseau TCP/IP. Si le fichier est chiffré avant d’être copié ou déplacé vers un dossier WebDAV sur un serveur, il reste chiffré lors de la transmission et est stocké sur le serveur.

### Chiffrer le cache des fichiers en mode hors connexion

Par défaut, le cache des fichiers en mode hors connexion est protégé sur les partitions NTFS par des listes de précautions, mais le fait de chiffrer le cache renforce la sécurité sur un ordinateur local. Par défaut, le cache de l’ordinateur local n’est pas chiffré, de sorte que les fichiers chiffrés mis en cache à partir du réseau ne seront pas chiffrés sur l’ordinateur local. Cela risque de compromettre la sécurité dans certains environnements.

Lorsque le chiffrement est activé, tous les fichiers du cache de fichiers hors connexion sont chiffrés. Il s’agit du chiffrement des fichiers existants, ainsi que des fichiers ajoutés plus tard. La copie mise en cache de l’ordinateur local est affectée, mais pas la copie réseau associée.

Le cache peut être chiffré de l’une des deux manières suivantes:

1.  Via une stratégie de groupe. -Activez le paramètre **chiffrer le cache fichiers en mode hors connexion** , situé sur ordinateur Configuration\\Administrative Templates\\Network\\Offline fichiers, dans l’éditeur de stratégies de groupe.

2.  Manuels. -Sélectionnez Outils, puis Options des dossiers dans le menu de commandes de l’Explorateur Windows. Sélectionnez l’onglet fichiers en mode hors connexion, puis activez la case à cocher **chiffrer les fichiers en mode hors connexion pour sécuriser les données** .

### Permettre à l’agent UE-V de créer des dossiers pour chaque utilisateur

Pour vous assurer que UE-V fonctionne de façon optimale, créez uniquement le partage racine sur le serveur et laissez l’agent UE-V créer des dossiers pour chaque utilisateur. UE-V va créer ces dossiers utilisateur avec la sécurité appropriée.

Cette configuration d’autorisation permet aux utilisateurs de créer des dossiers pour le stockage des paramètres. UE-V agent crée et sécurise un dossier settingspackage tout en étant exécuté dans le contexte de l’utilisateur. L’utilisateur reçoit le contrôle total de son dossier settingspackage. Les autres utilisateurs n’héritent pas de l’accès à ce dossier. Vous n’avez pas besoin de créer et de sécuriser des annuaires utilisateurs individuels. Cette opération sera exécutée automatiquement par l’agent qui s’exécute dans le contexte de l’utilisateur.

**Remarque**  
Une sécurité supplémentaire peut être configurée quand un serveur Windows est utilisé pour le partage de stockage de paramètres. UE-V peut être configuré pour vérifier que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés. Pour activer la sécurité supplémentaire, utilisez la commande suivante:

1.  Ajoutez une clé de Registre REG \ _DWORD nommée «RepositoryOwnerCheckEnabled» à `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .

2.  Définissez la valeur de clé de Registre sur 1.

Lorsque ce paramètre de configuration est en place, l’agent UE-V vérifie que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier settingspackage. Si ce n’est pas le cas, l’agent UE-V n’autorise pas l’accès au dossier.



Si vous devez créer des dossiers pour les utilisateurs et vérifier que vous disposez des autorisations appropriées.

Nous vous recommandons vivement de ne pas créer de dossiers, mais plutôt que d’utiliser l’agent UE-V pour créer le dossier de l’utilisateur.

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a>Vérifiez que les autorisations appropriées sont définies lors du stockage des paramètres d’UE-V dans le répertoire d’accueil d’un utilisateur.

Si vous redirigez les paramètres d’UE-V vers le répertoire de base d’un utilisateur, veillez à ce que les autorisations sur le répertoire de base de l’utilisateur soient définies correctement pour votre organisation.

## Rubriques connexes


[Sécurité et confidentialité pour UE-V1.0](security-and-privacy-for-ue-v-10.md)









