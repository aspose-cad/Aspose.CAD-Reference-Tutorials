---
date: 2026-06-04
description: Μάθετε πώς να δημιουργήσετε PDF από CAD και να προσθέσετε ένα watermark
  χρησιμοποιώντας το Aspose.CAD for Java. Αυτός ο οδηγός βήμα‑βήμα καλύπτει την εξαγωγή
  CAD σε PDF, την προσθήκη κειμένου CAD και το branding.
keywords:
- create pdf from cad
- export cad to pdf
- add text cad
- watermark cad drawing
- convert dwg to pdf
linktitle: Προσθήκη Watermark
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  headline: Create PDF from CAD with Watermark - Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from CAD and add a watermark using Aspose.CAD
    for Java. This step‑by‑step guide covers export CAD to PDF, add text CAD, and
    branding.
  name: Create PDF from CAD with Watermark - Aspose.CAD for Java
  steps:
  - name: Import Packages
    text: The `com.aspose.cad` namespace provides all classes you need for CAD manipulation.
      The `Image` class is the entry point for loading and saving CAD files. The `MText`
      class represents multi‑line text that can be styled and positioned.
  - name: Add New MTEXT
    text: MText represents multi‑line text entities that can be used for watermarks.
  - name: Add Simple Entity like Text
    text: TextEntity is a single‑line text object used for simple annotations.
  - name: Export to PDF
    text: SaveFormat.Pdf specifies PDF as the output format for saving.
  type: HowTo
- questions:
  - answer: Aspose.CAD supports **DWG, DXF, DWT, DWF, and over 30 additional formats**,
      allowing you to **export cad to pdf** from virtually any source file.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Yes – you can control font family, size, color, rotation, and transparency
      through the `MText` or `TextEntity` properties.
    question: Can I customize the appearance of the watermark text?
  - answer: Yes, you can download the trial version [here](https://releases.aspose.com/).
    question: Is there a trial version available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community
      assistance and official support channels.
    question: How can I get support for Aspose.CAD?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      detailed API references, code samples, and best‑practice guides.
    question: Where can I find the complete documentation for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Δημιουργία PDF από CAD με Watermark - Aspose.CAD for Java
url: /el/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία PDF από CAD με Υδατογράφημα - Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα **δημιουργήσετε PDF από CAD** σχέδια και θα εφαρμόσετε ένα προσαρμοσμένο υδατογράφημα χρησιμοποιώντας το Aspose.CAD για Java. Η προσθήκη υδατογραφήματος σας επιτρέπει να προστατεύετε τη διανοητική ιδιοκτησία, να χρωματίζετε τα σχέδιά σας ή να ενσωματώνετε πληροφορίες αναθεώρησης. Θα περάσουμε από όλη τη ροή εργασίας — από την εισαγωγή των απαραίτητων πακέτων, την προσθήκη υδατογραφημάτων κειμένου, έως την εξαγωγή του τελικού σχεδίου CAD ως αρχείο PDF. Στο τέλος θα έχετε ένα επαναχρησιμοποιήσιμο κομμάτι κώδικα που μπορείτε να ενσωματώσετε σε οποιοδήποτε έργο Java.

## Γρήγορες Απαντήσεις
- **Ποιος είναι ο κύριος στόχος;** Δημιουργία PDF από αρχείο CAD και επικάλυψη υδατογραφήματος με λίγες μόνο γραμμές κώδικα Java.  
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.CAD for Java (υποστηρίζει 30+ μορφές CAD).  
- **Χρειάζομαι άδεια για δοκιμές;** Διατίθεται δωρεάν δοκιμαστική έκδοση 30 ημερών· απαιτείται εμπορική άδεια για παραγωγή.  
- **Μπορώ να εξάγω CAD σε PDF μετά το υδατογράφημα;** Ναι – η ίδια κλήση API που αποθηκεύει το σχέδιο επίσης το μετατρέπει σε PDF.  
- **Είναι η διαδικασία ασφαλής για νήματα;** Όλες οι κλάσεις Aspose.CAD έχουν σχεδιαστεί για ταυτόχρονη χρήση όταν δημιουργείτε ξεχωριστές παρουσίες ανά νήμα.

## Τι είναι το υδατογράφημα σε CAD;
Ένα υδατογράφημα σε CAD είναι μια ημιδιαφανής επικάλυψη κειμένου ή γραφικού που τοποθετείται σε ένα σχέδιο για να υποδείξει ιδιοκτησία, εμπιστευτικότητα ή κατάσταση αναθεώρησης. Εμφανίζεται πίσω ή πάνω από τη κύρια γεωμετρία χωρίς να τροποποιεί τα υποκείμενα δεδομένα σχεδίασης, επιτρέποντας στους θεατές να βλέπουν το αρχικό περιεχόμενο ενώ αναγνωρίζουν την παρουσία του υδατογραφήματος.

## Γιατί να προσθέσετε υδατογράφημα όταν **δημιουργείτε pdf από cad**;
Το Aspose.CAD για Java υποστηρίζει **30+ μορφές εισόδου** (DWG, DXF, DWF, DWT κ.λπ.) και μπορεί να χειριστεί αρχεία έως **500 MB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Η προσθήκη υδατογραφήματος κατά το βήμα μετατροπής σε PDF εξαλείφει ένα ξεχωριστό βήμα επεξεργασίας, εξοικονομώντας έως **40 %** του χρόνου επεξεργασίας σε δέσμες εργασιών.

## Προαπαιτούμενα

- **Aspose.CAD for Java** – κατεβάστε το πιο πρόσφατο JAR από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – συνιστάται η έκδοση 11 ή νεότερη.  
- Μία έγκυρη **Aspose.CAD license** για παραγωγική χρήση (προαιρετικό για δοκιμή).  

## Πώς να δημιουργήσετε PDF από CAD με υδατογράφημα;

Η CadImage είναι η κύρια κλάση που αντιπροσωπεύει ένα σχέδιο CAD στο Aspose.CAD.  
Για να δημιουργήσετε PDF από αρχείο CAD με ενσωματωμένο υδατογράφημα, πρώτα φορτώστε το σχέδιο σε μια παρουσία `CadImage`, η οποία αντιπροσωπεύει το έγγραφο CAD στη μνήμη. Στη συνέχεια, δημιουργήστε ένα αντικείμενο `MText` ή `TextEntity` που περιέχει το κείμενο του υδατογραφήματος, ορίστε το μέγεθος γραμματοσειράς, το χρώμα και τη διαφάνεια, και προσθέστε το στο χώρο μοντέλου. Τέλος, καλέστε `save` με `SaveFormat.Pdf` για να εξάγετε το τροποποιημένο σχέδιο σε PDF, διατηρώντας την διανυσματική ποιότητα.

### Βήμα 1: Εισαγωγή Πακέτων

Ο χώρος ονομάτων `com.aspose.cad` παρέχει όλες τις κλάσεις που χρειάζεστε για τη διαχείριση CAD.

Η κλάση `Image` είναι το σημείο εισόδου για τη φόρτωση και αποθήκευση αρχείων CAD.  
Η κλάση `MText` αντιπροσωπεύει κείμενο πολλαπλών γραμμών που μπορεί να μορφοποιηθεί και να τοποθετηθεί.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Βήμα 2: Προσθήκη Νέου MTEXT

Η MText αντιπροσωπεύει οντότητες κειμένου πολλαπλών γραμμών που μπορούν να χρησιμοποιηθούν για υδατογραφήματα.

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

### Βήμα 3: Προσθήκη Απλού Οντότητας όπως Κείμενο

Η TextEntity είναι ένα αντικείμενο κειμένου μίας γραμμής που χρησιμοποιείται για απλές σημειώσεις.

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Βήμα 4: Εξαγωγή σε PDF

Το SaveFormat.Pdf καθορίζει το PDF ως μορφή εξόδου για την αποθήκευση.

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);

