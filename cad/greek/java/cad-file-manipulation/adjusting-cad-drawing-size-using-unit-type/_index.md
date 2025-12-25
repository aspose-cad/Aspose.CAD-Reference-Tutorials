---
date: 2025-12-25
description: Μάθετε πώς να εξάγετε DWG σε BMP χρησιμοποιώντας το Aspose.CAD για Java.
  Αυτός ο οδηγός βήμα‑βήμα δείχνει πώς να προσαρμόσετε το μέγεθος του σχεδίου CAD
  και να μετατρέψετε το CAD σε BMP αποδοτικά.
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
title: Εξαγωγή DWG σε BMP – Προσαρμογή μεγέθους CAD χρησιμοποιώντας τύπο μονάδας (Java)
url: /el/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DWG σε BMP – Προσαρμογή του Μεγέθους Σχεδίου CAD Χρησιμοποιώντας τον Τύπο Μονάδας με το Aspose.CAD για Java

## Εισαγωγή

Όταν χρειάζεστε **export DWG to BMP**, ο έλεγχος του μεγέθους εξόδου και της μονάδας μέτρησης είναι απαραίτητος για την επεξεργασία ή την εκτύπωση. Σε αυτό το tutorial θα μάθετε πώς να προσαρμόζετε το μέγεθος του σχεδίου CAD και να μετατρέπετε το CAD σε BMP με το Aspose.CAD για Java, χρησιμοποιώντας την ιδιότητα `UnitType` για τον ορισμό της μονάδας μέτρησης. Τα βήματα εξηγούνται με απλή γλώσσα, ώστε να μπορείτε να τα ακολουθήσετε ακόμη και αν είστε νέοι στη βιβλιοθήκη.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “export DWG to BMP”;** Μετατροπή ενός σχεδίου DWG σε εικόνα raster BMP.  
- **Ποια ιδιότητα ελέγχει το μέγεθος εξόδου;** `CadRasterizationOptions.setUnitType()` ορίζει τη μονάδα (π.χ., εκατοστό).  
- **Χρειάζομαι άδεια για την εκτέλεση του κώδικα;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται άδεια για παραγωγική χρήση.  
- **Μπορώ να επιλέξω άλλες διατάξεις;** Ναι, χρησιμοποιήστε το `setLayouts()` για να καθορίσετε διατάξεις μοντέλου ή χαρτιού.  
- **Ποιοι μορφές εξόδου υποστηρίζονται;** Εκτός από BMP, μπορείτε να εξάγετε σε PNG, JPEG, TIFF κ.λπ., αλλάζοντας την κλάση επιλογών.

## Τι είναι το **export DWG to BMP**;

Η εξαγωγή DWG σε BMP σημαίνει rasterizing ένα αρχείο DWG βασισμένο σε διανύσματα σε εικόνα bitmap (BMP). Αυτό είναι χρήσιμο όταν χρειάζεστε μια ακριβή αναπαράσταση pixel για παλαιά συστήματα, pipelines επεξεργασίας εικόνας ή απλές περιπτώσεις εμφάνισης.

## Γιατί να προσαρμόσετε το μέγεθος του σχεδίου CAD με **Unit Type**;

