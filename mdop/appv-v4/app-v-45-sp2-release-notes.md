---
title: Notes de publication d'App-V4.5SP2
description: Notes de publication d'App-V4.5SP2
author: dansimp
ms.assetid: 1b3a8a83-4523-4634-9f75-29bc22ca5815
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 35cff3b2a2c110a4d8beba883a4cf9332381ea60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10808073"
---
# Notes de publication d'App-V4.5SP2


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

**Important**  Lisez attentivement ces notes de publication avant de procéder à l’installation du système de gestion de Microsoft Application Virtualization. Ces notes de publication contiennent des informations dont vous avez besoin pour installer correctement le système de gestion de la virtualisation des applications. Ces notes de publication contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et la documentation du système de gestion de la virtualisation des applications, la dernière modification doit être considérée comme faisant autorité.

 

Pour obtenir des informations mises à jour sur les problèmes connus, consultez la page Microsoft TechNet sur les [notes de publication de App-V 4,5 SP2](https://go.microsoft.com/fwlink/?LinkId=184640) ( https://go.microsoft.com/fwlink/?LinkId=184640) .

## À propos de Microsoft Application Virtualization 4,5 Service Pack 2


Ces notes de publication ont été mises à jour pour refléter les modifications introduites dans Microsoft Application Virtualization (App-V) 4.5 Service Pack2 (SP2). Ce service pack contient les modifications suivantes:

-   La prise en charge d’Office 2010: App-V 4.5 SP2 prend désormais en charge la virtualisation de Microsoft Office 2010. Pour obtenir des instructions sur le séquençage de Microsoft Office 2010 avec App-V 4,5 SP2, voir [instructions d’ordre du classement d’Office 2010 dans Microsoft App-v 4,6](https://go.microsoft.com/fwlink/?LinkId=191539) ( https://go.microsoft.com/fwlink/?LinkId=191539) .

-   Prise en charge de la mise en miroir de base de données: App-V 4.5 SP2 prend désormais en charge la mise en miroir de base de données Microsoft SQL Server. Pour plus d’informations sur la configuration de la mise en miroir de base de données dans votre environnement App-V, voir Configuration de la [prise en charge de la mise en miroir de Microsoft SQL Server pour App-v](https://go.microsoft.com/fwlink/?LinkId=190880) ( https://go.microsoft.com/fwlink/?LinkId=190880) .

-   Commentaires des clients et correctif cumulatif: App-V 4.5 SP2 inclut également un correctif cumulatif pour résoudre les problèmes détectés après la publication de l’application-V 4.5 SP1. Les mises à jour concernent une combinaison de problèmes connus et de commentaires des clients provenant des équipes internes Microsoft, des partenaires et des clients qui utilisent App-V 4.5. Pour obtenir la liste complète des mises à jour, reportez-vous à l’article 980847 de la base de connaissances Microsoft, à la [Description de Microsoft application virtualization 4,5 Service Pack 2](https://go.microsoft.com/fwlink/?LinkId=191540) ( https://go.microsoft.com/fwlink/?LinkId=191540) .

## À propos de la documentation relative aux produits


La documentation complète pour la virtualisation des applications (App-V) est disponible sur Microsoft TechNet dans la [bibliothèque TechCenter](https://go.microsoft.com/fwlink/?LinkId=122939) de la virtualisation des applications ( https://go.microsoft.com/fwlink/?LinkId=122939) . La documentation TechNet inclut l’aide en ligne pour le Sequencer de virtualisation d’application, les clients de virtualisation d’application et le serveur de virtualisation des applications. Il inclut également le Guide de planification et de déploiement de l’application virtualisation du Guide des opérations de virtualisation des applications.

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité, nous vous recommandons d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, reportez-vous à la rubrique [sécurité Microsoft](https://go.microsoft.com/fwlink/?LinkId=3482) ( https://go.microsoft.com/fwlink/?LinkId=3482) .

## Fournir des commentaires


Vous pouvez fournir des commentaires, formuler une suggestion ou signaler un problème avec le système de gestion Microsoft Application Virtualization (App-V) via le Forum de la communauté sur le Forum de documentation de l’application virtualisation d’application [-v](https://go.microsoft.com/fwlink/?LinkId=122917) ( https://go.microsoft.com/fwlink/?LinkId=122917) .

Vous pouvez également envoyer vos commentaires sur la documentation directement à l’équipe de documentation de l’application-V à l’adresse <appvdocs@microsoft.com> .

## Problèmes connus liés à Application Virtualization 4.5 SP2


Cette section fournit les informations les plus récentes sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.5 SP2. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures du logiciel.

### Conseils pour l’installation de la console de gestion du serveur

Si vous avez besoin d’installer le logiciel de gestion sur des systèmes autres que la première publication de la virtualisation des applications et sur les serveurs de diffusion en continu, l’installation du serveur prend en charge l’installation de la console de gestion des applications et des services Web sur des serveurs distincts à partir du serveur d’administration principal de l’application. Pour distribuer les composants de gestion sur plusieurs serveurs, la délégation Kerberos doit être activée sur le serveur sur lequel est installé le service Web Application Virtualization. Pour plus d’informations sur la façon d’activer cette prise en charge, voir [configuration du serveur pour être approuvé pour la délégation](https://go.microsoft.com/fwlink/?LinkId=166682) ( https://go.microsoft.com/fwlink/?LinkId=166682) .

### Instructions d’installation ou de mise à niveau des clients vers App-V 4.5 SP2 à l’aide de Setup.msi

Lors de l’installation ou de la mise à niveau de vos clients application-V vers App-V 4,5 SP2 à l’aide de Setup.msi, les composants requis ne sont pas installés automatiquement.

Contournementvous doit installer manuellement les éléments requis avant d’installer ou de mettre à niveau les clients App-V vers App-V 4.5 SP2. Pour plus d’informations sur l’installation des éléments requis et du client App-V, voir [Comment installer le client à l’aide de la ligne de commande](https://go.microsoft.com/fwlink/?LinkId=144106) ( https://go.microsoft.com/fwlink/?LinkId=144106) .

Lorsque vous avez terminé, installez les clients App-V 4,5 SP2 en utilisant Setup.msi avec des informations d’identification d’administration. Ce fichier est disponible dans la version multimédia App-V 4,5 SP2 dans le dossier Installers\\Client

Lors de l’installation du rapport d’erreurs de l’application Microsoft, utilisez la commande suivante si vous installez ou effectuez la mise à niveau vers le client de bureau App-V 4,5 SP2:

**msiexec/i dw20shared.msi APPGUID = {C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D} ALLUSERS = 1 reboot = supprimer, = All REINSTALLMODE = vomus**

Par ailleurs, si vous procédez à l’installation ou à la mise à niveau vers le client App-V 4,5 SP2 pour les services Bureau à distance, utilisez la commande suivante:

**msiexec/i dw20shared.msi APPGUID = {ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5} ALLUSERS = 1 reboot = supprimer, = All REINSTALLMODE = vomus**

**Remarque**  
-   Le paramètre APPGUID référence le code de produit des clients App-V que vous installez ou mettez à niveau. Le code de produit est unique pour chaque Setup.msi. Vous pouvez utiliser l’éditeur de base de données Orca ou un outil similaire pour examiner les fichiers Windows Installer et déterminer le code de produit. Cette étape est nécessaire pour toutes les installations ou mises à niveau vers App-V 4,5 SP2.

-   Cette étape n’est pas obligatoire si vous effectuez une mise à niveau et que vous avez déjà installé Dw20shared.msi.

 

### Amélioration des performances lors du séquençage du .NET Framework

Lorsque vous séquençagez Microsoft .NET Framework, vous risquez de réduire les performances du système, car le service .NET Framework NGEN tente de précompiler des assemblys en tant que tâche en arrière-plan.

WORKAROUNDWhen-xxxxxxx xxxxxxxxx xxxxxxxxx xxxxxxx xxxxxxxxx xxxxxxx xxxxxxxx Mscorsvw.exe (xxx) XXX xxxxxxxxx xxxxxxx. Vous devez utiliser l’onglet **service virtuel** dans le Sequencer App-V et définir le type de démarrage sur **Disabled**.

### Lorsque vous désinstallez le client Microsoft Application Virtualization, les paramètres utilisateur associés à l’utilisateur effectuant la désinstallation sont supprimés.

Lorsque vous désinstallez le client App-V, le programme d’installation Windows supprime du profil de l’utilisateur actuel. Si votre ordinateur utilise des profils d’itinérance, n’utilisez pas votre compte réseau personnel pour désinstaller le client, car cela a pour effet de supprimer les paramètres de vos applications virtuelles sur tous vos ordinateurs.

Contournementvous doit désinstaller le client App-V avec un compte d’administrateur qui n’est pas utilisé pour exécuter des applications virtuelles.

### Les modifications apportées sur le système de fichiers virtuel et les onglets du Registre virtuel doivent être enregistrées lors de l’exécution de l’Assistant séquençage.

Si vous ouvrez un package pour effectuer une mise à niveau, ou si vous avez déjà exécuté l’Assistant séquençage avec un nouveau package et apporté des modifications au package dans les onglets système de fichiers virtuel ou registre virtuel, ces modifications ne sont pas enregistrées automatiquement.

WORKAROUNDSave les modifications avant de réexécuter l’Assistant pour vérifier qu’elles sont reflétées dans l’environnement virtuel de l’Assistant.

### Le Sequencer de la ligne de commande doit être exécuté à partir d’une invite de commandes avec élévation de privilèges

Lorsque vous utilisez le Sequencer de ligne de commande, il ne demande pas d’élévation.

WORKAROUNDRunz le Sequencer de la ligne de commande à l’aide d’une invite de commandes avec élévation de privilèges.

### Les noms de variables de chemin court dans les fichiers OSD peuvent provoquer des erreurs

Si vous recevez un message d’erreur 450478-1F702339-0000010B "le nom du répertoire n’est pas valide" lors du démarrage d’une application virtuelle sur le client, il est possible que la variable dans l’OSD soit définie de manière incorrecte. Cela peut se produire si le programme d’installation de l’application définit un nom de chemin court au cours du séquençage.

WORKAROUNDRemove le tilde de fin de n’importe quelle variable CSIDL qui existe dans le fichier OSD.

### <a href="" id="correct-syntax-for-decodepath-parameter-for-command-line-sequencer-"></a>Syntaxe correcte pour le paramètre DECODEPATH pour le Sequencer de ligne de commande

Dans le Sequencer de ligne de commande, lors de l’ouverture d’un package pour la mise à niveau et de son décodage à la racine du lecteur Q, la syntaxe du paramètre *DECODEPATH* ne doit pas inclure de barre oblique de fin.

Contournementvous pouvez utiliser **Q:** plutôt que **Q:\\** (en omettant le caractère «\ \» de fin).

### <a href="" id="when-upgrading-app-v-4-2-packages--you-encounter-problems-caused-by-windows-installer-files-in-the-virtual-file-system-"></a>Lors de la upgradingAPP-V 4,2 packages, vous rencontrez des problèmes liés aux fichiers Windows Installer dans le système de fichiers virtuel

Lors de la mise à niveau d’un package à partir de APP-V 4.2, il est possible que vous rencontriez des problèmes liés à une incompatibilité entre les fichiers du système Windows Installer inclus par défaut dans APP-V 4.2 et les bibliothèques Windows Installer en local sur votre station de travail de séquençage. Les fichiers suivants sont situés en CSIDL \ _SYSTEM \ \:

Cabinet.dll

Msi.dll

Msiexec.exe

Msihnd.dll

Msimsg.dlll

WORKAROUNDDelete tous les fichiers précédents du package. Supprimez les mappages de l’onglet **VFS** et des fichiers réels dans le dossier CSIDL \ _SYSTEM dans votre chemin de décodage.

### <a href="" id="on-windows-xp--by-default--client-installation-logging-is-not-enabled-"></a>Sur WindowsXP, par défaut, la journalisation de l’installation du client n’est pas activée

Lors de l’installation du client, pour vérifier que toutes les erreurs d’installation sont capturées lors de la résolution des problèmes, vous devez activer la journalisation à l’aide de la ligne de commande.

WORKAROUNDAdd le paramètre */l\ * VX! log.txt* à la ligne de commande, comme le montre l’exemple suivant:

**setup.exe/s/v "/qn/l\ * VX! log.txt "**

**msiexec.exe/i setup.msi/qn/l\ * VX! log.txt**

Vous pouvez également définir la clé de Registre sur la valeur suivante:

**\ [HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Policies\\Microsoft\\Windows\\Installer\] "Logging" = "voicewarmupx!"**

### Pour que l’authentification Kerberos fonctionne, les noms de principal de service doivent être inscrits pour IIS

Lorsque vous utilisez Internet Information Services (IIS) 6.0 orIIS 7.0 pour l’extraction de fichiers d’icônes ou d’OSD et la diffusion en continu de packages, le SPN doit être enregistré comme suit:

-   Sur le serveur IIS, exécutez les commandes suivantes à l’aide de l’outil Kit de ressources de SETSPN.EXE. Le nom de domaine complet (FQDN) du serveur doit être utilisé.

    **Setspn-r SOFTGRID/ &lt; FQDN du serveur&gt;**

    **Nom de domaine complet setspn-r HTTP/ &lt; serveur&gt;**

Pour plus d’informations, reportez-vous à [authentification intégrée de Windows (IIS 6,0)](https://go.microsoft.com/fwlink/?LinkId=131407) ( https://go.microsoft.com/fwlink/?LinkId=131407) .

### Changements de compatibilité .NET

Microsoft Application Virtualization (App-V) cumulative update1 ou version ultérieure prend en charge le séquençage du .NET Framework sur WindowsXP SP2 ou version ultérieure. Les routines de séquençage pour les applications .NET qui ont été écrites pour SoftGrid 4.2 peuvent être mises à jour lorsqu’elles sont utilisées avec le Sequencer App-V 4,5. Pour plus d’informations et de solutions de contournement, voir l’article TechCenter sur la [prise en charge de .net dans Microsoft application virtualization 4,5](https://go.microsoft.com/fwlink/?LinkId=123412) ( https://go.microsoft.com/fwlink/?LinkId=123412) .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Après la mise à niveau du client à partir de App-V 4.2, certaines applications ne sont pas affichées

Recherchez l’erreur suivante dans le journal: «le client de virtualisation des applications n’a pas pu analyser le fichier OSD». Le client App-V 4,5 filtre les applications qui disposent d’un fichier OSD contenant une balise de système d’exploitation vide &lt; &gt; &lt; &gt; .

WORKAROUNDDelete la balise de système d’exploitation vide du fichier OSD.

### Le serveur App-V nécessite des exemptions dans son pare-feu pour certains processus

Pour que le serveur diffuse correctement les applications, le processus principal du serveur, y compris le répartiteur, doit avoir accès via le pare-feu.

WORKAROUNDSet d’exemption dans le pare-feu du serveur pour les processus suivants: Sghwsvr.exe et Sghwdsptr.exe. Cela s’applique au serveur de gestion application-V et au serveur de streaming App-V.

### Lorsque le programme d’installation du serveur est exécuté en mode silencieux, il ne vérifie pas correctement le fichier MSXML6

Le serveur de gestion de l’application-V dépend de MSXML6. Toutefois, si vous exécutez le programme d’installation en mode silencieux, par exemple à l’aide de la commande **msiexec-i setup.msi/qn** sur un système sur lequel MSXML6 n’est pas installé, le programme d’installation ne détecte pas de dépendance manquante et ne peut tout de même être installé. Par conséquent, lorsque des clients essaient d’actualiser des informations de publication à partir du serveur de gestion App-V, ils reçoivent des erreurs.

WORKAROUNDVerifyx, xxx xxx xxxxxxx xxx xxxxxxx xxx xxxxxxx xxx XXXXXXX XXXXXXX XXXXXXX xxx xxxxxxx.

### Code d’erreur 000C800 lorsque vous tentez de vous connecter à la console de gestion des applications virtuelles

Un administrateur de virtualisation des applications qui n’est pas un administrateur local sur le serveur de service Web de gestion des applications reçoit une erreur (code d’erreur: 000C800) lorsque vous tentez de vous connecter à la console de gestion App-V, et l’entrée sftmmc. log indique que l’accès à SftMgmt. UDL est refusé. Pour établir une connexion réussie à la console de gestion des applications, un administrateur ne disposant pas des droits d’administrateur local sur le serveur de service Web de gestion des applications doit avoir au moins des autorisations de lecture et d’exécution sur le fichier SftMgmt. UDL.

Les administrateurs d’applications virtuelles doivent disposer d’autorisations de lecture et d’exécution sur le fichier SftMgmt. UDL dans le dossier%systemdrive%\\Program Files\\Microsoft Virt d’application gestion Server\\App Virt service de gestion.

### Les paramètres de ligne de commande du programme d’installation du client sont ignorés quand ils sont utilisés conjointement avec KEEPCURRENTSETTINGS = 1

Quand elle est utilisée conjointement avec KEEPCURRENTSETTINGS = 1, les paramètres de ligne de commande du programme d’installation du client suivants sont ignorés: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA et REQUIRESECURECONNECTION.

WORKAROUNDIf vous avez des paramètres que vous voulez conserver, utilisez KEEPCURRENTSETTINGS = 1, puis définissez les autres paramètres après le déploiement. Le modèle ADM App-V peut être utilisé pour définir les paramètres du client suivants: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES et ALLOWINDEPENDENTFILESTREAMING. Vous pouvez télécharger le modèle ADM à partir du centre de téléchargement Microsoft sur le modèle [d’administration Microsoft Application Virtualization (modèle ADM)](https://go.microsoft.com/fwlink/?LinkId=121835) ( https://go.microsoft.com/fwlink/?LinkId=121835) .

### Informations de copyright des notes de publication

Ce document est fourni «en l’état». Les informations contenues dans ce document, y compris les URL et autres références de sites Web, pourront faire l’objet de modifications sans préavis. Vous assumez le risque d’utilisation.

Quelques exemples présentés dans les présentes sont fournis à titre indicatif uniquement et sont fictifs.Aucune association ou connexion réelle ne doit être intentionnelle ou intentionnelle.

Ce document ne vous fournit aucun droit légal de propriété intellectuelle de tout produit Microsoft. Vous pouvez copier le présent document pour une utilisation interne à des fins de référence. Vous pouvez modifier ce document à des fins de référence interne.



Microsoft, Active Directory, ActiveSync, MS-DOS, Windows, windowsserver2003 et Windows Vista sont des marques commerciales du groupe de sociétés Microsoft.

Toutes les autres marques déposées sont la propriété de leurs détenteurs respectifs.

 

 





