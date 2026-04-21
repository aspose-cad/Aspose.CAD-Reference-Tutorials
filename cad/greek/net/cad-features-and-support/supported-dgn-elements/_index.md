---
date: 2026-03-29
description: Μάθετε πώς να μετατρέπετε DGN σε PNG χρησιμοποιώντας το Aspose.CAD για
  .NET. Αυτός ο οδηγός καλύπτει επίσης την υποστήριξη μορφών αρχείων CAD και το πλήρες
  σύνολο των υποστηριζόμενων στοιχείων DGN.
linktitle: Supported DGN Elements
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Μετατροπή DGN σε PNG με το Aspose.CAD για .NET
url: /el/net/cad-features-and-support/supported-dgn-elements/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DGN σε PNG με Aspose.CAD για .NET

## Εισαγωγή

Είστε προγραμματιστής .NET που θέλει να **μετατρέψει DGN σε PNG** άψογα; Το Aspose.CAD για .NET παρέχει μια ισχυρή λύση για την αποδοτική διαχείριση αρχείων DGN. Σε αυτό το εκπαιδευτικό υλικό, θα εμβαθύνουμε στα υποστηριζόμενα στοιχεία DGN, καθοδηγώντας σας στη διαδικασία εργασίας με το Aspose.CAD για .NET ενώ θα σας δείξουμε ακριβώς πώς να εξάγετε αυτά τα στοιχεία σε εικόνες PNG.

## Γρήγορες Απαντήσεις
- **Τι κάνει το Aspose.CAD;** Διαβάζει, τροποποιεί και μετατρέπει αρχεία CAD/BIM (συμπεριλαμβανομένου του DGN) σε μορφές raster όπως PNG.  
- **Μπορώ να μετατρέψω στοιχεία DGN 2D και 3D;** Ναι – υποστηρίζονται τόσο οι οντότητες 2‑Δ όσο και 3‑Δ.  
- **Ποιες εκδόσεις .NET απαιτούνται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Χρειάζομαι άδεια για δοκιμές;** Διατίθεται δωρεάν δοκιμή· απαιτείται άδεια για παραγωγή.  
- **Από πού μπορώ να κατεβάσω τη βιβλιοθήκη;** Κατεβάστε την από την επίσημη ιστοσελίδα της Aspose (σύνδεσμος παρακάτω).

## Τι είναι η «μετατροπή DGN σε PNG»;
Η μετατροπή DGN σε PNG σημαίνει απόδοση του διανυσματικού σχεδίου DGN (2‑Δ ή 3‑Δ) σε μορφή raster εικόνας (PNG). Αυτό είναι χρήσιμο όταν χρειάζεται να εμφανίσετε σχέδια CAD στο web, να τα ενσωματώσετε σε αναφορές ή να δημιουργήσετε μικρογραφίες χωρίς να απαιτείται προβολέας CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για .NET για υποστήριξη μορφών αρχείων CAD;
- **Πλήρης υποστήριξη μορφών αρχείων CAD** – DGN, DWG, DXF, DWF και άλλα.  
- **Χωρίς εξωτερικές εξαρτήσεις** – καθαρή βιβλιοθήκη .NET, χωρίς εγκαταστάσεις CAD.  
- **Απόδοση υψηλής πιστότητας** – διατηρεί το βάρος γραμμών, τα χρώματα και τη γεωμετρία 3‑Δ.  
- **Επεξεργασία παρτίδας** – εύκολη επανάληψη σε πολλά αρχεία σε εφαρμογή διακομιστή.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

