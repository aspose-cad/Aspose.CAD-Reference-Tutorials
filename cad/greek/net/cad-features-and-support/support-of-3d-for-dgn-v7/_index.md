---
date: 2026-03-29
description: Μάθετε πώς να διαμορφώσετε τις επιλογές rasterization του CAD και να
  εξάγετε DGN σε PDF με υποστήριξη 3D χρησιμοποιώντας το Aspose.CAD για .NET.
linktitle: Support of 3D for DGN V7
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Διαμορφώστε τις επιλογές ραστεροποίησης CAD για DGN V7 3D
url: /el/net/cad-features-and-support/support-of-3d-for-dgn-v7/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Διαμόρφωση επιλογών rasterization CAD για DGN V7 3D

## Εισαγωγή

Σε αυτό το ολοκληρωμένο tutorial θα μάθετε **πώς να διαμορφώσετε τις επιλογές rasterization CAD** για να εξάγετε ένα αρχείο DGN V7 3‑Δ σε PDF χρησιμοποιώντας το Aspose.CAD για .NET. Είτε δημιουργείτε έναν προβολέα CAD, ένα εργαλείο αναφοράς ή μια αυτοματοποιημένη γραμμή μετατροπής, η κατανόηση αυτών των ρυθμίσεων σας παρέχει ακριβή έλεγχο του μεγέθους σελίδας, της κλιμάκωσης διάταξης, των χρωμάτων φόντου και των συγκεκριμένων προβολών που θέλετε να αποδώσετε. Ας προχωρήσουμε στη διαδικασία βήμα προς βήμα.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει το “configure CAD rasterization options”;**  
  Αναφέρεται στον ορισμό ιδιοτήτων όπως διαστάσεις σελίδας, κλιμάκωση, χρώμα φόντου και επιλογή διάταξης πριν από τη μετατροπή ενός αρχείου CAD σε μορφή raster (π.χ., PDF).
- **Πώς να εξάγετε DGN σε PDF με υποστήριξη 3‑Δ;**  
  Φορτώστε το DGN με `DgnImage`, ορίστε `PdfOptions` + `CadRasterizationOptions`, στη συνέχεια καλέστε `Save`.
- **Χρειάζομαι άδεια για παραγωγική χρήση;**  
  Ναι – απαιτείται εμπορική άδεια για την ανάπτυξη· διατίθεται δωρεάν δοκιμή.
- **Ποιες εκδόσεις .NET υποστηρίζονται;**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Μπορώ να επιλέξω συγκεκριμένες προβολές για εξαγωγή;**  
  Απόλυτα – ορίστε τον πίνακα `Layouts` στις επιλογές rasterization.

## Τι είναι το “configure CAD rasterization options”

Η διαμόρφωση των επιλογών rasterization CAD σημαίνει την προσαρμογή του τρόπου rasterization (μετατροπής) ενός σχεδίου CAD (από διανυσματικό σε bitmap ή PDF). Με την προσαρμογή αυτών των ρυθμίσεων ελέγχετε την οπτική έξοδο, την απόδοση και το μέγεθος αρχείου του παραγόμενου εγγράφου.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για εξαγωγή 3‑Δ DGN V7;

- **Πλήρης ενσωμάτωση .NET** – δεν απαιτούνται COM ή εγγενή DLLs.  
- **Υποστηρίζει γεωμετρία 3‑Δ** – διατηρεί τις πληροφορίες βάθους κατά την απόδοση σε PDF.  
- **Λεπτομερής έλεγχος** – επιλέξτε ακριβείς διατάξεις, κλιμάκωση και χρώματα φόντου.  
- **Διαπλατφορμική** – λειτουργεί σε Windows, Linux και macOS με .NET Core.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Aspose.CAD for .NET** – κατεβάστε το από [εδώ](https://releases.aspose.com/cad/net/).  
- **Visual Studio** ή οποιοδήποτε συμβατό .NET IDE.  
- **Ένα δείγμα αρχείου DGN** – για αυτόν τον οδηγό θα χρησιμοποιήσουμε το `Nikon_D90_Camera.dgn` (περιλαμβάνεται στο πακέτο δειγμάτων Aspose).  

Τώρα που όλα είναι έτοιμα, ας βυθίσουμε στον κώδικα.

## Εισαγωγή χώρων ονομάτων

Στο .NET project σας, εισάγετε τους απαιτούμενους χώρους ονομάτων:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dgn;
using Aspose.CAD.ImageOptions;
```

## Βήμα 1: Ρύθμιση του καταλόγου εγγράφων σας

Δημιουργήστε μια μεταβλητή που δείχνει στο φάκελο όπου θα βρίσκονται το πηγαίο DGN και τα αρχεία εξόδου.

```csharp
string MyDir = "Your Document Directory";
```

## Βήμα 2: Φόρτωση του αρχείου DGN

Φορτώστε το αρχείο DGN ως `DgnImage`. Αυτό το αντικείμενο σας δίνει πρόσβαση στα δεδομένα CAD και στη διαδικασία rasterization.

```csharp
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";
string outFile = MyDir + "Nikon_D90_Camera.dgn";

using (DgnImage dgnImage = (DgnImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Βήμα 3: Διαμόρφωση επιλογών εξαγωγής PDF (Configure CAD Rasterization Options)

Εδώ **διαμορφώνουμε τις επιλογές rasterization CAD** που καθορίζουν πώς το 3‑Δ μοντέλο αποδίδεται σε PDF. Μπορείτε να προσαρμόσετε το μέγεθος σελίδας, να ενεργοποιήσετε την αυτόματη κλιμάκωση διάταξης, να ορίσετε χρώμα φόντου και να επιλέξετε τις ακριβείς διατάξεις (προβολές) που θέλετε να εξάγετε.

```csharp
var options = new PdfOptions
{
    VectorRasterizationOptions = new CadRasterizationOptions
    {
        PageWidth = 1500,
        PageHeight = 1500,
        AutomaticLayoutsScaling = true,
        BackgroundColor = Color.Black,
        Layouts = new string[] { "1", "2", "3", "9" } // Only export specified views
    }
};
```

## Βήμα 4: Αποθήκευση της raster εικόνας

Τέλος, εξάγετε το DGN σε αρχείο PDF χρησιμοποιώντας τις επιλογές που μόλις διαμορφώσατε.

```csharp
dgnImage.Save(outFile, options);
```

## Κοινά προβλήματα και λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Κενό PDF εξόδου** | Επαληθεύστε ότι ο πίνακας `Layouts` περιέχει τα σωστά αναγνωριστικά προβολών που υπάρχουν στο αρχείο DGN. |
| **Λανθασμένα χρώματα** | Βεβαιωθείτε ότι το `BackgroundColor` έχει οριστεί στην επιθυμητή τιμή· χρησιμοποιήστε `Color.White` για ανοιχτό φόντο. |
| **Προβλήματα απόδοσης σε μεγάλα αρχεία** | Ενεργοποιήστε το `AutomaticLayoutsScaling` και εξετάστε τη μείωση των `PageWidth/PageHeight` για μικρότερη ανάλυση raster. |
| **Εξαίρεση άδειας** | Εγκαταστήστε μια έγκυρη άδεια Aspose.CAD πριν φορτώσετε την εικόνα για να αποφύγετε υδατογραφήματα δοκιμής. |

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET με άλλες μορφές αρχείων CAD;**  
Α: Ναι, το Aspose.CAD υποστηρίζει DWG, DXF, DWF, DGN και πολλές άλλες μορφές.

**Ε: Πώς μπορώ να διαχειριστώ εξαιρέσεις όταν εργάζομαι με το Aspose.CAD;**  
Α: Τυλίξτε τον κώδικά σας σε ένα μπλοκ `try‑catch` και εξετάστε το `Aspose.CAD.CADException` για λεπτομερείς πληροφορίες σφάλματος.

**Ε: Είναι το Aspose.CAD κατάλληλο για εμπορικά έργα;**  
Α: Απόλυτα. Μπορείτε να αγοράσετε άδεια [εδώ](https://purchase.aspose.com/buy).

**Ε: Μπορώ να δοκιμάσω το Aspose.CAD για .NET πριν την αγορά;**  
Α: Ναι, διαθέσιμη είναι δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω υποστήριξη κοινότητας για το Aspose.CAD;**  
Α: Συμμετέχετε στο φόρουμ συζήτησης [εδώ](https://forum.aspose.com/c/cad/19).

---

**Τελευταία ενημέρωση:** 2026-03-29  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}