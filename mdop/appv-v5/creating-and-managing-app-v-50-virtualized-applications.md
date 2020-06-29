---
title: Création et gestion d'applications virtualisées App-V5.0
description: Création et gestion d'applications virtualisées App-V5.0
author: dansimp
ms.assetid: 66bab403-d7e0-4e7b-bc8f-a29a98a7160a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 86332c7753b70abbaaf289fc1ba046bf59d1dd89
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805923"
---
# Création et gestion d'applications virtualisées App-V5.0


Une fois que vous avez correctement déployé le Sequencer Microsoft Application Virtualization (App-V) 5,0, vous pouvez l’utiliser pour surveiller et enregistrer le processus d’installation et de configuration pour qu’une application s’exécute en tant qu’application virtualisée.

**Remarques**  Pour plus d’informations sur la configuration du Sequencer Microsoft Application Virtualization (App-V) 5,0, le séquençage des meilleures pratiques et un exemple de création et de mise à jour d’une application virtuelle, voir le Guide de mise en route de [Microsoft application virtualization 5,0](https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5.0 Sequencing Guide.docx) ( https://download.microsoft.com/download/F/7/8/F784A197-73BE-48FF-83DA-4102C05A6D44/App-V 5,0 séquençage Guide.docx).

 

## Séquençage d’une application


Vous pouvez utiliser le Sequencer App-V 5,0 pour effectuer les tâches suivantes:

-   Créer des packages virtuels qui peuvent être déployés sur des ordinateurs exécutant le client App-V 5,0.

-   Mettre à niveau des packages existants. Vous pouvez développer un package existant sur l’ordinateur exécutant le Sequencer, puis mettre à niveau l’application pour créer une version plus récente.

-   Modifier les informations de configuration associées à un package existant. Par exemple, vous pouvez ajouter un raccourci ou modifier une association de type de fichier.

    **Remarques**  Vous devez créer des raccourcis et les enregistrer dans un emplacement réseau disponible pour autoriser l’itinérance. Si un raccourci est créé et enregistré dans un emplacement privé, le package doit être publié localement sur l’ordinateur exécutant le client App-V 5,0.

     

-   Convertir des packages virtuels existants.

Le Sequencer utilise le répertoire **% tmp% \ \ Scratch** ou **% TEMP% \ \ Scratch** , ainsi que **le répertoire temporaire pour** le stockage des fichiers temporaires lors du séquençage. Sur l’ordinateur qui exécute le Sequencer, vous devez configurer ces annuaires avec l’espace disque disponible correspondant à la configuration estimée requise pour l’installation de l’application. La configuration des répertoires temporaires et du répertoire temporaire sur différentes partitions de disque dur peut contribuer à améliorer les performances lors du séquençage.

Lorsque vous utilisez le Sequencer pour créer une nouvelle application virtuelle, les fichiers répertoriés suivants sont créés. Ces fichiers comprennent le package App-V 5,0.

-   fichier. msi. Ce fichier Windows Installer (. msi) est créé par le Sequencer et est utilisé pour installer le package virtuel sur les ordinateurs cibles.

-   Report.xml un fichier. Dans ce fichier, le Sequencer enregistre tous les problèmes, avertissements et erreurs identifiés lors du séquençage. Il affiche les informations après la création du package. Vous pouvez nous faire parvenir ce rapport pour détecter et résoudre les problèmes.

-   fichier. AppV. Il s’agit du fichier d’application virtuel.

-   Fichier de configuration de déploiement. Le fichier de configuration de déploiement détermine la façon dont l’application virtuelle sera déployée sur les ordinateurs cibles.

-   Fichier de configuration de l’utilisateur. Le fichier de configuration utilisateur détermine la façon dont l’application virtuelle s’exécute sur les ordinateurs cibles.

**Important**  Vous devez configurer les dossiers% TMP% et% TEMP% que le convertisseur de package utilise pour être sécurisé et l’annuaire. Un emplacement sécurisé est accessible uniquement par un administrateur. Par ailleurs, lorsque vous séquencez le package, vous devez enregistrer le package à un emplacement sécurisé ou vérifier qu’aucun autre utilisateur n’est autorisé à se connecter pendant le processus de conversion et de surveillance.

 

La boîte de dialogue **options** de la console Sequencer contient les onglets suivants:

-   Informations **générales**. Utilisez cet onglet pour autoriser l’exécution des mises à jour de Microsoft lors du séquençage. Sélectionnez **Ajouter la version du package au nom du fichier** pour configurer la séquence pour ajouter un numéro de version au package virtualisé en cours de séquence. Sélectionnez **toujours faire confiance à la source des accélérateurs de package** pour créer des packages virtualisés à l’aide d’un accélérateur de package sans être invité à procéder à une autorisation.

    **Important**  Les accélérateurs de package créés à l’aide de App-V 4.6 ne sont pas pris en charge par App-V 5,0.

     

-   **Analyser des éléments**. Cet onglet affiche les emplacements de chemin d’accès de fichier associés qui seront analysés ou qui sont considérés comme étant dans l’environnement virtuel. Les jetons sont utiles pour ajouter des fichiers à l’aide de l’onglet **fichiers du package** dans **modification avancée**.

-   **Éléments d’exclusion**. Utilisez cet onglet pour spécifier quels dossiers et répertoires ne doivent pas être analysés lors du séquençage. Pour ajouter des données d’application locales enregistrées dans le dossier Data App local du package, cliquez sur **nouveau** , puis spécifiez l’emplacement et le **type de mappage**associé. Cette option est obligatoire pour certains packages.

App-V 5,0 prend en charge les applications incluant des services Microsoft Windows. Si une application inclut un service Windows, le service sera inclus dans le package virtuel séquencé tant qu’il est installé lors de la surveillance par le Sequencer. Si une application virtuelle crée un service Windows lors de son exécution initiale, puis ultérieurement, après l’installation, l’application doit être exécutée pendant que le Sequencer analyse le fonctionnement du service Windows. Seuls les services exécutés sous le compte système local sont pris en charge. Les services qui sont configurés pour le démarrage automatique ou le démarrage automatique retardé sont démarrés avant que la première application virtuelle d’un package s’exécute à l’intérieur de l’environnement virtuel du package. Les services Windows configurés pour être démarrés à la demande par une application sont démarrés lorsque l’application virtuelle à l’intérieur du package démarre le service via l’appel d’API.

[Comment séquencer une nouvelle application avec App-V5.0](how-to-sequence-a-new-application-with-app-v-50-beta-gb18030.md)

## <a href="" id="---------app-v-5-0-sp2-shell-extension-support"></a> Prise en charge de l’extension Shell App-V 5.0 SP2


App-V 5.0 SP2 prend en charge les extensions d’environnement. Les extensions d’environnement seront détectées et incorporées dans le package lors du séquençage.

Les extensions d’interpréteur sont incorporées automatiquement dans le package lors du processus de séquençage. Lorsque le package est publié, l’extension d’interpréteur de Shell donne aux utilisateurs les mêmes fonctionnalités que si l’application a été installée localement.

**Configuration requise pour l’utilisation des extensions d’interpréteur de tâches:**

-   Les packages contenant des extensions d’interpréteur de Troie doivent être publiés globalement. L’application ne nécessite aucune installation ou configuration supplémentaire sur le client pour activer la fonctionnalité d’extension du shell.

-   Le nombre de bits d’application, de Sequencer et de client App-V doit correspondre ou les extensions de Shell ne fonctionnent pas. Exemple:

    -   La version de l’application est 64 bits.

    -   Le Sequencer s’exécute sur un ordinateur 64 bits.

    -   Le package est remis à un ordinateur client d’application 64 bits.

Le tableau suivant répertorie les extensions d’environnement prises en charge:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Gestionnaire d'</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Gestionnaire de menu contextuel</p></td>
<td align="left"><p>Ajoute des éléments de menu dans le menu contextuel. Il est appelé avant que le menu contextuel ne s’affiche.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire de glisser-déplacer</p></td>
<td align="left"><p>Contrôle l’action en cliquant avec le bouton droit, puis en faisant glisser et en modifiant le menu contextuel qui s’affiche.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Supprimer le gestionnaire de cibles</p></td>
<td align="left"><p>Contrôle l’action après le glissement et la suppression d’un objet de données sur une cible de dépôt telle qu’un fichier.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’objets de données</p></td>
<td align="left"><p>Contrôle l’action après qu’un fichier est copié dans le presse-papiers ou glissé et déposé sur une cible de déplacement. Il peut fournir des formats de presse-papiers supplémentaires à la cible de dépôt.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de feuilles de propriétés</p></td>
<td align="left"><p>Remplace ou ajoute des pages dans la boîte de dialogue feuille de propriétés d’un objet.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’info-bulle</p></td>
<td align="left"><p>Permet de récupérer les indicateurs et les informations de l’info-bulle d’un élément et de l’afficher dans une info-bulle contextuelle lors du survol de la souris.</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Gestionnaire de colonnes</p></td>
<td align="left"><p>Autorise la création et l’affichage de colonnes personnalisées dans l' <strong> affichage détaillé de l’Explorateur Windows </strong> . Elle peut être utilisée pour étendre le tri et le regroupement.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Gestionnaire d’aperçu</p></td>
<td align="left"><p>Permet d’afficher un aperçu d’un fichier dans le volet de visualisation de l’Explorateur Windows.</p></td>
</tr>
</tbody>
</table>

 

## Extension de la prise en charge de l’extension de fichier


Les extensions de fichier copie sur écriture (vache) permettent à l’application-V 5,0 d’écrire de manière dynamique sur des emplacements spécifiques contenus dans le package virtuel lors de son utilisation.

Le tableau suivant répertorie les types de fichiers qui peuvent exister dans un package virtuel sous le répertoire VFS, mais qui ne peuvent pas être mis à jour sur l’ordinateur exécutant le client App-V 5,0. Tous les autres fichiers et répertoires peuvent être modifiés.

. acm

. ASA

.asp

. aspx

. ax

.bat

.cer

.chm

. CLB

.cmd

.cnt

. cnv

.com

.cpl

. CPX

.crt

.dll

.drv

.exe

.fon

.grp

.hlp

.hta

. IME

.inf

.ins

.isp

. ses

.js

.jse

.lnk

.msc

.msi

.msp

.mst

. mui

. nls

.ocx

. PAL

.pcd

.pif

.reg

.scf

.scr

. SCT

.shb

.shs

.sys

. tlb

. tsp

.url

.vb

.vbe

.vbs

.vsmacros

.ws

. Échap

.wsf

.wsh

 

## Modification d’un package d’application virtuelle existant


Vous pouvez utiliser le Sequencer pour modifier un package existant. L’ordinateur sur lequel vous procédez ainsi doit correspondre à l’architecture de processeur de l’ordinateur que vous avez utilisé pour créer l’application. Par exemple, si vous avez initialement séquencé un package à l’aide d’un ordinateur exécutant un système d’exploitation 64 bits, vous devez modifier le package à l’aide d’un ordinateur exécutant un système d’exploitation 64 bits.

[Comment modifier un package d'application virtuelle existant](how-to-modify-an-existing-virtual-application-package-beta.md)

## Création d’un modèle de projet


Un fichier. appvt est un modèle de projet qui peut être utilisé pour enregistrer les paramètres personnalisés fréquemment appliqués. Vous pouvez ensuite plus facilement utiliser ces paramètres pour de futurs séquençages.

Les modèles de projet App-V 5,0 diffèrent des accélérateurs d’application à l’application-V 5,0, car les accélérateurs d’application-V 5,0 sont propres à l’application et les modèles de projets App-V 5,0 peuvent être appliqués à plusieurs applications. Par ailleurs, vous ne pouvez pas utiliser un modèle de projet lorsque vous utilisez un accélérateur de package pour créer un package d’application virtuelle. Les paramètres généraux suivants sont enregistrés avec un modèle de projet App-V 5,0:

Un modèle peut spécifier et stocker plusieurs paramètres comme suit:

-   **Options de surveillance avancée**. Autorise l’exécution de Microsoft Update lors du suivi. Enregistre les paramètres autoriser les interactions locales

-   **Options générales**. Active l’utilisation du **programme d’installation Windows**, **Ajouter la version du package au nom de fichier**.

-   **Éléments d’exclusion.** Contient la liste modèle d’exclusion.

[Comment créer et utiliser un modèle de projet](how-to-create-and-use-a-project-template.md)

## Création d’un accélérateur de package


**Remarques**  Les accélérateurs de package créés à l’aide d’une version antérieure de App-V doivent être recréés à l’aide de App-V 5,0.

 

Vous pouvez utiliser les accélérateurs de package App-V 5,0 pour générer automatiquement un nouveau package d’application virtuel. Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package.

Dans certains cas, pour créer l’accélérateur de package, vous devrez peut-être installer l’application localement sur l’ordinateur qui exécute le Sequencer. Dans ces cas, vous devez commencer par créer l’accélérateur de package à l’aide du support d’installation. Si plusieurs fichiers manquants sont requis, vous devez installer l’application localement sur l’ordinateur qui exécute le Sequencer, puis créer l’accélérateur de package.

Une fois que vous avez correctement créé un accélérateur de package, vous pouvez réutiliser et partager l’accélérateur de package. Le fait de créer des accélérateurs de package App-V 5,0 est une tâche avancée. Les accélérateurs de package peuvent contenir des informations relatives aux mots de passe et aux utilisateurs. Par conséquent, vous devez enregistrer les accélérateurs de packages et le média d’installation associé dans un emplacement sécurisé, et vous devez signer numériquement l’accélérateur de package après l’avoir créé, afin que l’éditeur puisse être vérifié lorsque l’accélérateur de package App-V 5,0 est appliqué.

[Comment créer un accélérateur de package](how-to-create-a-package-accelerator.md)

[Comment créer un package d'application virtuelle à l'aide d'un accélérateur de package App-V](how-to-create-a-virtual-application-package-using-an-app-v-package-accelerator.md)

## Rapports d’erreur de Sequencer


Le Sequencer App-V 5,0 peut détecter les problèmes courants de séquençage lors du séquençage. La page **rapport d’installation** à la fin de l’Assistant séquençage affiche les messages de diagnostic classés en **erreurs**, **avertissements**et **informations** en fonction de la gravité du problème.

Vous pouvez également accéder à des informations supplémentaires sur les erreurs de séquençage à l’aide de l’observateur d’événements Windows.






## <a href="" id="other-resources-for-the-app-v-5-0-sequencer-"></a>Autres ressources pour le Sequencer App-V 5,0


-   [Opérations d'App-V5.0](operations-for-app-v-50.md)

 

 





