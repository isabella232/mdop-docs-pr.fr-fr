---
title: À propos des paramètres de configuration du client
description: À propos des paramètres de configuration du client
author: dansimp
ms.assetid: cc7ae28c-b2ac-4f68-b992-5ccdbd5316a4
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 289f5b35ac223d488152ff7ee1f42b1cf50341df
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10806103"
---
# <span data-ttu-id="c3328-103">À propos des paramètres de configuration du client</span><span class="sxs-lookup"><span data-stu-id="c3328-103">About Client Configuration Settings</span></span>


<span data-ttu-id="c3328-104">Le client Microsoft Application Virtualization (App-V) 5,0 stocke sa configuration dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c3328-104">The Microsoft Application Virtualization (App-V) 5.0 client stores its configuration in the registry.</span></span> <span data-ttu-id="c3328-105">Vous pouvez recueillir des informations utiles sur le client si vous comprenez le format des données dans le registre.</span><span class="sxs-lookup"><span data-stu-id="c3328-105">You can gather some useful information about the client if you understand the format of data in the registry.</span></span> <span data-ttu-id="c3328-106">Vous pouvez également configurer de nombreuses actions client en modifiant des entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="c3328-106">You can also configure many client actions by changing registry entries.</span></span> <span data-ttu-id="c3328-107">Cette rubrique répertorie les paramètres de configuration du client App-V 5,0 et explique leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="c3328-107">This topic lists the App-V 5.0 Client configuration settings and explains their uses.</span></span> <span data-ttu-id="c3328-108">Vous pouvez utiliser PowerShell pour modifier les paramètres de configuration du client.</span><span class="sxs-lookup"><span data-stu-id="c3328-108">You can use PowerShell to modify the client configuration settings.</span></span> <span data-ttu-id="c3328-109">Pour plus d’informations sur l’utilisation des applications PowerShell et App-V 5,0, voir [administration de l’application-v à l’aide de PowerShell](administering-app-v-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="c3328-109">For more information about using PowerShell and App-V 5.0 see [Administering App-V by Using PowerShell](administering-app-v-by-using-powershell.md).</span></span>

## <a href="" id="---------app-v-5-0-client-configuration-settings"></a> <span data-ttu-id="c3328-110">Paramètres de configuration du client App-V 5,0</span><span class="sxs-lookup"><span data-stu-id="c3328-110">App-V 5.0 Client Configuration Settings</span></span>


<span data-ttu-id="c3328-111">Le tableau suivant contient des informations sur les paramètres de configuration du client App-V 5,0:</span><span class="sxs-lookup"><span data-stu-id="c3328-111">The following table displays information about the App-V 5.0 client configuration settings:</span></span>

