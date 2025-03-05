---
title: Μετατροπή Layouts σε Raster Image στο Aspose.CAD για .NET
linktitle: Μετατροπή Layouts σε Raster Image
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μετατρέψτε εύκολα τις διατάξεις CAD σε εικόνες ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Βελτιώστε την ανάπτυξή σας με ισχυρές δυνατότητες χειρισμού CAD.
type: docs
weight: 12
url: /el/net/cad-drawing-manipulation/convert-layouts-to-raster-image/
---
## Εισαγωγή

Ψάχνετε να μετατρέψετε αβίαστα διατάξεις σε εικόνες ράστερ στις εφαρμογές σας .NET; Μην ψάχνετε άλλο! Αυτός ο οδηγός βήμα προς βήμα θα σας καθοδηγήσει στη διαδικασία χρησιμοποιώντας το Aspose.CAD για .NET, μια ισχυρή βιβλιοθήκη που απλοποιεί τις εργασίες σχεδίασης με τη βοήθεια υπολογιστή (CAD).

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Aspose.CAD για .NET Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης από το[Σελίδα λήψης Aspose.CAD για .NET](https://releases.aspose.com/cad/net/).

- Περιβάλλον ανάπτυξης: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα λειτουργικό περιβάλλον ανάπτυξης .NET στον υπολογιστή σας.

- Έγγραφο σε μετατροπή: Προετοιμάστε ένα έγγραφο CAD που περιέχει τις διατάξεις που θέλετε να μετατρέψετε σε εικόνες ράστερ.

- Ο Κατάλογος εγγράφων σας: Αντικαταστήστε το σύμβολο κράτησης θέσης "Ο Κατάλογος εγγράφων σας" στον κώδικα με τη διαδρομή προς τον κατάλογο εγγράφων σας.

## Εισαγωγή χώρων ονομάτων

Αρχικά, ας εισάγουμε τους απαραίτητους χώρους ονομάτων για να κάνουμε τις λειτουργίες Aspose.CAD προσβάσιμες στον κώδικά σας.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φορτώστε το έγγραφο CAD

Ξεκινήστε φορτώνοντας το έγγραφο CAD χρησιμοποιώντας τη βιβλιοθήκη Aspose.CAD.

```csharp
string sourceFilePath = MyDir + "conic_pyramid.dxf";
using (Image image = Image.Load(sourceFilePath))
{
    //Ο κωδικός σας για περαιτέρω βήματα θα πάει εδώ
}
```

## Βήμα 2: Διαμόρφωση επιλογών ραστεροποίησης

 Δημιουργήστε ένα παράδειγμα του`CadRasterizationOptions` για να ορίσετε το πλάτος, το ύψος της σελίδας και να καθορίσετε τις διατάξεις που θέλετε να μετατρέψετε.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1200;
rasterizationOptions.PageHeight = 1200;
rasterizationOptions.Layouts = new string[] { "Model", "Layout1" };
```

## Βήμα 3: Ρυθμίστε τις επιλογές Tiff για την εικόνα που προκύπτει

 Δημιουργήστε ένα παράδειγμα του`TiffOptions`για να ορίσετε τη μορφή της εικόνας που προκύπτει.

```csharp
ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);
options.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 4: Αποθηκεύστε την εικόνα που προκύπτει

Καθορίστε τη διαδρομή εξόδου και αποθηκεύστε την εικόνα που μετατράπηκε.

```csharp
string outputFilePath = MyDir + "conic_pyramid_layoutstorasterimage_out.tiff";
image.Save(outputFilePath, options);
```

## συμπέρασμα

Συγχαρητήρια! Μετατρέψατε επιτυχώς διατάξεις CAD σε μορφή εικόνας ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Οι δυνατότητες είναι τεράστιες και αυτός ο οδηγός χρησιμεύει ως αφετηρία για τις προσπάθειές σας που σχετίζονται με το CAD.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.CAD συμβατό με όλες τις μορφές CAD;

 A1: Το Aspose.CAD υποστηρίζει ένα ευρύ φάσμα μορφών CAD, συμπεριλαμβανομένων των DWG, DXF, DWF, STL και άλλων. Ελεγξε το[τεκμηρίωση](https://reference.aspose.com/cad/net/) για μια ολοκληρωμένη λίστα.

### Ε2: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.CAD;

 A2: Επισκεφθείτε το[σελίδα προσωρινής άδειας](https://purchase.aspose.com/temporary-license/) να αποκτήσει προσωρινή άδεια για σκοπούς δοκιμών και αξιολόγησης.

### Ε3: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD;

 A3: Τα φόρουμ είναι ένα εξαιρετικό μέρος για να αναζητήσετε βοήθεια. Επισκέψου το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για να συνδεθείτε με την κοινότητα και να λάβετε βοήθεια.

### Ε4: Μπορώ να δοκιμάσω το Aspose.CAD δωρεάν;

 Α4: Απολύτως! Πιάσε το δικό σου[δωρεάν δοκιμή](https://releases.aspose.com/) για να εξερευνήσετε τις δυνατότητες και τις δυνατότητες του Aspose.CAD.

### Ε5: Πού μπορώ να αγοράσω άδεια χρήσης για το Aspose.CAD;

 A5: Πλοηγηθείτε στο[σελίδα αγοράς](https://purchase.aspose.com/buy) για να αγοράσετε μια άδεια και να ξεκλειδώσετε το πλήρες δυναμικό του Aspose.CAD.