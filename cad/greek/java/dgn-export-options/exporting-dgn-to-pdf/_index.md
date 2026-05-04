---
date: 2026-05-04
description: Μάθετε πώς να μετατρέπετε αρχεία CAD PDF εξάγοντας DGN σε AutoCAD PDF
  χρησιμοποιώντας το Aspose.CAD για Java. Οδηγός βήμα‑προς‑βήμα με προσαρμόσιμο μέγεθος
  PDF και επιλογές.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Εξαγωγή DGN σε μορφή AutoCAD σε PDF
second_title: Aspose.CAD Java API
title: Μετατροπή CAD PDF – Απρόσκοπτη εξαγωγή DGN σε PDF AutoCAD με το Aspose.CAD
  για Java
url: /el/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή CAD PDF: Απρόσκοπτη Εξαγωγή DGN σε PDF AutoCAD με το Aspose.CAD για Java

## Εισαγωγή

Αν χρειάζεστε να **convert CAD PDF** αρχεία απευθείας από πηγές DGN, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα σας καθοδηγήσουμε στη χρήση του Aspose.CAD για Java για την εξαγωγή αρχείων DGN σε PDF συμβατό με AutoCAD. Θα δείτε πώς να ορίσετε προσαρμοσμένες διαστάσεις σελίδας, να επιλέξετε συγκεκριμένες διατάξεις και να ρυθμίσετε λεπτομερώς την έξοδο PDF — όλα με σαφή, βήμα‑βήμα κώδικα που μπορείτε να ενσωματώσετε στο δικό σας έργο.

## Γρήγορες Απαντήσεις
- **What does “convert CAD PDF” mean?** Αναφέρεται στη μετατροπή αρχείων πηγής CAD (όπως DGN) σε PDF που διατηρεί τα διανυσματικά δεδομένα και την πιστότητα της διάταξης.  
- **Which library handles the conversion?** Το Aspose.CAD για Java παρέχει μια αξιόπιστη, δωρεάν δοκιμή χωρίς άδεια για αυτήν την εργασία.  
- **Do I need a license for development?** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για χρήση σε παραγωγή.  
- **Can I customize the PDF size?** Ναι – το `CadRasterizationOptions` σας επιτρέπει να ορίσετε το πλάτος, το ύψος και την κλιμάκωση της σελίδας.  
- **How many lines of code are required?** Λιγότερες από 20 γραμμές κώδικα Java για τη φόρτωση, τη ρύθμιση και την αποθήκευση του PDF.

## Τι είναι το “convert CAD PDF”;
Η μετατροπή CAD PDF σημαίνει ότι λαμβάνετε ένα εγγενές σχέδιο CAD (π.χ., DGN) και παράγετε ένα PDF που διατηρεί τα αρχικά διανυσματικά γραφικά, τα στρώματα και τις πληροφορίες διάταξης. Το παραγόμενο PDF μπορεί να προβληθεί σε οποιαδήποτε συσκευή χωρίς την ανάγκη λογισμικού CAD, καθιστώντας το ιδανικό για κοινή χρήση, εκτύπωση ή αρχειοθέτηση.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java για τη μετατροπή CAD PDF;
- **Full format support** – DGN, DWG, DXF, και πολλά άλλα.  
- **No external dependencies** – καθαρά Java, χωρίς εγγενείς DLLs.  
- **Fine‑grained control** – μπορείτε να επιλέξετε ποιες διατάξεις θα εξαχθούν, να ορίσετε προσαρμοσμένα μεγέθη σελίδας και να ελέγξετε την ποιότητα rasterization.  
- **Scalable for batch jobs** – φορτώστε και αποθηκεύστε δεκάδες αρχεία σε βρόχο με ελάχιστο κόστος.

## Προαπαιτούμενα
Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

