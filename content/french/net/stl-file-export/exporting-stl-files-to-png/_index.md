---
title: Conversion STL en PNG facilitée avec Aspose.CAD pour .NET
linktitle: Exportation de fichiers STL vers PNG
second_title: Aspose.CAD .NET - Format de fichier CAO et BIM
description: Convertissez sans effort des fichiers STL en PNG à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une intégration transparente. Télécharger maintenant!
type: docs
weight: 10
url: /fr/net/stl-file-export/exporting-stl-files-to-png/
---
## Introduction
Dans le monde dynamique de la conception assistée par ordinateur (CAO), une conversion efficace des fichiers est cruciale. Aspose.CAD pour .NET est une boîte à outils puissante qui simplifie le processus d'exportation de fichiers STL au format PNG, offrant aux développeurs la flexibilité et les fonctionnalités dont ils ont besoin. Ce didacticiel vous guidera étape par étape tout au long du processus, garantissant une transition en douceur du STL au PNG à l'aide d'Aspose.CAD.
## Conditions préalables
Avant de plonger dans le didacticiel, assurez-vous d'avoir les éléments suivants en place :
1.  Aspose.CAD pour .NET : téléchargez et installez la bibliothèque Aspose.CAD. Tu peux le trouver[ici](https://releases.aspose.com/cad/net/).
2. Environnement de développement : configurez votre environnement de développement .NET préféré.
3. Fichier STL : préparez un fichier STL pour la conversion. Pour ce didacticiel, nous utiliserons un exemple de fichier nommé "galeon.stl".
## Importer des espaces de noms
Pour lancer le processus, importez les espaces de noms nécessaires dans votre application .NET. Cela garantit que vous avez accès aux classes et méthodes requises pour la conversion STL en PNG.
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
## Étape 1 : Définir le répertoire et le chemin du fichier source
```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "galeon.stl";
```
Assurez-vous de remplacer « Votre répertoire de documents » par le chemin du répertoire réel où se trouve votre fichier STL.
## Étape 2 : Charger l'image CAO
```csharp
using (var cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // D'autres étapes seront exécutées dans ce bloc
}
```
Cette étape charge le fichier STL sous forme d'image CAO, vous permettant de le manipuler et de l'exporter.
## Étape 3 : Définir les options de rastérisation
```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 100;
rasterizationOptions.PageHeight = 100;
```
Ajustez la largeur et la hauteur de la page en fonction de vos préférences et exigences. Ces paramètres déterminent les dimensions du PNG exporté.
## Étape 4 : Configurer les options PNG
```csharp
PngOptions pngOptions = new PngOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
```
Créez des options PNG en incorporant les paramètres de rastérisation définis à l'étape précédente.
## Étape 5 : Enregistrez le fichier PNG
```csharp
string outPath = sourceFilePath + ".png";
cadImage.Save(outPath, pngOptions);
```
Spécifiez le chemin de sortie du fichier PNG et enregistrez l'image CAO au format PNG à l'aide des options fournies.
Répétez ces étapes si nécessaire pour votre cas d'utilisation spécifique et vous réussirez à exporter des fichiers STL au format PNG avec Aspose.CAD pour .NET.
## Conclusion
Aspose.CAD pour .NET simplifie la tâche complexe de conversion de fichiers STL en PNG, offrant ainsi aux développeurs une boîte à outils fiable. En suivant ce guide étape par étape, vous pouvez intégrer de manière transparente cette fonctionnalité dans vos applications.
## FAQ
### Q : Puis-je personnaliser les dimensions du PNG exporté ?
 Absolument! À l'étape 3, ajustez le`PageWidth` et`PageHeight` valeurs pour répondre à vos exigences spécifiques.
### Q : Une licence temporaire est-elle disponible à des fins de test ?
 Oui, vous pouvez obtenir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/) pour les tests et l'évaluation.
### Q : Où puis-je trouver une assistance supplémentaire ou des discussions communautaires ?
 Visiter le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour du soutien et des discussions collaboratives.
### Q : Existe-t-il d'autres formats de fichiers pris en charge pour la conversion ?
 Oui, Aspose.CAD prend en charge divers formats de CAO au-delà de STL. Se référer au[Documentation](https://reference.aspose.com/cad/net/) pour une liste complète.
### Q : Puis-je traiter par lots plusieurs fichiers STL ?
Certainement! Implémentez une boucle basée sur les étapes fournies pour traiter par lots plusieurs fichiers STL.