---
date: 2025-12-10
description: Μάθετε πώς να μετατρέπετε CAD σε PDF χρησιμοποιώντας το Aspose.CAD για
  Java, ρυθμίζοντας το μέγεθος του καμβά, την αυτόματη κλιμάκωση διάταξης και εξάγοντας
  σε TIFF.
linktitle: Convert CAD to PDF – Set Canvas Size & Mode
second_title: Aspose.CAD Java API
title: Μετατροπή CAD σε PDF – Ορισμός Μεγέθους Καμβά & Λειτουργίας (Java)
url: /el/java/advanced-cad-features/set-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Καμβά και Λειτουργίας

## Εισαγωγή

Αναζητάτε να **convert CAD to PDF** ενώ έχετε πλήρη έλεγχο του μεγέθους του καμβά και της λειτουργίας απόδοσης; Αυτός ο ολοκληρωμένος οδηγός σας καθοδηγεί βήμα‑βήμα για τον ορισμό του μεγέθους του καμβά σε Java, την ενεργοποίηση της αυτόματης κλιμάκωσης διάταξης και, στη συνέχεια, την εξαγωγή του αποτελέσματος τόσο σε PDF όσο και σε TIFF χρησιμοποιώντας το Aspose.CAD. Είτε βελτιώνετε μια παραγωγική γραμμή είτε πειραματίζεστε με ένα πρωτότυπο, θα βρείτε σαφείς, εφαρμόσιμες οδηγίες εδώ.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “convert CAD to PDF”;** Μετατροπή ενός σχεδίου CAD (π.χ. DXF, DWG) σε έγγραφο PDF που μπορεί να προβληθεί σε οποιαδήποτε πλατφόρμα.  
- **Μπορώ επίσης να εξάγω σε TIFF;** Ναι—χρησιμοποιήστε `TiffOptions` για δημιουργία εικόνων raster υψηλής ανάλυσης.  
- **Ποια επιλογή ελέγχει το μέγεθος του καμβά σε Java;** `CadRasterizationOptions.setPageWidth/Height`.  
- **Τι είναι η αυτόματη κλιμάκωση διάταξης;** Μια σημαία (`setAutomaticLayoutsScaling(true)`) που διατηρεί τις αρχικές αναλογίες διάταξης όταν αλλάζει το μέγεθος του καμβά.  
- **Χρειάζομαι άδεια για το Aspose.CAD;** Απαιτείται προσωρινή ή μόνιμη άδεια για παραγωγική χρήση.

## Τι είναι **convert CAD to PDF**;

Η μετατροπή CAD σε PDF σημαίνει λήψη διανυσματικών σχεδίων μηχανικής και απόδοσή τους ως σελίδες PDF, διατηρώντας τις γραμμές, τα στρώματα και τη γεωμετρία, ενώ κάνει το αρχείο παγκοσμίως προσβάσιμο.

## Γιατί να ορίσετε το μέγεθος του καμβά **java**;

