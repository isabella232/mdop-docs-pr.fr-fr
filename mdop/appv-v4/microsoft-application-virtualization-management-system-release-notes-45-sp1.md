---
title: Notes de publication du système de gestion des applications Microsoft application 4,5 SP1
description: Notes de publication du système de gestion des applications Microsoft application 4,5 SP1
author: dansimp
ms.assetid: 5d6b11ea-7b87-4084-9a7c-0d831f247aa3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 5c24d2e98ad09460ca22e4b29d75ae2b9c72d0bf
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806594"
---
# Notes de publication du système de gestion des applications Microsoft application 4,5 SP1


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

**Important**  Lisez attentivement ces notes de publication avant d’installer le système de gestion de la virtualisation des applications. Ces notes de publication contiennent des informations dont vous avez besoin pour installer correctement le système de gestion de la virtualisation des applications. Ces notes de publication contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et la documentation du système de gestion de la virtualisation des applications, la dernière modification doit être considérée comme faisant autorité.

 

Pour obtenir des informations à jour sur les problèmes connus, consultez la page sur le site Microsoft TechNet <https://go.microsoft.com/fwlink/?LinkId=122918> .

## À propos de Microsoft Application Virtualization 4,5 Service Pack 1


Ces notes de publication ont été mises à jour pour refléter les modifications introduites dans Microsoft Application Virtualization (App-V) 4.5 Service Pack1 (SP1). Ce service pack contient les modifications suivantes:

-   Prise en charge de Windows 7 et Windows Server 2008 R2: App-V 4,5 SP1 fournit une prise en charge pour Windows 7 et Windows Server 2008 R2, y compris la prise en charge des fonctionnalités de Windows 7 telles que la barre des tâches, AppLocker, BranchCache et BitLocker to go.La prise en charge de Windows Server 2008 R2 est réservée au serveur de virtualisation des applications. Pour plus d’informations sur la prise en charge d’AppLocker dans Windows 7, voir <https://go.microsoft.com/fwlink/?LinkID=156732> .

-   Prise en charge des domaines Kerberos tiers: App-V 4,5 SP1 fournit une prise en charge des environnements disposant d’une relation d’approbation et de comptes d’utilisateurs mappés entre un domaine Windows et un domaine Kerberos MIT, qui est un scénario courant dans de nombreuses universités. Pour plus d’informations sur la façon d’activer cette prise en charge, consultez le site Microsoft TechNet Library à l’adresse <https://go.microsoft.com/fwlink/?LinkId=166004> .

-   Prise en charge améliorée de la publication d’applications et de la diffusion en continu via HTTP/HTTPs: App-V 4,5 SP1 fournit une prise en charge de la publication d’applications et de la diffusion en continu via les protocoles HTTP/HTTPs pour Windows XP Édition familiale, Windows Vista Édition familiale basique et Windows 7 Édition familiale basique.

-   Commentaires des clients et correctif cumulatif: App-V 4.5 SP1 inclut également un cumul des correctifs pour résoudre les problèmes détectés depuis la version 4.5 de Microsoft Application Virtualization (App-V) 4.5 CU1. Les mises à jour sont le résultat d’une combinaison de problèmes connus et de commentaires des clients provenant de nos équipes, partenaires et clients internes utilisant App-V 4.5. Pour obtenir la liste complète des mises à jour, consultez l’article de la base de connaissances à l’adresse <https://go.microsoft.com/fwlink/?LinkId=167121> .

## À propos de la documentation relative aux produits


La documentation complète pour la virtualisation des applications (App-V) est disponible sur Microsoft TechNet dans le TechCenter Application Virtualization (App-V) <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentation TechNet inclut l’aide en ligne pour le Sequencer d’application Virtualization, le client de virtualisation d’application et le serveur de virtualisation des applications. Il inclut également le Guide de planification et de déploiement de l’application virtualisation du Guide des opérations de virtualisation des applications.

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité, nous vous recommandons d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, consultez le site Web de sécurité Microsoft à l’adresse <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Fournir des commentaires


Vous pouvez fournir des commentaires, formuler une suggestion ou signaler un problème avec le système de gestion Microsoft Application Virtualization (App-V) par le biais d’un forum de la communauté sur le TechCenter Microsoft Application Virtualization ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

Vous pouvez également envoyer vos commentaires directement dans la documentation à l’équipe de documentation de l’application-V. Envoyez votre commentaires de documentation à appvdocs@microsoft.com.

## Problèmes connus liés à la virtualisation des applications 4.5 SP1


Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.5 SP1. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures du logiciel.

### Conseils pour l’installation de la console de gestion du serveur

