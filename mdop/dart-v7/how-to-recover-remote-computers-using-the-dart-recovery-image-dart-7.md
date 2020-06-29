---
title: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: 66bc45fb-dc40-4d47-b583-5bb1ff5c97a7
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 885ab1d1cf8f51dc4fd4613e41a20a2525ea7d6d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809569"
---
# Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT


Les fonctionnalités de connexion à distance de Microsoft Diagnostics and Recovery Tools (DaRT) 7 permettent à un administrateur informatique d’exécuter les outils DaRT à distance sur un ordinateur d’utilisateur final. Lorsque certaines informations sont fournies par l’utilisateur final (ou par un professionnel du support technique travaillant sur l’ordinateur de l’utilisateur final), l’administrateur informatique ou l’agent de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.

**Important**  
Les deux ordinateurs qui établissent une connexion à distance doivent faire partie du même réseau.



**Pour récupérer un ordinateur distant à l’aide de DaRT**

1.  Démarrez un ordinateur utilisateur final en utilisant l’image de récupération DaRT.

    En règle générale, vous devez utiliser l’une des méthodes suivantes pour démarrer dans DaRT afin de récupérer un ordinateur distant, selon la manière dont vous déployez l’image de récupération DaRT. Pour plus d’informations sur le déploiement de l’image de récupération DaRT, voir [déploiement de l’image de récupération 7,0 de DART](deploying-the-dart-70-recovery-image-dart-7.md).

    -   Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.

    -   Démarrez dans DaRT à partir d’une partition distante sur le réseau.

    Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 7,0 de DART](planning-how-to-save-and-deploy-the-dart-70-recovery-image.md).

    Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.

    **Remarque**  
    La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.



2.  Au démarrage de l’ordinateur dans l’image de récupération DaRT, la boîte de dialogue **netstart** s’affiche. Vous êtes invité à indiquer si vous souhaitez initialiser les services réseau. Si vous cliquez sur **Oui**, on suppose qu’un serveur DHCP est présent sur le réseau et qu’une tentative d’obtention d’une adresse IP du serveur est effectuée. Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.

    Pour ignorer le processus d’initialisation du réseau, cliquez sur **non**.

3.  Après la boîte de dialogue initialisation du réseau, vous êtes invité à indiquer si vous souhaitez remapper les lettres de lecteur. Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion. Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne. Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.

