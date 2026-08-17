---
date: 2026-08-17
description: Μάθετε πώς να προσθέσετε image σε αρχεία dwg χρησιμοποιώντας C# και Aspose.CAD
  για .NET. Αυτός ο οδηγός σας καθοδηγεί μέσω του importing images, του setting insertion
  points και του exporting σε PDF.
keywords:
- add image to dwg
- convert dwg to pdf
- set insertion point dwg
- embed png in dwg
- save dwg as pdf
lastmod: 2026-08-17
linktitle: Importing Images σε αρχεία DWG με C#
og_description: Μάθετε πώς να προσθέσετε image σε αρχεία dwg χρησιμοποιώντας C#. Αυτό
  το tutorial καλύπτει το importing images, το setting insertion points και το converting
  dwg σε pdf με Aspose.CAD.
og_image_alt: Guide showing C# code to embed an image into a DWG file using Aspose.CAD
og_title: Πώς να προσθέσετε image σε αρχεία dwg με C# χρησιμοποιώντας το Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-08-17'
  description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  headline: How to add image to dwg files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to add image to dwg files using C# and Aspose.CAD for .NET.
    This guide walks you through importing images, setting insertion points, and exporting
    to PDF.
  name: How to add image to dwg files with C# using Aspose.CAD
  steps:
  - name: set up your document directory
    text: Prepare the folder that contains the source DWG and the image you want to
      embed.
  - name: load the dwg file
    text: The `CadImage` class represents a DWG drawing and provides access to its
      entities, layers, and metadata.
  - name: define the image properties
    text: Create an `Image` object that points to the raster file (e.g., PNG) and
      specify its format.
  - name: set insertion point dwg and vectors
    text: Specify where the image should appear inside the drawing and how it should
      be scaled. The insertion point is defined by a 2‑D coordinate, while the vectors
      control width and height.
  - name: create and configure the raster image
    text: Instantiate a `RasterImage` object, assign the image data, and set any additional
      rendering options.
  - name: add image to dwg file
    text: Insert the configured raster image into the DWG’s entities collection so
      it becomes part of the drawing.
  - name: save as pdf (export dwg to pdf)
    text: After embedding the image you can **convert dwg to pdf** or **save dwg as
      pdf** with a single call. This is useful for sharing the drawing with stakeholders
      who don’t have CAD software.
  type: HowTo
