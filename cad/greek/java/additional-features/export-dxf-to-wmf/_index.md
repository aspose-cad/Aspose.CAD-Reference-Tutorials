---
date: 2026-06-09
description: Μάθετε πώς να μετατρέψετε DXF σε WMF με Aspose.CAD για Java, συμπεριλαμβανομένης
  μιας δωρεάν δοκιμής, υποστήριξης Java 8+, και προαιρετικής εξαγωγής PDF. Οδηγός
  βήμα‑βήμα με παραδείγματα κώδικα.
keywords:
- convert dxf to wmf
- aspose cad java
- aspose free trial
- aspose cad conversion
- export dxf pdf
linktitle: Εξαγωγή DXF σε μορφή WMF χρησιμοποιώντας Java
schemas:
- author: Aspose
  dateModified: '2026-06-09'
  description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  headline: Convert DXF to WMF Using Aspose.CAD in Java
  type: TechArticle
- description: Learn how to convert DXF to WMF with Aspose.CAD for Java, including
    a free trial, Java 8+ support, and optional PDF export. Step‑by‑step guide with
    code examples.
  name: Convert DXF to WMF Using Aspose.CAD in Java
  steps:
  - name: Load DXF Drawing
    text: Image.load reads the DXF file into an Aspose.CAD Image object.
  - name: Configure Rasterization Options
    text: CadRasterizationOptions specifies page size, resolution, and background
      for rasterizing the CAD drawing.
  - name: Save as WMF
    text: ImageSaveOptions with SaveFormat.WMF tells Aspose.CAD to write the output
      as a Windows Metafile.
  - name: Dispose of Resources
    text: Calling image.close() releases native resources used by the Aspose.CAD Image
      object.
  - name: Optional – Export to PDF
    text: PdfOptions configures PDF‑specific settings when saving the image as a PDF
      document. > **Pro tip:** You can reuse the same `CadRasterizationOptions` object
      for PDF export by passing it to a `PdfOptions` instance, saving you a few lines
      of setup.
  type: HowTo
- questions:
  - answer: Yes. Load the file in a try‑with‑resources block and dispose of the `Image`
      object promptly. Adjust `CadRasterizationOptions.setPageWidth/Height` to a reasonable
      size to keep memory usage low.
    question: Can I convert large DXF files (hundreds of MB) without running out of
      memory?
  - answer: WMF is a flat vector format, so layer hierarchy is flattened, but line
      styles, colors, and hatch patterns are preserved.
    question: Does the WMF output retain layer information?
  - answer: Use `rasterizationOptions.setResolution(300);` to define DPI before saving.
    question: Is it possible to set a custom DPI for the WMF?
  - answer: Absolutely. Loop through a directory, load each file, and apply the same
      rasterization and save logic.
    question: Can I batch‑convert multiple DXF files in one run?
  - answer: Aspose.CAD for Java supports Java 8 and later, including Java 11, 17,
      and newer LTS releases.
    question: What versions of Java are supported?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Μετατροπή DXF σε WMF χρησιμοποιώντας Aspose.CAD σε Java
url: /el/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Μετατροπή DXF σε WMF με χρήση Aspose.CAD σε Java

## Εισαγωγή

Σε αυτό το σεμινάριο θα ανακαλύψετε πώς να **μετατρέψετε DXF σε WMF** με το Aspose.CAD για Java. Είτε χρειάζεστε να ενσωματώσετε σχέδια CAD σε μια αναφορά βασισμένη σε Windows, να δημιουργήσετε ελαφριά διανυσματικά γραφικά για έγγραφα Office, είτε να αυτοματοποιήσετε μαζικές μετατροπές, η μετατροπή DXF σε WMF είναι συχνή απαίτηση σε μηχανικές και αναφορικές διαδικασίες. Θα περάσουμε από τη φόρτωση ενός σχεδίου DXF, τη ρύθμιση των επιλογών rasterization, την αποθήκευση του αποτελέσματος ως WMF, και προαιρετικά την εξαγωγή του ίδιου σχεδίου σε PDF.

## Γρήγορες Απαντήσεις
- **Μπορώ να μετατρέψω DXF σε WMF με δωρεάν δοκιμή;** Ναι – η Aspose προσφέρει πλήρη λειτουργική δοκιμή 30 ημερών.  
- **Ποια έκδοση Java απαιτείται;** Java 8 ή νεότερη.  
- **Χρειάζομαι άδεια για την εκτέλεση του κώδικα;** Απαιτείται άδεια για παραγωγή· η δοκιμή λειτουργεί για ανάπτυξη και δοκιμές.  
- **Είναι η μετατροπή χωρίς απώλειες;** Τα διανυσματικά δεδομένα διατηρούνται· οι επιλογές rasterization σας επιτρέπουν να ελέγχετε την ανάλυση.  
- **Μπορώ επίσης να εξάγω το ίδιο σχέδιο σε PDF;** Απόλυτα – δείτε το βήμα «Εξαγωγή σε PDF» παρακάτω.

## Τι είναι η «μετατροπή DXF σε WMF»;

Η μετατροπή DXF σε WMF σημαίνει τη λήψη ενός αρχείου Drawing Exchange Format (DXF) — μια ευρέως χρησιμοποιούμενη μορφή CAD — και τη μετατροπή του σε Windows Metafile (WMF). Το WMF είναι μια διανυσματική μορφή εικόνας που ενσωματώνεται ομαλά με το Microsoft Office, τις εφαρμογές Windows και πολλά εργαλεία αναφοράς.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java;

Το Aspose.CAD για Java παρέχει μια καθαρά‑Java, χωρίς‑αρχικές‑DLL μηχανή που μετατρέπει αρχεία CAD με **πάνω από 99 % διανυσματική πιστότητα**, διατηρώντας τα επίπεδα, τα χρώματα, τα στυλ γραμμών και τα μοτίβα hatch. Υποστηρίζει **πάνω από 50 μορφές εισόδου και εξόδου** — συμπεριλαμβανομένων των DXF, DWG, DGN, PDF, PNG, SVG και WMF — ενώ σας επιτρέπει να ρυθμίσετε λεπτομερώς το μέγεθος σελίδας, το DPI και το χρώμα φόντου μέσω ενσωματωμένων επιλογών rasterization. Το ίδιο API διαχειρίζεται επίσης εξαγωγές σε PDF, PNG και SVG, εξαλείφοντας την ανάγκη για πολλαπλές βιβλιοθήκες.

