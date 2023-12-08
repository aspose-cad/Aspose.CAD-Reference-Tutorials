---
title: Exportation de fichiers IGES au format PDF - Guide Aspose.CAD
linktitle: Exportation de fichiers IGES au format PDF
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Découvrez comment exporter sans effort des fichiers IGES au format PDF à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une manipulation précise des fichiers CAO.
type: docs
weight: 11
url: /fr/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
---
## Introduction

Dans le monde dynamique de la conception assistée par ordinateur (CAO), la nécessité de convertir les fichiers IGES au format PDF est une exigence courante. Aspose.CAD for .NET fournit une solution puissante pour cette tâche, offrant flexibilité et précision dans la gestion des fichiers CAO. Dans ce didacticiel, nous vous guiderons tout au long du processus d'exportation de fichiers IGES au format PDF à l'aide d'Aspose.CAD pour .NET. Allons-y !

## Conditions préalables

Avant de commencer, assurez-vous que les conditions préalables suivantes sont remplies :

1.  Bibliothèque Aspose.CAD pour .NET : assurez-vous que la bibliothèque Aspose.CAD pour .NET est intégrée à votre projet. Vous pouvez le télécharger depuis[ici](https://releases.aspose.com/cad/net/).

2. Environnement de développement : configurez un environnement de développement .NET, tel que Visual Studio, avec les configurations nécessaires.

Maintenant que les prérequis sont triés, passons à l’importation des espaces de noms requis.

## Importer des espaces de noms

Dans votre code, incluez les espaces de noms suivants :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

Ces espaces de noms fournissent des classes essentielles pour travailler avec des images CAO et des options de rastérisation.

## Étape 1 : Configurez votre projet

Avant de plonger dans le code, créez un nouveau projet ou ouvrez-en un existant dans votre environnement de développement .NET préféré.

## Étape 2 : ajouter une référence Aspose.CAD

Référencez la bibliothèque Aspose.CAD dans votre projet. Vous pouvez le faire en ajoutant le fichier DLL Aspose.CAD téléchargé.

## Étape 3 : initialiser le chemin

Définissez le chemin d'accès à votre répertoire de documents où se trouve le fichier IGES :

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

## Étape 4 : Charger l'image CAO

 Utilisez Aspose.CAD`Image.Load` méthode pour charger le fichier IGES :

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Votre code va ici
}
```

## Étape 5 : configurer les options de rastérisation

Définissez les options de rastérisation pour personnaliser la sortie PDF :

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

## Étape 6 : Enregistrer au format PDF

Enregistrez l'image CAO sous forme de fichier PDF avec les options spécifiées :

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

Avec ces six étapes simples, vous avez réussi à exporter un fichier IGES au format PDF à l'aide d'Aspose.CAD pour .NET.

## Conclusion

Dans ce didacticiel, nous avons exploré un moyen transparent de convertir des fichiers IGES en PDF à l'aide d'Aspose.CAD pour .NET. Le guide étape par étape garantit un processus fluide et efficace, vous permettant de gérer les fichiers CAO avec précision.


## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour .NET dans une application Web ?

A1 : Oui, Aspose.CAD pour .NET convient aux applications de bureau et Web, offrant des solutions polyvalentes pour la manipulation de fichiers CAO.

### Q2 : Où puis-je trouver de la documentation supplémentaire pour Aspose.CAD ?

 A2 : Explorez la documentation complète[ici](https://reference.aspose.com/cad/net/) pour des informations détaillées sur Aspose.CAD pour .NET.

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, vous pouvez accéder à un essai gratuit[ici](https://releases.aspose.com/) pour découvrir les capacités d'Aspose.CAD pour .NET.

### Q4 : Comment puis-je obtenir une licence temporaire ?

 A4 : Pour les licences temporaires, visitez[ce lien](https://purchase.aspose.com/temporary-license/) pour obtenir les informations de licence requises.

### Q5 : Besoin d'aide ou avez des questions ?

A5 : Rejoignez la communauté Aspose.CAD sur le[forum d'entraide](https://forum.aspose.com/c/cad/19) pour une aide et des discussions rapides.