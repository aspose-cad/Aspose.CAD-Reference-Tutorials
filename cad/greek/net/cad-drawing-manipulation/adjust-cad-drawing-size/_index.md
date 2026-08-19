---
date: 2026-03-19
description: Μάθετε πώς να αλλάζετε το μέγεθος των σχεδίων CAD στο .NET με το Aspose.CAD,
  συμπεριλαμβανομένου του πώς να κλιμακώνετε τις μονάδες σχεδίασης CAD και να προσαρμόζετε
  το μέγεθος της διάταξης. Ακολουθήστε τον βήμα‑βήμα οδηγό μας.
linktitle: Adjusting CAD Drawing Size
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να αλλάξετε το μέγεθος των σχεδίων CAD με το Aspose.CAD για .NET
url: /el/net/cad-drawing-manipulation/adjust-cad-drawing-size/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Αλλάξετε το Μέγεθος των Σχεδίων CAD με το Aspose.CAD για .NET

## Εισαγωγή

Αν χρειάζεστε **πώς να αλλάξετε το μέγεθος CAD** αρχεία απευθείας από την εφαρμογή .NET, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα σας δείξουμε πώς να αλλάξετε τις ρυθμίσεις μονάδας CAD, να κλιμακώσετε τις διαστάσεις του σχεδίου CAD και να προσαρμόσετε το μέγεθος του CAD προγραμματιστικά χρησιμοποιώντας το Aspose.CAD για .NET. Στο τέλος του οδηγού θα έχετε μια σταθερή, έτοιμη για παραγωγή λύση για την αλλαγή μεγέθους οποιουδήποτε υποστηριζόμενου μορφότυπου CAD.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.CAD for .NET  
- **Μπορώ να αλλάξω τον τύπο μονάδας;** Ναι – set `UnitType` in `CadRasterizationOptions`  
- **Απαιτείται άδεια για παραγωγή;** Απαιτείται έγκυρη άδεια Aspose.CAD για χρήση εκτός δοκιμής  
- **Σε ποιο μορφότυπο εικόνας εξάγει το παράδειγμα;** BMP (αλλά οποιοδήποτε υποστηριζόμενο μορφότυπο raster λειτουργεί)  
- **Πόσες γραμμές κώδικα;** Λιγότερες από 30 γραμμές για μια πλήρη λειτουργία αλλαγής μεγέθους  

## Τι σημαίνει “πώς να αλλάξετε το μέγεθος CAD” στην πράξη;
Η αλλαγή μεγέθους ενός σχεδίου CAD σημαίνει τη μετατροπή των διανυσματικών δεδομένων σε εικόνα raster σε συγκεκριμένη κλίμακα ή μονάδα (π.χ., εκατοστά, ίντσες). Αυτό είναι χρήσιμο όταν χρειάζεται να ενσωματώσετε σχέδια σε αναφορές, να δημιουργήσετε μικρογραφίες ή να ενσωματώσετε οπτικά CAD σε ιστοσελίδες.

## Γιατί να προσαρμόσετε το μέγεθος CAD με το Aspose.CAD;
- **Χωρίς εξωτερικό λογισμικό CAD** – όλα εκτελούνται μέσα στον κώδικα .NET.  
- **Λεπτομερής έλεγχος** πάνω στις μονάδες, διατάξεις και επιλογές rasterization.  
- **Υποστήριξη πολλαπλών μορφότυπων** – ο ίδιος κώδικας λειτουργεί για DWG, DXF, DWF και άλλα.  

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

- Aspose.CAD for .NET Library: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη από τη [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).  
- Δείγμα Σχεδίου CAD: Ένα αρχείο όπως `sample.dwg` τοποθετημένο στον φάκελο εγγράφων του έργου σας.  

## Εισαγωγή Namespaces

Πρώτα, εισάγετε τα namespaces που σας δίνουν πρόσβαση στις κλάσεις του Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση του Σχεδίου CAD

Φορτώστε το αρχείο προέλευσης σε ένα αντικείμενο `Image`. Αυτό το αντικείμενο αντιπροσωπεύει το σχέδιο CAD στη μνήμη και θα είναι η βάση για όλες τις περαιτέρω λειτουργίες.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "sample.dwg";

// Load a CAD drawing in an instance of Image
using (var image = Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code here...
}
```

## Βήμα 2: Δημιουργία BmpOptions (ή οποιουδήποτε άλλου raster μορφότυπου)

`BmpOptions` λέει στο Aspose.CAD πώς να αποδώσει τα διανυσματικά δεδομένα όταν τα αποθηκεύετε ως bitmap. Μπορείτε να το αντικαταστήσετε με `PngOptions`, `JpegOptions` κ.λπ., ανάλογα με τον επιθυμητό μορφότυπο.

```csharp
Aspose.CAD.ImageOptions.BmpOptions bmpOptions = new Aspose.CAD.ImageOptions.BmpOptions();
```

## Βήμα 3: Ορισμός CadRasterizationOptions

`CadRasterizationOptions` περιέχει τις βασικές ρυθμίσεις για κλιμάκωση, μετατροπή μονάδων και επιλογή διάταξης. Η σύνδεσή του με την ιδιότητα `VectorRasterizationOptions` του `BmpOptions` διασφαλίζει ότι ο rasterizer χρησιμοποιεί τις προσαρμοσμένες ρυθμίσεις σας.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions cadRasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
bmpOptions.VectorRasterizationOptions = cadRasterizationOptions;
```

