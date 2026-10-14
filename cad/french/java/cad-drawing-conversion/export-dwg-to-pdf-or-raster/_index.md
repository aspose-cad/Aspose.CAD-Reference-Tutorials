---
date: 2026-10-14
description: Découvrez comment la bibliothèque Java CAD Aspose.CAD for Java peut exporter
  des fichiers DWG vers PDF ou images raster rapidement et avec précision.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Exporter DWG, PDF et images raster
og_description: Exportez rapidement des fichiers DWG en PDF avec Aspose.CAD for Java.
  Découvrez la conversion PDF haute qualité, les options raster et les licences dans
  ce guide étape par étape.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Exporter DWG, PDF et images raster à l'aide de la bibliothèque Java CAD
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Exporter DWG, PDF et images raster à l'aide de la bibliothèque Java CAD Aspose.CAD
url: /fr/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter des PDF DWG et des images raster en utilisant la bibliothèque Java CAD Aspose.CAD

## Introduction

Exporter des DWG en PDF est une exigence fréquente pour les ingénieurs, les architectes et toute personne qui doit partager des dessins CAO sans exposer le format de fichier natif. Avec **Aspose.CAD for Java**, vous pouvez **export dwg pdf** — ou des images raster — en quelques lignes de code Java, en conservant la fidélité vectorielle et la précision de la mise en page. Ce tutoriel vous guide à travers le chargement d'un fichier DWG, la configuration de la rasterisation et l'enregistrement du résultat sous forme de PDF ou d'image de haute qualité. Vous verrez également pourquoi Aspose.CAD est la bibliothèque Java CAD préférée pour une conversion fiable et multiplateforme.

Pour un guide ciblé uniquement sur la conversion PDF, consultez le [Tutoriel d'exportation DWG vers PDF](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Réponses rapides
- **Quel est le sujet de ce tutoriel ?** Exportation de fichiers DWG en PDF ou en images raster à l'aide d'Aspose.CAD for Java.  
- **Ai-je besoin d'une licence ?** Une licence temporaire gratuite est disponible pour l'évaluation ; une licence complète est requise pour la production.  
- **Quelle version de Java est prise en charge ?** Toute version d'exécution Java 8+ fonctionne avec la dernière API Java d'Aspose.CAD.  
- **Puis-je convertir DWG vers d'autres formats d'image ?** Oui – les mêmes options de rasterisation vous permettent de produire des PNG, JPEG, BMP, etc.  
- **Combien de temps prend la conversion ?** Typiquement moins d'une seconde pour les dessins standards ; les fichiers plus volumineux peuvent prendre quelques secondes.

## Pourquoi la bibliothèque Java CAD est-elle le meilleur choix pour la conversion DWG ?

Aspose.CAD for Java est le meilleur choix car il fournit une implémentation pure Java qui ne nécessite aucune DLL native, détecte automatiquement les unités métriques ou impériales, délivre une sortie raster jusqu'à 1200 DPI, et génère des PDF préservant les vecteurs sans dépendances externes. La bibliothèque propose également un modèle de licence flexible qui vous permet de commencer avec une licence temporaire et de passer à une utilisation en entreprise.

## Qu’est‑ce que « export dwg to pdf » ?

`Export dwg pdf` est le processus de conversion d'un fichier de dessin DWG natif en document PDF tout en préservant les données vectorielles, les calques et l'échelle. Cette conversion produit un fichier indépendant du dispositif qui peut être visualisé sur n'importe quelle plateforme sans besoin d'AutoCAD. Comme le PDF conserve les informations vectorielles, le texte reste recherchable et les graphiques restent nets à n'importe quel niveau de zoom, ce qui le rend idéal pour la documentation, la révision client et le stockage d'archives.

## Pourquoi utiliser Aspose.CAD Java pour cette conversion ?

Vous devriez utiliser Aspose.CAD Java car la bibliothèque gère la conversion d'unités, la rasterisation et l'intégration PDF en interne, éliminant le besoin d'outils tiers ou de pipelines en ligne de commande complexes. Son API est conçue pour les développeurs : un seul objet `Image` représente le dessin, et quelques objets de configuration vous permettent d'ajuster finement le DPI, la taille de page et la compression. Le résultat est une sortie cohérente et reproductible sur les environnements Windows, Linux et macOS.

## Prérequis

- Connaissances de base en programmation Java.  
- Bibliothèque Aspose.CAD for Java installée. Si vous ne l'avez pas encore téléchargée, obtenez‑la **[télécharger Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Un fichier DWG pour les tests – l'échantillon **Bottom_plate.dwg** est utilisé dans ce guide.  

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires pour lancer la conversion :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Guide étape par étape

### Étape 1 : Charger le fichier DWG

Tout d'abord, chargez votre dessin DWG à l'aide de la classe `Image`. Cela crée une représentation en mémoire avec laquelle Aspose.CAD peut travailler.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Étape 2 : Déterminer le type d'unité

Comprendre si le dessin utilise des unités métriques ou impériales est essentiel pour un bon dimensionnement. La méthode d'aide `IsMetric` (implémentation omise pour plus de concision) renvoie un indicateur booléen.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Étape 3 : Définir les options de rasterisation

La classe `CadRasterizationOptions` définit les paramètres de rasterisation tels que le DPI, la taille de page et la conversion d'unités. En fonction du système d'unités, configurez la taille de page, le redimensionnement et le type d'unité cible. Ces options déterminent la façon dont le DWG est rasterisé avant d'être encapsulé dans un PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Étape 4 : Configurer les options PDF (options PDF CAD)

La classe `PdfOptions` spécifie les paramètres spécifiques au PDF, y compris la compression et les métadonnées. Créez une instance `PdfOptions` et attachez les paramètres de rasterisation. Cela indique à Aspose.CAD comment intégrer le contenu rasterisé dans le PDF final.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Étape 5 : Enregistrer en PDF

La méthode `save` écrit l'image vers le chemin de fichier indiqué en utilisant les options fournies. Enfin, exportez le dessin vers un fichier PDF. La méthode `save` prend le chemin de sortie et les `PdfOptions` configurés.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Lorsque le code se termine, vous trouverez **Saved.pdf** dans votre dossier `DWGDrawings`, prêt pour la distribution ou l'archivage.

## Comment convertir des images raster DWG avec la bibliothèque Java CAD ?

Vous pouvez convertir DWG en formats raster en remplaçant `PdfOptions` par une classe d'options spécifique au raster telle que `PngOptions` ou `JpegOptions`. Réutilisez la même instance `CadRasterizationOptions`, ajustez le format de sortie et appelez la méthode `save` avec le nouvel objet d'options. Cette approche vous permet de générer des fichiers PNG, JPEG, BMP ou TIFF avec une seule modification de ligne, tout en conservant un flux de travail cohérent.

## Comment générer un PDF DWG en utilisant les options PDF CAD ?

L'exemple ci‑above génère déjà une sortie **pdf dwg**. Pour affiner la taille du PDF, activez la compression en appelant `pdfOptions.setCompress(true)`. Vous pouvez également intégrer des métadonnées personnalisées, définir la version du PDF ou ajouter une protection par mot de passe via des propriétés supplémentaires de `PdfOptions`. Ces ajustements vous donnent un contrôle total sur le PDF final sans quitter le code Java.

## Problèmes courants et astuces

- **Taille de page incorrecte** – Vérifiez la logique de conversion d'unités ; des coefficients incompatibles peuvent produire des pages surdimensionnées.  
- **Polices ou épaisseurs de ligne manquantes** – Assurez‑vous que le DWG référence toutes les ressources externes avant la conversion.  
- **Performance sur les grands dessins** – Augmentez le paramètre `DPI` dans `CadRasterizationOptions` uniquement lorsque une qualité supérieure est requise ; un DPI plus bas accélère le traitement.  
- **Problèmes de licence** – Pour l'évaluation, vous pouvez utiliser une **licence temporaire Aspose** ; une licence complète est requise pour les déploiements en production.

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD for Java avec d'autres frameworks Java ?**  
Oui, Aspose.CAD for Java s'intègre parfaitement aux frameworks Java populaires tels que Spring, Jakarta EE et Android.

**Q : Une licence temporaire est‑elle disponible pour Aspose.CAD for Java ?**  
Oui, vous pouvez obtenir une licence temporaire **[obtenir une licence temporaire](https://purchase.aspose.com/temporary-license/)**.

**Q : Où puis‑je trouver du support pour Aspose.CAD for Java ?**  
Visitez le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** pour obtenir de l'aide de la communauté et des ingénieurs Aspose.

**Q : Comment puis‑je acheter une licence pour Aspose.CAD for Java ?**  
Vous pouvez acheter une licence **[acheter une licence](https://purchase.aspose.com/buy)**.

**Q : Quelles unités Aspose.CAD for Java prend‑il en charge ?**  
Aspose.CAD for Java prend en charge les unités métriques et impériales, détectant automatiquement le système d'unités du dessin.

**Q : Puis‑je convertir DWG vers d'autres formats d'image (par ex., PNG, JPEG) en utilisant la même API ?**  
Absolument. Remplacez `PdfOptions` par les options d'image raster appropriées (par ex., `PngOptions`) et réutilisez le même `CadRasterizationOptions`.

## Conclusion

Ce tutoriel a démontré comment **export dwg pdf** et des images raster en utilisant la **bibliothèque java cad** Aspose.CAD for Java. En suivant le guide étape par étape, vous pouvez intégrer une conversion CAD fiable dans n'importe quelle application Java, que vous ayez besoin de PDF pour la documentation ou d'images raster pour l'affichage web. La nature pure Java de la bibliothèque, la sortie de haute qualité et la licence flexible en font un choix solide tant pour les petites utilitaires que pour les pipelines d'entreprise à grande échelle.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Tutoriels associés

- [Exporter DWG en PDF : mise en page spécifique avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exporter DWG en PDF en Java – définir la taille de page PDF avec Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Exporter DWG en PDF avec lignes cachées – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}