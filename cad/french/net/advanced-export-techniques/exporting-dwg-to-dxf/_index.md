---
title: Exporter un DWG au format DXF en C# - Tutoriel Aspose.CAD
linktitle: Exportation de DWG au format DXF en C#
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Débloquez la manipulation de fichiers CAO en C# avec Aspose.CAD. Apprenez à exporter DWG vers DXF sans effort. Suivez notre guide étape par étape pour une intégration transparente.
type: docs
weight: 10
url: /fr/net/advanced-export-techniques/exporting-dwg-to-dxf/
---
## Introduction

Si vous êtes un développeur .NET à la recherche d'une solution puissante pour manipuler des fichiers CAO, Aspose.CAD est votre outil incontournable. Dans ce didacticiel étape par étape, nous vous guiderons tout au long du processus d'exportation d'un fichier DWG au format DXF à l'aide de C# avec Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1.  Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD à partir de[ce lien](https://releases.aspose.com/cad/net/).

2. Environnement de développement : configurez un environnement de développement C#, tel que Visual Studio.

3. Exemple de fichier DWG : préparez un exemple de fichier DWG que vous souhaitez exporter. Pour ce didacticiel, nous utiliserons un fichier nommé "Line.dwg" dans le répertoire "Votre répertoire de documents".

## Importer des espaces de noms

Dans votre projet C#, incluez les espaces de noms nécessaires pour travailler avec Aspose.CAD :

```csharp
using Aspose.CAD.FileFormats.Cad;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Étape 1 : Charger le fichier DWG

Commencez par charger le fichier DWG dans votre application C#. Voici un extrait de code pour y parvenir :

```csharp
string MyDir = "Your Document Directory";
string inputFile = MyDir + "Line.dwg";
using (var cadImage = (CadImage)Image.Load(inputFile))
{
    //Votre code pour les étapes ultérieures sera ici
}
```

## Étape 2 : Enregistrer au format DXF

Une fois le fichier DWG chargé, l'étape suivante consiste à l'enregistrer en tant que fichier DXF. Ajoutez le code suivant dans le bloc using précédent :

```csharp
string outFile = MyDir + "Line_19.2.dxf";
cadImage.Save(outFile);
```

## Conclusion

Toutes nos félicitations! Vous avez exporté avec succès un fichier DWG au format DXF à l'aide d'Aspose.CAD en C#. Ce processus simple mais puissant ouvre un monde de possibilités pour la manipulation de fichiers CAO dans vos applications.

## FAQ

### Q1 : Aspose.CAD est-il compatible avec les derniers formats de fichiers CAO ?

A1 : Oui, Aspose.CAD est régulièrement mis à jour pour garantir la compatibilité avec les derniers formats de fichiers CAO.

### Q2 : Puis-je utiliser Aspose.CAD dans mes projets commerciaux ?

 A2 : Absolument ! Aspose.CAD est livré avec des options de licence pour un usage personnel et commercial. Visite[ce lien](https://purchase.aspose.com/buy) pour plus de détails.

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, vous pouvez explorer Aspose.CAD avec un essai gratuit. Visite[ce lien](https://releases.aspose.com/) pour commencer.

### Q4 : Où puis-je trouver une documentation détaillée pour Aspose.CAD ?

 A4 : Reportez-vous à la documentation sur[ce lien](https://reference.aspose.com/cad/net/) pour des conseils complets.

### Q5 : Besoin d'aide ou avez des questions spécifiques ?

 A5 : Visitez le forum de la communauté Aspose.CAD[ici](https://forum.aspose.com/c/cad/19)pour l’assistance d’experts et le soutien de la communauté.