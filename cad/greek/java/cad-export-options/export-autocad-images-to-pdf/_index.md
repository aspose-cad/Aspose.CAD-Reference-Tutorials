---
date: 2026-10-19
description: Μάθετε πώς να εξάγετε σχέδια AutoCAD σε PDF με προσαρμοσμένο μέγεθος
  σελίδας PDF χρησιμοποιώντας το Aspose.CAD for Java. Αυτός ο οδηγός βήμα‑βήμα καλύπτει
  τη μετατροπή DWG σε PDF, τις επιλογές rasterization και την άδεια χρήσης.
keywords:
- custom pdf page size
- export autocad to pdf
- save cad as pdf
- generate pdf from dwg
- dwg to pdf java
lastmod: 2026-10-19
linktitle: Εξαγωγή εικόνων AutoCAD σε PDF
og_description: Ορίστε προσαρμοσμένο μέγεθος σελίδας PDF κατά την εξαγωγή σχεδίων
  AutoCAD σε PDF χρησιμοποιώντας το Aspose.CAD for Java. Μάθετε τη μετατροπή DWG σε
  PDF, τις ρυθμίσεις rasterization και την άδεια χρήσης σε λίγα λεπτά.
og_image_alt: Guide showing how to export AutoCAD drawings to PDF with custom page
  dimensions using Aspose.CAD for Java
og_title: Ορισμός προσαρμοσμένου μεγέθους σελίδας PDF για εξαγωγή AutoCAD με Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-19'
  description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  headline: Set custom PDF page size for AutoCAD export with Aspose.CAD
  type: TechArticle
- description: Learn how to export AutoCAD drawings to PDF with a custom PDF page
    size using Aspose.CAD for Java. This step‑by‑step guide covers converting DWG
    to PDF, rasterization options, and licensing.
  name: Set custom PDF page size for AutoCAD export with Aspose.CAD
  steps:
  - name: set the resource directory path
    text: '> **Pro tip:** Replace `"Your Document Directory"` with the absolute path
      to the folder you created in the prerequisites.'
  - name: load the CAD image
    text: The `Image` class loads the CAD file and gives you access to Aspose.CAD’s
      rasterization engine. > **Why this matters:** Once the CAD file is loaded, you
      can manipulate rasterization options before rendering to PDF.
  - name: set rasterization options
    text: The `CadRasterizationOptions` class specifies how the CAD drawing is rasterized
      before being saved as PDF. Adjust `pageWidth` and `pageHeight` to define a **custom
      PDF page size**. You can also enable 3‑D rendering by uncommenting the `setTypeOfEntities`
      line. - `pageWidth` / `pageHeight` – measured
  - name: configure PDF options
    text: The `PdfOptions` class holds PDF‑specific settings and links the rasterization
      options to the output file, ensuring the custom page dimensions are applied
      correctly.
  - name: save the PDF
    text: The `save` method writes the rendered image to the specified PDF file. The
      resulting file, `Export3DImagestoPDF_out_.pdf`, is a **save cad as pdf** representation
      of your original AutoCAD drawing with the exact page dimensions you specified.
  type: HowTo
- questions:
  - answer: Yes, the library supports DWG, DXF, DWF, DGN, and many more, giving you
      flexibility across projects.
    question: Can I use Aspose.CAD for Java with other CAD file formats?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to request a time‑limited license for evaluation.
    question: How do I obtain a temporary license for Aspose.CAD for Java?
  - answer: Absolutely. Use `setLayouts("Model")` or specify other layout names to
      control which view is rendered.
    question: Are there layout options for rasterization?
  - answer: Yes – modify `pageWidth` and `pageHeight` in the rasterization options
      to any dimensions you need.
    question: Can I customize the size of the output PDF file?
  - answer: The dedicated [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) offers
      community support and official responses from the Aspose team.
    question: Where can I get help or discuss issues related to Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
- PDF generation
- DWG export
title: Ορισμός προσαρμοσμένου μεγέθους σελίδας PDF για εξαγωγή AutoCAD με Aspose.CAD
url: /el/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή AutoCAD PDF - εξαγωγή εικόνων AutoCAD σε PDF με Aspose.CAD for Java

## Εισαγωγή

Αν χρειάζεστε **convert DWG to PDF** και να ελέγξετε τις ακριβείς διαστάσεις του αρχείου εξόδου, βρίσκεστε στο σωστό μέρος. Αυτό το tutorial δείχνει πώς να ορίσετε ένα **custom PDF page size** κατά την εξαγωγή εικόνων AutoCAD σε PDF με Aspose.CAD for Java. Στο τέλος του οδηγού θα ξέρετε πώς να φορτώσετε ένα DWG, να διαμορφώσετε τις επιλογές rasterization όπως DPI και πλάτος/ύψος σελίδας, να εφαρμόσετε άδεια, και να δημιουργήσετε ένα PDF έτοιμο για παραγωγή.

## Γρήγορες απαντήσεις
- **Μπορώ να μετατρέψω DWG σε PDF με Java;** Ναι – το Aspose.CAD for Java υποστηρίζει εγγενώς DWG, DXF, DWF και πολλές άλλες μορφές CAD.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Μια πλήρης άδεια Aspose.CAD αφαιρεί όλους τους περιορισμούς αξιολόγησης· μια προσωρινή άδεια είναι διαθέσιμη για δοκιμή.  
- **Ποιες εκδόσεις Java είναι συμβατές;** Η βιβλιοθήκη λειτουργεί με Java 8 και οποιοδήποτε νεότερο JDK.  
- **Πώς αλλάζω τις διαστάσεις της σελίδας PDF;** Ορίστε `pageWidth` και `pageHeight` στο `PdfOptions.getRasterizationOptions()` σε οποιοδήποτε μέγεθος απαιτείτε.  
- **Υποστηρίζεται η απόδοση 3‑D;** Ναι – ενεργοποιήστε `TypeOfEntities.Entities3D` για rasterize 3‑D entities.

## Τι είναι η εξαγωγή AutoCAD PDF;
Η εξαγωγή AutoCAD PDF σημαίνει μετατροπή διανυσματικών CAD σχεδίων (DWG, DXF, DWF κ.λπ.) σε ένα φορητό έγγραφο PDF διατηρώντας τα επίπεδα, τα βάρη γραμμών και προαιρετική 3‑D γεωμετρία. Αυτό σας επιτρέπει να μοιράζεστε σχέδια με πελάτες, να αρχειοθετείτε τα σχέδια ή να εκτυπώνετε χωρίς εγκατάσταση λογισμικού CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD for Java για μετατροπή DWG σε PDF;
Το Aspose.CAD for Java είναι ιδανικό για τη μετατροπή DWG σε PDF επειδή προσφέρει εκτενή υποστήριξη μορφών, λειτουργεί σε καθαρή Java χωρίς εγγενείς εξαρτήσεις, παρέχει rasterization υψηλής ανάλυσης με πλήρη έλεγχο DPI και μεγέθους σελίδας, και περιλαμβάνει ευέλικτη άδεια που σας επιτρέπει να ξεκινήσετε με δοκιμαστική έκδοση και να προχωρήσετε στην παραγωγή.

- **Ευρεία κάλυψη μορφών** – υποστηρίζει πάνω από 50 μορφές εισόδου και εξόδου, συμπεριλαμβανομένων DWG, DXF, DWF, DGN και PDF.  
- **Καθαρή υλοποίηση Java** – χωρίς εγγενή DLLs ή εξωτερικές εξαρτήσεις, έτσι η ανάπτυξη είναι απλή σε οποιαδήποτε πλατφόρμα.  
- **Rasterization υψηλής ανάλυσης** – μπορείτε να καθορίσετε DPI, μέγεθος σελίδας και διάταξη, παρέχοντάς σας πλήρη έλεγχο του **custom PDF page size** του αποτελέσματος.  
- **Κλιμακώσιμη άδεια** – ξεκινήστε με δωρεάν δοκιμή, στη συνέχεια αναβαθμίστε σε μόνιμη **Aspose CAD license**.  

## Προαπαιτούμενα

- **Java Development Kit** – JDK 8 ή νεότερο εγκατεστημένο στο σύστημά σας.  
- **Aspose.CAD for Java** – κατεβάστε το τελευταίο JAR από το [download link](https://releases.aspose.com/cad/java/).  
- **Working directory** – ένας φάκελος που περιέχει τα πηγαία αρχεία DWG και θα λάβει τα παραγόμενα PDF.

## Εισαγωγή namespaces

Η κλάση `Image` είναι το κύριο αντικείμενο του Aspose.CAD που αντιπροσωπεύει ένα CAD σχέδιο στη μνήμη. Εισάγετε τα απαιτούμενα πακέτα πριν ξεκινήσετε τον κώδικα.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Τώρα ας περάσουμε από τον κώδικα βήμα‑βήμα.

## Πώς να ορίσετε προσαρμοσμένο μέγεθος σελίδας PDF κατά την εξαγωγή DWG σε PDF;

Φορτώστε το DWG, ορίστε το επιθυμητό πλάτος και ύψος σελίδας, και στη συνέχεια αποθηκεύστε το αποτέλεσμα ως PDF – αυτό είναι ό,τι χρειάζεστε για να δημιουργήσετε ένα PDF με προσαρμοσμένο μέγεθος σελίδας. Τα παρακάτω βήματα απεικονίζουν την ακριβή ακολουθία και τον ελάχιστο κώδικα που απαιτείται.

### Βήμα 1: ορίστε τη διαδρομή του φακέλου πόρων

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Συμβουλή:** Αντικαταστήστε το `"Your Document Directory"` με την απόλυτη διαδρομή του φακέλου που δημιουργήσατε στα προαπαιτούμενα.

### Βήμα 2: φορτώστε την εικόνα CAD

Η κλάση `Image` φορτώνει το αρχείο CAD και σας δίνει πρόσβαση στη μηχανή rasterization του Aspose.CAD.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Γιατί είναι σημαντικό:** Μόλις φορτωθεί το αρχείο CAD, μπορείτε να τροποποιήσετε τις επιλογές rasterization πριν την απόδοση σε PDF.

### Βήμα 3: ορίστε τις επιλογές rasterization

Η κλάση `CadRasterizationOptions` καθορίζει πώς rasterizes το σχέδιο CAD πριν αποθηκευτεί ως PDF. Ρυθμίστε `pageWidth` και `pageHeight` για να ορίσετε ένα **custom PDF page size**. Μπορείτε επίσης να ενεργοποιήσετε την απόδοση 3‑D αφαιρώντας το σχόλιο από τη γραμμή `setTypeOfEntities`.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- `pageWidth` / `pageHeight` – μετράται σε εικονοστοιχεία· αλλάξτε αυτές τις τιμές ώστε να ταιριάζουν με A4, Letter ή οποιαδήποτε προσαρμοσμένη διάσταση.  
- `setTypeOfEntities(TypeOfEntities.Entities3D)` – αποδίδει 3‑D οντότητες όταν χρειάζεται.  
- `setLayouts` – επιλέγει ποια διάταξη (Model, Layout1 κ.λπ.) θα rasterize.

### Βήμα 4: διαμορφώστε τις επιλογές PDF

Η κλάση `PdfOptions` περιέχει ρυθμίσεις ειδικές για PDF και συνδέει τις επιλογές rasterization με το αρχείο εξόδου, εξασφαλίζοντας ότι οι προσαρμοσμένες διαστάσεις σελίδας εφαρμόζονται σωστά.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 5: αποθηκεύστε το PDF

Η μέθοδος `save` γράφει την αποδοθείσα εικόνα στο καθορισμένο αρχείο PDF.

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Το παραγόμενο αρχείο, `Export3DImagestoPDF_out_.pdf`, είναι μια **save cad as pdf** αναπαράσταση του αρχικού σας σχεδίου AutoCAD με τις ακριβείς διαστάσεις σελίδας που καθορίσατε.

## Συχνά προβλήματα & λύσεις

| Σύμπτωμα | Πιθανή αιτία | Διόρθωση |
|----------|--------------|----------|
| Κενό PDF εξόδου | Οι επιλογές rasterization δεν έχουν οριστεί ή υπάρχει ασυμφωνία διάταξης | Επαληθεύστε ότι το `setLayouts` ταιριάζει με το όνομα διάταξης στο αρχείο CAD. |
| Εικόνα χαμηλής ανάλυσης | `pageWidth`/`pageHeight` πολύ μικρά ή DPI χαμηλό | Αυξήστε τις διαστάσεις ή καλέστε `rasterizationOptions.setResolution(...)` με υψηλότερο DPI. |
| Εξαίρεση άδειας | Δεν έχει εφαρμοστεί έγκυρη άδεια | Εφαρμόστε μόνιμη άδεια Aspose.CAD ή χρησιμοποιήστε προσωρινή άδεια για δοκιμή. |

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλες μορφές αρχείων CAD;**  
A: Ναι, η βιβλιοθήκη υποστηρίζει DWG, DXF, DWF, DGN και πολλές άλλες, προσφέροντάς σας ευελιξία σε όλα τα έργα.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD for Java;**  
A: Επισκεφθείτε τη [temporary license page](https://purchase.aspose.com/temporary-license/) για να ζητήσετε άδεια περιορισμένου χρόνου για αξιολόγηση.

**Q: Υπάρχουν επιλογές διάταξης για rasterization;**  
A: Απολύτως. Χρησιμοποιήστε `setLayouts("Model")` ή καθορίστε άλλα ονόματα διάταξης για να ελέγξετε ποια προβολή αποδίδεται.

**Q: Μπορώ να προσαρμόσω το μέγεθος του παραγόμενου αρχείου PDF;**  
A: Ναι – τροποποιήστε `pageWidth` και `pageHeight` στις επιλογές rasterization σε οποιεσδήποτε διαστάσεις χρειάζεστε.

**Q: Πού μπορώ να λάβω βοήθεια ή να συζητήσω ζητήματα σχετικά με το Aspose.CAD for Java;**  
A: Το αφιερωμένο [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) προσφέρει υποστήριξη από την κοινότητα και επίσημες απαντήσεις από την ομάδα του Aspose.

## Πρόσθετες Συχνές Ερωτήσεις (μορφή φιλική προς AI)

**Q: Το Aspose.CAD απαιτεί κάποια εγγενή βιβλιοθήκη στα Windows ή Linux;**  
A: Όχι. Το Aspose.CAD for Java είναι βιβλιοθήκη καθαρής Java, έτσι τρέχει σε οποιαδήποτε πλατφόρμα που υποστηρίζει το JDK χωρίς πρόσθετες εγγενείς DLLs.

**Q: Πόσο μεγάλο DWG αρχείο μπορεί να επεξεργαστεί η βιβλιοθήκη;**  
A: Η βιβλιοθήκη μπορεί να επεξεργαστεί σχέδια με εκατοντάδες σελίδες (μέχρι 500 MB) χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, χάρη στην αρχιτεκτονική ροής δεδομένων.

**Q: Είναι δυνατόν να μετατρέψετε μαζικά πολλά DWG αρχεία σε PDF σε μία εκτέλεση;**  
A: Ναι. Επανάληψη σε έναν φάκελο, φόρτωση κάθε αρχείου με `Image.load()`, εφαρμογή των ίδιων επιλογών rasterization, και κλήση `save()` για κάθε PDF εξόδου.

**Q: Ποια απόδοση μπορώ να περιμένω σε έναν τυπικό διακομιστή;**  
A: Η μετατροπή ενός DWG 100‑σελίδων στα 300 DPI σε τυπικό CPU 2.5 GHz διαρκεί περίπου 12 δευτερόλεπτα, βάσει των δοκιμών benchmark του Aspose.

**Q: Η βιβλιοθήκη διατηρεί τις πληροφορίες επιπέδων στο PDF;**  
A: Παρόλο που το αποτέλεσμα είναι rasterized, η οπτική εμφάνιση των επιπέδων, των βαρών γραμμών και των χρωμάτων αναπαράγεται πιστά.

---

**Τελευταία ενημέρωση:** 2026-10-19  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.10  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF και Ενεργοποίηση Παρακολούθησης με Aspose.CAD Java](/cad/java/additional-features/enable-tracking/)
- [Εξαγωγή DWG σε PDF: Συγκεκριμένη Διάταξη με Aspose.CAD Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Εξαγωγή DWG σε BMP και Προσαρμογή Μεγέθους CAD Χρησιμοποιώντας Τύπο Μονάδας με Aspose.CAD for Java](/cad/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}