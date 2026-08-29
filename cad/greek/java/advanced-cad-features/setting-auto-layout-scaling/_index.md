---
date: 2026-08-29
description: Μάθετε πώς να ορίσετε προσαρμοσμένο μέγεθος σελίδας pdf και να δημιουργήσετε
  PDF από CAD χρησιμοποιώντας το Aspose.CAD for Java. Αυτός ο οδηγός βήμα‑βήμα καλύπτει
  την εξαγωγή CAD σε PDF με Auto Layout Scaling.
keywords:
- custom pdf page size
- create pdf from cad
- dwg to pdf java
- custom page size pdf
- java convert cad pdf
lastmod: 2026-08-29
linktitle: Ρύθμιση Auto Layout Scaling
og_description: Ορίστε προσαρμοσμένο μέγεθος σελίδας pdf κατά τη μετατροπή αρχείων
  CAD σε PDF με το Aspose.CAD for Java. Ακολουθήστε τον οδηγό βήμα‑βήμα για να χρησιμοποιήσετε
  Auto Layout Scaling και να επιτύχετε τέλεια αποτελέσματα διάταξης.
og_image_alt: 'Tutorial: set custom pdf page size for CAD to PDF conversion using
  Aspose.CAD Java'
og_title: Ορίστε προσαρμοσμένο μέγεθος σελίδας pdf για εξαγωγή CAD PDF – Aspose.CAD
  Java
schemas:
- author: Aspose
  dateModified: '2026-08-29'
  description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  headline: How to set custom pdf page size for CAD PDF export
  type: TechArticle
- description: Learn how to set a custom pdf page size and create PDF from CAD using
    Aspose.CAD for Java. This step‑by‑step guide covers export CAD to PDF with Auto
    Layout Scaling.
  name: How to set custom pdf page size for CAD PDF export
  steps:
  - name: load the CAD file
    text: Loading the source file is the first step in **how to export CAD** to a
      PDF document.
  - name: create rasterization options
    text: The `CadRasterizationOptions` class defines how the CAD drawing is rasterized
      and which page dimensions to use. It also lets you control DPI, background color,
      and other rendering details.
  - name: set auto layout scaling
    text: Enable the automatic scaling feature. This is the core of **how to set scaling**
      for a CAD‑to‑PDF conversion.
  - name: create PDF options
    text: Link the rasterization settings to the PDF export options.
  - name: export to PDF
    text: Finally, save the rendered image as a PDF file. This step completes the
      **convert dxf to pdf** workflow. Repeat the steps above for any additional CAD
      files you need to process, whether they are **DWG**, **DWF**, or other supported
      formats.
  type: HowTo
