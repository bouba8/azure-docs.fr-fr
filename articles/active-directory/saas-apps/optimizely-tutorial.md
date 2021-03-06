---
title: "Tutoriel : Intégration d'Azure Active Directory à Optimizely | Microsoft Docs"
description: Découvrez comment configurer l’authentification unique entre Azure Active Directory et Optimizely.
services: active-directory
documentationCenter: na
author: jeevansd
manager: daveba
ms.assetid: 28ef03e1-9aad-4301-af97-d94e853edc74
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 08/07/2018
ms.author: jeedes
ms.collection: M365-identity-device-management
ms.openlocfilehash: 534a373024556db86d0553b68ce3f847ff085486
ms.sourcegitcommit: 301128ea7d883d432720c64238b0d28ebe9aed59
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56210711"
---
# <a name="tutorial-azure-active-directory-integration-with-optimizely"></a>Tutoriel : Intégration d'Azure Active Directory à Optimizely

Dans ce didacticiel, vous allez apprendre à intégrer Optimizely avec Azure Active Directory (Azure AD).

L’intégration d’Optimizely à Azure AD vous offre les avantages suivants :

- Dans Azure AD, vous pouvez contrôler qui a accès à Optimizely.
- Vous pouvez autoriser les utilisateurs à se connecter automatiquement à Optimizely (via l’authentification unique) avec leur compte Azure AD.
- Vous pouvez gérer vos comptes à partir d’un emplacement central : le portail Azure.

Pour en savoir plus sur l’intégration des applications SaaS avec Azure AD, consultez [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](../manage-apps/what-is-single-sign-on.md).

## <a name="prerequisites"></a>Prérequis

Pour configurer l’intégration d’Azure AD avec Optimizely, vous avez besoin des éléments suivants :

- Un abonnement Azure AD
- Un abonnement Optimizely pour lequel l’authentification unique est activée

> [!NOTE]
> Pour tester les étapes de ce didacticiel, nous déconseillons l’utilisation d’un environnement de production.

Vous devez en outre suivre les recommandations ci-dessous :

- N’utilisez pas votre environnement de production, sauf si cela est nécessaire.
- Si vous n’avez pas d’environnement d’essai Azure AD, vous pouvez obtenir un essai d’un mois [ici](https://azure.microsoft.com/pricing/free-trial/).

## <a name="scenario-description"></a>Description du scénario

Dans ce didacticiel, vous testez l’authentification unique Azure AD dans un environnement de test.
Le scénario décrit dans ce didacticiel se compose des deux sections principales suivantes :

1. Ajout d’Optimizely à partir de la galerie
2. Configuration et test de l’authentification unique Azure AD

## <a name="adding-optimizely-from-the-gallery"></a>Ajout d’Optimizely à partir de la galerie

Pour configurer l’intégration d’Optimizely avec Azure AD, vous devez ajouter Optimizely à partir de la galerie à votre liste d’applications SaaS gérées.

**Pour ajouter Optimizely à partir de la galerie, procédez comme suit :**

1. Dans le volet de navigation gauche du **[portail Azure](https://portal.azure.com)**, cliquez sur l’icône **Azure Active Directory**. 

    ![Active Directory][1]

2. Accédez à **Applications d’entreprise**. Accédez ensuite à **Toutes les applications**.

    ![APPLICATIONS][2]

3. Pour ajouter l’application, cliquez sur le bouton **Nouvelle application** en haut de la boîte de dialogue.

    ![APPLICATIONS][3]

4. Dans la zone de recherche, tapez **Optimizely**.

    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/tutorial_optimizely_search.png)

5. Dans le volet de résultats, sélectionnez **Optimizely**, puis cliquez sur **Ajouter** pour ajouter l’application.

    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/tutorial_optimizely_addfromgallery.png)

## <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configuration et test de l’authentification unique Azure AD

Dans cette section, vous allez configurer et tester l’authentification unique Azure AD avec Optimizely avec un utilisateur de test appelé « Britta Simon ».

Pour que l’authentification unique fonctionne, Azure AD doit savoir qui est l’utilisateur Optimizely équivalent dans Azure AD. En d’autres termes, une relation entre l’utilisateur Azure AD et l’utilisateur Optimizely associé doit être établie.

Pour cela, affectez la valeur de **nom d’utilisateur** dans Azure AD comme valeur de **nom d’utilisateur** dans Optimizely.

Pour configurer et tester l’authentification unique Azure AD avec Optimizely, vous devez suivre les indications des sections suivantes :

