---
date: 2025-12-03
description: Μάθετε πώς να ορίζετε το μέγεθος της σελίδας PDF κατά τη μετατροπή DWG
  σε PDF και να ενεργοποιείτε την παρακολούθηση σε αρχεία DWG χρησιμοποιώντας το Aspose.CAD
  for Java – ένας πλήρης οδηγός για την εξαγωγή PDF σχεδίου CAD με ακρίβεια.
language: el
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Ορισμός μεγέθους σελίδας PDF και ενεργοποίηση παρακολούθησης σε αρχεία DWG
  χρησιμοποιώντας το Aspose.CAD σε Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Σελίδας PDF και Ενεργοποίηση Παρακολούθησης σε Αρχεία DWG Χρησιμοποιώντας το Aspose.CAD σε Java

## Εισαγωγή

Αν χρειάζεστε **ορισμό μεγέθους σελίδας PDF** όταν *μετατρέπετε DWG σε PDF* και θέλετε επίσης να παρακολουθείτε τυχόν προβλήματα απόδοσης, το Aspose.CAD for Java σας παρέχει έναν καθαρό, προγραμματιζόμενο τρόπο για να κάνετε και τα δύο. Σε αυτό το tutorial θα περάσουμε βήμα‑βήμα τις ακριβείς ρυθμίσεις για τις διαστάσεις της σελίδας, την ενεργοποίηση της παρακολούθησης και την εξαγωγή ενός PDF CAD—όλα από Java. Στο τέλος θα καταλάβετε γιατί η σωστή ρύθμιση του μεγέθους σελίδας είναι σημαντική για τα CAD σχέδια και πώς να συλλέγετε λεπτομερείς πληροφορίες παρακολούθησης κατά τη διαδικασία εξαγωγής.

## Γρήγορες Απαντήσεις
- **Τι επηρεάζει το “set PDF page size”;** Ορίζει το πλάτος και το ύψος του τελικού καμβά PDF, εξασφαλίζοντας ότι το σχέδιο σας ταιριάζει τέλεια.  
- **Χρειάζομαι άδεια για αυτή τη λειτουργία;** Μια δοκιμαστική έκδοση λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση του Aspose.CAD απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση που υποστηρίζει `CadRasterizationOptions`.  
- **Μπορώ να το χρησιμοποιήσω με άλλες μορφές CAD;** Το παράδειγμα δείχνει DWG/DXF, αλλά η ίδια προσέγγιση λειτουργεί για τις περισσότερες υποστηριζόμενες μορφές.  
- **Πόσο διαρκεί η μετατροπή;** Συνήθως κάτω από ένα δευτερόλεπτο για μικρά αρχεία· μεγαλύτερα σχέδια μπορεί να χρειαστούν περισσότερο χρόνο.

## Τι σημαίνει “set PDF page size” στο πλαίσιο εξαγωγής CAD;
Ο ορισμός του μεγέθους σελίδας PDF ενημερώνει τον renderer για τις ακριβείς διαστάσεις (σε pixel ή points) του καμβά εξόδου. Αυτό είναι ιδιαίτερα σημαντικό για τεχνικά σχέδια όπου η κλίμακα και η διάταξη πρέπει να διατηρηθούν. Χωρίς ρητές ρυθμίσεις μεγέθους σελίδας, το PDF μπορεί να προεπιλεγεί σε μέγεθος που κόβει ή παραμορφώνει το σχέδιο.

## Γιατί να ορίσετε το μέγεθος σελίδας PDF κατά την εξαγωγή CAD σχεδίων;
- **Διατήρηση κλίμακας** – Οι μηχανικοί βασίζονται σε εκτυπώσεις ακριβούς κλίμακας.  
- **Προσαρμογή σε χαρτί** – Επιλέξτε A4, Letter ή προσαρμοσμένο μέγεθος που ταιριάζει στις προδιαγραφές του έργου.  
- **Βελτίωση αναγνωσιμότητας** – Μεγαλύτερες σελίδες μπορούν να εμφανίσουν λεπτομέρειες χωρίς ζουμ.  
- **Συνεπής έξοδος** – Αυτόματες διαδικασίες παράγουν PDF με ίδιες διαστάσεις σε κάθε εκτέλεση.

## Πώς να ορίσετε το μέγεθος σελίδας PDF όταν μετατρέπετε DWG σε PDF;
Παρακάτω θα ρυθμίσουμε το `CadRasterizationOptions` με προσαρμοσμένες τιμές πλάτους και ύψους πριν την εξαγωγή. Αυτό το βήμα αντιμετωπίζει άμεσα την κύρια λέξη‑κλειδί **set PDF page size**.

## Προαπαιτούμενα

