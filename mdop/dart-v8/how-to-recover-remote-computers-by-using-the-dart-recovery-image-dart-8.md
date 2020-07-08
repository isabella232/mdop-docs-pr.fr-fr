---
title: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: 363ccd48-6820-4b5b-a43a-323c0b208a9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 3b3e3155dbea8da18338b8a167d22f73b1c8e4bb
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810530"
---
# Procédure pour récupérer des ordinateurs distants à l'aide de l'image de récupération DaRT


Utilisez la fonctionnalité de connexion à distance dans Microsoft Diagnostics and Recovery Tools (DaRT) 8,0 pour exécuter les outils DaRT à distance sur un ordinateur d’utilisateur final. Lorsque l’utilisateur final fournit à l’administrateur ou au service de support technique des informations spécifiques, l’administrateur informatique ou le service de support technique peut prendre le contrôle de l’ordinateur de l’utilisateur final et exécuter les outils DaRT nécessaires à distance.

Si vous avez désactivé les outils DaRT lors de la création de l’image de récupération, vous avez toujours accès à tous les outils. L’ensemble des outils, à l’exception de la connexion à distance, ne sont pas disponibles pour les utilisateurs finaux.

**Pour récupérer un ordinateur distant à l’aide de l’image de récupération DaRT**

1.  Démarrez un ordinateur utilisateur final en utilisant l’image de récupération DaRT.

    En règle générale, vous devez utiliser l’une des méthodes suivantes pour démarrer dans DaRT afin de récupérer un ordinateur distant, selon la manière dont vous déployez l’image de récupération DaRT. Pour plus d’informations sur le déploiement de l’image de récupération DaRT, voir [déploiement de dart 8,0](deploying-dart-80-dart-8.md).

    -   Démarrez dans DaRT à partir d’une partition de récupération sur l’ordinateur qui pose problème.

    -   Démarrez dans DaRT à partir d’une partition distante sur le réseau.

    Pour plus d’informations sur les avantages et inconvénients de chaque méthode, voir [planification de l’enregistrement et du déploiement de l’image de récupération 8,0 de DART](planning-how-to-save-and-deploy-the-dart-80-recovery-image-dart-8.md).

    Quelle que soit la méthode que vous utilisez pour démarrer dans DaRT, vous devez activer le périphérique de démarrage dans le BIOS pour l’option de démarrage ou les options que vous voulez mettre à disposition de l’utilisateur final.

    **Remarque**  
    La configuration du BIOS est unique, en fonction du type de disque dur, de cartes réseau et d’autres éléments utilisés au sein de votre organisation.



~~~
As the computer is booting into the DaRT recovery image, the **NetStart** dialog box appears.
~~~

2. Lorsque le système vous demande si vous souhaitez initialiser les services réseau, sélectionnez l’une des options suivantes:

   **Oui** -il est supposé qu’un serveur DHCP est présent sur le réseau et une tentative d’obtention d’une adresse IP du serveur est effectuée. Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.

   **Non** -ignorer le processus d’initialisation du réseau.

3. Indiquez si vous souhaitez remapper les lettres de lecteur. Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion. Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne. Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.

4. Dans la boîte de dialogue **options de récupération du système** , sélectionnez une disposition de clavier.

5. Vérifiez le répertoire racine du système affiché, le type de système d’exploitation installé et la taille de partition. Si vous ne voyez pas votre système d’exploitation et suspectez l’absence de pilotes dans le cas contraire, cliquez sur **charger les pilotes** pour charger les pilotes suspects, puis insérez le support d’installation de l’appareil et sélectionnez le pilote.

6. Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.

   **Remarque**  
   Si l’environnement de récupération Windows (WinRE) détecte un problème ou s’il suspect que Windows 8 ne démarrait pas correctement la dernière fois qu’il a été essayé, l' **outil de réparation du démarrage** peut commencer à s’exécuter automatiquement. Pour plus d’informations sur la façon de résoudre ce problème, reportez-vous à la rubrique [résolution des problèmes DaRT 8,0](troubleshooting-dart-80-dart-8.md).



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft** pour ouvrir les **outils de diagnostics et de récupération**.

8. Dans la fenêtre **jeu d’outils de diagnostics et de récupération** , cliquez sur **connexion à distance** pour ouvrir la fenêtre de **connexion à distance DART** . Si vous êtes invité à fournir l’accès distant au support technique, cliquez sur **OK**.

   La fenêtre de connexion à distance DaRT s’ouvre et affiche un numéro de ticket, une adresse IP et des informations de port.

9. Sur l’ordinateur du support technique, ouvrez la **visionneuse de connexion à distance DART**.

10. Cliquez sur **Démarrer**, sur **tous les programmes**, sur **Microsoft DART 8,0**, puis sur **visionneuse de connexions à distance DART**.

11. Dans la fenêtre de **connexion à distance de DART** , entrez les informations requises sur le ticket, l’adresse IP et le port.

   **Remarque**  
   Ces informations sont créées sur l’ordinateur de l’utilisateur final et doivent être fournies par l’utilisateur final. Plusieurs adresses IP peuvent être proposées, en fonction du nombre de personnes disponibles sur l’ordinateur de l’utilisateur final.



12. Cliquez sur **Se connecter**.

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

Lorsque DaRT démarre, il crée le fichier inv32.xml dans \\Windows\\System32\\ sur le disque RAM. Ce fichier contient des informations de connexion: adresse IP, port et numéro de ticket. Vous pouvez copier ce fichier sur un partage réseau pour déclencher un flux de travail de support technique. Par exemple, un programme personnalisé peut vérifier le partage réseau pour les fichiers de connexion, puis créer un ticket de support ou envoyer des notifications par courrier électronique.

**Pour exécuter la visionneuse de connexions à distance à l’invite de commandes**

1.  Pour exécuter la **visionneuse de connexions à distance DART** à l’invite de commandes, spécifiez la commande **DartRemoteViewer.exe** et utilisez les paramètres suivants:

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


[Opérations de DaRT8.0](operations-for-dart-80-dart-8.md)

[Récupération des ordinateurs à l'aide de DaRT8.0](recovering-computers-using-dart-80-dart-8.md)









