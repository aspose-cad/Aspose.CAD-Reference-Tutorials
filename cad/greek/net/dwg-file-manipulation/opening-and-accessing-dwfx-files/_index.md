---
date: 2026-04-09
description: Μάθετε πώς να φορτώνετε αρχείο DWFX σε C# και να μετατρέπετε CAD σε PDF
  χρησιμοποιώντας το Aspose.CAD για .NET. Οδηγός βήμα‑προς‑βήμα για αδιάλειπτη ενσωμάτωση.
keywords:
- load dwfx file c#
- c# convert cad to pdf
- aspose.cad dwfx
linktitle: Άνοιγμα και πρόσβαση σε αρχεία DWFX σε C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να φορτώσετε αρχείο DWFX σε C# με οδηγό Aspose.CAD
url: /el/net/dwg-file-manipulation/opening-and-accessing-dwfx-files/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να φορτώσετε αρχείο DWFX σε C# με τον οδηγό Aspose.CAD

## Εισαγωγή

Αν χρειάζεστε να **φορτώσετε αρχείο DWFX C#** και να το μετατρέψετε σε PDF, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε βήμα προς βήμα τις ακριβείς διαδικασίες που απαιτούνται για το άνοιγμα ενός σχεδίου DWFX με το Aspose.CAD for .NET, τη ρύθμιση της rasterization, και τελικά **c# convert CAD to PDF**. Είτε δημιουργείτε μια εφαρμογή επιφάνειας εργασίας είτε μια web υπηρεσία, η προσέγγιση παραμένει η ίδια και λειτουργεί με οποιαδήποτε έκδοση .NET υποστηρίζεται από το Aspose.CAD.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρειάζομαι;** Aspose.CAD for .NET  
- **Μπορώ να μετατρέψω DWFX σε PDF;** Yes – just configure `CadRasterizationOptions` and use `PdfOptions`.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Χρειάζομαι άδεια για δοκιμές;** A free trial works for development; a permanent license is required for production.  
- **Πόσο χρόνο χρειάζεται ο κώδικας για να εκτελεστεί;** Loading and converting a typical DWFX file finishes in under a second on a modern CPU.

## Τι είναι το αρχείο DWFX;

Το DWFX (Design Web Format XPS) είναι μια αναπαράσταση βασισμένη σε XML ενός σχεδίου CAD που μπορεί να αποτυπωθεί σε προγράμματα περιήγησης και άλλους προβολείς. Επειδή αποθηκεύει διανυσματικά δεδομένα, είναι ιδανικό για μετατροπή σε PDF υψηλής ποιότητας χωρίς απώλεια λεπτομερειών.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για τη φόρτωση αρχείων DWFX σε C#;

* **Πλήρης υποστήριξη μορφής** – Aspose.CAD understands DWFX along with dozens of other CAD formats.  
* **Καμία εξωτερική εξάρτηση** – Pure .NET, no need for AutoCAD or other native components.  
* **Εύκολη μετατροπή raster‑σε‑vector** – Switch between raster images and vector PDFs with a few lines of code.  

## Προαπαιτούμενα

Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε:

