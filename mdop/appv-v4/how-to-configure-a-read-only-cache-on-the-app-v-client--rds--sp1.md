---
title: Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)
description: Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)
author: dansimp
ms.assetid: b6607fe2-6f92-4567-99f1-d8e3c8a591e0
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, appcompat, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 08/30/2016
ms.openlocfilehash: a44844ae9ffc3497151be7713f6a43fda0ccd8fa
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10807310"
---
# Procédure pour configurer un cache en lecture seule dans App-V Client (RDS)


**Important**  Pour pouvoir utiliser cette procédure, vous devez exécuter App-V 4,6, SP1.

 

Vous pouvez déployer le client App-V en utilisant un cache partagé rempli avec toutes les applications requises pour tous les utilisateurs. Vous configurez ensuite les clients App-V Remote Desktop Services (RDS) pour utiliser le même fichier de cache. Les utilisateurs peuvent accéder à des applications spécifiques à l’aide du processus de publication d’application-V. Dans la mesure où le cache est déjà préchargé avec toutes les applications, aucun flux n’est déclenché lorsqu’un utilisateur démarre une application. Toutefois, les packages utilisés pour préremplir le cache doivent être placés sur un serveur App-V qui prend en charge la diffusion en continu du protocole RTSP (Real Time Streaming Protocol) et qui accorde des autorisations d’accès aux clients App-V. Si vous publiez les applications à l’aide d’un serveur de gestion App-V, vous pouvez l’utiliser pour fournir cette fonction de diffusion en continu.

**Remarques**  Les détails décrits dans ces procédures sont uniquement destinés à des exemples. Vous pouvez utiliser différentes méthodes pour achever le processus global.

 

## Déploiement du client App-V dans un scénario RDS


Le processus de déploiement comporte quatre tâches principales:

-   Création et remplissage du fichier cache principal partagé

-   Copie du fichier cache partagé sur le serveur de stockage

-   Configuration du logiciel client App-V

-   Gestion du cycle de déploiement des mises à jour pour le fichier cache partagé après le déploiement initial

Les tâches suivantes nécessitent une planification soigneuse. Nous vous recommandons de préparer et de documenter un processus méthodique et reproductible à respecter par votre organisation. Cela est particulièrement important pour la préparation et le déploiement du fichier cache principal partagé et pour la gestion en continu des mises à jour de l’application, qui requièrent chacune une mise à jour du cache partagé principal. Utilisez les procédures suivantes pour effectuer ces tâches principales.

**Remarques**  Même si vous pouvez publier les applications à l’aide de plusieurs méthodes différentes, les procédures suivantes sont basées sur l’utilisation d’un serveur d’administration d’applications-V pour la publication.

 

**Pour configurer le cache en lecture seule pour le déploiement initial**

1. Configurez et configurez un serveur de gestion d’application-V pour la prise en charge de l’authentification des utilisateurs et de la publication.

2. Remplissez le dossier de contenu de ce serveur de gestion avec tous les packages d’application requis pour tous les utilisateurs.

3. Configurer un ordinateur intermédiaire sur lequel le client App-V est installé. Connectez-vous à l’ordinateur intermédiaire à l’aide d’un compte qui a accès à toutes les applications de sorte que l’ensemble complet d’applications soit publié sur l’ordinateur, puis diffusez le cache des applications afin qu’elles soient entièrement chargées.

   **Important**  
   L’ordinateur intermédiaire doit utiliser le même type de système d’exploitation et l’même architecture système que ceux utilisés par les VM sur lesquelles le client App-V sera exécuté.

     

4. Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés, car cela verrouille le fichier du cache.

   **Remarque**  
   Vous pouvez ou arrêter d’arrêter et de désactiver le service de virtualisation des applications, puis redémarrez l’ordinateur. Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.

     

5. Copiez le fichier cache Sftfs. FSD sur un réseau SAN sur lequel tous les serveurs RDS peuvent y accéder, par exemple dans un dossier partagé. Définissez les autorisations d’accès aux dossiers sur lecture seule pour le groupe tout le monde et sur contrôle total pour les administrateurs qui gèrent les mises à jour de fichier cache. L’emplacement du fichier cache peut être obtenu à partir de l’AppFS\\FileName. de Registre

   **Important**  
   Le fichier FSD doit être placé dans un emplacement dont la réactivité et la fiabilité sont égales aux performances de stockage attachées localement, par exemple un réseau SAN.

     

