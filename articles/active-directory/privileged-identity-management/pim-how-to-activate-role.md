---
title: Activer les rôles d’annuaire Azure AD dans PIM | Microsoft Docs
description: Découvrez comment activer des rôles d’annuaire Azure AD dans Azure AD Privileged Identity Management (PIM).
services: active-directory
documentationcenter: ''
author: rolyon
manager: mtillman
editor: ''
ms.service: active-directory
ms.topic: conceptual
ms.workload: identity
ms.subservice: pim
ms.date: 11/21/2018
ms.author: rolyon
ms.custom: pim
ms.collection: M365-identity-device-management
ms.openlocfilehash: 0023ac374ef70593d0ab2d9589c99d0f37e19ff8
ms.sourcegitcommit: 301128ea7d883d432720c64238b0d28ebe9aed59
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56189597"
---
# <a name="activate-my-azure-ad-directory-roles-in-pim"></a>Activer des rôles d’annuaire Azure AD dans PIM

Le service Azure Active Directory (Azure AD) Privileged Identity Management (PIM) simplifie la gestion par les entreprises de l’accès privilégié aux ressources dans Azure AD et d’autres services en ligne Microsoft, tels qu’Office 365 ou Microsoft Intune.  

Si vous êtes éligible à un rôle d’administrateur, vous pouvez activer ce rôle quand vous devez effectuer des actions privilégiées. Par exemple, si vous gérez occasionnellement des fonctionnalités d’Office 365, les administrateurs de rôle privilégié de votre organisation peuvent ne pas vous attribuer le rôle d’administrateur général permanent, étant donné que ce rôle affecte également les autres services. Au lieu de cela, ils peuvent vous attribuer des rôles Azure AD tels qu’administrateur Exchange Online. Vous pouvez faire une demande pour activer ce rôle lorsque vous avez besoin de ses privilèges. Vous aurez ainsi le contrôle d’administrateur pendant une période prédéterminée.

Cet article s’adresse aux administrateurs qui ont besoin d’activer leur rôle d’annuaire Azure AD dans PIM.

## <a name="activate-a-role"></a>Activer un rôle

Lorsque vous avez besoin d’endosser un rôle d’annuaire Azure AD, vous pouvez demander une activation à l’aide de l’option de navigation **Mes rôles** dans PIM.

