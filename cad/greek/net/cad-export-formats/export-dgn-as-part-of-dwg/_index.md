---
date: 2026-03-21
description: Μάθετε πώς να δημιουργείτε PDF από DWG και να εξάγετε DGN ως μέρος του
  DWG χρησιμοποιώντας το Aspose.CAD για .NET. Αυτός ο οδηγός δείχνει επίσης πώς να
  μετατρέψετε DWG σε PDF και να ορίσετε τις επιλογές PDF.
linktitle: Export DGN as Part of DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Δημιουργία PDF από DWG και Εξαγωγή DGN ως μέρος του DWG – Aspose.CAD για .NET
url: /el/net/cad-export-formats/export-dgn-as-part-of-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία PDF από DWG και Εξαγωγή DGN ως Μέρος του DWG – Aspose.CAD για .NET

## Εισαγωγή

Αν χρειάζεστε **δημιουργία PDF από DWG** αρχεία ενώ ταυτόχρονα ενσωματώνετε ένα σχέδιο DGN ως μέρος του DWG, το Aspose.CAD για .NET το καθιστά απλό. Σε αυτό το tutorial θα περάσουμε από όλη τη ροή εργασίας: φόρτωση ενός DWG, εντοπισμός του ενσωματωμένου DGN underlay, διαμόρφωση των επιλογών rasterization, και τελικά εξαγωγή του αποτελέσματος σε έγγραφο PDF. Είτε δημιουργείτε ένα εργαλείο μαζικής μετατροπής, μια μηχανή αναφορών ή μια υπηρεσία ενσωμάτωσης CAD‑BIM, τα παρακάτω βήματα θα σας προσφέρουν μια σταθερή, έτοιμη για παραγωγή βάση.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή DWG → PDF;** Aspose.CAD for .NET  
- **Μπορώ να εξάγω ένα DGN underlay ενώ δημιουργώ το PDF;** Yes – the underlay is accessed via `CadDgnUnderlay`.  
- **Ποια μέθοδος ορίζει τις επιλογές PDF;** `PdfOptions` together with `CadRasterizationOptions`.  
- **Χρειάζομαι άδεια για εμπορική χρήση;** Yes, a valid Aspose.CAD license is required.  
- **Υποστηριζόμενες εκδόσεις .NET;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι η “δημιουργία PDF από DWG”;

Η δημιουργία PDF από ένα αρχείο DWG σημαίνει την απόδοση του διανυσματικού σχεδίου σε έγγραφο PDF raster ή vector‑based. Αυτή η διαδικασία είναι χρήσιμη για την κοινή χρήση σχεδίων με ενδιαφερόμενους που δεν διαθέτουν λογισμικό CAD, για αρχειοθέτηση ή για δημιουργία εκτυπώσιμων αναφορών. Το Aspose.CAD απλοποιεί την εργασία διαχειριζόμενο τη βαριά δουλειά της ανάλυσης των οντοτήτων DWG και παρέχοντας λεπτομερή έλεγχο της εξόδου μέσω του `PdfOptions`.

## Γιατί να εξάγετε DGN ως μέρος ενός DWG;

Ένα DGN underlay συχνά αντιπροσωπεύει γεωμετρία αναφοράς από έργα MicroStation. Εξάγοντας το DGN μαζί με το DWG διατηρείτε το αρχικό πλαίσιο σχεδίου, εξασφαλίζοντας ότι οι επόμενοι χρήστες βλέπουν το πλήρες σύνολο σχεδίων. Αυτό είναι ιδιαίτερα πολύτιμο σε πολυτομεακά έργα όπου τα αρχεία DWG και DGN συνυπάρχουν.

## Προαπαιτούμενα

