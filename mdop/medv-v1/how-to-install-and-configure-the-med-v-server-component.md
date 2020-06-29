---
title: Procédure pour installer et configurer le composant serveur MED-V
description: Procédure pour installer et configurer le composant serveur MED-V
author: dansimp
ms.assetid: 2d3c5b15-df2c-4ab6-bf78-f47ef8ae7418
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 4fb0cc5c9ffe76e987e316d0285f172dd0b76578
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10812078"
---
# <span data-ttu-id="130ee-103">Procédure pour installer et configurer le composant serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="130ee-103">How to Install and Configure the MED-V Server Component</span></span>


<span data-ttu-id="130ee-104">Cette section explique comment [installer](#bkmk-howtoinstallthemedvserver) et [configurer](#bkmk-howtoconfigurethemedvserver) le serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="130ee-104">This section explains how to [install](#bkmk-howtoinstallthemedvserver) and [configure](#bkmk-howtoconfigurethemedvserver) the MED-V server.</span></span>

## <a href="" id="bkmk-howtoinstallthemedvserver"></a><span data-ttu-id="130ee-105">Comment installer le serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="130ee-105">How to Install the MED-V Server</span></span>


**<span data-ttu-id="130ee-106">Pour installer le serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="130ee-106">To install the MED-V server</span></span>**

1.  <span data-ttu-id="130ee-107">Installez le package. msi du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="130ee-107">Install the MED-V Server .msi package.</span></span>

    <span data-ttu-id="130ee-108">Le package MED-V Server. msi est appelé *MED-V\_Server\_x.msi*, où x représente le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="130ee-108">The MED-V Server .msi package is called *MED-V\_Server\_x.msi*, where x is the version number.</span></span>

    <span data-ttu-id="130ee-109">Par exemple, *MED-V\_Server\_1.0.65.msi*.</span><span class="sxs-lookup"><span data-stu-id="130ee-109">For example, *MED-V\_Server\_1.0.65.msi*.</span></span>

2.  <span data-ttu-id="130ee-110">Lorsque l’écran d’accueil de l' **Assistant InstallShield** s’affiche, cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="130ee-110">When the **InstallShield Wizard Welcome** screen appears, click **Next**.</span></span>

3.  <span data-ttu-id="130ee-111">Dans l’écran **contrat de licence** , lisez le contrat de licence, cliquez sur **J’accepte les termes du contrat de licence**, puis cliquez sur **suivant**.</span><span class="sxs-lookup"><span data-stu-id="130ee-111">On the **License Agreement** screen, read the license agreement, click **I accept the terms in the license agreement**, and then click **Next**.</span></span>

    <span data-ttu-id="130ee-112">L’écran **dossier de destination** s’affiche avec le dossier d’installation par défaut affiché.</span><span class="sxs-lookup"><span data-stu-id="130ee-112">The **Destination Folder** screen appears, with the default installation folder displayed.</span></span>

    <span data-ttu-id="130ee-113">Le dossier d’installation par défaut est *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span><span class="sxs-lookup"><span data-stu-id="130ee-113">The default installation folder is *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.</span></span>

    -   <span data-ttu-id="130ee-114">Pour modifier le dossier dans lequel MED-V doit être installé, cliquez sur **modifier** et naviguez jusqu’à un dossier existant.</span><span class="sxs-lookup"><span data-stu-id="130ee-114">To change the folder where MED-V should be installed, click **Change** and browse to an existing folder.</span></span>

4.  <span data-ttu-id="130ee-115">Cliquez sur **Suivant**.</span><span class="sxs-lookup"><span data-stu-id="130ee-115">Click **Next**.</span></span>

5.  <span data-ttu-id="130ee-116">Dans l’écran **prêt à installer le programme** , cliquez sur **installer**.</span><span class="sxs-lookup"><span data-stu-id="130ee-116">On the **Ready to Install the Program** screen, click **Install**.</span></span>

    <span data-ttu-id="130ee-117">L’installation du serveur MED-V démarre.</span><span class="sxs-lookup"><span data-stu-id="130ee-117">The MED-V server installation starts.</span></span> <span data-ttu-id="130ee-118">Cela peut prendre quelques minutes et l’écran risque de ne pas afficher de texte.</span><span class="sxs-lookup"><span data-stu-id="130ee-118">This can take several minutes, and the screen might not display text.</span></span> <span data-ttu-id="130ee-119">Lors de l’installation, plusieurs écrans de progression apparaissent.</span><span class="sxs-lookup"><span data-stu-id="130ee-119">During installation, several progress screens appear.</span></span> <span data-ttu-id="130ee-120">Si un message s’affiche, suivez les instructions fournies.</span><span class="sxs-lookup"><span data-stu-id="130ee-120">If a message appears, follow the instructions provided.</span></span>

6.  <span data-ttu-id="130ee-121">Lorsque l’écran de fin de l' **Assistant InstallShield** s’affiche, cliquez sur **Terminer** pour terminer l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="130ee-121">When the **InstallShield Wizard Completed** screen appears, click **Finish** to complete the wizard.</span></span>

**<span data-ttu-id="130ee-122">Remarque</span><span class="sxs-lookup"><span data-stu-id="130ee-122">Note</span></span>**  
<span data-ttu-id="130ee-123">Si vous installez le serveur MED-V via Microsoft Remote Desktop, utilisez la syntaxe suivante: **mstsc/admin**. Assurez-vous que votre session RDP s’adresse à la console.</span><span class="sxs-lookup"><span data-stu-id="130ee-123">If you are installing the MED-V server via Microsoft Remote Desktop, use the following syntax: **mstsc/admin**. Ensure that your RDP session is directed to the console.</span></span>



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a><span data-ttu-id="130ee-124">Comment configurer le serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="130ee-124">How to Configure the MED-V Server</span></span>


<span data-ttu-id="130ee-125">Les paramètres serveur suivants peuvent être configurés:</span><span class="sxs-lookup"><span data-stu-id="130ee-125">The following server settings can be configured:</span></span>

-   [<span data-ttu-id="130ee-126">Connexions</span><span class="sxs-lookup"><span data-stu-id="130ee-126">Connections</span></span>](#bkmk-configuringconnections)

-   [<span data-ttu-id="130ee-127">Images</span><span class="sxs-lookup"><span data-stu-id="130ee-127">Images</span></span>](#bkmk-configuringimages)

-   [<span data-ttu-id="130ee-128">Autorisations</span><span class="sxs-lookup"><span data-stu-id="130ee-128">Permissions</span></span>](#bkmk-configuringpermissions)

-   [<span data-ttu-id="130ee-129">Rapports</span><span class="sxs-lookup"><span data-stu-id="130ee-129">Reports</span></span>](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a><span data-ttu-id="130ee-130">Configuration de connexions</span><span class="sxs-lookup"><span data-stu-id="130ee-130">Configuring Connections</span></span>

**<span data-ttu-id="130ee-131">Pour configurer des connexions</span><span class="sxs-lookup"><span data-stu-id="130ee-131">To configure connections</span></span>**

1.  <span data-ttu-id="130ee-132">Dans le menu Démarrer de Windows, sélectionnez **tous les programmes &gt; med-v &gt; med-v Server Configuration Manager**.</span><span class="sxs-lookup"><span data-stu-id="130ee-132">On the Windows Start menu, select **All Programs &gt; MED-V &gt; MED-V Server Configuration Manager**.</span></span>

    **<span data-ttu-id="130ee-133">Remarque</span><span class="sxs-lookup"><span data-stu-id="130ee-133">Note</span></span>**  
    <span data-ttu-id="130ee-134">Remarque: Si vous avez activé la case à cocher **lancer med-v Server Configuration Manager** lors de l’installation du serveur, le gestionnaire de configuration du serveur med-v s’exécute automatiquement à la fin de l’installation du serveur.</span><span class="sxs-lookup"><span data-stu-id="130ee-134">Note: If you selected the **Launch MED-V Server Configuration Manager** check box during the server installation, the MED-V server configuration manager starts automatically after the server installation is complete.</span></span>



~~~
The MED-V Server Configuration Manager appears.
~~~

2. <span data-ttu-id="130ee-135">Dans l’onglet **connexions** , configurez les paramètres de connexions client suivants:</span><span class="sxs-lookup"><span data-stu-id="130ee-135">On the **Connections** tab, configure the following client connections settings:</span></span>

   -   <span data-ttu-id="130ee-136">**Activer les connexions non chiffrées (https) (à l’aide du port**) activez cette case à cocher pour activer les connexions non chiffrées à l’aide d’un port spécifié.</span><span class="sxs-lookup"><span data-stu-id="130ee-136">**Enable unencrypted connections (http), using port**—Select this check box to enable unencrypted connections using a specified port.</span></span> <span data-ttu-id="130ee-137">Dans la zone Port, entrez le port de serveur sur lequel accepter les connexions non chiffrées (http).</span><span class="sxs-lookup"><span data-stu-id="130ee-137">In the port box, enter the server port on which to accept unencrypted connections (http).</span></span>

   -   <span data-ttu-id="130ee-138">**Activer les connexions chiffrées (https), à l’aide du port**: activez cette case à cocher pour activer les connexions chiffrées à l’aide d’un port spécifié.</span><span class="sxs-lookup"><span data-stu-id="130ee-138">**Enable encrypted connections (https), using port**—Select this check box to enable encrypted connections using a specified port.</span></span> <span data-ttu-id="130ee-139">Dans la zone Port, entrez le port de serveur sur lequel accepter les connexions chiffrées (https).</span><span class="sxs-lookup"><span data-stu-id="130ee-139">In the port box, enter the server port on which to accept encrypted connections (https).</span></span>

       <span data-ttu-id="130ee-140">HTTPS est une configuration facultative qui peut être définie pour garantir la sécurité des transactions entre le serveur MED-V et les clients MED-V.</span><span class="sxs-lookup"><span data-stu-id="130ee-140">Https is an optional configuration which can be set to ensure secure transactions between the MED-V server and MED-V clients.</span></span> <span data-ttu-id="130ee-141">Pour configurer https, vous devez effectuer les procédures suivantes:</span><span class="sxs-lookup"><span data-stu-id="130ee-141">To configure https, you must perform the following procedures:</span></span>

       -   <span data-ttu-id="130ee-142">Configurer un certificat sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="130ee-142">Configure a certificate on the server.</span></span>

       -   <span data-ttu-id="130ee-143">Associez le certificat de serveur au port spécifié à l’aide de netsh.</span><span class="sxs-lookup"><span data-stu-id="130ee-143">Associate the server certificate with the port specified using netsh.</span></span> <span data-ttu-id="130ee-144">Pour plus d’informations, reportez-vous aux rubriques suivantes:</span><span class="sxs-lookup"><span data-stu-id="130ee-144">For information, see the following:</span></span>

           -   [<span data-ttu-id="130ee-145">Commandes netsh pour le protocole HTTP (Hypertext Transfer Protocol)</span><span class="sxs-lookup"><span data-stu-id="130ee-145">Netsh Commands for Hypertext Transfer Protocol (HTTP)</span></span>](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [<span data-ttu-id="130ee-146">Procédure: configurer un port avec un certificat SSL</span><span class="sxs-lookup"><span data-stu-id="130ee-146">How to: Configure a Port with an SSL Certificate</span></span>](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [<span data-ttu-id="130ee-147">Procédure: configurer un port avec un certificat SSL</span><span class="sxs-lookup"><span data-stu-id="130ee-147">How to: Configure a Port with an SSL Certificate</span></span>](https://msdn.microsoft.com/library/ms733791.aspx)

3. <span data-ttu-id="130ee-148">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="130ee-148">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringimages"></a><span data-ttu-id="130ee-149">Configuration d’images</span><span class="sxs-lookup"><span data-stu-id="130ee-149">Configuring Images</span></span>

**<span data-ttu-id="130ee-150">Pour configurer des images</span><span class="sxs-lookup"><span data-stu-id="130ee-150">To configure images</span></span>**

1.  <span data-ttu-id="130ee-151">Cliquez sur l’onglet **images** .</span><span class="sxs-lookup"><span data-stu-id="130ee-151">Click the **Images** tab.</span></span>

2.  <span data-ttu-id="130ee-152">Configurez les paramètres de gestion d’image suivants:</span><span class="sxs-lookup"><span data-stu-id="130ee-152">Configure the following image management settings:</span></span>

    -   <span data-ttu-id="130ee-153">**Annuaire VMS**: Annuaire d’ordinateur virtuel (répertoire dans lequel les images sont stockées).</span><span class="sxs-lookup"><span data-stu-id="130ee-153">**VMs Directory**—The virtual machine directory (the directory where the images are stored).</span></span> <span data-ttu-id="130ee-154">Ce champ contient un chemin d’accès UNC au répertoire image sur le serveur de distribution d’images qui doit être accessible à partir du serveur MED-V.</span><span class="sxs-lookup"><span data-stu-id="130ee-154">This field contains a UNC path to the image directory on the image distribution server that should be accessible from the MED-V server.</span></span>

    -   <span data-ttu-id="130ee-155">**URL VMS**: emplacement du serveur sur lequel les images sont stockées.</span><span class="sxs-lookup"><span data-stu-id="130ee-155">**VMs URL**—The location of the server where the images are stored.</span></span>

3.  <span data-ttu-id="130ee-156">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="130ee-156">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringpermissions"></a><span data-ttu-id="130ee-157">Configuration des autorisations</span><span class="sxs-lookup"><span data-stu-id="130ee-157">Configuring Permissions</span></span>

**<span data-ttu-id="130ee-158">Pour configurer des autorisations</span><span class="sxs-lookup"><span data-stu-id="130ee-158">To configure permissions</span></span>**

1.  <span data-ttu-id="130ee-159">Cliquez sur l’onglet **autorisations** .</span><span class="sxs-lookup"><span data-stu-id="130ee-159">Click the **Permissions** tab.</span></span>

2.  <span data-ttu-id="130ee-160">La liste de tous les utilisateurs qui peuvent se connecter est fournie.</span><span class="sxs-lookup"><span data-stu-id="130ee-160">A list of all users who can log in is provided.</span></span> <span data-ttu-id="130ee-161">Pour appliquer des autorisations de lecture et d’écriture à un utilisateur, activez la case à cocher en regard de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="130ee-161">To apply read and write permissions to a user, select the check box next to the user.</span></span> <span data-ttu-id="130ee-162">Pour appliquer des autorisations en lecture seule à un utilisateur, décochez la case.</span><span class="sxs-lookup"><span data-stu-id="130ee-162">To apply read-only permissions to a user, clear the check box.</span></span>

3.  <span data-ttu-id="130ee-163">Pour ajouter des utilisateurs ou des groupes de domaines, cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="130ee-163">To add domain users or groups, click **Add**.</span></span>

    <span data-ttu-id="130ee-164">La boîte de dialogue **entrer un nom d’utilisateur ou de groupe** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="130ee-164">The **Enter User or Group names** dialog box appears.</span></span>

    1.  <span data-ttu-id="130ee-165">Sélectionnez utilisateurs ou groupes du domaine en effectuant l’une des opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="130ee-165">Select domain users or groups by doing one of the following:</span></span>

        -   <span data-ttu-id="130ee-166">Dans le champ **Entrez des noms d’utilisateur ou de groupe** , entrez un nom d’utilisateur ou de groupe qui existe dans le domaine ou qui existe en tant qu’utilisateur local ou groupe sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="130ee-166">In the **Enter User or Group names** field, type a user or group that exists in the domain or exists as a local user or group on the computer.</span></span> <span data-ttu-id="130ee-167">Puis cliquez sur **vérifier les noms** pour le résoudre au nom existant complet.</span><span class="sxs-lookup"><span data-stu-id="130ee-167">Then click **Check Names** to resolve it to the full existent name.</span></span>

        -   <span data-ttu-id="130ee-168">Cliquez sur **Rechercher** pour ouvrir la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** standard.</span><span class="sxs-lookup"><span data-stu-id="130ee-168">Click **Find** to open the standard **Select Users or Groups** dialog box.</span></span> <span data-ttu-id="130ee-169">Sélectionnez ensuite utilisateurs ou groupes de domaines.</span><span class="sxs-lookup"><span data-stu-id="130ee-169">Then select domain users or groups.</span></span>

    2.  <span data-ttu-id="130ee-170">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="130ee-170">Click **OK**.</span></span>

4.  <span data-ttu-id="130ee-171">Pour supprimer des utilisateurs ou des groupes de domaines, sélectionnez un utilisateur ou un groupe, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="130ee-171">To remove domain users or groups, select a user or group and click **Remove**.</span></span>

5.  <span data-ttu-id="130ee-172">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="130ee-172">Click **OK**.</span></span>

### <a href="" id="bkmk-configuringreports"></a><span data-ttu-id="130ee-173">Configuration de rapports</span><span class="sxs-lookup"><span data-stu-id="130ee-173">Configuring Reports</span></span>

**<span data-ttu-id="130ee-174">Pour configurer des rapports</span><span class="sxs-lookup"><span data-stu-id="130ee-174">To configure reports</span></span>**

1.  <span data-ttu-id="130ee-175">Cliquez sur l’onglet **rapports** .</span><span class="sxs-lookup"><span data-stu-id="130ee-175">Click the **Reports** tab.</span></span>

2.  <span data-ttu-id="130ee-176">Pour prendre en charge les rapports, sélectionnez **activer les rapports**.</span><span class="sxs-lookup"><span data-stu-id="130ee-176">To support reports, select **Enable reports**.</span></span>

3.  <span data-ttu-id="130ee-177">Dans la zone **chaîne de connexion** , entrez une chaîne de connexion pour la base de données MSSQL.</span><span class="sxs-lookup"><span data-stu-id="130ee-177">In the **Connection String** box, enter a connection string for the MSSQL database.</span></span>

    -   <span data-ttu-id="130ee-178">Lorsque SQL Server est installé sur un serveur distant, utilisez la chaîne de connexion suivante:</span><span class="sxs-lookup"><span data-stu-id="130ee-178">When SQL Server is installed on a remote server, use the following connection string:</span></span>

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **<span data-ttu-id="130ee-179">Remarque</span><span class="sxs-lookup"><span data-stu-id="130ee-179">Note</span></span>**  
        <span data-ttu-id="130ee-180">Remarque: pour vous connecter à SQL Express, utilisez:</span><span class="sxs-lookup"><span data-stu-id="130ee-180">Note: To connect to SQL Express, use:</span></span> `Data Source=<ServerName>\sqlexpress.`



4.  <span data-ttu-id="130ee-181">Pour créer la base de données, cliquez sur **créer une base de données**.</span><span class="sxs-lookup"><span data-stu-id="130ee-181">To create the database, click **Create Database**.</span></span>

5.  <span data-ttu-id="130ee-182">Pour tester la connexion, cliquez sur **tester la connexion**.</span><span class="sxs-lookup"><span data-stu-id="130ee-182">To test the connection, click **Test Connection**.</span></span>

6.  <span data-ttu-id="130ee-183">Pour configurer les options de suppression de la base de données, cliquez sur **effacer les options**.</span><span class="sxs-lookup"><span data-stu-id="130ee-183">To configure database clearing options, click **Clear Options**.</span></span>

    <span data-ttu-id="130ee-184">La boîte **de dialogue Effacer les options de la base de données** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="130ee-184">The **Clear Database Options** dialog box appears.</span></span>

    1.  <span data-ttu-id="130ee-185">Choisissez l’une des options suivantes:</span><span class="sxs-lookup"><span data-stu-id="130ee-185">Choose one of the following options:</span></span>

        -   <span data-ttu-id="130ee-186">**Effacer les données de plus de**: effacer toutes les données antérieures au nombre de jours spécifié; dans la zone nombre, entrez un nombre de jours.</span><span class="sxs-lookup"><span data-stu-id="130ee-186">**Clear data older than**—Clear all data older than the number of days specified; in the number box, enter a number of days.</span></span>

        -   <span data-ttu-id="130ee-187">**Effacer toutes les données de la base de**données: effacez toutes les données existantes dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="130ee-187">**Clear all data from database**—Clear all existent data in the database.</span></span>

        -   <span data-ttu-id="130ee-188">**Déplacer une base de**données: supprimer la base de données.</span><span class="sxs-lookup"><span data-stu-id="130ee-188">**Drop database**—Delete the database.</span></span>

    2.  <span data-ttu-id="130ee-189">Cliquez sur **OK** pour appliquer les modifications et fermer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="130ee-189">Click **OK** to apply changes and close the dialog box.</span></span>

7.  <span data-ttu-id="130ee-190">Cliquez sur **OK** pour enregistrer les modifications ou cliquez sur **Annuler** pour fermer la boîte de dialogue sans enregistrer les modifications.</span><span class="sxs-lookup"><span data-stu-id="130ee-190">Click **OK** to save the changes, or click **Cancel** to close the dialog box without saving changes.</span></span>

8.  <span data-ttu-id="130ee-191">Si vous y êtes invité, redémarrez le service du serveur MED-V pour appliquer les modifications aux paramètres du réseau.</span><span class="sxs-lookup"><span data-stu-id="130ee-191">If prompted, restart the MED-V server service to apply changes to the network settings.</span></span>

## <span data-ttu-id="130ee-192">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="130ee-192">Related topics</span></span>


[<span data-ttu-id="130ee-193">Configurations prises en charge</span><span class="sxs-lookup"><span data-stu-id="130ee-193">Supported Configurations</span></span>](supported-configurationsmedv-orientation.md)

[<span data-ttu-id="130ee-194">Concevoir l'infrastructure de serveur MED-V</span><span class="sxs-lookup"><span data-stu-id="130ee-194">Design the MED-V Server Infrastructure</span></span>](design-the-med-v-server-infrastructure.md)









