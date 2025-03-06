---
title: Εξαγωγή DGN σε Εικόνα Raster στο Aspose.CAD για .NET
linktitle: Εξαγωγή DGN σε Εικόνα Raster
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μετατρέψτε το DGN σε εικόνες ράστερ χωρίς κόπο χρησιμοποιώντας το Aspose.CAD για .NET. Εξερευνήστε τον οδηγό βήμα προς βήμα και απελευθερώστε τη δύναμη του .NET στη διαχείριση αρχείων CAD.
weight: 13
url: /el/net/cad-export-formats/export-dgn-to-raster-image/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DGN σε Εικόνα Raster στο Aspose.CAD για .NET

## Εισαγωγή

Στο δυναμικό πεδίο της ανάπτυξης .NET, το Aspose.CAD αναδεικνύεται ως ένα ισχυρό εργαλείο για το χειρισμό αρχείων σχεδίασης με τη βοήθεια υπολογιστή (CAD). Αυτό το σεμινάριο εξετάζει τη διαδικασία εξαγωγής αρχείων DGN σε εικόνες ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Αν θέλετε να μετατρέψετε τα αρχεία DGN σας σε οπτικά συναρπαστικές εικόνες ράστερ απρόσκοπτα, βρίσκεστε στο σωστό μέρος.

## Προαπαιτούμενα

Πριν ξεκινήσουμε αυτό το ταξίδι, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

-  Aspose.CAD για .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD στο έργο σας .NET. Μπορείτε να βρείτε τη βιβλιοθήκη και τη σχετική τεκμηρίωση στο[δικτυακός τόπος](https://reference.aspose.com/cad/net/).

- Δείγμα αρχείου DGN: Έχετε ένα αρχείο DGN έτοιμο για μετατροπή. Στο παράδειγμά μας, θα χρησιμοποιήσουμε το "Nikon_D90_Camera.dgn."

Τώρα, ας βουτήξουμε στον οδηγό βήμα προς βήμα.

## Εισαγωγή χώρων ονομάτων

Στο έργο σας .NET, ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων για το Aspose.CAD. Αυτό το βήμα σάς επιτρέπει να έχετε πρόσβαση στις κλάσεις και τις μεθόδους που απαιτούνται για τη μετατροπή εικόνας DGN σε ράστερ.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση αρχείου DGN

 Ξεκινήστε φορτώνοντας το αρχείο DGN στο a`CadImage` αντικείμενο. Αυτό παρέχει τη βάση για επόμενες λειτουργίες.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Nikon_D90_Camera.dgn";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Ο κωδικός σας για περαιτέρω επεξεργασία βρίσκεται εδώ
}
```

## Βήμα 2: Ορίστε τις επιλογές ραστεροποίησης

 Δημιουργώ ένα`CadRasterizationOptions` αντικείμενο και ορίστε διάφορες ιδιότητες για να προσαρμόσετε τη διαδικασία ραστεροποίησης σύμφωνα με τις απαιτήσεις σας.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 600;
rasterizationOptions.PageHeight = 300;
rasterizationOptions.NoScaling = true;
rasterizationOptions.AutomaticLayoutsScaling = false;
```

## Βήμα 3: Δημιουργία αντικειμένου JpegOptions

 Επειδή στοχεύουμε να μετατρέψουμε το αρχείο DGN σε JPEG, δημιουργήστε ένα`JpegOptions` αντικείμενο και αντιστοίχιση των προηγουμένως καθορισμένων`CadRasterizationOptions` σε αυτό.

```csharp
ImageOptionsBase options = new JpegOptions();
options.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 4: Αποθηκεύστε την εικόνα Raster

 Χρησιμοποιήστε το`Save` μέθοδος του`CadImage` κλάση για εξαγωγή του αρχείου DGN σε μια εικόνα ράστερ στην επιθυμητή μορφή, σε αυτήν την περίπτωση, ένα JPEG.

```csharp
cadImage.Save(MyDir + "ExportDGNToRasterImage_out.jpg", options);
```

## συμπέρασμα

Συγχαρητήρια! Έχετε πλοηγηθεί με επιτυχία στα βήματα για την εξαγωγή ενός αρχείου DGN σε μια εικόνα ράστερ χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το σεμινάριο σάς έχει εξοπλίσει με τις απαραίτητες γνώσεις για να ενσωματώσετε αυτή τη λειτουργικότητα στα έργα σας .NET χωρίς κόπο.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να εξάγω αρχεία DGN σε μορφές άλλες από JPEG;

A1: Ναι, το Aspose.CAD για .NET υποστηρίζει διάφορες μορφές εξόδου. Μπορείτε να τροποποιήσετε τις επιλογές ανάλογα στο Βήμα 3.

### Ε2 Πώς μπορώ να χειριστώ τις εξαιρέσεις κατά τη διαδικασία μετατροπής;

A2: Βεβαιωθείτε ότι έχετε τον κατάλληλο χειρισμό εξαιρέσεων, όπως φαίνεται στον παρεχόμενο κώδικα, για την αντιμετώπιση πιθανών ζητημάτων.

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.CAD για .NET;

 A3: Ναι, μπορείτε να εξερευνήσετε το προϊόν με μια δωρεάν δοκιμή. Επίσκεψη[εδώ](https://releases.aspose.com/) Για περισσότερες πληροφορίες.

### Ε4: Πού μπορώ να αναζητήσω βοήθεια ή να συζητήσω ζητήματα που σχετίζονται με το Aspose.CAD για .NET;

 A4: Προχωρήστε στο[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για κοινοτική υποστήριξη και συζητήσεις.

### Ε5: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.CAD για .NET;

 Α5: Επίσκεψη[αυτός ο σύνδεσμος](https://purchase.aspose.com/temporary-license/)να αποκτήσετε προσωρινή άδεια για τις αναπτυξιακές σας ανάγκες.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
