---
title: Μετατροπή DWG σε PDF με Συντεταγμένες σε C# - Εκμάθηση Aspose.CAD
linktitle: Μετατροπή DWG σε PDF με συντεταγμένες σε C#
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να μετατρέπετε το DWG σε PDF με συγκεκριμένες συντεταγμένες σε C# χρησιμοποιώντας το Aspose.CAD. Ακολουθήστε τον οδηγό βήμα προς βήμα για ακριβείς και αποτελεσματικές μετατροπές αρχείων CAD.
type: docs
weight: 11
url: /el/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
---
## Εισαγωγή

Καλώς ήρθατε σε αυτό το ολοκληρωμένο σεμινάριο για τη μετατροπή αρχείων DWG σε PDF με καθορισμένες συντεταγμένες χρησιμοποιώντας το Aspose.CAD για .NET. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που επιτρέπει στους προγραμματιστές να εργάζονται με μορφές αρχείων CAD στις εφαρμογές τους .NET απρόσκοπτα. Σε αυτό το σεμινάριο, θα σας καθοδηγήσουμε στη διαδικασία μετατροπής ενός αρχείου DWG σε PDF παρέχοντας παράλληλα συγκεκριμένες συντεταγμένες για βελτίωση της ακρίβειας.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Aspose.CAD Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.CAD για .NET. Μπορείτε να βρείτε τη βιβλιοθήκη[εδώ](https://releases.aspose.com/cad/net/).

- Περιβάλλον ανάπτυξης: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα συμβατό περιβάλλον ανάπτυξης, συμπεριλαμβανομένου του Visual Studio ή οποιουδήποτε άλλου προτιμώμενου IDE.

- Αρχείο DWG: Έχετε ένα αρχείο DWG έτοιμο για μετατροπή. Μπορείτε να χρησιμοποιήσετε το παρεχόμενο παράδειγμα αρχείου ή το προσαρμοσμένο αρχείο DWG.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας C#, εισαγάγετε τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Ας αναλύσουμε τον κώδικα σε έναν οδηγό βήμα προς βήμα για καλύτερη κατανόηση:

## Βήμα 1: Ορίστε τον Κατάλογο Εγγράφων

```csharp
string MyDir = "Your Document Directory";
```

## Βήμα 2: Ορίστε τη διαδρομή αρχείου προέλευσης DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Βήμα 3: Φορτώστε το αρχείο DWG και διαμορφώστε τις επιλογές ραστεροποίησης

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Βήμα 4: Καθορίστε τις συντεταγμένες και τη θύρα προβολής

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Βήμα 5: Εφαρμογή ρυθμίσεων Viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Βήμα 6: Διαμόρφωση επιλογών PDF και εξαγωγή

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Βήμα 7: Εμφάνιση μηνύματος επιτυχίας

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## συμπέρασμα

Συγχαρητήρια! Μετατρέψατε επιτυχώς ένα αρχείο DWG σε PDF με καθορισμένες συντεταγμένες χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το σεμινάριο κάλυψε βασικά βήματα και παρείχε έναν σαφή οδηγό για τους προγραμματιστές.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλες μορφές αρχείων CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF, DWF και άλλων.

### Ε2: Πώς μπορώ να χειριστώ σφάλματα κατά τη διαδικασία μετατροπής;

A2: Εφαρμόστε μηχανισμούς διαχείρισης σφαλμάτων χρησιμοποιώντας μπλοκ try-catch για τη λήψη και τη διαχείριση εξαιρέσεων.

### Ε3: Είναι το Aspose.CAD κατάλληλο για περιβάλλοντα Windows και Linux;

A3: Ναι, το Aspose.CAD είναι συμβατό με πλατφόρμες Windows και Linux.

### Ε4: Μπορώ να προσαρμόσω περαιτέρω την έξοδο PDF;

Α4: Σίγουρα! Εξερευνήστε τις εκτενείς επιλογές που παρέχονται από το Aspose.CAD για να προσαρμόσετε την έξοδο PDF στις συγκεκριμένες απαιτήσεις σας.

### Ε5: Πού μπορώ να βρω πρόσθετη υποστήριξη ή συζητήσεις στην κοινότητα;

A5: Επισκεφθείτε το[Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και συζητήσεις.