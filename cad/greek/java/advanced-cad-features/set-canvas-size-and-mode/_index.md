---
title: Ορίστε το μέγεθος και τη λειτουργία καμβά
linktitle: Ορίστε το μέγεθος και τη λειτουργία καμβά
second_title: Aspose.CAD Java API
description: Εξερευνήστε τη δύναμη του Aspose.CAD για Java με τον αναλυτικό οδηγό μας για τη ρύθμιση του μεγέθους και της λειτουργίας καμβά. Μετατρέψτε εύκολα αρχεία CAD σε μορφές PDF και TIFF.
type: docs
weight: 16
url: /el/java/advanced-cad-features/set-canvas-size-and-mode/
---
## Εισαγωγή

Θέλετε να αξιοποιήσετε τη δύναμη του Aspose.CAD για Java για να βελτιώσετε τη διαδικασία μετατροπής CAD; Αυτός ο περιεκτικός οδηγός θα σας καθοδηγήσει στα βήματα ρύθμισης του μεγέθους και της λειτουργίας καμβά χρησιμοποιώντας το Aspose.CAD για Java. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε, αυτός ο οδηγός θα σας παρέχει τις πληροφορίες που χρειάζεστε.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD για Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD στο περιβάλλον Java σας. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/java/).

- Κατάλογος εγγράφων: Ρυθμίστε έναν κατάλογο εγγράφων για να αποθηκεύσετε τα αρχεία CAD σας. Αυτός ο κατάλογος θα αναφέρεται στα βήματα εκμάθησης.

Τώρα, ας ξεκινήσουμε με τον οδηγό βήμα προς βήμα.

## Εισαγωγή χώρων ονομάτων

Σε αυτό το βήμα, θα εισαγάγουμε τους απαραίτητους χώρους ονομάτων για να ξεκινήσετε το έργο Aspose.CAD.
```java
import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;
```

## Βήμα 1: Εισαγωγή κλάσεων Aspose.CAD

```java
// Η διαδρομή προς τον κατάλογο πόρων.
String dataDir = "Your Document Directory" + "CADConversion/";

String srcFile = dataDir + "conic_pyramid.dxf";
com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
```

 Σε αυτό το απόσπασμα, ρυθμίζουμε τη διαδρομή προς τον κατάλογο πόρων και φορτώνουμε ένα αρχείο DXF χρησιμοποιώντας το Aspose.CAD's`Image` τάξη.

## Βήμα 2: Ορίστε τις ιδιότητες CadRasterizationOptions

```java
// Δημιουργήστε μια παρουσία του CadRasterizationOptions και ορίστε τις διάφορες ιδιότητές του
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);

rasterizationOptions.setAutomaticLayoutsScaling(true);
rasterizationOptions.setNoScaling(true);
```

 Εδώ, δημιουργούμε ένα παράδειγμα του`CadRasterizationOptions` και να διαμορφώσετε ιδιότητες όπως πλάτος σελίδας, ύψος σελίδας και επιλογές κλιμάκωσης.

## Βήμα 3: Δημιουργήστε PdfOptions και ορίστε VectorRasterizationOptions

```java
// Δημιουργήστε μια παρουσία του PdfOptions
PdfOptions pdfOptions = new PdfOptions();

// Ορίστε την ιδιότητα VectorRasterizationOptions
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

 Τώρα, δημιουργούμε ένα`PdfOptions` παράδειγμα και ορίστε το`VectorRasterizationOptions` ιδιοκτησία στην προηγουμένως διαμορφωμένη`CadRasterizationOptions`.

## Βήμα 4: Εξαγωγή σε PDF

```java
// Εξαγωγή CAD σε PDF
objImage.save(dataDir + "result_out_.pdf", pdfOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε αρχείο PDF χρησιμοποιώντας τις καθορισμένες επιλογές.

## Βήμα 5: Δημιουργήστε TiffOptions και ορίστε VectorRasterizationOptions

```java
// Δημιουργήστε μια παρουσία του TiffOptions
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

// Ορίστε την ιδιότητα VectorRasterizationOptions
tiffOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Σε αυτό το βήμα, δημιουργήσαμε ένα`TiffOptions` παράδειγμα και ρυθμίστε το`VectorRasterizationOptions` ιδιοκτησία.

## Βήμα 6: Εξαγωγή στο TIFF

```java
// Εξαγωγή CAD σε TIFF
objImage.save(dataDir + "result_out_.tiff", tiffOptions);
```

Τέλος, αποθηκεύουμε την εικόνα CAD σε ένα αρχείο TIFF χρησιμοποιώντας τις καθορισμένες επιλογές.

## συμπέρασμα

 Συγχαρητήρια! Έχετε ορίσει με επιτυχία το μέγεθος και τη λειτουργία του καμβά χρησιμοποιώντας το Aspose.CAD για Java. Αυτό το σεμινάριο παρέχει μια σταθερή βάση για τα έργα μετατροπής CAD. Εξερευνήστε περισσότερες δυνατότητες και δυνατότητες στο[Τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/java/).

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλα πλαίσια Java;

A1: Ναι, το Aspose.CAD έχει σχεδιαστεί για να ενσωματώνεται απρόσκοπτα με διάφορα πλαίσια Java.

### Ε2: Είναι διαθέσιμη μια προσωρινή άδεια χρήσης για το Aspose.CAD;

 A2: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε3: Πού μπορώ να λάβω υποστήριξη κοινότητας για το Aspose.CAD;

 A3: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και συζητήσεις.

### Ε4: Μπορώ να δοκιμάσω το Aspose.CAD δωρεάν;

 Α4: Απολύτως! Αποκτήστε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε5: Πώς μπορώ να αγοράσω Aspose.CAD για Java;

 A5: Αγοράστε το προϊόν[εδώ](https://purchase.aspose.com/buy).