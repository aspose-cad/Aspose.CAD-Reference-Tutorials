---
title: Exporter des objets OLE à partir de fichiers DWG - Tutoriel Aspose.CAD
linktitle: Exportation d'objets OLE à partir de fichiers DWG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Explorez le guide étape par étape sur l'exportation d'objets OLE à partir de fichiers DWG à l'aide d'Aspose.CAD pour .NET. Améliorez vos compétences en manipulation de fichiers CAO sans effort.
type: docs
weight: 12
url: /fr/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
---
## Introduction

Cherchez-vous à extraire facilement des objets OLE à partir de fichiers DWG ? Aspose.CAD for .NET est là pour rationaliser le processus pour vous. Dans ce didacticiel, nous vous guiderons étape par étape dans l'exportation d'objets OLE, afin que vous puissiez tirer le meilleur parti de cette puissante bibliothèque .NET. 

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

-  Aspose.CAD pour la bibliothèque .NET : assurez-vous que la bibliothèque est installée. Vous pouvez le télécharger depuis le[Page de téléchargement d'Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).

-  Répertoire de documents : configurez un répertoire dans lequel vos fichiers DWG sont stockés. Remplacer`"Your Document Directory"` dans l'extrait de code fourni avec le chemin réel.

## Importer des espaces de noms

Dans votre projet .NET, vous devrez importer les espaces de noms nécessaires pour tirer parti des fonctionnalités d'Aspose.CAD. Utilisez l'extrait de code suivant :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Définir le répertoire des documents

```csharp
string MyDir = "Your Document Directory";
```

 Remplacer`"Your Document Directory"` avec le chemin où se trouvent vos fichiers DWG.

## Étape 2 : Spécifier les fichiers DWG

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Répertoriez les fichiers DWG que vous souhaitez traiter dans le tableau.

## Étape 3 : configurer les options d'exportation

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Personnalisez les options d'exportation en fonction de vos besoins. Dans cet exemple, nous configurons l'exportation PNG avec une mise en page spécifiée.

## Étape 4 : Parcourir les fichiers et exporter

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Parcourez les fichiers DWG spécifiés, chargez chacun d'eux et enregistrez le fichier PNG exporté avec les options définies.

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès des objets OLE à partir de fichiers DWG à l'aide d'Aspose.CAD pour .NET. Cette puissante bibliothèque simplifie les tâches complexes, offrant efficacité et flexibilité dans la manipulation des fichiers CAO.

## FAQ

### Q1 : Aspose.CAD pour .NET convient-il aux fichiers CAO juniors et seniors ?

A1 : Oui, Aspose.CAD pour .NET est polyvalent et peut gérer une large gamme de fichiers CAO, y compris les variantes junior et senior.

### Q2 : Puis-je personnaliser les options d’exportation pour différentes mises en page ?

A2 : Absolument ! Comme le montre le didacticiel, vous pouvez personnaliser les options d'exportation, y compris les mises en page, pour répondre à vos besoins spécifiques.

### Q3 : Où puis-je trouver une documentation détaillée pour Aspose.CAD pour .NET ?

 A3 : Explorez le[Documentation Aspose.CAD pour .NET](https://reference.aspose.com/cad/net/) pour des informations détaillées et des exemples.

### Q4 : Existe-t-il un essai gratuit ?

 A4 : Oui, vous pouvez découvrir les capacités d'Aspose.CAD pour .NET avec un essai gratuit. Visite[ce lien](https://releases.aspose.com/) pour commencer.

### Q5 : Comment puis-je obtenir de l'aide ou me connecter avec la communauté ?

 A5 : Pour obtenir du soutien et l'engagement de la communauté, visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19).