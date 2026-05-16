---
date: 2026-03-26
description: Apprenez à créer des PDF à partir de fichiers CAD et à convertir des
  DXF en PDF en utilisant Aspose.CAD pour .NET. Personnalisez les options de stylo
  pour des visuels époustouflants en PDF, PNG, BMP et plus encore.
linktitle: Pen Support in Export
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Créer un PDF à partir de CAD avec des options de stylo personnalisées – Aspose.CAD
  pour .NET
url: /fr/net/cad-features-and-support/pen-support-in-export/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Améliorez l'Export CAD avec des Options de Stylo Personnalisées dans Aspose.CAD pour .NET

## Introduction

Si vous devez **créer un PDF à partir de fichiers CAD** rapidement et avec un contrôle visuel complet, Aspose.CAD pour .NET vous offre exactement cela. En tirant parti de la fonction de prise en charge des stylos de la bibliothèque, vous pouvez définir les caps de début et de fin, les jointures de lignes et d’autres attributs de dessin, produisant des PDF qui ont exactement l’apparence souhaitée. Ce tutoriel vous guide à travers l’ensemble du processus — du chargement d’un fichier DXF à l’exportation d’un PDF soigné — tout en montrant comment les mêmes paramètres peuvent être réutilisés lorsque vous **exportez un CAD vers PNG** ou **rasterisez des données d’image CAD** pour d’autres formats.

## Réponses rapides
- **Que signifie « créer un PDF à partir de CAD » ?** Cela convertit les dessins CAD vectoriels (par ex., DXF) en un document PDF tout en préservant la géométrie et le style.  
- **Quels formats prennent en charge les options de stylo ?** PDF, PNG, BMP, GIF, JPEG2000, JPEG, PSD, TIFF et WMF.  
- **Ai‑je besoin d’une licence pour le développement ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Puis‑je modifier les caps de ligne pour d’autres formats ?** Oui — les options de stylo s’appliquent à toute cible de rasterisation prise en charge par Aspose.CAD.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu’est‑ce que la prise en charge des stylos dans l’export CAD ?

La prise en charge des stylos vous permet de personnaliser la façon dont les lignes sont dessinées lorsqu’un dessin CAD est rasterisé ou vector‑rasterisé. Vous pouvez définir des propriétés telles que `StartCap`, `EndCap`, `LineJoin` et `DashStyle`. Ces réglages influencent l’apparence finale de l’image ou du PDF exporté, vous offrant un contrôle granulaire sur la qualité visuelle.

## Pourquoi utiliser des options de stylo personnalisées lorsque vous **créez un PDF à partir de CAD** ?

- **Cohérence de la marque** – harmonisez les styles de ligne d’entreprise dans tous les documents.  
- **Lisibilité améliorée** – des caps et des jointures plus épais rendent les dessins techniques plus clairs à l’écran et à l’impression.  
- **Flexibilité multi‑format** – la même configuration de stylo fonctionne pour PNG, BMP et autres formats raster, vous faisant gagner du temps.

## Prérequis

