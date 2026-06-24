---
date: 2026-06-14
description: Μάθετε πώς να εξάγετε CAD σε PDF και να μετατρέψετε DGN σε PDF χρησιμοποιώντας
  το Aspose.CAD for Java. Οδηγός βήμα προς βήμα για προγραμματιστές Java.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Εξαγωγή ενσωματωμένου DGN
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με Aspose.CAD for Java
url: /el/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε **πώς να εξάγετε CAD σε PDF** μετατρέποντας ένα ενσωματωμένο αρχείο DGN σε ένα έγγραφο PDF υψηλής ποιότητας με το Aspose.CAD για Java. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που δίνει στους προγραμματιστές Java πλήρη έλεγχο πάνω στη διαχείριση αρχείων CAD, είτε χρειάζεστε **να μετατρέψετε DGN σε PDF**, **να μετατρέψετε DWG σε PDF**, ή απλώς να αποδώσετε σχέδια CAD σε άλλες μορφές. Ακολουθήστε τον οδηγό βήμα προς βήμα παρακάτω και θα μπορείτε να ενσωματώσετε αυτή τη δυνατότητα στις εφαρμογές σας σε λίγα λεπτά.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “export CAD to PDF”;** Μετατρέπει τα σχέδια CAD (DWG, DGN κ.λπ.) σε αρχεία PDF διατηρώντας την ποιότητα των διανυσματικών στοιχείων.  
- **Ποια βιβλιοθήκη χρησιμοποιείται;** Aspose.CAD for Java.  
- **Χρειάζομαι άδεια;** Απαιτείται άδεια για παραγωγική χρήση· διατίθεται δωρεάν δοκιμαστική έκδοση.  
- **Ποιες είναι οι κύριες προαπαιτήσεις;** Περιβάλλον ανάπτυξης Java και το JAR του Aspose.CAD for Java.  
- **Μπορώ να προσαρμόσω το αποτέλεσμα;** Ναι – μπορείτε να επιλέξετε διατάξεις, να ορίσετε επιλογές rasterization και να ελέγξετε τις ρυθμίσεις PDF.

## Τι είναι η “εξαγωγή CAD σε PDF”;

Η εξαγωγή CAD σε PDF μετατρέπει ένα εγγενές σχέδιο CAD (DWG, DGN κ.λπ.) σε αρχείο PDF που διατηρεί τη αρχική διανυσματική γεωμετρία, τα στρώματα και τη διάταξη, επιτρέποντας σε οποιονδήποτε να προβάλλει, εκτυπώσει ή μοιραστεί το σχέδιο χωρίς λογισμικό CAD. Αυτή η μετατροπή δημιουργεί ένα ανεξάρτητο από πλατφόρμα έγγραφο που φαίνεται ταυτόσημο σε οποιοδήποτε επίπεδο μεγέθυνσης, καθιστώντας το ιδανικό για συνεργασία και αρχειοθέτηση.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java για τη μετατροπή DGN σε PDF;

Το Aspose.CAD για Java παρέχει μια καθαρά Java λύση που εξαλείφει την ανάγκη για εξωτερικά εργαλεία CAD, εξασφαλίζει ακριβή διανυσματική πιστότητα στα παραγόμενα PDF και προσφέρει εκτενείς επιλογές διαμόρφωσης όπως επιλογή διάταξης, έλεγχο DPI και ενσωμάτωση γραμματοσειρών, καθιστώντας το ιδανικό τόσο για απλές όσο και για επιχειρησιακές μετατροπές μεγάλης κλίμακας.

- **Χωρίς εξωτερικές εξαρτήσεις** – λειτουργεί αποκλειστικά σε Java σε οποιοδήποτε λειτουργικό σύστημα.  
- **Διατηρεί τα διανυσματικά δεδομένα** – τα PDF παραμένουν καθαρά σε οποιοδήποτε επίπεδο μεγέθυνσης.  
- **Λεπτομερής έλεγχος** – επιλέξτε συγκεκριμένες διατάξεις, ορίστε DPI rasterization και ενσωματώστε γραμματοσειρές.  
- **Έτοιμο για επιχειρήσεις** – υποστηρίζει αρχεία έως **2 GB**, επεξεργασία χιλιάδων σχεδίων σε batch και ευέλικτη αδειοδότηση.  

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