Ο ορισμός του τύπου μονάδας σας επιτρέπει να ελέγχετε τις φυσικές διαστάσεις της εξαγόμενης εικόνας χωρίς να υπολογίζετε χειροκίνητα τους παράγοντες κλιμάκωσης. Αυτό διασφαλίζει ότι το bitmap ταιριάζει με πραγματικές μετρήσεις (π.χ., εκατοστά), κάτι που είναι κρίσιμο για τεχνικά σχέδια και έντυπη τεκμηρίωση.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- **Java Development Environment** – Ένα λειτουργικό JDK (8 ή νεότερο) και ένα IDE ή εργαλείο κατασκευής (Maven/Gradle).  
- **Aspose.CAD for Java Library** – Κατεβάστε και ενσωματώστε τη βιβλιοθήκη Aspose.CAD στο Java project σας. Μπορείτε να αποκτήσετε τη βιβλιοθήκη [εδώ](https://releases.aspose.com/cad/java/).

## Εισαγωγή Ονοματοχώρων

Στον κώδικα Java, συμπεριλάβετε τους απαραίτητους ονοματοχώρους για πρόσβαση στις λειτουργίες του Aspose.CAD. Προσθέστε τις παρακάτω εισαγωγές:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία προσαρμογής του μεγέθους του σχεδίου CAD χρησιμοποιώντας τον τύπο μονάδας σε διαχειρίσιμα βήματα:

## Βήμα 1: Ορισμός Καταλόγου Δεδομένων

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ορίστε τη διαδρομή για τον κατάλογο όπου βρίσκονται τα αρχεία CAD σας.

## Βήμα 2: Φόρτωση Σχεδίου CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

Φορτώστε το σχέδιο CAD χρησιμοποιώντας την κλάση `Image` του Aspose.CAD.

## Βήμα 3: Δημιουργία BMP Options

```java
BmpOptions bmpOptions = new BmpOptions();
```

Δημιουργήστε μια παρουσία της κλάσης `BmpOptions` για εξαγωγή της διάταξης CAD σε μορφή BMP.

## Βήμα 4: Διαμόρφωση Rasterization Options

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Δημιουργήστε μια παρουσία του `CadRasterizationOptions` και συνδέστε την με το `BmpOptions` για rasterization διανυσματικών δεδομένων.

## Βήμα 5: Ορισμός Τύπου Μονάδας

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Καθορίστε τον επιθυμητό τύπο μονάδας για το σχέδιο CAD. Σε αυτό το παράδειγμα, το έχουμε ορίσει σε **Centimeter**, το οποίο επηρεάζει άμεσα το μέγεθος της εξαγόμενης εικόνας όταν **προσαρμόζετε το μέγεθος του σχεδίου CAD**.

## Βήμα 6: Ορισμός Διατάξεων

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Ορίστε τις διατάξεις που θα ληφθούν υπόψη κατά την εξαγωγή. Σε αυτή την περίπτωση, έχουμε επιλέξει τη διάταξη **"Model"**, αλλά μπορείτε να μεταβείτε σε διατάξεις paper space αν χρειαστεί.

## Βήμα 7: Εξαγωγή σε BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Τέλος, αποθηκεύστε το τροποποιημένο σχέδιο CAD σε μορφή BMP. Αυτό το βήμα ολοκληρώνει τη ροή εργασίας **export DWG to BMP** διατηρώντας τις ρυθμίσεις μεγέθους που διαμορφώσατε.

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η εικόνα εξόδου είναι πολύ μικρή** | Ο τύπος μονάδας δεν έχει οριστεί ή χρησιμοποιείται η προεπιλογή (pixel). | Καλέστε το `setUnitType()` με τη ζητούμενη μέτρηση (π.χ., `UnitType.Centimeter`). |
| **Εξάχθηκε λανθασμένη διάταξη** | Λάθος στην ονομασία διάταξης | Επαληθεύστε τα ονόματα διατάξεων με έναν προβολέα CAD· χρησιμοποιήστε ακριβή συμβολοσειρά στο `setLayouts()`. |
| **Απόκλιση άδειας** | Εκτέλεση χωρίς έγκυρη άδεια σε παραγωγικό περιβάλλον | Εφαρμόστε προσωρινή ή μόνιμη άδεια όπως περιγράφεται στις Συχνές Ερωτήσεις. |

## Συχνές Ερωτήσεις (Εκτεταμένες)

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλες γλώσσες προγραμματισμού;**  
A: Το Aspose.CAD υποστηρίζει κυρίως Java, αλλά υπάρχουν εκδόσεις διαθέσιμες για άλλες γλώσσες όπως .NET.

**Q: Υπάρχουν επιλογές αδειοδότησης για το Aspose.CAD;**  
A: Ναι, μπορείτε να εξερευνήσετε τις επιλογές αδειοδότησης και να αγοράσετε το Aspose.CAD [εδώ](https://purchase.aspose.com/buy).

**Q: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD;**  
A: Φυσικά, μπορείτε να αποκτήσετε δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;**  
A: Επισκεφθείτε το φόρουμ Aspose.CAD [εδώ](https://forum.aspose.com/c/cad/19) για ολοκληρωμένη υποστήριξη.

**Q: Μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD;**  
A: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

**Τελευταία Ενημέρωση:** 2025-12-25  
**Δοκιμάστηκε Με:** Aspose.CAD for Java 24.10  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}