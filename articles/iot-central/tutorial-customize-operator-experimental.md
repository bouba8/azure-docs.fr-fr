---
title: Personnaliser les vues de l’opérateur dans Azure IoT Central | Microsoft Docs
description: En tant que générateur, personnalisez les vues de l’opérateur dans votre application Azure IoT Central.
author: sandeeppujar
ms.author: sandeepu
ms.date: 01/29/2018
ms.topic: tutorial
ms.service: iot-central
services: iot-central
ms.custom: mvc
ms.openlocfilehash: 267a619fe32a8d4af0ee9cc8a5001d7a321c3098
ms.sourcegitcommit: 415742227ba5c3b089f7909aa16e0d8d5418f7fd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55765147"
---
# <a name="tutorial-customize-the-azure-iot-central-operators-view-new-ui-design"></a>Tutoriel : Personnaliser la vue de l’opérateur d’Azure IoT Central (nouvelle conception d’interface utilisateur)

Ce didacticiel vous montre, en tant que générateur, comment personnaliser la vue de l’opérateur de votre application. Lorsque vous apportez une modification à l’application en tant que générateur, vous pouvez afficher un aperçu de vue de l’opérateur dans l’application Microsoft Azure IoT Central.

Dans ce didacticiel, vous personnalisez l’application pour afficher des informations pertinentes sur le climatiseur raccordé pour un opérateur. Vos personnalisations permettent à l’opérateur de gérer les climatiseurs raccordés à l’application.

Ce tutoriel vous montre comment effectuer les opérations suivantes :

> [!div class="checklist"]
> * Configurer le tableau de bord de votre appareil
> * Configurer la disposition des paramètres de votre appareil
> * Configurer la disposition des propriétés de votre appareil
> * Afficher un aperçu de l’appareil en tant qu’opérateur
> * Configurer votre page d’accueil par défaut
> * Afficher un aperçu de la page d’accueil par défaut en tant qu’opérateur

[!INCLUDE [iot-central-experimental-note](../../includes/iot-central-experimental-note.md)]

## <a name="prerequisites"></a>Prérequis

Avant de commencer, vous devez effectuer les deux didacticiels précédents :

* [Définir un nouveau type d’appareil dans votre application Azure IoT Central](tutorial-define-device-type-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json).
* [Configurer des règles et des actions pour votre appareil](tutorial-configure-rules-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json).

## <a name="configure-your-device-dashboard"></a>Configurer le tableau de bord de votre appareil

En tant que générateur, vous pouvez définir les informations qui s’affichent sur le tableau de bord d’un appareil. Dans le tutoriel [Définir un nouveau type d’appareil dans votre application](tutorial-define-device-type-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json), vous avez ajouté un graphique linéaire et d’autres informations au tableau de bord **Climatiseur connecté**.

1. Pour modifier le modèle d’appareil **Climatiseur connecté**, choisissez **Modèles d’appareil** dans le menu de navigation de gauche :

    ![Page Modèles d’appareil](media/tutorial-customize-operator-experimental/devicetemplates.png)

2. Pour personnaliser le tableau de bord de l’appareil, cliquez sur le modèle d’appareil **Climatiseur connecté (1.0.0)** que vous avez créé dans le tutoriel [Définir un nouveau type d’appareil dans votre application](tutorial-define-device-type-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json).

3. Pour modifier le tableau de bord, sélectionnez l’onglet **Tableau de bord**.

4. Pour ajouter une vignette d’indicateur de performance clé (KPI) au tableau de bord, choisissez **KPI** :

    Pour définir le KPI, utilisez les informations du tableau suivant :

    | Paramètre     | Valeur |
    | ----------- | ----- |
    | Nom        | Température maximale |
    | Période  | 1 semaine précédente |
    | Type de mesure | Télémétrie |
    | Mesure | température |
    | Agrégation | Maximale |
    | Visibilité  | activé |

    ![Ajouter un KPI](media/tutorial-customize-operator-experimental/addkpi.png)

5. Cliquez sur **Enregistrer**. Vous pouvez maintenant voir la vignette du KPI sur le tableau de bord :

    ![Vignette de KPI](media/tutorial-customize-operator-experimental/temperaturekpi.png)

6. Pour déplacer ou redimensionner une vignette sur le tableau de bord, déplacez le pointeur de souris sur la vignette. Vous pouvez faire glisser la vignette vers un nouvel emplacement ou la redimensionner.

## <a name="configure-your-settings-layout"></a>Configurer la disposition de vos paramètres

En tant que générateur, vous pouvez également configurer la vue de l’opérateur des paramètres d’appareil. Un opérateur utilise l’onglet des paramètres de l’appareil pour configurer un appareil. Par exemple, un opérateur utilise l’onglet des paramètres pour définir la température cible du climatiseur connecté.

1. Pour modifier la disposition des paramètres de votre climatiseur connecté, choisissez l’onglet **Paramètres**.

2. Vous pouvez déplacer et redimensionner les vignettes de paramètres :

    ![Modifier la disposition des paramètres](media/tutorial-customize-operator-experimental/settingslayout.png)

## <a name="configure-your-properties-layout"></a>Configurer la disposition de vos propriétés

En plus du tableau de bord et des paramètres, vous pouvez également configurer la vue de l’opérateur des propriétés de l’appareil. Un opérateur utilise l’onglet des propriétés de l’appareil pour gérer les métadonnées de l’appareil. Par exemple, un opérateur utilise l’onglet des propriétés pour afficher le numéro de série d’un appareil ou mettre à jour les informations de contact du fabricant.

