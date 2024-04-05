---
title: Εξαγωγή ενσωματωμένου DGN σε PDF με το Aspose.CAD για Java
linktitle: Εξαγωγή ενσωματωμένου DGN
second_title: Aspose.CAD Java API
description: Εξερευνήστε τον οδηγό βήμα προς βήμα για την εξαγωγή ενσωματωμένων αρχείων DGN σε PDF χρησιμοποιώντας το Aspose.CAD για Java. Βελτιώστε τις εφαρμογές σας Java με απρόσκοπτη διαχείριση αρχείων CAD.
type: docs
weight: 11
url: /el/java/dgn-export-options/export-embedded-dgn/
---
## Εισαγωγή

Καλώς ήρθατε σε αυτό το περιεκτικό σεμινάριο εξαγωγής ενσωματωμένων αρχείων DGN χρησιμοποιώντας το Aspose.CAD για Java. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές Java να εργάζονται με αρχεία CAD απρόσκοπτα. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία εξαγωγής ενσωματωμένων αρχείων DGN σε PDF χρησιμοποιώντας οδηγίες βήμα προς βήμα. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε, αυτό το σεμινάριο θα σας βοηθήσει να αξιοποιήσετε τις δυνατότητες του Aspose.CAD για να βελτιώσετε τις εφαρμογές σας Java.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
- Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα περιβάλλον ανάπτυξης Java στον υπολογιστή σας.
-  Aspose.CAD για Java: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD για Java από[εδώ](https://releases.aspose.com/cad/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, πρέπει να εισαγάγετε τα απαραίτητα πακέτα στο έργο σας Java. Προσθέστε τις ακόλουθες δηλώσεις εισαγωγής στον κώδικά σας:

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

Τώρα, ας αναλύσουμε το παράδειγμα κώδικα σε πολλά βήματα:

## Βήμα 1: Ρύθμιση Διαδρομών Εισόδου και Εξόδου

Καθορίστε τη διαδρομή καταλόγου όπου βρίσκεται το έγγραφό σας και καθορίστε το όνομα αρχείου εισόδου DWG.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

## Βήμα 2: Φορτώστε το αρχείο DWG

 Φορτώστε το αρχείο DWG σε ένα`Image` αντικείμενο χρησιμοποιώντας Aspose.CAD.

```java
Image objImage = Image.load(fileName);
```

## Βήμα 3: Διαμορφώστε τις επιλογές Rasterization

Διαμορφώστε τις επιλογές ραστεροποίησης, όπως διατάξεις που θα συμπεριληφθούν στην εξαγωγή.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

## Βήμα 4: Διαμόρφωση επιλογών PDF

Ρυθμίστε τις επιλογές PDF, συμπεριλαμβανομένων των διανυσματικών επιλογών ραστεροποίησης.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Βήμα 5: Αποθήκευση αρχείου PDF

Αποθηκεύστε το αρχείο PDF με τις διαμορφωμένες επιλογές.
```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## συμπέρασμα

Συγχαρητήρια! Εξάγατε με επιτυχία ένα ενσωματωμένο αρχείο DGN σε PDF χρησιμοποιώντας το Aspose.CAD για Java. Αυτό το σεμινάριο κάλυψε τα βασικά βήματα για την ενσωμάτωση του Aspose.CAD στην εφαρμογή Java για αποτελεσματικό χειρισμό αρχείων CAD.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java σε ένα εμπορικό έργο;

 A1: Ναι, το Aspose.CAD για Java είναι μια εμπορική βιβλιοθήκη. Μπορείτε να αποκτήσετε άδεια από[εδώ](https://purchase.aspose.com/buy).

### Ε2: Υπάρχει δωρεάν δοκιμή διαθέσιμη;

 A2: Ναι, μπορείτε να έχετε πρόσβαση σε μια δωρεάν δοκιμή του Aspose.CAD για Java[εδώ](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;

A3: Μπορείτε να αναζητήσετε υποστήριξη από την κοινότητα Aspose.CAD στο[δικαστήριο](https://forum.aspose.com/c/cad/19).

### Ε4: Τι γίνεται αν χρειάζομαι μια προσωρινή άδεια;

 A4: Μπορείτε να αποκτήσετε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να βρω την τεκμηρίωση;

 A5: Η τεκμηρίωση είναι διαθέσιμη[εδώ](https://reference.aspose.com/cad/java/).