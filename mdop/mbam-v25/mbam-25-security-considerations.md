---
title: Considérations relatives à la sécurité pour MBAM2.5
description: Considérations relatives à la sécurité pour MBAM2.5
author: dansimp
ms.assetid: f6613c63-b32b-45fb-a6e8-673d6dae7d16
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 04/23/2017
ms.openlocfilehash: 86a756ab6f983fa1f22de6835b5993e1215d1dbe
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811994"
---
# Considérations relatives à la sécurité pour MBAM2.5


Cette rubrique contient les informations suivantes sur la façon de sécuriser l’administration et la surveillance de l’utilisation de Microsoft BitLocker (MBAM):

-   [Configurer MBAM pour qu’il dispose du TRUSTed OwnerAuth passwords](#bkmk-tpm)

-   [Configurer MBAM pour déverrouiller automatiquement le TPM après un verrouillage](#bkmk-autounlock)

-   [Connexion sécurisée à SQL Server](#bkmk-secure-databases)

-   [Créer des comptes et des groupes](#bkmk-accts-groups)

-   [Utiliser les fichiers journaux de MBAM](#bkmk-logfiles)

-   [Examiner les points de TDE de base de données MBAM](#bkmk-tde)

-   [Comprendre les considérations générales en matière de sécurité](#bkmk-general-security)

## <a href="" id="bkmk-tpm"></a>Configurer MBAM pour qu’il dispose du TRUSTed OwnerAuth passwords

**Remarques** Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. De plus, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée. Pour en savoir plus, voir [mot de passe du propriétaire du TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

En fonction de sa configuration, le module de plateforme sécurisée (TPM) se verrouille automatiquement dans certaines situations, par exemple lorsque trop de mots de passe incorrects ont été saisis et qu’ils peuvent rester verrouillés pendant un certain temps. Lors du verrouillage du module de plateforme sécurisée, BitLocker ne peut pas accéder aux clés de chiffrement pour effectuer des opérations de déverrouillage ou de déchiffrement, nécessitant l’entrée de leur clé de récupération BitLocker pour accéder au lecteur du système d’exploitation. Pour réinitialiser le verrouillage du TPM, vous devez fournir le mot de passe OwnerAuth TPM.

MBAM pouvez stocker le mot de passe OwnerAuth TPM dans la base de données MBAM s’il possède le TPM ou s’il a déposé le mot de passe. Les mots de passe OwnerAuth sont alors facilement accessibles sur le site Web d’administration et de surveillance lorsque vous devez effectuer une récupération à partir du verrouillage du TPM, ce qui évite d’avoir besoin d’attendre que le verrouillage soit résolu.

### OwnerAuth de confiance dans Windows 8 ou version ultérieure

**Remarques** Pour Windows 10, version 1607 ou ultérieure, seules les fenêtres peuvent prendre possession du module de plateforme sécurisée. Dans addiiton, Windows ne conserve pas le mot de passe du propriétaire du TPM lors de la mise en service du module de plateforme sécurisée. Pour en savoir plus, voir [mot de passe du propriétaire du TPM](https://docs.microsoft.com/windows/security/information-protection/tpm/change-the-tpm-owner-password) .

Dans Windows 8 (ou une version ultérieure), MBAM ne doit plus être propriétaire du TPM pour stocker le mot de passe OwnerAuth, tant que OwnerAuth est disponible sur l’ordinateur local.

Pour permettre à MBAM de se mettre sur tiers de confiance, puis de stocker les mots de passe OwnerAuth TPM, vous devez configurer les paramètres de stratégie de groupe suivants.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre de stratégie de groupe</th>
<th align="left">Configuration</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Activer la sauvegarde du TPM dans les services de domaine Active Directory</p></td>
<td align="left"><p>Désactivé ou non configuré</p></td>
</tr>
<tr class="even">
<td align="left"><p>Configurer le niveau des informations d’autorisation de propriétaire du TPM disponibles pour le système d’exploitation</p></td>
<td align="left"><p>Délégué/aucun ou non configuré</p></td>
</tr>
</tbody>
</table>

 

L’emplacement de ces paramètres de stratégie de **Computer Configuration** groupe est l’un des &gt; **modèles d’administration** de configuration de votre ordinateur &gt; **System** &gt; **Trusted Platform Module Services**.

**Remarques**  Windows supprime le OwnerAuth en local une fois que MBAM a réussi à y avoir ses paramètres.

 

### OwnerAuth de confiance dans Windows 7

Dans Windows 7, MBAM doit avoir le module de plateforme sécurisée pour que les informations sur le TPM OwnerAuth automatiquement dans la base de données MBAM. Si MBAM ne possède pas le module de plateforme sécurisée, vous devez utiliser les applets de commande d’importation de données Active Directory (AD) MBAM pour copier le TPM OwnerAuth d’Active Directory dans la base de données MBAM.

### Cmdlets d’importation de données Active Directory MBAM

Les applets de contrôle d’importation de données Active Directory MBAM vous permettent de récupérer des packages de clés de récupération et des mots de passe OwnerAuth stockés dans Active Directory.

Le serveur MBAM 2,5 SP1 est fourni avec quatre cmdlets PowerShell qui préremplissent les bases de données MBAM avec les informations de récupération de volume et de propriétaire du TPM stockées dans Active Directory.

Pour les clés et packages de récupération de volume:

-   Lecture-ADRecoveryInformation

-   Ecriture-MbamRecoveryInformation

Pour les informations sur le propriétaire du TPM:

-   Lecture-ADTpmInformation

-   Ecriture-MbamTpmInformation

Pour associer des utilisateurs aux ordinateurs:

-   Ecriture-MbamComputerUser

Les applets de contrôle de lecture-publicité \ * lisent des informations à partir d’Active Directory. Les applets de pression d’écriture-MBAM \ * entraversent les données dans les bases de données MBAM. Pour plus d’informations sur ces cmdlets, notamment la syntaxe, les paramètres et les exemples, voir [référence de l’applet de contrôle pour l’administration et l’analyse de la 2,5](https://technet.microsoft.com/library/dn459018.aspx) .

**Créer des associations utilisateur-ordinateur:** Les applets de contrôle d’importation de données Active Directory MBAM collectent des informations à partir d’Active Directory et insèrent les données dans la base de données MBAM. Toutefois, elles n’associent pas les utilisateurs aux volumes. Vous pouvez télécharger le script PowerShell Add-ComputerUser.ps1 pour créer des associations utilisateur-ordinateur, ce qui permet aux utilisateurs de regagner l’accès à un ordinateur via le site Web d’administration et de surveillance ou en utilisant le portail libre-service pour la récupération. Le script Add-ComputerUser.ps1 recueille des données de l’attribut **géré par** dans Active Directory (AD), le propriétaire de l’objet dans AD ou à partir d’un fichier CSV personnalisé. Le script ajoute ensuite les utilisateurs trouvés à l’objet pipeline d’informations de récupération, qui doit être passé à Write-MbamRecoveryInformation pour insérer les données dans la base de données de récupération.

Téléchargez le script Add-ComputerUser.ps1 PowerShell à partir du [Centre de téléchargement Microsoft](https://go.microsoft.com/fwlink/?LinkId=613122).

Vous pouvez spécifier des **Add-ComputerUser.ps1d’aide** pour obtenir de l’aide sur le script, y compris des exemples d’utilisation des cmdlets et du script.

Pour créer des associations utilisateur-ordinateur une fois que vous avez installé le serveur MBAM, utilisez l’applet de cmdlet PowerShell Write-MbamComputerUser. À l’instar du script PowerShell Add-ComputerUser.ps1, cette applet de commande permet de spécifier des utilisateurs qui peuvent utiliser le portail libre-service pour obtenir des informations sur le module de plateforme sécurisée ou un mot de passe pour l’ordinateur spécifié.

**Remarques**  L’agent MBAM remplacera les associations d’utilisateurs à ordinateur lorsque ce dernier commence à faire des rapports sur le serveur.

 

Éléments **requis:** Les applets de applet de lecture-publicité \ * peuvent récupérer des informations à partir de la publicité uniquement si elles sont exécutées en tant que compte d’utilisateur à privilèges élevés, tel qu’un administrateur de domaine, ou exécuté en tant que compte dans un groupe de sécurité personnalisé disposant d’un accès en lecture aux informations (recommandé).

[Guide des opérations de chiffrement de lecteur BitLocker: récupération des volumes chiffrés avec AD DS](https://technet.microsoft.com/library/cc771778(WS.10).aspx) fournit des détails sur la création d’un groupe de sécurité personnalisé (ou de plusieurs groupes) avec accès en lecture aux informations publicitaires.

**Autorisations d’écriture de service Web de récupération et de MBAM:** Les applets de commande Write-MBAM \ * acceptent l’URL du service de récupération et de matériel de MBAM, qui permet de publier les informations de récupération et de TPM. En règle générale, seul un compte de service d’ordinateur de domaine peut communiquer avec le service de récupération MBAM et de matériel. Dans MBAM 2,5 SP1, vous pouvez configurer le service de récupération et de matériel MBAM avec un groupe de sécurité appelé DataMigrationAccessGroup dont les membres sont autorisés à ignorer la vérification du compte de service d’ordinateur de domaine. Les applets de applet de MBAM \ * doivent être exécutées en tant qu’utilisateur appartenant au groupe configuré. (Vous pouvez également spécifier les informations d’identification d’un utilisateur individuel dans le groupe configuré à l’aide du paramètre-Credential dans les applets de connexion en écriture-MBAM \ *.)

Vous pouvez configurer le service de récupération MBAM et de matériel avec le nom de ce groupe de sécurité de l’une des manières suivantes:

-   Indiquez le nom du groupe de sécurité (ou individu) dans le paramètre-DataMigrationAccessGroup de l’applet de passe PowerShell Enable-MbamWebApplication-AgentService.

-   Configurez le groupe après l’installation de MBAM de récupération et de configuration matérielle en modifiant le fichier web.config dans le &lt; &gt; dossier Inetpub \\Microsoft gestion de BitLocker Solution\\Recovery et Service\\ de matériel.

    ```xml
    <add key="DataMigrationUsersGroupName" value="<groupName>|<empty>" />
    ```

    où &lt; NomGroupe &gt; est remplacé par le domaine et le nom du groupe (ou de l’utilisateur individuel) qui sera utilisé pour permettre la migration des données à partir d’Active Directory.

-   Dans le gestionnaire des services Internet (IIS), utilisez l’éditeur de configuration pour modifier ce appSetting.

Dans l’exemple suivant, la commande, lorsqu’elle est exécutée en tant que membre du groupe ADRecoveryInformation et du groupe utilisateurs de la migration des données, récupère les informations de récupération du volume sur les ordinateurs de l’unité d’organisation de poste de travail (UO) du domaine contoso.com, puis les enregistre dans MBAM à l’aide du service de récupération et de matériel de MBAM exécuté sur le serveur mbam.contoso.com.

``` syntax
PS C:\> Read-ADRecoveryInformation -Server contoso.com -SearchBase "OU=WORKSTATIONS,DC=CONTOSO,DC=COM" | Write-MbamRecoveryInformation -RecoveryServiceEndPoint "https://mbam.contoso.com/MBAMRecoveryAndHardwareService/CoreService.svc"
```

Les **applets de commande de lecture-publicité \ *** acceptent le nom ou l’adresse IP d’un serveur d’hébergement Active Directory pour rechercher des informations de récupération ou de GPC. Nous vous recommandons de fournir le nom unique des conteneurs publicitaires dans lesquels l’objet ordinateur réside en tant que valeur du paramètre SearchBase. Si les ordinateurs sont stockés dans plusieurs unités d’organisation, les applets de commande peuvent accepter l’entrée de pipeline pour s’exécuter une seule fois pour chaque conteneur. Le nom unique d’un conteneur d’annonces est semblable à UO = machines, DC = contoso, DC = com. L’exécution d’une recherche ciblant des conteneurs spécifiques offre les avantages suivants:

-   Réduit le risque d’expiration lors de l’interrogation d’un jeu de données AD volumineux pour les objets ordinateur.

-   Il est possible que vous ne puissiez pas ignorer les unités d’organisation contenant des serveurs de centre de gestion ou d’autres classes d’ordinateurs pour lesquels la sauvegarde n’est pas appropriée ou nécessaire.

Une autre option consiste à fournir l’indicateur-recurse avec ou sans le SearchBase facultatif pour rechercher des objets d’ordinateur dans tous les conteneurs sous le SearchBase spécifié ou le domaine complet. Lorsque vous utilisez l’indicateur-recurse, vous pouvez également utiliser le paramètre-MaxPageSize pour contrôler la quantité de mémoire locale et distante requise pour le service de la requête.

Ces applets de applet écrivent dans les objets pipeline de type PsObject. Chaque instance de PsObject contient une clé de récupération de volume unique ou une chaîne de propriétaire de TPM avec son nom d’ordinateur associé, son horodatage ainsi que d’autres informations requises pour la publier dans le magasin de données MBAM.

Les **applets de commande Write-MBAM \ *** acceptent les valeurs de paramètre des informations de récupération issues du pipeline par nom de propriété. Cela permet aux cmdlets d’écriture-MBAM \ * d’accepter la sortie du pipeline des applets de commande (par exemple, Read-ADRecoveryInformation – Server contoso.com-recurse | Write-MbamRecoveryInformation – RecoveryServiceEndpoint mbam.contoso.com).

Les **applets de connexion en écriture-MBAM** : incluent des paramètres facultatifs qui fournissent des options de tolérance de pannes, de journalisation détaillée et de préférences pour WhatIf et Confirm.

Les **applets de connexion en écriture-MBAM \ *** incluent également un paramètre *Time* facultatif dont la valeur est un objet **DateTime** . Cet objet inclut un attribut *type* qui peut être défini sur `Local` , `UTC` ou `Unspecified` . Lorsque le paramètre *Time* est rempli à partir de données provenant de l’annuaire Active Directory, le temps est converti en UTC et ce *type* d’attribut est défini automatiquement sur `UTC` . Toutefois, lors du remplissage du paramètre *Time* à l’aide d’une autre source, telle qu’un fichier texte, vous devez définir explicitement l’attribut *Kind* sur sa valeur appropriée.

**Remarques**  Les applets de action en lecture/publicité ne permettent pas de détecter les comptes d’utilisateurs qui représentent les utilisateurs de l’ordinateur. Des associations de comptes d’utilisateur sont nécessaires pour les éléments suivants:

-   Permettre aux utilisateurs de récupérer des mots de passe/packages de volume à l’aide du portail libre-service

-   Les utilisateurs qui ne sont pas dans le groupe de sécurité des utilisateurs du support technique MBAM avancés tels qu’ils ont été définis au cours de l’installation, en recouvrant au nom d’autres utilisateurs.

 

## <a href="" id="bkmk-autounlock"></a>Configurer MBAM pour déverrouiller automatiquement le TPM après un verrouillage


Vous pouvez configurer MBAM 2,5 SP1 pour déverrouiller automatiquement le TPM en cas de verrouillage. Si la réinitialisation automatique du verrouillage du TPM est activée, MBAM peut détecter qu’un utilisateur est verrouillé, puis obtenir le mot de passe OwnerAuth de la base de données MBAM pour déverrouiller automatiquement le TPM pour l’utilisateur. La fonction de réinitialisation automatique du verrouillage du système d’exploitation n’est disponible que si la clé de récupération du système d’exploitation a été récupérée via le portail libre-service ou le site Web d’administration et de surveillance.

**Important**  Pour activer la réinitialisation automatique du verrouillage du module de plateforme sécurisée, vous devez configurer cette fonctionnalité sur le côté serveur et dans la stratégie de groupe du côté client.

 

-   Pour activer la réinitialisation automatique du verrouillage du TPM côté client, configurez le paramètre de stratégie de groupe «configuration **Computer Configuration** de la réinitialisation automatique du verrouillage du TPM» situé sur les &gt; **modèles d’administration** Configuration ordinateur &gt; **composants Windows** &gt; **MDOP MBAM** &gt; **gestion du client**.

-   Pour activer la réinitialisation automatique du verrouillage du TPM sur le côté serveur, vous pouvez activer la case à cocher «Activer la réinitialisation automatique du verrouillage du TPM» dans l’Assistant Configuration du serveur MBAM lors de l’installation.

    Vous pouvez également activer la réinitialisation automatique du verrouillage du module de plateforme sécurisée dans PowerShell en spécifiant le commutateur «-TPM lockout Auto reset» lors de l’activation du composant WebPart service agent.

Dès qu’un utilisateur entre la clé de récupération BitLocker qu’il a obtenue à partir du portail libre-service ou du site Web d’administration et de surveillance, l’agent MBAM détermine si le TPM est verrouillé. S’il est verrouillé, l’application tente de récupérer le module de plateforme sécurisée OwnerAuth pour l’ordinateur à partir de la base de données MBAM. Si le TPM OwnerAuth est correctement récupéré, il sera utilisé pour déverrouiller le TPM. Le déverrouillage du TPM rend le module de plateforme sécurisée entièrement fonctionnel et l’utilisateur ne sera pas obligé d’entrer le mot de passe de récupération lors de redémarrages ultérieurs à partir du verrouillage du TPM.

La réinitialisation automatique du verrouillage du TPM est désactivée par défaut.

**Remarques**  La réinitialisation automatique du verrouillage du TPM est uniquement prise en charge sur les ordinateurs exécutant la version 1,2 du TPM. Le module de plateforme sécurisée 2,0 fournit une fonctionnalité de réinitialisation automatique de verrouillage intégré.

 

**Le rapport d’audit de récupération inclut des** événements liés à la réinitialisation automatique du verrouillage du TPM. Si une requête est lancée à partir du client MBAM pour récupérer un mot de passe OwnerAuth Les entrées d’audit incluent les événements suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Saisir</th>
<th align="left">Valeur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Source de requête d’audit</p></td>
<td align="left"><p>Déverrouillage de TPM d’agent</p></td>
</tr>
<tr class="even">
<td align="left"><p>Type de clé</p></td>
<td align="left"><p>Hachage du mot de passe TPM</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Description de raison</p></td>
<td align="left"><p>Réinitialisation du TPM</p></td>
</tr>
</tbody>
</table>

 

## <a href="" id="bkmk-secure-databases"></a>Connexion sécurisée à SQL Server


Dans MBAM, SQL Server communique avec SQL Server Reporting Services et les services Web pour le site Web d’administration et de surveillance et le portail libre-service. Nous vous recommandons de sécuriser la communication avec SQL Server. Pour plus d’informations, voir [chiffrement de connexions à SQL Server](https://technet.microsoft.com/library/ms189067.aspx).

Pour plus d’informations sur la sécurisation des sites Web MBAM, voir [planification de la sécurisation des sites Web MBAM](planning-how-to-secure-the-mbam-websites.md).

## <a href="" id="bkmk-accts-groups"></a>Créer des comptes et des groupes


La meilleure pratique pour gérer les comptes d’utilisateur consiste à créer des groupes globaux de domaine et à y ajouter des comptes d’utilisateurs. Pour obtenir une description des comptes et groupes recommandés, voir [planification pour les comptes et groupes MBAM 2,5](planning-for-mbam-25-groups-and-accounts.md).

## <a href="" id="bkmk-logfiles"></a>Utiliser les fichiers journaux de MBAM


Cette section décrit les fichiers journaux du client MBAM et MBAM.

**Fichiers journaux de configuration de MBAM Server**

Le fichier **MBAMServerSetup.exe** génère les fichiers journaux suivants dans le dossier **% temp%** de l’utilisateur au cours de l’installation de MBAM:

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 numéros &gt; . log**

    Enregistre les actions effectuées lors de l’installation de MBAM et la configuration des fonctionnalités de MBAM Server.

-   **Microsoft \ _BitLocker \ _Administration \ _and \ _Monitoring \ _ &lt; 14 \ _numbers &gt;\_0\_MBAMServer.msi. log**

    Consigne une action supplémentaire prise lors de l’installation.

**Fichiers journaux de configuration de MBAM Server**

-   **Journaux des applications et services/Microsoft Windows/MBAM-installation**

    Enregistre les erreurs qui se produisent lorsque vous utilisez des cmdlets Windows PowerShell ou l’Assistant Configuration de MBAM Server pour configurer les fonctionnalités de MBAM Server.

**Fichiers journaux d’installation du client MBAM**

-   **Fichiers MSI de &lt; cinq caractères aléatoires &gt;**

    Enregistre les actions effectuées lors de l’installation du client MBAM.

**MBAM-fichiers journaux Web**

-   Affiche les activités des portails et services Web.

## <a href="" id="bkmk-tde"></a>Examiner les points de TDE de base de données MBAM


La fonction de chiffrement de données (TDE) qui est disponible dans SQL Server est une installation facultative des instances de base de données qui hébergent les fonctionnalités de base de données MBAM.

Avec TDE, vous pouvez effectuer un chiffrement complet en temps réel au niveau de la base de données. TDE est le choix le plus optimal pour le chiffrement en bloc pour répondre aux exigences de conformité aux réglementations ou à la sécurité des données d’entreprise. TDE fonctionne au niveau du fichier, qui est semblable à deux fonctionnalités Windows: le système de fichiers de chiffrement (EFS) et le chiffrement de lecteur BitLocker. Ces deux fonctionnalités chiffrent également les données sur le disque dur. TDE ne remplace pas le chiffrement au niveau de la cellule, EFS ou BitLocker.

Lorsque TDE est activé sur une base de données, toutes les sauvegardes sont chiffrées. Par conséquent, il est nécessaire de veiller à ce que le certificat utilisé pour protéger la clé de chiffrement de la base de données soit sauvegardé et entretenu par la sauvegarde de la base de données. En cas de perte de ce (ou ces certificats), les données ne seront pas lisibles.

Sauvegardez le certificat avec la base de données. Chaque sauvegarde de certificat doit comporter deux fichiers. Ces deux fichiers doivent être archivés. Idéalement pour la sécurité, elles doivent être sauvegardées séparément du fichier de sauvegarde de la base de données. Vous pouvez également envisager d’utiliser la fonctionnalité de gestion des clés extensible (EKM) (voir gestion de clés extensible) pour stocker et gérer les clés utilisées pour TDE.

Pour obtenir un exemple de la façon d’activer TDE pour les instances de base de données MBAM, voir [fonctionnement du chiffrement de données transparent (TDE)](https://technet.microsoft.com/library/bb934049.aspx).

## <a href="" id="bkmk-general-security"></a>Comprendre les considérations générales en matière de sécurité


**Comprenez les risques en matière de sécurité.** Le risque le plus sérieux lors de l’utilisation de l’administration et de la surveillance de BitLocker est que ses fonctionnalités peuvent être compromises par un utilisateur non autorisé qui peut ensuite reconfigurer le chiffrement de lecteur BitLocker et obtenir des données de clé de chiffrement BitLocker sur des clients MBAM. Toutefois, en raison d’une attaque par déni de service, la perte de fonctionnalité MBAM n’a pas de répercussions catastrophiques, contrairement, par exemple, la perte de messages électroniques ou de communications réseau ou la gestion de l’alimentation.

**Sécurisez vos ordinateurs de façon sécurisée**. Il n’y a aucune sécurité sans sécurité physique. Un attaquant qui obtient l’accès physique à un serveur MBAM peut peut-être l’utiliser pour attaquer la base de clients tout entière. Toutes les attaques physiques potentielles doivent être considérées comme présentant un risque élevé et atténuées de manière appropriée. Les serveurs MBAM doivent être stockés dans une salle serveur sécurisée avec un accès contrôlé. Sécurisez ces ordinateurs lorsque les administrateurs ne sont pas présents physiquement en faisant en sorte que le système d’exploitation verrouille l’ordinateur ou à l’aide d’un économiseur d’écran sécurisé.

**Appliquez les mises à jour de sécurité les plus récentes à tous les ordinateurs**. Restez informé des nouvelles mises à jour pour les systèmes d’exploitation Windows, SQL Server et MBAM en vous abonnant au service de notification de sécurité sur le [TechCenter de sécurité](https://go.microsoft.com/fwlink/?LinkId=28819).

**Utiliser des mots de passe forts ou des expressions de passe**. Utilisez toujours des mots de passe forts d’au moins 15 caractères pour tous les comptes d’administrateur de MBAM. N’utilisez jamais de mots de passe vides. Pour plus d’informations sur les concepts de mot de passe, voir [stratégie de mot de passe](https://technet.microsoft.com/library/hh994572.aspx).



## Rubriques connexes


[Planification du déploiement de MBAM2.5](planning-to-deploy-mbam-25.md)

 
## Vous avez une suggestion pour MBAM?
- Ajoutez ou Votez en fonction [de suggestions.](http://mbam.uservoice.com/forums/268571-microsoft-bitlocker-administration-and-monitoring)
- Pour les problèmes liés à MBAM, utilisez le [Forum TechNet MBAM](https://social.technet.microsoft.com/Forums/home?forum=mdopmbam).
 





