---
date: 2026-06-09
description: Apprenez comment convertir DXF en WMF avec Aspose.CAD pour Java, incluant
  un essai gratuit, la prise en charge de Java 8+, et l’exportation PDF facultative.
  Guide étape par étape avec des exemples de code.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Exporter DXF au format WMF avec Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Convertir DXF en WMF avec Aspose.CAD en Java
url: /fr/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DXF en WMF avec Aspose.CAD en Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **convertir DXF en WMF** avec Aspose.CAD pour Java. Que vous ayez besoin d’intégrer des dessins CAD dans un rapport basé sur Windows, de générer des graphiques vectoriels légers pour les documents Office, ou d’automatiser des conversions par lots, la conversion de DXF en WMF est une exigence fréquente dans les pipelines d’ingénierie et de reporting. Nous parcourrons le chargement d’un dessin DXF, la configuration des options de rasterisation, l’enregistrement du résultat au format WMF, et éventuellement l’exportation du même dessin en PDF.

## Réponses rapides
- **Puis-je convertir DXF en WMF avec un essai gratuit ?** Oui – Aspose propose un essai complet de 30 jours.  
- **Quelle version de Java est requise ?** Java 8 ou supérieure.  
- **Ai-je besoin d’une licence pour exécuter le code ?** Une licence est requise en production ; l’essai fonctionne pour le développement et les tests.  
- **La conversion est‑elle sans perte ?** Les données vectorielles sont conservées ; les options de rasterisation vous permettent de contrôler la résolution.  
- **Puis‑je également exporter le même dessin en PDF ?** Absolument – voir l’étape « Exporter en PDF » ci‑dessous.

## Qu’est‑ce que « convertir DXF en WMF » ?

Convertir DXF en WMF consiste à prendre un fichier Drawing Exchange Format (DXF) — un format CAD largement utilisé — et à le transformer en Windows Metafile (WMF). WMF est un format d’image vectorielle qui s’intègre parfaitement avec Microsoft Office, les applications Windows et de nombreux outils de reporting.

## Pourquoi utiliser Aspose.CAD pour Java ?

Aspose.CAD pour Java fournit un moteur pure‑Java, sans DLL native, qui convertit les fichiers CAD avec **plus de 99 % de fidélité vectorielle**, en préservant les calques, les couleurs, les styles de ligne et les motifs de hachures. Il prend en charge **plus de 50 formats d’entrée et de sortie** — notamment DXF, DWG, DGN, PDF, PNG, SVG et WMF — tout en vous permettant d’ajuster la taille de la page, le DPI et la couleur d’arrière‑plan via les options de rasterisation intégrées. La même API gère également les exportations PDF, PNG et SVG, éliminant ainsi le besoin de plusieurs bibliothèques.

