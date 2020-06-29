---
title: Procédure pour configurer le Pare-feu Windows Server2008 pour App-V
description: Procédure pour configurer le Pare-feu Windows Server2008 pour App-V
author: dansimp
ms.assetid: 57f4ed17-0651-4a3c-be1e-29d9520c6aeb
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 19e4cda9ac3b908f68e4f69b9663033d8a21ae41
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807218"
---
# Procédure pour configurer le Pare-feu Windows Server2008 pour App-V


Avec l’introduction de Windows Server 2008, le pare-feu et les composants IPsec ont été fusionnés en un seul service, et les fonctionnalités de ce service ont été améliorées. Le nouveau service de pare-feu prend en charge l’inspection par État en entrée et en sortie. Par ailleurs, vous pouvez configurer des règles de pare-feu et des stratégies IPsec spécifiques par le biais de stratégies de groupe. Pour plus d’informations sur le pare-feu Windows dans Windows Server 2008, voir <https://go.microsoft.com/fwlink/?LinkId=151980> .

La procédure suivante n’inclut pas l’ajout d’une exception pour la publication de l’OSD et de l’OSD via SMB ou HTTP/HTTPs. Ces exceptions sont automatiquement ajoutées en fonction du profil réseau et des rôles installés sur le pare-feu Windows Server 2008.

**Remarques**  Si le serveur de gestion est configuré pour utiliser RTSP, répétez cette procédure pour ajouter le `sghwsvr.exe` programme en tant qu’exception.

Le serveur de streaming App-V nécessite l’exception `sglwdsptr.exe` de programme pour la communication RTSP. Un serveur de streaming App-V qui utilise RTSP pour la communication nécessite également une exception de programme pour `sglwsvr.exe` .

 

**Pour configurer le pare-feu Windows Server 2008 pour App-V**

1.  Ouvrez le **pare-feu Windows avec Advanced Security** Management Console via le panneau de configuration ou en `wf.msc` le tapant dans la ligne d’exécution.

2.  Créez une nouvelle règle de trafic entrant, puis sélectionnez **programme**.

3.  Sélectionnez le chemin du programme et naviguez jusqu’à `sghwdsptr.exe` , qui se trouve par défaut à `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .

4.  Cliquez sur **Suivant**.

5.  Dans la page **action** , sélectionnez **autoriser la connexion**, puis cliquez sur **suivant**.

6.  Sélectionnez les **profils** appropriés à appliquer à la règle de trafic entrant.

7.  Entrez le nom et la description de la règle, puis cliquez sur **Terminer**.

## Rubriques connexes


[Procédure pour configurer le Pare-feu Windows Server2003 pour App-V](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





