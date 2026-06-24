---
date: 2026-05-20
description: Μάθετε πώς να μετατρέψετε DWG σε PDF ενώ παρακάμπτετε την αυτόματη ανίχνευση
  κωδικοσελίδας χρησιμοποιώντας το Aspose.CAD for Java. Περιλαμβάνει βήματα εξαγωγής
  dwg σε pdf, συμβουλές κωδικοποίησης και αντιμετώπιση προβλημάτων.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Παράκαμψη αυτόματης ανίχνευσης κωδικοσελίδας σε αρχεία DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Μετατροπή DWG σε PDF – Παράκαμψη ανίχνευσης κωδικοσελίδας σε Java
url: /el/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DWG σε PDF – Παράκαμψη Ανίχνευσης Σελίδας Κώδικα σε Java

Σε αυτό το ολοκληρωμένο σεμινάριο θα μάθετε **πώς να μετατρέψετε DWG σε PDF** ενώ παρακάμπτετε την αυτόματη ανίχνευση σελίδας κώδικα που μπορεί να καταστρέψει το κείμενο. Το Aspose.CAD for Java σας παρέχει ακριβή έλεγχο της κωδικοποίησης χαρακτήρων, επιτρέποντάς σας να ανακτήσετε κατεστραμμένα δεδομένα CIF/MIF και να δημιουργήσετε αξιόπιστο PDF. Είτε δημιουργείτε έναν μετατροπέα παρτίδας είτε προσθέτετε επεξεργασία CAD σε μια μεγαλύτερη υπηρεσία Java, τα παρακάτω βήματα σας καθοδηγούν σε όλη τη ροή εργασίας — από τη ρύθμιση του έργου μέχρι την επαλήθευση.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “παράκαμψη σελίδας κώδικα”;** Αναγκάζει το Aspose.CAD να χρησιμοποιεί μια συγκεκριμένη κωδικοποίηση χαρακτήρων αντί να μαντεύει.
- **Μπορώ να εξάγω DWG απευθείας σε PDF;** Ναι – μετά τον ορισμό της σωστής σελίδας κώδικα, μπορείτε να αποθηκεύσετε την εικόνα CAD ως PDF.
- **Ποια κωδικοποίηση λειτουργεί για ιαπωνικό κείμενο;** `CodePages.Japanese` και `MifCodePages.Japanese` είναι οι σωστές επιλογές.
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια· μια προσωρινή άδεια είναι διαθέσιμη για δοκιμές.
- **Ποια έκδοση του Aspose.CAD απαιτείται;** Οποιαδήποτε πρόσφατη έκδοση που υποστηρίζει `LoadOptions` και `PdfOptions`.

## Τι είναι η “εξαγωγή CAD σε PDF”;
Η εξαγωγή CAD σε PDF μετατρέπει ένα διανυσματικό σχέδιο DWG σε ένα καθολικά προβλέψιμο, σταθερό έγγραφο PDF. Η μετατροπή διατηρεί όλα τα γεωμετρικά στοιχεία, τις γραμμές, τα στρώματα και το ενσωματωμένο κείμενο, ενώ «ισοπεδώνει» το σχέδιο σε μορφή που μπορεί εύκολα να μοιραστεί, εκτυπωθεί, αρχειοθετηθεί ή ενσωματωθεί σε άλλες εφαρμογές χωρίς την ανάγκη λογισμικού CAD.

## Γιατί να παρακάμψετε την αυτόματη ανίχνευση σελίδας κώδικα;
Ο καθορισμός της σελίδας κώδικα με το χέρι εγγυάται ότι τα byte του κειμένου ερμηνεύονται σωστά, εξαλείφοντας τους ακατάλληλους χαρακτήρες που συχνά εμφανίζονται όταν η αυτόματη ανίχνευση του Aspose.CAD μαντεύει λανθασμένη κωδικοποίηση παλαιού τύπου. Αυτό είναι απαραίτητο για μη λατινικά αλφάβητα όπως ιαπωνικό, κυριλλικό ή αραβικό, και διασφαλίζει ότι το εξαγόμενο PDF ταιριάζει με το αρχικό σχέδιο.

## Προαπαιτούμενα
- **Περιβάλλον Ανάπτυξης Java** – JDK 8+ και το προτιμώμενο IDE σας.  
- **Aspose.CAD for Java** – Κατεβάστε τη βιβλιοθήκη από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/cad/java/).  
- **DWG Sample File** – Χρησιμοποιήστε το παρεχόμενο `SimpleEntities.dwg` ή οποιοδήποτε DWG χρειάζεστε για μετατροπή.

## Εισαγωγή Πακέτων
Οι κλάσεις `Document`, `LoadOptions` και `PdfOptions` αποτελούν τον πυρήνα της διαδικασίας μετατροπής.

Η κλάση `Document` αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη, παρέχοντας μεθόδους για φόρτωση, επεξεργασία και αποθήκευση του αρχείου σε διάφορες μορφές.  
Η κλάση `LoadOptions` σας επιτρέπει να καθορίσετε τη σελίδα κώδικα και τις επιλογές ανάκτησης κατά τη φόρτωση ενός αρχείου DWG.  
Η κλάση `PdfOptions` ελέγχει τις ρυθμίσεις ειδικές για PDF, όπως συμπίεση, rasterization και μεταδεδομένα.

