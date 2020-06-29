---
title: Configurer la sécurité de messagerie électronique pour AGPM
description: Configurer la sécurité de messagerie électronique pour AGPM
author: dansimp
ms.assetid: b9c48894-0a10-4d03-8027-50ed3b02485a
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop
ms.mktglfcycl: manage
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: a384c2a21f912ca7ec55a5e4c74ca7062bfe864c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807729"
---
# <span data-ttu-id="2734a-103">Configurer la sécurité de messagerie électronique pour AGPM</span><span class="sxs-lookup"><span data-stu-id="2734a-103">Configure E-Mail Security for AGPM</span></span>


<span data-ttu-id="2734a-104">Par défaut, les notifications par courrier électronique envoyées en raison d’actions dans la gestion de la stratégie de groupe avancée (AGPM) ne sont pas chiffrées et sont envoyées via le port SMTP 25.</span><span class="sxs-lookup"><span data-stu-id="2734a-104">By default, e-mail notifications sent because of actions in Advanced Group Policy Management (AGPM) are not encrypted and are sent through SMTP port 25.</span></span> <span data-ttu-id="2734a-105">Toutefois, vous pouvez configurer la sécurité de messagerie pour AGPM en utilisant des paramètres de Registre pour spécifier l’utilisation du chiffrement SSL (Secure Sockets Layer) et le port SMTP à utiliser.</span><span class="sxs-lookup"><span data-stu-id="2734a-105">However, you can configure e-mail security for AGPM by using registry settings to specify whether to use Secure Sockets Layer (SSL) encryption and which SMTP port to use.</span></span>

<span data-ttu-id="2734a-106">En chiffrant les notifications par courrier électronique AGPM, vous pouvez mieux protéger celles susceptibles de divulguer des informations sensibles sur la sécurité de votre organisation.</span><span class="sxs-lookup"><span data-stu-id="2734a-106">By encrypting AGPM e-mail notifications, you can better protect those that could reveal sensitive information about your organization’s security.</span></span> <span data-ttu-id="2734a-107">Le chiffrement des notifications par courrier électronique est recommandé quand ils sont relayés par le biais de serveurs de messagerie distants, et peuvent être requis par certains règlements de conformité.</span><span class="sxs-lookup"><span data-stu-id="2734a-107">Encrypting e-mail notifications is recommended when they are being relayed through remote mail servers, and may be required by some compliance regulations.</span></span>

<span data-ttu-id="2734a-108">**Attention**  La modification incorrecte du registre pourrait endommager sérieusement votre système.</span><span class="sxs-lookup"><span data-stu-id="2734a-108">**Caution** Incorrectly editing the registry may severely damage your system.</span></span> <span data-ttu-id="2734a-109">Avant d’apporter des modifications au registre, il est recommandé de sauvegarder toutes les données importantes de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2734a-109">Before making changes to the registry, you should back up any valued data on the computer.</span></span>

 

<span data-ttu-id="2734a-110">Un compte d’utilisateur ayant le rôle d’administrateur AGPM (contrôle total), le compte d’utilisateur de l’Approbateur ayant créé l’objet de stratégie de groupe (GPO) utilisé dans ces procédures, ou un compte d’utilisateur disposant des autorisations nécessaires dans AGPM est requis pour effectuer ces procédures.</span><span class="sxs-lookup"><span data-stu-id="2734a-110">A user account that has the AGPM Administrator (Full Control) role, the user account of the Approver who created the Group Policy Object (GPO) used in these procedures, or a user account that has the necessary permissions in AGPM is required to complete these procedures.</span></span> <span data-ttu-id="2734a-111">Passez en revue les détails dans «autres considérations» dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="2734a-111">Review the details in "Additional considerations" in this topic.</span></span>

**<span data-ttu-id="2734a-112">Pour configurer la sécurité de la messagerie électronique pour AGPM en utilisant les préférences de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="2734a-112">To configure e-mail security for AGPM by using Group Policy preferences</span></span>**

