---
title: Notes de publication sur le système de gestion des applications Microsoft application
description: Notes de publication sur le système de gestion des applications Microsoft application
author: dansimp
ms.assetid: e1a4d5ee-53c7-4b48-814c-a34ce0e698dc
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: c34abab9a49bd69f760a9b531d0950cc581253c1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806597"
---
# Notes de publication sur le système de gestion des applications Microsoft application


Pour effectuer une recherche dans ces notes de publication, appuyez sur CTRL + F.

**Important**  Lisez attentivement ces notes de publication avant d’installer le système de gestion de la virtualisation des applications. Ces notes de publication contiennent des informations dont vous avez besoin pour installer correctement le système de gestion de la virtualisation des applications. Ce document contient des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et la documentation du système de gestion de la virtualisation des applications, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu fourni avec ce produit.

 

Pour obtenir des informations à jour sur les problèmes connus, consultez la page sur le site Microsoft TechNet <https://go.microsoft.com/fwlink/?LinkId=122918> .

## À propos de Microsoft Application Virtualization 4,5 Update cumulative 1


Ces notes de publication ont été mises à jour pour refléter les modifications introduites à l’aide de Microsoft Application Virtualization 4.5 cumulative update1 (App-V 4.5 CU1), qui fournit les mises à jour les plus récentes de l’application virtualisation (App-V) 4.5. Cette mise à jour cumulative contient les modifications suivantes:

-   Prise en charge de la version bêta d’Server2008R2 et de Windows CU1 bêta: App-V 4.5 répond aux problèmes de compatibilité liés à la version bêta d’un Windows Server2008R2 Beta. Une assistance sera fournie pour les problèmes de blocage qui empêchent l’exécution d’App-V 4.5 CU1 dans un environnement de test sur les versions préliminaires d’une application. Cela permet de s’assurer que vos applications virtuelles peuvent s’exécuter correctement dans un environnement de test dans lequel la compatibilité entre le client App-V 4.5 et la version bêta de l’application Beta est requise.

    **Important**  L’exécution de App-V 4.5 CU1 sur n’importe quelle version de votre ordinateur ou de Windows Server2008R2 dans un environnement d’exploitation en direct n’est pas prise en charge.

     

-   Prise en charge améliorée du séquençage de .NET Framework: App-V 4.5 CU1 répond aux problèmes précédents liés au séquençage de .NET Framework 3.5 et versions antérieures sur WindowsXP (SP2 ou version ultérieure). Pour plus d’informations sur les nouvelles fonctionnalités, voir l’article TechNet sur le site <https://go.microsoft.com/fwlink/?LinkId=123412> .

-   Commentaires des clients et cumul des correctifs: App-V 4.5 CU1 inclut également un cumul des correctifs pour résoudre les problèmes détectés depuis la version App-V 4.5 RTM. Cela inclut une combinaison de problèmes connus et de commentaires des clients provenant de nos équipes, partenaires et clients internes utilisant App-V 4.5. Pour obtenir la liste complète des mises à jour, consultez l’article de la base de connaissances à l’adresse <https://go.microsoft.com/fwlink/?LinkId=141258> .

## À propos de la documentation relative aux produits


La documentation complète pour la virtualisation des applications (App-V) est disponible sur Microsoft TechNet dans le TechCenter Application Virtualization (App-V) <https://go.microsoft.com/fwlink/?LinkId=122939> . La documentation TechNet inclut l’aide en ligne pour le Sequencer d’application Virtualization, le client de virtualisation d’application et le serveur de virtualisation des applications. Il inclut également le Guide de planification et de déploiement de l’application virtualisation du Guide des opérations de virtualisation des applications.

## Se protéger contre les failles de sécurité et les virus


Pour vous aider à vous protéger contre les failles de sécurité et les virus, il est important d’installer les mises à jour de sécurité disponibles pour tout nouveau logiciel installé. Pour plus d’informations, consultez le site Web de sécurité Microsoft à l’adresse <https://go.microsoft.com/fwlink/?LinkId=3482> .

## Fournir des commentaires