## Βήμα 4: Ορισμός UnitType (αλλαγή μονάδας CAD)

Εδώ αλλάζουμε τη μονάδα CAD από την προεπιλογή σε εκατοστά. Εδώ βρίσκεται η λέξη-κλειδί **change cad unit**, και επηρεάζει άμεσα το τελικό μέγεθος της εικόνας.

```csharp
cadRasterizationOptions.UnitType = Aspose.CAD.ImageOptions.UnitType.Centimeter;
```

## Βήμα 5: Επιλογή Διατάξεων (ορισμός διατάξεων CAD)

Αν το σχέδιό σας περιέχει πολλαπλές διατάξεις (π.χ., Model, Sheet1), καθορίστε ποιες θέλετε να rasterize. Η επιλογή της σωστής διάταξης είναι απαραίτητη όταν **set cad layouts** για ένα αλλαγμένο μέγεθος εξόδου.

```csharp
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Βήμα 6: Εξαγωγή σε BMP (αλλαγή μεγέθους σχεδίου CAD)

Τέλος, αποθηκεύστε την rasterized εικόνα. Το αρχείο εξόδου αντικατοπτρίζει το νέο μέγεθος, τη μονάδα και τη διάταξη που διαμορφώσατε—ολοκληρώνοντας αποτελεσματικά τη λειτουργία **resize CAD drawing**.

```csharp
string outPath = sourceFilePath + ".bmp";
image.Save(outPath, bmpOptions);
```

Τώρα έχετε ένα αρχείο BMP που αντιπροσωπεύει το αλλαγμένο μέγεθος του σχεδίου CAD, έτοιμο για περαιτέρω επεξεργασία ή εμφάνιση.

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Διόρθωση |
|----------|----------------|----------|
| Η έξοδος είναι θολή | Προεπιλεγμένο χαμηλό DPI (dots per inch) | Ορίστε `cadRasterizationOptions.Resolution = 300;` πριν από την αποθήκευση |
| Εμφανίζεται λανθασμένη διάταξη | Λάθος όνομα διάταξης | Επαληθεύστε το ακριβές όνομα διάταξης χρησιμοποιώντας έναν προβολέα CAD ή τη συλλογή `Layouts` |
| Η μετατροπή μονάδας φαίνεται λανθασμένη | Ανάμειξη μετρικών και αυτοκρατορικών μονάδων | Βεβαιωθείτε ότι το `UnitType` ταιριάζει με το επιθυμητό σύστημα μέτρησης |

## Συχνές Ερωτήσεις

### Q1: Είναι το Aspose.CAD για .NET συμβατό με όλα τα μορφότυπα CAD;
A1: Το Aspose.CAD για .NET υποστηρίζει μια ευρεία γκάμα μορφότυπων CAD, συμπεριλαμβανομένων των DWG, DXF, DWF και άλλων. Ελέγξτε την [documentation](https://reference.aspose.com/cad/net/) για την πλήρη λίστα.

### Q2: Μπορώ να αλλάξω το μέγεθος πολλαπλών διατάξεων ταυτόχρονα;
A2: Ναι, μπορείτε να αλλάξετε το μέγεθος πολλαπλών διατάξεων προσαρμόζοντας τον πίνακα `Layouts` στο `CadRasterizationOptions`.

### Q3: Πού μπορώ να λάβω υποστήριξη για το Aspose.CAD για .NET;
A3: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη κοινότητας και βοήθεια.

### Q4: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
A4: Ναι, μπορείτε να δοκιμάσετε μια [free trial](https://releases.aspose.com/) για να αξιολογήσετε τις δυνατότητες του Aspose.CAD για .NET.

### Q5: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD για .NET;
A5: Αποκτήστε μια προσωρινή άδεια για δοκιμαστικούς σκοπούς [here](https://purchase.aspose.com/temporary-license/).

## Συχνές Ερωτήσεις

**Q: Πώς κλιμακώνω ένα σχέδιο CAD χωρίς να αλλάξω τον τύπο μονάδας;**  
A: Προσαρμόστε την ιδιότητα `Zoom` του `CadRasterizationOptions` (π.χ., `cadRasterizationOptions.Zoom = 2.0;`) για να διπλασιάσετε το μέγεθος διατηρώντας την αρχική μονάδα.

**Q: Μπορώ να εξάγω σε μορφότυπους διαφορετικούς από BMP;**  
A: Απόλυτα. Αντικαταστήστε το `BmpOptions` με `PngOptions`, `JpegOptions`, ή οποιαδήποτε άλλη υποστηριζόμενη κλάση raster μορφότυπου.

**Q: Είναι δυνατόν να επεξεργαστείτε μαζικά έναν φάκελο σχεδίων;**  
A: Ναι. Επανάληψη μέσω των αρχείων σε έναν κατάλογο, εφαρμογή της ίδιας λογικής rasterization, και αποθήκευση κάθε εξόδου με μοναδικό όνομα.

---

**Τελευταία ενημέρωση:** 2026-03-19  
**Δοκιμή με:** Aspose.CAD for .NET 24.11 (latest at time of writing)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}