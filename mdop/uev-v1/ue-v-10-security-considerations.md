---
title: Considérations sur la sécurité relatives à UE-V1.0
description: Considérations sur la sécurité relatives à UE-V1.0
author: dansimp
ms.assetid: c5cdf9ff-dc96-4491-98e9-0eada898ffe0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: b503028ae327f92759fe0f64f33fe0cffc62b05c
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10810290"
---
# <span data-ttu-id="eb2e8-103">Considérations sur la sécurité relatives à UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="eb2e8-103">UE-V 1.0 Security Considerations</span></span>


<span data-ttu-id="eb2e8-104">Cette rubrique fournit une vue d’ensemble des comptes et des groupes, des fichiers journaux et d’autres considérations relatives à la sécurité relatives à la virtualisation de l’utilisation de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-104">This topic contains a brief overview of accounts and groups, log files, and other security-related considerations for Microsoft User Experience Virtualization (UE-V).</span></span> <span data-ttu-id="eb2e8-105">Pour plus d’informations, suivez les liens fournis ici.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-105">For more information, follow the links that are provided here.</span></span>

## <span data-ttu-id="eb2e8-106">Considérations en matière de sécurité pour la configuration d’UE-V</span><span class="sxs-lookup"><span data-stu-id="eb2e8-106">Security considerations for UE-V configuration</span></span>


**<span data-ttu-id="eb2e8-107">Lorsque vous créez le partage de stockage des paramètres, limitez l’accès du partage aux utilisateurs qui ont besoin d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-107">When you create the settings storage share, limit the share access to users that need access.</span></span>**

<span data-ttu-id="eb2e8-108">Étant donné que les packages de paramètres peuvent contenir des informations personnelles, vous devez veiller à les protéger aussi bien que possible.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-108">Because settings packages may contain personal information, you should take care to protect them as well as possible.</span></span> <span data-ttu-id="eb2e8-109">En général, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-109">In general, do the following:</span></span>

-   <span data-ttu-id="eb2e8-110">Limitez le partage aux seuls utilisateurs qui ont besoin d’y accéder.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-110">Restrict the share to only the users that need access.</span></span> <span data-ttu-id="eb2e8-111">Créer un groupe de sécurité pour les utilisateurs qui ont Redirigé des dossiers sur un partage particulier et limiter l’accès à ces utilisateurs uniquement;</span><span class="sxs-lookup"><span data-stu-id="eb2e8-111">Create a security group for users that have redirected folders on a particular share, and limit access to only those users.</span></span>

-   <span data-ttu-id="eb2e8-112">Lorsque vous créez le partage, masquez le partage en plaçant un $ après le nom du partage.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-112">When you create the share, hide the share by putting a $ after the share name.</span></span> <span data-ttu-id="eb2e8-113">Cela permet de masquer le partage dans les navigateurs informels et le partage ne sera pas visible dans les emplacements réseau.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-113">This will hide the share from casual browsers, and the share will not be visible in My Network Places.</span></span>

-   <span data-ttu-id="eb2e8-114">Octroiez aux utilisateurs uniquement le volume minimum d’autorisations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-114">Only give users the minimum amount of permissions needed.</span></span> <span data-ttu-id="eb2e8-115">Les autorisations nécessaires sont indiquées dans les tableaux ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-115">The permissions needed are shown in the tables below.</span></span>

    1.  <span data-ttu-id="eb2e8-116">Définissez les autorisations de niveau de partage (SMB) suivantes pour le dossier Setting Storage Location:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-116">Set the following share-level (SMB) permissions for the setting storage location folder:</span></span>

        <table>
        <colgroup>
        <col width="50%" />
        <col width="50%" />
        </colgroup>
        <thead>
        <tr class="header">
        <th align="left"><span data-ttu-id="eb2e8-117">Compte d’utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb2e8-117">User account</span></span></th>
        <th align="left"><span data-ttu-id="eb2e8-118">Autorisations recommandées</span><span class="sxs-lookup"><span data-stu-id="eb2e8-118">Recommended permissions</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr class="odd">
        <td align="left"><p><span data-ttu-id="eb2e8-119">Tout le monde</span><span class="sxs-lookup"><span data-stu-id="eb2e8-119">Everyone</span></span></p></td>
        <td align="left"><p><span data-ttu-id="eb2e8-120">Aucune autorisation</span><span class="sxs-lookup"><span data-stu-id="eb2e8-120">No Permissions</span></span></p></td>
        </tr>
        <tr class="even">
        <td align="left"><p><span data-ttu-id="eb2e8-121">Groupe de sécurité d’UE-V</span><span class="sxs-lookup"><span data-stu-id="eb2e8-121">Security group of UE-V</span></span></p></td>
        <td align="left"><p><span data-ttu-id="eb2e8-122">Contrôle total</span><span class="sxs-lookup"><span data-stu-id="eb2e8-122">Full Control</span></span></p></td>
        </tr>
        </tbody>
        </table>



