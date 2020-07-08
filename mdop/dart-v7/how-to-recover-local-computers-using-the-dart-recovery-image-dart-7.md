---
title: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: be29b5a8-be08-4cf2-822e-77a51d3f3b65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 4c605db895b5ea812d90db51d3c2de9653e2dd2d
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810151"
---
# Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT


Pour récupérer un ordinateur local à l’aide de Microsoft Diagnostics et Recovery Tools Tools (DaRT) 7, vous devez avoir une présentation physique de l’ordinateur de l’utilisateur final rencontrant des problèmes qui nécessitent DaRT. Vous pouvez également exécuter DaRT à distance en suivant les instructions de la [procédure de récupération d’ordinateurs distants à l’aide de l’image de récupération DART](how-to-recover-remote-computers-using-the-dart-recovery-image-dart-7.md).

**Pour récupérer un ordinateur local à l’aide de DaRT**

1.  Au démarrage de l’ordinateur dans l’image de récupération DaRT, la boîte de dialogue **netstart** s’affiche. Vous êtes invité à indiquer si vous souhaitez initialiser les services réseau. Si vous cliquez sur **Oui**, on suppose qu’un serveur DHCP est présent sur le réseau et qu’une tentative d’obtention d’une adresse IP du serveur est effectuée. Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.

    Pour ignorer le processus d’initialisation du réseau, cliquez sur **non**.

2.  Après la boîte de dialogue initialisation du réseau, vous êtes invité à indiquer si vous souhaitez remapper les lettres de lecteur. Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion. Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne. Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.

3.  Après la boîte de dialogue remappage, une boîte de dialogue **options de récupération du système** s’affiche et vous invite à sélectionner une disposition de clavier. Il affiche ensuite le répertoire racine du système, le type de système d’exploitation installé et la taille de partition. Si vous ne voyez pas votre système d’exploitation et que vous suspectez qu’il n’y a pas de problème, cliquez sur **charger des pilotes** pour charger les pilotes suspects. Vous êtes alors invité à insérer le média d’installation pour l’appareil et à sélectionner le pilote. Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.

    **Remarque**  
    Si l’environnement de récupération Windows (WinRE) détecte ou suspecte que Windows 7 ne démarrait pas correctement la dernière fois qu’il a été essayé, la **réparation du démarrage** peut commencer à s’exécuter automatiquement.



~~~
If any of the registry hives are corrupted or missing, Registry Editor, and several other DaRT utilities, will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

4. Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft**.

   La fenêtre du **jeu d’outils de diagnostics et de récupération** s’ouvre. Vous pouvez désormais exécuter tous les outils ou assistants proposés lors de la création de l’image de récupération DaRT.

Vous pouvez cliquer sur **aide** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour ouvrir le fichier d’aide du client qui fournit des instructions détaillées et des informations nécessaires à l’exécution des outils DART individuels. Vous pouvez également cliquer sur l' **Assistant solution** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour choisir l’outil le plus approprié pour la situation, en fonction d’un bref entretien que l’Assistant fournit.

Pour obtenir des informations générales sur l’un des outils DaRT, voir [vue d’ensemble des outils dans DaRT 7,0](overview-of-the-tools-in-dart-70-new-ia.md).

**Pour exécuter DaRT à l’invite de commandes**

1. Vous pouvez exécuter DaRT à l’invite de commandes en spécifiant la commande **netstart.exe** et en utilisant l’un des paramètres suivants:

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
   <td align="left"><p>-réseau</p></td>
   <td align="left"><p>Initialise les services réseau.</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>-remonter</p></td>
   <td align="left"><p>Remappez les lettres de lecteur.</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>-invite</p></td>
   <td align="left"><p>Affiche des messages demandant à l’utilisateur final de spécifier si le réseau doit être initialisé et remapper les lecteurs.</p>
   <div class="alert">
   <strong>Important</strong><br/><p>La réponse de l’utilisateur final aux invites remplace les commutateurs-réseau et-remontage.</p>
   </div>
   <div>

   </div></td>
   </tr>
   </tbody>
   </table>



2. Vous pouvez personnaliser DaRT de telle sorte qu’un ordinateur qui démarre sur DaRT ouvre automatiquement l’outil de **connexion à distance** qui est utilisé pour établir une connexion à distance avec l’assistance.

## Rubriques connexes


[Récupération des ordinateurs à l'aide de DaRT7.0](recovering-computers-using-dart-70-dart-7.md)









