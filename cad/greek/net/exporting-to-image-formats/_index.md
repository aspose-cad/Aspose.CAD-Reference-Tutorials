---
date: 2026-07-18
description: Η μετατροπή Aspose CAD σας επιτρέπει να εξάγετε εύκολα IFC σε PNG και
  IGES σε PDF. Μάθετε βήμα‑βήμα πώς να μετατρέπετε αρχεία CAD με το Aspose.CAD για
  .NET σε λίγα λεπτά.
keywords:
- aspose cad conversion
- export cad to png
- convert iges to pdf
lastmod: 2026-07-18
linktitle: Εξαγωγή σε μορφές εικόνας
og_description: Η μετατροπή Aspose CAD επιτρέπει γρήγορη εξαγωγή IFC σε PNG και IGES
  σε PDF. Ακολουθήστε αυτόν τον οδηγό για απρόσκοπτη διαχείριση αρχείων CAD με το
  Aspose.CAD για .NET.
og_image_alt: Guide showing Aspose CAD conversion from CAD files to PNG and PDF
og_title: 'Μετατροπή Aspose CAD: Εξαγωγή σε μορφές εικόνας'
schemas:
- author: Aspose
  dateModified: '2026-07-18'
  description: Aspose CAD conversion lets you effortlessly export IFC to PNG and IGES
    to PDF. Learn step‑by‑step how to convert CAD files with Aspose.CAD for .NET in
    minutes.
  headline: 'Aspose CAD Conversion: Exporting to Image Formats'
  type: TechArticle
- questions:
  - answer: Yes, iterate over a folder with `foreach (var file in Directory.GetFiles(path,
      "*.ifc")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, ".png"),
      ImageFormat.Png); }`. The `Directory.GetFiles` method returns the names of files
      (including their paths) that match a specified pattern in a directory.
    question: Can I convert multiple CAD files in one batch?
  - answer: Layer visibility is respected; you can toggle layers via `LoadOptions`
      before saving, ensuring only selected layers appear in the output.
    question: Does Aspose.CAD preserve layer information in the exported image?
  - answer: The library comfortably processes files up to **2 GB**; larger files should
      be split or streamed using `LoadOptions.MemoryLimit`.
    question: What is the maximum file size Aspose.CAD can handle?
  - answer: Yes—by saving as `ImageFormat.Pdf` the output retains vector data, allowing
      infinite scaling without quality loss.
    question: Is there support for converting CAD to vector‑based PDFs?
  - answer: A single Aspose.CAD license covers all supported .NET runtimes (Framework,
      Core, and .NET 5+).
    question: Do I need a separate license for each .NET platform?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- cad conversion
- export cad to png
- iges to pdf
- ifc to png
title: 'Μετατροπή Aspose CAD: Εξαγωγή σε μορφές εικόνας'
url: /el/net/exporting-to-image-formats/
weight: 39
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή Aspose CAD: Εξαγωγή σε Μορφές Εικόνας

Στα σύγχρονα ροές εργασίας μηχανικής και σχεδίασης, **aspose cad conversion** είναι απαραίτητη για τη μετατροπή πολύπλοκων αρχείων CAD και BIM σε μορφές εικόνας που μπορούν να προβληθούν παντού. Είτε χρειάζεστε να μοιραστείτε μια γρήγορη προεπισκόπηση ενός μοντέλου IFC είτε να δημιουργήσετε ένα εκτυπώσιμο PDF από ένα σχέδιο IGES, αυτό το εκπαιδευτικό υλικό σας καθοδηγεί βήμα προς βήμα χρησιμοποιώντας το Aspose.CAD για .NET. Θα δείτε πώς να διατηρήσετε τη γεωμετρία, τα χρώματα και τα επίπεδα αμετάβλητα κατά την εξαγωγή σε PNG, PDF και άλλες μορφές raster.

## Γρήγορες Απαντήσεις
- **Ποιες μορφές μπορεί να εξάγει το Aspose.CAD;** Πάνω από 30 μορφές CAD/BIM σε περισσότερους από 20 τύπους εικόνας, συμπεριλαμβανομένων PNG, JPEG, PDF και TIFF.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Μπορούν να επεξεργαστούν μεγάλα αρχεία;** Ναι – το Aspose.CAD διαχειρίζεται αρχεία έως 2 GB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη.  
- **Απαιτείται κάποιο πρόσθετο λογισμικό;** Δεν χρειάζονται εξωτερικά εργαλεία CAD· η βιβλιοθήκη εκτελεί όλες τις μετατροπές εσωτερικά.

