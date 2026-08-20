---
date: 2026-04-06
description: Μάθετε πώς να μετατρέψετε DWF σε JPG σε C# χρησιμοποιώντας το Aspose.CAD
  και ανακαλύψτε πώς να εξάγετε το μέγεθος διάταξης DWF από αρχεία DWG.
keywords:
- convert dwf to jpg
- how to extract dwf
- convert dwg to jpg
linktitle: Εργασία με αρχεία DWG σε C# – Λήψη μεγέθους διάταξης DWF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Μετατροπή DWF σε JPG σε C# – Λήψη μεγέθους διάταξης DWF από DWG
url: /el/net/dwg-file-manipulation/get-size-of-dwf-layout/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DWF σε JPG σε C# – Λήψη Μεγέθους Διάταξης DWF από DWG

## Εισαγωγή

Αν χρειάζεστε **μετατροπή DWF σε JPG** ενώ ταυτόχρονα θέλετε να βρείτε τις ακριβείς διαστάσεις της διάταξης, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε βήμα‑βήμα από ένα πλήρες, end‑to‑end παράδειγμα που χρησιμοποιεί Aspose.CAD for .NET για να ανοίξει ένα αρχείο DWF που προέρχεται από DWG, να διαβάσει το μέγεθος κάθε διάταξης και να αποθηκεύσει τη διάταξη ως εικόνα JPG υψηλής ποιότητας. Στο τέλος θα γνωρίζετε πώς να εξάγετε πληροφορίες διάταξης DWF και θα έχετε ένα επαναχρησιμοποιήσιμο snippet κώδικα που μπορείτε να ενσωματώσετε σε οποιοδήποτε έργο C#.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “convert DWF to JPG”;** Σημαίνει την ραστεροποίηση μιας διανυσματικής διάταξης DWF σε εικόνα bitmap JPEG.  
- **Γιατί να διαβάσω πρώτα το μέγεθος διάταξης;** Η γνώση των ακριβών διαστάσεων σας επιτρέπει να ορίσετε τις σωστές διαστάσεις σελίδας, αποφεύγοντας τεντωμένο ή κομμένο αποτέλεσμα.  
- **Ποια βιβλιοθήκη το διαχειρίζεται;** Το Aspose.CAD for .NET παρέχει πλήρη υποστήριξη για DWG, DWF και μετατροπή σε raster εικόνες.  
- **Χρειάζομαι άδεια;** Μια προσωρινή άδεια λειτουργεί για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι το “convert DWF to JPG” και γιατί είναι σημαντικό;

Η μετατροπή ενός αρχείου DWF (Design Web Format) σε JPG δημιουργεί μια φορητή εικόνα που μπορεί να εμφανιστεί σε προγράμματα περιήγησης, να ενσωματωθεί σε αναφορές ή να μοιραστεί με ενδιαφερόμενους που δεν διαθέτουν λογισμικό CAD. Η μετατροπή σας δίνει επίσης την ευελιξία να επεξεργαστείτε την εικόνα (αλλαγή μεγέθους, συμπίεση, υδατογράφημα) χρησιμοποιώντας τυπικά εργαλεία επεξεργασίας εικόνας.

## Γιατί να εξάγουμε το μέγεθος διάταξης DWF;

Ένα αρχείο DWF μπορεί να περιέχει πολλαπλές διατάξεις, καθεμία με το δικό της σύστημα συντεταγμένων και μονάδες (ίντσες, χιλιοστά κ.λπ.). Η εξαγωγή του μεγέθους διάταξης σας επιτρέπει να:

1. Διατηρήσετε την αρχική αναλογία διαστάσεων κατά τη ραστεροποίηση.  
2. Επιλέξετε το σωστό DPI για έξοδο υψηλής ανάλυσης.  
3. Αυτοματοποιήσετε την επεξεργασία πολλαπλών διατάξεων χωρίς χειροκίνητες ρυθμίσεις.

## Προαπαιτούμενα

Για να ακολουθήσετε αυτό το tutorial απρόσκοπτα, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Aspose.CAD for .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει το Aspose.CAD for .NET. Μπορείτε να το κατεβάσετε από τη [Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/).