1. **[Configuration de l’authentification unique Azure AD](#configuring-azure-ad-single-sign-on)** pour permettre à vos utilisateurs d’utiliser cette fonctionnalité.
2. **[Création d’un utilisateur de test Azure AD](#creating-an-azure-ad-test-user)** pour tester l’authentification unique Azure AD avec Britta Simon.
3. **[Création d’un utilisateur de test Optimizely](#creating-an-optimizely-test-user)** pour avoir un équivalent de Britta Simon dans Optimizely lié à la représentation Azure AD associée.
4. **[Affectation de l’utilisateur de test Azure AD](#assigning-the-azure-ad-test-user)** : permet à Britta Simon d’utiliser l’authentification unique Azure AD.
5. **[Testing Single Sign-On](#testing-single-sign-on)** pour vérifier si la configuration fonctionne.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuration de l’authentification unique Azure AD

Dans cette section, vous allez activer l’authentification unique Azure AD dans le portail Azure et configurer l’authentification unique dans votre application Optimizely.

**Pour configurer l’authentification unique Azure AD avec Optimizely, procédez comme suit :**

1. Dans le portail Azure, sur la page d’intégration de l’application **Optimizely**, cliquez sur **Authentification unique**.

    ![Configurer l'authentification unique][4]

2. Dans la boîte de dialogue **Authentification unique**, pour le **Mode**, sélectionnez **Authentification basée sur SAML** pour activer l’authentification unique.

    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_optimizely_samlbase.png)

3. Dans la section **Domaine et URL Optimizely**, procédez comme suit :

    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_optimizely_url.png)

    a. Dans la zone de texte **URL de connexion**, tapez une URL au format suivant : `https://app.optimizely.net/<instance name>`

    b. Dans la zone de texte **Identificateur**, tapez une URL au format suivant : `urn:auth0:optimizely:contoso`

    > [!NOTE]
    > Il ne s’agit pas des valeurs réelles. Vous mettrez à jour la valeur avec l’URL de connexion et l’identificateur réels. La procédure est expliquée plus loin dans le didacticiel.

4. L’application Optimizely attend les assertions SAML dans un format spécifique. Configurez les revendications suivantes pour cette application. Vous pouvez gérer les valeurs de ces attributs à partir de la section « **Attributs utilisateur** » sur la page d’intégration des applications. La capture d’écran suivante montre un exemple :
    
    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_optimizely_attribute.png)
    
5. Dans la section **Attributs utilisateur**, cliquez sur **Afficher et modifier tous les autres attributs utilisateur** pour développer les attributs. Dans chacun des attributs affichés, procédez comme suit :

    | Nom de l'attribut | Valeur de l’attribut |
    | ---------------| --------------- |
    | email | user.mail |

    a. Cliquez sur **Ajouter un attribut** pour ouvrir la boîte de dialogue **Ajouter un attribut**.

    ![Configure Single Sign-On](./media/optimizely-tutorial/tutorial_attribute_04.png)

    ![Configure Single Sign-On](./media/optimizely-tutorial/tutorial_attribute_05.png)

    b. Dans la zone de texte **Nom**, indiquez le **nom d’attribut** pour cette ligne.

    c. Dans la liste **Valeur** , saisissez la valeur d’attribut affichée pour cette ligne.

    d. Cliquez sur **OK**.

6. Dans la section **Certificat de signature SAML**, cliquez sur **Téléchargez le certificat (Base64)** puis enregistrez le fichier du certificat sur votre ordinateur.

    ![Configure Single Sign-On](./media/optimizely-tutorial/tutorial_optimizely_certificate.png)

7. Cliquez sur le bouton **Enregistrer** .

    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_general_400.png)

8. Dans la section **Configuration d’Optimizely**, cliquez sur **Configurer Optimizely** pour ouvrir la fenêtre **Configurer l’authentification**. Copiez l **’URL du service d’authentification unique SAML** à partir de la **section Référence rapide.**

    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_optimizely_configure.png)

9. Pour configurer l’authentification unique côté **Optimizely**, contactez votre responsable de compte Optimizely et fournissez-lui le **certificat (Base64)** téléchargé et **l’URL du service d’authentification unique SAML**.

10. En réponse à votre e-mail, Optimizely vous fournit l’URL de connexion (authentification unique initiée par le fournisseur de service) et l’identificateur (ID d’entité du fournisseur de service).

    a. Copiez **l’URL d’authentification unique initiée par SP** fournie par Optimizely, puis collez-la dans la zone de texte **URL de connexion** de la section **Domaine et URL Optimizely** sur le portail Azure.

    b. Copiez **l’ID d’entité du fournisseur d’identité** fourni par Optimizely, puis collez-le dans la zone de texte **Identificateur** de la section **Domaine et URL Optimizely** sur le portail Azure.

11. Dans une autre fenêtre de navigateur, connectez-vous à votre application Optimizely.

12. Cliquez sur le nom de votre compte dans l’angle supérieur droit, puis sur **Paramètres du compte**.

    ![Authentification unique Azure AD](./media/optimizely-tutorial/tutorial_optimizely_09.png)

13. Sous l’onglet Compte, cochez la case **Activer l’authentification unique** sous Authentification unique dans la section **Vue d’ensemble**.
  
    ![Authentification unique Azure AD](./media/optimizely-tutorial/tutorial_optimizely_10.png)

14. Cliquez sur **Enregistrer**.

### <a name="creating-an-azure-ad-test-user"></a>Création d’un utilisateur de test Azure AD

L’objectif de cette section est de créer un utilisateur de test appelé Britta Simon dans le portail Azure.

![Créer un utilisateur Azure AD][100]

**Pour créer un utilisateur de test dans Azure AD, procédez comme suit :**

1. Dans le panneau de navigation gauche du **portail Azure**, cliquez sur l’icône **Azure Active Directory**.

    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_01.png) 

