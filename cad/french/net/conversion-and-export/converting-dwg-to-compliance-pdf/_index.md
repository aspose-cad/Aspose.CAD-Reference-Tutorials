---
title: Conversion d'un fichier DWG en PDF conforme - Tutoriel Aspose.CAD
linktitle: Conversion de DWG en PDF de conformité
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez DWG en PDF conforme avec Aspose.CAD pour .NET. Suivez notre tutoriel pour des conseils étape par étape.
weight: 13
url: /fr/net/conversion-and-export/converting-dwg-to-compliance-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversion d'un fichier DWG en PDF conforme - Tutoriel Aspose.CAD

## Introduction

Bienvenue dans notre didacticiel étape par étape sur la conversion de fichiers DWG en PDF de conformité à l'aide d'Aspose.CAD pour .NET. Aspose.CAD est une puissante API .NET qui permet aux développeurs de travailler sans effort avec les formats de fichiers CAO. Dans ce didacticiel, nous vous guiderons tout au long du processus de conversion d'un fichier DWG en PDF de conformité avec des exemples et des explications détaillés.

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD est intégrée à votre projet .NET. Vous pouvez le télécharger[ici](https://releases.aspose.com/cad/net/).

- Environnement de développement : installez un environnement de développement .NET fonctionnel et assurez-vous qu'il est correctement configuré.

- Exemple de fichier DWG : téléchargez un exemple de fichier DWG que vous souhaitez convertir au format PDF de conformité.

## Importer des espaces de noms

Dans votre projet .NET, importez les espaces de noms nécessaires pour utiliser les fonctionnalités Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Décomposons maintenant le processus de conversion d'un fichier DWG en PDF de conformité en plusieurs étapes.

## Étape 1 : Charger le fichier DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

Aspose.CAD.Image cadImage = Aspose.CAD.Image.Load(sourceFilePath);
```

## Étape 2 : définir les options de rastérisation

 Créer une instance de`CadRasterizationOptions` et configurez ses propriétés, telles que la couleur d'arrière-plan, la largeur de la page et la hauteur de la page.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions
{
    BackgroundColor = Aspose.CAD.Color.White,
    PageWidth = 1600,
    PageHeight = 1600
};
```

## Étape 3 : Créer des options PDF

 Créer une instance de`PdfOptions` et définissez les options de rastérisation vectorielle.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions,
    CorePdfOptions = new PdfDocumentOptions { Compliance = PdfCompliance.PdfA1a }
};
```

## Étape 4 : Enregistrer au format PDF (conformité A1a)

Enregistrez l'image CAO au format PDF de conformité avec la conformité A1a.

```csharp
cadImage.Save(MyDir + "PDFA1_A.pdf", pdfOptions);
```

## Étape 5 : Enregistrer au format PDF (conformité A1b)

Modifiez le type de conformité en A1b et enregistrez l'image CAO au format PDF de conformité.

```csharp
pdfOptions.CorePdfOptions.Compliance = PdfCompliance.PdfA1b;
cadImage.Save(MyDir + "PDFA1_B.pdf", pdfOptions);
```

## Conclusion

Toutes nos félicitations! Vous avez converti avec succès un fichier DWG en PDF de conformité à l'aide d'Aspose.CAD pour .NET. Ce didacticiel fournit un guide complet aux développeurs souhaitant intégrer des fonctionnalités de conversion CAO dans leurs applications.

## FAQ

### Q1 : Puis-je convertir d'autres formats CAO en PDF de conformité à l'aide d'Aspose.CAD ?

A1 : Oui, Aspose.CAD prend en charge divers formats CAO, permettant la conversion en PDF de conformité.

### Q2 : Aspose.CAD est-il compatible avec .NET Core ?

A2 : Oui, Aspose.CAD est compatible avec .NET Framework et .NET Core.

### Q3 : Existe-t-il des options de licence pour Aspose.CAD ?

 A3 : Oui, vous pouvez explorer les options de licence[ici](https://purchase.aspose.com/buy).

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez bénéficier d'un essai gratuit[ici](https://releases.aspose.com/).

### Q5 : Où puis-je obtenir de l'aide pour Aspose.CAD ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour toute question relative au support.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
