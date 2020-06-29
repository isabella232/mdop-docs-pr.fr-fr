---
title: Créer un package d'espace de travail MED-V
description: Créer un package d'espace de travail MED-V
author: dansimp
ms.assetid: 3f75fe73-41ac-4389-ae21-5efb2d437f4d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e20cf4cc9394c4a5e90178fff4fc36ed83c12d60
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809851"
---
# Créer un package d'espace de travail MED-V


Un espace de travail MED-V est l’environnement de bureau Windows XP dans lequel les utilisateurs finaux interagissent avec l’ordinateur virtuel fourni par MED-V. L’administrateur crée et personnalise l’espace de travail MED-V. L’espace de travail se compose d’une image et de la stratégie de groupe définissant les règles et les fonctionnalités de l’espace de travail MED-V.

Vous pouvez créer plusieurs espaces de travail MED-V, chacun personnalisé avec ses propres configurations, paramètres et règles. Un utilisateur, un groupe ou plusieurs utilisateurs ou groupes peuvent être associés à chaque espace de travail MED-V. La personnalisation rend l’espace de travail MED-V uniquement disponible pour cet utilisateur ou groupe.

Utilisez le **Gestionnaire de package d’espace de travail MED-v** pour créer des espaces de travail MED-v. Le **module de création de package de l’espace de travail MED-V** est divisé en deux sections principales:

-   Panneau principal incluant trois boutons qui vous permettent de créer et de gérer des espaces de travail MED-V. Le bouton **créer un package d’espace de travail MED-v** ouvre l' **Assistant créer un package d’espace de travail MED-v** qui vous permet de créer vos espaces de travail MED-v.

-   **Centre d’aide** sur le côté droit de la fenêtre proposant des informations et des conseils pour vous aider à créer, tester et gérer vos espaces de travail MED-V.

**Important**  
Pour pouvoir utiliser le **Gestionnaire de package d’espace de travail MED-V**, vous devez d’abord vérifier que la stratégie d’exécution Windows PowerShell est définie sur non restreinte.

`Set-ExecutionPolicy Unrestricted`

Par ailleurs, la stratégie du réseau SAN de l’ordinateur sur lequel est exécuté le package de l' **espace de travail MED-V** doit être définie sur «tout en ligne». Pour vérifier le paramètre de la stratégie SAN, exécutez les commandes suivantes à l’invite de commandes avec les informations d’identification d’administration:

`diskpart.exe`

`DISKPART> san`

`DISKPART> exit`

Le cas échéant, modifiez la stratégie SAN en «tout en ligne» en tapant les commandes suivantes à l’invite de commandes avec les informations d’identification d’administration:

`diskpart.exe`

`DISKPART> san policy=onlineall`

`DISKPART> exit`



**Important**  
Si un logiciel de chiffrement automatique de disque est installé sur l’ordinateur que vous utilisez pour monter le disque dur virtuel et générer le package d’espace de travail MED-V, vous devez désactiver le logiciel avant de commencer. Dans le cas contraire, vous ne pouvez pas utiliser l’espace de travail MED-V sur un autre ordinateur.



Les informations fournies ici peuvent vous aider à créer votre package de déploiement d’espace de travail MED-V.

## <a href="" id="bkmk-prereq"></a>Conditions préalables


Avant de commencer à créer votre package de déploiement d’espace de travail MED-V, vérifiez que vous avez accès aux éléments suivants:

-   **Image Windows XP préparée**

    Pour plus d’informations sur la création d’une image Windows XP à utiliser avec MED-V, voir [préparer une image med-v](prepare-a-med-v-image.md).

-   **Fichier texte ou liste contenant des informations de redirection d’URL**

    Votre fichier texte ou liste d’URL de redirection d’URL contient les URL que vous voulez rediriger de l’ordinateur hôte vers Internet Explorer dans l’espace de travail MED-V. Lorsque vous utilisez l’Assistant Packaging pour créer votre espace de travail MED-V, vous importez, tapez ou copiez et collez ces informations de redirection comme une des étapes du processus de création de package.

    **Remarque**  
    La redirection d’URL dans MED-V ne prend en charge que les protocoles HTTP et HTTPs. MED-V ne fournit pas de prise en charge pour FTP ou tout autre protocole.



~~~
Enter each web address on a single line, for example:

http://www.contoso.com/webapps/webapp1

http://www.contoso.com/webapps/webapp2

http://\*.contoso.com

http://www.contoso.com/webapps/\*

