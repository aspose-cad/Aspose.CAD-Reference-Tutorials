---
title: Ρύθμιση μεγέθους καμβά και λειτουργίας στο Aspose.CAD για .NET
linktitle: Ρύθμιση μεγέθους καμβά και λειτουργίας
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Εξερευνήστε τον οδηγό βήμα προς βήμα για τη ρύθμιση του μεγέθους και της λειτουργίας καμβά στο Aspose.CAD για .NET. Βελτιστοποιήστε την απόδοση CAD με ευκολία χρησιμοποιώντας αυτό το περιεκτικό σεμινάριο.
weight: 16
url: /el/net/cad-features-and-support/setting-canvas-size-and-mode/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ρύθμιση μεγέθους καμβά και λειτουργίας στο Aspose.CAD για .NET

## Εισαγωγή

Είστε έτοιμοι να ξεκλειδώσετε πλήρως τις δυνατότητες του Aspose.CAD για .NET και να φέρετε επανάσταση στην εμπειρία απόδοσης CAD; Σε αυτό το βήμα προς βήμα σεμινάριο, θα εμβαθύνουμε στις περιπλοκές της ρύθμισης του μεγέθους και της λειτουργίας καμβά χρησιμοποιώντας την ισχυρή βιβλιοθήκη Aspose.CAD. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε, αυτός ο οδηγός θα σας καθοδηγήσει στη διαδικασία, διασφαλίζοντας ότι αξιοποιείτε αποτελεσματικά τις δυνατότητες του Aspose.CAD.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.CAD από το[Ιστότοπος Aspose.CAD](https://releases.aspose.com/cad/net/).

- Περιβάλλον ανάπτυξης: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα περιβάλλον ανάπτυξης .NET στον υπολογιστή σας.

-  Δείγμα αρχείου CAD: Για αυτό το σεμινάριο, θα χρησιμοποιήσουμε ένα δείγμα αρχείου DXF. Μπορείτε να βρείτε ένα στο[Τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/net/).

## Εισαγωγή χώρων ονομάτων

Για να ξεκινήσετε, εισαγάγετε τους απαραίτητους χώρους ονομάτων στην αρχή της εφαρμογής σας .NET:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση αρχείου CAD

Ξεκινήστε φορτώνοντας το αρχείο CAD χρησιμοποιώντας τον ακόλουθο κώδικα:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    //Ο κωδικός σας για περαιτέρω βήματα θα πάει εδώ
}
```

## Βήμα 2: Δημιουργήστε CadRasterizationOptions

 Δημιουργήστε ένα παράδειγμα του`CadRasterizationOptions` και ορίστε τις ιδιότητες του:

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

## Βήμα 3: Δημιουργία PdfOptions

 Δημιουργήστε ένα παράδειγμα του`PdfOptions` και ρυθμίστε το`VectorRasterizationOptions` ιδιοκτησία:

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 4: Εξαγωγή σε PDF

Εξάγετε το αρχείο CAD σε PDF χρησιμοποιώντας τις διαμορφωμένες επιλογές:

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

## Βήμα 5: Δημιουργήστε TiffOptions

 Δημιουργήστε ένα παράδειγμα του`TiffOptions` και ρυθμίστε το`VectorRasterizationOptions` ιδιοκτησία:

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 6: Εξαγωγή στο TIFF

Εξάγετε το αρχείο CAD στο TIFF χρησιμοποιώντας τις διαμορφωμένες επιλογές:

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## συμπέρασμα

Συγχαρητήρια! Έχετε ορίσει με επιτυχία το μέγεθος και τη λειτουργία καμβά στο Aspose.CAD για .NET. Αυτή η ισχυρή δυνατότητα ανοίγει έναν κόσμο δυνατοτήτων για απόδοση CAD. Πειραματιστείτε με διαφορετικές επιλογές και ανακαλύψτε τις πλήρεις δυνατότητες του Aspose.CAD στις εφαρμογές σας .NET.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλες βιβλιοθήκες .NET;

A1: Ναι, το Aspose.CAD ενσωματώνεται απρόσκοπτα με άλλες βιβλιοθήκες .NET, παρέχοντας βελτιωμένες δυνατότητες για χειρισμό CAD.

### Ε2: Διατίθεται δωρεάν δοκιμή για το Aspose.CAD;

 A2: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD με μια δωρεάν δοκιμή. Επίσκεψη[εδώ](https://releases.aspose.com/) για να ξεκινήσετε.

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;

 A3: Για υποστήριξη και συζητήσεις, επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Ε4: Πού μπορώ να βρω ολοκληρωμένη τεκμηρίωση για το Aspose.CAD;

 A4: Ανατρέξτε στο[Τεκμηρίωση Aspose.CAD](https://reference.aspose.com/cad/net/) για λεπτομερείς πληροφορίες και παραδείγματα.

### Ε5: Πώς μπορώ να αγοράσω το Aspose.CAD για .NET;

 A5: Για να αγοράσετε Aspose.CAD, επισκεφτείτε το[σελίδα αγοράς](https://purchase.aspose.com/buy).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
