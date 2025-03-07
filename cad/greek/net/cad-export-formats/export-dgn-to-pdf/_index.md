---
title: Εξαγωγή DGN σε PDF στο Aspose.CAD για .NET
linktitle: Εξαγωγή DGN σε PDF
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να εξάγετε αρχεία DGN σε PDF χωρίς κόπο με το Aspose.CAD για .NET. Ένας βήμα προς βήμα οδηγός για απρόσκοπτη διαχείριση αρχείων CAD.
weight: 12
url: /el/net/cad-export-formats/export-dgn-to-pdf/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DGN σε PDF στο Aspose.CAD για .NET

## Εισαγωγή

Στον κόσμο της ανάπτυξης .NET, η Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που διευκολύνει τον χειρισμό και τη μετατροπή αρχείων CAD. Μια κοινή εργασία που αντιμετωπίζουν συχνά οι προγραμματιστές είναι η εξαγωγή αρχείων DGN σε μορφή PDF. Σε αυτό το σεμινάριο, θα ακολουθήσουμε τη διαδικασία βήμα προς βήμα, χρησιμοποιώντας το Aspose.CAD για .NET.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τα εξής:

- Γνώση εργασίας της C# και του πλαισίου .NET.
-  Εγκαταστάθηκε το Aspose.CAD για τη βιβλιοθήκη .NET. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/net/).
- Ένα δείγμα αρχείου DGN, για παράδειγμα, "Nikon_D90_Camera.dgn" για αυτό το σεμινάριο.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας C#, ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση αρχείου DGN

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage cadImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Ο κωδικός σας εδώ...
}
```

## Βήμα 2: Διαμόρφωση επιλογών ραστεροποίησης

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Βήμα 3: Δημιουργία επιλογών PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 4: Αποθήκευση ως PDF

```csharp
cadImage.Save(MyDir + "ExportDGNToPdf_out.pdf", pdfOptions);
```

## συμπέρασμα

Συγχαρητήρια! Εξάγατε με επιτυχία ένα αρχείο DGN σε PDF χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το σεμινάριο κάλυψε τα βασικά βήματα, από τη φόρτωση του αρχείου DGN έως τη διαμόρφωση των επιλογών ραστεροποίησης και την αποθήκευση της εξόδου ως PDF.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET χωρίς προηγούμενη γνώση του CAD;

Α1: Απολύτως! Το Aspose.CAD απλοποιεί πολύπλοκες εργασίες CAD, καθιστώντας το προσβάσιμο για προγραμματιστές με διαφορετικά υπόβαθρα.

### Ε2: Πού μπορώ να βρω περισσότερα παραδείγματα και τεκμηρίωση για το Aspose.CAD;

 A2: Εξερευνήστε το[τεκμηρίωση](https://reference.aspose.com/cad/net/) για ολοκληρωμένους οδηγούς και παραδείγματα.

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.CAD;

A3: Ναι, μπορείτε να λάβετε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω προσωρινές άδειες για το Aspose.CAD;

 A4: Λάβετε προσωρινές άδειες[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;

A5: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
