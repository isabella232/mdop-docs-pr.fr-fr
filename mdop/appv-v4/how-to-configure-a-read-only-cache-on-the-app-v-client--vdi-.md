---
title: Procédure pour configurer un cache en lecture seule dans App-V Client (VDI)
description: Procédure pour configurer un cache en lecture seule dans App-V Client (VDI)
author: dansimp
ms.assetid: 7a41e017-9e23-4a6a-a659-04d23f008b83
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: 114f9dfbf55a3f62b6bc8bec6b37a659ffbfaf56
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807309"
---
# Procédure pour configurer un cache en lecture seule dans App-V Client (VDI)


Dans Microsoft Application Virtualization (App-V) 4,6, le client prend en charge l’utilisation d’une mémoire cache en lecture seule partagée. Le cache en lecture seule partagé permet au client d’utiliser efficacement l’espace disque dans un système de bureau virtuel, dans lequel les utilisateurs exécutent des applications sur des machines virtuelles hébergées dans un environnement serveur du centre de données et partagent le stockage réseau sur un réseau de zone de stockage. Les procédures suivantes fournissent une vue d’ensemble du processus requis pour implémenter le client App-V dans l’une des principales architectures VDI, connu sous le nom de «VM en pool» ou «VM statique». Il est supposé que vous êtes familiarisé avec la planification, le déploiement et l’exploitation du système App-V et de ses composants, ainsi que de l’opération et de la gestion du serveur VDI. Pour plus d’informations sur App-V, voir [virtualisation des applications](https://go.microsoft.com/fwlink/?LinkId=122939) (https://go.microsoft.com/fwlink/?LinkId=122939)

**Remarques**  Les détails décrits dans ces procédures sont uniquement destinés à des exemples. Vous pouvez utiliser différentes méthodes pour achever le processus global.

 

## Déploiement du client App-V dans un scénario VDI


Vous pouvez déployer le client App-V dans un scénario VDI en utilisant un cache en lecture seule partagé qui a été rempli avec toutes les applications requises pour tous les utilisateurs. Vous configurez ensuite l’image de l’ordinateur virtuel VDI maître de telle sorte que tous les clients App-V utilisent le même fichier de cache. Les utilisateurs peuvent accéder à des applications spécifiques à l’aide du processus de publication d’application-V. Dans la mesure où le cache est déjà préchargé avec toutes les applications, aucun flux n’est déclenché lorsqu’un utilisateur démarre une application. Toutefois, les packages utilisés pour préremplir le cache doivent être placés sur un serveur App-V qui prend en charge la diffusion en continu du protocole RTSP (Real Time Streaming Protocol) et qui accorde des autorisations d’accès aux clients App-V. Si vous publiez les applications à l’aide d’un serveur de gestion App-V, vous pouvez l’utiliser pour fournir cette fonction de diffusion en continu.

Le processus de déploiement comporte quatre tâches principales:

-   Création et remplissage du fichier cache principal partagé

-   Copie du fichier cache partagé vers l’espace de stockage du serveur VDI

-   Configuration du logiciel client App-V sur l’image maître d’infrastructure VDI

-   Gestion du cycle de déploiement des mises à jour pour le fichier cache partagé après le déploiement initial

Les tâches suivantes nécessitent une planification soigneuse. Nous vous recommandons de préparer et de documenter un processus méthodique et reproductible à respecter par votre organisation. Ceci est particulièrement important pour la préparation initiale et le déploiement du fichier cache principal partagé et pour la gestion des mises à jour de l’application, qui requièrent chacune une mise à jour du cache partagé maître. Utilisez les procédures suivantes pour effectuer ces tâches principales.

**Remarques**  Même si vous pouvez publier les applications à l’aide de plusieurs méthodes différentes, les procédures suivantes sont basées sur l’utilisation d’un serveur de gestion d’applications-V pour la publication.

 

**Pour configurer le cache en lecture seule pour le déploiement initial dans un scénario d’infrastructure VDI en pool ou d’infrastructure virtuelle VM**

1. Configurez et configurez un serveur d’administration d’applications-V dans un VM sur le serveur VDI pour fournir une authentification et une prise en charge de la publication.

2. Remplissez le dossier de contenu de ce serveur de gestion avec tous les packages d’application requis pour tous les utilisateurs.

3. Configurer un ordinateur intermédiaire sur lequel le client App-V est installé. Connectez-vous à l’ordinateur intermédiaire à l’aide d’un compte qui a accès à toutes les applications de sorte que l’ensemble complet d’applications soit publié sur l’ordinateur, puis diffusez le cache des applications afin qu’elles soient entièrement chargées.

   **Important**  
   L’ordinateur intermédiaire doit utiliser le même type de système d’exploitation et l’même architecture système que ceux utilisés par les VM sur lesquelles le client App-V sera exécuté.

     

4. Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés, ce qui verrouille le fichier de cache.

   **Remarque**  
   Vous pouvez également arrêter et désactiver le service de virtualisation des applications, puis redémarrer l’ordinateur. Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.

     

5. Copiez le fichier cache Sftfs. FSD sur le réseau de stockage du serveur VDI sur lequel tous les ordinateurs virtuels peuvent y accéder, par exemple dans un dossier partagé. Définissez les autorisations d’accès aux dossiers sur lecture seule pour le groupe tout le monde et sur contrôle total pour les administrateurs qui gèrent les mises à jour de fichier cache. L’emplacement du fichier cache peut être obtenu à partir de l’AppFS\\FileName. de Registre

   **Important**  
   Le fichier FSD doit se trouve dans un emplacement doté de la réactivité et de la fiabilité correspondant aux performances de stockage connectées localement, par exemple un réseau SAN.

     

6. Installez le client de bureau App-V sur l’image de l’ordinateur virtuel VDI maître, puis configurez-le pour qu’il utilise le cache en lecture seule en ajoutant les valeurs de clé de Registre suivantes à la clé AppFS sur le client. La clé AppFS est située dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\ [Wow6432Node\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS.

   <table>
   <colgroup>
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   <col width="25%" />
   </colgroup>
   <thead>
   <tr class="header">
   <th align="left">Clé</th>
   <th align="left">Type</th>
   <th align="left">Valeur</th>
   <th align="left">Objectif</th>
   </tr>
   </thead>
   <tbody>
   <tr class="odd">
   <td align="left"><p>FileName</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>Path to FSD</p></td>
   <td align="left"><p>Spécifie le chemin d’accès au fichier cache partagé, par exemple \VDIServername\Sharefolder\SFTFS. FSD (obligatoire).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>1</p></td>
   <td align="left"><p>Configure le client pour qu’il fonctionne en mode lecture seule. Cela permet de s’assurer que le client ne tente pas de diffuser en continu des mises à jour du cache du package. (obligatoire)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>chemin d’accès au fichier journal des erreurs (. ETL)</p></td>
   <td align="left"><p>Entrée utilisée pour spécifier le chemin d’accès au journal des erreurs. Recommande. Utiliser un chemin d’accès local tel que C:\Logs\Sftfs.etl).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configurez le client d’image VM maître de façon à utiliser le serveur de publication et à utiliser l’actualisation de publication lors de la connexion. Lorsque les utilisateurs ouvrent une session sur le système VDI et qu’ils sont créés à partir de l’image VM maître, un cycle d’actualisation de publication se produit et publie toutes les applications pour lesquelles leur compte est autorisé. Ces applications sont exécutées à partir du cache partagé.

**Pour configurer le client pour la mise à niveau du package dans un scénario VM en pool**

1.  Effectuez la mise à niveau et le test du package d’application.

2.  Mettez à niveau le package sur le serveur App-V. Ensuite, publiez et diffusez la nouvelle version des applications sur le client de l’ordinateur intermédiaire de sorte qu’elles soient entièrement chargées dans le cache.

3.  Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés.

    **Remarques**  Vous pouvez également arrêter et désactiver le service de virtualisation des applications dans services. msc, puis redémarrez l’ordinateur. Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.

     

4.  Copiez le fichier cache Sftfs. FSD sur le réseau de stockage du serveur VDI sur lequel tous les ordinateurs virtuels peuvent y accéder, par exemple dans un dossier partagé. Vous pouvez utiliser un autre nom de fichier, par exemple, SFTFS \ _V2. FSD, pour distinguer la nouvelle version.

5.  Pour configurer le client de bureau App-V sur l’image de l’ordinateur virtuel VDI maître pour utiliser le fichier cache partagé mis à jour, modifiez la valeur nom de fichier de clé de Registre AppFS pour qu’elle pointe vers l’emplacement du fichier mis à jour, par exemple, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Lorsqu’un utilisateur se déconnecte et se reconnecte, un nouvel ordinateur virtuel est créé pour eux à l’aide de l’image maître mise à jour. Tous leurs paramètres utilisateur seront conservés et appliqués au nouvel ordinateur virtuel. Ils ont alors accès aux applications mises à jour.

**Pour configurer le client pour la mise à niveau du package dans un scénario d’ordinateur virtuel statique**

1.  Effectuez la mise à niveau et le test du package d’application.

2.  Mettez à niveau le package sur le serveur App-V. Ensuite, publiez et diffusez la nouvelle version des applications sur le client de l’ordinateur intermédiaire de sorte que les applications soient entièrement chargées dans le cache.

3.  Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés.

    **Remarques**  Vous pouvez également arrêter et désactiver le service de virtualisation des applications dans services. msc, puis redémarrez l’ordinateur. Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.

     

4.  Copiez le fichier cache Sftfs. FSD sur le réseau de stockage du serveur VDI sur lequel tous les ordinateurs virtuels peuvent y accéder, par exemple dans un dossier partagé. Vous pouvez utiliser un autre nom de fichier, par exemple, SFTFS \ _V2. FSD, pour distinguer la nouvelle version.

5.  Pour configurer le client de bureau App-V sur l’image de l’ordinateur virtuel VDI maître pour utiliser le fichier cache partagé mis à jour, modifiez la valeur nom de fichier de clé de Registre AppFS pour qu’elle pointe vers l’emplacement du fichier mis à jour, par exemple, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Cela permet à tous les nouveaux utilisateurs d’obtenir la nouvelle version.

6.  Créez un script qui modifie la valeur nom de fichier de la clé AppFS pour la définir sur l’emplacement du cache mis à jour, par exemple, \\\\VDIServername\\Sharefolder\\SFTFS\ _V2. FSD. Configurez ce script pour qu’il s’exécute lorsque l’utilisateur se déconnecte ou qu’il se connecte pour qu’il s’exécute avant le début des pilotes clients App-V, par exemple, à l’aide des paramètres de stratégie de groupe. Lorsqu’un utilisateur se déconnecte et se reconnecte, son ordinateur virtuel existant est mis à jour et utilise la copie mise à jour du cache. Ils ont ensuite accès aux applications mises à jour.

## Utiliser des liens symboliques lors de la mise à niveau du cache


Au lieu de modifier la valeur nom de fichier de la clé AppFS chaque fois qu’un nouveau fichier cache contient des packages nouveaux ou mis à niveau, vous pouvez utiliser un lien symbolique dans les systèmes d’exploitation suivants: Windows Vista, Windows 7 et Windows Server 2008. Pour plus d’informations sur les liens symboliques, voir [liens symboliques](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . En revanche, Windows XP ne prend pas en charge l’utilisation de liens symboliques et vous devez plutôt utiliser des points de jonction. Pour plus d’informations sur les jointures, reportez-vous à [l’article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) de la base de connaissances Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) et également à la jointure d’outil [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) () https://go.microsoft.com/fwlink/?LinkId=182554) .

**Pour configurer un lien symbolique pour référencer le cache**

1.  Pendant la phase de déploiement initiale, ouvrez une fenêtre d’invite de commandes en tant qu’administrateur local sur le système d’exploitation hôte du serveur VDI.

2.  Créez un lien symbolique à l’aide de la commande MKLINK, puis configurez-le pour qu’il pointe sur le fichier Sftfs. FSD.

    **     mklink symlinkname \\\\vdihostserver\\sharefolder\\sftfs.fsd**

3.  Sur l’image de l’ordinateur virtuel VDI maître, ouvrez une fenêtre d’invite de commandes à l’aide de l’option **exécuter en tant qu’administrateur** , puis accordez des autorisations de lien distant pour permettre à l’ordinateur virtuel d’accéder au lien symbolique du système d’exploitation de l’hôte VDI. Par défaut, les autorisations de liaison distantes ne sont pas activées.

    **fsutil behavior Set SymlinkEvaluation R2R: 1**

    **Remarques**  Sur le serveur de stockage, les autorisations de liaison appropriées doivent être activées. En fonction de l’emplacement du lien et du fichier Sftfs. FSD, les autorisations sont **L2L: 1** ou **L2R: 1** ou **R2L: 1** ou **R2R: 1**.

     

4.  Lorsque vous configurez le client de bureau App-V sur l’image de l’ordinateur virtuel VDI maître, définissez la valeur nom de fichier de clé AppFS sur le chemin d’accès UNC du fichier FSD qui utilise le lien symbolique. par exemple, attribuez-lui la valeur \\\\VDIHostserver\\Symlinkname. Lorsque le client App-V accède au cache pour la première fois, le lien symbolique passe au client un handle vers le fichier du cache. Le client continue d’utiliser ce handle tant que le client est en cours d’exécution. La valeur du lien symbolique peut être mise à jour en toute sécurité même si l’ancien cache partagé est ouvert.

5.  Lorsque vous devez effectuer la mise à niveau d’un package ou ajouter un nouveau package au cache, suivez les étapes 1 à 5 de la procédure de mise à niveau pour le scénario d’ordinateur virtuel statique ou de pool. Ensuite, supprimez le lien symbolique et recréez-le pour qu’il pointe vers la nouvelle version du fichier cache partagé. Au redémarrage de l’ordinateur virtuel, le client reçoit un handle vers la copie mise à jour du cache, car l’ordinateur virtuel utilise le chemin d’accès contenant le lien symbolique mis à jour. Les utilisateurs ont ensuite accès aux applications nouvelles et mises à jour.

## Rubriques connexes


[Procédure pour installer le serveur Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





