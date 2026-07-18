---
date: 2026-07-18
description: La conversion Aspose CAD vous permet d'exporter facilement IFC vers PNG
  et IGES vers PDF. Apprenez pas à pas comment convertir des fichiers CAD avec Aspose.CAD
  pour .NET en quelques minutes.
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: Exportation vers des formats d'image
og_description: La conversion Aspose CAD permet une exportation rapide d'IFC vers
  PNG et IGES vers PDF. Suivez ce guide pour une gestion fluide des fichiers CAD avec
  Aspose.CAD pour .NET.
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: 'Conversion Aspose CAD : Exportation vers des formats d''image'
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: 'Conversion Aspose CAD : Exportation vers des formats d''image'
url: /fr/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Conversion Aspose CAD : Exportation vers des formats d'image

Dans les flux de travail modernes d'ingénierie et de conception, **aspose cad conversion** est essentiel pour transformer des fichiers CAD et BIM complexes en formats d'image universellement consultables. Que vous ayez besoin de partager un aperçu rapide d'un modèle IFC ou de générer un PDF imprimable à partir d'un dessin IGES, ce tutoriel vous guide pas à pas en utilisant Aspose.CAD pour .NET. Vous verrez comment conserver la géométrie, les couleurs et les calques tout en exportant vers PNG, PDF et d'autres formats raster.

## Réponses rapides
- **Quels formats Aspose.CAD peut‑il exporter ?** Plus de 30 formats CAD/BIM vers plus de 20 types d'image, y compris PNG, JPEG, PDF et TIFF.  
- **Ai‑je besoin d'une licence pour le développement ?** Un essai gratuit suffit pour l'évaluation ; une licence commerciale est requise pour la production.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Les gros fichiers peuvent‑ils être traités ?** Oui – Aspose.CAD traite des fichiers jusqu'à 2 GB sans charger le document complet en mémoire.  
- **Un logiciel supplémentaire est‑il requis ?** Aucun outil CAD externe n'est nécessaire ; la bibliothèque effectue toutes les conversions en interne.

## Qu'est‑ce que la conversion Aspose CAD ?
La classe `Image` représente un document CAD chargé en mémoire et fournit des méthodes pour l'enregistrer dans différents formats. La conversion Aspose CAD transforme les fichiers CAD/BIM en d'autres formats à l'aide d'Aspose.CAD pour .NET. Chargez la source avec `Image`, choisissez le format cible et appelez `Save`. Ce modèle en deux étapes préserve les calques, les épaisseurs de ligne et les textures, en respectant l'intention de conception originale.

## Comment exporter des fichiers IFC en PNG ?
La classe `Image` représente un document CAD chargé en mémoire et fournit des méthodes pour l'enregistrer dans différents formats. Chargez le fichier IFC avec `new Image("model.ifc")` et appelez `image.Save("model.png", ImageFormat.Png)`. Aspose.CAD lit la géométrie 3 D, la aplatit en une image raster et crée un PNG haute résolution qui conserve la profondeur de couleur et la transparence. Pour le traitement par lots, parcourez un dossier et enregistrez chaque fichier.

## Comment exporter des fichiers IGES en PDF ?
La classe `Image` représente un document CAD chargé en mémoire et fournit des méthodes pour l'enregistrer dans différents formats. Créez une instance `Image` à partir du fichier IGES et appelez `image.Save("drawing.pdf", ImageFormat.Pdf)`. La conversion préserve les informations vectorielles, les styles de ligne et les annotations, produisant un PDF qui peut être ouvert dans n'importe quel lecteur sans perte de détails. Utilisez la propriété optionnelle `Resolution` pour augmenter le DPI des PDF prêts à l'impression.

## Pourquoi utiliser Aspose.CAD pour .NET ?
Aspose.CAD prend en charge **plus de 30 formats d'entrée** (y compris IFC, IGES, DWG, DWF et STL) et peut produire **plus de 20 types d'image**. Il traite des dessins de plusieurs centaines de pages en moins de 5 secondes sur un serveur typique, et il fonctionne entièrement hors ligne—aucune installation CAD native n'est nécessaire. Ces avantages quantifiés en font un choix rentable et haute performance tant pour les entreprises que pour les développeurs indépendants.

## Pièges courants et astuces professionnelles
La classe `LoadOptions` vous permet de personnaliser la façon dont un fichier CAD est chargé, par exemple en définissant des limites de mémoire ou en spécifiant des calques.  
L'objet `FontSettings` définit les règles de substitution et d'intégration des polices utilisées pendant la conversion.  

- **Piège :** Ignorer le DPI par défaut peut produire des images basse résolution.  
  **Astuce :** Définissez `image.DpiX` et `image.DpiY` à 300 pour des PNG de qualité impression.  
- **Piège :** Les gros fichiers IGES peuvent dépasser les limites de mémoire.  
  **Astuce :** Utilisez `LoadOptions` avec `MemoryLimit` pour diffuser le fichier par morceaux.  
- **Piège :** L'absence de polices dans les modèles IFC entraîne du texte de substitution.  
  **Astuce :** Intégrez les polices requises à l'aide de l'objet `FontSettings` avant la conversion.

## Tutoriels d'exportation vers des formats d'image
### [Exporter des fichiers IFC en PNG - Tutoriel Aspose.CAD](./exporting-ifc-files-to-png/)
Explorez Aspose.CAD pour .NET, une solution robuste pour une conversion fluide d'IFC en PNG. Téléchargez dès maintenant pour un traitement efficace des fichiers CAD.  
### [Exporter des fichiers IGES en PDF - Guide Aspose.CAD](./exporting-iges-files-to-pdf/)
Apprenez à exporter facilement des fichiers IGES en PDF à l'aide d'Aspose.CAD pour .NET. Suivez notre guide étape par étape pour une manipulation précise des fichiers CAD.

## Questions fréquemment posées

**Q : Puis‑je convertir plusieurs fichiers CAD en un seul lot ?**  
R : Oui, parcourez un dossier avec `foreach (var file in Directory.GetFiles(path, "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"), ImageFormat.Png); }`.  
La méthode `Directory.GetFiles` renvoie les noms des fichiers (y compris leurs chemins) qui correspondent à un motif spécifié dans un répertoire.

**Q : Aspose.CAD préserve‑t‑il les informations de calque dans l'image exportée ?**  
R : La visibilité des calques est respectée ; vous pouvez activer/désactiver les calques via `LoadOptions` avant l'enregistrement, garantissant que seuls les calques sélectionnés apparaissent dans le résultat.

**Q : Quelle est la taille maximale de fichier qu'Aspose.CAD peut gérer ?**  
R : La bibliothèque traite aisément des fichiers jusqu'à **2 GB** ; les fichiers plus volumineux doivent être découpés ou diffusés à l'aide de `LoadOptions.MemoryLimit`.

**Q : Existe‑t‑il une prise en charge de la conversion CAD vers des PDF vectoriels ?**  
R : Oui—en enregistrant sous `ImageFormat.Pdf`, la sortie conserve les données vectorielles, permettant un redimensionnement infini sans perte de qualité.

**Q : Ai‑je besoin d'une licence distincte pour chaque plateforme .NET ?**  
R : Une seule licence Aspose.CAD couvre toutes les plateformes .NET prises en charge (Framework, Core et .NET 5+).

---

**Dernière mise à jour :** 2026-07-18  
**Testé avec :** Aspose.CAD 24.12 for .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Exporter des fichiers IFC en PNG - Tutoriel Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [Exporter des fichiers IGES en PDF - Guide Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Exporter les mises en page CAD vers des formats d'image raster dans Aspose.CAD pour .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}