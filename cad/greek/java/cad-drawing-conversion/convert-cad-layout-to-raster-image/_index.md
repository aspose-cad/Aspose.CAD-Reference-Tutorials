---
date: 2026-10-04
description: Μάθετε πώς να μετατρέπετε γρήγορα το dwg σε png και να εξάγετε το cad
  ως png ή άλλες μορφές raster χρησιμοποιώντας το Aspose.CAD for Java. Λάβετε αποτελέσματα
  υψηλής ποιότητας γρήγορα.
keywords:
- convert dwg to png
- dwg to raster image
- convert cad to pdf
- export cad as png
- convert dwg to jpeg
lastmod: 2026-10-04
linktitle: Μετατροπή διάταξης CAD σε μορφή raster εικόνας
og_description: Μετατρέψτε γρήγορα το DWG σε PNG με το Aspose.CAD for Java. Μάθετε
  βήμα‑βήμα πώς να εξάγετε το CAD ως PNG, JPEG, TIFF και άλλα.
og_image_alt: 'Developer guide: Convert DWG to PNG and other raster formats using
  Aspose.CAD for Java'
og_title: Μετατροπή DWG σε PNG και άλλες μορφές raster χρησιμοποιώντας το Aspose.CAD
  for Java
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  headline: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to quickly convert dwg to png and export cad as png or other
    raster formats using Aspose.CAD for Java. Get high‑quality results fast.
  name: Convert DWG to PNG and other raster formats using Aspose.CAD for Java
  steps:
  - name: set up the resource directory
    text: Replace `"Your Document Directory"` with the absolute path where your CAD
      files reside. This directory will be used for both input and output files.
  - name: load the CAD file
    text: '`Image.load` parses the source file and creates an in‑memory representation
      that you can rasterize. You can load any supported format (DWG, DXF, DGN, etc.)
      – this is the **how to convert cad** part.'
  - name: configure rasterization options
    text: '`CadRasterizationOptions` defines how the vector data is turned into pixels.
      `setPageWidth` and `setPageHeight` control output resolution (larger values
      = higher DPI). `setLayouts` lets you **convert CAD to raster** for specific
      layouts; omit it to rasterize the whole drawing.'
  - name: set image options
    text: '`TiffOptions` (or `PngOptions` for PNG) tells Aspose which raster format
      to generate and lets you fine‑tune compression, color depth, and other format‑specific
      settings. Choose the options class that matches your desired output.'
  - name: save the resultant image
    text: Call `save` on the `Image` instance, passing the output file name and the
      options object. Change the file extension to `.png` (and use `PngOptions`) to
      **save CAD as PNG**. The same pattern works for JPEG, BMP, or PDF. > **Common
      pitfall:** Forgetting to match the file extension with the options cla
  type: HowTo
- questions:
  - answer: Yes, it supports over 30 CAD and raster formats, including DWG, DXF, DGN,
      and SVG.
    question: Is Aspose.CAD compatible with different CAD file formats?
  - answer: Absolutely. Adjust `setPageWidth`, `setPageHeight`, or `setResolution`
      in `CadRasterizationOptions` to achieve the desired DPI.
    question: Can I customize the resolution of the output raster image?
  - answer: Provide an array with all layout names to `setLayouts`, e.g., `new String[]{"Model","Layout1","Layout2"}`.
    question: How can I convert multiple CAD layouts in a single run?
  - answer: Yes—PNG, JPEG, BMP, PDF, and more are available via their respective `*Options`
      classes.
    question: Are there output formats besides TIFF supported?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      support and official assistance.
    question: Where can I get help or share my experience with Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- Aspose.CAD
- Java raster conversion
- CAD image processing
title: Μετατροπή DWG σε PNG και άλλες μορφές raster χρησιμοποιώντας το Aspose.CAD
  for Java
url: /el/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DWG σε PNG και άλλες μορφές raster χρησιμοποιώντας το Aspose.CAD για Java

## Εισαγωγή

