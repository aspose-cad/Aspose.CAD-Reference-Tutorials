---
date: 2026-03-29
description: Μάθετε πώς να δημιουργείτε PDF από CAD, να ορίζετε το μέγεθος του καμβά
  και να εξάγετε CAD σε PDF ή TIFF χρησιμοποιώντας το Aspose.CAD για .NET σε αυτόν
  τον οδηγό βήμα‑βήμα.
linktitle: Setting Canvas Size and Mode
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: 'Πώς να δημιουργήσετε PDF από CAD: Ορίστε το μέγεθος και τη λειτουργία του
  καμβά στο Aspose.CAD για .NET'
url: /el/net/cad-features-and-support/setting-canvas-size-and-mode/
weight: 16
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ορισμός Μεγέθους Καμβά και Λειτουργίας στο Aspose.CAD για .NET

## Εισαγωγή

Έτοιμοι να **δημιουργήσετε PDF από CAD** αρχεία ενώ ελέγχετε τις διαστάσεις εξόδου; Σε αυτό το σεμινάριο θα περάσουμε από τον ορισμό του μεγέθους και της λειτουργίας του καμβά, τη φόρτωση ενός αρχείου CAD και την εξαγωγή του σε PDF ή TIFF με το Aspose.CAD για .NET. Είτε χρειάζεστε **μετατροπή DXF σε PDF**, δημιουργία υψηλής ανάλυσης σχεδίων, είτε απλώς να προσαρμόσετε την περιοχή rasterization, τα παρακάτω βήματα θα σας προσφέρουν μια σταθερή, έτοιμη για παραγωγή λύση.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει «δημιουργία PDF από CAD»;** Μετατροπή ενός σχεδίου CAD (π.χ., DXF, DWG) σε έγγραφο PDF που διατηρεί τα διανυσματικά και raster στοιχεία.  
- **Ποια επιλογή ελέγχει το μέγεθος εξόδου;** `CadRasterizationOptions.PageWidth` και `PageHeight` (μέγεθος καμβά).  
- **Μπορώ επίσης να εξάγω σε TIFF;** Ναι – χρησιμοποιήστε `TiffOptions` με τις ίδιες ρυθμίσεις rasterization.  
- **Χρειάζομαι άδεια για παραγωγή;** Απαιτείται εμπορική άδεια· διατίθεται δωρεάν δοκιμή.  
- **Υποστηριζόμενες εκδόσεις .NET;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Τι σημαίνει «δημιουργία PDF από CAD»;
Η δημιουργία PDF από CAD σημαίνει την απόδοση του σχεδίου CAD σε μορφή προσανατολισμένης σε σελίδα (PDF) που μπορεί να προβληθεί, εκτυπωθεί ή μοιραστεί χωρίς την ανάγκη λογισμικού CAD. Το Aspose.CAD αναλαμβάνει το δύσκολο κομμάτι, επιτρέποντάς σας να ορίσετε το μέγεθος του καμβά, την κλιμάκωση και τη μορφή εξόδου.

## Γιατί να ορίσετε το μέγεθος του καμβά κατά τη δημιουργία PDF από CAD;
Ο ορισμός του μεγέθους του καμβά σας δίνει ακριβή έλεγχο επί της ανάλυσης και των διαστάσεων του παραγόμενου PDF ή TIFF. Αυτό είναι ιδιαίτερα χρήσιμο όταν:
- Προετοιμάζετε σχέδια για εκτύπωση σε συγκεκριμένα μεγέθη χαρτιού.  
- Δημιουργείτε μικρογραφίες ή εικόνες υψηλής ανάλυσης για προεπισκόπηση στο web.  
- Διασφαλίζετε συνεπή διάταξη σε πολλά έγγραφα.

## Προαπαιτούμενα