## Τι είναι η Μετατροπή Aspose CAD;
Η κλάση `Image` αντιπροσωπεύει ένα έγγραφο CAD που έχει φορτωθεί στη μνήμη και παρέχει μεθόδους για αποθήκευση σε διάφορες μορφές. Η Μετατροπή Aspose CAD μετατρέπει αρχεία CAD/BIM σε άλλες μορφές χρησιμοποιώντας το Aspose.CAD για .NET. Φορτώστε την πηγή με `Image`, επιλέξτε τη μορφή προορισμού και καλέστε `Save`. Αυτό το μοτίβο δύο βημάτων διατηρεί τα επίπεδα, τα βάρη γραμμής και τις υφές, ταιριάζοντας με την αρχική πρόθεση σχεδίασης.

## Πώς να Εξάγετε Αρχεία IFC σε PNG;
Η κλάση `Image` αντιπροσωπεύει ένα έγγραφο CAD που έχει φορτωθεί στη μνήμη και παρέχει μεθόδους για αποθήκευση σε διάφορες μορφές. Φορτώστε το αρχείο IFC με `new Image("model.ifc")` και καλέστε `image.Save("model.png", ImageFormat.Png)`. Το Aspose.CAD διαβάζει τη 3‑Δ γεωμετρία, τη μετατρέπει σε εικόνα raster και γράφει ένα PNG υψηλής ανάλυσης που διατηρεί το βάθος χρώματος και τη διαφάνεια. Για επεξεργασία σε δέσμη, κάντε βρόχο σε έναν φάκελο και αποθηκεύστε κάθε αρχείο.

## Πώς να Εξάγετε Αρχεία IGES σε PDF;
Η κλάση `Image` αντιπροσωπεύει ένα έγγραφο CAD που έχει φορτωθεί στη μνήμη και παρέχει μεθόδους για αποθήκευση σε διάφορες μορφές. Δημιουργήστε ένα αντικείμενο `Image` από το αρχείο IGES και καλέστε `image.Save("drawing.pdf", ImageFormat.Pdf)`. Η μετατροπή διατηρεί τις διανυσματικές πληροφορίες, τα στυλ γραμμών και τις σημειώσεις, παράγοντας ένα PDF που μπορεί να ανοιχθεί σε οποιονδήποτε προβολέα χωρίς απώλεια λεπτομερειών. Χρησιμοποιήστε την προαιρετική ιδιότητα `Resolution` για να αυξήσετε το DPI για PDF έτοιμα για εκτύπωση.

## Γιατί να Χρησιμοποιήσετε το Aspose.CAD για .NET;
Το Aspose.CAD υποστηρίζει **30+ μορφές εισόδου** (συμπεριλαμβανομένων IFC, IGES, DWG, DWF και STL) και μπορεί να εξάγει **20+ τύπους εικόνας**. Επεξεργάζεται σχέδια πολλών εκατοντάδων σελίδων σε λιγότερο από 5 δευτερόλεπτα σε έναν τυπικό διακομιστή και λειτουργεί πλήρως offline—χωρίς ανάγκη για εγκαταστάσεις CAD. Αυτά τα ποσοτικοποιημένα οφέλη το καθιστούν μια οικονομική, υψηλής απόδοσης επιλογή τόσο για επιχειρήσεις όσο και για ελεύθερους προγραμματιστές.

## Συνηθισμένα Πιθανά Σφάλματα και Επαγγελματικές Συμβουλές
Η κλάση `LoadOptions` σας επιτρέπει να προσαρμόσετε τον τρόπο φόρτωσης ενός αρχείου CAD, όπως ορίζοντας όρια μνήμης ή καθορίζοντας επίπεδα.  
Το αντικείμενο `FontSettings` ορίζει κανόνες αντικατάστασης και ενσωμάτωσης γραμματοσειρών που χρησιμοποιούνται κατά τη μετατροπή.

- **Πρόβλημα:** Η αγνόηση του προεπιλεγμένου DPI μπορεί να παράγει εικόνες χαμηλής ανάλυσης.  
  **Συμβουλή:** Ορίστε `image.DpiX` και `image.DpiY` σε 300 για PNG υψηλής ποιότητας εκτύπωσης.  