2. Pour afficher la liste des utilisateurs, accédez à **Utilisateurs et groupes**, puis cliquez sur **Tous les utilisateurs**.
    
    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_02.png) 

3. Pour ouvrir la boîte de dialogue **Utilisateur**, cliquez sur **Ajouter** en haut de la boîte de dialogue.
 
    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_03.png) 

4. Dans la boîte de dialogue **Utilisateur**, procédez comme suit :
 
    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_04.png) 

    a. Dans la zone de texte **Nom**, entrez **BrittaSimon**.

    b. Dans la zone de texte **Nom d’utilisateur** , tapez l’**adresse de messagerie** de Britta Simon.

    c. Sélectionnez **Afficher le mot de passe** et notez la valeur du **mot de passe**.

    d. Cliquez sur **Créer**.

### <a name="creating-an-optimizely-test-user"></a>Création d’un utilisateur de test Optimizely

Dans cette section, vous allez créer un utilisateur appelé Britta Simon dans Optimizely.

1. Sur la page d’accueil, sélectionnez l’onglet **Collaborateurs**.

2. Pour ajouter un nouveau collaborateur au projet, cliquez sur **Nouveau collaborateur**.
   
    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_10.png)

3. Renseignez l’adresse de messagerie et assignez un rôle au nouveau collaborateur. Cliquez sur **Invite**.

    ![Création d’un utilisateur de test Azure AD](./media/optimizely-tutorial/create_aaduser_11.png)

4. Il reçoit une invitation par courrier électronique. À l’aide de l’adresse de messagerie, il doit se connecter à Optimizely.

### <a name="assigning-the-azure-ad-test-user"></a>Affectation de l’utilisateur de test Azure AD

Dans cette section, vous allez autoriser Britta Simon à utiliser l’authentification unique Azure en lui accordant l’accès à Optimizely.

![Affecter des utilisateurs][200] 

**Pour affecter Britta Simon à Optimizely, procédez comme suit :**

1. Dans le portail Azure, ouvrez la vue des applications, accédez à la vue des répertoires, accédez à **Applications d’entreprise**, puis cliquez sur **Toutes les applications**.

    ![Affecter des utilisateurs][201]

2. Dans la liste des applications, sélectionnez **Optimizely**.

    ![Configurer l'authentification unique](./media/optimizely-tutorial/tutorial_optimizely_app.png) 

3. Dans le menu de gauche, cliquez sur **Utilisateurs et groupes**.

    ![Affecter des utilisateurs][202]

4. Cliquez sur le bouton **Ajouter**. Ensuite, sélectionnez **Utilisateurs et groupes** dans la boîte de dialogue **Ajouter une affectation**.

    ![Affecter des utilisateurs][203]

5. Dans la boîte de dialogue **Utilisateurs et groupes**, sélectionnez **Britta Simon** dans la liste des utilisateurs.

6. Cliquez sur le bouton **Sélectionner** dans la boîte de dialogue **Utilisateurs et groupes**.

7. Cliquez sur le bouton **Affecter** dans la boîte de dialogue **Ajouter une affectation**.

### <a name="testing-single-sign-on"></a>Test de l’authentification unique

Dans cette section, vous allez tester la configuration de l’authentification unique Azure AD à l’aide du volet d’accès.

Lorsque vous cliquez sur la vignette Optimizely dans le volet d’accès, vous devez être connecté automatiquement à votre application Optimizely.

## <a name="additional-resources"></a>Ressources supplémentaires

* [Liste de didacticiels sur l’intégration d’applications SaaS avec Azure Active Directory](tutorial-list.md)
* [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](../manage-apps/what-is-single-sign-on.md)

<!--Image references-->

[1]: ./media/optimizely-tutorial/tutorial_general_01.png
[2]: ./media/optimizely-tutorial/tutorial_general_02.png
[3]: ./media/optimizely-tutorial/tutorial_general_03.png
[4]: ./media/optimizely-tutorial/tutorial_general_04.png

[100]: ./media/optimizely-tutorial/tutorial_general_100.png

[200]: ./media/optimizely-tutorial/tutorial_general_200.png
[201]: ./media/optimizely-tutorial/tutorial_general_201.png
[202]: ./media/optimizely-tutorial/tutorial_general_202.png
[203]: ./media/optimizely-tutorial/tutorial_general_203.png