- **Aspose.CAD Library** – κατεβάστε το [εδώ](https://releases.aspose.com/cad/java/).  
- **Document Directory** – ένας φάκελος στον υπολογιστή σας όπου θα βρίσκονται τα εισερχόμενα αρχεία DGN και τα εξαγόμενα PDFs.

## Εισαγωγή Πακέτων

Στο έργο Java σας, εισάγετε τα απαραίτητα πακέτα για πρόσβαση στις λειτουργίες του Aspose.CAD:

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Τώρα, ας αναλύσουμε τον κώδικα παραδείγματος σε πολλαπλά βήματα:

## Βήμα 1: Ορισμός Διαδρομών Αρχείων (πώς να εξάγετε dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Βεβαιωθείτε ότι αντικαθιστάτε το `"Your Document Directory"` με την πραγματική διαδρομή όπου βρίσκονται τα αρχεία σας.

## Βήμα 2: Φόρτωση Εικόνας DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Φορτώστε το αρχείο DGN χρησιμοποιώντας το Aspose.CAD.

## Βήμα 3: Ορισμός Επιλογών Εξαγωγής PDF (προσαρμογή μεγέθους pdf, ορισμός επιλογών pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Εδώ ορίζουμε τις επιλογές εξαγωγής PDF, συμπεριλαμβανομένων των διαστάσεων σελίδας, της αυτόματης κλιμάκωσης και των συγκεκριμένων διατάξεων DGN (προβολών) που θέλετε να συμπεριλάβετε στο τελικό PDF.

## Βήμα 4: Αποθήκευση Αρχείου PDF

```java
objImage.save(outFile, options);
```

Αποθηκεύστε το εξαχθέν αρχείο PDF. Η μέθοδος `save` εφαρμόζει όλες τις επιλογές που διαμορφώσατε στο προηγούμενο βήμα.

Επαναλάβετε αυτά τα βήματα για τυχόν επιπλέον αρχεία DGN που θέλετε να μετατρέψετε. Συγχαρητήρια! Έχετε ολοκληρώσει επιτυχώς τη **convert CAD PDF** εξάγοντας αρχεία DGN σε μορφή AutoCAD σε PDF χρησιμοποιώντας το Aspose.CAD για Java.

## Συχνά Προβλήματα και Λύσεις
| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| **Αρχείο δεν βρέθηκε** | Λανθασμένη διαδρομή `dataDir` | Ελέγξτε ξανά τη διαδρομή του φακέλου και βεβαιωθείτε ότι το αρχείο DGN υπάρχει. |
| **Κενές σελίδες στο PDF** | `AutomaticLayoutsScaling` ορισμένο σε `false` ή λείπουν τα IDs των διατάξεων | Διατηρήστε `setAutomaticLayoutsScaling(true)` και επαληθεύστε τα ονόματα διατάξεων (`"1","2",…`). |
| **Έξοδος χαμηλής ανάλυσης** | Το προεπιλεγμένο DPI rasterization είναι χαμηλό | Χρησιμοποιήστε `vectorOptions.setResolution(300);` για να αυξήσετε την ποιότητα (προσθέστε πριν από `setVectorRasterizationOptions`). |
| **Εξαίρεση άδειας** | Εκτέλεση χωρίς έγκυρη άδεια σε παραγωγή | Εφαρμόστε προσωρινή ή αγορασμένη άδεια όπως περιγράφεται στην τεκμηρίωση του Aspose. |

## Συχνές Ερωτήσεις (Πρόσθετες)

**Q: Μπορώ να εξάγω μόνο μία διάταξη από ένα αρχείο DGN πολλαπλών διατάξεων;**  
A: Ναι – καθορίστε τα επιθυμητά IDs διατάξεων στο `vectorOptions.setLayouts(new String[] { "2" });`.

**Q: Είναι δυνατόν να ενσωματωθούν γραμματοσειρές στο παραγόμενο PDF;**  
A: Το Aspose.CAD ενσωματώνει αυτόματα τις απαραίτητες γραμματοσειρές όταν τα διανυσματικά δεδομένα rasterize; μπορείτε επίσης να ελέγξετε την ενσωμάτωση γραμματοσειρών μέσω `PdfOptions` αν χρειάζεται.

**Q: Πώς μπορώ να επεξεργαστώ πολλά αρχεία DGN σε batch;**  
A: Τυλίξτε τα βήματα μέσα σε έναν βρόχο `for` που διατρέχει μια λίστα ονομάτων αρχείων, επαναχρησιμοποιώντας την ίδια παρουσία `PdfOptions` για κάθε επανάληψη.

**Q: Υποστηρίζει η βιβλιοθήκη PDFs με προστασία κωδικού;**  
A: Ναι – μπορείτε να ορίσετε κωδικό πρόσβασης στο αντικείμενο `PdfOptions` μέσω `options.setPassword("yourPassword");`.

**Q: Πού μπορώ να βρω περισσότερα παραδείγματα;**  
A: Η επίσημη τεκμηρίωση του Aspose.CAD και το αποθετήριο παραδειγμάτων περιέχουν πολλά επιπλέον σενάρια.

## Συχνές Ερωτήσεις (Αρχικές)

### Q1: Είναι το Aspose.CAD συμβατό με όλες τις μορφές αρχείων CAD;
A1: Ναι, το Aspose.CAD υποστηρίζει ένα ευρύ φάσμα μορφών CAD, εξασφαλίζοντας ευελιξία στην επεξεργασία διαφόρων τύπων αρχείων.

### Q2: Μπορώ να προσαρμόσω τις ρυθμίσεις εξαγωγής PDF;
A2: Απόλυτα. Όπως φαίνεται στο tutorial, μπορείτε να προσαρμόσετε επιλογές όπως διαστάσεις σελίδας και διατάξεις ώστε να ταιριάζουν στις απαιτήσεις σας.

### Q3: Πού μπορώ να βρω πρόσθετη υποστήριξη ή βοήθεια;
A3: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη κοινότητας και συζητήσεις.

### Q4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
A4: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q5: Πώς μπορώ να αποκτήσω προσωρινή άδεια;
A5: Αποκτήστε μια προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Σε αυτό το tutorial εξερευνήσαμε πώς να **convert CAD PDF** αρχεία αξιοποιώντας το Aspose.CAD για Java. Με λίγες μόνο γραμμές κώδικα μπορείτε να φορτώσετε ένα σχέδιο DGN, να ρυθμίσετε λεπτομερώς τις επιλογές εξαγωγής PDF και να δημιουργήσετε PDFs υψηλής ποιότητας έτοιμα για κοινή χρήση ή αρχειοθέτηση. Μη διστάσετε να πειραματιστείτε με διαφορετικά μεγέθη σελίδας, διατάξεις ή επεξεργασία batch ώστε να ταιριάζουν στις ανάγκες του έργου σας.

---

**Last Updated:** 2026-05-04  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}