1. Pour modifier la disposition des propriétés de votre climatiseur connecté, choisissez l’onglet **Propriétés**.

2. Vous pouvez déplacer et redimensionner les champs de propriétés :

    ![Modifier la mise en page des propriétés](media/tutorial-customize-operator-experimental/propertieslayout.png)

## <a name="preview-the-connected-air-conditioner-device-as-an-operator"></a>Afficher un aperçu du climatiseur raccordé en tant qu’opérateur

Vous utilisez l’onglet **Modèles d’appareil** afin de personnaliser les onglets du tableau de bord, des paramètres et des propriétés pour un opérateur. Vous utilisez l’onglet **Device Explorer** pour voir et utiliser le modèle d’appareil.

1. Pour voir et utiliser le modèle du climatiseur connecté en tant qu’opérateur, accédez à la page **Device Explorer** et choisissez l’appareil simulé qu’IoT Central a généré à partir de votre modèle :

    ![Voir et utiliser le modèle d’appareil](media/tutorial-customize-operator-experimental/usetemplate.png)

2. Pour mettre à jour l’emplacement de cet appareil, choisissez **Propriétés** et modifiez la valeur dans la vignette Emplacement. Cliquez ensuite sur **Enregistrer** :

    ![Modifier une valeur de propriété](media/tutorial-customize-operator-experimental/editproperty.png)

3. Pour envoyer un paramètre à votre climatiseur raccordé, choisissez **Paramètres**, modifiez une valeur de paramètre dans une vignette, puis choisissez **Mettre à jour** :

    ![Envoyer un paramètre à l’appareil](media/tutorial-customize-operator-experimental/sendsetting.png)

    Lorsque l’appareil accuse réception de la nouvelle valeur de paramètre, le paramètre s’affiche comme étant **synchronisés** sur la vignette.

4. En tant qu’opérateur, vous pouvez afficher le tableau de bord de l’appareil tel qu’il est configuré par le générateur :

    ![Vue de l’opérateur du tableau de bord de l’appareil](media/tutorial-customize-operator-experimental/operatordashboard.png)

## <a name="configure-the-default-home-page"></a>Configurer la page d’accueil par défaut

Lorsqu’un générateur ou un opérateur se connecte à une application Azure IoT Central, il voit une page d’accueil. En tant que générateur, vous pouvez configurer le contenu de cette page d’accueil afin d’inclure le contenu le plus utile et pertinent pour un opérateur.

1. Pour personnaliser la page d’accueil par défaut, accédez à la page **Accueil**, puis sélectionnez **Modifier** en haut à droite de la page. Un panneau glissant apparaît sur la gauche avec une liste d’objets que vous pouvez ajouter dans la page **Accueil** :

    ![Page Générateur d’applications](media/tutorial-customize-operator-experimental/builderhome.png)

2. Pour personnaliser la page **Accueil**, ajoutez des vignettes à partir de la **bibliothèque**. Choisissez **Link** (Lier) et ajoutez les détails sur le site web de votre organisation. Cliquez ensuite sur **Enregistrer** :

    ![Ajouter un lien vers la page d'accueil](media/tutorial-customize-operator-experimental/addlink.png)

    > [!NOTE]
    > Vous pouvez également ajouter des liens vers des pages de votre application Azure IoT Central. Par exemple, vous pouvez ajouter un lien vers le tableau de bord d’un appareil ou une page de paramètres.

3. Si vous le souhaitez, choisissez **Image** et charger une image à afficher sur votre page d’accueil. Une image peut inclure une URL à laquelle vous pouvez accéder lorsque vous cliquez dessus :

    ![Ajouter une image à la page d’accueil](media/tutorial-customize-operator-experimental/addimage.png)

    Pour en savoir plus, consultez [Préparer et charger des images dans votre application Azure IoT Central](howto-prepare-images-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json).

## <a name="preview-the-default-home-page-as-an-operator"></a>Afficher un aperçu de la page d’accueil par défaut en tant qu’opérateur

Pour afficher un aperçu de la page d’accueil en tant qu’opérateur, cliquez sur **Terminé** en haut à droite de la page :

![Activer/désactiver le mode Création](media/tutorial-customize-operator-experimental/operatorviewhome.png)

Vous pouvez cliquer sur le lien et des vignettes d’image pour accéder aux URL que vous avez définies en tant que générateur.

## <a name="next-steps"></a>Étapes suivantes

Dans ce didacticiel, vous avez appris à personnaliser la vue de l’opérateur de l’application.

<!-- Repeat task list from intro -->
> [!div class="nextstepaction"]
> * Configurer le tableau de bord de votre appareil
> * Configurer la disposition des paramètres de votre appareil
> * Configurer la disposition des propriétés de votre appareil
> * Afficher un aperçu de l’appareil en tant qu’opérateur
> * Configurer votre page d’accueil par défaut
> * Afficher un aperçu de la page d’accueil par défaut en tant qu’opérateur

Maintenant que vous avez appris à personnaliser la vue de l’opérateur de l’application, les étapes suivantes suggérées consistent à :

* [Surveiller vos appareils (en tant qu’opérateur)](tutorial-monitor-devices-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json)
* [Ajouter un appareil à votre application (en tant qu’opérateur et développeur d’appareil)](tutorial-add-device-experimental.md?toc=/azure/iot-central-experimental/toc.json&bc=/azure/iot-central-experimental/breadcrumb/toc.json)
