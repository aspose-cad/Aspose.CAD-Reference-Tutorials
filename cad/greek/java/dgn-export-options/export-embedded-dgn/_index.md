---
date: 2026-01-07
description: Μάθετε πώς να εξάγετε CAD σε PDF και να μετατρέψετε DGN σε PDF χρησιμοποιώντας
  το Aspose.CAD για Java. Οδηγός βήμα‑προς‑βήμα για προγραμματιστές Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με το Aspose.CAD για Java
url: /el/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με Aspose.CAD for Java

## Εισαγωγή

Σε αυτό το tutorial θα βρείτε **πώς να εξηγήσετε το CAD σε PDF** μετατρέποντας ένα ενσωματωμένο αρχείο DGN σε ένα PDF υψηλής ποιότητας με το Aspose.CAD για Java. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που δίνει στους προγραμματιστές Java πλήρη έλεγχο πάνω στη διαχείριση αρχείων CAD, είτε χρειάζεται **μετατροπή DGN σε PDF**, **μετατροπή DWG σε PDF**, είτε απλώς να αποδώσετε σχέδια CAD σε άλλες μορφές. Ακολουθήστε τον οδηγό βήμα‑βήμα παρακάτω και θα μπορείτε να ενσωματώσετε αυτή τη δυνατότητα στις εφαρμογές σας σε λίγα λεπτά.

## Γρήγορες απαντήσεις
- **Τι σημαίνει “εξαγωγή CAD σε PDF”;** Μετατρέπει τα σχέδια CAD (DWG, DGN κ.λπ.) σε αρχεία PDF διατηρώντας την ποιότητα των διανυσματικών δεδομένων.
- **Ποια βιβλιοθήκη χρησιμοποιείται;** Aspose.CAD for Java.
- **Χρειάζομαι άδεια;** Απαιτείται άδεια για παραγωγή· διατίθεται δωρεάν δοκιμή.
- **Ποιά είναι τα κύρια προαπαιτούμενα;** Περιβάλλον ανάπτυξη Java και το JAR του Aspose.CAD for Java.
- **Μπορώ να προσαρμόσω το αποτέλεσμα;** Ναι – μπορείτε να χρησιμοποιήσετε διατάξεις, να ορίσετε ραστεροποίηση επιλογών και να ελέγξετε τις ρυθμίσεις PDF.

## Τι είναι η "εξαγωγή CAD σε PDF";

Η εξαγωγή CAD σε PDF σημαίνει τη λήψη ενός εγγενούς αρχείου CAD (όπως DWG ή DGN) και τη δημιουργία ενός εγγράφου PDF που αναπαριστά τη γεωμετρία του αρχικού αρχείου. Το PDF μπορεί να χρησιμοποιηθεί σε πλατφόρμα χωρίς την ανάγκη λογισμικού CAD, καθιστώντας το ιδανικό για κοινή χρήση, εκτύπωση ή αρχειοθέτηση.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java για να μετατρέψετε το DGN σε PDF;
- **Χωρής εξωτερικές εξαρτήσεις** – λειτουργεί αποκλειστικά σε Java.
- **Διατηρεί τα διανυσματικά δεδομένα** – τα PDF παραμένουν καθαρά σε επίπεδο ζουμ.
- **Λεπτομερής έλεγχος** – επιλέξτε συγκεκριμένες διατάξεις, ορίστε το DPI rasterization και ενσωματώστε γραμματοσειρές.
- **Έτοιμο για επιχειρήσεις** – υποστηρίζει μεγάλα αρχεία, επεξεργασία δέσμης και επιλογές αδειοδότησης.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι διαθέτετε τα εξής:

