---
title: Notes de publication de MBAM2.0 SP1
description: Notes de publication de MBAM2.0 SP1
author: dansimp
ms.assetid: b39002ba-33c6-45ec-9d1b-464327b60f5c
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, security
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 54a77fc7a493b36217ae2cdc875226b25fdc6e7b
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811243"
---
# Notes de publication de MBAM2.0 SP1


Pour effectuer une recherche dans ces notes de publication, appuyez sur Ctrl + F.

Lisez attentivement ces notes de publication avant d’installer Microsoft BitLocker administration et l’analyse (MBAM) 2,0 Service Pack 1 (SP1). Ces notes de publication contiennent des informations nécessaires pour l’installation réussie de l’administration et de la surveillance de 2,0 SP1 et contiennent des informations qui ne sont pas disponibles dans la documentation du produit. S’il existe une différence entre ces notes de publication et d’autres documents MBAM 2,0 SP1, la dernière modification doit être considérée comme faisant autorité. Ces notes de publication remplacent le contenu qui est inclus dans ce produit.

## <a href="" id="---------mbam-2-0-sp1-known-issues"></a> Problèmes connus de MBAM 2,0 SP1


Cette section contient des problèmes connus de MBAM 2,0 SP1.

### La mise à niveau d’MBAM avec la topologie intégrée de Configuration Manager vers MBAM 2,0 SP1 nécessite une suppression manuelle des objets Configuration Manager

Si vous utilisez MBAM avec Configuration Manager et que vous souhaitez effectuer une mise à niveau vers MBAM 2,0 SP1, vous devez supprimer manuellement tous les objets de Configuration Manager installés dans Configuration Manager dans le cadre de l’installation d’MBAM. Les objets que vous devez supprimer manuellement sont les rapports MBAM, la collection MBAM d’ordinateurs pris en charge et la ligne de base de configuration de protection de BitLocker ainsi que les éléments de configuration associés.

**Solution de contournement**: mettez à niveau les objets de Configuration Manager en procédant comme suit:

1.  Sauvegardez des données de conformité existantes dans un fichier externe, comme décrit dans les étapes suivantes.

    **Remarques**  Toutes les données de conformité BitLocker existantes seront supprimées lorsque vous supprimez le planning de référence existant dans Configuration Manager. Les données seront régénérées dans le temps, mais nous vous conseillons d’enregistrer une copie des données dans le cas où vous aurez besoin des informations de conformité d’un ordinateur particulier avant la régénération des données de conformité.

     

    1.  Pour enregistrer les données de conformité BitLocker historiques, ouvrez le rapport **Détails de conformité de BitLocker Enterprise** .

    2.  Cliquez sur l’icône **Enregistrer** dans le rapport et sélectionnez **Excel**.

        Le rapport enregistré contient des données telles que le nom de l’ordinateur, le nom de domaine, l’état de conformité, l’exemption, les utilisateurs de l’appareil, les détails de l’état de la conformité et la date/heure du dernier contact. Des informations, telles que les informations détaillées sur le volume et la force de cryptage, ne sont pas enregistrées.

2.  Désinstaller **MBAM** du serveur à l’aide du programme d’installation de **MBAM** .

3.  Supprimez manuellement les objets suivants de Configuration Manager:

    -   Collection d’ordinateurs pris en charge par MBAM

    -   Baseline protection de BitLocker

    -   Élément de configuration de protection de lecteur du système d’exploitation BitLocker

    -   Élément de configuration de protection de périphériques de données fixes BitLocker

4.  Supprimez manuellement le dossier MBAM rapports dans le site SQL Server Reporting Services Configuration Manager. Pour cela, procédez comme suit:

    1.  Utilisez Internet Explorer pour accéder au point Reporting Services, par exemple http:// &lt; yourcmserver &gt; /reports.

    2.  Cliquez sur le lien correspondant au code du site gestionnaire de configuration.

    3.  Supprimez le dossier MBAM.

5.  Utilisez le programme d’installation de MBAM Server pour réinstaller les objets d’intégration de Configuration Manager. Les ordinateurs client vont commencer à télécharger les données de compatibilité de BitLocker au fil du temps.

### Le bouton d’envoi du portail libre-service ne fonctionne pas dans Internet Explorer10

Lorsque vous utilisez Internet Explorer10 pour accéder au site Web d’administration et de contrôle, le bouton d' **envoi** sur le site Web ne fonctionne pas.

