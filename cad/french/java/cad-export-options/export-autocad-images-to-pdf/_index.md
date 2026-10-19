---
date: 2026-10-19
description: Apprenez comment exporter des dessins AutoCAD vers PDF avec une taille
  de page PDF personnalisée en utilisant Aspose.CAD pour Java. Ce guide étape par
  étape couvre la conversion DWG en PDF, les options de rasterization et le licensing.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Exporter des images AutoCAD en PDF
og_description: Définissez une taille de page PDF personnalisée lors de l'exportation
  de dessins AutoCAD vers PDF en utilisant Aspose.CAD pour Java. Apprenez la conversion
  DWG en PDF, les paramètres de rasterization et le licensing en quelques minutes.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Définir une taille de page PDF personnalisée pour l'exportation AutoCAD
  avec Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Définir une taille de page PDF personnalisée pour l'exportation AutoCAD avec
  Aspose.CAD
url: /fr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter PDF AutoCAD - exporter des images AutoCAD en PDF avec Aspose.CAD pour Java

## Introduction

Si vous devez **convertir DWG en PDF** et contrôler les dimensions exactes du fichier de sortie, vous êtes au bon endroit. Ce tutoriel vous montre comment définir une **taille de page PDF personnalisée** lors de l'exportation d'images AutoCAD en PDF avec Aspose.CAD pour Java. À la fin du guide, vous saurez comment charger un DWG, configurer les options de rasterisation telles que le DPI et la largeur/hauteur de la page, appliquer une licence et générer un PDF prêt pour la production.

## Réponses rapides
- **Puis-je convertir DWG en PDF avec Java ?** Oui – Aspose.CAD for Java prend en charge nativement les formats DWG, DXF, DWF et de nombreux autres formats CAD.  
- **Ai-je besoin d'une licence pour une utilisation en production ?** Une licence complète Aspose.CAD supprime toutes les limites d'évaluation ; une licence temporaire est disponible pour les tests.  
- **Quelles versions de Java sont compatibles ?** La bibliothèque fonctionne avec Java 8 et toute version ultérieure du JDK.  
- **Comment modifier les dimensions de la page PDF ?** Définissez `pageWidth` et `pageHeight` sur `PdfOptions.getRasterizationOptions()` à la taille souhaitée.  
- **Le rendu 3D est‑il pris en charge ?** Oui – activez `TypeOfEntities.Entities3D` pour rasteriser les entités 3D.

## Qu'est-ce que l'exportation PDF AutoCAD ?
Exporter un PDF AutoCAD signifie convertir des dessins CAO basés sur des vecteurs (DWG, DXF, DWF, etc.) en un document PDF portable tout en conservant les calques, les épaisseurs de ligne et la géométrie 3D optionnelle. Cela vous permet de partager des conceptions avec des clients, d'archiver des dessins ou d'imprimer sans installer de logiciel CAO.

## Pourquoi utiliser Aspose.CAD pour Java pour convertir DWG en PDF ?
Aspose.CAD pour Java est idéal pour convertir DWG en PDF car il offre une prise en charge étendue des formats, fonctionne en Java pur sans dépendances natives, fournit une rasterisation haute résolution avec un contrôle complet du DPI et de la taille de la page, et inclut une licence flexible qui vous permet de commencer avec un essai et de passer à la production.

- **Couverture étendue des formats** – prend en charge plus de 50 formats d'entrée et de sortie, y compris DWG, DXF, DWF, DGN et PDF.  
- **Implémentation Java pure** – aucune DLL native ni dépendance externe, le déploiement est donc simple sur n'importe quelle plateforme.  
- **Rasterisation haute résolution** – vous pouvez spécifier le DPI, la taille de la page et la mise en page, vous offrant un contrôle complet sur la **taille de page PDF personnalisée** du résultat.  
- **Licence évolutive** – commencez avec un essai gratuit, puis passez à une **licence Aspose CAD** permanente.  

## Prérequis

- **Kit de développement Java** – JDK 8 ou plus récent installé sur votre machine.  
- **Aspose.CAD pour Java** – téléchargez le dernier JAR depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Répertoire de travail** – un dossier contenant les fichiers DWG source et qui recevra les PDF générés.

## Importer les espaces de noms

La classe `Image` est l'objet principal d'Aspose.CAD qui représente un dessin CAO en mémoire. Importez les packages requis avant de commencer à coder.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Passons maintenant en revue le code étape par étape.

## Comment définir une taille de page PDF personnalisée lors de l'exportation de DWG en PDF ?

Chargez votre DWG, définissez la largeur et la hauteur de page souhaitées, puis enregistrez le résultat au format PDF – c’est tout ce dont vous avez besoin pour créer un PDF avec une taille de page personnalisée. Les étapes suivantes illustrent la séquence exacte et le code minimal requis.

### Étape 1 : définir le chemin du répertoire des ressources

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Astuce :** Remplacez `"Your Document Directory"` par le chemin absolu du dossier que vous avez créé dans les prérequis.

### Étape 2 : charger l'image CAD

