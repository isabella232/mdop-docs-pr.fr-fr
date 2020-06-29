---
title: Procédure pour configurer la sécurité post-installation de Streaming Server
description: Procédure pour configurer la sécurité post-installation de Streaming Server
author: dansimp
ms.assetid: 9bde3677-d1aa-4dcc-904e-bb49a268d748
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: e1945b38da5dd50c0bd2fb0c741bd92012e78586
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807293"
---
# <span data-ttu-id="0ffd5-103">Procédure pour configurer la sécurité post-installation de Streaming Server</span><span class="sxs-lookup"><span data-stu-id="0ffd5-103">How to Configure Streaming Server Security Post-Installation</span></span>


<span data-ttu-id="0ffd5-104">Configurez le serveur de streaming App-V pour renforcer la sécurité par le biais du Registre.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-104">Configure the App-V Streaming Server for enhanced security through the registry.</span></span> <span data-ttu-id="0ffd5-105">Comme pour le serveur de gestion App-V, un certificat doit être correctement configuré avec l’identificateur EKU approprié pour l’authentification du serveur avant de terminer la procédure de post-installation suivante.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-105">As with the App-V Management Server, a certificate must be correctly provisioned with the correct EKU identifier for Server Authentication before you complete the following post-installation procedure.</span></span>

**<span data-ttu-id="0ffd5-106">Pour configurer la sécurité du serveur de diffusion après l’installation</span><span class="sxs-lookup"><span data-stu-id="0ffd5-106">To configure Streaming Server security post-installation</span></span>**

1.  <span data-ttu-id="0ffd5-107">Créez une console MMC, ajoutez le composant logiciel enfichable **certificats** et sélectionnez magasin de certificats de l' **ordinateur local**.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-107">Create an MMC, add the **Certificates** snap-in, and select **Local Machine certificate store**.</span></span>

2.  <span data-ttu-id="0ffd5-108">Ouvrez les certificats **personnels** pour l’ordinateur, puis ouvrez le certificat approvisionné pour App-V.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-108">Open the **Personal** certificates for the computer, and open the certificate provisioned for App-V.</span></span>

3.  <span data-ttu-id="0ffd5-109">Dans l’onglet **Détails** , faites défiler vers le bas jusqu’à l’empreinte numérique et copiez le hachage dans le volet Détails.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-109">On the **Details** tab, scroll down to the thumbprint and copy the hash in the details pane.</span></span>

4.  <span data-ttu-id="0ffd5-110">Ouvrez l’éditeur du Registre et naviguez jusqu’à `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server` .</span><span class="sxs-lookup"><span data-stu-id="0ffd5-110">Open the registry editor, and navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server`.</span></span>

5.  <span data-ttu-id="0ffd5-111">Modifiez la `X509CertHash` valeur, collez le hachage de l’empreinte numérique dans le champ valeur et supprimez tous les espaces.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-111">Edit the `X509CertHash` value, paste the thumbprint hash in the value field, and remove all spaces.</span></span> <span data-ttu-id="0ffd5-112">Cliquez sur **OK** pour accepter la modification.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-112">Click **OK** to accept the edit.</span></span>

6.  <span data-ttu-id="0ffd5-113">Dans l’éditeur du Registre, accédez à `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts` .</span><span class="sxs-lookup"><span data-stu-id="0ffd5-113">In the registry editor, navigate to `HKLM\Software\Microsoft\SoftGrid\4.5\Distribution server\RtspsPorts`.</span></span>

7.  <span data-ttu-id="0ffd5-114">Créez une nouvelle valeur **DWORD** nommée «322», puis entrez la valeur décimale 322 ou la valeur hexadécimale 142.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-114">Create a new **DWORD** value named "322," and then enter the decimal value as 322 or the hexadecimal value as 142.</span></span>

8.  <span data-ttu-id="0ffd5-115">Redémarrez le service de diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="0ffd5-115">Restart the streaming service.</span></span>

## <span data-ttu-id="0ffd5-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ffd5-116">Related topics</span></span>


[<span data-ttu-id="0ffd5-117">Procédure pour configurer la sécurité post-installation de Management Server</span><span class="sxs-lookup"><span data-stu-id="0ffd5-117">How to Configure Management Server Security Post-Installation</span></span>](how-to-configure-management-server-security-post-installation.md)

[<span data-ttu-id="0ffd5-118">Résolution des problèmes d'autorisation de certificat</span><span class="sxs-lookup"><span data-stu-id="0ffd5-118">Troubleshooting Certificate Permission Issues</span></span>](troubleshooting-certificate-permission-issues.md)

 

 