`Aspose.CAD for Java` είναι μια βιβλιοθήκη που επιτρέπει την προγραμματιστική μετατροπή αρχείων CAD σε raster εικόνες όπως PNG, JPEG και TIFF. Η μετατροπή DWG σε PNG (ή άλλες μορφές raster εικόνας) είναι συχνή απαίτηση όταν χρειάζεται να μοιραστείτε σχέδια CAD με συναδέλφους που δεν διαθέτουν προβολέα CAD, να ενσωματώσετε σχέδια σε τεκμηρίωση ή να δημιουργήσετε μικρογραφίες για διαδικτυακές γκαλερί. Σε αυτόν τον οδηγό θα μάθετε πώς να μετατρέψετε dwg σε png γρήγορα και αξιόπιστα, είτε εργάζεστε με ένα πλήρες αρχείο σχεδίασης είτε μόνο με συγκεκριμένη διάταξη. Μπορεί επίσης να χρειαστεί να **convert CAD to raster** για προεπισκοπήσεις ιστού, εργαλεία αναφοράς ή κινητές εφαρμογές.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή DWG σε PNG;** Το Aspose.CAD for Java παρέχει τη μηχανή μετατροπής.  
- **Ποιες μορφές raster μπορώ να εξάγω;** PNG, JPEG, TIFF, PDF, BMP, και περισσότερες από 30 επιπλέον μορφές.  
- **Χρειάζομαι άδεια για δοκιμές;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να επιλέξω συγκεκριμένη διάταξη;** Ναι – χρησιμοποιήστε το `setLayouts` για να στοχεύσετε το “Model”, “Layout1”, κλπ.  
- **Είναι δυνατή η έξοδος υψηλής ανάλυσης;** Απολύτως – προσαρμόστε τα `setPageWidth` και `setPageHeight` (ή `setResolution`) για να ελέγξετε το DPI.

## Τι σημαίνει η “convert dwg to png”;

Η μετατροπή dwg σε png σημαίνει τη μετατροπή ενός διανυσματικού σχεδίου DWG σε μια εικόνα PNG βασισμένη σε εικονοστοιχεία που μπορεί να προβληθεί από οποιονδήποτε τυπικό προβολέα εικόνων. Αυτή η διαδικασία rasterizes τα διανυσματικά στοιχεία, διατηρώντας το πάχος γραμμής, τα χρώματα και τα επίπεδα ενώ τα μετατρέπει σε bitmap σταθερής ανάλυσης. Το αποτέλεσμα είναι ιδανικό για ενσωμάτωση σε PDF, έγγραφα Word ή ιστοσελίδες όπου η υποστήριξη διανυσματικών γραφικών είναι περιορισμένη.

## Γιατί να εξάγετε CAD ως PNG (ή άλλες μορφές raster);

Η εξαγωγή CAD ως PNG σας παρέχει καθολική συμβατότητα, γρήγορη φόρτωση και εύκολη ενσωμάτωση σε όλες τις κύριες πλατφόρμες. Οι raster εικόνες φορτώνουν άμεσα σε σύγκριση με το άνοιγμα ενός βαρέως αρχείου DWG, και η μη απώλεια συμπίεση του PNG εξασφαλίζει οπτική πιστότητα. Με τον έλεγχο της ανάλυσης, του χρώματος φόντου και της διάταξης, εγγυάστε ότι κάθε ενδιαφερόμενος βλέπει την ίδια εμφάνιση, είτε το αρχείο προβάλλεται σε επιτραπέζιο υπολογιστή, κινητή συσκευή ή μέσα σε πρόγραμμα περιήγησης.

## Συνηθισμένες περιπτώσεις χρήσης

| Σενάριο | Γιατί η έξοδος raster βοηθά |
|----------|------------------------|
| **Τεκμηρίωση έργου** | Η ενσωμάτωση PNG σε PDF ή έγγραφα Word αποφεύγει την ανάγκη λογισμικού CAD για τους αξιολογητές. |
| **Διαδικτυακές πύλες** | Οι μικρογραφίες που δημιουργούνται από αρχεία DWG φορτώνουν άμεσα και βελτιώνουν την εμπειρία χρήστη. |
| **Κινητές εφαρμογές** | Οι raster εικόνες εμφανίζονται σωστά σε συσκευές που δεν διαθέτουν προβολείς CAD. |
| **Αυτοματοποιημένες αναφορές** | Μαζική μετατροπή πολλαπλών διατάξεων σε PNG/JPEG για ενσωμάτωση σε γραφήματα ή πίνακες ελέγχου. |

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