- **Πρόβλημα:** Τα μεγάλα αρχεία IGES μπορεί να υπερβούν τα όρια μνήμης.  
  **Συμβουλή:** Χρησιμοποιήστε `LoadOptions` με `MemoryLimit` για να μεταφέρετε το αρχείο σε τμήματα.  
- **Πρόβλημα:** Η έλλειψη γραμματοσειρών σε μοντέλα IFC οδηγεί σε κείμενο κράτησης θέσης.  
  **Συμβουλή:** Ενσωματώστε τις απαιτούμενες γραμματοσειρές χρησιμοποιώντας το αντικείμενο `FontSettings` πριν από τη μετατροπή.

## Εκπαιδευτικά για Εξαγωγή σε Μορφές Εικόνας
### [Εξαγωγή Αρχείων IFC σε PNG - Εκπαιδευτικό Aspose.CAD](./exporting-ifc-files-to-png/)
Εξερευνήστε το Aspose.CAD για .NET, μια ισχυρή λύση για απρόσκοπτη μετατροπή IFC σε PNG. Κατεβάστε το τώρα για αποδοτική επεξεργασία αρχείων CAD.
### [Εξαγωγή Αρχείων IGES σε PDF - Οδηγός Aspose.CAD](./exporting-iges-files-to-pdf/)
Μάθετε πώς να εξάγετε άψογα αρχεία IGES σε PDF χρησιμοποιώντας το Aspose.CAD για .NET. Ακολουθήστε τον βήμα‑προς‑βήμα οδηγό μας για ακριβή διαχείριση αρχείων CAD.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να μετατρέψω πολλά αρχεία CAD σε μία δέσμη;**  
Α: Ναι, επαναλάβετε πάνω σε έναν φάκελο με `foreach (var file in Directory.GetFiles(path, \"*.ifc\")) { var img = new Image(file); img.Save(Path.ChangeExtension(file, \".png\"), ImageFormat.Png); }`.  
Η μέθοδος `Directory.GetFiles` επιστρέφει τα ονόματα των αρχείων (συμπεριλαμβανομένων των διαδρομών τους) που ταιριάζουν με το καθορισμένο μοτίβο σε έναν κατάλογο.

**Ε: Διατηρεί το Aspose.CAD τις πληροφορίες επιπέδων στην εξαγόμενη εικόνα;**  
Α: Η ορατότητα των επιπέδων τηρείται· μπορείτε να ενεργοποιήσετε/απενεργοποιήσετε επίπεδα μέσω του `LoadOptions` πριν από την αποθήκευση, εξασφαλίζοντας ότι μόνο τα επιλεγμένα επίπεδα εμφανίζονται στο αποτέλεσμα.

**Ε: Ποιο είναι το μέγιστο μέγεθος αρχείου που μπορεί να διαχειριστεί το Aspose.CAD;**  
Α: Η βιβλιοθήκη επεξεργάζεται άνετα αρχεία έως **2 GB**· μεγαλύτερα αρχεία πρέπει να χωριστούν ή να μεταφερθούν σε ροή χρησιμοποιώντας το `LoadOptions.MemoryLimit`.

**Ε: Υπάρχει υποστήριξη για μετατροπή CAD σε PDF βασισμένα σε διανύσματα;**  
Α: Ναι—αποθηκεύοντας ως `ImageFormat.Pdf` το αποτέλεσμα διατηρεί τα διανυσματικά δεδομένα, επιτρέποντας απεριόριστη κλιμάκωση χωρίς απώλεια ποιότητας.

**Ε: Χρειάζομαι ξεχωριστή άδεια για κάθε πλατφόρμα .NET;**  
Α: Μία άδεια Aspose.CAD καλύπτει όλες τις υποστηριζόμενες εκτελέσεις .NET (Framework, Core και .NET 5+).

---

**Τελευταία Ενημέρωση:** 2026-07-18  
**Δοκιμή Με:** Aspose.CAD 24.12 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Εκπαιδευτικά
- [Εξαγωγή Αρχείων IFC σε PNG - Εκπαιδευτικό Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-ifc-files-to-png/)
- [Εξαγωγή Αρχείων IGES σε PDF - Οδηγός Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Εξαγωγή Διατάξεων CAD σε Μορφές Raster Εικόνας στο Aspose.CAD για .NET](/cad/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}