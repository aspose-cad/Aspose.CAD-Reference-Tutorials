---
date: 2026-01-07
description: Μάθετε πώς να εξάγετε CAD σε PDF και να μετατρέψετε DGN σε PDF χρησιμοποιώντας
  το Aspose.CAD για Java. Οδηγός βήμα‑προς‑βήμα για προγραμματιστές Java.
linktitle: Export Embedded DGN
second_title: Aspose.CAD Java API
title: Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με το Aspose.CAD για Java
url: /el/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή CAD σε PDF – Εξαγωγή ενσωματωμένου DGN με Aspose.CAD for Java

## Introduction

Σε αυτό το tutorial θα ανακαλύψετε **πώς να εξάγετε CAD σε PDF** μετατρέποντας ένα ενσωματωμένο αρχείο DGN σε ένα PDF υψηλής ποιότητας με το Aspose.CAD for Java. Το Aspose.CAD είναι μια ισχυρή βιβλιοθήκη που δίνει στους προγραμματιστές Java πλήρη έλεγχο πάνω στη διαχείριση αρχείων CAD, είτε χρειάζεστε **convert DGN to PDF**, **convert DWG to PDF**, είτε απλώς να αποδώσετε σχέδια CAD σε άλλες μορφές. Ακολουθήστε τον οδηγό βήμα‑βήμα παρακάτω και θα μπορείτε να ενσωματώσετε αυτή τη δυνατότητα στις εφαρμογές σας σε λίγα λεπτά.

## Quick Answers
- **Τι σημαίνει “εξαγωγή CAD σε PDF”;** Μετατρέπει τα σχέδια CAD (DWG, DGN κ.λπ.) σε αρχεία PDF διατηρώντας την ποιότητα των διανυσματικών δεδομένων.  
- **Ποια βιβλιοθήκη χρησιμοποιείται;** Aspose.CAD for Java.  
- **Χρειάζομαι άδεια;** Απαιτείται άδεια για παραγωγή· διατίθεται δωρεάν δοκιμή.  
- **Ποια είναι τα κύρια προαπαιτούμενα;** Περιβάλλον ανάπτυξης Java και το JAR του Aspose.CAD for Java.  
- **Μπορώ να προσαρμόσω το αποτέλεσμα;** Ναι – μπορείτε να επιλέξετε διατάξεις, να ορίσετε επιλογές rasterization και να ελέγξετε τις ρυθμίσεις PDF.

## What is “export CAD to PDF”?

Η εξαγωγή CAD σε PDF σημαίνει τη λήψη ενός εγγενούς αρχείου CAD (όπως DWG ή DGN) και τη δημιουργία ενός εγγράφου PDF που αναπαριστά πιστά τη γεωμετρία του αρχικού αρχείου. Το PDF μπορεί να προβληθεί σε οποιαδήποτε πλατφόρμα χωρίς την ανάγκη λογισμικού CAD, καθιστώντας το ιδανικό για κοινή χρήση, εκτύπωση ή αρχειοθέτηση.

## Why use Aspose.CAD for Java to convert DGN to PDF?
- **Χωρίς εξωτερικές εξαρτήσεις** – λειτουργεί αποκλειστικά σε Java.  
- **Διατηρεί τα διανυσματικά δεδομένα** – τα PDF παραμένουν καθαρά σε οποιοδήποτε επίπεδο ζουμ.  
- **Λεπτομερής έλεγχος** – επιλέξτε συγκεκριμένες διατάξεις, ορίστε DPI rasterization και ενσωματώστε γραμματοσειρές.  
- **Έτοιμο για επιχειρήσεις** – υποστηρίζει μεγάλα αρχεία, επεξεργασία δέσμης και επιλογές αδειοδότησης.

## Prerequisites

Πριν ξεκινήσουμε, βεβαιωθείτε ότι διαθέτετε τα εξής:

- **Περιβάλλον Ανάπτυξης Java** – εγκατεστημένο και ρυθμισμένο JDK 8 ή νεότερο.  
- **Aspose.CAD for Java** – κατεβάστε το πιο πρόσφατο JAR από [here](https://releases.aspose.com/cad/java/).

## Import Packages

Για να ξεκινήσετε, πρέπει να εισάγετε τις απαραίτητες κλάσεις στο έργο σας Java. Προσθέστε τις παρακάτω δηλώσεις import στο αρχείο πηγαίου κώδικα:

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

## How to export DGN to PDF using Aspose.CAD for Java?

Παρακάτω υπάρχει ένας σαφής, αριθμημένος οδηγός που δείχνει ακριβώς πώς να μετατρέψετε ένα ενσωματωμένο αρχείο DGN (αποθηκευμένο μέσα σε DWG) σε PDF.

### Step 1: Set Up Input and Output Paths

Ορίστε τον φάκελο που περιέχει το αρχείο προέλευσης και καθορίστε το DWG που περιέχει το ενσωματωμένο DGN.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Step 2: Load DWG File

Φορτώστε το αρχείο DWG σε ένα αντικείμενο `Image`. Το Aspose.CAD ανιχνεύει αυτόματα τα ενσωματωμένα δεδομένα DGN.

```java
Image objImage = Image.load(fileName);
```

### Step 3: Configure Rasterization Options

Επιλέξτε ποιες διατάξεις θέλετε να συμπεριλάβετε στο PDF. Σε αυτό το παράδειγμα εξάγουμε μόνο τη διάταξη **Model**.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Step 4: Configure PDF Options

Συνδέστε τις ρυθμίσεις rasterization με τις επιλογές εξαγωγής PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Step 5: Save PDF File

Τέλος, γράψτε το PDF στο δίσκο χρησιμοποιώντας τις διαμορφωμένες επιλογές```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Convert DWG to PDF – an additional tip

Αν το αρχείο προέλευσής σας είναι ένα απλό DWG (χωρίς ενσωματωμένο DGN), μπορείτε να επαναχρησιμοποιήσετε τον ίδιο κώδικα – απλώς αλλάξτε το `fileName` ώστε να δείχνει στο DWG που θέλετε να μετατρέψετε. Οι ρυθμίσεις rasterization και PDF παραμένουν ίδιες, παρέχοντάς σας μια συνεπή ροή εργασίας **convert DWG to PDF**.

## Common Issues and Solutions

| Issue | Reason | Solution |
|-------|--------|----------|
| **Blank PDF output** | Layout name mismatch | Verify that the layout name passed to `setLayouts` exactly matches the layout in the source file (case‑sensitive). |
| **License exception** | Using the trial without a license | Apply a valid Aspose.CAD license before loading the image (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **File not found** | Incorrect `dataDir` path | Use an absolute path or ensure the relative path is correct relative to the project’s working directory. |
| **Low‑resolution graphics** | Default rasterization DPI is low | Set `rasterizationOptions.setPageWidth/Height` or `setResolution` to increase DPI. |

## Frequently Asked Questions

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java σε εμπορικό έργο;**  
A: Ναι, το Aspose.CAD for Java είναι εμπορική βιβλιοθήκη. Μπορείτε να αποκτήσετε άδεια από [here](https://purchase.aspose.com/buy).

**Q: Υπάρχει διαθέσιμη δωρεάν δοκιμή;**  
A: Ναι, μπορείτε να αποκτήσετε δωρεάν δοκιμή του Aspose.CAD for Java [here](https://releases.aspose.com/).

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD for Java;**  
A: Μπορείτε να ζητήσετε υποστήριξη από την κοινότητα Aspose.CAD στο [forum](https://forum.aspose.com/c/cad/19).

**Q: Τι κάνω αν χρειάζομαι προσωρινή άδεια;**  
A: Μπορείτε να αποκτήσετε προσωρινή άδεια [here](https://purchase.aspose.com/temporary-license/).

**Q: Πού μπορώ να βρω την τεκμηρίωση;**  
A: Η τεκμηρίωση είναι διαθέσιμη [here](https://reference.aspose.com/cad/java/).

## Conclusion

Τώρα έχετε μάθει πώς να **εξάγετε CAD σε PDF**, συγκεκριμένα πώς να **convert DGN to PDF** και ακόμη και **convert DWG to PDF** χρησιμοποιώντας το Aspose.CAD for Java. Ακολουθώντας τα παραπάνω βήματα, μπορείτε να ενσωματώσετε αδιάλειπτη μετατροπή CAD‑σε‑PDF σε οποιαδήποτε λύση βασισμένη σε Java, παρέχοντας PDFs υψηλής ποιότητας στους χρήστες σας χωρίς την ανάγκη πρόσθετου λογισμικού CAD.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Τελευταία ενημέρωση:** 2026-01-07  
**Δοκιμή με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose