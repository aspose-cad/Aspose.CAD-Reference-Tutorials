---
date: 2026-06-19
description: Μάθετε πώς να ορίσετε χρονικό όριο κατά την αποθήκευση των σχεδίων CAD
  με το Aspose.CAD για Java. Βελτιώστε την απόδοση, αποφύγετε τις κρεμάσεις και εξάγετε
  τα CAD σε PDF αποδοτικά.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Ορίστε χρονικό όριο στην αποθήκευση
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Πώς να ορίσετε χρονικό όριο κατά την αποθήκευση για CAD με το Aspose.CAD
url: /el/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να ορίσετε χρονικό όριο κατά την αποθήκευση για CAD με Aspose.CAD

## Εισαγωγή

Σε αυτόν τον ολοκληρωμένο οδηγό θα μάθετε **πώς να ορίσετε χρονικό όριο** κατά την αποθήκευση σχεδίων CAD χρησιμοποιώντας το Aspose.CAD for Java. Η εφαρμογή χρονικού ορίου αποτρέπει τις μακροχρόνιες λειτουργίες αποθήκευσης από το να κρεμάσουν την εφαρμογή σας, κάτι που είναι ιδιαίτερα σημαντικό όταν χρειάζεται να **εξάγετε CAD σε PDF** ή **μετατρέψετε DWG σε PDF** σε σενάρια επεξεργασίας παρτίδας. Το Aspose.CAD for Java υποστηρίζει περισσότερα από 50 μορφές CAD και μπορεί να διαχειριστεί αρχεία με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, παρέχοντας προβλέψιμη απόδοση και χρήση πόρων.

## Γρήγορες Απαντήσεις
- **Τι κάνει το χρονικό όριο;** Ακυρώνει τη λειτουργία αποθήκευσης μετά από καθορισμένο χρονικό διάστημα, ελευθερώνοντας το νήμα και αποτρέποντας διαρροές πόρων.  
- **Ποια κλάση ελέγχει το χρονικό όριο;** Η `InterruptionTokenSource` παρέχει το token ακύρωσης που χρησιμοποιείται από τη ρουτίνα αποθήκευσης.  
- **Μπορώ ακόμα να εξάγω CAD σε PDF μετά από χρονικό όριο;** Ναι – μπορείτε να πιάσετε την εξαίρεση διακοπής και να επαναλάβετε ή να καταγράψετε την αποτυχία.  
- **Χρειάζομαι ειδική άδεια;** Μια κανονική άδεια Aspose.CAD είναι επαρκής· η λειτουργία χρονικού ορίου είναι ενσωματωμένη.  
- **Είναι αυτή η προσέγγιση ασφαλής για νήματα;** Ναι, όταν κάθε αποθήκευση εκτελείται σε δικό της νήμα με το δικό του token.

## Τι είναι ένα χρονικό όριο στις λειτουργίες αποθήκευσης CAD;
Το χρονικό όριο είναι ένα ρυθμιζόμενο όριο χρόνου που, όταν υπερβείται, αναγκάζει τη διαδικασία αποθήκευσης να σταματήσει και να ρίξει μια εξαίρεση διακοπής. Αυτό προστατεύει την εφαρμογή Java από ατέρμονες κρεμάσεις που προκαλούνται από πολύπλοκα σχέδια ή προβλήματα I/O.

## Γιατί να ορίσετε χρονικό όριο κατά την αποθήκευση αρχείων CAD;
Το Aspose.CAD μπορεί να **μετατρέψει DWG σε PDF** και **να εξάγει CAD σε PDF** σε κάτω από ένα δευτερόλεπτο για τυπικά σχέδια, αλλά εξαιρετικά μεγάλα ή κατεστραμμένα αρχεία μπορεί να χρειαστούν λεπτά. Ορίζοντας ένα χρονικό όριο εγγυάστε ότι οποιαδήποτε μονή αποθήκευση δεν θα υπερβεί, για παράδειγμα, 30 δευτερόλεπτα, διατηρώντας τη συνολική απόδοση της παρτίδας σταθερή και αποτρέποντας την εξάντληση νημάτων.

## Προαπαιτούμενα