Si vous avez besoin d’installer le logiciel de gestion sur des systèmes autres que la publication principale d’application et le serveur de diffusion en continu, l’installation du serveur prend en charge l’installation de la console de gestion et du service Web de gestion sur des serveurs distincts à partir du serveur d’administration principal de l’application-V. Pour distribuer les composants de gestion sur plusieurs serveurs, la délégation Kerberos doit être activée sur le serveur sur lequel est installé le service Web. Pour plus d’informations sur l’activation de cette prise en charge, consultez la page Microsoft TechNet sur <https://go.microsoft.com/fwlink/?LinkId=166682>

### Instructions d’installation ou de mise à niveau des clients vers App-V 4.5 SP1 à l’aide de setup.msi

Lors de l’installation ou de la mise à niveau de vos clients application-V vers App-V 4,5 SP1 à l’aide de setup.msi, les composants requis ne sont pas installés automatiquement.

Contournementvous doit installer manuellement les éléments requis avant d’installer ou de mettre à niveau le client App-V toApp-V 4,5 SP1. Pour plus d’informations sur l’installation des éléments requis et du client App-V, voir <https://go.microsoft.com/fwlink/?LinkId=144106> .

Une fois cette opération effectuée, installez le client App-V 4,5 SP1 en utilisant setup.msi avec des privilèges élevés. Ce fichier est disponible dans la version Media App-V 4,5 SP1 du dossier Installers\\Client

Lors de l’installation du rapport d’erreurs de l’application Microsoft, utilisez la commande suivante si vous installez ou effectuez la mise à niveau vers le client de bureau App-V 4,5 SP1:

    msiexec /i dw20shared.msi APPGUID={93468B43-C19D-44F9-8BCC-114076DB0443}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Par ailleurs, si vous procédez à l’installation ou à la mise à niveau vers le client App-V 4,5 SP1 pour les services Bureau à distance, utilisez la commande suivante:

    msiexec /i dw20shared.msi APPGUID={0042AD3C-99A4-4E58-B5F0-744D5AD96E1C} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Remarques**  Le paramètre APPGUID référence le code de produit du client App-V que vous installez ou mettez à niveau. Le code de produit est unique pour chaque setup.msi. Vous pouvez utiliser l’éditeur de base de données Orca ou un outil similaire pour examiner les fichiers Windows Installer et déterminer le code de produit. Cette étape est nécessaire pour toutes les installations ou mises à niveau vers App-V 4,5 SP1.

 

### Amélioration des performances lors du séquençage du .NET Framework

Lorsque vous séquençagez .NET Framework, vous pouvez bénéficier d’une diminution des performances du système, car le service Microsoft .NET Framework NGEN tente de précompiler des assemblys en tant que tâche en arrière-plan.

WORKAROUNDWhen-xxxxxxx xxxxxxxxx xxxxxxxxx xxxxxxx xxxxxxxxx xxxxxxx xxxxxxxx mscorsvw.exe (xxx) XXXXXXX XXXXXXX Vous devez utiliser l’onglet **Virtual Services** dans le Sequencer et définir le type de démarrage sur Disabled.

### Lorsque vous désinstallez le client Microsoft Application Virtualization, les paramètres utilisateur associés à l’utilisateur effectuant la désinstallation seront supprimés.

Lorsque vous désinstallez le client App-V, le programme d’installation Windows supprime du profil de l’utilisateur actuel les paramètres de virtualisation des applications. Si votre ordinateur utilise des profils d’itinérance, n’utilisez pas votre compte réseau personnel pour désinstaller le client, car cela a pour effet de supprimer les paramètres de vos applications virtuelles sur tous vos ordinateurs.

Contournementvous doit effectuer la désinstallation du client App-V avec un compte d’administrateur qui n’est pas utilisé pour exécuter des applications virtuelles.

### Les modifications apportées sur le système de fichiers virtuel et les onglets du Registre virtuel doivent être enregistrées lors de l’exécution de l’Assistant séquençage.

Si vous ouvrez un package pour effectuer une mise à niveau, ou si vous avez déjà exécuté l’Assistant séquençage avec un nouveau package et apporté des modifications au package dans les onglets système de fichiers virtuel ou registre virtuel, ces modifications ne sont pas enregistrées automatiquement.

WORKAROUNDSave les modifications avant de réexécuter l’Assistant pour vérifier qu’elles sont reflétées dans l’environnement virtuel de l’Assistant.

### Le Sequencer de la ligne de commande doit être exécuté à partir d’une invite de commandes avec élévation de privilèges

Lorsque vous utilisez le Sequencer de ligne de commande, il ne demande pas d’élévation.

