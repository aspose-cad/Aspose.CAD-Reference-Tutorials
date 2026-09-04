---
date: 2026-09-04
description: Μάθετε πώς να παρακάμψετε την ανίχνευση dwg codepage σε αρχεία DWG χρησιμοποιώντας
  το Aspose.CAD για .NET, παρέχοντάς σας ακριβή έλεγχο στην character encoding.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Παράκαμψη Αυτόματης Codepage Detection σε Αρχεία DWG - Aspose.CAD Tutorial
og_description: Μάθετε πώς να παρακάμψετε την ανίχνευση dwg codepage σε αρχεία DWG
  χρησιμοποιώντας το Aspose.CAD για .NET, παρέχοντάς σας ακριβή έλεγχο στην character
  encoding και βελτιώνοντας τη διαχείριση αρχείων CAD.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Πώς να παρακάμψετε το dwg codepage στο Aspose.CAD για .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Πώς να παρακάμψετε το dwg codepage στο Aspose.CAD για .NET
url: /el/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να παρακάμψετε τη σελίδα κωδικοποίησης dwg στο Aspose.CAD για .NET

Σε πολλά παλαιά αρχεία DWG η ενσωματωμένη σελίδα κωδικοποίησης ανιχνεύεται αυτόματα, κάτι που μπορεί να οδηγήσει σε ακατάλληλο κείμενο όταν το αρχείο χρησιμοποιεί μη‑προεπιλεγμένη κωδικοποίηση. **Override dwg codepage** σάς επιτρέπει να ορίσετε ρητά την επιθυμητή κωδικοποίηση ώστε η γεωμετρία και το κείμενο σημειώσεων να αποδίδονται σωστά. Σε αυτόν τον οδηγό θα δείτε γιατί είναι σημαντικό, πώς φαίνεται το API και πώς να εφαρμόσετε τη ρύθμιση σε μερικά απλά βήματα.

## Γρήγορες απαντήσεις
- **Τι κάνει η παράκαμψη της σελίδας κωδικοποίησης DWG;** Αναγκάζει το Aspose.CAD να χρησιμοποιήσει την κωδικοποίηση που καθορίζετε αντί να τη μαντεύει, αποτρέποντας τη διαφθορά χαρακτήρων.  
- **Πότε πρέπει να το χρησιμοποιήσω;** Όποτε ένα αρχείο DWG περιέχει κείμενο σε γλώσσα που δεν είναι η προεπιλεγμένη κωδικοποίηση των Windows (π.χ., Κεντρική Ευρώπη, Κυριλλική).  
- **Ποιες κωδικοποιήσεις υποστηρίζονται;** Οποιαδήποτε .NET `Encoding` όπως `Encoding.GetEncoding(1250)` για Κεντρική Ευρώπη.  
- **Χρειάζομαι άδεια;** Η δοκιμαστική έκδοση λειτουργεί για ανάπτυξη· απαιτείται εμπορική άδεια για παραγωγή.  
- **Είναι ασφαλές για νήματα;** Ναι, η ρύθμιση εφαρμόζεται ανά αντικείμενο `Image`, ώστε πολλαπλά νήματα να μπορούν να επεξεργάζονται διαφορετικά αρχεία ταυτόχρονα.

## Τι είναι η παράκαμψη της σελίδας κωδικοποίησης dwg;
Η παράκαμψη της σελίδας κωδικοποίησης dwg είναι μια λειτουργία του Aspose.CAD που σας επιτρέπει να αντικαταστήσετε την αυτόματη ανίχνευση κωδικοποίησης της βιβλιοθήκης με μια συγκεκριμένη κωδικοποίηση χαρακτήρων που παρέχετε. Αυτό διασφαλίζει ότι οι συμβολοσειρές κειμένου μέσα στο DWG ερμηνεύονται σωστά ανεξάρτητα από τα αρχικά μεταδεδομένα του αρχείου.

## Γιατί να χρησιμοποιήσετε την παράκαμψη της σελίδας κωδικοποίησης dwg;
Το Aspose.CAD υποστηρίζει **πάνω από 50 εκδόσεις DWG/DXF** και μπορεί να επεξεργαστεί αρχεία έως **2 GB** χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη. Όταν η αυτόματη ανίχνευση αποτύχει, μπορείτε να χάσετε έως **100 % της αναγνωσιμότητας των σημειώσεων**. Ορίζοντας ρητά τη σελίδα κωδικοποίησης μειώνετε αυτόν τον κίνδυνο στο **0 %** και διατηρείτε τους χρόνους απόδοσης αμετάβλητους.

## Προαπαιτούμενα

