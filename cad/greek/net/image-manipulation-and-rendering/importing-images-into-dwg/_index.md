---
title: Εισαγωγή εικόνων σε αρχεία DWG με C# - Οδηγός Aspose.CAD
linktitle: Εισαγωγή εικόνων σε αρχεία DWG με C#
second_title: Aspose.CAD .NET - Μορφή αρχείου CAD και BIM
description: Μάθετε να εισάγετε εικόνες σε αρχεία DWG χρησιμοποιώντας C# με το Aspose.CAD για .NET. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για απρόσκοπτη ενσωμάτωση.
weight: 11
url: /el/net/image-manipulation-and-rendering/importing-images-into-dwg/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εισαγωγή εικόνων σε αρχεία DWG με C# - Οδηγός Aspose.CAD

## Εισαγωγή

Στον τομέα της σχεδίασης με τη βοήθεια υπολογιστή (CAD), η ενσωμάτωση εικόνων σε αρχεία DWG είναι μια κοινή και κρίσιμη εργασία. Το Aspose.CAD για .NET παρέχει ένα ισχυρό σύνολο εργαλείων για τον εξορθολογισμό αυτής της διαδικασίας, καθιστώντας το προσβάσιμο για προγραμματιστές C#. Σε αυτό το σεμινάριο, θα εξερευνήσουμε τον τρόπο εισαγωγής εικόνων σε αρχεία DWG βήμα προς βήμα.

## Προαπαιτούμενα

Πριν βουτήξετε στον οδηγό, βεβαιωθείτε ότι έχετε τα εξής:

- Βασικές γνώσεις προγραμματισμού C#.
-  Το Aspose.CAD για .NET έχει εγκατασταθεί. Μπορείτε να το κατεβάσετε[εδώ](https://releases.aspose.com/cad/net/).
- Δημιουργήθηκε ένα αναπτυξιακό περιβάλλον.

## Εισαγωγή χώρων ονομάτων

Φροντίστε να συμπεριλάβετε τους απαραίτητους χώρους ονομάτων στο έργο σας C#:

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Βήμα 1: Ρυθμίστε τον Κατάλογο Εγγράφων σας

```csharp
string MyDir = "Your Document Directory";
```

## Βήμα 2: Φορτώστε το αρχείο DWG

```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

## Βήμα 3: Καθορίστε τις ιδιότητες εικόνας

```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

## Βήμα 4: Ορίστε το σημείο εισαγωγής και τα διανύσματα

```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

## Βήμα 5: Δημιουργήστε και διαμορφώστε την εικόνα ράστερ

```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

## Βήμα 6: Προσθήκη εικόνας στο αρχείο DWG

```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

## Βήμα 7: Αποθήκευση ως PDF

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;

cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
cadImage1.Save(MyDir + "export2.pdf", pdfOptions);
```

## συμπέρασμα

Η ενσωμάτωση εικόνων σε αρχεία DWG χρησιμοποιώντας C# και Aspose.CAD για .NET είναι μια απρόσκοπτη διαδικασία, που δίνει τη δυνατότητα στους προγραμματιστές να βελτιώσουν τα έργα τους CAD με οπτικά στοιχεία χωρίς κόπο.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για .NET με άλλες γλώσσες προγραμματισμού;

A1: Το Aspose.CAD έχει σχεδιαστεί κυρίως για .NET, αλλά το Aspose παρέχει βιβλιοθήκες για διάφορες γλώσσες προγραμματισμού.

### Ε2: Διατίθεται δωρεάν δοκιμή για το Aspose.CAD για .NET;

 A2: Ναι, μπορείτε να εξερευνήσετε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε3: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD;

 A3: Η τεκμηρίωση είναι διαθέσιμη[εδώ](https://reference.aspose.com/cad/net/).

### Ε4: Πώς μπορώ να αποκτήσω μια προσωρινή άδεια χρήσης για το Aspose.CAD για .NET;

 Α4: Επίσκεψη[αυτός ο σύνδεσμος](https://purchase.aspose.com/temporary-license/) να πάρει προσωρινή άδεια.

### Ε5: Υπάρχουν φόρουμ κοινότητας για υποστήριξη Aspose.CAD;

 A5: Ναι, μπορείτε να αναζητήσετε υποστήριξη και να ασχοληθείτε με την κοινότητα[εδώ](https://forum.aspose.com/c/cad/19).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