**Important**  
If you import a text file that includes a URL that uses special characters (such as ~ ! @ \# and so on), make sure that you specify UTF-8 encoding when you save the text file. Special characters do not import correctly into the MED-V Workspace Packager if the text file was saved using the default ANSI encoding.
~~~



## Empaquetage d’un espace de travail MED-V pour une langue autre que celle du langage de l’ordinateur de package de l’espace de travail MED-V


Par défaut, l’espace de travail MED-V prend en charge les caractères dans la langue du système et en anglais. Pour créer un espace de travail MED-V pour une langue autre que celle installée sur l’ordinateur, spécifiez **-loc \ [locale \]** dans le script PowerShell (. ps1) après le nom de l’espace de travail MED-v.

Pour créer un package d’espace de travail MED-V dans une langue autre que la langue par défaut de l’ordinateur de package de l’espace de travail MED-v, générez un script dans la langue par défaut en exécutant le gestionnaire de package MED-v, puis modifiez le script de sortie comme il est requis pour vos paramètres régionaux. Le script est situé dans le répertoire de sortie de l’espace de travail MED-V qui a été spécifié lors de la création de packages. Les noms des paramètres régionaux apparaissent dans la zone de recherche. Fichiers WXL dans l’annuaire suivant:

C:\\Program Files\\Microsoft Enterprise Desktop Virtualization\\WindowsPowerShell\\Modules\\Microsoft.Medv.Administration.Commands.WorkspacePackager\\locale

## Création d’un package d’espace de travail MED-V


Pour créer un package d’espace de travail MED-V, procédez comme suit:

****

1.  Pour ouvrir le **Gestionnaire de package de l’espace de travail MED-v**, cliquez sur **Démarrer**, **tous les programmes**, cliquez sur **Microsoft Enterprise Desktop Virtualization**, puis sur **med-v Workspace**.

2.  Dans le volet principal du **Gestionnaire de package de l’espace de travail MED-v** , cliquez sur **créer un package d’espace de travail MED-v**.

    L' **Assistant Création de package d’espace de travail MED** -v s’affiche. L’Assistant comprend les pages suivantes:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <tbody>
    <tr class="odd">
    <td align="left"><p><strong>Informations de package</strong></p></td>
    <td align="left"><p>Spécifiez un nom pour l’espace de travail MED-V et sélectionnez un dossier dans lequel les fichiers de package d’espace de travail MED-V sont enregistrés.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Sélectionner l’image Windows XP</strong></p></td>
    <td align="left"><p>Spécifiez l’image de votre PC virtuel Windows XP préparé.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Configuration pour la première fois</strong></p></td>
    <td align="left"><p>Spécifiez le processus d’installation que MED-V suit lors de la première configuration.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Messages MED-V</strong></p></td>
    <td align="left"><p>Spécifiez les messages et l’URL facultative pour les informations d’aide que l’utilisateur final voit lors du premier démarrage.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Attribution d’un nom aux ordinateurs</strong></p></td>
    <td align="left"><p>Spécifiez le nom de l’ordinateur virtuel MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Copier les paramètres à partir de l’hôte</strong></p></td>
    <td align="left"><p>Spécifiez le mode de définition des paramètres de l’espace de travail MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Démarrage et mise en réseau</strong></p></td>
    <td align="left"><p>Spécifiez les paramètres de démarrage de l’espace de travail, de la mise en réseau et des informations d’identification de l’utilisateur MED-V.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p><strong>Redirection Web</strong></p></td>
    <td align="left"><p>Spécifiez un fichier texte ou une liste d’URL que vous voulez rediriger vers Internet Explorer dans l’espace de travail MED-V.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p><strong>Résumé</strong></p></td>
    <td align="left"><p>Vérifiez vos paramètres d’espace de travail MED-V et commencez à créer votre package de déploiement d’espace de travail MED-V.</p></td>
    </tr>
    </tbody>
    </table>



3.  Dans la page informations sur le **paquet** , entrez un nom pour l’espace de travail MED-v, puis sélectionnez un dossier dans lequel les fichiers de package d’espace de travail MED-v sont enregistrés.

    **Warning**  
    Vous devez nommer l’espace de travail MED-V et spécifier un dossier pour continuer.



~~~
After you have finished, click **Next**.
~~~

4. Dans la page **Sélectionner une image Windows XP** , spécifiez l’emplacement de l’image de votre PC virtuel MED-V Windows XP (fichier. vhd).

   **Warning**  
   Vous devez spécifier une image de disque dur virtuel Windows XP pour continuer.



~~~
After you have finished, click **Next**.
~~~

5. Dans la page de **configuration initiale** , indiquez si vous souhaitez que la première configuration s’exécute lorsque vous avez effectué une assistance ou qu’il soit utilisé pour l’utilisation de l’espace de travail MED-V ou qu’il soit utilisé par tous les utilisateurs finaux sur un ordinateur partagé.

   Si vous sélectionnez l’option **d’installation sans assistance, sans notification**, l’utilisateur final n’est pas informé avant l’exécution de la première configuration et l’ordinateur virtuel n’est pas présenté à l’utilisateur final lors de la première configuration. De plus, la page **messages MED-V** de l’Assistant est masquée, car aucun message n’est requis lors de la première exécution du mode sans assistance.

   Si vous sélectionnez l’option **d’installation sans assistance, mais que les utilisateurs finaux peuvent notifier avant le début de la première configuration**, l’utilisateur final est averti avant l’exécution de la première fois. Toutefois, l’ordinateur virtuel n’est pas présenté à l’utilisateur final lors de la première configuration.

   Sélectionnez **configuration assistée** si l’utilisateur final doit entrer des informations lors du premier démarrage.

   Le comportement par défaut est le **programme d’installation sans assistance, mais avertir les utilisateurs finaux avant le premier démarrage du programme d’installation**.

   **Vigilance**  
   Si vous avez créé le fichier Sysprep. inf de façon à ce que la mini-installation exige l’entrée utilisateur, vous devez sélectionner l’option **d’installation avec assistance** ou des problèmes peuvent se produire lors de la première configuration.



~~~
You can also specify how a MED-V workspace is used on computers that are shared by multiple end users. You can decide that you want to create a unique MED-V workspace for each end user or that you want the MED-V workspace made available to all end users who share the computer. The default is that the MED-V workspace is unique for each end user.

**Important**  
We recommend that you disable the fast user switching feature in Windows if you configure the MED-V workspace to be accessed by all users on a shared computer. Problems can occur if an end user logs on by using the fast user switching feature in Windows when another user is still logged on.



**Tip**  
When you create a name mask for the MED-V workspace on the **Naming Computers** page, make sure that each virtual machine on a shared computer has a unique computer name.



You can also specify whether the MED-V workspace is added to the Administrators group or administrator credentials are managed outside MED-V. By default, the MED-V workspace is not automatically added to the Administrators group.

After you have finished, click **Next**.
~~~

6. Dans la page **messages MED-V** , spécifiez les messages suivants que l’utilisateur final voit lors de la première configuration:

   -   Le message visible par l’utilisateur final lors du premier démarrage de l’installation.

   -   Le message qui s’affiche lorsque l’utilisateur final se trouve lors de l’échec de la première configuration ou d’une erreur.

   **Remarque**  
   La page **messages MED-V** de l’Assistant est masquée si vous avez sélectionné **installation sans assistance, sans notification** sur la **première** page de configuration.



~~~
You can also specify an optional URL location for help information that is provided to the end user when first time setup is running.

For example, the URL can point to an internal IT webpage with answers to questions such as "How long will this take and how will I know when it has completed?" or "What do you do if you get an error message?"

**Note**  
If you specify a URL, a link is shown during first time setup that points the end user to this help information. If you do not specify a URL, no link is provided.



After you have finished, click **Next**.
~~~

7. Dans la page attribution d’un **nom aux ordinateurs** , vous pouvez spécifier si le nom de l’ordinateur est géré par MED-V ou par un outil de gestion du système tel que Sysprep. Par défaut, la gestion des noms d’ordinateur est gérée par un outil de gestion du système.

   Si vous spécifiez que le nom de l’ordinateur est géré par MED-V, sélectionnez une convention d’affectation de noms d’ordinateur prédéfinie (Mask) dans la liste déroulante. Un aperçu du nom d’un exemple d’ordinateur s’affiche en fonction de l’ordinateur que vous utilisez pour créer le package d’espace de travail MED-V.

   Si vous sélectionnez l’une des conventions d’affectation de noms personnalisées, les champs que vous pouvez spécifier sont limités aux caractères suivants:

   -   Les champs préfixe et suffixe sont limités aux caractères A-Z, a-z, 0-9 et aux caractères spéciaux. @ \ # $% ^ & ()-\ _ _ ' {}. et ~.

   -   Les champs hostname et username sont limités aux chiffres 0 à 9.

   **Important**  
   Les noms d’ordinateurs doivent être uniques et ne comporter pas plus de 15 caractères. Lorsque vous déterminez la méthode d’attribution d’noms de votre ordinateur, envisagez d’utiliser des utilisateurs finaux disposant de plusieurs ordinateurs ou du partage d’un ordinateur, et évitez d’utiliser des masques de nom d’ordinateur qui pourraient provoquer une collision sur le réseau.



~~~
**Caution**  
The computer name settings that you specify on this page override those specified in the Sysprep.inf answer file.



After you have finished, click **Next**.
~~~

8. Dans la page **copier les paramètres à partir de l’hôte** , vous pouvez sélectionner les paramètres suivants pour spécifier la façon dont l’espace de travail MED-V est configuré:

   **Vigilance**  
   Les paramètres que vous spécifiez sur cette page qui sont copiés à partir de l’ordinateur hôte vers l’espace de travail MED-V remplacent ceux spécifiés dans le fichier de réponses Sysprep. inf.



~~~
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td align="left"><p><strong>Copy regional settings</strong></p></td>
<td align="left"><p>Select this check box to copy the regional settings from the host computer to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[RegionalSettings]
Language
SystemLocale
UserLocale
UserLocale_DefaultUser
InputLocale
InputLocale_DefaultUser
</code></pre></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy user settings</strong></p></td>
<td align="left"><p>Select this check box to copy certain user settings, such as user name and company name, from the host to the MED-V workspace.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><p>If you select this check box, the following settings are set in the Sysprep.inf file:</p>
<pre class="syntax" space="preserve"><code>[UserData]
OrgName
FullName</code></pre>
<div class="alert">
<strong>Note</strong>  
<p>Personal settings, such as Internet browsing history, are not copied over to the MED-V workspace.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain name</strong></p></td>
<td align="left"><p>Select this check box to let the guest join the same domain as the host.</p></td>
</tr>
<tr class="even">
<td align="left"><p></p></td>
<td align="left"><div class="alert">
<strong>Important</strong>  
<p>The MED-V guest must be configured to join a domain that lets users log on by using the credentials that they use to log on to the MED-V host.</p>
</div>
<div>

</div></td>
</tr>
<tr class="odd">
<td align="left"><p><strong>Copy domain organizational unit</strong></p></td>
<td align="left"><p>Select this check box to copy the domain organizational unit from the host computer to the MED-V workspace. This check box is only enabled if you select to copy the domain name from the host computer.</p></td>
</tr>
</tbody>
</table>



After you have finished, click **Next**.
~~~

9. Dans la page de **démarrage et de réseau** , vous pouvez modifier le comportement par défaut des paramètres suivants:

   <table>
   <colgroup>
   <col width="50%" />
   <col width="50%" />
   </colgroup>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>Démarrer l’espace de travail MED-V</strong></p></td>
   <td align="left"><p>Indiquez si vous voulez démarrer l’espace de travail MED-V lors de l’ouverture de session de l’utilisateur, lors de la première utilisation, ou pour permettre à l’utilisateur final de décider du démarrage de l’espace de travail MED-V.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>L’espace de travail MED-V démarre de l’une des deux manières suivantes: si l’utilisateur final se connecte, ou s’il commence une action qui nécessite MED-V, comme l’ouverture d’une application publiée ou la saisie d’une URL nécessitant une redirection.</p>
   <p>Vous pouvez définir ce paramètre pour l’utilisateur final ou laisser l’utilisateur final contrôler le démarrage de MED-V.</p>
   <div class="alert">
   <strong>Remarque</strong><br/><p>Si vous spécifiez une décision définie par l’utilisateur final, le comportement par défaut qu’il présente est que l’espace de travail MED-V démarre lorsqu’il se connecte. Les utilisateurs peuvent modifier ce paramètre par défaut en cliquant avec le bouton droit sur l’icône MED-V dans la zone de notification et en sélectionnant <strong> paramètres utilisateur med-v </strong> . Si vous définissez ce paramètre pour l’utilisateur final, il ne peut pas modifier le mode de démarrage de MED-V.</p>
   </div>
   <div>

   </div></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Réseaux</strong></p></td>
   <td align="left"><p>Sélectionnez <strong> partagé </strong> ou <strong> Bridged </strong> pour votre paramètre réseau. La valeur par défaut est <strong> Shared </strong> .</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p><strong>Partagé </strong> - l’espace de travail MED-V utilise la traduction d’adresses réseau (NAT) pour partager les adresses IP de l’hôte&#39;s pour le trafic sortant.</p>
   <p><strong>Bridged </strong> - l’espace de travail MED-V dispose de sa propre adresse réseau, généralement obtenue via le protocole DHCP.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p><strong>Stocker les informations d’identification</strong></p></td>
   <td align="left"><p>Indiquez si vous souhaitez stocker les informations d’identification de l’utilisateur final.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p></p></td>
   <td align="left"><p>Le comportement par défaut est que le stockage des informations d’identification est désactivé de sorte que l’utilisateur final doit être authentifié à chaque ouverture de session.</p>
   <div class="alert">
   <strong>Important</strong><br/><p>Même si la mise en cache des informations d’identification de l’utilisateur final offre une meilleure utilisation de l’utilisateur, vous devez connaître les risques liés.</p>
   <p>Les informations d’identification de domaine de l’utilisateur final sont stockées dans un format réversible dans le gestionnaire d’informations d’identification Windows. Par conséquent, une personne malveillante pourrait écrire un programme qui récupère le mot de passe et peut accéder aux informations d’identification de l’utilisateur. Vous pouvez limiter ce risque uniquement en désactivant le stockage des informations d’identification de l’utilisateur final.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



~~~
After you have finished, click **Next**.
~~~

10. Dans la page **redirection Web** , vous pouvez entrer, coller ou importer une liste des URL redirigées vers Internet Explorer dans l’espace de travail MED-V. Pour plus d’informations sur la configuration de vos informations de redirection d’URL, voir [conditions préalables](#bkmk-prereq).

   Vous pouvez également spécifier le mode de configuration d’Internet Explorer dans l’espace de travail MED-V pour les utilisateurs finaux. Par défaut, le niveau de sécurité de zone Internet est réglé sur élevé. Par ailleurs, certaines fonctionnalités de navigation par défaut, telles que la barre d’adresse, sont supprimées. Cette configuration par défaut d’Internet Explorer dans l’espace de travail MED-V fournit un environnement de navigation plus sûr aux utilisateurs finaux.

   **Vigilance**  
   En modifiant les paramètres par défaut, vous pouvez personnaliser Internet Explorer dans l’espace de travail MED-V. Sachez que si vous modifiez les paramètres par défaut afin de les rendre moins sécurisés, vous pouvez exposer votre organisation aux risques en matière de sécurité présents dans les versions antérieures d’Internet Explorer. Pour plus d’informations, consultez [meilleures pratiques en matière de sécurité pour les opérations MED-V](security-best-practices-for-med-v-operations.md).



~~~
After you have finished, click **Next**.
~~~

11. Dans la page **Résumé** , vous pouvez consulter les paramètres de création de packages de cet espace de travail MED-V. Si vous voulez modifier des paramètres, cliquez sur le bouton **précédent** pour revenir à la page correspondante. Lorsque vous avez terminé de vérifier les paramètres, cliquez sur **créer**.

   La page de **fin** de l' **Assistant Création d’un package d’espace de travail MED-V** s’ouvre pour montrer la progression de la création du package.

   **Remarque**  
   Le processus de création de package de l’espace de travail MED-V peut prendre plusieurs minutes en fonction de la taille de VHD spécifiée.



~~~
If the MED-V workspace package is created successfully, the **Completion** page displays a list of the files that you created and their respective locations. The following is a list of the files that are created and their descriptions:

-   **setup.exe**—an installation program that you deploy and run on end-user computers to install the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.msi**—an installer file that you deploy to the end-user computers. The setup.exe file will run this file to install the MED-V workspaces.

-   **&lt;*vhd\_name*&gt;.medv**—a compressed VHD file that you deploy to the end-user computers. The setup.exe file uses it when it installs the MED-V workspaces.

-   **&lt;*workspace\_name*&gt;.reg**—the configuration settings that are installed when the setup.exe, &lt;*workspace\_name*&gt;.msi, and &lt;*vhd\_name*&gt;.medv files are deployed and setup.exe is run.

-   **&lt;*workspace\_name*&gt;.ps1**—a Windows PowerShell script that you can use to rebuild the registry file and re-build the MED-V workspace package.

    **Important**  
    Before deployment, you can edit configuration settings by updating the .ps1 file that has your preferred method of script editing, such as Windows PowerShell. After you change the .ps1 file, use that file to rebuild the MED-V workspace package that you deploy to your enterprise. For more information, see [Configuring Advanced Settings by Using Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md).

    However, after the MED-V workspace is deployed, you must edit configuration settings through the registry. For a list and description of the configuration settings, see [Managing MED-V Workspace Configuration Settings](managing-med-v-workspace-configuration-settings.md).
~~~



12. Cliquez sur **Fermer** pour fermer l’Assistant Création de packages et revenir au **Gestionnaire de package de l’espace de travail MED-V**.

Votre package d’espace de travail MED-V est désormais prêt à être testé avant le déploiement.

## Rubriques connexes


[Configuration de paramètres avancés à l'aide de Windows PowerShell](configuring-advanced-settings-by-using-windows-powershell.md)

[Tester le package d'espace de travail MED-V](testing-the-med-v-workspace-package.md)

[Préparer une image MED-V](prepare-a-med-v-image.md)