La classe `Image` charge le fichier CAD et vous donne accès au moteur de rasterisation d'Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Pourquoi c’est important :** Une fois le fichier CAD chargé, vous pouvez manipuler les options de rasterisation avant de le rendre en PDF.

### Étape 3 : définir les options de rasterisation

La classe `CadRasterizationOptions` spécifie comment le dessin CAD est rasterisé avant d'être enregistré en PDF. Ajustez `pageWidth` et `pageHeight` pour définir une **taille de page PDF personnalisée**. Vous pouvez également activer le rendu 3D en décommentant la ligne `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – mesurés en pixels ; modifiez ces valeurs pour correspondre à A4, Letter ou toute dimension personnalisée.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – rend les entités 3D lorsque nécessaire.  
- `setLayouts` – sélectionne la mise en page (Model, Layout1, etc.) à rasteriser.

### Étape 4 : configurer les options PDF

La classe `PdfOptions` contient les paramètres spécifiques au PDF et lie les options de rasterisation au fichier de sortie, garantissant que les dimensions de page personnalisées sont appliquées correctement.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : enregistrer le PDF

La méthode `save` écrit l'image rendue dans le fichier PDF spécifié.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Le fichier résultant, `Export3DImagestoPDF_out_.pdf`, est une représentation **save cad as pdf** de votre dessin AutoCAD original avec les dimensions de page exactes que vous avez spécifiées.

## Problèmes courants et solutions

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| PDF blanc en sortie | Options de rasterisation non définies ou mise en page incohérente | Vérifiez que `setLayouts` correspond au nom de la mise en page dans votre fichier CAD. |
| Image à basse résolution | `pageWidth`/`pageHeight` trop petits ou DPI faible | Augmentez les dimensions ou appelez `rasterizationOptions.setResolution(...)` avec un DPI plus élevé. |
| Exception de licence | Aucune licence valide appliquée | Appliquez une licence permanente Aspose.CAD ou utilisez une licence temporaire pour les tests. |

## Questions fréquentes

**Q : Puis-je utiliser Aspose.CAD pour Java avec d'autres formats de fichiers CAD ?**  
R : Oui, la bibliothèque prend en charge DWG, DXF, DWF, DGN et bien d'autres, vous offrant une flexibilité pour vos projets.

**Q : Comment obtenir une licence temporaire pour Aspose.CAD pour Java ?**  
R : Consultez la [page de licence temporaire](https://purchase.aspose.com/temporary-license/) pour demander une licence à durée limitée pour l'évaluation.

**Q : Existe-t-il des options de mise en page pour la rasterisation ?**  
R : Absolument. Utilisez `setLayouts("Model")` ou spécifiez d'autres noms de mise en page pour contrôler la vue à rendre.

**Q : Puis-je personnaliser la taille du fichier PDF de sortie ?**  
R : Oui – modifiez `pageWidth` et `pageHeight` dans les options de rasterisation selon les dimensions souhaitées.

**Q : Où puis-je obtenir de l'aide ou discuter des problèmes liés à Aspose.CAD pour Java ?**  
R : Le [forum dédié Aspose.CAD](https://forum.aspose.com/c/cad/19) propose un support communautaire et des réponses officielles de l'équipe Aspose.

## FAQ supplémentaire (format adapté à l'IA)

**Q : Aspose.CAD nécessite-t-il des bibliothèques natives sous Windows ou Linux ?**  
R : Non. Aspose.CAD pour Java est une bibliothèque pure Java, elle s'exécute sur n'importe quelle plateforme supportant le JDK sans DLL natives supplémentaires.

**Q : Quelle taille de fichier DWG la bibliothèque peut‑elle traiter ?**  
R : La bibliothèque peut gérer des dessins de plusieurs centaines de pages (jusqu'à 500 Mo) sans charger le fichier complet en mémoire, grâce à son architecture de streaming.

**Q : Est‑il possible de convertir en lot de nombreux fichiers DWG en PDF en une seule exécution ?**  
R : Oui. Parcourez un répertoire, chargez chaque fichier avec `Image.load()`, appliquez les mêmes options de rasterisation et appelez `save()` pour chaque PDF de sortie.

**Q : Quelle performance puis‑je attendre sur un serveur type ?**  
R : Convertir un DWG de 100 pages à 300 DPI sur un CPU standard de 2,5 GHz prend environ 12 secondes, selon les tests de référence d'Aspose.

**Q : La bibliothèque conserve‑t‑elle les informations de calque dans le PDF ?**  
R : Bien que la sortie soit rasterisée, l'apparence visuelle des calques, des épaisseurs de ligne et des couleurs est reproduite fidèlement.

---

**Dernière mise à jour :** 2026-10-19  
**Testé avec :** Aspose.CAD for Java 24.10  
**Auteur :** Aspose

## Tutoriels associés

- [Exporter DWG en PDF et activer le suivi avec Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Exporter DWG en PDF : mise en page spécifique avec Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exporter DWG en BMP et ajuster la taille CAD en utilisant le type d'unité avec Aspose.CAD pour Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}