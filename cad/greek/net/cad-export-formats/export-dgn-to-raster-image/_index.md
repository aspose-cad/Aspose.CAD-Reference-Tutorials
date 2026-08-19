---
date: 2026-03-24
description: Μάθετε πώς να μετατρέπετε dgn σε png και να αποθηκεύετε cad ως jpeg χρησιμοποιώντας
  το Aspose.CAD για .NET – ένας γρήγορος οδηγός για τη μετατροπή CAD σε εικόνα.
linktitle: Export DGN to Raster Image
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να μετατρέψετε DGN σε PNG στο Aspose.CAD για .NET
url: /el/net/cad-export-formats/export-dgn-to-raster-image/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DGN σε PNG στο Aspose.CAD για .NET

Στη σύγχρονη ανάπτυξη .NET, η **μετατροπή dgn σε png** είναι μια συχνή απαίτηση όταν χρειάζεται να εμφανίσετε CAD σχέδια στο web ή να τα ενσωματώσετε σε αναφορές. Το Aspose.CAD για .NET κάνει αυτή τη μετατροπή απλή, επιτρέποντάς σας να μετατρέψετε ένα αρχείο DGN σε εικόνα raster υψηλής ποιότητας με λίγες μόνο γραμμές κώδικα. Σε αυτόν τον οδηγό θα περάσουμε από όλη τη διαδικασία, από τη ρύθμιση του έργου μέχρι την αποθήκευση του τελικού αρχείου PNG (ή JPEG).

## Γρήγορες Απαντήσεις
- **Μπορώ να μετατρέψω DGN σε PNG με το Aspose.CAD;** Ναι – απλώς ρυθμίστε τις επιλογές rasterization και επιλέξτε έξοδο PNG ή JPEG.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Απαιτείται έγκυρη άδεια Aspose.CAD για μη‑δοκιμαστικές εγκαταστάσεις.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.  
- **Ποιες μορφές εικόνας είναι διαθέσιμες;** PNG, JPEG, BMP, GIF, TIFF και άλλες.  
- **Είναι απαραίτητος ο χειρισμός εξαιρέσεων;** Απόλυτα – τυλίξτε τη μετατροπή σε try/catch για να διαχειριστείτε προβλήματα πρόσβασης αρχείων.

