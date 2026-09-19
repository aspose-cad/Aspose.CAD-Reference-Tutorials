---
date: 2026-09-19
description: Μάθετε πώς να εφαρμόσετε την Aspose CAD metered licensing στο .NET για
  να παρακολουθείτε το resource usage των εφαρμογών .NET αποδοτικά. Ακολουθήστε τον
  step‑by‑step guide μας.
keywords:
- aspose cad metered licensing
- monitor resource usage .net
- aspose cad licensing
lastmod: 2026-09-19
linktitle: Metered Licensing
og_description: Μάθετε πώς να εφαρμόσετε την Aspose CAD metered licensing στο .NET
  για να παρακολουθείτε το resource usage των εφαρμογών .NET αποδοτικά. Ακολουθήστε
  τον step‑by‑step guide μας.
og_image_alt: Guide to Aspose CAD metered licensing for .NET developers
og_title: Πώς να χρησιμοποιήσετε την Aspose CAD metered licensing στο .NET
schemas:
- author: Aspose
  dateModified: '2026-09-19'
  description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  headline: How to use Aspose CAD metered licensing in .NET
  type: TechArticle
- description: Learn how to implement Aspose CAD metered licensing in .NET to monitor
    resource usage .NET applications efficiently. Follow our step‑by‑step guide.
  name: How to use Aspose CAD metered licensing in .NET
  steps:
  - name: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
    text: '**Aspose.CAD installed** – download the latest package from the [Aspose.CAD
      website](https://releases.aspose.com/cad/net/).'
  - name: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
    text: '**Public and private keys** – obtain them from the [Aspose.CAD purchase
      page](https://purchase.aspose.com/buy).'
  - name: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
    text: '**Basic .NET knowledge** – the guide assumes you are comfortable with C#
      projects targeting .NET 6 or later.'
  type: HowTo
- questions:
  - answer: Yes, the free trial version available from the [free trial version](https://releases.aspose.com/)
      supports metered licensing.
    question: Can I use metered licensing with a free trial?
  - answer: Monitoring before and after each major operation gives the most accurate
      insight, but you can also poll at regular intervals for long‑running services.
    question: How often should I check consumption quantities?
  - answer: Yes, the same public/private key pair can be reused across multiple projects
      and environments.
    question: Are metered keys reusable?
  - answer: The library will throw a licensing exception. You can either purchase
      additional credits or contact support via the [Aspose.CAD support](https://forum.aspose.com/c/cad/19)
      forum.
    question: What happens if I exceed my metered limit?
  - answer: Absolutely – explore [temporary licensing options](https://purchase.aspose.com/temporary-license/)
      for limited‑duration needs.
    question: Can I temporarily license Aspose.CAD for a short‑term project?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- aspose cad
- metered licensing
- .net resource monitoring
title: Πώς να χρησιμοποιήσετε την Aspose CAD metered licensing στο .NET
url: /el/net/licensing-and-configuration/metered-licensing/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Aspose CAD μετρημένη άδεια σε .NET

## Εισαγωγή

Η μετρημένη άδεια Aspose CAD σας επιτρέπει να ελέγχετε πόσες κλήσεις CAD/BIM API καταναλώνει η εφαρμογή σας .NET, παρέχοντας ακριβή τιμολόγηση και πληροφορίες χρήσης. Ενσωματώνοντας αυτό το μοντέλο αδειοδότησης μπορείτε να **παρακολουθείτε τη χρήση πόρων** των εφαρμογών .NET χωρίς σκληρό κωδικοποίηση ορίων, κάνοντας την κλιμάκωση και τη διαχείριση κόστους απλή. Ο παρακάτω οδηγός σας καθοδηγεί βήμα προς βήμα, από την εισαγωγή ονοματοχώρων μέχρι την ανάγνωση δεδομένων κατανάλωσης πριν και μετά την επεξεργασία.

## Σύντομες απαντήσεις
- **Τι είναι η μετρημένη άδεια;** Ένα μοντέλο βασισμένο στη χρήση, όπου κάθε κλήση API καταναλώνει μια προκαθορισμένη μονάδα.
- **Χρειάζομαι άδεια δοκιμής;** Ναι – η δωρεάν δοκιμή λειτουργεί με μετρημένα κλειδιά.
- **Πώς μπορώ να δω την κατανάλωση;** Κλήστε `License.GetConsumptionQuantity()` πριν και μετά τις λειτουργίες σας.
- **Είναι ασφαλές για νήματα;** Ναι, η μηχανή αδειοδότησης έχει σχεδιαστεί για ταυτόχρονες εργασίες .NET.
- **Μπορώ να επαναχρησιμοποιήσω το ίδιο κλειδί;** Απόλυτα – το ίδιο ζεύγος δημόσιου/ιδιωτικού κλειδιού μπορεί να μοιραστεί μεταξύ έργων.

## Τι είναι η μετρημένη άδεια Aspose CAD;

Η μετρημένη άδεια Aspose CAD είναι ένα μοντέλο αδειοδότησης βάσει χρήσης που παρακολουθεί κάθε κλήση API που κάνει η βιβλιοθήκη Aspose.CAD για .NET. Επιτρέπει στους προγραμματιστές να πληρώνουν μόνο για τους πόρους που πραγματικά καταναλώνουν, αντί να αγοράζουν μια μόνιμη θέση.

## Γιατί να χρησιμοποιήσετε μετρημένη άδεια με το Aspose CAD;

Η μετρημένη άδεια σας δίνει ακριβή έλεγχο του κόστους χρεώνοντας μόνο για την πραγματική χρήση του API. Απομακρύνει την ανάγκη για προπληρωμένες θέσεις και κλιμακώνεται αυτόματα με το φορτίο εργασίας, καθιστώντας την ιδανική για διαλείπουσα ή cloud‑βασισμένη επεξεργασία όπου η χρήση κυμαίνεται.

## Προαπαιτούμενα

1. **Aspose.CAD εγκατεστημένο** – κατεβάστε το τελευταίο πακέτο από την [Aspose.CAD website](https://releases.aspose.com/cad/net/).  
2. **Δημόσια και ιδιωτικά κλειδιά** – αποκτήστε τα από τη [Aspose.CAD purchase page](https://purchase.aspose.com/buy).  
3. **Βασικές γνώσεις .NET** – ο οδηγός υποθέτει ότι είστε άνετοι με έργα C# που στοχεύουν στο .NET 6 ή νεότερο.

## Εισαγωγή ονοματοχώρων

Προσθέστε τις απαιτούμενες οδηγίες `using` στην αρχή του αρχείου C# ώστε ο μεταγλωττιστής να εντοπίζει τις κλάσεις Aspose.CAD.

```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;
using Aspose.CAD.License;
```

Ο χώρος ονομάτων `License` περιέχει τις κλάσεις που απαιτούνται για τη μετρημένη άδεια.

## Πώς να ορίσετε το μετρημένο κλειδί;

`SetMeteredKey` καταχωρίζει τα δημόσια και ιδιωτικά κλειδιά μετρημένης άδειας σας με τη μηχανή Aspose.CAD. Καλέστε αυτή τη μέθοδο μία φορά κατά την εκκίνηση της εφαρμογής, περνώντας τα κλειδιά που λάβατε από την Aspose. Αυτό εξασφαλίζει ότι όλες οι επόμενες κλήσεις API παρακολουθούνται στο λογαριασμό σας.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Πώς να λάβετε την ποσότητα κατανάλωσης πριν από την κλήση API;

`GetConsumptionQuantity` επιστρέφει το συνολικό αριθμό μονάδων που έχει καταναλώσει η βιβλιοθήκη μέχρι το σημείο κλήσης. Καταγράψτε αυτή την τιμή πριν εκτελέσετε οποιεσδήποτε λειτουργίες CAD για να δημιουργήσετε μια βάση. Συγκρίνοντας την με την τιμή μετά την επεξεργασία, μπορείτε να καθορίσετε την ακριβή χρήση μονάδων μιας συγκεκριμένης εργασίας.

```csharp
//ExStart:MeteredLicensing
// Access the setMeteredKey property and pass public and private keys as parameters
Aspose.CAD.Metered.SetMeteredKey("PublicKey", "PrivateKey");
```

## Πώς να επεξεργαστείτε δεδομένα CAD με το Aspose.CAD;

`CadImage` αντιπροσωπεύει ένα φορτωμένο αρχείο CAD και παρέχει μεθόδους για απόδοση ή μετατροπή. Μετά τον ορισμό του μετρημένου κλειδιού, φορτώστε το αρχείο CAD σας σε μια παρουσία `CadImage`. Στη συνέχεια μπορείτε να αποδώσετε σε μορφές raster, να μετατρέψετε σε άλλους τύπους CAD ή να εξάγετε μεταδεδομένα, όλα θα μετρηθούν προς το μετρημένο όριό σας.

```csharp
// Get metered data amount before calling API
decimal amountbefore = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed Before: " + amountbefore.ToString());
```

## Πώς να λάβετε την ποσότητα κατανάλωσης μετά την κλήση API;

`GetConsumptionQuantity` μπορεί να κληθεί ξανά μετά την επεξεργασία για να λάβει το ενημερωμένο σύνολο μονάδων. Αφαιρέστε τη προηγούμενη καταγεγραμμένη βάση για να υπολογίσετε πόσες μονάδες κατανάλωσε η πρόσφατη λειτουργία. Αυτές οι πληροφορίες σας βοηθούν να παρακολουθείτε τα πρότυπα χρήσης και να βελτιστοποιείτε τον κώδικά σας για χαμηλότερο κόστος.

```csharp
// Do processing
//Aspose.CAD.FileFormats.Cad.CadImage image = (Aspose.CAD.FileFormats.Cad.CadImage)Aspose.CAD.Image.load("BlockRefDgn.dwg");
```

## Συχνά προβλήματα και αντιμετώπιση

- **Σφάλμα μη ορισμένης άδειας:** Βεβαιωθείτε ότι το `SetMeteredKey` κλήθηκε πριν από οποιαδήποτε χρήση του Aspose.CAD API.  
- **Απρόσμενη υψηλή κατανάλωση:** Επαληθεύστε ότι δεν φορτώνετε ακούσια μεγάλες δέσμες αρχείων σε βρόχο· κάθε φόρτωση μετρά ως ξεχωριστή κλήση.  
- **Ανησυχίες για την ασφάλεια νήματος:** Η μηχανή αδειοδότησης είναι ασφαλής για νήματα, αλλά αποφύγετε την κλήση του `SetMeteredKey` πολλαπλές φορές ταυτόχρονα.

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω τη μετρημένη άδεια με δωρεάν δοκιμή;**  
A: Ναι, η δωρεάν έκδοση δοκιμής διαθέσιμη από το [free trial version](https://releases.aspose.com/) υποστηρίζει τη μετρημένη άδεια.

**Q: Πόσο συχνά πρέπει να ελέγχω τις ποσότητες κατανάλωσης;**  
A: Η παρακολούθηση πριν και μετά κάθε σημαντικής λειτουργίας παρέχει την πιο ακριβή εικόνα, αλλά μπορείτε επίσης να ελέγχετε σε τακτικά διαστήματα για υπηρεσίες μεγάλης διάρκειας.

**Q: Είναι τα μετρημένα κλειδιά επαναχρησιμοποιήσιμα;**  
A: Ναι, το ίδιο ζεύγος δημόσιου/ιδιωτικού κλειδιού μπορεί να επαναχρησιμοποιηθεί σε πολλαπλά έργα και περιβάλλοντα.

**Q: Τι συμβαίνει αν υπερβώ το όριο της μετρημένης άδειας;**  
A: Η βιβλιοθήκη θα ρίξει εξαίρεση αδειοδότησης. Μπορείτε είτε να αγοράσετε επιπλέον μονάδες είτε να επικοινωνήσετε με την υποστήριξη μέσω του φόρουμ [Aspose.CAD support](https://forum.aspose.com/c/cad/19).

**Q: Μπορώ να λάβω προσωρινή άδεια για το Aspose.CAD για ένα βραχυπρόθεσμο έργο;**  
A: Απόλυτα – εξερευνήστε τις [temporary licensing options](https://purchase.aspose.com/temporary-license/) για ανάγκες περιορισμένης διάρκειας.

---

**Τελευταία ενημέρωση:** 2026-09-19  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

```csharp
// Get metered data amount after calling API
decimal amountafter = Aspose.CAD.Metered.GetConsumptionQuantity();
// Display information
Console.WriteLine("Amount Consumed After: " + amountafter.ToString());
//ExEnd:MeteredLicensing 
```

## Σχετικά μαθήματα

- [Εφαρμογή άδειας στο Aspose.CAD για .NET – Βήμα‑βήμα](/cad/net/)
- [Πώς να μετατρέψετε και να εξάγετε σχέδια CAD σε PDF με το Aspose.CAD για .NET – Μάθημα](/cad/net/advanced-export-techniques/exporting-cad-drawings-to-pdf/)
- [Μετατροπή CAD σε PNG στο Aspose.CAD για .NET](/cad/net/cad-drawing-manipulation/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}