**Solution**: sur le serveur sur lequel vous avez installé le site Web d’administration et de surveillance, installez le [correctif pour les fichiers de définition de navigateur ASP.net](https://go.microsoft.com/fwlink/?LinkId=317798).

### Les noms de domaines internationaux ne sont pas pris en charge

MBAM 2,0 SP1 ne prend pas en charge les noms de domaines internationaux.

**Solution de contournement**: aucune.

### Les rapports figurant sur le site Web d’administration et de surveillance affichent un avertissement si SSL n’est pas configuré dans SSRS

Si SQLServer Reporting Services (SSRS) n’a pas été configuré pour utiliser SSL (Secure Socket Layer), l’URL des rapports sera définie sur HTTP au lieu de HTTPs lors de l’installation du serveur MBAM. Si vous naviguez jusqu’au site Web Administration et surveillance et sélectionnez un rapport, le message suivant s’affiche: «seul le contenu sécurisé est affiché».

**Solution**: pour résoudre ce problème, configurez SSL dans le **Gestionnaire de configuration Reporting Services** sur le serveur MBAM sur lequel SqlServer Reporting Services est installé. Désinstallez, puis réinstallez le site Web du serveur d’administration et de surveillance.

### Cliquer sur retour dans le rapport synthèse de conformité peut générer une erreur

Si vous explorez un rapport de synthèse de conformité, puis cliquez sur le lien **retour** dans le rapport SSRS, une erreur peut se produire.

**Solution de contournement**: aucune.

### Le chiffrement de l’espace utilisé uniquement ne fonctionne pas correctement

Si vous chiffrez un ordinateur pour la première fois après avoir installé le client MBAM, et que vous avez défini un objet de stratégie de groupe pour implémenter l’espace utilisé uniquement pour le chiffrement, MBAM chiffre par erreur le disque entier au lieu de chiffrer uniquement l’espace utilisé du disque. Si un ordinateur est déjà chiffré avec un chiffrement de l’espace utilisé uniquement avant d’installer le client MBAM, et que vous avez défini l’espace utilisé uniquement pour le chiffrement de l’objet de stratégie de groupe, MBAM reconnaît ce paramètre et signale correctement le chiffrement dans les rapports de conformité.

**Solution de contournement**: aucune.

### Le niveau de cryptage ne s’affiche pas correctement dans le rapport de conformité ordinateur

Si vous ne définissez pas de niveau de chiffrement spécifique dans l’objet **choisir la méthode de chiffrement de lecteur et** la stratégie de groupe force de chiffrement, le rapport de conformité de l’ordinateur dans la topologie intégrée de Configuration Manager s’affiche toujours comme **inconnu** pour la puissance de chiffrement, même si la puissance de chiffrement utilise la valeur par défaut du chiffrement de 128 bits. Le rapport affiche le niveau de cryptage approprié si vous définissez un niveau de cryptage spécifique dans l’objet de stratégie de groupe.

**Solution de contournement**: définissez toujours une clé de chiffrement spécifique dans la **méthode sélectionner le chiffrement de lecteur et** l’objet de stratégie de groupe niveau de mesure du chiffrement.

### Distribution de l’état de conformité par type de lecteur affiche les anciennes données après la mise à jour des éléments de configuration

Après avoir mis à jour les éléments de configuration MBAM dans SystemCenter2012 ConfigurationManager, le graphique barre de distribution de l’état de conformité par type de lecteur sur le tableau de bord de conformité de BitLocker Enterprise affiche des données basées sur des informations provenant de versions antérieures des éléments de configuration.

**Solution de contournement**: aucune. La modification des éléments de configuration MBAM n’est pas prise en charge et le rapport risque de ne pas apparaître comme prévu.

### La configuration de la sécurité améliorée risque de provoquer l’affichage incorrect des États

Si la configuration de sécurité améliorée d’Internet Explorer (ESC) est activée, un message d' **accès refusé** peut s’afficher lorsque vous tentez d’afficher des rapports sur le serveur MBAM. Par défaut, la configuration de la sécurité améliorée est activée pour protéger le serveur en diminuant l’exposition du serveur aux attaques potentielles qui peuvent se produire via le contenu Web et les scripts d’application.

**Solution**: si le message **accès refusé** s’affiche lorsque vous essayez d’afficher des rapports sur le serveur MBAM, vous pouvez définir un objet de stratégie de groupe ou modifier le paramètre par défaut manuellement dans votre image pour désactiver la configuration de sécurité améliorée. Vous pouvez également afficher les rapports à partir d’un autre ordinateur sur lequel la configuration de la sécurité améliorée n’est pas activée.

### <a href="" id="-------------mbam-server-installation-fails-when-you-upgrade-from-sql-server-2008-to-sql-server-2012"></a> Échec de l’installation de MBAM Server lors de la mise à niveau de SQLServer2008 vers SQLServer2012

Si vous effectuez une mise à niveau de SQLServer2008 vers SQLServer2012, puis essayez d’installer la base de données de conformité et d’audit ou la base de données de récupération, l’installation échoue et restaure. L’échec se produit parce que le fichier SQLCMD.exe requis a été supprimé lors de la mise à niveau de SQLServer et qu’il est introuvable par le programme d’installation MBAM. Les lignes du fichier journal MSI risquent de ressembler à ce qui suit:

CA Recovery DB RunDbInstallScript: BinDir-E:\\MSSQL\\100\\Tools\\Binn\\SqlCmd.exeRunDbInstallScript de récupération de la base de connaissances: dbInstance-xxxxxx\\I01RunDbInstallScript récupération de la base de connaissances: sqlScript-C:\\Program Files\\Microsoft\\Microsoft BitLocker administration et Monitoring\\Setup\\KeyRecovery.sqlRunDbInstallScript Recovery DB: dbName-MBAM \ _Recovery \ _and \ _HardwareRunDbInstallScript de la _Recovery base de connaissances: DefaultFilename-MBAM AUTORITÉ de I01\\MSSQL\\DATA\\RunDbInstallScript de récupération de la base de connaissances: defaultLogPath-K:\\MSSQL\\MSSQL10. CA Recovery DB I01\\MSSQL\\Data\\RunDbInstallScript: scriptLogPath-C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log-e-E-S xxxxxxx\\I01-i "C:\\Program Files\\Microsoft\\Microsoft BitLocker and Monitoring\\Setup\\KeyRecovery.sql"-v DatabaseName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultFileName = "MBAM \ _Recovery \ _and \ _Hardware" DefaultDataPath = "F:\\MSSQL\\MSSQL10. I01\\MSSQL\\DATA\\ "DefaultLogPath =" K:\\MSSQL\\MSSQL10. I01\\MSSQL\\Data\\ "-o" C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\InstallKeyComplianceDatabase.log "RunDbInstallScript de récupération de la base de connaissances: commencez à exécuter l’installation de la base de données de récupération scriptRunDbInstallScript de la base de données de récupération: le fichier journal de récupération de la base de données de récupération se trouve dans C:\\Users\\xxxxxx\\AppData\\Local\\Temp\\\\InstallKeyRecoveryDatabase.logRunDbInstallScript exception de l’autorité de certification.

Le programme d’installation de l’application MBAM Server Windows est codé en dur pour trouver le chemin d’accès SQLCMD.exe en consultant la valeur de chaîne Path dans le Registre sous HKLM\\Software\\Microsoft\\Microsoft SQLServer\\100\\Tools\\ClientSetup. La clé est toujours présente lors de la migration de SQLServer2008 vers SQLServer2012, mais le chemin d’accès référencé par la valeur Data ne contient pas le fichier SQLCMD.exe, car le processus SQLupgrade a supprimé le fichier.

**Solution de contournement**: renommez temporairement la valeur de chaîne de chemin d’accès SQLServer\\100\\Tools\\ClientSetup HKLM\\Software\\Microsoft\\Microsoft sur **path \ _OLD**, puis exécutez de nouveau Windows Installer sur le serveur MBAM. Lorsque l’installation est terminée, et crée les bases de données dans SQLServer2012, renommez **path \ _OLD** sur **path**.

## HotFix et Articles de la base de connaissances pour MBAM 2,0 SP1


Cette section contient des correctifs et des Articles de la base de connaissances pour MBAM 2,0 SP1.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><strong>Article de la base de connaissances</strong></th>
<th align="left">Title</th>
<th align="left"><strong>Link</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p>2831166</p></td>
<td align="left"><p>L’installation de Microsoft BitLocker administration et surveillance (MBAM) 2,0 échoue avec les &quot; objets System Center cm déjà installés&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2831166/EN-US" data-raw-source="[support.microsoft.com/kb/2831166/EN-US](https://support.microsoft.com/kb/2831166/EN-US)">support.microsoft.com/kb/2831166/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870849</p></td>
<td align="left"><p>Les utilisateurs ne peuvent pas récupérer la clé de récupération BitLocker à l’aide du portail libre-service MBAM 2.0</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870849/EN-US" data-raw-source="[support.microsoft.com/kb/2870849/EN-US](https://support.microsoft.com/kb/2870849/EN-US)">support.microsoft.com/kb/2870849/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2756402</p></td>
<td align="left"><p>Le client MBAM échoue avec l’ID d’événement 4 et le code d’erreur 0x8004100E dans la description de l’événement.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2756402/EN-US" data-raw-source="[support.microsoft.com/kb/2756402/EN-US](https://support.microsoft.com/kb/2756402/EN-US)">support.microsoft.com/kb/2756402/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620287</p></td>
<td align="left"><p>Message d’erreur «erreur serveur dans l’application «/Reports» lorsque vous cliquez sur l’onglet rapports dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620287/EN-US" data-raw-source="[support.microsoft.com/kb/2620287/EN-US](https://support.microsoft.com/kb/2620287/EN-US)">support.microsoft.com/kb/2620287/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2639518</p></td>
<td align="left"><p>Erreur lors de l’ouverture des rapports de conformité entreprise ou ordinateur dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2639518/EN-US" data-raw-source="[support.microsoft.com/kb/2639518/EN-US](https://support.microsoft.com/kb/2639518/EN-US)">support.microsoft.com/kb/2639518/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM entreprise n’a pas effectué de mise à jour</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2712461</p></td>
<td align="left"><p>L’installation de MBAM sur un contrôleur de domaine n’est pas prise en charge.</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2712461/EN-US" data-raw-source="[support.microsoft.com/kb/2712461/EN-US](https://support.microsoft.com/kb/2712461/EN-US)">support.microsoft.com/kb/2712461/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2876732</p></td>
<td align="left"><p>Vous recevez le code d’erreur 0x80071a90 lors de l’installation d’MBAM 2.0 dans le cadre d’une intégration autonome ou du gestionnaire de configuration</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2876732/EN-US" data-raw-source="[support.microsoft.com/kb/2876732/EN-US](https://support.microsoft.com/kb/2876732/EN-US)">support.microsoft.com/kb/2876732/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2754259</p></td>
<td align="left"><p>MBAM et sécuriser la communication réseau</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2754259/EN-US" data-raw-source="[support.microsoft.com/kb/2754259/EN-US](https://support.microsoft.com/kb/2754259/EN-US)">support.microsoft.com/kb/2754259/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870842</p></td>
<td align="left"><p>Échec de l’installation d’MBAM 2.0 lors du scénario d’intégration de Configuration Manager avec SQL Server 2008</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870842/EN-US" data-raw-source="[support.microsoft.com/kb/2870842/EN-US](https://support.microsoft.com/kb/2870842/EN-US)">support.microsoft.com/kb/2870842/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2668533</p></td>
<td align="left"><p>Échec de la configuration d’MBAM si le SSRS SQL n’est pas configuré correctement</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2668533/EN-US" data-raw-source="[support.microsoft.com/kb/2668533/EN-US](https://support.microsoft.com/kb/2668533/EN-US)">support.microsoft.com/kb/2668533/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2870847</p></td>
<td align="left"><p>Le programme d’installation de MBAM 2,0 est en échec avec &quot; récupération d’erreur dans les paramètres de rôle du serveur Configuration Manager pour &#39;Reporting Services Point&#39;&quot;</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870847/EN-US" data-raw-source="[support.microsoft.com/kb/2870847/EN-US](https://support.microsoft.com/kb/2870847/EN-US)">support.microsoft.com/kb/2870847/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2870839</p></td>
<td align="left"><p>Les rapports d’entreprise MBAM 2.0 ne sont pas actualisés dans la topologie autonome MBAM 2.0 en raison de l’échec du CreateCache de travail SQL</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2870839/EN-US" data-raw-source="[support.microsoft.com/kb/2870839/EN-US](https://support.microsoft.com/kb/2870839/EN-US)">support.microsoft.com/kb/2870839/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2620269</p></td>
<td align="left"><p>MBAM entreprise n’a pas effectué de mise à jour</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2620269/EN-US" data-raw-source="[support.microsoft.com/kb/2620269/EN-US](https://support.microsoft.com/kb/2620269/EN-US)">support.microsoft.com/kb/2620269/EN-US</a></p></td>
</tr>
<tr class="odd">
<td align="left"><p>2935997</p></td>
<td align="left"><p>MBAM-XX XXXXXXXXX xxxxxxxxx xxxxxxxxx</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2935997/EN-US" data-raw-source="[support.microsoft.com/kb/2935997/EN-US](https://support.microsoft.com/kb/2935997/EN-US)">support.microsoft.com/kb/2935997/EN-US</a></p></td>
</tr>
<tr class="even">
<td align="left"><p>2612822</p></td>
<td align="left"><p>L’enregistrement d’ordinateur est rejeté dans MBAM</p></td>
<td align="left"><p><a href="https://support.microsoft.com/kb/2612822/EN-US" data-raw-source="[support.microsoft.com/kb/2612822/EN-US](https://support.microsoft.com/kb/2612822/EN-US)">support.microsoft.com/kb/2612822/EN-US</a></p></td>
</tr>
</tbody>
</table>

 

## Rubriques connexes


[À propos de MBAM2.0 SP1](about-mbam-20-sp1.md)

 

 





