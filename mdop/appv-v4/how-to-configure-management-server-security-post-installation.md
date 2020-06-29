---
title: Procédure pour configurer la sécurité post-installation de Management Server
description: Procédure pour configurer la sécurité post-installation de Management Server
author: dansimp
ms.assetid: 71979fa6-3d0b-4a8b-994e-cb728d013090
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 521e72ead78055a7d3261664ccb75d454c22e622
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807306"
---
# <span data-ttu-id="f77af-103">Procédure pour configurer la sécurité post-installation de Management Server</span><span class="sxs-lookup"><span data-stu-id="f77af-103">How to Configure Management Server Security Post-Installation</span></span>


<span data-ttu-id="f77af-104">Utilisez la console de gestion App-V pour ajouter le certificat et configurer le serveur de gestion App-V pour une sécurité renforcée.</span><span class="sxs-lookup"><span data-stu-id="f77af-104">Use the App-V Management Console to add the certificate and configure the App-V Management Server for enhanced security.</span></span> <span data-ttu-id="f77af-105">Vous pouvez utiliser la procédure suivante pour configurer la sécurité après l’installation.</span><span class="sxs-lookup"><span data-stu-id="f77af-105">You can use the following procedure to configure security post-installation.</span></span>

**<span data-ttu-id="f77af-106">Pour configurer la sécurité du serveur de gestion après l’installation</span><span class="sxs-lookup"><span data-stu-id="f77af-106">To configure Management Server security post-installation</span></span>**

1.  <span data-ttu-id="f77af-107">Ouvrez la console de gestion App-V, puis connectez-vous au **service de gestion** avec les privilèges d’administrateur d’application-v.</span><span class="sxs-lookup"><span data-stu-id="f77af-107">Open the App-V Management Console, and connect to the **Management Service** with App-V administrator privileges.</span></span>

2.  <span data-ttu-id="f77af-108">Développez le serveur, développez **groupes de serveurs**, puis sélectionnez le groupe de serveurs approprié avec lequel le serveur de gestion a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="f77af-108">Expand the server, expand **Server Groups**, and then select the appropriate server group with which the Management Server was registered.</span></span>

3.  <span data-ttu-id="f77af-109">Cliquez avec le bouton droit sur l’objet serveur de gestion, puis sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f77af-109">Right-click the Management Server object, and select **Properties**.</span></span>

4.  <span data-ttu-id="f77af-110">Dans l’onglet **ports** , cliquez sur **certificat de serveur** , puis terminez l’Assistant pour sélectionner le certificat configuré correctement.</span><span class="sxs-lookup"><span data-stu-id="f77af-110">On the **Ports** tab, click **Server Certificate** and complete the wizard to select the properly provisioned certificate.</span></span>

    <span data-ttu-id="f77af-111">**Remarques**  Si aucun certificat n’est affiché dans l’Assistant, un certificat n’a pas été approvisionné ou le certificat répond aux exigences de App-V.</span><span class="sxs-lookup"><span data-stu-id="f77af-111">**Note** If no certificates are displayed in the wizard, a certificate has not been provisioned or the certificate does meet the requirements of App-V.</span></span>

     

5.  <span data-ttu-id="f77af-112">Cliquez sur **suivant** pour passer à la page de l' **Assistant Bienvenue** sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="f77af-112">Click **Next** to continue on to the **Welcome To Certificate Wizard** page.</span></span>

6.  <span data-ttu-id="f77af-113">Sélectionnez le certificat approprié dans l’écran **certificats disponibles** .</span><span class="sxs-lookup"><span data-stu-id="f77af-113">Select the correct certificate in the **Available Certificates** screen.</span></span>

7.  <span data-ttu-id="f77af-114">Cliquez sur **Terminer**.</span><span class="sxs-lookup"><span data-stu-id="f77af-114">Click **Finish**.</span></span>

8.  <span data-ttu-id="f77af-115">Une fois l’Assistant terminé, effacez **RTSP** comme port d’écoute disponible.</span><span class="sxs-lookup"><span data-stu-id="f77af-115">After completing the wizard, clear **RTSP** as an available listening port.</span></span> <span data-ttu-id="f77af-116">Cela empêche les connexions d’être effectuées via un canal de communication non sécurisé.</span><span class="sxs-lookup"><span data-stu-id="f77af-116">This prevents connections from being made over a non-secure communication channel.</span></span>

9.  <span data-ttu-id="f77af-117">Cliquez sur **appliquer**, puis redémarrez le service **serveur d’applications virtuelles Microsoft** .</span><span class="sxs-lookup"><span data-stu-id="f77af-117">Click **Apply**, and restart the **Microsoft Virtual Application Server** service.</span></span> <span data-ttu-id="f77af-118">Pour effectuer cette tâche, utilisez le composant logiciel enfichable MMC du service.</span><span class="sxs-lookup"><span data-stu-id="f77af-118">Use the service’s MMC snap-in to accomplish this task.</span></span>

## <span data-ttu-id="f77af-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f77af-119">Related topics</span></span>


[<span data-ttu-id="f77af-120">Procédure pour configurer la sécurité post-installation de Streaming Server</span><span class="sxs-lookup"><span data-stu-id="f77af-120">How to Configure Streaming Server Security Post-Installation</span></span>](how-to-configure-streaming-server-security-post-installation.md)

[<span data-ttu-id="f77af-121">Résolution des problèmes d'autorisation de certificat</span><span class="sxs-lookup"><span data-stu-id="f77af-121">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





