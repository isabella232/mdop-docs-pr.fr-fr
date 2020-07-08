---
title: À propos d'App-V5.1
description: À propos d'App-V5.1
author: dansimp
ms.assetid: 35bc9908-d502-4a9c-873f-8ee17b6d9d74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4f2404dcd431b32f5d9a4ae7c49f1e376979e04e
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806109"
---
# À propos d'App-V5.1


Les sections suivantes permettent de consulter des informations sur les modifications importantes apportées à l’application virtualisation des applications (App-V) 5,1:

[Conditions préalables pour le logiciel App-V 5,1 et configurations prises en charge](#bkmk-51-prereq-configs)

[Migration vers App-V 5,1](#bkmk-migrate-to-51)

[Nouveautés de l’application-V 5,1](#bkmk-whatsnew)

[Prise en charge de App-V pour Windows 10](#bkmk-win10support)

[Modifications apportées à la console de gestion App-V](#bkmk-mgmtconsole)

[Améliorations apportées au Sequencer](#bkmk-seqimprove)

[Améliorations apportées au convertisseur de package](#bkmk-pkgconvimprove)

[Prise en charge de plusieurs scripts sur un seul déclencheur d’événements](#bkmk-supmultscripts)

[Le chemin d’accès codé au dossier d’installation est redirigé vers la racine du système de fichiers virtuel](#bkmk-hardcodepath)

## <a href="" id="bkmk-51-prereq-configs"></a>Conditions préalables pour le logiciel App-V 5,1 et configurations prises en charge


Pour plus d’informations 5,1 sur les configurations logicielles prises en charge, voir les liens suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Liens vers les composants requis et les configurations prises en charge</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="app-v-51-prerequisites.md" data-raw-source="[App-V 5.1 Prerequisites](app-v-51-prerequisites.md)">Composants requis d'App-V5.1</a></p></td>
<td align="left"><p>Logiciels requis que vous devez installer avant de démarrer l’installation App-V 5,1</p></td>
</tr>
<tr class="even">
<td align="left"><p><a href="app-v-51-supported-configurations.md" data-raw-source="[App-V 5.1 Supported Configurations](app-v-51-supported-configurations.md)">Configurations prises en charge par App-V5.1</a></p></td>
<td align="left"><p>Systèmes d’exploitation pris en charge et configuration matérielle requise pour le serveur App-V, le Sequencer et les composants clients</p></td>
</tr>
</tbody>
</table>



**Prise en charge de l’utilisation de Configuration Manager avec App-V:** App-V 5,1 prend en charge System Center 2012 R2 Configuration Manager SP1. Pour plus d’informations sur l’intégration de votre environnement App-v au gestionnaire de configuration et à la gestion de configuration, voir [planification de l’intégration d’App-v à Configuration Manager](https://technet.microsoft.com/library/jj822982.aspx) .

## <a href="" id="bkmk-migrate-to-51"></a>Migration vers App-V 5,1


Utilisez les informations ci-dessous pour effectuer une mise à niveau vers l’application-V 5,1 à partir d’une version antérieure. Pour plus d’informations, reportez-vous [à la rubrique migration vers App-V 5,1 à partir d’une version précédente](migrating-to-app-v-51-from-a-previous-version.md) .

### Avant de commencer la mise à niveau

Passez en revue les informations suivantes avant de commencer la mise à niveau:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Éléments à réviser avant la mise à niveau</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Composants à mettre à niveau, dans n’importe quel ordre</p></td>
<td align="left"><ol>
<li><p>App-V Server</p></li>
<li><p>Sequencer</p></li>
<li><p>Client App-V ou App-V (service bureau à distance)</p></li>
</ol>
<div class="alert">
<strong>Remarque</strong><br/><p>Avant le SP2 App-V 5,0, l’interface utilisateur de gestion des clients a été fournie avec l’installation du client App-V. Pour les installations d’App-V 5,0 SP2 (ou version ultérieure), vous pouvez utiliser l’interface utilisateur de gestion du client en le téléchargeant à partir de l’application de l' <a href="https://www.microsoft.com/download/details.aspx?id=41186" data-raw-source="[Application Virtualization 5.0 Client UI Application](https://www.microsoft.com/download/details.aspx?id=41186)"> interface utilisateur du client de virtualisation des applications 5,0 </a> .</p>
</div>
<div>

</div></td>
</tr>
<tr class="even">
<td align="left"><p>Mise à niveau à partir de App-V 4. x</p></td>
<td align="left"><p>Vous devez d’abord effectuer une mise à niveau vers App-V 5,0. Vous ne pouvez pas effectuer la mise à niveau directement de App-V 4. x vers App-V 5,1. Pour plus d’informations, voir:</p>
<ul>
<li><p>«Différences entre App-V 4,6 et App-V 5,0» dans <a href="about-app-v-50.md" data-raw-source="[About App-V 5.0](about-app-v-50.md)"> à propos de App-v 5,0</a></p></li>
<li><p><a href="planning-for-migrating-from-a-previous-version-of-app-v.md" data-raw-source="[Planning for Migrating from a Previous Version of App-V](planning-for-migrating-from-a-previous-version-of-app-v.md)">Planification d'une migration à partir d'une version précédente d'App-V</a></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td align="left"><p>Mise à niveau à partir de App-V 5,0 ou version ultérieure</p></td>
<td align="left"><p>Vous pouvez effectuer une mise à niveau vers App-V 5,1 directement à partir des versions suivantes:</p>
<ul>
<li><p>App-V 5,0</p></li>
<li><p>App-V 5,0 SP1</p></li>
<li><p>App-V 5,0 SP2</p></li>
<li><p>App-V 5,0 SP3</p></li>
</ul>
<p>Pour effectuer une mise à niveau vers App-V 5,1, suivez les étapes décrites dans les sections restantes de cette rubrique.</p>
<p>Les packages et les groupes de connexion continuent de fonctionner avec l’application-V 5,1 comme il le fait actuellement.</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-steps-upgrd-infrastruc"></a>Procédure de mise à niveau de l’infrastructure App-V

Suivez les étapes ci-dessous pour mettre à niveau chaque composant de l’infrastructure App-V vers App-V 5,1. L’ordre suivant n’est qu’une suggestion; vous pouvez mettre à niveau des composants dans n’importe quel ordre.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Étape</th>
<th align="left">Pour plus d’informations</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Étape 1: mettez à niveau le serveur App-V.</p>
<div class="alert">
<strong>Remarque</strong><br/><p>Si vous n’utilisez pas le serveur App-V, ignorez cette étape et passez à l’étape suivante.</p>
</div>
<div>

</div></td>
<td align="left"><p>Procédez comme suit: </p>
<ol>
<li><p>Effectuez l’une des opérations suivantes, selon la méthode que vous utilisez pour mettre à niveau la base de données de gestion et/ou la base de données de création de rapports, procédez comme suit:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Méthode de mise à niveau de base de données</th>
<th align="left">Étape</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Windows Installer</p></td>
<td align="left"><p>Ignorez cette étape et passez à l’étape 2, «si vous effectuez la mise à niveau de l’application-V Server».</p></td>
</tr>
<tr class="even">
<td align="left"><p>Scripts SQL</p></td>
<td align="left"><p>Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-databases-by-using-sql-scripts.md" data-raw-source="[How to Deploy the App-V Databases by Using SQL Scripts](how-to-deploy-the-app-v-databases-by-using-sql-scripts.md)"> procédure de déploiement des bases de données App-V à l’aide de scripts SQL </a> .</p></td>
</tr>
</tbody>
</table>
<li><p>Si vous effectuez une mise à niveau de l’application-V Server à partir du correctif logiciel App-V 5,0 SP1 ou version ultérieure, suivez les étapes de la section <a href="check-reg-key-svr.md" data-raw-source="[Check registry keys after installing the App-V 5.0 SP3 Server](check-reg-key-svr.md)"> vérifier les clés de registre après l’installation de l’app-v 5,0 SP3 Server </a> .</p></li>
<li><p>Suivez les étapes décrites dans la <a href="how-to-deploy-the-app-v-51-server.md" data-raw-source="[How to Deploy the App-V 5.1 Server](how-to-deploy-the-app-v-51-server.md)"> procédure de déploiement du serveur App-V 5,1</a></p></li>
<p> </p></li>
</ol></td>
</tr>
<tr class="even">
<td align="left"><p>Étape 2: mettre à niveau le Sequencer App-V.</p></td>
<td align="left"><p>Découvrez <a href="how-to-install-the-sequencer-beta-gb18030.md" data-raw-source="[How to Install the Sequencer](how-to-install-the-sequencer-beta-gb18030.md)"> Comment installer le Sequencer </a> .</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Étape 3: mettez à niveau le client App-V ou le client RDS (App-V).</p></td>
<td align="left"><p>Découvrez <a href="how-to-deploy-the-app-v-client-gb18030.md" data-raw-source="[How to Deploy the App-V Client](how-to-deploy-the-app-v-client-gb18030.md)"> comment déployer le client App-V </a> .</p></td>
</tr>
</tbody>
</table>



### Conversion de packages créés à l’aide d’une version antérieure d’App-V

Utilisez l’utilitaire convertisseur de package pour mettre à niveau des packages d’application virtuels créés à l’aide de versions de App-V antérieures à App-V 5,0. Le convertisseur de package utilise PowerShell pour convertir des packages et peut faciliter l’automatisation du processus si vous avez de nombreux packages qui nécessitent une conversion.

**Remarque**  
Les packages App-V 5,1 sont exactement les mêmes que les packages App-V 5,0. Il n’y a aucune modification du format de package entre les versions et il n’est donc pas nécessaire de convertir les packages App-V 5,0 en packages App-V 5,1.



## <a href="" id="bkmk-whatsnew"></a>Nouveautés de l’application-V 5,1


Ces sections concernent les utilisateurs qui connaissent déjà App-V et qui souhaitent savoir ce qui a changé dans App-V 5,1. Si vous n’avez pas encore l’habitude d’utiliser l’application-V, vous devez commencer par lire la [planification pour App-v 5,1](planning-for-app-v-51.md).

### <a href="" id="bkmk-win10support"></a>Prise en charge de App-V pour Windows 10

Le tableau suivant répertorie la prise en charge de Windows 10 pour App-V. Windows 10 n’est pas pris en charge dans les versions de App-V antérieures à App-V 5,1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Composant</th>
<th align="left">App-V 5.1</th>
<th align="left">App-V 5,0</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Client App-V</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="even">
<td align="left"><p>Client de RDS App-V</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
<tr class="odd">
<td align="left"><p>Séquenceur App-V</p></td>
<td align="left"><p>Oui</p></td>
<td align="left"><p>Non</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-mgmtconsole"></a>Modifications apportées à la console de gestion App-V

Cette section compare les fonctionnalités actuelles et précédentes de la console de gestion de l’application.

### Silverlight n’est plus nécessaire

L’interface utilisateur de la console de gestion n’exige plus Silverlight. La console de gestion 5,1 est basée sur HTML5 et JavaScript.

### Les notifications et les messages s’affichent individuellement dans une boîte de dialogue

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nouveauté de App-V 5,1</th>
<th align="left">Avant l’application-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Nombre d’indicateur de messages:</strong></p>
<p>Dans la barre de titre de la console de gestion App-V, un numéro est désormais affiché en regard d’une icône d’indicateur indiquant le nombre de messages en attente de lecture.</p></td>
<td align="left"><p>Vous ne pouviez voir qu’un seul message ou erreur à la fois, et vous n’êtes pas en mesure de déterminer le nombre de messages.</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Aspect du message:</strong></p>
<ul>
<li><p>Les messages qui requièrent une entrée utilisateur s’affichent dans une boîte de dialogue séparée qui s’affiche en haut de la page actuellement affichée et nécessitent une réponse avant de pouvoir les faire disparaître.</p></li>
<li><p>Les messages et les erreurs apparaissent dans une liste, l’un sous l’autre.</p></li>
</ul></td>
<td align="left"><p>Vous ne pouviez voir qu’un seul message ou erreur à la fois.</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Ignorer les messages:</strong></p>
<p>Utilisez le <strong> lien rejeter tout </strong> pour masquer tous les messages et erreurs en une fois, ou les ignorer un par un.</p></td>
<td align="left"><p>Vous pouvez faire disparaître des messages et des erreurs une seule fois.</p></td>
</tr>
</tbody>
</table>



### Les pages de console sont désormais des URL distinctes

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nouveauté de App-V 5,1</th>
<th align="left">Avant l’application-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Chaque page de la console possède une autre URL qui vous permet de marquer des pages spécifiques pour un accès rapide à l’avenir.</p>
<p>Le nombre qui apparaît dans certaines URL indique le package spécifique. Ces numéros sont uniques.</p></td>
<td align="left"><p>Toutes les pages de la console sont accessibles par le biais de la même URL.</p></td>
</tr>
</tbody>
</table>



### Nouvelle page de groupes de connexion séparés et option de menu

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nouveauté de App-V 5,1</th>
<th align="left">Avant l’application-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>La page groupes de connexion fait désormais partie du menu principal, au même niveau que la page PACKAGES.</p></td>
<td align="left"><p>Pour ouvrir la page groupes de connexions, vous naviguez dans la page PACKAGES.</p></td>
</tr>
</tbody>
</table>



### Les options de menu pour les packages ont changé

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Nouveauté de App-V 5,1</th>
<th align="left">Avant l’application-V 5,1</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Les options suivantes sont désormais des boutons qui apparaissent en bas de la page PACKAGES:</p>
<ul>
<li><p>Ajouter ou mettre à niveau</p></li>
<li><p>Publier</p></li>
<li><p>Annuler la publication</p></li>
<li><p>Delete</p></li>
</ul>
<p>Les options suivantes s’affichent quand vous cliquez avec le bouton droit sur un paquet pour ouvrir le menu contextuel de menu déroulant:</p>
<ul>
<li><p>Publier</p></li>
<li><p>Annuler la publication</p></li>
<li><p>Modifier l’accès aux publicités</p></li>
<li><p>Modifier la configuration de déploiement</p></li>
<li><p>Transférer la configuration de déploiement de...</p></li>
<li><p>Transférer l’accès et la configuration de...</p></li>
<li><p>Delete</p></li>
</ul>
<p>Lorsque vous cliquez sur <strong> supprimer </strong> pour supprimer un package, une boîte de dialogue s’ouvre et vous demande de confirmer que vous souhaitez supprimer le package.</p></td>
<td align="left"><p>L' <strong> option Ajouter ou mettre à niveau </strong> était un bouton dans la partie supérieure droite de la page Packages.</p>
<p>Les <strong> </strong> options publier, <strong> Annuler </strong> et <strong> supprimer </strong> étaient disponibles uniquement si vous avez cliqué avec le bouton droit sur un nom de package dans la liste packages.</p></td>
</tr>
<tr class="even">
<td align="left"><p>Les opérations de package suivantes sont désormais des boutons de la page Détails du package pour chaque package:</p>
<ul>
<li><p>Transfert (menu déroulant avec les options suivantes):</p>
<ul>
<li><p>Transférer la configuration de déploiement de...</p></li>
<li><p>Transférer l’accès et la configuration de...</p></li>
</ul></li>
<li><p>Modifier (groupes de connexion et accès AD)</p></li>
<li><p>Annuler la publication</p></li>
<li><p>Delete</p></li>
<li><p>Modifier la configuration par défaut</p></li>
</ul></td>
<td align="left"><p>Ces options de package n’étaient disponibles que si vous avez cliqué avec le bouton droit sur un nom de package dans la liste packages.</p></td>
</tr>
</tbody>
</table>



### Les icônes dans le volet de gauche contiennent de nouvelles couleurs et du texte

Les couleurs des icônes dans le volet de gauche ont été modifiées, et le texte qui a été ajouté pour rendre les icônes cohérentes avec d’autres produits Microsoft.

### La page de présentation a été supprimée

Dans le volet gauche de la console de gestion, l’option de menu vue d’ensemble et la page de vue d’ensemble qui lui sont associées ont été supprimées.

### <a href="" id="bkmk-seqimprove"></a>Améliorations apportées au Sequencer

Les améliorations suivantes ont été apportées à l’éditeur de package dans le Sequencer App-V 5,1.

### Importer et exporter le fichier manifeste

Vous pouvez importer et exporter le fichier AppxManifest.xml. Pour exporter le fichier manifeste, sélectionnez l’onglet **avancé** , puis, dans la zone fichier manifeste, cliquez sur **Exporter...**. Vous pouvez modifier le fichier manifeste, tel que la suppression d’extensions d’interpréteur de fichiers ou la modification d’associations de type de fichier.

Après avoir apporté vos modifications, cliquez sur **Importer...** , puis sélectionnez le fichier que vous avez modifié. Après l’importation réussie, le fichier manifeste est mis à jour immédiatement dans l’éditeur de package.

**Vigilance**  
Lorsque vous importez le fichier, vos modifications sont validées par rapport au schéma XML. Si le fichier n’est pas valide, une erreur s’affiche. Sachez qu’il est possible d’importer un fichier qui est validé par rapport au schéma XML, mais qui peut toujours ne pas s’exécuter pour d’autres raisons.



### Liste des systèmes d’exploitation Windows 10

Dans l’onglet déploiement, les bits Windows 10 32 bits et Windows 10-64 qui ont été ajoutés à la liste des systèmes d’exploitation pour lesquels vous pouvez effectuer le Sequencer d’un package. Si vous sélectionnez **un système d’exploitation**, Windows 10 est automatiquement inclus parmi les systèmes d’exploitation pris en charge par le package séquencé.

### Le chemin actuel s’affiche en bas de l’éditeur du Registre virtuel

Dans l’onglet registre virtuel, le chemin d’accès s’affiche désormais en bas de l’éditeur du Registre virtuel, qui vous permet de déterminer la clé actuellement sélectionnée. Auparavant, vous deviez faire défiler l’arborescence du Registre pour trouver la clé actuellement sélectionnée.

### <a href="" id="combined--find-and-replace--dialog-box-and-shortcut-keys-added-in-virtual-registry-editor"></a>Combinaison de la boîte de dialogue Rechercher et remplacer» et des touches de raccourci ajoutées dans l’éditeur du Registre virtuel

Dans l’éditeur du Registre virtuel, des raccourcis clavier ont été ajoutés pour l’option Rechercher (Ctrl + F), et une boîte de dialogue qui combine les tâches «Rechercher» et «remplacer» a été ajoutée pour vous permettre de rechercher et de remplacer des valeurs et des données. Pour accéder à cette boîte de dialogue combinée, sélectionnez une touche et effectuez l’une des opérations suivantes:

-   Appuyez sur **Ctrl + H** .

-   Cliquez avec le bouton droit sur une touche et sélectionnez **remplacer**.

-   Sélectionnez **Afficher** le &gt; **Registre virtuel** &gt; **remplacer**.

Auparavant, la boîte de dialogue «remplacer» n’existait pas et vous deviez apporter les modifications manuellement.

### Renommer correctement les clés de Registre et les fichiers de package

Vous pouvez renommer les clés et fichiers du Registre virtuel sans problèmes de Sequencer. Auparavant, le Sequencer a cessé de fonctionner si vous essayez de renommer une clé.

### Importer et exporter des clés de Registre virtuelles

Vous pouvez importer et exporter des clés de Registre virtuelles. Pour importer une clé, cliquez avec le bouton droit sur le nœud sous lequel importer la clé, accédez à la clé que vous voulez importer, puis cliquez sur **Importer**. Pour exporter une clé, cliquez avec le bouton droit sur la clé et sélectionnez **Exporter**.

### Importer un annuaire dans le système de fichiers virtuel

Vous pouvez importer un répertoire dans le VFS. Pour importer un répertoire, cliquez sur l’onglet **fichiers de package** , puis cliquez sur **Afficher** le &gt; répertoire d’importation du système de **fichiers virtuel** &gt; **Import Directory**. Si vous essayez d’importer un répertoire contenant des fichiers déjà présents sur le VFS, l’importation échoue et un message explicatif s’affiche. Avant l’application-V 5,1, il est impossible d’importer des répertoires.

### Importez ou exportez un fichier VFS sans le supprimer, puis rajoutez-le dans le package.

Vous pouvez importer ou exporter des fichiers à partir du VFS sans supprimer le fichier, puis l’ajouter de nouveau au package. Par exemple, vous pouvez utiliser cette fonctionnalité pour exporter un journal de modification sur un disque local, modifier le fichier à l’aide d’un éditeur externe, puis importer à nouveau le fichier dans le VFS.

Pour exporter un fichier, sélectionnez l’onglet **fichiers du package** , cliquez avec le bouton droit sur le fichier dans le VFS, cliquez sur **Exporter**, puis choisissez un emplacement d’exportation à partir duquel vous pouvez effectuer les modifications.

Pour importer un fichier, sélectionnez l’onglet **fichiers du package** , puis cliquez avec le bouton droit sur le fichier que vous avez exporté. Recherchez le fichier que vous avez modifié, puis cliquez sur **Importer**. Le fichier importé remplacera le fichier existant.

Lorsque vous importez un fichier, vous devez **l’enregistrer en cliquant sur** &gt; **Enregistrer**.

### Le menu pour l’ajout d’un fichier de package a été déplacé

L’option de menu pour l’ajout d’un fichier de package a été déplacée. Pour accéder à l’option Ajouter, sélectionnez l’onglet **fichiers du package** , puis cliquez sur **Afficher** le &gt; **système de fichiers virtuel** &gt; **Ajouter un fichier**. Auparavant, cliquez avec le bouton droit sur un dossier sous le nœud VFS et sélectionnez **Ajouter un fichier**.

### Le nœud de Registre virtuel développe les ruches d’ordinateur et d’utilisateur par défaut

Lorsque vous ouvrez le registre virtuel, les ruches ordinateur et utilisateur sont affichées sous le nœud de registre de niveau supérieur. Auparavant, vous deviez développer le nœud REGISTRY pour afficher les ruches au-dessous.

### Activer ou désactiver les objets d’assistance du navigateur

Vous pouvez activer ou désactiver les objets d’assistance du navigateur en activant une nouvelle case à cocher, activer les objets d’assistance du navigateur, sous l’onglet avancé de l’interface utilisateur de Sequencer. Si les objets d’assistance du navigateur:

-   Existe dans le package et activés, la case à cocher est activée par défaut.

-   Existe dans le package et sont désactivés, la case à cocher est désactivée par défaut.

-   Existe dans le package, avec un ou plusieurs activés et un ou plusieurs désactivé, la case à cocher est définie sur indéterminé par défaut.

-   Qui n’existent pas dans le package, la case à cocher est désactivée.

### <a href="" id="bkmk-pkgconvimprove"></a>Améliorations apportées au convertisseur de package

Vous pouvez désormais utiliser le convertisseur de package pour convertir les packages App-V 4,6 qui contiennent des scripts, et les informations de Registre et les scripts des fichiers source. OSD sont désormais inclus dans la sortie du convertisseur de package.

Pour plus d’informations, y compris des exemples, voir [migration vers App-V 5,1 à partir d’une version précédente](migrating-to-app-v-51-from-a-previous-version.md).

### <a href="" id="bkmk-supmultscripts"></a>Prise en charge de plusieurs scripts sur un seul déclencheur d’événements

App-V 5,1 prend en charge l’utilisation de plusieurs scripts sur un seul déclencheur d’événements pour les packages App-V, notamment les packages que vous convertissez de App-V 4,6 à l’application-V 5,0 ou version ultérieure. Pour activer l’utilisation de plusieurs scripts, App-V 5,1 utilise une application de lancement de script, nommée ScriptRunner.exe, installée dans le cadre de l’installation du client App-V.

Pour plus d’informations, y compris une liste de déclencheurs d’événements et le contexte dans lequel les scripts peuvent être exécutés, voir la section scripts dans [à propos de la configuration dynamique App-V 5,1](about-app-v-51-dynamic-configuration.md).

### <a href="" id="bkmk-hardcodepath"></a>Le chemin d’accès codé au dossier d’installation est redirigé vers la racine du système de fichiers virtuel

Lorsque vous convertissez des packages de App-V 4,6 en 5,1, le package App-V 5,1 peut accéder au lecteur codé en dur que vous avez besoin d’utiliser lors de la création de packages 4,6. La lettre de lecteur sera le lecteur que vous avez sélectionné comme lecteur d’installation sur le système de séquençage 4,6. (La lettre du lecteur par défaut est Q:\\.)

Auparavant, le dossier racine 4,6 n’était pas reconnu et n’était pas accessible par les packages App-V 5,0. Les packages App-V 5,1 peuvent accéder aux fichiers en dur par le chemin d’accès complet ou peuvent énumérer par programme les fichiers sous la racine d’installation App-V 4,6.

**Détails techniques:** Le convertisseur d’application de package App-V 5,1 enregistre le dossier racine d’installation App-V 4,6 et les noms de dossiers courts dans le fichier FilesystemMetadata.xml de l’élément FileSystem. Lorsque le client App-V 5,1 crée le processus virtuel, il mappera les demandes de la racine d’installation de l’application-V 4,6 à la racine du système de fichiers virtuel.

## Obtention de technologies MDOP


App-V est un composant du pack d’optimisation du bureau Microsoft (MDOP). MDOP fait partie de Microsoft Software Assurance. Pour plus d’informations sur l’utilisation de Microsoft Software Assurance et sur l’acquisition de MDOP, voir [Comment obtenir MDOP](https://go.microsoft.com/fwlink/?LinkId=322049).






## Rubriques connexes


[Notes de publication pour App-V5.1](release-notes-for-app-v-51.md)