- **Περιβάλλον Ανάπτυξης Java** – εγκατεστημένο και ρυθμισμένο JDK 8 ή νεότερο.  
- **Aspose.CAD for Java** – κατεβάστε το τελευταίο JAR από [here](https://releases.aspose.com/cad/java/).

## Εισαγωγή Πακέτων

Οι δηλώσεις `import` φέρνουν τις απαιτούμενες κλάσεις του Aspose.CAD στο πεδίο ορατότητας.  
Η `Image` είναι η βασική κλάση που αντιπροσωπεύει οποιοδήποτε rasterizable αρχείο CAD, ενώ οι `PdfOptions` και `RasterizationOptions` σας επιτρέπουν να ρυθμίσετε λεπτομερώς την έξοδο PDF.  
Η `CadRasterizationOptions` καθορίζει τις παραμέτρους rasterization όπως DPI, μέγεθος σελίδας και διάταξη για την απόδοση CAD.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Πώς να εξάγετε CAD σε PDF χρησιμοποιώντας το Aspose.CAD για Java;

Η διαδικασία ξεκινά με τη φόρτωση του αρχείου DWG που περιέχει το ενσωματωμένο DGN, στη συνέχεια ορίζονται οι παράμετροι rasterization για να καθοριστεί η ανάλυση εξόδου και η διάταξη, τα παραπάνω συνδέονται με ένα αντικείμενο PdfOptions και τέλος καλείται η μέθοδος save για τη δημιουργία του PDF. Αυτή η προσέγγιση εξασφαλίζει αποτελέσματα υψηλής ποιότητας, διατηρώντας τα διανύσματα, με ελάχιστο κώδικα.

Παρακάτω υπάρχει ένας σαφής, αριθμημένος οδηγός που δείχνει ακριβώς πώς να μετατρέψετε ένα ενσωματωμένο αρχείο DGN (αποθηκευμένο μέσα σε DWG) σε PDF.

### Βήμα 1: Ορισμός Διαδρομών Εισόδου και Εξόδου

Ορίστε τον φάκελο που περιέχει το αρχείο προέλευσης και καθορίστε το DWG που περιέχει το ενσωματωμένο DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Βήμα 2: Φόρτωση Αρχείου DWG

Η `Image` φορτώνει το DWG και ανιχνεύει αυτόματα τυχόν ενσωματωμένα δεδομένα DGN, εκθέτοντάς τα για περαιτέρω επεξεργασία.

```java
Image objImage = Image.load(fileName);
```

### Βήμα 3: Διαμόρφωση Επιλογών Rasterization

Επιλέξτε ποια διάταξη(ες) θέλετε να συμπεριλάβετε στο PDF. Σε αυτό το παράδειγμα εξάγουμε μόνο τη διάταξη **Model**, η οποία είναι η πιο κοινή προβολή για τεχνικά σχέδια.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Βήμα 4: Διαμόρφωση Επιλογών PDF

Συνδέστε τις ρυθμίσεις rasterization με τις επιλογές εξαγωγής PDF ώστε το τελικό έγγραφο να σέβεται τη επιλεγμένη διάταξη και DPI.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 5: Αποθήκευση Αρχείου PDF

Τέλος, γράψτε το PDF στο δίσκο χρησιμοποιώντας τις ρυθμισμένες επιλογές. Η μέθοδος `save` γράφει την ρυθμισμένη εικόνα στη μορφή αρχείου προορισμού στο δίσκο.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Μετατροπή DWG σε PDF – μια επιπλέον συμβουλή

Αν το αρχείο προέλευσης είναι ένα απλό DWG (χωρίς ενσωματωμένο DGN), μπορείτε να επαναχρησιμοποιήσετε τον ίδιο κώδικα – απλώς αλλάξτε το `fileName` ώστε να δείχνει στο DWG που θέλετε να μετατρέψετε. Οι επιλογές rasterization και PDF παραμένουν ίδιες, παρέχοντάς σας μια συνεπή **convert DWG to PDF** ροή εργασίας.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| **Κενό PDF εξόδου** | Μη αντιστοίχιση ονόματος διάταξης | Επαληθεύστε ότι το όνομα διάταξης που περνάτε στο `setLayouts` ταιριάζει ακριβώς με τη διάταξη στο αρχείο προέλευσης (διάκριση πεζών-κεφαλαίων). |
| **Απόκλιση άδειας** | Χρήση της δοκιμαστικής έκδοσης χωρίς άδεια | Εφαρμόστε μια έγκυρη άδεια Aspose.CAD πριν φορτώσετε την εικόνα (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Αρχείο δεν βρέθηκε** | Λανθασμένη διαδρομή `dataDir` | Χρησιμοποιήστε απόλυτη διαδρομή ή βεβαιωθείτε ότι η σχετική διαδρομή είναι σωστή σε σχέση με τον φάκελο εργασίας του έργου. |
| **Γραφικά χαμηλής ανάλυσης** | Η προεπιλεγμένη DPI rasterization είναι χαμηλή | Ορίστε `rasterizationOptions.setResolution(300)` ή προσαρμόστε `setPageWidth/Height` για να αυξήσετε το DPI. |

## Συχνές Ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java σε εμπορικό έργο;**  
A: Ναι, το Aspose.CAD για Java είναι εμπορική βιβλιοθήκη. Μπορείτε να αποκτήσετε άδεια από [here](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμαστική έκδοση;**  
A: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμαστική έκδοση του Aspose.CAD για Java [here](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;**  
A: Μπορείτε να ζητήσετε υποστήριξη από την κοινότητα Aspose.CAD στο [forum](https://forum.aspose.com/c/cad/19).

**Q: Τι κάνω αν χρειάζομαι προσωρινή άδεια;**  
A: Μπορείτε να αποκτήσετε προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/).

**Q: Πού μπορώ να βρω την επίσημη τεκμηρίωση;**  
A: Η τεκμηρίωση είναι διαθέσιμη [here](https://reference.aspose.com/cad/java/).

## Συμπέρασμα

Τώρα έχετε μάθει πώς να **εξάγετε CAD σε PDF**, συγκεκριμένα πώς να **μετατρέψετε DGN σε PDF** και ακόμη και **να μετατρέψετε DWG σε PDF** χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθώντας τα παραπάνω βήματα, μπορείτε να ενσωματώσετε αδιάλειπτη μετατροπή CAD‑σε‑PDF σε οποιαδήποτε λύση βασισμένη σε Java, παρέχοντας PDF υψηλής ποιότητας στους χρήστες σας χωρίς την ανάγκη πρόσθετου λογισμικού CAD.

---

**Τελευταία ενημέρωση:** 2026-06-14  
**Δοκιμή με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή DGN σε DWG με Aspose.CAD για Java – Μάθημα](/cad/java/dgn-export-options/)
- [Απρόσκοπτη εξαγωγή DGN σε AutoCAD PDF με Aspose.CAD για Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg σε pdf java – Εξαγωγή CAD σε PDF με Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}