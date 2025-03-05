---
title: Προσαρμογή μεγέθους σχεδίου CAD στο Aspose.CAD για .NET
linktitle: Προσαρμογή μεγέθους σχεδίου CAD
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να προσαρμόζετε εύκολα τα μεγέθη σχεδίων CAD στο .NET χρησιμοποιώντας το Aspose.CAD. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη αλλαγή μεγέθους.
type: docs
weight: 10
url: /el/net/cad-drawing-manipulation/adjust-cad-drawing-size/
---
## Εισαγωγή

Ψάχνετε να προσαρμόσετε απρόσκοπτα το μέγεθος των σχεδίων CAD στις εφαρμογές σας .NET; Το Aspose.CAD για .NET παρέχει μια ισχυρή λύση, επιτρέποντάς σας να χειρίζεστε εύκολα το μέγεθος του σχεδίου CAD. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία, αναλύοντας κάθε βήμα για να διασφαλίσουμε ότι κατανοείτε τις περιπλοκές της αλλαγής μεγέθους σχεδίων CAD χρησιμοποιώντας το Aspose.CAD.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Aspose.CAD για .NET Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης από το[Σελίδα λήψης Aspose.CAD για .NET](https://releases.aspose.com/cad/net/).
- Δείγμα σχεδίου CAD: Βεβαιωθείτε ότι έχετε ένα δείγμα αρχείου σχεδίου CAD (π.χ. "sample.dwg") στον κατάλογο εγγράφων σας.

## Εισαγωγή χώρων ονομάτων

Ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων στην εφαρμογή σας .NET. Αυτό το βήμα είναι ζωτικής σημασίας για την πρόσβαση στις λειτουργίες που παρέχονται από το Aspose.CAD για .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση σχεδίου CAD

Ξεκινήστε φορτώνοντας το σχέδιο CAD σε μια παρουσία της κλάσης Aspose.CAD.Image. Βεβαιωθείτε ότι έχετε τη σωστή διαδρομή αρχείου για το δείγμα του σχεδίου σας.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Φορτώστε ένα σχέδιο CAD σε μια παρουσία εικόνας
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Ο κωδικός σας εδώ...
}
```

## Βήμα 2: Δημιουργία BmpOptions

Δημιουργήστε μια παρουσία της κλάσης BmpOptions, η οποία είναι υπεύθυνη για τον καθορισμό επιλογών κατά την αποθήκευση του σχεδίου CAD ως αρχείο BMP.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Βήμα 3: Ορίστε τις επιλογές CadRasterization

Δημιουργήστε την κλάση CadRasterizationOptions και διαμορφώστε τις ιδιότητές της για διανυσματική ραστεροποίηση.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Βήμα 4: Ορίστε την ιδιότητα UnitType

Ορίστε την ιδιότητα UnitType του CadRasterizationOptions για να καθορίσετε τον τύπο μονάδας για αλλαγή μεγέθους. Σε αυτό το παράδειγμα, έχει οριστεί σε Centimeter.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Βήμα 5: Ορίστε την ιδιότητα Layouts

Καθορίστε τις διατάξεις που θέλετε να συμπεριλάβετε στο σχέδιο αλλαγής μεγέθους ορίζοντας την ιδιότητα Layouts.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Βήμα 6: Εξαγωγή σε BMP

Τέλος, αποθηκεύστε τη διάταξη αλλαγής μεγέθους ως αρχείο BMP χρησιμοποιώντας τη μέθοδο Save.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Τώρα έχετε προσαρμόσει επιτυχώς το μέγεθος του σχεδίου σας CAD χρησιμοποιώντας το Aspose.CAD για .NET!

## συμπέρασμα

Σε αυτό το σεμινάριο, ακολουθήσαμε τη διαδικασία αλλαγής μεγέθους σχεδίων CAD στο .NET χρησιμοποιώντας το Aspose.CAD. Ακολουθώντας αυτά τα βήματα, μπορείτε να ενσωματώσετε απρόσκοπτα αυτή τη λειτουργία στις εφαρμογές σας, παρέχοντας μια ομαλή εμπειρία χρήστη.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.CAD για .NET συμβατό με όλες τις μορφές CAD;

 A1: Το Aspose.CAD για .NET υποστηρίζει ένα ευρύ φάσμα μορφών CAD, συμπεριλαμβανομένων των DWG, DXF, DWF και άλλων. Ελεγξε το[τεκμηρίωση](https://reference.aspose.com/cad/net/) για την πλήρη λίστα.

### Ε2: Μπορώ να αλλάξω το μέγεθος πολλών διατάξεων ταυτόχρονα;

A2: Ναι, μπορείτε να αλλάξετε το μέγεθος πολλαπλών διατάξεων προσαρμόζοντας τον πίνακα διατάξεων στις Επιλογές CadRasterization.

### Ε3: Πού μπορώ να λάβω υποστήριξη για το Aspose.CAD για .NET;

 A3: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και βοήθεια.

### Ε4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A4: Ναι, μπορείτε να εξερευνήσετε α[δωρεάν δοκιμή](https://releases.aspose.com/) για την αξιολόγηση των δυνατοτήτων του Aspose.CAD για .NET.

### Ε5: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.CAD για .NET;

 A5: Λάβετε μια προσωρινή άδεια για σκοπούς δοκιμής[εδώ](https://purchase.aspose.com/temporary-license/).