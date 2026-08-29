---
date: 2026-08-29
description: Μάθετε πώς να ορίσετε το μέγεθος σελίδας pdf και να μετατρέψετε CAD σε
  PDF χρησιμοποιώντας το Aspose.CAD για Java, με automatic layout scaling και TIFF
  export.
keywords:
- set pdf page size
- convert cad to pdf
- canvas size java
- high resolution tiff
- change pdf dimensions
lastmod: 2026-08-29
linktitle: Ορισμός μεγέθους σελίδας pdf – μετατροπή cad σε pdf
og_description: Μάθετε πώς να ορίσετε το μέγεθος σελίδας pdf κατά τη μετατροπή σχεδίων
  CAD σε PDF σε Java χρησιμοποιώντας το Aspose.CAD. Αυτός ο οδηγός καλύπτει canvas
  dimensions, automatic layout scaling και εξαγωγή σε high‑resolution TIFF.
og_image_alt: Tutorial showing how to set pdf page size and convert CAD to PDF in
  Java
og_title: Ορισμός μεγέθους σελίδας pdf – μετατροπή CAD σε PDF με Aspose σε Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set pdf page size and convert CAD to PDF using Aspose.CAD
    for Java, with automatic layout scaling and TIFF export.
  headline: Set pdf page size – convert cad to pdf (Java)
  type: TechArticle
- questions:
  - answer: No. Canvas size controls page dimensions; vector data remains resolution‑independent,
      ensuring crisp rendering at any zoom level.
    question: does the canvas size affect vector quality in the PDF?
  - answer: Yes. Adjust `rasterizationOptions.setResolution(dpiValue)` before creating
      `TiffOptions`.
    question: can I set a different DPI for the TIFF output?
  - answer: Use Aspose.PDF to load the generated PDF and call `pdf.getPages().setPageSize(PageSize.A4)`
      or a custom size.
    question: how can I change PDF dimensions for an existing PDF without re‑rendering
      the CAD?
  - answer: Keep `setAutomaticLayoutsScaling(true)` and avoid `setNoScaling(true)`;
      this retains layer visibility and layout fidelity.
    question: what is the best way to convert dxf to pdf while preserving layers?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- set pdf page size
- convert cad
- Aspose.CAD
- Java
- high resolution tiff
title: Ορισμός μεγέθους σελίδας pdf – μετατροπή cad σε pdf (Java)
url: /el/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός μεγέθους σελίδας pdf – μετατροπή CAD σε pdf (Java)

## Εισαγωγή

Αν χρειάζεστε να **ορίσετε το μέγεθος σελίδας pdf** κατά τη μετατροπή σχεδίων CAD σε PDF, βρίσκεστε στο σωστό μέρος. Σε αυτό το μάθημα θα σας δείξουμε πώς να χρησιμοποιήσετε το Aspose.CAD για Java για να ορίσετε ακριβείς διαστάσεις καμβά, να ενεργοποιήσετε την αυτόματη κλιμάκωση διάταξης και στη συνέχεια να εξάγετε το αποτέλεσμα τόσο σε PDF όσο και σε TIFF. Είτε προετοιμάζετε τεχνικά σχήματα για εκτύπωση είτε δημιουργείτε μικρογραφίες για μια διαδικτυακή γκαλερί, ο έλεγχος του μεγέθους της σελίδας και της ανάλυσης εξόδου είναι ουσιώδης.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “μετατροπή CAD σε PDF”;** Μετατροπή ενός σχεδίου CAD (π.χ., DXF, DWG) σε έγγραφο PDF που μπορεί να προβληθεί σε οποιαδήποτε πλατφόρμα.  
- **Μπορώ επίσης να εξάγω σε TIFF;** Ναι—χρησιμοποιήστε `TiffOptions` για δημιουργία εικόνων raster υψηλής ανάλυσης.  
- **Ποια επιλογή ελέγχει το μέγεθος του καμβά σε Java;** `CadRasterizationOptions.setPageWidth/Height`.  
- **Τι είναι η αυτόματη κλιμάκωση διάταξης;** Μία σημαία (`setAutomaticLayoutsScaling(true)`) που διατηρεί τις αρχικές αναλογίες διάταξης όταν αλλάζει το μέγεθος του καμβά.  
- **Χρειάζομαι άδεια για το Aspose.CAD;** Απαιτείται προσωρινή ή μόνιμη άδεια για χρήση σε παραγωγή.

## Πώς να ορίσετε το μέγεθος σελίδας pdf κατά τη μετατροπή CAD σε PDF σε Java

Φορτώστε το αρχείο CAD, διαμορφώστε το `CadRasterizationOptions` με το επιθυμητό πλάτος και ύψος, ενεργοποιήστε την αυτόματη κλιμάκωση διάταξης και, στη συνέχεια, αποθηκεύστε το αποτέλεσμα ως PDF. Αυτή η προσέγγιση δύο βημάτων σας επιτρέπει να ελέγχετε τις ακριβείς διαστάσεις της σελίδας εξόδου χωρίς να θυσιάζετε την ποιότητα του διανύσματος.

## Τι είναι η μετατροπή CAD σε PDF;

Η μετατροπή CAD σε PDF σημαίνει λήψη διανυσματικών τεχνικών σχεδίων και απόδοση τους ως σελίδες PDF, διατηρώντας τις γραμμές, τα επίπεδα και τη γεωμετρία, ενώ το αρχείο γίνεται καθολικά προσβάσιμο. Η διαδικασία rasterizes το σχέδιο σύμφωνα με τις καθορισμένες επιλογές, παράγοντας ένα PDF που μπορεί να ανοιχθεί σε οποιαδήποτε συσκευή χωρίς να απαιτείται λογισμικό CAD, και διατηρεί την οπτική πιστότητα του αρχικού σχεδίου.

## Γιατί να ορίσετε το μέγεθος καμβά σε Java;

Ο ορισμός του μεγέθους του καμβά σε Java σας επιτρέπει να ορίσετε την ανάλυση εξόδου και τις διαστάσεις της σελίδας, διασφαλίζοντας ότι το παραγόμενο PDF ή TIFF ταιριάζει με τις απαιτήσεις εκτύπωσης ή προβολής σας. Επίσης, σας δίνει έλεγχο στη συμπεριφορά κλιμάκωσης, κάτι που είναι απαραίτητο για σχέδια μεγάλου φορμάτ.

## Προαπαιτούμενα

