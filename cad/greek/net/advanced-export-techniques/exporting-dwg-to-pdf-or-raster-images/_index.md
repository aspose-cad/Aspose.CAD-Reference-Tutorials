---
date: 2026-03-16
description: Μάθετε πώς να μετατρέπετε DWG σε PDF ή ραστερ εικόνες με το Aspose.CAD
  για .NET. Αυτός ο βήμα‑βήμα οδηγός CAD σε PDF καλύπτει την εξαγωγή DWG σε μορφές
  εικόνας όπως PNG και δείχνει πώς να εξάγετε DWG σε αρχεία εικόνας αποδοτικά.
linktitle: Exporting DWG to PDF or Raster Images
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να μετατρέψετε DWG σε PDF και εικόνες raster χρησιμοποιώντας το Aspose.CAD
  για .NET
url: /el/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DWG σε PDF ή Ράστερ Εικόνες - Οδηγός Aspose.CAD

## Εισαγωγή

Αν χρειάζεστε **convert DWG to PDF** (ή σε μορφές ράστερ όπως PNG) απευθείας από μια εφαρμογή .NET, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε βήμα-βήμα τις ακριβείς διαδικασίες που απαιτούνται για τη χρήση του Aspose.CAD for .NET για την εκτέλεση της μετατροπής, θα εξηγήσουμε γιατί η βιβλιοθήκη είναι μια αξιόπιστη επιλογή, και θα σας δείξουμε πώς να διαχειριστείτε τόσο την έξοδο PDF όσο και εικόνας με λίγες μόνο γραμμές κώδικα.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή DWG;** Aspose.CAD for .NET  
- **Μπορώ να εξάγω DWG σε PNG καθώς και σε PDF;** Yes – the same rasterization options work for both formats.  
- **Χρειάζομαι άδεια για ανάπτυξη;** A free trial works for testing; a commercial license is required for production.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Γίνεται αυτόματη μετατροπή μονάδων;** You can define the unit system manually (metric or imperial) as shown in the code.

## Τι είναι το “convert DWG to PDF”;
Η μετατροπή DWG σε PDF σημαίνει ότι παίρνουμε ένα σχέδιο CAD (DWG) και το αποδίδουμε σε ένα φορητό, μόνο για προβολή έγγραφο (PDF). Αυτό είναι χρήσιμο για την κοινή χρήση σχεδίων με ενδιαφερόμενους που δεν διαθέτουν λογισμικό CAD, για τη δημιουργία εκτυπώσιμης τεκμηρίωσης ή για την αρχειοθέτηση σχεδίων σε μια καθολικά αναγνώσιμη μορφή.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για αυτή τη μετατροπή;
- **No external dependencies** – Η βιβλιοθήκη λειτουργεί εξ ολοκλήρου σε managed code.  
- **High fidelity** – Διατηρεί τα layers, τα line weights και τις πληροφορίες layout.  
- **Built‑in raster options** – Επιτρέπει την εξαγωγή σε PNG, JPEG, BMP κ.λπ., με ένα μόνο αντικείμενο ρύθμισης.  
- **Cross‑platform** – Λειτουργεί σε Windows, Linux και macOS με .NET Core.

## Προαπαιτούμενα

Πριν ξεκινήσουμε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Βασική κατανόηση του προγραμματισμού .NET.  
- Εγκατεστημένη η βιβλιοθήκη Aspose.CAD for .NET. Αν όχι, κατεβάστε την [εδώ](https://releases.aspose.com/cad/net/).  
- Το αγαπημένο σας ολοκληρωμένο περιβάλλον ανάπτυξης (IDE) ρυθμισμένο για ανάπτυξη .NET.

## Εισαγωγή Namespaces

Ας ξεκινήσουμε εισάγοντας τα απαραίτητα namespaces στο .NET project σας. Αυτό εξασφαλίζει ότι έχετε πρόσβαση στη λειτουργικότητα του Aspose.CAD στον κώδικά σας.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
```

## Βήμα 1: Φόρτωση αρχείου DWG

Ξεκινήστε φορτώνοντας το αρχείο DWG που θέλετε να μετατρέψετε. Αντικαταστήστε το `"Your Document Directory"` με τη διαδρομή προς το αρχείο DWG σας.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";

using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading DWG goes here
}
```

## Βήμα 2: Ρύθμιση εξαγωγής PDF (Πώς να εξάγετε DWG σε PDF)

Τώρα, ας διαμορφώσουμε τις ρυθμίσεις εξαγωγής PDF. Αυτό το παράδειγμα δείχνει πώς να ορίσετε το layout και να διαχειριστείτε τις μετατροπές μονάδων.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };

// Check and define the unit system
bool currentUnitIsMetric = false;
double currentUnitCoefficient = 1.0;
DefineUnitSystem(cadImage.UnitType, out currentUnitIsMetric, out currentUnitCoefficient);

// Your code for setting up PDF export goes here
```

## Βήμα 3: Εξαγωγή σε PDF

Εκτελέστε την εξαγωγή σε PDF χρησιμοποιώντας τις διαμορφωμένες ρυθμίσεις.

```csharp
PdfOptions pdfOptions = new PdfOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath, pdfOptions);
```

## Βήμα 4: Εξαγωγή σε Ράστερ Εικόνες (export dwg to image)

Επεκτείνετε τη λειτουργικότητα για εξαγωγή σε ράστερ εικόνες, όπως PNG.

```csharp
// A4 size at 300 DPI - 2480 x 3508
rasterizationOptions.PageHeight = 3508;
rasterizationOptions.PageWidth = 2480;

PngOptions pngOptions = new PngOptions
{
    VectorRasterizationOptions = rasterizationOptions
};

cadImage.Save(outPath.Replace("pdf", "png"), pngOptions);
```

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Πώς να διορθώσετε |
|----------|----------------|-------------------|
| **Κενές σελίδες σε PDF** | Το layout δεν έχει οριστεί σωστά | Βεβαιωθείτε ότι το `rasterizationOptions.Layouts` περιλαμβάνει το σωστό όνομα layout (π.χ., `"Model"`). |
| **Λανθασμένες διαστάσεις** | Ασυμφωνία DPI ή μεγέθους σελίδας | Ρυθμίστε τις τιμές `PageHeight`, `PageWidth` και DPI στο `CadRasterizationOptions`. |
| **Οι μονάδες εμφανίζονται λανθασμένες** | Η μετατροπή μονάδων δεν έχει οριστεί | Χρησιμοποιήστε το `DefineUnitSystem` για να ορίσετε το `currentUnitIsMetric` και το `currentUnitCoefficient` βάσει του `cadImage.UnitType`. |
| **Απόκλιση άδειας** | Περιορισμοί έκδοσης trial | Εφαρμόστε προσωρινή ή μόνιμη άδεια πριν καλέσετε το `Image.Load`. |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD for .NET στα εμπορικά μου έργα;
A1: Ναι, μπορείτε. Επισκεφθείτε το [purchase.aspose.com/buy](https://purchase.aspose.com/buy) για λεπτομέρειες αδειοδότησης.

### Q2: Υπάρχει διαθέσιμη δωρεάν δοκιμή;
A2: Φυσικά! Πάρτε τη δωρεάν δοκιμή σας [εδώ](https://releases.aspose.com/).

### Q3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD for .NET;
A3: Μεταβείτε στο [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα.

### Q4: Μπορώ να αποκτήσω προσωρινή άδεια για δοκιμαστικούς σκοπούς;
A4: Ναι, μπορείτε να λάβετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q5: Πού μπορώ να βρω την αναλυτική τεκμηρίωση;
A5: Η τεκμηρίωση είναι διαθέσιμη στο [Aspose.CAD](https://reference.aspose.com/cad/net/).

### Q6: Πώς να **αποθηκεύσετε CAD ως PNG** με υψηλή ποιότητα;
A6: Ορίστε το `PageHeight` και το `PageWidth` στις επιθυμητές διαστάσεις pixel και επιλέξτε DPI 300 ή μεγαλύτερο στο `CadRasterizationOptions`.

### Q7: Ποιος είναι ο καλύτερος τρόπος για **how to convert dwg** όταν το αρχείο προέλευσης περιέχει πολλαπλά layouts;
A7: Συμπληρώστε το `rasterizationOptions.Layouts` με όλα τα ονόματα layout που θέλετε να εξάγετε, στη συνέχεια κάντε βρόχο σε κάθε layout και καλέστε το `Save` για κάθε μορφή εξόδου.

---

**Τελευταία ενημέρωση:** 2026-03-16  
**Δοκιμάστηκε με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}