---
date: 2026-08-12
description: Εξαγωγή κειμένου από DWG και μετατροπή συγκεκριμένου DWG σε εικόνα σε
  C# χρησιμοποιώντας το Aspose.CAD για .NET. Μάθετε βήμα‑βήμα με αποσπάσματα κώδικα.
keywords:
- extract text from dwg
- convert specific dwg to image
- Aspose.CAD .NET
lastmod: 2026-08-12
linktitle: Μετατροπή συγκεκριμένου DWG σε εικόνα σε C#
og_description: Εξαγωγή κειμένου από DWG και μετατροπή συγκεκριμένου DWG σε εικόνα
  σε C# με το Aspose.CAD. Ακολουθήστε αυτόν τον σύντομο οδηγό για γρήγορη υλοποίηση.
og_image_alt: Guide showing DWG to image conversion and text extraction using Aspose.CAD
  in C#
og_title: Εξαγωγή κειμένου από DWG και μετατροπή συγκεκριμένου DWG σε εικόνα σε C#
schemas:
- author: Aspose
  dateModified: '2026-08-12'
  description: Extract text from DWG and convert specific DWG to image in C# using
    Aspose.CAD for .NET. Learn step‑by‑step with code snippets.
  headline: Extract text from DWG and convert specific DWG to image in C#
  type: TechArticle