~~~
2.  Set the following NTFS permissions for the settings storage location folder:

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Folder</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Admins</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Security group of UE-V users</p></td>
    <td align="left"><p>List Folder/Read Data, Create Folders/Append Data</p></td>
    <td align="left"><p>This Folder Only</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>Remove all Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    </tbody>
    </table>



3.  Set the following share-level (SMB) permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="50%" />
    <col width="50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommend permissions</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>Read Permission Levels</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Read/Write Permission Levels</p></td>
    </tr>
    </tbody>
    </table>



4.  Set the following NTFS permissions for the settings template catalog folder.

    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th align="left">User account</th>
    <th align="left">Recommended permissions</th>
    <th align="left">Apply to</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td align="left"><p>Creator/Owner</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Domain Computers</p></td>
    <td align="left"><p>List Folder Contents and Read</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    <tr class="odd">
    <td align="left"><p>Everyone</p></td>
    <td align="left"><p>No Permissions</p></td>
    <td align="left"><p>No Permissions</p></td>
    </tr>
    <tr class="even">
    <td align="left"><p>Administrators</p></td>
    <td align="left"><p>Full Control</p></td>
    <td align="left"><p>This Folder, Subfolders and Files</p></td>
    </tr>
    </tbody>
    </table>
~~~



### <span data-ttu-id="eb2e8-123">Utiliser Windows Server 2003 ou un serveur ultérieur pour héberger des partages de fichiers redirigés</span><span class="sxs-lookup"><span data-stu-id="eb2e8-123">Use Windows Server 2003 or later servers to host redirected file shares</span></span>

<span data-ttu-id="eb2e8-124">Les fichiers de package de paramètres utilisateur contiennent des informations personnelles transférées entre l’ordinateur client et le serveur qui stocke les packages de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-124">User settings package files contain personal information that is transferred between the client computer and the server that stores the settings packages.</span></span> <span data-ttu-id="eb2e8-125">Pour cette raison, vous devez vous assurer que les données sont protégées lors de leur déplacement sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-125">Because of this, you should ensure that the data is protected while it travels over the network.</span></span>

<span data-ttu-id="eb2e8-126">Les données de paramètres utilisateur sont vulnérables aux menaces potentielles suivantes: interception des données lors de leur passage sur le réseau. falsification des données lors du passage sur le réseau; et l’usurpation d’identité du serveur qui héberge les données.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-126">User settings data is vulnerable to these potential threats: interception of the data as it passes over the network; tampering with the data as it passes over the network; and spoofing of the server that hosts the data.</span></span>

<span data-ttu-id="eb2e8-127">Plusieurs fonctionnalités de Windows Server 2003 et versions ultérieures peuvent vous aider à sécuriser les données des utilisateurs:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-127">Several features of Windows Server 2003 and above can help to secure user data:</span></span>

