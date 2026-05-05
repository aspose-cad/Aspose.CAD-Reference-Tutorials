---
date: 2026-02-15
description: Μάθετε πώς να ορίζετε το μέγεθος της σελίδας PDF και να μετατρέπετε CAD
  σε PDF χρησιμοποιώντας το Aspose.CAD για Java, με αυτόματη κλιμάκωση της διάταξης
  και εξαγωγή σε TIFF.
linktitle: Set PDF Page Size – Convert CAD to PDF
second_title: Aspose.CAD Java API
title: Ορισμός μεγέθους σελίδας PDF – Μετατροπή CAD σε PDF (Java)
url: /el/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

.

Let's construct final output.{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Καμβά και Λειτουργίας

## Εισαγωγή

Αν χρειάζεστε να **ορίσετε το μέγεθος σελίδας PDF** κατά τη μετατροπή σχεδίων CAD σε PDF, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα σας δείξουμε πώς να χρησιμοποιήσετε το Aspose.CAD for Java για να ορίσετε ακριβείς διαστάσεις καμβά, να ενεργοποιήσετε την αυτόματη κλιμάκωση διάταξης και στη συνέχεια να εξάγετε το αποτέλεσμα τόσο σε PDF όσο και σε TIFF. Είτε προετοιμάζετε τεχνικά σχήματα για εκτύπωση είτε δημιουργείτε μικρογραφίες για μια διαδικτυακή γκαλερί, ο έλεγχος του μεγέθους σελίδας και της ανάλυσης εξόδου είναι απαραίτητος.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “convert CAD to PDF”;** Η μετατροπή ενός σχεδίου CAD (π.χ., DXF, DWG) σε έγγραφο PDF που μπορεί να προβληθεί σε οποιαδήποτε πλατφόρμα.  
- **Μπορώ επίσης να εξάγω σε TIFF;** Ναι—χρησιμοποιήστε `TiffOptions` για τη δημιουργία raster εικόνων υψηλής ανάλυσης.  
- **Ποια επιλογή ελέγχει το μέγεθος του καμβά σε Java;** `CadRasterizationOptions.setPageWidth/Height`.  
- **Τι είναι η αυτόματη κλιμάκωση διάταξης;** Μια σημαία (`setAutomaticLayoutsScaling(true)`) που διατηρεί τις αρχικές αναλογίες διάταξης όταν αλλάζει το μέγεθος του καμβά.  
- **Χρειάζομαι άδεια για το Aspose.CAD;** Απαιτείται προσωρινή ή μόνιμη άδεια για χρήση σε παραγωγή.

## Πώς να Ορίσετε το Μέγεθος Σελίδας PDF Κατά τη Μετατροπή CAD σε PDF (Java)

Ο ορισμός του μεγέθους σελίδας PDF (ή του μεγέθους καμβά) σας επιτρέπει να καθορίσετε τις τελικές διαστάσεις του εγγράφου, κάτι που είναι ιδιαίτερα χρήσιμο όταν πρέπει να **αλλάξετε τις διαστάσεις PDF** ώστε να ταιριάζουν με τα πρότυπα εκτύπωσης ή τις απαιτήσεις UI. Παρακάτω περπατάμε βήμα προς βήμα, εξηγώντας το *γιατί* πίσω από κάθε γραμμή κώδικα.

## Τι είναι το **convert CAD to PDF**;

Η μετατροπή CAD σε PDF σημαίνει τη λήψη διανυσματικών τεχνικών σχεδίων και την απόδοσή τους ως σελίδες PDF, διατηρώντας τις γραμμές, τα στρώματα και τη γεωμετρία, ενώ το αρχείο γίνεται καθολικά προσβάσιμο.

## Γιατί να ορίσετε το μέγεθος του καμβά **java**;

