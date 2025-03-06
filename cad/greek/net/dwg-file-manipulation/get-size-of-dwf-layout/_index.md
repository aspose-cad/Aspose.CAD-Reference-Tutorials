---
title: Εργασία με αρχεία DWG σε C# - Λάβετε το μέγεθος της διάταξης DWF
linktitle: Εργασία με αρχεία DWG σε C# - Λάβετε το μέγεθος της διάταξης DWF
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Εξερευνήστε τη δύναμη του Aspose.CAD για .NET στον χειρισμό αρχείων DWG. Μάθετε να εξάγετε μεγέθη διάταξης DWF χωρίς κόπο χρησιμοποιώντας C#.
weight: 10
url: /el/net/dwg-file-manipulation/get-size-of-dwf-layout/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εργασία με αρχεία DWG σε C# - Λάβετε το μέγεθος της διάταξης DWF

## Εισαγωγή

Στον τομέα της σχεδίασης με τη βοήθεια υπολογιστή (CAD) και της ανάπτυξης .NET, το Aspose.CAD αποτελεί ένα ισχυρό εργαλείο για το χειρισμό αρχείων DWG. Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία εργασίας με αρχεία DWG σε C# και εξαγωγής του μεγέθους μιας διάταξης DWF. Πριν βουτήξουμε στον κώδικα, ας βεβαιωθούμε ότι έχετε προετοιμάσει τα πάντα για να ξεκινήσετε αυτό το ταξίδι.

## Προαπαιτούμενα

Για να ακολουθήσετε απρόσκοπτα αυτό το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD για .NET: Βεβαιωθείτε ότι έχετε εγκατεστημένο το Aspose.CAD για .NET. Μπορείτε να το κατεβάσετε από το[Σελίδα λήψης Aspose.CAD για .NET](https://releases.aspose.com/cad/net/).

Τώρα που έχετε τα απαραίτητα εργαλεία, ας μεταβούμε στην αρένα κωδικοποίησης.

## Εισαγωγή χώρων ονομάτων

Πριν ξεκινήσουμε να εργαζόμαστε με τον κώδικα, ας εισαγάγουμε τους απαιτούμενους χώρους ονομάτων:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Dwf;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

Αυτοί οι χώροι ονομάτων θα παρέχουν τις βασικές κλάσεις και μεθόδους για το χειρισμό αρχείων CAD με το Aspose.CAD στην εφαρμογή C#.

## Βήμα 1: Ρυθμίστε το περιβάλλον σας

Ξεκινήστε διασφαλίζοντας ότι έχετε ρυθμίσει το σωστό περιβάλλον για το έργο σας. Ανατρέξτε στη βιβλιοθήκη Aspose.CAD στο έργο σας C#.

## Βήμα 2: Καθορισμός Διαδρομών Αρχείων

Καθορίστε τις διαδρομές για το αρχείο DWG και τον κατάλογο εξόδου για τα αρχεία JPG που δημιουργούνται:

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

## Βήμα 3: Φορτώστε την εικόνα DWF

Φορτώστε την εικόνα DWF χρησιμοποιώντας το Aspose.CAD:

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Ο κώδικας για περαιτέρω βήματα θα πάει εδώ
}
```

## Βήμα 4: Επανάληψη μέσω σελίδων

Επαναλάβετε τις σελίδες της εικόνας DWF:

```csharp
foreach (var page in image.Pages)
{
    // Ο κώδικας για περαιτέρω βήματα θα πάει εδώ
}
```

## Βήμα 5: Λάβετε πληροφορίες διάταξης

Λάβετε πληροφορίες διάταξης από κάθε σελίδα:

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Βήμα 6: Ρύθμιση επιλογών JPG

Ρυθμίστε επιλογές για την αποθήκευση της διάταξης ως αρχείο JPG:

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Ο κώδικας για περαιτέρω βήματα θα πάει εδώ
}
```

## Βήμα 7: Προσδιορίστε το μέγεθος σελίδας

Προσδιορίστε το μέγεθος της διάταξης DWF:

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Ο κώδικας για περαιτέρω βήματα θα πάει εδώ
```

## Βήμα 8: Ρύθμιση Διαστάσεων σελίδας

Ρυθμίστε τις διαστάσεις της σελίδας με βάση τον τύπο μονάδας:

```csharp
if (page.UnitType == UnitType.Inch)
{
    options.PageHeight = CommonHelper.INtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.INtoPixels(sizeExtX, CommonHelper.DPI);
}
else if (page.UnitType == UnitType.Millimeter)
{
    options.PageHeight = CommonHelper.MMtoPixels(sizeExtY, CommonHelper.DPI);
    options.PageWidth = CommonHelper.MMtoPixels(sizeExtX, CommonHelper.DPI);
}
else
{
    options.PageHeight = (float)sizeExtY;
    options.PageWidth = (float)sizeExtX;
}
```

## Βήμα 9: Αποθηκεύστε το αρχείο JPG

Αποθηκεύστε το αρχείο JPG με τις καθορισμένες επιλογές:

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Τώρα έχετε εξαγάγει με επιτυχία το μέγεθος της διάταξης DWF από το αρχείο DWG χρησιμοποιώντας το Aspose.CAD σε C#. Μη διστάσετε να εξερευνήσετε περισσότερες δυνατότητες και λειτουργίες που προσφέρει το Aspose.CAD για την ανάπτυξη .NET.

## συμπέρασμα

Σε αυτό το σεμινάριο, ακολουθήσαμε τη διαδικασία εργασίας με αρχεία DWG σε C# χρησιμοποιώντας το Aspose.CAD. Ακολουθώντας αυτά τα βήματα, μπορείτε όχι μόνο να αποκτήσετε το μέγεθος μιας διάταξης DWF αλλά και να αξιοποιήσετε τις δυνατότητες του Aspose.CAD για διάφορες εργασίες που σχετίζονται με το CAD στα έργα σας .NET.

## Συχνές ερωτήσεις

### Ε1: Είναι το Aspose.CAD συμβατό με τις πιο πρόσφατες μορφές αρχείων DWG;

 A1: Το Aspose.CAD υποστηρίζει διάφορες μορφές αρχείων DWG, συμπεριλαμβανομένων των πιο πρόσφατων εκδόσεων. Αναφέρομαι στο[τεκμηρίωση](https://reference.aspose.com/cad/net/) για συγκεκριμένες λεπτομέρειες συμβατότητας.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.CAD τόσο για εμπορικά όσο και για προσωπικά έργα;

 A2: Ναι, το Aspose.CAD προσφέρει ευέλικτες επιλογές αδειοδότησης τόσο για εμπορική όσο και για προσωπική χρήση. Επισκέψου το[σελίδα αγοράς](https://purchase.aspose.com/buy) Για περισσότερες πληροφορίες.

### Ε3: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.CAD;

 A3: Μπορείτε να λάβετε μια προσωρινή άδεια από[εδώ](https://purchase.aspose.com/temporary-license/) για σκοπούς αξιολόγησης.

### Ε4: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD;

A4: Για οποιαδήποτε απορία ή βοήθεια, επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Ε5: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.CAD;

 A5: Ναι, μπορείτε να αποκτήσετε πρόσβαση σε μια δωρεάν δοκιμαστική έκδοση του Aspose.CAD[εδώ](https://releases.aspose.com/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
