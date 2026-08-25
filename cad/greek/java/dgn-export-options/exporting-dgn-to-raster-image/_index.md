---
date: 2026-05-25
description: Μάθετε πώς να εξάγετε αρχεία dgn σε εικόνες JPEG με Aspose.CAD for Java.
  Αυτός ο οδηγός βήμα‑βήμα σας δείχνει πώς να μετατρέψετε dgn σε jpeg αποδοτικά.
keywords:
- how to export dgn
- convert dgn to jpeg
- java convert cad to image
linktitle: Εξαγωγή DGN σε μορφή AutoCAD σε μορφή Raster Image Format
schemas:
- author: Aspose
  dateModified: '2026-05-25'
  description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  headline: How to Export DGN to JPEG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export dgn files to JPEG images with Aspose.CAD for Java.
    This step‑by‑step guide shows you how to convert dgn to jpeg efficiently.
  name: How to Export DGN to JPEG with Aspose.CAD for Java
  steps:
  - name: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
    text: '**Aspose.CAD Library** – download the latest JAR from the official site [here](https://releases.aspose.com/cad/java/).
      You can also explore other product releases [here](https://releases.aspose.com/).'
  - name: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
    text: '**Java Development Kit (JDK)** – Java 8 or newer installed on your machine.'
  - name: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
    text: '**IDE** – IntelliJ IDEA, Eclipse, or any Java‑compatible editor you prefer.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF,
      and SVG, enabling a single API for many conversion scenarios.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Refer to the official docs [here](https://reference.aspose.com/cad/java/).
    question: Where can I find documentation for Aspose.CAD for Java?
  - answer: Visit the support forum [here](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can buy a license [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Πώς να εξάγετε DGN σε JPEG με Aspose.CAD for Java
url: /el/java/dgn-export-options/exporting-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Java DGN σε JPEG Μετατροπή με Aspose.CAD Οδηγός

## Εισαγωγή

In this comprehensive guide you’ll discover **how to export dgn** files to JPEG images using Aspose.CAD for Java. Whether you’re building a batch‑processing service or adding on‑the‑fly preview generation to a CAD viewer, this tutorial walks you through every step, from loading the source file to saving the raster output. You’ll also see practical tips that keep your code clean and performant.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρειάζομαι;** Aspose.CAD for Java (download [εδώ](https://releases.aspose.com/cad/java/)).
- **Μπορώ να μετατρέψω DGN σε JPEG σε μία γραμμή;** Ναι – load with `CadImage.load` and call `save` with `JpegOptions`.
- **Απαιτείται άδεια για παραγωγή;** Ναι, μια εμπορική άδεια αφαιρεί το υδατογράφημα αξιολόγησης.
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 μέχρι 17 υποστηρίζονται πλήρως.
- **Πόσο μεγάλο DGN μπορώ να επεξεργαστώ;** Αρχεία έως 2 GB διαχειρίζονται χωρίς να φορτωθεί ολόκληρο το αρχείο στη μνήμη.

## Τι είναι το «πώς να εξάγετε dgn»;
*«How to export dgn»* refers to the process of converting a MicroStation DGN design file into another format, typically a raster image such as JPEG, for easier viewing or sharing. This conversion enables stakeholders who do not have CAD software to inspect designs, embed images in documents, or generate thumbnails for web galleries, improving accessibility and collaboration across teams.

## Γιατί να χρησιμοποιήσετε Aspose.CAD για Java;
Aspose.CAD supports **30+ CAD formats** (including DGN, DWG, DXF) and can render files **up to 2 GB** without requiring the original CAD application. Its raster engine processes multi‑page drawings at **> 50 fps** on standard server hardware, delivering high‑quality JPEG output with a single API call.

## Προαπαιτούμενα

Before diving in, ensure you have:

1. **Aspose.CAD Library** – κατεβάστε το τελευταίο JAR από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/cad/java/). Μπορείτε επίσης να εξερευνήσετε άλλες εκδόσεις προϊόντων [εδώ](https://releases.aspose.com/).  
2. **Java Development Kit (JDK)** – Java 8 ή νεότερη εγκατεστημένη στο σύστημά σας.  
3. **IDE** – IntelliJ IDEA, Eclipse ή οποιονδήποτε επεξεργαστή συμβατό με Java που προτιμάτε.

## Εισαγωγή Πακέτων

In your Java project, import the necessary Aspose.CAD classes:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
```

## Πώς να εξάγετε dgn σε JPEG χρησιμοποιώντας Aspose.CAD σε Java;

The `CadImage` class represents a CAD document loaded into memory, providing methods for rendering and saving.

Load your DGN file with `CadImage.load("source.dgn")`, configure `JpegOptions` (including quality and resolution), set appropriate `RasterizationOptions` such as page dimensions and background color, and finally call `image.save("output.jpg", jpegOptions)`. This three‑step flow handles vector‑to‑raster conversion, preserves line weights, and writes a high‑quality JPEG file in under a second for typical drawings.

## Βήμα 1: Φόρτωση Αρχείου DGN

The `CadImage` class represents a CAD document loaded into memory.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Βήμα 2: Δημιουργία Αντικειμένου JpegOptions

`JpegOptions` defines settings specific to JPEG output, such as compression quality and resolution.

```java
ImageOptionsBase options = new JpegOptions();
```

## Βήμα 3: Ανάθεση Ρυθμίσεων Rasterization

`RasterizationOptions` determines how vector graphics are rasterized, including page size, DPI, background color, and anti‑aliasing.

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Βήμα 4: Αποθήκευση της Μετατρεπόμενης Εικόνας

Calling `save` writes the raster image to disk using the options you supplied.

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

### Συνηθισμένες Περιπτώσεις Χρήσης

- **Δημιουργία προεπισκόπησης ιστού** – Convert engineering drawings to lightweight JPEG thumbnails for quick display in browsers.  
- **Ομαδική αρχειοθέτηση** – Automate conversion of thousands of DGN files to JPEG for long‑term storage without needing MicroStation.  
- **Αναφορές** – Embed CAD snapshots into PDF or HTML reports directly from Java code.

### Συνηθισμένα Προβλήματα και Λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Η εικόνα εμφανίζεται κενή** | Ensure `RasterizationOptions.setPageWidth/Height` matches the drawing’s extents, and set a non‑transparent background. |
| **Έξοδος χαμηλής ποιότητας** | Increase `JpegOptions.setQuality(100)` and set a higher DPI (e.g., `RasterizationOptions.setResolution(300)`). |
| **Σφάλματα έλλειψης μνήμης** | Use `CadImage.load` with the `loadOptions.setLoadMode(LoadMode.Memory)` to stream large files. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω Aspose.CAD για Java με άλλες μορφές αρχείων CAD;**  
Α: Yes, Aspose.CAD supports over 30 vector formats, including DWG, DXF, DWF, and SVG, enabling a single API for many conversion scenarios.

**Ε: Υπάρχει δωρεάν δοκιμή διαθέσιμη για Aspose.CAD για Java;**  
Α: Yes, you can access a free trial [εδώ](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω τεκμηρίωση για Aspose.CAD για Java;**  
Α: Refer to the official docs [εδώ](https://reference.aspose.com/cad/java/).

**Ε: Πώς μπορώ να λάβω υποστήριξη για Aspose.CAD για Java;**  
Α: Visit the support forum [εδώ](https://forum.aspose.com/c/cad/19).

**Ε: Πού μπορώ να αγοράσω άδεια για Aspose.CAD για Java;**  
Α: You can buy a license [εδώ](https://purchase.aspose.com/buy).

---

**Last Updated:** 2026-05-25  
**Tested With:** Aspose.CAD 24.11 for Java  
**Author:** Aspose

## Σχετικές Οδηγίες

- [Απρόσκοπτη Εξαγωγή DGN σε AutoCAD PDF με Aspose.CAD για Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Εξαγωγή DGN σε DWG με Aspose.CAD για Java – Οδηγός](/cad/java/dgn-export-options/)
- [Αποθήκευση CAD ως PNG – Μετατροπή Σχεδίου CAD σε Μορφή Raster Εικόνας Χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}