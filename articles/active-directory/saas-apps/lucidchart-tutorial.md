---
title: 'Tutoriel : Intégration d’Azure Active Directory à Lucidchart | Microsoft Docs'
description: Découvrez comment configurer l’authentification unique entre Azure Active Directory et Lucidchart.
services: active-directory
documentationCenter: na
author: jeevansd
manager: daveba
ms.assetid: 1068d364-11f3-43b5-bd6d-26f00ecd5baa
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 06/21/2017
ms.author: jeedes
ms.collection: M365-identity-device-management
ms.openlocfilehash: 26b9fc0fa194b9e2be97eb3bb8471b61e7fb3b8f
ms.sourcegitcommit: 301128ea7d883d432720c64238b0d28ebe9aed59
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56202755"
---
# <a name="tutorial-azure-active-directory-integration-with-lucidchart"></a>Tutoriel : Intégration d’Azure Active Directory à Lucidchart

Dans ce didacticiel, vous allez apprendre à intégrer Lucidchart à Azure Active Directory (Azure AD).

L’intégration d’Azure AD à Lucidchart offre les avantages suivants :

- Dans Azure AD, vous pouvez contrôler qui a accès à Lucidchart.
- Vous pouvez autoriser vos utilisateurs à se connecter automatiquement à Lucidchart (via l’authentification unique) avec leur compte Azure AD.
- Vous pouvez gérer vos comptes à partir d’un emplacement central : le portail Azure.

Pour en savoir plus sur l’intégration des applications SaaS avec Azure AD, consultez [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](../manage-apps/what-is-single-sign-on.md).

## <a name="prerequisites"></a>Prérequis

Pour configurer l’intégration d’Azure AD à Lucidchart, vous avez besoin des éléments suivants :

- Un abonnement Azure AD
- Un abonnement Lucidchart pour lequel l’authentification unique est activée

> [!NOTE]
> Pour tester les étapes de ce didacticiel, nous déconseillons l’utilisation d’un environnement de production.

Vous devez en outre suivre les recommandations ci-dessous :

- N’utilisez pas votre environnement de production, sauf si cela est nécessaire.
- Si vous n’avez pas d’environnement d’essai Azure AD, vous pouvez obtenir un essai d’un mois [ici](https://azure.microsoft.com/pricing/free-trial/).

## <a name="scenario-description"></a>Description du scénario
Dans ce didacticiel, vous testez l’authentification unique Azure AD dans un environnement de test. Le scénario décrit dans ce didacticiel se compose des deux sections principales suivantes :

1. Ajout de Lucidchart à partir de la galerie
1. Configuration et test de l’authentification unique Azure AD

## <a name="adding-lucidchart-from-the-gallery"></a>Ajout de Lucidchart à partir de la galerie
Pour configurer l’intégration de Lucidchart à Azure AD, vous devez ajouter Lucidchart à partir de la galerie à votre liste d’applications SaaS gérées.

**Pour ajouter Lucidchart à partir de la galerie, procédez comme suit :**

1. Dans le volet de navigation gauche du **[portail Azure](https://portal.azure.com)**, cliquez sur l’icône **Azure Active Directory**. 

    ![Active Directory][1]

1. Accédez à **Applications d’entreprise**. Accédez ensuite à **Toutes les applications**.

    ![APPLICATIONS][2]
    
1. Pour ajouter l’application, cliquez sur le bouton **Nouvelle application** en haut de la boîte de dialogue.

    ![APPLICATIONS][3]

1. Dans la zone de recherche, tapez **Lucidchart**.

    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/tutorial_lucidchart_search.png)

1. Dans le panneau de résultats, sélectionnez **Lucidchart**, puis cliquez sur le bouton **Ajouter** pour ajouter l’application.

    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/tutorial_lucidchart_addfromgallery.png)

##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configuration et test de l’authentification unique Azure AD
Dans cette section, vous allez configurer et tester l’authentification unique Azure AD avec Lucidchart à l’aide d’un utilisateur de test appelé « Britta Simon ».

Pour que l’authentification unique fonctionne, Azure AD doit savoir qui est l’utilisateur Lucidchart équivalent dans Azure AD. En d’autres termes, une relation entre un utilisateur Azure AD et l’utilisateur Lucidchart associé doit être établie.

Dans Lucidchart, affectez la valeur du **nom d’utilisateur** dans Azure AD comme valeur du **nom d’utilisateur** pour établir la relation.

Pour configurer et tester l’authentification unique Azure AD avec Lucidchart, vous devez suivre les indications des sections suivantes :

1. **[Configuration de l’authentification unique Azure AD](#configuring-azure-ad-single-sign-on)** pour permettre à vos utilisateurs d’utiliser cette fonctionnalité.
1. **[Création d’un utilisateur de test Azure AD](#creating-an-azure-ad-test-user)** pour tester l’authentification unique Azure AD avec Britta Simon.
1. **[Création d’un utilisateur de test Lucidchart](#creating-a-lucidchart-test-user)** pour avoir un équivalent de Britta Simon dans Lucidchart lié à la représentation Azure AD de l’utilisateur.
1. **[Affectation de l’utilisateur de test Azure AD](#assigning-the-azure-ad-test-user)** : permet à Britta Simon d’utiliser l’authentification unique Azure AD.
1. **[Testing Single Sign-On](#testing-single-sign-on)** pour vérifier si la configuration fonctionne.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuration de l’authentification unique Azure AD

Dans cette section, vous allez activer l’authentification unique Azure AD dans le portail Azure et configurer l’authentification unique dans votre application Lucidchart.

**Pour configurer l’authentification unique Azure AD avec Lucidchart, procédez comme suit :**

1. Dans le portail Azure, sur la page d’intégration de l’application **Lucidchart**, cliquez sur **Authentification unique**.

    ![Configurer l'authentification unique][4]

1. Dans la boîte de dialogue **Authentification unique**, pour le **Mode**, sélectionnez **Authentification basée sur SAML** pour activer l’authentification unique.
 
    ![Configurer l'authentification unique](./media/lucidchart-tutorial/tutorial_lucidchart_samlbase.png)

1. Dans la section **Lucidchart Domain and URLs** (Domaine et URL Lucidchart), procédez comme suit :

    ![Configurer l'authentification unique](./media/lucidchart-tutorial/tutorial_lucidchart_url.png)

    Dans la zone de texte **URL d’authentification**, tapez l’URL : `https://chart2.office.lucidchart.com/saml/sso/azure`

1. Dans la section **Certificat de signature SAML**, cliquez sur **Métadonnées XML** puis enregistrez le fichier de métadonnées sur votre ordinateur.

    ![Configure Single Sign-On](./media/lucidchart-tutorial/tutorial_lucidchart_certificate.png) 

1. Cliquez sur le bouton **Enregistrer** .

    ![Configurer l'authentification unique](./media/lucidchart-tutorial/tutorial_general_400.png)

1. Dans une autre fenêtre de navigateur web, connectez-vous à votre site d’entreprise Lucidchart en tant qu’administrateur.

1. Dans le menu situé en haut, cliquez sur **Team**.
   
    ![Équipe](./media/lucidchart-tutorial/ic791190.png "Équipe")

1. Cliquez sur **Applications \> Gérer SAML**.
   
    ![Gérer SAML](./media/lucidchart-tutorial/ic791191.png "Gérer SAML")

1. Dans la boîte de dialogue **SAML Authentication Settings** , procédez comme suit :
   
    a. Sélectionnez **Enable SAML Authentication**, puis cliquez sur **Optional**.

    ![Paramètres d’authentification SAML](./media/lucidchart-tutorial/ic791192.png "Paramètres d’authentification SAML")
 
    b. Dans la zone de texte **Domain**, entrez votre domaine, puis cliquez sur **Change Certificate**.

    ![Modifier le certificat](./media/lucidchart-tutorial/ic791193.png "Modifier le certificat")
 
    c. Ouvrez votre fichier de métadonnées téléchargé, copiez son contenu, puis collez-le dans la zone de texte **Upload Metadata** .

    ![Charger les métadonnées](./media/lucidchart-tutorial/ic791194.png "Charger les métadonnées")
 
    d. Sélectionnez **Automatically Add new user to the team** (Ajouter automatiquement un utilisateur à l’équipe), puis cliquez sur **Enregistrer les modifications**.

    ![Enregistrer les modifications](./media/lucidchart-tutorial/ic791195.png "Enregistrer les modifications")

> [!TIP]
> Vous pouvez maintenant lire une version concise de ces instructions dans le [portail Azure](https://portal.azure.com), pendant que vous configurez l’application.  Après avoir ajouté cette application à partir de la section **Active Directory > Applications d’entreprise**, cliquez simplement sur l’onglet **Authentification unique** et accédez à la documentation incorporée par le biais de la section **Configuration** en bas. Pour en savoir plus sur la fonctionnalité de documentation incorporée, accédez à : [Documentation incorporée Azure AD]( https://go.microsoft.com/fwlink/?linkid=845985)

### <a name="creating-an-azure-ad-test-user"></a>Création d’un utilisateur de test Azure AD
L’objectif de cette section est de créer un utilisateur de test appelé Britta Simon dans le portail Azure.

![Créer un utilisateur Azure AD][100]

**Pour créer un utilisateur de test dans Azure AD, procédez comme suit :**

1. Dans le panneau de navigation gauche du **portail Azure**, cliquez sur l’icône **Azure Active Directory**.

    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/create_aaduser_01.png) 

1. Pour afficher la liste des utilisateurs, accédez à **Utilisateurs et groupes**, puis cliquez sur **Tous les utilisateurs**.
    
    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/create_aaduser_02.png) 

1. Pour ouvrir la boîte de dialogue **Utilisateur**, cliquez sur **Ajouter** en haut de la boîte de dialogue.
 
    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/create_aaduser_03.png) 

1. Dans la boîte de dialogue **Utilisateur**, procédez comme suit :
 
    ![Création d’un utilisateur de test Azure AD](./media/lucidchart-tutorial/create_aaduser_04.png) 

    a. Dans la zone de texte **Nom**, entrez **BrittaSimon**.

    b. Dans la zone de texte **Nom d’utilisateur**, tapez **l’adresse e-mail** de Britta Simon.

    c. Sélectionnez **Afficher le mot de passe** et notez la valeur du **mot de passe**.

    d. Cliquez sur **Créer**.
 
### <a name="creating-a-lucidchart-test-user"></a>Création d’un utilisateur de test Lucidchart

Aucun élément d’action ne vous permet de configurer l’approvisionnement des utilisateurs dans Lucidchart.  Lorsqu’un utilisateur tente de se connecter à Lucidchart à l’aide du panneau d’accès, Lucidchart vérifie si cet utilisateur existe.  

Si aucun compte d’utilisateur n’est disponible, Lucidchart le crée automatiquement.

### <a name="assigning-the-azure-ad-test-user"></a>Affectation de l’utilisateur de test Azure AD

Dans cette section, vous allez autoriser Britta Simon à utiliser l’authentification unique Azure en lui accordant l’accès à Lucidchart.

![Affecter des utilisateurs][200] 

**Pour affecter Britta Simon à Lucidchart, procédez comme suit :**

1. Dans le portail Azure, ouvrez la vue des applications, accédez à la vue des répertoires, accédez à **Applications d’entreprise**, puis cliquez sur **Toutes les applications**.

    ![Affecter des utilisateurs][201] 

1. Dans la liste des applications, sélectionnez **Lucidchart**.

    ![Configurer l'authentification unique](./media/lucidchart-tutorial/tutorial_lucidchart_app.png) 

1. Dans le menu de gauche, cliquez sur **Utilisateurs et groupes**.

    ![Affecter des utilisateurs][202] 

1. Cliquez sur le bouton **Ajouter**. Ensuite, sélectionnez **Utilisateurs et groupes** dans la boîte de dialogue **Ajouter une affectation**.

    ![Affecter des utilisateurs][203]

1. Dans la boîte de dialogue **Utilisateurs et groupes**, sélectionnez **Britta Simon** dans la liste des utilisateurs.

1. Cliquez sur le bouton **Sélectionner** dans la boîte de dialogue **Utilisateurs et groupes**.

1. Cliquez sur le bouton **Affecter** dans la boîte de dialogue **Ajouter une affectation**.
    
### <a name="testing-single-sign-on"></a>Test de l’authentification unique

Dans cette section, vous allez tester la configuration de l’authentification unique Azure AD à l’aide du volet d’accès.

Lorsque vous cliquez sur la vignette Lucidchart dans le panneau d’accès, vous devez être connecté automatiquement à votre application Lucidchart.
Pour plus d’informations sur le panneau d’accès, consultez [Présentation du panneau d’accès](../user-help/active-directory-saas-access-panel-introduction.md).

## <a name="additional-resources"></a>Ressources supplémentaires

* [Liste de didacticiels sur l’intégration d’applications SaaS avec Azure Active Directory](tutorial-list.md)
* [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](../manage-apps/what-is-single-sign-on.md)



<!--Image references-->

[1]: ./media/lucidchart-tutorial/tutorial_general_01.png
[2]: ./media/lucidchart-tutorial/tutorial_general_02.png
[3]: ./media/lucidchart-tutorial/tutorial_general_03.png
[4]: ./media/lucidchart-tutorial/tutorial_general_04.png

[100]: ./media/lucidchart-tutorial/tutorial_general_100.png

[200]: ./media/lucidchart-tutorial/tutorial_general_200.png
[201]: ./media/lucidchart-tutorial/tutorial_general_201.png
[202]: ./media/lucidchart-tutorial/tutorial_general_202.png
[203]: ./media/lucidchart-tutorial/tutorial_general_203.png

