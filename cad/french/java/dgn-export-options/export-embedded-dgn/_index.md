---
date: 2026-01-07
description: Apprenez à exporter des fichiers CAD au format PDF et à convertir des
  DGN en PDF à l'aide d'Aspose.CAD pour Java. Guide étape par étape pour les développeurs
  Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Exporter le CAD en PDF – Exporter le DGN intégré avec Aspose.CAD pour Java
url: /fr/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en PDF – Exporter DGN intégré avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter CAD en PDF** en convertissant un fichier DGN intégré en un document PDF de haute qualité avec Aspose.CAD pour Java. Aspose.CAD est une bibliothèque robuste qui offre aux développeurs Java un contrôle total sur la manipulation des fichiers CAD, que vous ayez besoin de **convertir DGN en PDF**, **convertir DWG en PDF**, ou simplement de rendre les dessins CAD dans d’autres formats. Suivez le guide étape par étape ci‑dessous, et vous pourrez intégrer cette fonctionnalité dans vos applications en quelques minutes.

## Quick Answers
- **Que signifie « export CAD to PDF » ?** Cela convertit les dessins CAD (DWG, DGN, etc.) en fichiers PDF tout en préservant la qualité vectorielle.  
- **Quelle bibliothèque est utilisée ?** Aspose.CAD pour Java.  
- **Ai‑je besoin d’une licence ?** Une licence est requise pour la production ; un essai gratuit est disponible.  
- **Quelles sont les principales conditions préalables ?** Environnement de développement Java et le JAR Aspose.CAD pour Java.  
- **Puis‑je personnaliser la sortie ?** Oui – vous pouvez sélectionner les mises en page, définir les options de rasterisation et contrôler les paramètres PDF.

## What is “export CAD to PDF”?

Exporter CAD en PDF consiste à prendre un fichier CAD natif (tel que DWG ou DGN) et à générer un document PDF qui représente fidèlement la géométrie originale. Le PDF peut être visualisé sur n’importe quelle plateforme sans nécessiter de logiciel CAD, ce qui le rend idéal pour le partage, l’impression ou l’archivage.

## Why use Aspose.CAD for Java to convert DGN to PDF?
- **Aucune dépendance externe** – fonctionne uniquement en Java.  
- **Préserve les données vectorielles** – les PDF restent nets quel que soit le niveau de zoom.  
- **Contrôle granulaire** – choisissez des mises en page spécifiques, définissez le DPI de rasterisation et intégrez les polices.  
- **Prêt pour l’entreprise** – prend en charge les gros fichiers, le traitement par lots et les options de licence.

## Prerequisites

Avant de commencer, assurez‑vous de disposer de :

- **Environnement de développement Java** – JDK 8 ou supérieur installé et configuré.  
- **Aspose.CAD pour Java** – téléchargez le dernier JAR depuis [here](https://releases.aspose.com/cad/java/).  

## Import Packages

Pour démarrer, vous devez importer les classes nécessaires dans votre projet Java. Ajoutez les instructions d’importation suivantes à votre fichier source :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## How to export DGN to PDF using Aspose.CAD for Java?

Voici un guide clair, numéroté, qui montre exactement comment convertir un fichier DGN intégré (stocké à l’intérieur d’un DWG) en PDF.

### Step 1: Set Up Input and Output Paths

Définissez le répertoire contenant votre fichier source et indiquez le DWG qui possède le DGN intégré.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Step 2: Load DWG File

Chargez le fichier DWG dans un objet `Image`. Aspose.CAD détecte automatiquement les données DGN intégrées.

```java
Image objImage = Image.load(fileName);
```

### Step 3: Configure Rasterization Options

Sélectionnez la ou les mises en page que vous souhaitez inclure dans le PDF. Dans cet exemple, nous exportons uniquement la mise en page **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Step 4: Configure PDF Options

Attachez les paramètres de rasterisation aux options d’exportation PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Save PDF File

Enfin, écrivez le PDF sur le disque en utilisant les options configurées.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Convert DWG to PDF – an additional tip

Si votre fichier source est un DWG simple (sans DGN intégré), vous pouvez réutiliser le même code – il suffit de changer la variable `fileName` pour pointer vers le DWG que vous souhaitez convertir. Les options de rasterisation et PDF restent identiques, vous offrant ainsi un flux de travail **convert DWG to PDF** cohérent.

## Common Issues and Solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **Blank PDF output** | Layout name mismatch | Verify that the layout name passed to `setLayouts` exactly matches the layout in the source file (case‑sensitive). |
| **License exception** | Using the trial without a license | Apply a valid Aspose.CAD license before loading the image (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the relative path is correct relative to the project’s working directory. |
| **Low‑resolution graphics** | Default rasterization DPI is low | Set `rasterizationOptions.setPageWidth/Height` or `setResolution` to increase DPI. |

## Frequently Asked Questions

**Q : Puis‑je utiliser Aspose.CAD pour Java dans un projet commercial ?**  
A : Oui, Aspose.CAD pour Java est une bibliothèque commerciale. Vous pouvez obtenir une licence depuis [here](https://purchase.aspose.com/buy).

**Q : Un essai gratuit est‑il disponible ?**  
A : Oui, vous pouvez accéder à un essai gratuit d’Aspose.CAD pour Java [here](https://releases.aspose.com/).

**Q : Comment obtenir du support pour Aspose.CAD pour Java ?**  
A : Vous pouvez demander de l’aide à la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19).

**Q : Et si j’ai besoin d’une licence temporaire ?**  
A : Vous pouvez obtenir une licence temporaire [here](https://purchase.aspose.com/temporary-license/).

**Q : Où trouver la documentation ?**  
A : La documentation est disponible [here](https://reference.aspose.com/cad/java/).

## Conclusion

Vous avez maintenant appris comment **exporter CAD en PDF**, plus précisément comment **convertir DGN en PDF** et même **convertir DWG en PDF** à l’aide d’Aspose.CAD pour Java. En suivant les étapes ci‑dessus, vous pouvez intégrer une conversion CAD‑vers‑PDF fluide dans toute solution Java, offrant des PDF de haute qualité à vos utilisateurs sans nécessiter de logiciel CAD supplémentaire.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-01-07  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose