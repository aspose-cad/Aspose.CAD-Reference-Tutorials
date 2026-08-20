---
date: 2026-04-06
description: Μάθετε πώς να μετατρέπετε DWG σε PDF και να προσθέτετε προσαρμοσμένο
  κείμενο χρησιμοποιώντας C# και Aspose.CAD. Αυτός ο οδηγός βήμα‑βήμα καλύπτει τη
  δημιουργία PDF από DWG, την εισαγωγή μιας οντότητας κειμένου και την αλλαγή της
  γραμματοσειράς κειμένου στο DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Προσθήκη κειμένου σε αρχεία DWG με C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Μετατροπή DWG σε PDF και προσθήκη κειμένου σε C# – Εκπαίδευση Aspose.CAD
url: /el/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DWG σε PDF και Προσθήκη Κειμένου σε C# – Εγχειρίδιο Aspose.CAD

## Εισαγωγή

Στον ταχύτατα εξελισσόμενο κόσμο του CAD και της ανάπτυξης .NET, η **μετατροπή DWG σε PDF** ενώ εισάγετε προσαρμοσμένες σημειώσεις είναι συχνή απαίτηση. Είτε χρειάζεστε να δημιουργήσετε εκτυπώσιμα σχέδια για πελάτες είτε να ενσωματώσετε δυναμικές σημειώσεις απευθείας σε DWG, το Aspose.CAD κάνει τη δουλειά απλή. Σε αυτό το εγχειρίδιο θα μάθετε πώς να **μετατρέψετε DWG σε PDF**, **προσθέτετε μια οντότητα κειμένου**, και ακόμη **αλλάζετε τη γραμματοσειρά κειμένου DWG** χρησιμοποιώντας C#.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη είναι η καλύτερη για μετατροπή DWG‑σε‑PDF;** Aspose.CAD για .NET  
- **Μπορώ να προσθέσω προσαρμοσμένο κείμενο κατά τη μετατροπή;** Ναι – δημιουργήστε μια οντότητα `CadText` και προσθέστε την πριν από την αποθήκευση.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια· διατίθεται δωρεάν δοκιμή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Είναι δυνατόν να αλλάξετε τη γραμματοσειρά του κειμένου;** Ναι, προσαρμόστε τις ιδιότητες του `CadText` όπως `StyleType` και `TextHeight`.

## Τι είναι η «μετατροπή dwg σε pdf»;

Η μετατροπή ενός αρχείου DWG σε PDF μετατρέπει ένα διανυσματικό σχέδιο CAD σε ένα ευρέως διαμοιραζόμενο, ανεξάρτητο από συσκευή έγγραφο. Το PDF διατηρεί τη αρχική γεωμετρία και τα στρώματα, ενώ σας επιτρέπει να ενσωματώσετε σημειώσεις, κείμενο ή άλλα μεταδεδομένα. Το Aspose.CAD διαχειρίζεται αυτόματα τη ραστεροποίηση και την διανυσματική απόδοση, έτσι δεν χρειάζεστε κανένα λογισμικό CAD τρίτου μέρους στον διακομιστή.

## Γιατί να προσθέσετε κείμενο σε DWG πριν από τη μετατροπή;

Η ενσωμάτωση κειμένου απευθείας στο DWG σας δίνει πλήρη έλεγχο πάνω στη θέση, το στυλ και την ανάθεση στρώματος. Όταν το αρχείο μετατραπεί αργότερα σε PDF, το κείμενο εμφανίζεται ακριβώς εκεί που το τοποθετήσατε, διατηρώντας την πρόθεση του σχεδίου και εξαλείφοντας την ανάγκη για μεταγενέστερη επεξεργασία σε πρόγραμμα επεξεργασίας PDF.

## Προαπαιτούμενα