6. Installez le client App-V RDS sur chaque serveur RDS, puis configurez-le pour utiliser le cache en lecture seule en ajoutant les valeurs de clé de Registre suivantes à la clé AppFS sur le client. La clé AppFS est située dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\\] Microsoft\\SoftGrid\\4.5\\Client\\AppFS pour les ordinateurs 32 bits et dans HKEY \ _LOCAL \ _MACHINE \\SOFTWARE\\Wow6432Node\\Microsoft\\SoftGrid\\4.5\\Client\\AppFS pour les ordinateurs 64 bits.

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
   <td align="left"><p>chemin de FSD</p></td>
   <td align="left"><p>Spécifie le chemin d’accès du fichier cache partagé, par exemple \RDSServername\Sharefolder\SFTFS. FSD (obligatoire).</p></td>
   </tr>
   <tr class="even">
   <td align="left"><p>ReadOnlyFSD</p></td>
   <td align="left"><p>DWORD</p></td>
   <td align="left"><p>1</p></td>
   <td align="left"><p>Configure le client pour qu’il fonctionne en mode lecture seule. Cela permet de s’assurer que le client n’essaiera pas de transmettre les mises à jour au cache du package. (obligatoire)</p></td>
   </tr>
   <tr class="odd">
   <td align="left"><p>ErrorLogLocation</p></td>
   <td align="left"><p>String</p></td>
   <td align="left"><p>chemin du fichier journal des erreurs (. ETL)</p></td>
   <td align="left"><p>Entrée utilisée pour spécifier le chemin d’accès du journal des erreurs. Recommande. Utiliser un chemin d’accès local tel que C:\Logs\Sftfs.etl).</p></td>
   </tr>
   </tbody>
   </table>

     

7. Configurez chaque serveur RDS dans la batterie de serveurs pour utiliser le serveur de publication et utiliser la mise à jour de publication lorsque les utilisateurs se connectent. Lorsque l’utilisateur se connecte aux serveurs RDS, un cycle de mise à jour de publication se produit et publie toutes les applications pour lesquelles son compte est autorisé. Ces applications sont exécutées à partir du cache partagé.

**Pour configurer le client RDS pour la mise à niveau du package**

1.  Effectuez la mise à niveau et le test du package d’application.

2.  Mettez à niveau le package sur le serveur App-V. Ensuite, publiez et diffusez la nouvelle version des applications sur le client de l’ordinateur intermédiaire de sorte qu’elles soient entièrement chargées dans le cache.

3.  Redémarrez l’ordinateur intermédiaire en mode sans échec pour vous assurer que les pilotes ne sont pas démarrés.

    **Remarques**  Vous pouvez ou arrêter d’abord le service de virtualisation des applications dans services. msc, puis le redémarrer. Après avoir copié le fichier, n’oubliez pas d’activer et de redémarrer le service.

     

4.  Copiez le fichier cache Sftfs. FSD sur un réseau SAN sur lequel tous les serveurs RDS peuvent y accéder, par exemple dans un dossier partagé. Vous pouvez utiliser un autre nom de fichier, par exemple, SFTFS \ _V2. FSD, pour distinguer la nouvelle version.

5.  Pour configurer le client RDS App-V sur chaque serveur RDS dans la batterie de serveurs pour qu’il utilise le fichier cache partagé mis à jour, modifiez la valeur nom de fichier de la clé de Registre AppFS pour qu’elle pointe vers l’emplacement du fichier mis à jour, par exemple, \\\\RDSServername\\Sharefolder\\SFTFS\ _V2. FSD. Cela garantit que chaque serveur RDS reçoit la copie mise à jour du cache lorsque les pilotes d’application-vclient redémarrent.

    **Important**  Vous devez redémarrer les serveurs RDS pour pouvoir utiliser le fichier cache partagé mis à jour.

     