Στο έργο Java, εισάγετε τις απαραίτητες κλάσεις Aspose.CAD:

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Πώς να μετατρέψετε DWG σε PDF με παράκαμψη σελίδας κώδικα;
Φορτώστε το αρχείο DWG χρησιμοποιώντας `LoadOptions` για να καθορίσετε τη συγκεκριμένη σελίδα κώδικα, στη συνέχεια καλέστε τη μέθοδο `save` στο προκύπτον `CadImage` με μια διαμορφωμένη παρουσία `PdfOptions`. Αυτή η προσέγγιση σε δύο βήματα εξασφαλίζει ότι το κείμενο ερμηνεύεται σωστά και ότι το παραγόμενο PDF διατηρεί την πιστότητα, τα στρώματα και την ποιότητα διανυσματικού σχεδίου του αρχικού.

### Βήμα 1: Ρύθμιση του Έργου Java
Δημιουργήστε ένα έργο Maven ή Gradle και προσθέστε το JAR του Aspose.CAD στο classpath. Αυτό εξασφαλίζει ότι το IDE μπορεί να επιλύσει τις εισαχθείσες κλάσεις και ότι η εκτέλεση μπορεί να εντοπίσει τη βιβλιοθήκη.

### Βήμα 2: Φόρτωση του Αρχείου DWG με Καθορισμένη Σελίδα Κώδικα
Ενημερώστε το Aspose.CAD ποια κωδικοποίηση να χρησιμοποιήσει και αν θα προσπαθήσει να ανακτήσει κατεστραμμένα δεδομένα CIF/MIF.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Βήμα 3: Εξαγωγή της Εικόνας CAD σε PDF
Με την εφαρμογή της σωστής σελίδας κώδικα, μπορείτε με ασφάλεια να εξάγετε το σχέδιο. Το αντικείμενο `PdfOptions` σας επιτρέπει να ρυθμίσετε λεπτομερώς την έξοδο PDF (συμπίεση, rasterization κ.λπ.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Βήμα 4: Επαλήθευση Επιτυχίας
Ένα απλό μήνυμα στην κονσόλα επιβεβαιώνει ότι η διαδικασία ολοκληρώθηκε χωρίς εξαιρέσεις.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Μπορείτε να επαναλάβετε αυτά τα βήματα για πολλαπλά αρχεία DWG, προσαρμόζοντας τη διαδρομή προέλευσης και το όνομα εξόδου όπως απαιτείται.

## Συχνά Προβλήματα & Λύσεις
- **Τα ακατάλληλα χαρακτήρες εξακολουθούν να εμφανίζονται:** Ελέγξτε ξανά ότι το `specifiedEncoding` ταιριάζει με τη σελίδα κώδικα του αρχικού DWG. Χρησιμοποιήστε διαφορετικό enum `CodePages` αν χρειάζεται.  
- **`NullPointerException` στο `cadImage.save`:** Βεβαιωθείτε ότι το αρχείο DWG φορτώνεται σωστά· ελέγξτε τη διαδρομή και τα δικαιώματα αρχείου.  
- **Το μέγεθος του PDF είναι μεγάλο:** Ενεργοποιήστε τη συμπίεση στο `PdfOptions` (π.χ., `pdfOptions.setCompress(true)`) για να μειώσετε το μέγεθος του αρχείου χωρίς να χάσετε ποιότητα.

## Συχνές Ερωτήσεις

**Ε1: Είναι το Aspose.CAD συμβατό με όλες τις εκδόσεις αρχείων DWG;**  
A1: Το Aspose.CAD υποστηρίζει πάνω από 30 εκδόσεις DWG, συμπεριλαμβανομένου του AutoCAD 2018 και παλαιότερων εκδόσεων.

**Ε2: Μπορώ να χρησιμοποιήσω το Aspose.CAD για εμπορικά έργα;**  
A2: Ναι, απαιτείται εμπορική άδεια για παραγωγική χρήση. Μπορείτε να αποκτήσετε άδεια [εδώ](https://purchase.aspose.com/buy).

**Ε3: Υπάρχουν περιορισμοί στην δωρεάν δοκιμαστική έκδοση;**  
A1: Η δοκιμαστική έκδοση επιβάλλει περιορισμούς μεγέθους και λειτουργιών· συμβουλευτείτε την επίσημη τεκμηρίωση για λεπτομέρειες.

**Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;**  
A4: Επισκεφθείτε την κοινότητα [Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για βοήθεια και συζητήσεις.

**Ε5: Υπάρχει προσωρινή άδεια διαθέσιμη για δοκιμαστικούς σκοπούς;**  
A5: Ναι, μια προσωρινή άδεια μπορεί να ζητηθεί [εδώ](https://purchase.aspose.com/temporary-license/).

---

**Τελευταία Ενημέρωση:** 2026-05-20  
**Δοκιμάστηκε Με:** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Συγγραφέας:** Aspose

## Σχετικά Σεμινάρια

- [Εξαγωγή DWG σε PDF και Μετατροπή Σχεδίων CAD – Σεμινάριο Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Εξαγωγή Συγκεκριμένης Διάταξης DWG σε PDF Χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Εξαγωγή DWG σε PDF ή Raster Χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}