---
title: Εύκολη εξαγωγή DGN σε AutoCAD PDF με Aspose.CAD για Java
linktitle: Εξαγωγή DGN σε μορφή AutoCAD σε PDF
second_title: Aspose.CAD Java API
description: Εξερευνήστε τον οδηγό βήμα προς βήμα για την εξαγωγή αρχείων DGN σε μορφή AutoCAD σε PDF χρησιμοποιώντας το Aspose.CAD για Java. Αυξήστε τις δυνατότητες χειρισμού CAD της εφαρμογής Java σας χωρίς κόπο.
type: docs
weight: 12
url: /el/java/dgn-export-options/exporting-dgn-to-pdf/
---
## Εισαγωγή

Καλώς ήρθατε σε αυτό το ολοκληρωμένο σεμινάριο σχετικά με τη χρήση του Aspose.CAD για Java για την εξαγωγή αρχείων DGN σε μορφή AutoCAD σε PDF. Αν θέλετε να βελτιώσετε την ικανότητα της εφαρμογής Java να χειρίζεται αρχεία CAD, το Aspose.CAD είναι μια εξαιρετική επιλογή. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία εξαγωγής αρχείων DGN βήμα προς βήμα.


## Προαπαιτούμενα
Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
-  Aspose.CAD Library: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD για Java. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/java/).
- Κατάλογος εγγράφων: Ρυθμίστε έναν κατάλογο εγγράφων όπου θα αποθηκεύονται τα αρχεία εισόδου και εξόδου.

## Εισαγωγή πακέτων

Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα για πρόσβαση στις λειτουργίες Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Τώρα, ας αναλύσουμε το παράδειγμα κώδικα σε πολλά βήματα:

## Βήμα 1: Καθορισμός Διαδρομών Αρχείων

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Βεβαιωθείτε ότι έχετε αντικαταστήσει τον "Κατάλογο εγγράφων σας" με την πραγματική διαδρομή όπου βρίσκονται τα αρχεία σας.

## Βήμα 2: Φόρτωση εικόνας DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Φορτώστε το αρχείο DGN χρησιμοποιώντας το Aspose.CAD.

## Βήμα 3: Ορίστε τις επιλογές εξαγωγής PDF

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Εξαγωγή συγκεκριμένων προβολών
options.setVectorRasterizationOptions(vectorOptions);
```

Καθορίστε τις επιλογές εξαγωγής PDF, συμπεριλαμβανομένων των διαστάσεων σελίδας και των προτιμήσεων διάταξης.

## Βήμα 4: Αποθήκευση αρχείου PDF

```java
objImage.save(outFile, options);
```

Αποθηκεύστε το εξαγόμενο αρχείο PDF.

Επαναλάβετε αυτά τα βήματα για τυχόν επιπλέον αρχεία DGN που θέλετε να μετατρέψετε. Συγχαρητήρια! Εξάγατε με επιτυχία αρχεία DGN σε μορφή AutoCAD σε PDF χρησιμοποιώντας το Aspose.CAD για Java.

## συμπέρασμα

Σε αυτό το σεμινάριο, εξερευνήσαμε πώς να αξιοποιήσετε το Aspose.CAD για Java για να βελτιώσετε τις δυνατότητες διαχείρισης αρχείων CAD της εφαρμογής σας. Με απλά βήματα και παραδείγματα κώδικα, μπορείτε τώρα να εξάγετε απρόσκοπτα αρχεία DGN σε μορφή AutoCAD σε PDF.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.CAD συμβατό με όλες τις μορφές αρχείων CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει ένα ευρύ φάσμα μορφών CAD, διασφαλίζοντας ευελιξία στο χειρισμό διαφόρων τύπων αρχείων.

### Ε2: Μπορώ να προσαρμόσω τις ρυθμίσεις εξαγωγής PDF;

Α2: Απολύτως. Όπως φαίνεται στο σεμινάριο, μπορείτε να προσαρμόσετε επιλογές, όπως τις διαστάσεις και τις διατάξεις σελίδας, ώστε να ταιριάζουν στις απαιτήσεις σας.

### Ε3: Πού μπορώ να βρω πρόσθετη υποστήριξη ή βοήθεια;

 A3: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και συζητήσεις.

### Ε4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A4: Ναι, μπορείτε να έχετε πρόσβαση στη δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε5: Πώς μπορώ να αποκτήσω προσωρινή άδεια;

 A5: Πάρτε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).