- **Java Development Kit (JDK)** – Java 8 ή νεότερη εγκατεστημένη στο σύστημά σας.  
- **Aspose.CAD for Java** – Κατεβάστε από την επίσημη [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – Ένας φάκελος που περιέχει τα αρχεία DWG/DXF που θέλετε να επεξεργαστείτε.

## Εισαγωγή Namespaces

Πρώτα, εισάγετε τις κλάσεις που θα χρειαστείτε. Το μπλοκ κώδικα παραμένει αμετάβλητο από το αρχικό tutorial.

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

## Βήμα 1: Φόρτωση του αρχείου DWG/DXF

Φορτώστε το πηγαίο σας σχέδιο. Προσαρμόστε τη διαδρομή ώστε να δείχνει στο δικό σας αρχείο.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Βήμα 2: Ρύθμιση επιλογών εξαγωγής PDF (συμπεριλαμβανομένου του μεγέθους σελίδας)

Εδώ ορίζουμε το πλάτος και το ύψος της σελίδας—αυτό είναι το σημείο όπου **set PDF page size**. Οι τιμές είναι σε pixel· μπορείτε να τις μετατρέψετε από ίντσες ή χιλιοστά όπως χρειάζεται.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Συμβουλή:** Αν προτιμάτε τυπικά μεγέθη χαρτιού, χρησιμοποιήστε τη μετατροπή `1 inch = 72 points`. Για μια σελίδα A4 (8.27 × 11.69 in), ορίστε `pageWidth = 595` και `pageHeight = 842`.

## Βήμα 3: Υλοποίηση Παρακολούθησης

Η παρακολούθηση καταγράφει τυχόν προβλήματα απόδοσης. Προσθέτουμε έναν προσαρμοσμένο handler που θα κληθεί μετά την εξαγωγή.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Βήμα 4: Εξαγωγή σε PDF

Τώρα εκτελείται η μετατροπή. Το PDF θα δημιουργηθεί με τις διαστάσεις που καθορίσατε και οι πληροφορίες παρακολούθησης θα εκτυπωθούν στην κονσόλα.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Βήμα 5: Κατηγορία CadRenderHandler

Ο handler εκτυπώνει τυχόν αποτυχίες που συνέβησαν κατά την απόδοση. Αυτό σας βοηθά να εντοπίσετε προβλήματα όταν **exporting CAD drawing PDF**.

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

## Συνηθισμένα Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενό PDF** | Το μέγεθος σελίδας ορίστηκε σε 0 ή πολύ μικρό | Επαληθεύστε ότι τα `setPageWidth` και `setPageHeight` είναι θετικές τιμές. |
| **Απουσία γεωμετρίας** | Σφάλματα απόδοσης που καταγράφηκαν από τον handler | Εξετάστε την έξοδο της κονσόλας από το `ErrorHandler` και αντιμετωπίστε τον συγκεκριμένο `RenderCode`. |
| **Αρχείο δεν βρέθηκε** | Λανθασμένη διαδρομή `dataDir` | Χρησιμοποιήστε απόλυτη διαδρομή ή βεβαιωθείτε ότι ο φάκελος υπάρχει. |
| **Απόρριψη άδειας** | Χρήση δοκιμαστικής έκδοσης χωρίς έγκυρη άδεια για μεγάλα αρχεία | Εφαρμόστε την άδεια Aspose.CAD πριν φορτώσετε την εικόνα. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να ενεργοποιήσω την παρακολούθηση για άλλες μορφές αρχείων CAD χρησιμοποιώντας το Aspose.CAD for Java;**  
Α: Το Aspose.CAD υποστηρίζει κυρίως DWG/DXF για παρακολούθηση. Για άλλες μορφές, ανατρέξτε στην επίσημη τεκμηρίωση.

**Ε: Πώς μπορώ να διαχειριστώ πρόσθετες επιλογές εξαγωγής στο Aspose.CAD for Java;**  
Α: Η βιβλιοθήκη προσφέρει πολλές επιλογές όπως DPI, χρώμα φόντου και rasterization διανυσματικών. Δείτε την [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) για λεπτομέρειες.

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.CAD for Java;**  
Α: Ναι, μπορείτε να κατεβάσετε δωρεάν δοκιμαστική έκδοση από το [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Ε: Πού μπορώ να ζητήσω βοήθεια ή να συζητήσω προβλήματα σχετικά με το Aspose.CAD for Java;**  
Α: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα και επίσημες απαντήσεις.

**Ε: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD for Java;**  
Α: Ακολουθήστε τα βήματα που περιγράφονται στη σελίδα [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Τελευταία ενημέρωση:** 2025-12-03  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.11 (τελευταία έκδοση τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}