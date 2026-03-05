---
date: 2026-03-05
description: Μάθετε πώς να εξάγετε DWG σε PDF, να ενεργοποιήσετε τις κρυφές γραμμές
  και να μετατρέψετε DWG σε PDF με το Aspose.CAD για Java σε αυτόν τον οδηγό βήμα‑βήμα.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Εξαγωγή DWG σε PDF με κρυφές γραμμές – Aspose.CAD για Java
url: /el/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DWG σε PDF με Κρυφές Γραμμές – Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **εξάγετε dwg σε pdf** διατηρώντας τις κρυφές γραμμές χρησιμοποιώντας το Aspose.CAD για Java. Είτε χρειάζεστε να **μετατρέψετε DWG σε PDF**, να δημιουργήσετε έναν οδηγό σε στυλ **dwg to pdf tutorial**, είτε απλώς να **αποθηκεύσετε DWG ως PDF** με υποστήριξη κρυφών γραμμών, θα σας καθοδηγήσουμε βήμα προς βήμα. Στο τέλος, θα έχετε μια έτοιμη λύση που μπορείτε να ενσωματώσετε σε οποιοδήποτε έργο Java.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Ενεργοποίηση της απόδοσης κρυφών γραμμών κατά την εξαγωγή DWG σε PDF με το Aspose.CAD για Java.  
- **Ποια κύρια λειτουργία εκτελείται;** `export dwg to pdf`.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια είναι τα προαπαιτούμενα;** Περιβάλλον ανάπτυξης Java, βιβλιοθήκη Aspose.CAD για Java και αρχεία DWG.  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για μια βασική ρύθμιση.

## Τι είναι η «εξαγωγή dwg σε pdf»;
Η εξαγωγή ενός αρχείου DWG σε PDF μετατρέπει το διανυσματικό σχέδιο CAD σε μορφή φορητού εγγράφου, διατηρώντας τα επίπεδα, τους τύπους γραμμών και την προαιρετική απόδοση κρυφών γραμμών. Αυτό διευκολύνει την κοινή χρήση σχεδίων CAD με ενδιαφερόμενους που ενδέχεται να μην διαθέτουν λογισμικό CAD.

## Πώς να Ενεργοποιήσετε τις Κρυφές Γραμμές Κατά την Εξαγωγή DWG σε PDF
Οι κρυφές γραμμές ελέγχονται μέσω της ρύθμισης layout στις επιλογές rasterization. Επιλέγοντας το layout **Model**, το Aspose.CAD ενημερώνει τον renderer να αντιμετωπίζει τις κρυφές άκρες ως αόρατες, παρέχοντάς σας μια καθαρή 2‑Δ αναπαράσταση ενός 3‑Δ μοντέλου.

## Γιατί να ενεργοποιήσετε τις κρυφές γραμμές κατά την εξαγωγή;
Οι κρυφές γραμμές παρέχουν μια πιο σαφή οπτική αναπαράσταση σύνθετων 3‑Δ μοντέλων σε μια 2‑Δ σελίδα, διασφαλίζοντας ότι μόνο οι ορατές άκρες τονίζονται. Αυτό βελτιώνει την αναγνωσιμότητα και συχνά απαιτείται για τεχνική τεκμηρίωση.

## Προαπαιτούμενα

1. **Aspose.CAD for Java** – κατεβάστε τη βιβλιοθήκη από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/cad/java/).  
2. **Αρχεία DWG** – διατηρήστε τα αρχικά σχέδια DWG αποθηκευμένα σε γνωστό φάκελο.  
3. **Περιβάλλον ανάπτυξης Java** – JDK 8+ και το προτιμώμενο IDE σας (Eclipse, IntelliJ κ.λπ.).  

Τώρα που έχετε ρυθμίσει τα πάντα, ας βουτήξουμε στον κώδικα.

## Import Namespaces

Ξεκινήστε εισάγοντας τις απαραίτητες κλάσεις ώστε να μπορείτε να εργαστείτε με εικόνες CAD και επιλογές PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Step 1: Set Up Your Project

