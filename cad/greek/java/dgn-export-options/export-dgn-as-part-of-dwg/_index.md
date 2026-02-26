---
date: 2026-01-10
description: Μάθετε πώς να εξάγετε dgn σε dwg και να μετατρέψετε MicroStation DGN
  σε AutoCAD DWG χρησιμοποιώντας το Aspose.CAD για Java. Οδηγός βήμα‑προς‑βήμα.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD Java API
title: Εξαγωγή DGN σε DWG με το Aspose.CAD για Java
url: /el/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DGN σε DWG με Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial, θα μάθετε πώς να **export dgn to dwg** και να ενσωματώσετε ένα σχέδιο MicroStation DGN μέσα σε ένα αρχείο AutoCAD DWG χρησιμοποιώντας τη βιβλιοθήκη Aspose.CAD για Java. Είτε μεταφέρετε παλιά σχέδια MicroStation είτε χρειάζεστε να συνδυάσετε DGN underlays με DWG layouts, αυτός ο οδηγός σας καθοδηγεί βήμα-βήμα—from τη ρύθμιση του περιβάλλοντος μέχρι τη δημιουργία μιας προεπισκόπησης PDF του τελικού DWG.

## Γρήγορες Απαντήσεις
- **Τι επιτυγχάνει η «export dgn to dwg»;** Ενσωματώνει ένα DGN underlay σε DWG, επιτρέποντας απρόσκοπτη προβολή στο AutoCAD.
- **Σε ποια μορφή μπορώ να εξάγω το αποτέλεσμα για γρήγορη προεπισκόπηση;** Μπορείτε να **export cad file to pdf** χρησιμοποιώντας `PdfOptions`.
- **Χρειάζεται άδεια για την εκτέλεση του κώδικα;** Απαιτείται προσωρινή ή επί πληρωμή άδεια Aspose.CAD για χρήση σε παραγωγή.
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 ή νεότερη λειτουργεί με την τελευταία έκδοση του Aspose.CAD for Java.
- **Υπάρχει δωρεάν δοκιμή;** Ναι – κατεβάστε μια δοκιμή από την ιστοσελίδα της Aspose.

## Τι είναι η «εξαγωγή dgn σε dwg»;
Η εξαγωγή DGN σε DWG σημαίνει μετατροπή ή ενσωμάτωση ενός σχεδίου MicroStation DGN ως underlay μέσα σε ένα σχέδιο AutoCAD DWG. Αυτό επιτρέπει στους επαγγελματίες CAD να αξιοποιήσουν υπάρχοντα DGN assets χωρίς να χρειάζεται να δημιουργήσουν ξανά τη γεωμετρία από την αρχή.

