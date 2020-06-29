---
title: Procédure pour installer le client App-V Client à l'aide de setup.exe
description: Procédure pour installer le client App-V Client à l'aide de setup.exe
author: dansimp
ms.assetid: 106a5d97-b5f6-4a16-bf52-a84f4d558c74
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 60f79a2d2f74848ab121ba13cdf8c215088d54db
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807066"
---
# Procédure pour installer le client App-V Client à l'aide de setup.exe


Cette rubrique explique comment installer le client App-V à l’aide du programme setup.exe. Lorsque vous installez le client App-V à l’aide du programme setup.exe, le programme d’installation détermine les logiciels requis requis et les installe automatiquement avant d’installer le client.

**Pour installer le client de virtualisation des applications à l’aide de Setup.exe**

1.  Vérifiez que vous êtes connecté avec un compte disposant de droits d’administrateur sur l’ordinateur.

2.  Ouvrez une fenêtre d’invite de commandes, puis modifiez le répertoire dans le dossier qui contient les fichiers d’installation. Lors de l’installation de la version 4.6 ou d’une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32 ou 64 bits. L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.

3.  Entrez la chaîne de commande d’installation à l’invite de commandes. Vous pouvez également créer un fichier de commandes et l’exécuter à partir de l’invite de commandes. Vous pouvez également utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter la commande.

4.  L’exemple de ligne de commande suivant montre comment setup.exe peut être utilisé avec plusieurs paramètres facultatifs. Pour plus d’informations sur ces paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).

    **"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10 240 \ \ "SWIPUBSVRDISPLAY = \ \" production System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""**

    **Important**  
    -   Les guillemets qui s’affichent dans la section «**/v**» doivent être considérés comme des caractères spéciaux et entrés avec un « **\\** » précédent. Les guillemets sont requis uniquement lorsque la valeur contient un espace; Toutefois, pour des fins de cohérence, toutes les instances de l’exemple précédent sont indiquées par des guillemets.

    -   Le caractère «» **%** doit être précédé du caractère «» dans «**% HomeDrive%**» **^** . Dans le cas contraire, l’interpréteur de commandes Windows définit la valeur sur celle de l’utilisateur qui exécute l’installation.

    -   Les commutateurs d' **InstallShield** **/s** et **/qn** sont nécessaires pour rendre cette installation silencieuse. Le commutateur **/qn** doit suivre le commutateur **/v** , en les séparant uniquement par un guillemet sans espaces intermédiaires.

    -   Le dossier spécifié dans la valeur **SWIGLOBALDATA** doit déjà exister.

     

5.  Lorsque l’installation est terminée, nous vous recommandons d’exécuter une analyse Microsoft Update pour vérifier que les mises à jour les plus récentes sont installées.

## Rubriques connexes


[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





