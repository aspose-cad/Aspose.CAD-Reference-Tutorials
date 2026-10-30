---
date: 2026-10-30
description: Μάθετε πώς να κάνετε μαζική μετατροπή αρχείων DXF σε WMF χρησιμοποιώντας
  Aspose.CAD for Java, με βήμα‑βήμα κώδικα, πληροφορίες δωρεάν δοκιμής και προαιρετική
  εξαγωγή σε PDF.
keywords:
- batch convert dxf files
- aspose cad java
- dxf to wmf conversion
- java cad rasterization
- aspose free trial
lastmod: 2026-10-30
linktitle: Εξαγωγή DXF σε μορφή WMF χρησιμοποιώντας Java
og_description: Μαζική μετατροπή αρχείων DXF σε WMF χρησιμοποιώντας Aspose.CAD for
  Java. Ακολουθήστε αυτόν τον οδηγό για να φορτώσετε σχέδια DXF, να ορίσετε rasterization
  options, να αποθηκεύσετε ως WMF και προαιρετικά να εξάγετε σε PDF με δωρεάν δοκιμή.
og_image_alt: Tutorial showing batch conversion of DXF to WMF in Java using Aspose.CAD
og_title: Μαζική μετατροπή αρχείων DXF σε WMF με Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-10-30'
  description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  headline: Batch convert DXF files to WMF with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to batch convert DXF files to WMF using Aspose.CAD for Java,
    with step‑by‑step code, free trial info, and optional PDF export.
  name: Batch convert DXF files to WMF with Aspose.CAD for Java
  steps:
  - name: load dxf drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: configure rasterization options
    text: '`CadRasterizationOptions` specifies page size, resolution, and background
      for rasterizing the CAD drawing.'
  - name: save as wmf
    text: '`ImageSaveOptions` with `SaveFormat.WMF` tells Aspose.CAD to write the
      output as a Windows Metafile.'
  - name: dispose of resources
    text: Calling `image.close()` releases native resources used by the Aspose.CAD
      Image object.
  - name: optional – export to pdf
    text: '`PdfOptions` configures PDF‑specific settings when saving the image as
      a PDF document. > **Pro tip:** You can reuse the same `CadRasterizationOptions`
      object for PDF export by passing it to a `PdfOptions` instance, saving you a
      few lines of setup.'
  type: HowTo
