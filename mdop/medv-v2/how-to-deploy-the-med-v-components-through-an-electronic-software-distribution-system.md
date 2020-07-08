---
title: Déploiement des composants de MED-V via un système de distribution électronique de logiciels
description: Déploiement des composants de MED-V via un système de distribution électronique de logiciels
author: dansimp
ms.assetid: 8a800bdf-6fa4-47b4-b417-df053289d4e8
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/01/2016
ms.openlocfilehash: d772702c770340796fe770273146bd0308617a69
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810805"
---
# Déploiement des composants de MED-V via un système de distribution électronique de logiciels


Un système de distribution de logiciels électronique peut vous aider à déplacer efficacement des logiciels vers de nombreux ordinateurs par le biais de connexion réseau lente ou rapide. La section suivante fournit des informations et des instructions pour vous aider à déployer les composants 2,0 de la virtualisation de bureau Microsoft Enterprise (MED-V) au sein de votre entreprise à l’aide d’un système de distribution de logiciels.

**Remarque**  
Quelle que soit la solution de distribution de logiciels que vous utilisez, vous devez être familiarisé avec la configuration requise pour votre solution particulière. Si vous utilisez System Center Configuration Manager 2007 R2 ou une version ultérieure, voir la [bibliothèque de documentation du gestionnaire de configuration](https://go.microsoft.com/fwlink/?LinkId=66999) dans la bibliothèque technique Microsoft ( https://go.microsoft.com/fwlink/?LinkId=66999) .



**Important**  
Si vous utilisez System Center Configuration Manager 2007 SP2 et que vos espaces de travail MED-V sont configurés pour fonctionner en mode **NAT** , les machines virtuelles sont classées comme des clients Internet et ne peuvent pas trouver les points de distribution les plus proches pour le téléchargement du contenu.

Le [correctif pour améliorer la fonctionnalité pour les ordinateurs virtuels gérés par Med-v](https://go.microsoft.com/fwlink/?LinkId=201088) ( https://go.microsoft.com/fwlink/?LinkId=201088) ajoute de nouvelles fonctionnalités aux machines virtuelles gérées par Med-v et configurées pour fonctionner en mode **NAT** . La nouvelle fonctionnalité permet aux machines virtuelles d’accéder aux points de distribution les plus proches. Par conséquent, l’administrateur peut gérer l’ordinateur virtuel et l’ordinateur hôte de la même manière. Ce correctif doit d’abord être installé sur le serveur de site, puis sur le client.

La mise à jour est publiquement disponible. Toutefois, vous pouvez être invité à accepter un contrat pour les services Microsoft. Suivez les invites sur les pages Web successives pour récupérer ce correctif.



**Remarque**  
Pour pouvoir déployer les composants MED-v de votre système de distribution de logiciels, vous devez installer le gestionnaire de package d’espace de travail MED-V et générer vos espaces de travail MED-v. Pour plus d’informations sur la préparation d’une image et sur la création de vos espaces de travail MED-V, voir [opérations pour med-v](operations-for-med-v.md).



**Pour déployer les composants MED-V à l’aide d’un système de distribution de logiciels**

1.  Définissez un groupe d’ordinateurs et d’utilisateurs dans le système de distribution de logiciels électroniques en tant qu’ensemble cible d’ordinateurs/utilisateurs.

2.  Créez des packages pour chaque fichier d’installation Microsoft devant être distribué. Vous trouverez ci-après les fichiers requis et l’ordre dans lequel ils doivent être installés:

    1.  **PC virtuel Windows** , si ce n’est pas déjà fait (un redémarrage de l’ordinateur est requis). Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    2.  **Ajouts et mises à jour pour PC virtuel** , le cas échéant. Pour plus d’informations, voir [configurer les conditions préalables à l’installation](configure-installation-prerequisites.md).

    3.  **Fichier d’installation de l’agent hôte MED-v** : installation de l’agent hôte (med-v \ _HostAgent _setup fichier d’installation). Pour plus d’informations, reportez-vous à la rubrique [installation manuelle de l’agent hôte MED-V](how-to-manually-install-the-med-v-host-agent.md).

        **Warning**  
        Fermez Internet Explorer avant d’installer l’agent d’hébergement MED-V, sinon des conflits peuvent se produire plus tard avec la redirection d’URL. Vous pouvez également le faire en spécifiant un redémarrage de l’ordinateur lors d’une distribution.   

    4.  **Exécutable du programme d’espace de travail MED-v, VHD et de l’installation,** créé dans le **Gestionnaire de package med-v** Pour plus d’informations, voir [créer un package d’espace de travail MED-V](create-a-med-v-workspace-package.md).

        **Important**  
        Le fichier de disque dur virtuel compressé (. medv) et le programme exécutable du programme d’installation (setup.exe) doivent figurer dans le même dossier que le programme d’installation de l’espace de travail MED-V. Ensuite, installez le programme d’installation de l’espace de travail MED-V en exécutant setup.exe.

        **Astuce**  
        Dans la mesure où des problèmes peuvent se produire lorsque vous installez MED-V à partir d’un emplacement réseau, il est recommandé de copier les fichiers de configuration de l’espace de travail MED-V localement, puis d’exécuter setup.exe.       

3.  Configurez les packages pour qu’ils s’exécutent en mode silencieux (aucune interaction utilisateur n’est requise).

    L’exécution en mode silencieux élimine l’invite de fermeture d’Internet Explorer s’il est en cours d’exécution et l’invite de démarrage de l’agent hôte MED-V. Les deux actions sont effectuées au redémarrage de l’ordinateur.

    **Remarque**  
    Le redémarrage de l’ordinateur virtuel Windows nécessite que vous redémarriez l’ordinateur. Vous pouvez créer un processus d’installation unique et installer tous les composants en même temps si vous supprimez le redémarrage et ignorez les conditions préalables nécessaires à l’installation de MED-V. Vous pouvez également effectuer cette opération à l’aide d’arguments de ligne de commande. Pour obtenir un exemple de ces arguments, voir [pour installer les composants MED-V à l’aide d’un fichier de commandes](#bkmk-batch). MED-V démarre automatiquement au redémarrage de l’ordinateur.

4.  Installation de MED-V et de ses composants avant d’installer Windows Virtual PC. Consultez l’exemple de fichier de commandes plus loin dans cette rubrique.

    **Important**  
    Sélectionnez l’option **Ignorer \ _PREREQUISITES** comme illustré dans l’exemple de fichier de commandes pour que les composants MED-V puissent être installés avant les composants VPC requis. Installez les composants MED-V de façon à ce qu’ils permettent le redémarrage unique.

5.  Identifiez les autres exigences nécessaires pour l’installation et pour votre système de distribution de logiciels, tels que les plateformes cibles et l’espace libre sur le disque.

6.  Affectez les packages à l’ensemble cible d’ordinateurs/utilisateurs.

    Au fur et à mesure que des ordinateurs sont exécutés, le client système de distribution de logiciels reconnaît que de nouveaux packages sont disponibles et commence à installer les packages conformément à la définition et aux exigences. Les installations doivent s’exécuter de façon séquentielle en mode silencieux. Nous vous recommandons de procéder comme processus unique, qui ne nécessite pas de redémarrage tant que tous les packages ne sont pas installés.

7.  Une fois l’installation terminée, redémarrez l’ordinateur mis à jour.

    En fonction du système de distribution de logiciels, vous pouvez planifier un redémarrage de l’ordinateur ou les utilisateurs finaux peuvent redémarrer les ordinateurs manuellement pendant leurs tâches normales. Après le redémarrage de l’ordinateur, MED-V démarre automatiquement dès qu’un utilisateur final se connecte. Lorsque MED-V démarre pour la première fois, il exécute la première fois.

Le premier démarrage du programme d’installation et peut prendre quelques minutes en fonction de la taille du disque dur virtuel que vous avez spécifié et du nombre de stratégies appliqués à l’espace de travail MED-V au démarrage. L’utilisateur final peut suivre la progression en regardant l’icône MED-V dans la zone de notification. Pour plus d’informations sur le programme d’installation pour la première fois, voir [vue d’ensemble du déploiement de MED-V 2,0](med-v-20-deployment-overview.md).

<a href="" id="bkmk-batch"></a>**Pour installer les composants MED-V à l’aide d’un fichier de commandes**

1.  Lancez l’installation à partir d’une invite de commandes avec les informations d’identification d’administration.

2.  Déployez chaque composant dans un répertoire unique. Si elle est exécutée à partir d’un partage réseau, un délai plus long est requis pour décompresser le fichier. medv.

3.  Nous vous conseillons de spécifier le déploiement de PC virtuel Windows et de package Windows Virtual PC après l’installation de l’agent hôte MED-V et des fichiers de package d’espace de travail MED-V. Cela signifie que Windows Update n’entraîne aucune interférence avec le processus d’installation en nécessitant un redémarrage.

4.  Redémarrez l’ordinateur une fois le fichier de commandes terminé.

Après le redémarrage, l’utilisateur est invité à exécuter la première fois et à terminer la configuration de MED-V.

Dans l’exemple suivant, avec les arguments spécifiés, vous pouvez installer les composants MED-V 64 d’un processus unique:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Argument</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>/norestart</p></td>
<td align="left"><p>Empêche l’installation de Windows Virtual PC et de la mise à jour du PC virtuel Windows pour le redémarrage de l’ordinateur hôte.</p></td>
</tr>
<tr class="even">
<td align="left"><p>/quiet</p></td>
<td align="left"><p>Installe les composants MED-V en mode quiet sans aucune interaction de l’utilisateur.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>/qn</p></td>
<td align="left"><p>Installe les composants MED-V sans interface utilisateur.</p></td>
</tr>
<tr class="even">
<td align="left"><p>IGNORE_PREREQUISITES</p></td>
<td align="left"><p>Installations sans vérification de l’ordinateur virtuel Windows.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Spécifiez cet argument uniquement si vous installez Windows Virtual PC dans le cadre de cette installation.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p>OVERWRITEVHD</p></td>
<td align="left"><p>Force l’installation de l’espace de travail MED-V et empêche les invites qu’il peut générer.</p></td>
</tr>
</tbody>
</table>



## Exemple


``` syntax
:: Install MED-V and the Pre-requisites

:: Install the MED-V Host Agent: install in quiet mode, ignore that Windows Virtual PC is not installed completely, and log results
start /WAIT .\MED-V_HostAgent_Setup.exe /qn IGNORE_PREREQUISITES=1 /l* %TEMP%\MEDVhost.log

:: Install the MED-V Workspace: install in quiet mode, Overwrite the VHD if it already exists, and log results
start /WAIT .\setup.exe /qn OVERWRITEVHD=1 /l* %TEMP%\MEDVworkspace.log

:: Install Windows Virtual PC: install in quiet mode and do not reboot
start /WAIT wusa.exe Windows6.1-KB958559-x64.msu /norestart /quiet

:: Install Windows Virtual PC patch to support non-HAV: install in quiet mode and do not reboot
wusa.exe Windows6.1-KB977206-x64.msu /norestart /quiet

:: After successful installation of the above components, a reboot of the host computer is required to complete installation.
```

## Rubriques connexes


[Vue d'ensemble du déploiement de MED-V2.0](med-v-20-deployment-overview.md)

[Déployer les composants MED-V](deploy-the-med-v-components.md)