Δημιουργήστε ένα έργο Java και προσθέστε το JAR του Aspose.CAD στο μονοπάτι κατασκευής. Στη συνέχεια ορίστε το φάκελο που περιέχει τα αρχεία DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Συμβουλή:** Χρησιμοποιήστε απόλυτη διαδρομή ή ρυθμίστε σχετική διαδρομή βάσει του φακέλου πόρων του έργου σας.

## Step 2: Load DWG File

Φορτώστε το πηγαίο αρχείο DWG σε ένα αντικείμενο `CadImage` ώστε να μπορείτε να το επεξεργαστείτε.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Step 3: Configure Rasterization Options

Επιλέξτε τα επίπεδα που θέλετε να συμπεριλάβετε και ορίστε το μέγεθος σελίδας ώστε να ταιριάζει με το αρχικό σχέδιο. Εδώ ενεργοποιούμε την απόδοση κρυφών γραμμών καθορίζοντας το layout.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Step 4: Set PDF Options

Ενημερώστε το Aspose.CAD να rasterize τα διανυσματικά δεδομένα σε PDF, χρησιμοποιώντας το layout “Model” για να διατηρήσει τις κρυφές γραμμές κρυφές.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Step 5: Save the Result

Τέλος, εξάγετε το DWG ως αρχείο PDF. Οι κρυφές γραμμές θα τηρηθούν σύμφωνα με το layout που ορίσατε.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Συνηθισμένο λάθος:** Αν ξεχάσετε να ορίσετε το layout σε `"Model"` όλες οι γραμμές (συμπεριλαμβανομένων των κρυφών) θα εμφανιστούν συμπαγείς στο PDF.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Γιατί συμβαίνει | Πώς να διορθώσετε |
|----------|----------------|-------------------|
| Το PDF εμφανίζει όλες τις γραμμές συμπαγείς | Το layout δεν έχει οριστεί σε **Model** | Βεβαιωθείτε ότι καλείται `rasterizationOptions.setLayouts(new String[] { "Model" });` πριν από την αποθήκευση. |
| Απουσία επιπέδων στο αποτέλεσμα | Λανθασμένα ονόματα επιπέδων | Επαληθεύστε τα ονόματα των επιπέδων στο αρχείο DWG και ταιριάξτε τα ακριβώς στη `list`. |
| Σφάλμα έλλειψης μνήμης σε μεγάλα αρχεία | Μεγάλο μέγεθος rasterization | Μειώστε τις διαστάσεις της σελίδας ή επεξεργαστείτε το σχέδιο σε τμήματα αν είναι δυνατόν. |

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλες μορφές αρχείων CAD;
A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD όπως DWG, DXF, DWF κ.λπ.

### Q2: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD για Java;
A2: Ναι, μπορείτε να βρείτε τη δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;
A3: Επισκεφθείτε το φόρουμ Aspose.CAD [εδώ](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα.

### Q4: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD για Java;
A4: Ανατρέξτε στην τεκμηρίωση [εδώ](https://reference.aspose.com/cad/java/).

### Q5: Μπορώ να αγοράσω προσωρινή άδεια για το Aspose.CAD για Java;
A5: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q6: Λειτουργεί αυτή η μέθοδος επίσης για τη μετατροπή DWG σε PDF σε περιβάλλον server χωρίς UI;
A6: Απολύτως. Δεδομένου ότι ο κώδικας χρησιμοποιεί μόνο το API του Aspose.CAD, εκτελείται χωρίς εξαρτήσεις UI, καθιστώντας το ιδανικό για αυτοματοποίηση στο server‑side.

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή μέθοδο για **εξαγωγή dwg σε pdf** με υποστήριξη κρυφών γραμμών χρησιμοποιώντας το Aspose.CAD για Java. Αυτή η προσέγγιση μπορεί να ενσωματωθεί σε εργαλεία μαζικής επεξεργασίας, web services ή εφαρμογές desktop για αυτοματοποίηση της μετατροπής CAD‑σε‑PDF.

---

**Τελευταία ενημέρωση:** 2026-03-05  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}