WORKAROUNDRun le Sequencer de la ligne de commande à l’aide d’une invite de commandes avec élévation de privilèges.

### Les noms de variables de chemin court dans les fichiers OSD peuvent provoquer des erreurs

Si vous recevez un message d’erreur 450478-1F702339-0000010B "le nom du répertoire n’est pas valide" lors du démarrage d’une application virtuelle sur le client, il est possible que la variable dans l’OSD soit définie de manière incorrecte. Cela peut se produire si le programme d’installation de l’application définit un nom de chemin court au cours du séquençage.

WORKAROUNDRemove le tilde de fin de n’importe quelle variable CSIDL qui existe dans le fichier OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Syntaxe correcte pour le paramètre DECODEPATH pour le Sequencer de ligne de commande

Dans le Sequencer de ligne de commande, lors de l’ouverture d’un package de mise à niveau et de décodage à la racine du lecteur Q, la syntaxe du paramètre *DECODEPATH* ne doit pas inclure de barre oblique de fin.

Contournementvous pouvez utiliser **Q:** plutôt que **Q:\\** (en omettant le caractère «\ \» de fin).

### <a href="" id="when-upgrading-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Lors de la mise à niveau des packages 4.2, vous rencontrez des problèmes liés aux fichiers Windows Installer dans le système de fichiers virtuel

Lors de la mise à niveau d’un package à partir de la version 4.2, il est possible que vous rencontriez des problèmes liés à une incompatibilité entre les fichiers du système d’installation Windows qui ont été inclus par défaut dans la version 4.2 et les bibliothèques Windows Installer locales sur votre station de travail de séquençage. Les fichiers suivants sont situés en CSIDL \ _SYSTEM \ \:

cabinet.dll

msi.dll

msiexec.exe

msihnd.dll

msimsg.dlll

WORKAROUNDDelete tous les fichiers précédents du package. Supprimez les mappages sous l’onglet **VFS** ainsi que les fichiers réels dans le dossier CSIDL \ _SYSTEM dans votre chemin de décodage.

### <a href="" id="on-windows-xp--client-install-logging-is-not-enabled-by-default-"></a>Sur WindowsXP, la journalisation de l’installation du client n’est pas activée par défaut

Lors de l’installation du client, pour vérifier qu’aucune erreur d’installation n’est capturée, vous devez activer la journalisation à l’aide de la ligne de commande.

WORKAROUNDAdd le paramètre */l\ * VX! log.txt* à la ligne de commande, comme le montre l’exemple suivant:

setup.exe/s/v "/qn/l\ * VX! log.txt "

msiexec.exe/i setup.msi/qn/l\ * VX! log.txt

Vous pouvez également définir la clé de Registre sur la valeur suivante:

\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"

### Pour que l’authentification Kerberos fonctionne, les noms de principal de service doivent être inscrits pour IIS

Dans le cadre de l’utilisation des services Internet (IIS) 6.0 ou 7.0 pour la récupération et la diffusion en continu des packages d’icônes ou de fichiers OSD, le SPN doit être inscrit comme suit:

-   Sur le serveur IIS, exécutez les commandes suivantes à l’aide de l’outil Kit de ressources de SETSPN.EXE. Le nom de domaine complet (FQDN) du serveur doit être utilisé.

    Setspn-r SOFTGRID/ &lt; FQDN du serveur&gt;

    Nom de domaine complet setspn-r HTTP/ &lt; serveur&gt;

Pour plus d’informations, voir <https://go.microsoft.com/fwlink/?LinkId=131407>.

### Changements de compatibilité .NET

Microsoft Application Virtualization (App-V) cumulative update1 ou version ultérieure prend en charge le séquençage du .NET Framework sur WindowsXP (SP2 ou version ultérieure). Les routines de séquençage pour les applications .NET qui ont été écrites pour SoftGrid 4.2 peuvent avoir besoin d’être mises à jour lorsqu’elles sont utilisées avec le Sequencer App-V 4,5. Pour plus d’informations et de solutions de contournement, consultez l’article de la base de connaissances à l’adresse <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Après la mise à niveau du client à partir de App-V 4.2, certaines applications ne sont pas affichées

Recherchez l’erreur suivante dans le journal: «le client de virtualisation des applications n’a pas pu analyser le fichier OSD». Le client App-V 4,5 filtre les applications qui disposent d’un fichier OSD contenant une balise de système d’exploitation vide ( &lt; OS &gt; &lt; /OS &gt; ).

WORKAROUNDDelete la balise de système d’exploitation vide du fichier OSD.

