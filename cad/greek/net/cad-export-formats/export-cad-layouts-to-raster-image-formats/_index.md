---
title: Εξαγωγή διατάξεων CAD σε μορφές εικόνας ράστερ στο Aspose.CAD για .NET
linktitle: Εξαγωγή διατάξεων CAD σε μορφές εικόνας ράστερ
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να εξάγετε διατάξεις CAD σε εικόνες ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη μετατροπή.
weight: 10
url: /el/net/cad-export-formats/export-cad-layouts-to-raster-image-formats/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή διατάξεων CAD σε μορφές εικόνας ράστερ στο Aspose.CAD για .NET

## Εισαγωγή

Ψάχνετε να μετατρέψετε αποτελεσματικά διατάξεις CAD σε μορφές εικόνας ράστερ χρησιμοποιώντας το Aspose.CAD για .NET; Αυτός ο οδηγός βήμα προς βήμα θα σας καθοδηγήσει στη διαδικασία, παρέχοντας λεπτομερείς οδηγίες και αποσπάσματα κώδικα για να κάνετε την εργασία απρόσκοπτη. Είτε είστε έμπειρος προγραμματιστής είτε αρχάριος στο Aspose.CAD, αυτό το σεμινάριο καλύπτει όλα τα επίπεδα τεχνογνωσίας.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τα εξής:

- Aspose.CAD για .NET Library: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD. Εάν όχι, μπορείτε να το κατεβάσετε από το[Ιστότοπος Aspose.CAD](https://releases.aspose.com/cad/net/).

- Αρχείο σχεδίασης CAD: Προετοιμάστε ένα αρχείο σχεδίασης CAD (π.χ. conic_pyramid.dxf) που θέλετε να μετατρέψετε σε μορφές εικόνας ράστερ.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας .NET, εισαγάγετε τους απαραίτητους χώρους ονομάτων για να αξιοποιήσετε τις λειτουργίες Aspose.CAD. Συμπεριλάβετε τους ακόλουθους χώρους ονομάτων στην αρχή του κώδικά σας:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση σχεδίου CAD

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

// Φορτώστε ένα σχέδιο CAD σε μια παρουσία εικόνας
using (var image = Image.Load(sourceFilePath))
{
    // Ο κωδικός σας για τη φόρτωση του σχεδίου CAD πηγαίνει εδώ
}
```

## Βήμα 2: Δημιουργήστε CadRasterizationOptions

```csharp
// Δημιουργήστε μια παρουσία του CadRasterizationOptions
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 500;
rasterizationOptions.PageHeight = 500;
```

## Βήμα 3: Καθορίστε επίπεδα

```csharp
// Προσθέστε το όνομα του επιπέδου στη λίστα επιπέδων του CadRasterizationOptions
rasterizationOptions.Layers = new string[] { "LayerA" };
```

## Βήμα 4: Δημιουργήστε JpegOptions

```csharp
// Δημιουργήστε μια παρουσία του JpegOptions (ή οποιωνδήποτε Επιλογών εικόνας για μορφές ράστερ)
var options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 5: Εξαγωγή σε μορφή Jpeg

```csharp
// Εξαγωγή κάθε επιπέδου σε μορφή Jpeg
MyDir = MyDir + "CADLayersToRasterImageFormats_out.jpg";
image.Save(MyDir, options);
```

## Πρόσθετο βήμα: Μετατροπή όλων των επιπέδων

Εάν θέλετε να μετατρέψετε όλα τα επίπεδα, χρησιμοποιήστε την ακόλουθη μέθοδο:

```csharp
ConvertAllLayersToRasterImageFormats();
```

Αυτή η μέθοδος επαναλαμβάνεται σε όλα τα επίπεδα στο σχέδιο CAD, εξάγοντας κάθε επίπεδο σε ένα ξεχωριστό αρχείο Jpeg.

## συμπέρασμα

Συγχαρητήρια! Μάθατε με επιτυχία πώς να εξάγετε διατάξεις CAD σε μορφές εικόνας ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το σεμινάριο παρέχει έναν ολοκληρωμένο οδηγό για προγραμματιστές που αναζητούν αποτελεσματικές και αξιόπιστες λύσεις για μετατροπή CAD.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω άλλες μορφές εικόνας για εξαγωγή;

 Α1: Ναι, μπορείς. Απλώς αντικαταστήστε`JpegOptions` με τις επιλογές της επιθυμητής μορφής, όπως π.χ`PngOptions` ή`BmpOptions`.

### Ε2: Υπάρχει διαθέσιμη δοκιμαστική έκδοση;

 A2: Ναι, μπορείτε να εξερευνήσετε τη λειτουργικότητα του Aspose.CAD κατεβάζοντας τη δοκιμαστική έκδοση[εδώ](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;

 A3: Επισκεφθείτε το Aspose.CAD[δικαστήριο](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη ή σκεφτείτε να αγοράσετε άδεια για αποκλειστική υποστήριξη.

### Ε4: Είναι διαθέσιμες προσωρινές άδειες;

 A4: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να βρω την τεκμηρίωση;

 A5: Ανατρέξτε στη λεπτομερή τεκμηρίωση[εδώ](https://reference.aspose.com/cad/net/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
