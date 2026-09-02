---
date: 2026-07-04
description: Μάθετε πώς να ορίσετε το μέγεθος σελίδας PDF και να εξάγετε PDF από 3D
  CAD images χρησιμοποιώντας το Aspose.CAD for .NET – ένας οδηγός βήμα‑βήμα για τη
  μετατροπή DWG σε PDF και την αποθήκευση CAD ως PDF.
keywords:
- set pdf page size
- export pdf from cad
- convert dwg to pdf
- save cad as pdf
- cad to pdf tutorial
linktitle: Εξαγωγή 3D Images σε PDF
schemas:
- author: Aspose
  dateModified: '2026-07-04'
  description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  headline: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  type: TechArticle
- description: Learn how to set PDF page size and export PDF from 3D CAD images using
    Aspose.CAD for .NET – a step‑by‑step guide to convert DWG to PDF and save CAD
    as PDF.
  name: Set PDF page size – Export 3D Images to PDF with Aspose.CAD
  steps:
  - name: Load the CAD Image
    text: '`Image` class represents a CAD drawing loaded into memory, ready for rasterization.'
  - name: Configure Rasterization Options (Save CAD as PDF)
    text: '`RasterizationOptions` class defines how the CAD data is rasterized, including
      page size, DPI, and whether 3‑D entities are rendered.'
  - name: Set PDF Options (Create PDF from CAD)
    text: '`PdfOptions` class holds the output format settings and links the rasterization
      options to PDF generation.'
  - name: Save as PDF (Generate PDF from 3D Model)
    text: '`Save` method on the `Image` object writes the rasterized content to the
      specified PDF file, producing a ready‑to‑share document.'
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD supports more than 50 input and output formats, including
      DWG, DXF, DGN, STL, and IFC, ensuring flexibility for any project.
    question: Is Aspose.CAD compatible with all CAD file formats?
  - answer: Absolutely. Set `PageWidth` and `PageHeight` in `RasterizationOptions`
      to any size in points, inches, or millimetres before calling `Save`.
    question: Can I customize the page dimensions when exporting to PDF?
  - answer: Yes, you can obtain temporary licenses for Aspose.CAD by visiting [Temporary
      License](https://purchase.aspose.com/temporary-license/).
    question: Are temporary licenses available for Aspose.CAD?
  - answer: Head to the [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) for
      expert help and peer‑to‑peer advice.
    question: Where can I find additional support or community discussions?
  - answer: Yes, you can explore the features of Aspose.CAD by accessing the [free
      trial](https://releases.aspose.com/).
    question: Is there a free trial version of Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ορισμός μεγέθους σελίδας PDF – Εξαγωγή 3D Images σε PDF με Aspose.CAD
url: /el/net/3d-image-export/exporting-3d-images-to-pdf/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή 3D Εικόνων σε PDF - Εγχειρίδιο Aspose.CAD

## Εισαγωγή

Αν χρειάζεστε να **set PDF page size** ενώ μετατρέπετε ένα 3‑D CAD σχέδιο σε PDF, βρίσκεστε στο σωστό μέρος. Αυτό το εγχειρίδιο σας δείχνει, βήμα προς βήμα, πώς να φορτώσετε ένα αρχείο CAD, να διαμορφώσετε τις επιλογές rasterization—συμπεριλαμβανομένων των προσαρμοσμένων διαστάσεων σελίδας—και να δημιουργήσετε ένα PDF υψηλής πιστότητας χρησιμοποιώντας το Aspose.CAD για .NET. Στο τέλος θα μπορείτε να **export PDF from CAD**, **save CAD as PDF**, και να ελέγχετε κάθε λεπτομέρεια διάταξης χωρίς να εγκαταστήσετε το AutoCAD.

## Γρήγορες Απαντήσεις
- **What does “export PDF from CAD” mean?** Μετατρέπει ένα σχέδιο CAD (DWG, DXF, DGN, κ.λπ.) σε PDF που μπορεί να ανοίξει σε οποιαδήποτε συσκευή.  
- **Which library performs the conversion?** Το Aspose.CAD για .NET παρέχει rasterization και εξαγωγή PDF χωρίς εξωτερικές εξαρτήσεις.  
- **Do I need a license?** Απαιτείται προσωρινή ή πλήρης άδεια για παραγωγή· διατίθεται δωρεάν δοκιμαστική έκδοση.  
- **Can I set custom page dimensions?** Ναι—χρησιμοποιήστε `PageWidth` και `PageHeight` στο `RasterizationOptions`.  
- **Will 3‑D geometry be retained?** Τα 3‑D στοιχεία rasterize; ενεργοποιήστε `TypeOfEntities.Entities3D` για πλήρη υποστήριξη 3‑D.

## Τι είναι η «export PDF» στο πλαίσιο του CAD;

Η εξαγωγή PDF από CAD σημαίνει τη λήψη ενός σχεδίου CAD (DWG, DXF, DGN, κ.λπ.) και η μετατροπή του σε αρχείο PDF που μπορεί να περιέχει διανυσματικά γραφικά, rasterized 3‑D προβολές και ακριβείς πληροφορίες διάταξης σελίδας, καθιστώντας εύκολη τη διανομή σε όποιον δεν διαθέτει λογισμικό CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για εξαγωγή PDF;

Το Aspose.CAD σας επιτρέπει να **set PDF page size** και να εξάγετε PDFs εξ ολοκλήρου σε διαχειριζόμενο κώδικα .NET. Υποστηρίζει πάνω από 50 μορφές CAD, επεξεργάζεται αρχεία έως 2 GB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, και διατηρεί τα βάρη γραμμών, τα χρώματα και την προαιρετική απόδοση 3‑D οντοτήτων με DPI rasterization έως 1200. Η βιβλιοθήκη λειτουργεί σε Windows, Linux και macOS, έτσι τα παραγόμενα PDFs λειτουργούν σε οποιαδήποτε πλατφόρμα.

## Προαπαιτούμενα

- **Aspose.CAD for .NET** εγκατεστημένο. Κατεβάστε το από τη [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Ένας φάκελος που περιέχει τα αρχεία CAD που θέλετε να μετατρέψετε (π.χ., `C:\CAD\`).  
- .NET 6.0 ή νεότερο (ή .NET Framework 4.7.2).  

## Εισαγωγή Namespaces

Οι δηλώσεις `using` εισάγουν τα namespaces του Aspose.CAD που απαιτούνται για εργασία με rasterization και επιλογές PDF.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

## Οδηγός βήμα‑βήμα

### Πώς να ορίσετε το μέγεθος σελίδας PDF κατά την εξαγωγή CAD σε PDF;

Φορτώστε το αρχείο CAD, διαμορφώστε τις διαστάσεις σελίδας στο `RasterizationOptions`, συνδέστε αυτές τις επιλογές με ένα αντικείμενο `PdfOptions` και καλέστε `Save`. Αυτή η τετραβήματική ροή σας δίνει πλήρη έλεγχο του μεγέθους και της ποιότητας εξόδου ενώ διατηρεί τον κώδικα σύντομο.

### Βήμα 1: Φόρτωση της CAD Εικόνας

Η κλάση `Image` αντιπροσωπεύει ένα σχέδιο CAD που έχει φορτωθεί στη μνήμη, έτοιμο για rasterization.  

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code for loading the CAD image goes here
}
```

### Βήμα 2: Διαμόρφωση Rasterization Options (Αποθήκευση CAD ως PDF)

Η κλάση `RasterizationOptions` ορίζει πώς rasterize τα δεδομένα CAD, συμπεριλαμβανομένου του μεγέθους σελίδας, DPI και αν αποδίδονται 3‑D οντότητες.  

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
// rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;

rasterizationOptions.Layouts = new string[] { "Model" };
```

### Βήμα 3: Ορισμός PDF Options (Δημιουργία PDF από CAD)

Η κλάση `PdfOptions` περιέχει τις ρυθμίσεις μορφής εξόδου και συνδέει τις επιλογές rasterization με τη δημιουργία PDF.  

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Βήμα 4: Αποθήκευση ως PDF (Δημιουργία PDF από 3D Μοντέλο)

Η μέθοδος `Save` του αντικειμένου `Image` γράφει το rasterized περιεχόμενο στο καθορισμένο αρχείο PDF, παράγοντας ένα έγγραφο έτοιμο για διαμοιρασμό.  

```csharp
MyDir = MyDir + "Export3DImagestoPDF_out.pdf";
cadImage.Save(MyDir, pdfOptions);
```

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|-------|--------|-----|
| **Output PDF is blank** | Λάθος όνομα διάταξης ή έλλειψη διάταξης `Model`. | Επαληθεύστε ότι `rasterizationOptions.Layouts` ταιριάζει με μια διάταξη που υπάρχει στο αρχείο CAD. |
| **Low resolution** | Η προεπιλεγμένη DPI rasterization είναι χαμηλή. | Ορίστε `rasterizationOptions.Resolution = 300;` πριν από την αποθήκευση. |
| **3‑D entities not shown** | Το `TypeOfEntities` είναι σχολιασμένο. | Αποσχολιάστε `rasterizationOptions.TypeOfEntities = TypeOfEntities.Entities3D;`. |
| **License exception** | Χρήση δοκιμαστικής έκδοσης χωρίς άδεια. | Εφαρμόστε προσωρινή ή μόνιμη άδεια μέσω `License license = new License(); license.SetLicense("Aspose.CAD.lic");`. |

## Συχνές Ερωτήσεις

**Q:** Είναι το Aspose.CAD συμβατό με όλες τις μορφές αρχείων CAD;  
**A:** Ναι, το Aspose.CAD υποστηρίζει πάνω από 50 μορφές εισόδου και εξόδου, συμπεριλαμβανομένων των DWG, DXF, DGN, STL και IFC, εξασφαλίζοντας ευελιξία για οποιοδήποτε έργο.

**Q:** Μπορώ να προσαρμόσω τις διαστάσεις σελίδας κατά την εξαγωγή σε PDF;  
**A:** Απόλυτα. Ορίστε `PageWidth` και `PageHeight` στο `RasterizationOptions` σε οποιοδήποτε μέγεθος σε points, ίντσες ή χιλιοστά πριν καλέσετε `Save`.

**Q:** Διατίθενται προσωρινές άδειες για το Aspose.CAD;  
**A:** Ναι, μπορείτε να αποκτήσετε προσωρινές άδειες για το Aspose.CAD επισκεπτόμενοι το [Temporary License](https://purchase.aspose.com/temporary-license/).

**Q:** Πού μπορώ να βρω επιπλέον υποστήριξη ή συζητήσεις της κοινότητας;  
**A:** Μεταβείτε στο [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) για εξειδικευμένη βοήθεια και συμβουλές από ομοτίμους.

**Q:** Υπάρχει δωρεάν δοκιμαστική έκδοση του Aspose.CAD;  
**A:** Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD μέσω του [free trial](https://releases.aspose.com/).

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή μέθοδο να **set PDF page size** και **export PDF from 3D CAD images** χρησιμοποιώντας το Aspose.CAD για .NET. Με την προσαρμογή των επιλογών rasterization μπορείτε να ρυθμίσετε με ακρίβεια την ανάλυση, τη διάταξη σελίδας και την απόδοση 3‑D οντοτήτων ώστε να καλύψετε οποιαδήποτε απαίτηση τεκμηρίωσης. Πειραματιστείτε με διαφορετικές ρυθμίσεις DPI και διαστάσεις σελίδας για να επιτύχετε την ιδανική ισορροπία μεταξύ μεγέθους αρχείου και οπτικής πιστότητας.

{{< blocks/products/products-backtop-button >}}

## Σχετικές Οδηγίες

- [Εξαγωγή Συγκεκριμένων Διατάξεων σε PDF - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Εξαγωγή DWG σε PDF ή Raster Images - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Εξαγωγή DGN σε PDF στο Aspose.CAD για .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

--- 

**Τελευταία Ενημέρωση:** 2026-07-04  
**Δοκιμή Με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose