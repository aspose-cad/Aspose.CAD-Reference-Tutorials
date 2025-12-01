---
date: 2025-12-01
description: Μάθετε πώς να ορίζετε το μέγεθος σελίδας PDF, να μετατρέπετε DWG σε PDF
  και να ενεργοποιείτε την παρακολούθηση αλλαγών DWG χρησιμοποιώντας το Aspose.CAD
  για Java.
language: el
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Ορισμός μεγέθους σελίδας PDF και παρακολούθηση DWG με Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Σελίδας PDF και Παρακολούθηση DWG με Aspose.CAD Java

## Εισαγωγή

Κατά τη συνεργασία σε έργα CAD, συχνά χρειάζεται να **ορίσετε το μέγεθος σελίδας PDF** για συνεπή διάταξη, **να μετατρέψετε DWG σε PDF**, και να παρακολουθείτε κάθε αλλαγή που γίνεται στο σχέδιο. Το Aspose.CAD για Java καθιστά όλα αυτά εφικτά σε μια ενιαία, απλοποιημένη ροή εργασίας. Σε αυτό το tutorial θα περάσουμε βήμα‑βήμα τις ακριβείς ενέργειες για **ορισμό μεγέθους σελίδας PDF**, ενεργοποίηση **παρακολούθησης αλλαγών DWG**, και εξαγωγή του σχεδίου ως PDF — όλα με χρήση Java.

## Γρήγορες Απαντήσεις
- **Πώς ορίζω το μέγεθος σελίδας PDF;** Χρησιμοποιήστε `CadRasterizationOptions.setPageWidth()` και `setPageHeight()` πριν την εξαγωγή.  
- **Μπορώ να παρακολουθώ αλλαγές κατά την εξαγωγή;** Ναι – υλοποιήστε έναν προσαρμοσμένο `CadRenderHandler` για να καταγράψετε τα αποτελέσματα παρακολούθησης.  
- **Ποια μέθοδος μετατρέπει DWG σε PDF;** Καλέστε `image.save(stream, pdfOptions)` αφού διαμορφώσετε τις επιλογές.  
- **Ποιες είναι οι κύριες προαπαιτήσεις;** JDK, Aspose.CAD για Java, και ένας φάκελος με αρχεία DWG/DXF.  
- **Απαιτείται άδεια για παραγωγική χρήση;** Ναι, απαιτείται έγκυρη άδεια Aspose.CAD για μη‑δοκιμαστικές αναπτύξεις.

## Τι σημαίνει “ορισμός μεγέθους σελίδας PDF” στο πλαίσιο εξαγωγής DWG;

Ο ορισμός του μεγέθους σελίδας PDF καθορίζει τις διαστάσεις του τελικού καμβά PDF (πλάτος × ύψος σε εικονοστοιχεία). Αυτό είναι απαραίτητο όταν θέλετε το εξαγόμενο σχέδιο να ταιριάζει σε συγκεκριμένο μέγεθος χαρτιού ή οθόνης, εξασφαλίζοντας ότι όλα τα στοιχεία εμφανίζονται ακριβώς όπου τα περιμένετε.

##τί να ενεργοποιήσετε την παρακολούθηση κατά την εξαγωγή αρχείων DWG;

Η παρακολούθηση (ή η καταγραφή αλλαγών) καταγράφει τυχόν προβλήματα απόδοσης, ελλιπείς γραμματοσειρές ή μη υποστηριζόμενα στοιχεία που εμφανίζονται κατά τη μετατροπή. Καταγράφοντας αυτές τις πληροφορίες μπορείτε να:

- Εντοπίσετε γρήγορα προβλήματα που πρέπει να διορθωθούν πριν την τελική παράδοση.  
- Παρέχετε σαφή ανατροφοδότηση στα μέλη της ομάδας σχετικά με το τι τροποποιήθηκε ή παραλείφθηκε.  
- Διατηρήσετε ένα αρχείο ελέγχου για βιομηχανίες με αυστηρές απαιτήσεις συμμόρφωσης.

## Προαπαιτήσεις

