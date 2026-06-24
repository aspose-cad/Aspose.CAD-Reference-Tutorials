---
date: 2026-03-24
description: Apprenez à convertir DGN en PNG et à enregistrer CAD en JPEG avec Aspose.CAD
  pour .NET – un guide rapide pour la conversion de CAD en image.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment convertir DGN en PNG avec Aspose.CAD pour .NET
url: /fr/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DGN en PNG avec Aspose.CAD pour .NET

Dans le développement .NET moderne, **convert dgn to png** est une exigence courante lorsque vous devez afficher des dessins CAD sur le web ou les intégrer dans des rapports. Aspose.CAD pour .NET rend cette conversion simple, vous permettant de transformer un fichier DGN en une image raster de haute qualité avec seulement quelques lignes de code. Dans ce guide, nous parcourrons l’ensemble du processus, de la configuration du projet à l’enregistrement du fichier PNG (ou JPEG) final.

## Réponses rapides
- **Puis-je convertir DGN en PNG avec Aspose.CAD ?** Oui – il suffit de configurer les options de rasterisation et de choisir la sortie PNG ou JPEG.  
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence valide d’Aspose.CAD est requise pour les déploiements non‑essai.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Quels formats d’image sont disponibles ?** PNG, JPEG, BMP, GIF, TIFF, et plus encore.  
- **La gestion des exceptions est‑elle nécessaire ?** Absolument – encapsulez la conversion dans un try/catch pour gérer les problèmes d’accès aux fichiers.

## Qu’est‑ce que « convert dgn to png » ?
Convertir un fichier DGN (MicroStation) en PNG signifie rasteriser les données vectorielles CAD en une image basée sur des pixels. Cela est utile pour la génération de prévisualisations, l’insertion de dessins dans des e‑mails HTML ou la création de miniatures pour les systèmes de gestion de documents.

## Pourquoi utiliser Aspose.CAD pour la conversion CAD en image ?
- **Aucune dépendance externe** – fonctionne entièrement en code géré.  
- **Haute fidélité** – préserve les épaisseurs de ligne, les calques et les couleurs.  
- **Sortie flexible** – passez de PNG à JPEG, BMP, etc., en modifiant une seule option.  
- **Performance optimisée** – la rasterisation est rapide même pour les dessins volumineux.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Aspose.CAD pour .NET** installé dans votre projet. Vous pouvez le télécharger depuis le [site web](https://reference.aspose.com/cad/net/).  
- Un fichier DGN d’exemple (par ex., `Nikon_D90_Camera.dgn`) placé dans un répertoire connu.

## Importer les espaces de noms

Commencez par ajouter les instructions `using` requises afin de pouvoir accéder aux classes Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Étape 1 : Charger le fichier DGN

Chargez le DGN source dans un objet `CadImage`. Cet objet représente le dessin CAD en mémoire et servira de source pour la rasterisation.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Étape 2 : Définir les options de rasterisation

Configurez la façon dont le dessin CAD doit être rasterisé. Vous pouvez contrôler la taille de l’image, l’échelle et la couleur d’arrière‑plan ici.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Étape 3 : Choisir le format de sortie (PNG ou JPEG)

Bien que le tutoriel se concentre sur le PNG, vous pouvez également **enregistrer cad en jpeg**. Créez l’objet d’options d’image approprié et associez‑y les paramètres de rasterisation.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Astuce :** Pour générer un fichier PNG, remplacez `new JpegOptions()` par `new PngOptions()`.

## Étape 4 : Enregistrer l’image raster

Enfin, appelez `Save` sur l’instance `CadImage`, en fournissant le nom de fichier souhaité et l’objet d’options que vous avez configuré.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Si vous avez basculé vers `PngOptions`, le fichier sera enregistré sous le nom `ExportDGNToRasterImage_out.png`.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Image de sortie vide** | `NoScaling` mal configuré ou mise en page non sélectionnée | Définissez `AutomaticLayoutsScaling = true` ou spécifiez la mise en page désirée. |
| **Manque de mémoire pour les gros fichiers** | Chargement d’un DGN volumineux sans diffusion | Utilisez `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Version DGN non prise en charge** | Versions anciennes de MicroStation | Assurez‑vous d’utiliser la dernière version d’Aspose.CAD qui supporte les formats hérités. |

## Questions fréquentes

**Q : Puis‑je exporter des fichiers DGN vers des formats autres que JPEG ?**  
**R :** Oui, Aspose.CAD pour .NET prend en charge PNG, BMP, GIF, TIFF, et plus encore – il suffit d’échanger la classe d’options (par ex., `new PngOptions()`).

**Q : Comment dois‑je gérer les exceptions pendant la conversion ?**  
**R :** Encapsulez le code de conversion dans un bloc `try/catch` et consignez `Aspose.CAD.CadException` pour obtenir des informations détaillées sur l’erreur.

**Q : Existe‑t‑il une version d’essai disponible pour Aspose.CAD pour .NET ?**  
**R :** Oui, vous pouvez explorer le produit avec une version d’essai gratuite. Consultez [ici](https://releases.aspose.com/) pour plus d’informations.

**Q : Où puis‑je obtenir de l’aide ou discuter des problèmes liés à Aspose.CAD pour .NET ?**  
**R :** Rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

**Q : Comment obtenir une licence temporaire pour Aspose.CAD pour .NET ?**  
**R :** Visitez [ce lien](https://purchase.aspose.com/temporary-license/) pour acquérir une licence temporaire adaptée à vos besoins de développement.

## Conclusion

Vous avez maintenant appris comment **convertir dgn en png** (ou JPEG) en utilisant Aspose.CAD pour .NET. En ajustant les options de rasterisation et en changeant la classe d’options d’image, vous pouvez adapter la sortie à n’importe quel besoin de projet. N’hésitez pas à expérimenter avec différentes tailles de page, réglages DPI et formats de fichier pour obtenir l’image raster parfaite pour votre application.

---

**Dernière mise à jour :** 2026-03-24  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}