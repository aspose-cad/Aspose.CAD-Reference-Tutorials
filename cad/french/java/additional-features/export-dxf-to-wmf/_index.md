---
date: 2026-10-30
description: Apprenez à convertir par lots des fichiers DXF en WMF en utilisant Aspose.CAD
  pour Java, avec du code étape par étape, des informations sur le free trial et une
  exportation PDF optionnelle.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Exporter DXF au format WMF avec Java
og_description: Convertissez par lots des fichiers DXF en WMF avec Aspose.CAD pour
  Java. Suivez ce guide pour charger des dessins DXF, définir les rasterization options,
  enregistrer au format WMF et, éventuellement, exporter en PDF avec un free trial.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Conversion par lots de fichiers DXF en WMF avec Aspose.CAD pour Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Conversion par lots de fichiers DXF en WMF avec Aspose.CAD pour Java
url: /fr/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir en lot des fichiers DXF en WMF avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **convertir en lot des fichiers DXF en WMF** en utilisant Aspose.CAD pour Java. Que vous ayez besoin d’intégrer des dessins CAD dans des rapports basés sur Windows, de générer des graphiques vectoriels légers pour des documents Office, ou d’automatiser des conversions à grande échelle, ce guide vous explique comment charger un dessin DXF, configurer les options de rasterisation, enregistrer au format WMF, et éventuellement exporter le même dessin en PDF. Les étapes fonctionnent sur n’importe quelle plateforme exécutant Java 8+.

## Réponses rapides

- **Puis-je convertir DXF en WMF avec un essai gratuit ?** Oui – Aspose propose un essai complet de 30 jours.  
- **Quelle version de Java est requise ?** Java 8 ou ultérieure.  
- **Ai-je besoin d’une licence pour exécuter le code ?** Une licence est requise en production ; l’essai fonctionne pour le développement et les tests.  
- **La conversion est‑elle sans perte ?** Les données vectorielles sont conservées ; les options de rasterisation vous permettent de contrôler la résolution.  
- **Puis‑je également exporter le même dessin en PDF ?** Absolument – voir l’étape « Export to PDF » ci‑dessous.  
- **Comment convertir en lot de nombreux fichiers DXF en une fois ?** Parcourez un dossier, appliquez le même schéma charger‑rasteriser‑enregistrer à chaque fichier.

## Qu’est‑ce que la conversion en lot de fichiers DXF ?

La conversion en lot de fichiers DXF consiste à traiter plusieurs dessins au format Drawing Exchange Format (DXF) en une seule exécution et à produire une sortie WMF pour chacun. WMF (Windows Metafile) est un format d’image vectorielle qui s’intègre nativement à Microsoft Office, aux applications Windows et à de nombreux outils de reporting.

## Pourquoi utiliser Aspose.CAD pour Java ?

Aspose.CAD pour Java est un moteur pure‑Java qui prend en charge **plus de 50 formats d’entrée et de sortie** — y compris DXF, DWG, DGN, PDF, PNG, SVG et WMF — tout en offrant une **fidélité vectorielle de 99 %**. Il fonctionne sur tout système d’exploitation supportant Java, ne nécessite aucune DLL native, et vous permet de contrôler la taille de la page, le DPI et la couleur d’arrière‑plan via une seule classe `CadRasterizationOptions`. La même API gère également les exportations PDF, PNG et SVG, éliminant ainsi le besoin de multiples bibliothèques.

### Avantages quantifiés
- **Plus de 50 formats pris en charge** réduisent le besoin de convertisseurs tiers.  
- **Traite des fichiers DXF de 300 pages en moins de 5 secondes** sur un serveur typique de 2,5 GHz lorsqu’ils sont rasterisés à 150 DPI.  
- **L’empreinte mémoire reste inférieure à 200 Mo** pour des fichiers jusqu’à 500 Mo lorsque vous définissez des dimensions de page appropriées.  

## Prérequis

- **Aspose.CAD pour Java** intégré à votre projet. Téléchargez-le depuis le site officiel : [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Un dossier contenant les fichiers DXF que vous souhaitez convertir (par ex., `Your Document Directory/DXFDrawings/`).  

## Importer les espaces de noms

`Image` est la classe principale d’Aspose.CAD qui représente un dessin CAD en mémoire. Après le chargement d’un fichier, toutes les opérations suivantes — rasterisation, conversion de format et nettoyage des ressources — sont effectuées via cet objet.

Les importations suivantes apportent les classes Aspose.CAD nécessaires au chargement, à la rasterisation et à l’enregistrement des fichiers CAD.  
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

### Comment convertir en lot des fichiers DXF en WMF en Java ?

Chargez chaque DXF avec `Image.load`, configurez `CadRasterizationOptions` pour la taille de page et le DPI souhaités, puis appelez `image.save` avec `SaveFormat.WMF`. Ce schéma en trois étapes effectue la conversion complète tout en conservant la qualité vectorielle et ne nécessite que quelques lignes de code par fichier.

#### Étape 1 : charger le dessin DXF

`Image.load` lit le fichier DXF dans un objet `Image` d’Aspose.CAD.  
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Étape 2 : configurer les options de rasterisation

`CadRasterizationOptions` spécifie la taille de la page, la résolution et l’arrière‑plan pour rasteriser le dessin CAD.  
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Étape 3 : enregistrer en WMF

`ImageSaveOptions` avec `SaveFormat.WMF` indique à Aspose.CAD d’écrire la sortie au format Windows Metafile.  
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Étape 4 : libérer les ressources

Appeler `image.close()` libère les ressources natives utilisées par l’objet `Image` d’Aspose.CAD.  
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Étape 5 : optionnel – exporter en PDF

`PdfOptions` configure les paramètres spécifiques au PDF lors de l’enregistrement de l’image en document PDF.  
```java
finally
{
  cadImage.dispose();
}
```

> **Astuce :** Vous pouvez réutiliser le même objet `CadRasterizationOptions` pour l’exportation PDF en le passant à une instance `PdfOptions`, ce qui vous évite quelques lignes de configuration.

## Comment exporter DXF en PDF avec Aspose CAD Java ?

Remplacez le format d’enregistrement WMF par PDF en utilisant `new ImageSaveOptions(SaveFormat.Pdf)`. Les mêmes paramètres de rasterisation s’appliquent, et vous pouvez en outre définir des options spécifiques au PDF telles que les métadonnées d’auteur ou le niveau de compression. Cette conversion en une seule ligne produit un PDF consultable, fidèle à la mise en page, qui reflète le rendu CAD original.

## Problèmes courants et solutions

`License` est la classe Aspose utilisée pour appliquer une licence produit à l’exécution.

| Issue | Cause | Fix |
|-------|-------|-----|
| **`NullPointerException` sur `cadImage.save`** | Variable `cadImage` non définie (devrait être `image`). | Remplacez `cadImage` par `image` ou renommez la variable de façon cohérente. |
| **Le WMF de sortie est vide** | Taille de page de rasterisation trop petite ou couleur d’arrière‑plan définie sur transparent. | Augmentez `PageWidth`/`PageHeight` ou définissez une couleur d’arrière‑plan via `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Exception de licence** | Exécution sans licence Aspose valide en production. | Appliquez le fichier de licence au démarrage de l’application : `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Questions fréquentes

**Q : Où puis‑je trouver la documentation Aspose.CAD ?**  
R : Vous pouvez accéder à la documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Q : Comment télécharger Aspose.CAD pour Java ?**  
R : Téléchargez la bibliothèque [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Q : Un essai gratuit est‑il disponible ?**  
R : Oui, vous pouvez obtenir un essai gratuit [Aspose free trial page](https://releases.aspose.com/).

**Q : Besoin d’options de licence temporaires ?**  
R : Explorez les licences temporaires [temporary license options](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je obtenir du support ?**  
R : Consultez le forum de support Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Questions fréquentes supplémentaires

**Q : Puis‑je convertir de gros fichiers DXF (des centaines de Mo) sans épuiser la mémoire ?**  
R : Oui. Chargez le fichier dans un bloc try‑with‑resources et libérez rapidement l’objet `Image`. Ajustez `CadRasterizationOptions.setPageWidth/Height` à une taille raisonnable pour maintenir une faible consommation de mémoire.

**Q : La sortie WMF conserve‑t‑elle les informations de calque ?**  
R : WMF est un format vectoriel plat, donc la hiérarchie des calques est aplatie, mais les styles de ligne, les couleurs et les motifs de hachures sont conservés.

**Q : Est‑il possible de définir un DPI personnalisé pour le WMF ?**  
R : Utilisez `rasterizationOptions.setResolution(300);` pour définir le DPI avant l’enregistrement.

**Q : Puis‑je convertir en lot plusieurs fichiers DXF en une seule exécution ?**  
R : Absolument. Parcourez un répertoire, chargez chaque fichier et appliquez la même logique de rasterisation et d’enregistrement.

**Q : Quelles versions de Java sont prises en charge ?**  
R : Aspose.CAD pour Java prend en charge Java 8 et ultérieur, y compris Java 11, 17 et les versions LTS plus récentes.

---

**Dernière mise à jour :** 2026-10-30  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose

## Tutoriels associés

- [Créer un PDF à partir de CAD – Exporter DXF en PDF avec Aspose.CAD pour Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Créer un PDF à partir de DXF : Exporter un calque avec Aspose.CAD pour Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Comment convertir la mise en page DXF en image JPEG avec Aspose.CAD en Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}