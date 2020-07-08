---
title: Procédure pour installer le client App-V Client à l'aide de setup.msi
description: Procédure pour installer le client App-V Client à l'aide de setup.msi
author: dansimp
ms.assetid: 7221f384-36d6-409a-94a2-86f54fd75322
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 7fb3a145a6c57cccbae3f4e6b191b89d93278ff8
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807065"
---
# Procédure pour installer le client App-V Client à l'aide de setup.msi


Cette rubrique explique comment installer le client App-V à l’aide du programme setup.msi. Avant d’installer le client App-V à l’aide du programme setup.msi, vous devez d’abord déterminer si des logiciels requis doivent être installés, puis vous devez l’installer. Pour installer les logiciels requis, voir la section [installation de logiciels requis](#prereq-sw) de cette rubrique. Pour installer le logiciel client, reportez-vous à la section [installation du client App-V à l’aide de la Setup.msi programme](#msi-setup) de cette rubrique.

## <a href="" id="prereq-sw"></a>Installation de logiciels requis


Vous pouvez utiliser les procédures suivantes pour installer les logiciels requis. Vous pouvez créer un fichier de commandes et exécuter les commandes à partir de l’invite de commandes, ou vous pouvez utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter les commandes.

**Remarques**  Les versions x86 des logiciels suivants sont requises pour les versions x86 et x64 du client App-V.

 

**Pour installer le package redistribuable Microsoft VisualC + + 2005SP1 (x86)**

1. Téléchargez le package de logiciels [Microsoft Visual C++ 2005 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=119961) à partir du centre de téléchargement Microsoft ( <https://go.microsoft.com/fwlink/?LinkId=119961> ). \ [Valeur de jeton de modèle \] pour la version 4,5 SP2 et les versions ultérieures du client App-V, téléchargez vcredist\_x86.exe à partir de [Microsoft Visual C++ 2005 Service Pack 1 package redistribuable la mise à jour de sécurité ATL](https://go.microsoft.com/fwlink/?LinkId=169360) ( https://go.microsoft.com/fwlink/?LinkId=169360).\ [valeur du jeton de modèle]

2. Pour procéder à l’installation en silence, utilisez l’option de ligne de commande «/Q» avec vcredist\_x86.exe, par exemple **vcredist\_x86.exe/q**.

3. Pour installer le logiciel à l’aide du fichier vcredist\_x86.msi, utilisez l’option de ligne de commande «/C/T: &lt; fullpathtofolder &gt; » pour extraire les fichiers vcredist.msi et vcredis1.cab de vcredist\_x86.exe dans un dossier temporaire. Pour procéder à l’installation en silence, utilisez l’option/quiet de la ligne de commande (par exemple, **msiexec/i vcredist.msi** /quiet.

### Pour installer le package redistribuable Microsoft VisualC + + 2008SP1 (x86)

**Important**  Pour la version 4.6 et une version ultérieure du client App-V, vous devez également installer la mise à jour de sécurité ATL du package redistribuable Microsoft Visual C++ 2008.

 

****

1.  Téléchargez le package de logiciels de [mise à jour de sécurité ATL de Microsoft Visual C++ 2008 Service Pack 1](https://go.microsoft.com/fwlink/?LinkId=150700) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=150700) .

2.  Pour procéder à l’installation en silence, utilisez l’option de ligne de commande «/Q» avec vcredist\_x86.exe, par exemple **vcredist\_x86.exe/q**.

### Pour installer Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)

****

1.  Téléchargez le package de logiciels [Microsoft Core XML Services (MSXML) 6.0 SP1 (x86)](https://go.microsoft.com/fwlink/?LinkId=63266) à partir du centre de téléchargement Microsoft ( https://go.microsoft.com/fwlink/?LinkId=63266) .

2.  Pour procéder à l’installation en silence, utilisez l’option/quiet de la ligne de commande (par exemple, **msiexec/i msxml6\_x86.msi/quiet**).

### Pour installer le rapport d’erreurs d’application Microsoft

Lors de l’installation du rapport d’erreurs d’application Microsoft, vous devez utiliser le paramètre *APPGUID* pour spécifier le code de produit App-V. Le code de produit est unique pour chaque type et version de client App-V. Sélectionnez le bon code de produit du tableau suivant.

**Important**  Pour App-V 4.6 SP2 et les versions ultérieures, vous n’avez plus besoin d’installer le signalement d’erreurs des applications Microsoft (dw20shared.msi). App-V utilise désormais le signalement d’erreurs Microsoft.

 

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left">Version</th>
<th align="left">Code de produit pour le client de bureau</th>
<th align="left">Code de produit du client pour les services Bureau à distance</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>App-V 4,5 CU1</p></td>
<td align="left"><p>FE495DBC-6D42-4698-B61F-86E655E0796D</p></td>
<td align="left"><p>8A97C241-D92A-47DC-B360-E716C1AAA929</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,5 SP1</p></td>
<td align="left"><p>93468B43-C19D-44F9-8BCC-114076DB0443</p></td>
<td align="left"><p>0042AD3C-99A4-4E58-B5F0-744D5AD96E1C</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,5 SP2</p></td>
<td align="left"><p>C6FC75B9-7D86-4C44-8BDB-EAFE1F0E200D</p></td>
<td align="left"><p>ECF80BBA-CA07-4A74-9ED6-E064F38AF1F5</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86</p></td>
<td align="left"><p>9E9D30B2-2065-4FDE-B756-8F1A6EABAFC3</p></td>
<td align="left"><p>439FAC21-B423-41D4-8126-54F9FCB70039</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64</p></td>
<td align="left"><p>E569E45F-7BA6-4C7F-B6BA-3FFCBE92FC22</p></td>
<td align="left"><p>D2977C18-D88A-47CB-AFD8-652DD36F4D0D</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 ¹</p></td>
<td align="left"><p>40C3258B-F9D1-46DF-AE97-72C1F86F2427</p></td>
<td align="left"><p>9915D911-CC73-4122-AF4F-564F89454655</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 ¹</p></td>
<td align="left"><p>1650E31F-23B8-40B5-A60A-C5934F557E3B</p></td>
<td align="left"><p>7580D918-C621-49E7-9877-3CC59F9BD1DA</p></td>
</tr>
<tr class="even">
<td align="left"><p>App-V 4,6 x86 SP1</p></td>
<td align="left"><p>DB9F70CD-29BC-480B-8BA2-C9C2232C4553</p></td>
<td align="left"><p>1354855A-2298-4C73-9022-EF0686C65991</p></td>
</tr>
<tr class="odd">
<td align="left"><p>App-V 4,6 x64 SP1</p></td>
<td align="left"><p>342C9BB8-65A0-46DE-AB7A-8031E151AF69</p></td>
<td align="left"><p>B2C6C8D5-FE76-4056-A326-EE5D633EA175</p></td>
</tr>
</tbody>
</table>

 

¹ version «langues» App-V.

**Remarques**  Si vous avez besoin de trouver le code de produit, vous pouvez utiliser l’éditeur de base de données Orca.exe ou un outil similaire pour examiner les fichiers Windows Installer et rechercher la valeur de la propriété *ProductCode* . Pour plus d’informations sur l’utilisation de Orca.exe, voir [outils de développement Windows Installer](https://go.microsoft.com/fwlink/?LinkId=150008) ( https://go.microsoft.com/fwlink/?LinkId=150008) .

 

****

1.  Recherchez le programme d’installation du signalement d’erreurs Microsoft application, dw20shared.msi, qui se trouve dans le dossier **Support\\Watson** sur le média de publication.

2.  Pour installer le logiciel, exécutez la commande suivante:

         **msiexec /i dw20shared.msi APPGUID={valuefromtable} REBOOT=Suppress REINSTALL=ALL REINSTALLMODE=vomus**

## <a href="" id="msi-setup"></a>Installation du client App-V à l’aide du programme Setup.msi


Utilisez la procédure suivante pour installer le client App-V. Assurez-vous que tous les logiciels requis requis sont installés. \ [Valeur de jeton de modèle] pour la version 4.6 et les versions ultérieures du client App-V, le programme setup.msi vérifie le système et, si la configuration logicielle requise n’est pas installée, il génère un message d’erreur indiquant que l’installation ne peut pas continuer. \ [Valeur du jeton de modèle \]

**Pour installer le client de virtualisation des applications à l’aide de Setup.msi**

1.  Vérifiez que vous êtes connecté avec un compte disposant de droits d’administrateur sur l’ordinateur.

2.  Ouvrez une fenêtre d’invite de commandes à l’aide de droits élevés, puis modifiez le répertoire dans le dossier contenant les fichiers d’installation. Lors de l’installation de la version 4.6 ou d’une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32 ou 64 bits. L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.

3.  Entrez la chaîne de commande d’installation à l’invite de commandes. Vous pouvez également créer un fichier de commandes et l’exécuter à partir de l’invite de commandes. Vous pouvez également utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter la commande.

4.  L’exemple de ligne de commande suivant montre comment setup.msi peut être utilisé avec plusieurs paramètres facultatifs. Pour plus d’informations sur ces paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).

    **msiexec.exe/i "setup.msi" SWICACHESIZE = "10 240" SWIPUBSVRDISPLAY = "système de production" SWIPUBSVRTYPE = "HTTP/Secure" SWIPUBSVRHOST = "PRODSYS" SWIPUBSVRPORT = "443" SWIPUBSVRPATH = "/AppVirt/appsntype.xml" SWIPUBSVRREFRESH = "sur" SWIGLOBALDATA = "D:\\AppVirt\\Global" SWIUSERDATA = "^% LOCALAPPDATA ^%\\Windows\\Application virtualisation client" SWIFSDRIVE = "S"/q**

    **Important**  
    -   Le commutateur Windows Installer «**/q**» est utilisé pour effectuer une installation silencieuse.

    -   Le caractère «» **%** doit être précédé du caractère «» dans «**% HomeDrive%**» **^** . Dans le cas contraire, l’interpréteur de commandes Windows définit la valeur sur celle de l’utilisateur qui exécute l’installation.

    -   Pour activer la journalisation de l’installation, utilisez le **fichier/l\**

     

## Rubriques connexes


[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