-   <span data-ttu-id="eb2e8-128">**Kerberos** : Kerberos est standard pour toutes les versions de Windows 2000 et de windows Server 2003 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-128">**Kerberos** - Kerberos is standard on all versions of Windows 2000 and Windows Server 2003 and later.</span></span> <span data-ttu-id="eb2e8-129">Kerberos vérifie le niveau de sécurité le plus élevé aux ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-129">Kerberos ensures the highest level of security to network resources.</span></span> <span data-ttu-id="eb2e8-130">NTLM authentifie uniquement le client; Kerberos authentifie le serveur et le client.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-130">NTLM authenticates the client only; Kerberos authenticates the server and the client.</span></span> <span data-ttu-id="eb2e8-131">Lorsque la valeur NTLM est utilisée, le client ne sait pas si le serveur est valide.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-131">When NTLM is used, the client does not know whether the server is valid.</span></span> <span data-ttu-id="eb2e8-132">Ceci est particulièrement important si le client échange des fichiers personnels avec le serveur, comme c’est le cas pour les profils itinérants.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-132">This is particularly important if the client is exchanging personal files with the server, as is the case with Roaming Profiles.</span></span> <span data-ttu-id="eb2e8-133">Kerberos fournit une meilleure sécurité que le protocole NTLM.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-133">Kerberos provides better security than NTLM.</span></span> <span data-ttu-id="eb2e8-134">Kerberos n’est pas disponible dans la version 4,0 ou les systèmes d’exploitation de version antérieure de Windows NT.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-134">Kerberos is not available on Windows NT version 4.0 or earlier operating systems.</span></span>

-   <span data-ttu-id="eb2e8-135">**IPSec** : le protocole IPSec fournit une authentification au niveau du réseau, l’intégrité des données et le chiffrement.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-135">**IPsec** - The IP Security Protocol (IPsec) provides network-level authentication, data integrity, and encryption.</span></span> <span data-ttu-id="eb2e8-136">IPsec vérifie les points suivants:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-136">IPsec ensures the following:</span></span>

    -   <span data-ttu-id="eb2e8-137">Les données itinérantes sont sûres de la modification des données lors de l’itinéraire.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-137">Roamed data is safe from data modification while en route.</span></span>

    -   <span data-ttu-id="eb2e8-138">Les données itinérantes sont sûres de l’interception, de l’affichage ou de la copie.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-138">Roamed data is safe from interception, viewing, or copying.</span></span>

    -   <span data-ttu-id="eb2e8-139">Les données itinérantes ne sont pas accessibles par les parties non authentifiées.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-139">Roamed data is safe from being accessed by unauthenticated parties.</span></span>

-   <span data-ttu-id="eb2e8-140">**Signature SMB** : le protocole d’authentification par bloc de message serveur (SMB) prend en charge l’authentification des messages qui empêche les messages actifs et les attaques de type «homme-au-milieu».</span><span class="sxs-lookup"><span data-stu-id="eb2e8-140">**SMB Signing** - The Server Message Block (SMB) authentication protocol supports message authentication which prevents active message and "man-in-the-middle" attacks.</span></span> <span data-ttu-id="eb2e8-141">La signature SMB fournit cette authentification en plaçant une signature numérique dans chaque SMB.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-141">SMB signing provides this authentication by placing a digital signature into each SMB.</span></span> <span data-ttu-id="eb2e8-142">La signature numérique est alors vérifiée par le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-142">The digital signature is then verified by both the client and the server.</span></span> <span data-ttu-id="eb2e8-143">Pour pouvoir utiliser la signature SMB, vous devez d’abord l’activer ou l’exiger sur le client SMB et le serveur SMB.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-143">In order to use SMB signing, you must first either enable it or require it on both the SMB client and the SMB server.</span></span> <span data-ttu-id="eb2e8-144">Notez que la signature SMB impose une pénalité en termes de performances.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-144">Note that the SMB signing imposes a performance penalty.</span></span> <span data-ttu-id="eb2e8-145">Il n’utilise pas encore plus de bande passante réseau, mais il utilise davantage de cycles UC sur le client et côté serveur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-145">It does not consume any more network bandwidth, but it uses more CPU cycles on the client and server side.</span></span>

### <span data-ttu-id="eb2e8-146">Toujours utiliser le système de fichiers NTFS pour les volumes qui contiennent des données d’utilisateurs</span><span class="sxs-lookup"><span data-stu-id="eb2e8-146">Always use the NTFS File system for volumes holding users data</span></span>

<span data-ttu-id="eb2e8-147">Pour la configuration la plus sécurisée, configurez les serveurs qui hébergent les fichiers de paramètres d’UE-V de façon à utiliser le système de fichiers NTFS.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-147">For the most secure configuration, configure servers that host the UE-V settings files to use the NTFS File System.</span></span> <span data-ttu-id="eb2e8-148">Contrairement à FAT, le système NTFS prend en charge les listes de contrôle d’accès discrétionnaire (DACL) et les listes de contrôle d’accès (SACL).</span><span class="sxs-lookup"><span data-stu-id="eb2e8-148">Unlike FAT, NTFS supports Discretionary access control lists (DACLs) and system access control lists (SACLs).</span></span> <span data-ttu-id="eb2e8-149">Les DACL et les SACL contrôlent les utilisateurs autorisés à effectuer des opérations sur un fichier, ainsi que les événements déclenchant la journalisation des actions exécutées sur un fichier.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-149">DACLs and SACLs control who can perform operations on a file and what events will trigger the logging of actions performed on a file.</span></span>

### <a href="" id="do-not-rely-on-efs-to-encrypt-users--files-when-transmitted-over-the-network"></a><span data-ttu-id="eb2e8-150">Ne pas s’appuyer sur le système EFS pour chiffrer les fichiers des utilisateurs lors de leur transmission via le réseau</span><span class="sxs-lookup"><span data-stu-id="eb2e8-150">Do not rely on EFS to encrypt users’ files when transmitted over the network</span></span>

<span data-ttu-id="eb2e8-151">Lorsque vous utilisez le système de fichiers EFS pour chiffrer les fichiers sur un serveur distant, les données chiffrées ne sont pas chiffrées lors du transit sur le réseau. Elle est uniquement chiffrée lorsque celle-ci est stockée sur le disque.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-151">When you use Encrypting File System (EFS) to encrypt files on a remote server, the encrypted data is not encrypted during transit over the network; It only becomes encrypted when stored on disk.</span></span>

<span data-ttu-id="eb2e8-152">Il existe des exceptions à cette configuration lorsque votre système inclut le protocole IPsec (Internet Protocol Security) ou WebDAV (Web Distributed Authoring and Versioning).</span><span class="sxs-lookup"><span data-stu-id="eb2e8-152">The exceptions to this are when your system includes Internet Protocol security (IPsec) or Web Distributed Authoring and Versioning (WebDAV).</span></span> <span data-ttu-id="eb2e8-153">IPsec chiffre les données lors de leur transport via un réseau TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-153">IPsec encrypts data while it is transported over a TCP/IP network.</span></span> <span data-ttu-id="eb2e8-154">Si le fichier est chiffré avant d’être copié ou déplacé vers un dossier WebDAV sur un serveur, il reste chiffré lors de la transmission et est stocké sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-154">If the file is encrypted before being copied or moved to a WebDAV folder on a server, it will remain encrypted during the transmission and while it is stored on the server.</span></span>

### <span data-ttu-id="eb2e8-155">Chiffrer le cache des fichiers en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="eb2e8-155">Encrypt the Offline Files cache</span></span>

<span data-ttu-id="eb2e8-156">Par défaut, le cache des fichiers en mode hors connexion est protégé sur les partitions NTFS par des listes de précautions, mais le fait de chiffrer le cache renforce la sécurité sur un ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-156">By default, the Offline Files cache is protected on NTFS partitions by ACLs, but encrypting the cache further enhances security on a local computer.</span></span> <span data-ttu-id="eb2e8-157">Par défaut, le cache de l’ordinateur local n’est pas chiffré, de sorte que les fichiers chiffrés mis en cache à partir du réseau ne seront pas chiffrés sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-157">By default, the cache on the local computer is not encrypted, so any encrypted files cached from the network will not be encrypted on the local computer.</span></span> <span data-ttu-id="eb2e8-158">Cela risque de compromettre la sécurité dans certains environnements.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-158">This may pose a security risk in some environments.</span></span>