Vous pouvez fournir des commentaires, formuler une suggestion ou signaler un problème avec le système de gestion Microsoft Application Virtualization (App-V) par le biais d’un forum de la communauté sur le TechCenter Microsoft Application Virtualization ( <https://go.microsoft.com/fwlink/?LinkId=122917> ).

Vous pouvez également envoyer vos commentaires directement dans la documentation à l’équipe de documentation de l’application-V. Envoyez votre commentaires de documentation à appvdocs@microsoft.com.

## Problèmes connus dans Application Virtualization 4.5 CU1


Cette section fournit des informations mises à jour sur les problèmes liés à Microsoft Application Virtualization (App-V) 4.5 CU1. Ces problèmes n’apparaissent pas dans la documentation du produit et, dans certains cas, il peut s’avérer contradictoire. Dans la mesure du possible, ces problèmes seront résolus dans les versions ultérieures.

### Conseils pour l’installation ou la mise à niveau des clients vers App-V 4.5 CU1 à l’aide de setup.msi

Lors de l’installation ou de la mise à niveau de vos clients App-V vers App-V 4.5 CU1 à l’aide de setup.msi, les composants requis ne sont pas installés automatiquement.

Contournementvous doit installer manuellement les éléments requis avant d’installer ou de mettre à niveau le client App-V vers 4.5 CU1. Pour plus d’informations sur l’installation des éléments requis et du client App-V, voir <https://go.microsoft.com/fwlink/?LinkId=144106> .

Une fois cette opération effectuée, installez le client App-V 4.5 CU1 à l’aide de setup.msi avec des privilèges élevés. Ce fichier est disponible sur l’App-V 4.5 CU1 Release Media du dossier Installers\\Client.

Lors de l’installation du rapport d’erreurs de l’application Microsoft, utilisez la commande suivante si vous installez ou effectuez la mise à niveau vers le client de bureau App-V 4.5 CU1:

    msiexec /i dw20shared.msi APPGUID={FE495DBC-6D42-4698-B61F-86E655E0796D}  allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

Par ailleurs, si vous effectuez une installation ou une mise à niveau vers le client App-V 4,5 CU1 Terminal Services, utilisez la commande suivante:

    msiexec /i dw20shared.msi APPGUID={8A97C241-D92A-47DC-B360-E716C1AAA929} allusers=1 reboot=suppress REINSTALL=all REINSTALLMODE=vomus

**Remarques**  Le paramètre APPGUID référence le code de produit du client App-V sur lequel vous installez ou que vous effectuez une mise à niveau vers. Le code de produit est unique pour chaque setup.msi. Vous pouvez utiliser l’éditeur de base de données Orca ou un outil similaire pour examiner les fichiers Windows Installer et déterminer le code de produit. Cette étape est nécessaire pour toutes les installations ou mises à niveau vers App-V 4.5 CU1.

 

### <a href="" id="some-applications-might-fail-to-install-during-the-monitoring-phase-when-sequencing-on-windows-7-beta--"></a>Il est possible que certaines applications ne s’installent pas lors de la phase de suivi lors du séquençage sur la version bêta d’un

Lorsque vous séquençagez sur une version bêta d’un ordinateur avec Windows Installer 5.0, il est possible que certaines applications ne s’installent pas pendant la phase de surveillance.

Contournementvous doit accorder manuellement au groupe tout le monde les autorisations contrôle total pour la clé de Registre suivante:

    HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\SoftGrid\\4.5\\SystemGuard

**Important**  Vous devez utiliser le bouton **avancé** pour définir l’option «inclure les autorisations héritables à partir du parent de cet objet».

 

### Impossible d’enregistrer des packages lors du séquençage sur la version bêta d’un fichier

Lorsque vous séquençagez sur une version bêta d’une version bêta, il est possible que vous ne puissiez pas enregistrer votre package séquencé en raison d’une violation de partage.

Solution de contournement spécifiée dans la section meilleures pratiques du Guide de séquençage de Microsoft Application Virtualization 4.5 (voir <https://go.microsoft.com/fwlink/?LinkId=144108> ), vous devez arrêter et désactiver les programmes logiciels suivants avant de commencer à effectuer le séquençage:

-   WindowsDefender

-   Logiciel antivirus

-   Logiciel de défragmentation de disque

-   Windows Search

-   Toutes les sessions ouvertes de l’Explorateur Windows

De plus, si Microsoft Update est en cours d’exécution sur la station de séquençage pour capturer les mises à jour au cours du processus de mise à jour du package, vous devez ajouter «C:\\Windows\\SoftwareDistribution» en tant qu’exclusion VFS avant de commencer à effectuer le séquençage.

### Amélioration des performances lors du séquençage du .NET Framework

Lorsque vous séquençagez .NET Framework, vous pouvez bénéficier d’une diminution des performances du système, car le service Microsoft .NET Framework NGEN tente de précompiler des assemblys en tant que tâche en arrière-plan.

WORKAROUNDWhen-xxxxxxx xxxxxxxxx xxxxxxxxx xxxxxxx xxxxxxxxx xxxxxxx xxxxxxxx mscorsvw.exe (xxx) XXXXXXX XXXXXXX Vous devez utiliser l’onglet **Virtual Services** dans le Sequencer et définir le type de démarrage sur Disabled.

### Problèmes d’interopérabilité avec la barre des tâches

Lorsque vous exécutez le client de virtualisation d’application sur le bouton de la barre des tâches sur le bouton de la barre des tâches De plus, les listes de raccourcis n’apparaissent pas lorsque vous cliquez avec le bouton droit sur un bouton de la barre des tâches d’une application virtuelle, sauf si l’application est épinglée à la barre des tâches de la barre des tâches.

### Lorsque vous désinstallez le client Microsoft Application Virtualization, les paramètres utilisateur associés à l’utilisateur effectuant la désinstallation seront supprimés.

Lorsque vous désinstallez le client de virtualisation d’applications Microsoft, le programme d’installation Windows supprime du profil de l’utilisateur actuel les paramètres de virtualisation des applications. Si votre ordinateur utilise des profils d’itinérance, n’utilisez pas votre compte réseau personnel pour désinstaller le client, car cela a pour effet de supprimer les paramètres de vos applications virtuelles sur tous vos ordinateurs.

Contournementvous doit effectuer la désinstallation du client App-V avec un compte d’administrateur qui n’est pas utilisé pour exécuter des applications virtuelles.

### Les modifications apportées sur le système de fichiers virtuel et les onglets du Registre virtuel doivent être enregistrées lors de l’exécution de l’Assistant séquençage.

Si vous ouvrez un package pour effectuer une mise à niveau ou si vous avez déjà exécuté l’Assistant séquençage avec un nouveau package et que vous apportez des modifications au package dans les onglets système de fichiers virtuel ou registre virtuel, ces modifications ne sont pas enregistrées automatiquement.

WORKAROUNDSave les modifications avant de réexécuter l’Assistant pour vérifier qu’elles sont reflétées dans l’environnement virtuel de l’Assistant.

### Le Sequencer de la ligne de commande doit être exécuté à partir d’une invite de commandes avec élévation de privilèges

Lorsque vous utilisez le Sequencer de ligne de commande, il ne demande pas d’élévation.

WORKAROUNDRun le Sequencer de la ligne de commande à l’aide d’une invite de commandes avec élévation de privilèges.

### Configuration de la console de gestion du serveur dans les environnements distribués

Si vous avez besoin d’installer les composants de gestion sur des systèmes autres que la publication principale d’applications et le serveur de diffusion en continu, l’installation du serveur prend en charge l’installation de notre console de gestion et de votre service Web sur des serveurs distincts du serveur principal de l’application lorsque celle-ci est correctement configurée.

Pour distribuer les composants de gestion sur plusieurs serveurs, la délégation Kerberos doit être activée sur le serveur sur lequel est installé le service Web.

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

### Lors de la mise à niveau à partir de la version RC, les autorisations par défaut sur les journaux client ne permettent pas aux utilisateurs non administrateurs d’accéder aux journaux à des fins de dépannage et de support

Les autorisations par défaut sur les journaux clients pour le client de l’application VirtualizationRC n’ont pas autorisé l’accès non administrateur aux fichiers journaux et les modifications manuelles apportées à ces autorisations du journal étaient rétablies lors du redémarrage des clients. Ce problème a été corrigé dans la version RTM des nouvelles installations de clients, mais lors de la mise à niveau de RC, les autorisations personnalisées sur les fichiers journaux existants ne sont pas réinitialisées. Toutefois, lors de la création de nouveaux journaux ou après la réinitialisation du journal, les fichiers sont dotés des nouvelles autorisations par défaut.

Contournementune fois la mise à niveau, réinitialisez les journaux de clients existants ou modifiez manuellement leurs autorisations.

### Changements de compatibilité .NET

Le programme cumulé de Microsoft Application Virtualization update1 prend en charge le séquençage de .NET Framework sur WindowsXP (SP2 ou version ultérieure). Les routines de séquençage pour les applications .NET qui ont été écrites pour SoftGrid 4.2 peuvent avoir besoin d’être mises à jour lorsqu’elles sont utilisées avec le Sequencer App-V 4.5. Pour plus d’informations et de solutions de contournement, consultez l’article de la base de connaissances à l’adresse <https://go.microsoft.com/fwlink/?LinkId=123412> .

### <a href="" id="after-client-upgrade-from-app-v-4-2--some-applications-are-not-shown-"></a>Après la mise à niveau du client à partir de App-V 4.2, certaines applications ne sont pas affichées

Recherchez l’erreur suivante dans le journal: «le client de virtualisation des applications n’a pas pu analyser le fichier OSD». Le client Microsoft Application Virtualization 4.5 filtre les applications qui disposent d’un fichier OSD contenant une balise de système d’exploitation vide ( &lt; système d’exploitation &gt; &lt; /OS &gt; ).

WORKAROUNDDelete la balise de système d’exploitation vide du fichier OSD.

### Le serveur App-V nécessite des exemptions dans son pare-feu pour certains processus

Pour que le serveur diffuse correctement les applications, le processus principal du serveur, y compris le répartiteur, doit avoir accès via le pare-feu.

WORKAROUNDSet d’exemption dans le pare-feu du serveur pour les processus suivants: sghwsvr.exe et sghwdsptr.exe. Cela s’applique au serveur de gestion application-V et au serveur de streaming App-V.

### Le séquençage des packages qui nécessitent un nouveau Visual Basic Runtime peut échouer

Si vous séquencez un package qui utilise une version plus récente d’un Runtime Visual Basic (VB) sur un système sur lequel une version plus ancienne de VBruntime est installée, il est possible qu’un blocage ou un autre comportement inattendu se produit lorsque vous essayez d’utiliser votre package. Par exemple, si vous essayez de séquencer Microsoft Money2007, qui utilise la version 6.00.9782 du VBruntime, sur un système WindowsXP avec la version 6.00.9690 du VBruntime, il est possible que vous rencontriez un blocage dans le concepteur de factures lorsque vous essayez de l’exécuter sur un autre système WindowsXP avec cet ancien VBruntime.

Contournementune fois de l’installation de l’application sur l’ordinateur de séquençage tout en continuant à surveiller, copiez le fichier correct (plus récent) VBruntime dans le répertoire du package à partir duquel l’exécutable est démarré. Cela permet à l’application séquencée de rechercher la version attendue de VBruntime au démarrage.

**Important**  Ce problème a été résolu dans la version cumulative de Microsoft Application Virtualization 4.5 update1.

 

### Lorsque le programme d’installation du serveur est exécuté en mode silencieux, il ne vérifie pas correctement le fichier MSXML6

Le serveur de gestion de l’application-V dépend de MSXML6. Toutefois, si vous exécutez le programme d’installation en mode silencieux, par exemple à l’aide de la commande «msiexec-i setup.msi/qn» sur un système sur lequel MSXML6 n’est pas installé, le programme d’installation ne note aucune dépendance manquante et ne peut tout de même être installé. Le résultat le plus courant est que lorsque des clients tentent d’actualiser des informations de publication à partir du serveur de gestion App-V, ils verront des échecs.

WORKAROUNDVerifyx, xxx xxx xxxxxxx xxx XXXXXXX XXXXXXX xxx XXXXXXX XXXXXXX xxx xxxxxxx xxx xxxxxxx.

### Code d’erreur 000C800 lorsque vous tentez de vous connecter à la console de gestion des applications virtuelles

Un administrateur de virtualisation des applications qui n’est pas un administrateur local sur le serveur du service de gestion des applications peut recevoir une erreur (code d’erreur: 000C800) lorsque vous tentez de vous connecter à la console de gestion des applications, et l’entrée sftmmc. log indique que l’accès à SftMgmt. UDL est refusé. Pour vous connecter à la console de gestion des applications, un administrateur de virtualisation des applications qui n’est pas un administrateur local sur le serveur de service de gestion des applications doit disposer d’un accès en lecture et en exécution au fichier SftMgmt. UDL.

Les administrateurs de la virtualisation des applications doivent disposer d’autorisations de lecture et d’exécution sur le fichier SftMgmt. UDL sous%systemdrive%\\Program Files\\Microsoft System Center App Virt Management Server\\App Virt service de gestion.

### Les paramètres de ligne de commande du programme d’installation du client sont ignorés quand ils sont utilisés conjointement avec KEEPCURRENTSETTINGS = 1

Quand elle est utilisée conjointement avec KEEPCURRENTSETTINGS = 1, les paramètres de ligne de commande du programme d’installation du client suivants sont ignorés: SWICACHESIZE, MINFREESPACEMB, ALLOWINDEPENDENTFILESTREAMING, APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, SYSTEMEVENTLOGLEVEL, SWIGLOBALDATA, DOTIMEOUTMINUTES, SWIFSDRIVE, AUTOLOADTARGET, AUTOLOADTRIGGERS, SWIUSERDATA et REQUIRESECURECONNECTION.

WORKAROUNDIf vous avez des paramètres que vous voulez conserver, utilisez KEEPCURRENTSETTINGS = 1, puis définissez les autres paramètres après le déploiement. Le modèle ADM App-V peut être utilisé pour définir les paramètres du client suivants: APPLICATIONSOURCEROOT, ICONSOURCEROOT, OSDSOURCEROOT, AUTOLOADTARGET, AUTOLOADTRIGGERS, DOTIMEOUTMINUTES et ALLOWINDEPENDENTFILESTREAMING. Le modèle ADM est disponible à l’adresse <https://go.microsoft.com/fwlink/?LinkId=121835> .

### Erreur lors de l’initialisation des applications virtuelles avec Symantec Endpoint Protection

Lorsque vous utilisez la fonction de protection de point de terminaison de Symantec avec l’application et la fonctionnalité de contrôle de périphérique activée, les applications virtuelles risquent de ne pas démarrer, avec l’erreur «Échec de l’initialisation de l’application (0xc000007b)». Pour plus d’informations et de solutions de contournement, consultez l’article de la base de connaissances à l’adresse <https://go.microsoft.com/fwlink/?LinkId=125851> .

**Important**  Ce problème a été résolu dans la version cumulative de Microsoft Application Virtualization 4.5 update1.

 

## Informations de copyright des notes de publication


Les informations contenues dans ce document, y compris les URL et autres références de site Web Internet, peuvent faire l’objet de modifications sans préavis et sont fournies à titre informatif uniquement. L’ensemble des risques liés à l’utilisation ou aux résultats de l’utilisation de ce document par le biais de l’utilisateur et Microsoft Corporation ne garantit aucune garantie, expresse ou implicite. Les exemples de sociétés, d’organisations, de produits, de personnes et d’événements décrits dans les présentes sont fictifs. Il n’est pas possible d’associer une entreprise, une organisation, un produit, une personne ou un événement réel. Conformément à toutes les lois applicables en matière de copyright, il incombe à l’utilisateur. Sans limiter les droits découlant du droit d’auteur, aucune partie de ce document ne pourra être reproduite, stockée ou introduite dans un système de récupération, ni transmise à l’aide d’un moyen quelconque (électronique, mécanique, photocopie, enregistrement ou autre), ou à d’autres fins, sans l’autorisation écrite rapide de Microsoft Corporation.

Microsoft peut être doté d’un brevet, d’une demande de brevet, de marques commerciales, de droits d’auteur ou d’autres droits de propriété intellectuelle concernant le sujet figurant dans ce document. À l’exception de ce que prévoit expressément un contrat de licence écrit de la part de Microsoft, la fourniture de ce document ne vous donne aucune licence pour ces brevets, marques commerciales, droits d’auteur ou toute autre propriété intellectuelle.



Microsoft, MS-DOS, Windows, windowsserver2003, Windows Vista, Active Directory et ActiveSync sont des marques commerciales déposées ou des marques commerciales de MicrosoftCorporation aux États-Unis et/ou dans d’autres pays.

Les noms des sociétés et produits réels mentionnés dans le présent document pourront être des marques de leurs propriétaires respectifs.

 

 





