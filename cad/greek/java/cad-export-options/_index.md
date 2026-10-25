---
date: 2026-10-25
description: Μάθετε πώς να μετατρέψετε DWG σε PDF, να εξάγετε διατάξεις CAD, αρχεία
  BMP, IFC και STL χρησιμοποιώντας το Aspose.CAD for Java. Περιλαμβάνει σημειώσεις
  αδειοδότησης, συμβουλές απόδοσης και πραγματικές περιπτώσεις χρήσης.
keywords:
- convert dwg to pdf
- cad layout pdf export
- generate pdf from dwg
- java convert cad pdf
- export stl to png
lastmod: 2026-10-25
linktitle: Επιλογές Εξαγωγής CAD
og_description: Μετατρέψτε DWG σε PDF, BMP, IFC και STL με το Aspose.CAD for Java.
  Μάθετε βήμα‑βήμα, δείτε αριθμούς απόδοσης και λάβετε οδηγίες αδειοδότησης σε αυτόν
  τον οδηγό του 2026.
og_image_alt: Screenshot of Aspose.CAD Java API converting DWG to PDF
og_title: Μετατροπή DWG σε PDF και άλλες επιλογές εξαγωγής CAD σε Java
schemas:
- author: Aspose
  dateModified: '2026-10-25'
  description: Learn how to convert DWG to PDF, export CAD layouts, BMP, IFC, and
    STL files using Aspose.CAD for Java. Includes licensing notes, performance tips,
    and real‑world use cases.
  headline: How to convert DWG to PDF and other CAD export options in Java
  type: TechArticle
- questions:
  - answer: Load the IFC file with `Image.load("model.ifc")` and call `save("model.png",
      new PngOptions())`.
    question: How do I convert IFC to PNG using Aspose.CAD?
  - answer: Yes—Aspose.CAD treats layouts as images internally, so `save("layout.pdf",
      new PdfOptions())` handles it automatically.
    question: Can I export a CAD layout directly to PDF without converting to an image
      first?
  - answer: Exporting an AutoCAD drawing converts the entire drawing, while exporting
      a layout targets a specific paper‑space view, preserving its page settings.
    question: What is the difference between exporting AutoCAD to PDF and exporting
      a CAD layout to PDF?
  - answer: No inherent limit; each layout becomes a separate page in the resulting
      PDF.
    question: Is there a limit on the number of pages when exporting a multi‑sheet
      DWG to PDF?
  - answer: A single Aspose.CAD license covers all supported formats (PDF, PNG, BMP,
      etc.).
    question: Do I need a separate license for each export format?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- convert dwg to pdf
- Aspose.CAD
- Java CAD conversion
- CAD export tutorials
title: Πώς να μετατρέψετε DWG σε PDF και άλλες επιλογές εξαγωγής CAD σε Java
url: /el/java/cad-export-options/
weight: 30
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Επιλογές εξαγωγής CAD

## Εισαγωγή

Αν είστε προγραμματιστής Java που χρειάζεται να **μετατρέψετε DWG σε PDF** γρήγορα και αξιόπιστα, βρίσκεστε στο σωστό μέρος. Αυτός ο οδηγός περιγράφει τα πιο συνηθισμένα σενάρια εξαγωγής του Aspose.CAD for Java — συμπεριλαμβανομένων εικόνων AutoCAD, διατάξεων CAD, BMP, PDF, IFC και αρχείων STL. Θα δείτε γιατί αυτές οι δυνατότητες είναι σημαντικές σε πραγματικά έργα, θα μάθετε συμβουλές βέλτιστων πρακτικών και θα έχετε έτοιμα αποσπάσματα κώδικα για να τα αντιγράψετε στις δικές σας εφαρμογές.

## Γρήγορες απαντήσεις
- **Ποιος είναι ο πιο απλός τρόπος για να εξάγετε AutoCAD σε PDF;** Χρησιμοποιήστε `Image.save("output.pdf", new PdfOptions())` από το Aspose.CAD.  
- **Σε ποιες μορφές μπορώ να μετατρέψω αρχεία IFC;** Η PNG υποστηρίζεται πλήρως· απλώς φορτώστε το αρχείο IFC και αποθηκεύστε το ως PNG.  
- **Μπορώ να εξάγω αρχεία STL απευθείας σε PNG;** Ναι· φορτώστε το μοντέλο STL και καλέστε `save("image.png")`.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια για μη‑δοκιμαστικές εγκαταστάσεις.  
- **Ποια έκδοση της Java απαιτείται;** Συνιστάται Java 8 ή νεότερη.

