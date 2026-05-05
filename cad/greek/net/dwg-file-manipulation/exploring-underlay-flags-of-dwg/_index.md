---
date: 2026-04-09
description: Μάθετε πώς να μετατρέψετε DWG σε εικόνα και πώς να διαβάζετε τις σημαίες
  υποβάθμισης χρησιμοποιώντας το Aspose.CAD για .NET σε αυτόν τον οδηγό βήμα‑προς‑βήμα.
keywords:
- convert dwg to image
- how to read underlay
- Aspose.CAD DWG underlay flags
linktitle: Εξερεύνηση Σημαίων Υποβάθρου Αρχείων DWG
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Μετατροπή DWG σε εικόνα – Εξερεύνηση των σημαιών υποστρώματος αρχείων DWG -
  Εγχειρίδιο Aspose.CAD
url: /el/net/dwg-file-manipulation/exploring-underlay-flags-of-dwg/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξερεύνηση Σημαδιών Υπόστρωσης Αρχείων DWG - Εκπαίδευση Aspose.CAD

## Εισαγωγή

Αν εμβαθύνετε στον πολύπλοκο κόσμο των αρχείων CAD, συγκεκριμένα των αρχείων DWG, και θέλετε να **μετατρέψετε DWG σε εικόνα** ενώ ταυτόχρονα ανακαλύπτετε **πώς να διαβάσετε τις σημαίες υπόστρωσης**, βρίσκεστε στο σωστό μέρος. Αυτό το tutorial σας οδηγεί βήμα-βήμα χρησιμοποιώντας τη δυναμική βιβλιοθήκη Aspose.CAD για .NET, ώστε να μπορείτε να εξάγετε πληροφορίες υπόστρωσης και να αποδώσετε το σχέδιο ως εικόνα με σιγουριά.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει η «μετατροπή DWG σε εικόνα»;**  
  Σημαίνει την απόδοση ενός σχεδίου DWG σε μορφή raster (PNG, JPEG κ.λπ.) χρησιμοποιώντας το Aspose.CAD.
- **Ποια μέθοδος αποκαλύπτει τις σημαίες υπόστρωσης;**  
  Πρόσβαση στην ιδιότητα `Flags` του αντικειμένου `CadUnderlay` μετά τη φόρτωση του DWG.
- **Χρειάζομαι άδεια για το Aspose.CAD;**  
  Μια προσωρινή άδεια είναι διαθέσιμη για αξιολόγηση· απαιτείται πλήρης άδεια για παραγωγή.
- **Ποιες εκδόσεις .NET υποστηρίζονται;**  
  .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6 και μεταγενέστερες.
- **Μπορώ να εξάγω τη γεωμετρία της υπόστρωσης;**  
  Ναι – η διαδρομή της υπόστρωσης, το σημείο εισαγωγής, η κλίμακα, η περιστροφή και οι καταστάσεις των σημαδιών είναι όλα προσβάσιμα.

## Τι είναι η «μετατροπή DWG σε εικόνα» και γιατί είναι σημαντική;

Η μετατροπή ενός αρχείου DWG σε εικόνα σας επιτρέπει να εμφανίζετε σχέδια CAD σε προγράμματα περιήγησης, να τα ενσωματώνετε σε αναφορές ή να τα μοιράζεστε με ενδιαφερόμενους που δεν διαθέτουν προβολέα CAD. Κατά την απόδοση, συχνά χρειάζεται να ελέγξετε τα αντικείμενα **υπόστρωσης** (π.χ. αναφορές DGN) για να διασφαλίσετε ότι εμφανίζονται σωστά. Η κατανόηση των σημαδιών υπόστρωσης σας βοηθά να αντιμετωπίσετε προβλήματα αποκοπής, μονόχρωμης απόδοσης και ορατότητας πριν δημιουργήσετε την τελική εικόνα.

## Προαπαιτούμενα

