---
title: Εξαγωγή DGN σε DWG με Aspose.CAD για Java
linktitle: Εξαγωγή DGN ως μέρος του DWG
second_title: Aspose.CAD Java API
description: Εξερευνήστε πώς να εξάγετε το DGN ως μέρος του DWG χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για αποτελεσματική διαχείριση αρχείων CAD.
type: docs
weight: 10
url: /el/java/dgn-export-options/export-dgn-as-part-of-dwg/
---
## Εισαγωγή

Σε αυτό το σεμινάριο, θα εξερευνήσουμε πώς να χρησιμοποιήσετε το Aspose.CAD για Java για την εξαγωγή ενός αρχείου DGN (Σχεδίαση MicroStation) ως μέρος ενός αρχείου DWG (Σχέδιο AutoCAD). Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που παρέχει ολοκληρωμένη λειτουργικότητα για εργασία με μορφές αρχείων CAD. Αυτός ο οδηγός βήμα προς βήμα θα σας βοηθήσει να κατανοήσετε τη διαδικασία εξαγωγής DGN ως μέρος του DWG χρησιμοποιώντας Java.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
1. Aspose.CAD Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.CAD για Java. Μπορείτε να βρείτε τη βιβλιοθήκη[εδώ](https://releases.aspose.com/cad/java/).
2. Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκαταστήσει Java στο σύστημά σας.
3. Ενσωματωμένο περιβάλλον ανάπτυξης (IDE): Επιλέξτε ένα Java IDE όπως το Eclipse ή το IntelliJ για μια πιο ομαλή εμπειρία ανάπτυξης.

## Εισαγωγή πακέτων

Στο έργο σας Java, εισαγάγετε τα απαραίτητα πακέτα Aspose.CAD για να ενεργοποιήσετε τη διαχείριση αρχείων CAD. Εδώ είναι ένα παράδειγμα:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Βήμα 1: Ορισμός Διαδρομών Αρχείων

 Καθορίστε τις διαδρομές αρχείου εισόδου και εξόδου για το αρχείο DWG. Ενημερώστε το`dataDir`, `fileName` , και`outPath` μεταβλητές αναλόγως.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Βήμα 2: Δημιουργία παρουσίας PdfOptions

 Δημιουργήστε ένα παράδειγμα του`PdfOptions` class, καθώς εξάγουμε το αρχείο DWG σε μορφή PDF.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Βήμα 3: Φορτώστε το αρχείο DWG

 Φορτώστε το υπάρχον αρχείο DWG ως εικόνα και μετατρέψτε το σε`CadImage` τύπος.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Βήμα 4: Επανάληψη μέσω οντοτήτων

Περάστε από κάθε οντότητα μέσα στο αρχείο DWG και ελέγξτε αν πρόκειται για ορισμό εικόνας. Εάν είναι, ανακτήστε την εξωτερική αναφορά στο αντικείμενο.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Βήμα 5: Ορίστε τις επιλογές ραστεροποίησης

 Ορίστε ρυθμίσεις για το`CadRasterizationOptions`αντικείμενο, συμπεριλαμβανομένου του πλάτους, του ύψους, των διατάξεων και του χρώματος φόντου σελίδας.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

## Βήμα 6: Ορίστε τις επιλογές διανυσματικής ραστεροποίησης

Ορίστε τις επιλογές διανυσματικής ραστεροποίησης για την εξαγωγή.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Βήμα 7: Εξαγωγή DWG σε PDF

 Τέλος, εξάγετε το DWG σε PDF καλώντας το`save` μέθοδος.

```java
cadImage.save(outPath, exportOptions);
```

## συμπέρασμα

Συγχαρητήρια! Μάθατε με επιτυχία πώς να εξάγετε ένα αρχείο DGN ως μέρος ενός αρχείου DWG χρησιμοποιώντας το Aspose.CAD για Java. Αυτή η ισχυρή βιβλιοθήκη παρέχει εκτεταμένες δυνατότητες για εργασία με αρχεία CAD, καθιστώντας τις εργασίες χειρισμού αρχείων CAD αποτελεσματικές και απλές.

## Συχνές ερωτήσεις

### Ε1: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.CAD για Java;

 A1: Μπορείτε να βρείτε την τεκμηρίωση[εδώ](https://reference.aspose.com/cad/java/).

### Ε2: Πώς μπορώ να κατεβάσω τη βιβλιοθήκη Aspose.CAD για Java;

 A2: Μπορείτε να κάνετε λήψη της βιβλιοθήκης από[αυτός ο σύνδεσμος](https://releases.aspose.com/cad/java/).

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.CAD για Java;

 A3: Ναι, μπορείτε να βρείτε τη δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε4: Πού μπορώ να λάβω μια προσωρινή άδεια χρήσης για το Aspose.CAD για Java;

 A4: Λάβετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;

 A5: Επισκεφθείτε το φόρουμ υποστήριξης κοινότητας Aspose.CAD[εδώ](https://forum.aspose.com/c/cad/19).