<table style="width:100%;">
<colgroup>
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
<col width="16%" />
</colgroup>
<thead>
<tr class="header">
<th align="left"><span data-ttu-id="c3328-112">Nom du paramètre</span><span class="sxs-lookup"><span data-stu-id="c3328-112">Setting Name</span></span></th>
<th align="left"><span data-ttu-id="c3328-113">Indicateur de configuration</span><span class="sxs-lookup"><span data-stu-id="c3328-113">Setup Flag</span></span></th>
<th align="left"><span data-ttu-id="c3328-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3328-114">Description</span></span></th>
<th align="left"><span data-ttu-id="c3328-115">Définir des options</span><span class="sxs-lookup"><span data-stu-id="c3328-115">Setting Options</span></span></th>
<th align="left"><span data-ttu-id="c3328-116">Valeur de clé de Registre</span><span class="sxs-lookup"><span data-stu-id="c3328-116">Registry Key Value</span></span></th>
<th align="left"><span data-ttu-id="c3328-117">Clés et valeurs de l’état de stratégie désactivé</span><span class="sxs-lookup"><span data-stu-id="c3328-117">Disabled Policy State Keys and Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-118">PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="c3328-118">PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-119">PACKAGEINSTALLATIONROOT</span><span class="sxs-lookup"><span data-stu-id="c3328-119">PACKAGEINSTALLATIONROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-120">Spécifie le répertoire dans lequel toutes les nouvelles applications et mises à jour sont installées.</span><span class="sxs-lookup"><span data-stu-id="c3328-120">Specifies directory where all new applications and updates will be installed.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-121">String</span><span class="sxs-lookup"><span data-stu-id="c3328-121">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-122">Streaming\PackageInstallationRoot</span><span class="sxs-lookup"><span data-stu-id="c3328-122">Streaming\PackageInstallationRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-123">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-123">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-124">PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="c3328-124">PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-125">PACKAGESOURCEROOT</span><span class="sxs-lookup"><span data-stu-id="c3328-125">PACKAGESOURCEROOT</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-126">Remplace l’emplacement source pour le téléchargement du contenu du package.</span><span class="sxs-lookup"><span data-stu-id="c3328-126">Overrides source location for downloading package content.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-127">String</span><span class="sxs-lookup"><span data-stu-id="c3328-127">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-128">Streaming\PackageSourceRoot</span><span class="sxs-lookup"><span data-stu-id="c3328-128">Streaming\PackageSourceRoot</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-129">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-129">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-130">AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="c3328-130">AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-131">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-131">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-132">Ce paramètre détermine si les applications virtualisées sont lancées sur des ordinateurs Windows 8 connectés par le biais d’une connexion réseau limitée (par exemple, 4G).</span><span class="sxs-lookup"><span data-stu-id="c3328-132">This setting controls whether virtualized applications are launched on Windows 8 machines connected via a metered network connection (For example, 4G).</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-133">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-133">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-134">Streaming\AllowHighCostLaunch</span><span class="sxs-lookup"><span data-stu-id="c3328-134">Streaming\AllowHighCostLaunch</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-135">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-135">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-136">ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="c3328-136">ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-137">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-137">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-138">Spécifie le nombre de tentatives de nouvelle session interrompue.</span><span class="sxs-lookup"><span data-stu-id="c3328-138">Specifies the number of times to retry a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-139">Entier (0-99)</span><span class="sxs-lookup"><span data-stu-id="c3328-139">Integer (0-99)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-140">Streaming\ReestablishmentRetries</span><span class="sxs-lookup"><span data-stu-id="c3328-140">Streaming\ReestablishmentRetries</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-141">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-141">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-142">ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-142">ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-143">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-143">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-144">Spécifie le nombre de secondes entre les tentatives de rétablissement d’une session perdue.</span><span class="sxs-lookup"><span data-stu-id="c3328-144">Specifies the number of seconds between attempts to reestablish a dropped session.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-145">Entier (0-3600)</span><span class="sxs-lookup"><span data-stu-id="c3328-145">Integer (0-3600)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-146">Streaming\ReestablishmentInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-146">Streaming\ReestablishmentInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-147">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-147">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-148">AutoLoad</span><span class="sxs-lookup"><span data-stu-id="c3328-148">AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-149">AUTOLOAD</span><span class="sxs-lookup"><span data-stu-id="c3328-149">AUTOLOAD</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-150">Spécifie la façon dont les nouveaux packages doivent être chargés automatiquement par l’application-V sur un ordinateur spécifique.</span><span class="sxs-lookup"><span data-stu-id="c3328-150">Specifies how new packages should be loaded automatically by App-V on a specific computer.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-151">(0x0) aucun; (0x1) précédemment utilisée; (0X2) tous</span><span class="sxs-lookup"><span data-stu-id="c3328-151">(0x0) None; (0x1) Previously used; (0x2) All</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-152">Streaming\AutoLoad</span><span class="sxs-lookup"><span data-stu-id="c3328-152">Streaming\AutoLoad</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-153">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-153">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-154">LocationProvider</span><span class="sxs-lookup"><span data-stu-id="c3328-154">LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-155">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-155">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-156">Spécifie le CLSID pour une implémentation compatible de l’interface IAppvPackageLocationProvider.</span><span class="sxs-lookup"><span data-stu-id="c3328-156">Specifies the CLSID for a compatible implementation of the IAppvPackageLocationProvider interface.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-157">String</span><span class="sxs-lookup"><span data-stu-id="c3328-157">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-158">Streaming\LocationProvider</span><span class="sxs-lookup"><span data-stu-id="c3328-158">Streaming\LocationProvider</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-159">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-159">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-160">CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="c3328-160">CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-161">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-161">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-162">Spécifie le chemin d’accès d’un certificat valide dans le magasin de certificats.</span><span class="sxs-lookup"><span data-stu-id="c3328-162">Specifies the path to a valid certificate in the certificate store.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-163">String</span><span class="sxs-lookup"><span data-stu-id="c3328-163">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-164">Streaming\CertFilterForClientSsl</span><span class="sxs-lookup"><span data-stu-id="c3328-164">Streaming\CertFilterForClientSsl</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-165">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-165">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-166">VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="c3328-166">VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-167">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-167">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-168">Vérifie l’état de révocation des certificats de serveur avant la transmission à l’aide de HTTPs.</span><span class="sxs-lookup"><span data-stu-id="c3328-168">Verifies Server certificate revocation status before steaming using HTTPS.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-169">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-169">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-170">Streaming\VerifyCertificateRevocationList</span><span class="sxs-lookup"><span data-stu-id="c3328-170">Streaming\VerifyCertificateRevocationList</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-171">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-171">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-172">SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="c3328-172">SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-173">SHAREDCONTENTSTOREMODE</span><span class="sxs-lookup"><span data-stu-id="c3328-173">SHAREDCONTENTSTOREMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-174">Spécifie que le contenu du package en flux ne sera pas enregistré sur le disque dur local.</span><span class="sxs-lookup"><span data-stu-id="c3328-174">Specifies that streamed package contents will be not be saved to the local hard disk.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-175">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-175">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-176">Streaming\SharedContentStoreMode</span><span class="sxs-lookup"><span data-stu-id="c3328-176">Streaming\SharedContentStoreMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-177">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-177">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-178">Nom</span><span class="sxs-lookup"><span data-stu-id="c3328-178">Name</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-179">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-179">Note</span></span></strong><br/><p><span data-ttu-id="c3328-180">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-180">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-181">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-181">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-182">PUBLISHINGSERVERNAME</span><span class="sxs-lookup"><span data-stu-id="c3328-182">PUBLISHINGSERVERNAME</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-183">Affiche le nom du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c3328-183">Displays the name of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-184">String</span><span class="sxs-lookup"><span data-stu-id="c3328-184">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-185">Publishing\Servers {serverId} \ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="c3328-185">Publishing\Servers{serverId}\FriendlyName</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-186">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-186">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-187">URL</span><span class="sxs-lookup"><span data-stu-id="c3328-187">URL</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-188">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-188">Note</span></span></strong><br/><p><span data-ttu-id="c3328-189">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-189">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-190">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-190">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-191">PUBLISHINGSERVERURL</span><span class="sxs-lookup"><span data-stu-id="c3328-191">PUBLISHINGSERVERURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-192">Affiche l’URL du serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="c3328-192">Displays the URL of publishing server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-193">String</span><span class="sxs-lookup"><span data-stu-id="c3328-193">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-194">Publishing\Servers {serverId} \ URL</span><span class="sxs-lookup"><span data-stu-id="c3328-194">Publishing\Servers{serverId}\URL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-195">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-195">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-196">GlobalRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="c3328-196">GlobalRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-197">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-197">Note</span></span></strong><br/><p><span data-ttu-id="c3328-198">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-198">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-199">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-199">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-200">GLOBALREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="c3328-200">GLOBALREFRESHENABLED</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-201">Active l’actualisation globale de la publication (booléen)</span><span class="sxs-lookup"><span data-stu-id="c3328-201">Enables global publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-202">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-202">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-203">Publishing\Servers {serverId} \ GlobalEnabled</span><span class="sxs-lookup"><span data-stu-id="c3328-203">Publishing\Servers{serverId}\GlobalEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-204">Faux</span><span class="sxs-lookup"><span data-stu-id="c3328-204">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-205">GlobalRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="c3328-205">GlobalRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-206">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-206">Note</span></span></strong><br/><p><span data-ttu-id="c3328-207">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-207">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-208">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-208">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-209">GLOBALREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="c3328-209">GLOBALREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-210">Déclenche une actualisation globale de publication lors de l’ouverture de session.</span><span class="sxs-lookup"><span data-stu-id="c3328-210">Triggers a global publishing refresh on logon.</span></span> <span data-ttu-id="c3328-211">Expression</span><span class="sxs-lookup"><span data-stu-id="c3328-211">( Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-212">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-212">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-213">Publishing\Servers {serverId} \ GlobalLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="c3328-213">Publishing\Servers{serverId}\GlobalLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-214">Faux</span><span class="sxs-lookup"><span data-stu-id="c3328-214">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-215">GlobalRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-215">GlobalRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-216">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-216">Note</span></span></strong><br/><p><span data-ttu-id="c3328-217">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-217">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-218">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-218">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-219">GLOBALREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="c3328-219">GLOBALREFRESHINTERVAL</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="c3328-220">Spécifie l’intervalle d’actualisation de publication à l’aide de GlobalRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="c3328-220">Specifies the publishing refresh interval using the GlobalRefreshIntervalUnit.</span></span> <span data-ttu-id="c3328-221">Pour désactiver l’actualisation du package, sélectionnez 0.</span><span class="sxs-lookup"><span data-stu-id="c3328-221">To disable package refresh, select 0.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-222">Entier (0-744</span><span class="sxs-lookup"><span data-stu-id="c3328-222">Integer (0-744</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-223">Publishing\Servers {serverId} \ GlobalPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-223">Publishing\Servers{serverId}\GlobalPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-224">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-224">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-225">GlobalRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="c3328-225">GlobalRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-226">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-226">Note</span></span></strong><br/><p><span data-ttu-id="c3328-227">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-227">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-228">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-228">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-229">GLOBALREFRESHINTERVALUNI</span><span class="sxs-lookup"><span data-stu-id="c3328-229">GLOBALREFRESHINTERVALUNI</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-230">Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31).</span><span class="sxs-lookup"><span data-stu-id="c3328-230">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="c3328-231">0 pour l’heure, 1 pour le jour</span><span class="sxs-lookup"><span data-stu-id="c3328-231">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-232">Publishing\Servers {serverId} \ GlobalPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="c3328-232">Publishing\Servers{serverId}\GlobalPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-233">1</span><span class="sxs-lookup"><span data-stu-id="c3328-233">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-234">UserRefreshEnabled</span><span class="sxs-lookup"><span data-stu-id="c3328-234">UserRefreshEnabled</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-235">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-235">Note</span></span></strong><br/><p><span data-ttu-id="c3328-236">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-236">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-237">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-237">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-238">USERREFRESHENABLED</span><span class="sxs-lookup"><span data-stu-id="c3328-238">USERREFRESHENABLED</span></span> </p></td>
<td align="left"><p><span data-ttu-id="c3328-239">Active l’actualisation de la publication des utilisateurs (booléen)</span><span class="sxs-lookup"><span data-stu-id="c3328-239">Enables user publishing refresh (Boolean)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-240">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-240">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-241">Publishing\Servers {serverId} \ UserEnabled</span><span class="sxs-lookup"><span data-stu-id="c3328-241">Publishing\Servers{serverId}\UserEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-242">Faux</span><span class="sxs-lookup"><span data-stu-id="c3328-242">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-243">UserRefreshOnLogon</span><span class="sxs-lookup"><span data-stu-id="c3328-243">UserRefreshOnLogon</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-244">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-244">Note</span></span></strong><br/><p><span data-ttu-id="c3328-245">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-245">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-246">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-246">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-247">USERREFRESHONLOGON</span><span class="sxs-lookup"><span data-stu-id="c3328-247">USERREFRESHONLOGON</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-248">Déclenche une actualisation du ONLOGON de publication par un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3328-248">Triggers a user publishing refresh onlogon.</span></span> <span data-ttu-id="c3328-249">Expression</span><span class="sxs-lookup"><span data-stu-id="c3328-249">( Boolean)</span></span></p>
<p><span data-ttu-id="c3328-250">Statistiques (avec espaces): 60</span><span class="sxs-lookup"><span data-stu-id="c3328-250">Word count (with spaces): 60</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-251">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-251">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-252">Publishing\Servers {serverId} \ UserLogonRefresh</span><span class="sxs-lookup"><span data-stu-id="c3328-252">Publishing\Servers{serverId}\UserLogonRefresh</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-253">Faux</span><span class="sxs-lookup"><span data-stu-id="c3328-253">False</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-254">UserRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-254">UserRefreshInterval</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-255">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-255">Note</span></span></strong><br/><p><span data-ttu-id="c3328-256">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-256">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-257">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-257">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-258">USERREFRESHINTERVAL</span><span class="sxs-lookup"><span data-stu-id="c3328-258">USERREFRESHINTERVAL</span></span>     </p></td>
<td align="left"><p><span data-ttu-id="c3328-259">Spécifie l’intervalle d’actualisation de publication à l’aide de UserRefreshIntervalUnit.</span><span class="sxs-lookup"><span data-stu-id="c3328-259">Specifies the publishing refresh interval using the UserRefreshIntervalUnit.</span></span> <span data-ttu-id="c3328-260">Pour désactiver l’actualisation du package, sélectionnez 0.</span><span class="sxs-lookup"><span data-stu-id="c3328-260">To disable package refresh, select 0.</span></span></p>
<p><span data-ttu-id="c3328-261">Statistiques (avec espaces): 85</span><span class="sxs-lookup"><span data-stu-id="c3328-261">Word count (with spaces): 85</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-262">Entier (0-744 heures)</span><span class="sxs-lookup"><span data-stu-id="c3328-262">Integer (0-744 Hours)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-263">Publishing\Servers {serverId} \ UserPeriodicRefreshInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-263">Publishing\Servers{serverId}\UserPeriodicRefreshInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-264">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-264">0</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-265">UserRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="c3328-265">UserRefreshIntervalUnit</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-266">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-266">Note</span></span></strong><br/><p><span data-ttu-id="c3328-267">Ce paramètre ne peut pas être modifié à l’aide de l' <strong> applet de la cmdLet Set-AppvclientConfiguration </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-267">This setting cannot be modified using the <strong>set-AppvclientConfiguration</strong> cmdLet.</span></span> <span data-ttu-id="c3328-268">Vous devez utiliser l' <strong> applet de cmdlet Set-AppvPublishingServer </strong> .</span><span class="sxs-lookup"><span data-stu-id="c3328-268">You must use the <strong>Set-AppvPublishingServer</strong> cmdlet.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-269">USERREFRESHINTERVALUNIT</span><span class="sxs-lookup"><span data-stu-id="c3328-269">USERREFRESHINTERVALUNIT</span></span>  </p></td>
<td align="left"><p><span data-ttu-id="c3328-270">Spécifie l’unité de l’intervalle (heure 0-23, jour 0-31).</span><span class="sxs-lookup"><span data-stu-id="c3328-270">Specifies the interval unit (Hour 0-23, Day 0-31).</span></span> </p></td>
<td align="left"><p><span data-ttu-id="c3328-271">0 pour l’heure, 1 pour le jour</span><span class="sxs-lookup"><span data-stu-id="c3328-271">0 for hour, 1 for day</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-272">Publishing\Servers {serverId} \ UserPeriodicRefreshIntervalUnit</span><span class="sxs-lookup"><span data-stu-id="c3328-272">Publishing\Servers{serverId}\UserPeriodicRefreshIntervalUnit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-273">1</span><span class="sxs-lookup"><span data-stu-id="c3328-273">1</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-274">MigrationMode</span><span class="sxs-lookup"><span data-stu-id="c3328-274">MigrationMode</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-275">MIGRATIONMODE</span><span class="sxs-lookup"><span data-stu-id="c3328-275">MIGRATIONMODE</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-276">Le mode migration permet au client App-V de modifier des raccourcis et FTA pour les packages créés à l’aide d’une version antérieure d’App-V.</span><span class="sxs-lookup"><span data-stu-id="c3328-276">Migration mode allows the App-V client to modify shortcuts and FTA’s for packages created using a previous version of App-V.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-277">True (état activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-277">True(enabled state); False (disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-278">Coexistence\MigrationMode</span><span class="sxs-lookup"><span data-stu-id="c3328-278">Coexistence\MigrationMode</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-279">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="c3328-279">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-280">CEIPOPTIN</span><span class="sxs-lookup"><span data-stu-id="c3328-280">CEIPOPTIN</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-281">Permet à l’ordinateur exécutant le client App-V 5,0 de collecter et de renvoyer des informations d’utilisation pour nous aider à améliorer l’application.</span><span class="sxs-lookup"><span data-stu-id="c3328-281">Allows the computer running the App-V 5.0 Client to collect and return certain usage information to help allow us to further improve the application.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-282">0 pour désactivé; 1 pour activé</span><span class="sxs-lookup"><span data-stu-id="c3328-282">0 for disabled; 1 for enabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-283">LOGICIEL/Microsoft/AppV/CEIP/CEIPEnable</span><span class="sxs-lookup"><span data-stu-id="c3328-283">SOFTWARE/Microsoft/AppV/CEIP/CEIPEnable</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-284">0,4</span><span class="sxs-lookup"><span data-stu-id="c3328-284">0</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-285">EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="c3328-285">EnablePackageScripts</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-286">ENABLEPACKAGESCRIPTS</span><span class="sxs-lookup"><span data-stu-id="c3328-286">ENABLEPACKAGESCRIPTS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-287">Active les scripts définis dans le manifeste du package de fichiers de configuration qui doivent s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c3328-287">Enables scripts defined in the package manifest of configuration files that should run.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-288">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-288">True(enabled); False(Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-289">\Scripting\EnablePackageScripts</span><span class="sxs-lookup"><span data-stu-id="c3328-289">\Scripting\EnablePackageScripts</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-290">RoamingFileExclusions</span><span class="sxs-lookup"><span data-stu-id="c3328-290">RoamingFileExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-291">ROAMINGFILEEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="c3328-291">ROAMINGFILEEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-292">Spécifie les chemins d’accès relatifs au fichier% UserProfile% qui ne sont pas itinérants avec un profil utilisateur&#39;s.</span><span class="sxs-lookup"><span data-stu-id="c3328-292">Specifies the file paths relative to %userprofile% that do not roam with a user&#39;s profile.</span></span> <span data-ttu-id="c3328-293">Exemple d’utilisation:/ROAMINGFILEEXCLUSIONS =&#39;Bureau; mes images&#39;</span><span class="sxs-lookup"><span data-stu-id="c3328-293">Example usage:  /ROAMINGFILEEXCLUSIONS=&#39;desktop;my pictures&#39;</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-294">RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="c3328-294">RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-295">ROAMINGREGISTRYEXCLUSIONS</span><span class="sxs-lookup"><span data-stu-id="c3328-295">ROAMINGREGISTRYEXCLUSIONS</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-296">Spécifie les chemins de Registre qui ne sont pas itinérants avec un profil utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3328-296">Specifies the registry paths that do not roam with a user profile.</span></span> <span data-ttu-id="c3328-297">Exemple d’utilisation:/ROAMINGREGISTRYEXCLUSIONS = software\classes; software\clients</span><span class="sxs-lookup"><span data-stu-id="c3328-297">Example usage: /ROAMINGREGISTRYEXCLUSIONS=software\classes;software\clients</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-298">String</span><span class="sxs-lookup"><span data-stu-id="c3328-298">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-299">Integration\RoamingRegistryExclusions</span><span class="sxs-lookup"><span data-stu-id="c3328-299">Integration\RoamingRegistryExclusions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-300">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-300">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-301">IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="c3328-301">IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-302">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-302">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-303">Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié par utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c3328-303">Specifies the location to create symbolic links associated with the current version of a per-user published package.</span></span> <span data-ttu-id="c3328-304">toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin.</span><span class="sxs-lookup"><span data-stu-id="c3328-304">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="c3328-305">Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package.</span><span class="sxs-lookup"><span data-stu-id="c3328-305">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="c3328-306">Par exemple:%localappdata%\Microsoft\AppV\Client\Integration.</span><span class="sxs-lookup"><span data-stu-id="c3328-306">For example: %localappdata%\Microsoft\AppV\Client\Integration.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-307">String</span><span class="sxs-lookup"><span data-stu-id="c3328-307">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-308">Integration\IntegrationRootUser</span><span class="sxs-lookup"><span data-stu-id="c3328-308">Integration\IntegrationRootUser</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-309">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-309">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-310">IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="c3328-310">IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-311">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-311">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-312">Spécifie l’emplacement permettant de créer des liens symboliques associés à la version actuelle d’un package publié globalement.</span><span class="sxs-lookup"><span data-stu-id="c3328-312">Specifies the location to create symbolic links associated with the current version of a globally published package.</span></span> <span data-ttu-id="c3328-313">toutes les extensions d’application virtuelles, par exemple les raccourcis clavier et les associations de types de fichiers, pointent vers ce chemin.</span><span class="sxs-lookup"><span data-stu-id="c3328-313">all virtual application extensions, for example shortcuts and file type associations, will point to this path.</span></span> <span data-ttu-id="c3328-314">Si vous ne spécifiez pas de chemin d’accès, les liens symboliques ne seront pas utilisés lors de la publication du package.</span><span class="sxs-lookup"><span data-stu-id="c3328-314">If you do not specify a path, symbolic links will not be used when you publish the package.</span></span> <span data-ttu-id="c3328-315">Par exemple:%allusersprofile%\Microsoft\AppV\Client\Integration</span><span class="sxs-lookup"><span data-stu-id="c3328-315">For example: %allusersprofile%\Microsoft\AppV\Client\Integration</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-316">String</span><span class="sxs-lookup"><span data-stu-id="c3328-316">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-317">Integration\IntegrationRootGlobal</span><span class="sxs-lookup"><span data-stu-id="c3328-317">Integration\IntegrationRootGlobal</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-318">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-318">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-319">VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="c3328-319">VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-320">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-320">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-321">Liste délimitée par des virgules des extensions de nom de fichier qui peut être utilisée pour déterminer si une application installée localement peut être exécutée dans l’environnement virtuel.</span><span class="sxs-lookup"><span data-stu-id="c3328-321">A comma -delineated list of file name extensions that can be used to determine if a locally installed application can be run in the virtual environment.</span></span></p>
<p><span data-ttu-id="c3328-322">Lors de la création de raccourcis, de FTAs et d’autres points d’extension lors de la publication, App-V compare l’extension de nom de fichier à la liste si l’application associée au point d’extension est installée localement.</span><span class="sxs-lookup"><span data-stu-id="c3328-322">When shortcuts, FTAs, and other extension points are created during publishing, App-V will compare the file name extension to the list if the application that is associated with the extension point is locally installed.</span></span> <span data-ttu-id="c3328-323">Si l’extension se trouve, le <strong> paramètre de ligne de commande RunVirtual est </strong> ajouté et l’application s’exécute quasiment.</span><span class="sxs-lookup"><span data-stu-id="c3328-323">If the extension is located, the <strong>RunVirtual</strong> command line parameter will be added, and the application will run virtually.</span></span></p>
<p><span data-ttu-id="c3328-324">Pour plus d’informations sur <strong> le </strong> paramètre RunVirtual, voir <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)"> exécution d’une application installée localement dans un environnement virtuel avec des applications virtualisées </a> .</span><span class="sxs-lookup"><span data-stu-id="c3328-324">For more information about the <strong>RunVirtual</strong> parameter, see <a href="running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md" data-raw-source="[Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications](running-a-locally-installed-application-inside-a-virtual-environment-with-virtualized-applications.md)">Running a Locally Installed Application Inside a Virtual Environment with Virtualized Applications</a>.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-325">String</span><span class="sxs-lookup"><span data-stu-id="c3328-325">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-326">Integration\VirtualizableExtensions</span><span class="sxs-lookup"><span data-stu-id="c3328-326">Integration\VirtualizableExtensions</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-327">Valeur de stratégie non écrite</span><span class="sxs-lookup"><span data-stu-id="c3328-327">Policy value not written</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-328">ReportingEnabled</span><span class="sxs-lookup"><span data-stu-id="c3328-328">ReportingEnabled</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-329">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-329">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-330">Permet au client de renvoyer des informations vers un serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3328-330">Enables the client to return information to a reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-331">True (activé); Faux (état désactivé)</span><span class="sxs-lookup"><span data-stu-id="c3328-331">True (enabled); False (Disabled state)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-332">Reporting\EnableReporting</span><span class="sxs-lookup"><span data-stu-id="c3328-332">Reporting\EnableReporting</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-333">Faux</span><span class="sxs-lookup"><span data-stu-id="c3328-333">False</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-334">ReportingServerURL</span><span class="sxs-lookup"><span data-stu-id="c3328-334">ReportingServerURL</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-335">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-335">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-336">Spécifie l’emplacement sur le serveur de création de rapports où les informations client sont enregistrées.</span><span class="sxs-lookup"><span data-stu-id="c3328-336">Specifies the location on the reporting server where client information is saved.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-337">String</span><span class="sxs-lookup"><span data-stu-id="c3328-337">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-338">Reporting\ReportingServer</span><span class="sxs-lookup"><span data-stu-id="c3328-338">Reporting\ReportingServer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-339">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-339">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-340">ReportingDataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="c3328-340">ReportingDataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-341">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-341">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-342">Spécifie la taille maximale en mégaoctets (Mo) du cache XML pour le stockage des informations de rapport.</span><span class="sxs-lookup"><span data-stu-id="c3328-342">Specifies the maximum size in megabytes (MB) of the XML cache for storing reporting information.</span></span> <span data-ttu-id="c3328-343">La taille s’applique au cache en mémoire.</span><span class="sxs-lookup"><span data-stu-id="c3328-343">The size applies to the cache in memory.</span></span> <span data-ttu-id="c3328-344">Lorsque la limite est atteinte, le fichier journal est restauré.</span><span class="sxs-lookup"><span data-stu-id="c3328-344">When the limit is reached, the log file will roll over.</span></span> <span data-ttu-id="c3328-345">Définie entre 0 et 1024.</span><span class="sxs-lookup"><span data-stu-id="c3328-345">Set between 0 and 1024.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-346">Entier [0-1024]</span><span class="sxs-lookup"><span data-stu-id="c3328-346">Integer [0-1024]</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-347">Reporting\DataCacheLimit</span><span class="sxs-lookup"><span data-stu-id="c3328-347">Reporting\DataCacheLimit</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-348">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-348">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-349">ReportingDataBlockSize</span><span class="sxs-lookup"><span data-stu-id="c3328-349">ReportingDataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-350">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-350">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-351">Spécifie la taille maximale en octets à transmettre au serveur pour signaler les demandes de chargement.</span><span class="sxs-lookup"><span data-stu-id="c3328-351">Specifies the maximum size in bytes to transmit to the server for reporting upload requests.</span></span> <span data-ttu-id="c3328-352">Vous pouvez ainsi éviter les échecs de transmission permanents lorsque le journal atteint une taille significative.</span><span class="sxs-lookup"><span data-stu-id="c3328-352">This can help avoid permanent transmission failures when the log has reached a significant size.</span></span> <span data-ttu-id="c3328-353">Définissez entre 1024 et illimité.</span><span class="sxs-lookup"><span data-stu-id="c3328-353">Set between 1024 and unlimited.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-354">Entier [1024-illimité]</span><span class="sxs-lookup"><span data-stu-id="c3328-354">Integer [1024 - Unlimited]</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-355">Reporting\DataBlockSize</span><span class="sxs-lookup"><span data-stu-id="c3328-355">Reporting\DataBlockSize</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-356">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-356">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-357">ReportingStartTime</span><span class="sxs-lookup"><span data-stu-id="c3328-357">ReportingStartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-358">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-358">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-359">Spécifie le temps nécessaire pour lancer le client pour envoyer des données au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3328-359">Specifies the time to initiate the client to send data to the reporting server.</span></span> <span data-ttu-id="c3328-360">Vous devez spécifier un entier valide entre 0-23 correspondant à l’heure du jour.</span><span class="sxs-lookup"><span data-stu-id="c3328-360">You must specify a valid integer between 0-23 corresponding to the hour of the day.</span></span> <span data-ttu-id="c3328-361">Par défaut, le <strong> ReportingStartTime </strong> commence à la journée en cours à 10 P. M. ou 22.</span><span class="sxs-lookup"><span data-stu-id="c3328-361">By default the <strong>ReportingStartTime</strong> will start on the current day at 10 P.M.or 22.</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-362">Remarque</span><span class="sxs-lookup"><span data-stu-id="c3328-362">Note</span></span></strong><br/><p><span data-ttu-id="c3328-363">Vous devez configurer ce paramètre sur une date à laquelle les ordinateurs exécutant le client App-V 5,0 sont moins susceptibles de se déconnecter.</span><span class="sxs-lookup"><span data-stu-id="c3328-363">You should configure this setting to a time when computers running the App-V 5.0 client are least likely to be offline.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-364">Entier (0 à 23)</span><span class="sxs-lookup"><span data-stu-id="c3328-364">Integer (0 – 23)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-365">Rapport \ StartTime</span><span class="sxs-lookup"><span data-stu-id="c3328-365">Reporting\ StartTime</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-366">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-366">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-367">ReportingInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-367">ReportingInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-368">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-368">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-369">Spécifie l’intervalle de réessayer que le client doit utiliser pour renvoyer les données au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3328-369">Specifies the retry interval that the client will use to resend data to the reporting server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-370">Integer</span><span class="sxs-lookup"><span data-stu-id="c3328-370">Integer</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-371">Reporting\RetryInterval</span><span class="sxs-lookup"><span data-stu-id="c3328-371">Reporting\RetryInterval</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-372">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-372">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-373">ReportingRandomDelay</span><span class="sxs-lookup"><span data-stu-id="c3328-373">ReportingRandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-374">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-374">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-375">Spécifie le délai maximal (en minutes) pour les données à envoyer au serveur de rapports.</span><span class="sxs-lookup"><span data-stu-id="c3328-375">Specifies the maximum delay (in minutes) for data to be sent to the reporting server.</span></span> <span data-ttu-id="c3328-376">Lorsque la tâche planifiée est lancée, le client génère un délai aléatoire compris entre 0 et <strong> ReportingRandomDelay </strong> et attend la durée spécifiée avant d’envoyer des données.</span><span class="sxs-lookup"><span data-stu-id="c3328-376">When the scheduled task is started, the client generates a random delay between 0 and <strong>ReportingRandomDelay</strong> and will wait the specified duration before sending data.</span></span> <span data-ttu-id="c3328-377">Cela peut vous aider à éviter les collisions sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="c3328-377">This can help to prevent collisions on the server.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-378">Entier [0-ReportingRandomDelay]</span><span class="sxs-lookup"><span data-stu-id="c3328-378">Integer [0 - ReportingRandomDelay]</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-379">Reporting\RandomDelay</span><span class="sxs-lookup"><span data-stu-id="c3328-379">Reporting\RandomDelay</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-380">Valeur de stratégie non rédigée (comme non configuré)</span><span class="sxs-lookup"><span data-stu-id="c3328-380">Policy value not written (same as Not Configured)</span></span></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-381">EnableDynamicVirtualization</span><span class="sxs-lookup"><span data-stu-id="c3328-381">EnableDynamicVirtualization</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-382">Important</span><span class="sxs-lookup"><span data-stu-id="c3328-382">Important</span></span></strong><br/><p><span data-ttu-id="c3328-383">Ce paramètre est disponible uniquement avec App-V 5,0 SP2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="c3328-383">This setting is available only with App-V 5.0 SP2 or later.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-384">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-384">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-385">Permet aux extensions d’environnement prises en charge, aux objets d’assistance du navigateur et aux contrôles Active X d’être virtualisés et exécutés avec des applications virtuelles.</span><span class="sxs-lookup"><span data-stu-id="c3328-385">Enables supported Shell Extensions, Browser Helper Objects, and Active X controls to be virtualized and run with virtual applications.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-386">1 (activé), 0 (désactivée)</span><span class="sxs-lookup"><span data-stu-id="c3328-386">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-387">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Virtualization</span><span class="sxs-lookup"><span data-stu-id="c3328-387">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Virtualization</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-388">EnablePublishingRefreshUI</span><span class="sxs-lookup"><span data-stu-id="c3328-388">EnablePublishingRefreshUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-389">Important</span><span class="sxs-lookup"><span data-stu-id="c3328-389">Important</span></span></strong><br/><p><span data-ttu-id="c3328-390">Ce paramètre est disponible uniquement avec App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c3328-390">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-391">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-391">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-392">Active la barre de progression de l’actualisation de la publication pour l’ordinateur exécutant le client App-V 5,0.</span><span class="sxs-lookup"><span data-stu-id="c3328-392">Enables the publishing refresh progress bar for the computer running the App-V 5.0 Client.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-393">1 (activé), 0 (désactivée)</span><span class="sxs-lookup"><span data-stu-id="c3328-393">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-394">HKEY_LOCAL_MACHINE \Software\Microsoft\AppV\Client\Publishing</span><span class="sxs-lookup"><span data-stu-id="c3328-394">HKEY_LOCAL_MACHINE\Software\Microsoft\AppV\Client\Publishing</span></span></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="even">
<td align="left"><p><span data-ttu-id="c3328-395">HideUI</span><span class="sxs-lookup"><span data-stu-id="c3328-395">HideUI</span></span></p>
<div class="alert">
<strong><span data-ttu-id="c3328-396">Important</span><span class="sxs-lookup"><span data-stu-id="c3328-396">Important</span></span></strong><br/><p><span data-ttu-id="c3328-397">Ce paramètre est disponible uniquement avec App-V 5,0 SP2.</span><span class="sxs-lookup"><span data-stu-id="c3328-397">This setting is available only with App-V 5.0 SP2.</span></span></p>
</div>
<div>

</div></td>
<td align="left"><p><span data-ttu-id="c3328-398">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-398">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-399">Masque la barre de progression de l’actualisation de la publication.</span><span class="sxs-lookup"><span data-stu-id="c3328-399">Hides the publishing refresh progress bar.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-400">1 (activé), 0 (désactivée)</span><span class="sxs-lookup"><span data-stu-id="c3328-400">1 (Enabled), 0 (Disabled)</span></span></p></td>
<td align="left"><p></p></td>
<td align="left"><p></p></td>
</tr>
<tr class="odd">
<td align="left"><p><span data-ttu-id="c3328-401">ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="c3328-401">ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-402">Non disponible.</span><span class="sxs-lookup"><span data-stu-id="c3328-402">Not available.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-403">Spécifie une liste de chemins de processus (qui peuvent contenir des caractères génériques), qui sont candidats à l’utilisation de la virtualisation dynamique (extensions d’environnement prises en charge, objets d’assistance du navigateur et contrôles ActiveX).</span><span class="sxs-lookup"><span data-stu-id="c3328-403">Specifies a list of process paths (that may contain wildcards), which are candidates for using dynamic virtualization (supported shell extensions, browser helper objects, and ActiveX controls).</span></span> <span data-ttu-id="c3328-404">Seuls les processus dont le chemin complet correspond à l’un de ces éléments peuvent utiliser la virtualisation dynamique.</span><span class="sxs-lookup"><span data-stu-id="c3328-404">Only processes whose full path matches one of these items can use dynamic virtualization.</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-405">String</span><span class="sxs-lookup"><span data-stu-id="c3328-405">String</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-406">Virtualization\ProcessesUsingVirtualComponents</span><span class="sxs-lookup"><span data-stu-id="c3328-406">Virtualization\ProcessesUsingVirtualComponents</span></span></p></td>
<td align="left"><p><span data-ttu-id="c3328-407">Chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="c3328-407">Empty string.</span></span></p></td>
</tr>
</tbody>
</table>








## <span data-ttu-id="c3328-408">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c3328-408">Related topics</span></span>


[<span data-ttu-id="c3328-409">Déploiement d'App-V5.0 Sequencer et Client</span><span class="sxs-lookup"><span data-stu-id="c3328-409">Deploying the App-V 5.0 Sequencer and Client</span></span>](deploying-the-app-v-50-sequencer-and-client.md)

[<span data-ttu-id="c3328-410">Modification de la configuration d'App-V5.0 Client à l'aide du modèle ADMX et d'une stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="c3328-410">How to Modify App-V 5.0 Client Configuration Using the ADMX Template and Group Policy</span></span>](how-to-modify-app-v-50-client-configuration-using-the-admx-template-and-group-policy.md)

[<span data-ttu-id="c3328-411">Comment déployer App-V Client</span><span class="sxs-lookup"><span data-stu-id="c3328-411">How to Deploy the App-V Client</span></span>](how-to-deploy-the-app-v-client-gb18030.md)









