---
date: 2026-03-13
description: Μάθετε πώς να ορίζετε τις επιλογές rasterization του CAD και να εξάγετε
  συγκεκριμένες διατάξεις DWG σε PDF χρησιμοποιώντας το Aspose.CAD για .NET – ο απόλυτος
  οδηγός για τη δημιουργία PDF από αρχείο CAD.
linktitle: Exporting Specific Layouts to PDF
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Ορισμός επιλογών rasterization CAD – Εξαγωγή συγκεκριμένων διατάξεων σε PDF
  - Οδηγός Aspose.CAD
url: /el/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή Συγκεκριμένων Διατάξεων σε PDF - Οδηγός Aspose.CAD

## Εισαγωγή

Σε αυτό το σεμινάριο θα ανακαλύψετε **πώς να ορίσετε τις επιλογές rasterization CAD** ώστε να μπορείτε να εξάγετε μια μόνο διάταξη — ή πολλαπλές διατάξεις — από ένα αρχείο DWG απευθείας σε PDF. Το Aspose.CAD για .NET καθιστά τη διαδικασία *dwg to pdf conversion c#* απλή, παρέχοντάς σας πλήρη έλεγχο του μεγέθους σελίδας, της ανάλυσης και της επιλογής διάταξης. Στο τέλος του οδηγού θα μπορείτε να **δημιουργήσετε PDF από αρχείο CAD** με μόνο λίγες γραμμές κώδικα.

## Γρήγορες Απαντήσεις
- **Τι κάνει η “set cad rasterization options”;**  
  Λέει στο Aspose.CAD πώς να αποδώσει τα διανυσματικά δεδομένα (διατάξεις, επίπεδα, πάχη γραμμών) σε rasterized σελίδες PDF.  
- **Ποια μέθοδος εξάγει μια διάταξη DWG σε PDF;**  
  Χρησιμοποιήστε `Image.Save` με ένα ρυθμισμένο `PdfOptions` που περιέχει το `CadRasterizationOptions` σας.  
- **Μπορώ να εξάγω περισσότερες από μία διατάξεις ταυτόχρονα;**  
  Ναι – παρέχετε έναν πίνακα με ονόματα διατάξεων στην ιδιότητα `Layouts`.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;**  
  Απαιτείται εμπορική άδεια· διατίθεται δωρεάν δοκιμαστική έκδοση για αξιολόγηση.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;**  
  .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6 και μεταγενέστερες.

## Τι είναι η “set cad rasterization options”;
`CadRasterizationOptions` είναι η κλάση που ελέγχει πώς τα CAD entities rasterize όταν μετατρέπονται σε μορφές βασισμένες σε raster όπως το PDF. Ρυθμίζοντας τις ιδιότητές της — διαστάσεις σελίδας, επιλογή διάταξης, χρώμα φόντου κ.λπ. — καθορίζετε το οπτικό αποτέλεσμα της λειτουργίας **export dwg layout to pdf**.

## Γιατί να ορίσετε τις επιλογές rasterization CAD;
- **Precision** – Διατηρεί τα πάχη γραμμών και τις κλίμακες ακριβώς όπως εμφανίζονται στο αρχικό σχέδιο CAD.  
- **Performance** – Αποδίδει μόνο τις διατάξεις που χρειάζεστε, μειώνοντας το μέγεθος του αρχείου και το χρόνο επεξεργασίας.  
- **Flexibility** – Ρυθμίζει το πλάτος/ύψος σελίδας, DPI και φόντο ώστε να ταιριάζει με τα πρότυπα αναφοράς σας.  

## Προαπαιτούμενα

Πριν βουτήξουμε στον κώδικα, βεβαιωθείτε ότι έχετε:

- **Aspose.CAD for .NET** εγκατεστημένο. Μπορείτε να το κατεβάσετε [εδώ](https://releases.aspose.com/cad/net/).  
- Ένα περιβάλλον ανάπτυξης .NET (Visual Studio, VS Code ή οποιοδήποτε IDE προτιμάτε).  
- Ένα αρχείο DWG που περιέχει τουλάχιστον μία διάταξη (το δείγμα αρχείου που χρησιμοποιείται εδώ είναι `visualization_-_conference_room.dwg`).

## Εισαγωγή Namespaces

Στο .NET project σας, εισάγετε τα απαραίτητα namespaces για το Aspose.CAD:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Οδηγός Βήμα‑βήμα

### Βήμα 1: Φόρτωση του αρχείου DWG

Πρώτα, υποδείξτε στο Aspose.CAD το πηγαίο αρχείο DWG που θέλετε να μετατρέψετε.

```csharp
// The path to the documents directory.
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";

using (Image image = Image.Load(sourceFilePath))
{
    // Your code for further steps goes here.
}
```

### Βήμα 2: Ορίστε **CadRasterizationOptions**

Εδώ ρυθμίζουμε τις ρυθμίσεις rasterization που καθορίζουν το μέγεθος σελίδας PDF και την ανάλυση.

```csharp
// Create an instance of CadRasterizationOptions and set its various properties
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
```

> **Pro tip:** Προσαρμόστε το `PageWidth` και το `PageHeight` ώστε να ταιριάζουν με τις διαστάσεις της στόχευσης PDF διάταξης. Μεγαλύτερες τιμές αυξάνουν τη λεπτομέρεια αλλά και το μέγεθος του αρχείου.

### Βήμα 3: Καθορίστε το όνομα της διάταξης

Πείτε στο Aspose.CAD ποια διάταξη(ες) θα αποδοθούν. Αντικαταστήστε το `"Layout1"` με το ακριβές όνομα της διάταξης στο αρχείο DWG σας.

```csharp
// Specify desired layout name
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

> **Why this matters:** Περιορίζοντας τον πίνακα `Layouts` αποφεύγετε την εξαγωγή ανεπιθύμητων φύλλων, κάνοντας τη λειτουργία **dwg to pdf conversion c#** ταχύτερη και το παραγόμενο PDF πιο καθαρό.

### Βήμα 4: Δημιουργήστε `PdfOptions`

Συνδέστε τις ρυθμίσεις rasterization με τις επιλογές εξαγωγής PDF.

```csharp
// Create an instance of PdfOptions
PdfOptions pdfOptions = new PdfOptions();
// Set the VectorRasterizationOptions property
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

### Βήμα 5: Εξαγωγή σε PDF

Τέλος, αποθηκεύστε τη διαμορφωμένη διάταξη ως αρχείο PDF.

```csharp
MyDir = MyDir + "ExportSpecificLayoutToPDF_out.pdf";
// Export the DWG to PDF
image.Save(MyDir, pdfOptions);
```

### Βήμα 6: Εμφάνιση μηνύματος επιτυχίας

Μια γρήγορη έξοδος στην κονσόλα επιβεβαιώνει ότι η λειτουργία ολοκληρώθηκε με επιτυχία.

```csharp
// Display success message
Console.WriteLine("\nThe DWG file with a specific layout exported successfully to PDF.\nFile saved at " + MyDir);
```

## Συχνά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| **No PDF generated** | Ο πίνακας `Layouts` δεν ταιριάζει με κανένα όνομα διάταξης στο DWG. | Επαληθεύστε τα ονόματα διατάξεων χρησιμοποιώντας έναν CAD viewer και ενημερώστε την ιδιότητα `Layouts`. |
| **Blank pages** | Τα `PageWidth`/`PageHeight` έχουν τιμή 0 ή εξαιρετικά μικρές τιμές. | Χρησιμοποιήστε ρεαλιστικές διαστάσεις (π.χ., 1600 × 1600) ή αφήστε το Aspose να υπολογίσει αυτόματα παραλείποντας αυτές τις ιδιότητες. |
| **Incorrect scaling** | Δεν έχει οριστεί DPI όταν απαιτείται υψηλή ανάλυση. | Ορίστε `rasterizationOptions.Resolution = 300;` (ή το επιθυμητό DPI) πριν την εξαγωγή. |

## Συχνές Ερωτήσεις

**Q: Μπορώ να εξάγω πολλαπλές διατάξεις ταυτόχρονα;**  
A: Ναι, απλώς τροποποιήστε τον πίνακα `Layouts` στο Βήμα 3 ώστε να περιλαμβάνει όλα τα επιθυμητά ονόματα διατάξεων, π.χ., `new string[] { "Layout1", "Layout2" }`.

**Q: Είναι το Aspose.CAD συμβατό με άλλες μορφές αρχείων CAD;**  
A: Απόλυτα. Υποστηρίζει DWG, DXF, DWF, DGN και πολλές άλλες μορφές.

**Q: Πώς μπορώ να ρυθμίσω τις ρυθμίσεις εξόδου PDF πέρα από το μέγεθος σελίδας;**  
A: Εξερευνήστε πρόσθετες ιδιότητες του `CadRasterizationOptions` όπως `Resolution`, `BackgroundColor` και `DrawType` για να βελτιστοποιήσετε το αποτέλεσμα.

**Q: Πού μπορώ να βρω επιπλέον τεκμηρίωση για το Aspose.CAD;**  
A: Επισκεφθείτε την [documentation](https://reference.aspose.com/cad/net/) για αναλυτικές αναφορές API και παραδείγματα.

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμαστική έκδοση;**  
A: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

## Συμπέρασμα

Έχετε τώρα μάθει πώς να **ορίσετε τις επιλογές rasterization CAD** και να τις χρησιμοποιήσετε για **εξαγωγή συγκεκριμένων διατάξεων DWG σε PDF** με το Aspose.CAD για .NET. Αυτή η προσέγγιση σας δίνει ακριβή έλεγχο της διαδικασίας μετατροπής, επιτρέποντάς σας να ενσωματώσετε τη λειτουργία CAD‑to‑PDF σε οποιαδήποτε εφαρμογή C# γρήγορα και αξιόπιστα.

---

**Last Updated:** 2026-03-13  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}