<span data-ttu-id="eb2e8-159">Lorsque le chiffrement est activé, tous les fichiers du cache de fichiers hors connexion sont chiffrés.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-159">When encryption is enabled, all files in the Offline Files cache are encrypted.</span></span> <span data-ttu-id="eb2e8-160">Il s’agit du chiffrement des fichiers existants, ainsi que des fichiers ajoutés plus tard.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-160">This includes encrypting existing files as well as files that are added later.</span></span> <span data-ttu-id="eb2e8-161">La copie mise en cache de l’ordinateur local est affectée, mais pas la copie réseau associée.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-161">The cached copy on the local computer is affected, but the associated network copy is not.</span></span>

<span data-ttu-id="eb2e8-162">Le cache peut être chiffré de l’une des deux manières suivantes:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-162">The cache can be encrypted in one of two ways:</span></span>

1.  <span data-ttu-id="eb2e8-163">Via une stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-163">Via Group Policy.</span></span> <span data-ttu-id="eb2e8-164">-Activez le paramètre **chiffrer le cache fichiers en mode hors connexion** , situé sur ordinateur Configuration\\Administrative Templates\\Network\\Offline fichiers, dans l’éditeur de stratégies de groupe.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-164">- Enable the **Encrypt the Offline Files Cache** setting, located at Computer Configuration\\Administrative Templates\\Network\\Offline Files, in the Group Policy editor.</span></span>

2.  <span data-ttu-id="eb2e8-165">Manuels.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-165">Manually.</span></span> <span data-ttu-id="eb2e8-166">-Sélectionnez Outils, puis Options des dossiers dans le menu de commandes de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-166">- Select Tools and then Folder Options in the command menu of Windows Explorer.</span></span> <span data-ttu-id="eb2e8-167">Sélectionnez l’onglet fichiers en mode hors connexion, puis activez la case à cocher **chiffrer les fichiers en mode hors connexion pour sécuriser les données** .</span><span class="sxs-lookup"><span data-stu-id="eb2e8-167">Select the Offline Files tab, and then select the **Encrypt offline files to secure data** check box.</span></span>

### <span data-ttu-id="eb2e8-168">Permettre à l’agent UE-V de créer des dossiers pour chaque utilisateur</span><span class="sxs-lookup"><span data-stu-id="eb2e8-168">Let the UE-V Agent create folders for each user</span></span>

<span data-ttu-id="eb2e8-169">Pour vous assurer que UE-V fonctionne de façon optimale, créez uniquement le partage racine sur le serveur et laissez l’agent UE-V créer des dossiers pour chaque utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-169">To ensure that UE-V works optimally, create only the root share on the server, and let the UE-V Agent create the folders for each user.</span></span> <span data-ttu-id="eb2e8-170">UE-V va créer ces dossiers utilisateur avec la sécurité appropriée.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-170">UE-V will create these user folders with the appropriate security.</span></span>

<span data-ttu-id="eb2e8-171">Cette configuration d’autorisation permet aux utilisateurs de créer des dossiers pour le stockage des paramètres.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-171">This permission configuration allows users to create folders for settings storage.</span></span> <span data-ttu-id="eb2e8-172">UE-V agent crée et sécurise un dossier settingspackage tout en étant exécuté dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-172">The UE-V agent creates and secures a settingspackage folder while running in the context of the user.</span></span> <span data-ttu-id="eb2e8-173">L’utilisateur reçoit le contrôle total de son dossier settingspackage.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-173">The user receives full control to their settingspackage folder.</span></span> <span data-ttu-id="eb2e8-174">Les autres utilisateurs n’héritent pas de l’accès à ce dossier.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-174">Other users do not inherit access to this folder.</span></span> <span data-ttu-id="eb2e8-175">Vous n’avez pas besoin de créer et de sécuriser des annuaires utilisateurs individuels.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-175">You do not need to create and secure individual user directories.</span></span> <span data-ttu-id="eb2e8-176">Cette opération sera exécutée automatiquement par l’agent qui s’exécute dans le contexte de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-176">This will be done automatically by the agent that runs in the context of the user.</span></span>