## Τι είναι η “μετατροπή dgn σε png”;
Η μετατροπή ενός αρχείου DGN (MicroStation) σε PNG σημαίνει rasterization των διανυσματικών δεδομένων CAD σε εικόνα βασισμένη σε pixel. Αυτό είναι χρήσιμο για δημιουργία προεπισκοπήσεων, ενσωμάτωση σχεδίων σε HTML email ή δημιουργία μικρογραφιών για συστήματα διαχείρισης εγγράφων.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για μετατροπή CAD σε εικόνα;
- **Χωρίς εξωτερικές εξαρτήσεις** – λειτουργεί αποκλειστικά σε managed code.  
- **Υψηλή πιστότητα** – διατηρεί τα βάρη γραμμών, τα στρώματα και τα χρώματα.  
- **Ευέλικτη έξοδος** – αλλάξτε μεταξύ PNG, JPEG, BMP κ.λπ., με μια μόνο ρύθμιση.  
- **Βελτιστοποιημένη απόδοση** – η rasterization είναι γρήγορη ακόμη και για μεγάλα σχέδια.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Aspose.CAD για .NET** εγκατεστημένο στο έργο σας. Μπορείτε να το κατεβάσετε από την [ιστοσελίδα](https://reference.aspose.com/cad/net/).  
- Ένα δείγμα αρχείου DGN (π.χ. `Nikon_D90_Camera.dgn`) τοποθετημένο σε γνωστό φάκελο.

## Εισαγωγή Namespaces

Ξεκινήστε προσθέτοντας τις απαιτούμενες δηλώσεις `using` ώστε να έχετε πρόσβαση στις κλάσεις του Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση του Αρχείου DGN

Φορτώστε το πηγαίο DGN σε ένα αντικείμενο `CadImage`. Αυτό το αντικείμενο αντιπροσωπεύει το CAD σχέδιο στη μνήμη και θα είναι η πηγή για τη rasterization.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for further processing goes here
}
```

## Βήμα 2: Ορισμός Ρυθμίσεων Rasterization

Ρυθμίστε πώς θα rasterize το CAD σχέδιο. Εδώ μπορείτε να ελέγξετε το μέγεθος εικόνας, την κλίμακα και το χρώμα φόντου.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Βήμα 3: Επιλογή Μορφής Εξόδου (PNG ή JPEG)

Αν και το tutorial εστιάζει στο PNG, μπορείτε επίσης να **αποθηκεύσετε cad ως jpeg**. Δημιουργήστε το κατάλληλο αντικείμενο επιλογών εικόνας και συνδέστε τις ρυθμίσεις rasterization.

```csharp
ImageOptionsBase options = new JpegOptions();   // Change to PngOptions() for PNG output
options.VectorRasterizationOptions = rasterizationOptions;
```

> **Συμβουλή επαγγελματία:** Για να δημιουργήσετε αρχείο PNG, αντικαταστήστε το `new JpegOptions()` με `new PngOptions()`.

## Βήμα 4: Αποθήκευση της Raster Εικόνας

Τέλος, καλέστε τη μέθοδο `Save` στο αντικείμενο `CadImage`, παρέχοντας το επιθυμητό όνομα αρχείου και το αντικείμενο επιλογών που διαμορφώσατε.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

Αν χρησιμοποιήσατε `PngOptions`, το αρχείο θα αποθηκευτεί ως `ExportDGNToRasterImage_out.png`.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **Κενή εικόνα εξόδου** | `NoScaling` ορίστηκε λανθασμένα ή δεν επιλέχθηκε layout | Ορίστε `AutomaticLayoutsScaling = true` ή καθορίστε το επιθυμητό layout. |
| **Έλλειψη μνήμης για μεγάλα αρχεία** | Φόρτωση τεράστιου DGN χωρίς streaming | Χρησιμοποιήστε `Image.Load(sourceFilePath, new LoadOptions { LoadOnDemand = true })`. |
| **Μη υποστηριζόμενη έκδοση DGN** | Παλαιότερες εκδόσεις MicroStation | Βεβαιωθείτε ότι έχετε την πιο πρόσφατη έκδοση του Aspose.CAD που υποστηρίζει παλαιά φορμά. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να εξάγω αρχεία DGN σε μορφές εκτός του JPEG;**  
Α: Ναι, το Aspose.CAD για .NET υποστηρίζει PNG, BMP, GIF, TIFF και άλλες – απλώς αλλάξτε την κλάση επιλογών (π.χ. `new PngOptions()`).

**Ε: Πώς πρέπει να διαχειρίζομαι εξαιρέσεις κατά τη μετατροπή;**  
Α: Τυλίξτε τον κώδικα μετατροπής σε μπλοκ `try/catch` και καταγράψτε το `Aspose.CAD.CadException` για λεπτομερείς πληροφορίες σφάλματος.

**Ε: Υπάρχει διαθέσιμη δοκιμαστική έκδοση του Aspose.CAD για .NET;**  
Α: Ναι, μπορείτε να δοκιμάσετε το προϊόν με δωρεάν δοκιμή. Επισκεφθείτε [εδώ](https://releases.aspose.com/) για περισσότερες πληροφορίες.

**Ε: Πού μπορώ να ζητήσω βοήθεια ή να συζητήσω προβλήματα σχετικά με το Aspose.CAD για .NET;**  
Α: Μεταβείτε στο [φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα και συζητήσεις.

**Ε: Πώς αποκτώ προσωρινή άδεια για το Aspose.CAD για .NET;**  
Α: Επισκεφθείτε [αυτόν τον σύνδεσμο](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε προσωρινή άδεια για τις ανάγκες ανάπτυξής σας.

## Συμπέρασμα

Τώρα έχετε μάθει πώς να **μετατρέψετε dgn σε png** (ή JPEG) χρησιμοποιώντας το Aspose.CAD για .NET. Με την προσαρμογή των ρυθμίσεων rasterization και την αλλαγή της κλάσης επιλογών εικόνας, μπορείτε να προσαρμόσετε την έξοδο ώστε να ταιριάζει σε οποιαδήποτε απαίτηση του έργου σας. Μη διστάσετε να πειραματιστείτε με διαφορετικά μεγέθη σελίδας, ρυθμίσεις DPI και μορφές αρχείων για να αποκτήσετε την τέλεια raster εικόνα για την εφαρμογή σας.

---

**Τελευταία ενημέρωση:** 2026-03-24  
**Δοκιμή με:** Aspose.CAD 24.11 για .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}