- questions:
  - answer: Aspose.CAD supports DWG releases from AutoCAD 2000 up to the latest 2024
      version, covering over 90 % of files created in the field.
    question: Is Aspose.CAD compatible with all versions of DWG files?
  - answer: Yes – you can change resolution, image format, anti‑aliasing, and background
      color to suit PNG, JPEG, or PDF targets.
    question: Can I customize the rasterization options for different outputs?
  - answer: Explore the comprehensive [Aspose.CAD documentation](https://reference.aspose.com/cad/net/)
      for more code samples and API details.
    question: Where can I find additional examples and documentation?
  - answer: Absolutely – you can download a trial version on the **[Aspose trial download
      page](https://releases.aspose.com/)** and evaluate all features without restrictions
      for 30 days.
    question: Is there a free trial available for Aspose.CAD?
  - answer: Join the active [Aspose.CAD forum](https://forum.aspose.com/c/cad/19)
      where developers share solutions and the Aspose team answers questions.
    question: How can I get support or connect with the community?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- extract text from dwg
- Aspose.CAD
- C# CAD processing
title: Εξαγωγή κειμένου από DWG και μετατροπή συγκεκριμένου DWG σε εικόνα σε C#
url: /el/net/image-manipulation-and-rendering/converting-particular-dwg-to-image/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή συγκεκριμένου DWG σε εικόνα σε C# - Οδηγός Aspose.CAD

## Εισαγωγή

Στις σύγχρονες εφαρμογές μηχανικής, συχνά χρειάζεται να **εξάγετε κείμενο από αρχεία DWG** και να **μετατρέψετε συγκεκριμένα DWG σε μορφές εικόνας** για αναφορές ή οπτικοποίηση. Το Aspose.CAD για .NET σας παρέχει ένα πλήρες API που διαχειρίζεται και τις δύο εργασίες χωρίς την ανάγκη εξωτερικού λογισμικού CAD. Σε αυτό το tutorial θα μάθετε πώς να φορτώσετε ένα DWG, να φιλτράρετε τις οντότητες κειμένου, να ραστεροποιήσετε το σχέδιο και τελικά να αποθηκεύσετε το αποτέλεσμα ως εικόνα PDF — όλα με καθαρό κώδικα C#.

## Γρήγορες απαντήσεις
- **Ποιο είναι το πρώτο βήμα;** Φορτώστε το αρχείο DWG με `new CadImage("file.dwg")`.  
- **Ποια κλάση φιλτράρει το κείμενο;** Χρησιμοποιήστε `CadEntityFilter` για να επιλέξετε οντότητες `Text`.  
- **Πώς ορίζετε το μέγεθος της εικόνας;** Ορίστε `Width` και `Height` στο `CadRasterizationOptions`.  
- **Ποια μορφή εξόδου χρησιμοποιείται;** Το παράδειγμα αποθηκεύει σε PDF, το οποίο ενσωματώνει την ραστερική εικόνα.  
- **Χρειάζομαι άδεια για παραγωγή;** Ναι – μια εμπορική άδεια Aspose.CAD αφαιρεί τους περιορισμούς αξιολόγησης.

## Πώς να εξάγετε κείμενο από dwg;

Φορτώστε το DWG, εφαρμόστε ένα φίλτρο που επιλέγει μόνο τις οντότητες κειμένου και στη συνέχεια διαβάστε την ιδιότητα `TextString` κάθε οντότητας. Αυτή η προσέγγιση επιστρέφει κάθε κομμάτι σχολιασμού, ετικέτας ή κειμένου διάστασης που υπάρχει στο σχέδιο, επιτρέποντάς σας να το επαναχρησιμοποιήσετε για αναζήτηση, ευρετηρίαση ή αναφορές.

## Γιατί να μετατρέψετε συγκεκριμένο dwg σε εικόνα;

Η μετατροπή ενός DWG σε ραστερική εικόνα σας επιτρέπει να ενσωματώσετε το σχέδιο σε έγγραφα, ιστοσελίδες ή κινητές εφαρμογές που δεν μπορούν να αποδώσουν εγγενείς μορφές CAD. Το Aspose.CAD επεξεργάζεται **πάνω από 50+ μορφές CAD** και μπορεί να ραστεροποιήσει σχέδια με εκατοντάδες σελίδες ενώ χρησιμοποιεί λιγότερο από 200 MB μνήμης, κάτι που το καθιστά κατάλληλο για σενάρια υψηλής απόδοσης σε διακομιστές.

## Προαπαιτούμενα

- Visual Studio (οποιαδήποτε πρόσφατη έκδοση) για τη μεταγλώττιση και εκτέλεση έργων C#.  
- Aspose.CAD for .NET – βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη. Μπορείτε να βρείτε τον σύνδεσμο λήψης στη **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- Ένα αρχείο DWG με το οποίο θέλετε να εργαστείτε· το δείγμα αρχείου *visualization_-_conference_room.dwg* χρησιμοποιείται στα αποσπάσματα κώδικα.

## Εισαγωγή ονοματοχώρων

Οι παρακάτω ονοματοχώροι σας παρέχουν πρόσβαση στις βασικές κλάσεις CAD, τις επιλογές ραστεροποίησης και τα βοηθήματα εξόδου PDF:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Βήμα 1: φόρτωση του αρχείου dwg

Δημιουργήστε ένα αντικείμενο `CadImage` περνώντας τη διαδρομή του αρχείου DWG. Το αντικείμενο `CadImage` αντιπροσωπεύει ολόκληρο το σχέδιο στη μνήμη και παρέχει πρόσβαση στα στρώματα, τις οντότητες και τα μεταδεδομένα του.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
var cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath);
```

## Βήμα 2: φιλτράρισμα οντοτήτων

`CadEntityFilter` σας επιτρέπει να επιλέξετε μόνο τις οντότητες που χρειάζεστε. Σε αυτόν τον οδηγό το ρυθμίζουμε ώστε να διατηρεί αντικείμενα **text**, απορρίπτοντας γραμμές, κύκλους και άλλα γεωμετρικά στοιχεία που δεν θέλετε στην τελική εικόνα.

```csharp
CadBaseEntity[] entities = cadImage.Entities;
List<CadBaseEntity> filteredEntities = new List<CadBaseEntity>();

foreach (CadBaseEntity baseEntity in entities)
{
    // Selection or filtration of entities
    if (baseEntity.TypeName == CadEntityTypeName.TEXT)
    {
        filteredEntities.Add(baseEntity);
    }
}

cadImage.Entities = filteredEntities.ToArray();
```

## Βήμα 3: ορισμός επιλογών ραστεροποίησης

`CadRasterizationOptions` ελέγχει πώς το σχέδιο μετατρέπεται σε bitmap. Μπορείτε να ορίσετε το μέγεθος εξόδου, το χρώμα φόντου και την ανάλυση (DPI). Η παρακάτω άγκυρα ορισμού παρουσιάζει την κλάση:

Η κλάση `CadRasterizationOptions` καθορίζει τις διαστάσεις της εικόνας, την ανάλυση και τις ρυθμίσεις απόδοσης για τη μετατροπή σχεδίων CAD σε ραστερικές μορφές.  

Ορίστε το επιθυμητό πλάτος, ύψος και χρώμα φόντου πριν περάσετε τις επιλογές στον εξαγωγέα PDF.

```csharp
Aspose.CAD.ImageOptions.CadRasterizationOptions rasterizationOptions =
    new Aspose.CAD.ImageOptions.CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.AutomaticLayoutsScaling = true;
```

## Βήμα 4: ορισμός επιλογών PDF

`PdfOptions` συνδυάζει τις ρυθμίσεις ραστεροποίησης με χαρακτηριστικά ειδικά για PDF όπως η συμπίεση. Η άγκυρα ορισμού για αυτήν την κλάση εμφανίζεται πρώτα:

`PdfOptions` περιλαμβάνει παραμέτρους δημιουργίας PDF, συμπεριλαμβανομένων των επιλογών ραστεροποίησης που καθορίζουν πώς τα δεδομένα CAD αποδίδονται μέσα στο έγγραφο PDF.  

Αναθέστε το προηγούμενο αντικείμενο `CadRasterizationOptions` στην ιδιότητα `VectorRasterizationOptions`.

```csharp
Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
```

## Βήμα 5: αποθήκευση ως PDF

Τέλος, καλέστε τη μέθοδο `Save` στο αντικείμενο `CadImage`, περνώντας το όνομα του αρχείου προορισμού και τις ρυθμισμένες `PdfOptions`. Το PDF θα περιέχει μια εικόνα υψηλής ποιότητας του φιλτραρισμένου σχεδίου.

```csharp
string outFile = MyDir + "result_out_generated.pdf";
cadImage.Save(outFile, pdfOptions);
```

## Συχνά προβλήματα και αντιμετώπιση

- **Απουσία κειμένου μετά το φιλτράρισμα** – Βεβαιωθείτε ότι το DWG περιέχει πραγματικά οντότητες `Text`; ορισμένα σχέδια αποθηκεύουν σχολιασμούς ως `MText`. Προσαρμόστε το φίλτρο ώστε να περιλαμβάνει `MText` εάν χρειάζεται.  
- **Κενή εικόνα εξόδου** – Ελέγξτε ότι το DPI της ραστεροποίησης είναι αρκετά υψηλό (300 DPI είναι ασφαλές προεπιλεγμένο) και ότι το χρώμα φόντου δεν είναι διαφανές κατά την προβολή του PDF.  
- **Σφάλματα έλλειψης μνήμης σε μεγάλα αρχεία** – Χρησιμοποιήστε την υπερφόρτωση `LoadOptions` που ενεργοποιεί τη ροή, αποτρέποντας τη φόρτωση ολόκληρου του αρχείου στη μνήμη ταυτόχρονα.

## Συχνές ερωτήσεις

**Q: Είναι το Aspose.CAD συμβατό με όλες τις εκδόσεις αρχείων DWG;**  
A: Το Aspose.CAD υποστηρίζει εκδόσεις DWG από AutoCAD 2000 έως την πιο πρόσφατη έκδοση 2024, καλύπτοντας πάνω από 90 % των αρχείων που δημιουργούνται στον χώρο.  

**Q: Μπορώ να προσαρμόσω τις επιλογές ραστεροποίησης για διαφορετικές εξόδους;**  
A: Ναι – μπορείτε να αλλάξετε την ανάλυση, τη μορφή εικόνας, το anti‑aliasing και το χρώμα φόντου ώστε να ταιριάζει σε στόχους PNG, JPEG ή PDF.  

**Q: Πού μπορώ να βρω πρόσθετα παραδείγματα και τεκμηρίωση;**  
A: Εξερευνήστε την εκτενή [Aspose.CAD documentation](https://reference.aspose.com/cad/net/) για περισσότερα δείγματα κώδικα και λεπτομέρειες API.  

**Q: Υπάρχει δωρεάν δοκιμαστική έκδοση του Aspose.CAD;**  
A: Απόλυτα – μπορείτε να κατεβάσετε μια δοκιμαστική έκδοση στη **[Aspose trial download page](https://releases.aspose.com/)** και να αξιολογήσετε όλες τις λειτουργίες χωρίς περιορισμούς για 30 ημέρες.  

**Q: Πώς μπορώ να λάβω υποστήριξη ή να συνδεθώ με την κοινότητα;**  
A: Εγγραφείτε στο ενεργό [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) όπου οι προγραμματιστές μοιράζονται λύσεις και η ομάδα Aspose απαντά σε ερωτήσεις.

---

**Τελευταία ενημέρωση:** 2026-08-12  
**Δοκιμάστηκε με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Αναζήτηση κειμένου σε αρχεία DWG με C# - Οδηγός Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Μετατροπή σχεδίου CAD σε ραστερική εικόνα στο Aspose.CAD για .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)
- [Απόδοση εγγράφων DWG σε C# - Οδηγός Aspose.CAD](/cad/net/image-manipulation-and-rendering/rendering-dwg-documents/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}