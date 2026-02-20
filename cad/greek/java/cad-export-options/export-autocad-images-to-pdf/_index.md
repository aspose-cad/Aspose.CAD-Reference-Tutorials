---
date: 2026-02-20
description: Μάθετε πώς να εξάγετε PDF AutoCAD χρησιμοποιώντας το Aspose.CAD for Java.
  Αυτός ο οδηγός βήμα‑βήμα σας δείχνει πώς να **μετατρέψετε DWG σε PDF**, **αποθηκεύσετε
  CAD ως PDF**, και να διαχειριστείτε την άδεια.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Μετατροπή DWG σε PDF - Εξαγωγή εικόνων AutoCAD σε PDF με το Aspose.CAD για
  Java
url: /el/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

 craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή AutoCAD PDF - Εξαγωγή εικόνων AutoCAD σε PDF με Aspose.CAD για Java

## Εισαγωγή

Αναζητάτε **να μετατρέψετε DWG σε PDF** χρησιμοποιώντας Java; Μην ψάχνετε άλλο! Σε αυτό το tutorial θα σας καθοδηγήσουμε στη μετατροπή εικόνων AutoCAD σε PDF με το Aspose.CAD για Java, μια ισχυρή βιβλιοθήκη που κάνει τη διαδικασία **convert DWG to PDF** απλή. Στο τέλος θα καταλάβετε πώς να **save CAD as PDF**, να εφαρμόσετε προσαρμοσμένες ρυθμίσεις rasterization και να εργαστείτε με μια άδεια Aspose.CAD για παραγωγική χρήση.

## Γρήγορες Απαντήσεις
- **Μπορώ να μετατρέψω DWG σε PDF με Java;** Ναι, το Aspose.CAD for Java διαχειρίζεται DWG, DXF και πολλές άλλες μορφές.  
- **Χρειάζεται άδεια;** Απαιτείται **Aspose CAD license** για απεριόριστη χρήση· διατίθεται προσωρινή άδεια για αξιολόγηση.  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8+ (η βιβλιοθήκη είναι συμβατή με όλα τα σύγχρονα JDK).  
- **Μπορώ να προσαρμόσω το μέγεθος σελίδας PDF;** Απόλυτα – προσαρμόστε `pageWidth` και `pageHeight` στις επιλογές rasterization.  
- **Είναι δυνατή η rasterization 3‑D;** Ναι, ενεργοποιήστε `TypeOfEntities.Entities3D` για πλήρη 3‑D απόδοση.

## Τι είναι η **export autocad pdf**;
Η εξαγωγή AutoCAD PDF σημαίνει τη μετατροπή διανυσματικών σχεδίων CAD (DWG, DXF, DWF κ.λπ.) σε ένα φορητό έγγραφο PDF, διατηρώντας τα επίπεδα, τα βάρη γραμμών και προαιρετικά τη 3‑D γεωμετρία. Αυτό είναι χρήσιμο για την κοινή χρήση σχεδίων με πελάτες, την αρχειοθέτηση ή την εκτύπωση χωρίς την ανάγκη λογισμικού CAD.

## Γιατί να μετατρέψετε DWG σε PDF με Aspose.CAD για Java;
- **Πλήρης υποστήριξη μορφών** – λειτουργεί με DWG, DXF, DWF και πολλές άλλες.  
- **Χωρίς εξωτερικές εξαρτήσεις** – καθαρή βιβλιοθήκη Java, χωρίς native DLLs.  
- **Υψηλής ποιότητας rasterization** – έλεγχος DPI, μεγέθους σελίδας και διάταξης, ώστε να μπορείτε να **customize PDF page size** ώστε να ταιριάζει στις απαιτήσεις του έργου σας.  
- **Ευελιξία αδειών** – ξεκινήστε με δωρεάν δοκιμή, στη συνέχεια αναβαθμίστε σε μόνιμη **Aspose CAD license**.  

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε:

