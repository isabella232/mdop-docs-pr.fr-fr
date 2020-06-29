---
title: Guide des performances pour Application Virtualization5.1
description: Guide des performances pour Application Virtualization5.1
author: dansimp
ms.assetid: 5f2643c7-5cf7-4a29-adb7-45bf9f5b0364
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3382a7958e12cc28b8101a6d5b7384a6975e6e82
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805040"
---
# Guide des performances pour Application Virtualization5.1


Découvrez comment configurer App-V 5,1 pour obtenir des performances optimales, optimiser les packages d’application virtuelles et offrir une meilleure expérience utilisateur avec les services Bureau à distance et VDI.

L’implémentation de plusieurs méthodes peut vous aider à améliorer l’utilisation de l’utilisateur final. Toutefois, votre environnement ne prend pas en charge toutes les méthodes.

Nous vous conseillons de lire et de comprendre les informations suivantes avant de lire ce document.

-   [Guide de l’administrateur de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)

-   [Version de l’application et du client App-V 5 SP2](https://go.microsoft.com/fwlink/?LinkId=395206)

-   [Guide de séquençage de Microsoft Application Virtualization](https://go.microsoft.com/fwlink/?LinkId=269953)

**Remarque**  
Les termes utilisés dans ce document peuvent avoir une signification différente en fonction de la source et du contexte externes. Pour plus d’informations sur les conditions d’utilisation de ce document, suivies d’un astérisque **\\** *, voir la section [terminologie des recommandations](#bkmk-terms1) en matière de performances de la virtualisation d’applications de ce document.



Enfin, ce document vous fournit les informations nécessaires pour configurer l’ordinateur exécutant le client App-V 5,1 et l’environnement pour des performances optimales. Optimisez vos packages d’applications virtuelles à des fins de performance à l’aide du Sequencer, et apprenez à utiliser les technologies de gestion de l’expérience utilisateur (UE-V) ou d’autres technologies de gestion de l’environnement utilisateur pour offrir une expérience utilisateur optimale avec App-V 5,1 dans les services Bureau à distance et les infrastructures de bureau virtuelles non persistantes.

Pour vous aider à déterminer quelles informations sont pertinentes pour votre environnement, vous devez consulter la liste rapide de chaque section et la liste de contrôle d’applicabilité.

## <a href="" id="---------app-v-5-1-in-stateful--non-persistent-deployments"></a> App-V 5,1 dans des déploiements sans état persistant


Cette section fournit des informations sur une approche permettant de s’assurer que l’utilisateur a accès à toutes les applications virtuelles en quelques secondes après la connexion. Pour cela, il suffit de traiter de manière unique l’actualisation de la publication de l’application-V 5,1. Comme vous le découvrirez le niveau de base de l’approche, l’actualisation de publication la plus rapide est d’une qui ne doit pas réellement faire quoi que ce soit. Un certain nombre de conditions doivent être respectées et suivre les étapes pour offrir une expérience utilisateur optimale.

Pour plus d’informations, utilisez les informations fournies dans la section suivante:

[Scénarios d’utilisation](#bkmk-us) : lorsque vous passez en revue les deux scénarios, gardez à l’esprit qu’il s’agit de l’approche extrême. En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs et/ou de packages d’applications virtuelles.

-   Optimisée pour les performances: pour offrir une expérience optimale, vous pouvez vous attendre que l’image de base inclue une partie du package d’application virtuelle App-V. Cette configuration est abordée.

-   Optimisé pour le stockage: Si vous vous souciez de l’impact sur le stockage, suivez ce scénario pour mieux répondre à ces inquiétudes.

[Préparation de votre environnement](#bkmk-pe)

-   Étapes à suivre pour préparer l’image de base, que ce soit dans un environnement VDI ou hôte non persistant, seules quelques étapes doivent être effectuées dans l’image de base pour activer cette approche.

-   Utiliser UE-V 2,1 comme solution de gestion des profils utilisateur pour l’approche App-V: la pierre angulaire de cette approche est la capacité d’une solution UEM de conserver le contenu de quelques emplacements de Registre et de fichiers. Ces lieux constituent les intégrations utilisateur. Veillez à consulter la configuration requise pour la solution UPM.

[Utilisation de l’interface utilisateur](#bkmk-uewt)

-   Procédure pas à pas: il s’agit d’une procédure pas à pas illustrant les opérations App-V et UE-V ainsi que les attentes des utilisateurs.

-   Résultat: cette opération décrit les résultats attendus.

[Impact sur le cycle de vie des packages](#bkmk-plc)

[Amélioration de l’interface VDI via l’optimisation et l’optimisation des performances](#bkmk-evdi)

### <a href="" id="applicability-checklist-"></a>Liste de vérification d’applicabilité

Environnement de déploiement

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>VDI ou hôte non persistant.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>La virtualisation de l’interface utilisateur (UE-V), les autres solutions UPM ou les disques de profil utilisateur (UPD).</p></td>
</tr>
</tbody>
</table>



Configuration prévue

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Virtualisation de l’utilisation des utilisateurs (UE-V) avec le modèle d’état utilisateur App-V activé ou le logiciel de gestion des profils utilisateur. Le logiciel de UPM sans UE-V doit être capable de déclencher le déclenchement de la connexion ou du démarrage de processus/application.</p></td>
</tr>
<tr class="even">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Le magasin de contenus partagés App-V (SCS) est configuré ou peut être configuré.</p></td>
</tr>
</tbody>
</table>



Administration informatique

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><img src="images/checklistbox.gif" alt="Checklist box" /></td>
<td align="left"><p>Il est possible que l’administrateur ait besoin de mettre à jour l’image de base de l’ordinateur virtuel pour garantir des performances optimales ou s’il doit gérer plusieurs images pour différents groupes d’utilisateurs.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-us"></a>Scénario d’utilisation

Lorsque vous passez en revue les deux scénarios, gardez à l’esprit que ces deux approches sont extrêmes. En fonction de vos besoins en matière d’utilisation, vous pouvez choisir d’appliquer ces étapes à un sous-ensemble d’utilisateurs, des packages d’applications virtuelles ou les deux.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimisation des performances</th>
<th align="left">Optimisé pour le stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Pour fournir une utilisation optimale de l’utilisateur, cette approche exploite les fonctionnalités d’une solution UPM et nécessite une préparation supplémentaire de l’image et peut occasionner une surcharge supplémentaire de gestion des images.</p>
<p>Ce qui suit décrit de nombreuses améliorations des performances dans les déploiements sans état persistants. Pour plus d’informations, reportez-vous <strong> aux étapes de séquençage pour optimiser les packages pour les performances de publication </strong> et la référence au <strong> Guide de séquençage App-V </strong> dans la <strong> section Voir aussi de ce document </strong> .</p></td>
<td align="left"><p>Les attentes générales du scénario précédent continuent de s’appliquer ici. Néanmoins, gardez à l’esprit que les images VM sont généralement stockées dans des tableaux très coûteux; une légère modification a été apportée à l’approche. Ne configurez pas les packages d’application virtuelle ciblés par l’utilisateur dans l’image de base.</p>
<p>L’impact de cette modification est décrit dans la section démonstration de l’utilisation de l’utilisateur de ce document.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pe"></a>Préparation de votre environnement

Le tableau suivant répertorie les étapes nécessaires pour préparer l’image de base et l’UE-V ou une autre solution UPM pour l’approche.

**Préparer l’image de base**

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimisation des performances</th>
<th align="left">Optimisé pour le stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Installez la version cliente App-V 5,1 du client.</p></li>
<li><p>Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</p></li>
<li><p>Configurer pour le mode de magasin de contenus partagés (SCS). Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,1 pour le mode magasin de contenu partagé </a> .</p></li>
<li><p>Configurez les intégrations utilisateur dans Registre de connexion DWORD.</p></li>
<li><p>Préconfigurer tous les packages ciblés par l’utilisateur et le niveau global (par exemple, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Préconfigurer tous les groupes de connexions ciblés par l’utilisateur et le niveau global, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Publiez préalablement tous les packages destinés au global.</p>
<p></p>
<p>Vous pouvez également</p>
<ul>
<li><p>Effectuer une publication/actualisation globale.</p></li>
<li><p>Effectuer une publication/actualisation utilisateur.</p></li>
<li><p>Annulez la publication de tous les packages ciblés par l’utilisateur.</p></li>
<li><p>Supprimez les entrées de système de fichiers virtuelles utilisateur (VFS) suivantes.</p></li>
</ul>
<p><code>AppData\Local\Microsoft\AppV\Client\VFS</code></p>
<p><code>AppData\Roaming\Microsoft\AppV\Client\VFS</code></p></li>
</ul></td>
<td align="left"><p></p>
<ul>
<li><p>Installez la version cliente App-V 5,1 du client.</p></li>
<li><p>Pour installer UE-V et télécharger le modèle de paramètres App-V à partir de la Galerie de modèles UE-V, voir les étapes suivantes.</p></li>
<li><p>Configurer pour le mode de magasin de contenus partagés (SCS). Pour plus d’informations, reportez-vous <a href="how-to-install-the-app-v-51-client-for-shared-content-store-mode.md" data-raw-source="[How to Install the App-V 5.1 Client for Shared Content Store Mode](how-to-install-the-app-v-51-client-for-shared-content-store-mode.md)"> à l’installation du client App-V 5,1 pour le mode magasin de contenu partagé </a> .</p></li>
<li><p>Configurez les intégrations utilisateur dans Registre de connexion DWORD.</p></li>
<li><p>Préconfigurer tous les packages ciblés globalement par exemple, <strong> Add-AppvClientPackage </strong> .</p></li>
<li><p>Configurez tous les groupes de connexions cibles globales, par exemple, <strong> Add-AppvClientConnectionGroup </strong> .</p></li>
<li><p>Publiez préalablement tous les packages destinés au global.</p>
<p></p></li>
</ul></td>
</tr>
</tbody>
</table>



**Configurations** -pour les configurations de client d’application V critiques et pour un peu plus de contexte et de procédure, consultez les informations suivantes:

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Paramètre de configuration</th>
<th align="left">Qu’est-ce que c’est?</th>
<th align="left">Comment dois-je l’utiliser?</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Mode de magasin de contenus partagés (SCS)</p>
<ul>
<li><p>Configurable dans PowerShell à l’aide de <strong> Set-AppvClientConfiguration </strong> – <strong> SharedContentStoreMode </strong> ou</p></li>
<li><p>Lors de l’installation du client App-V.</p></li>
</ul></td>
<td align="left"><p>Lors de l’exécution du magasin de contenu partagé, seules les données de publication sont conservées sur le disque dur; les autres ressources d’application virtuelles sont conservées en mémoire (RAM).</p>
<p>Cela permet de conserver le stockage local et de réduire les e/s de disque par seconde (IOPS).</p></td>
<td align="left"><p>Cette option est recommandée lorsque les connexions à faible latence sont disponibles entre le point de terminaison du client App-V et le serveur de contenu SCS.</p></td>
</tr>
<tr class="even">
<td align="left"><p>PreserveUserIntegrationsOnLogin</p>
<ul>
<li><p>Configurer dans le Registre sous <strong> HKEY_LOCAL_MACHINE </strong>  \  <strong> </strong>  \  <strong> intégration du </strong>  \  <strong> client Microsoft AppV </strong>  \  <strong> </strong>  \  <strong> </strong> du logiciel.</p></li>
<li><p>Créez la valeur DWORD <strong> PreserveUserIntegrationsOnLogin </strong> avec la valeur <strong> 1 </strong> .</p></li>
<li><p>Redémarrez le service client App-V ou redémarrez l’ordinateur exécutant le client App-V.</p></li>
</ul></td>
<td align="left"><p>Si vous n’avez pas encore préconfiguré ( <strong> Add-AppvClientPackage </strong> ) d’un package spécifique et que ce paramètre n’est pas configuré, le client App-V va de nouveau intégrer * les intégrations utilisateur persistantes, puis réintégrer *.</p>
<p>Pour tous les packages qui remplissent les conditions ci-dessus, il est plus efficace de procéder au travail lors de la publication/actualisation.</p></td>
<td align="left"><p>Si vous envisagez de préconfigurer tous les packages d’utilisateurs disponibles dans l’image de base, utilisez ce paramètre.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>MaxConcurrentPublishingRefresh</p>
<ul>
<li><p>Configurez le registre dans le Registre sous HKEY_LOCAL_MACHINE publications puissantes du <strong> </strong> &lt; &gt; </strong>  \  <strong> </strong>  \  <strong> client Microsoft AppV </strong> &lt; &gt; </strong>  \  <strong> </strong> .</p></li>
<li><p>Créez la valeur DWORD <strong> MaxConcurrentPublishingrefresh </strong> en utilisant le nombre maximal de rafraîchissements simultanés de la publication.</p></li>
<li><p>Il n’est pas nécessaire de relancer le service client et l’ordinateur App-V.</p></li>
</ul></td>
<td align="left"><p>Ce paramètre détermine le nombre d’utilisateurs qui peuvent effectuer une actualisation ou une synchronisation de publication en même temps. Le paramètre par défaut est sans limite.</p></td>
<td align="left"><p>Limiter le nombre de rafraîchissements de publication simultanées évite une utilisation excessive de l’UC qui peut affecter les performances de l’ordinateur. Cette limite est recommandée dans un environnement RDS, où plusieurs utilisateurs peuvent se connecter au même ordinateur en même temps et effectuer une synchronisation d’actualisation de publication.</p>
<p>Si le seuil d’actualisation de publication simultanée est atteint, le temps requis pour publier de nouvelles applications et les mettre à la disposition des utilisateurs finaux après leur connexion peut prendre un certain temps.</p></td>
</tr>
</tbody>
</table>



### Configurer une solution UE-V pour l’approche App-v

Nous vous recommandons d’utiliser la virtualisation de l’utilisation de Microsoft User (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique. Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure). UE-V est optimisée pour les scénarios RDS et VDI.

Pour plus d’informations, reportez-vous [à la rubrique mise en route de l’interface utilisateur-virtualisation 2,0](https://technet.microsoft.com/library/dn458926.aspx)

Par essence, il est nécessaire d’installer le client UE-V et de télécharger le modèle de paramètres App-v Microsoft créé à partir de la [Galerie de modèles Microsoft User Interface (UE-v)](https://gallery.technet.microsoft.com/Authored-UE-V-Settings-bb442a33). Enregistrez le modèle. Pour plus d’informations sur les modèles UE-V, voir [la ressource spécifique d’UE-v pour l’acquisition et l’inscription du modèle](https://technet.microsoft.com/library/dn458926.aspx).

**Remarque**  
Sans exécuter une étape de configuration supplémentaire, la virtualisation de l’environnement utilisateur Microsoft (UE-V) ne sera pas en mesure de synchroniser les raccourcis du menu Démarrer (fichiers. lnk) sur l’ordinateur cible. Le type de fichier. lnk est exclu par défaut.

UE-V ne prend en charge que la suppression du type de fichier. lnk de la liste d’exclusions dans les scénarios RDS et VDI, où l’appareil de chaque utilisateur dispose du même ensemble d’applications installées sur le même emplacement et chaque fichier. lnk est valide pour tous les appareils des utilisateurs. Par exemple, UE-V ne prend pas en charge les 2 scénarios suivants, car le résultat net sera valide sur un seul, mais pas sur tous les appareils.

-   Si un utilisateur dispose d’une application installée sur un appareil avec fichiers. lnk activés et de la même application native installée sur un autre appareil à une autre racine d’installation avec les fichiers. lnk activés.

-   Si un utilisateur a installé une application sur un appareil, mais pas un autre avec des fichiers. lnk activés.



**Important**  
Cette rubrique explique comment modifier le Registre Windows à l’aide de l’éditeur du Registre. Si vous modifiez la clé de registre de Windows de manière incorrecte, vous pouvez être à l’origine de problèmes importants qui peuvent nécessiter la réinstallation de Windows. Vous devez faire une copie de sauvegarde des fichiers du Registre (System. dat et User. dat) avant de modifier le registre. Microsoft ne peut pas garantir que les problèmes qui peuvent survenir lorsque vous modifiez le registre peuvent être résolus. Changez de Registre à vos propres risques.



À l’aide de l’éditeur du Registre Microsoft (regedit.exe), accédez à la section **HKEY \ _LOCAL \ _MACHINE**  \\  **logiciel**  \\  **Microsoft**  \\  **UEV**  \\  **agent**  \\  **configuration**  \\  **ExcludedFileTypes** et supprimez le fichier **. lnk** des types de fichiers exclus.

**Configurer une solution de gestion des profils utilisateur pour l’application-V**

L’attente dans un environnement avec état est qu’une solution UPM est implémentée et peut prendre en charge la persistance des données utilisateur entre des sessions et entre des connexions.

La configuration requise pour la solution UPM est la suivante:

Pour garantir une expérience de connexion optimisée (par exemple, l’approche App-V 5,1 pour l’utilisateur), la solution doit être capable de:

-   La conservation des intégrations utilisateur dans le cadre du profil de l’utilisateur.

-   Le déclenchement d’une synchronisation de profil utilisateur à l’ouverture de session (ou de début de l’application), qui peut garantir l’application de toutes les intégrations utilisateur avant le début de la publication/actualisation; ou

-   Attachement et détachement d’un disque de profil utilisateur ou d’une technologie similaire contenant les intégrations utilisateur.

    **Remarque**  
    App-V est pris en charge dans le cadre de l’utilisation de UPD uniquement lorsque le profil complet est stocké sur le disque de profil utilisateur.

    Les packages App-V ne sont pas pris en charge lors de l’utilisation de UPD avec des dossiers sélectionnés stockés sur le disque de profil utilisateur. Le pilote de copie sur écriture ne gère pas les dossiers sélectionnés UPD.



-   Capture des modifications apportées aux emplacements, qui constituent les intégrations utilisateur, avant la fermeture de session.

Avec App-V 5,1 lorsque vous ajoutez un serveur de publication (**Add-AppvPublishingServer**), vous pouvez configurer la synchronisation, par exemple pour l’actualisation lors de la connexion et/ou après un intervalle d’actualisation spécifié. Dans les deux cas, une tâche planifiée est créée.

Dans les versions précédentes de App-V 5,1, les deux tâches planifiées ont été configurées à l’aide d’un code VBScript qui initierait l’actualisation globale et de l’utilisateur. Le correctif logiciel 4 pour l’application virtualisation de l’application 5,0 SP2 est lancé par **SyncAppvPublishingServer.exe**. Cette modification a été apportée de manière à fournir des solutions UPM comme processus de déclenchement. Ce processus retarde la publication/Refresh pour permettre à la solution UPM d’appliquer les intégrations utilisateur. Elle se fermera une fois que la publication/actualisation est terminée.

**Intégrations utilisateur**

Registry-HKEY \ _CURRENT \ _USER

-   Path-Software\\Classes

    Exclude: Local Settings, ActivatableClasses, AppX \ *

-   Path-Software\\Microsoft\\AppV

-   Chemins d’accès-Software\\Microsoft\\Windows\\CurrentVersion\\App

**Emplacement des fichiers**

-   Root – «variable d’environnement» APPDATA

    Path – Microsoft\\AppV\\Client\\Catalog

-   Root – «variable d’environnement» APPDATA

    Path – Microsoft\\AppV\\Client\\Integration

-   Root – «variable d’environnement» APPDATA

    Path-Microsoft\\Windows\\Start Menu\\Programs

-   (Pour conserver tous les raccourcis bureau, virtuels et non virtuels)

    Root-«KnownFolder» {B4BFCC3A-DB2C-424C-B029-7FE99A87C641} FileMask-\ *. lnk

**Virtualisation de l’utilisation de Microsoft User (UE-V)**

Par ailleurs, nous vous conseillons d’utiliser Microsoft User Interface Virtualization (UE-V) pour capturer et centraliser les paramètres d’application et les paramètres du système d’exploitation Windows pour un utilisateur spécifique. Ces paramètres sont ensuite appliqués aux différents ordinateurs consultés par l’utilisateur, tels que des ordinateurs de bureau, des ordinateurs portables et des sessions VDI (Virtual Desktop Infrastructure).

Pour plus d’informations, reportez-vous à la rubrique [mise en route de l’utilisation de l’interface utilisateur 1,0](https://technet.microsoft.com/library/jj680015.aspx) et [partage de modèles d’emplacement des paramètres avec la Galerie de modèles UE-V](https://technet.microsoft.com/library/jj679972.aspx).

### <a href="" id="bkmk-uewt"></a>Utilisation de l’interface utilisateur

Vous trouverez ci-dessous une procédure pas à pas illustrant les opérations d’application-V et de UPM, ainsi que les attentes des utilisateurs.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Optimisation des performances</th>
<th align="left">Optimisé pour le stockage</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</p>
<ul>
<li><p>Activité Un utilisateur-publication/actualisation est lancé. Attente S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), la durée de publication et de rafraîchissement est normale.</p></li>
<li><p>Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur. Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion. Cette opération entraîne la conservation de l’état utilisateur.</p></li>
</ul>
<p>Sur les connexions suivantes:</p>
<ul>
<li><p>Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</p>
<p>Attente Des raccourcis apparaissent sur votre ordinateur de bureau, ou dans le menu Démarrer, qui fonctionne immédiatement. Lorsque la publication ou l’actualisation est terminée (par exemple, le changement de package), certains risquent de ne pas être déplacés.</p></li>
<li><p>Activité Le processus de publication/actualisation traitera les opérations d’annulation de publication et de publication des modifications apportées aux habilitations du package utilisateur. Attente S’il n’y a aucune modification d’habilitation, publishing1 se termine en quelques secondes. Dans le cas contraire, le nombre et la complexité de la publication et de la mise à jour des applications virtuelles seront augmentés.</p></li>
<li><p>Activité La solution UPM répartira les intégrations des utilisateurs lors de la fermeture de session. Attente Comme précédent.</p></li>
</ul>
<p>¹ l’opération de publication ( <strong> publication-AppVClientPackage </strong> ) ajoute des entrées au catalogue de l’utilisateur, des cartes de habilitation pour l’utilisateur, identifie le magasin local et se termine en effectuant les étapes d’intégration.</p></td>
<td align="left"><p>Après l’implémentation de cette approche dans l’environnement VDI/hôte de connexion à la première connexion,</p>
<ul>
<li><p>Activité Un utilisateur-publication/actualisation est lancé. Attente</p>
<ul>
<li><p>S’il s’agit de la première fois qu’un utilisateur a publié des applications virtuelles (par exemple, non persistant), cette méthode prend la durée habituelle d’une publication/actualisation.</p></li>
<li><p>Les connexions préalables et suivantes seront affectées en préconfigurant les packages (Ajouter/actualiser).</p>
<p></p></li>
</ul></li>
<li><p>Activité Après la publication et l’actualisation, la solution UPM capture les intégrations utilisateur. Attente En fonction de la configuration de la solution UPM, cela peut se produire dans le cadre du processus de déconnexion. Cela entraînera la même surcharge ou une surcharge similaire à la conservation de l’état utilisateur.</p></li>
</ul>
<p>Sur les connexions suivantes:</p>
<ul>
<li><p>Activité La solution UPM applique les intégrations utilisateur au système avant la publication/actualisation.</p></li>
<li><p>Activité L’ajout/actualisation doit préconfigurer toutes les applications ciblées par l’utilisateur. Attente</p>
<ul>
<li><p>Cela peut ralentir considérablement la disponibilité des applications (selon une période de 10 secondes).</p></li>
<li><p>Cela augmente l’heure d’actualisation de publication par rapport au nombre et à la complexité * des applications virtuelles.</p>
<p></p></li>
</ul></li>
<li><p>Activité La publication et l’actualisation traitent les opérations d’annulation de la publication et de publication des modifications apportées aux habilitations du package d’utilisateur.</p></li>
</ul></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">About</th>
<th align="left">About</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p></p>
<ul>
<li><p>Dans la mesure où les intégrations utilisateur sont entièrement préservées, il n’y a pas de tâche, par exemple, l’intégration de l’opération de publication/actualisation. Toutes les applications virtuelles seront disponibles en quelques secondes de connexion.</p></li>
<li><p>La publication/actualisation traite les modifications apportées aux utilisateurs ayant des applications virtuelles qui ont une incidence sur l’interface utilisateur.</p></li>
</ul></td>
<td align="left"><p>Dans la mesure où l’ajout/actualisation doit reconfigurer toutes les applications virtuelles sur la machine virtuelle, le délai d’actualisation de publication sur chaque connexion sera prolongé.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-plc"></a>Impact sur le cycle de vie d’un package

La mise à niveau d’un package est un aspect essentiel du cycle de vie du package. Pour garantir que les utilisateurs ont accès aux packages d’applications virtuelles mis à niveau appropriés (publiés) ou mis à niveau (non publié), il est recommandé de mettre à jour l’image de base pour refléter ces modifications. Pour mieux comprendre pourquoi examinez la section suivante:

App-V 5,0 SP2 a instauré le concept d’États en attente. Par le passé,

-   Si un administrateur a changé d’habilitation ou a créé une nouvelle version d’un package (mise à niveau) et, au cours d’une publication/actualisation, le package était en cours d’utilisation, l’opération d’annulation de publication

-   À présent, si un package est en cours d’utilisation, l’opération est en attente. Les opérations d’annulation de publication et de publication en attente seront traitées lors du redémarrage du service ou si une autre commande publier ou annuler la publication est émise. Dans ce dernier cas, si l’application virtuelle est en cours d’utilisation, l’application virtuelle reste dans un état d’attente. Pour les packages publiés globalement, un redémarrage (ou un redémarrage du service) est souvent nécessaire.

Dans un environnement non persistant, il est peu probable que les opérations en attente soient traitées. Les opérations en attente, par exemple les tâches sont capturées sous **HKEY \ _CURRENT \ _USER**  \\  **logiciel**  \\  **Microsoft**  \\  **AppV**  \\  **client**  \\  **PendingTasks**. Même si cet emplacement est persistant par la solution UPM, si elle n’est pas appliquée à l’environnement avant de se connecter, ce dernier ne sera pas traité.

### <a href="" id="bkmk-evdi"></a>Amélioration de l’interface VDI par le biais de l’optimisation des performances

La section suivante contient des listes contenant des informations sur les documents et les téléchargements Microsoft qui pourraient s’avérer utiles lors de l’optimisation de votre environnement en matière de performances.

**Blog et script .NET NGEN (vivement recommandé)**

À propos de la technologie NGEN

-   [Comment accélérer l’optimisation de NGEN](https://blogs.msdn.com/b/dotnet/archive/2013/08/06/wondering-why-mscorsvw-exe-has-high-cpu-usage-you-can-speed-it-up.aspx)

-   [Script](https://aka.ms/DrainNGenQueue)

**Rôles serveur et serveur Windows**

Recommandations en matière d’optimisation des performances du serveur pour

-   [Microsoft Windows Server 2012 R2](https://msdn.microsoft.com/library/windows/hardware/dn529133.aspx)

-   [Microsoft Windows Server 2012](https://download.microsoft.com/download/0/0/B/00BE76AF-D340-4759-8ECD-C80BC53B6231/performance-tuning-guidelines-windows-server-2012.docx)

-   [Microsoft Windows Server 2008 R2](https://download.microsoft.com/download/6/B/2/6B2EBD3A-302E-4553-AC00-9885BBF31E21/Perf-tun-srv-R2.docx)

**Rôles de serveur**

-   [Hôte de virtualisation du Bureau à distance](https://msdn.microsoft.com/library/windows/hardware/dn567643.aspx)

-   [Hôte de session Bureau à distance](https://msdn.microsoft.com/library/windows/hardware/dn567648.aspx)

-   [Pertinence IIS: gestion d’App-V, publication, création de rapports Web services](https://msdn.microsoft.com/library/windows/hardware/dn567678.aspx)

-   [Pertinence du serveur de fichiers (SMB): s’il est utilisé pour le stockage et la remise des contenus App-V dans le mode SCS](https://technet.microsoft.com/library/jj134210.aspx)

**Recommandations en matière d’optimisation des performances de client Windows (système d’exploitation invité)**

-   [Microsoft Windows 7](https://download.microsoft.com/download/E/5/7/E5783D68-160B-4366-8387-114FC3E45EB4/Performance Tuning Guidelines for Windows 7 Desktop Virtualization v1.9.docx)

-   [Script d’optimisation: (fourni par le support Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2012/10/15/the-microsoft-premier-field-engineer-pfe-view-on-virtual-desktop-vdi-density.aspx)

-   [Microsoft Windows 8](https://download.microsoft.com/download/6/0/1/601D7797-A063-4FA7-A2E5-74519B57C2B4/Windows_8_VDI_Image_Client_Tuning_Guide.pdf)

-   [Script d’optimisation: (fourni par le support Microsoft)](https://blogs.technet.com/b/jeff_stokes/archive/2013/04/09/hot-off-the-presses-get-it-now-the-windows-8-vdi-optimization-script-courtesy-of-pfe.aspx)

## Étapes de séquençage pour optimiser les packages de performance de publication


Plusieurs fonctionnalités d’application V permettent de créer de nouveaux scénarios ou d’activer de nouveaux scénarios de déploiement de clients. Les fonctionnalités suivantes peuvent avoir un impact sur les performances des opérations de publication et de lancement.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Facteur</th>
<th align="left">Avantages</th>
<th align="left">Compromis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aucun bloc de fonctionnalité 1 (FB1, également connu sous le nom de FB-principal)</p></td>
<td align="left"><p>Non FB1 indique que l’application sera lancée immédiatement et qu’elle nécessite une erreur de type fichier (l’application nécessite un fichier, une DLL et qu’elle doit descendre sur le réseau) lors du lancement. S’il existe des limitations réseau, FB1:</p>
<ul>
<li><p>Réduisez le nombre de pannes de flux et de bande passante réseau utilisées lorsque vous lancez une application pour la première fois.</p></li>
<li><p>Retardez le lancement jusqu’à ce que la totalité du FB1 ait été diffusée.</p></li>
</ul></td>
<td align="left"><p>Le dysfonctionnement du flux réduit le temps de démarrage.</p></td>
<td align="left"><p>Les packages d’application virtuelle pour lesquels FB1 est configuré doivent être à nouveau séquencés.</p></td>
</tr>
</tbody>
</table>



### Suppression de FB1

La suppression de FB1 ne nécessite pas le programme d’installation d’application d’origine. Après avoir suivi les étapes ci-dessous, il est recommandé de rétablir l’ordinateur qui exécute le Sequencer sur une capture instantanée saine.

**Interface utilisateur de Sequencer** -créez un nouveau package d’application virtuel.

1.  Suivez les étapes de la séquence pour personnaliser- &gt; streaming.

2.  À l’étape de diffusion, ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou peu fiable**.

3.  Le cas échéant, passez au **système d’exploitation cible**.

**Modifier un package d’application virtuel existant**

1.  Effectuez les étapes de séquençage en continu.

2.  Ne sélectionnez pas **l’option optimiser le package de déploiement sur un réseau lent ou non fiable**.

3.  Accédez à **créer un package**.

**PowerShell** -mise à jour d’un package d’application virtuel existant.

1.  Ouvrez une session PowerShell avec élévation de privilèges.

2.  Import-module **appvsequencer**.

3.  **Update-AppvSequencerPackage**  -  **AppvPackageFilePath**

    "C:\\Packages\\MyPackage.appv"-programme d’installation

    "C:\\PackageInstall\\PackageUpgrade.exe empty.exe"-OutputPath

    "C:\\UpgradedPackages"

    **Remarque**  
    Cette applet de commande nécessite un exécutable (. exe) ou un fichier de commandes (. bat). Vous devez fournir un exécutable vide ou un fichier de commandes.



<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Concernant</th>
<th align="left">Avantages</th>
<th align="left">Compromis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Aucune installation SXS lors de la publication</p></td>
<td align="left"><p>Il n’est pas nécessaire de réorganiser les packages d’applications virtuelles. Les assemblys SxS peuvent rester dans le package d’application virtuel.</p></td>
<td align="left"><p>Les dépendances d’assembly SxS ne sont pas installées au moment de la publication.</p></td>
<td align="left"><p>Les dépendances d’assemblage SxS doivent être préinstallées.</p></td>
</tr>
</tbody>
</table>



### Création d’un package d’application virtuelle sur le Sequencer

Si, au cours d’une analyse de Sequencer, un assemblage SxS (par exemple, un CV + + Runtime) est installé dans le cadre de l’installation d’une application, l’assemblage SxS est automatiquement détecté et inclus dans le package. L’administrateur est alors averti et dispose de l’option d’exclusion de l’assembly SxS.

**Côté client**:

Lors de la publication d’un package d’application virtuelle, le client App-V détectera si une dépendance à l’SxS requise est déjà installée. Si la dépendance n’est pas disponible sur l’ordinateur et qu’elle est incluse dans le package, un programme d’installation Windows traditionnel (.** MSI**) l’installation de l’assembly SxS sera lancée. Comme nous l’avons mentionné précédemment, installez simplement la dépendance sur l’ordinateur exécutant le client pour vérifier que l’installation de Windows Installer (. msi) ne se produit pas.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Concernant</th>
<th align="left">Avantages</th>
<th align="left">Compromis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisation sélective de fichiers de configuration dynamiques</p></td>
<td align="left"><p>Le client App-V 5,1 doit analyser et traiter les fichiers de configuration dynamique suivants.</p>
<p>Soyez conscient de la taille et de la complexité (exécution du script, inclusions ou exclusions VREG) du fichier.</p>
<p>De nombreux packages d’applications virtuelles peuvent avoir déjà des fichiers de configurations dynamiques spécifiques à un utilisateur ou à un ordinateur.</p></td>
<td align="left"><p>Les durées de publication sont améliorées si ces fichiers sont utilisés de manière sélective ou pas du tout.</p></td>
<td align="left"><p>Les packages d’applications virtuelles devront être reconfigurés individuellement ou via la console de gestion de l’application-V Server pour supprimer les fichiers de configuration dynamique associés.</p></td>
</tr>
</tbody>
</table>



### Désactivation d’une configuration dynamique à l’aide de PowerShell

-   Pour les packages déjà publiés, vous pouvez utiliser `Set-AppVClientPackage –Name Myapp –Path c:\Packages\Apps\MyApp.appv` sans

    Paramètre **-DynamicDeploymentConfiguration**

-   De même, lorsque vous ajoutez de nouveaux packages à l’aide de `Add-AppVClientPackage –Path c:\Packages\Apps\MyApp.appv` , n’utilisez pas le

    Paramètre **-DynamicDeploymentConfiguration** .

Pour obtenir des informations sur la façon d’appliquer une configuration dynamique, voir:

-   [Comment appliquer le fichier de configuration utilisateur à l'aide de PowerShell](how-to-apply-the-user-configuration-file-by-using-powershell51.md)

-   [Comment appliquer le fichier de configuration du déploiement à l'aide de PowerShell](how-to-apply-the-deployment-configuration-file-by-using-powershell51.md)

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Concernant</th>
<th align="left">Avantages</th>
<th align="left">Compromis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Compte d’exécution de script synchrone lors du cycle de vie du package.</p></td>
<td align="left"><p>S’il est incorporé dans le package, l’ajout (PowerShell) peut être considérablement plus lent.</p>
<p>L’exécution de scripts lors du lancement d’une application virtuelle (StartVirtualEnvironment, StartProcess) et/ou ajout + publication aura un impact sur les performances perçues lors d’une ou plusieurs de ces opérations de cycle de vie.</p></td>
<td align="left"><p>L’utilisation de scripts asynchrones (sans blocage) permet de garantir que les opérations de cycle de vie s’exécutent efficacement.</p></td>
<td align="left"><p>Cette étape nécessite une connaissance du fonctionnement de tous les packages d’applications virtuelles incluant des brochures de script intégrées, qui disposent de fichiers de configurations dynamiques associés et de références et d’exécution des scripts de manière synchrone.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Supprimer les polices virtuelles superflues du package.</p></td>
<td align="left"><p>La plupart des applications examinées par l’équipe de produit App-V contenaient un petit nombre de polices, généralement moins de 20.</p></td>
<td align="left"><p>Les polices virtuelles influent sur les performances de la publication.</p></td>
<td align="left"><p>Les polices souhaitées devront être activées ou installées en mode natif. Pour obtenir des instructions, voir installer ou désinstaller des polices.</p></td>
</tr>
</tbody>
</table>



### Identifier les polices virtuelles qui existent dans le package

-   Effectuez une copie du package.

-   Renommer le package \ _copy. AppV en Package\_copy.zip

-   Ouvrez AppxManifest.xml et recherchez les éléments suivants:

    &lt;AppV: extension category = "AppV. polices"&gt;

    &lt;AppV: polices&gt;

    &lt;AppV: chemin de police = "\ [{Fonts} \] \\private\\CalibriL.ttf" DelayLoad = "true" &gt; &lt; /AppV: font&gt;

    **Remarque**  
    S’il existe des polices marquées comme **DelayLoad**, celles-ci n’ont aucun impact sur le premier lancement.



~~~
&lt;/appv:Fonts&gt;
~~~

### Exclusion de polices virtuelles du package

Utilisez le fichier de configuration dynamique qui correspond le mieux à la configuration de déploiement pour tous les utilisateurs sur un ordinateur, configuration utilisateur pour des utilisateurs ou des utilisateurs spécifiques.

-   Désactiver les polices avec le déploiement ou la configuration de l’utilisateur.

Polices

--&gt;

&lt;Polices activées = "faux"/&gt;

&lt;!--

## <a href="" id="bkmk-terms1"></a> Terminologie des recommandations en matière de performances de App-V 5,1


Les termes suivants sont utilisés lors de la description des concepts et actions liés à l’optimisation des performances d’App-V 5,1.

-   **Complexité** : désigne l’une ou plusieurs caractéristiques de package susceptibles d’avoir un impact sur les performances lors de la préconfiguration (**Add-AppvClientPackage**) ou de l’intégration (**publication-AppvClientPackage**). Voici quelques exemples de caractéristiques: taille du manifeste, nombre de polices virtuelles, nombre de fichiers.

-   **Désintégration** : supprime les intégrations utilisateur.

-   **Nouvelle intégration** : applique les intégrations utilisateur.

-   **Non permanent, en regroupement** : crée un ordinateur exécutant un environnement virtuel chaque fois qu’il se connecte.

-   **Permanent et personnel** : ordinateur exécutant un environnement virtuel qui reste le même pour chaque connexion.

-   **État** -pour ce document, ce qui signifie que les intégrations des utilisateurs sont conservées entre les sessions et qu’une technologie de gestion de l’environnement utilisateur est utilisée en conjonction avec un hôte de session hôte ou VDI non persistant.

-   **Sans état** – représente un scénario dans lequel aucun état utilisateur n’est persistant entre les sessions.

-   **Déclencheur** (déclencheur d’action natif). UPM utilise ces types de déclencheurs pour lancer des opérations de surveillance ou de synchronisation.

-   **Interface utilisateur** : dans le contexte de App-V 5,1, l’interface utilisateur, quantitativement, est la somme des parties suivantes:

    -   À partir du moment où les utilisateurs ouvrent une session pour pouvoir manipuler le bureau.

    -   À partir du moment où le Bureau peut être utilisé pour une actualisation de publication (dans les termes de PowerShell, la synchronisation) lors de l’utilisation de l’infrastructure serveur complète App-V 5,1. Dans les instances autonomes, il s’agit du moment où les commandes PowerShell **Add-AppVClientPackage** et **Publish-AppVClientPackage** sont initialisées.

    -   Du début à la fin de l’actualisation de la publication. Dans les instances autonomes, il s’agit de la première à la dernière application virtuelle publiée.

    -   À partir du moment où l’application virtuelle est disponible pour le lancement à partir d’un raccourci. Par ailleurs, il s’agit de l’emplacement d’enregistrement de l’Association de type de fichier et lancera une application virtuelle spécifiée.

-   **Gestion des profils utilisateur** : l’approche contrôlée et structurée pour gérer les composants utilisateur associés à l’environnement. Par exemple, profils utilisateur, gestion des préférences et de la stratégie, contrôle d’application et déploiement d’application. Vous pouvez utiliser la création de scripts ou des solutions tierces pour configurer l’environnement selon vos besoins.






## Rubriques connexes


[Guide de l’administrateur de Microsoft Application Virtualization 5,1](microsoft-application-virtualization-51-administrators-guide.md)









