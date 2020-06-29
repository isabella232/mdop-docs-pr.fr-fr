---
title: Compactage des disques durs virtuels MED-V
description: Compactage des disques durs virtuels MED-V
author: dansimp
ms.assetid: 5e6122d1-9847-4b33-adab-594919eec3c5
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: f71aefb1e4e901078b4d0a421065b7bd5acdf0ee
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10809858"
---
# Compactage des disques durs virtuels MED-V


Même s’il est facultatif, vous pouvez compacter le disque dur virtuel (VHD) pour récupérer l’espace libre sur le disque et réduire la taille du VHD avant de configurer l’image du PC virtuel Windows.

**Important**  Avant de continuer, créez une copie de sauvegarde de votre image Windows XP.

 

**Préparation du disque dur virtuel**

1.  Ouvrez votre image Windows XP.

    Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, sur **PC virtuel Windows**, puis double-cliquez sur votre image Windows XP.

2.  Effacez le cache DLL.

    1.  À l’invite de commandes dans l’ordinateur virtuel, tapez **SFC/CacheSize = 1**.

    2.  Redémarrez l’ordinateur virtuel.

    3.  À l’invite de commandes dans l’ordinateur virtuel, tapez **sfc/purgecache**.

3.  Supprimez les fichiers inutiles, tels que les programmes de désinstallation, les fichiers temporaires, les fichiers journaux, les fichiers de page, les dossiers partagés, etc.

4.  Désactiver la restauration du système. Vous pouvez également spécifier cette étape dans votre fichier Sysprep. inf.

    1.  Dans le **panneau**de configuration, double-cliquez sur **système**, puis sélectionnez l’onglet **restauration du système** .

    2.  Sélectionnez **désactiver la restauration du système**, puis cliquez sur **OK**.

5.  Définissez les tailles maximales du journal des événements et effacez tous les événements.

    1.  Ouvrez l’observateur d’événements.

        Cliquez sur **Démarrer**, sur **panneau de configuration**, double-cliquez sur **Outils d’administration**, puis double-cliquez sur **Observateur d’événements**.

    2.  Cliquez avec le bouton droit sur **application**, puis cliquez sur **Propriétés**.

    3.  Dans la zone **taille du journal** , définissez **taille maximale du journal** sur 512 Ko, puis sélectionnez **remplacer les événements selon les besoins**.

    4.  Cliquez sur **effacer le journal**. Dans la boîte de dialogue **Observateur d’événements** qui s’affiche, cliquez sur **non**.

    5.  Dans la fenêtre **Propriétés** , cliquez sur **OK**.

    6.  Répétez les étapes a à e pour les journaux **système** et de **sécurité** .

6.  Exécutez l’outil Nettoyage de disque.

    Cliquez **sur Démarrer**, **sur tous les programmes**, sur **accessoires**, sur **Outils système**, puis sur **nettoyage de disque**.

7.  Configurez votre fichier de page selon vos besoins.

    1.  Dans le **panneau de configuration**, double-cliquez sur **système**, puis sélectionnez l’onglet **avancé** .

    2.  Dans la zone **performance** , cliquez sur **paramètres**.

    3.  Dans la zone **mémoire virtuelle** , cliquez sur **modifier**.

    4.  Configurez les paramètres de votre fichier page.

8.  Fermez l’image Windows XP.

**Défragmentation et précompactage du disque dur virtuel**

1.  Dans **le panneau de configuration** de l’ordinateur hôte exécutant Windows 7, cliquez sur **Outils d’administration**, double-cliquez sur gestion de l' **ordinateur**, puis cliquez sur gestion des **disques**.

2.  À l’aide de la console de gestion des disques, joignez (montez) le disque dur virtuel, puis défragmentez le disque.

3.  À l’aide d’un outil d’extraction ISO, extrayez la précompact. ISO située dans le dossier C:\\Program Files\\Windows Virtual PC\\Integration composants.

4.  Utilisez le programme precompact.exe pour compresser le disque dur virtuel Windows XP.

5.  À l’aide de la console de gestion des disques, détachez le disque dur virtuel.

**Compression du disque dur virtuel**

1.  Ouvrez l’ordinateur virtuel Windows.

    Cliquez sur **Démarrer**, sur **tous les programmes**, sur **PC virtuel Windows**, puis sur **PC virtuel Windows**.

2.  Cliquez avec le bouton droit sur votre image Windows XP, puis sélectionnez **paramètres**.

3.  Cliquez sur **disque dur** pour la personne qui correspond à votre image Windows XP, puis cliquez sur **modifier**.

4.  Cliquez sur **Compact disque dur virtuel**.

5.  Cliquez sur **compact** , puis cliquez sur **OK**.

Créez une copie de sauvegarde de votre disque dur virtuel compacté.

## Rubriques connexes


[Configuration d'une image Windows Virtual PC pour MED-V](configuring-a-windows-virtual-pc-image-for-med-v.md)

[Informations techniques de référence pour MED-V](technical-reference-for-med-v.md)

 

 





