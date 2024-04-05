---
title: Προσθήκη υδατογραφημάτων σε σχέδια CAD - Εκμάθηση Aspose.CAD για Java
linktitle: Προσθέστε υδατογράφημα
second_title: Aspose.CAD Java API
description: Βελτιώστε τα σχέδιά σας CAD με εξατομικευμένα υδατογραφήματα χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη ενσωμάτωση.
type: docs
weight: 12
url: /el/java/other-cad-operations/add-watermark/
---
## Εισαγωγή

Καλώς ήρθατε σε αυτόν τον περιεκτικό οδηγό για την προσθήκη υδατογραφημάτων σε σχέδια CAD χρησιμοποιώντας το Aspose.CAD για Java. Σε αυτό το σεμινάριο, θα μάθετε πώς να ενσωματώνετε αποτελεσματικά τα υδατογραφήματα, ενισχύοντας τα έγγραφά σας CAD με εξατομικευμένα μηνύματα ή επωνυμία. Το Aspose.CAD για Java παρέχει ένα ισχυρό σύνολο δυνατοτήτων, καθιστώντας τη διαδικασία προσθήκης υδατογραφήματος απλή.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD για Java: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD στο περιβάλλον Java σας. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/java/).
- Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκατεστημένη την πιο πρόσφατη έκδοση του JDK στο σύστημά σας.

## Εισαγωγή πακέτων

Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα Aspose.CAD για να ξεκινήσετε:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Βήμα 1: Προσθήκη νέου MTEXT

```java
//προσθήκη νέου MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

## Βήμα 2: Προσθέστε απλή οντότητα σαν κείμενο

Μπορείτε επίσης να προσθέσετε μια πιο απλή οντότητα όπως κείμενο:

```java
// ή προσθέστε πιο απλή οντότητα όπως το Κείμενο
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

## Βήμα 3: Εξαγωγή σε PDF

Εξάγετε το σχέδιο CAD με το προστιθέμενο υδατογράφημα σε ένα αρχείο PDF:

```java
// εξαγωγή σε pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## συμπέρασμα

Συγχαρητήρια! Προσθέσατε με επιτυχία υδατογραφήματα στα σχέδιά σας CAD χρησιμοποιώντας το Aspose.CAD για Java. Αυτή η απλή αλλά ισχυρή διαδικασία σάς επιτρέπει να εξατομικεύσετε τα σχέδιά σας ή να τα προστατεύσετε με την επωνυμία.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.CAD συμβατό με όλες τις μορφές αρχείων CAD;

A1: Το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF, DWT και DWF.

### Ε2: Μπορώ να προσαρμόσω την εμφάνιση του κειμένου του υδατογραφήματος;

A2: Ναι, έχετε τον πλήρη έλεγχο της εμφάνισης του υδατογραφήματος, συμπεριλαμβανομένου του μεγέθους κειμένου, του χρώματος και της θέσης.

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.CAD για Java;

 A3: Ναι, μπορείτε να κάνετε λήψη της δοκιμαστικής έκδοσης[εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;

 A4: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη.

### Ε5: Πού μπορώ να βρω την πλήρη τεκμηρίωση για το Aspose.CAD για Java;

 A5: Ανατρέξτε στο[τεκμηρίωση](https://reference.aspose.com/cad/java/) για αναλυτικές πληροφορίες.