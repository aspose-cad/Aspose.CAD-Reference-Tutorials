---
title: Εξαγωγή DGN ως μέρος του DWG στο Aspose.CAD για .NET
linktitle: Εξαγωγή DGN ως μέρος του DWG
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε πώς να εξάγετε το DGN ως μέρος του DWG στο Aspose.CAD για .NET. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη ενσωμάτωση.
weight: 11
url: /el/net/cad-export-formats/export-dgn-as-part-of-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DGN ως μέρος του DWG στο Aspose.CAD για .NET

## Εισαγωγή

Στον κόσμο της ανάπτυξης .NET, το Aspose.CAD ξεχωρίζει ως μια ισχυρή βιβλιοθήκη για εργασία με αρχεία σχεδίασης με τη βοήθεια υπολογιστή (CAD). Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία εξαγωγής ενός αρχείου DGN (Design) ως μέρος ενός αρχείου DWG (Σχέδιο) χρησιμοποιώντας το Aspose.CAD για .NET. Είτε είστε έμπειρος προγραμματιστής είτε μόλις ξεκινάτε, αυτός ο οδηγός βήμα προς βήμα θα σας βοηθήσει να αξιοποιήσετε τις δυνατότητες του Aspose.CAD για να επιτύχετε αποτελεσματικά αυτήν τη συγκεκριμένη εργασία.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD για .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD για .NET. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/net/).

- Περιβάλλον ανάπτυξης: Ρυθμίστε το περιβάλλον ανάπτυξης .NET που προτιμάτε, όπως το Visual Studio.

- Βασικές γνώσεις C#: Εξοικειωθείτε με τη γλώσσα προγραμματισμού C#.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας C#, συμπεριλάβετε τους απαραίτητους χώρους ονομάτων για πρόσβαση στη λειτουργικότητα Aspose.CAD. Προσθέστε τα ακόλουθα χρησιμοποιώντας οδηγίες στην αρχή του αρχείου κώδικα:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

Τώρα, ας αναλύσουμε τον παρεχόμενο κώδικα σε πολλά βήματα:

## Βήμα 1: Καθορισμός Διαδρομών Αρχείων

```csharp
//Διαδρομές αρχείων εισόδου και εξόδου
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

## Βήμα 2: Δημιουργία παρουσίας PdfOptions

```csharp
// Δημιουργήστε μια παρουσία της κλάσης PdfOptions για εξαγωγή DWG σε PDF
PdfOptions exportOptions = new PdfOptions();
```

## Βήμα 3: Φορτώστε το αρχείο DWG

```csharp
// Φορτώστε το υπάρχον αρχείο DWG ως εικόνα και μετατρέψτε το σε τύπο CadImage
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

## Βήμα 4: Επανάληψη μέσω οντοτήτων

```csharp
// Επαναλάβετε σε κάθε οντότητα μέσα στο αρχείο DWG
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

## Βήμα 5: Ελέγξτε τον τύπο οντότητας

```csharp
// Ελέγξτε εάν η οντότητα είναι ορισμός εικόνας
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

## Βήμα 6: Λήψη διαδρομής υποστρώματος

```csharp
// Εάν πρόκειται για ορισμό εικόνας, λάβετε την εξωτερική αναφορά στο αντικείμενο
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

## Βήμα 7: Ορίστε τις επιλογές ραστεροποίησης

```csharp
// Ορίστε ρυθμίσεις για το αντικείμενο CadRasterizationOptions
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

## Βήμα 8: Εξαγωγή DWG σε PDF

```csharp
// Εξάγετε το DWG σε PDF καλώντας τη μέθοδο αποθήκευσης
cadImage.Save(outPath, exportOptions);
```

## συμπέρασμα

Συγχαρητήρια! Έχετε προχωρήσει με επιτυχία στη διαδικασία εξαγωγής ενός αρχείου DGN ως τμήμα ενός αρχείου DWG χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το σεμινάριο σάς παρέχει τα βασικά βήματα και τα αποσπάσματα κώδικα για να επιτύχετε απρόσκοπτα αυτήν τη συγκεκριμένη εργασία.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET στα εμπορικά έργα μου;
 Α1: Ναι, μπορείς. Επίσκεψη[εδώ](https://purchase.aspose.com/buy) για να εξερευνήσετε τις επιλογές αδειοδότησης.

### Ε2: Υπάρχουν περιορισμοί στο μέγεθος των αρχείων DWG που μπορώ να επεξεργαστώ;
A2: Το Aspose.CAD υποστηρίζει το χειρισμό μεγάλων αρχείων DWG, αλλά ενδέχεται να ισχύουν περιορισμοί υλικού.

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση;
A3: Ναι, μπορείτε να λάβετε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω προσωρινές άδειες;
 A4: Μπορούν να ληφθούν προσωρινές άδειες[εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να αναζητήσω βοήθεια εάν αντιμετωπίσω προβλήματα;
 A5: Μπορείτε να επισκεφτείτε το φόρουμ Aspose.CAD[εδώ](https://forum.aspose.com/c/cad/19) για υποστήριξη.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
