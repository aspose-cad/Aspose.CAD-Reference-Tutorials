---
title: Μετατροπή Java DGN σε JPEG με Εκμάθηση Aspose.CAD
linktitle: Εξαγωγή DGN σε μορφή AutoCAD σε μορφή εικόνας ράστερ
second_title: Aspose.CAD Java API
description: Μάθετε πώς να εξάγετε αρχεία DGN σε εικόνες JPEG σε Java χρησιμοποιώντας το Aspose.CAD. Αυτό το σεμινάριο βήμα προς βήμα σας καθοδηγεί στη διαδικασία χωρίς κόπο.
weight: 13
url: /el/java/dgn-export-options/exporting-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή Java DGN σε JPEG με Εκμάθηση Aspose.CAD

## Εισαγωγή

Καλώς ήρθατε σε αυτό το περιεκτικό σεμινάριο σχετικά με την εξαγωγή αρχείων DGN (Design) σε μορφή εικόνας Raster χρησιμοποιώντας το Aspose.CAD για Java. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές Java να εργάζονται με αρχεία CAD απρόσκοπτα. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία μετατροπής αρχείων DGN σε εικόνες JPEG, παρέχοντάς σας βήμα προς βήμα οδηγίες και παραδείγματα κώδικα.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
1.  Aspose.CAD Library: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD για Java. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει Java στον υπολογιστή σας.
3. Ενσωματωμένο περιβάλλον ανάπτυξης (IDE): Χρησιμοποιήστε ένα IDE συμβατό με Java όπως το IntelliJ ή το Eclipse.

## Εισαγωγή πακέτων

Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα για το Aspose.CAD. Προσθέστε τις ακόλουθες γραμμές στον κώδικά σας:

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

## Βήμα 1: Φόρτωση αρχείου DGN

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
DgnImage dgnImage = (DgnImage) Image.load(dataDir + "Nikon_D90_Camera.dgn");
```

## Βήμα 2: Δημιουργία αντικειμένου JpegOptions

```java
ImageOptionsBase options = new JpegOptions();
```

## Βήμα 3: Εκχώρηση Επιλογών Rasterization

```java
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(600);
vectorOptions.setPageHeight(400);
vectorOptions.setNoScaling(true);
vectorOptions.setAutomaticLayoutsScaling(false);
options.setVectorRasterizationOptions(vectorOptions);
```

## Βήμα 4: Αποθηκεύστε την εικόνα που έχει μετατραπεί

```java
OutputStream outStream = new FileOutputStream(dataDir + "ExportDGNToRasterImage_Out.jpg");
dgnImage.save(outStream, options);
```

Επαναλάβετε αυτά τα βήματα για τα συγκεκριμένα αρχεία DGN, προσαρμόζοντας ανάλογα τις διαδρομές αρχείων.

## συμπέρασμα

Συγχαρητήρια! Μάθατε με επιτυχία πώς να εξάγετε αρχεία DGN σε μορφή εικόνας ράστερ χρησιμοποιώντας το Aspose.CAD για Java. Αυτό το σεμινάριο σάς έχει εξοπλίσει με τη γνώση για να ενσωματώσετε αυτήν τη λειτουργικότητα στις εφαρμογές σας Java.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλες μορφές αρχείων CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, παρέχοντας μια ευέλικτη λύση για προγραμματιστές Java.

### Ε2: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.CAD για Java;

 A2: Ναι, μπορείτε να έχετε πρόσβαση σε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε3: Πού μπορώ να βρω τεκμηρίωση για το Aspose.CAD για Java;

 A3: Ανατρέξτε στην τεκμηρίωση[εδώ](https://reference.aspose.com/cad/java/).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;

 A4: Επισκεφθείτε το φόρουμ υποστήριξης[εδώ](https://forum.aspose.com/c/cad/19).

### Ε5: Πού μπορώ να αγοράσω άδεια χρήσης για το Aspose.CAD για Java;

 A5: Μπορείτε να αγοράσετε μια άδεια[εδώ](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