## Γιατί να μετατρέψετε MicroStation DGN σε AutoCAD DWG;
- **Collaboration:** Οι ομάδες που χρησιμοποιούν AutoCAD μπορούν να προβάλλουν και να επεξεργάζονται το περιεχόμενο DGN άμεσα.
- **Standardization:** Το DWG είναι η de‑facto μορφή για πολλές επόμενες διαδικασίες (π.χ., δημιουργία PDF, 3D rendering).
- **Preservation:** Διατηρεί αμετάβλητες τις αρχικές αναφορές DGN, μειώνοντας την απώλεια δεδομένων.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω:
1. **Aspose.CAD Library:** Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD για Java. Μπορείτε να βρείτε τη βιβλιοθήκη [here](https://releases.aspose.com/cad/java/).
2. **Java Development Kit (JDK):** Βεβαιωθείτε ότι έχετε εγκατεστημένη τη Java στο σύστημά σας.
3. **Integrated Development Environment (IDE):** Επιλέξτε ένα Java IDE όπως το Eclipse ή το IntelliJ για πιο ομαλή ανάπτυξη.

## Εισαγωγή Πακέτων

Στο Java project σας, εισάγετε τα απαραίτητα πακέτα Aspose.CAD για να ενεργοποιήσετε τη διαχείριση αρχείων CAD. Δείτε ένα παράδειγμα:

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

## Βήμα 1: Ορισμός Διαδρομών Αρχείων

Ορίστε τις διαδρομές εισόδου και εξόδου για το αρχείο DWG. Ενημερώστε τις μεταβλητές `dataDir`, `fileName` και `outPath` αναλόγως.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

## Βήμα 2: Δημιουργία Παραδείγματος PdfOptions

Δημιουργήστε ένα αντικείμενο της κλάσης `PdfOptions`, καθώς **exporting the CAD file to PDF** για γρήγορη επαλήθευση.

```java
PdfOptions exportOptions = new PdfOptions();
```

## Βήμα 3: Φόρτωση Αρχείου DWG

Φορτώστε το υπάρχον αρχείο DWG ως εικόνα και μετατρέψτε το στον τύπο `CadImage`.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

## Βήμα 4: Επανάληψη μέσω Οντοτήτων

Διασχίστε κάθε οντότητα μέσα στο αρχείο DWG και ελέγξτε αν είναι ορισμός εικόνας. Αν ναι, ανακτήστε την εξωτερική αναφορά στο αντικείμενο.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

## Βήμα 5: Ορισμός Επιλογών Ραστοποίησης

Ορίστε τις ρυθμίσεις για το αντικείμενο `CadRasterizationOptions`, συμπεριλαμβανομένου του πλάτους σελίδας, ύψους, layouts και χρώματος φόντου.

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

## Βήμα 6: Ορισμός Επιλογών Ραστοποίησης Διανυσματικών

Ορίστε τις επιλογές ραστοποίησης διανυσματικών για την εξαγωγή.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

## Βήμα 7: Εξαγωγή DWG σε PDF

Τέλος, εξάγετε το DWG σε PDF καλώντας τη μέθοδο `save`.

```java
cadImage.save(outPath, exportOptions);
```

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| **No DGN underlay appears** | Το DWG δεν περιέχει οντότητα `DGNUNDERLAY`. | Επαληθεύστε ότι το πηγαίο DWG περιλαμβάνει αναφορά DGN. |
| **PDF is blank** | Οι επιλογές ραστοποίησης έχουν μηδενικό μέγεθος ή λάθος layout. | Βεβαιωθείτε ότι `setPageWidth`/`setPageHeight` είναι θετικές και ότι `setLayouts` ταιριάζει με το όνομα του layout του DWG. |
| **License exception** | Εκτέλεση χωρίς έγκυρη άδεια Aspose.CAD. | Εφαρμόστε προσωρινή ή αγορασμένη άδεια πριν καλέσετε οποιαδήποτε μέθοδο API. |

## Συχνές Ερωτήσεις

### Q1: Πού μπορώ να βρω την τεκμηρίωση για Aspose.CAD for Java;
A1: Η τεκμηρίωση είναι διαθέσιμη [here](https://reference.aspose.com/cad/java/).

### Q2: Πώς μπορώ να κατεβάσω τη βιβλιοθήκη Aspose.CAD για Java;
A2: Μπορείτε να κατεβάσετε τη βιβλιοθήκη από [this link](https://releases.aspose.com/cad/java/).

### Q3: Υπάρχει δωρεάν δοκιμή για Aspose.CAD for Java;
A3: Ναι, μπορείτε να βρείτε τη δωρεάν δοκιμή [here](https://releases.aspose.com/).

### Q4: Πού μπορώ να αποκτήσω προσωρινή άδεια για Aspose.CAD for Java;
A4: Αποκτήστε μια προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/).

### Q5: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;
A5: Επισκεφθείτε το φόρουμ υποστήριξης της κοινότητας Aspose.CAD [here](https://forum.aspose.com/c/cad/19).

### Q6: Μπορώ να μετατρέψω το παραγόμενο PDF ξανά σε DWG;
A6: Το PDF είναι μια ραστική προεπισκόπηση· η μετατροπή πίσω σε DWG απαιτεί ξεχωριστό εργαλείο reverse‑engineering.

### Q7: Λειτουργεί αυτή η προσέγγιση με άλλες μορφές CAD όπως DWF ή DXF;
A7: Ναι, το Aspose.CAD υποστηρίζει πολλές μορφές· αρκεί να προσαρμόσετε τις επεκτάσεις αρχείων και τις ρυθμίσεις ραστοποίησης ανάλογα.

**Last Updated:** 2026-01-10  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}