---
title: Vue d’ensemble d’Azure Cost Management | Microsoft Docs
description: Azure Cost Management est une solution de gestion des coûts qui aide non seulement à superviser et à maîtriser les dépenses Azure, mais aussi à optimiser l’utilisation des ressources.
services: cost-management
keywords: ''
author: bandersmsft
ms.author: banders
ms.date: 02/05/2018
ms.topic: overview
ms.service: cost-management
manager: benshy
ms.custom: ''
ms.openlocfilehash: e526d7fac3c66c5eaf9686db3c9f9f9506d6fc6b
ms.sourcegitcommit: 415742227ba5c3b089f7909aa16e0d8d5418f7fd
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2019
ms.locfileid: "55768655"
---
# <a name="what-is-azure-cost-management"></a>Qu’est-ce que la gestion des coûts Azure ?

La gestion des coûts est le processus qui vous permet de prévoir et de maîtriser les coûts de votre entreprise avec efficacité. Les tâches de gestion des coûts sont normalement effectuées par les équipes de finance, d’administration et d’application. Azure Cost Management aide les organisations à planifier en gardant le coût à l’esprit. Il permet aussi d’analyser efficacement les coûts et de prendre des mesures pour optimiser les dépenses cloud. Pour découvrir plus en détail comment une organisation doit approcher la gestion des coûts, consultez l’article [Bonnes pratiques pour Azure Cost Management](cost-mgt-best-practices.md).

Bien que liées, la facturation diffère de la gestion des coûts. La facturation est le processus qui vous permet de facturer des biens ou des services aux clients et de gérer les relations commerciales.  Les équipes d’approvisionnement et de finance s’occupent généralement des tâches de facturation.

Cost Management révèle les modèles de coût et d’utilisation de l’organisation avec une analytique avancée. Dans Cost Management, les rapports affichent le coût, l’utilisation et l’instance réservée d’Azure ainsi que l’utilisation d’Azure Hybrid Benefit. Ensemble, les rapports indiquent vos coûts d’utilisation internes et externes ainsi que les frais de la Place de marché Azure. Les autre frais comme les achats de réservation, le support et les taxes n’apparaissent pas encore dans les rapports. Ils vous aident à comprendre vos dépenses et votre utilisation des ressources, et à trouver des anomalies dans les dépenses. Des analyses prédictives sont aussi disponibles. Cost Management utilise des groupes d’administration, des budgets et des recommandations Azure pour montrer avec clarté comment vos dépenses sont organisées et comment vous pourriez réduire les coûts.

Vous pouvez utiliser le portail Azure ou différentes API pour automatiser l’exportation visant à intégrer les données de coût à des processus et systèmes externes. Vous avez aussi à disposition une exportation automatisée des données de facturation ainsi que des rapports planifiés.

## <a name="plan-and-control-expenses"></a>Planifier et maîtriser les dépenses

Cost Management vous aide à planifier et à contrôler vos coûts de différentes façons : Analyse des coûts, budgets, suggestions et exportation des données de gestion des coûts.

Utilisez l’analyse du coût pour explorer et analyser les coûts de votre organisation. Vous pouvez voir les coûts agrégés par l’organisation afin de comprendre où les coûts ont augmenté et d’identifier les tendances de dépenses. Vous pouvez aussi voir les coûts cumulés au fil du temps pour évaluer des tendances mensuelles, trimestrielles ou même annuelles par rapport à un budget.

Les budgets vous aident à planifier et à suivre la comptabilité de votre organisation. Ils empêchent de dépasser les plafonds ou les limites de coût. Les budgets peuvent aussi vous permettre d’informer les autres de leurs dépenses pour gérer les coûts de manière proactive. Vous pouvez aussi voir la progression des dépenses.

Les recommandations vous montrent comment optimiser et améliorer votre efficacité en identifiant les ressources inactives et sous-utilisées. Elles peuvent aussi indiquer les options de ressource les moins chères. Si vous agissez sur des recommandations, vous changez la façon dont vous utilisez vos ressources pour économiser de l’argent. Pour agir, consultez d’abord les recommandations d’optimisation des coûts pour voir les inefficacités d’utilisation potentielles. Ensuite, agissez sur une recommandation pour modifier votre utilisation des ressources Azure et bénéficier d’une option plus rentable. Vérifiez ensuite que l’action que vous prenez change votre situation en mieux.

Si vous utilisez des systèmes externes pour accéder ou consulter les données de gestion des coûts, vous pouvez facilement exporter les données à partir d’Azure. Vous pouvez également définir une exportation planifiée quotidienne au format CSV et stocker les fichiers de données dans le stockage Azure. Ensuite, vous pouvez accéder aux données à partir de votre système externe.

## <a name="consider-cloudyn"></a>Envisager Cloudyn

[Cloudyn](overview.md) est un service Azure lié à Cost Management. Avec Cloudyn, vous pouvez suivre l’utilisation du cloud et les dépenses pour vos ressources Azure. Il prend également en charge d’autres fournisseurs cloud, notamment AWS et Google. Les rapports du tableau de bord vous aident à comprendre la répartition des coûts, de même que la rétrofacturation et la facturation interne. Actuellement, Cost Management ne prend pas en charge la rétrofacturation/facturation interne ni d’autres fournisseurs de services cloud. Par contre, Cloudyn est une option qui les _prend_ en charge. Actuellement, Cost Management prend uniquement en charge les comptes EA Azure. Il ne prend pas en charge les comptes individuels ou de paiement à l’utilisation ni les comptes de fournisseur de services cloud Microsoft, alors que Cloudyn oui. Si vous avez l’un de ces comptes, vous pouvez utiliser Cloudyn pour vous permettre de gérer vos coûts.

## <a name="additional-azure-tools"></a>Autres outils Azure

Azure dispose d’autres outils qui ne font pas partie de l’ensemble des fonctionnalités Azure Cost Management. Toutefois, ils jouent un rôle important dans le processus de gestion des coûts. Pour en savoir plus sur ces outils, consultez les liens suivants.

- [Calculatrice de prix Azure](https://azure.microsoft.com/pricing/calculator/) - Utilisez cet outil pour estimer vos coûts cloud à l’avance.
- [Azure Migrate](../migrate/migrate-overview.md) - Évaluez la charge actuelle de votre centre de données pour savoir ce dont vous avez besoin pour une solution de remplacement Azure.
- [Azure Advisor](../advisor/advisor-overview.md) - Identifiez les machines virtuelles inutilisées et recevez des recommandations sur les achats d’instance réservée Azure.
- [Azure Hybrid Benefit](https://azure.microsoft.com/pricing/hybrid-benefit/) - Utilisez vos licences Windows Server ou SQL Server locales actuelles pour les machines virtuelles dans Azure afin d’économiser.


## <a name="next-steps"></a>Étapes suivantes

Maintenant que vous êtes familiarisé avec Cost Management, l’étape suivante consiste à commencer à utiliser le service.

- Commencez à utiliser Azure Cost Management pour [analyser les coûts](quick-acm-cost-analysis.md).
- Vous pouvez également en savoir plus sur les [bonnes pratiques pour Azure Cost Management](cost-mgt-best-practices.md).