1. Connectez-vous au [Portail Azure](https://portal.azure.com/).

1. Ouvrez **Azure AD Privileged Identity Management**. Pour plus d’informations sur l’ajout de la vignette PIM à votre tableau de bord, consultez [Commencer à utiliser PIM](pim-getting-started.md).

1. Cliquez sur **Rôles d’annuaire Azure AD**.

1. Cliquez sur **Mes rôles** pour afficher la liste de vos rôles d’annuaire Azure AD éligibles.

    ![Rôles d’annuaire Azure AD - Mes rôles](./media/pim-how-to-activate-role/directory-roles-my-roles.png)

1. Recherchez un rôle à activer.

    ![Rôles d’annuaire Azure AD - Liste Mes rôles](./media/pim-how-to-activate-role/directory-roles-my-roles-activate.png)

1. Cliquez sur **Activer** pour ouvrir le volet où se trouvent les informations d’activation du rôle.

1. Si votre rôle exige une authentification multifacteur (MFA), cliquez sur **Vérifier votre identité avant de continuer**. Vous ne devez vous authentifier qu’une seule fois par session.

    ![Vérification multifacteur avant activation du rôle](./media/pim-how-to-activate-role/directory-roles-my-roles-mfa.png)

1. Cliquez sur **Vérifier mon identité** et suivez les instructions pour effectuer une vérification de sécurité supplémentaire.

    ![Vérification de sécurité supplémentaire](./media/pim-how-to-activate-role/additional-security-verification.png)

1. Cliquez sur **Activer** pour ouvrir le volet Activation.

    ![Volet Activation](./media/pim-how-to-activate-role/directory-roles-activate.png)

1. Si nécessaire, spécifiez une heure de début personnalisée pour l’activation.

1. Spécifiez la durée de l’activation.

1. Dans la zone de texte **Raison de l’activation**, entrez le motif de la demande d’activation. Certains rôles vous obligent à fournir un numéro de ticket d’incident.

    ![Volet Activation terminée](./media/pim-how-to-activate-role/directory-roles-activation-pane.png)

1. Cliquez sur **Activer**.

    Si le rôle ne nécessite pas d’approbation, il est activé et ajouté à la liste des rôles actifs. Si vous voulez utiliser le rôle tout de suite, suivez les étapes décrites dans la section suivante.

    Si [l’activation du rôle nécessite une approbation](./azure-ad-pim-approval-workflow.md), une notification s’affiche dans le coin supérieur droit de votre navigateur pour vous informer que la demande est en attente d’approbation.

    ![Notification de demande en attente](./media/pim-how-to-activate-role/directory-roles-activate-notification.png)

## <a name="use-a-role-immediately-after-activation"></a>Utiliser un rôle immédiatement après son activation

Quand vous activez un rôle dans PIM, 10 minutes au moins sont nécessaires avant de pouvoir accéder au portail d’administration souhaité ou d’exécuter des fonctions au sein d’une charge de travail d’administration spécifique. Pour forcer une mise à jour de vos autorisations, utilisez la page **Accès à l’application** de la façon décrite dans les étapes suivantes.

1. Ouvrez Azure AD Privileged Identity Management.

1. Cliquez sur la page **Accès à l’application**.

    ![Accès à l’application PIM](./media/pim-how-to-activate-role/pim-application-access.png)

1. Cliquez sur le lien **Azure Active Directory** pour rouvrir le portail sur la page **Tous les utilisateurs**.

    Quand vous cliquez sur ce lien, vous invalidez votre jeton actuel et vous forcez le portail Azure pour obtenir un nouveau jeton qui doit normalement contenir vos autorisations mises à jour.

## <a name="view-the-status-of-your-requests"></a>Afficher l’état de vos demandes

Vous pouvez afficher l’état de vos demandes d’activation en attente.

1. Ouvrez Azure AD Privileged Identity Management.

1. Cliquez sur **Rôles d’annuaire Azure AD**.

1. Cliquez sur **Mes demandes** pour afficher la liste de vos demandes.

    ![Rôles d’annuaire Azure AD - Mes demandes](./media/pim-how-to-activate-role/directory-roles-my-requests.png)

## <a name="deactivate-a-role"></a>Désactiver un rôle

Une fois qu’un rôle a été activé, il se désactive automatiquement quand sa limite de temps (durée éligible) est atteinte.

Si vous terminez vos tâches d’administration plus tôt que prévu, vous pouvez également désactiver un rôle manuellement dans Azure AD Privileged Identity Management.

1. Ouvrez Azure AD Privileged Identity Management.

1. Cliquez sur **Rôles d’annuaire Azure AD**.

1. Cliquez sur **Mes rôles**.

1. Cliquez sur **Rôles actifs** pour afficher la liste des rôles actifs.

1. Accédez au rôle dont vous n’avez plus besoin, puis cliquez sur **Désactiver**.

## <a name="cancel-a-pending-request"></a>Annuler une demande en attente

Si vous n’avez pas besoin de l’activation d’un rôle nécessitant une approbation, vous pouvez annuler une demande en attente à tout moment.

1. Ouvrez Azure AD Privileged Identity Management.

1. Cliquez sur **Rôles d’annuaire Azure AD**.

1. Cliquez sur **Mes demandes**.

1. Pour le rôle que vous souhaitez annuler, cliquez sur le bouton **Annuler**.

    Lorsque vous cliquez sur Annuler, la demande est annulée. Pour réactiver le rôle, vous devez envoyer une nouvelle demande d’activation.

   ![Annuler une demande en attente](./media/pim-how-to-activate-role/directory-role-cancel.png)

## <a name="troubleshoot"></a>Résolution des problèmes

### <a name="permissions-not-granted-after-activating-a-role"></a>Autorisations non accordées après l’activation d’un rôle

Quand vous activez un rôle dans PIM, 10 minutes au moins sont nécessaires avant de pouvoir accéder au portail d’administration souhaité ou d’exécuter des fonctions au sein d’une charge de travail d’administration spécifique. Pour forcer une mise à jour de vos autorisations, utilisez la page **Accès à l’application** comme décrit précédemment dans [Utiliser un rôle immédiatement après son activation](#use-a-role-immediately-after-activation).

Pour des étapes de dépannage supplémentaires, consultez [Résolution des problèmes des autorisations élevées](https://social.technet.microsoft.com/wiki/contents/articles/37568.troubleshooting-elevated-permissions-with-azure-ad-privileged-identity-management.aspx).

## <a name="next-steps"></a>Étapes suivantes

- [Activer des rôles de ressources Azure dans PIM](pim-resource-roles-activate-your-roles.md)