- Βιβλιοθήκη Aspose.CAD: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD από την [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Περιβάλλον Ανάπτυξης: Βεβαιωθείτε ότι έχετε ένα .NET περιβάλλον ανάπτυξης εγκατεστημένο στον υπολογιστή σας.
- Δείγμα αρχείου CAD: Για αυτό το σεμινάριο, θα χρησιμοποιήσουμε ένα δείγμα αρχείου DXF. Μπορείτε να βρείτε ένα στην [Aspose.CAD documentation](https://reference.aspose.com/cad/net/).

## Εισαγωγή Χώρων Ονομάτων

Πρώτα, εισάγετε τους χώρους ονομάτων που απαιτούνται για την επεξεργασία CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Πώς να δημιουργήσετε PDF από CAD με προσαρμοσμένο μέγεθος καμβά

### Βήμα 1: Φόρτωση αρχείου CAD

Ξεκινάμε με **φόρτωση του αρχείου CAD** (π.χ., ένα DXF) σε ένα αντικείμενο `Image`. Αυτό είναι το σημείο όπου **φορτώνετε το αρχείο CAD** στη μνήμη.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps will go here
}
```

### Βήμα 2: Δημιουργία CadRasterizationOptions

Δημιουργήστε μια παρουσία `CadRasterizationOptions` και ορίστε το μέγεθος του καμβά. Οι ιδιότητες `PageWidth` και `PageHeight` σας επιτρέπουν να **ορίσετε το μέγεθος του καμβά** στις ακριβείς διαστάσεις που χρειάζεστε.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
rasterizationOptions.NoScaling = false;
```

### Βήμα 3: Δημιουργία PdfOptions (Εξαγωγή CAD σε PDF)

Συνδέστε τις ρυθμίσεις rasterization με ένα αντικείμενο `PdfOptions`. Αυτή η διαμόρφωση σας επιτρέπει να **εξάγετε CAD σε PDF** με τον προσαρμοσμένο καμβά που ορίσατε.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Βήμα 4: Εξαγωγή σε PDF (Μετατροπή DXF σε PDF)

Τώρα αποθηκεύστε την εικόνα ως PDF. Αυτό το βήμα **δημιουργεί PDF από CAD** χρησιμοποιώντας τις επιλογές που ορίσαμε.

```csharp
image.Save(MyDir + "result_out.pdf", pdfOptions);
```

### Βήμα 5: Δημιουργία TiffOptions (Εξαγωγή CAD σε TIFF)

Αν χρειάζεστε επίσης μια raster εικόνα, διαμορφώστε το `TiffOptions`. Οι ίδιες ρυθμίσεις rasterization επαναχρησιμοποιούνται, έτσι η **εξαγωγή CAD σε TIFF** σέβεται το μέγεθος του καμβά.

```csharp
TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);
tiffOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Βήμα 6: Εξαγωγή σε TIFF

Τέλος, αποθηκεύστε το σχέδιο ως αρχείο TIFF.

```csharp
image.Save(MyDir + "result_out.tiff", tiffOptions);
```

## Κοινά Προβλήματα και Λύσεις

- **Ο καμβάς φαίνεται περικομμένος** – Επαληθεύστε ότι το `AutomaticLayoutsScaling` είναι ορισμένο σε `true` και το `NoScaling` σε `false` ώστε το σχέδιο να κλιμακώνεται ώστε να ταιριάζει στον καμβά.  
- **PDF χαμηλής ανάλυσης** – Αυξήστε τα `PageWidth`/`PageHeight` ή ορίστε το `Resolution` στο `CadRasterizationOptions`.  
- **Σφάλμα αρχείου δεν βρέθηκε** – Βεβαιωθείτε ότι το `MyDir` δείχνει σε έγκυρο φάκελο και ότι το όνομα του αρχείου DXF ταιριάζει ακριβώς.

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλες βιβλιοθήκες .NET;
A1: Ναι, το Aspose.CAD ενσωματώνεται άψογα με άλλες βιβλιοθήκες .NET, παρέχοντας βελτιωμένες δυνατότητες για τη διαχείριση CAD.

### Ε2: Υπάρχει δωρεάν δοκιμή για το Aspose.CAD;
A2: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD με δωρεάν δοκιμή. Επισκεφθείτε [εδώ](https://releases.aspose.com/) για να ξεκινήσετε.

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;
A3: Για υποστήριξη και συζητήσεις, επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19).

### Ε4: Πού μπορώ να βρω ολοκληρωμένη τεκμηρίωση για το Aspose.CAD;
A4: Ανατρέξτε στην [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) για λεπτομερείς πληροφορίες και παραδείγματα.

### Ε5: Πώς μπορώ να αγοράσω το Aspose.CAD για .NET;
A5: Για να αγοράσετε το Aspose.CAD, επισκεφθείτε τη [purchase page](https://purchase.aspose.com/buy).

**Πρόσθετες Ε&Α**

**Ε: Μπορώ να εξάγω ένα πολυσελίδες σχέδιο CAD σε ένα ενιαίο PDF;**  
Α: Ναι. Ορίστε το `PageCount` στο `CadRasterizationOptions` και η βιβλιοθήκη θα συνενώσει τις σελίδες σε ένα PDF.

**Ε: Επηρεάζει το μέγεθος του καμβά την ποιότητα των διανυσματικών δεδομένων;**  
Α: Τα διανυσματικά δεδομένα παραμένουν ανεξάρτητα από την ανάλυση· το μέγεθος του καμβά επηρεάζει μόνο τα raster στοιχεία και την ανάλυση της εικόνας.

**Τελευταία ενημέρωση:** 2026-03-29  
**Δοκιμάστηκε με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}