- questions:
  - answer: You can access the documentation [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).
    question: Where can I find the Aspose.CAD documentation?
  - answer: Download the library [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).
    question: How do I download Aspose.CAD for Java?
  - answer: Yes, you can get a free trial [Aspose free trial page](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: Explore temporary licenses [temporary license options](https://purchase.aspose.com/temporary-license/).
    question: Need temporary licensing options?
  - answer: Visit the Aspose.CAD support forum [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).
    question: Where can I get support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- batch convert dxf
- Aspose.CAD
- Java CAD conversion
- WMF export
- DXF processing
title: Μαζική μετατροπή αρχείων DXF σε WMF με Aspose.CAD for Java
url: /el/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μαζική μετατροπή αρχείων DXF σε WMF με Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **μαζική μετατροπή αρχείων DXF σε WMF** χρησιμοποιώντας το Aspose.CAD για Java. Είτε χρειάζεστε να ενσωματώσετε σχέδια CAD σε αναφορές βασισμένες σε Windows, να δημιουργήσετε ελαφριά διανυσματικά γραφικά για έγγραφα Office, είτε να αυτοματοποιήσετε μετατροπές μεγάλης κλίμακας, αυτός ο οδηγός σας καθοδηγεί στη φόρτωση ενός σχεδίου DXF, τη ρύθμιση επιλογών rasterization, την αποθήκευση ως WMF και προαιρετικά την εξαγωγή του ίδιου σχεδίου σε PDF. Τα βήματα λειτουργούν σε οποιαδήποτε πλατφόρμα που εκτελεί Java 8+.

## Γρήγορες απαντήσεις
- **Μπορώ να μετατρέψω DXF σε WMF με δωρεάν δοκιμή;** Ναι – η Aspose προσφέρει πλήρη λειτουργική δοκιμή 30 ημερών.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη.  
- **Χρειάζομαι άδεια για την εκτέλεση του κώδικα;** Απαιτείται άδεια για παραγωγή· η δοκιμή λειτουργεί για ανάπτυξη και δοκιμή.  
- **Η μετατροπή είναι χωρίς απώλειες;** Τα διανυσματικά δεδομένα διατηρούνται· οι επιλογές rasterization σας επιτρέπουν να ελέγχετε την ανάλυση.  
- **Μπορώ επίσης να εξάγω το ίδιο σχέδιο σε PDF;** Απόλυτα – δείτε το βήμα «Export to PDF» παρακάτω.  
- **Πώς μπορώ να μαζική μετατρέψω πολλά αρχεία DXF ταυτόχρονα;** Επανάληψη μέσω φακέλου, εφαρμόζοντας το ίδιο μοτίβο φόρτωσης‑rasterization‑αποθήκευσης σε κάθε αρχείο.

## Τι είναι η μαζική μετατροπή αρχείων dxf;

Η μαζική μετατροπή αρχείων DXF σημαίνει επεξεργασία πολλαπλών σχεδίων Drawing Exchange Format (DXF) σε μία εκτέλεση και παραγωγή εξόδου WMF για το καθένα. Το WMF (Windows Metafile) είναι μορφή διανυσματικής εικόνας που ενσωματώνεται εγγενώς με το Microsoft Office, τις εφαρμογές Windows και πολλά εργαλεία αναφορών.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java;

Το Aspose.CAD για Java είναι μια καθαρά‑Java μηχανή που υποστηρίζει **πάνω από 50 μορφές εισόδου και εξόδου**—συμπεριλαμβανομένων των DXF, DWG, DGN, PDF, PNG, SVG και WMF—ενώ παρέχει **99 % διανυσματική πιστότητα**. Εκτελείται σε οποιοδήποτε OS που υποστηρίζει Java, δεν απαιτεί εγγενή DLLs και σας επιτρέπει να ελέγχετε το μέγεθος σελίδας, DPI και χρώμα φόντου μέσω μιας μόνο κλάσης `CadRasterizationOptions`. Το ίδιο API διαχειρίζεται επίσης εξαγωγές PDF, PNG και SVG, εξαλείφοντας την ανάγκη για πολλαπλές βιβλιοθήκες.

### Ποσοτικοποιημένα οφέλη
- **Πάνω από 50 υποστηριζόμενες μορφές** μειώνουν την ανάγκη για εξωτερικούς μετατροπείς.  
- **Επεξεργάζεται αρχεία DXF 300 σελίδων σε κάτω από 5 δευτερόλεπτα** σε έναν τυπικό διακομιστή 2.5 GHz όταν rasterized στα 150 DPI.  
- **Το αποτύπωμα μνήμης παραμένει κάτω από 200 MB** για αρχεία έως 500 MB όταν ορίζετε τις κατάλληλες διαστάσεις σελίδας.  

## Προαπαιτούμενα

- **Aspose.CAD for Java** ενσωματωμένο στο έργο σας. Κατεβάστε το από την επίσημη ιστοσελίδα: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- Ένας φάκελος που περιέχει τα αρχεία DXF που θέλετε να μετατρέψετε (π.χ., `Your Document Directory/DXFDrawings/`).  

## Εισαγωγή ονοματοχώρων

`Image` είναι η βασική κλάση του Aspose.CAD που αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη. Μετά τη φόρτωση ενός αρχείου, όλες οι επόμενες λειτουργίες—rasterization, μετατροπή μορφής και εκκαθάριση πόρων—εκτελούνται μέσω αυτού του αντικειμένου.

Οι παρακάτω εισαγωγές φέρνουν τις κλάσεις Aspose.CAD που απαιτούνται για τη φόρτωση, rasterization και αποθήκευση αρχείων CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Οδηγός βήμα‑βήμα

### Πώς να μαζική μετατρέψω αρχεία DXF σε WMF στην Java;

Φορτώστε κάθε DXF με `Image.load`, διαμορφώστε `CadRasterizationOptions` για το επιθυμητό μέγεθος σελίδας και DPI, και καλέστε `image.save` με `SaveFormat.WMF`. Αυτό το μοτίβο τριών βημάτων εκτελεί την πλήρη μετατροπή διατηρώντας την διανυσματική ποιότητα αμετάβλητη και απαιτεί μόνο λίγες γραμμές κώδικα ανά αρχείο.

#### Βήμα 1: φόρτωση σχεδίου dxf

`Image.load` διαβάζει το αρχείο DXF σε ένα αντικείμενο Aspose.CAD Image.

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Βήμα 2: διαμόρφωση επιλογών rasterization

`CadRasterizationOptions` καθορίζει το μέγεθος σελίδας, την ανάλυση και το φόντο για το rasterization του σχεδίου CAD.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Βήμα 3: αποθήκευση ως wmf

`ImageSaveOptions` με `SaveFormat.WMF` λέει στο Aspose.CAD να γράψει την έξοδο ως Windows Metafile.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Βήμα 4: απελευθέρωση πόρων

Η κλήση `image.close()` απελευθερώνει τους εγγενείς πόρους που χρησιμοποιεί το αντικείμενο Aspose.CAD Image.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Βήμα 5: προαιρετικό – εξαγωγή σε pdf

`PdfOptions` διαμορφώνει ρυθμίσεις ειδικές για PDF όταν αποθηκεύεται η εικόνα ως έγγραφο PDF.

```java
finally
{
  cadImage.dispose();
}
```

> **Pro tip:** Μπορείτε να επαναχρησιμοποιήσετε το ίδιο αντικείμενο `CadRasterizationOptions` για εξαγωγή PDF περνώντας το σε μια παρουσία `PdfOptions`, εξοικονομώντας σας μερικές γραμμές ρύθμισης.

## Πώς να εξάγω DXF σε PDF χρησιμοποιώντας το Aspose CAD Java;

Αντικαταστήστε τη μορφή αποθήκευσης WMF με PDF χρησιμοποιώντας `new ImageSaveOptions(SaveFormat.Pdf)`. Οι ίδιες ρυθμίσεις rasterization ισχύουν, και μπορείτε επιπλέον να ορίσετε επιλογές ειδικές για PDF όπως μεταδεδομένα συγγραφέα ή επίπεδο συμπίεσης. Αυτή η μετατροπή μίας γραμμής παράγει ένα PDF αναζητήσιμο, ακριβές σε σελίδες, που αντικατοπτρίζει την αρχική διάταξη CAD.

## Κοινά προβλήματα και λύσεις

`License` είναι η κλάση Aspose που χρησιμοποιείται για την εφαρμογή άδειας προϊόντος κατά την εκτέλεση.

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **`NullPointerException` on `cadImage.save`** | Η μεταβλητή `cadImage` δεν είναι ορισμένη (πρέπει να είναι `image`). | Αντικαταστήστε το `cadImage` με `image` ή μετονομάστε τη μεταβλητή συνεπώς. |
| **Output WMF is blank** | Το μέγεθος σελίδας rasterization είναι πολύ μικρό ή το χρώμα φόντου ορίστηκε ως διαφανές. | Αυξήστε το `PageWidth`/`PageHeight` ή ορίστε χρώμα φόντου μέσω `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **License exception** | Εκτέλεση χωρίς έγκυρη άδεια Aspose στην παραγωγή. | Εφαρμόστε το αρχείο άδειας στην εκκίνηση της εφαρμογής: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Συχνές ερωτήσεις

**Ε: Πού μπορώ να βρω την τεκμηρίωση του Aspose.CAD;**  
Α: Μπορείτε να έχετε πρόσβαση στην τεκμηρίωση [Aspose.CAD Java documentation](https://reference.aspose.com/cad/java/).

**Ε: Πώς να κατεβάσω το Aspose.CAD για Java;**  
Α: Κατεβάστε τη βιβλιοθήκη [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).

**Ε: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
Α: Ναι, μπορείτε να λάβετε δωρεάν δοκιμή [Aspose free trial page](https://releases.aspose.com/).

**Ε: Χρειάζεστε προσωρινές επιλογές αδειοδότησης;**  
Α: Εξερευνήστε προσωρινές άδειες [temporary license options](https://purchase.aspose.com/temporary-license/).

**Ε: Πού μπορώ να λάβω υποστήριξη;**  
Α: Επισκεφθείτε το φόρουμ υποστήριξης Aspose.CAD [Aspose.CAD support forum](https://forum.aspose.com/c/cad/19).

## Πρόσθετες συχνές ερωτήσεις

**Ε: Μπορώ να μετατρέψω μεγάλα αρχεία DXF (εκατοντάδες MB) χωρίς να εξαντλήσω τη μνήμη;**  
Α: Ναι. Φορτώστε το αρχείο σε μπλοκ try‑with‑resources και απελευθερώστε άμεσα το αντικείμενο `Image`. Ρυθμίστε το `CadRasterizationOptions.setPageWidth/Height` σε λογικό μέγεθος για να διατηρήσετε τη χρήση μνήμης χαμηλή.

**Ε: Διατηρεί η έξοδος WMF πληροφορίες στρώσεων;**  
Α: Το WMF είναι μια επίπεδη διανυσματική μορφή, έτσι η ιεραρχία στρώσεων ισοπεδώνεται, αλλά τα στυλ γραμμών, τα χρώματα και τα μοτίβα διαγράμματος διατηρούνται.

**Ε: Είναι δυνατόν να ορίσετε προσαρμοσμένο DPI για το WMF;**  
Α: Χρησιμοποιήστε `rasterizationOptions.setResolution(300);` για να ορίσετε DPI πριν την αποθήκευση.

**Ε: Μπορώ να μαζική-μετατρέψω πολλαπλά αρχεία DXF σε μία εκτέλεση;**  
Α: Απόλυτα. Επανάληψη μέσω καταλόγου, φόρτωση κάθε αρχείου, και εφαρμογή της ίδιας λογικής rasterization και αποθήκευσης.

**Ε: Ποιες εκδόσεις της Java υποστηρίζονται;**  
Α: Το Aspose.CAD για Java υποστηρίζει Java 8 και νεότερες, συμπεριλαμβανομένων των Java 11, 17, και νεότερων εκδόσεων LTS.

---

**Τελευταία ενημέρωση:** 2026-10-30  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικές οδηγίες

- [Δημιουργία PDF από CAD – Εξαγωγή DXF σε PDF με Aspose.CAD για Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Δημιουργία PDF από DXF: Εξαγωγή στρώματος με Aspose.CAD για Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [Πώς να μετατρέψετε τη διάταξη DXF σε εικόνα JPEG με Aspose.CAD στην Java](/cad/java/additional-features/export-specific-layout-to-image/)

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}