- Βασικές γνώσεις προγραμματισμού .NET.  
- Εγκατεστημένο Visual Studio στον υπολογιστή σας.  
- Βιβλιοθήκη Aspose.CAD για .NET, την οποία μπορείτε να κατεβάσετε [εδώ](https://releases.aspose.com/cad/net/).

## Εισαγωγή Namespaces

Για να ξεκινήσετε το έργο σας, εισάγετε τα απαραίτητα namespaces στην εφαρμογή .NET. Αυτό το βήμα εξασφαλίζει ότι έχετε πρόσβαση στις λειτουργίες που παρέχει το Aspose.CAD για .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.FileFormats.Dgn.DgnElements;
```

## Πώς να Μετατρέψετε DGN σε PNG

### Βήμα 1: Φόρτωση του Αρχείου DGN

Ξεκινήστε φορτώνοντας ένα υπάρχον αρχείο DGN ως `DgnImage` στην εφαρμογή .NET.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

### Βήμα 2: Επανάληψη μέσω των Στοιχείων DGN

Περιηγηθείτε στα στοιχεία DGN χρησιμοποιώντας έναν βρόχο `foreach`. Το Aspose.CAD για .NET παρέχει μια ποικιλία τύπων στοιχείων DGN με τα οποία μπορείτε να εργαστείτε.

```csharp
foreach (DgnDrawingElementBase element in dgnImage.Elements)
{
    // Your code here
}
```

### Βήμα 3: Διαχείριση Πρώην Υποστηριζόμενων Στοιχείων 2‑Δ

Αυτές οι οντότητες υποστηρίζονται πλέον και για απόδοση 3‑Δ. Η εντολή switch σας επιτρέπει να διακλαδώνετε τη λογική βάσει του τύπου του στοιχείου.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.Line:
    case DgnElementType.Ellipse:
    case DgnElementType.Curve:
    // Additional cases
        {
            // Your code here
            break;
        }
}
```

### Βήμα 4: Διαχείριση Υποστηριζόμενων Στοιχείων 3‑Δ

Το Aspose.CAD προσθέτει πλήρη υποστήριξη για αρκετά στοιχεία DGN 3‑Δ. Επεκτείνετε το switch για να τα επεξεργαστείτε όπως απαιτείται.

```csharp
switch (element.Metadata.Type)
{
    case DgnElementType.SolidHeader3D:
    case DgnElementType.Cone:
    case DgnElementType.CellHeader:
        {
            // Your code here
            break;
        }
}
```

### Βήμα 5: Εξαγωγή και Αποθήκευση ως PNG

Μετά από τυχόν απαιτούμενες επεξεργασίες, εξάγετε το σχέδιο DGN σε εικόνα raster PNG και αποθηκεύστε το στον καθορισμένο φάκελο.

```csharp
Console.WriteLine("\nThe DGN file exported successfully to raster image.\nFile saved at " + MyDir);
```

> **Συμβουλή:** Χρησιμοποιήστε `Image.Save` με `new PngOptions()` για να ελέγξετε την ανάλυση, το χρώμα φόντου και άλλες ρυθμίσεις ειδικές για PNG.

## Επισκόπηση Υποστήριξης Μορφών Αρχείων CAD

Το Aspose.CAD για .NET δεν περιορίζεται μόνο στο DGN. Υποστηρίζει επίσης DWG, DXF, DWF και πολλές άλλες μορφές CAD, παρέχοντάς σας ένα ενιαίο API για τη διαχείριση ενός ευρέος φάσματος τεχνικών σχεδίων. Αυτό το καθιστά ιδανικό για έργα που απαιτούν **υποστήριξη μορφών αρχείων CAD** σε πολλαπλά πρότυπα.

## Συχνά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Η εικόνα εμφανίζεται κενή** | Εξήχθη με μηδενικό DPI | Καθορίστε `ResolutionX` και `ResolutionY` στο `PngOptions`. |
| **Λείπει γεωμετρία 3‑Δ** | Ο τύπος στοιχείου δεν αντιμετωπίστηκε στο switch | Προσθέστε την ελλιπή περίπτωση `DgnElementType` και αποδώστε ανάλογα. |
| **Έλλειψη μνήμης σε μεγάλα αρχεία** | Φόρτωση ολόκληρου του αρχείου ταυτόχρονα | Επεξεργαστείτε τα στοιχεία σε παρτίδες ή χρησιμοποιήστε streaming όπου είναι δυνατόν. |

## Συχνές Ερωτήσεις

### Q1: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.CAD για .NET;
A1: Μπορείτε να βρείτε την τεκμηρίωση [εδώ](https://reference.aspose.com/cad/net/).

### Q2: Πώς να κατεβάσω το Aspose.CAD για .NET;
A2: Μπορείτε να κατεβάσετε τη βιβλιοθήκη [εδώ](https://releases.aspose.com/cad/net/).

### Q3: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD για .NET;
A3: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q4: Πού μπορώ να αποκτήσω προσωρινές άδειες για το Aspose.CAD για .NET;
A4: Οι προσωρινές άδειες είναι διαθέσιμες [εδώ](https://purchase.aspose.com/temporary-license/).

### Q5: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;
A5: Επισκεφθείτε το κοινό Aspose.CAD για .NET [φόρουμ υποστήριξης](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-03-29  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}