Ο ορισμός του μεγέθους του καμβά σε Java σας επιτρέπει να καθορίσετε την ανάλυση εξόδου και τις διαστάσεις της σελίδας, διασφαλίζοντας ότι το παραγόμενο PDF ή TIFF ταιριάζει στις απαιτήσεις εκτύπωσης ή προβολής. Παρέχει επίσης έλεγχο της συμπεριφοράς κλιμάκωσης, κάτι ουσιώδες για σχέδια μεγάλου φορμάτ.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Aspose.CAD for Java: Βεβαιωθείτε ότι η βιβλιοθήκη Aspose.CAD είναι εγκατεστημένη στο περιβάλλον Java. Μπορείτε να την κατεβάσετε [εδώ](https://releases.aspose.com/cad/java/).

- Document Directory: Δημιουργήστε έναν φάκελο εγγράφων για την αποθήκευση των αρχείων CAD. Αυτός ο φάκελος θα αναφέρεται στα βήματα του tutorial.

Τώρα, ας ξεκινήσουμε με τον οδηγό βήμα‑βήμα.

## Εισαγωγή Namespaces

Σε αυτό το βήμα, θα εισάγουμε τα απαραίτητα namespaces για να ξεκινήσετε το έργο Aspose.CAD.

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

Σε αυτό το απόσπασμα, ορίζουμε τη διαδρομή προς τον φάκελο πόρων και φορτώνουμε ένα αρχείο DXF χρησιμοποιώντας την κλάση `Image` του Aspose.CAD.

## Βήμα 2: Ορισμός Ιδιοτήτων **CadRasterizationOptions** (set canvas size java)

```java
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

Εδώ, δημιουργούμε μια παρουσία του `CadRasterizationOptions` και ρυθμίζουμε ιδιότητες όπως το πλάτος σελίδας, το ύψος σελίδας και την **automatic layout scaling**. Αυτό αποτελεί τον πυρήνα της **configure canvas mode** για τη μετατροπή σας.

## Βήμα 3: Δημιουργία PdfOptions και Ορισμός VectorRasterizationOptions

```java
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Set the VectorRasterizationOptions property
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Τώρα, δημιουργούμε μια παρουσία του `PdfOptions` και ορίζουμε την ιδιότητα `VectorRasterizationOptions` στην προηγουμένως διαμορφωμένη `CadRasterizationOptions`.

## Βήμα 4: Εξαγωγή σε PDF (convert cad to pdf)

```java
// Export CAD to PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο PDF χρησιμοποιώντας τις καθορισμένες επιλογές, ολοκληρώνοντας τη διαδικασία **convert CAD to PDF**.

## Βήμα 5: Δημιουργία TiffOptions και Ορισμός VectorRasterizationOptions (export cad to tiff)

```java
// Create an instance of TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Set the VectorRasterizationOptions property
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Σε αυτό το βήμα, δημιουργούμε μια παρουσία του `TiffOptions` και ρυθμίζουμε την ιδιότητα `VectorRasterizationOptions`.

## Βήμα 6: Εξαγωγή σε TIFF

```java
// Export CAD to TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο TIFF χρησιμοποιώντας τις καθορισμένες επιλογές, δείχνοντας πώς να **export CAD to TIFF** μετά τον ορισμό του μεγέθους του καμβά.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Το PDF εξόδου είναι κενό | `setNoScaling(true)` απενεργοποιεί την απόδοση για ορισμένα σχέδια | Αφαιρέστε `setNoScaling(true)` ή ορίστε το σε `false`. |
| Η ανάλυση του TIFF φαίνεται χαμηλή | Το πλάτος/ύψος σελίδας είναι πολύ μικρό | Αυξήστε τις τιμές `setPageWidth` / `setPageHeight`. |
| Η διάταξη φαίνεται παραμορφωμένη | Η αυτόματη κλιμάκωση διάταξης είναι απενεργοποιημένη | Βεβαιωθείτε ότι το `setAutomaticLayoutsScaling(true)` είναι ενεργοποιημένο. |

## Συμπέρασμα

Συγχαρητήρια! Έχετε ολοκληρώσει επιτυχώς τη **convert CAD to PDF** και την **export CAD to TIFF** ενώ **set canvas size java**, ενεργοποιώντας την **automatic layout scaling**, και μάθατε πώς να **configure canvas mode** για εξόδους υψηλής ποιότητας. Αυτό το tutorial παρέχει μια ισχυρή βάση για τα έργα μετατροπής CAD σας. Εξερευνήστε περισσότερες δυνατότητες και δυνατότητες στην [τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/java/).

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλα Java frameworks;

A1: Ναι, το Aspose.CAD έχει σχεδιαστεί ώστε να ενσωματώνεται απρόσκοπτα με διάφορα Java frameworks.

### Q2: Διατίθεται προσωρινή άδεια για το Aspose.CAD;

A2: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q3: Πού μπορώ να βρω υποστήριξη κοινότητας για το Aspose.CAD;

A3: Επισκεφθείτε το [φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για υποστήριξη και συζητήσεις.

### Q4: Μπορώ να δοκιμάσω το Aspose.CAD δωρεάν;

A4: Απόλυτα! Λάβετε δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q5: Πώς αγοράζω το Aspose.CAD for Java;

A5: Αγοράστε το προϊόν [εδώ](https://purchase.aspose.com/buy).

**Πρόσθετες Ερωτήσεις & Απαντήσεις**

**Ε: Επηρεάζει το μέγεθος του καμβά την ποιότητα του διανύσματος στο PDF;**  
Α: Όχι. Το μέγεθος του καμβά ελέγχει τις διαστάσεις της σελίδας· τα διανυσματικά δεδομένα παραμένουν ανεξάρτητα από την ανάλυση, εξασφαλίζοντας καθαρή απόδοση σε οποιοδήποτε επίπεδο ζουμ.

**Ε: Μπορώ να ορίσω διαφορετικό DPI για την έξοδο TIFF;**  
Α: Ναι. Ρυθμίστε `rasterizationOptions.setResolution(dpiValue)` πριν δημιουργήσετε το `TiffOptions`.

---

**Τελευταία Ενημέρωση:** 2025-12-10  
**Δοκιμασμένο Με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}