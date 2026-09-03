---
date: 2026-08-23
description: Μάθετε πώς να δημιουργήσετε viewport dwg c# χρησιμοποιώντας Aspose.CAD.
  Αυτός ο οδηγός καλύπτει τη φόρτωση ενός αρχείου DWG, τη ρύθμιση της rasterization,
  τον ορισμό ενός viewport και την αποθήκευση του αποτελέσματος ως PDF.
keywords:
- create viewport dwg c#
- render dwg c#
- aspose.cad .net
lastmod: 2026-08-23
linktitle: Απόδοση εγγράφων DWG σε C#
og_description: Μάθετε πώς να δημιουργήσετε viewport dwg c# χρησιμοποιώντας Aspose.CAD
  σε .NET. Αυτός ο οδηγός βήμα‑βήμα δείχνει τη φόρτωση, τη rasterizing, τον ορισμό
  viewports και την αποθήκευση σε PDF.
og_image_alt: Guide showing how to create viewport dwg c# with Aspose.CAD in .NET
og_title: Πώς να δημιουργήσετε viewport dwg c# με Aspose.CAD για .NET
schemas:
- author: Aspose
  dateModified: '2026-08-23'
  description: Learn how to create viewport dwg c# using Aspose.CAD. This guide covers
    loading a DWG file, configuring rasterization, defining a viewport, and saving
    the result as PDF.
  headline: How to create viewport dwg c# with Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: Load the DWG file with `CadImage.Load`.
    question: What is the first step?
  - answer: '`Viewport` inside `CadRasterizationOptions`.'
    question: Which class defines the view area?
  - answer: Yes, using `PdfOptions` after rasterization.
    question: Can I output to PDF?
  - answer: A commercial license is required; a free trial works for evaluation.
    question: Do I need a license for production?
  - answer: Absolutely – Aspose.CAD works with .NET Framework, .NET Core, and .NET 5/6.
    question: Is .NET Core supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- create viewport dwg c#
- Aspose.CAD
- C# CAD rendering
- DWG to PDF
- CAD viewports
title: Πώς να δημιουργήσετε viewport dwg c# με Aspose.CAD για .NET
url: /el/net/image-manipulation-and-rendering/rendering-dwg-documents/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Απόδοση εγγράφων DWG σε C# – δημιουργία viewport dwg c# tutorial

## Εισαγωγή

Σε αυτό το ολοκληρωμένο tutorial θα μάθετε πώς να **create viewport dwg c#** με το Aspose.CAD και να αποδώσετε ένα αρχείο DWG σε PDF. Είτε χρειάζεστε την εξαγωγή ενός συγκεκριμένου layout, τη δημιουργία ενός εκτυπώσιμου φύλλου, είτε την ενσωμάτωση μιας προβολής CAD σε αναφορά, ο έλεγχος του viewport σας δίνει ακριβή έλεγχο απόδοσης. Το Aspose.CAD υποστηρίζει **20+ CAD formats** και μπορεί να επεξεργαστεί αρχεία με χιλιάδες οντότητες χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, καθιστώντας το ιδανικό για εφαρμογές .NET υψηλής απόδοσης.

## Γρήγορες απαντήσεις
- **Ποιο είναι το πρώτο βήμα;** Φορτώστε το αρχείο DWG με `CadImage.Load`.
- **Ποια κλάση ορίζει την περιοχή προβολής;** `Viewport` μέσα στο `CadRasterizationOptions`.
- **Μπορώ να εξάγω σε PDF;** Ναι, χρησιμοποιώντας `PdfOptions` μετά τη rasterization.
- **Χρειάζεται άδεια για παραγωγή;** Απαιτείται εμπορική άδεια· μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση.
- **Υποστηρίζεται το .NET Core;** Απόλυτα – το Aspose.CAD λειτουργεί με .NET Framework, .NET Core και .NET 5/6.

## Προαπαιτούμενα

Πριν βυθιστείτε στον κώδικα, βεβαιωθείτε ότι έχετε:

- Βασικές γνώσεις προγραμματισμού C#.
- Εγκατεστημένο Visual Studio (οποιαδήποτε πρόσφατη έκδοση).
- Βιβλιοθήκη Aspose.CAD προστεθειμένη στο έργο σας. Μπορείτε να τη κατεβάσετε από [Aspose.CAD download page](https://releases.aspose.com/cad/net/).
- Ένα δείγμα αρχείου DWG όπως το **Bottom_plate.dwg** για να ακολουθήσετε.

## Εισαγωγή ονοματοχώρων

Προσθέστε τις απαιτούμενες οδηγίες `using` στην κορυφή του αρχείου C# ώστε ο μεταγλωττιστής να εντοπίζει τους τύπους Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.FileFormats.Cad;
```

Τώρα που το περιβάλλον είναι έτοιμο, ας περάσουμε βήμα-βήμα στην υλοποίηση.

## Πώς να δημιουργήσετε viewport dwg c#;

Για να δημιουργήσετε ένα προσαρμοσμένο viewport, πρώτα φορτώστε το αρχείο DWG σε ένα αντικείμενο `CadImage`, στη συνέχεια διαμορφώστε το `CadRasterizationOptions` με το επιθυμητό layout και κλίμακα. Ορίστε την περιοχή που θέλετε να εμφανίσετε, δημιουργήστε ένα `CadVportTableObject` με το υπολογισμένο κέντρο, ύψος και λόγο διαστάσεων, αντικαταστήστε το ενεργό viewport, ορίστε τυχόν επιλογές PDF και, τέλος, αποθηκεύστε το αποτέλεσμα.

## Βήμα 1: φόρτωση του αρχείου dwg

`CadImage.Load` φορτώνει ένα αρχείο DWG σε ένα αντικείμενο `CadImage`, το οποίο αντιπροσωπεύει το σχέδιο CAD στη μνήμη.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "Bottom_plate.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code for loading the DWG file goes here.
}
```

## Βήμα 2: ρύθμιση επιλογών rasterization

`CadRasterizationOptions` καθορίζει πώς θα rasterize το σχέδιο CAD, συμπεριλαμβανομένης της επιλογής layout, κλίμακας και μεγέθους εξόδου.

```csharp
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.Layouts = new string[] { "Model" };
rasterizationOptions.NoScaling = true;
// Additional rasterization configurations can be added here.
```

## Βήμα 3: ορισμός περιοχής για σχεδίαση

`Point` ορίζει τις συντεταγμένες X και Y της πάνω‑αριστερής γωνίας της περιοχής που θα αποδοθεί.

```csharp
Point topLeft = new Point(6156, 7053);
double width = 3108;
double height = 2489;
```

## Βήμα 4: δημιουργία νέου viewport

`CadVportTableObject` αντιπροσωπεύει ένα αντικείμενο viewport που ελέγχει την ορατή περιοχή και το λόγο διαστάσεων του αποδομένου σχεδίου.

```csharp
CadVportTableObject newView = new CadVportTableObject();
newView.Name.Value = "*Active";
newView.CenterPoint.X = topLeft.X + width / 2f;
newView.CenterPoint.Y = topLeft.Y - height / 2f;
newView.ViewHeight.Value = height;
newView.ViewAspectRatio.Value = width / height;
```

## Βήμα 5: αντικατάσταση ενεργού viewport

Ο βρόχος αντικαθιστά το ενεργό viewport με το νέο που δημιουργήθηκε για να εφαρμοστούν οι προσαρμοσμένες ρυθμίσεις προβολής.

```csharp
for (int i = 0; i < cadImage.ViewPorts.Count; i++)
{
    CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
    if ((currentView.Name.Value == null && cadImage.ViewPorts.Count == 1) ||
    string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
    {
        cadImage.ViewPorts[i] = newView;
        break;
    }
}
```

## Βήμα 6: ρύθμιση επιλογών PDF

`PdfOptions` διαμορφώνει τις παραμέτρους εξόδου PDF όπως συμπίεση και μεταδεδομένα.

```csharp
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 7: αποθήκευση του αποδομένου dwg ως PDF

`image.Save` γράφει την αποδομένη εικόνα σε αρχείο χρησιμοποιώντας τις καθορισμένες επιλογές μορφής.

```csharp
cadImage.Save(MyDir, pdfOptions);
```

## Γιατί να χρησιμοποιήσετε προσαρμοσμένο viewport κατά την απόδοση DWG;

Ένα προσαρμοσμένο viewport σας επιτρέπει να απομονώσετε ένα συγκεκριμένο layout ή περιοχή, μειώνοντας το μέγεθος του αρχείου και βελτιώνοντας την ταχύτητα απόδοσης. Το Aspose.CAD μπορεί να αποδώσει ένα DWG 300‑σελίδων σε λιγότερο από 2 δευτερόλεπτα όταν χρησιμοποιείται εστιασμένο viewport, σε σύγκριση με την πλήρη απόδοση που μπορεί να διαρκέσει αρκετά δευτερόλεπτα περισσότερο.

## Κοινά προβλήματα και λύσεις

- **Blank output** – Βεβαιωθείτε ότι οι συντεταγμένες του viewport βρίσκονται εντός των ορίων του σχεδίου· χρησιμοποιήστε `CadImage.Size` για να επαληθεύσετε τα όρια.
- **Missing layers** – Ορίστε `CadRasterizationOptions.Layouts` στο σωστό όνομα layout· διαφορετικά το προεπιλεγμένο layout μπορεί να είναι κενό.
- **Performance slowdown** – Απενεργοποιήστε το anti‑aliasing στο `CadRasterizationOptions` αν χρειάζεστε μόνο μια γρήγορη προεπισκόπηση.

## Συχνές ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλα μορφότυπα αρχείων CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει διάφορα μορφότυπα, συμπεριλαμβανομένων των DWG, DXF, DWF και περισσότερων από 20 επιπλέον τύπων CAD.

### Q2: Είναι το Aspose.CAD συμβατό με .NET Core;

A2: Ναι, το Aspose.CAD λειτουργεί με .NET Framework, .NET Core και τις τελευταίες εκδόσεις .NET.

### Q3: Πώς μπορώ να διαχειριστώ διαφορετικά layouts σε ένα αρχείο DWG;

A3: Καθορίστε το επιθυμητό layout χρησιμοποιώντας την ιδιότητα `Layouts` του `CadRasterizationOptions` πριν από την απόδοση.

### Q4: Υπάρχουν ζητήματα αδειοδότησης για τη χρήση του Aspose.CAD;

A4: Για λεπτομέρειες αδειοδότησης, επισκεφθείτε τη [Aspose.CAD licensing page](https://purchase.aspose.com/buy).

### Q5: Πού μπορώ να βρω πρόσθετη υποστήριξη;

A5: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για βοήθεια από την κοινότητα και συζητήσεις.

### Q6: Μπορώ να αποδώσω απευθείας σε PNG αντί για PDF;

A6: Ναι, αλλάξτε το `PdfOptions` σε `PngOptions` και καλέστε `image.Save("output.png", pngOptions)`.

### Q7: Πώς ενσωματώνω την αποδομένη εικόνα σε μια εφαρμογή Windows Forms;

A7: Φορτώστε την αποθηκευμένη εικόνα σε ένα στοιχείο `PictureBox` χρησιμοποιώντας `Image.FromFile("output.png")`.

## Συμπέρασμα

Τώρα γνωρίζετε πώς να **create viewport dwg c#** και να αποδώσετε ένα αρχείο DWG σε PDF (ή άλλα raster formats) χρησιμοποιώντας το Aspose.CAD. Με τον έλεγχο του viewport αποκτάτε λεπτομερή διαχείριση της οπτικής εξόδου, κάτι που είναι απαραίτητο για τη δημιουργία ακριβών τεχνικών σχεδίων, αναφορών ή μικρογραφιών. Εξερευνήστε πρόσθετες ρυθμίσεις rasterization, πειραματιστείτε με διαφορετικές μορφές εξόδου και ενσωματώστε τον κώδικα σε μεγαλύτερες υπηρεσίες .NET ή επιτραπέζιες βοηθητικές εφαρμογές.

---

**Τελευταία ενημέρωση:** 2026-08-23  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Πώς να ορίσετε Viewport κατά τη μετατροπή DWG σε PDF με Συντεταγμένες σε C# - Aspose.CAD Tutorial](/cad/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/)
- [Μάθετε να ορίζετε CAD Rasterization Options – Εξαγωγή Συγκεκριμένων Layouts σε PDF με Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)
- [Πώς να μετατρέψετε DWG σε PDF και Raster Images χρησιμοποιώντας Aspose.CAD για .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}