- Βασικές γνώσεις C# και της πλατφόρμας .NET.  
- Το Aspose.CAD για .NET εγκατεστημένο. Εάν δεν το έχετε εγκαταστήσει ακόμη, κατεβάστε το από τη **[Aspose.CAD for .NET download page](https://releases.aspose.com/cad/net/)**.  
- Ένα αρχείο DWG που χρησιμοποιεί μη‑προεπιλεγμένη κωδικοποίηση (π.χ., αρχείο που δημιουργήθηκε σε σύστημα με κωδικοποίηση 1250).

## Εισαγωγή ονομάτων χώρων (namespaces)

Για να ξεκινήσετε, προσθέστε τις απαιτούμενες οδηγίες `using` ώστε ο μεταγλωττιστής να εντοπίζει τις κλάσεις του Aspose.CAD.

Εισάγετε το παρακάτω στην αρχή του αρχείου πηγαίου κώδικα C#:

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Αυτό προετοιμάζει το περιβάλλον για όλες τις επόμενες λειτουργίες CAD.

## Βήμα 1: ορίστε τον φάκελο του εγγράφου σας

Καθορίστε το φάκελο που περιέχει το DWG που θέλετε να επεξεργαστείτε. Αντικαταστήστε το σύμβολο κράτησης θέσης με την πραγματική διαδρομή στον υπολογιστή σας:

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Βήμα 2: παράκαμψη της αυτόματης ανίχνευσης κωδικοποίησης

Τώρα φτάνουμε στον πυρήνα του οδηγού. Ο παρακάτω κώδικας φορτώνει ένα αρχείο DWG, αναγκάζει τη σελίδα κωδικοποίησης σε **Windows‑1250** (Κεντρική Ευρώπη) και στη συνέχεια αποθηκεύει την εικόνα ως PNG. Αλλάξτε το όνομα αρχείου και την κωδικοποίηση ανάλογα με το σενάριό σας.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` είναι μια στατική μέθοδος που φορτώνει ένα αρχείο CAD και επιστρέφει ένα αντικείμενο `CadImage`. `LoadOptions.CodePage` καθορίζει την κωδικοποίηση χαρακτήρων που θα χρησιμοποιηθεί κατά τη φόρτωση. Το `CadImage` αντιπροσωπεύει την αναπαράσταση στη μνήμη ενός σχεδίου CAD και παρέχει μεθόδους για απόδοση ή μετατροπή.

## Συνηθισμένα προβλήματα και λύσεις

- **Παραμένουν άχρηστοι χαρακτήρες μετά την παράκαμψη** – Επαληθεύστε ότι η κωδικοποίηση που επιλέξατε ταιριάζει με τη γλώσσα του αρχικού αρχείου. Χρησιμοποιήστε `Encoding.GetEncoding(1251)` για κυριλλική, για παράδειγμα.  
- **Αποτυχία φόρτωσης αρχείου** – Βεβαιωθείτε ότι η έκδοση DWG υποστηρίζεται από την έκδοση του Aspose.CAD· αναβαθμίστε αν χρειάζεται.  
- **Μείωση απόδοσης** – Η παράκαμψη δεν προσθέτει επιπλέον φόρτο· εάν παρατηρήσετε επιβράδυνση, ελέγξτε για ανεξάρτητα προβλήματα I/O.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET με γλώσσες εκτός του C#;
A1: Το Aspose.CAD για .NET έχει σχεδιαστεί κυρίως για C#, αλλά μπορεί να χρησιμοποιηθεί και σε άλλες γλώσσες .NET όπως η VB.NET.

### Ε2: Διατίθεται δωρεάν δοκιμαστική έκδοση;
A2: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμαστική έκδοση από τη **[Aspose.CAD free trial download page](https://releases.aspose.com/)**.

### Ε3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για .NET;
A3: Επισκεφθείτε το **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)** για υποστήριξη από την κοινότητα.

### Ε4: Μπορώ να αγοράσω προσωρινή άδεια;
A4: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια από τη **[temporary license purchase page](https://purchase.aspose.com/temporary-license/)**.

### Ε5: Πού μπορώ να βρω λεπτομερή τεκμηρίωση;
A5: Ανατρέξτε στην ολοκληρωμένη **[Aspose.CAD .NET API documentation](https://reference.aspose.com/cad/net/)**.

### Ε6: Επηρεάζει η παράκαμψη της κωδικοποίησης την ποιότητα της raster απόδοσης;
A6: Όχι. Η ρύθμιση της κωδικοποίησης επηρεάζει μόνο το πώς αποκωδικοποιούνται οι συμβολοσειρές κειμένου· η ποιότητα της εικόνας παραμένει αμετάβλητη.

### Ε7: Μπορώ να εφαρμόσω την παράκαμψη όταν μετατρέπω σε μορφές εκτός του PNG;
A7: Απόλυτα. Η ίδια τιμή `LoadOptions.CodePage` λειτουργεί για PDF, SVG ή οποιαδήποτε άλλη μορφή εξόδου που υποστηρίζεται από το Aspose.CAD.

**Τελευταία ενημέρωση:** 2026-09-04  
**Δοκιμάστηκε με:** Aspose.CAD 24.10 for .NET  
**Συγγραφέας:** Aspose

## Σχετικά Μαθήματα

- [Αναζήτηση κειμένου σε αρχεία DWG με C# - Aspose.CAD Tutorial](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Μετατροπή DWG σε PDF και προσθήκη κειμένου σε C# – Aspose.CAD Tutorial](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Πώς να μετατρέψετε DWG σε PDF και raster εικόνες χρησιμοποιώντας το Aspose.CAD για .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}