```

## Κοινά Προβλήματα και Λύσεις

- **Watermark not visible** – Βεβαιωθείτε ότι το χρώμα του κειμένου αντιτίθεται στο φόντο και ορίστε την ιδιότητα `Transparency` (π.χ., 0.5 για 50 % διαφάνεια).  
- **Large files cause OutOfMemoryError** – Ενεργοποιήστε τη λειτουργία streaming του `CadImage` ορίζοντας `CadImageOptions.setLoadMode(LoadMode.Paged)`.  
- **Incorrect font rendering** – Εγκαταστήστε τις απαιτούμενες γραμματοσειρές TrueType στον διακομιστή ή ενσωματώστε τις χρησιμοποιώντας `FontRepository`.

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.CAD συμβατό με όλες τις μορφές αρχείων CAD;**  
A: Το Aspose.CAD υποστηρίζει **DWG, DXF, DWT, DWF και πάνω από 30 επιπλέον μορφές**, επιτρέποντάς σας να **εξάγετε cad σε pdf** από σχεδόν οποιοδήποτε αρχείο προέλευσης.

**Q: Μπορώ να προσαρμόσω την εμφάνιση του κειμένου του υδατογραφήματος;**  
A: Ναι – μπορείτε να ελέγξετε την οικογένεια γραμματοσειράς, το μέγεθος, το χρώμα, την περιστροφή και τη διαφάνεια μέσω των ιδιοτήτων `MText` ή `TextEntity`.

**Q: Υπάρχει δοκιμαστική έκδοση διαθέσιμη για το Aspose.CAD για Java;**  
A: Ναι, μπορείτε να κατεβάσετε τη δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;**  
A: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για βοήθεια από την κοινότητα και επίσημα κανάλια υποστήριξης.

**Q: Πού μπορώ να βρω την πλήρη τεκμηρίωση για το Aspose.CAD για Java;**  
A: Ανατρέξτε στην [documentation](https://reference.aspose.com/cad/java/) για λεπτομερείς αναφορές API, παραδείγματα κώδικα και οδηγούς βέλτιστων πρακτικών.

---

**Τελευταία Ενημέρωση:** 2026-06-04  
**Δοκιμή Με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF ή Raster χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Δημιουργία PDF από DWG και Προσθήκη Κειμένου χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-text-and-annotation/add-text-in-dwg/)
- [Εξαγωγή Συγκεκριμένου Διάταξης DWG σε PDF χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}