### Le serveur App-V nécessite des exemptions dans son pare-feu pour certains processus

Pour que le serveur diffuse correctement les applications, le processus principal du serveur, y compris le répartiteur, doit avoir accès via le pare-feu.

WORKAROUNDSet d’exemption dans le pare-feu du serveur pour les processus suivants: sghwsvr.exe et sghwdsptr.exe. Cela s’applique au serveur de gestion application-V et au serveur de streaming App-V.

### Lorsque le programme d’installation du serveur est exécuté en mode silencieux, il ne vérifie pas correctement le fichier MSXML6

Le serveur de gestion de l’application-V dépend de MSXML6. Toutefois, si vous exécutez le programme d’installation en mode silencieux, par exemple à l’aide de la commande «msiexec-i setup.msi/qn» sur un système sur lequel MSXML6 n’est pas installé, le programme d’installation ne détecte tout de même le niveau de dépendance manquant. Par conséquent, lorsque des clients tentent d’actualiser des informations de publication à partir du serveur de gestion App-V, ils verront des échecs.

WORKAROUNDVerifyx, xxx xxx xxxxxxx xxx XXXXXXX XXXXXXX xxx XXXXXXX XXXXXXX xxx xxxxxxx xxx xxxxxxx.

### Code d’erreur 000C800 lorsque vous tentez de vous connecter à la console de gestion des applications virtuelles

Un administrateur de virtualisation des applications qui n’est pas un administrateur local sur le serveur de service Web de l’application-V va recevoir une erreur (code d’erreur: 000C800) lorsque vous tentez de vous connecter à la console de gestion App-V, et l’entrée sftmmc. log indique que l’accès à SftMgmt. UDL est refusé. Pour établir une connexion réussie à la console de gestion des applications, un administrateur ne disposant pas des droits d’administrateur local sur le serveur de service Web de gestion des applications doit avoir au moins des autorisations de lecture et d’exécution sur le fichier SftMgmt. UDL.

Les administrateurs de la virtualisation des applications doivent disposer d’autorisations de lecture et d’exécution sur le fichier SftMgmt. UDL sous%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt service de gestion.

### Les paramètres de ligne de commande du programme d’installation du client sont ignorés quand ils sont utilisés conjointement avec KEEPCURRENTSETTINGS = 1

Quand elle est utilisée conjointement avec KEEPCURRENTSETTINGS = 1, les paramètres de ligne de commande du programme d’installation du client suivants sont ignorés: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA et REQUIRESECURECONNECTION.

WORKAROUNDIf vous avez des paramètres que vous voulez conserver, utilisez KEEPCURRENTSETTINGS = 1, puis définissez les autres paramètres après le déploiement. Le modèle ADM App-V peut être utilisé pour définir les paramètres du client suivants: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES et ALLOWINDEPENDENTFILESTREAMING. Le modèle ADM est disponible à l’adresse <https://go.microsoft.com/fwlink/?LinkId=121835> .

## Informations de copyright des notes de publication


Les informations contenues dans ce document, y compris les URL et autres références de site Web Internet, peuvent faire l’objet de modifications sans préavis et fournies à titre informatif uniquement. Le risque qu’une utilisation ou des résultats résultant de l’utilisation de ce document reste l’utilisateur, et Microsoft Corporation ne fournit aucune garantie, expresse ou implicite. Sauf mention contraire, les sociétés, organisations, produits, noms de domaines, adresses de messagerie, logos, personnes, lieux et événements décrits dans les exemples ci-dessous sont fictifs. Il n’est pas possible d’associer une société, une organisation, un produit, un nom de domaine, une adresse de messagerie, un logo, une personne, un lieu ou un événement. Conformément à toutes les lois applicables en matière de copyright, il incombe à l’utilisateur. Sans limiter les droits découlant du droit d’auteur, aucune partie de ce document ne pourra être reproduite, stockée ou introduite dans un système de récupération, ni transmise à l’aide d’un moyen quelconque (électronique, mécanique, photocopie, enregistrement ou autre), ou à d’autres fins, sans l’autorisation écrite rapide de Microsoft Corporation.

Microsoft peut être doté d’un brevet, d’une demande de brevet, de marques commerciales, de droits d’auteur ou d’autres droits de propriété intellectuelle concernant le sujet figurant dans ce document. À l’exception de ce que prévoit expressément un contrat de licence écrit de la part de Microsoft, la fourniture de ce document ne vous donne aucune licence pour ces brevets, marques commerciales, droits d’auteur ou toute autre propriété intellectuelle.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, windowsserver2003 et Windows Vista sont des marques commerciales du groupe de sociétés Microsoft.

Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.

 

 





