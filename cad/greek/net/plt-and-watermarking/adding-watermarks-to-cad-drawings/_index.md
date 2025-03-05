---
title: Προσθήκη υδατογραφημάτων σε σχέδια CAD - Οδηγός Aspose.CAD
linktitle: Προσθήκη υδατογραφημάτων σε σχέδια CAD
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Βελτιώστε τα σχέδιά σας CAD με επαγγελματικά υδατογραφήματα χρησιμοποιώντας το Aspose.CAD για .NET. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για εξατομικευμένα και ελκυστικά σχέδια.
type: docs
weight: 11
url: /el/net/plt-and-watermarking/adding-watermarks-to-cad-drawings/
---
## Εισαγωγή

Ψάχνετε να βελτιώσετε τα σχέδια CAD προσθέτοντας επαγγελματικά υδατογραφήματα; Το Aspose.CAD για .NET παρέχει μια ισχυρή λύση για την απρόσκοπτη ενσωμάτωση υδατογραφημάτων στα αρχεία CAD σας. Σε αυτόν τον οδηγό βήμα προς βήμα, θα σας καθοδηγήσουμε στη διαδικασία προσθήκης υδατογραφημάτων χρησιμοποιώντας το Aspose.CAD, διασφαλίζοντας ότι τα σχέδιά σας όχι μόνο μεταφέρουν κρίσιμες πληροφορίες αλλά και φέρουν το μοναδικό σας σημάδι.

## Προαπαιτούμενα

Πριν βουτήξετε στο σεμινάριο, βεβαιωθείτε ότι έχετε τα εξής:
-  Aspose.CAD για .NET: Βεβαιωθείτε ότι έχετε εγκαταστήσει τη βιβλιοθήκη Aspose.CAD. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/net/).
- Ο Κατάλογος Εγγράφων σας: Ρυθμίστε έναν κατάλογο για να αποθηκεύσετε τα σχέδιά σας CAD.
Τώρα, ας ξεκινήσουμε με την προσθήκη υδατογραφημάτων στα σχέδιά σας CAD!

## Εισαγωγή χώρων ονομάτων

Ξεκινήστε εισάγοντας τους απαραίτητους χώρους ονομάτων στο έργο σας .NET:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Βήμα 1: Φορτώστε το Σχέδιο CAD

```csharp
// Η διαδρομή προς τον κατάλογο εγγράφων.
string MyDir = "Your Document Directory";
using (CadImage cadImage = (CadImage)Image.Load(MyDir + "Drawing11.dwg")) {
```

## Βήμα 2: Προσθήκη υδατογραφήματος ως MTEXT

```csharp
// Προσθήκη νέου MTEXT
CadMText watermark = new CadMText();
watermark.Text = "Watermark message";
watermark.InitialTextHeight = 40;
watermark.InsertionPoint = new Cad3DPoint(300, 40);
watermark.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(watermark);
```

## Βήμα 3: Ή Προσθήκη υδατογραφήματος ως κείμενο

```csharp
// Εναλλακτικά, προσθέστε μια απλούστερη οντότητα όπως το Κείμενο
CadText text = new CadText();
text.DefaultValue = "Watermark text";
text.TextHeight = 40;
text.FirstAlignment = new Cad3DPoint(300, 40);
text.LayerName = "0";
cadImage.BlockEntities["*Model_Space"].AddEntity(text);
```

## Βήμα 4: Εξαγωγή σε PDF

```csharp
// Εξαγωγή του σχεδίου CAD με υδατογράφημα σε PDF
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = 1600;
rasterizationOptions.PageHeight = 1600;
rasterizationOptions.Layouts = new[] { "Model" };
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.VectorRasterizationOptions = rasterizationOptions;
cadImage.Save(MyDir + "AddWatermark_out.pdf", pdfOptions);
```

Επαναλάβετε αυτά τα βήματα για διαφορετικά σχέδια και θα έχετε υδατογραφημένα αρχεία CAD με επαγγελματική εμφάνιση σε χρόνο μηδέν!

## συμπέρασμα

Συγχαρητήρια! Έχετε μάθει με επιτυχία πώς να προσθέτετε υδατογραφήματα στα σχέδιά σας CAD χρησιμοποιώντας το Aspose.CAD για .NET. Αυτή η απλή αλλά ισχυρή διαδικασία σάς επιτρέπει να εξατομικεύσετε τα σχέδιά σας διατηρώντας παράλληλα την ακεραιότητα των τεχνικών σχεδίων σας.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να προσαρμόσω την εμφάνιση του υδατογραφήματος;

A1: Ναι, μπορείτε να προσαρμόσετε το κείμενο, τη γραμματοσειρά, το μέγεθος και τη θέση του υδατογραφήματος σύμφωνα με τις προτιμήσεις σας.

### Ε2: Είναι το Aspose.CAD συμβατό με διαφορετικές μορφές αρχείων CAD;

A2: Το Aspose.CAD υποστηρίζει διάφορες μορφές αρχείων CAD, συμπεριλαμβανομένων των DWG και DXF, διασφαλίζοντας ευρεία συμβατότητα.

### Ε3: Μπορώ να προσθέσω πολλά υδατογραφήματα σε ένα μεμονωμένο σχέδιο CAD;

Α3: Απολύτως! Μπορείτε να προσθέσετε όσα υδατογραφήματα χρειάζεται, παρέχοντας ευελιξία για διαφορετικές περιπτώσεις χρήσης.

### Ε4: Το Aspose.CAD προσφέρει δωρεάν δοκιμή;

A4: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD με μια δωρεάν δοκιμή. Αποκτήστε το[εδώ](https://releases.aspose.com/).

### Ε5: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD;

 A5: Για οποιαδήποτε απορία ή βοήθεια, επισκεφθείτε τη διεύθυνση[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19).