1.  <span data-ttu-id="2734a-113">Dans l’arborescence de la **console de gestion des stratégies de groupe** , modifiez un objet de stratégie de groupe qui s’applique à tous les serveurs AGPM pour lesquels vous souhaitez configurer la sécurité de messagerie électronique.</span><span class="sxs-lookup"><span data-stu-id="2734a-113">In the **Group Policy Management Console** tree, edit a GPO that is applied to all AGPM Servers for which you want to configure e-mail security.</span></span> <span data-ttu-id="2734a-114">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="2734a-114">(For more information, see [Editing a GPO](editing-a-gpo-agpm40.md).)</span></span>

2.  <span data-ttu-id="2734a-115">Dans la fenêtre **éditeur de gestion des stratégies de groupe** , développez la section Configuration de l' **ordinateur**, **Préférences**, **Paramètres Windows**et dossiers **du Registre** .</span><span class="sxs-lookup"><span data-stu-id="2734a-115">In the **Group Policy Management Editor** window, expand the **Computer Configuration**, **Preferences**, **Windows Settings**, and **Registry** folders.</span></span>

3.  <span data-ttu-id="2734a-116">Dans l’arborescence de la console, cliquez avec le bouton droit sur **Registre**, pointez sur **nouveau**, cliquez sur **élément de collection**et tapez **sécurité de messagerie électronique AGPM**.</span><span class="sxs-lookup"><span data-stu-id="2734a-116">In the console tree, right-click **Registry**, point to **New**, click **Collection Item**, and type **AGPM e-mail security**.</span></span>

4.  <span data-ttu-id="2734a-117">Créer un élément de préférence Registre pour activer le chiffrement:</span><span class="sxs-lookup"><span data-stu-id="2734a-117">Create a Registry preference item to turn on encryption:</span></span>

    1.  <span data-ttu-id="2734a-118">Dans l’arborescence de la console, cliquez avec le bouton droit sur **sécurité des messages AGPM**, pointez sur **nouveau**, puis cliquez sur **élément Registre**.</span><span class="sxs-lookup"><span data-stu-id="2734a-118">In the console tree, right-click **AGPM e-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="2734a-119">Dans la boîte de dialogue **nouvelles propriétés de Registre** , sélectionnez l’action **mettre à jour** .</span><span class="sxs-lookup"><span data-stu-id="2734a-119">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="2734a-120">Pour **Hive**, sélectionnez **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="2734a-120">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="2734a-121">Pour le **chemin d’accès**de la clé, tapez **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="2734a-121">For **Key Path**, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="2734a-122">Pour **nom**de la valeur, tapez **EncryptSmtp**.</span><span class="sxs-lookup"><span data-stu-id="2734a-122">For **Value name**, type **EncryptSmtp**.</span></span>

    6.  <span data-ttu-id="2734a-123">Pour **type de valeur**, sélectionnez **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2734a-123">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="2734a-124">Pour **base**, sélectionnez **décimal**, et pour les données de la **valeur**, tapez **1** pour utiliser le chiffrement SSL, ou **0** pour permettre l’envoi du courrier sans chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2734a-124">For **Base**, select **Decimal**, and for **Value data**, type **1** to use SSL encryption, or **0** to let e-mail to be sent without encryption.</span></span> <span data-ttu-id="2734a-125">Par défaut, le courrier électronique est envoyé sans chiffrement.</span><span class="sxs-lookup"><span data-stu-id="2734a-125">By default, e-mail is sent without encryption.</span></span> <span data-ttu-id="2734a-126">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2734a-126">Click **OK**.</span></span>