1. **Java development environment** – JDK 8 ή νεότερο εγκατεστημένο και ρυθμισμένο.  
2. **Aspose.CAD for Java** – Κατεβάστε το τελευταίο JAR από την [Aspose.CAD for Java documentation](https://reference.aspose.com/cad/java/).  

## Εισαγωγή ονοματοχώρων

`com.aspose.cad.Image` είναι η βασική κλάση που αντιπροσωπεύει οποιοδήποτε αρχείο CAD στη μνήμη. `com.aspose.cad.imageoptions.*` παρέχει αντικείμενα επιλογών για κάθε μορφή raster. Εισάγετε τις κλάσεις που θα χρειαστείτε για να φορτώσετε ένα σχέδιο, να διαμορφώσετε τη rasterization και να αποθηκεύσετε το αποτέλεσμα.

> **Συμβουλή:** Αν σκοπεύετε να **export CAD as PNG** αντί για TIFF, αντικαταστήστε το `TiffOptions` με το `PngOptions` (βρίσκεται στο `com.aspose.cad.imageoptions.PngOptions`).

## Οδηγός βήμα‑βήμα

### Βήμα 1: ρύθμιση του καταλόγου πόρων

Αντικαταστήστε το `"Your Document Directory"` με το απόλυτο μονοπάτι όπου βρίσκονται τα αρχεία CAD σας. Αυτός ο κατάλογος θα χρησιμοποιηθεί τόσο για αρχεία εισόδου όσο και εξόδου.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

### Βήμα 2: φόρτωση του αρχείου CAD

`Image.load` αναλύει το αρχείο προέλευσης και δημιουργεί μια αναπαράσταση στη μνήμη που μπορείτε να rasterize. Μπορείτε να φορτώσετε οποιαδήποτε υποστηριζόμενη μορφή (DWG, DXF, DGN, κλπ.) – αυτό είναι το μέρος **how to convert cad**.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";
```

### Βήμα 3: διαμόρφωση επιλογών rasterization

`CadRasterizationOptions` ορίζει πώς τα διανυσματικά δεδομένα μετατρέπονται σε εικονοστοιχεία. `setPageWidth` και `setPageHeight` ελέγχουν την ανάλυση εξόδου (μεγαλύτερες τιμές = υψηλότερο DPI). `setLayouts` σας επιτρέπει να **convert CAD to raster** για συγκεκριμένες διατάξεις· παραλείψτε το για rasterize ολόκληρο το σχέδιο.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Βήμα 4: ρύθμιση επιλογών εικόνας

`TiffOptions` (ή `PngOptions` για PNG) ενημερώνει το Aspose ποια μορφή raster να δημιουργήσει και σας επιτρέπει να ρυθμίσετε λεπτομερώς τη συμπίεση, το βάθος χρώματος και άλλες ρυθμίσεις ειδικές για τη μορφή. Επιλέξτε την κλάση επιλογών που ταιριάζει στην επιθυμητή έξοδο.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});
```

### Βήμα 5: αποθήκευση της προκύπτουσας εικόνας

Καλέστε το `save` στο αντικείμενο `Image`, περνώντας το όνομα του αρχείου εξόδου και το αντικείμενο επιλογών. Αλλάξτε την επέκταση αρχείου σε `.png` (και χρησιμοποιήστε `PngOptions`) για **save CAD as PNG**. Το ίδιο μοτίβο λειτουργεί για JPEG, BMP ή PDF.

```java
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.setVectorRasterizationOptions(rasterizationOptions);
```

> **Συνηθισμένο λάθος:** Η παράλειψη του να ταιριάζει η επέκταση αρχείου με την κλάση επιλογών θα προκαλέσει `UnsupportedFormatException`. Πάντα διατηρείτε τα σε συγχρονισμό.

## Συχνά προβλήματα και λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Κενή εικόνα εξόδου** | Βεβαιωθείτε ότι τα ονόματα διατάξεων στο `setLayouts` ταιριάζουν ακριβώς με αυτά στο πηγαίο αρχείο CAD. |
| **PNG χαμηλής ανάλυσης** | Αυξήστε το `setPageWidth` / `setPageHeight` ή ορίστε `setResolution` στις επιλογές rasterization. |
| **Μη υποστηριζόμενη έκδοση DWG** | Βεβαιωθείτε ότι χρησιμοποιείτε την πιο πρόσφατη έκδοση του Aspose.CAD· παλαιότερες εκδόσεις μπορεί να μην υποστηρίζουν νεότερες εκδόσεις DWG. |
| **Σφάλματα μνήμης σε μεγάλα αρχεία** | Επεξεργαστείτε τις σελίδες μία τη φορά ή αυξήστε τη μνήμη heap της JVM (`-Xmx2g`). |

## Συχνές ερωτήσεις

**Ε: Είναι το Aspose.CAD συμβατό με διαφορετικές μορφές αρχείων CAD;**  
Α: Ναι, υποστηρίζει πάνω από 30 μορφές CAD και raster, συμπεριλαμβανομένων DWG, DXF, DGN και SVG.

**Ε: Μπορώ να προσαρμόσω την ανάλυση της εξόδου raster εικόνας;**  
Α: Απολύτως. Προσαρμόστε τα `setPageWidth`, `setPageHeight` ή `setResolution` στο `CadRasterizationOptions` για να επιτύχετε το επιθυμητό DPI.

**Ε: Πώς μπορώ να μετατρέψω πολλαπλές διατάξεις CAD σε μία εκτέλεση;**  
Α: Παρέχετε έναν πίνακα με όλα τα ονόματα διατάξεων στο `setLayouts`, π.χ., `new String[]{"Model","Layout1","Layout2"}`.

**Ε: Υπάρχουν μορφές εξόδου εκτός του TIFF που υποστηρίζονται;**  
Α: Ναι—PNG, JPEG, BMP, PDF και άλλες είναι διαθέσιμες μέσω των αντίστοιχων κλάσεων `*Options`.

**Ε: Πού μπορώ να λάβω βοήθεια ή να μοιραστώ την εμπειρία μου με το Aspose.CAD;**  
Α: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη της κοινότητας και επίσημη βοήθεια.

## Συμπέρασμα

Ακολουθώντας αυτά τα βήματα μπορείτε να **convert DWG to PNG**, **export CAD as PNG**, **save CAD as JPEG**, ή να δημιουργήσετε οποιαδήποτε άλλη μορφή raster χρειάζεστε. Το Aspose.CAD for Java αναλαμβάνει το βαριά έργο, επιτρέποντάς σας να εστιάσετε στην ενσωμάτωση εικόνων υψηλής ποιότητας στις εφαρμογές, την τεκμηρίωση ή τις διαδικτυακές πύλες. Η υποστήριξη της βιβλιοθήκης για πάνω από 30 μορφές και η δυνατότητα απόδοσης σχεδίων με εκατοντάδες σελίδες χωρίς τη φόρτωση ολόκληρου του αρχείου στη μνήμη την καθιστούν μια ισχυρή επιλογή για CAD rasterization επιπέδου επιχείρησης.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  







```java
image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);
```

```bash
java -jar aspose-cad.jar -i input.dwg -o output.png -w 1200 -h 1200
```

## Σχετικά Μαθήματα

- [Γρήγορη Εξαγωγή DWG σε PDF ή Raster Χρησιμοποιώντας τη βιβλιοθήκη java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Μετατροπή DWG σε BMP με Aspose.CAD for Java](/cad/java/cad-export-options/export-to-bmp/)
- [Εξαγωγή DWG σε PDF: Συγκεκριμένη Διάταξη Χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}