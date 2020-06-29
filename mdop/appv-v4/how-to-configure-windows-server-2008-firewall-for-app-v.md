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
# <span data-ttu-id="437fa-103">Procédure pour configurer le Pare-feu Windows Server2008 pour App-V</span><span class="sxs-lookup"><span data-stu-id="437fa-103">How to Configure Windows Server 2008 Firewall for App-V</span></span>


<span data-ttu-id="437fa-104">Avec l’introduction de Windows Server 2008, le pare-feu et les composants IPsec ont été fusionnés en un seul service, et les fonctionnalités de ce service ont été améliorées.</span><span class="sxs-lookup"><span data-stu-id="437fa-104">With the introduction of Windows Server2008, the firewall and IPsec components were merged into one service, and the capabilities of this service were enhanced.</span></span> <span data-ttu-id="437fa-105">Le nouveau service de pare-feu prend en charge l’inspection par État en entrée et en sortie.</span><span class="sxs-lookup"><span data-stu-id="437fa-105">The new firewall service supports incoming and outgoing stateful inspection.</span></span> <span data-ttu-id="437fa-106">Par ailleurs, vous pouvez configurer des règles de pare-feu et des stratégies IPsec spécifiques par le biais de stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="437fa-106">Also, you can configure specific firewall rules and IPsec policies through group policies.</span></span> <span data-ttu-id="437fa-107">Pour plus d’informations sur le pare-feu Windows dans Windows Server 2008, voir <https://go.microsoft.com/fwlink/?LinkId=151980> .</span><span class="sxs-lookup"><span data-stu-id="437fa-107">For additional information about the Windows firewall in Windows Server2008, see <https://go.microsoft.com/fwlink/?LinkId=151980>.</span></span>

<span data-ttu-id="437fa-108">La procédure suivante n’inclut pas l’ajout d’une exception pour la publication de l’OSD et de l’OSD via SMB ou HTTP/HTTPs.</span><span class="sxs-lookup"><span data-stu-id="437fa-108">The following procedure does not include adding an exception for ICO and OSD publishing through SMB or HTTP/HTTPS.</span></span> <span data-ttu-id="437fa-109">Ces exceptions sont automatiquement ajoutées en fonction du profil réseau et des rôles installés sur le pare-feu Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="437fa-109">Those exceptions are automatically added based on the network profile and roles installed on the Windows Server 2008 firewall.</span></span>

<span data-ttu-id="437fa-110">**Remarques**  Si le serveur de gestion est configuré pour utiliser RTSP, répétez cette procédure pour ajouter le `sghwsvr.exe` programme en tant qu’exception.</span><span class="sxs-lookup"><span data-stu-id="437fa-110">**Note** If the Management Server is configured to use RTSP, repeat this procedure to add the `sghwsvr.exe` program as an exception.</span></span>

<span data-ttu-id="437fa-111">Le serveur de streaming App-V nécessite l’exception `sglwdsptr.exe` de programme pour la communication RTSP.</span><span class="sxs-lookup"><span data-stu-id="437fa-111">The App-V Streaming Server requires the program exception `sglwdsptr.exe` for RTSPS communication.</span></span> <span data-ttu-id="437fa-112">Un serveur de streaming App-V qui utilise RTSP pour la communication nécessite également une exception de programme pour `sglwsvr.exe` .</span><span class="sxs-lookup"><span data-stu-id="437fa-112">An App-V Streaming Server that uses RTSP for communication also requires a program exception for `sglwsvr.exe`.</span></span>

 

**<span data-ttu-id="437fa-113">Pour configurer le pare-feu Windows Server 2008 pour App-V</span><span class="sxs-lookup"><span data-stu-id="437fa-113">To configure Windows Server2008 firewall for App-V</span></span>**

1.  <span data-ttu-id="437fa-114">Ouvrez le **pare-feu Windows avec Advanced Security** Management Console via le panneau de configuration ou en `wf.msc` le tapant dans la ligne d’exécution.</span><span class="sxs-lookup"><span data-stu-id="437fa-114">Open the **Windows Firewall with Advanced Security** management console through the Control Panel or by typing `wf.msc` on the Run line.</span></span>

2.  <span data-ttu-id="437fa-115">Créez une nouvelle règle de trafic entrant, puis sélectionnez **programme**.</span><span class="sxs-lookup"><span data-stu-id="437fa-115">Create a new inbound rule, and select **Program**.</span></span>

3.  <span data-ttu-id="437fa-116">Sélectionnez le chemin du programme et naviguez jusqu’à `sghwdsptr.exe` , qui se trouve par défaut à `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin` .</span><span class="sxs-lookup"><span data-stu-id="437fa-116">Select the program path, and browse to `sghwdsptr.exe`, which is located by default at `%ProgramFiles%\Microsoft System Center App Virt Management Server\App Virt Management Server\bin`.</span></span>

4.  <span data-ttu-id="437fa-117">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="437fa-117">Click **Next**.</span></span>

5.  <span data-ttu-id="437fa-118">Dans la page **action** , sélectionnez **autoriser la connexion**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="437fa-118">On the **Action** page, select **Allow the connection**, and then click **Next**.</span></span>

6.  <span data-ttu-id="437fa-119">Sélectionnez les **profils** appropriés à appliquer à la règle de trafic entrant.</span><span class="sxs-lookup"><span data-stu-id="437fa-119">Select the appropriate **Profiles** to apply to the inbound rule.</span></span>

7.  <span data-ttu-id="437fa-120">Entrez le nom et la description de la règle, puis cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="437fa-120">Provide a name and description for the rule, and click **Finish**.</span></span>

## <span data-ttu-id="437fa-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="437fa-121">Related topics</span></span>


[<span data-ttu-id="437fa-122">Procédure pour configurer le Pare-feu Windows Server2003 pour App-V</span><span class="sxs-lookup"><span data-stu-id="437fa-122">How to Configure Windows Server 2003 Firewall for App-V</span></span>](how-to-configure-windows-server-2003-firewall-for-app-v.md)

 

 





