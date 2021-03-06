---
title: Nouveautés Notes de publication - Azure Active Directory | Microsoft Docs
description: Découvrez les nouveautés d’Azure Active Directory, notamment les dernières notes de publication, les problèmes connus, les corrections de bogues, les fonctionnalités dépréciées et les modifications à venir.
services: active-directory
author: eross-msft
manager: daveba
featureFlags:
- clicktale
ms.assetid: 06a149f7-4aa1-4fb9-a8ec-ac2633b031fb
ms.service: active-directory
ms.subservice: fundamentals
ms.workload: identity
ms.topic: conceptual
ms.date: 01/31/2019
ms.author: lizross
ms.reviewer: dhanyahk
ms.custom: it-pro
ms.collection: M365-identity-device-management
ms.openlocfilehash: 8b7616eed4a17f33ad3b490c625c69cebb32a3f8
ms.sourcegitcommit: 301128ea7d883d432720c64238b0d28ebe9aed59
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2019
ms.locfileid: "56164530"
---
# <a name="whats-new-in-azure-active-directory"></a>Nouveautés d’Azure Active Directory

>Soyez notifié de la disponibilité des mises à jour sur cette page en faisant un copier-coller de cette URL : `https://docs.microsoft.com/api/search/rss?search=%22release+notes+for+azure+AD%22&locale=en-us` dans votre lecteur de flux ![icône RSS](./media/whats-new/feed-icon-16x16.png).

Azure AD bénéficie d’améliorations en continu. Pour vous informer des développements les plus récents, cet article détaille les thèmes suivants :

- Versions les plus récentes
- Problèmes connus
- Résolution des bogues
- Fonctionnalités dépréciées
- Modifications planifiées

Cette page est mise à jour tous les mois. Donc, consultez-la régulièrement. Si vous recherchez des éléments antérieurs aux six derniers mois, vous les trouverez dans l’[Archive des nouveautés d’Azure Active Directory](whats-new-archive.md).

---
## <a name="january-2019"></a>Janvier 2019

### <a name="active-directory-b2b-collaboration-using-one-time-passcode-authentication-public-preview"></a>Collaboration Active Directory B2B à l'aide de l'authentification par code secret à usage unique (préversion publique)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** B2B  
**Fonctionnalité de produit :** B2B/B2C

Nous avons introduit l'authentification par code secret à usage unique (OTP) pour les utilisateurs invités B2B qui ne peuvent pas être authentifiés par d'autres moyens, comme Azure AD, un compte Microsoft (MSA) ou la fédération Google. Avec cette nouvelle méthode d'authentification, les utilisateurs invités n'ont pas besoin de créer de nouveau compte Microsoft. Lors de l'échange d'une invitation ou de l'accès à une ressource partagée, l'utilisateur invité peut demander qu'un code temporaire soit envoyé à une adresse e-mail. À l'aide de ce code temporaire, l'utilisateur invité peut continuer à se connecter.

Pour plus d'informations, consultez [Authentification à l'aide d'un code secret à usage unique envoyé par e-mail (préversion)](https://docs.microsoft.com/azure/active-directory/b2b/one-time-passcode) et le blog [Azure AD permet à tous les utilisateurs de partager et de collaborer en toute simplicité sans compte](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-AD-makes-sharing-and-collaboration-seamless-for-any-user/ba-p/325949).

### <a name="new-azure-ad-application-proxy-cookie-settings"></a>Nouveaux paramètres de cookies pour le proxy d'application Azure AD

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Proxy d’application  
**Fonctionnalité de produit :** Contrôle d’accès

Nous avons introduit trois nouveaux paramètres de cookies, disponibles pour vos applications publiées via le proxy d’application :

- **Utiliser un cookie HTTPOnly.** Définit l'indicateur **HTTPOnly** sur l'accès du proxy d'application et les cookies de session. Cette option offre des avantages supplémentaires en termes de sécurité, et permet notamment d'éviter de copier ou de modifier les cookies via des scripts côté client. Nous vous recommandons d’activer cet indicateur (sélectionnez **Oui**) pour bénéficier de ces avantages supplémentaires.

- **Utiliser un cookie sécurisé.** Définit l'indicateur **Sécurisé** sur l'accès du proxy d'application et les cookies de session. Cette option offre des avantages supplémentaires en termes de sécurité, et veille à ce que les cookies soient uniquement transmis via des canaux sécurisés TLS, tels que HTTPS. Nous vous recommandons d’activer cet indicateur (sélectionnez **Oui**) pour bénéficier de ces avantages supplémentaires.

- **Utiliser un cookie persistant.** Empêche l'expiration des cookies d'accès lorsque le navigateur web est fermé. La durée de vie de ces cookies correspond à la durée de vie du jeton d'accès. Cela étant, les cookies sont réinitialisés une fois le délai d'expiration atteint ou si l’utilisateur supprime manuellement le cookie. Nous vous recommandons de conserver le paramètre par défaut **Non**, et de n'activer le paramètre que pour les applications plus anciennes qui ne partagent pas de cookies entre processus.

Pour plus d’informations sur les nouveaux cookies, consultez [Paramètres de cookies pour l’accès aux applications locales dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-configure-cookie-settings).

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---january-2019"></a>Nouvelles applications fédérées disponibles dans la galerie d'applications Azure AD - Janvier 2019

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En janvier 2019, nous avons ajouté à notre galerie d’applications les 35 applications suivantes qui prennent en charge la fédération :

