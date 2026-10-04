---
date: 2026-10-04
description: Μάθετε πώς να αναζητήσετε κείμενο σε αρχεία DWG χρησιμοποιώντας C# και
  Aspose.CAD για .NET. Εξάγετε κείμενο, διαβάστε αρχεία DWG και ενισχύστε τις εφαρμογές
  CAD σας.
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Αναζήτηση κειμένου και διαχείριση
og_description: Αναζήτηση κειμένου σε αρχεία DWG χρησιμοποιώντας C# και Aspose.CAD
  για .NET. Εξάγετε κείμενο, διαβάστε αρχεία DWG και βελτιώστε την απόδοση των εφαρμογών
  CAD.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Αναζήτηση κειμένου σε αρχεία DWG με C# χρησιμοποιώντας το Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Αναζήτηση κειμένου σε αρχεία DWG με C# χρησιμοποιώντας το Aspose.CAD
url: /el/net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αναζήτηση κειμένου σε αρχεία DWG με C# χρησιμοποιώντας το Aspose.CAD

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **search text in DWG** αρχεία με C# χρησιμοποιώντας τη δυνατή βιβλιοθήκη Aspose.CAD για .NET. Είτε χρειάζεστε να εντοπίσετε σημειώσεις, να εξάγετε τιμές χαρακτηριστικών ή να δημιουργήσετε ένα ευρετήριο αναζήτησης, τα παρακάτω βήματα θα σας καθοδηγήσουν σε μια αξιόπιστη, υψηλής απόδοσης λύση που λειτουργεί τόσο στο .NET Framework όσο και στο .NET Core.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την αναζήτηση κειμένου DWG;** Aspose.CAD for .NET.
- **Μπορώ να εξάγω κείμενο από DWG;** Ναι – το API επιστρέφει αλφαριθμητικές συμβολοσειρές plain‑text για κάθε εντοπισμένο αντικείμενο.
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν προσωρινή άδεια λειτουργεί για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.
- **Η λειτουργία είναι αποδοτική στη μνήμη;** Ναι, το Aspose.CAD επεξεργάζεται τα αρχεία ροή‑wise, επιτρέποντας τη διαχείριση DWG με εκατοντάδες σελίδες χωρίς να φορτώνεται ολόκληρο το αρχείο στη μνήμη RAM.

## Τι είναι η αναζήτηση κειμένου σε DWG;

CadImage είναι το αντικείμενο του Aspose.CAD που αντιπροσωπεύει ένα φορτωμένο σχέδιο CAD, εκθέτοντας τις οντότητές του όπως τα τμήματα κειμένου.  
Το TextFragment αντιπροσωπεύει ένα μεμονωμένο κομμάτι εξαγόμενου κειμένου, συμπεριλαμβανομένου του περιεχομένου και της γεωμετρικής του θέσης.

Η φράση *search text in DWG* αναφέρεται στην προγραμματική εντόπιση δεδομένων συμβολοσειράς—όπως ονόματα επιπέδων, τιμές χαρακτηριστικών ή κείμενο σημειώσεων—μέσα σε αρχείο σχεδίου DWG. Το Aspose.CAD εκθέτει αυτή τη δυνατότητα μέσω του αντικειμένου `CadImage` και της συλλογής `TextFragment`, επιτρέποντας στους προγραμματιστές να ανακτούν και να διαχειρίζονται το κείμενο αποδοτικά.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για την αναζήτηση κειμένου DWG;

Το Aspose.CAD υποστηρίζει **30+ μορφές CAD και BIM** (συμπεριλαμβανομένων DWG, DXF, DGN, DWF) και μπορεί να επεξεργαστεί αρχεία έως **500 MB** χωρίς πλήρη φόρτωση στη μνήμη. Η βιβλιοθήκη εγγυάται **99 % ακρίβεια εξαγωγής κειμένου** σε σύνθετα σχέδια, κάτι που αποτελεί ποσοτική βελτίωση σε σχέση με πολλούς ανοιχτού κώδικα αναλυτές που συχνά παραλείπουν ενσωματωμένα MTEXT ή χαρακτηριστικά μπλοκ.

## Πώς να αναζητήσετε κείμενο σε αρχεία DWG με C#;

Το Image.Load είναι μια στατική μέθοδος που διαβάζει ένα αρχείο CAD και επιστρέφει μια παρουσία CadImage.

Φορτώστε το DWG χρησιμοποιώντας το `Image.Load`, ανακτήστε τη συλλογή `TextFragments` και φιλτράρετε την με LINQ βάσει του όρου αναζήτησης. Αυτό το σύντομο μοτίβο εκτελείται σε γραμμικό χρόνο σε σχέση με τον αριθμό των οντοτήτων κειμένου, δεν απαιτεί πρόσθετες βιβλιοθήκες και λειτουργεί σταθερά σε περιβάλλοντα .NET Framework και .NET Core.

### Βήμα 1: εγκαταστήστε το πακέτο NuGet Aspose.CAD
Ανοίξτε την κονσόλα του NuGet Package Manager και εκτελέστε:

```
Install-Package Aspose.CAD
```

Αυτό προσθέτει τα απαιτούμενα assemblies και ενημερώνει το αρχείο έργου σας.

### Βήμα 2: ανοίξτε το αρχείο DWG
Δημιουργήστε μια παρουσία `CadImage` καλώντας το `Image.Load`. Η μέθοδος εντοπίζει αυτόματα τη μορφή του αρχείου και προετοιμάζει μια αναπαράσταση στη μνήμη.

