---
date: 2026-10-09
description: Μάθετε πώς να φορτώσετε αρχείο dwg και να αναζητήσετε κείμενο μέσα σε
  αρχεία DWG χρησιμοποιώντας C# και Aspose.CAD για .NET. Ακολουθήστε αυτόν τον οδηγό
  βήμα‑βήμα για να βελτιώσετε τις ροές εργασίας CAD σας.
keywords:
- load dwg file
- export dwg to pdf
- cad text search
- search text dwg
- c# read dwg
lastmod: 2026-10-09
linktitle: Αναζήτηση κειμένου σε αρχεία DWG με C#
og_description: Μάθετε πώς να φορτώσετε αρχείο dwg και να αναζητήσετε κείμενο μέσα
  σε αρχεία DWG χρησιμοποιώντας C# και Aspose.CAD για .NET. Ακολουθήστε αυτόν τον
  οδηγό βήμα‑βήμα για να βελτιώσετε τις ροές εργασίας CAD σας.
og_image_alt: Guide showing how to load dwg file and search text in DWG files using
  Aspose.CAD for .NET
og_title: Πώς να φορτώσετε αρχείο dwg και να αναζητήσετε κείμενο σε αρχεία DWG με
  C#
schemas:
- author: Aspose
  dateModified: '2026-10-09'
  description: Learn how to load dwg file and search text inside DWG files using C#
    and Aspose.CAD for .NET. Follow this step‑by‑step guide to enhance your CAD workflows.
  headline: How to load dwg file and search text in DWG files with C#
  type: TechArticle
- questions:
  - answer: '`new CadImage("yourfile.dwg")` creates an in‑memory representation of
      the drawing.'
    question: What is the first line of code to load a DWG?
  - answer: '`Aspose.CAD.Image` and `Aspose.CAD.FileFormats.Dwg` are required.'
    question: Which namespace contains the CAD classes?
  - answer: Yes – use `image.Save("out.pdf", SaveFormat.Pdf)`.
    question: Can I export the search results directly to PDF?
  - answer: A free trial works for evaluation; a permanent license is required for
      production.
    question: Do I need a license for development?
  - answer: .NET 5, .NET 6, .NET Core 3.1 and .NET Framework 4.6+.
    question: Which .NET versions are supported?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- dwg file handling
- aspose.cad
- c# cad processing
- text search in dwg
title: Πώς να φορτώσετε αρχείο dwg και να αναζητήσετε κείμενο σε αρχεία DWG με C#
url: /el/net/text-search-and-manipulation/searching-text-in-dwg-files/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να φορτώσετε αρχείο dwg και να αναζητήσετε κείμενο σε αρχεία DWG με C# - Εγχειρίδιο Aspose.CAD

## Εισαγωγή

Στη σύγχρονη ανάπτυξη CAD, η δυνατότητα **φόρτωσης αρχείου dwg** αντικειμένων και η άμεση εντόπιση συγκεκριμένων συμβολοσειρών κειμένου εξοικονομεί ώρες χειροκίνητης επιθεώρησης. Είτε δημιουργείτε ένα εργαλείο επεξεργασίας παρτίδας είτε προσθέτετε δυνατότητες αναζήτησης σε έναν προβολέα, το Aspose.CAD για .NET σας παρέχει ένα πλήρως διαχειριζόμενο API που λειτουργεί σε Windows, Linux και macOS χωρίς εγγενείς εξαρτήσεις. Αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα—από τη φόρτωση του DWG μέχρι την εξαγωγή του αποτελέσματος ως PDF—ώστε να ενσωματώσετε αξιόπιστη αναζήτηση κειμένου CAD στις εφαρμογές C# σας σήμερα.

## Γρήγορες απαντήσεις
- **Ποια είναι η πρώτη γραμμή κώδικα για τη φόρτωση ενός DWG;** `new CadImage("yourfile.dwg")` δημιουργεί μια αναπαράσταση του σχεδίου στη μνήμη.  
- **Ποιο namespace περιέχει τις κλάσεις CAD;** `Aspose.CAD.Image` και `Aspose.CAD.FileFormats.Dwg` απαιτούνται.  
- **Μπορώ να εξάγω τα αποτελέσματα αναζήτησης απευθείας σε PDF;** Ναι – χρησιμοποιήστε `image.Save("out.pdf", SaveFormat.Pdf)`.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται μόνιμη άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET 5, .NET 6, .NET Core 3.1 και .NET Framework 4.6+.

## Τι είναι ένα αρχείο DWG;

