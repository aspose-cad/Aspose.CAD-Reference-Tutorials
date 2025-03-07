---
title: Χρονικό όριο στην Αποθήκευση για CAD με Aspose.CAD
linktitle: Βάλτε το Timeout στην Αποθήκευση
second_title: Aspose.CAD Java API
description: Μάθετε πώς να ενισχύσετε την απόδοση της εφαρμογής Java με το Aspose.CAD. Βάλτε ένα χρονικό όριο αποθήκευσης για σχέδια CAD. Ακολουθήστε τον βήμα προς βήμα οδηγό μας.
weight: 15
url: /el/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Χρονικό όριο στην Αποθήκευση για CAD με Aspose.CAD

## Εισαγωγή

Καλώς ήρθατε στο σεμινάριο σχετικά με την τοποθέτηση χρονικού ορίου κατά την αποθήκευση χρησιμοποιώντας το Aspose.CAD για Java. Σε αυτόν τον οδηγό, θα σας καθοδηγήσουμε στη διαδικασία ορισμού ενός χρονικού ορίου για την αποθήκευση σχεδίων CAD για τη βελτίωση της απόδοσης της εφαρμογής σας. Το Aspose.CAD για Java είναι μια ισχυρή βιβλιοθήκη που σας επιτρέπει να εργάζεστε με αρχεία CAD στις εφαρμογές σας Java χωρίς προβλήματα.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:
-  Aspose.CAD για Java Library: Βεβαιωθείτε ότι έχετε ενσωματωμένη τη βιβλιοθήκη Aspose.CAD για Java στο έργο σας. Μπορείτε να κατεβάσετε τη βιβλιοθήκη από το[δικτυακός τόπος](https://releases.aspose.com/cad/java/).
- Περιβάλλον ανάπτυξης: Ρυθμίστε το περιβάλλον ανάπτυξης Java με όλα τα απαραίτητα εργαλεία και εξαρτήσεις.

## Εισαγωγή πακέτων

Για να ξεκινήσετε, εισαγάγετε τα απαιτούμενα πακέτα στο έργο σας Java. Προσθέστε τις ακόλουθες γραμμές στην αρχή του αρχείου σας Java:

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Τώρα, ας αναλύσουμε το παράδειγμα κώδικα σε οδηγίες βήμα προς βήμα:

## Βήμα 1: Ορισμός καταλόγου προέλευσης και εξόδου

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Βεβαιωθείτε ότι έχετε τους σωστούς καταλόγους προέλευσης και εξόδου για τα σχέδιά σας CAD.

## Βήμα 2: Δημιουργήστε πηγή διακριτικού διακοπής

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Εκκινήστε μια πηγή διακριτικού διακοπής για τη διαχείριση των διακοπών κατά τη λειτουργία αποθήκευσης.

## Βήμα 3: Φορτώστε το σχέδιο CAD

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Φορτώστε το σχέδιο CAD στο α`CadImage` αντικείμενο.

## Βήμα 4: Διαμόρφωση επιλογών ραστεροποίησης

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Διαμορφώστε τις επιλογές ραστεροποίησης για το σχέδιο CAD.

## Βήμα 5: Διαμόρφωση επιλογών PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Ρυθμίστε τις επιλογές PDF με επιλογές διανυσματικής ραστεροποίησης και το διακριτικό διακοπής.

## Βήμα 6: Αποθήκευση σχεδίου με χρονικό όριο

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Αποθηκεύστε το σχέδιο CAD σε ένα αρχείο PDF με το καθορισμένο χρονικό όριο.

## Βήμα 7: Χειριστείτε τη διακοπή

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

Δημιουργήστε ένα νήμα για να χειριστείτε τη λειτουργία αποθήκευσης και να τη διακόψετε μετά από ένα καθορισμένο χρονικό όριο.

## συμπέρασμα

Συγχαρητήρια! Έχετε μάθει με επιτυχία πώς να θέσετε ένα χρονικό όριο αποθήκευσης χρησιμοποιώντας το Aspose.CAD για Java. Αυτή η δυνατότητα μπορεί να βελτιώσει σημαντικά την αποτελεσματικότητα των εφαρμογών σας που σχετίζονται με το CAD.

## Συχνές ερωτήσεις

### Ε1: Πώς μπορώ να κατεβάσω το Aspose.CAD για Java;

 A1: Μπορείτε να το κατεβάσετε από το[σελίδα εκδόσεων](https://releases.aspose.com/cad/java/).

### Ε2: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.CAD για Java;

 A2: Ανατρέξτε στο[τεκμηρίωση](https://reference.aspose.com/cad/java/) για ολοκληρωμένη ενημέρωση.

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

A3: Ναι, μπορείτε να λάβετε δωρεάν δοκιμή από[αυτός ο σύνδεσμος](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να αποκτήσω προσωρινή άδεια;

 Α4: Επίσκεψη[εδώ](https://purchase.aspose.com/temporary-license/) για λεπτομέρειες προσωρινής άδειας.

### Ε5: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;

 Α5: Κατευθυνθείτε προς το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