- **Περιβάλλον Ανάπτυξης Java** – εγκατεστημένο και ρυθμισμένο JDK 8 ή νεότερο.
- **Aspose.CAD for Java** – κατεβάστε το πιο πρόσφατο JAR από [here](https://releases.aspose.com/cad/java/).

## Εισαγωγή πακέτων

Για να ξεκινήσετε, πρέπει να εισάγετε τις απαραίτητες κλάσεις στο έργο σας Java. Προσθέστε τις παρακάτω δηλώσεις import στο αρχείο πηγαίου κώδικα:

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

## Πώς να εξάγετε DGN σε PDF χρησιμοποιώντας το Aspose.CAD για Java;

Παρακάτω υπάρχει ένας σαφής, αριθμημένος οδηγός που δείχνει ακριβώς πώς να μετατρέψετε ένα ενσωματωμένο αρχείο DGN (αποθηκευμένο μέσα σε DWG) σε PDF.

### Βήμα 1: Ρύθμιση διαδρομών εισόδου και εξόδου

Ορίστε τον φάκελο που περιέχει το αρχείο προέλευσης και καθορίστε το DWG που περιέχει το ενσωματωμένο DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Βήμα 2: Φόρτωση αρχείου DWG

Φορτώστε το αρχείο DWG σε ένα αντικείμενο `Image`. Το Aspose.CAD ανιχνεύει αυτόματα τα ενσωματωμένα δεδομένα DGN.

```java
Image objImage = Image.load(fileName);
```

### Βήμα 3: Ρύθμιση επιλογών ραστεροποίησης

Επιλέξτε ποιες διατάξεις θέλετε να συμπεριλάβετε στο PDF. Σε αυτό το παράδειγμα εξάγουμε μόνο τη διάταξη **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Βήμα 4: Ρύθμιση επιλογών PDF

Συνδέστε τις ρυθμίσεις rasterization με τις επιλογές εξαγωγής PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 5: Αποθήκευση αρχείου PDF

Τέλος, γράψτε το PDF στο δίσκο χρησιμοποιώντας τις διαμορφωμένες επιλογές```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Μετατροπή DWG σε PDF – μια επιπλέον συμβουλή

Αν το αρχείο προέλευσής σας είναι ένα απλό DWG (χωρίς ενσωματωμένο DGN), μπορείτε να επαναχρησιμοποιήσετε τον ίδιο κώδικα – απλώς αλλάξτε το `fileName` ώστε να εμφανίζεται στο DWG που θέλετε να μετατρέψετε. Οι ρυθμίσεις rasterization και PDF παραμένουν ίδιες, παρέχετε μια συνεπή ροή εργασίας **convert DWG to PDF**.

## Κοινά ζητήματα και λύσεις

| Τεύχος | Λόγος | Λύση |
|-------|--------|----------|
| **Κενή έξοδος PDF** | Αναντιστοιχία ονόματος διάταξης | Βεβαιωθείτε ότι το όνομα διάταξης που μεταβιβάστηκε στο `setLayouts` ταιριάζει ακριβώς με τη διάταξη στο αρχείο προέλευσης (με διάκριση πεζών-κεφαλαίων). |
| **Εξαίρεση άδειας** | Χρήση της δοκιμής χωρίς άδεια | Εφαρμόστε μια έγκυρη άδεια χρήσης Aspose.CAD πριν από τη φόρτωση της εικόνας (`Άδεια άδειας χρήσης = νέα άδεια (); license.setLicense("Aspose.CAD.lic");`). |
| **Το αρχείο δεν βρέθηκε** | Λανθασμένη διαδρομή «dataDir» | Χρησιμοποιήστε μια απόλυτη διαδρομή ή βεβαιωθείτε ότι η σχετική διαδρομή είναι σωστή σε σχέση με τον κατάλογο εργασίας του έργου. |
| **Γραφικά χαμηλής ανάλυσης** | Το προεπιλεγμένο DPI ραστεροποίησης είναι χαμηλό | Ορίστε το "rasterizationOptions.setPageWidth/Height" ή το "setResolution" για να αυξήσετε το DPI. |

## Συχνές Ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java σε εμπορικό έργο;**
A: Ναι, το Aspose.CAD for Java είναι εμπορική βιβλιοθήκη. Μπορείτε να αποκτήσετε άδεια από [here](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**
Α: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή του Aspose.CAD για Java [εδώ](https://releases.aspose.com/).

**Ε: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;**
A: Μπορείτε να ζητήσετε υποστήριξη από την κοινότητα Aspose.CAD στο [forum](https://forum.aspose.com/c/cad/19).

**Q: Τι κάνω αν χρειάζομαι προσωρινή άδεια;**
A: Μπορείτε να αποκτήσετε προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/).

**Q: Πού μπορώ να βρω την τεκμηρίωση;**
Α: Η τεκμηρίωση είναι διαθέσιμη [εδώ](https://reference.aspose.com/cad/java/).

## Συμπέρασμα

Τώρα έχετε μάθει πώς να **εξάγετε CAD σε PDF**, συγκεκριμένα πώς να **μετατρέψετε το DGN σε PDF** και ακόμη και **μετατρέψετε το DWG σε PDF** χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθώντας τα παραπάνω βήματα, μπορείτε να ενσωματώσετε αδιάλειπτη μετατροπή CAD‑‑PDF σε παρεχόμενη λύση βασισμένη σε Java, προσθέτοντας PDF υψηλής ποιότητας στους χρήστες σας χωρίς την ανάγκη πρόσθετου λογισμικού CAD.

---

**Τελευταία ενημέρωση:** 2026-01-07  
**Δοκιμή με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
