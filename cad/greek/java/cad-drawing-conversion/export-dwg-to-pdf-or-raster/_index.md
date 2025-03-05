---
title: Εξαγωγή DWG σε PDF ή Raster χρησιμοποιώντας Aspose.CAD για Java
linktitle: Εξαγωγή DWG σε PDF ή Raster
second_title: Aspose.CAD Java API
description: Εξερευνήστε την απρόσκοπτη διαδικασία εξαγωγής αρχείων DWG σε PDF ή εικόνες ράστερ σε Java χρησιμοποιώντας το Aspose.CAD. Αυτός ο οδηγός βήμα προς βήμα εξασφαλίζει ακρίβεια και αποτελεσματικότητα.
type: docs
weight: 13
url: /el/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
---
## Εισαγωγή

Στον δυναμικό κόσμο του σχεδιασμού με τη βοήθεια υπολογιστή (CAD), ο αποτελεσματικός χειρισμός των σχεδίων είναι ζωτικής σημασίας. Το Aspose.CAD για Java παρέχει μια ισχυρή λύση για την εξαγωγή αρχείων DWG σε εικόνες PDF ή ράστερ. Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία, διασφαλίζοντας ότι αξιοποιείτε πλήρως τις δυνατότητες του Aspose.CAD για Java.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τα εξής:

- Βασική κατανόηση προγραμματισμού Java.
-  Εγκαταστάθηκε το Aspose.CAD για τη βιβλιοθήκη Java. Εάν όχι, κατεβάστε το[εδώ](https://releases.aspose.com/cad/java/).
- Ένα αρχείο DWG για δοκιμαστικούς σκοπούς. Μπορείτε να χρησιμοποιήσετε το παρεχόμενο αρχείο "Bottom_plate.dwg".

## Εισαγωγή χώρων ονομάτων

Στο έργο σας Java, εισαγάγετε τους απαραίτητους χώρους ονομάτων για να ξεκινήσετε τη διαδικασία:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Βήμα 1: Φορτώστε το αρχείο DWG

 Ξεκινήστε φορτώνοντας το αρχείο DWG χρησιμοποιώντας το Aspose.CAD's`Image` τάξη:

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Βήμα 2: Προσδιορίστε τον τύπο μονάδας

Στη συνέχεια, ελέγξτε τον τύπο μονάδας του φορτωμένου αρχείου DWG:

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

## Βήμα 3: Ορίστε τις επιλογές ραστεροποίησης

Με βάση τον τύπο της μονάδας, διαμορφώστε τις επιλογές ραστεροποίησης:

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Μετρικές μονάδες
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Αυτοκρατορικές μονάδες
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

## Βήμα 4: Διαμόρφωση επιλογών PDF

Ρύθμιση επιλογών εξαγωγής PDF:

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Βήμα 5: Αποθήκευση ως PDF

Τέλος, αποθηκεύστε το αρχείο DWG ως PDF:

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Και εκεί το έχετε! Εξάγατε με επιτυχία ένα αρχείο DWG σε PDF χρησιμοποιώντας το Aspose.CAD για Java.

## συμπέρασμα

Αυτό το σεμινάριο παρείχε έναν οδηγό βήμα προς βήμα σχετικά με την αξιοποίηση του Aspose.CAD για Java για την εξαγωγή αρχείων DWG σε εικόνες PDF ή ράστερ. Αυτή η βιβλιοθήκη απλοποιεί τη διαδικασία, επιτρέποντάς σας να χειρίζεστε αποτελεσματικά τα σχέδια CAD στις εφαρμογές σας Java.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλα πλαίσια Java;

A1: Ναι, το Aspose.CAD για Java ενσωματώνεται απρόσκοπτα με δημοφιλή πλαίσια Java.

### Ε2: Είναι διαθέσιμη μια προσωρινή άδεια χρήσης για το Aspose.CAD για Java;

 A2: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε3: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD για Java;

 A3: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για βοήθεια από την κοινότητα.

### Ε4: Πώς μπορώ να αγοράσω μια άδεια χρήσης για το Aspose.CAD για Java;

 A4: Μπορείτε να αγοράσετε μια άδεια[εδώ](https://purchase.aspose.com/buy).

### Ε5: Ποιες μονάδες υποστηρίζει το Aspose.CAD για Java;

A5: Το Aspose.CAD για Java υποστηρίζει μετρικές και αυτοκρατορικές μονάδες.