---
date: 2026-04-03
description: Μάθετε πώς να ορίσετε το viewport και να μετατρέψετε DWG σε PDF σε C#
  χρησιμοποιώντας το Aspose.CAD. Αυτό το tutorial μετατροπής DWG σε PDF δείχνει ακριβή
  εξαγωγή με συντεταγμένες.
keywords:
- how to set viewport
- dwg to pdf tutorial
- convert dwg to pdf c#
linktitle: Μετατροπή DWG σε PDF με Συντεταγμένες σε C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Πώς να ορίσετε το Viewport κατά τη μετατροπή DWG σε PDF με Συντεταγμένες σε
  C# - Εκπαιδευτικό σεμινάριο Aspose.CAD
url: /el/net/conversion-and-export/converting-dwg-to-pdf-with-coordinates/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DWG σε PDF με Συντεταγμένες σε C# - Εγχειρίδιο Aspose.CAD

## Εισαγωγή

Καλώς ήρθατε σε αυτό το ολοκληρωμένο εγχειρίδιο σχετικά με **πώς να ορίσετε το viewport** κατά τη μετατροπή αρχείων DWG σε PDF με καθορισμένες συντεταγμένες χρησιμοποιώντας το Aspose.CAD για .NET. Με τον έλεγχο του viewport λαμβάνετε PDF με τέλεια ακρίβεια pixel που ταιριάζουν ακριβώς στην περιοχή που χρειάζεστε — ιδανικά για σχέδια κατασκευής, προεπισκοπήσεις σχεδίων δαπέδου ή οποιαδήποτε ροή εργασίας BIM.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “set viewport”;** Ορίζει την ορατή περιοχή και την κλίμακα του σχεδίου CAD κατά τη διαδικασία rasterization.  
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή;** Aspose.CAD για .NET.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγή.  
- **Υποστηριζόμενες πλατφόρμες;** Windows, Linux και macOS με .NET 5/6/7 ή .NET Framework 4.6+.  
- **Τυπικός χρόνος υλοποίησης;** Περίπου 10‑15 λεπτά για μια βασική μετατροπή.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- **Aspose.CAD Library** – Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD για .NET. Μπορείτε να βρείτε τη βιβλιοθήκη [εδώ](https://releases.aspose.com/cad/net/).
- **Development Environment** – Visual Studio, Rider ή οποιοδήποτε IDE που υποστηρίζει ανάπτυξη .NET.
- **DWG File** – Έχετε ένα αρχείο DWG έτοιμο για μετατροπή. Μπορείτε να χρησιμοποιήσετε το παρεχόμενο αρχείο παραδείγματος ή το δικό σας προσαρμοσμένο αρχείο DWG.

## Πώς να Ορίσετε το Viewport για Ακριβή Εξαγωγή PDF

Ο καθορισμός του viewport είναι το βασικό βήμα που σας επιτρέπει να ορίσετε την ακριβή περιοχή του σχεδίου που θέλετε να αποδώσετε. Στον παρακάτω κώδικα δημιουργούμε ένα νέο `CadVportTableObject`, το τοποθετούμε με την κορυφαία‑αριστερή συντεταγμένη και υπολογίζουμε το πλάτος, το ύψος και την αναλογία διαστάσεων. Αυτή είναι η **πώς να ορίσετε το viewport** υλοποίηση που καθοδηγεί το υπόλοιπο της μετατροπής.

## Εισαγωγή Ονομάτων Χώρων

Στο έργο C# σας, εισάγετε τα απαραίτητα ονόματα χώρων:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadParameters;
using Aspose.CAD.FileFormats.Cad.CadTables;
using Aspose.CAD.ImageOptions;
```

Ας αναλύσουμε τον κώδικα βήμα‑βήμα για καλύτερη κατανόηση:

## Βήμα 1: Ορισμός του Καταλόγου Εγγράφου

```csharp
string MyDir = "Your Document Directory";
```

## Βήμα 2: Ορισμός της Διαδρομής του Πηγαίου Αρχείου DWG

```csharp
string sourceFilePath = MyDir + "visualization_-_conference_room.dwg";
```

## Βήμα 3: Φόρτωση Αρχείου DWG και Διαμόρφωση Επιλογών Rasterization

```csharp
using (CadImage cadImage = (CadImage)Image.Load(sourceFilePath))
{
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.Layouts = new string[] { "Model" };
    rasterizationOptions.NoScaling = true;
```

## Βήμα 4: Ορισμός Συντεταγμένων και Viewport  

Εδώ πραγματικά **ορίζουμε το viewport** (πώς να ορίσετε το viewport) καθορίζοντας την επάνω‑αριστερή γωνία, το πλάτος και το ύψος της περιοχής που θέλετε να εξάγετε.

```csharp
    Point topLeft = new Point(500, 1000);
    double width = 3108;
    double height = 2489;

    CadVportTableObject newView = new CadVportTableObject();
    newView.Name = new CadStringParameter();
    newView.Name.Init("*Active");
    newView.CenterPoint.X = topLeft.X + width / 2f;
    newView.CenterPoint.Y = topLeft.Y - height / 2f;
    newView.ViewHeight.Value = height;
    newView.ViewAspectRatio.Value = width / height;
```

## Βήμα 5: Εφαρμογή Ρυθμίσεων Viewport

```csharp
    for (int i = 0; i < cadImage.ViewPorts.Count; i++)
    {
        CadVportTableObject currentView = (CadVportTableObject)(cadImage.ViewPorts[i]);
        if (cadImage.ViewPorts.Count == 1 || string.Equals(currentView.Name.Value.ToLowerInvariant(), "*active"))
        {
            cadImage.ViewPorts[i] = newView;
            break;
        }
    }
```

## Βήμα 6: Διαμόρφωση Επιλογών PDF και Εξαγωγή  

Τώρα συνδέουμε όλα μαζί και **μετατρέπουμε το DWG σε PDF** χρησιμοποιώντας τις επιλογές rasterization που μόλις προετοιμάσαμε.

```csharp
    Aspose.CAD.ImageOptions.PdfOptions pdfOptions = new Aspose.CAD.ImageOptions.PdfOptions();
    pdfOptions.VectorRasterizationOptions = rasterizationOptions;

    MyDir = MyDir + "ConvertDWGToPDFBySupplyingCoordinates_out.pdf";
    cadImage.Save(MyDir, pdfOptions);
}
```

## Βήμα 7: Εμφάνιση Μηνύματος Επιτυχίας

```csharp
Console.WriteLine("\nThe DWG file exported successfully to PDF.\nFile saved at " + MyDir);
```

## Συνηθισμένες Περιπτώσεις Χρήσης

- **Construction documentation** – Δημιουργία εκτυπώσιμων PDF συγκεκριμένων τμημάτων σχεδίου δαπέδου.  
- **BIM coordination** – Εξαγωγή μόνο της περιοχής ενδιαφέροντος για ανίχνευση συγκρούσεων.  
- **Client presentations** – Παροχή καθαρού PDF ενός επιλεγμένου δωματίου ή υψομέτρου χωρίς να αποκαλύπτεται ολόκληρο το σχέδιο.

## Συμπέρασμα

Συγχαρητήρια! Μετατρέψατε επιτυχώς **DWG σε PDF** με ακριβείς συντεταγμένες και μάθατε **πώς να ορίσετε το viewport** χρησιμοποιώντας το Aspose.CAD για .NET. Αυτό το **dwg to pdf tutorial** δείχνει πώς να **δημιουργήσετε pdf από dwg** και **εξάγετε dwg ως pdf c#** διατηρώντας πλήρη έλεγχο της περιοχής εξόδου.

## Συχνές Ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD με άλλες μορφές αρχείων CAD;

Α1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF, DWF και άλλων.

### Ε2: Πώς μπορώ να διαχειριστώ σφάλματα κατά τη διαδικασία μετατροπής;

Α2: Εφαρμόστε μηχανισμούς διαχείρισης σφαλμάτων χρησιμοποιώντας μπλοκ try‑catch για να συλλάβετε και να διαχειριστείτε εξαιρέσεις.

### Ε3: Είναι το Aspose.CAD κατάλληλο και για περιβάλλοντα Windows και Linux;

Α3: Ναι, το Aspose.CAD είναι συμβατό με πλατφόρμες Windows και Linux.

### Ε4: Μπορώ να προσαρμόσω περαιτέρω την έξοδο PDF;

Α4: Φυσικά! Εξερευνήστε τις εκτενείς επιλογές που παρέχει το Aspose.CAD για να προσαρμόσετε την έξοδο PDF στις συγκεκριμένες απαιτήσεις σας.

### Ε5: Πού μπορώ να βρω πρόσθετη υποστήριξη ή συζητήσεις της κοινότητας;

Α5: Επισκεφθείτε το [Aspose.CAD Forum](https://forum.aspose.com/c/cad/19) για υποστήριξη της κοινότητας και συζητήσεις.

## Πρόσθετες Συχνές Ερωτήσεις

**Ε: Λειτουργεί αυτή η προσέγγιση με μεγάλα αρχεία DWG (εκατοντάδες MB);**  
Α: Ναι. Η rasterization εκτελείται σελίδα‑με‑σελίδα, και μπορείτε να προσαρμόσετε το `rasterizationOptions` (π.χ., `Resolution`) για να ισορροπήσετε την ποιότητα και τη χρήση μνήμης.

**Ε: Μπορώ να εξάγω πολλαπλά viewports σε ξεχωριστές σελίδες PDF;**  
Α: Μπορείτε να κάνετε βρόχο μέσω των `cadImage.ViewPorts`, να ορίσετε το καθένα ως ενεργό και να καλέσετε `Save` για κάθε σελίδα, έπειτα να συγχωνεύσετε τα PDF χρησιμοποιώντας το Aspose.PDF.

**Ε: Είναι δυνατόν να προσθέσετε υδατογράφημα στο παραγόμενο PDF;**  
Α: Μετά την αποθήκευση του PDF, μπορείτε να το ανοίξετε ξανά με το Aspose.PDF και να εφαρμόσετε υδατογράφημα κειμένου ή εικόνας πριν το παραδώσετε στον χρήστη.

---

**Τελευταία ενημέρωση:** 2026-04-03  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}