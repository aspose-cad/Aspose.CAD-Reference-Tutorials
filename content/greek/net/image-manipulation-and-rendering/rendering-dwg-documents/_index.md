---
title: Απόδοση εγγράφων DWG σε C# - Οδηγός Aspose.CAD
linktitle: Απόδοση εγγράφων DWG σε C#
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να αποδίδετε έγγραφα DWG σε C# χρησιμοποιώντας το Aspose.CAD. Αυτός ο οδηγός βήμα προς βήμα καλύπτει την εισαγωγή, τη διαμόρφωση και την αποθήκευση με παραδείγματα κώδικα.
type: docs
weight: 17
url: /el/net/image-manipulation-and-rendering/rendering-dwg-documents/
---
## Εισαγωγή

Καλώς ήρθατε στον αναλυτικό οδηγό για την απόδοση εγγράφων DWG σε C# χρησιμοποιώντας το Aspose.CAD. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε με το .NET, αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία αξιοποίησης του Aspose.CAD για την αποτελεσματική απόδοση των αρχείων DWG. Το Aspose.CAD είναι ένα ισχυρό API που παρέχει ισχυρές λειτουργίες για εργασία με μορφές αρχείων CAD, καθιστώντας το μια πρώτη επιλογή για προγραμματιστές που ασχολούνται με αρχεία DWG.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Βασικές γνώσεις γλώσσας προγραμματισμού C#.
- Το Visual Studio είναι εγκατεστημένο στον υπολογιστή σας.
-  Η βιβλιοθήκη Aspose.CAD είναι ενσωματωμένη στο έργο σας. Μπορείτε να το κατεβάσετε από[εδώ](https://releases.aspose.com/cad/net/).
- Ένα δείγμα αρχείου DWG, όπως "Bottom_plate.dwg", για να ακολουθήσει μαζί με τα παραδείγματα.

## Εισαγωγή χώρων ονομάτων

Για να ξεκινήσετε, φροντίστε να εισαγάγετε τους απαραίτητους χώρους ονομάτων στην αρχή του κώδικα C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Τώρα, ας αναλύσουμε το παρεχόμενο παράδειγμα σε πολλά βήματα:

## Βήμα 1: Φορτώστε το αρχείο DWG

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Ο κωδικός σας για τη φόρτωση του αρχείου DWG πηγαίνει εδώ.
}
```

## Βήμα 2: Διαμόρφωση επιλογών ραστεροποίησης

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
//Επιπρόσθετες διαμορφώσεις ραστεροποίησης μπορούν να προστεθούν εδώ.
```

## Βήμα 3: Ορίστε την περιοχή προς σχεδίαση

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Βήμα 4: Δημιουργήστε μια νέα θύρα προβολής

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Βήμα 5: Αντικαταστήστε το Active Viewport

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Βήμα 6: Διαμόρφωση επιλογών PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 7: Αποθηκεύστε το Rendered DWG ως PDF

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## συμπέρασμα

Συγχαρητήρια! Έχετε αποδώσει με επιτυχία ένα έγγραφο DWG σε PDF χρησιμοποιώντας το Aspose.CAD σε C#. Μη διστάσετε να εξερευνήσετε περισσότερες δυνατότητες και να προσαρμόσετε τον κώδικα με βάση τις συγκεκριμένες απαιτήσεις σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλες μορφές αρχείων CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF, DWF και άλλων.

### Ε2: Είναι το Aspose.CAD συμβατό με .NET Core;

A2: Ναι, το Aspose.CAD είναι συμβατό τόσο με .NET Framework όσο και με .NET Core.

### Ε3: Πώς μπορώ να χειριστώ διαφορετικές διατάξεις σε ένα αρχείο DWG;

 A3: Μπορείτε να καθορίσετε την επιθυμητή διάταξη στο`Layouts` Ιδιοκτησία του`CadRasterizationOptions`.

### Ε4: Υπάρχουν ζητήματα αδειοδότησης για τη χρήση του Aspose.CAD;

 A4: Για λεπτομέρειες αδειοδότησης, επισκεφθείτε[εδώ](https://purchase.aspose.com/buy).

### Ε5: Πού μπορώ να βρω πρόσθετη υποστήριξη;

A5: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και συζητήσεις.