Πριν βυθιστείτε στο tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:
- **Aspose.CAD for Java Library** – Βεβαιωθείτε ότι έχετε ενσωματώσει τη βιβλιοθήκη Aspose.CAD for Java στο έργο σας. Μπορείτε να κατεβάσετε τη βιβλιοθήκη από το [website](https://releases.aspose.com/cad/java/).
- **Development Environment** – Ρυθμίστε το περιβάλλον ανάπτυξης Java με όλα τα απαραίτητα εργαλεία και εξαρτήσεις.

## Εισαγωγή Πακέτων

Για να ξεκινήσετε, εισάγετε τα απαιτούμενα πακέτα στο έργο Java σας. Προσθέστε τις παρακάτω γραμμές στην αρχή του αρχείου Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Τώρα, ας αναλύσουμε τον κώδικα παραδείγματος σε βήμα‑βήμα οδηγίες:

## Πώς να ορίσετε χρονικό όριο κατά την αποθήκευση για σχέδια CAD;

Φορτώστε το αρχείο CAD, δημιουργήστε ένα `InterruptionTokenSource` με το επιθυμητό χρονικό όριο και περάστε το token στις επιλογές αποθήκευσης PDF. Εάν η λειτουργία υπερβεί το χρονικό όριο, το Aspose.CAD ρίχνει ένα `OperationCanceledException`, το οποίο μπορείτε να πιάσετε για να διαχειριστείτε την αποτυχία με χάρη.

### Βήμα 1: Ορίστε τους Φακέλους Πηγής και Εξόδου

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Βεβαιωθείτε ότι έχετε τους σωστούς φακέλους πηγής και εξόδου για τα σχέδια CAD σας.

### Βήμα 2: Δημιουργία Πηγής Token Διακοπής

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Αρχικοποιήστε μια πηγή token διακοπής για να διαχειριστείτε τις διακοπές κατά τη λειτουργία αποθήκευσης.

### Βήμα 3: Φόρτωση Σχεδίου CAD

Η κλάση `CadImage` είναι το βασικό αντικείμενο του Aspose.CAD που αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη, προσφέροντας μεθόδους για απόδοση και μετατροπή.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Βήμα 4: Διαμόρφωση Επιλογών Ραστεροποίησης

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Διαμορφώστε τις επιλογές ραστεροποίησης για το σχέδιο CAD.

### Βήμα 5: Διαμόρφωση Επιλογών PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ρυθμίστε τις επιλογές PDF με επιλογές ραστεροποίησης διανυσμάτων και το token διακοπής.

### Βήμα 6: Αποθήκευση Σχεδίου με Χρονικό Όριο

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Αποθηκεύστε το σχέδιο CAD σε αρχείο PDF με το καθορισμένο χρονικό όριο.

### Βήμα 7: Διαχείριση Διακοπής

`OperationCanceledException` ρίχνεται όταν μια λειτουργία αποθήκευσης υπερβαίνει το καθορισμένο χρονικό όριο.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Δημιουργήστε ένα νήμα για να διαχειριστεί την λειτουργία αποθήκευσης και διακόψτε το μετά από ένα καθορισμένο χρονικό όριο.

## Κοινά Προβλήματα και Λύσεις

- **Timeout Too Short** – Εάν λαμβάνετε συχνές διακοπές, αυξήστε την τιμή του χρονικού ορίου για να υποστηρίξετε μεγαλύτερα σχέδια.  
- **InterruptedException Not Caught** – Πάντα τυλίξτε την κλήση αποθήκευσης σε μπλοκ try‑catch για `OperationCanceledException` ώστε να αποτρέψετε την κατάρρευση της εφαρμογής.  
- **Memory Consumption** – Χρησιμοποιήστε `PdfOptions.setVectorRasterizationOptions` για να ρέετε την έξοδο αντί να φορτώνετε ολόκληρο το αρχείο στη μνήμη.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω αυτή τη λειτουργία για να μετατρέψω DWG σε PDF σε μια παρτίδα εργασίας;**  
Α: Ναι, τυλίξτε κάθε μετατροπή στο δικό της νήμα με ξεχωριστό token διακοπής για να επιβάλετε χρονικά όρια ανά αρχείο.

**Ε: Λειτουργεί το χρονικό όριο σε όλες τις μορφές εξόδου;**  
Α: Ο μηχανισμός χρονικού ορίου συνδέεται με το `InterruptionTokenSource` και λειτουργεί με οποιαδήποτε μορφή που σέβεται το token, συμπεριλαμβανομένων PDF, PNG και SVG.

**Ε: Τι συμβαίνει με τα μερικώς γραμμένα αρχεία μετά από χρονικό όριο;**  
Α: Το Aspose.CAD απορρίπτει αυτόματα το ημιτελές αποτέλεσμα, ώστε να μην καταλήξετε με κατεστραμμένα PDF.

**Ε: Απαιτείται άδεια για χρήση σε παραγωγή;**  
Α: Ναι, απαιτείται έγκυρη άδεια Aspose.CAD για εμπορικές εγκαταστάσεις· διατίθεται δωρεάν δοκιμή για αξιολόγηση.

**Ε: Πού μπορώ να βρω περισσότερα παραδείγματα χρήσης token διακοπής;**  
Α: Η επίσημη τεκμηρίωση Aspose.CAD παρέχει πρόσθετα αποσπάσματα κώδικα και οδηγίες βέλτιστων πρακτικών.

## Πρόσθετοι Πόροι

- [releases page](https://releases.aspose.com/cad/java/) – Άμεση σελίδα λήψης για τις τελευταίες εκδόσεις Aspose.CAD for Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Πλήρης αναφορά API και οδηγίες προγραμματιστών.  
- [this link](https://releases.aspose.com/) – Γενικές κυκλοφορίες προϊόντων Aspose.  
- [here](https://purchase.aspose.com/temporary-license/) – Αποκτήστε προσωρινή άδεια για δοκιμή.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Υποστήριξη κοινότητας και συζητήσεις.

## Συμπέρασμα

Τώρα έχετε κατακτήσει **πώς να ορίσετε χρονικό όριο** για την αποθήκευση σχεδίων CAD με το Aspose.CAD for Java. Ενσωματώνοντας ένα `InterruptionTokenSource` στη ροή εργασίας σας, μπορείτε αξιόπιστα **να εξάγετε CAD σε PDF** ή **να μετατρέψετε DWG σε PDF** χωρίς να διατρέχετε κίνδυνο μακροχρόνιων κλειδώσεων, διατηρώντας την εφαρμογή σας ανταποκρινόμενη και κλιμακώσιμη.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF ή Raster χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Εξαγωγή Συγκεκριμένου Διάταξης DWG σε PDF χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Μετατροπή DWG σε PNG και Άλλες Raster Μορφές χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}