- **Aspose.CAD για .NET** – κατεβάστε το [εδώ](https://releases.aspose.com/cad/net/).  
- **Περιβάλλον Ανάπτυξης** – Visual Studio (οποιαδήποτε πρόσφατη έκδοση) ή το προτιμώμενο .NET IDE σας.  
- **Βασικές γνώσεις C#** – πρέπει να είστε εξοικειωμένοι με τη σύνταξη C# και τη δομή έργου .NET.

## Εισαγωγή Namespaces

Προσθέστε τις απαιτούμενες οδηγίες `using` στην αρχή του αρχείου πηγαίου κώδικα C#:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Οδηγός Βήμα‑βήμα

### Βήμα 1: Ορισμός Διαδρομών Αρχείων

Ορίστε το αρχείο DWG εισόδου και το όνομα του αρχείου PDF εξόδου.

```csharp
// Input and Output file paths
string fileName = "BlockRefDgn.dwg";
string outPath = fileName + ".pdf";
```

### Βήμα 2: Δημιουργία Αντικειμένου `PdfOptions` (ορισμός επιλογών pdf)

`PdfOptions` σας επιτρέπει να ελέγχετε πώς δημιουργείται το PDF, όπως το μέγεθος σελίδας, η συμπίεση και τα μεταδεδομένα.

```csharp
// Create an instance of PdfOptions class for exporting DWG to PDF
PdfOptions exportOptions = new PdfOptions();
```

### Βήμα 3: Φόρτωση του Αρχείου DWG

Φορτώστε το DWG ως `CadImage` ώστε να μπορείτε να εξετάσετε τις οντότητές του.

```csharp
// Load the existing DWG file as an image and convert it to CadImage type
using (CadImage cadImage = (CadImage)Image.Load(fileName))
```

### Βήμα 4: Επανάληψη μέσω των Οντοτήτων

Περιηγηθείτε σε κάθε οντότητα του σχεδίου για να εντοπίσετε το DGN underlay.

```csharp
// Iterate through each entity inside the DWG file
foreach (CadBaseEntity baseEntity in cadImage.Entities)
```

### Βήμα 5: Έλεγχος Τύπου Οντότητας (πώς να εξάγετε dgn)

Καθορίστε εάν η τρέχουσα οντότητα είναι DGN underlay.

```csharp
// Check if the entity is an image definition
if (baseEntity.TypeName == CadEntityTypeName.DGNUNDERLAY)
```

### Βήμα 6: Λήψη Διαδρομής Underlay

Ανακτήστε τη διαδρομή εξωτερικής αναφοράς του αρχείου DGN.

```csharp
// If it's an image definition, get the external reference to the object
CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
Console.WriteLine(dgnFile.UnderlayPath);
```

### Βήμα 7: Ορισμός Επιλογών Rasterization (μετατροπή dwg σε pdf)

Διαμορφώστε πώς θα rasterize το DWG πριν το τοποθετήσετε στο PDF.

```csharp
// Define settings for CadRasterizationOptions object
exportOptions.VectorRasterizationOptions = new CadRasterizationOptions()
{
    PageWidth = 1600,
    PageHeight = 1600,
    Layouts = new string[] { "Model" },
    AutomaticLayoutsScaling = false,
    NoScaling = true,
    BackgroundColor = Color.Black,
    DrawType = CadDrawTypeMode.UseObjectColor
};
```

### Βήμα 8: Εξαγωγή DWG σε PDF

Τέλος, αποθηκεύστε την αποδοθείσα εικόνα ως αρχείο PDF.

```csharp
// Export the DWG to PDF by calling Save method
cadImage.Save(outPath, exportOptions);
```

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **`Image.Load` throws “File not found”** | Λανθασμένη διαδρομή ή έλλειψη αρχείου. | Χρησιμοποιήστε απόλυτη διαδρομή ή βεβαιωθείτε ότι το DWG έχει αντιγραφεί στο φάκελο εξόδου. |
| **Underlay path is empty** | Το DGN underlay δεν είναι ενσωματωμένο ή η αναφορά είναι σπασμένη. | Επιβεβαιώστε ότι το DWG περιέχει πραγματικά ένα DGN underlay και ότι το εξωτερικό αρχείο DGN είναι προσβάσιμο. |
| **PDF output is blank** | Οι επιλογές rasterization έχουν οριστεί σε μέγεθος μηδέν. | Ρυθμίστε `PageWidth`/`PageHeight` ή ορίστε `NoScaling = false`. |
| **License exception** | Εκτέλεση χωρίς έγκυρη άδεια Aspose.CAD. | Εφαρμόστε την άδεια πριν φορτώσετε την εικόνα: `License lic = new License(); lic.SetLicense("Aspose.CAD.lic");` |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET στα εμπορικά μου έργα;
A1: Ναι, μπορείτε. Επισκεφθείτε [εδώ](https://purchase.aspose.com/buy) για να εξερευνήσετε τις επιλογές αδειοδότησης.

### Q2: Υπάρχουν περιορισμοί στο μέγεθος των αρχείων DWG που μπορώ να επεξεργαστώ;
A2: Το Aspose.CAD υποστηρίζει την επεξεργασία μεγάλων αρχείων DWG, αλλά μπορεί να ισχύουν περιορισμοί υλικού.

### Q3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση;
A3: Ναι, μπορείτε να λάβετε δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q4: Πώς μπορώ να αποκτήσω προσωρινές άδειες;
A4: Προσωρινές άδειες μπορούν να ληφθούν [εδώ](https://purchase.aspose.com/temporary-license/).

### Q5: Πού μπορώ να ζητήσω βοήθεια αν αντιμετωπίσω προβλήματα;
A5: Μπορείτε να επισκεφθείτε το φόρουμ Aspose.CAD [εδώ](https://forum.aspose.com/c/cad/19) για υποστήριξη.

**Ε: Πώς ορίζω πρόσθετα μεταδεδομένα PDF (συγγραφέας, τίτλος κ.λπ.;)**  
Α: Χρησιμοποιήστε τις ιδιότητες `exportOptions.Metadata` πριν καλέσετε `Save`.

**Ε: Μπορώ να εξάγω πολλαπλές διατάξεις σε ξεχωριστές σελίδες PDF;**  
Α: Ναι – ορίστε `Layouts = new string[] { "Layout1", "Layout2" }` στο `CadRasterizationOptions`.

**Ε: Υποστηρίζει το Aspose.CAD τη μετατροπή DWG σε άλλες μορφές εικόνας;**  
Α: Απόλυτα. Μπορείτε να εξάγετε σε PNG, JPEG, SVG και άλλα χρησιμοποιώντας τις αντίστοιχες υπερφορτώσεις του `Image.Save`.

---

**Τελευταία Ενημέρωση:** 2026-03-21  
**Δοκιμάστηκε Με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}