4.  Après la boîte de dialogue remappage, une boîte de dialogue **options de récupération du système** s’affiche et vous invite à sélectionner une disposition de clavier. Il affiche ensuite le répertoire racine du système, le type de système d’exploitation installé et la taille de partition. Si vous ne voyez pas votre système d’exploitation et que vous suspectez qu’il n’y a pas de problème, cliquez sur **charger des pilotes** pour charger les pilotes suspects. Vous êtes alors invité à insérer le média d’installation pour l’appareil et à sélectionner le pilote. Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.

    **Remarque**  
    Si l’environnement de récupération Windows (WinRE) détecte ou suspecte que Windows 7 ne démarrait pas correctement la dernière fois qu’il a été essayé, la **réparation du démarrage** peut commencer à s’exécuter automatiquement. Pour plus d’informations sur la façon de résoudre ce problème, reportez-vous à la rubrique [résolution des problèmes DaRT 7,0](troubleshooting-dart-70-new-ia.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

5. Dans la fenêtre des **options de récupération du système** , sélectionnez **Microsoft Diagnostics and Recovery Tools** pour ouvrir la fenêtre de **Diagnostics et d’outils de récupération** .

6. Dans la fenêtre **jeu d’outils de diagnostics et de récupération** , cliquez sur **connexion à distance** pour ouvrir la fenêtre de **connexion à distance DART** . Si vous êtes invité à fournir l’accès distant au support technique, cliquez sur **OK**.

   La fenêtre de connexion à distance DaRT s’ouvre et affiche un numéro de ticket, une adresse IP et des informations de port.

7. Sur l’ordinateur de l’agent de support technique, ouvrez la **visionneuse de connexion à distance DART**.

   Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft DART 7**, puis sur **visionneuse de connexions à distance DART**.

8. Dans la fenêtre de **connexion à distance de DART** , entrez les informations requises sur le ticket, l’adresse IP et le port.

   **Remarque**  
   Ces informations sont créées sur l’ordinateur de l’utilisateur final et doivent être fournies par l’utilisateur final. Plusieurs adresses IP peuvent être proposées, en fonction du nombre de personnes disponibles sur l’ordinateur de l’utilisateur final.



9. Cliquez sur **Se connecter**.

L’administrateur informatique suppose désormais le contrôle de l’ordinateur de l’utilisateur final et peut exécuter les outils DaRT à distance.

**Remarque**  
Un fichier nommé inv32.xml contient des informations de connexion distantes, telles que le numéro de port et l’adresse IP. Par défaut, le fichier se trouve généralement sur%windir%\\system32.



**Pour personnaliser le processus de connexion à distance**

1. Vous pouvez personnaliser le processus de connexion à distance en modifiant le fichier winpeshl.ini. Pour plus d’informations sur la modification du fichier winpeshl.ini, voir [Winpeshl.ini de fichiers](https://go.microsoft.com/fwlink/?LinkId=219413).

   Spécifiez les commandes et les paramètres suivants pour personnaliser l’établissement d’une connexion distante avec un ordinateur d’utilisateur final:

   <table>
   <colgroup>
   <col width="33%" />
   <col width="33%" />
   <col width="33%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Commande</th>
   <th align="left">Paramètre</th>
   <th align="left">Description</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p><strong>RemoteRecovery.exe</strong></p></td>
   <td align="left"><p>-nomessage</p></td>
   <td align="left"><p>Spécifie que l’invite de confirmation ne s’affiche pas. <strong>La connexion à distance </strong> continue comme si l’utilisateur final avait répondu &quot; Oui &quot; à l’invite de confirmation.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p><strong>WaitForConnection.exe</strong></p></td>
   <td align="left"><p>aucune</p></td>
   <td align="left"><p>Empêche la poursuite d’un script personnalisé tant que <strong> la connexion à distance n' </strong> est pas en cours d’exécution ou qu’une connexion valide est établie avec l’ordinateur de l’utilisateur final.</p>
   <div class="alert">
   <strong>Important</strong><br/><p>Cette commande n’utilise aucune fonction si elle est spécifiée de manière indépendante. Il doit être spécifié dans un script pour fonctionner correctement.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Voici un exemple de fichier winpeshl.ini personnalisé pour ouvrir l’outil de **connexion à distance** dès qu’une tentative de démarrage dans DART est lancée:

   ```ini
   [LaunchApps]
   "%windir%\system32\netstart.exe -network -remount"
   "cmd /C start %windir%\system32\RemoteRecovery.exe -nomessage"
   "%windir%\system32\WaitForConnection.exe"
   "%SYSTEMDRIVE%\sources\recovery\recenv.exe"
   ```

**Pour exécuter la visionneuse de connexions à distance à l’invite de commandes**

1.  Vous pouvez exécuter la **visionneuse de connexions à distance DART** à l’invite de commandes en spécifiant la commande **DartRemoteViewer.exe** et en utilisant les paramètres suivants:

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">Paramètre</th>
    <th align="left">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>-ticket = &lt; <em> ticketnumber</em>&gt;</p></td>
    <td align="left"><p>Où &lt; <em> ticketnumber </em> &gt; correspond au numéro de ticket, y compris aux tirets, qui est généré par la connexion à distance.</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>-IPAddress = &lt; <em> IPAddress</em>&gt;</p></td>
    <td align="left"><p>Où &lt; <em> IPAddress </em> &gt; est l’adresse IP générée par la connexion à distance.</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>-port = &lt; <em> port</em>&gt;</p></td>
    <td align="left"><p>Où &lt; <em> port </em> &gt; correspond au port qui correspond à l’adresse IP spécifiée.</p></td>
    </tr>
    </tbody>
    </table>



~~~
**Note**  
The variables for these parameters are created on the end-user computer and must be provided by the end user.
~~~



2. Si les trois paramètres sont spécifiés et que les données sont valides, une connexion est effectuée immédiatement au démarrage du programme. Si un paramètre n’est pas valide, le programme démarre comme s’il n’y a aucun paramètre spécifié.

## Rubriques connexes


[Récupération des ordinateurs à l'aide de DaRT7.0](recovering-computers-using-dart-70-dart-7.md)









