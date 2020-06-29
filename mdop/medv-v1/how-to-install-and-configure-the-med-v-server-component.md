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
# Procédure pour installer et configurer le composant serveur MED-V


Cette section explique comment [installer](#bkmk-howtoinstallthemedvserver) et [configurer](#bkmk-howtoconfigurethemedvserver) le serveur MED-V.

## <a href="" id="bkmk-howtoinstallthemedvserver"></a>Comment installer le serveur MED-V


**Pour installer le serveur MED-V**

1.  Installez le package. msi du serveur MED-V.

    Le package MED-V Server. msi est appelé *MED-V\_Server\_x.msi*, où x représente le numéro de version.

    Par exemple, *MED-V\_Server\_1.0.65.msi*.

2.  Lorsque l’écran d’accueil de l' **Assistant InstallShield** s’affiche, cliquez sur **suivant**.

3.  Dans l’écran **contrat de licence** , lisez le contrat de licence, cliquez sur **J’accepte les termes du contrat de licence**, puis cliquez sur **suivant**.

    L’écran **dossier de destination** s’affiche avec le dossier d’installation par défaut affiché.

    Le dossier d’installation par défaut est *%systemdrive%\\Program Files\\Microsoft Enterprise Desktop Virtualization\\*.

    -   Pour modifier le dossier dans lequel MED-V doit être installé, cliquez sur **modifier** et naviguez jusqu’à un dossier existant.

4.  Cliquez sur **Suivant**.

5.  Dans l’écran **prêt à installer le programme** , cliquez sur **installer**.

    L’installation du serveur MED-V démarre. Cela peut prendre quelques minutes et l’écran risque de ne pas afficher de texte. Lors de l’installation, plusieurs écrans de progression apparaissent. Si un message s’affiche, suivez les instructions fournies.

6.  Lorsque l’écran de fin de l' **Assistant InstallShield** s’affiche, cliquez sur **Terminer** pour terminer l’Assistant.

**Remarque**  
Si vous installez le serveur MED-V via Microsoft Remote Desktop, utilisez la syntaxe suivante: **mstsc/admin**. Assurez-vous que votre session RDP s’adresse à la console.



## <a href="" id="bkmk-howtoconfigurethemedvserver"></a>Comment configurer le serveur MED-V


Les paramètres serveur suivants peuvent être configurés:

-   [Connexions](#bkmk-configuringconnections)

-   [Images](#bkmk-configuringimages)

-   [Autorisations](#bkmk-configuringpermissions)

-   [Rapports](#bkmk-configuringreports)

### <a href="" id="bkmk-configuringconnections"></a>Configuration de connexions

**Pour configurer des connexions**

1.  Dans le menu Démarrer de Windows, sélectionnez **tous les programmes &gt; med-v &gt; med-v Server Configuration Manager**.

    **Remarque**  
    Remarque: Si vous avez activé la case à cocher **lancer med-v Server Configuration Manager** lors de l’installation du serveur, le gestionnaire de configuration du serveur med-v s’exécute automatiquement à la fin de l’installation du serveur.



~~~
The MED-V Server Configuration Manager appears.
~~~

2. Dans l’onglet **connexions** , configurez les paramètres de connexions client suivants:

   -   **Activer les connexions non chiffrées (https) (à l’aide du port**) activez cette case à cocher pour activer les connexions non chiffrées à l’aide d’un port spécifié. Dans la zone Port, entrez le port de serveur sur lequel accepter les connexions non chiffrées (http).

   -   **Activer les connexions chiffrées (https), à l’aide du port**: activez cette case à cocher pour activer les connexions chiffrées à l’aide d’un port spécifié. Dans la zone Port, entrez le port de serveur sur lequel accepter les connexions chiffrées (https).

       HTTPS est une configuration facultative qui peut être définie pour garantir la sécurité des transactions entre le serveur MED-V et les clients MED-V. Pour configurer https, vous devez effectuer les procédures suivantes:

       -   Configurer un certificat sur le serveur.

       -   Associez le certificat de serveur au port spécifié à l’aide de netsh. Pour plus d’informations, reportez-vous aux rubriques suivantes:

           -   [Commandes netsh pour le protocole HTTP (Hypertext Transfer Protocol)](https://go.microsoft.com/fwlink/?LinkId=183314)

           -   [Procédure: configurer un port avec un certificat SSL](https://go.microsoft.com/fwlink/?LinkID=183315)

           -   [Procédure: configurer un port avec un certificat SSL](https://msdn.microsoft.com/library/ms733791.aspx)

3. Cliquez sur **OK**.

### <a href="" id="bkmk-configuringimages"></a>Configuration d’images

**Pour configurer des images**

1.  Cliquez sur l’onglet **images** .

2.  Configurez les paramètres de gestion d’image suivants:

    -   **Annuaire VMS**: Annuaire d’ordinateur virtuel (répertoire dans lequel les images sont stockées). Ce champ contient un chemin d’accès UNC au répertoire image sur le serveur de distribution d’images qui doit être accessible à partir du serveur MED-V.

    -   **URL VMS**: emplacement du serveur sur lequel les images sont stockées.

3.  Cliquez sur **OK**.

### <a href="" id="bkmk-configuringpermissions"></a>Configuration des autorisations

**Pour configurer des autorisations**

1.  Cliquez sur l’onglet **autorisations** .

2.  La liste de tous les utilisateurs qui peuvent se connecter est fournie. Pour appliquer des autorisations de lecture et d’écriture à un utilisateur, activez la case à cocher en regard de l’utilisateur. Pour appliquer des autorisations en lecture seule à un utilisateur, décochez la case.

3.  Pour ajouter des utilisateurs ou des groupes de domaines, cliquez sur **Ajouter**.

    La boîte de dialogue **entrer un nom d’utilisateur ou de groupe** s’affiche.

    1.  Sélectionnez utilisateurs ou groupes du domaine en effectuant l’une des opérations suivantes:

        -   Dans le champ **Entrez des noms d’utilisateur ou de groupe** , entrez un nom d’utilisateur ou de groupe qui existe dans le domaine ou qui existe en tant qu’utilisateur local ou groupe sur l’ordinateur. Puis cliquez sur **vérifier les noms** pour le résoudre au nom existant complet.

        -   Cliquez sur **Rechercher** pour ouvrir la boîte de dialogue **Sélectionner des utilisateurs ou des groupes** standard. Sélectionnez ensuite utilisateurs ou groupes de domaines.

    2.  Cliquez sur **OK**.

4.  Pour supprimer des utilisateurs ou des groupes de domaines, sélectionnez un utilisateur ou un groupe, puis cliquez sur **supprimer**.

5.  Cliquez sur **OK**.

### <a href="" id="bkmk-configuringreports"></a>Configuration de rapports

**Pour configurer des rapports**

1.  Cliquez sur l’onglet **rapports** .

2.  Pour prendre en charge les rapports, sélectionnez **activer les rapports**.

3.  Dans la zone **chaîne de connexion** , entrez une chaîne de connexion pour la base de données MSSQL.

    -   Lorsque SQL Server est installé sur un serveur distant, utilisez la chaîne de connexion suivante:

        `Data Source=<ServerName>;Initial Catalog=<DBName>;uid=sa;pwd=<Password>;`

        **Remarque**  
        Remarque: pour vous connecter à SQL Express, utilisez: `Data Source=<ServerName>\sqlexpress.`



4.  Pour créer la base de données, cliquez sur **créer une base de données**.

5.  Pour tester la connexion, cliquez sur **tester la connexion**.

6.  Pour configurer les options de suppression de la base de données, cliquez sur **effacer les options**.

    La boîte **de dialogue Effacer les options de la base de données** s’affiche.

    1.  Choisissez l’une des options suivantes:

        -   **Effacer les données de plus de**: effacer toutes les données antérieures au nombre de jours spécifié; dans la zone nombre, entrez un nombre de jours.

        -   **Effacer toutes les données de la base de**données: effacez toutes les données existantes dans la base de données.

        -   **Déplacer une base de**données: supprimer la base de données.

    2.  Cliquez sur **OK** pour appliquer les modifications et fermer la boîte de dialogue.

7.  Cliquez sur **OK** pour enregistrer les modifications ou cliquez sur **Annuler** pour fermer la boîte de dialogue sans enregistrer les modifications.

8.  Si vous y êtes invité, redémarrez le service du serveur MED-V pour appliquer les modifications aux paramètres du réseau.

## Rubriques connexes


[Configurations prises en charge](supported-configurationsmedv-orientation.md)

[Concevoir l'infrastructure de serveur MED-V](design-the-med-v-server-infrastructure.md)









