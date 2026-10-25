---
date: 2026-10-25
description: Μάθετε πώς να μετατρέψετε DWG σε PNG και να αποθηκεύσετε CAD ως PNG χρησιμοποιώντας
  το Aspose.CAD for Java, διαχειριζόμενοι αρχεία DWG, DXF, DWF και άλλα αρχεία CAD
  με υψηλής απόδοσης rasterization.
keywords:
- convert dwg to png
- save cad as png
- cad to png conversion
- how to rasterize cad
- convert dwg raster image
lastmod: 2026-10-25
linktitle: Μετατροπή σχεδίου CAD σε μορφή raster εικόνας
og_description: Μετατρέψτε DWG σε PNG γρήγορα με το Aspose.CAD for Java. Αυτός ο οδηγός
  σας δείχνει πώς να αποθηκεύσετε CAD ως PNG, να διαμορφώσετε επιλογές raster και
  να διαχειριστείτε μαζικές μετατροπές—ιδανικό για προεπισκοπήσεις ιστού και αναφορές.
og_image_alt: 'Developer guide: convert DWG to PNG using Aspose.CAD Java API'
og_title: Πώς να μετατρέψετε DWG σε PNG χρησιμοποιώντας το Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  headline: How to convert DWG to PNG using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to convert DWG to PNG and save CAD as PNG using Aspose.CAD
    for Java, handling DWG, DXF, DWF and other CAD files with high‑performance rasterization.
  name: How to convert DWG to PNG using Aspose.CAD for Java
  steps:
  - name: '**Java Development Kit** – JDK 8 or later installed and configured.'
    text: '**Java Development Kit** – JDK 8 or later installed and configured.'
  - name: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
    text: '**Aspose.CAD for Java** – download the latest JAR from the official Aspose.CAD
      for Java releases page [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).'
  - name: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
    text: '**A DWG file** – any valid DWG, DXF or DWF drawing you want to rasterize.'
  type: HowTo
- questions:
  - answer: Set the `backgroundColor` property on `CadRasterizationOptions` before
      creating the `PngOptions` instance.
    question: How do I convert a DWG file to PNG with a custom background color?
  - answer: Yes—wrap the loading, rasterization, and saving steps inside a loop that
      iterates over your file collection.
    question: Can I process multiple CAD files in one batch operation?
  - answer: The default DPI of 96 produces screen‑quality PNGs; raise the DPI to 300
      for high‑resolution print output.
    question: What image quality can I expect from the default settings?
  - answer: Absolutely. PNGs are saved with an alpha channel by default, and you can
      explicitly set a transparent background in the rasterization options.
    question: Does Aspose.CAD support transparent backgrounds in PNG output?
  - answer: Yes—replace `PngOptions` with `JpegOptions` or `BmpOptions` while reusing
      the same `CadRasterizationOptions`.
    question: Can I convert CAD files to other raster formats like JPEG or BMP?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java CAD processing
- raster image conversion
title: Πώς να μετατρέψετε DWG σε PNG χρησιμοποιώντας το Aspose.CAD for Java
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να μετατρέψετε DWG σε PNG χρησιμοποιώντας το Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το μάθημα θα μάθετε πώς να **μετατρέψετε DWG σε PNG** με το Aspose.CAD για Java. Η μετατροπή σχεδίων CAD σε μορφές raster εικόνας όπως PNG είναι μια κοινή ανάγκη όταν θέλετε να ενσωματώσετε σχέδια σε ιστοσελίδες, να δημιουργήσετε μικρογραφίες ή να τα συμπεριλάβετε σε αναφορές PDF. Το Aspose.CAD προσφέρει μια καθαρή λύση Java που διαχειρίζεται DWG, DXF, DWF και περισσότερες από 50 άλλες μορφές CAD χωρίς εξαρτήσεις native, παρέχοντας χρόνους μετατροπής κάτω από ένα δευτερόλεπτο για τυπικά σχέδια.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή;** Aspose.CAD για Java.  
- **Μπορώ να μετατρέψω DWG σε PNG;** Ναι – το ίδιο API λειτουργεί για DWG, DXF, DWF και πολλές άλλες μορφές.  
- **Χρειάζεται άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια για μη‑αξιολογική χρήση.  
- **Μπορεί το μέγεθος raster να ρυθμιστεί;** Απόλυτα – μπορείτε να ορίσετε πλάτος σελίδας, ύψος, DPI και χρώμα φόντου μέσω των επιλογών rasterization.  
- **Πόσο διαρκεί η μετατροπή;** Συνήθως κάτω από ένα δευτερόλεπτο για τυπικά σχέδια· μεγαλύτερα αρχεία με εκατοντάδες σελίδες μπορεί να χρειαστούν λίγα δευτερόλεπτα.