## Τι είναι η εξαγωγή AutoCAD σε PDF;

Η εξαγωγή σχεδίων AutoCAD σε PDF σημαίνει τη μετατροπή αρχείων DWG/DXF βασισμένων σε διανύσματα σε μια ευρέως αποδεκτή, προσανατολισμένη σε σελίδες μορφή. Το PDF διατηρεί τα επίπεδα, τα βάρη γραμμών και τα χρώματα, καθιστώντας το ιδανικό για την κοινή χρήση σχεδίων με πελάτες, αξιολογητές ή συστήματα κατώτερης αλυσίδας που δεν κατανοούν τα εγγενή αρχεία CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD for Java;

Το Aspose.CAD for Java είναι μια βιβλιοθήκη **pure‑Java** — δεν απαιτούνται εγγενή DLL ή COM interop. Αναπαράγει γεωμετρία, κείμενο και δεδομένα raster με **υψηλή πιστότητα**, υποστηρίζει **επεξεργασία δέσμης** χιλιάδων αρχείων και διαχειρίζεται **πάνω από 60 μορφές εισόδου και εξόδου** (συμπεριλαμβανομένων DWG, DXF, IFC, STL, BMP, PNG και PDF). Η αποδοτική μνήμη pipeline της βιβλιοθήκης σας επιτρέπει να επεξεργάζεστε σχέδια με εκατοντάδες σελίδες χωρίς να φορτώνετε ολόκληρο το αρχείο στη RAM.

## Γιατί είναι σημαντικό

Η δυνατότητα **μετατροπής DWG σε PDF** σε πραγματικό χρόνο σας επιτρέπει να αυτοματοποιήσετε τη δημιουργία αναφορών, να δημιουργήσετε παραδοτέα έτοιμα για πελάτες και να ενσωματώσετε δεδομένα CAD σε διαδικτυακές πύλες χωρίς να εκθέτετε τα ακατέργαστα αρχεία DWG. Το ίδιο API δημιουργεί επίσης εξαγωγές βασισμένες σε εικόνες (BMP, PNG) για μικρογραφίες, γρήγορους οπτικούς ελέγχους και ελαφριές προεπισκοπήσεις.

## Προαπαιτούμενα
- Java 8 ή νεότερη εγκατεστημένη.  
- Βιβλιοθήκη Aspose.CAD for Java προστέθηκε στο έργο σας (Maven, Gradle ή χειροκίνητο JAR).  
- Έγκυρη άδεια Aspose για παραγωγική χρήση (διατίθεται δωρεάν δοκιμή για αξιολόγηση).

## Πώς να μετατρέψετε DWG σε PDF σε Java

`Image` είναι η κύρια κλάση του Aspose.CAD που αντιπροσωπεύει ένα έγγραφο CAD στη μνήμη.  
`PdfOptions` ρυθμίζει τις ρυθμίσεις εξόδου ειδικές για PDF όπως η ανάλυση και η συμπίεση.

Φορτώστε το DWG (ή οποιαδήποτε υποστηριζόμενη μορφή CAD) με `Image.load`, στη συνέχεια καλέστε `save` χρησιμοποιώντας μια παρουσία `PdfOptions`. Αυτό το μοτίβο δύο βημάτων διαχειρίζεται τη μετατροπή vector‑σε‑PDF, διατηρεί τα επίπεδα και σας επιτρέπει να ρυθμίσετε το DPI ή τις ρυθμίσεις συμπίεσης.

Η κλάση `Image` αντιπροσωπεύει οποιοδήποτε υποστηριζόμενο έγγραφο CAD στη μνήμη, ενώ το `PdfOptions` ρυθμίζει το PDF εξόδου. Δεν απαιτούνται επιπλέον εργαλεία μετατροπής ή εξωτερικά βοηθήματα.

