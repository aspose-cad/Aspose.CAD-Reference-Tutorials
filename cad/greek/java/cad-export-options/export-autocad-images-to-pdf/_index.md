---
date: 2026-10-19
description: Μάθετε πώς να μετατρέψετε DWG σε PDF σε Java με το Aspose.CAD. Αυτός
  ο οδηγός βήμα‑βήμα σας δείχνει πώς να εξάγετε AutoCAD PDF, να αποθηκεύσετε CAD ως
  PDF και να εφαρμόσετε άδεια.
keywords:
- dwg to pdf java
- export autocad pdf
- java pdf export library
- aspose cad license
- save cad pdf
- customize pdf page size
lastmod: 2026-10-19
linktitle: Εξαγωγή εικόνων AutoCAD σε PDF
og_description: Μάθετε πώς να μετατρέψετε DWG σε PDF σε Java με το Aspose.CAD. Αυτός
  ο οδηγός σας καθοδηγεί στη διαδικασία εξαγωγής AutoCAD PDF, αποθήκευσης CAD ως PDF
  και αδειοδότησης.
og_image_alt: 'Tutorial: convert DWG to PDF in Java with Aspose.CAD'
og_title: Μετατροπή DWG σε PDF σε Java χρησιμοποιώντας το Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  headline: Convert DWG to PDF in Java using Aspose.CAD
  type: TechArticle
- description: Learn how to convert DWG to PDF in Java with Aspose.CAD. This step‑by‑step
    guide shows you how to export AutoCAD PDF, save CAD as PDF, and apply a license.
  name: Convert DWG to PDF in Java using Aspose.CAD
  steps:
  - name: set the resource directory path
    text: Replace `"Your Document Directory"` with the absolute path to the folder
      you created in the prerequisites. > **Pro tip:** Use `Paths.get(...).toAbsolutePath()`
      to avoid path‑related errors on different operating systems.
  - name: load the CAD image
    text: Loading the CAD file into an `Image` object gives you full access to Aspose.CAD’s
      rasterization engine. The `Image` class loads the DWG file and prepares it for
      conversion. > **Why this matters:** Once the drawing is in memory, you can query
      its layouts, layers, and metadata before rasterizing.
  - name: set rasterization options
    text: Adjust `pageWidth` and `pageHeight` to **customize PDF page size**. Enabling
      `setTypeOfEntities(TypeOfEntities.Entities3D)` allows full 3‑D rendering when
      needed. The `RasterizationOptions` object controls DPI, page dimensions, and
      entity types for the output. - `pageWidth` / `pageHeight` are measur
  - name: configure PDF options
    text: Tie the rasterization settings to the PDF output, ensuring the vector data
      is correctly transformed. The `PdfOptions` class links the rasterization configuration
      with the final PDF file.
  - name: save the PDF
    text: The resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf**
      representation of your original AutoCAD drawing. The `save` method writes the
      rasterized image to a PDF file on disk.
  type: HowTo
- questions:
  - answer: Yes – the library supports DWG, DXF, DWF, DGN, and over 30 additional
      formats, giving you flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")`, `setLayouts("Layout1")`, etc.,
      to choose which view is rendered into the PDF.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to match any required page dimensions.
    question: Can I change the size of the output PDF file?
  - answer: The dedicated community is available at the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where you can ask questions and share solutions.
    question: Where can I get help if I run into problems?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- dwg to pdf
- aspose.cad
- java cad conversion
- export autocad pdf
title: Μετατροπή DWG σε PDF σε Java χρησιμοποιώντας το Aspose.CAD
url: /el/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή AutoCAD PDF – εξαγωγή εικόνων AutoCAD σε PDF με Aspose.CAD for Java

## Εισαγωγή

Αν χρειάζεστε **convert DWG to PDF in Java**, βρίσκεστε στο σωστό μέρος. Αυτός ο οδηγός δείχνει πώς να εξάγετε εικόνες AutoCAD σε PDF χρησιμοποιώντας το Aspose.CAD for Java, μια καθαρά‑Java βιβλιοθήκη που διαχειρίζεται DWG, DXF, DWF και πολλές άλλες μορφές CAD χωρίς εγγενείς εξαρτήσεις. Στο τέλος θα μπορείτε να **save CAD as PDF**, να ρυθμίσετε τις επιλογές rasterization όπως το μέγεθος σελίδας, και να εφαρμόσετε σωστά μια **Aspose CAD license** για παραγωγική χρήση.