- Βασική κατανόηση της C# και του προγραμματισμού .NET.  
- Βιβλιοθήκη **Aspose.CAD for .NET** εγκατεστημένη. Αν δεν την έχετε ακόμη, κατεβάστε τη **[εδώ](https://releases.aspose.com/cad/net/)**.  
- Ένα αρχείο DWG για δοκιμές – το δείγμα **«BlockRefDgn.dwg»** χρησιμοποιείται σε όλη αυτήν την καθοδήγηση.

## Εισαγωγή Χώρων Ονομάτων

Για να ξεκινήσετε, εισάγετε τους απαραίτητους χώρους ονομάτων:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
```

## Βήμα 1: Φόρτωση Αρχείου DWG και Μετατροπή σε `CadImage`

Πρώτα, φορτώστε το αρχείο DWG και μετατρέψτε το σε `CadImage`. Αυτό το αντικείμενο σας δίνει πρόσβαση σε όλες τις οντότητες του σχεδίου, συμπεριλαμβανομένων των υποστρώσεων.

```csharp
string fileName = MyDir + "BlockRefDgn.dwg";

// Load DWG file and convert to CadImage
using (CadImage image = (CadImage)Image.Load(fileName))
{
    // Your code for subsequent steps will go here
}
```

## Βήμα 2: Επανάληψη Μέσω Οντοτήτων

Στη συνέχεια, κάντε βρόχο σε κάθε οντότητα του σχεδίου. Εδώ θα εντοπίσετε τα αντικείμενα υπόστρωσης.

```csharp
foreach (CadBaseEntity entity in image.Entities)
{
    // Your code for subsequent steps will go here
}
```

## Βήμα 3: Έλεγχος για Τύπο `CadDgnUnderlay`

Αναγνωρίστε τις οντότητες υπόστρωσης ελέγχοντας τον τύπο χρόνου εκτέλεσης. Η κλάση `CadDgnUnderlay` αντιπροσωπεύει τις DGN υπόστρωσεις ενσωματωμένες σε DWG.

```csharp
if (entity is CadDgnUnderlay)
{
    // Your code for subsequent steps will go here
}
```

## Βήμα 4: Πρόσβαση σε Σημαίες Υπόστρωσης

Μόλις έχετε ένα `CadDgnUnderlay`, μετατρέψτε το σε `CadUnderlay` για να διαβάσετε τις ιδιότητές του και τις καταστάσεις των σημαδιών. Οι σημαίες σας λένε αν η υπόστρωση είναι ορατή, αποκομμένη ή αποδίδεται μονόχρωμα.

```csharp
CadUnderlay underlay = entity as CadUnderlay;

Console.WriteLine(underlay.UnderlayPath);
Console.WriteLine(underlay.UnderlayName);
Console.WriteLine(underlay.InsertionPoint.X);
Console.WriteLine(underlay.InsertionPoint.Y);
Console.WriteLine(underlay.RotationAngle);
Console.WriteLine(underlay.ScaleX);
Console.WriteLine(underlay.ScaleY);
Console.WriteLine(underlay.ScaleZ);
Console.WriteLine((underlay.Flags & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
Console.WriteLine((underlay.Flags & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
```

### Τι σας λέει η έξοδος

- **UnderlayPath / UnderlayName** – πού βρίσκεται το εξωτερικό αρχείο DGN.  
- **InsertionPoint (X, Y)** – συντεταγμένες όπου τοποθετείται η υπόστρωση στο χώρο του DWG.  
- **RotationAngle** – η γωνία περιστροφής που εφαρμόζεται στην υπόστρωση.  
- **ScaleX / ScaleY / ScaleZ** – παράγοντες κλίμακας για κάθε άξονα.  
- **Flags** – λογικές τιμές που υποδεικνύουν ορατότητα (`UnderlayIsOn`), αποκοπή (`ClippingIsOn`) και μονόχρωμη απόδοση (`Monochrome`).

## Συχνά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Δεν υπάρχει έξοδος για ελέγχους σημαδιών | Οι σημαίες υπόστρωσης είναι προεπιλεγμένες στο 0 όταν η υπόστρωση είναι απενεργοποιημένη. | Βεβαιωθείτε ότι το DWG περιέχει ενεργή υπόστρωση ή αλλάξτε την ορατότητα στο αρχικό αρχείο CAD. |
| Εξαίρεση `Invalid cast` | Η οντότητα δεν είναι `CadDgnUnderlay`. | Επαληθεύστε ότι υπάρχει η προϋπόθεση `if (entity is CadDgnUnderlay)` πριν την μετατροπή. |
| Η απόδοση της εικόνας αποτυγχάνει μετά την εξαγωγή σημαδιών | Η υπόστρωση μπορεί να είναι αποκομμένη ή απενεργοποιημένη, οδηγώντας σε κενή περιοχή. | Ρυθμίστε τις σημαίες (`UnderlayIsOn = true`, `ClippingIsOn = false`) πριν αποδώσετε την τελική εικόνα. |

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET με άλλες μορφές αρχείων CAD;

A1: Το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF, DGN και άλλων. Ελέγξτε την τεκμηρίωση για την πλήρη λίστα.

### Ε2: Διατίθεται προσωρινή άδεια για το Aspose.CAD για .NET;

A2: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια **[εδώ](https://purchase.aspose.com/temporary-license/)**.

### Ε3: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD για .NET;

A3: Επισκεφθείτε το φόρουμ υποστήριξης **[εδώ](https://forum.aspose.com/c/cad/19)** για βοήθεια.

### Ε4: Πώς μπορώ να αγοράσω το Aspose.CAD για .NET;

A4: Αγοράστε τη βιβλιοθήκη **[εδώ](https://purchase.aspose.com/buy)**.

### Ε5: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

A5: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή **[εδώ](https://releases.aspose.com/)**.

## Συμπέρασμα

Συγχαρητήρια! Έχετε μάθει με επιτυχία **πώς να μετατρέψετε DWG σε εικόνα** ενώ ταυτόχρονα έχετε κατακτήσει **πώς να διαβάζετε τις σημαίες υπόστρωσης** χρησιμοποιώντας το Aspose.CAD για .NET. Με αυτή τη γνώση μπορείτε:

- Να αποδίδετε σχέδια DWG ως raster εικόνες για διαδικτυακές ή αναφορικές εφαρμογές.  
- Να ελέγχετε και να τροποποιείτε τις ιδιότητες της υπόστρωσης για σωστή εμφάνιση.  
- Να εντοπίζετε προβλήματα ορατότητας, αποκοπής και μονόχρωμης απόδοσης πριν τη δημιουργία της τελικής εικόνας.

Ανακαλύψτε άλλα χαρακτηριστικά του Aspose.CAD όπως διαχείριση επιπέδων, εξαγωγή κειμένου και μαζική μετατροπή για να επεκτείνετε περαιτέρω τις ροές εργασίας αυτοματοποίησης CAD.

---

**Last Updated:** 2026-04-09  
**Tested With:** Aspose.CAD for .NET 24.11  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}