**<span data-ttu-id="eb2e8-177">Remarque</span><span class="sxs-lookup"><span data-stu-id="eb2e8-177">Note</span></span>**  
<span data-ttu-id="eb2e8-178">Une sécurité supplémentaire peut être configurée quand un serveur Windows est utilisé pour le partage de stockage de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-178">Additional security can be configured when a Windows server is utilized for the settings storage share.</span></span> <span data-ttu-id="eb2e8-179">UE-V peut être configuré pour vérifier que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier dans lequel les packages de paramètres sont stockés.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-179">UE-V can be configured to verify that either the local administrator's group or the current user is the owner of the folder where settings packages are stored.</span></span> <span data-ttu-id="eb2e8-180">Pour activer la sécurité supplémentaire, utilisez la commande suivante:</span><span class="sxs-lookup"><span data-stu-id="eb2e8-180">To enable additional security use the following command:</span></span>

1.  <span data-ttu-id="eb2e8-181">Ajoutez une clé de Registre REG \ _DWORD nommée «RepositoryOwnerCheckEnabled» à `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration` .</span><span class="sxs-lookup"><span data-stu-id="eb2e8-181">Add a REG\_DWORD registry key named "RepositoryOwnerCheckEnabled" to `HKEY_LOCAL_MACHINE\Software\Microsoft\UEV\Agent\Configuration`.</span></span>

2.  <span data-ttu-id="eb2e8-182">Définissez la valeur de clé de Registre sur 1.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-182">Set registry key value to 1.</span></span>

<span data-ttu-id="eb2e8-183">Lorsque ce paramètre de configuration est en place, l’agent UE-V vérifie que le groupe de l’administrateur local ou l’utilisateur actuel est le propriétaire du dossier settingspackage.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-183">When this configuration setting is in place, the UE-V agent verifies that the local administrator’s group or current user is the owner of the settingspackage folder.</span></span> <span data-ttu-id="eb2e8-184">Si ce n’est pas le cas, l’agent UE-V n’autorise pas l’accès au dossier.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-184">If not, then the UE-V agent will not allow access to the folder.</span></span>



<span data-ttu-id="eb2e8-185">Si vous devez créer des dossiers pour les utilisateurs et vérifier que vous disposez des autorisations appropriées.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-185">If you must create folders for the users and ensure that you have the correct permissions set.</span></span>

<span data-ttu-id="eb2e8-186">Nous vous recommandons vivement de ne pas créer de dossiers, mais plutôt que d’utiliser l’agent UE-V pour créer le dossier de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-186">We strongly recommend that you do not precreate folders and that instead, you allow the UE-V agent to create the folder for the user.</span></span>

### <a href="" id="ensure-that-correct-permissions-are-set-when-storing-ue-v-settings-in-a-user-s-home-directory"></a><span data-ttu-id="eb2e8-187">Vérifiez que les autorisations appropriées sont définies lors du stockage des paramètres d’UE-V dans le répertoire d’accueil d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-187">Ensure that correct permissions are set when storing UE-V settings in a user’s home directory</span></span>

<span data-ttu-id="eb2e8-188">Si vous redirigez les paramètres d’UE-V vers le répertoire de base d’un utilisateur, veillez à ce que les autorisations sur le répertoire de base de l’utilisateur soient définies correctement pour votre organisation.</span><span class="sxs-lookup"><span data-stu-id="eb2e8-188">If you redirect UE-V settings to a user’s home directory, be sure that the permissions on the user's home directory are set appropriately for your organization.</span></span>

## <span data-ttu-id="eb2e8-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eb2e8-189">Related topics</span></span>


[<span data-ttu-id="eb2e8-190">Sécurité et confidentialité pour UE-V1.0</span><span class="sxs-lookup"><span data-stu-id="eb2e8-190">Security and Privacy for UE-V 1.0</span></span>](security-and-privacy-for-ue-v-10.md)