- **Aspose.CAD Library** – κατεβάστε την από το [download link](https://releases.aspose.com/cad/net/).  
- **Ένα λειτουργικό περιβάλλον .NET** (Visual Studio 2022, .NET 6 ή οποιαδήποτε συμβατή έκδοση).  
- **Ένας φάκελος για τα αρχεία δοκιμής σας** – θα τον αναφέρουμε ως `MyDir` σε όλη την οδηγία.

Τώρα, ας περάσουμε τη διαδικασία βήμα προς βήμα.

## Εισαγωγή Namespaces

Προσθέστε τις απαιτούμενες δηλώσεις `using` ώστε να μπορείτε να έχετε πρόσβαση στις κλάσεις του Aspose.CAD.

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
using Aspose.CAD.ImageOptions;
```

## Βήμα 1: Φόρτωση του αρχείου DWG

Φορτώστε το πηγαίο αρχείο DWG σε ένα αντικείμενο `Image`. Αυτό το αντικείμενο σας δίνει πρόσβαση στις υποκείμενες οντότητες CAD.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Βήμα 2: Δημιουργία αντικειμένου CadText (Εισαγωγή οντότητας κειμένου)

Η κλάση `CadText` αντιπροσωπεύει μια μοναδική γραμμή κειμένου σε DWG. Εδώ ορίζουμε το στυλ, την τιμή, το χρώμα, το στρώμα και τη θέση του. Προσαρμόστε το `StyleType` ή το `TextHeight` για **αλλαγή της γραμματοσειράς κειμένου DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Βήμα 3: Προσθήκη της οντότητας κειμένου στο Model Space

Ο χώρος μοντέλου DWG περιέχει τις περισσότερες οντότητες σχεδίου. Προσθέτοντας το `CadText` μας στο μπλοκ `*Model_Space`, το κείμενο γίνεται μέρος του σχεδίου.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Βήμα 4: Διαμόρφωση επιλογών PDF (Δημιουργία PDF από DWG)

Διαμορφώστε τις επιλογές ραστεροποίησης που ελέγχουν πώς το DWG αποδίδεται σε PDF. Μπορείτε να ρυθμίσετε το μέγεθος σελίδας, τον τύπο σχεδίασης και τη διάταξη.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Βήμα 5: Αποθήκευση του τροποποιημένου DWG ως PDF

Τέλος, εξάγετε το τροποποιημένο σχέδιο. Το προκύπτον PDF περιλαμβάνει το νεοεισαγμένο κείμενο.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Συμβουλή:** Εάν χρειάζεστε PDF υψηλότερης ανάλυσης, αυξήστε αναλογικά το `PageHeight` και το `PageWidth`.

## Συχνά Προβλήματα & Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|----------|-------|----------|
| Το κείμενο δεν εμφανίζεται στο PDF | Λανθασμένο στρώμα ή ID χρώματος | Βεβαιωθείτε ότι το `LayerName` υπάρχει και το `ColorId` έχει οριστεί σε ορατό χρώμα (π.χ., 7 για λευκό). |
| Το κείμενο είναι εκτός θέσης | Εσφαλμένες συντεταγμένες ευθυγράμμισης | Επαληθεύστε τις τιμές `FirstAlignment.X/Y` σε σχέση με τις μονάδες του σχεδίου. |
| Το PDF είναι κενό | Οι επιλογές ραστεροποίησης δεν έχουν οριστεί | Ορίστε το `DrawType` σε `UseObjectColor` ή `UseObjectLineWeight`. |

## Συχνές Ερωτήσεις (Υπάρχουσες)

### Ε1: Είναι το Aspose.CAD συμβατό με όλες τις εκδόσεις αρχείων DWG;

Α1: Το Aspose.CAD υποστηρίζει ένα ευρύ φάσμα εκδόσεων αρχείων DWG, εξασφαλίζοντας συμβατότητα με διάφορο λογισμικό CAD.

### Ε2: Μπορώ να προσθέσω πολλαπλές οντότητες κειμένου σε ένα αρχείο DWG χρησιμοποιώντας το Aspose.CAD;

Α2: Ναι, μπορείτε να προσθέσετε πολλαπλές οντότητες κειμένου σε αρχείο DWG επαναλαμβάνοντας τη διαδικασία που περιγράφεται στο εγχειρίδιο.

### Ε3: Πώς μπορώ να αλλάξω τη γραμματοσειρά και το στυλ του κειμένου στο Aspose.CAD;

Α3: Για να τροποποιήσετε τη γραμματοσειρά και το στυλ, προσαρμόστε τις ιδιότητες του αντικειμένου `CadText` πριν το προσθέσετε στο αρχείο DWG.

### Ε4: Υπάρχουν ζητήματα αδειοδότησης για τη χρήση του Aspose.CAD σε εμπορικό έργο;

Α4: Ναι, βεβαιωθείτε ότι τηρείτε τους όρους αδειοδότησης του Aspose.CAD. Ανατρέξτε στην [Aspose.CAD Purchase](https://purchase.aspose.com/buy) για λεπτομέρειες.

### Ε5: Πού μπορώ να ζητήσω βοήθεια ή να συζητήσω ερωτήματα σχετικά με το Aspose.CAD;

Α5: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για να συνδεθείτε με την κοινότητα και να λάβετε υποστήριξη.

## Πρόσθετες Συχνές Ερωτήσεις

**Ε: Πώς δημιουργώ PDF από DWG χωρίς να προσθέσω κείμενο;**  
Α: Παραλείψτε το βήμα δημιουργίας `CadText` και διαμορφώστε απευθείας τις `PdfOptions` πριν καλέσετε `image.Save(...)`.

**Ε: Μπορώ να αλλάξω το χρώμα του κειμένου προγραμματιστικά;**  
Α: Ναι, ορίστε το `cadText.ColorId` σε συγκεκριμένο αριθμό χρώματος ACI (π.χ., 1 για κόκκινο).

**Ε: Είναι δυνατόν να εισάγετε κείμενο πολλαπλών γραμμών;**  
Α: Χρησιμοποιήστε `CadMText` για μπλοκ κειμένου πολλαπλών γραμμών· η προσέγγιση είναι παρόμοια με το `CadText`.

**Ε: Υποστηρίζει το Aspose.CAD μαζική μετατροπή πολλαπλών αρχείων DWG;**  
Α: Απόλυτα – κάντε βρόχο σε έναν φάκελο με αρχεία DWG, εφαρμόστε τα ίδια βήματα και αποθηκεύστε το καθένα ως PDF.

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή ροή εργασίας για **μετατροπή DWG σε PDF**, **προσθήκη προσαρμοσμένου κειμένου**, και **προσαρμογή εμφάνισης κειμένου** χρησιμοποιώντας C# και Aspose.CAD. Αυτή η τεχνική είναι ιδανική για αυτοματοποιημένη δημιουργία σχεδίων, pipelines αναφοράς, ή οποιοδήποτε σενάριο όπου χρειάζεται να εμπλουτίσετε αρχεία CAD άμεσα.

---

**Τελευταία ενημέρωση:** 2026-04-06  
**Δοκιμή με:** Aspose.CAD 24.11 for .NET  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}