### Βήμα 3: απαριθμήστε τα τμήματα κειμένου
`image.TextFragments` επιστρέφει μια συλλογή αντικειμένων `TextFragment`, το καθένα εκθέτει τα `Text`, `Location`, `Height` και `LayerName`. Μπορείτε να επαναλάβετε ή να φιλτράρετε τη συλλογή με LINQ.

### Βήμα 4: εφαρμόστε τα κριτήρια αναζήτησής σας
Χρησιμοποιήστε `String.Contains`, `Regex.IsMatch` ή οποιοδήποτε προσαρμοσμένο πρότυπο για να εντοπίσετε το ακριβές κείμενο που χρειάζεστε. Για αναζητήσεις χωρίς διάκριση πεζών‑κεφαλαίων, καλέστε `ToLowerInvariant()` και στις δύο πλευρές.

### Βήμα 5: διαχειριστείτε τα αποτελέσματα
Τυπικές ενέργειες περιλαμβάνουν την καταγραφή των συντεταγμένων του τμήματος, την εξαγωγή σε CSV ή την επισήμανση της οντότητας σε προβολέα. Επειδή το API σας παρέχει την ακριβή `Location`, μπορείτε να το περάσετε σε οποιοδήποτε επόμενο στοιχείο οπτικοποίησης CAD.

## Πώς να εξάγετε κείμενο από DWG;

Το TextFragment είναι το αντικείμενο που κρατά το εξαγόμενο κείμενο και τα συναφή μεταδεδομένα όπως θέση και επίπεδο.

Η εξαγωγή κειμένου είναι παρόμοια με την αναζήτηση· απλώς απαριθμήστε τη συλλογή `TextFragment` και διαβάστε την ιδιότητα `TextFragment.Text` για κάθε αντικείμενο. Μπορείτε να συνενώσετε τις συμβολοσειρές σε ένα ενιαίο έγγραφο, να τις γράψετε σε αρχείο CSV ή να τις περάσετε σε ευρετήριο αναζήτησης για γρήγορη ανάκτηση σε πολλαπλά σχέδια.

## Συνηθισμένα προβλήματα και αντιμετώπιση σφαλμάτων
- **Missing MTEXT:** Ορισμένες παλαιότερες εκδόσεις DWG αποθηκεύουν κείμενο πολλών γραμμών σε χαρακτηριστικά μπλοκ. Βεβαιωθείτε ότι ελέγχετε επίσης το `image.Blocks` για αντικείμενα `Attribute`.
- **Encoding issues:** Τα αρχεία DWG μπορεί να χρησιμοποιούν μη‑Unicode κωδικοσελίδες. Ορίστε το `image.LoadOptions.Encoding` στην κατάλληλη `System.Text.Encoding` πριν τη φόρτωση.
- **Large files:** Για αρχεία μεγαλύτερα από 200 MB, ενεργοποιήστε το `image.LoadOptions.Streaming = true` για να διατηρήσετε τη χρήση μνήμης κάτω από 100 MB.

## Συχνές ερωτήσεις

**Q: Μπορώ να αναζητήσω κείμενο σε DWG αρχεία προστατευμένα με κωδικό;**  
A: Ναι. Παρέχετε τον κωδικό μέσω `CadLoadOptions.Password` όταν καλείτε το `Image.Load`.

**Q: Υποστηρίζει το API την αναζήτηση σε πολλαπλά DWG αρχεία ταυτόχρονα;**  
A: Απόλυτα. Επανάληψη μέσω ενός καταλόγου, φόρτωση κάθε αρχείου και επαναχρησιμοποίηση του ίδιου φίλτρου LINQ – η βιβλιοθήκη είναι thread‑safe για παράλληλη επεξεργασία.

**Q: Πόσο ακριβής είναι η εξαγωγή κειμένου για σύνθετες σημειώσεις;**  
A: Το Aspose.CAD αναφέρει **99 % ποσοστό επιτυχίας** σε σύνολα δοκιμών βιομηχανικού προτύπου, διαχειριζόμενο MTEXT, ορισμούς χαρακτηριστικών και ακόμη και ενσωματωμένους χαρακτήρες Unicode.

**Q: Υπάρχει τρόπος να επισημάνετε το βρεθέν κείμενο σε προβολέα;**  
A: Αφού λάβετε το `Location` κάθε `TextFragment`, μπορείτε να σχεδιάσετε μια προσωρινή επικάλυψη χρησιμοποιώντας οποιονδήποτε προβολέα CAD που δέχεται γεωμετρικές πρωτότυπες.

**Q: Ποιο μοντέλο αδειοδότησης ισχύει για το Aspose.CAD;**  
A: Το προϊόν χρησιμοποιεί μοντέλο αδειοδότησης ανά προγραμματιστή ή ανά διακομιστή· μια δωρεάν άδεια αξιολόγησης είναι διαθέσιμη για 30 ημέρες.

---

**Τελευταία ενημέρωση:** 2026-10-04  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

## Μαθήματα αναζήτησης και επεξεργασίας κειμένου
### [Αναζήτηση κειμένου σε αρχεία DWG με C# - Μαθήματα Aspose.CAD](./searching-text-in-dwg-files/)

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Σχετικά μαθήματα

- [Μετατροπή DWG σε PDF και προσθήκη κειμένου σε C# – Μαθήματα Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Πώς να μετατρέψετε DWG σε PDF και εικόνες raster χρησιμοποιώντας το Aspose.CAD για .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Πώς να αποδώσετε CAD και να μετατρέψετε DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}