- questions:
  - answer: Aspose.CAD for Java supports a broad range of formats, including DWG,
      DXF, DWF, and more than 30 additional CAD types.
    question: Is Aspose.CAD for Java compatible with all CAD file formats?
  - answer: Yes, the `CadRasterizationOptions` class provides properties for fine‑tuning
      scaling, DPI, background color, and other rasterization settings.
    question: Can I customize the scaling options further?
  - answer: Refer to the [documentation](https://reference.aspose.com/cad/java/) for
      in‑depth information and examples.
    question: Where can I find additional documentation for Aspose.CAD for Java?
  - answer: Yes, you can explore a [free trial](https://releases.aspose.com/) to experience
      the capabilities of Aspose.CAD for Java.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to connect
      with the community and seek support.
    question: How can I seek assistance or engage in discussions about Aspose.CAD
      for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- custom pdf page size
- Aspose.CAD
- Java CAD conversion
title: Πώς να ορίσετε προσαρμοσμένο μέγεθος σελίδας pdf για εξαγωγή CAD PDF
url: /el/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός προσαρμοσμένου μεγέθους σελίδας pdf – δημιουργία PDF από CAD με αυτόματη κλιμάκωση διάταξης

## Εισαγωγή

Αν χρειάζεστε να **ορίσετε προσαρμοσμένο μέγεθος σελίδας pdf** ενώ **δημιουργείτε PDF από CAD** αρχεία γρήγορα και με τέλεια κλιμάκωση, το Aspose.CAD for Java σας καλύπτει. Η Auto Layout Scaling αυτόματα αλλάζει το μέγεθος των διατάξεων CAD ώστε να γεμίζουν τις διαστάσεις της στόχευσης σελίδας, εξασφαλίζοντας ότι το παραγόμενο PDF ταιριάζει με το προοριζόμενο μέγεθος φύλλου ανεξαρτήτως του αρχικού σχεδίου. Σε αυτό το tutorial θα περάσουμε από τη διαδικασία – από τη φόρτωση ενός αρχείου DXF μέχρι την εξαγωγή PDF – τονίζοντας τις δυνατότητες **export CAD to PDF** της βιβλιοθήκης και δείχνοντας πώς μπορείτε επίσης να **μετατρέψετε DWG σε PDF** ή να **αυξήσετε την ανάλυση PDF** όταν χρειάζεται.

## Σύντομες απαντήσεις
- **Τι κάνει η Auto Layout Scaling;** Αυτόματα αλλάζει το μέγεθος των διατάξεων CAD ώστε να ταιριάζουν με τις διαστάσεις της στόχευσης σελίδας κατά τη rasterization.  
- **Ποια μορφές CAD μπορώ να μετατρέψω;** Οποιαδήποτε μορφή υποστηρίζεται από το Aspose.CAD (π.χ., DXF, DWG, DWF) μπορεί να μετατραπεί σε PDF.  
- **Χρειάζομαι άδεια για παραγωγή;** Ναι, απαιτείται εμπορική άδεια για μη‑αξιολογική χρήση.  
- **Πόσο διαρκεί μια τυπική μετατροπή;** Σε σύγχρονο υλικό ένα τυπικό αρχείο μετατρέπεται σε λιγότερο από ένα δευτερόλεπτο.  
- **Μπορώ να αλλάξω το μέγεθος της σελίδας;** Απόλυτα – χρησιμοποιήστε `CadRasterizationOptions` για να ορίσετε προσαρμοσμένες διαστάσεις σελίδας.

## Τι σημαίνει «δημιουργία PDF από CAD»;
Η δημιουργία PDF από CAD σημαίνει τη λήψη ενός διανυσματικού (vector‑based) σχεδίου μηχανικής (DXF, DWG, κ.λπ.) και η rasterization του σε έγγραφο PDF. Το PDF διατηρεί την οπτική πιστότητα του αρχικού σχεδίου ενώ είναι ευρέως προβλέψιμο σε οποιαδήποτε πλατφόρμα, και μπορεί να ανοιχθεί σε συσκευές που δεν υποστηρίζουν εγγενείς μορφές CAD.

## Γιατί να χρησιμοποιήσετε αυτόματη κλιμάκωση διάταξης;
Η Auto Layout Scaling εγγυάται ότι κάθε διάταξη καταλαμβάνει πλήρως τη σελίδα PDF χωρίς χειροκίνητους υπολογισμούς, εξοικονομώντας χρόνο και εξαλείφοντας σφάλματα κλιμάκωσης. Επίσης διασφαλίζει ότι τα πάχη γραμμών και τα χρώματα διατηρούνται ακριβώς σε διαφορετικά μεγέθη εξόδου. Παρέχει συνεπή, υψηλής ποιότητας έξοδο σε δεκάδες αρχεία CAD και υποστηρίζει επεξεργασία παρτίδας για μεγάλα έργα.

## Προαπαιτούμενα

1. **Aspose.CAD for Java Library** – κατεβάστε την τελευταία έκδοση από τη [download page](https://releases.aspose.com/cad/java/).  
2. **Resource directory** – δημιουργήστε έναν φάκελο στον υπολογιστή σας για αποθήκευση αρχείων CAD· αντικαταστήστε το `"Your Document Directory"` στον κώδικα με αυτή τη διαδρομή.  
3. **Sample CAD file** – για αυτόν τον οδηγό θα χρησιμοποιήσουμε το `conic_pyramid.dxf`, το οποίο περιλαμβάνεται στο σύνολο δείγματος δεδομένων του Aspose.

## Εισαγωγή ονοματοχώρων

Αρχικά, εισάγετε τις απαιτούμενες κλάσεις. Αυτό μας δίνει πρόσβαση σε λειτουργίες φόρτωσης εικόνας, rasterization και εξαγωγής PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Πώς να ορίσετε προσαρμοσμένο μέγεθος σελίδας για PDF από CAD

Πριν βουτήξουμε στον κώδικα βήμα‑βήμα, ας διευκρινίσουμε γιατί οι προσαρμοσμένες διαστάσεις σελίδας έχουν σημασία. Ο ορισμός ενός **custom pdf page size** σας επιτρέπει να ταιριάξετε με τα πρότυπα μεγέθη φύλλων της βιομηχανίας (A4, A1, Letter) ή να ορίσετε ένα προσαρμοσμένο καμβά, κάτι που είναι απαραίτητο για κανονιστικές υποβολές, τεχνικά εγχειρίδια ή εργασίες εκτύπωσης υψηλής ανάλυσης.

### Βήμα 1: φόρτωση του αρχείου CAD

Η φόρτωση του αρχείου προέλευσης είναι το πρώτο βήμα στο **how to export CAD** σε ένα έγγραφο PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Βήμα 2: δημιουργία επιλογών rasterization

Η κλάση `CadRasterizationOptions` ορίζει πώς γίνεται η rasterization του σχεδίου CAD και ποιες διαστάσεις σελίδας θα χρησιμοποιηθούν. Επίσης σας επιτρέπει να ελέγξετε το DPI, το χρώμα φόντου και άλλες λεπτομέρειες απόδοσης.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Βήμα 3: ορισμός αυτόματης κλιμάκωσης διάταξης

Ενεργοποιήστε τη λειτουργία αυτόματης κλιμάκωσης. Αυτό είναι το κεντρικό στοιχείο του **how to set scaling** για μετατροπή CAD‑σε‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Βήμα 4: δημιουργία επιλογών PDF

Συνδέστε τις ρυθμίσεις rasterization με τις επιλογές εξαγωγής PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 5: εξαγωγή σε PDF

Τέλος, αποθηκεύστε την αποδομημένη εικόνα ως αρχείο PDF. Αυτό το βήμα ολοκληρώνει τη ροή εργασίας **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Επαναλάβετε τα παραπάνω βήματα για τυχόν επιπλέον αρχεία CAD που χρειάζεται να επεξεργαστείτε, είτε είναι **DWG**, **DWF**, ή άλλες υποστηριζόμενες μορφές.

## Συνηθισμένες περιπτώσεις χρήσης

| Σενάριο | Γιατί να ορίσετε προσαρμοσμένο μέγεθος σελίδας; |
|----------|----------------------------------------------|
| **Construction drawing submission** | Ευθυγραμμίζει το PDF με τα τυπικά μεγέθη φύλλων A1/A2 που απαιτούνται από τις ρυθμιστικές αρχές. |
| **Embedding in technical manuals** | Εξασφαλίζει ότι το σχέδιο ταιριάζει με την προκαθορισμένη διάταξη του εγχειριδίου χωρίς επιπλέον κλιμάκωση. |
| **High‑resolution printing** | Σας επιτρέπει να αυξήσετε το DPI (π.χ., `rasterizationOptions.setResolution(300)`) διατηρώντας σταθερές τις διαστάσεις της σελίδας. |

## Συνηθισμένα προβλήματα & αντιμετώπιση

| Σύμπτωμα | Πιθανή αιτία | Διόρθωση |
|---------|--------------|----------|
| Κενό PDF | Οι επιλογές rasterization δεν έχουν οριστεί ή η διαδρομή αρχείου είναι λανθασμένη | Επαληθεύστε τη διαδρομή `srcFile` και βεβαιωθείτε ότι `setPageWidth/Height` δεν είναι μηδενικά |
| Παραμορφωμένη κλιμάκωση | `setAutomaticLayoutsScaling` παραμένει `false` | Ενεργοποιήστε την αυτόματη κλιμάκωση ή υπολογίστε χειροκίνητα τον παράγοντα κλιμάκωσης |
| Ελλιπείς στρώσεις | Το αρχικό DXF περιέχει μη υποστηριζόμενες οντότητες | Ελέγξτε τις σημειώσεις έκδοσης του Aspose.CAD για τις υποστηριζόμενες οντότητες |

Το Aspose.CAD υποστηρίζει τη μετατροπή **30+ μορφών CAD** και μπορεί να επεξεργαστεί αρχεία έως **500 MB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, παρέχοντας γρήγορες, μνημονικά αποδοτικές μετατροπές για επιχειρησιακά φορτία εργασίας.

## Συχνές ερωτήσεις

**Q: Είναι το Aspose.CAD for Java συμβατό με όλες τις μορφές αρχείων CAD;**  
A: Το Aspose.CAD for Java υποστηρίζει ένα ευρύ φάσμα μορφών, συμπεριλαμβανομένων των DWG, DXF, DWF, και περισσότερων από 30 επιπλέον τύπων CAD.

**Q: Μπορώ να προσαρμόσω περαιτέρω τις επιλογές κλιμάκωσης;**  
A: Ναι, η κλάση `CadRasterizationOptions` παρέχει ιδιότητες για λεπτομερή ρύθμιση της κλιμάκωσης, DPI, χρώματος φόντου και άλλων ρυθμίσεων rasterization.

**Q: Πού μπορώ να βρω πρόσθετη τεκμηρίωση για το Aspose.CAD for Java;**  
A: Ανατρέξτε στην [documentation](https://reference.aspose.com/cad/java/) για λεπτομερείς πληροφορίες και παραδείγματα.

**Q: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD for Java;**  
A: Ναι, μπορείτε να δοκιμάσετε μια [free trial](https://releases.aspose.com/) για να γνωρίσετε τις δυνατότητες του Aspose.CAD for Java.

**Q: Πώς μπορώ να ζητήσω βοήθεια ή να συμμετάσχω σε συζητήσεις σχετικά με το Aspose.CAD for Java;**  
A: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για να συνδεθείτε με την κοινότητα και να ζητήσετε υποστήριξη.

**Πρόσθετες συχνές ερωτήσεις**

**Q: Πώς μετατρέπω ένα αρχείο DWG σε PDF αντί για DXF;**  
A: Ο ίδιος κώδικας λειτουργεί· απλώς αλλάξτε την επέκταση αρχείου στο `srcFile` σε `.dwg`.

**Q: Μπορώ να ορίσω προσαρμοσμένο DPI για PDF υψηλότερης ανάλυσης;**  
A: Ναι, χρησιμοποιήστε `rasterizationOptions.setResolution(300);` (ή οποιοδήποτε DPI χρειάζεστε).

**Q: Είναι δυνατόν να ενσωματωθούν γραμματοσειρές στο παραγόμενο PDF;**  
A: Το Aspose.CAD rasterizes το σχέδιο, έτσι οι γραμματοσειρές αποδίδονται ως διανύσματα· δεν απαιτείται ξεχωριστή ενσωμάτωση γραμματοσειρών.

## Συμπέρασμα

Ακολουθώντας αυτόν τον οδηγό, γνωρίζετε πλέον πώς να **ορίσετε προσαρμοσμένο μέγεθος pdf σελίδας** και να **δημιουργήσετε PDF από CAD** αρχεία χρησιμοποιώντας το Aspose.CAD for Java με Auto Layout Scaling. Η διαδικασία απλοποιεί τη ροή εργασίας **export CAD to PDF**, εξασφαλίζει συνεπή κλιμάκωση και σας εξοικονομεί πολύτιμο χρόνο ανάπτυξης. Μη διστάσετε να πειραματιστείτε με διαφορετικά μεγέθη σελίδας, αναλύσεις και μορφές CAD για να ταιριάξουν στις ανάγκες του έργου σας, είτε **μετατρέπετε DWG σε PDF**, **αυξάνετε την ανάλυση PDF**, είτε δημιουργείτε έναν **java CAD to PDF** επεξεργαστή παρτίδας.

---

**Τελευταία ενημέρωση:** 2026-08-29  
**Δοκιμή με:** Aspose.CAD for Java 24.12 (latest)  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Πώς να ορίσετε το μέγεθος σελίδας PDF και να ενεργοποιήσετε την παρακολούθηση για τη διαδικασία απόδοσης CAD χρησιμοποιώντας Aspose.CAD for Java](/cad/java/advanced-cad-features/enable-tracking-for-cad-rendering-process/)
- [Ορισμός μεγέθους σελίδας PDF – Μετατροπή CAD σε PDF (Java)](/cad/java/advanced-cad-features/set-canvas-size-and-mode/)
- [Γρήγορη εξαγωγή DWG σε PDF ή raster χρησιμοποιώντας τη βιβλιοθήκη java cad Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}