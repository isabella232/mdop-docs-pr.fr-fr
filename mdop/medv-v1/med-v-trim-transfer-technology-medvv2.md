---
title: Technologie de transfert de découpage MED-V
description: Technologie de transfert de découpage MED-V
author: dansimp
ms.assetid: 2744e855-a486-4028-9606-f0084794ec65
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: fa11c8036954070bbff465a6ad78992fdd52f3a2
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811604"
---
# Technologie de transfert de découpage MED-V


## <a href="" id="bkmk-medvtrimtransfertechnology"></a>


La technologie de déduplication avancée de MED-V accélère le téléchargement d’images virtuelles d’machines virtuelles sur le réseau local (LAN) ou sur réseau étendu (WAN), ce qui permet de réduire la bande passante réseau nécessaire au transfert d’une machine virtuelle d’espace de travail MED-V vers plusieurs utilisateurs finaux.

Cette technologie avancée utilise des données locales existantes pour générer l’image de l’ordinateur virtuel, en tirant parti du fait que, dans de nombreux cas, la majeure partie de l’ordinateur virtuel (par exemple, les fichiers système et d’application) existe déjà sur le disque de l’utilisateur final. Par exemple, si un ordinateur virtuel contenant WindowsXP est remis à un client exécutant une copie locale de WindowsXP, MED-V supprime automatiquement les éléments WindowsXP redondants du transfert. Pour garantir un espace de travail valide et fonctionnel, le client MED-V vérifie l’intégrité des données locales avant qu’elle ne soit utilisée, ce qui permet de garantir que les blocs de données locaux constituent une version de bit absolument identique à celle de l’image de l’ordinateur virtuel souhaité. Les blocs qui ne correspondent pas sont utilisés.

Le processus est économe en bande passante et transparente, et les transferts s’exécutent en arrière-plan, à l’aide de ressources réseau et processeur inutilisées.

Lors de la mise à jour vers une nouvelle version d’image (par exemple, lorsque les administrateurs souhaitent distribuer une nouvelle application ou un nouveau correctif), seuls les éléments qui ont changé («Delta») sont téléchargés, et non la totalité de l’ordinateur virtuel, réduisant considérablement le temps de bande passante et de remise réseau requis.

Vous pouvez configurer les dossiers indexés sur l’hôte dans le cadre du protocole de transfert de découpage, en fonction du système d’exploitation hôte. Ces paramètres sont configurés dans le fichier *ClientSettings.xml* , qui se trouve dans le dossier **Servers\\Configuration Server\\** .

Le service doit être redémarré lors de l’application de nouveaux paramètres.

```xml
<HostIndexingXP type="System.String[]"> 
- <ArrayOfString>
<string>%WINDIR%</string> 
<string>%ProgramFiles%\Common Files</string> 
<string>%ProgramFiles%\Internet Explorer</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
<string>%ProgramFiles%\Windows NT</string> 
<string>%ProgramFiles%\Messenger</string> 
<string>%ProgramFiles%\Adobe</string> 
<string>%ProgramFiles%\Outlook Express</string> 
</ArrayOfString> 
</HostIndexingXP> 
- <HostIndexingVista type="System.String[]"> 
- <ArrayOfString> 
<string>%WINDIR%\MSAgent</string> 
<string>%WINDIR%\winsxs</string> 
<string>%WINDIR%\system</string> 
<string>%WINDIR%\system32</string> 
<string>%WINDIR%\Microsoft.NET</string> 
<string>%WINDIR%\SoftwareDistribution</string> 
<string>%WINDIR%\L2Schemas</string> 
<string>%WINDIR%\Cursors</string> 
<string>%WINDIR%\Boot</string> 
<string>%WINDIR%\Help</string> 
<string>%WINDIR%\assembly</string> 
<string>%WINDIR%\inf</string> 
<string>%WINDIR%\fonts</string> 
<string>%WINDIR%\Installer</string> 
<string>%WINDIR%\IME</string> 
<string>%WINDIR%\Resources</string> 
<string>%WINDIR%\servicing</string> 
<string>%ProgramFiles%\MED-V</string> 
<string>%ProgramFiles%\Microsoft Office</string> 
</ArrayOfString> 
</HostIndexingVista>
```

 

 





