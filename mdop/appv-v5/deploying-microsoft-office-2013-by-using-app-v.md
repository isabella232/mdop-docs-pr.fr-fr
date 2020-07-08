---
title: Déploiement de Microsoft Office2013 à l’aide d’App-V
description: Déploiement de Microsoft Office2013 à l’aide d’App-V
author: dansimp
ms.assetid: 02df5dc8-79e2-4c5c-8398-dbfb23344ab3
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 11/02/2016
ms.openlocfilehash: c57227d531c61949f9160c27fc249db72dbc6523
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10805874"
---
# Déploiement de Microsoft Office2013 à l’aide d’App-V


Les informations contenues dans cet article vous permettent d’utiliser Microsoft Application Virtualization 5,0 ou une version ultérieure, de mettre Microsoft Office 2013 en tant qu’application virtualisée sur les ordinateurs de votre organisation. Pour plus d’informations sur l’utilisation de App-V pour générer Office 2010, voir [déploiement de Microsoft Office 2010 à l’aide d’App-v](deploying-microsoft-office-2010-by-using-app-v.md). Pour réussir le déploiement d’Office 2013 avec App-V, vous devez être familiarisé avec les applications Office 2013 et pp-V.

Cette rubrique contient les sections suivantes:

-   [Ce que vous devez savoir avant de commencer](#bkmk-before-you-start)

-   [Création d’un package 2013 Office pour App-V avec l’outil déploiement d’Office](#bkmk-create-office-pkg)

-   [Publication du package Office pour App-V 5,0](#bkmk-pub-pkg-office)

-   [Personnalisation et gestion des packages d’application Office V](#bkmk-custmz-manage-office-pkgs)

## <a href="" id="bkmk-before-you-start"></a>Ce que vous devez savoir avant de commencer


Avant de déployer Office 2013 à l’aide de App-V, passez en revue les informations de planification suivantes.

### <a href="" id="bkmk-supp-vers-coexist"></a>Versions d’Office et coexistence Office prises en charge

Utilisez le tableau ci-dessous pour obtenir des informations sur les versions d’Office prises en charge et sur l’exécution des versions coexistantes d’Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Informations à réviser</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-office-vers-supp-appv)">Planification de l'utilisation d'App-V avec Office</a></p></td>
<td align="left"><ul>
<li><p>Versions d’Office prises en charge</p></li>
<li><p>Types de déploiement pris en charge (par exemple, un ordinateur de bureau, une infrastructure de bureau virtuel ou un pool d’infrastructure VDI)</p></li>
<li><p>Options de gestion des licences Office</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p><a href="planning-for-using-app-v-with-office.md#bkmk-plan-coexisting" data-raw-source="[Planning for Using App-V with Office](planning-for-using-app-v-with-office.md#bkmk-plan-coexisting)">Planification de l'utilisation d'App-V avec Office</a></p></td>
<td align="left"><p>Remarques relatives à l’installation de différentes versions d’Office sur le même ordinateur</p></td>
</tr>
</tbody>
</table>



### <a href="" id="bkmk-pkg-pub-reqs"></a>Exigences en matière de création de packages, de publication et de déploiement

Avant de déployer Office à l’aide de App-V, consultez la configuration requise suivante.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Condition requise</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Packages</p></td>
<td align="left"><ul>
<li><p>Toutes les applications Office que vous voulez déployer pour les utilisateurs doivent se trouver dans un seul package.</p></li>
<li><p>Dans App-V 5,0 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer des packages. Vous ne pouvez pas utiliser le Sequencer.</p></li>
<li><p>Si vous déployez Microsoft Visio 2013 et Microsoft Project 2013 avec Office, vous devez les inclure dans le même package qu’Office. Pour plus d’informations, reportez-vous à <a href="#bkmk-deploy-visio-project" data-raw-source="[Deploying Visio 2013 and Project 2013 with Office](#bkmk-deploy-visio-project)"> déploiement de Visio 2013 et Project 2013 avec Office </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Publishing</p></td>
<td align="left"><ul>
<li><p>Vous ne pouvez publier qu’un seul package Office sur chaque ordinateur client.</p></li>
<li><p>Vous devez publier le package Office globalement. Vous ne pouvez pas publier l’utilisateur.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td align="left"><p>Déploiement de l’un des produits suivants sur un ordinateur partagé, par exemple, à l’aide des services Bureau à distance:</p>
<ul>
<li><p>Applications 365 Microsoft pour les entreprises</p></li>
<li><p>Visio Pro pour Office 365</p></li>
<li><p>Project Pro pour Office 365</p></li>
</ul></td>
<td align="left"><p>Vous devez activer <a href="https://technet.microsoft.com/library/dn782860.aspx" data-raw-source="[shared computer activation](https://technet.microsoft.com/library/dn782860.aspx)"> l’activation d’ordinateurs partagés </a> .</p>
<p>Vous n’utilisez pas l’activation d’ordinateurs partagés si vous déployez un produit sous licence en volume, par exemple:</p>
<ul>
<li><p>Office professionnel plus 2013</p></li>
<li><p>Visio professionnel 2013</p></li>
<li><p>Project Professionnel 2013</p></li>
</ul></td>
</tr>
</tbody>
</table>



### Exclusion d’applications Office d’un package

Le tableau suivant décrit les méthodes recommandées pour exclure des applications Office spécifiques d’un package.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Utilisez le <strong> </strong> paramètre ExcludeApp lorsque vous créez le package à l’aide de l’outil déploiement d’Office.</p></td>
<td align="left"><ul>
<li><p>Vous permet d’exclure des applications Office spécifiques du package lorsque l’outil déploiement d’Office crée le package. Par exemple, vous pouvez utiliser ce paramètre pour créer un package qui contient uniquement Microsoft Word.</p></li>
<li><p>Pour plus d’informations, consultez <a href="https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement" data-raw-source="[ExcludeApp element](https://technet.microsoft.com/library/jj219426.aspx#bkmk-excludeappelement)"> ExcludeApp élément </a> .</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Modifier le fichier DeploymentConfig.xml</p></td>
<td align="left"><ul>
<li><p>Modifiez le fichier DeploymentConfig.xml après la création du package. Ce fichier contient les paramètres de package par défaut pour tous les utilisateurs sur un ordinateur exécutant le client App-V.</p></li>
<li><p>Pour plus d’informations, reportez-vous à <a href="#bkmk-disable-office-apps" data-raw-source="[Disabling Office 2013 applications](#bkmk-disable-office-apps)"> désactivation des applications Office 2013 </a> .</p></li>
</ul></td>
</tr>
</tbody>
</table>



## <a href="" id="bkmk-create-office-pkg"></a>Création d’un package 2013 Office pour App-V avec l’outil déploiement d’Office


Suivez les étapes ci-dessous pour créer un package 2013 Office pour App-V 5,0 ou version ultérieure.

**Important**  
Dans App-V 5,0 et les versions ultérieures, vous devez utiliser l’outil déploiement d’Office pour créer un package. Vous ne pouvez pas utiliser le Sequencer pour créer des packages.


### Consulter les conditions préalables à l’utilisation de l’outil déploiement d’Office

Sur l’ordinateur sur lequel vous installez l’outil déploiement d’Office, vous devez disposer des éléments suivants:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Prérequises</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Logiciels requis</p></td>
<td align="left"><p>.NET Framework 4</p></td>
</tr>
<tr class="even">
<td align="left"><p>Systèmes d’exploitation pris en charge</p></td>
<td align="left"><ul>
<li><p>version 64 bits de Windows 8</p></li>
<li><p>version 64 bits de Windows 7</p></li>
</ul></td>
</tr>
</tbody>
</table>


**Remarque**  
Dans cette rubrique, le terme «Office 2013 App-V package» fait référence à la gestion des licences d’abonnement et au programme de licence en volume.


### Créer des packages App-V d’Office 2013 à l’aide de l’outil déploiement d’Office

Vous pouvez créer des packages App-V d’Office 2013 à l’aide de l’outil déploiement d’Office. Les instructions suivantes vous expliquent comment créer un package App-V pour Office 2013 avec les licences en volume ou les licences d’abonnement.

Créer des packages App-V Office 2013 sur des ordinateurs Windows 64 bits. Une fois créé, le package App-V pour Office 2013 s’exécute 32 sur les ordinateurs Windows 7 et 64 bits et.

### Télécharger l’outil déploiement d’Office

Les packages App-V d’Office 2013 sont créés à l’aide de l’outil déploiement d’Office qui génère un package App-V pour Office 2013. Le package ne peut pas être créé ou modifié via le Sequencer App-V. Pour commencer à créer un package:

1.  Télécharger l' [outil déploiement d’Office pour Office «démarrer en un clic](https://www.microsoft.com/download/details.aspx?id=36778)».

2.  Exécutez le fichier. exe et extrayez ses fonctionnalités dans l’emplacement souhaité. Pour faciliter ce processus, vous pouvez créer un dossier réseau partagé dans lequel les fonctionnalités seront enregistrées.

    Par exemple: \\\\Server\\Office2013

3.  Vérifiez qu’il existe une setup.exe et qu’un fichier configuration.xml se trouvent à l’emplacement que vous avez spécifié.

### Télécharger les applications Office 2013

Après avoir téléchargé l’outil déploiement d’Office, vous pouvez l’utiliser pour obtenir les dernières applications Office 2013. Après avoir effectué les applications Office, vous créez le package App-V pour Office 2013.

Le fichier XML inclus dans l’outil déploiement d’Office spécifie les détails du produit, tels que les langues et les applications Office inclus.

1. **Personnalisez le fichier de configuration XML d’exemple:** Utilisez l’exemple de fichier de configuration XML que vous avez téléchargé auprès de l’outil déploiement d’Office pour personnaliser les applications Office:

   1. Ouvrez l’exemple de fichier XML dans le bloc-notes ou dans votre éditeur de texte.

   2. L’exemple configuration.xml ouverture et la possibilité de le modifier, vous pouvez spécifier des produits, des langues et le chemin d’accès au dossier dans lequel vous enregistrez les applications Office 2013. Voici un exemple de base du fichier configuration.xml:

      ```xml
      <Configuration>
         <Add SourcePath= ”\\Server\Office2013” OfficeClientEdition="32" >
          <Product ID="O365ProPlusRetail ">
            <Language ID="en-us" />
          </Product>
          <Product ID="VisioProRetail">
            <Language ID="en-us" />
          </Product>
        </Add>
      </Configuration>
      ```

      **Remarque**  
      Le fichier XML de configuration est un exemple de fichier XML. Le fichier inclut des lignes commentées. Vous pouvez «ne pas commenter» ces lignes pour personnaliser des paramètres supplémentaires à l’aide du fichier.

      Le fichier de configuration XML ci-dessus spécifie qu’Office 2013 ProPlus 32-bit Edition, y compris Visio ProPlus, sera téléchargé en anglais vers le \\\\server\\Office 2013, qui est l’emplacement où les applications Office seront enregistrées. Notez que l’ID de produit des applications n’aura aucune incidence sur la licence finale d’Office. Les packages App-V pour Office 2013 avec différentes licences peuvent être créés à partir des mêmes applications par le biais du mode de gestion de licences à un stade ultérieur. Le tableau ci-dessous résume les attributs et éléments personnalisés du fichier XML:

      <table>
      <colgroup>
      <col width="33%" />
      <col width="33%" />
      <col width="33%" />
      </colgroup>
      <thead>
      <tr class="header">
      <th align="left">Entrée</th>
      <th align="left">Description</th>
      <th align="left">Exemple</th>
      </tr>
      </thead>
      <tbody>
      <tr class="odd">
      <td align="left"><p>Ajouter un élément</p></td>
      <td align="left"><p>Spécifie les produits et les langues à inclure dans le package.</p></td>
      <td align="left"><p>N/A</p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>OfficeClientEdition (attribut de l’élément Add)</p></td>
      <td align="left"><p>Spécifie l’édition d’un produit Office 2013 à utiliser: 32-bit ou 64 bits. L’opération échoue si <strong> OfficeClientEdition </strong> n’est pas défini sur une valeur valide.</p></td>
      <td align="left"><p><strong>OfficeClientEdition </strong> = &quot; 32&quot;</p>
      <p><strong>OfficeClientEdition </strong> = &quot; 64&quot;</p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Élément Product</p></td>
      <td align="left"><p>Spécifie l’application. Les applications Project 2013 et Visio 2013 doivent être spécifiées ici en tant que produit supplémentaire à inclure dans les applications.</p></td>
      <td align="left"><p><code>Product ID =&quot;O365ProPlusRetail &quot;</code></p>
      <p><code>Product ID =&quot;VisioProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProjectProRetail&quot;</code></p>
      <p><code>Product ID =&quot;ProPlusVolume&quot;</code></p>
      <p><code>Product ID =&quot;VisioProVolume&quot;</code></p>
      <p><code>Product ID = &quot;ProjectProVolume&quot;</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>Élément Language</p></td>
      <td align="left"><p>Spécifie la langue prise en charge dans les applications</p></td>
      <td align="left"><p><code>Language ID=&quot;en-us&quot;</code></p></td>
      </tr>
      <tr class="odd">
      <td align="left"><p>Version (attribut de l’élément Add)</p></td>
      <td align="left"><p>Facultatif. Spécifie une build à utiliser pour le package.</p>
      <p>Utilise par défaut la version publiée la plus récente (telle qu’elle est définie dans v32.CAB au niveau de la source d’Office).</p></td>
      <td align="left"><p><code>15.1.2.3</code></p></td>
      </tr>
      <tr class="even">
      <td align="left"><p>SourcePath (attribut de l’élément Add)</p></td>
      <td align="left"><p>Spécifie l’emplacement dans lequel les applications seront enregistrées.</p></td>
      <td align="left"><p><code>Sourcepath = &quot;\Server\Office2013”</code></p></td>
      </tr>
      </tbody>
      </table>

      Après avoir modifié le fichier configuration.xml pour spécifier le produit, les langues et également l’emplacement dans lequel enregistrer les applications 2013 Office, vous pouvez enregistrer le fichier de configuration, par exemple, en tant que Customconfig.xml.

2. **Téléchargez les applications à l’emplacement spécifié:** Utilisez une invite de commandes avec élévation de privilèges et un système d’exploitation 64 bits pour télécharger les applications Office 2013 qui seront converties ultérieurement en package App-V. Vous trouverez ci-dessous un exemple de commande avec une description des détails:

   ``` syntax
   \\server\Office2013\setup.exe /download \\server\Office2013\Customconfig.xml
   ```

   Dans l’exemple suivant:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2013</strong></p></td>
   <td align="left"><p>est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>est l’outil déploiement d’Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/Download</strong></p></td>
   <td align="left"><p>télécharge les applications Office 2013 que vous spécifiez dans le fichier customConfig.xml. Ces bits peuvent être convertis ultérieurement dans un package App-V pour Office 2013 avec le programme de licence en volume.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2013\Customconfig.xml</strong></p></td>
   <td align="left"><p>transmet le fichier de configuration XML requis pour terminer le processus de téléchargement (dans cet exemple, customconfig.xml. Après l’utilisation de la commande Télécharger, les applications Office se trouvent dans l’emplacement spécifié dans le fichier XML de configuration (dans cet exemple, \Server\Office2013.).</p></td>
   </tr>
   </tbody>
   </table>



### Convertir les applications Office en package App-V

Après avoir téléchargé les applications Office 2013 par le biais de l’outil déploiement d’Office, utilisez l’outil déploiement d’Office pour les convertir en package d’application Office 2013. Suivez les étapes qui correspondent à votre modèle de gestion des licences.

**Résumé de ce que vous devez faire:**

-   Créez les packages App-V d’Office 2013 sur les ordinateurs Windows 64 bits. Toutefois, le package s’exécute 32 sur les ordinateurs Windows 7 et 64 bits de Windows 7 et de Windows 8.

-   Pour créer un package App-V pour la gestion des licences d’abonnement ou le programme de licence en volume à l’aide de l’outil déploiement d’Office, vous devez modifier le fichier de configuration CustomConfig.xml.

    Le tableau suivant récapitule les valeurs que vous devez entrer dans le fichier CustomConfig.xml pour le modèle de gestion des licences que vous utilisez. Les étapes des sections qui suivent le tableau spécifient les entrées exactes que vous devez effectuer.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">ID produit</th>
<th align="left">Gestion des licences en volume</th>
<th align="left">Licences d’abonnement</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Office 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p></td>
<td align="left"><p>O365proplusretail)</p></td>
</tr>
<tr class="even">
<td align="left"><p><strong>Office 2013 avec Visio 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p>
<p>VisioProVolume</p></td>
<td align="left"><p>O365proplusretail)</p>
<p>VisioProRetail</p></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Office 2013 avec Visio 2013 et Project 2013</strong></p></td>
<td align="left"><p>ProPlusVolume</p>
<p>VisioProVolume</p>
<p>ProjectProVolume</p></td>
<td align="left"><p>O365proplusretail)</p>
<p>VisioProRetail</p>
<p>ProjectProRetail</p></td>
</tr>
</tbody>
</table>



**Convertir les applications Office en package App-V**

1. Dans le bloc-notes, rouvrez le fichier CustomConfig.xml, puis apportez les modifications suivantes au fichier:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Paramètre</th>
   <th align="left">Ce à quoi changer la valeur</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>Chemin_source</p></td>
   <td align="left"><p>Pointez sur les applications Office téléchargées auparavant.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ProductID</p></td>
   <td align="left"><p>Spécifiez le type de licence, comme indiqué dans les exemples suivants:</p>
   <ul>
   <li><p>Licences d’abonnement</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\server\Office 2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;O365ProPlusRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProRetail&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt; </code></pre>
   <p>Dans cet exemple, les modifications suivantes ont été apportées à la création d’un package avec les licences d’abonnement:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Chemin_source</strong></p></td>
   <td align="left"><p>est le chemin d’accès, qui a été modifié de sorte qu’il pointe vers les applications Office téléchargées auparavant.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>ID produit</strong></p></td>
   <td align="left"><p>pour Office a changé en <code>O365ProPlusRetail</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>ID produit</strong></p></td>
   <td align="left"><p>pour Visio a changé en <code>VisioProRetail</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   <li><p>Gestion des licences en volume</p>
   <pre class="syntax" space="preserve"><code>&lt;Configuration&gt;
      &lt;Add SourcePath= &quot;\Server\Office2013&quot; OfficeClientEdition=&quot;32&quot; &gt;
       &lt;Product ID=&quot;ProPlusVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
       &lt;Product ID=&quot;VisioProVolume&quot;&gt;
         &lt;Language ID=&quot;en-us&quot; /&gt;
       &lt;/Product&gt;
     &lt;/Add&gt;
   &lt;/Configuration&gt;</code></pre>
   <p>Dans cet exemple, les modifications suivantes ont été apportées à la création d’un package avec le programme de licence en volume:</p>
   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Chemin_source</strong></p></td>
   <td align="left"><p>est le chemin d’accès, qui a été modifié de sorte qu’il pointe vers les applications Office téléchargées auparavant.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>ID produit</strong></p></td>
   <td align="left"><p>pour Office a changé en <code>ProPlusVolume</code> .</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>ID produit</strong></p></td>
   <td align="left"><p>pour Visio a changé en <code>VisioProVolume</code> .</p></td>
   </tr>
   </tbody>
   </table>
   <p> </p>
   <p></p></li>
   </ul></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ExcludeApp (facultatif)</p></td>
   <td align="left"><p>Vous permet de spécifier les programmes Office que vous ne souhaitez pas inclure dans le package App-V créé par l’outil déploiement d’Office. Par exemple, vous pouvez exclure Access et InfoPath.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>PACKAGEGUID (facultatif)</p></td>
   <td align="left"><p>Par défaut, tous les packages App-V créés par l’outil déploiement d’Office partagent le même ID de package App-V. Vous pouvez utiliser PACKAGEGUID pour spécifier un ID de package différent pour chaque package, qui vous permet de publier plusieurs packages App-V, créés par l’outil déploiement d’Office, et de les gérer à l’aide du serveur App-V.</p>
   <p>Un exemple d’utilisation de ce paramètre est le cas si vous créez des packages différents pour différents utilisateurs. Par exemple, vous pouvez créer un package uniquement avec Office 2013 pour certains utilisateurs et créer un autre package avec Office 2013 et Visio 2013 pour un autre groupe d’utilisateurs.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Même si vous utilisez des ID de package uniques, vous pouvez toujours déployer un seul package d’application-V sur un seul appareil.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Utilisez la commande/Packager pour convertir les applications Office en un package App-V pour Office 2013.

   Exemple:

   ``` syntax
   \\server\Office2013\setup.exe /packager \\server\Office2013\Customconfig.xml  \\server\share\Office2013AppV
   ```

   Dans l’exemple suivant:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>\server\Office2013</strong></p></td>
   <td align="left"><p>est l’emplacement de partage réseau qui contient l’outil déploiement d’Office et le fichier Configuration.xml personnalisé Customconfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>Setup.exe</strong></p></td>
   <td align="left"><p>est l’outil déploiement d’Office.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>/packager</strong></p></td>
   <td align="left"><p>crée le package App-V pour Office 2013 avec la licence en volume spécifiée dans le fichier customConfig.xml.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>\server\Office2013\Customconfig.xml</strong></p></td>
   <td align="left"><p>transmet le fichier XML de configuration (dans ce cas, customConfig) qui a été préparé pour la phase d’emballage.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>\server\share\Office 2013AppV</strong></p></td>
   <td align="left"><p>Spécifie l’emplacement du package Office App-V nouvellement créé.</p></td>
   </tr>
   </tbody>
   </table>



~~~
After you run the **/packager** command, the following folders appear up in the directory where you specified the package should be saved:

-   **App-V Packages** – contains an Office 2013 App-V package and two deployment configuration files.

-   **WorkingDir**

**Note**  
To troubleshoot any issues, see the log files in the %temp% directory (default).
~~~



3. Vérifiez que le package App-V pour Office 2013 fonctionne correctement:

   1.  Publiez le package App-V pour Office 2013 que vous avez créé dans le monde entier, sur un ordinateur de test et vérifiez que les raccourcis vers Office 2013 apparaissent.

   2.  Démarrez quelques applications Office 2013, telles qu’Excel ou Word, pour vous assurer que votre package fonctionne correctement.

## <a href="" id="bkmk-pub-pkg-office"></a>Publication du package Office pour App-V 5,0


Utilisez les informations suivantes pour publier un package Office.

### Méthodes de publication des packages App-V d’Office

Déployez le package App-V pour Office 2013 à l’aide des méthodes que vous utilisez pour les autres packages:

-   SystemCenterConfigurationManager

-   App-V Server

-   Commandes PowerShell autonomes

### Conditions préalables et configuration requise pour la publication

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Conditions préalables ou requises</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Activer les scripts PowerShell sur les clients App-V</p></td>
<td align="left"><p>Pour publier des packages Office 2013, vous devez exécuter un script.</p>
<p>Par défaut, les scripts de package sont désactivés sur les clients App-V. Pour activer les scripts, exécutez la commande PowerShell suivante:</p>
<pre class="syntax" space="preserve"><code>Set-AppvClientConfiguration –EnablePackageScripts 1</code></pre></td>
</tr>
<tr class="even">
<td align="left"><p>Publier le package 2013 Office globalement</p></td>
<td align="left"><p>Les points d’extension dans le package d’application Office V doivent être installés au niveau de l’ordinateur.</p>
<p>Lorsque vous publiez au niveau de l’ordinateur, aucune action ou redistribuable ne doit être requis, et le package 2013 Office autorise globalement ses applications à fonctionner comme Office en natif, ce qui évite aux administrateurs de personnaliser les packages.</p></td>
</tr>
</tbody>
</table>



### Publication d’un package Office

Exécutez la commande suivante pour publier un package Office globalement:

-   `Add-AppvClientPackage <Path_to_AppV_Package> | Publish-AppvClientPackage –global`

-   À partir de la console de gestion Web sur le serveur App-V, vous pouvez ajouter des autorisations à un groupe d’ordinateurs plutôt qu’à un groupe d’utilisateurs pour permettre la publication globale des packages dans le groupe correspondant.

## <a href="" id="bkmk-custmz-manage-office-pkgs"></a>Personnalisation et gestion des packages d’application Office V


Pour gérer vos packages d’application Office V, utilisez les mêmes opérations que pour tous les autres packages, mais il existe quelques exceptions, comme indiqué dans les sections suivantes.

-   [Activation de plug-ins Office à l’aide de groupes de connexion](#bkmk-enable-office-plugins)

-   [Désactivation des applications Office 2013](#bkmk-disable-office-apps)

-   [Désactivation des raccourcis d’Office 2013](#bkmk-disable-shortcuts)

-   [Gestion des mises à jour de package Office 2013](#bkmk-manage-office-pkg-upgrd)

-   [Gestion des mises à niveau de la gestion des licences Office 2013](#bkmk-manage-office-lic-upgrd)

-   [Déploiement de Visio 2013 et de Project 2013 avec Office](#bkmk-deploy-visio-project)

### <a href="" id="bkmk-enable-office-plugins"></a>Activation de plug-ins Office à l’aide de groupes de connexion

Suivez les étapes décrites dans cette section pour activer les plug-ins Office avec votre package Office. Pour utiliser les plug-ins Office, vous devez utiliser le Sequencer App-V pour créer un package distinct contenant uniquement les plug-ins. Vous ne pouvez pas utiliser l’outil déploiement d’Office pour créer le package de plug-ins. Ensuite, créez un groupe de connexion contenant le package Office et le package enfichable, comme décrit dans les étapes suivantes.

**Pour activer les plug-ins pour les packages App-V pour Office**

1.  Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.

2.  Séquencez vos plug-ins en utilisant le Sequencer App-V 5,0. Assurez-vous qu’Office 2013 est installé sur l’ordinateur utilisé pour la séquence du plug-in. Nous vous recommandons d’utiliser les applications Microsoft 365 pour les entreprises (non virtuelles) sur l’ordinateur de séquençage lors de la séquence des plug-ins Office 2013.

3.  Créer un package App-V 5,0 qui inclut les plug-ins souhaités.

4.  Ajoutez un groupe de connexions via App-V Server, System Center Configuration Manager ou une cmdlet PowerShell.

5.  Ajoutez le package App-V d’Office 2013 et le package de plug-ins que vous avez séquencé au groupe de connexions que vous avez créé.

    **Important**  
    L’ordre des packages dans le groupe de connexions détermine l’ordre dans lequel le contenu du package est fusionné. Dans votre fichier de descripteur de groupe de connexion, ajoutez d’abord le package App-V pour Office 2013, puis ajoutez le package App-in App-V.



6.  Assurez-vous que les deux packages sont publiés sur l’ordinateur cible et que le package du plug-in est publié globalement pour correspondre aux paramètres globaux du package Office 2013 App-V publié.

7.  Vérifiez que le fichier de configuration de déploiement du package du plug-in a les mêmes paramètres que le package App-V pour Office 2013.

    Dans la mesure où le package App-V d’Office 2013 est intégré au système d’exploitation, les paramètres de package du plug-in doivent correspondre. Vous pouvez effectuer une recherche dans le fichier de configuration de déploiement pour «mode COM» et vous assurer que la valeur de votre package de plug-ins est «intégrée» et que les «InProcessEnabled» et «OutOfProcessEnabled» correspondent aux paramètres du package application Office 2013 V publié.

8.  Ouvrez le fichier de configuration de déploiement et attribuez la valeur **false**aux **objets activés** .

9.  Si vous avez apporté des modifications au fichier de configuration de déploiement après le séquençage, assurez-vous que le package du plug-in est publié avec le fichier.

10. Vérifiez que le groupe de connexion que vous avez créé est activé sur l’ordinateur de votre choix. Le groupe de connexion créé est probablement «en attente» si le package App-V d’Office 2013 est en cours d’utilisation lorsque le groupe de connexion est activé. Si tel est le cas, vous devez redémarrer pour pouvoir activer le groupe de connexion.

11. Une fois que vous avez correctement publié les deux packages et activé le groupe de connexion, démarrez l’application Office 2013 cible et vérifiez que le plug-in que vous avez publié et ajouté au groupe de connexions fonctionne comme prévu.

### <a href="" id="bkmk-disable-office-apps"></a>Désactivation des applications Office 2013

Il est possible que vous souhaitiez désactiver des applications spécifiques dans votre package d’application Office V. Par exemple, vous pouvez désactiver l’accès sans avoir accès au principal de l’application Office. Lorsque vous désactivez une application, l’utilisateur final ne verra plus le raccourci de l’application. Vous n’avez pas besoin de relancer l’application. Lorsque vous modifiez le fichier de configuration de déploiement une fois que le package App-V pour Office 2013 a été publié, vous enverrez les modifications, vous ajoutez le package App-V d’Office 2013, puis vous le republiez avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2013 App-V.

**Remarque**  
Pour exclure des applications Office spécifiques (par exemple, Access et InfoPath) lors de la création du package App-V avec l’outil déploiement d’Office, utilisez le paramètre **ExcludeApp** . Pour plus d’informations, voir informations [de référence sur le fichier démarrer en un clic configuration.xml](https://technet.microsoft.com/library/jj219426.aspx).



**Pour désactiver une application Office 2013**

1.  Ouvrez un fichier de configuration de déploiement avec un éditeur de texte tel que **le bloc-notes** et recherchez «applications».

2.  Recherchez l’application Office que vous voulez désactiver, par exemple, Access 2013.

3.  Remplacez la valeur «Enabled» par «true» par «false».

4.  Enregistrez le fichier de configuration de déploiement.

5.  Ajoutez le package App-V pour Office 2013 avec le nouveau fichier de configuration de déploiement.

    ```xml
    <Application Id="[{AppVPackageRoot)]\officefl5\INFOPATH.EXE" Enabled="true">
      <VisualElements>
        <Name>InfoPath Filler 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[{AppVPackageRoot}]\office15\lync.exe" Enabled="true">
      <VisualElements>
        <Name>Lync 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    <Application Id="[(AppVPackageRoot}]\office15\MSACCESS.EXE" Enabled="true">
      <VisualElements>
        <Name>Access 2013</Name>
        <Icon />
        <Description />
      </VisualElements>
    </Application>
    ```

6.  Ajoutez à nouveau le package App-V pour Office 2013, puis republiez-le avec le nouveau fichier de configuration de déploiement pour appliquer les nouveaux paramètres aux applications Office 2013 App-V.

### <a href="" id="bkmk-disable-shortcuts"></a>Désactivation des raccourcis d’Office 2013

Vous pouvez désactiver les raccourcis pour certaines applications Office au lieu d’annuler la publication ou de la suppression du package. L’exemple suivant explique comment désactiver les raccourcis clavier pour Microsoft Access.

**Pour désactiver les raccourcis pour les applications Office 2013**

1.  Ouvrez un fichier de configuration de déploiement dans le bloc-notes et recherchez «raccourcis».

2.  Pour désactiver certains raccourcis, vous pouvez supprimer ou commenter les raccourcis spécifiques que vous ne voulez pas utiliser. Vous devez laisser le sous-système présenter et activé. Par exemple, dans l’exemple ci-dessous, supprimez les raccourcis de Microsoft Access, tout en conservant le raccourci vers le sous-système &lt; &gt; &lt; /Shortcut &gt; intact pour désactiver le raccourci Microsoft Access.

    ``` syntax
    Shortcuts

    -->
     <Shortcuts Enabled="true">
      <Extensions>
        <Extension Category="AppV.Shortcut">
          <Shortcut>
           <File>[{Common Programs}]\Microsoft Office 2013\Access 2013.lnk</File>
           <Target>[{AppvPackageRoot}])office15\MSACCESS.EXE</Target>
           <Icon>[{Windows}]\Installer\{90150000-000F-0000-0000-000000FF1CE)\accicons.exe.Ø.ico</Icon>
           <Arguments />
           <WorkingDirectory />
           <AppuserModelId>Microsoft.Office.MSACCESS.EXE.15</AppUserModelId>
           <AppUserModelExcludeFromShowInNewInstall>true</AppUserModelExcludeFromShowInNewInstall>
           <Description>Build a professional app quickly to manage data.</Description>
           <ShowCommand>l</ShowCommand>
           <ApplicationId>[{AppVPackageRoot}]\office15\MSACCESS.EXE</ApplicationId>
        </Shortcut>
    ```

3.  Enregistrez le fichier de configuration de déploiement.

4.  Republiez le package App-V d’Office 2013 avec un nouveau fichier de configuration de déploiement.

Il est possible de modifier de nombreux paramètres supplémentaires par le biais de la modification de la configuration de déploiement pour les packages App-V (par exemple, associations de types de fichiers, système de fichiers virtuel, etc.). Pour plus d’informations sur l’utilisation des fichiers de configuration de déploiement pour modifier les paramètres de package App-V, reportez-vous à la section ressources supplémentaires à la fin de ce document.

### <a href="" id="bkmk-manage-office-pkg-upgrd"></a>Gestion des mises à jour de package Office 2013

Pour mettre à niveau un package 2013 Office, utilisez l’outil déploiement d’Office. Pour effectuer la mise à niveau d’un package 2013 Office, procédez comme suit.

**Comment mettre à niveau un package Office 2013 déjà déployé**

1.  Créer un nouveau package Office 2013 par le biais de l’outil déploiement d’Office qui utilise le logiciel d’application Office 2013 le plus récent. Les derniers bits d’Office 2013 peuvent toujours être obtenus par le biais de la phase de téléchargement de la création d’un package App-V pour Office 2013. Le package 2013 Office qui vient d’être créé dispose des dernières mises à jour et un nouvel ID de version. Tous les packages créés à l’aide de l’outil déploiement d’Office ont la même ligne.

    **Remarque**  
    Les packages d’application Office V possèdent deux ID de version:

    -   ID de version d’un package App-V Office 2013 unique pour tous les packages créés à l’aide de l’outil déploiement d’Office.

    -   Un deuxième ID de version de package App-V, x. x. x. x par exemple, dans le manifeste AppX qui changera uniquement s’il existe une nouvelle version d’Office. Par exemple, si une nouvelle version d’Office 2013 avec des mises à niveau est disponible et qu’un package est créé par le biais de l’outil déploiement d’Office pour incorporer ces mises à jour, l’ID de version X. X. X. X sera modifié de manière à refléter la modification de la version d’Office. Le serveur App-V utilisera l’ID de version X. X. X. X pour différencier ce package et détecter qu’il contient de nouvelles mises à niveau du package déjà publié et, par conséquent, le publier dans le cadre d’une mise à niveau vers le package Office 2013 existant.



2.  Publiez globalement les packages d’application Office 2013 nouvellement créés sur les ordinateurs sur lesquels vous souhaitez appliquer les nouvelles mises à jour. Dans la mesure où le nouveau package utilise la même ligne de l’ancien package de l’application Office 2013-V, la publication du nouveau package avec les mises à jour apportera uniquement les nouvelles modifications apportées à l’ancien package et sera donc rapide.

3.  Les mises à niveau seront appliquées de la même manière que les packages App-V globalement publiés. Étant donné que les applications seront probablement utilisées, les mises à niveau peuvent être retardées jusqu’au redémarrage de l’ordinateur.

### <a href="" id="bkmk-manage-office-lic-upgrd"></a>Gestion des mises à niveau de la gestion des licences Office 2013

Si un nouveau package App-V d’Office 2013 a une licence différente de celle du package App-V pour Office 2013 actuellement déployé. Par exemple, le package 2013 Office déployé est un abonnement Office 2013 et le nouveau package Office 2013 est basé sur les licences en volume, les instructions suivantes doivent être suivies pour garantir la mise à niveau de la gestion des licences:

**Comment mettre à niveau une licence Office 2013**

1.  Annulez la publication du package App-V du programme de licence d’abonnement Office 2013 déjà déployé.

2.  Supprimez le package App-V de l’abonnement Office 2013 non publié.

3.  Redémarrez l’ordinateur.

4.  Ajoutez la nouvelle version de licence en volume d’Office 2013 App-V.

5.  Publiez l’application Office 2013 App-V ajoutée avec le programme de licence en volume.

Un package App-V pour Office 2013 avec les licences que vous avez choisies sera déployé avec succès.

### <a href="" id="bkmk-deploy-visio-project"></a>Déploiement de Visio 2013 et de Project 2013 avec Office

Le tableau suivant décrit les exigences et les options de déploiement de Visio 2013 et de Project 2013 avec Office.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Tâche</th>
<th align="left">Détails</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Comment puis-je empaqueter et publier Visio 2013 et Project 2013 avec Office?</p></td>
<td align="left"><p>Vous devez inclure Visio 2013 et Project 2013 dans le même package qu’Office.</p>
<p>Si vous ne déployez pas Office, vous pouvez créer un package contenant Visio et/ou Project, tant que vous suivez <a href="../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md" data-raw-source="[Deploying Microsoft Office 2010 by Using App-V](../appv-v5/deploying-microsoft-office-2010-by-using-app-v.md)"> le déploiement de Microsoft Office 2010 à l’aide de App-V </a> .</p></td>
</tr>
<tr class="even">
<td align="left"><p>Comment puis-je déployer Visio 2013 et Project 2013 vers des utilisateurs spécifiques?</p></td>
<td align="left"><p>Appliquez l’une des méthodes suivantes:</p>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Si vous souhaitez...</th>
<th align="left">... Utilisez ensuite cette méthode</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>Création de deux packages différents et déploiement de chacun d’eux dans un groupe d’utilisateurs différent</p></td>
<td align="left"><p>Créez et déployez les packages suivants:</p>
<ul>
<li><p>Package qui contient uniquement Office-déploiement sur des ordinateurs pour lesquels les utilisateurs ont besoin uniquement d’Office.</p></li>
<li><p>Un package qui contient Office, Visio et Project-déployer sur des ordinateurs pour lesquels les utilisateurs ont besoin des trois applications.</p></li>
</ul></td>
</tr>
<tr class="even">
<td align="left"><p>Si vous n’avez besoin que d’un seul package pour l’ensemble de votre organisation, ou si vous avez des utilisateurs qui partagent des ordinateurs:</p></td>
<td align="left"><p>Procédez comme suit:</p>
<ol>
<li><p>Créer un package qui contient Office, Visio et Project.</p></li>
<li><p>Déployer le package auprès de tous les utilisateurs.</p></li>
<li><p>Utilisez <a href="https://technet.microsoft.com/library/dd723678.aspx" data-raw-source="[Microsoft AppLocker](https://technet.microsoft.com/library/dd723678.aspx)"> Microsoft AppLocker </a> pour empêcher des utilisateurs spécifiques d’utiliser Visio et Project.</p></li>
</ol></td>
</tr>
</tbody>
</table>
<p> </p></td>
</tr>
</tbody>
</table>



## Ressources supplémentaires


**Office 2013 App-V 5,0 packages 5,0 ressources supplémentaires**

[Outil déploiement d’Office pour Office «démarrer en un clic»](https://go.microsoft.com/fwlink/p/?LinkID=330672)

[Scénarios pris en charge pour le déploiement de Microsoft Office en tant que package App-V séquencé](https://go.microsoft.com/fwlink/p/?LinkId=330680)

**Packages App-V 5,0 dans Office 2010**

[Kit de séquençage Microsoft Office 2010 pour Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330681)

[Problèmes connus lors de la création ou de l’utilisation d’un package App-V 5,0 Office 2010](https://go.microsoft.com/fwlink/p/?LinkId=330682)

[Comment séquencer Microsoft Office 2010 dans Microsoft Application Virtualization 5,0](https://go.microsoft.com/fwlink/p/?LinkId=330676)

**Groupes de connexion**

[Déploiement de groupes de connexion dans Microsoft App-V v5](https://go.microsoft.com/fwlink/p/?LinkId=330683)

[Gestion des groupes de connexion](managing-connection-groups.md)

**Configuration dynamique**

[À propos de la configuration dynamique d'App-V5.0](about-app-v-50-dynamic-configuration.md)