[Firstbird](https://docs.microsoft.com/azure/active-directory/saas-apps/firstbird-tutorial), [Folloze](https://docs.microsoft.com/azure/active-directory/saas-apps/folloze-tutorial), [Talent Palette](https://docs.microsoft.com/azure/active-directory/saas-apps/talent-palette-tutorial), [Infor CloudSuite](https://docs.microsoft.com/azure/active-directory/saas-apps/infor-cloud-suite-tutorial), [Cisco Umbrella](https://docs.microsoft.com/azure/active-directory/saas-apps/cisco-umbrella-tutorial), [Zscaler Internet Access Administrator](https://docs.microsoft.com/azure/active-directory/saas-apps/zscaler-internet-access-administrator-tutorial), [Expiration Reminder](https://docs.microsoft.com/azure/active-directory/saas-apps/expiration-reminder-tutorial), [InstaVR Viewer](https://docs.microsoft.com/azure/active-directory/saas-apps/instavr-viewer-tutorial), [CorpTax](https://docs.microsoft.com/azure/active-directory/saas-apps/corptax-tutorial), [Verb](https://app.verb.net/login), [OpenLattice](https://openlattice.com/agora), [TheOrgWiki](https://www.theorgwiki.com/signup), [Pavaso Digital Close](https://docs.microsoft.com/azure/active-directory/saas-apps/pavaso-digital-close-tutorial), [GoodPractice Toolkit](https://docs.microsoft.com/azure/active-directory/saas-apps/goodpractice-toolkit-tutorial), [Cloud Service PICCO](https://docs.microsoft.com/azure/active-directory/saas-apps/cloud-service-picco-tutorial), [AuditBoard](https://docs.microsoft.com/azure/active-directory/saas-apps/auditboard-tutorial), [iProva](https://docs.microsoft.com/azure/active-directory/saas-apps/iprova-tutorial), [Workable](https://docs.microsoft.com/azure/active-directory/saas-apps/workable-tutorial), [CallPlease](https://webapp.callplease.com/create-account/create-account.html), [GTNexus SSO System](https://docs.microsoft.com/azure/active-directory/saas-apps/gtnexus-sso-module-tutorial), [CBRE ServiceInsight](https://docs.microsoft.com/azure/active-directory/saas-apps/cbre-serviceinsight-tutorial), [Deskradar](https://docs.microsoft.com/azure/active-directory/saas-apps/deskradar-tutorial), [Coralogixv](https://docs.microsoft.com/azure/active-directory/saas-apps/coralogix-tutorial), [Signagelive](https://docs.microsoft.com/azure/active-directory/saas-apps/signagelive-tutorial), [ARES for Enterprise](https://docs.microsoft.com/azure/active-directory/saas-apps/ares-for-enterprise-tutorial), [K2 for Office 365](https://www.k2.com/O365), [Xledger](https://www.xledger.net/), [iDiD Manager](https://docs.microsoft.com/azure/active-directory/saas-apps/idid-manager-tutorial), [HighGear](https://docs.microsoft.com/azure/active-directory/saas-apps/highgear-tutorial), [Visitly](https://docs.microsoft.com/azure/active-directory/saas-apps/visitly-tutorial), [Korn Ferry ALP](https://docs.microsoft.com/azure/active-directory/saas-apps/korn-ferry-alp-tutorial), [Acadia](https://docs.microsoft.com/azure/active-directory/saas-apps/acadia-tutorial), [Adoddle cSaas Platform](https://docs.microsoft.com/azure/active-directory/saas-apps/adoddle-csaas-platform-tutorial)<!-- , [CaféX Portal (Meetings)](https://docs.microsoft.com/azure/active-directory/saas-apps/cafexportal-meetings-tutorial), [MazeMap Link](https://docs.microsoft.com/azure/active-directory/saas-apps/mazemaplink-tutorial)-->  

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---

### <a name="new-azure-ad-identity-protection-enhancements-public-preview"></a>Nouvelles améliorations apportées à Azure AD Identity Protection (préversion publique)

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Identity Protection  
**Fonctionnalité de produit :** Protection et sécurité des identités

Nous sommes heureux d’annoncer l'ajout des améliorations suivantes à l’offre de préversion publique d’Azure AD Identity Protection, notamment :

- Interface utilisateur mise à jour et mieux intégrée

- API supplémentaires

- Évaluation des risques renforcée via Machine Learning

- Alignement des produits pour les utilisateurs et les connexions à risque

Consultez [Qu’est-ce qu’Azure Active Directory Identity Protection (version actualisée) ?](https://aka.ms/IdentityProtectionDocs) pour plus d'informations et partager vos idées via des invites intégrées au produit.

---

### <a name="new-app-lock-feature-for-the-microsoft-authenticator-app-on-ios-and-android-devices"></a>Nouvelle fonctionnalité Verrou d'application dans l'application Microsoft Authenticator sur les appareils iOS et Android

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Application Microsoft Authenticator  
**Fonctionnalité de produit :** Protection et sécurité des identités

Pour sécuriser les codes secrets à usage unique, informations et paramètres d'application, vous pouvez activer la fonctionnalité Verrou d'application dans l'application Microsoft Authenticator. Si vous activez Verrou d'application, vous êtes invité à vous authentifier à l'aide de votre code PIN ou verrou biométrique chaque fois que vous ouvrez l’application Microsoft Authenticator.

Pour plus d’informations, consultez [Forum aux questions sur l’application Microsoft Authenticator](https://docs.microsoft.com/azure/active-directory/user-help/microsoft-authenticator-app-faq).

---

### <a name="enhanced-azure-ad-privileged-identity-management-pim-export-capabilities"></a>Fonctionnalités d'exportation améliorées dans Azure AD Privileged Identity Management (PIM)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Privileged Identity Management  
**Fonctionnalité de produit :** Privileged Identity Management

Les administrateurs Privileged Identity Management (PIM) peuvent désormais exporter toutes les affectations de rôles actifs et éligibles pour une ressource spécifique, ce qui comprend les affectations de rôles pour toutes les ressources enfants. Auparavant, il était difficile pour les administrateurs d’obtenir une liste complète des attributions de rôle d’un abonnement, et ils devaient les exporter pour chaque ressource spécifique.

Pour plus d'informations, consultez [Afficher l’historique d’audit et d’activité pour les rôles de ressources Azure dans PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/azure-pim-resource-rbac).

---

## <a name="novemberdecember-2018"></a>Novembre/décembre 2018

### <a name="users-removed-from-synchronization-scope-no-longer-switch-to-cloud-only-accounts"></a>Des utilisateurs retirés de l’étendue de synchronisation ne basculent plus vers des comptes uniquement cloud

**Type :** Résolution  
**Catégorie de service :** User Management  
**Fonctionnalité de produit :** Répertoire

>[!Important]
>Nous avons entendu et nous comprenons votre frustration provoquée par ce correctif. Nous avons donc annulé cette modification jusqu’à ce que nous soyons en mesure de rendre l’implémentation de ce correctif plus facile dans votre organisation.

Nous avons résolu un bogue qui faisait que l’indicateur DirSyncEnabled d’un utilisateur passait erronément à **False** lorsque l’objet Active Directory Domain Services (AD DS) était exclu de l’étendue de synchronisation, puis déplacé vers la Corbeille dans Azure AD lors du cycle de synchronisation suivant. Ce correctif a pour effet que, si l’utilisateur est exclu de l’étendue de la synchronisation, puis restauré à partir de la Corbeille Azure AD, le compte d’utilisateur reste synchronisé à partir de l’AD local, comme prévu, et ne peut pas être géré dans le cloud car sa source d’autorité demeure en tant qu’AD local.

Avant ce correctif, un problème se produisait quand l’indicateur DirSyncEnabled était commuté sur False. Cela donnait la fausse impression que ces comptes avaient été convertis en objets uniquement cloud, et que les comptes pouvaient être gérés dans le nuage. Cependant, les comptes conservaient toujours leur source d’autorité comme locale, et toutes les propriétés synchronisées (attributs fantômes) provenant de l’AD local. Cette situation entraînait plusieurs problèmes dans Azure AD et dans d’autres charges de travail cloud (telles qu’Exchange Online) qui s’attendaient à traiter ces comptes comme synchronisés à partir d’AD, mais se comportaient désormais comme des comptes uniquement cloud.

À ce stade, la seule façon de convertir véritablement un compte synchronisé à partir d’AD vers un compte uniquement cloud consiste à désactiver la synchronisation d’annuaires au niveau du locataire, ce qui déclenche une opération de serveur principal pour transférer la source d’autorité. Ce type de modification de source d’autorité nécessite (sans que ce soit limitatif) un nettoyage de tous les attributs associés locaux (tels que LastDirSyncTime et les attributs fantômes), et l’envoi d’un signal à d’autres charges de travail cloud pour que son objet respectif soit également converti en un compte uniquement cloud.

Ce correctif empêche donc des mises à jour directes de l’attribut ImmutableID d’un utilisateur synchronisé à partir d’Active Directory, qui étaient requises dans certains scénarios par le passé. Par conception, l’ImmutableID d’un objet dans Azure AD, comme son nom l’indique, est censé être immuable. De nouvelles fonctionnalités implémentées dans Azure AD Connect Health et le client de synchronization Azure AD Connect sont disponibles pour de tels scénarios :

- **Mise à jour d’ImmutableID à grande échelle pour de nombreux utilisateurs en suivant une approche par étapes**
  
  Par exemple, vous devez effectuer une migration inter-forêts d’AD DS un peu longue. Solution : Utilisez Azure AD Connect pour **configurer l’ancre source**, puis, lorsque l’utilisateur migre, copiez les valeurs d’ImmutableID existantes d’Azure AD dans l’attribut ms-DS-Consistency-Guid de l’utilisateur d’AD DS local de la nouvelle forêt. Pour plus d’informations, voir [Utilisation de ms-DS-ConsistencyGuid en tant qu’attribut sourceAnchor](/azure/active-directory/hybrid/plan-connect-design-concepts#using-ms-ds-consistencyguid-as-sourceanchor).

- **Mises à jour d’ImmutableID à grande échelle pour de nombreux utilisateurs en une fois**

  Par exemple, lors de l’implémentation d’Azure AD Connect, vous commettez une erreur qui vous amène à devoir modifier l’attribut SourceAnchor. Solution : Désactivez la synchronisation d’annuaires au niveau locataire, et effacez toutes les valeurs d’ImmutableID non valides. Pour plus d’informations, voir [Désactiver la synchronisation d’annuaires pour Office 365](/office365/enterprise/turn-off-directory-synchronization).

- **Rétablissement de correspondance entre l’utilisateur local et un utilisateur existant dans Azure AD** Par exemple, un utilisateur recréé dans AD DS génère un doublon dans le compte Azure AD au lieu qu’une correspondance soit rétablie avec un compte Azure AD existant (objet orphelin). Solution : Utilisez Azure AD Connect Health dans le portail Microsoft Azure pour remapper l’ancre source/l’ImmutableID. Pour plus d’informations, voir [Scénario d’objet orphelin](/azure/active-directory/hybrid/how-to-connect-health-diagnose-sync-errors#orphaned-object-scenario).

### <a name="breaking-change-updates-to-the-audit-and-sign-in-logs-schema-through-azure-monitor"></a>Modification critique : Mises à jour du schéma des journaux de connexion et d’audit via Azure Monitor

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Monitoring et création de rapports

Nous publions actuellement à la fois des flux de journaux d’audit et de connexion via Azure Monitor. Vous pouvez donc en toute transparence intégrer les fichiers journaux avec vos outils SIEM ou Log Analytics. En réponse à vos commentaires et en vue de l’annonce de la disponibilité générale de cette fonctionnalité, nous apportons les modifications suivantes à notre schéma. Ces modifications de schéma et les mises à jour de documentation connexes se produiront d’ici la première semaine de janvier.

#### <a name="new-fields-in-the-audit-schema"></a>Nouveaux champs du schéma d’audit
Nous ajoutons un nouveau champ **Type d’opération**, pour fournir le type d’opération effectuée sur la ressource. Par exemple, **Ajouter**, **Mettre à jour** ou **Supprimer**.

#### <a name="changed-fields-in-the-audit-schema"></a>Champs modifiés du schéma d’audit
Les champs suivants font l’objet de modifications dans le schéma d’audit :

|Nom du champ|Ce qui a changé|Anciennes valeurs|Nouvelles valeurs|
|----------|------------|----------|----------|
|Catégorie|Il s’agissait du champ **Nom de service** qui se nomme à présent **Catégories d’audit**. **Nom du service** a été renommé en **loggedByService**.|<ul><li>Approvisionnement des comptes</li><li>Annuaire principal</li><li>Réinitialisation de mot de passe en libre service</li></ul>|<ul><li>User Management</li><li>Gestion des groupes</li><li>Gestion des applications</li></ul>|
|targetResources|Inclut **TargetResourceType** au niveau supérieur.|&nbsp;|<ul><li>Stratégie</li><li>Application</li><li>Utilisateur</li><li>Groupe</li></ul>|
|loggedByService|Fournit le nom du service ayant généré le journal d’audit.|Null|<ul><li>Approvisionnement des comptes</li><li>Annuaire principal</li><li>Réinitialisation de mot de passe libre-service</li></ul>|
|Résultat|Fournit le résultat des journaux d’audit. Auparavant, nous présentions une énumération, mais nous montrons maintenant la valeur réelle.|<ul><li>0</li><li>1</li></ul>|<ul><li>Succès</li><li>Échec</li></ul>|

#### <a name="changed-fields-in-the-sign-in-schema"></a>Champs modifiés du schéma de connexion
Les champs suivants font l’objet de modifications dans le schéma de connexion :

|Nom du champ|Ce qui a changé|Anciennes valeurs|Nouvelles valeurs|
|----------|------------|----------|----------|
|appliedConditionalAccessPolicies|Ce champ était nommé **conditionalaccessPolicies**. Il s’intitule à présent **conditionalaccessPolicies**.|Aucune modification|Aucune modification|
|conditionalAccessStatus|Fournit le résultat de l’état de la stratégie d’accès conditionnel au moment de la connexion. Auparavant, nous présentions une énumération, mais nous montrons maintenant la valeur réelle.|<ul><li>0</li><li>1</li><li>2</li><li>3</li></ul>|<ul><li>Succès</li><li>Échec</li><li>Non appliqué</li><li>Désactivé</li></ul>|
|appliedConditionalAccessPolicies: result|Fournit le résultat de l’état individuel de la stratégie d’accès conditionnel au moment de la connexion. Auparavant, nous présentions une énumération, mais nous montrons maintenant la valeur réelle.|<ul><li>0</li><li>1</li><li>2</li><li>3</li></ul>|<ul><li>Succès</li><li>Échec</li><li>Non appliqué</li><li>Désactivé</li></ul>|

Pour plus d’informations sur le schéma, consultez [Interpréter le schéma des journaux d’audit Azure Active Directory dans Azure Monitor (préversion)](https://docs.microsoft.com/azure/active-directory/reports-monitoring/reference-azure-monitor-audit-log-schema).

---

### <a name="identity-protection-improvements-to-the-supervised-machine-learning-model-and-the-risk-score-engine"></a>Améliorations de la protection des identités apportées dans le modèle Machine Learning supervisé et le moteur d’indice de risque

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Identity Protection  
**Fonctionnalité de produit :** Indices de risque

Les améliorations apportées à l’utilisateur Identity Protection et au moteur d’évaluation des risques de connexion peuvent contribuer à améliorer la couverture et l’exactitude du risque utilisateur. Les administrateurs peuvent constater que le niveau de risque utilisateur n’est plus directement lié au niveau de risque de détections spécifiques, et qu’il existe une augmentation du nombre et du niveau des événements de connexion à risque.

Les détections de risque sont à présent évaluées par le modèle Machine Learning supervisé, qui calcule le risque utilisateur à l’aide des fonctionnalités supplémentaires des connexions utilisateur et d’un modèle de détections. Selon ce modèle, l’administrateur peut rechercher les utilisateurs présentant des indices de risque élevés, même si les détections associées à cet utilisateur sont de risque faible ou moyen. 

---

### <a name="administrators-can-reset-their-own-password-using-the-microsoft-authenticator-app-public-preview"></a>Les administrateurs peuvent réinitialiser leur mot de passe à l’aide de l’application Microsoft Authenticator (préversion publique)

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Réinitialisation de mot de passe en libre-service  
**Fonctionnalité de produit :** Authentification utilisateur

Les administrateurs Azure AD peuvent à présent réinitialiser leur mot de passe en utilisant les notifications d’application Microsoft Authenticator ou un code à partir d’un jeton matériel ou d’une application d’authentificateur mobile. Pour réinitialiser leur mot de passe, les administrateurs peuvent à présent utiliser deux des méthodes suivantes :

- Notification de l’application Microsoft Authenticator

- Autre application mobile d’authentificateur/code de jeton matériel

- Email

- appel téléphonique

- SMS

Pour plus d’informations sur l’utilisation de l’application Microsoft Authenticator pour réinitialiser les mots de passe, consultez [Réinitialisation de mot de passe en libre-service Azure AD - Application Mobile et SSPR (préversion)](https://docs.microsoft.com/azure/active-directory/authentication/concept-sspr-howitworks#mobile-app-and-sspr-preview)

---

### <a name="new-azure-ad-cloud-device-administrator-role-public-preview"></a>Nouveau rôle Administrateur d’appareil cloud Azure AD (préversion publique)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Gestion et inscription des appareils  
**Fonctionnalité de produit :** Contrôle d’accès

Les administrateurs peuvent attribuer des utilisateurs au nouveau rôle Administrateur d’appareil cloud pour effectuer des tâches d’administration des appareils cloud. Les utilisateurs attribués au rôle Administrateur d’appareil cloud peuvent activer, désactiver et supprimer des appareils dans Azure AD et lire des clés BitLocker Windows 10 (le cas échéant) dans le portail Azure.

Pour plus d’informations sur les rôles et les autorisations, consultez [Attribution de rôles d’administrateur dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/users-groups-roles/directory-assign-admin-roles).

---

### <a name="manage-your-devices-using-the-new-activity-timestamp-in-azure-ad-public-preview"></a>Gérer vos appareils avec le nouveau timestamp d’activité dans Azure AD (préversion publique)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Gestion et inscription des appareils  
**Fonctionnalité de produit :** Gestion du cycle de vie des appareils

Nous sommes conscients qu’au fil du temps, vous devez actualiser et mettre hors service des appareils de votre organisation dans Azure AD, pour éviter la présence d’appareils obsolètes dans votre environnement. Pour faciliter ce processus, Azure AD met maintenant à jour vos appareils avec un nouveau timestamp d’activité, pour vous aider à gérer le cycle de vie de vos appareils.

Pour en savoir plus sur la récupération et l’utilisation de ce timestamp, consultez la page [Procédure : Gérer les appareils obsolètes dans Azure AD](https://docs.microsoft.com/azure/active-directory/devices/manage-stale-devices)

---

### <a name="administrators-can-require-users-to-accept-a-terms-of-use-on-each-device"></a>Les administrateurs peuvent demander aux utilisateurs d’accepter les conditions d’utilisation sur chaque appareil

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Conditions d’utilisation  
**Fonctionnalité de produit :** Gouvernance
 
Les administrateurs peuvent maintenant activer l’option **Require users to consent on every device (Demander le consentement des utilisateurs sur chaque appareil)** pour demander aux utilisateurs d’accepter vos conditions d’utilisation sur chaque appareil à partir duquel ils utilisent votre locataire.

Pour plus d’informations, consultez la section [Conditions d’utilisation par appareil de la page Fonctionnalité Conditions d’utilisation d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/governance/active-directory-tou#per-device-terms-of-use).

---

### <a name="administrators-can-configure-a-terms-of-use-to-expire-based-on-a-recurring-schedule"></a>Les administrateurs peuvent configurer l’expiration des conditions d’utilisation selon une planification périodique

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Conditions d’utilisation  
**Fonctionnalité de produit :** Gouvernance
 

Les administrateurs peuvent maintenant activer l’option **Faire expirer les consentements** pour faire expirer les conditions d’utilisation de tous vos utilisateurs en fonction de votre planification périodique spécifiée. La planification peut être une fois par an, deux fois par an, tous les trimestres ou tous les mois. Une fois que les conditions d’utilisation ont expiré, les utilisateurs doivent les réaccepter.

Pour plus d’informations, consultez la section [Ajouter des conditions d’utilisation de la page Fonctionnalité Conditions d’utilisation d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/governance/active-directory-tou#add-terms-of-use).

---

### <a name="administrators-can-configure-a-terms-of-use-to-expire-based-on-each-users-schedule"></a>Les administrateurs peuvent configurer l’expiration des conditions d’utilisation selon la planification de chaque utilisateur

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Conditions d’utilisation  
**Fonctionnalité de produit :** Gouvernance

Les administrateurs peuvent maintenant spécifier la durée après laquelle l’utilisateur doit réaccepter les conditions d’utilisation. Par exemple, les administrateurs peuvent spécifier que les utilisateurs doivent réaccepter les conditions d’utilisation tous les 90 jours.

Pour plus d’informations, consultez la section [Ajouter des conditions d’utilisation de la page Fonctionnalité Conditions d’utilisation d’Azure Active Directory](https://docs.microsoft.com/azure/active-directory/governance/active-directory-tou#add-terms-of-use).
 
---

### <a name="new-azure-ad-privileged-identity-management-pim-emails-for-azure-active-directory-roles"></a>Nouveaux e-mails Azure Active Directory Privileged Identity Management (PIM) pour les rôles Azure Active Directory

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Privileged Identity Management  
**Fonctionnalité de produit :** Privileged Identity Management
 
Les clients qui utilisent Azure AD Privileged Identity Management (PIM) peuvent à présent recevoir un e-mail de synthèse hebdomadaire, comprenant notamment les informations suivantes pour les sept derniers jours :

- Vue d’ensemble des principales attributions de rôles éligibles et permanentes

- Nombre d’utilisateurs activant des rôles

- Nombre d’utilisateurs attribués à des rôles dans PIM

- Nombre d’utilisateurs attribués à des rôles en dehors de PIM

- Nombre d’utilisateurs « rendus permanents » dans PIM

Pour plus d’informations sur PIM et les notifications par e-mail disponibles, consultez [Notifications par e-mail dans PIM](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-email-notifications).

---

### <a name="group-based-licensing-is-now-generally-available"></a>Disponibilité générale de la gestion des licences basée sur les groupes

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Autres  
**Fonctionnalité de produit :** Répertoire

La gestion des licences basée sur les groupes passe de la préversion publique à la disponibilité générale. Dans le cadre de cette disponibilité générale, nous avons accru la scalabilité de cette fonctionnalité et ajouté la possibilité de retraiter les attributions de la gestion des licences basée sur les groupes pour un seul utilisateur, ainsi que la possibilité d’utiliser la gestion des licences basée sur les groupes avec des licences Office 365 E3/A3.

Pour plus d’informations sur la gestion des licences basée sur les groupes, consultez la page sur la [gestion des licences basée sur les groupes dans Azure Active Directory](https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-licensing-whatis-azure-portal).

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---november-2018"></a>Nouvelles applications fédérées disponibles dans la galerie d’applications Azure AD (novembre 2018)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En novembre 2018, nous avons ajouté dans notre galerie d’applications les 26 nouvelles applications ci-après qui prennent en charge la fédération :

[CoreStack](https://cloud.corestack.io/site/login), [HubSpot](https://docs.microsoft.com/azure/active-directory/saas-apps/HubSpot-tutorial), [GetThere](https://docs.microsoft.com/azure/active-directory/saas-apps/getthere-tutorial), [Gra-Pe](https://docs.microsoft.com/azure/active-directory/saas-apps/grape-tutorial), [eHour](https://getehour.com/try-now), [Consent2Go](https://docs.microsoft.com/azure/active-directory/saas-apps/Consent2Go-tutorial), [Appinux](https://docs.microsoft.com/azure/active-directory/saas-apps/appinux-tutorial), [DriveDollar](https://www.drivedollar.com/Account/Login), [Useall](https://docs.microsoft.com/azure/active-directory/saas-apps/useall-tutorial), [Infinite Campus](https://docs.microsoft.com/azure/active-directory/saas-apps/infinitecampus-tutorial), [Alaya](https://alayagood.com/en/demo/), [HeyBuddy](https://docs.microsoft.com/azure/active-directory/saas-apps/heybuddy-tutorial), [Wrike SAML](https://docs.microsoft.com/azure/active-directory/saas-apps/wrike-tutorial), [Drift](https://docs.microsoft.com/azure/active-directory/saas-apps/drift-tutorial), [Zenegy for Business Central 365](https://accounting.zenegy.com/), [Everbridge Member Portal](https://docs.microsoft.com/azure/active-directory/saas-apps/everbridge-tutorial), [IDEO](https://profile.ideo.com/users/sign_up), [Ivanti Service Manager (ISM)](https://docs.microsoft.com/azure/active-directory/saas-apps/ivanti-service-manager-tutorial), [Peakon](https://docs.microsoft.com/azure/active-directory/saas-apps/peakon-tutorial), [Allbound SSO](https://docs.microsoft.com/azure/active-directory/saas-apps/allbound-sso-tutorial), [Plex Apps - Classic Test](https://test.plexonline.com/signon), [Plex Apps – Classic](https://www.plexonline.com/signon), [Plex Apps - UX Test](https://test.cloud.plex.com/sso), [Plex Apps – UX](https://cloud.plex.com/sso), [Plex Apps – IAM](https://accounts.plex.com/), [CRAFTS - Childcare Records, Attendance, & Financial Tracking System](https://getcrafts.ca/craftsregistration) 

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---

## <a name="october-2018"></a>Octobre 2018

### <a name="azure-ad-logs-now-work-with-azure-log-analytics-public-preview"></a>Les journaux Azure AD fonctionnent maintenant avec Azure Log Analytics (préversion publique)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Monitoring et création de rapports

Nous sommes heureux d’annoncer que vous pouvez maintenant transférer vos journaux Azure AD vers Azure Log Analytics ! Grâce à cette fonctionnalité très demandée, vous pouvez encore mieux accéder aux analyses de votre activité, de vos opérations et de votre sécurité, et elle vous aide à surveiller votre infrastructure. Pour plus d’informations, consultez le blog [Journaux d’activité Azure Active Directory dans Azure Log Analytics désormais disponible](https://techcommunity.microsoft.com/t5/Azure-Active-Directory-Identity/Azure-Active-Directory-Activity-logs-in-Azure-Log-Analytics-now/ba-p/274843).

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---october-2018"></a>Nouvelles applications fédérées disponibles dans la galerie d'applications Azure AD (octobre 2018)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En octobre 2018, nous avons ajouté à notre galerie d’applications les 14 nouvelles applications ci-dessous, qui prennent en charge la fédération :

[My Award Points](https://docs.microsoft.com/azure/active-directory/saas-apps/myawardpoints-tutorial), [Vibe HCM](https://docs.microsoft.com/azure/active-directory/saas-apps/vibehcm-tutorial), ambyint, [MyWorkDrive](https://docs.microsoft.com/azure/active-directory/saas-apps/myworkdrive-tutorial), [BorrowBox](https://docs.microsoft.com/azure/active-directory/saas-apps/borrowbox-tutorial), Dialpad, [ON24 Virtual Environment](https://docs.microsoft.com/azure/active-directory/saas-apps/on24-tutorial), [RingCentral](https://docs.microsoft.com/azure/active-directory/saas-apps/ringcentral-tutorial), [Zscaler Three](https://docs.microsoft.com/azure/active-directory/saas-apps/zscaler-three-tutorial), [Phraseanet](https://docs.microsoft.com/azure/active-directory/saas-apps/phraseanet-tutorial), [Appraisd](https://docs.microsoft.com/azure/active-directory/saas-apps/appraisd-tutorial), [Workspot Control](https://docs.microsoft.com/azure/active-directory/saas-apps/workspotcontrol-tutorial), [Shuccho Navi](https://docs.microsoft.com/azure/active-directory/saas-apps/shucchonavi-tutorial), [Glassfrog](https://docs.microsoft.com/azure/active-directory/saas-apps/glassfrog-tutorial)

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---

### <a name="azure-ad-domain-services-email-notifications"></a>Notifications par e-mail pour Azure AD Domain Services

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Services de domaine Azure AD  
**Fonctionnalité de produit :** Services de domaine Azure AD

Azure AD Domain Services fournit sur le portail Azure des alertes sur les erreurs de configuration ou les problèmes avec votre domaine géré. Ces alertes incluent des guides pas à pas pour que vous puissiez essayer de résoudre les problèmes sans avoir à contacter le support.

En octobre, vous serez en mesure de personnaliser les paramètres de notification pour votre domaine managé afin d’en cas de nouvelles alertes, un e-mail soit envoyé à un groupe de personnes désigné, ce qui évite de devoir vérifier en permanence le portail pour détecter les mises à jour.

Pour plus d’informations, consultez [Paramètres de notification dans Azure AD Domain Services](https://docs.microsoft.com/azure/active-directory-domain-services/active-directory-ds-notifications).

---

### <a name="azure-ad-portal-supports-using-the-forcedelete-domain-api-to-delete-custom-domains"></a>Le portail Azure AD assure la prise en charge à l’aide de l’API du domaine ForceDelete pour supprimer des domaines personnalisés. 

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Gestion de répertoires  
**Fonctionnalité de produit :** Répertoire

Nous sommes heureux de vous annoncer que vous pouvez maintenant utiliser l'API de domaine ForceDelete pour supprimer vos noms de domaine personnalisés en renommant de façon asynchrone les références, comme les utilisateurs, les groupes et les applications de votre nom de domaine personnalisé (contoso.com) pour revenir au nom de domaine par défaut initial (contoso.onmicrosoft.com).

Ce changement vous permet de supprimer plus rapidement vos noms de domaine personnalisés si votre organisation n'utilise plus le nom, ou si vous devez utiliser le nom de domaine avec un autre AD Azure.

Pour plus d’informations, consultez [Supprimer un nom de domaine personnalisé](https://docs.microsoft.com/azure/active-directory/users-groups-roles/domains-manage#delete-a-custom-domain-name).

---

## <a name="september-2018"></a>Septembre 2018
 
### <a name="updated-administrator-role-permissions-for-dynamic-groups"></a>Mise à jour des autorisations des rôles d’administrateur pour les groupes dynamiques

**Type :** Résolution  
**Catégorie de service :** Gestion des groupes  
**Fonctionnalité de produit :** Collaboration

Nous avons résolu un problème afin que des rôles d’administrateur spécifiques soient désormais en mesure de créer et mettre à jour des règles d’appartenance dynamique sans avoir besoin d’être le propriétaire du groupe.

Ces rôles sont les suivants :

- Administrateur général ou Rédacteur d’entreprise

- Administrateur de services Intune

- Administrateur de compte utilisateur

Pour plus d’informations, consultez l’article [Créer un groupe dynamique et vérifier l’état](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-create-rule).

---

### <a name="simplified-single-sign-on-sso-configuration-settings-for-some-third-party-apps"></a>Simplification des paramètres de configuration d’authentification unique (SSO) pour certaines applications tierces

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Authentification unique

Nous sommes conscients que la configuration de l’authentification unique (SSO) pour les applications SaaS (software as a service) peut se révéler complexe en raison du caractère unique de chaque configuration d’application. Nous avons conçu une expérience de configuration simplifiée qui renseigne automatiquement les paramètres de configuration SSO pour les applications SaaS tierces suivantes :

- Zendesk

- ArcGis Online

- Jamf Pro

Pour commencer à utiliser cette expérience en un clic, accédez au **Portail Azure** > page **Configuration de l’authentification unique** de l’application. Pour plus d’informations, consultez l’article [Intégration des applications SaaS avec Azure Active Directory](https://docs.microsoft.com/azure/active-directory/saas-apps/tutorial-list).

---

### <a name="azure-active-directory---where-is-your-data-located-page"></a>Page Azure Active Directory - Where is your data located? (Azure Active Directory - Où se trouvent vos données ?)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Autres  
**Fonctionnalité de produit :** GoLocal

Sur la page **Azure Active Directory - Where is your data located?** (Azure Active Directory - Où se trouvent vos données ?), sélectionnez la région de votre entreprise pour connaître le centre de données Azure qui héberge vos données Azure AD au repos pour tous les services Azure AD. Vous pouvez filtrer les informations par service Azure AD pour la région de votre entreprise.

Pour accéder à cette fonctionnalité et pour obtenir plus d’informations, consultez l’article [Azure Active Directory - Where is your data located?](https://aka.ms/AADDataMap) (Azure Active Directory - Où se trouvent vos données ?).

---

### <a name="new-deployment-plan-available-for-the-my-apps-access-panel"></a>Nouveau plan de déploiement disponible pour le panneau d’accès MyApps

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** My Apps  
**Fonctionnalité de produit :** Authentification unique

Consultez le nouveau plan de déploiement disponible pour le panneau d’accès MyApps (https://aka.ms/deploymentplans).
Le panneau d’accès MyApps permet aux utilisateurs de rechercher l’ensemble de leurs applications et d’y accéder à partir d’un emplacement unique. Ce portail offre également aux utilisateurs différentes fonctionnalités en libre-service, telles que des fonctions de demande d’accès aux applications et aux groupes ou de gestion de l’accès à ces ressources pour le compte d’autres utilisateurs.

Pour plus d’informations, consultez l’article [Qu’est-ce que le portail MyApps ?](https://docs.microsoft.com/azure/active-directory/user-help/active-directory-saas-access-panel-introduction).

---

### <a name="new-troubleshooting-and-support-tab-on-the-sign-ins-logs-page-of-the-azure-portal"></a>Nouvel onglet Résolution des problèmes et support sur la page des journaux de connexions du Portail Azure

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Monitoring et création de rapports

Le nouvel onglet **Résolution des problèmes et support** de la page **Connexions** du Portail Azure est destinée à aider les administrateurs et les ingénieurs du support à résoudre les problèmes liés aux connexions Azure AD. Ce nouvel onglet fournit le code d’erreur, le message d’erreur et des recommandations de correction (le cas échéant) pour faciliter la résolution du problème. Si vous ne parvenez pas à résoudre le problème, nous vous indiquons également une nouvelle façon de créer un ticket de support à l’aide de l’expérience **Copier dans le Presse-papiers**, qui remplit les champs **ID de demande** et **Date (UTC)** pour le fichier journal dans votre ticket de support.  

![Journaux de connexions avec le nouvel onglet](media/whats-new/troubleshooting-and-support.png)

---

### <a name="enhanced-support-for-custom-extension-properties-used-to-create-dynamic-membership-rules"></a>Amélioration de la prise en charge des propriétés d’extension personnalisées utilisées pour créer des règles d’appartenance dynamique

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Gestion des groupes  
**Fonctionnalité de produit :** Collaboration

Grâce à cette mise à jour, vous pouvez désormais cliquer sur le lien **Get custom extension properties** (Obtenir les propriétés d’extension personnalisées) du générateur de règles de groupe d’utilisateurs dynamiques, entrer votre ID d’application unique et recevoir la liste complète des propriétés d’extension personnalisées à utiliser lors de la création d’une règle d’appartenance dynamique pour les utilisateurs. Vous pouvez également actualiser cette liste afin d’obtenir les nouvelles propriétés d’extension personnalisées pour cette application.

Pour plus d’informations sur l’utilisation de propriétés d’extension personnalisées pour les règles d’appartenance dynamiques, consultez la section [Attributs d’extension et propriétés d’extension personnalisée](https://docs.microsoft.com/azure/active-directory/users-groups-roles/groups-dynamic-membership#extension-properties-and-custom-extension-properties).

---

### <a name="new-approved-client-apps-for-azure-ad-app-based-conditional-access"></a>Nouvelles applications clientes approuvées pour l’accès conditionnel basé sur les applications Azure AD

**Type :** Modification planifiée  
**Catégorie de service :** Accès conditionnel  
**Fonctionnalité de produit :** Protection et sécurité des identités

Les applications suivantes se trouvent sur la liste des [applications clientes approuvées](https://docs.microsoft.com/azure/active-directory/conditional-access/technical-reference#approved-client-app-requirement) :

- Microsoft To-Do

- Microsoft Stream

Pour plus d'informations, consultez les pages suivantes :

- [Accès conditionnel basé sur les applications Azure AD](https://docs.microsoft.com/azure/active-directory/conditional-access/app-based-conditional-access)

---

### <a name="new-support-for-self-service-password-reset-from-the-windows-7881-lock-screen"></a>Nouvelle prise en charge de la réinitialisation de mot de passe en libre-service à partir de l’écran de verrouillage Windows 7/8/8.1

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** SSPR  
**Fonctionnalité de produit :** Authentification utilisateur

Une fois que vous avez configuré cette nouvelle fonctionnalité, vos utilisateurs voient s’afficher un lien leur permettant de réinitialiser leur mot de passe à partir de l’écran **Verrouiller** d’un appareil exécutant Windows 7, Windows 8 ou Windows 8.1. En cliquant sur ce lien, l’utilisateur est orienté vers le même flux de réinitialisation de mot de passe que par le biais du navigateur web.

Pour plus d’informations, consultez l’article [How to enable password reset from Windows 7, 8, and 8.1](https://aka.ms/ssprforwindows78) (Activation de la réinitialisation de mot de passe à partir de Windows 7, 8 et 8.1).

---

### <a name="change-notice-authorization-codes-will-no-longer-be-available-for-reuse"></a>Notification de modification : Les codes d’autorisation ne pourront plus être réutilisés 

**Type :** Modification planifiée  
**Catégorie de service :** Authentifications (connexions)  
**Fonctionnalité de produit :** Authentification utilisateur

À compter du 15 novembre 2018, Azure AD n’acceptera plus les codes d’authentification utilisés pour les applications. Cette modification de sécurité a pour but d’assurer la conformité d’Azure AD avec la spécification OAuth et s’appliquera aux points de terminaison v1 et v2.

Si votre application réutilise des codes d’autorisation pour obtenir des jetons pour différentes ressources, nous vous recommandons d’utiliser le code pour obtenir un jeton d’actualisation, puis d’utiliser ce jeton d’actualisation pour acquérir des jetons supplémentaires pour d’autres ressources. Les codes d’autorisation ne peuvent être utilisés qu’une seule fois, tandis que les jetons d’actualisation peuvent être utilisés plusieurs fois sur différentes ressources. Toute application qui tente de réutiliser un code d’authentification pendant le flux de code OAuth obtient une erreur invalid_grant.

Pour découvrir les modifications liées à ce protocole et à d’autres protocoles, consultez la [liste complète des nouveautés en matière d’authentification](https://docs.microsoft.com/azure/active-directory/develop/reference-breaking-changes).

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---september-2018"></a>Nouvelles applications fédérées disponibles dans la galerie d’applications Azure AD - Septembre 2018

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En septembre 2018, nous avons ajouté à notre galerie d’applications les 16 nouvelles applications ci-après qui prennent en charge la fédération :

[Uberflip](https://docs.microsoft.com/azure/active-directory/saas-apps/uberflip-tutorial), [Comeet Recruiting Software](https://docs.microsoft.com/azure/active-directory/saas-apps/comeetrecruitingsoftware-tutorial), [Workteam](https://docs.microsoft.com/azure/active-directory/saas-apps/workteam-tutorial), [ArcGIS Enterprise](https://docs.microsoft.com/azure/active-directory/saas-apps/arcgisenterprise-tutorial), [Nuclino](https://docs.microsoft.com/azure/active-directory/saas-apps/nuclino-tutorial), [JDA Cloud](https://docs.microsoft.com/azure/active-directory/saas-apps/jdacloud-tutorial), [Snowflake](https://docs.microsoft.com/azure/active-directory/saas-apps/snowflake-tutorial), NavigoCloud, [Figma](https://docs.microsoft.com/azure/active-directory/saas-apps/figma-tutorial), join.me, [ZephyrSSO](https://docs.microsoft.com/azure/active-directory/saas-apps/zephyrsso-tutorial), [Silverback](https://docs.microsoft.com/azure/active-directory/saas-apps/silverback-tutorial), Riverbed Xirrus EasyPass, [Rackspace SSO](https://docs.microsoft.com/azure/active-directory/saas-apps/rackspacesso-tutorial), Enlyft SSO for Azure, SurveyMonkey, [Convene](https://docs.microsoft.com/azure/active-directory/saas-apps/convene-tutorial), [dmarcian](https://docs.microsoft.com/azure/active-directory/saas-apps/dmarcian-tutorial)

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---

### <a name="support-for-additional-claims-transformations-methods"></a>Prise en charge de méthodes de transformation de revendication supplémentaires

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Authentification unique

Nous avons introduit de nouvelles méthodes de transformation de revendication, ToLower() et ToUpper(), qui sont applicables aux jetons SAML à partir de la page **Configuration de l’authentification unique** basée sur SAML.

Pour plus d’informations, consultez l’article [Procédure : personnaliser des revendications émises dans le jeton SAML pour les applications d’entreprise dans Azure AD](https://docs.microsoft.com/azure/active-directory/develop/active-directory-saml-claims-customization).

---

### <a name="updated-saml-based-app-configuration-ui-preview"></a>Mise à jour de l’interface utilisateur de configuration d’applications basées sur SAML (préversion)

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Authentification unique

L’interface utilisateur de configuration d’applications basées sur SAML que nous avons mise à jour vous offre :

- une expérience améliorée de configuration pas à pas de vos applications SAML ;

- un surcroît de visibilité sur les éléments manquants ou incorrects de votre configuration ;

- la possibilité d’ajouter plusieurs adresses e-mail pour la notification d’expiration du certificat ;

- de nouvelles méthodes de transformation de revendication, ToLower() et ToUpper(), et bien plus encore ;

- un moyen de charger votre propre certificat de signature de jetons pour vos applications d’entreprise ;

- la possibilité de définir le format NameID pour les applications SAML et de définir la valeur NameID sous forme d’Extensions d’annuaire.

Pour activer cet affichage mis à jour, cliquez sur le lien **Essayer la nouvelle expérience** en haut de la page **Authentification unique**. Pour plus d’informations, consultez [Tutoriel : Configurez l’authentification unique SAML pour une application avec Azure Active Directory](https://docs.microsoft.com/azure/active-directory/manage-apps/configure-single-sign-on-portal).

---

## <a name="august-2018"></a>Août 2018

### <a name="changes-to-azure-active-directory-ip-address-ranges"></a>Modifications apportées aux plages d’adresses IP Azure Active Directory

**Type :** Modification planifiée  
**Catégorie de service :** Autres  
**Fonctionnalité de produit :** Plateforme

Nous sommes en train d’introduire dans Azure AD des plages d’adresses IP plus vastes. Si vous avez configuré des plages d’adresses IP Azure AD pour vos pare-feu, routeurs ou groupes de sécurité réseau, vous allez donc devoir les mettre à jour. Nous procédons à cette mise à jour afin que vous n’ayez pas à modifier à nouveau les configurations de plage IP de votre pare-feu, routeur ou groupe de sécurité réseau lorsque Azure AD ajoute de nouveaux points de terminaison. 

Le trafic réseau va migrer vers ces nouvelles plages au cours des deux prochains mois. Pour ne pas interrompre le service, vous devez ajouter ces nouvelles valeurs à vos adresses IP avant le 10 septembre 2018 :

- 20.190.128.0/18 

- 40.126.0.0/18 

Nous vous recommandons vivement de ne pas supprimer les anciennes plages d’adresses IP tant que votre trafic réseau n’a pas été entièrement migré vers les nouvelles plages. Pour obtenir des informations sur la migration et savoir quand vous pouvez supprimer les anciennes plages, consultez [URL et plages d’adresses IP Office 365](https://support.office.com/article/Office-365-URLs-and-IP-address-ranges-8548a211-3fe7-47cb-abb1-355ea5aa88a2).

---

### <a name="change-notice-authorization-codes-will-no-longer-be-available-for-reuse"></a>Notification de modification : Les codes d’autorisation ne pourront plus être réutilisés 

**Type :** Modification planifiée  
**Catégorie de service :** Authentifications (connexions)  
**Fonctionnalité de produit :** Authentification utilisateur

À compter du 15 novembre 2018, Azure AD n’acceptera plus les codes d’authentification utilisés pour les applications. Cette modification de sécurité a pour but d’assurer la conformité d’Azure AD avec la spécification OAuth et s’appliquera aux points de terminaison v1 et v2.

Si votre application réutilise des codes d’autorisation pour obtenir des jetons pour différentes ressources, nous vous recommandons d’utiliser le code pour obtenir un jeton d’actualisation, puis d’utiliser ce jeton d’actualisation pour acquérir des jetons supplémentaires pour d’autres ressources. Les codes d’autorisation ne peuvent être utilisés qu’une seule fois, tandis que les jetons d’actualisation peuvent être utilisés plusieurs fois sur différentes ressources. Toute application qui tente de réutiliser un code d’authentification pendant le flux de code OAuth obtient une erreur invalid_grant.

Pour découvrir les modifications liées à ce protocole et à d’autres protocoles, consultez la [liste complète des nouveautés en matière d’authentification](https://docs.microsoft.com/azure/active-directory/develop/reference-breaking-changes).
 
---

### <a name="converged-security-info-management-for-self-service-password-sspr-and-multi-factor-authentication-mfa"></a>Informations de sécurité convergées pour le mot de passe en libre-service (SSPR) et l’authentification multifacteur (MFA)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** SSPR  
**Fonctionnalité de produit :** Authentification utilisateur
 
Cette nouvelle fonctionnalité permet de gérer les informations de sécurité (numéro de téléphone, application mobile, etc.) pour SSPR et MFA de manière centralisée, alors qu’elles étaient auparavant dispersées à deux emplacements différents.

Cette centralisation fonctionne également pour les personnes utilisant soit SSPR, soit MFA. En outre, si votre entreprise n’impose pas l’inscription MFA ou SSPR, les utilisateurs peuvent toujours inscrire les méthodes d’informations de sécurité MFA ou SSPR autorisées par leur entreprise à partir du portail My Apps.

Il s’agit d’une inscription à une version préliminaire publique. Les administrateurs peuvent activer la nouvelle expérience (le cas échéant) pour un groupe sélectionné ou tous les utilisateurs d’un client. Pour plus d’informations sur cette centralisation, consultez le [blog Converged experience](https://cloudblogs.microsoft.com/enterprisemobility/2018/08/06/mfa-and-sspr-updates-now-in-public-preview/).

---

### <a name="new-http-only-cookies-setting-in-azure-ad-application-proxy-apps"></a>Nouveau paramètre Cookies HTTP uniquement dans les applications de proxy d’application Azure AD

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Proxy d’application  
**Fonctionnalité de produit :** Contrôle d’accès

Il existe un nouveau paramètre nommé **Cookies HTTP uniquement** dans vos applications de proxy d’application. Ce paramètre assure une sécurité supplémentaire en incluant l’indicateur HTTPOnly dans l’en-tête de réponse HTTP des cookies de session et d’accès au proxy d’application, en bloquant l’accès au cookie depuis un script côté client et en empêchant des actions telles que la copie ou la modification du cookie. Bien que cet indicateur n’ait jamais été utilisé auparavant, vos cookies ont toujours été chiffrés et transmis au moyen d’une connexion SSL pour vous protéger contre les modifications incorrectes.

Ce paramètre n’est pas compatible avec les applications utilisant les contrôles ActiveX, telles que Bureau à distance. Le cas échéant, nous vous recommandons de désactiver ce paramètre.

Pour plus d’informations sur le paramètre Cookies HTTP uniquement, voir [Publier des applications avec le proxy d’application Azure AD](https://docs.microsoft.com/azure/active-directory/manage-apps/application-proxy-publish-azure-portal).

---

### <a name="privileged-identity-management-pim-for-azure-resources-supports-management-group-resource-types"></a>Privileged Identity Management (PIM) pour les ressources Azure prend en charge les types de ressources Groupe d’administration

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Privileged Identity Management  
**Fonctionnalité de produit :** Privileged Identity Management
 
Les paramètres d’activation et d’attribution juste-à-temps peuvent désormais être appliqués aux types de ressources Groupe d’administration, comme vous le faites déjà pour les abonnements, les groupes de ressources et les ressources (telles que les machines virtuelles, App Services et bien plus encore). En outre, toute personne disposant d’un rôle donnant un accès administrateur pour un Groupe d’administration peut découvrir et gérer cette ressource dans PIM.

Pour plus d’informations sur PIM et les ressources Azure, voir [Découvrir et gérer les ressources Azure à l’aide de Privileged Identity Management](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-resource-roles-discover-resources).
 
---

### <a name="application-access-preview-provides-faster-access-to-the-azure-ad-portal"></a>L’accès à l’application (version préliminaire) assure un accès plus rapide au portail Azure AD

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Privileged Identity Management  
**Fonctionnalité de produit :** Privileged Identity Management
 
Aujourd'hui, lors de l’activation d’un rôle avec PIM, l’application des autorisations peut prendre jusqu'à 10 minutes. Si vous choisissez d’utiliser l’accès Application, qui est actuellement en version préliminaire publique, les administrateurs peuvent accéder au portail Azure AD dès l’envoi de la demande d’activation.

Actuellement, l’accès Application prend uniquement en charge l’utilisation du portail Azure AD et les ressources Azure. Pour plus d’informations sur PIM et l’accès Application, voir [Qu’est-ce qu’Azure AD Privileged Identity Management ?](https://docs.microsoft.com/azure/active-directory/privileged-identity-management/pim-configure).
 
---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---august-2018"></a>Nouvelles applications fédérées disponibles dans la galerie Azure AD App - Août 2018

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En août 2018, nous avons ajouté à notre galerie d’applications les 16 applications suivantes qui prennent en charge la fédération :

[Hornbill](https://docs.microsoft.com/azure/active-directory/saas-apps/hornbill-tutorial), [Bridgeline Unbound](https://docs.microsoft.com/azure/active-directory/saas-apps/bridgelineunbound-tutorial), [Sauce Labs - Mobile and Web Testing](https://docs.microsoft.com/azure/active-directory/saas-apps/saucelabs-mobileandwebtesting-tutorial), [Meta Networks Connector](https://docs.microsoft.com/azure/active-directory/saas-apps/metanetworksconnector-tutorial), [Way We Do](https://docs.microsoft.com/azure/active-directory/saas-apps/waywedo-tutorial), [Spotinst](https://docs.microsoft.com/azure/active-directory/saas-apps/spotinst-tutorial), [ProMaster (par Inlogik)](https://docs.microsoft.com/azure/active-directory/saas-apps/promaster-tutorial), SchoolBooking, [4me](https://docs.microsoft.com/azure/active-directory/saas-apps/4me-tutorial), [Dossier](https://docs.microsoft.com/azure/active-directory/saas-apps/DOSSIER-tutorial), [N2F - Expense reports](https://docs.microsoft.com/azure/active-directory/saas-apps/n2f-expensereports-tutorial), [Comm100 Live Chat](https://docs.microsoft.com/azure/active-directory/saas-apps/comm100livechat-tutorial), [SafeConnect](https://docs.microsoft.com/azure/active-directory/saas-apps/safeconnect-tutorial), [ZenQMS](https://docs.microsoft.com/azure/active-directory/saas-apps/zenqms-tutorial), [eLuminate](https://docs.microsoft.com/azure/active-directory/saas-apps/eluminate-tutorial), [Dovetale](https://docs.microsoft.com/azure/active-directory/saas-apps/dovetale-tutorial).

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---

### <a name="native-tableau-support-is-now-available-in-azure-ad-application-proxy"></a>La prise en charge native de Tableau est désormais disponible dans le proxy d’application Azure AD

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Proxy d’application  
**Fonctionnalité de produit :** Contrôle d’accès

Grâce à notre mise à jour d’OpenID Connect vers le protocole OAuth 2.0 Code Grant pour notre protocole d’authentification préalable, vous n’avez plus de configuration supplémentaire à effectuer pour utiliser Tableau avec le proxy d’application. Ce changement de protocole aide également le proxy d’application à mieux prendre en charge les applications plus récentes en utilisant uniquement les redirections HTTP, qui sont couramment prises en charge dans les balises HTML et JavaScript.

Pour plus d’informations sur la prise en charge native de Tableau, voir [Proxy d’application Azure AD offre désormais la prise en charge native de Tableau](https://blogs.technet.microsoft.com/applicationproxyblog/2018/08/14/azure-ad-application-proxy-now-with-native-tableau-support).

---

### <a name="new-support-to-add-google-as-an-identity-provider-for-b2b-guest-users-in-azure-active-directory-preview"></a>Nouvelle prise en charge pour ajouter Google comme fournisseur d’identité pour les utilisateurs invités B2B dans Azure Active Directory (version préliminaire)

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** B2B  
**Fonctionnalité de produit :** B2B/B2C

En configurant la fédération avec Google dans votre organisation, vous pouvez laisser les utilisateurs Gmail invités se connecter à vos applications et ressources partagées à l’aide de leur compte Google, sans qu’ils aient besoin de créer un compte Microsoft (compte de service administré ou MSA) personnel ou un compte Azure AD.

Il s’agit d’une inscription à une version préliminaire publique. Pour plus d’informations sur la fédération Google, voir [Ajouter Google comme fournisseur d’identité pour les utilisateurs invités B2B](https://docs.microsoft.com/azure/active-directory/b2b/google-federation).

---

## <a name="july-2018"></a>Juillet 2018

### <a name="improvements-to-azure-active-directory-email-notifications"></a>Améliorations apportées aux notifications par e-mail Azure Active Directory

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Autres  
**Fonctionnalité de produit :** Gestion du cycle de vie des identités
 
Azure Active Directory (Azure AD) a une nouvelle conception visuelle, ainsi qu’un nouvel expéditeur, avec une nouvelle adresse e-mail et un nouveau nom d’affichage, lorsqu’ils proviendront des services suivants :
 
- Révisions d’accès Azure AD
- Azure AD Connect Health 
- Azure AD Identity Protection 
- Azure AD Privileged Identity Management
- Notifications de l’expiration prochaine des certificats des applications d’entreprise
- Notifications du service de provisionnement des applications d’entreprise
 
Les notifications par e-mail proviendront de l’adresse e-mail et du nom d’affichage suivants :

- Adresse e-mail : azure-noreply@microsoft.com
- Nom complet : Microsoft Azure
 
Pour voir un exemple de nouvelle notification et obtenir plus d’informations, consultez [Notifications par e-mail dans Azure AD Privileged Identity Management](https://go.microsoft.com/fwlink/?linkid=2005832).

---

### <a name="azure-ad-activity-logs-are-now-available-through-azure-monitor"></a>Les journaux d’activité Azure AD sont désormais disponibles via Azure Monitor

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Monitoring et création de rapports

Les journaux d’activité Azure AD sont désormais disponibles en version préliminaire publique pour Azure Monitor (service de supervision à l’échelle de la plateforme d’Azure). Azure Monitor vous offre une rétention à long terme et une intégration transparente, en plus de ces améliorations :

- Rétention à long terme par le routage de vos fichiers journaux sur votre propre compte de stockage Azure.

- Intégration transparente de SIEM, sans avoir à écrire ou gérer des scripts personnalisés.

- Intégration transparente avec vos propres solutions personnalisées, outils d’analytique ou solutions de gestion des incidents.

Pour plus d’informations sur ces nouvelles fonctionnalités, consultez notre blog [Les journaux d’activité d’Azure AD dans Azure Monitor diagnostics est désormais disponible en version préliminaire publique](https://cloudblogs.microsoft.com/enterprisemobility/2018/07/26/azure-ad-activity-logs-in-azure-monitor-diagnostics-now-in-public-preview/) et notre documentation, [Journaux d’activité d’Azure Active Directory dans Azure Monitor (préversion)](https://docs.microsoft.com/azure/active-directory/reporting-azure-monitor-diagnostics-overview).

---

### <a name="conditional-access-information-added-to-the-azure-ad-sign-ins-report"></a>Informations d’accès conditionnel ajoutées au rapport de connexion Azure AD

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Protection et sécurité des identités
 
Cette mise à jour vous permet de voir quelles stratégies sont évaluées lorsqu’un utilisateur se connecte, ainsi que le résultat de la stratégie. En outre, le rapport inclut désormais le type d’application client utilisé par l’utilisateur, pour que vous puissiez identifier le trafic de protocole hérité. Les entrées de rapport peuvent également désormais rechercher un ID de corrélation, qui se trouve dans le message d’erreur visible par l’utilisateur et peuvent être utilisées pour identifier et résoudre les problèmes de la requête de connexion correspondante.

---

### <a name="view-legacy-authentications-through-sign-ins-activity-logs"></a>Afficher les authentifications héritées via les journaux d’activité de connexions

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Reporting  
**Fonctionnalité de produit :** Monitoring et création de rapports
 
Avec le nouveau champ **Application cliente** des journaux d’activité de connexions, les clients peuvent désormais voir les utilisateurs qui utilisent des authentifications héritées. Les clients peuvent accéder à ces informations à l’aide de l’API Microsoft Graph Connexions ou via les journaux d’activité de connexions dans le portail Azure AD et ainsi utiliser la commande **Application cliente** pour filtrer les authentifications héritées. Pour plus de détails, consultez la documentation.

---

### <a name="new-federated-apps-available-in-azure-ad-app-gallery---july-2018"></a>Nouvelles applications fédérées disponibles dans la galerie Azure AD App - Juillet 2018

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Applications d’entreprise  
**Fonctionnalité de produit :** Intégration tierce
 
En juillet 2018, nous avons ajouté à notre galerie d’applications les 16 applications suivantes qui prennent en charge la fédération :

[Hub de l’innovation](https://docs.microsoft.com/azure/active-directory/saas-apps/innovationhub-tutorial), [Leapsome](https://docs.microsoft.com/azure/active-directory/saas-apps/leapsome-tutorial), [Authentification unique pour certains administrateurs](https://docs.microsoft.com/azure/active-directory/saas-apps/certainadminsso-tutorial), mise en lots PSUC, [iPass SmartConnect](https://docs.microsoft.com/azure/active-directory/saas-apps/ipasssmartconnect-tutorial), [Screencast-O-Matic](https://docs.microsoft.com/azure/active-directory/saas-apps/screencast-tutorial), Classe unifiée de PowerSchool, [intégration Eli](https://docs.microsoft.com/azure/active-directory/saas-apps/elionboarding-tutorial), [prise en charge à distance Bomgar](https://docs.microsoft.com/azure/active-directory/saas-apps/bomgarremotesupport-tutorial), [Nimblex](https://docs.microsoft.com/azure/active-directory/saas-apps/nimblex-tutorial), [Imagineer WebVision](https://docs.microsoft.com/azure/active-directory/saas-apps/imagineerwebvision-tutorial), [Insight4GRC](https://docs.microsoft.com/azure/active-directory/saas-apps/insight4grc-tutorial), [Connecteur SecureW2 JoinNow](https://docs.microsoft.com/azure/active-directory/saas-apps/securejoinnow-tutorial), [Kanbanize](https://review.docs.microsoft.com/azure/active-directory/saas-apps/kanbanize-tutorial), [SmartLPA](https://review.docs.microsoft.com/azure/active-directory/saas-apps/smartlpa-tutorial), [Base de compétences](https://docs.microsoft.com/azure/active-directory/saas-apps/skillsbase-tutorial)

Pour plus d’informations sur les applications, consultez [Intégration des applications SaaS à Azure Active Directory](https://aka.ms/appstutorial). Pour plus d’informations sur le référencement de votre application dans la galerie Azure AD App, consultez [Lister votre application dans la galerie d’applications Azure Active Directory](https://aka.ms/azureadapprequest).

---
 
### <a name="new-user-provisioning-saas-app-integrations---july-2018"></a>Nouvelles intégrations d’applications SaaS pour l’attribution d’utilisateurs - juillet 2018

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** Provisionnement d’applications  
**Fonctionnalité de produit :** Intégration tierce
 
Azure AD vous permet d’automatiser la création, la maintenance et la suppression d’identités utilisateur dans des applications SaaS comme Dropbox, Salesforce, ServiceNow, etc. En juillet 2018, nous avons ajouté une prise en charge de l’attribution des utilisateurs pour les applications suivantes dans la galerie d’applications Azure AD :

- [Cisco Spark](https://docs.microsoft.com/azure/active-directory/saas-apps/cisco-spark-provisioning-tutorial)

- [Cisco WebEx](https://docs.microsoft.com/azure/active-directory/saas-apps/cisco-webex-provisioning-tutorial)

- [Bonusly](https://docs.microsoft.com/azure/active-directory/saas-apps/bonusly-provisioning-tutorial)

Pour obtenir la liste de toutes les applications qui prennent en charge l’attribution d’utilisateurs dans la galerie Azure AD, consultez [Intégration d’application SaaS avec Azure Active Directory](https://aka.ms/appstutorial).

---

### <a name="connect-health-for-sync---an-easier-way-to-fix-orphaned-and-duplicate-attribute-sync-errors"></a>Connect Health pour la synchronisation - un moyen plus simple pour corriger les erreurs de synchronisation d’attribut en double et orphelins

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** AD Connect  
**Fonctionnalité de produit :** Monitoring et création de rapports
 
Azure AD Connect Health introduit la mise à jour du libre-service pour vous aider à mettre en surbrillance et corriger les erreurs de synchronisation. Cette fonctionnalité résout les erreurs de synchronisation d’attribut en double et corrige les objets qui sont orphelins à partir d’Azure AD. Ce diagnostic offre les avantages suivants :

- Permet de réduire les erreurs de synchronisation d’attribut en double, en fournissant des corrections spécifiques

- Applique une correction pour les scénarios Azure AD dédiés, résolution des erreurs en une seule étape

- Aucune mise à niveau ou configuration n’est nécessaire pour démarrer et utiliser cette fonctionnalité

Pour plus d’informations, consultez [Diagnostiquer et corriger les erreurs de synchronisation d’attribut en double](https://docs.microsoft.com/azure/active-directory/connect-health/active-directory-aadconnect-health-diagnose-sync-errors)

---

### <a name="visual-updates-to-the-azure-ad-and-msa-sign-in-experiences"></a>Mises à jour de Visual à Azure AD et expériences de connexion MSA

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Azure AD  
**Fonctionnalité de produit :** Authentification utilisateur

Nous mettons à jour l’interface utilisateur pour l’expérience de connexion des services en ligne de Microsoft, tels qu’Office 365 et Azure. Cette modification rend les écrans plus simples et moins encombrés. Pour plus d’informations sur cette modification, consultez le blog [Améliorations à venir à l’expérience de connexion Azure AD](https://cloudblogs.microsoft.com/enterprisemobility/2018/04/04/upcoming-improvements-to-the-azure-ad-sign-in-experience/).

---

### <a name="new-release-of-azure-ad-connect---july-2018"></a>Nouvelle version d’Azure AD Connect - juillet 2018

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Provisionnement d’applications  
**Fonctionnalité de produit :** Gestion du cycle de vie des identités

La dernière version d’Azure AD Connect comprend : 

- Correctifs de bogues et mises à jour de la prise en charge 

- Disponibilité générale de l’intégration Ping Federate

- Mises à jour de la dernière SQL 2012 du client 

Pour plus d’informations sur cette mise à jour, consultez [Azure AD Connect : Historique de publication des versions](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-version-history)

---

### <a name="updates-to-the-terms-of-use-tou-end-user-ui"></a>Mises à jour de l’interface utilisateur des conditions d’utilisation (conditions d’utilisation)

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Conditions d’utilisation  
**Fonctionnalité de produit :** Gouvernance

Nous mettons à jour la chaîne de l’acceptation de l’interface utilisateur des conditions d’utilisation.

**Texte actif**  Vous devez accepter les conditions d'utilisation pour accéder aux ressources [tenantName].<br>**Nouveau texte.** Vous devez lire les conditions d'utilisation pour accéder à la ressource [tenantName].

**Texte actuel :** Choosing to accept means that you agree to all of the above terms of use. (Accepter signifie que vous acceptez les conditions d’utilisation ci-dessus.)<br>**Nouveau texte :** Please click Accept to confirm that you have read and understood the terms of use. (Veuillez cliquer sur Accepter pour confirmer que vous avez lu et compris les conditions d’utilisation.)

---
 
### <a name="pass-through-authentication-supports-legacy-protocols-and-applications"></a>L’authentification directe prend en charge les applications et les protocoles hérités

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** Authentifications (connexions)  
**Fonctionnalité de produit :** Authentification utilisateur
 
L’authentification directe prend en charge les applications et les protocoles hérités. Les limitations suivantes sont maintenant entièrement prises en charge :

- L’utilisateur se connecte aux applications clientes Office héritées, Office 2010 et Office 2013 sans exiger une authentification moderne.

- Accédez aux informations de disponibilité et de partage de calendrier dans des environnements hybrides Exchange sur Office 2010 uniquement.

- L’utilisateur se connecte à des applications clientes Skype Entreprise, sans exiger une authentification moderne.

- L'utilisateur se connecte à PowerShell version 1.0.

- Le programme d’inscription des appareils Apple (Apple DEP) à l’aide de l’Assistant de configuration iOS. 

---
 
### <a name="converged-security-info-management-for-self-service-password-reset-and-multi-factor-authentication"></a>Informations de sécurité convergées pour la réinitialisation de mot de passe en libre-service et l’authentification multifacteur

**Type :** Nouvelle fonctionnalité  
**Catégorie de service :** SSPR  
**Fonctionnalité de produit :** Authentification utilisateur

Cette nouvelle fonctionnalité permet aux utilisateurs de gérer leurs informations de sécurité (par exemple, numéro de téléphone, adresse de messagerie, application mobile, etc) pour la réinitialisation de mot de passe libre-service (SSPR) et l’authentification multifacteur (MFA) dans une seule expérience. Les utilisateurs ne devront plus inscrire les mêmes informations de sécurité pour SSPR et MFA dans deux expériences différentes. Cette nouvelle expérience s’applique également aux utilisateurs qui dispose de SSPR ou MFA.

Si une organisation ne respecte pas l’inscription MFA ou SSPR, les utilisateurs peuvent inscrire leurs informations de sécurité via le portail **Mes applications**. À partir de là, les utilisateurs peuvent inscrire des méthodes activées pour MFA ou SSPR. 

Il s’agit d’une inscription à une version préliminaire publique. Les administrateurs peuvent activer la nouvelle expérience (le cas échéant) pour un groupe sélectionné d’utilisateurs ou de tous les utilisateurs d’un client.

---
 
### <a name="use-the-microsoft-authenticator-app-to-verify-your-identity-when-you-reset-your-password"></a>Utilisez l’application Microsoft Authenticator pour vérifier votre identité lorsque vous réinitialisez votre mot de passe

**Type :** Fonctionnalité modifiée  
**Catégorie de service :** SSPR  
**Fonctionnalité de produit :** Authentification utilisateur

Cette fonctionnalité permet aux non administrateurs de vérifier leur identité lors de la réinitialisation d’un mot de passe à l’aide d’une notification ou d’un code à partir de Microsoft Authenticator (ou toute autre application authentificatrice). Une fois que les administrateurs ont activé cette méthode de réinitialisation de mot de passe en libre-service, les utilisateurs qui ont inscrit une application mobile par le biais d’aka.ms/mfasetup ou d’aka.ms/setupsecurityinfo peuvent utiliser leur application mobile comme méthode de vérification lorsqu’ils réinitialisent leur mot de passe.

Les notifications d’application mobile peuvent uniquement être activées dans le cadre d’une stratégie qui nécessite deux méthodes pour réinitialiser votre mot de passe.

---