5.  <span data-ttu-id="2734a-127">Créer un élément de préférence Registre pour spécifier le port SMTP:</span><span class="sxs-lookup"><span data-stu-id="2734a-127">Create a Registry preference item to specify the SMTP port:</span></span>

    1.  <span data-ttu-id="2734a-128">Dans l’arborescence de la console, cliquez avec le bouton droit sur **sécurité des messages AGPM**, pointez sur **nouveau**, puis cliquez sur **élément Registre**.</span><span class="sxs-lookup"><span data-stu-id="2734a-128">In the console tree, right-click **AGPM E-mail security**, point to **New**, and then click **Registry Item**.</span></span>

    2.  <span data-ttu-id="2734a-129">Dans la boîte de dialogue **nouvelles propriétés de Registre** , sélectionnez l’action **mettre à jour** .</span><span class="sxs-lookup"><span data-stu-id="2734a-129">In the **New Registry Properties** dialog box, select the **Update** action.</span></span>

    3.  <span data-ttu-id="2734a-130">Pour **Hive**, sélectionnez **HKEY \ _LOCAL \ _MACHINE**.</span><span class="sxs-lookup"><span data-stu-id="2734a-130">For **Hive**, select **HKEY\_LOCAL\_MACHINE**.</span></span>

    4.  <span data-ttu-id="2734a-131">Dans la boîte de dialogue **chemin d’accès** de la clé, tapez **SOFTWARE\\Microsoft\\AGPM**.</span><span class="sxs-lookup"><span data-stu-id="2734a-131">For **Key Path** dialog box, type **SOFTWARE\\Microsoft\\AGPM**.</span></span>

    5.  <span data-ttu-id="2734a-132">Pour **nom**de la valeur, tapez **SmtpPort**.</span><span class="sxs-lookup"><span data-stu-id="2734a-132">For **Value name**, type **SmtpPort**.</span></span>

    6.  <span data-ttu-id="2734a-133">Pour **type de valeur**, sélectionnez **reg \ _DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2734a-133">For **Value type**, select **REG\_DWORD**.</span></span>

    7.  <span data-ttu-id="2734a-134">Pour **base**, sélectionnez **décimal**et pour les **données**de la valeur, tapez un numéro de port pour le port SMTP.</span><span class="sxs-lookup"><span data-stu-id="2734a-134">For **Base**, select **Decimal**, and for **Value data**, type a port number for the SMTP port.</span></span> <span data-ttu-id="2734a-135">Par défaut, le port SMTP est le port 25 si le chiffrement n’est pas activé ou le port 587 si le chiffrement SSL est activé.</span><span class="sxs-lookup"><span data-stu-id="2734a-135">By default, the SMTP port is port 25 if encryption is not enabled or port 587 if SSL encryption is enabled.</span></span> <span data-ttu-id="2734a-136">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="2734a-136">Click **OK**.</span></span>

6.  <span data-ttu-id="2734a-137">Fermez la fenêtre de l' **éditeur de gestion des stratégies de groupe** , puis archivez et déployez l’objet de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2734a-137">Close the **Group Policy Management Editor** window, and then check in and deploy the GPO.</span></span> <span data-ttu-id="2734a-138">Pour plus d’informations, consultez [la rubrique déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md).</span><span class="sxs-lookup"><span data-stu-id="2734a-138">For more information, see [Deploy a GPO](deploy-a-gpo-agpm40.md).</span></span>

### <span data-ttu-id="2734a-139">Autres éléments à prendre en considération</span><span class="sxs-lookup"><span data-stu-id="2734a-139">Additional considerations</span></span>

-   <span data-ttu-id="2734a-140">Vous devez être en mesure de modifier et de déployer un objet de stratégie de groupe pour configurer les paramètres du Registre à l’aide des préférences de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="2734a-140">You must be able to edit and deploy a GPO to configure registry settings by using Group Policy Preferences.</span></span> <span data-ttu-id="2734a-141">Pour plus d’informations, voir [modification d’un objet de stratégie de groupe](editing-a-gpo-agpm40.md) et [déploiement d’un objet de stratégie de groupe](deploy-a-gpo-agpm40.md)</span><span class="sxs-lookup"><span data-stu-id="2734a-141">See [Editing a GPO](editing-a-gpo-agpm40.md) and [Deploy a GPO](deploy-a-gpo-agpm40.md) for additional detail.</span></span>

### <span data-ttu-id="2734a-142">Références supplémentaires</span><span class="sxs-lookup"><span data-stu-id="2734a-142">Additional references</span></span>

-   [<span data-ttu-id="2734a-143">Configuration de la Gestion avancée des stratégies de groupe</span><span class="sxs-lookup"><span data-stu-id="2734a-143">Configuring Advanced Group Policy Management</span></span>](configuring-advanced-group-policy-management-agpm40.md)

 

 