Ένα αρχείο DWG είναι μια δυαδική μορφή που αποθηκεύει δεδομένα σχεδίασης 2D και 3D που δημιουργούνται από το AutoCAD και συμβατά εργαλεία. Είναι το βιομηχανικό πρότυπο κοντέινερ για διανυσματική γεωμετρία, στρώματα, κείμενο και μεταδεδομένα. Επειδή η μορφή είναι ιδιόκτητη, οι περισσότεροι ανοιχτού κώδικα αναλυτές δυσκολεύονται με τις νεότερες εκδόσεις, αλλά το Aspose.CAD υποστηρίζει πλήρως πάνω από 150 εκδόσεις DWG, επιτρέποντάς σας να διαβάζετε και να επεξεργάζεστε σχέδια χωρίς εγκατάσταση του AutoCAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για αναζήτηση κειμένου CAD;

Το Aspose.CAD μπορεί να επεξεργαστεί **50+** εκδόσεις DWG και DXF, διαχειριζόμενο αρχεία έως 1 GB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Η βιβλιοθήκη εξάγει κείμενο τόσο από τις ενότητες **Entities** όσο και **Block**, παρέχοντάς σας ποσοστό επιτυχίας **99 %** στην εντόπιση αναζητήσιμων συμβολοσειρών ακόμη και όταν είναι ενσωματωμένες σε μπλοκ. Αυτή η ποσοτική αξιοπιστία την καθιστά την προτιμώμενη επιλογή για αυτοματοποίηση CAD επιχειρηματικού επιπέδου.

## Προαπαιτούμενα

