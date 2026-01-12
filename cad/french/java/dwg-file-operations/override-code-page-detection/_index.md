---
date: 2026-01-12
description: Apprenez à exporter des fichiers CAD en PDF tout en surchargeant la détection
  automatique de la page de code dans les fichiers DWG à l’aide d’Aspose.CAD pour
  Java. Gère l’encodage et les CIF/MIF malformés.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Exporter le CAD en PDF – Contourner la détection automatique de la page de
  code dans les fichiers DWG avec Java
url: /fr/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en PDF – Remplacer la détection automatique de la page de code dans les fichiers DWG avec Java

## Introduction

Dans ce guide complet, vous découvrirez **comment exporter CAD en PDF** tout en contournant la détection automatique de la page de code qui peut corrompre le texte dans les fichiers DWG. Aspose.CAD for Java vous offre un contrôle fin sur l’encodage, vous permettant de récupérer des données CIF/MIF malformées et de produire une sortie PDF fiable. Que vous construisiez un convertisseur par lots ou intégriez le traitement CAD dans une application Java plus vaste, les étapes ci‑dessous vous guideront à travers l’ensemble du flux de travail.

## Quick Answers
- **Que signifie « override code page » ?** Cela force Aspose.CAD à utiliser un encodage de caractères spécifique au lieu de deviner.
- **Puis‑je exporter un DWG directement en PDF ?** Oui – après avoir défini la bonne page de code, vous pouvez enregistrer l’image CAD au format PDF.
- **Quel encodage fonctionne pour le texte japonais ?** `CodePages.Japanese` et `MifCodePages.Japanese` sont les bons choix.
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise ; une licence temporaire est disponible pour les tests.
- **Quelle version d’Aspose.CAD est nécessaire ?** Toute version récente qui prend en charge `LoadOptions` et `PdfOptions`.

## What is “export CAD to PDF”?
Exporter CAD en PDF convertit les dessins CAD vectoriels en un format de document à mise en page fixe largement supporté. Le PDF résultant préserve les tracés, les calques et le texte tout en facilitant le partage, l’impression ou l’intégration du dessin dans d’autres applications.

## Why override the automatic code page detection?
Les fichiers DWG stockent souvent le texte à l’aide de pages de code héritées. L’auto‑détection d’Aspose.CAD peut mal interpréter ces octets, entraînant des caractères illisibles. En spécifiant manuellement la page de code, vous vous assurez que le texte apparaît exactement comme prévu dans le PDF exporté, notamment pour les scripts non latins tels que le japonais, le cyrillique ou l’arabe.

## Prerequisites
- **Environnement de développement Java** – JDK 8+ et votre IDE préféré.
- **Aspose.CAD for Java** – Téléchargez la bibliothèque depuis le site officiel [here](https://releases.aspose.com/cad/java/).
- **Fichier d’exemple DWG** – Utilisez le `SimpleEntities.dwg` fourni ou tout autre DWG que vous devez convertir.

## Import Packages
Dans votre projet Java, importez les classes Aspose.CAD nécessaires :

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Step‑by‑Step Guide

### Step 1: Set Up the Java Project
Créez un nouveau projet Maven ou Gradle et ajoutez le JAR Aspose.CAD au classpath. Cette étape garantit que l’IDE peut résoudre les classes importées.

### Step 2: Load the DWG File with a Specified Code Page
Indiquez à Aspose.CAD quel encodage utiliser et si vous devez tenter la récupération de données CIF/MIF malformées.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Step 3: Export the CAD Image to PDF
Avec la bonne page de code appliquée, vous pouvez exporter le dessin en toute sécurité. L’objet `PdfOptions` vous permet d’ajuster finement la sortie PDF (compression, rasterisation, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Step 4: Verify Success
Un simple message console confirme que le processus s’est terminé sans exception.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Vous pouvez répéter ces étapes pour plusieurs fichiers DWG, en ajustant le chemin source et le nom de sortie selon vos besoins.

## Common Issues & Solutions
- **Des caractères indésirables apparaissent toujours :** Vérifiez que le `specifiedEncoding` correspond à la page de code originale du DWG. Utilisez un autre enum `CodePages` si nécessaire.
- **`NullPointerException` sur `cadImage.save` :** Assurez‑vous que le fichier DWG se charge correctement ; vérifiez le chemin et les permissions du fichier.
- **La taille du PDF est grande :** Activez la compression dans `PdfOptions` (par ex., `pdfOptions.setCompress(true)`).

## Frequently Asked Questions

**Q1 : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?**  
R1 : Aspose.CAD prend en charge un large éventail de versions DWG, y compris AutoCAD 2018 et les versions antérieures.

**Q2 : Puis‑je utiliser Aspose.CAD pour des projets commerciaux ?**  
R2 : Oui, une licence commerciale est requise pour une utilisation en production. Vous pouvez obtenir une licence [here](https://purchase.aspose.com/buy).

**Q3 : Y a‑t‑il des limitations dans la version d’essai gratuite ?**  
R3 : L’essai impose des restrictions de taille et de fonctionnalités ; consultez la documentation officielle pour plus de détails.

**Q4 : Comment obtenir du support pour Aspose.CAD ?**  
R4 : Visitez la communauté [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

**Q5 : Une licence temporaire est‑elle disponible à des fins de test ?**  
R5 : Oui, une licence temporaire peut être demandée [here](https://purchase.aspose.com/temporary-license/).

---

**Last Updated:** 2026-01-12  
**Tested With:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}