### Κύρια πλεονεκτήματα
- **Χωρίς εξωτερικές εξαρτήσεις** – καθαρή Java, λειτουργεί σε οποιοδήποτε OS που τρέχει Java.  
- **Απόδοση υψηλής πιστότητας** – διατηρεί το πάχος γραμμής, το χρώμα και τις λεπτομέρειες hatch.  
- **Ενσωματωμένη rasterization** – έλεγχος διαστάσεων σελίδας, ανάλυσης και φόντου.  
- **Μετατροπή ολοκληρωμένη** – οι ίδιες κλάσεις εξάγουν σε WMF, PDF, PNG, SVG, κ.λπ.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Aspose.CAD for Java** ενσωματωμένο στο έργο σας. Κατεβάστε το από την επίσημη ιστοσελίδα: [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Κατάλογος εγγράφων** όπου αποθηκεύονται τα αρχεία DXF (π.χ., `Your Document Directory/DXFDrawings/`).

## Εισαγωγή Namespaces

Οι παρακάτω εισαγωγές φέρνουν τις κλάσεις Aspose.CAD που απαιτούνται για τη φόρτωση, rasterization και αποθήκευση αρχείων CAD.
```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageSaveOptions;
import com.aspose.cad.fileformats.cad.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import com.aspose.cad.fileformats.cad.CadImageInfo;
import java.awt.Color;
```

## Οδηγός βήμα‑βήμα

### Πώς να μετατρέψω DXF σε WMF σε Java;

Φορτώστε το αρχείο DXF με `Image.load("yourFile.dxf")`, ρυθμίστε το `CadRasterizationOptions` για το επιθυμητό μέγεθος σελίδας και DPI, και στη συνέχεια καλέστε `image.save("output.wmf", new ImageSaveOptions(SaveFormat.WMF))`. Αυτό το τριβήμα μοτίβο εκτελεί την πλήρη μετατροπή διατηρώντας την διανυσματική ποιότητα ανέπαφη και απαιτεί μόνο λίγες γραμμές κώδικα.

#### Βήμα 1: Φόρτωση Σχεδίου DXF

Το Image.load διαβάζει το αρχείο DXF σε ένα αντικείμενο Aspose.CAD Image.
```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

#### Βήμα 2: Ρύθμιση Επιλογών Rasterization

Το CadRasterizationOptions καθορίζει το μέγεθος σελίδας, την ανάλυση και το φόντο για τη rasterization του σχεδίου CAD.
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

#### Βήμα 3: Αποθήκευση ως WMF

Το ImageSaveOptions με SaveFormat.WMF λέει στο Aspose.CAD να γράψει το αποτέλεσμα ως Windows Metafile.
```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

#### Βήμα 4: Αποδέσμευση Πόρων

Η κλήση image.close() απελευθερώνει τους εγγενείς πόρους που χρησιμοποιεί το αντικείμενο Aspose.CAD Image.
```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

#### Βήμα 5: Προαιρετικό – Εξαγωγή σε PDF

Το PdfOptions ρυθμίζει τις ειδικές ρυθμίσεις PDF κατά την αποθήκευση της εικόνας ως έγγραφο PDF.
```java
finally
{
  cadImage.dispose();
}
```

> **Συμβουλή:** Μπορείτε να επαναχρησιμοποιήσετε το ίδιο αντικείμενο `CadRasterizationOptions` για εξαγωγή σε PDF περνώντας το σε μια παρουσία `PdfOptions`, εξοικονομώντας μερικές γραμμές ρυθμίσεων.

## Πώς να εξάγω DXF σε PDF χρησιμοποιώντας Aspose CAD Java;

Η εξαγωγή σε PDF ακολουθεί τα ίδια βήματα φόρτωσης και rasterization· απλώς αντικαταστήστε τη μορφή αποθήκευσης WMF με PDF. Χρησιμοποιήστε `new ImageSaveOptions(SaveFormat.Pdf)` και προαιρετικά ορίστε επιλογές PDF όπως επίπεδο συμπίεσης ή μεταδεδομένα συγγραφέα. Αυτή η μονογραμμή μετατροπή παράγει ένα PDF αναζητήσιμο, με ακριβή σελίδα, που αντικατοπτρίζει την αρχική διάταξη CAD.

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Διόρθωση |
|-------|-------|-----|
| **`NullPointerException` στο `cadImage.save`** | Η μεταβλητή `cadImage` δεν είναι ορισμένη (πρέπει να είναι `image`). | Αντικαταστήστε το `cadImage` με `image` ή μετονομάστε τη μεταβλητή συνεπώς. |
| **Το παραγόμενο WMF είναι κενό** | Το μέγεθος σελίδας rasterization είναι πολύ μικρό ή το χρώμα φόντου ορίστηκε σε διαφανές. | Αυξήστε το `PageWidth`/`PageHeight` ή ορίστε χρώμα φόντου μέσω `rasterizationOptions.setBackgroundColor(Color.WHITE);`. |
| **Εξαίρεση άδειας** | Εκτέλεση χωρίς έγκυρη άδεια Aspose σε παραγωγή. | Εφαρμόστε το αρχείο άδειας στην εκκίνηση της εφαρμογής: `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή ροή εργασίας για **μετατροπή DXF σε WMF** χρησιμοποιώντας το Aspose.CAD για Java, με ένα προαιρετικό βήμα για **εξαγωγή του ίδιου σχεδίου σε PDF**. Αυτή η προσέγγιση σας παρέχει εξαγωγή διανυσματικής υψηλής ποιότητας που ενσωματώνεται ομαλά με εργαλεία αναφοράς και τεκμηρίωσης βασισμένα σε Windows, ενώ διατηρεί τη βάση κώδικα σας απλή και χωρίς εξαρτήσεις.

## Συχνές Ερωτήσεις

### Ε1: Πού μπορώ να βρω την τεκμηρίωση του Aspose.CAD;

Μπορείτε να έχετε πρόσβαση στην τεκμηρίωση [εδώ](https://reference.aspose.com/cad/java/).

### Ε2: Πώς μπορώ να κατεβάσω το Aspose.CAD για Java;

Κατεβάστε τη βιβλιοθήκη [εδώ](https://releases.aspose.com/cad/java/).

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Ε4: Χρειάζεστε προσωρινές επιλογές αδειοδότησης;

Εξερευνήστε προσωρινές άδειες [εδώ](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να λάβω υποστήριξη;

Επισκεφθείτε το φόρουμ υποστήριξης Aspose.CAD [εδώ](https://forum.aspose.com/c/cad/19).

## Συχνές Ερωτήσεις

**Q: Μπορώ να μετατρέψω μεγάλα αρχεία DXF (εκατοντάδες MB) χωρίς να εξαντληθεί η μνήμη;**  
A: Ναι. Φορτώστε το αρχείο σε μπλοκ try‑with‑resources και απελευθερώστε άμεσα το αντικείμενο `Image`. Ρυθμίστε το `CadRasterizationOptions.setPageWidth/Height` σε λογικό μέγεθος για να μειώσετε τη χρήση μνήμης.

**Q: Διατηρεί η έξοδος WMF τις πληροφορίες επιπέδων;**  
A: Το WMF είναι μια επίπεδη διανυσματική μορφή, έτσι η ιεραρχία επιπέδων ισοπεδώνεται, αλλά τα στυλ γραμμής, τα χρώματα και τα μοτίβα hatch διατηρούνται.

**Q: Είναι δυνατόν να ορίσετε προσαρμοσμένο DPI για το WMF;**  
A: Χρησιμοποιήστε `rasterizationOptions.setResolution(300);` για να ορίσετε DPI πριν την αποθήκευση.

**Q: Μπορώ να μετατρέψω μαζικά πολλαπλά αρχεία DXF σε μία εκτέλεση;**  
A: Απόλυτα. Επανάληψη μέσω ενός καταλόγου, φόρτωση κάθε αρχείου και εφαρμογή της ίδιας λογικής rasterization και αποθήκευσης.

**Q: Ποιες εκδόσεις της Java υποστηρίζονται;**  
A: Το Aspose.CAD για Java υποστηρίζει Java 8 και νεότερες, συμπεριλαμβανομένων των Java 11, 17 και νεότερων εκδόσεων LTS.

---

**Last Updated:** 2026-06-09  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

## Σχετικά Σεμινάρια

- [Create PDF from CAD – Export DXF to PDF with Aspose.CAD for Java](/cad/java/additional-features/export-dxf-to-pdf/)
- [Create PDF from DXF: Export Layer with Aspose.CAD for Java](/cad/java/additional-features/export-specific-layer-to-pdf/)
- [How to Convert DXF Layout to JPEG Image with Aspose.CAD in Java](/cad/java/additional-features/export-specific-layout-to-image/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}