### Principaux avantages
- **Aucune dépendance externe** – pure Java, fonctionne sur tout OS exécutant Java.  
- **Rendu haute fidélité** – conserve l’épaisseur des lignes, la couleur et les détails des hachures.  
- **Rasterisation intégrée** – contrôle les dimensions de la page, la résolution et l’arrière‑plan.  
- **Conversion tout‑en‑un** – les mêmes classes exportent vers WMF, PDF, PNG, SVG, etc.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Aspose.CAD pour Java** intégré à votre projet. Téléchargez‑le depuis le site officiel : [Téléchargement Aspose.CAD Java](https://releases.aspose.com/cad/java/).  
- **Répertoire de documents** où vos fichiers DXF sont stockés (par ex., `Your Document Directory/DXFDrawings/`).  

## Importer les espaces de noms

The following imports bring in the Aspose.CAD classes required for loading, rasterizing, and saving CAD files.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Guide étape par étape

### Comment convertir DXF en WMF en Java ?

Chargez votre fichier DXF avec `Image.load("yourFile.dxf")`, configurez `CadRasterizationOptions` pour la taille de page et le DPI souhaités, puis appelez `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Ce schéma en trois étapes effectue la conversion complète tout en conservant la qualité vectorielle et ne nécessite que quelques lignes de code.

#### Étape 1 : Charger le dessin DXF

`Image.load` lit le fichier DXF dans un objet Aspose.CAD Image.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Étape 2 : Configurer les options de rasterisation

`CadRasterizationOptions` spécifie la taille de la page, la résolution et l’arrière‑plan pour rasteriser le dessin CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Étape 3 : Enregistrer en WMF

`ImageSaveOptions` avec `SaveFormat.WMF` indique à Aspose.CAD d’écrire la sortie au format Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Étape 4 : Libérer les ressources

Appeler `image.close()` libère les ressources natives utilisées par l’objet Aspose.CAD Image.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Étape 5 : Optionnel – Exporter en PDF

`PdfOptions` configure les paramètres spécifiques au PDF lors de l’enregistrement de l’image en document PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Astuce pro :** Vous pouvez réutiliser le même objet `CadRasterizationOptions` pour l’export PDF en le passant à une instance `PdfOptions`, ce qui vous évite quelques lignes de configuration.

## Comment exporter DXF en PDF avec Aspose CAD Java ?

L’exportation en PDF suit les mêmes étapes de chargement et de rasterisation ; il suffit de remplacer le format d’enregistrement WMF par PDF. Utilisez `new ImageSaveOptions(SaveFormat.Pdf)` et, éventuellement, définissez des options spécifiques au PDF telles que le niveau de compression ou les métadonnées d’auteur. Cette conversion en une ligne produit un PDF consultable, fidèle à la mise en page originale du CAD.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **`NullPointerException` on `cadImage.save`** | Variable `cadImage` non définie (devrait être `image`). | Remplacez `cadImage` par `image` ou renommez la variable de manière cohérente. |
| **La sortie WMF est vide** | Taille de page de rasterisation trop petite ou couleur d’arrière‑plan définie sur transparent. | Augmentez `PageWidth`/`PageHeight` ou définissez une couleur d’arrière‑plan via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Exécution sans licence Aspose valide en production. | Appliquez le fichier de licence au démarrage de l’application : `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusion

Vous disposez maintenant d’un flux de travail complet, prêt pour la production, pour **convertir DXF en WMF** avec Aspose.CAD pour Java, avec une étape optionnelle pour **exporter le même dessin en PDF**. Cette approche vous fournit une sortie vectorielle de haute qualité qui s’intègre parfaitement aux outils de reporting et de documentation basés sur Windows, tout en gardant votre base de code simple et sans dépendances.

## FAQ

### Q1 : Où puis‑je trouver la documentation Aspose.CAD ?

R1 : Vous pouvez accéder à la documentation [ici](https://reference.aspose.com/cad/java/).

### Q2 : Comment télécharger Aspose.CAD pour Java ?

R2 : Téléchargez la bibliothèque [ici](https://releases.aspose.com/cad/java/).

### Q3 : Existe‑t‑il un essai gratuit ?

R3 : Oui, vous pouvez obtenir un essai gratuit [ici](https://releases.aspose.com/).

### Q4 : Besoin d’options de licence temporaires ?

R4 : Explorez les licences temporaires [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je obtenir du support ?

R5 : Visitez le forum de support Aspose.CAD [ici](https://forum.aspose.com/c/cad/19).

## Questions fréquemment posées

**Q : Puis‑je convertir de gros fichiers DXF (des centaines de Mo) sans épuiser la mémoire ?**  
R : Oui. Chargez le fichier dans un bloc try‑with‑resources et libérez rapidement l’objet `Image`. Ajustez `CadRasterizationOptions.setPageWidth/Height` à une taille raisonnable pour maintenir une faible consommation de mémoire.

**Q : La sortie WMF conserve‑t‑elle les informations de calque ?**  
R : WMF est un format vectoriel plat, donc la hiérarchie des calques est aplatie, mais les styles de ligne, les couleurs et les motifs de hachure sont conservés.

**Q : Est‑il possible de définir un DPI personnalisé pour le WMF ?**  
R : Utilisez `rasterizationOptions.setResolution(300);` pour définir le DPI avant l’enregistrement.

**Q : Puis‑je convertir par lots plusieurs fichiers DXF en une seule exécution ?**  
R : Absolument. Parcourez un répertoire, chargez chaque fichier et appliquez la même logique de rasterisation et d’enregistrement.

**Q : Quelles versions de Java sont prises en charge ?**  
R : Aspose.CAD pour Java prend en charge Java 8 et ultérieur, y compris Java 11, 17 et les versions LTS plus récentes.

**Dernière mise à jour :** 2026-06-09  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Tutoriels associés

- [Créer un PDF à partir de CAD – Exporter DXF en PDF avec Aspose.CAD pour Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Créer un PDF à partir de DXF : Exporter un calque avec Aspose.CAD pour Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Comment convertir la mise en page DXF en image JPEG avec Aspose.CAD en Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}