- questions:
  - answer: The core library is .NET‑specific, but Aspose offers equivalent APIs for
      Java, Python and other platforms.
    question: Can I use Aspose.CAD for .NET with other programming languages?
  - answer: Yes, you can explore a free trial on the [Aspose free trial page](https://releases.aspose.com/).
    question: Is a free trial available for Aspose.CAD?
  - answer: The documentation is available in the [Aspose.CAD .NET API reference](https://reference.aspose.com/cad/net/).
    question: Where can I find detailed documentation for Aspose.CAD?
  - answer: Visit the [temporary license page](https://purchase.aspose.com/temporary-license/)
      to get a temporary license.
    question: How do I obtain a temporary license for Aspose.CAD?
  - answer: Yes, you can seek support and engage with the community in the [Aspose.CAD
      community forum](https://forum.aspose.com/c/cad/19).
    question: Are there community forums for Aspose.CAD support?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD
- Aspose.CAD
- C# image processing
- DWG manipulation
title: Πώς να προσθέσετε image σε αρχεία dwg με C# χρησιμοποιώντας το Aspose.CAD
url: /el/net/image-manipulation-and-rendering/importing-images-into-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να προσθέσετε εικόνα σε αρχεία dwg με C# χρησιμοποιώντας το Aspose.CAD

## Εισαγωγή

Η προσθήκη εικόνας σε αρχείο DWG είναι μια συνηθισμένη απαίτηση όταν χρειάζεται να εμπλουτίσετε τα CAD σχέδια με λογότυπα, φωτογραφίες ή raster γραφικά. Σε αυτό το μάθημα θα μάθετε πώς να **προσθέσετε εικόνα σε dwg** προγραμματιστικά χρησιμοποιώντας C# και Aspose.CAD για .NET, και προαιρετικά να μετατρέψετε το αποτέλεσμα σε PDF. Τα βήματα είναι χωρισμένα ώστε να μπορείτε να αντιγράψετε‑επικολλήσετε κάθε ενότητα στο δικό σας έργο.

## Γρήγορες απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται την εργασία;** Aspose.CAD for .NET.
- **Μπορώ να ενσωματώσω αρχεία PNG;** Ναι – PNG, JPEG, BMP και άλλες μορφές raster υποστηρίζονται.
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.
- **Υποστηρίζεται η εξαγωγή PDF;** Απόλυτα – μπορείτε να μετατρέψετε το ενημερωμένο DWG σε PDF με μία γραμμή.
- **Ποιες εκδόσεις .NET είναι συμβατές;** .NET Framework 4.6+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι ένα αρχείο DWG;

Ένα αρχείο DWG είναι η εγγενής δυαδική μορφή για σχέδια Autodesk AutoCAD, αποθηκεύοντας διανυσματική γεωμετρία, στρώσεις και μεταδεδομένα. Χρησιμοποιείται ευρέως στην αρχιτεκτονική, τη μηχανική και την κατασκευή, και το Aspose.CAD μπορεί να διαβάσει και να γράψει αυτή τη μορφή χωρίς να απαιτείται εγκατάσταση του AutoCAD.

## Γιατί να προσθέσετε εικόνα σε dwg με Aspose.CAD;

Το Aspose.CAD υποστηρίζει **πάνω από 50 μορφές εισόδου και εξόδου**, μπορεί να επεξεργαστεί αρχεία μεγαλύτερα από 500 MB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη, και παρέχει μια καθοριστική API που λειτουργεί σε περιβάλλοντα χωρίς γραφικό περιβάλλον. Αυτό καθιστά την μαζική επεξεργασία σχεδίων DWG γρήγορη και αξιόπιστη.

## Προαπαιτούμενα
- Βασικές γνώσεις προγραμματισμού C#.
- Aspose.CAD for .NET εγκατεστημένο. Μπορείτε να το κατεβάσετε από τη [Σελίδα λήψης Aspose.CAD for .NET](https://releases.aspose.com/cad/net/). Μπορείτε επίσης να εξερευνήσετε άλλα προϊόντα Aspose στη [σελίδα εκδόσεων Aspose](https://releases.aspose.com/).
- Ένα περιβάλλον ανάπτυξης όπως το Visual Studio 2022 ή νεότερο.

## Πώς να προσθέσετε εικόνα σε dwg χρησιμοποιώντας το Aspose.CAD;

Φορτώστε το στόχο DWG, δημιουργήστε ένα αντικείμενο raster εικόνας που περιγράφει την εικόνα που θέλετε να ενσωματώσετε, ορίστε το σημείο εισαγωγής και τα διανύσματα κλιμάκωσης, στη συνέχεια συνδέστε την εικόνα στο σχέδιο. Τέλος, αποθηκεύστε το τροποποιημένο DWG ή εξάγετέ το απευθείας σε PDF. Ολόκληρη η ροή εργασίας απαιτεί μόνο λίγες κλήσεις API και εκτελείται σε λιγότερο από ένα δευτερόλεπτο για τυπικά σχέδια 2‑σελίδων.

### Εισαγωγή ονοματοχώρων
```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

### Βήμα 1: ρυθμίστε τον φάκελο του εγγράφου σας
```csharp
string MyDir = "Your Document Directory";
```

### Βήμα 2: φορτώστε το αρχείο dwg
```csharp
string dwgPathToFile = MyDir + "Drawing11.dwg";
CadImage cadImage1 = (CadImage)Image.Load(dwgPathToFile);
```

### Βήμα 3: ορίστε τις ιδιότητες της εικόνας
```csharp
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.ObjectHandle = "A3B4";
```

### Βήμα 4: ορίστε το σημείο εισαγωγής dwg και τα διανύσματα
```csharp
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Βήμα 5: δημιουργήστε και διαμορφώστε την raster εικόνα
```csharp
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.ImageDefReference = "A3B4";
cadRasterImage.DisplayFlags = 7;
cadRasterImage.ClippingState = 0;
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.ClipBoundaryVertexList.Add(new Cad2DPoint(639.5, 561.5));
```

### Βήμα 6: προσθέστε εικόνα στο αρχείο dwg
```csharp
CadImage cadImage = (CadImage)cadImage1;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadRasterImage);

List<CadBaseObject> list = new List<CadBaseObject>(cadImage.Objects);
list.Add(cadRasterImageDef);
cadImage.Objects = list.ToArray();
```

### Βήμα 7: αποθηκεύστε ως pdf (εξαγωγή dwg σε pdf)
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

## Πώς να μετατρέψετε dwg σε pdf μετά την ενσωμάτωση μιας εικόνας;

Καλέστε τη μέθοδο `Save` στο αντικείμενο `CadImage`, περνώντας `SaveFormat.Pdf` και προαιρετικά ένα αντικείμενο `PdfOptions` για να ελέγξετε το μέγεθος σελίδας, τη rasterization και τα μεταδεδομένα. Το Aspose.CAD διατηρεί την ενσωματωμένη raster εικόνα, τις στρώσεις και τα βάρη γραμμών, παράγοντας μια πιστή αναπαράσταση PDF που μπορεί να ανοιχθεί σε οποιονδήποτε προβολέα. Η μετατροπή αυτή γίνεται με μία μόνο γραμμή κώδικα.

## Συχνά προβλήματα και λύσεις
- **Η εικόνα εμφανίζεται σε λάθος θέση** – ελέγξτε ξανά τις συντεταγμένες του σημείου εισαγωγής και τα διανύσματα κατεύθυνσης· είναι σχετικές με το αρχικό σημείο του σχεδίου.
- **Μεγάλες εικόνες προκαλούν αυξήσεις μνήμης** – χρησιμοποιήστε την επιλογή `Resize` στην raster εικόνα πριν την εισαγωγή, ή δουλέψτε με αντίγραφο χαμηλότερης ανάλυσης.
- **Η εξαγωγή PDF χάνει την ποιότητα των διανυσμάτων** – βεβαιωθείτε ότι αποθηκεύετε με `PdfOptions` που διατηρούν τα διανύσματα· οι raster εικόνες ενσωματώνονται πάντα όπως είναι.

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το Aspose.CAD for .NET με άλλες γλώσσες προγραμματισμού;**  
Α: Η βασική βιβλιοθήκη είναι ειδική για .NET, αλλά η Aspose προσφέρει ισοδύναμες API για Java, Python και άλλες πλατφόρμες.

**Ε: Διατίθεται δωρεάν δοκιμή για το Aspose.CAD;**  
Α: Ναι, μπορείτε να δοκιμάσετε δωρεάν στη [σελίδα δωρεάν δοκιμής Aspose](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD;**  
Α: Η τεκμηρίωση είναι διαθέσιμη στην [αναφορά API Aspose.CAD .NET](https://reference.aspose.com/cad/net/).

**Ε: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD;**  
Α: Επισκεφθείτε τη [σελίδα προσωρινής άδειας](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε προσωρινή άδεια.

**Ε: Υπάρχουν φόρουμ κοινότητας για υποστήριξη Aspose.CAD;**  
Α: Ναι, μπορείτε να ζητήσετε υποστήριξη και να συμμετάσχετε στην κοινότητα στο [φόρουμ κοινότητας Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Last Updated:** 2026-08-17  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF ή Raster Images - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [Εξαγωγή DWG σε μορφή DXF σε C# - Μαθήματα Aspose.CAD](/cad/net/advanced-export-techniques/exporting-dwg-to-dxf/)
- [Εξαγωγή Συγκεκριμένων Διατάξεων σε PDF - Οδηγός Aspose.CAD](/cad/net/advanced-export-techniques/exporting-specific-layouts-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}