---
date: 2026-07-09
description: Μάθετε πώς να μετατρέψετε IGES σε PDF χρησιμοποιώντας το Aspose.CAD για
  .NET. Ακολουθήστε αυτόν τον οδηγό βήμα‑βήμα για να εξάγετε αρχεία IGES ως PDF γρήγορα
  και με ακρίβεια.
keywords:
- convert iges to pdf
- export iges as pdf
- create pdf from iges
- convert cad file to pdf
- generate pdf from cad
lastmod: 2026-07-09
linktitle: Εξαγωγή αρχείων IGES σε PDF
og_description: Μετατρέψτε IGES σε PDF χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό
  το σεμινάριο δείχνει πώς να εξάγετε αρχεία IGES ως PDF αποδοτικά με βήματα χωρίς
  κώδικα.
og_image_alt: Guide showing conversion of IGES files to PDF with Aspose.CAD in .NET
og_title: Μετατροπή IGES σε PDF – Σύντομος Οδηγός Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-07-09'
  description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  headline: Convert IGES to PDF with Aspose.CAD – Quick Guide
  type: TechArticle
- description: Learn how to convert IGES to PDF using Aspose.CAD for .NET. Follow
    this step‑by‑step guide to export IGES files as PDF quickly and accurately.
  name: Convert IGES to PDF with Aspose.CAD – Quick Guide
  steps:
  - name: Set up Your Project
    text: Create a new .NET console or class‑library project, or open an existing
      one where you want to add the conversion feature.
  - name: Add Aspose.CAD Reference
    text: Add the downloaded Aspose.CAD DLL to your project references. In Visual
      Studio, right‑click **References → Add Reference → Browse** and select the DLL.
  - name: Initialize the Path
    text: Define the folder that contains your IGES file and the output location.
  - name: Load the CAD Image
    text: '`Image.Load` reads the IGES file and creates an in‑memory representation.
      The `Image` class is Aspose.CAD''s primary entry point for any CAD format.'
  - name: Configure Rasterization Options
    text: '`PdfOptions` (derived from `CadRasterizationOptions`) lets you set page
      size, resolution, and vector‑preserving flags. The `PdfOptions` class defines
      how the CAD drawing is rasterized and saved as PDF.'
  - name: Save as PDF
    text: Finally, write the PDF file to disk. With these six straightforward steps,
      you have successfully **convert iges to pdf** using Aspose.CAD for .NET.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD works in ASP.NET, ASP.NET Core, and other web frameworks,
      providing server‑side conversion without UI dependencies.
    question: Can I use Aspose.CAD for .NET in a web application?
  - answer: Explore the comprehensive documentation [here](https://reference.aspose.com/cad/net/)
      for detailed insights into all supported features.
    question: Where can I find additional documentation for Aspose.CAD?
  - answer: Yes, you can access a free trial [here](https://releases.aspose.com/)
      to evaluate the library before purchasing.
    question: Is there a free trial available?
  - answer: For temporary licenses, visit [this link](https://purchase.aspose.com/temporary-license/)
      to get the required licensing information.
    question: How can I obtain a temporary license?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      for prompt help and discussions.
    question: Need assistance or have questions?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- convert iges to pdf
- Aspose.CAD
- .NET CAD conversion
title: Μετατροπή IGES σε PDF με το Aspose.CAD – Σύντομος Οδηγός
url: /el/net/exporting-to-image-formats/exporting-iges-files-to-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή IGES σε PDF με Aspose.CAD

## Εισαγωγή

Στον ταχύτατα εξελισσόμενο κόσμο του υπολογιστικού σχεδιασμού, η **convert IGES to PDF** είναι μια καθημερινή εργασία που εκτελούν καθημερινά μηχανικοί και αρχιτέκτονες. Είτε χρειάζεστε ένα εκτυπώσιμο έγγραφο για ανασκόπηση από πελάτη είτε ένα ελαφρύ αρχείο για έλεγχο εκδόσεων, η εξαγωγή αρχείων IGES σε PDF διατηρεί τη αρχική γεωμετρία ενώ καθιστά το αρχείο παγκοσμίως προσβάσιμο. Αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα στη μετατροπή IGES σε PDF χρησιμοποιώντας το Aspose.CAD για .NET, ώστε να μπορείτε να αυτοματοποιήσετε τη διαδικασία σε οποιαδήποτε εφαρμογή .NET.

## Γρήγορες Απαντήσεις
- **What library handles the conversion?** Aspose.CAD for .NET.  
- **How many lines of code are required?** Typically two lines: load the IGES file and call `Save`.  
- **Can I control page size and quality?** Yes, via `CadRasterizationOptions`.  
- **Is a license needed for production?** A commercial license is required; a free trial is available. You can obtain a temporary license [this link](https://purchase.aspose.com/temporary-license/).  
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι η “convert IGES to PDF”;
*Converting IGES to PDF* σημαίνει τη λήψη ενός ουδέτερου αρχείου ανταλλαγής CAD (IGES) και την απόδοσή του ως Portable Document Format (PDF) που μπορεί να ανοιχθεί σε οποιαδήποτε συσκευή χωρίς λογισμικό CAD. Η μετατροπή διατηρεί τη διανυσματική γεωμετρία, τα επίπεδα και τις σημειώσεις, ενώ τα ενσωματώνει σε ένα έγγραφο σταθερής διάταξης.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για αυτή τη μετατροπή;
Το Aspose.CAD υποστηρίζει **30+ μορφές CAD και BIM** και μπορεί να επεξεργαστεί αρχεία έως **2 GB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, παρέχοντας γρήγορη μετατροπή από την πλευρά του διακομιστή χωρίς εξαρτήσεις τρίτων. Αυτή η ποσοτικοποιημένη απόδοση το καθιστά ιδανικό για αγωγούς επεξεργασίας παρτίδων και υπηρεσίες βασισμένες στο cloud.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. **Aspose.CAD for .NET Library** – download it from [here](https://releases.aspose.com/cad/net/). You can also view the API reference [here](https://reference.aspose.com/cad/net/).  
2. **.NET development environment** – Visual Studio, Rider, or any IDE that supports .NET 5+.

Τώρα που καλύφθηκαν τα προαπαιτούμενα, ας εισάγουμε τα namespaces που απαιτούνται για τη μετατροπή.

## Εισαγωγή Namespaces

Η κλάση `Image` είναι η κύρια κλάση που αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη. Η `CadRasterizationOptions` ορίζει πώς το σχέδιο CAD θα ραστεροποιηθεί για διανυσματική έξοδο. Η κλάση `PdfOptions` καθορίζει τις ρυθμίσεις εξόδου για αρχεία PDF.

``` 
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
```

Αυτά τα namespaces παρέχουν τη βασική λειτουργικότητα για τη φόρτωση, ραστεροποίηση και αποθήκευση σχεδίων CAD.

## Πώς να μετατρέψετε IGES σε PDF χρησιμοποιώντας το Aspose.CAD;

Φορτώστε το αρχείο IGES με `Image.Load` και καλέστε αμέσως `Save` με μια επιλογή ραστεροποίησης PDF – αυτή είναι η πλήρης μετατροπή σε δύο δηλώσεις. Η βιβλιοθήκη διαχειρίζεται αυτόματα την διανυσματική απόδοση, την ενσωμάτωση γραμματοσειρών και την κλιμάκωση σελίδας, ώστε να λαμβάνετε ένα πιστό αντίγραφο PDF του αρχικού μοντέλου IGES.

### Βήμα 1: Ρυθμίστε το Έργο Σας

Δημιουργήστε ένα νέο έργο .NET console ή class‑library, ή ανοίξτε ένα υπάρχον όπου θέλετε να προσθέσετε τη λειτουργία μετατροπής.

### Βήμα 2: Προσθέστε Αναφορά Aspose.CAD

Προσθέστε το ληφθέν Aspose.CAD DLL στις αναφορές του έργου σας. Στο Visual Studio, κάντε δεξί κλικ στο **References → Add Reference → Browse** και επιλέξτε το DLL.

### Βήμα 3: Αρχικοποιήστε τη Διαδρομή

Ορίστε το φάκελο που περιέχει το αρχείο IGES και την τοποθεσία εξόδου.

``` 
string sourceDir = @"C:\CAD\Source";
string outputDir = @"C:\CAD\Output";
string igesFile = Path.Combine(sourceDir, "sample.iges");
string pdfFile = Path.Combine(outputDir, "sample.pdf");
```

### Βήμα 4: Φορτώστε την Εικόνα CAD

`Image.Load` διαβάζει το αρχείο IGES και δημιουργεί μια αναπαράσταση στη μνήμη.

``` 
Image cadImage = Image.Load(igesFile);
```

Η κλάση `Image` είναι το κύριο σημείο εισόδου του Aspose.CAD για οποιαδήποτε μορφή CAD.

### Βήμα 5: Διαμορφώστε τις Επιλογές Ραστεροποίησης

`PdfOptions` (που προέρχεται από `CadRasterizationOptions`) σας επιτρέπει να ορίσετε το μέγεθος σελίδας, την ανάλυση και σημαίες διατήρησης διανυσματικότητας.

``` 
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 842,      // A4 width in points
        PageHeight = 595,     // A4 height in points
        Resolution = 300      // 300 DPI for high‑quality output
    }
};
```

Η κλάση `PdfOptions` καθορίζει πώς το σχέδιο CAD ραστεροποιείται και αποθηκεύεται ως PDF.

### Βήμα 6: Αποθήκευση ως PDF

Τέλος, γράψτε το αρχείο PDF στο δίσκο.

``` 
cadImage.Save(pdfFile, pdfOptions);
```

Με αυτά τα έξι απλά βήματα, έχετε επιτυχώς **convert iges to pdf** χρησιμοποιώντας το Aspose.CAD για .NET.

## Συνηθισμένα Προβλήματα & Συμβουλές

- **Μεγάλα αρχεία:** Αυξήστε το `Resolution` μόνο αν χρειάζεστε πιο λεπτομερή λεπτομέρεια· υψηλότερο DPI καταναλώνει περισσότερη μνήμη.  
- **Λείπουν γραμματοσειρές:** Βεβαιωθείτε ότι τυχόν προσαρμοσμένες γραμματοσειρές που χρησιμοποιούνται στο αρχείο IGES είναι εγκατεστημένες στον διακομιστή· διαφορετικά θα αντικατασταθούν.  
- **Μετατροπή παρτίδας:** Τυλίξτε τη λογική φόρτωσης‑αποθήκευσης σε βρόχο `foreach` για αυτόματη επεξεργασία πολλαπλών αρχείων IGES.

## Συχνές Ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET σε εφαρμογή web;**  
A: Ναι, το Aspose.CAD λειτουργεί σε ASP.NET, ASP.NET Core και άλλα web frameworks, παρέχοντας μετατροπή από την πλευρά του διακομιστή χωρίς εξαρτήσεις UI.

**Q: Πού μπορώ να βρω πρόσθετη τεκμηρίωση για το Aspose.CAD;**  
A: Εξερευνήστε την ολοκληρωμένη τεκμηρίωση [here](https://reference.aspose.com/cad/net/) για λεπτομερείς πληροφορίες σχετικά με όλες τις υποστηριζόμενες λειτουργίες.

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή [here](https://releases.aspose.com/) για να αξιολογήσετε τη βιβλιοθήκη πριν την αγορά.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια;**  
A: Για προσωρινές άδειες, επισκεφθείτε [this link](https://purchase.aspose.com/temporary-license/) για να λάβετε τις απαιτούμενες πληροφορίες άδειας.

**Q: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;**  
A: Συμμετέχετε στην κοινότητα Aspose.CAD στο [support forum](https://forum.aspose.com/c/cad/19) για άμεση βοήθεια και συζητήσεις.

**Τελευταία ενημέρωση:** 2026-07-09  
**Δοκιμάστηκε με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using static Aspose.CAD.Examples.CSharp.DWG_Drawings.SupportMLeaderEntityForDWGFormat;
using Aspose.CAD.ImageOptions;
```

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "figa2.igs";
```

```csharp
using (Image cadImage = Image.Load(sourceFilePath))
{
    // Your code goes here
}
```

```csharp
CadRasterizationOptions options = new CadRasterizationOptions
{
    PageHeight = 1000,
    PageWidth = 1000,
};

PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = options;
```

```csharp
cadImage.Save(MyDir + "figa2.pdf", pdfOptions);
```

Για πρόσθετους πόρους, δείτε τη σελίδα κυρίων εκδόσεων [here](https://releases.aspose.com/). Αν χρειάζεστε βοήθεια, επισκεφθείτε το [support forum](https://forum.aspose.com/c/cad/19).

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF ή Raster Images - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Εξαγωγή DXF σε PDF Format - Μαθήμα Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Εξαγωγή DGN σε PDF στο Aspose.CAD για .NET](/cad/net/cad-export-formats/export-dgn-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}