Πριν ξεκινήσετε το μάθημα, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- Aspose.CAD for Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD στο περιβάλλον Java. Μπορείτε να κατεβάσετε τη βιβλιοθήκη Aspose.CAD for Java [εδώ](https://releases.aspose.com/cad/java/).
- Φάκελος εγγράφων: Δημιουργήστε έναν φάκελο εγγράφων για την αποθήκευση των αρχείων CAD. Αυτός ο φάκελος θα αναφέρεται στα βήματα του μαθήματος.

Τώρα, ας ξεκινήσουμε με τον οδηγό βήμα‑βήμα.

## Εισαγωγή χώρων ονομάτων

Σε αυτό το βήμα, θα εισάγουμε τους απαραίτητους χώρους ονομάτων για να ξεκινήσετε το έργο Aspose.CAD.

`Image` είναι η κύρια κλάση που χρησιμοποιείται για τη φόρτωση αρχείων CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Βήμα 1: εισαγωγή κλάσεων Aspose.CAD

Η κλάση `Image` παρέχει μεθόδους για τη φόρτωση και αποθήκευση σχεδίων CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Σε αυτό το απόσπασμα, ορίζουμε τη διαδρομή προς το φάκελο πόρων και φορτώνουμε ένα αρχείο DXF χρησιμοποιώντας την κλάση `Image` του Aspose.CAD.

## Βήμα 2: ορισμός ιδιοτήτων CadRasterizationOptions (ορισμός μεγέθους καμβά σε Java)

`CadRasterizationOptions` καθορίζει ρυθμίσεις rasterization όπως το μέγεθος σελίδας και η κλιμάκωση για τη μετατροπή CAD‑σε‑raster.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Εδώ, δημιουργούμε μια παρουσία του `CadRasterizationOptions` και διαμορφώνουμε ιδιότητες όπως το πλάτος σελίδας, το ύψος σελίδας και **την αυτόματη κλιμάκωση διάταξης**. Αυτό αποτελεί τον πυρήνα της **διαμόρφωσης λειτουργίας καμβά** για τη μετατροπή σας.

## Βήμα 3: δημιουργία PdfOptions και ορισμός vectorRasterizationOptions

`PdfOptions` ορίζει τις ρυθμίσεις εξόδου PDF για τη μετατροπή.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Τώρα, δημιουργούμε μια παρουσία του `PdfOptions` και ορίζουμε την ιδιότητα `VectorRasterizationOptions` της σε προηγουμένως διαμορφωμένο `CadRasterizationOptions`.

## Βήμα 4: εξαγωγή σε PDF (μετατροπή CAD σε PDF)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο PDF χρησιμοποιώντας τις καθορισμένες επιλογές, ολοκληρώνοντας τη διαδικασία **μετατροπής CAD σε PDF**.

## Βήμα 5: δημιουργία TiffOptions και ορισμός vectorRasterizationOptions (εξαγωγή CAD σε TIFF)

`TiffOptions` διαμορφώνει τις παραμέτρους εξόδου TIFF όπως συμπίεση και ανάλυση.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Σε αυτό το βήμα, δημιουργούμε μια παρουσία του `TiffOptions` και διαμορφώνουμε την ιδιότητα `VectorRasterizationOptions` του.

## Βήμα 6: εξαγωγή σε TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο TIFF χρησιμοποιώντας τις καθορισμένες επιλογές, δείχνοντας πώς να **εξάγετε CAD σε TIFF** μετά τη διαμόρφωση του μεγέθους καμβά.

## Κοινά προβλήματα και λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Το PDF εξόδου είναι κενό | `setNoScaling(true)` απενεργοποιεί την απόδοση για ορισμένα σχέδια | Αφαιρέστε το `setNoScaling(true)` ή ορίστε το σε `false`. |
| Η ανάλυση του TIFF φαίνεται χαμηλή | Το πλάτος/ύψος σελίδας είναι πολύ μικρό | Αυξήστε τις τιμές `setPageWidth` / `setPageHeight`. |
| Η διάταξη φαίνεται παραμορφωμένη | Η αυτόματη κλιμάκωση διάταξης είναι απενεργοποιημένη | Βεβαιωθείτε ότι το `setAutomaticLayoutsScaling(true)` είναι ενεργοποιημένο. |

## Γιατί να προσαρμόσετε το μέγεθος καμβά και DPI;

Η αλλαγή του μεγέθους του καμβά επηρεάζει άμεσα την ανάλυση raster του αποτελέσματος. Εάν χρειάζεται να **αυξήσετε την ανάλυση του TIFF**, απλώς αυξήστε τις τιμές `setPageWidth` / `setPageHeight` ή καλέστε `rasterizationOptions.setResolution(300)` πριν δημιουργήσετε το `TiffOptions`. Αυτό σας παρέχει εικόνες raster υψηλής ποιότητας κατάλληλες για εκτύπωση ή λεπτομερή επιθεώρηση.

## Συχνές ερωτήσεις

**Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλα πλαίσια Java;**  
A: Ναι, το Aspose.CAD σχεδιάστηκε για να ενσωματώνεται άψογα με διάφορα πλαίσια Java.

**Q2: Υπάρχει διαθέσιμη προσωρινή άδεια για το Aspose.CAD;**  
A: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια στη σελίδα [εδώ](https://purchase.aspose.com/temporary-license/).

**Q3: Πού μπορώ να λάβω υποστήριξη από την κοινότητα για το Aspose.CAD;**  
A: Επισκεφθείτε το φόρουμ Aspose.CAD [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη και συζητήσεις.

**Q4: Μπορώ να δοκιμάσω το Aspose.CAD δωρεάν;**  
A: Απολύτως! Λάβετε τη σελίδα δωρεάν δοκιμής [εδώ](https://releases.aspose.com/).

**Q5: Πώς μπορώ να αγοράσω το Aspose.CAD για Java;**  
A: Αγοράστε το Aspose.CAD για Java [εδώ](https://purchase.aspose.com/buy).

**Q: Επηρεάζει το μέγεθος του καμβά την ποιότητα του διανύσματος στο PDF;**  
A: Όχι. Το μέγεθος του καμβά ελέγχει τις διαστάσεις της σελίδας· τα διανυσματικά δεδομένα παραμένουν ανεξάρτητα από την ανάλυση, εξασφαλίζοντας καθαρή απόδοση σε οποιοδήποτε επίπεδο ζουμ.

**Q: Μπορώ να ορίσω διαφορετικό DPI για την έξοδο TIFF;**  
A: Ναι. Ρυθμίστε `rasterizationOptions.setResolution(dpiValue)` πριν δημιουργήσετε το `TiffOptions`.

**Q: Πώς μπορώ να αλλάξω τις διαστάσεις PDF για ένα υπάρχον PDF χωρίς επαναδημιουργία του CAD;**  
A: Χρησιμοποιήστε το Aspose.PDF για να φορτώσετε το παραγόμενο PDF και καλέστε `pdf.getPages().setPageSize(PageSize.A4)` ή προσαρμοσμένο μέγεθος.

**Q: Ποιος είναι ο καλύτερος τρόπος για να μετατρέψετε dxf σε pdf διατηρώντας τα επίπεδα;**  
A: Διατηρήστε `setAutomaticLayoutsScaling(true)` και αποφύγετε το `setNoScaling(true)`· αυτό διατηρεί την ορατότητα των επιπέδων και την ακεραιότητα της διάταξης.

## Συμπέρασμα

Συγχαρητήρια! Έχετε ολοκληρώσει με επιτυχία τη **μετατροπή CAD σε PDF** και την **εξαγωγή CAD σε TIFF** ενώ **ορίσατε το μέγεθος καμβά σε Java**, ενεργοποιώντας την **αυτόματη κλιμάκωση διάταξης** και μαθαίνοντας πώς να **διαμορφώσετε τη λειτουργία καμβά** για εξόδους υψηλής ποιότητας. Αυτό το μάθημα παρέχει μια σταθερή βάση για τα έργα μετατροπής CAD σας. Εξερευνήστε περισσότερες δυνατότητες και δυνατότητες στην [τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Τελευταία ενημέρωση:** 2026-08-29  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Ορισμός Μεγέθους Καμβά – Προηγμένες Λειτουργίες CAD με Aspose.CAD για Java](/cad/java/advanced-cad-features/)
- [Εξαγωγή DWG σε PDF σε Java – Ορισμός Μεγέθους Σελίδας PDF με Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Ορισμός Προσαρμοσμένου Μεγέθους Σελίδας – PDF από CAD με Αυτόματη Κλιμάκωση Διάταξης](/cad/java/advanced-cad-features/setting-auto-layout-scaling/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}