## Πώς να μετατρέψετε DWG σε PNG χρησιμοποιώντας το Aspose.CAD

Φορτώστε το αρχείο CAD, διαμορφώστε τις επιλογές rasterization, δημιουργήστε επιλογές ειδικές για PNG και, τέλος, αποθηκεύστε την raster εικόνα. Αυτή η ολοκληρωμένη ροή μετατρέπει τα διανυσματικά δεδομένα DWG σε pixel‑based PNG διατηρώντας το βάρος των γραμμών, τα επίπεδα και τα χρώματα.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java;

Το Aspose.CAD υποστηρίζει **50+** μορφές εισόδου και εξόδου — συμπεριλαμβανομένων DWG, DXF, DWF, SVG και μορφές raster όπως PNG, JPEG και BMP. Μπορεί να επεξεργαστεί αρχεία έως **500 MB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, καθιστώντας το ιδανικό για παρτίδες. Η βιβλιοθήκη λειτουργεί σε οποιοδήποτε runtime Java 8+, δεν απαιτεί εξωτερικά DLLs και προσφέρει λεπτομερή έλεγχο της ανάλυσης, του χρώματος φόντου και της ποιότητας απόδοσης, όλα με λίγες γραμμές κώδικα.

## Προαπαιτούμενα

1. **Java Development Kit** – JDK 8 ή νεότερο εγκατεστημένο και ρυθμισμένο.  
2. **Aspose.CAD για Java** – κατεβάστε το τελευταίο JAR από τη σελίδα εκδόσεων του Aspose.CAD για Java [ Aspose.CAD for Java download page ](https://releases.aspose.com/cad/java/).  
3. **Αρχείο DWG** – οποιοδήποτε έγκυρο αρχείο DWG, DXF ή DWF που θέλετε να rasterize.  

Προσθέστε το JAR του Aspose.CAD στο classpath του έργου σας (Maven, Gradle ή χειροκίνητη ένταξη).

## Εισαγωγή ονοματοχώρων

Το πακέτο `com.aspose.cad` περιέχει όλες τις κλάσεις που χρειάζεστε για τη φόρτωση, rasterization και αποθήκευση σχεδίων CAD.

Η κλάση `Image` είναι το σημείο εισόδου του Aspose.CAD για τη φόρτωση οποιουδήποτε υποστηριζόμενου αρχείου CAD στη μνήμη.  
Η κλάση `CadRasterizationOptions` σας επιτρέπει να ορίσετε πώς τα διανυσματικά δεδομένα μετατρέπονται σε pixel (μέγεθος, DPI, φόντο κ.λπ.).  
Η κλάση `PngOptions` καθορίζει τις ρυθμίσεις εξόδου ειδικές για PNG, όπως επίπεδο συμπίεσης και διαχείριση διαφάνειας.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία μετατροπής ενός σχεδίου CAD σε raster εικόνα σε λεπτομερή βήματα:

## Βήμα 1: φόρτωση σχεδίου CAD

Η μέθοδος `Image.load()` διαβάζει το αρχείο προέλευσης και δημιουργεί μια αναπαράσταση στη μνήμη που μπορείτε αργότερα να rasterize.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Βήμα 2: ορισμός επιλογών rasterization

Δημιουργήστε ένα αντικείμενο `CadRasterizationOptions` και διαμορφώστε το πλάτος σελίδας, το ύψος, το DPI και το χρώμα φόντου. Αυτές οι ρυθμίσεις καθορίζουν την ποιότητα και το μέγεθος του τελικού PNG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

## Βήμα 3: δημιουργία επιλογών εικόνας

Δημιουργήστε ένα αντικείμενο `PngOptions` και αντιστοιχίστε του τις προηγουμένως διαμορφωμένες επιλογές rasterization. Αυτό συνδέει τις παραμέτρους μετατροπής vector‑to‑raster με τη μορφή εξόδου PNG.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

## Βήμα 4: αποθήκευση raster εικόνας

Καλέστε `image.save()` με το αντικείμενο `PngOptions` και τη διαδρομή του αρχείου προορισμού. Η μέθοδος γράφει το rasterized PNG στο δίσκο, ολοκληρώνοντας τη μετατροπή.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Επαναλάβετε αυτά τα βήματα για κάθε αρχείο CAD που χρειάζεται επεξεργασία και θα έχετε μια αξιόπιστη **cad to png conversion** pipeline.

## Κοινές περιπτώσεις χρήσης & συμβουλές

- **Web preview generation** – Μετατρέψτε μεγάλα αρχεία DWG σε ελαφριές μικρογραφίες PNG για άμεση προβολή στον περιηγητή.  
- **Report embedding** – Χρησιμοποιήστε την έξοδο PNG σε αναφορές PDF ή Word όπου δεν υποστηρίζονται οι εγγενείς μορφές CAD.  
- **Batch conversion** – Επανάληψη σε φάκελο αρχείων CAD, εφαρμόζοντας τις ίδιες ρυθμίσεις rasterization για συνεπή αποτελέσματα.  
- **Pro tip:** Αυξήστε το `rasterizationOptions.setResolution()` στα 300 DPI για εικόνες έτοιμες για εκτύπωση· το προεπιλεγμένο 96 DPI είναι βέλτιστο για οθόνη.  
- **How to convert DWG to other formats** – Αντικαταστήστε το `PngOptions` με `JpegOptions` ή `BmpOptions` διατηρώντας την ίδια διαμόρφωση rasterization.

## Συμπέρασμα

Ακολουθώντας τα παραπάνω βήματα, μπορείτε αποδοτικά **μετατρέψετε DWG σε PNG**, **αποθηκεύσετε CAD ως PNG**, ή να εκτελέσετε οποιαδήποτε **cad to png conversion** απαιτεί η εφαρμογή σας. Το Aspose.CAD για Java σας δίνει πλήρη έλεγχο της ανάλυσης, του χρώματος φόντου και της μορφής εξόδου, καθιστώντας το την προτιμώμενη λύση για προεπισκοπήσεις ιστού, αγωγούς τεκμηρίωσης και μεγάλης κλίμακας batch επεξεργασία.

## Συχνές ερωτήσεις

**Q: Πώς μετατρέπω ένα αρχείο DWG σε PNG με προσαρμοσμένο χρώμα φόντου;**  
A: Ορίστε την ιδιότητα `backgroundColor` στο `CadRasterizationOptions` πριν δημιουργήσετε το αντικείμενο `PngOptions`.

**Q: Μπορώ να επεξεργαστώ πολλά αρχεία CAD σε μία batch λειτουργία;**  
A: Ναι—τυλίξτε τα βήματα φόρτωσης, rasterization και αποθήκευσης μέσα σε έναν βρόχο που διατρέχει τη συλλογή αρχείων σας.

**Q: Ποια ποιότητα εικόνας μπορώ να περιμένω από τις προεπιλεγμένες ρυθμίσεις;**  
A: Το προεπιλεγμένο DPI των 96 παράγει PNGs ποιότητας οθόνης· αυξήστε το DPI στα 300 για υψηλής ανάλυσης εκτύπωση.

**Q: Υποστηρίζει το Aspose.CAD διαφάνεια φόντου στην έξοδο PNG;**  
A: Απόλυτα. Τα PNG αποθηκεύονται με κανάλι άλφα από προεπιλογή, και μπορείτε ρητά να ορίσετε διαφανές φόντο στις επιλογές rasterization.

**Q: Μπορώ να μετατρέψω αρχεία CAD σε άλλες raster μορφές όπως JPEG ή BMP;**  
A: Ναι—αντικαταστήστε το `PngOptions` με `JpegOptions` ή `BmpOptions` ενώ επαναχρησιμοποιείτε το ίδιο `CadRasterizationOptions`.

**Τελευταία ενημέρωση:** 2026-10-25  
**Δοκιμή με:** Aspose.CAD για Java 24.12 (τελευταία)  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Auto Adjust CAD Drawing Size and Convert DWG to BMP with Aspose.CAD for Java](/cad/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/)
- [Save DWG as JPEG with Layer Support in Java using Aspose.CAD](/cad/java/advanced-cad-features/support-of-layers-in-cad/)
- [Save CAD as PNG – Export OLE Objects Using Aspose.CAD for Java](/cad/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}