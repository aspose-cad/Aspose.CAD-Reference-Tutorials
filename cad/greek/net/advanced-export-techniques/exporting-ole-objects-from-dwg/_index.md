---
description: Μάθετε πώς να μετατρέπετε DWG σε PNG και να εξάγετε αντικείμενα OLE από
  αρχεία DWG χρησιμοποιώντας το Aspose.CAD για .NET – ένας γρήγορος, προσανατολισμένος
  στον κώδικα οδηγός.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Μετατροπή DWG σε PNG & Εξαγωγή αντικειμένων OLE - Εκπαίδευση Aspose.CAD
url: /el/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή αντικειμένων OLE από αρχεία DWG - Aspose.CAD Tutorial

## Εισαγωγή

Αν χρειάζεστε να **convert DWG to PNG** ενώ εξάγετε ενσωματωμένα αντικείμενα OLE, βρίσκεστε στο σωστό μέρος. Το Aspose.CAD for .NET καθιστά αυτή τη διαδικασία δύο βημάτων απλή, επιτρέποντάς σας να αυτοματοποιήσετε την εξαγωγή και τη ραστεροποίηση με λίγες γραμμές C#. Στα επόμενα λεπτά θα περάσουμε από όλη τη ροή εργασίας, από τη ρύθμιση του περιβάλλοντος μέχρι την αποθήκευση κάθε DWG ως PNG που περιέχει τα εξαγόμενα δεδομένα OLE.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Μετατροπή DWG σε PNG και εξαγωγή αντικειμένων OLE χρησιμοποιώντας το Aspose.CAD for .NET.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Μπορώ να επεξεργαστώ πολλαπλά αρχεία DWG ταυτόχρονα;** Ναι – το παράδειγμα διασχίζει έναν πίνακα ονομάτων αρχείων.  
- **Πού μπορώ να βρω περισσότερα παραδείγματα;** Δείτε την επίσημη τεκμηρίωση του Aspose.CAD και τους συνδέσμους του φόρουμ παρακάτω.

## Τι είναι **convert DWG to PNG**;
Η μετατροπή ενός DWG (σχέδιο AutoCAD) σε εικόνα PNG ραστεροποιεί τα διανυσματικά δεδομένα, καθιστώντας τα εύκολα στην προβολή ή την ενσωμάτωση σε ιστοσελίδες, αναφορές ή άλλες εφαρμογές που δεν υποστηρίζουν εγγενώς DWG. Όταν υπάρχουν αντικείμενα OLE, μπορούν να εξαχθούν και να αποθηκευτούν ως ξεχωριστά περιουσιακά στοιχεία κατά τη μετατροπή.

## Γιατί να εξάγετε αντικείμενα OLE από αρχεία CAD;
Πολλά σχέδια DWG ενσωματώνουν υπολογιστικά φύλλα, γραφήματα ή άλλα έγγραφα Office ως αντικείμενα OLE. Η εξαγωγή τους σας επιτρέπει να επαναχρησιμοποιήσετε τα αρχικά δεδομένα, να αυτοματοποιήσετε τις αναφορές ή να μεταφέρετε το περιεχόμενο σε νεότερες μορφές χωρίς να χάσετε τις ενσωματωμένες πληροφορίες.

## Προαπαιτούμενα