- Aspose.CAD pour .NET installé (téléchargez depuis la [page de version](https://releases.aspose.com/cad/net/)).  
- Connaissances de base du DXF (Drawing Exchange Format).  
- Familiarité avec la programmation C#.

## Importer les espaces de noms

Pour commencer, assurez‑vous d’importer les espaces de noms nécessaires dans votre projet C# :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
using System.Drawing.Drawing2D;
```

## Étape 1 : Configurer le répertoire de votre document

Définissez le dossier contenant le fichier CAD source :

```csharp
string MyDir = "Your Document Directory";
```

## Étape 2 : Charger l’image CAD

Chargez le dessin CAD (par exemple, un fichier DXF) dans un objet `Aspose.CAD.Image` :

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
CadImage cadImage = (CadImage)Image.Load(sourceFilePath);
```

## Étape 3 : Configurer les options de rasterisation

Créez les objets d’options de rasterisation et de PDF. Ces objets vous permettent de contrôler la façon dont les données CAD sont transformées en image raster ou en page PDF :

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
PdfOptions pdfOptions = new PdfOptions();
```

## Étape 4 : Personnaliser les options de stylo

C’est ici que vous **personnalisez le stylo** qui trace les lignes. Vous pouvez définir les caps de début et de fin sur `Flat`, `Round`, `Square`, etc. C’est le cœur du « comment exporter CAD » avec le style visuel dont vous avez besoin :

```csharp
rasterizationOptions.PenOptions = new PenOptions
{
   StartCap = LineCap.Flat,
   EndCap = LineCap.Flat
};
```

*Astuce :* Expérimentez avec `LineCap.Round` pour des extrémités de ligne plus lisses lorsque vous **exportez un CAD vers PNG**.

## Étape 5 : Appliquer les options de rasterisation vectorielle

Attachez les paramètres de rasterisation aux options PDF afin que le processus d’exportation sache quelle configuration de stylo utiliser :

```csharp
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Étape 6 : Enregistrer le PDF exporté

Enfin, générez le fichier PDF. Cette étape **crée un PDF à partir de CAD** avec les paramètres de stylo personnalisés appliqués :

```csharp
cadImage.Save(MyDir + "9LHATT-A56_generated.pdf", pdfOptions);
```

Vous pouvez remplacer `PdfOptions` par `PngOptions`, `BmpOptions`, etc., pour **exporter un CAD vers PNG** ou d’autres formats raster tout en conservant la même configuration de stylo.

## Cas d’utilisation courants

- **Documentation technique** – intégrez des styles de ligne précis dans les PDF d’ingénierie.  
- **Génération de rapports automatisée** – traitez en lot de nombreux fichiers DXF en PDF avec un profil de stylo unique.  
- **Services web** – exposez une API qui convertit les fichiers DXF téléchargés en PDF à la volée, en garantissant une stylisation cohérente.

## Dépannage & pièges courants

| Problème | Raison | Solution |
|----------|--------|----------|
| Les lignes exportées semblent plus épaisses que prévu | Le DPI est plus élevé que prévu | Définissez `rasterizationOptions.PageWidth` / `PageHeight` ou ajustez `Resolution`. |
| Les options de stylo sont ignorées pour la sortie PNG | Utilisation de `ImageOptions` au lieu de `VectorRasterizationOptions` | Assurez‑vous d’assigner `rasterizationOptions.PenOptions` avant l’enregistrement. |
| Le fichier PDF est vide | Le chemin du DXF source est incorrect ou le fichier est corrompu | Vérifiez `sourceFilePath` et confirmez que le DXF se charge sans exception. |

## FAQ

### Q1 : Puis‑je utiliser ces options de stylo pour d’autres formats d’image que le PDF ?

R1 : Oui, les options de stylo peuvent être appliquées à divers formats d’image tels que PNG, BMP, GIF, JPEG, etc.

### Q2 : Où puis‑je trouver une documentation supplémentaire pour Aspose.CAD pour .NET ?

R2 : Consultez la [documentation](https://reference.aspose.com/cad/net/) pour des informations complètes et des exemples.

### Q3 : Existe‑t‑il une version d’essai gratuite pour Aspose.CAD pour .NET ?

R3 : Oui, vous pouvez accéder à une version d’essai gratuite [ici](https://releases.aspose.com/).

### Q4 : Comment obtenir des licences temporaires pour Aspose.CAD pour .NET ?

R4 : Visitez la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour les options de licence temporaire.

### Q5 : Où puis‑je obtenir du support communautaire pour Aspose.CAD pour .NET ?

R5 : Rejoignez la communauté sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

## Questions fréquentes supplémentaires

**Q : Comment **convertir DXF en PDF** programmatique ?**  
R : Chargez le DXF avec `Image.Load`, configurez `CadRasterizationOptions` et `PdfOptions`, puis appelez `Save` comme illustré dans les étapes précédentes.

**Q : Puis‑je rasteriser une image CAD sans créer de PDF ?**  
R : Oui — utilisez `PngOptions`, `BmpOptions` ou toute autre classe de format raster et assignez les mêmes `rasterizationOptions` pour obtenir une rasterisation de haute qualité.

**Q : Est‑il possible de modifier la largeur de ligne lors de la création d’un PDF à partir de CAD ?**  
R : Ajustez `rasterizationOptions.CustomLineWidth` ou modifiez la propriété `PenOptions.Width` avant l’enregistrement.

**Q : La bibliothèque prend‑elle en charge les fichiers DXF 3D ?**  
R : Aspose.CAD se concentre sur les données vectorielles 2D ; les entités 3D sont ignorées lors de la rasterisation.

**Q : Quelle version d’Aspose.CAD est requise pour ces fonctionnalités ?**  
R : La prise en charge des stylos est disponible depuis la version 20.9 ; toute version ultérieure fonctionnera.

---

**Dernière mise à jour :** 2026-03-26  
**Testé avec :** Aspose.CAD pour .NET 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}