## Γρήγορες απαντήσεις
- **Μπορώ να μετατρέψω DWG σε PDF με Java;** Yes – Aspose.CAD for Java natively supports DWG, DXF and dozens of other CAD formats.  
- **Χρειάζομαι άδεια;** A permanent **Aspose CAD license** removes all evaluation restrictions; a temporary license is available for testing.  
- **Ποιες εκδόσεις Java υποστηρίζονται;** Java 8 and higher are fully supported.  
- **Μπορώ να ελέγξω τις διαστάσεις της σελίδας PDF;** Absolutely – set `pageWidth` and `pageHeight` in the rasterization options.  
- **Είναι δυνατή η απόδοση 3‑Δ;** Yes – enable `TypeOfEntities.Entities3D` to rasterize 3‑D entities.

## Τι είναι η εξαγωγή AutoCAD PDF;
Η εξαγωγή AutoCAD PDF είναι η διαδικασία μετατροπής διανυσματικών σχεδίων CAD σε ένα φορητό έγγραφο PDF. Διατηρεί τα επίπεδα, τα βάρη γραμμών, τα χρώματα και προαιρετικά τη γεωμετρία 3‑Δ, καθιστώντας εύκολο το μοίρασμα των σχεδίων με πελάτες ή την αρχειοθέτησή τους χωρίς την ανάγκη λογισμικού CAD.

## Γιατί να μετατρέψετε DWG σε PDF με Aspose.CAD for Java;
Το Aspose.CAD υποστηρίζει **50+ μορφές εισόδου και εξόδου**, επεξεργάζεται σχέδια με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, και λειτουργεί σε οποιαδήποτε πλατφόρμα που υποστηρίζει Java 8+. Η βιβλιοθήκη σας δίνει πλήρη έλεγχο πάνω σε DPI, μέγεθος σελίδας και διάταξη, ώστε να μπορείτε να **customize PDF page size** ώστε να ταιριάζει ακριβώς με τις προδιαγραφές του έργου, όλα χωρίς εγκατάσταση εγγενών DLL.

## Προαπαιτούμενα