## Utiliser des liens symboliques lors de la mise à niveau du cache


Au lieu de modifier la valeur de nom de fichier de la clé AppFS chaque fois qu’un nouveau fichier de cache est déployé contenant des packages nouveaux ou mis à niveau, vous pouvez utiliser un lien symbolique dans les systèmes d’exploitation suivants: Windows Vista, Windows 7 et Windows Server 2008. Pour plus d’informations sur les liens symboliques, voir [liens symboliques](https://go.microsoft.com/fwlink/?LinkId=157626) ( https://go.microsoft.com/fwlink/?LinkId=157626) . En revanche, Windows XP ne prend pas en charge l’utilisation de liens symboliques et vous devez plutôt utiliser des points de jonction. Pour plus d’informations sur les jointures, reportez-vous à [l’article 205524](https://go.microsoft.com/fwlink/?LinkId=182553) de la base de connaissances Microsoft ( https://go.microsoft.com/fwlink/?LinkId=182553) et également à la jointure d’outil [v 1.05](https://go.microsoft.com/fwlink/?LinkId=182554) () https://go.microsoft.com/fwlink/?LinkId=182554) .

**Pour configurer un lien symbolique pour référencer le cache**

1.  Pendant la phase de déploiement initiale, ouvrez une fenêtre d’invite de commandes en tant qu’administrateur local sur le système d’exploitation hôte du serveur RDS.

2.  Créez un lien symbolique à l’aide de la commande MKLINK, puis configurez-le pour qu’il pointe sur le fichier Sftfs. FSD.

    **     mklink symlinkname \\\\rdshostserver\\sharefolder\\sftfs.fsd**

3.  Sur l’image de l’ordinateur virtuel VDI maître, ouvrez une fenêtre d’invite de commandes à l’aide de l’option **exécuter en tant qu’administrateur** , puis accordez des autorisations de lien distant pour permettre à l’ordinateur virtuel d’accéder au lien symbolique du système d’exploitation de l’hôte VDI. Par défaut, les autorisations de liaison distantes ne sont pas activées.

    **fsutil behavior Set SymlinkEvaluation R2R: 1**

    **Remarques**  Sur le serveur de stockage, les autorisations de liaison appropriées doivent être activées. En fonction de l’emplacement du lien et du fichier Sftfs. FSD, les autorisations sont **L2L: 1** ou **L2R: 1** ou **R2L: 1** ou **R2R: 1**.

     

4.  Lorsque vous configurez le client RDS App-V, définissez la valeur nom de fichier clé AppFS sur le chemin d’accès UNC du fichier FSD qui utilise le lien symbolique. Par exemple, définissez le nom de fichier sur \\\\VDIHostserver\\Symlinkname. Lorsque le client App-V accède au cache pour la première fois, le lien symbolique passe au client un handle vers le fichier du cache. Le client continue d’utiliser ce handle tant que le client est en cours d’exécution. La valeur du lien symbolique peut être mise à jour en toute sécurité même si l’ancien cache partagé est ouvert.

5.  Lorsque vous devez mettre à niveau un package ou ajouter un nouveau package au cache, suivez les étapes 1 à 4 de la procédure de mise à niveau. Ensuite, supprimez le lien symbolique et recréez-le pour qu’il pointe vers la nouvelle version du fichier cache partagé. Ainsi, chaque serveur RDS reçoit la copie mise à jour du cache lors du redémarrage des pilotes clients App-V. Lorsque le serveur RDS est redémarré, le client App-V reçoit un handle vers la copie mise à jour du cache, car le client utilise le chemin d’accès contenant le lien symbolique mis à jour. Les utilisateurs ont ensuite accès aux applications nouvelles et mises à jour.

## Rubriques connexes


[Procédure pour installer le serveur Application Virtualization Management Server](how-to-install-application-virtualization-management-server.md)

[Procédure pour installer manuellement Application Virtualization Client](how-to-manually-install-the-application-virtualization-client.md)

[Procédure pour installer le client via la ligne de commande](how-to-install-the-client-by-using-the-command-line-new.md)

 

 





