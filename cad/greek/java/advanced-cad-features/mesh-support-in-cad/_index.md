---
date: 2026-09-24
description: Μάθετε πώς να δημιουργείτε PDF από αρχεία DWG χρησιμοποιώντας το Aspose.CAD
  for Java. Μετατρέψτε DWG σε PDF εύκολα με υποστήριξη mesh.
keywords:
- create pdf from dwg
- export dwg as pdf
- generate pdf from cad
- how to convert dwg pdf
- pdf generation from cad
lastmod: 2026-09-24
linktitle: Υποστήριξη mesh στο CAD
og_description: Δημιουργήστε PDF από DWG με το Aspose.CAD for Java σε δευτερόλεπτα.
  Αυτός ο οδηγός δείχνει τη μετατροπή με υποστήριξη mesh, τις προαπαιτήσεις, κώδικα
  βήμα‑βήμα και συμβουλές αντιμετώπισης προβλημάτων.
og_image_alt: Developer guide showing DWG to PDF conversion with Aspose.CAD for Java
og_title: Πώς να δημιουργήσετε PDF από DWG με Aspose.CAD for Java
schemas:
- author: Aspose
  dateModified: '2026-09-24'
  description: Learn how to create PDF from DWG files using Aspose.CAD for Java. Convert
    DWG to PDF effortlessly with mesh support.
  headline: How to create PDF from DWG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to create PDF from DWG files using Aspose.CAD for Java. Convert
    DWG to PDF effortlessly with mesh support.
  name: How to create PDF from DWG with Aspose.CAD for Java
  steps:
  - name: Set up the project
    text: Create a new Java project (or add to an existing one) and add the Aspose.CAD
      JAR to the project’s classpath. Define a base directory that will hold your
      source DWG and the generated PDF.
  - name: Define file paths
    text: Specify where the input DWG lives and where the output PDF should be written.
  - name: Load the CAD image
    text: '`CadImage` loads the DWG file into memory so that Aspose.CAD can work with
      its internal structure.'
  - name: Configure rasterization options
    text: '`RasterizationOptions` controls the size and layout of the generated PDF
      pages. The `Layouts` array tells Aspose.CAD to render the **Model** space, which
      includes mesh entities.'
  - name: Set PDF options
    text: '`PdfOptions` attaches the rasterization settings to the PDF export process,
      ensuring the defined options are applied when the file is saved.'
  - name: Save the PDF
    text: Finally, call the `save` method on the loaded `CadImage` instance to write
      a PDF file. The resulting document will contain a faithful representation of
      the original DWG, including any mesh geometry.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is designed for both personal and commercial
      projects. Licensing details are available on the [purchase page](https://purchase.aspose.com/buy).
    question: Is Aspose.CAD for Java suitable for commercial use?
  - answer: Obtain a temporary license from the [temporary license page](https://purchase.aspose.com/temporary-license/)
      for evaluation without cost.
    question: How can I get a temporary license for testing purposes?
  - answer: Visit the Aspose.CAD dedicated forum on [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19)
      for community assistance.
    question: Where can I find community support for Aspose.CAD for Java?
  - answer: Yes, Aspose.CAD for Java supports PNG, JPEG, BMP, and more. See the product
      documentation for the full list.
    question: Are there other output formats supported besides PDF?
  - answer: A free trial version is available at the [Aspose.CAD free trial download](https://releases.aspose.com/).
    question: Can I try Aspose.CAD for Java for free?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg
- aspose.cad
- java pdf generation
title: Πώς να δημιουργήσετε PDF από DWG με Aspose.CAD for Java
url: /el/java/advanced-cad-features/mesh-support-in-cad/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να δημιουργήσετε PDF από DWG με Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε **πώς να δημιουργήσετε PDF από DWG** αρχεία χρησιμοποιώντας το Aspose.CAD για Java. Η υποστήριξη πλεγμάτων της βιβλιοθήκης σας επιτρέπει να μετατρέψετε πολύπλοκα σχέδια CAD—συμπεριλαμβανομένων εκείνων που περιέχουν 3‑D πλέγματα—απευθείας σε PDF χωρίς να χάσετε λεπτομέρειες. Είτε χρειάζεστε **να μετατρέψετε DWG σε PDF** για αναφορές, αρχειοθέτηση ή επεξεργασία downstream, τα παρακάτω βήματα θα σας καθοδηγήσουν σε μια αξιόπιστη, έτοιμη για παραγωγή λύση. Αυτός ο οδηγός δείχνει επίσης πώς να **εξάγετε DWG ως PDF** και ακόμη **να δημιουργήσετε PDF από CAD** όταν χρειάζεστε υψηλής ποιότητας τεκμηρίωση.

## Γρήγορες απαντήσεις
- **Τι καλύπτει το tutorial;** Μετατροπή ενός αρχείου DWG που περιέχει πλέγματα σε PDF χρησιμοποιώντας το Aspose.CAD για Java.  
- **Χρειάζομαι άδεια;** Μια προσωρινή άδεια λειτουργεί για δοκιμές· απαιτείται πλήρης άδεια για εμπορική χρήση.  
- **Ποια έκδοση της Java υποστηρίζεται;** Java 8 ή νεότερη.  
- **Μπορώ να εξάγω άλλες μορφές;** Ναι – το Aspose.CAD υποστηρίζει επίσης PNG, JPEG, BMP και άλλα.  
- **Πόσο διαρκεί η μετατροπή;** Συνήθως κάτω από ένα δευτερόλεπτο για τυπικά σχέδια.

## Γιατί να δημιουργήσετε PDF από DWG;

Η δημιουργία PDF από αρχείο DWG παρέχει μια καθολικά προσβάσιμη μορφή που διατηρεί την οπτική πιστότητα του αρχικού σχεδίου. Τα PDF μπορούν να προβληθούν σε οποιαδήποτε συσκευή χωρίς εξειδικευμένο λογισμικό CAD, υποστηρίζουν αναζητήσιμο κείμενο και διατηρούν ακριβή κλίμακα και πάχη γραμμών, καθιστώντας τα ιδανικά για τεκμηρίωση, κοινή χρήση και μακροπρόθεσμη αρχειοθέτηση.

* **Αυτοματοποιημένες αναφορές** – ενσωματώστε τεχνικά σχέδια σε PDF αναφορές χωρίς να απαιτείται λογισμικό CAD στην πλευρά του θεατή.  
* **Αρχειοθέτηση εγγράφων** – αποθηκεύστε σχέδια σε μια σταθερή, αναζητήσιμη μορφή για μακροπρόθεσμη διατήρηση.  
* **Web services** – εκθέστε ένα API που δέχεται μεταφορτώσεις DWG και επιστρέφει PDF, ένα κοινό μοτίβο για πλατφόρμες SaaS που χρειάζονται **να μετατρέπουν CAD σε PDF** άμεσα.  

Η υποστήριξη πλεγμάτων του Aspose.CAD εξασφαλίζει ότι ακόμη και πολύπλοκη 3‑D γεωμετρία αναπαράγεται πιστά στο τελικό PDF.

## Προαπαιτούμενα

- **Περιβάλλον ανάπτυξης Java:** JDK 8 ή νεότερο εγκατεστημένο στο μηχάνημά σας.  
- **Βιβλιοθήκη Aspose.CAD για Java:** Κατεβάστε το τελευταίο JAR από το [download link](https://releases.aspose.com/cad/java/).  
- **Έγγραφο με πλέγματα:** Ένα αρχείο DWG που περιέχει δεδομένα πλέγματος (π.χ., `meshes.dwg`).  

## Εισαγωγή χώρων ονομάτων

`CadImage` είναι η βασική κλάση του Aspose.CAD που αντιπροσωπεύει ένα σχέδιο CAD φορτωμένο στη μνήμη. `RasterizationOptions` ορίζει πώς τα διανυσματικά δεδομένα rasterize (αποδοθούν) σε μια σελίδα, συμπεριλαμβανομένων DPI και διάταξης. `PdfOptions` περιβάλλει τις ρυθμίσεις rasterization και λέει στη βιβλιοθήκη να παράγει έξοδο PDF.

Στο αρχείο πηγαίου κώδικα Java, συμπεριλάβετε τις απαιτούμενες κλάσεις του Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Ρύθμιση του έργου

Δημιουργήστε ένα νέο έργο Java (ή προσθέστε σε υπάρχον) και προσθέστε το JAR του Aspose.CAD στο classpath του έργου. Ορίστε έναν βασικό φάκελο που θα περιέχει το πηγαίο DWG και το παραγόμενο PDF.

### Βήμα 2: Ορισμός διαδρομών αρχείων

Καθορίστε πού βρίσκεται το εισερχόμενο DWG και πού πρέπει να γραφτεί το εξαγόμενο PDF.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "meshes.dwg";
String outPath = dataDir + "meshes.pdf";
```

### Βήμα 3: Φόρτωση της εικόνας CAD

`CadImage` φορτώνει το αρχείο DWG στη μνήμη ώστε το Aspose.CAD να μπορεί να εργαστεί με την εσωτερική του δομή.

```java
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

### Βήμα 4: Διαμόρφωση επιλογών rasterization

`RasterizationOptions` ελέγχει το μέγεθος και τη διάταξη των παραγόμενων σελίδων PDF. Ο πίνακας `Layouts` λέει στο Aspose.CAD να αποδώσει το χώρο **Model**, που περιλαμβάνει οντότητες πλέγματος.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[] { "Model" });
```

### Βήμα 5: Ορισμός επιλογών PDF

`PdfOptions` συνδέει τις ρυθμίσεις rasterization με τη διαδικασία εξαγωγής PDF, εξασφαλίζοντας ότι οι καθορισμένες επιλογές εφαρμόζονται κατά την αποθήκευση του αρχείου.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 6: Αποθήκευση του PDF

Τέλος, καλέστε τη μέθοδο `save` στο φορτωμένο αντικείμενο `CadImage` για να γράψετε ένα αρχείο PDF. Το προκύπτον έγγραφο θα περιέχει μια πιστή αναπαράσταση του αρχικού DWG, συμπεριλαμβανομένης οποιασδήποτε γεωμετρίας πλέγματος.

```java
cadImage.save(outPath, pdfOptions);
```

#### Γιατί αυτό λειτουργεί για μετατροπή CAD σε PDF

Το Aspose.CAD εκτελεί rasterization βασισμένο σε διανύσματα, διατηρώντας τα πάχη γραμμών, τα χρώματα και τις λεπτομέρειες 3‑D πλέγματος. Διαμορφώνοντας τις επιλογές rasterization ελέγχετε την ανάλυση και τη διάταξη, εξασφαλίζοντας ότι η **εξαγωγή DWG ως PDF** φαίνεται ακριβώς όπως προορίζεται στο PDF.

## Πώς να μετατρέψετε DWG σε PDF με Aspose.CAD;

Για να μετατρέψετε ένα αρχείο DWG σε PDF με το Aspose.CAD, φορτώστε το σχέδιο χρησιμοποιώντας `CadImage.load`, διαμορφώστε `CadRasterizationOptions` για να καθορίσετε τη διάταξη μοντέλου και τις διαστάσεις σελίδας, τυλίξτε αυτές τις ρυθμίσεις σε ένα αντικείμενο `PdfOptions` και, στη συνέχεια, καλέστε `save` με το επιθυμητό όνομα αρχείου PDF. Αυτή η ακολουθία εξασφαλίζει ότι τα δεδομένα πλέγματος αποδίδονται σωστά.

Φορτώστε το αρχείο DWG χρησιμοποιώντας `CadImage.load("input.dwg")`, διαμορφώστε `RasterizationOptions` με `Layouts = new String[]{"Model"}`, τυλίξτε αυτές τις ρυθμίσεις σε ένα αντικείμενο `PdfOptions` και καλέστε `cadImage.save("output.pdf", pdfOptions)`. Αυτή η προσέγγιση μιας γραμμής‑συν‑ρύθμιση μετατρέπει οποιοδήποτε DWG πλούσιο σε πλέγματα σε PDF υψηλής ποιότητας σε κάτω από ένα δευτερόλεπτο σε τυπικό υλικό.

## Συνηθισμένες περιπτώσεις χρήσης

- **Αυτοματοποιημένες αναφορές:** Δημιουργία PDF αναφορών από τεχνικά σχέδια άμεσα.  
- **Αρχειοθέτηση εγγράφων:** Αποθήκευση σχεδίων CAD ως PDF για μακροπρόθεσμη διατήρηση.  
- **Web services:** Εκθέστε ένα API που δέχεται μεταφορτώσεις DWG και επιστρέφει PDF, χρήσιμο για πλατφόρμες SaaS.  

## Συμβουλές αντιμετώπισης προβλημάτων

- **Απουσία πλεγμάτων στην έξοδο:** Επαληθεύστε ότι η ιδιότητα `Layouts` περιλαμβάνει το `"Model"`· τα πλέγματα συχνά αποθηκεύονται στο χώρο μοντέλου.  
- **Λανθασμένη κλιμάκωση:** Προσαρμόστε το `PageWidth` και το `PageHeight` ώστε να ταιριάζουν με τις φυσικές μονάδες του σχεδίου.  
- **Σφάλματα άδειας:** Βεβαιωθείτε ότι έχετε καλέσει `License.setLicense()` με ένα έγκυρο αρχείο άδειας πριν φορτώσετε την εικόνα.  
- **dwg to pdf aspose specific issue:** Εάν αντιμετωπίσετε σφάλμα που δηλώνει ότι μια συγκεκριμένη έκδοση DWG δεν υποστηρίζεται, βεβαιωθείτε ότι χρησιμοποιείτε την πιο πρόσφατη έκδοση του Aspose.CAD (ο σύνδεσμος λήψης παραπάνω οδηγεί πάντα στην πιο πρόσφατη έκδοση).  

## Συχνές ερωτήσεις

**Q: Είναι το Aspose.CAD για Java κατάλληλο για εμπορική χρήση;**  
A: Ναι, το Aspose.CAD για Java έχει σχεδιαστεί τόσο για προσωπικά όσο και για εμπορικά έργα. Οι λεπτομέρειες αδειοδότησης διατίθενται στη [purchase page](https://purchase.aspose.com/buy).

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για δοκιμαστικούς σκοπούς;**  
A: Αποκτήστε μια προσωρινή άδεια από τη [temporary license page](https://purchase.aspose.com/temporary-license/) για αξιολόγηση χωρίς κόστος.

**Q: Πού μπορώ να βρω υποστήριξη κοινότητας για το Aspose.CAD για Java;**  
A: Επισκεφθείτε το αφιερωμένο φόρουμ του Aspose.CAD στο [https://forum.aspose.com/c/cad/19](https://forum.aspose.com/c/cad/19) για βοήθεια από την κοινότητα.

**Q: Υπάρχουν άλλες μορφές εξόδου εκτός του PDF;**  
A: Ναι, το Aspose.CAD για Java υποστηρίζει PNG, JPEG, BMP και άλλα. Δείτε την τεκμηρίωση προϊόντος για την πλήρη λίστα.

**Q: Μπορώ να δοκιμάσω το Aspose.CAD για Java δωρεάν;**  
A: Μια δωρεάν έκδοση δοκιμής είναι διαθέσιμη στη [Aspose.CAD free trial download](https://releases.aspose.com/).

---

**Τελευταία ενημέρωση:** 2026-09-24  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.11  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Μετατροπή CAD σε PDF – Ορισμός μεγέθους καμβά και προχωρημένες λειτουργίες με Aspose.CAD για Java](/cad/java/advanced-cad-features/)
- [Εξαγωγή DWG σε PDF: Συγκεκριμένη διάταξη χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Εξαγωγή DWG σε PDF με κρυφές γραμμές – Aspose.CAD για Java](/cad/java/cad-text-and-formatting/support-hidden-lines-in-dwg/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}