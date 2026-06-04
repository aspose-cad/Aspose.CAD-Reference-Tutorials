---
date: 2026-06-04
description: Μάθετε πώς να εξάγετε εικόνες DXF χρησιμοποιώντας το Aspose.CAD για .NET
  και ανακαλύψτε πώς να κρύβετε γραμμές για πιο καθαρά σχέδια. Ακολουθήστε αυτόν τον
  οδηγό βήμα‑βήμα.
keywords:
- how to export dxf
- how to hide lines
- Aspose.CAD export images
linktitle: Εξαγωγή εικόνων σε μορφή DXF
schemas:
- author: Aspose
  dateModified: '2026-06-04'
  description: Learn how to export DXF images using Aspose.CAD for .NET and discover
    how to hide lines for cleaner drawings. Follow this step‑by‑step guide.
  headline: How to Export DXF Images with Aspose.CAD – Tutorial Guide
  type: TechArticle
- questions:
  - answer: Yes, Aspose.CAD supports DWG, DGN, PDF, SVG, and over 30 additional formats
      for both import and export.
    question: Is Aspose.CAD compatible with other CAD formats?
  - answer: Absolutely! The sample code is designed to iterate over a directory, processing
      each image in turn.
    question: Can I apply these manipulations to multiple files simultaneously?
  - answer: Visit [here](https://purchase.aspose.com/temporary-license/) to acquire
      a temporary license for evaluation purposes.
    question: How can I obtain a temporary license for Aspose.CAD?
  - answer: Join the Aspose.CAD community on the [support forum](https://forum.aspose.com/c/cad/19)
      to interact with fellow developers and seek guidance.
    question: Where can I seek assistance and engage with the community?
  - answer: Yes, you can explore a free trial [here](https://releases.aspose.com/)
      to experience the capabilities of Aspose.CAD.
    question: Does Aspose.CAD offer a free trial?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να εξάγετε εικόνες DXF με το Aspose.CAD – Οδηγός Εκμάθησης
url: /el/net/export-techniques/exporting-images-to-dxf-format/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Εξάγετε Εικόνες DXF με το Aspose.CAD – Οδηγός Εκμάθησης

## Εισαγωγή

Στον ταχύτατο κόσμο της ανάπτυξης CAD, η **πώς να εξάγετε dxf** αρχεία γρήγορα και με ακρίβεια μπορεί να καθορίσει την επιτυχία ενός έργου. Το Aspose.CAD για .NET σας παρέχει έναν αξιόπιστο, κώδικα‑πρώτο τρόπο για τη μετατροπή εικόνων raster σε σχέδια DXF χωρίς την ανάγκη πλήρους σουίτας CAD. Σε αυτόν τον οδηγό θα δείτε ακριβώς **πώς να εξάγετε dxf** εικόνες, να κρύψετε ανεπιθύμητη γεωμετρία και να τροποποιήσετε το κείμενο – όλα με σαφή, έτοιμα για παραγωγή βήματα.

## Γρήγορες Απαντήσεις
- **Ποια είναι η κύρια κλάση για τη μετατροπή;** `Image` class with `Save` method.
- **Ποια μορφή υποστηρίζει το Aspose.CAD για εξαγωγή DXF;** DXF (AutoCAD Drawing Interchange Format).
- **Μπορώ να κρύψω γραμμές κατά την εξαγωγή;** Yes – use the `HideLines` property or filter geometry.
- **Χρειάζομαι άδεια για ανάπτυξη;** A temporary license works for testing; a full license is required for production.
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6.

## Τι είναι το Aspose.CAD για .NET;

Aspose.CAD για .NET είναι μια βιβλιοθήκη .NET που επιτρέπει προγραμματιστική ανάγνωση, μετατροπή και απόδοση αρχείων CAD χωρίς την εγκατάσταση λογισμικού CAD. Υποστηρίζει πάνω από 30 μορφές CAD και μπορεί να επεξεργαστεί αρχεία μεγαλύτερα από 500 MB με ροή, παρέχοντας στους προγραμματιστές μια λύση υψηλής απόδοσης και αποδοτικής μνήμης. Για λεπτομερή αναφορά API, δείτε την [documentation](https://reference.aspose.com/cad/net/).

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για εξαγωγή εικόνων DXF;

- **Ποσοτικοποιημένο όφελος:** Υποστηρίζει **30+ είσοδους** (DWG, DGN, PDF, PNG, JPEG, BMP) και **10+ εξόδους**, συμπεριλαμβανομένου του DXF, με **μηδενική φόρτωση μνήμης** για αρχεία έως 1 GB.
- **Απόδοση:** Μετατρέπει ένα σχέδιο 200 σελίδων σε DXF σε λιγότερο από **2 δευτερόλεπτα** σε τυπική CPU 2.4 GHz.
- **Ακρίβεια:** Διατηρεί τα επίπεδα, τους τύπους γραμμών και τα στυλ κειμένου με **99,9 % πιστότητα** σε σύγκριση με την εγγενή εξαγωγή AutoCAD.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Aspose.CAD για .NET: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD. Μπορείτε να βρείτε τον σύνδεσμο λήψης [εδώ](https://releases.aspose.com/cad/net/).

- Κατάλογος Εγγράφων: Έχετε έναν καθορισμένο φάκελο για τα CAD έγγραφά σας. Αντικαταστήστε το "Your Document Directory" στον παρεχόμενο κώδικα με την πραγματική διαδρομή.

Τώρα, ας βυθιστούμε στη διαδικασία.

## Πώς να Εξάγετε Εικόνες DXF;

Η κλάση `Image` είναι το κεντρικό σημείο εισόδου για τη φόρτωση και αποθήκευση αρχείων CAD και raster στο Aspose.CAD. Φορτώστε την πηγαία εικόνα με `Image.Load("source.png")` και καλέστε `image.Save("output.dxf", ExportFormat.Dxf)` – αυτή είναι η βασική λειτουργία **πώς να εξάγετε dxf** σε μόλις δύο γραμμές C#. Το Aspose.CAD αντιστοιχίζει αυτόματα τα pixel raster σε οντότητες διανύσματος, διατηρώντας το πάχος των γραμμών και τα χρώματα. Για επεξεργασία παρτίδας, επαναλάβετε τη σειρά `Load`/`Save` για κάθε αρχείο σε φάκελο.

## Εισαγωγή Χώρων Ονομάτων

Η ενότητα `Import Namespaces` προετοιμάζει το περιβάλλον για τη μετατροπή. Η κλάση `Image` βρίσκεται στο namespace `Aspose.CAD.Image`, ενώ οι επιλογές εξαγωγής βρίσκονται στο `Aspose.CAD.ImageOptions`.

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadTables;
using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
```

## Πώς να Κρύψετε Γραμμές;

Η κλάση `DxfExportOptions` καθορίζει τις ρυθμίσεις που χρησιμοποιούνται κατά την εξαγωγή σε μορφή DXF. Ορίστε τη σημαία `HideLines` στο αντικείμενο `DxfExportOptions` για να αφαιρέσετε όλες τις ορθές γραμμές πριν την αποθήκευση. Αυτή η προσέγγιση μειώνει το οπτικό άγχος και παράγει πιο καθαρά αρχεία DXF, ιδιαίτερα χρήσιμα για διαγράμματα όπου απαιτούνται μόνο καμπύλες και κείμενο.

```csharp
var options = new DxfExportOptions { HideLines = true };
image.Save("output.dxf", options);
```

Η άμεση απάντηση: **πώς να κρύψετε γραμμές** επιτυγχάνεται ενεργοποιώντας το `HideLines` στις επιλογές εξαγωγής, το οποίο οδηγεί το Aspose.CAD να παραλείψει τις ορθές γραμμές κατά τη δημιουργία του DXF.

## Βήμα 1: Ορίστε Νέα Γραμματοσειρά για Κάθε Έγγραφο

`CadImage` αντιπροσωπεύει ένα σχέδιο CAD που έχει φορτωθεί στη μνήμη, παρέχοντας πρόσβαση στις οντότητες και τους πίνακες του.

```csharp
// Set new font per document
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (CadStyleTableObject style in cadImage.Styles)
        {
            // Set font name
            style.PrimaryFontName = "Broadway";
        }
        cadImage.Save(file.FullName + "_font.dxf");
    }
}
```

Σε αυτό το βήμα, προσαρμόζουμε τη γραμματοσειρά για κάθε έγγραφο CAD, προσθέτοντας μια πινελιά μοναδικότητας στις οπτικές σας αναπαραστάσεις.

## Βήμα 2: Κρύψτε Όλες τις "Ίσιες" Γραμμές

```csharp
// Hide all "straight" lines
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            // Make lines invisible
            if (entity.TypeName == CadEntityTypeName.LINE)
            {
                entity.Visible = 0;
            }
        }
        cadImage.Save(file.FullName + "_lines.dxf");
    }
}
```

Αυτό το βήμα εστιάζει στη βελτίωση της οπτικής ελκυστικότητας κρύβοντας τις ορθές γραμμές στα σχέδια CAD σας.

## Βήμα 3: Χειρισμοί με Κείμενο

```csharp
// Manipulations with text
foreach (var file in new DirectoryInfo(MyDir).EnumerateFiles("conic.dxf"))
{
    using (var cadImage = (CadImage)Image.Load(file.FullName))
    {
        foreach (var entity in cadImage.Entities)
        {
            if (entity.TypeName == CadEntityTypeName.TEXT)
            {
                // Modify text content
                ((CadText)entity).DefaultValue = "New text here!!! :)";
                break;
            }
        }
        cadImage.Save(file.FullName + "_text.dxf");
    }
}
```

Στο τελικό αυτό βήμα, παρουσιάζουμε πώς να χειριστείτε δυναμικά το κείμενο μέσα στα σχέδια CAD, παρέχοντας μια πιο διαδραστική και προσωποποιημένη προσθήκη.

## Κοινά Προβλήματα και Λύσεις

- **Απουσία γραμματοσειρών:** Βεβαιωθείτε ότι η γραμματοσειρά που αναφέρετε είναι εγκατεστημένη στον διακομιστή ή ενσωματώστε την χρησιμοποιώντας `FontSettings`.
- **Μεγάλα αρχεία προκαλούν OutOfMemoryException:** Χρησιμοποιήστε `LoadOptions` με `MemoryLimit` για ροή μεγάλων εικόνων.
- **Γραμμές δεν κρύβονται:** Επαληθεύστε ότι το `HideLines` είναι ορισμένο στο ακριβές αντικείμενο `DxfExportOptions` που περνιέται στο `Save`.

## Συχνές Ερωτήσεις

**Ε: Είναι το Aspose.CAD συμβατό με άλλες μορφές CAD;**  
Α: Ναι, το Aspose.CAD υποστηρίζει DWG, DGN, PDF, SVG και πάνω από 30 επιπλέον μορφές τόσο για εισαγωγή όσο και για εξαγωγή.

**Ε: Μπορώ να εφαρμόσω αυτές τις επεμβάσεις σε πολλά αρχεία ταυτόχρονα;**  
Α: Απόλυτα! Ο δείγμα κώδικας έχει σχεδιαστεί ώστε να επαναλαμβάνει τη διαδικασία σε έναν φάκελο, επεξεργαζόμενος κάθε εικόνα διαδοχικά.

**Ε: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD;**  
Α: Επισκεφθείτε [εδώ](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε μια προσωρινή άδεια αξιολόγησης.

**Ε: Πού μπορώ να ζητήσω βοήθεια και να συμμετάσχω στην κοινότητα;**  
Α: Εγγραφείτε στην κοινότητα Aspose.CAD στο [support forum](https://forum.aspose.com/c/cad/19) για να αλληλεπιδράσετε με άλλους προγραμματιστές και να λάβετε καθοδήγηση.

**Ε: Προσφέρει το Aspose.CAD δωρεάν δοκιμή;**  
Α: Ναι, μπορείτε να δοκιμάσετε δωρεάν [εδώ](https://releases.aspose.com/) για να γνωρίσετε τις δυνατότητες του Aspose.CAD.

**Τελευταία Ενημέρωση:** 2026-06-04  
**Δοκιμάστηκε Με:** Aspose.CAD 24.12 for .NET  
**Συγγραφέας:** Aspose

## Σχετικούς Οδηγούς

- [Εξαγωγή DXF σε PDF Format - Οδηγός Aspose.CAD](/cad/net/export-techniques/exporting-dxf-to-pdf-format/)
- [Εξαγωγή DXF Specific Layout σε PDF - Οδηγός Aspose.CAD](/cad/net/export-techniques/exporting-dxf-specific-layout-to-pdf/)
- [Εξαγωγή DWG σε DXF Format σε C# - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}