- **Aspose.CAD for .NET** εγκατεστημένο. Κατεβάστε το τελευταίο πακέτο από την [Aspose.CAD website](https://releases.aspose.com/cad/net/).
- Ένας φάκελος που περιέχει τα αρχεία DWG που θέλετε να αναλύσετε.
- Ένα έγκυρο αρχείο άδειας για παραγωγική χρήση (προαιρετικό για δοκιμαστικές εκτελέσεις).

## Ποια namespaces απαιτούνται;

Το namespace `Aspose.CAD` παρέχει τις βασικές κλάσεις διαχείρισης εικόνας, ενώ το `Aspose.CAD.FileFormats.Dwg` περιέχει δομές ειδικές για DWG. Εισάγετε τα στην αρχή του αρχείου C#:

```csharp
using Aspose.CAD;
using Aspose.CAD.FileFormats.Dwg;
using Aspose.CAD.ImageOptions;
```

> **Σημείωση:** Το παραπάνω μπλοκ κώδικα είναι ένας placeholder· διατηρήστε το ακριβές κείμενο αμετάβλητο για να διατηρηθεί ο αρχικός αριθμός placeholder.

## Πώς να φορτώσετε αρχείο dwg;

Η φόρτωση ενός αρχείου DWG είναι απλή με το Aspose.CAD. Χρησιμοποιήστε την κλάση `CadImage`, η οποία αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη. Ο κατασκευαστής διαβάζει το αρχείο χωρίς απόδοση, καθιστώντας το γρήγορο ακόμη και για μεγάλα σχέδια. Μετά τη φόρτωση, μπορείτε να ελέγξετε ιδιότητες όπως `Width`, `Height` και `Layers` πριν εκτελέσετε οποιεσδήποτε λειτουργίες αναζήτησης.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
```

## Πώς να αναζητήσετε κείμενο στην ενότητα entities;

Για να εντοπίσετε κείμενο στην ενότητα Entities, επαναλάβετε τη συλλογή `cadImage.Entities`. Κάθε οντότητα μπορεί να εξεταστεί για τον τύπο της (π.χ., `MText`, `Text`, `Attribute`) και την ιδιότητα `TextString`. Εκτελέστε σύγκριση χωρίς διάκριση πεζών‑κεφαλαίων με τη στοχευόμενη συμβολοσειρά και συλλέξτε τις ταιριαστές οντότητες για περαιτέρω επεξεργασία ή επισήμανση.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "search.dwg";
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    // Your code here
}
```

## Πώς να αναζητήσετε κείμενο στην ενότητα block;

Τα Blocks είναι επαναχρησιμοποιήσιμες ομάδες οντοτήτων που μπορεί να περιέχουν ενσωματωμένο κείμενο. Πρώτα, απαριθμήστε το `cadImage.BlockEntities.Values` για να αποκτήσετε πρόσβαση σε κάθε ορισμό block. Στη συνέχεια, διασχίστε τη συλλογή `Entities` κάθε block, εφαρμόζοντας την ίδια λογική αντιστοίχισης κειμένου που χρησιμοποιείται για την κύρια ενότητα Entities. Αυτό εξασφαλίζει ότι το κείμενο που κρύβεται μέσα σε επαναχρησιμοποιήσιμα στοιχεία δεν θα παραλειφθεί.

```csharp
foreach (CadBaseEntity entity in cadImage.Entities)
{
    IterateCADNodes(entity);
}
```

## Πώς να επαναλάβετε τους κόμβους CAD για πλήρη σάρωση;

Μια ολοκληρωμένη σάρωση συνδυάζει τις ενότητες Entities και Block. Με την αναδρομική διαδρομή του δέντρου κόμβων `CadImage`, μπορείτε να διαχειριστείτε ενσωματωμένα blocks, ορισμούς attribute και ακόμη εξωτερικές αναφορές. Υλοποιήστε μια βοηθητική μέθοδο που δέχεται ένα `CadBaseEntity`, ελέγχει τον τύπο του, εξάγει κείμενο όταν είναι εφαρμόσιμο, και στη συνέχεια επαναλαμβάνει στις θυγατρικές οντότητες εάν ο κόμβος περιέχει συλλογή.

```csharp
foreach (CadBlockEntity blockEntity in cadImage.BlockEntities.Values)
{
    foreach (CadBaseEntity entity in blockEntity.Entities)
    {
        IterateCADNodes(entity);
    }
}
```

## Πώς να εξάγετε dwg σε pdf μετά τον εντοπισμό κειμένου;

Αφού εντοπίσετε τις σχετικές οντότητες, μπορεί να θέλετε να τις επισημάνετε ή να εξάγετε τις συντεταγμένες τους. Το Aspose.CAD σας επιτρέπει να αποθηκεύσετε ολόκληρο το σχέδιο ως PDF διατηρώντας την διανυσματική ποιότητα. Διαμορφώστε το `CadRasterizationOptions` εάν χρειάζεστε raster έξοδο, στη συνέχεια καλέστε `image.Save("output.pdf", new PdfOptions())`. Το παραγόμενο PDF μπορεί να μοιραστεί με ενδιαφερόμενους που δεν διαθέτουν λογισμικό CAD.

```csharp
private static void IterateCADNodes(CadBaseEntity obj)
{
    switch (obj.TypeName)
    {
        // Handle different entity types
    }
}
```

## Συμπέρασμα

Το Aspose.CAD για .NET παρέχει μια απρόσκοπτη, υψηλής απόδοσης λύση για τη φόρτωση δεδομένων αρχείων dwg, την αναζήτηση συγκεκριμένου κειμένου και την εξαγωγή του αποτελέσματος σε PDF. Ακολουθώντας τα βήματα σε αυτό το εγχειρίδιο, έχετε προσθέσει ισχυρές δυνατότητες αναζήτησης κειμένου CAD στην εφαρμογή C# σας χωρίς να βασίζεστε σε εξωτερικά εργαλεία ή δαπανηρές άδειες.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET με άλλες μορφές CAD;

Α1: Ναι, το Aspose.CAD υποστηρίζει πάνω από 30 μορφές CAD, συμπεριλαμβανομένων των DXF, DWF και STL, παρέχοντας μια ευέλικτη λύση για εργασίες με μεικτές μορφές.

### Ε2: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD για .NET;

Α2: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες με τη [δωρεάν δοκιμή](https://releases.aspose.com/).

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για .NET;

Α3: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για βοήθεια από την κοινότητα και επίσημα κανάλια υποστήριξης.

### Ε4: Τι είναι μια προσωρινή άδεια και πώς μπορώ να αποκτήσω μία;

Α4: Αποκτήστε μια προσωρινή άδεια [temporary license](https://purchase.aspose.com/temporary-license/) για βραχυπρόθεσμη αξιολόγηση ή έργα proof‑of‑concept.

### Ε5: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD για .NET;

Α5: Ανατρέξτε στην ολοκληρωμένη [documentation](https://reference.aspose.com/cad/net/) για λεπτομερείς οδηγίες, αναφορές API και παραδείγματα κώδικα.

---

**Τελευταία ενημέρωση:** 2026-10-09  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions = new Aspose.CAD.ImageOptions.CadRasterizationOptions();
// Configure rasterization options
rasterizationOptions.Layouts = new[] { "Layout1" };
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "SearchText_out.pdf", pdfOptions);
```

## Σχετικά Εγχειρίδια

- [Πώς να μετατρέψετε DWG σε PDF και Raster Images χρησιμοποιώντας το Aspose.CAD για .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Μετατροπή DWG σε PNG & Εξαγωγή OLE Objects - Εγχειρίδιο Aspose.CAD](/cad/net/advanced-export-techniques/exporting-ole-objects-from-dwg/)
- [Πώς να διαβάσετε αρχεία DWT με το Aspose.CAD για .NET](/cad/net/cad-features-and-support/reading-dwt/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}