- Aspose.CAD for .NET Library: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη. Μπορείτε να τη κατεβάσετε από τη [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Document Directory: Δημιουργήστε έναν φάκελο όπου αποθηκεύονται τα αρχεία DWG σας. Αντικαταστήστε το `"Your Document Directory"` στο παρεχόμενο απόσπασμα κώδικα με την πραγματική διαδρομή.

## Εισαγωγή Namespaces

Στο .NET project σας, εισάγετε τα απαιτούμενα namespaces:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Ορίστε το Document Directory

```csharp
string MyDir = "Your Document Directory";
```

Αντικαταστήστε το `"Your Document Directory"` με τη διαδρομή όπου βρίσκονται τα αρχεία DWG σας.

### Βήμα 2: Καταγράψτε τα αρχεία DWG που θέλετε να επεξεργαστείτε

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Βήμα 3: Διαμορφώστε τις επιλογές εξαγωγής για τη μετατροπή PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Μπορείτε να προσαρμόσετε το `CadRasterizationOptions` (π.χ., `PageWidth`, `PageHeight`, `BackgroundColor`) ώστε να ταιριάζει με την επιθυμητή ανάλυση εξόδου.

### Βήμα 4: Επανάληψη σε κάθε DWG και εκτέλεση της μετατροπής

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Κατά τη διάρκεια αυτής της επανάληψης η βιβλιοθήκη αυτόματα **extracts OLE objects** ενσωματωμένα σε κάθε σχέδιο και τα περιλαμβάνει στο παραγόμενο PNG. Εάν χρειάζεστε τα ακατέργαστα ρεύματα OLE, μπορείτε να προσπελάσετε τη συλλογή `cadImage.OleObjects` – ένας βολικός τρόπος για **how to extract ole** δεδομένα προγραμματιστικά.

## Κοινά Προβλήματα & Αντιμετώπιση

- **Missing layout name** – Βεβαιωθείτε ότι η διάταξη που καθορίζετε (`"Layout1"` στο παράδειγμα) υπάρχει στο πηγαίο DWG· διαφορετικά ο ραστεροποιητής επιστρέφει στον προεπιλεγμένο χώρο μοντέλου.  
- **Large files cause memory pressure** – Επεξεργαστείτε τα αρχεία ένα προς ένα (όπως φαίνεται) και απελευθερώστε άμεσα τα αντικείμενα `CadImage` με `using`.  
- **Unexpected colors** – Ορίστε το `rasterizationOptions.BackgroundColor` ώστε να ταιριάζει με το φόντο του σχεδίου αν απαιτείται διαφάνεια.

## Συχνές Ερωτήσεις

### Q1: Είναι το Aspose.CAD for .NET κατάλληλο τόσο για αρχάριους όσο και για προχωρημένα αρχεία CAD;
A1: Ναι, το Aspose.CAD for .NET είναι ευέλικτο και μπορεί να διαχειριστεί μια ευρεία γκάμα αρχείων CAD, συμπεριλαμβανομένων τόσο των αρχαρίων όσο και των προχωρημένων παραλλαγών.

### Q2: Μπορώ να προσαρμόσω τις επιλογές εξαγωγής για διαφορετικές διατάξεις;
A2: Απόλυτα! Όπως φαίνεται στο tutorial, μπορείτε να προσαρμόσετε τις επιλογές εξαγωγής, συμπεριλαμβανομένων των διατάξεων, ώστε να ταιριάζουν στις συγκεκριμένες ανάγκες σας.

### Q3: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD for .NET;
A3: Εξερευνήστε την [Aspose.CAD for .NET documentation](https://reference.aspose.com/cad/net/) για λεπτομερείς πληροφορίες και παραδείγματα.

### Q4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
A4: Ναι, μπορείτε να δοκιμάσετε τις δυνατότητες του Aspose.CAD for .NET με μια δωρεάν δοκιμή. Επισκεφθείτε [this link](https://releases.aspose.com/) για να ξεκινήσετε.

### Q5: Πώς μπορώ να λάβω υποστήριξη ή να συνδεθώ με την κοινότητα;
A5: Για υποστήριξη και συμμετοχή στην κοινότητα, επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Q6: Πώς μπορώ να **extract OLE from CAD** αρχεία χωρίς μετατροπή σε PNG;
A6: Χρησιμοποιήστε τη συλλογή `CadImage.OleObjects` μετά τη φόρτωση του DWG· μπορείτε να επαναλάβετε κάθε `OleObject` και να αποθηκεύσετε τα ακατέργαστα δεδομένα του σε αρχείο.

## Συμπέρασμα

Τώρα έχετε δει πώς να **convert DWG to PNG** ενώ εξάγετε αβίαστα **OLE objects** χρησιμοποιώντας το Aspose.CAD for .NET. Αυτή η προσέγγιση εξοικονομεί χρόνο, αφαιρεί τα χειροκίνητα βήματα αντιγραφής‑επικόλλησης και ενσωματώνεται ομαλά σε αυτοματοποιημένες γραμμές εργασίας. Μη διστάσετε να πειραματιστείτε με άλλες μορφές ραστεροποίησης (JPEG, BMP) ή να εξερευνήσετε το πλούσιο σύνολο λειτουργιών επεξεργασίας CAD που προσφέρει το Aspose.

---

**Τελευταία ενημέρωση:** 2026-03-13  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}