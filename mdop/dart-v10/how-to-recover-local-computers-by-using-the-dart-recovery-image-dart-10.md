---
title: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
description: Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT
author: dansimp
ms.assetid: a6adc717-827c-45e8-b9c3-06d0e919e0bd
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: support
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 06e8ad82f869568c9fa25fcbb16825b2abff06f1
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809444"
---
# Procédure pour récupérer des ordinateurs locaux à l'aide de l'image de récupération DaRT


Utilisez ces instructions pour récupérer un ordinateur en cours de présentation physique sur l’ordinateur de l’utilisateur final qui rencontre des problèmes.

**Récupération d’un ordinateur local à l’aide de l’image de récupération DaRT**

1.  Démarrez l’ordinateur de l’utilisateur final à l’aide de l’image de récupération Microsoft Diagnostics and Recovery Tools (DaRT) 10.

    Au démarrage de l’ordinateur dans l’image de récupération de DaRT 10, la boîte de dialogue de **démarrage** automatique s’affiche.

2.  Lorsque le système vous demande si vous souhaitez initialiser les services réseau, sélectionnez l’une des options suivantes:

    **Oui** -il est supposé qu’un serveur DHCP est présent sur le réseau et une tentative d’obtention d’une adresse IP du serveur est effectuée. Si le réseau utilise des adresses IP statiques au lieu de DHCP, vous pouvez utiliser l’outil de **configuration TCP/IP** dans DART pour spécifier une adresse IP statique.

    **Non** -ignorer le processus d’initialisation du réseau.

3.  Indiquez si vous souhaitez remapper les lettres de lecteur. Lorsque vous exécutez Windows en ligne, le volume système est généralement mappé au lecteur C. Toutefois, lorsque vous exécutez Windows Offline sous WinRE, le volume système d’origine peut être mappé sur un autre lecteur, ce qui peut entraîner une confusion. Si vous décidez de remapper, DaRT tente de mapper les lettres du lecteur hors ligne pour correspondre aux lettres de lecteur en ligne. Le remappage est effectué uniquement si un système d’exploitation hors connexion est sélectionné plus tard dans le processus de démarrage.

4.  Dans la boîte de dialogue **options de récupération du système** , sélectionnez une disposition de clavier.

5.  Vérifiez le répertoire racine du système affiché, le type de système d’exploitation installé et la taille de partition. Si vous ne voyez pas votre système d’exploitation et suspectez l’absence de pilotes dans le cas contraire, cliquez sur **charger les pilotes** pour charger les pilotes suspects, puis insérez le support d’installation de l’appareil et sélectionnez le pilote.

6.  Sélectionnez l’installation que vous voulez réparer ou diagnostiquer, puis cliquez sur **suivant**.

    **Remarque**  
    Si l’environnement de récupération Windows (WinRE) détecte un problème ou s’il suspect qu’il n’a pas démarré correctement le dernier **démarrage** de Windows 10, il est possible qu’il s’exécute automatiquement.



~~~
If any of the registry hives are corrupted or missing, Registry Editor and several other DaRT utilities will have limited functionality. If no operating system is selected, some tools will not be available.

The **System Recovery Options** window appears and lists various recovery tools.
~~~

7. Dans la fenêtre **options de récupération du système** , cliquez sur outils de **Diagnostics et de récupération Microsoft**.

   La fenêtre du **jeu d’outils de diagnostics et de récupération** s’ouvre. Vous pouvez désormais exécuter tous les outils ou assistants proposés lors de la création de l’image de récupération DaRT.

Vous pouvez cliquer sur **aide** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour ouvrir le fichier d’aide du client qui fournit des instructions détaillées et des informations nécessaires à l’exécution des outils DART individuels. Vous pouvez également cliquer sur l' **Assistant solution** dans la fenêtre **jeu d’outils de diagnostics et de récupération** pour choisir l’outil le plus approprié pour la situation, en fonction d’un bref entretien que l’Assistant fournit.

Pour obtenir des informations générales sur l’un des outils DaRT, voir [vue d’ensemble des outils dans DART 10](overview-of-the-tools-in-dart-10.md).

**Exécution de DaRT à l’invite de commandes**

- Pour exécuter DaRT à l’invite de commandes, spécifiez la commande **netstart.exe** puis utilisez l’un des paramètres suivants:

  <table>
  <colgroup>
  <col width="50%" />
  <col width="50%" />
  </colgroup>
  <tbody>
  <tr class="odd">
  <td align="left"><p><strong>Paramètre</strong></p></td>
  <td align="left"><p><strong>Description</strong></p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-réseau</p></td>
  <td align="left"><p>Initialise les services réseau.</p></td>
  </tr>
  <tr class="odd">
  <td align="left"><p>-remonter</p></td>
  <td align="left"><p>Remappez les lettres de lecteur.</p></td>
  </tr>
  <tr class="even">
  <td align="left"><p>-invite</p></td>
  <td align="left"><p>Affiche des messages demandant à l’utilisateur final de spécifier si le réseau doit être initialisé et remapper les lecteurs.</p>
  <div class="alert">
  <strong>Warning</strong><br/><p>La réponse de l’utilisateur final à l’invite a pour effet de remplacer les commutateurs-Network et – remount.</p>
  </div>
  <div>

  </div></td>
  </tr>
  </tbody>
  </table>



## Rubriques connexes


[Opérations de DaRT10](operations-for-dart-10.md)

[Récupération des ordinateurs à l'aide de DaRT10](recovering-computers-using-dart-10.md)









