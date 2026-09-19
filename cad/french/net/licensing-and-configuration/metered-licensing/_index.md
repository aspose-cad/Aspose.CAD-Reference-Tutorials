---
date: 2026-09-19
description: Apprenez comment mettre en œuvre la licence metered Aspose CAD dans .NET
  pour surveiller efficacement l'utilisation des ressources des applications .NET.
  Suivez notre guide étape par étape.
keywords:
- aspose cad metered licensing
- monitor resource usage .net
- aspose cad licensing
lastmod: 2026-09-19
linktitle: Metered Licensing
og_description: Apprenez comment mettre en œuvre la licence metered Aspose CAD dans
  .NET pour surveiller efficacement l'utilisation des ressources des applications
  .NET. Suivez notre guide étape par étape.
og_image_alt: Guide to Aspose CAD metered licensing for .NET developers
og_title: Comment utiliser la licence metered Aspose CAD dans .NET
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  headline: How to use Aspose CAD metered licensing in .NET
  type: TechArticle
- description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  name: How to use Aspose CAD metered licensing in .NET
  steps:
  - name: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
    text: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
  - name: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
    text: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
  type: HowTo
- questions:
  - answer: Yes, the free trial version available from the [free trial version](https://releases.aspose.com/)
      supports metered licensing.
    question: Can I use metered licensing with a free trial?
  - answer: Monitoring before and after each major operation gives the most accurate
      insight, but you can also poll at regular intervals for long‑running services.
    question: How often should I check consumption quantities?
  - answer: Yes, the same public/private key pair can be reused across multiple projects
      and environments.
    question: Are metered keys reusable?
  - answer: The library will throw a licensing exception. You can either purchase
      additional credits or contact support via the [Aspose.CAD support](https://forum.aspose.com/c/cad/19)
      forum.
    question: What happens if I exceed my metered limit?
  - answer: Absolutely – explore [temporary licensing options](https://purchase.aspose.com/temporary-license/)
      for limited‑duration needs.
    question: Can I temporarily license Aspose.CAD for a short‑term project?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- metered licensing
- .net resource monitoring
title: Comment utiliser la licence metered Aspose CAD dans .NET
url: /fr/net/licensing-and-configuration/metered-licensing/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Licence à consommation Aspose CAD pour .NET

## Introduction

La licence à consommation Aspose CAD vous permet de contrôler le nombre d'appels d'API CAD/BIM consommés par votre application .NET, vous offrant une facturation précise et une visibilité sur l'utilisation. En intégrant ce modèle de licence, vous pouvez **surveiller l'utilisation des ressources .NET** des applications sans coder en dur des limites, ce qui rend la mise à l'échelle et la gestion des coûts simples. Le guide suivant vous accompagne à chaque étape, de l'importation des espaces de noms à la lecture des données de consommation avant et après le traitement.

## Réponses rapides
- **Qu'est-ce que la licence à consommation ?** Un modèle basé sur l'usage où chaque appel d'API consomme un crédit prédéfini.
- **Ai-je besoin d'une licence d'essai ?** Oui – l'essai gratuit fonctionne avec les clés à consommation.
- **Comment puis-je voir la consommation ?** Appelez `License.GetConsumptionQuantity()` avant et après vos opérations.
- **Est‑elle thread‑safe ?** Oui, le moteur de licence est conçu pour les charges de travail .NET concurrentes.
- **Puis-je réutiliser la même clé ?** Absolument – la même paire publique/privée peut être partagée entre plusieurs projets.

## Qu'est-ce que la licence à consommation Aspose CAD ?

La licence à consommation Aspose CAD est un schéma de licence basé sur l'usage qui suit chaque appel d'API effectué par la bibliothèque Aspose.CAD pour .NET. Elle permet aux développeurs de ne payer que pour les ressources réellement consommées, au lieu d'acheter une licence perpétuelle.

## Pourquoi utiliser la licence à consommation avec Aspose CAD ?

La licence à consommation vous offre un contrôle précis des coûts en facturant uniquement l'utilisation réelle des API. Elle élimine le besoin d'achats de licences à l'avance et s'adapte automatiquement à la charge de travail, ce qui la rend idéale pour le traitement intermittent ou basé sur le cloud où l'utilisation varie.

## Prérequis

1. **Aspose.CAD installé** – téléchargez le dernier package depuis le [site web Aspose.CAD](https://releases.aspose.com/cad/net/).  
2. **Clés publiques et privées** – obtenez‑les sur la [page d'achat Aspose.CAD](https://purchase.aspose.com/buy).  
3. **Connaissances de base en .NET** – le guide suppose que vous êtes à l'aise avec les projets C# ciblant .NET 6 ou supérieur.

## Importer les espaces de noms

Ajoutez les directives `using` requises en haut de votre fichier C# afin que le compilateur puisse localiser les classes Aspose.CAD.

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.License;
```

L'espace de noms `License` contient les classes nécessaires à la licence à consommation.

## Comment définir la clé à consommation ?

`SetMeteredKey` enregistre vos clés publiques et privées de licence à consommation auprès du moteur Aspose.CAD. Appelez cette méthode une fois lors du démarrage de l'application, en transmettant les clés que vous avez reçues d'Aspose. Cela garantit que tous les appels d'API ultérieurs sont suivis par rapport à votre compte à consommation.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Comment obtenir la quantité de consommation avant l'appel d'API ?

`GetConsumptionQuantity` renvoie le nombre total de crédits consommés par la bibliothèque jusqu'au point d'appel. Capturez cette valeur avant d'effectuer toute opération CAD afin d'établir une référence. En la comparant à la valeur après le traitement, vous pouvez déterminer l'utilisation exacte de crédits d'une tâche spécifique.

```csharp
//ExStart:MeteredLicensing
// Access the setMeteredKey property and pass public and private keys as parameters
Aspose.CAD.Metered.SetMeteredKey("PublicKey", "PrivateKey");
```

## Comment traiter les données CAD avec Aspose.CAD ?

`CadImage` représente un fichier CAD chargé et fournit des méthodes de rendu ou de conversion. Après avoir défini la clé à consommation, chargez votre fichier CAD dans une instance `CadImage`. Vous pouvez alors rendre en formats raster, convertir vers d'autres types CAD, ou extraire les métadonnées, tout cela étant comptabilisé dans votre quota à consommation.

```csharp
// Get metered data amount before calling API
decimal amountbefore = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed Before: " + amountbefore.ToString());
```

## Comment obtenir la quantité de consommation après l'appel d'API ?

`GetConsumptionQuantity` peut être appelé à nouveau après le traitement pour récupérer le total de crédits mis à jour. Soustrayez la référence précédemment enregistrée afin de calculer le nombre de crédits consommés par l'opération récente. Cette information vous aide à surveiller les schémas d'utilisation et à optimiser votre code pour réduire les coûts.

```csharp
// Do processing
//Aspose.CAD.FileFormats.Cad.CadImage image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.load("BlockRefDgn.dwg");
```

## Problèmes courants et dépannage

- **Erreur « licence non définie » :** Assurez‑vous que `SetMeteredKey` est appelé avant toute utilisation de l'API Aspose.CAD.  
- **Consommation anormalement élevée :** Vérifiez que vous ne chargez pas involontairement de gros lots de fichiers dans une boucle ; chaque chargement compte comme un appel distinct.  
- **Problèmes de thread‑safety :** Le moteur de licence est thread‑safe, mais évitez d'appeler `SetMeteredKey` plusieurs fois simultanément.

## Questions fréquemment posées

**Q : Puis‑je utiliser la licence à consommation avec un essai gratuit ?**  
R : Oui, la version d'essai gratuite disponible depuis le [site d'essai gratuit](https://releases.aspose.com/) prend en charge la licence à consommation.

**Q : À quelle fréquence devrais‑je vérifier les quantités de consommation ?**  
R : Surveiller avant et après chaque opération majeure fournit l'information la plus précise, mais vous pouvez également interroger à intervalles réguliers pour les services de longue durée.

**Q : Les clés à consommation sont‑elles réutilisables ?**  
R : Oui, la même paire de clés publique/privée peut être réutilisée sur plusieurs projets et environnements.

**Q : Que se passe‑t‑il si je dépasse ma limite à consommation ?**  
R : La bibliothèque lèvera une exception de licence. Vous pouvez soit acheter des crédits supplémentaires, soit contacter le support via le forum [Aspose.CAD support](https://forum.aspose.com/c/cad/19).

**Q : Puis‑je obtenir une licence temporaire d'Aspose.CAD pour un projet à court terme ?**  
R : Absolument – explorez les [options de licence temporaire](https://purchase.aspose.com/temporary-license/) pour des besoins de durée limitée.

---

**Dernière mise à jour :** 2026-09-19  
**Testé avec :** Aspose.CAD 24.11 for .NET  
**Auteur :** Aspose  






```csharp
// Get metered data amount after calling API
decimal amountafter = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed After: " + amountafter.ToString());
//ExEnd:MeteredLicensing 
```

## Tutoriels associés

- [Appliquer une licence dans Aspose.CAD pour .NET – Tutoriel étape par étape](/cad/net/)
- [Comment convertir et exporter des dessins CAD en PDF avec Aspose.CAD pour .NET – Tutoriel](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Convertir CAD en PNG dans Aspose.CAD pour .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}