- **Περιβάλλον Ανάπτυξης Java** – εγκατεστημένο JDK 8 ή νεότερο.  
- **Aspose.CAD for Java Library** – κατεβάστε από το [download link](https://releases.aspose.com/cad/java/).  
- **Φάκελο Εγγράφων** – έναν φάκελο στον υπολογιστή σας όπου θα αποθηκευτούν τα πηγαία αρχεία CAD και τα παραγόμενα PDF.

## Import Namespaces

Στο έργο Java, εισάγετε τις απαραίτητες κλάσεις για να εργαστείτε με το Aspose.CAD:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Τώρα ας περάσουμε από τον κώδικα βήμα προς βήμα.

## Πώς να μετατρέψετε DWG σε PDF με Aspose.CAD για Java

### Βήμα 1: Ορισμός Διαδρομής Φακέλου Πόρων

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Συμβουλή:** Αντικαταστήστε το `"Your Document Directory"` με την απόλυτη διαδρομή του φακέλου που δημιουργήσατε στα προαπαιτούμενα.

### Βήμα 2: Φόρτωση της Εικόνας CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Γιατί είναι σημαντικό:** Η φόρτωση του αρχείου CAD σε αντικείμενο `Image` σας δίνει πλήρη πρόσβαση στη μηχανή rasterization του Aspose.CAD.

### Βήμα 3: Ορισμός Ρυθμίσεων Rasterization

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Προσαρμόστε `pageWidth` και `pageHeight` για **customize PDF page size**.  
- Αποσχολιάστε τη γραμμή `setTypeOfEntities` εάν χρειάζεστε **java convert cad pdf** για οντότητες 3‑D.  
- Η κλήση `setLayouts` επιλέγει ποια διάταξη (Model, Layout1, κ.λπ.) θα αποδοθεί.

### Βήμα 4: Διαμόρφωση Επιλογών PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Αυτό συνδέει τις ρυθμίσεις rasterization με την έξοδο PDF, διασφαλίζοντας ότι τα διανυσματικά δεδομένα μετατρέπονται σωστά.

### Βήμα 5: Αποθήκευση του PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Το παραγόμενο αρχείο, `Export3DImagestoPDF_out_.pdf`, είναι μια **save cad as pdf** αναπαράσταση του αρχικού σχεδίου AutoCAD.

## Κοινά Προβλήματα & Λύσεις

| Συμπτωμα | Πιθανή Αιτία | Διόρθωση |
|----------|--------------|----------|
| Κενό PDF | Οι ρυθμίσεις rasterization δεν έχουν οριστεί ή υπάρχει ασυμφωνία διάταξης | Επαληθεύστε ότι το `setLayouts` ταιριάζει με το όνομα διάταξης στο αρχείο CAD. |
| Χαμηλής ανάλυσης εικόνα | `pageWidth`/`pageHeight` πολύ μικρά | Αυξήστε τις διαστάσεις ή ορίστε υψηλότερο DPI μέσω `rasterizationOptions.setResolution(...)`. |
| Εξαίρεση άδειας | Δεν έχει εφαρμοστεί έγκυρη άδεια | Εφαρμόστε μια **Aspose CAD license** ή χρησιμοποιήστε προσωρινή άδεια για δοκιμή. |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω Aspose.CAD για Java με άλλες μορφές αρχείων CAD;
A1: Ναι, το Aspose.CAD υποστηρίζει μια ευρεία γκάμα μορφών συμπεριλαμβανομένων DWG, DWF, DGN και άλλων, προσφέροντας ευελιξία στα έργα σας.

### Q2: Πώς μπορώ να αποκτήσω προσωρινή άδεια για Aspose.CAD για Java;
A2: Επισκεφθείτε [εδώ](https://purchase.aspose.com/temporary-license/) για να αποκτήσετε προσωρινή άδεια αξιολόγησης.

### Q3: Υπάρχουν επιλογές διάταξης για rasterization;
A3: Ναι, μπορείτε να προσαρμόσετε τις διατάξεις (π.χ. `"Model"`, `"Layout1"`) μέσω της μεθόδου `setLayouts` για να ελέγξετε ποια προβολή θα αποδοθεί.

### Q4: Μπορώ να προσαρμόσω το μέγεθος του παραγόμενου αρχείου PDF;
A4: Απόλυτα! Προσαρμόστε τις παραμέτρους `pageWidth` και `pageHeight` στις ρυθμίσεις rasterization ώστε να ταιριάζουν στις επιθυμητές διαστάσεις.

### Q5: Πού μπορώ να ζητήσω βοήθεια ή να συζητήσω προβλήματα σχετικά με Aspose.CAD για Java;
A5: Μεταβείτε στο [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για εξειδικευμένη υποστήριξη και συζητήσεις της κοινότητας.

---

**Τελευταία ενημέρωση:** 2026-02-20  
**Δοκιμασμένο με:** Aspose.CAD for Java 24.10  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}