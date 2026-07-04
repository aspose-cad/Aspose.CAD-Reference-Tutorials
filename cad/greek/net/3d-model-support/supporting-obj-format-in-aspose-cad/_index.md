---
date: 2026-07-04
description: Μάθετε πώς να ορίζετε το μέγεθος σελίδας PDF κατά τη μετατροπή αρχείων
  OBJ σε PDF χρησιμοποιώντας το Aspose.CAD για .NET. Οδηγός βήμα‑βήμα με προαπαιτούμενα,
  επιλογές rasterization και επιλογές PDF.
keywords:
- set pdf page size
- load obj file
- save cad as pdf
- 3d model to pdf
- how to convert obj
linktitle: Υποστήριξη μορφής OBJ στο Aspose.CAD - Οδηγός
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size while converting OBJ files to PDF using
    Aspose.CAD for .NET. Step‑by‑step guide with prerequisites, rasterization options,
    and PDF options.
  headline: Set PDF Page Size for OBJ Files with Aspose.CAD - Tutorial
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports over **30** input formats—including DWG, DXF,
      DGN, and STL—and can export to more than **20** raster and vector formats.
    question: Is Aspose.CAD compatible with other CAD file formats?
  - answer: Absolutely! You can explore a free trial version [here](https://releases.aspose.com/).
    question: Can I try Aspose.CAD before purchasing?
  - answer: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) to ask
      questions and share experiences with the community.
    question: How do I obtain support for Aspose.CAD?
  - answer: Yes, temporary licenses can be obtained [here](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for testing?
  - answer: You can purchase Aspose.CAD [here](https://purchase.aspose.com/buy).
    question: Where can I purchase a full license?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ορισμός μεγέθους σελίδας PDF για αρχεία OBJ με Aspose.CAD - Οδηγός
url: /el/net/3d-model-support/supporting-obj-format-in-aspose-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Σελίδας PDF για Αρχεία OBJ με Aspose.CAD - Εκπαιδευτικό

## Εισαγωγή

Αν αναπτύσσετε εφαρμογές CAD σε .NET και χρειάζεστε **ορισμό μεγέθους σελίδας PDF** κατά τη μετατροπή μοντέλων OBJ, το Aspose.CAD για .NET προσφέρει ένα καθαρό, code‑first API που διαχειρίζεται τη rasterization και τη δημιουργία PDF σε μία ενιαία ροή. Σε αυτό το εκπαιδευτικό θα περάσουμε από την εγκατάσταση της βιβλιοθήκης, τη φόρτωση ενός αρχείου OBJ, τη διαμόρφωση των διαστάσεων της σελίδας και, τέλος, την αποθήκευση του αποτελέσματος ως PDF. Στο τέλος θα έχετε ένα επαναχρησιμοποιήσιμο μοτίβο για τη μετατροπή οποιουδήποτε 3‑D μοντέλου σε ένα PDF εγγράφου με τέλεια διαστάσεις.

## Γρήγορες Απαντήσεις
- **Μπορεί το Aspose.CAD να μετατρέψει OBJ σε PDF;** Ναι – φορτώστε το OBJ με `Image.Load` και κάντε rasterization σε PDF.
- **Πώς ορίζω προσαρμοσμένο μέγεθος σελίδας PDF;** Χρησιμοποιήστε `PdfOptions` → `PageSize` ή ορίστε πλάτος/ύψος στο `RasterizationOptions`.
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Χρειάζεται άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται άδεια για παραγωγή.
- **Η μετατροπή είναι αποδοτική σε μνήμη;** Το Aspose.CAD ρέει δεδομένα και μπορεί να διαχειριστεί PDF εκατοντάδων σελίδων χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη.

## Τι είναι η μορφή OBJ;
Η μορφή OBJ είναι ένας ευρέως χρησιμοποιούμενος, κειμενικός ορισμός γεωμετρίας 3‑D που αποθηκεύει θέσεις κορυφών, συντεταγμένες υφής και ορισμούς προσώπων. Υποστηρίζεται από τα περισσότερα εργαλεία 3‑D μοντελοποίησης και είναι ιδανική για ανταλλαγή μεταξύ CAD και pipelines απόδοσης.

## Γιατί να ορίσω προσαρμοσμένο μέγεθος σελίδας PDF;
Το Aspose.CAD μπορεί να αποδώσει ένα σχέδιο CAD σε οποιοδήποτε μέγεθος raster. Ορίζοντας ρητά τις διαστάσεις της σελίδας PDF διασφαλίζετε ότι το τελικό έγγραφο ταιριάζει με τα πρότυπα αναφοράς σας, προσαρμόζεται σε τυπικά μεγέθη χαρτιού (A4, Letter) ή συμμορφώνεται με προσαρμοσμένες διατάξεις εκτύπωσης. Ποσοτικό όφελος: το API μπορεί να δημιουργήσει PDF έως **200 mm × 200 mm** σε μία κλήση, επεξεργαζόμενο αρχεία μεγαλύτερα από **500 MB** χωρίς να ξεπεράσει 250 MB RAM.

## Προαπαιτούμενα

- **Aspose.CAD Library** – Βεβαιωθείτε ότι η βιβλιοθήκη Aspose.CAD είναι εγκατεστημένη στο .NET project σας. Μπορείτε να τη κατεβάσετε [εδώ](https://releases.aspose.com/cad/net/) και να δείτε την πλήρη αναφορά API στην [τεκμηρίωση](https://reference.aspose.com/cad/net/).
- **Document Directory** – Δημιουργήστε έναν φάκελο για τα CAD assets· θα τον αναφέρουμε ως “Your Document Directory” καθ’ όλη τη διάρκεια του οδηγού.
- **.NET Development Environment** – Visual Studio 2022 ή οποιοδήποτε IDE που υποστηρίζει .NET 6+.

## Πώς να ορίσετε μέγεθος σελίδας PDF κατά τη μετατροπή OBJ σε PDF;

Φορτώστε το αρχείο OBJ, διαμορφώστε τις επιλογές rasterization με το επιθυμητό πλάτος και ύψος, συνδέστε αυτές τις επιλογές σε ένα αντικείμενο `PdfOptions` και καλέστε `Save`. Αυτό το μοτίβο δύο βημάτων εγγυάται ότι η σελίδα PDF ταιριάζει με τις διαστάσεις που καθορίζετε, διατηρώντας ταυτόχρονα τις λεπτομέρειες του μοντέλου.

## Βήμα 1: Εισαγωγή Χώρων Ονομάτων

Η κλάση `Image` διαχειρίζεται όλες τις μορφές CAD, ενώ η κλάση `PdfOptions` ελέγχει την έξοδο PDF.  
`Image` αντιπροσωπεύει ένα CAD έγγραφο και παρέχει μεθόδους για φόρτωση και αποθήκευση αρχείων. `PdfOptions` ορίζει ρυθμίσεις για τη δημιουργία PDF όπως μέγεθος σελίδας και συμπίεση.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Βήμα 2: Φόρτωση Αρχείου OBJ

Φορτώστε το αρχείο OBJ στο αντικείμενο εικόνας Aspose.CAD. Αντικαταστήστε `"example-580-W.obj"` με το όνομα του δικού σας αρχείου OBJ.

```csharp
string MyDir = "Your Document Directory";
using (Aspose.CAD.Image CADDoc = Aspose.CAD.Image.Load(MyDir + "example-580-W.obj"))
{
    // Your code for further processing goes here
}
```

## Βήμα 3: Διαμόρφωση Επιλογών Rasterization

`RasterizationOptions` ορίζει το μέγεθος raster που τελικά γίνεται το μέγεθος σελίδας PDF. Ορίζοντας `PageWidth` και `PageHeight` ελέγχετε τις ακριβείς διαστάσεις του εξαγόμενου PDF.  
`CadRasterizationOptions` (πρόσβαση μέσω `RasterizationOptions`) καθορίζει παραμέτρους rasterization όπως διαστάσεις σελίδας και ανάλυση.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();

rasterizationOptions.PageWidth = CADDoc.Size.Width;
rasterizationOptions.PageHeight = CADDoc.Size.Height;
```

## Βήμα 4: Δημιουργία PDF Options

`PdfOptions` συνδέει τις ρυθμίσεις rasterization με τον PDF writer. Αναθέτοντας το αντικείμενο `RasterizationOptions`, διασφαλίζετε ότι το PDF κληρονομεί το μέγεθος σελίδας που ορίσατε.

```csharp
Aspose.CAD.ImageOptions.PdfOptions CADf = new Aspose.CAD.ImageOptions.PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 5: Αποθήκευση ως PDF

Κληθείτε τη μέθοδο `Save` στο αντικείμενο `Image`, περνώντας το όνομα του αρχείου προορισμού και τις ρυθμισμένες `PdfOptions`. Η βιβλιοθήκη γράφει ένα PDF με το ακριβές μέγεθος σελίδας που καθορίσατε.  
`Save` γράφει την εικόνα σε αρχείο χρησιμοποιώντας τη συγκεκριμένη μορφή και τις επιλογές.

```csharp
CADDoc.Save(MyDir + "example-580-W_custom.pdf", CADf);
```

## Συχνά Προβλήματα και Λύσεις

- **Λανθασμένες διαστάσεις σελίδας** – Βεβαιωθείτε ότι `PageWidth` και `PageHeight` έχουν οριστεί σε **pixel**· χρησιμοποιήστε το `Resolution` για να μετατρέψετε ίντσες ή χιλιοστά σε pixel (π.χ., 300 dpi → 1 inch = 300 px).
- **Απουσία υφών** – Τα αρχεία OBJ συχνά αναφέρονται σε εξωτερικά αρχεία `.mtl`· βεβαιωθείτε ότι το αρχείο υλικού βρίσκεται στον ίδιο φάκελο με το OBJ.
- **Μεγάλη χρήση μνήμης** – Ενεργοποιήστε `Image.SaveOptions.Compression` για να μειώσετε την πίεση μνήμης σε render υψηλής ανάλυσης.

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.CAD συμβατό με άλλες μορφές αρχείων CAD;**  
A: Ναι, το Aspose.CAD υποστηρίζει πάνω από **30** μορφές εισόδου—συμπεριλαμβανομένων DWG, DXF, DGN, και STL—και μπορεί να εξάγει σε περισσότερες από **20** μορφές raster και vector.

**Q: Μπορώ να δοκιμάσω το Aspose.CAD πριν το αγοράσω;**  
A: Φυσικά! Μπορείτε να εξερευνήσετε μια δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;**  
A: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για να θέσετε ερωτήσεις και να μοιραστείτε εμπειρίες με την κοινότητα.

**Q: Διατίθενται προσωρινές άδειες για δοκιμές;**  
A: Ναι, προσωρινές άδειες μπορούν να ληφθούν [εδώ](https://purchase.aspose.com/temporary-license/).

**Q: Πού μπορώ να αγοράσω πλήρη άδεια;**  
A: Μπορείτε να αγοράσετε το Aspose.CAD [εδώ](https://purchase.aspose.com/buy).

---

**Τελευταία Ενημέρωση:** 2026-07-04  
**Δοκιμασμένο Με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Εκπαιδευτικά

- [Εξαγωγή Αρχείων IGES σε PDF - Οδηγός Aspose.CAD](/cad/net/exporting-to-image-formats/exporting-iges-files-to-pdf/)
- [Εξαγωγή DXF σε PDF Format - Εκπαιδευτικό Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Εξαγωγή Σχεδίων CAD σε PDF - Εκπαιδευτικό Aspose.CAD](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}