### Βήμα 1: φόρτωση του αρχείου DWG
```java
// Load a DWG file – the Image class is the entry point for all Aspose.CAD operations
com.aspose.cad.Image cadImage = com.aspose.cad.Image.load("sample.dwg");
```

### Βήμα 2: ρύθμιση επιλογών PDF (προαιρετικό)
```java
// Create PDF options – you can set vector rasterization DPI, compression, etc.
com.aspose.cad.imageoptions.PdfOptions pdfOptions = new com.aspose.cad.imageoptions.PdfOptions();
pdfOptions.setVectorRasterizationOptions(
    new com.aspose.cad.imageoptions.VectorRasterizationOptions()
        .setPageWidth(2100)   // width in pixels (A4 at 300 DPI)
        .setPageHeight(2970)  // height in pixels
        .setResolution(300)   // 300 DPI for high‑quality output
);
```

### Βήμα 3: αποθήκευση ως PDF
```java
// Save the loaded DWG as a PDF file
cadImage.save("output.pdf", pdfOptions);

// Release resources – important when processing many files in a loop
cadImage.dispose();
```

Οι τρεις παραπάνω γραμμές αποτελούν μια πλήρη ροή εργασίας **convert DWG to PDF**. Μπορείτε να τις τοποθετήσετε μέσα σε έναν βρόχο για να επεξεργαστείτε κατά δέσμη έναν κατάλογο σχεδίων.

## Εξαγωγή διατάξεων CAD σε PDF

Η εξαγωγή μιας συγκεκριμένης διάταξης (προβολή paper‑space) λειτουργεί με τον ίδιο τρόπο επειδή το Aspose.CAD αντιμετωπίζει κάθε διάταξη ως εικόνα εσωτερικά. Απλώς φορτώστε το DWG, επιλέξτε τη διάταξη με το όνομα αν χρειάζεται και καλέστε `save` με `PdfOptions`. Δεν απαιτείται επιπλέον βήμα μετατροπής.

## Εξαγωγή σε BMP

`BmpOptions` καθορίζει τις παραμέτρους εξόδου μορφής BMP όπως το βάθος χρώματος και η ανάλυση. Όταν χρειάζεστε μικρογραφίες raster ή bitmap πόρους, χρησιμοποιήστε `BmpOptions` αντί για `PdfOptions`. Το ίδιο αντικείμενο `Image` μπορεί να αποθηκευτεί σε BMP με μία κλήση, επιτρέποντάς σας να δημιουργήσετε προεπισκοπήσεις υψηλής ανάλυσης για καταλόγους ή μικρογραφίες UI.

## Εξαγωγή σε PDF (γενικά αρχεία CAD)

Πέρα από το DWG, η βιβλιοθήκη μπορεί να μετατρέψει DXF, DWF και άλλα μορφότυπα CAD σε PDF με τον ίδιο κώδικα. Απλώς αλλάξτε την επέκταση αρχείου στο `Image.load`. Η υποκείμενη μηχανή μετατροπής ανιχνεύει αυτόματα τη μορφή προέλευσης.

## Εξαγωγή IFC σε PNG

`PngOptions` ορίζει τις ρυθμίσεις μορφής PNG όπως το επίπεδο συμπίεσης. Τα αρχεία IFC (Industry Foundation Classes) είναι κοινά σε ροές εργασίας BIM. Φορτώστε το IFC με `Image.load` και αποθηκεύστε το ως PNG χρησιμοποιώντας `PngOptions`. Αυτό παράγει μια raster εικόνα που μπορεί να ενσωματωθεί σε πίνακες ελέγχου ιστού ή τεκμηρίωση.

## Εξαγωγή STL σε PNG

`PngOptions` ορίζει τις ρυθμίσεις μορφής PNG όπως το επίπεδο συμπίεσης. Τα αρχεία STL περιγράφουν 3‑D πλέγματα. Το Aspose.CAD τα αποδίδει σε εικόνα 2‑D, την οποία μπορείτε να εξάγετε ως PNG για γρήγορους οπτικούς ελέγχους ή καταχωρίσεις προϊόντων. Το ίδιο μοτίβο `Image.save("model.png", new PngOptions())` ισχύει.

## Μαθήματα εξαγωγής CAD

