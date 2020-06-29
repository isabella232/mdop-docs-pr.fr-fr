---
title: Comment configurer la prédéfinition d'une image
description: Comment configurer la prédéfinition d'une image
author: dansimp
ms.assetid: 92781b5a-208f-45a4-a078-ee90cf9efd9d
ms.reviewer: ''
manager: dansimp
ms.author: dansimp
ms.pagetype: mdop, virtualization
ms.mktglfcycl: deploy
ms.sitesec: library
ms.prod: w10
ms.date: 06/16/2016
ms.openlocfilehash: 38ddb7a69845aa4dbcb9cbd16b84dedc04438732
ms.sourcegitcommit: 354664bc527d93f80687cd2eba70d1eea024c7c3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2020
ms.locfileid: "10811736"
---
# Comment configurer la prédéfinition d'une image


**Remarques**  Le préstaging d’image est uniquement utile pour le téléchargement d’image initial. Il n’est pas pris en charge pour la mise à jour des images.

 

## Comment configurer la prédéfinition d'une image


**Pour configurer le prédéploiement d’une image**

1.  Sur l’ordinateur client, sous le répertoire du magasin d’images, créez un dossier pour l’image de pré-intermédiaire et nommez-la *images MED-V*.

    **Remarques**  Ce dossier doit être appelé *images MED-V*.

     

2.  Dans le dossier images MED-V, créez un sous-dossier et nommez-le *PrestagedImages*.

    **Remarques**  Ce dossier doit être appelé *PrestagedImages*.

     

3.  Pour appliquer la sécurité des listes de contrôle d’accès (ACL) au dossier *images MED-V* , définissez la liste de contrôle d’accès suivante:

    **Utilisateurs de AUTHORITY\\Authenticated NT: (OI) (CI) (CI) (accès spécial:)**

                                             **READ\_CONTROL**

                                    **SYNCHRONIZE**

                                    **FILE\_GENERIC\_READ**

                                    **FILE\_READ\_DATA**

    **                                 FICHIER \ _APPEND \ _DATA**

                                    **FILE\_READ\_EA**

                                    **FILE\_READ\_ATTRIBUTES**

    **AUTORITE AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Remarques**  Nous vous recommandons d’appliquer la sécurité d’ACL au dossier *images MED-V* .

     

4.  Pour appliquer la sécurité d’ACL au dossier *PrestagedImages* , définissez la liste de contrôle d’accès suivante:

    **Utilisateurs de AUTHORITY\\Authenticated NT: (OI) (CI) (CI) (accès spécial:)**

    **LIRE \ _CONTROL**

    **LEURS**

    **FICHIER \ _GENERIC \ _READ**

    **FICHIER \ _READ \ _DATA**

    **FICHIER \ _READ \ _EA**

    **FICHIER \ _READ \ _ATTRIBUTES**

    **AUTORITE AUTHORITY\\SYSTEM: (OI) (CI) F**

    **BUILTIN\\Administrators: (OI) (CI) F**

    **Remarques**  Nous vous recommandons d’appliquer la sécurité d’ACL au dossier *PrestagedImages*

     

5.  Envoyez les fichiers image (CKM et INDEX) dans le dossier *PrestagedImages* .

    **Remarques**  Une fois les fichiers image transférés dans le dossier préinstallation, il est recommandé d’exécuter une vérification de l’intégrité des données et de marquer les fichiers en lecture seule.

     

6.  Incluez le paramètre suivant dans l’installation du client MED-V: *Client.MSI VMSFOLDER = «C:\\MED-V images»*.

## Comment mettre à jour le lieu de préinstallation


**Pour mettre à jour l’emplacement antérieur**

1.  La clé de Registre *PrestagedImagesPath*, qui pointe vers l’emplacement d’image par défaut. Il se trouve dans le répertoire suivant:

    -   Sur un ordinateur x86- `KEY_LOCAL_MACHINE\SOFTWARE\Kidaro`

    -   Sur un x64- `HKEY_LOCAL_MACHINE\SOFTWARE\WOW6432node`

2.  Si l’image se trouve dans un autre emplacement, modifiez le chemin.

 

 