- **Java Development Kit (JDK)** – οποιαδήποτε πρόσφατη έκδοση (8+).  
- **Aspose.CAD για Java** – κατεβάστε από την επίσημη [σελίδα λήψης Aspose CAD](https://releases.aspose.com/cad/java/).  
- **Φάκελος Εγγράφων** – ένας φάκελος που περιέχει τα αρχεία DWG/DXF που θέλετε να επεξεργαστείτε.

## Εισαγωγή Namespaces

Ξεκινήστε εισάγοντας τις απαραίτητες κλάσεις Aspose.CAD και τις τυπικές κλάσεις Java I/O.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Βήμα 1: Φόρτωση του αρχείου DWG (ή DXF)

Φορτώστε το πηγαίο σχέδιο σε ένα αντικείμενο `Image`. Προσαρμόστε τη διαδρομή ώστε να δείχνει στον δικό σας φάκελο.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Βήμα 2: Διαμόρφωση Επιλογών Εξαγωγής PDF (συμπεριλαμβανομένου του μεγέθους σελίδας)

Εδώ ορίζουμε τις επιλογές PDF και ρητά **ορίζουμε το μέγεθος σελίδας PDF** σε 800 × 600 εικονοστοιχεία. Αυτό είναι το σημείο όπου εφαρμόζεται η κύρια λέξη‑κλειδί.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Βήμα 3: Υλοποίηση Παρακολούθησης

Δημιουργήστε έναν προσαρμοσμένο διαχειριστή σφαλμάτων που θα λαμβάνει πληροφορίες παρακολούθησης κατά τη διαδικασία μετατροπής.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Βήμα 4: Εξαγωγή σε PDF

Με τις επιλογές και τον διαχειριστή παρακολούθησης σε θέση, εξάγετε το σχέδιο. Αυτό το βήμα **μετατρέπει DWG σε PDF** (ή DXF σε PDF στο παράδειγμά μας).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Βήμα 5: Κατηγορία CadRenderHandler – Καταγραφή Αποτελεσμάτων Παρακολούθησης

Η κλάση `ErrorHandler` επεκτείνει το `CadRenderHandler` και εκτυπώνει τυχόν προβλήματα απόδοσης που συνέβησαν κατά την **παρακολούθηση αλλαγών DWG** αρχείων.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Συχνά Προβλήματα & Πώς να Τα Επιδιορθώσετε

| Πρόβλημα | Γιατί Συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| **Ελλιπείς γραμματοσειρές** | Το αρχείο CAD αναφέρεται σε γραμματοσειρές που δεν είναι εγκατεστημένες στον διακομιστή. | Εγκαταστήστε τις απαιτούμενες γραμματοσειρές ή ενσωματώστε τις στο πηγαίο σχέδιο. |
| **Μη υποστηριζόμενα στοιχεία** | Ορισμένα στοιχεία DWG δεν υποστηρίζονται ακόμη από το Aspose.CAD. | Χρησιμοποιήστε την έξοδο παρακολούθησης για να τα εντοπίσετε και απλοποιήστε το σχέδιο. |
| **Λανθασμένο μέγεθος σελίδας** | Δεν κλήθηκε το `setPageWidth/Height` πριν την εξαγωγή. | Βεβαιωθείτε ότι το μέγεθος σελίδας έχει οριστεί στο `CadRasterizationOptions` όπως φαίνεται παραπάνω. |

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να ενεργοποιήσω την παρακολούθηση για άλλες μορφές αρχείων CAD χρησιμοποιώντας Aspose.CAD για Java;

Α1: Το Aspose.CAD υποστηρίζει κυρίως παρακολούθηση για αρχεία DWG/DXF. Για άλλες μορφές, ανατρέξτε στην επίσημη τεκμηρίωση για να δείτε ποιες δυνατότητες είναι διαθέσιμες.

### Ε2: Πώς μπορώ να διαχειριστώ πρόσθετες επιλογές εξαγωγής στο Aspose.CAD για Java;

Α2: Η βιβλιοθήκη προσφέρει πολλές επιλογές όπως DPI, χρώμα φόντου και ραστεροποίηση διανυσματικών στοιχείων. Εξερευνήστε τις στο [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.CAD για Java;

Α3: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμή από το [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Ε4: Πού μπορώ να ζητήσω βοήθεια ή να συζητήσω προβλήματα σχετικά με το Aspose.CAD για Java;

Α4: Το φόρουμ κοινότητας στο [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) είναι ένας εξαιρετικός χώρος για ερωτήσεις και ανταλλαγή εμπειριών.

### Ε5: Πώς να αποκτήσω προσωρινή άδεια για το Aspose.CAD για Java;

Α5: Ακολουθήστε τα βήματα που περιγράφονται στη σελίδα [Temporary License](https://purchase.aspose.com/temporary-license/) για να ζητήσετε άδεια περιορισμένου χρόνου για αξιολόγηση.

### Ε6: Μπορώ να **μετατρέψω DWG σε PDF** διατηρώντας τα επίπεδα;

Α6: Ναι. Διαμορφώνοντας το `CadRasterizationOptions` μπορείτε να διατηρήσετε τις πληροφορίες επιπέδων στο παραγόμενο PDF.

### Ε7: Ποιος είναι ο καλύτερος τρόπος για **εξαγωγή DWG ως PDF** με προσαρμοσμένες διαστάσεις σελίδας;

Α7: Ορίστε το επιθυμητό πλάτος και ύψος χρησιμοποιώντας `setPageWidth` και `setPageHeight` πριν καλέσετε `image.save()` – ακριβώς όπως δείχνει το Βήμα 2.

## Συμπέρασμα

Ακολουθώντας τα παραπάνω βήματα μπορείτε να **ορίσετε το μέγεθος σελίδας PDF**, **να μετατρέψετε DWG σε PDF**, και **να παρακολουθήσετε αλλαγές σε αρχεία DWG** χρησιμοποιώντας Aspose.CAD για Java. Αυτή η ροή εργασίας σας δίνει πλήρη έλεγχο πάνω στην έξοδο της διάταξης, ενώ παρέχει πολύτιδες διαγνώσεις που διατηρούν τη συνεργασία CAD ομαλή και χωρίς σφάλματα. Μη διστάσετε να εξερευνήσετε πρόσθετες επιλογές απόδοσης και να ενσωματώσετε αυτόν τον κώδικα σε μεγαλύτερα pipelines αυτοματοποίησης.

---

**Τελευταία ενημέρωση:** 2025-12-01  
**Δοκιμασμένο με:** Aspose.CAD για Java 24.12 (τελευταία έκδοση τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}