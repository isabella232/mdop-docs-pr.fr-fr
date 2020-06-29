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
# <span data-ttu-id="cd73a-103">Procédure pour installer le client App-V Client à l'aide de setup.exe</span><span class="sxs-lookup"><span data-stu-id="cd73a-103">How to Install the App-V Client by Using Setup.exe</span></span>


<span data-ttu-id="cd73a-104">Cette rubrique explique comment installer le client App-V à l’aide du programme setup.exe.</span><span class="sxs-lookup"><span data-stu-id="cd73a-104">This topic describes how to install the App-V client by using the setup.exe program.</span></span> <span data-ttu-id="cd73a-105">Lorsque vous installez le client App-V à l’aide du programme setup.exe, le programme d’installation détermine les logiciels requis requis et les installe automatiquement avant d’installer le client.</span><span class="sxs-lookup"><span data-stu-id="cd73a-105">When you install the App-V client using the setup.exe program, the installer determines which prerequisite software is needed and installs it automatically before it installs the client.</span></span>

**<span data-ttu-id="cd73a-106">Pour installer le client de virtualisation des applications à l’aide de Setup.exe</span><span class="sxs-lookup"><span data-stu-id="cd73a-106">To install the Application Virtualization Client by Using Setup.exe</span></span>**

1.  <span data-ttu-id="cd73a-107">Vérifiez que vous êtes connecté avec un compte disposant de droits d’administrateur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="cd73a-107">Make sure you are logged on with an account that has administrator rights on the computer.</span></span>

2.  <span data-ttu-id="cd73a-108">Ouvrez une fenêtre d’invite de commandes, puis modifiez le répertoire dans le dossier qui contient les fichiers d’installation.</span><span class="sxs-lookup"><span data-stu-id="cd73a-108">Open a Command Prompt window, and then change the directory to the folder that contains the setup files.</span></span> <span data-ttu-id="cd73a-109">Lors de l’installation de la version 4.6 ou d’une version ultérieure du client App-V, vous devez utiliser le programme d’installation approprié pour le système d’exploitation de l’ordinateur, 32 ou 64 bits.</span><span class="sxs-lookup"><span data-stu-id="cd73a-109">When installing version4.6 or a later version of the App-V client, you must use the correct installer for the computer’s operating system, 32-bit or 64-bit.</span></span> <span data-ttu-id="cd73a-110">L’installation échoue et un message d’erreur s’affiche si vous utilisez le mauvais programme d’installation.</span><span class="sxs-lookup"><span data-stu-id="cd73a-110">The installation will fail and an error message will be displayed if you use the wrong installer.</span></span>

3.  <span data-ttu-id="cd73a-111">Entrez la chaîne de commande d’installation à l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="cd73a-111">Enter the install command string at the command prompt.</span></span> <span data-ttu-id="cd73a-112">Vous pouvez également créer un fichier de commandes et l’exécuter à partir de l’invite de commandes.</span><span class="sxs-lookup"><span data-stu-id="cd73a-112">Alternatively, you can create a command file and run it from the command prompt.</span></span> <span data-ttu-id="cd73a-113">Vous pouvez également utiliser un langage de script tel que VBScript ou Windows PowerShell pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="cd73a-113">You can also use a scripting language such as VBScript or Windows PowerShell to run the command.</span></span>