- **Java Development Kit** – JDK 8 ή νεότερο εγκατεστημένο στον υπολογιστή σας.  
- **Aspose.CAD for Java** – κατεβάστε το τελευταίο JAR από το [download link](https://releases.aspose.com/cad/java/).  
- **Working directory** – ένας φάκελος όπου θα αποθηκευτούν τα πηγαία αρχεία DWG και τα παραγόμενα PDF.

## Εισαγωγή ονομάτων χώρων

Η κλάση `Image` αντιπροσωπεύει οποιοδήποτε CAD σχέδιο που μπορεί να rasterize, ενώ οι `RasterizationOptions` και `PdfOptions` σας επιτρέπουν να ρυθμίσετε λεπτομερώς τη μετατροπή.

Η κλάση `Image` είναι το κορυφαίο αντικείμενο του Aspose.CAD που κρατά ένα CAD σχέδιο στη μνήμη.  
Η κλάση `RasterizationOptions` ορίζει πώς τα διανυσματικά δεδομένα rasterize πριν γραφτούν σε PDF.  
Η κλάση `PdfOptions` συνδυάζει τις ρυθμίσεις rasterization με παραμέτρους εξόδου ειδικές για PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Τώρα ας περάσουμε από τον κώδικα βήμα‑βήμα.

## Πώς να μετατρέψετε DWG σε PDF με Aspose.CAD for Java;

Για να μετατρέψετε ένα αρχείο DWG σε PDF με το Aspose.CAD for Java, φορτώστε το σχέδιο χρησιμοποιώντας την κλάση Image, διαμορφώστε τις CadRasterizationOptions (όπως DPI, μέγεθος σελίδας και τύπους οντοτήτων), τυλίξτε αυτές τις επιλογές σε PdfOptions και, στη συνέχεια, καλέστε τη μέθοδο save καθορίζοντας ένα όνομα αρχείου .pdf. Αυτή η ακολουθία εξασφαλίζει ότι τα διανυσματικά δεδομένα rasterize σωστά και το παραγόμενο PDF ταιριάζει με τις απαιτήσεις διάταξης.

### Βήμα 1: ορίστε τη διαδρομή του καταλόγου πόρων

Αντικαταστήστε `"Your Document Directory"` με την απόλυτη διαδρομή του φακέλου που δημιουργήσατε στα προαπαιτούμενα.

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Συμβουλή:** Use `Paths.get(...).toAbsolutePath()` to avoid path‑related errors on different operating systems.

### Βήμα 2: φορτώστε την εικόνα CAD

Η φόρτωση του αρχείου CAD σε ένα αντικείμενο `Image` σας δίνει πλήρη πρόσβαση στη μηχανή rasterization του Aspose.CAD.

Η κλάση `Image` φορτώνει το αρχείο DWG και το προετοιμάζει για μετατροπή.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Γιατί αυτό είναι σημαντικό:** Once the drawing is in memory, you can query its layouts, layers, and metadata before rasterizing.

### Βήμα 3: ορίστε τις επιλογές rasterization

Ρυθμίστε το `pageWidth` και το `pageHeight` για **customize PDF page size**. Η ενεργοποίηση του `setTypeOfEntities(TypeOfEntities.Entities3D)` επιτρέπει πλήρη απόδοση 3‑Δ όταν χρειάζεται.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` μετρώνται σε points (1 pt = 1/72 in).  
- Αφαιρέστε το σχόλιο από τη γραμμή `setTypeOfEntities` για rasterization 3‑Δ.  
- `setLayouts` επιλέγει ποια διάταξη (Model, Layout1, κλπ.) θα αποδοθεί.

### Βήμα 4: διαμορφώστε τις επιλογές PDF

Συνδέστε τις ρυθμίσεις rasterization με την έξοδο PDF, εξασφαλίζοντας ότι τα διανυσματικά δεδομένα μετασχηματίζονται σωστά.

Η κλάση `PdfOptions` συνδέει τη διαμόρφωση rasterization με το τελικό αρχείο PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 5: αποθηκεύστε το PDF

Το παραγόμενο αρχείο, `Export3DImagestoPDF_out_.pdf`, είναι μια **save cad as pdf** αναπαράσταση του αρχικού σας σχεδίου AutoCAD.

Η μέθοδος `save` γράφει την rasterized εικόνα σε αρχείο PDF στον δίσκο.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

## Συχνά προβλήματα & λύσεις

| Σύμπτωμα | Πιθανή αιτία | Διόρθωση |
|----------|--------------|----------|
| Κενό PDF εξόδου | Οι επιλογές rasterization δεν έχουν οριστεί ή υπάρχει ασυμφωνία διάταξης | Επαληθεύστε ότι το `setLayouts` ταιριάζει με το όνομα διάταξης στο αρχείο CAD. |
| Εικόνα χαμηλής ανάλυσης | `pageWidth`/`pageHeight` πολύ μικρά | Αυξήστε τις διαστάσεις ή ορίστε υψηλότερο DPI μέσω `rasterizationOptions.setResolution(...)`. |
| Εξαίρεση άδειας | Δεν έχει εφαρμοστεί έγκυρη άδεια | Εφαρμόστε μια **Aspose CAD license** ή χρησιμοποιήστε προσωρινή άδεια για δοκιμή. |

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλες μορφές αρχείων CAD;**  
A: Ναι – η βιβλιοθήκη υποστηρίζει DWG, DXF, DWF, DGN και πάνω από 30 επιπλέον μορφές, παρέχοντάς σας ευελιξία σε διάφορα έργα.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD for Java;**  
A: Επισκεφθείτε τη [temporary license page](https://purchase.aspose.com/temporary-license/) για να ζητήσετε μια άδεια περιορισμένου χρόνου για αξιολόγηση.

**Q: Υπάρχουν επιλογές διάταξης για rasterization;**  
A: Απόλυτα. Χρησιμοποιήστε `setLayouts("Model")`, `setLayouts("Layout1")`, κλπ., για να επιλέξετε ποια προβολή θα αποδοθεί στο PDF.

**Q: Μπορώ να αλλάξω το μέγεθος του παραγόμενου αρχείου PDF;**  
A: Ναι – τροποποιήστε το `pageWidth` και το `pageHeight` στις επιλογές rasterization ώστε να ταιριάζουν με τις απαιτούμενες διαστάσεις σελίδας.

**Q: Πού μπορώ να λάβω βοήθεια αν αντιμετωπίσω προβλήματα;**  
A: Η αφιερωμένη κοινότητα είναι διαθέσιμη στο [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) όπου μπορείτε να θέσετε ερωτήσεις και να μοιραστείτε λύσεις.

---

**Τελευταία ενημέρωση:** 2026-10-19  
**Δοκιμή με:** Aspose.CAD for Java 24.10  
**Συγγραφέας:** Aspose

## Σχετικές οδηγίες

- [Εξαγωγή DWG σε PDF με Java – Ορισμός μεγέθους σελίδας PDF με Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Εξαγωγή DWG σε PDF: Συγκεκριμένη διάταξη χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Εξαγωγή DWG σε PDF και ενεργοποίηση παρακολούθησης με Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}