Ο ορισμός του μεγέθους του καμβά σε Java σας επιτρέπει να ορίσετε την ανάλυση εξόδου και τις διαστάσεις της σελίδας, διασφαλίζοντας ότι το παραγόμενο PDF ή TIFF ταιριάζει με τις απαιτήσεις εκτύπωσης ή προβολής σας. Σας δίνει επίσης έλεγχο στη συμπεριφορά κλιμάκωσης, κάτι που είναι απαραίτητο για σχέδια μεγάλου φορμάτ.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- Aspose.CAD for Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD στο περιβάλλον Java σας. Μπορείτε να την κατεβάσετε [εδώ](https://releases.aspose.com/cad/java/).
- Κατάλογος Εγγράφων: Δημιουργήστε έναν κατάλογο εγγράφων για την αποθήκευση των αρχείων CAD σας. Αυτός ο κατάλογος θα αναφέρεται στα βήματα του tutorial.

Τώρα, ας ξεκινήσουμε με τον οδηγό βήμα‑βήμα.

## Εισαγωγή Namespaces

Σε αυτό το βήμα, θα εισάγουμε τα απαραίτητα namespaces για να ξεκινήσετε το έργο σας με το Aspose.CAD.

```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Βήμα 1: Εισαγωγή Κλάσεων Aspose.CAD

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

Σε αυτό το απόσπασμα, ορίζουμε τη διαδρομή προς τον κατάλογο πόρων και φορτώνουμε ένα αρχείο DXF χρησιμοποιώντας την κλάση `Image` του Aspose.CAD.

## Βήμα 2: Ορισμός Ιδιοτήτων **CadRasterizationOptions** (set canvas size java)

Εδώ, δημιουργούμε μια παρουσία της `CadRasterizationOptions` και ρυθμίζουμε ιδιότητες όπως το πλάτος σελίδας, το ύψος σελίδας και την **αυτόματη κλιμάκωση διάταξης**. Αυτό αποτελεί τον πυρήνα του **configure canvas mode** για τη μετατροπή σας.

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

## Βήμα 3: Δημιουργία PdfOptions και Ορισμός VectorRasterizationOptions

Τώρα, δημιουργούμε μια παρουσία `PdfOptions` και ορίζουμε την ιδιότητα `VectorRasterizationOptions` της σε αυτήν που διαμορφώσαμε προηγουμένως, `CadRasterizationOptions`.

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Βήμα 4: Εξαγωγή σε PDF (convert cad to pdf)

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο PDF χρησιμοποιώντας τις καθορισμένες επιλογές, ολοκληρώνοντας τη διαδικασία **convert CAD to PDF**.

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

## Βήμα 5: Δημιουργία TiffOptions και Ορισμός VectorRasterizationOptions (export cad to tiff)

Σε αυτό το βήμα, δημιουργούμε μια παρουσία `TiffOptions` και διαμορφώνουμε την ιδιότητα `VectorRasterizationOptions` της.

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Βήμα 6: Εξαγωγή σε TIFF

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο TIFF χρησιμοποιώντας τις καθορισμένες επιλογές, δείχνοντας πώς να **export CAD to TIFF** μετά τον ορισμό του μεγέθους καμβά.

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Το PDF εξόδου είναι κενό | `setNoScaling(true)` απενεργοποιεί την απόδοση για ορισμένα σχέδια | Αφαιρέστε το `setNoScaling(true)` ή ορίστε το σε `false`. |
| Η ανάλυση του TIFF φαίνεται χαμηλή | Το πλάτος/ύψος σελίδας είναι πολύ μικρό | Αυξήστε τις τιμές `setPageWidth` / `setPageHeight`. |
| Η διάταξη φαίνεται παραμορφωμένη | Η αυτόματη κλιμάκωση διάταξης είναι απενεργοποιημένη | Βεβαιωθείτε ότι το `setAutomaticLayoutsScaling(true)` είναι ενεργοποιημένο. |

## Γιατί να Ρυθμίσετε το Μέγεθος Καμβά και DPI;

Η αλλαγή του μεγέθους του καμβά επηρεάζει άμεσα την ανάλυση raster του αποτελέσματος. Εάν χρειάζεται να **αυξήσετε την ανάλυση TIFF**, απλώς αυξήστε τις τιμές `setPageWidth` / `setPageHeight` ή καλέστε `rasterizationOptions.setResolution(300)` πριν δημιουργήσετε το `TiffOptions`. Αυτό σας παρέχει raster εικόνες υψηλής ποιότητας κατάλληλες για εκτύπωση ή λεπτομερή επιθεώρηση.

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλα Java frameworks;

Ναι, το Aspose.CAD έχει σχεδιαστεί ώστε να ενσωματώνεται άψογα με διάφορα Java frameworks.

### Q2: Υπάρχει διαθέσιμη προσωρινή άδεια για το Aspose.CAD;

Ναι, μπορείτε να αποκτήσετε μια προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q3: Πού μπορώ να λάβω υποστήριξη από την κοινότητα για το Aspose.CAD;

Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη και συζητήσεις από την κοινότητα.

### Q4: Μπορώ να δοκιμάσω το Aspose.CAD δωρεάν;

Απολύτως! Λάβετε μια δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q5: Πώς μπορώ να αγοράσω το Aspose.CAD for Java;

Αγοράστε το προϊόν [εδώ](https://purchase.aspose.com/buy).

**Additional Q&A**

**Q: Επηρεάζει το μέγεθος του καμβά την ποιότητα του διανύσματος στο PDF;**  
A: Όχι. Το μέγεθος του καμβά ελέγχει τις διαστάσεις της σελίδας· τα διανυσματικά δεδομένα παραμένουν ανεξάρτητα από την ανάλυση, εξασφαλίζοντας καθαρή απόδοση σε οποιοδήποτε επίπεδο ζουμ.

**Q: Μπορώ να ορίσω διαφορετικό DPI για την έξοδο TIFF;**  
A: Ναι. Προσαρμόστε το `rasterizationOptions.setResolution(dpiValue)` πριν δημιουργήσετε το `TiffOptions`.

**Q: Πώς μπορώ να **αλλάξω τις διαστάσεις PDF** για ένα υπάρχον PDF χωρίς επαναδημιουργία του CAD;**  
A: Χρησιμοποιήστε το Aspose.PDF για να φορτώσετε το παραγόμενο PDF και καλέστε `pdf.getPages().setPageSize(PageSize.A4)` ή ένα προσαρμοσμένο μέγεθος.

**Q: Ποιος είναι ο καλύτερος τρόπος για **convert dxf to pdf** διατηρώντας τα στρώματα;**  
A: Διατηρήστε το `setAutomaticLayoutsScaling(true)` και αποφύγετε το `setNoScaling(true)`· αυτό διατηρεί την ορατότητα των στρωμάτων και την ακρίβεια της διάταξης.

## Συμπέρασμα

Συγχαρητήρια! Έχετε ολοκληρώσει με επιτυχία τη **convert CAD to PDF** και την **export CAD to TIFF** ενώ **set canvas size java**, ενεργοποιώντας την **automatic layout scaling** και μαθαίνοντας πώς να **configure canvas mode** για εξόδους υψηλής ποιότητας. Αυτό το tutorial παρέχει μια ισχυρή βάση για τα έργα μετατροπής CAD σας. Εξερευνήστε περισσότερες δυνατότητες και επιλογές στην [τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/java/).

---

**Τελευταία Ενημέρωση:** 2026-02-15  
**Δοκιμάστηκε Με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}