4.  <span data-ttu-id="cd73a-114">L’exemple de ligne de commande suivant montre comment setup.exe peut être utilisé avec plusieurs paramètres facultatifs.</span><span class="sxs-lookup"><span data-stu-id="cd73a-114">The following command-line example shows how setup.exe can be used with a number of optional parameters.</span></span> <span data-ttu-id="cd73a-115">Pour plus d’informations sur ces paramètres, voir [paramètres de ligne de commande du programme de virtualisation des applications](application-virtualization-client-installer-command-line-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="cd73a-115">For more information about these parameters, see [Application Virtualization Client Installer Command-Line Parameters](application-virtualization-client-installer-command-line-parameters.md).</span></span>

    **<span data-ttu-id="cd73a-116">"setup.exe"/s/v "/qn SWICACHESIZE = \ \" 10 240 \ \ "SWIPUBSVRDISPLAY = \ \" production System\\ "SWIPUBSVRTYPE = \ \" HTTP/secure\\ "SWIPUBSVRHOST = \ \" PRODSYS\\ "SWIPUBSVRPORT = \ \" 443 \ \ "SWIPUBSVRPATH = \ \"/AppVirt/appsntype.xml \ \ "SWIPUBSVRREFRESH = \ \" on\\ "SWIGLOBALDATA = \ \" D:\\AppVirt\\Global\\ "SWIUSERDATA = \ \" ^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\ "SWIFSDRIVE = \ \" Q\\ ""</span><span class="sxs-lookup"><span data-stu-id="cd73a-116">"setup.exe" /s /v"/qn SWICACHESIZE=\\"10240\\" SWIPUBSVRDISPLAY=\\"Production System\\" SWIPUBSVRTYPE=\\"HTTP /secure\\" SWIPUBSVRHOST=\\"PRODSYS\\" SWIPUBSVRPORT=\\"443\\" SWIPUBSVRPATH=\\"/AppVirt/appsntype.xml\\" SWIPUBSVRREFRESH=\\"on\\" SWIGLOBALDATA=\\"D:\\AppVirt\\Global\\" SWIUSERDATA=\\"^% LOCALAPPDATA ^%\\Windows\\Application Virtualization Client\\" SWIFSDRIVE=\\"Q\\""</span></span>**

    **<span data-ttu-id="cd73a-117">Important</span><span class="sxs-lookup"><span data-stu-id="cd73a-117">Important</span></span>**  
    -   <span data-ttu-id="cd73a-118">Les guillemets qui s’affichent dans la section «**/v**» doivent être considérés comme des caractères spéciaux et entrés avec un « **\\** » précédent.</span><span class="sxs-lookup"><span data-stu-id="cd73a-118">The quotation marks that appear in the "**/v**" section must be treated as special characters and entered with a preceding "**\\**".</span></span> <span data-ttu-id="cd73a-119">Les guillemets sont requis uniquement lorsque la valeur contient un espace; Toutefois, pour des fins de cohérence, toutes les instances de l’exemple précédent sont indiquées par des guillemets.</span><span class="sxs-lookup"><span data-stu-id="cd73a-119">The quotation marks are required only when the value contains a space; however, for consistency, all the instances in the preceding example are shown as having quotation marks.</span></span>

    -   <span data-ttu-id="cd73a-120">Le caractère «» **%** doit être précédé du caractère «» dans «**% HomeDrive%**» **^** .</span><span class="sxs-lookup"><span data-stu-id="cd73a-120">The "**%**" characters in "**%HomeDrive%**" must be preceded by the "**^**" escape character.</span></span> <span data-ttu-id="cd73a-121">Dans le cas contraire, l’interpréteur de commandes Windows définit la valeur sur celle de l’utilisateur qui exécute l’installation.</span><span class="sxs-lookup"><span data-stu-id="cd73a-121">Otherwise, the Windows command shell sets the value to that of the user who is performing the installation.</span></span>

    -   <span data-ttu-id="cd73a-122">Les commutateurs d' **InstallShield** **/s** et **/qn** sont nécessaires pour rendre cette installation silencieuse.</span><span class="sxs-lookup"><span data-stu-id="cd73a-122">The **InstallShield** switches **/s** and **/qn** are needed to make this a silent install.</span></span> <span data-ttu-id="cd73a-123">Le commutateur **/qn** doit suivre le commutateur **/v** , en les séparant uniquement par un guillemet sans espaces intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="cd73a-123">The **/qn** switch must follow the **/v** switch, separated by only a quote character with no intervening spaces.</span></span>

    -   <span data-ttu-id="cd73a-124">Le dossier spécifié dans la valeur **SWIGLOBALDATA** doit déjà exister.</span><span class="sxs-lookup"><span data-stu-id="cd73a-124">The folder specified in the **SWIGLOBALDATA** value must already exist.</span></span>

     

5.  <span data-ttu-id="cd73a-125">Lorsque l’installation est terminée, nous vous recommandons d’exécuter une analyse Microsoft Update pour vérifier que les mises à jour les plus récentes sont installées.</span><span class="sxs-lookup"><span data-stu-id="cd73a-125">When the installation is complete, we recommend that you run a Microsoft Update scan to ensure the latest updates are installed.</span></span>

## <span data-ttu-id="cd73a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd73a-126">Related topics</span></span>


[<span data-ttu-id="cd73a-127">Procédure pour installer le client via la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="cd73a-127">How to Install the Client by Using the Command Line</span></span>](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





