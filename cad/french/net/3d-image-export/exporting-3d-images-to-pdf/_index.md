---
date: 2026-07-04
description: Apprenez comment définir la taille de la page PDF et exporter un PDF
  à partir d'images CAD 3D en utilisant Aspose.CAD pour .NET – un guide étape par
  étape pour convertir DWG en PDF et enregistrer le CAD au format PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Exportation d'images 3D en PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Définir la taille de la page PDF – Exporter des images 3D en PDF avec Aspose.CAD
url: /fr/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportation d'images 3D en PDF - Tutoriel Aspose.CAD

## Introduction

Si vous devez **définir la taille de la page PDF** lors de la conversion d'un dessin CAD 3‑D en PDF, vous êtes au bon endroit. Ce tutoriel vous montre, étape par étape, comment charger un fichier CAD, configurer les options de rasterisation — y compris les dimensions de page personnalisées — et générer un PDF haute fidélité en utilisant Aspose.CAD pour .NET. À la fin, vous pourrez **exporter un PDF depuis le CAD**, **enregistrer le CAD en PDF**, et contrôler chaque détail de mise en page sans installer AutoCAD.

## Réponses rapides

- **Que signifie « export PDF from CAD » ?** Cela convertit un dessin CAD (DWG, DXF, DGN, etc.) en un PDF qui peut être ouvert sur n'importe quel appareil.  
- **Quelle bibliothèque effectue la conversion ?** Aspose.CAD for .NET fournit la rasterisation et l'exportation PDF sans dépendances externes.  
- **Ai-je besoin d'une licence ?** Une licence temporaire ou complète est requise pour la production ; un essai gratuit est disponible.  
- **Puis-je définir des dimensions de page personnalisées ?** Oui — utilisez `PageWidth` et `PageHeight` dans `RasterizationOptions`.  
- **La géométrie 3‑D sera-t-elle conservée ?** Les entités 3‑D sont rasterisées ; activez `TypeOfEntities.Entities3D` pour un support complet de la 3‑D.  

## Qu'est-ce que « export PDF » dans le contexte du CAD ?

Exporter un PDF depuis le CAD signifie prendre un dessin CAD (DWG, DXF, DGN, etc.) et le convertir en un fichier PDF pouvant contenir des graphiques vectoriels, des vues 3‑D rasterisées et des informations de mise en page précises, facilitant le partage avec toute personne ne disposant pas d'un logiciel CAD.

## Pourquoi utiliser Aspose.CAD pour exporter un PDF ?

Aspose.CAD vous permet de **définir la taille de la page PDF** et d'exporter des PDF entièrement en code .NET géré. Il prend en charge plus de 50 formats CAD, traite des fichiers jusqu'à 2 Go sans charger le document complet en mémoire, et préserve les épaisseurs de ligne, les couleurs et le rendu optionnel des entités 3‑D avec une résolution de rasterisation DPI pouvant atteindre 1200. La bibliothèque fonctionne sous Windows, Linux et macOS, de sorte que les PDF générés fonctionnent sur n'importe quelle plateforme.

## Prérequis

- **Aspose.CAD for .NET** installé. Téléchargez-le depuis la [page de téléchargement Aspose.CAD for .NET](https://releases.aspose.com/cad/net/).  
- Un dossier contenant les fichiers CAD que vous souhaitez convertir (par ex., `C:\CAD\`).  
- .NET 6.0 ou ultérieur (ou .NET Framework 4.7.2).  

## Importer les espaces de noms

Les instructions `using` importent les espaces de noms Aspose.CAD nécessaires pour travailler avec les options de rasterisation et de PDF.  

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Guide étape par étape

### Comment définir la taille de la page PDF lors de l'exportation d'un CAD en PDF ?

Chargez votre fichier CAD, configurez les dimensions de la page dans `RasterizationOptions`, attachez ces options à une instance `PdfOptions`, puis appelez `Save`. Ce flux en quatre étapes vous donne un contrôle total sur la taille et la qualité du résultat tout en conservant un code concis.

### Étape 1 : Charger l'image CAD

La classe `Image` représente un dessin CAD chargé en mémoire, prêt pour la rasterisation.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Étape 2 : Configurer les options de rasterisation (Enregistrer le CAD en PDF)

La classe `RasterizationOptions` définit comment les données CAD sont rasterisées, y compris la taille de la page, le DPI et si les entités 3‑D sont rendues.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Étape 3 : Définir les options PDF (Créer un PDF à partir du CAD)

La classe `PdfOptions` contient les paramètres du format de sortie et lie les options de rasterisation à la génération du PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Étape 4 : Enregistrer en PDF (Générer un PDF à partir du modèle 3D)

La méthode `Save` de l'objet `Image` écrit le contenu rasterisé dans le fichier PDF spécifié, produisant un document prêt à être partagé.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **Le PDF de sortie est vide** | Nom de mise en page incorrect ou mise en page `Model` manquante. | Vérifiez que `rasterizationOptions.Layouts` correspond à une mise en page présente dans le fichier CAD. |
| **Résolution faible** | Le DPI de rasterisation par défaut est faible. | Définissez `rasterizationOptions.Resolution = 300;` avant d'enregistrer. |
| **Entités 3‑D non affichées** | `TypeOfEntities` est commenté. | Décommentez `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **Exception de licence** | Utilisation d'un essai sans licence. | Appliquez une licence temporaire ou permanente via `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Questions fréquentes

**Q : Aspose.CAD est-il compatible avec tous les formats de fichiers CAD ?**  
A : Oui, Aspose.CAD prend en charge plus de 50 formats d'entrée et de sortie, y compris DWG, DXF, DGN, STL et IFC, garantissant une flexibilité pour tout projet.

**Q : Puis-je personnaliser les dimensions de la page lors de l'exportation en PDF ?**  
A : Absolument. Définissez `PageWidth` et `PageHeight` dans `RasterizationOptions` à n'importe quelle taille en points, pouces ou millimètres avant d'appeler `Save`.

**Q : Des licences temporaires sont-elles disponibles pour Aspose.CAD ?**  
A : Oui, vous pouvez obtenir des licences temporaires pour Aspose.CAD en visitant [Licence temporaire](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver un support supplémentaire ou des discussions communautaires ?**  
A : Rendez‑vous sur le [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) pour obtenir de l'aide d'experts et des conseils entre pairs.

**Q : Existe‑t‑il une version d'essai gratuite d'Aspose.CAD ?**  
A : Oui, vous pouvez explorer les fonctionnalités d'Aspose.CAD en accédant à l'[essai gratuit](https://releases.aspose.com/).

## Conclusion

Vous disposez maintenant d'une méthode complète, prête pour la production, pour **définir la taille de la page PDF** et **exporter un PDF depuis des images CAD 3D** en utilisant Aspose.CAD pour .NET. En ajustant les options de rasterisation, vous pouvez affiner la résolution, la mise en page et le rendu des entités 3‑D pour répondre à n'importe quelle exigence de documentation. Expérimentez différents réglages de DPI et dimensions de page pour obtenir le parfait équilibre entre la taille du fichier et la fidélité visuelle.

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exportation de mises en page spécifiques en PDF - Guide Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Exportation de DWG en PDF ou images raster - Guide Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Exportation de DGN en PDF avec Aspose.CAD pour .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Dernière mise à jour:** 2026-07-04  
**Testé avec:** Aspose.CAD 24.11 for .NET  
**Auteur:** Aspose