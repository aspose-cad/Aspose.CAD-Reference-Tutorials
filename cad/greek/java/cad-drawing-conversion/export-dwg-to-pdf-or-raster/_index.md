---
date: 2026-10-14
description: Μάθετε πώς η βιβλιοθήκη CAD Java Aspose.CAD για Java μπορεί να εξάγει
  DWG σε PDF ή raster εικόνες γρήγορα και με ακρίβεια.
keywords:
- export dwg pdf
- high quality pdf
- dwg to pdf tutorial
- aspose cad java
- java cad library
lastmod: 2026-10-14
linktitle: Εξαγωγή DWG PDF και raster εικόνων
og_description: Εξαγωγή DWG PDF γρήγορα με Aspose.CAD για Java. Μάθετε για τη μετατροπή
  PDF υψηλής ποιότητας, τις επιλογές raster και την αδειοδότηση σε αυτόν τον οδηγό
  βήμα‑βήμα.
og_image_alt: Tutorial showing Java code to convert DWG drawings to PDF and raster
  formats with Aspose.CAD
og_title: Εξαγωγή DWG PDF και raster εικόνων χρησιμοποιώντας τη βιβλιοθήκη CAD Java
  Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-14'
  description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  headline: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  type: TechArticle
- description: Learn how the Java CAD library Aspose.CAD for Java can export DWG to
    PDF or raster images quickly and accurately.
  name: Export DWG PDF and raster images using Java CAD library Aspose.CAD
  steps:
  - name: Load the DWG file
    text: First, load your DWG drawing using the `Image` class. This creates an in‑memory
      representation that Aspose.CAD can work with.
  - name: Determine unit type
    text: Understanding whether the drawing uses metric or imperial units is essential
      for correct scaling. The helper method `IsMetric` (implementation omitted for
      brevity) returns a boolean flag.
  - name: Set rasterization options
    text: The `CadRasterizationOptions` class defines rasterization parameters such
      as DPI, page size, and unit conversion. Based on the unit system, configure
      page size, scaling, and the target unit type. These options drive how the DWG
      is rasterized before being wrapped into a PDF.
  - name: Configure PDF options (pdf options cad)
    text: The `PdfOptions` class specifies PDF‑specific settings, including compression
      and metadata. Create a `PdfOptions` instance and attach the rasterization settings.
      This tells Aspose.CAD how to embed the rasterized content into the final PDF.
  - name: Save as PDF
    text: The `save` method writes the image to the given file path using the supplied
      options. Finally, export the drawing to a PDF file. The `save` method takes
      the output path and the configured `PdfOptions`. When the code finishes, you’ll
      find **Saved.pdf** in your `DWGDrawings` folder, ready for distribu
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java seamlessly integrates with popular Java frameworks
      such as Spring, Jakarta EE, and Android.
    question: Can I use Aspose.CAD for Java with other Java frameworks?
  - answer: Yes, you can obtain a temporary license **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.
    question: Is a temporary license available for Aspose.CAD for Java?
  - answer: Visit the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** for
      assistance from the community and Aspose engineers.
    question: Where can I find support for Aspose.CAD for Java?
  - answer: You can purchase a license **[purchase a license](https://purchase.aspose.com/buy)**.
    question: How can I purchase a license for Aspose.CAD for Java?
  - answer: Aspose.CAD for Java supports both metric and imperial units, automatically
      detecting the drawing’s unit system.
    question: What units does Aspose.CAD for Java support?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- export dwg
- aspose.cad
- java cad conversion
title: Εξαγωγή DWG PDF και raster εικόνων χρησιμοποιώντας τη βιβλιοθήκη CAD Java Aspose.CAD
url: /el/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DWG PDF και εικόνων raster χρησιμοποιώντας τη βιβλιοθήκη Java CAD Aspose.CAD

## Εισαγωγή

Η εξαγωγή DWG σε PDF είναι συχνή απαίτηση για μηχανικούς, αρχιτέκτονες και όποιον χρειάζεται να μοιραστεί σχέδια CAD χωρίς να εκθέτει το εγγενές αρχείο. Με **Aspose.CAD for Java**, μπορείτε να **export dwg pdf** — ή εικόνες raster — σε λίγες μόνο γραμμές κώδικα Java, διατηρώντας την ακρίβεια των διανυσματικών δεδομένων και τη διάταξη. Αυτό το tutorial σας καθοδηγεί στη φόρτωση ενός αρχείου DWG, στη διαμόρφωση της rasterization και στην αποθήκευση του αποτελέσματος ως PDF ή εικόνα υψηλής ποιότητας. Θα δείτε επίσης γιατί το Aspose.CAD είναι η προτιμώμενη βιβλιοθήκη Java CAD για αξιόπιστη, διαπλατφορμική μετατροπή.

Για έναν εστιασμένο οδηγό μόνο για μετατροπή σε PDF, δείτε το [Export DWG to PDF tutorial](/java/cad-drawing-conversion/export-dwg-to-pdf/).

## Σύντομες απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Εξαγωγή αρχείων DWG σε PDF ή εικόνες raster χρησιμοποιώντας το Aspose.CAD for Java.  
- **Χρειάζομαι άδεια;** Μια δωρεάν προσωρινή άδεια είναι διαθέσιμη για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.  
- **Ποια έκδοση της Java υποστηρίζεται;** Οποιοδήποτε runtime Java 8+ λειτουργεί με το τελευταίο Aspose.CAD Java API.  
- **Μπορώ να μετατρέψω DWG σε άλλες μορφές εικόνας;** Ναι – οι ίδιες επιλογές rasterization σας επιτρέπουν να εξάγετε PNG, JPEG, BMP κ.λπ.  
- **Πόσο διαρκεί η μετατροπή;** Συνήθως λιγότερο από ένα δευτερόλεπτο για τυπικά σχέδια· μεγαλύτερα αρχεία μπορεί να χρειαστούν μερικά δευτερόλεπτα.

## Γιατί η βιβλιοθήκη Java CAD είναι η καλύτερη επιλογή για μετατροπή DWG;

Το Aspose.CAD for Java είναι η καλύτερη επιλογή επειδή παρέχει μια καθαρή υλοποίηση Java που δεν απαιτεί εγγενή DLLs, εντοπίζει αυτόματα τις μετρικές ή αυτοκρατορικές μονάδες, προσφέρει raster έξοδο έως 1200 DPI και δημιουργεί PDFs που διατηρούν τα διανύσματα χωρίς εξωτερικές εξαρτήσεις. Η βιβλιοθήκη προσφέρει επίσης ευέλικτο μοντέλο αδειοδότησης που σας επιτρέπει να ξεκινήσετε με προσωρινή άδεια και να κλιμακώσετε σε εταιρική χρήση.

## Τι είναι το “export dwg to pdf”;

`Export dwg pdf` είναι η διαδικασία μετατροπής ενός εγγενούς αρχείου σχεδίου DWG σε έγγραφο PDF ενώ διατηρούνται τα διανυσματικά δεδομένα, τα επίπεδα και η κλίμακα. Αυτή η μετατροπή παράγει ένα ανεξάρτητο από συσκευή αρχείο που μπορεί να προβληθεί σε οποιαδήποτε πλατφόρμα χωρίς την ανάγκη AutoCAD. Επειδή το PDF διατηρεί τις διανυσματικές πληροφορίες, το κείμενο παραμένει αναζητήσιμο και τα γραφικά παραμένουν καθαρά σε οποιοδήποτε επίπεδο ζουμ, καθιστώντας το ιδανικό για τεκμηρίωση, ανασκόπηση πελατών και αρχειοθέτηση.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD Java για αυτή τη μετατροπή;

Θα πρέπει να χρησιμοποιήσετε το Aspose.CAD Java επειδή η βιβλιοθήκη διαχειρίζεται εσωτερικά τη μετατροπή μονάδων, τη rasterization και την ενσωμάτωση PDF, εξαλείφοντας την ανάγκη για εργαλεία τρίτων ή πολύπλοκες γραμμές εντολών. Το API του είναι σχεδιασμένο για προγραμματιστές: ένα μόνο αντικείμενο `Image` αντιπροσωπεύει το σχέδιο, και μερικά αντικείμενα διαμόρφωσης σας επιτρέπουν να ρυθμίσετε DPI, μέγεθος σελίδας και συμπίεση. Το αποτέλεσμα είναι συνεπές, επαναλήψιμο output σε περιβάλλοντα Windows, Linux και macOS.

## Προαπαιτούμενα

- Βασικές γνώσεις προγραμματισμού Java.  
- Βιβλιοθήκη Aspose.CAD for Java εγκατεστημένη. Εάν δεν την έχετε κατεβάσει ακόμη, αποκτήστε την **[download Aspose.CAD for Java](https://releases.aspose.com/cad/java/)**.  
- Ένα αρχείο DWG για δοκιμή – το δείγμα **Bottom_plate.dwg** χρησιμοποιείται σε αυτόν τον οδηγό.  

## Εισαγωγή namespaces

Στο έργο Java, εισάγετε τις απαραίτητες κλάσεις για να ξεκινήσετε τη μετατροπή:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.UnitType;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του αρχείου DWG

Πρώτα, φορτώστε το σχέδιο DWG χρησιμοποιώντας την κλάση `Image`. Αυτό δημιουργεί μια αναπαράσταση στη μνήμη που το Aspose.CAD μπορεί να επεξεργαστεί.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

### Βήμα 2: Προσδιορισμός τύπου μονάδας

Η κατανόηση του αν το σχέδιο χρησιμοποιεί μετρικές ή αυτοκρατορικές μονάδες είναι ουσιώδης για σωστή κλιμάκωση. Η βοηθητική μέθοδος `IsMetric` (εφαρμογή παραλείπεται για συντομία) επιστρέφει μια λογική τιμή.

```java
Boolean currentUnitIsMetric = IsMetric(objImage.getUnitType());
int currentUnitCoefficient = objImage.getUnitType();
```

### Βήμα 3: Ορισμός επιλογών rasterization

Η κλάση `CadRasterizationOptions` ορίζει τις παραμέτρους rasterization όπως DPI, μέγεθος σελίδας και μετατροπή μονάδων. Βάσει του συστήματος μονάδων, διαμορφώστε το μέγεθος σελίδας, την κλίμακα και τον τύπο μονάδας προορισμού. Αυτές οι επιλογές καθορίζουν πώς το DWG θα rasterized πριν ενσωματωθεί σε PDF.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

if (currentUnitIsMetric) {
    // Metric units
    double metersCoeff = 1 / 1000.0;
    double scaleFactor = metersCoeff / currentUnitCoefficient;
    rasterizationOptions.setPageWidth((float)(210 * scaleFactor));
    rasterizationOptions.setPageHeight((float)(297 * scaleFactor));
    rasterizationOptions.setUnitType(UnitType.Millimeter);
} else {
    // Imperial units
    rasterizationOptions.setPageWidth((float)(8.27f / currentUnitCoefficient));
    rasterizationOptions.setPageHeight((float)(11.69f / currentUnitCoefficient));
    rasterizationOptions.setUnitType(UnitType.Inch);
}
```

### Βήμα 4: Διαμόρφωση επιλογών PDF (pdf options cad)

Η κλάση `PdfOptions` καθορίζει ρυθμίσεις ειδικές για PDF, συμπεριλαμβανομένης της συμπίεσης και των μεταδεδομένων. Δημιουργήστε ένα αντικείμενο `PdfOptions` και συνδέστε τις ρυθμίσεις rasterization. Αυτό ενημερώνει το Aspose.CAD πώς να ενσωματώσει το rasterized περιεχόμενο στο τελικό PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

### Βήμα 5: Αποθήκευση ως PDF

Η μέθοδος `save` γράφει την εικόνα στο καθορισμένο μονοπάτι αρχείου χρησιμοποιώντας τις παρεχόμενες επιλογές. Τέλος, εξάγετε το σχέδιο σε αρχείο PDF. Η μέθοδος `save` δέχεται το μονοπάτι εξόδου και το ρυθμισμένο `PdfOptions`.

```java
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

Όταν ολοκληρωθεί ο κώδικας, θα βρείτε **Saved.pdf** στον φάκελο `DWGDrawings`, έτοιμο για διανομή ή αρχειοθέτηση.

## Πώς να μετατρέψετε εικόνες raster DWG με τη βιβλιοθήκη Java CAD;

Μπορείτε να μετατρέψετε DWG σε μορφές raster αντικαθιστώντας το `PdfOptions` με μια κλάση επιλογών raster όπως `PngOptions` ή `JpegOptions`. Επαναχρησιμοποιήστε το ίδιο αντικείμενο `CadRasterizationOptions`, προσαρμόστε τη μορφή εξόδου και καλέστε τη μέθοδο `save` με το νέο αντικείμενο επιλογών. Αυτή η προσέγγιση σας επιτρέπει να δημιουργήσετε PNG, JPEG, BMP ή TIFF αρχεία με μία μόνο αλλαγή γραμμής, διατηρώντας τη ροή εργασίας συνεπή.

## Πώς να δημιουργήσετε PDF DWG χρησιμοποιώντας τις επιλογές PDF CAD;

Το παραπάνω παράδειγμα ήδη **generates pdf dwg** έξοδο. Για να βελτιώσετε το μέγεθος του PDF, ενεργοποιήστε τη συμπίεση καλώντας `pdfOptions.setCompress(true)`. Μπορείτε επίσης να ενσωματώσετε προσαρμοσμένα μεταδεδομένα, να ορίσετε την έκδοση PDF ή να προσθέσετε προστασία με κωδικό πρόσβασης μέσω πρόσθετων ιδιοτήτων `PdfOptions`. Αυτές οι ρυθμίσεις σας δίνουν πλήρη έλεγχο του τελικού PDF χωρίς να φύγετε από τον κώδικα Java.

## Συχνά προβλήματα & συμβουλές

- **Λανθασμένο μέγεθος σελίδας** – Ελέγξτε ξανά τη λογική μετατροπής μονάδων· μη ταιριαστοί συντελεστές μπορούν να παράγουν υπερμεγέθη σελίδες.  
- **Λείπουν γραμματοσειρές ή lineweights** – Βεβαιωθείτε ότι το DWG αναφέρει τυχόν εξωτερικούς πόρους πριν από τη μετατροπή.  
- **Απόδοση σε μεγάλα σχέδια** – Αυξήστε τη ρύθμιση `DPI` στο `CadRasterizationOptions` μόνο όταν απαιτείται υψηλότερη ποιότητα· χαμηλότερο DPI επιταχύνει την επεξεργασία.  
- **Ανησυχίες άδειας** – Για αξιολόγηση μπορείτε να χρησιμοποιήσετε μια **temporary license Aspose**· απαιτείται πλήρης άδεια για παραγωγικές εγκαταστάσεις.

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλα πλαίσια Java;**  
A: Ναι, το Aspose.CAD for Java ενσωματώνεται άψογα με δημοφιλή πλαίσια Java όπως το Spring, το Jakarta EE και το Android.

**Q: Διατίθεται προσωρινή άδεια για το Aspose.CAD for Java;**  
A: Ναι, μπορείτε να αποκτήσετε μια προσωρινή άδεια **[obtain a temporary license](https://purchase.aspose.com/temporary-license/)**.

**Q: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD for Java;**  
A: Επισκεφθείτε το **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** για βοήθεια από την κοινότητα και τους μηχανικούς της Aspose.

**Q: Πώς μπορώ να αγοράσω άδεια για το Aspose.CAD for Java;**  
A: Μπορείτε να αγοράσετε μια άδεια **[purchase a license](https://purchase.aspose.com/buy)**.

**Q: Ποιες μονάδες υποστηρίζει το Aspose.CAD for Java;**  
A: Το Aspose.CAD for Java υποστηρίζει τόσο μετρικές όσο και αυτοκρατορικές μονάδες, εντοπίζοντας αυτόματα το σύστημα μονάδων του σχεδίου.

**Q: Μπορώ να μετατρέψω DWG σε άλλες μορφές εικόνας (π.χ., PNG, JPEG) χρησιμοποιώντας το ίδιο API;**  
A: Απόλυτα. Αντικαταστήστε το `PdfOptions` με τις κατάλληλες επιλογές εικόνας raster (π.χ., `PngOptions`) και επαναχρησιμοποιήστε το ίδιο `CadRasterizationOptions`.

## Συμπέρασμα

Αυτό το tutorial έδειξε πώς να **export dwg pdf** και εικόνες raster χρησιμοποιώντας τη **java cad library** Aspose.CAD for Java. Ακολουθώντας τον οδηγό βήμα‑βήμα, μπορείτε να ενσωματώσετε αξιόπιστη μετατροπή CAD σε οποιαδήποτε εφαρμογή Java, είτε χρειάζεστε PDFs για τεκμηρίωση είτε εικόνες raster για προβολή στο web. Η καθαρή Java φύση της βιβλιοθήκης, η υψηλή ποιότητα εξόδου και η ευέλικτη αδειοδότηση την καθιστούν εξαιρετική επιλογή για μικρά εργαλεία αλλά και μεγάλες επιχειρησιακές γραμμές παραγωγής.

---

**Last Updated:** 2026-10-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose

## Σχετικά tutorials

- [Εξαγωγή DWG σε PDF: Συγκεκριμένη Διάταξη Χρησιμοποιώντας Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Εξαγωγή DWG σε PDF σε Java – Ορισμός Μεγέθους Σελίδας PDF με Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Εξαγωγή DWG σε PDF με Κρυφές Γραμμές – Aspose.CAD for Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}