### [Εξαγωγή εικόνων AutoCAD σε PDF - οδηγός Aspose.CAD for Java](./export-autocad-images-to-pdf/)
### [Εξαγωγή διατάξεων CAD σε PDF με Aspose.CAD for Java](./export-cad-layouts-to-pdf/)
### [Εξαγωγή σε BMP με Aspose.CAD for Java](./export-to-bmp/)
### [Εξαγωγή σε PDF με Aspose.CAD for Java](./export-to-pdf/)
### [Εξαγωγή IFC σε PNG με Aspose.CAD for Java](./export-ifc-to-png/)
### [Εξαγωγή STL σε PNG με Aspose.CAD for Java](./export-stl-to-png/)

## Συνηθισμένες περιπτώσεις χρήσης
- **Παραδοτέα πελάτη** – Παρέχετε ανασκοπήσεις σχεδίων σε PDF χωρίς να εκθέτετε τα πηγαία αρχεία DWG.  
- **Αυτοματοποιημένες αναφορές** – Δημιουργήστε μικρογραφίες PNG μοντέλων IFC ή STL για πίνακες ελέγχου.  
- **Διαδικασίες μετατροπής δέσμης** – Επεξεργαστείτε μεγάλα αρχεία CAD κατά τη διάρκεια της νύχτας χρησιμοποιώντας έναν απλό βρόχο Java.

## Συμβουλές & κόλπα
- **Συμβουλή επαγγελματία:** Ορίστε `PdfOptions.setVectorRasterizationOptions().setResolution(300)` για να ελέγξετε το DPI των εξαγωγών raster και να διατηρήσετε λογικά τα μεγέθη αρχείων.  
- **Αποφύγετε τις αυξήσεις μνήμης:** Καλέστε `Image.dispose()` μετά από κάθε `save` όταν επεξεργάζεστε πολλά αρχεία.  
- **Αντιμετώπιση προβλημάτων:** Εάν εξαφανιστούν τα επίπεδα, βεβαιωθείτε ότι το πηγαίο DWG έχει ορατά επίπεδα και ενεργοποιήστε τη συμπίεση με `PdfOptions.setCompress(true)`.

## Συχνές ερωτήσεις

**Q: Πώς μετατρέπω IFC σε PNG χρησιμοποιώντας το Aspose.CAD;**  
A: Φορτώστε το αρχείο IFC με `Image.load("model.ifc")` και καλέστε `save("model.png", new PngOptions())`.

**Q: Μπορώ να εξάγω μια διάταξη CAD απευθείας σε PDF χωρίς να τη μετατρέψω πρώτα σε εικόνα;**  
A: Ναι—το Aspose.CAD αντιμετωπίζει τις διατάξεις ως εικόνες εσωτερικά, έτσι το `save("layout.pdf", new PdfOptions())` το διαχειρίζεται αυτόματα.

**Q: Ποια είναι η διαφορά μεταξύ εξαγωγής AutoCAD σε PDF και εξαγωγής διάταξης CAD σε PDF;**  
A: Η εξαγωγή ενός σχεδίου AutoCAD μετατρέπει ολόκληρο το σχέδιο, ενώ η εξαγωγή μιας διάταξης στοχεύει σε μια συγκεκριμένη προβολή paper‑space, διατηρώντας τις ρυθμίσεις σελίδας της.

**Q: Υπάρχει όριο στον αριθμό των σελίδων κατά την εξαγωγή ενός πολυφύλλιου DWG σε PDF;**  
A: Δεν υπάρχει ενσωματωμένο όριο· κάθε διάταξη γίνεται ξεχωριστή σελίδα στο παραγόμενο PDF.

**Q: Χρειάζομαι ξεχωριστή άδεια για κάθε μορφή εξαγωγής;**  
A: Μία άδεια Aspose.CAD καλύπτει όλες τις υποστηριζόμενες μορφές (PDF, PNG, BMP κ.λπ.).

---

**Τελευταία ενημέρωση:** 2026-10-25  
**Δοκιμή με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Εξαγωγή CAD σε PDF: Εξαγωγή διατάξεων CAD σε PDF με Aspose.CAD for Java](/cad/java/cad-export-options/export-cad-layouts-to-pdf/)
- [Εξαγωγή DWG σε PDF σε Java – Ορισμός μεγέθους σελίδας PDF με Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}