Η διαθεσιμότητα της βιβλιοθήκης σημαίνει ότι μπορείτε να εστιάσετε στον κώδικα αντί να ψάχνετε εξαρτήσεις.

## Εισαγωγή Namespaces

Πριν ξεκινήσουμε τον κώδικα, εισάγουμε τους απαιτούμενους namespaces. Αυτοί παρέχουν τις κλάσεις που θα χρειαστούμε για εργασία με αρχεία CAD, επιλογές ραστεροποίησης και I/O αρχείων.

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

## Βήμα 1: Ρύθμιση του Περιβάλλοντός σας

Δημιουργήστε ένα νέο έργο console ή class‑library C#, προσθέστε αναφορά στο **Aspose.CAD.dll**, και βεβαιωθείτε ότι το έργο στοχεύει σε συμβατή έκδοση .NET.

## Βήμα 2: Ορισμός Διαδρομών Αρχείων (πώς να εξάγετε DWF)

Καθορίστε πού βρίσκεται το πηγαίο αρχείο DWF και πού θα γραφτούν τα παραγόμενα αρχεία JPG.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "blocks_and_tables.dwf";
```

> **Pro tip:** Χρησιμοποιήστε `Path.Combine(MyDir, "blocks_and_tables.dwf")` για ασφαλέστερη διαχείριση διαδρομών σε διαφορετικά λειτουργικά συστήματα.

## Βήμα 3: Φόρτωση της Εικόνας DWF

Φορτώστε το αρχείο DWF σε ένα αντικείμενο `Aspose.CAD.Image`. Το μετατρέπουμε σε `DwfImage` επειδή χρειαζόμαστε πρόσβαση σε ιδιότητες συγκεκριμένων σελίδων.

```csharp
using (DwfImage image = (DwfImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Code for further steps will go here
}
```

## Βήμα 4: Επανάληψη μέσω Σελίδων

Ένα DWF μπορεί να περιέχει πολλές σελίδες (διατάξεις). Επανάληψη σε κάθε μία ώστε να τις επεξεργαστούμε ξεχωριστά.

```csharp
foreach (var page in image.Pages)
{
    // Code for further steps will go here
}
```

## Βήμα 5: Λήψη Πληροφοριών Διάταξης

Μέσα στον βρόχο, ανακτήστε το όνομα της διάταξης. Αυτό το όνομα θα χρησιμοποιηθεί τόσο για καταγραφή όσο και για ονομασία του αρχείου εξόδου JPG.

```csharp
var layout = page.Name;
System.Console.WriteLine("Layout= " + layout);
```

## Βήμα 6: Ρύθμιση Επιλογών JPG

Δημιουργήστε μια παρουσία `JpegOptions` και διαμορφώστε τις επιλογές ραστεροποίησης. Η ιδιότητα `Layouts` λέει στο Aspose.CAD ποια διάταξη να αποδώσει.

```csharp
using (FileStream fs = new FileStream(MyDir + "layout_" + layout + ".jpg", FileMode.Create))
{
    JpegOptions jpegOptions = new JpegOptions();
    CadRasterizationOptions options = new CadRasterizationOptions();
    options.Layouts = new string[] { layout };
    // Code for further steps will go here
}
```

## Βήμα 7: Προσδιορισμός Μεγέθους Σελίδας (convert dwg to jpg)

Υπολογίστε το πλάτος και το ύψος της διάταξης στις φυσικές της μονάδες. Αυτές οι πληροφορίες είναι απαραίτητες για τον σωστό ορισμό του μεγέθους raster σελίδας.

```csharp
double sizeExtX = page.MaxPoint.X - page.MinPoint.X;
double sizeExtY = page.MaxPoint.Y - page.MinPoint.Y;
// Code for further steps will go here
```

## Βήμα 8: Ρύθμιση Διαστάσεων Σελίδας

Μετατρέψτε τις φυσικές μονάδες (ίντσες ή χιλιοστά) σε pixel χρησιμοποιώντας τις βοηθητικές μεθόδους του Aspose.CAD. Αν ο τύπος μονάδας δεν είναι κανένας από αυτούς, θα χρησιμοποιήσουμε τις ακατέργαστες τιμές.

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

## Βήμα 9: Αποθήκευση του Αρχείου JPG

Τέλος, συνδέστε τις επιλογές ραστεροποίησης με τις επιλογές JPEG και αποθηκεύστε την εικόνα στο δίσκο.

```csharp
jpegOptions.VectorRasterizationOptions = options;
image.Save(fs, jpegOptions);
}
```

Όταν ολοκληρωθεί ο βρόχος, θα έχετε ένα αρχείο JPG για κάθε διάταξη, το καθένα με ακριβές μέγεθος που ταιριάζει στις αρχικές διαστάσεις του DWF.

## Συχνά Προβλήματα και Λύσεις

| Σύμπτωμα | Πιθανή Αιτία | Διόρθωση |
|---------|--------------|-----|
| Κενό αρχείο JPG | Η ιδιότητα options.Layouts δεν έχει οριστεί σωστά | Επαληθεύστε ότι το όνομα διάταξης ταιριάζει με το page.Name. |
| Παραμορφωμένη εικόνα | Λάθος μετατροπή DPI | Χρησιμοποιήστε CommonHelper.DPI = 300 (ή το επιθυμητό DPI) πριν από τη μετατροπή. |
| Αρχείο δεν βρέθηκε | Λανθασμένη διαδρομή MyDir | Χρησιμοποιήστε απόλυτες διαδρομές ή Path.Combine. |
| Εξαίρεση άδειας | Δεν έχει εφαρμοστεί άδεια | Φορτώστε προσωρινή ή μόνιμη άδεια πριν καλέσετε Image.Load. |

## Συχνές Ερωτήσεις

### Ε1: Είναι το Aspose.CAD συμβατό με τις πιο πρόσφατες μορφές αρχείων DWG;

A1: Το Aspose.CAD υποστηρίζει διάφορες μορφές DWG, συμπεριλαμβανομένων των τελευταίων εκδόσεων. Ανατρέξτε στην [documentation](https://reference.aspose.com/cad/net/) για λεπτομέρειες συμβατότητας.

### Ε2: Μπορώ να χρησιμοποιήσω το Aspose.CAD για εμπορικά και προσωπικά έργα;

A2: Ναι, το Aspose.CAD προσφέρει ευέλικτες επιλογές αδειοδότησης για εμπορική και προσωπική χρήση. Επισκεφθείτε τη [purchase page](https://purchase.aspose.com/buy) για περισσότερες λεπτομέρειες.

### Ε3: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD;

A3: Μπορείτε να λάβετε προσωρινή άδεια από [εδώ](https://purchase.aspose.com/temporary-license/) για σκοπούς αξιολόγησης.

### Ε4: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD;

A4: Για οποιεσδήποτε ερωτήσεις ή βοήθεια, επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Ε5: Υπάρχει δωρεάν δοκιμαστική έκδοση του Aspose.CAD;

A5: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμαστική έκδοση του Aspose.CAD [εδώ](https://releases.aspose.com/).

### Ε6: Πώς μπορώ να μετατρέψω ένα αρχείο DWG απευθείας σε JPG χωρίς να εξάγω πρώτα το DWF;

A6: Μπορείτε να φορτώσετε το αρχείο DWG με `Aspose.CAD.Image.Load` και να χρησιμοποιήσετε την ίδια ροή ραστεροποίησης· απλώς ορίστε `options.Layouts` στα επιθυμητά ονόματα διάταξης από το DWG.

### Ε7: Διατηρεί η μετατροπή την ποιότητα του διανύσματος;

A7: Μόλις ραστεροποιηθεί σε JPG, η εικόνα είναι bitmap‑βασισμένη, οπότε η κλιμακωσιμότητα του διανύσματος χάνεται. Για απώλεια κλιμακωσιμότητας, σκεφτείτε εξαγωγή σε PNG ή SVG.

---

**Τελευταία ενημέρωση:** 2026-04-06  
**Δοκιμάστηκε με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}