1. **Aspose.CAD for .NET** installed. You can download it [here](https://releases.aspose.com/cad/net/).  
2. Ένας φάκελος που περιέχει τα αρχεία DWFX που θέλετε να επεξεργαστείτε. Σημειώστε τη πλήρη διαδρομή τόσο για την πηγή όσο και για τις τοποθεσίες εξόδου.

## Πώς να φορτώσετε αρχείο DWFX σε C#

Ακολουθεί ο οδηγός βήμα‑βήμα. Κάθε βήμα συνοδεύεται από μια σύντομη εξήγηση, ακολουθούμενη από το ακριβές μπλοκ κώδικα που πρέπει να αντιγράψετε.

### Εισαγωγή Ονομάτων Χώρων

```csharp
using Aspose.CAD.ImageOptions;
using System;
```

Αυτά τα ονόματα χώρων σας δίνουν πρόσβαση στην κλάση `Image` για τη φόρτωση αρχείων CAD και τις επιλογές που χρειάζονται για rasterization και έξοδο PDF.

### Βήμα 1: Ρύθμιση Καταλόγων Πηγής και Εξόδου

```csharp
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";
```

Αντικαταστήστε το `"Your Document Directory"` με τη διαδρομή όπου βρίσκεται το αρχείο DWFX σας και όπου θέλετε να αποθηκευτεί το PDF.

### Βήμα 2: Φόρτωση Αρχείου DWFX

```csharp
using (Image cadDrawing = Image.Load(SourceDir + "Tyrannosaurus.dwfx"))
```

`Image.Load` διαβάζει το αρχείο DWFX σε ένα αντικείμενο `Image` με το οποίο μπορεί να εργαστεί το Aspose.CAD. Αλλάξτε το `"Tyrannosaurus.dwfx"` με το όνομα του δικού σας σχεδίου.

### Βήμα 3: Ρύθμιση Επιλογών Rasterization

```csharp
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

Οι επιλογές rasterization λένε στο Aspose.CAD πόσο μεγάλη πρέπει να είναι η τελική σελίδα. Η χρήση των αρχικών διαστάσεων του σχεδίου διατηρεί την ακριβή κλίμακα.

### Βήμα 4: Αποθήκευση ως PDF (c# convert CAD to PDF)

```csharp
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
cadDrawing.Save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

Εδώ **c# convert CAD to PDF** προσθέτοντας τις ρυθμίσεις rasterization σε ένα αντικείμενο `PdfOptions` και καλώντας το `Save`. Το αρχείο εξόδου θα τοποθετηθεί στον φάκελο που καθορίσατε.

### Βήμα 5: Εμφάνιση Μηνύματος Επιτυχίας

```csharp
Console.WriteLine("OpenDwfxFile executed successfully");
```

Ένα απλό μήνυμα στην κονσόλα σας ενημερώνει ότι η μετατροπή ολοκληρώθηκε χωρίς σφάλματα.

## Κοινά Προβλήματα & Συμβουλές

* **Αρχείο δεν βρέθηκε** – Double‑check the `SourceDir` path and ensure the file name matches exactly, including case.  
* **Κενό PDF** – Make sure the DWFX file actually contains vector data; some export tools generate empty drawings.  
* **Απόδοση** – For very large drawings, consider reducing `PageWidth`/`PageHeight` or setting a lower `Resolution` in `CadRasterizationOptions`.

## Συχνές Ερωτήσεις

### Ε1: Είναι το Aspose.CAD for .NET συμβατό με όλα τα αρχεία DWFX;

Α1: Το Aspose.CAD for .NET υποστηρίζει μια ευρεία γκάμα μορφών CAD, συμπεριλαμβανομένου του DWFX. Ωστόσο, συνιστάται να ελέγξετε την τεκμηρίωση για συγκεκριμένες λεπτομέρειες συμβατότητας.

### Ε2: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.CAD for .NET;

Α2: Η τεκμηρίωση είναι διαθέσιμη [εδώ](https://reference.aspose.com/cad/net/).

### Ε3: Μπορώ να δοκιμάσω το Aspose.CAD for .NET πριν την αγορά;

Α3: Ναι, μπορείτε να κατεβάσετε μια δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD for .NET;

Α4: Οι προσωρινές άδειες μπορούν να αποκτηθούν [εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Χρειάζεστε υποστήριξη ή έχετε περισσότερες ερωτήσεις;

Α5: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για βοήθεια.

### Ε6: Μπορώ να επεξεργαστώ πολλαπλά αρχεία DWFX σε παρτίδα;

Α6: Απόλυτα. Τυλίξτε τη λογική φόρτωσης και αποθήκευσης μέσα σε έναν βρόχο `foreach` που διατρέχει τα αρχεία σε έναν φάκελο.

### Ε7: Διατηρεί η μετατροπή τα επίπεδα και τα χρώματα;

Α7: Οι διανυσματικές πληροφορίες όπως τα επίπεδα και τα χρώματα διατηρούνται στο PDF όταν το πηγαίο DWFX περιέχει αυτά τα δεδομένα.

**Τελευταία ενημέρωση:** 2026-04-09  
**Δοκιμή με:** Aspose.CAD for .NET 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}