---
date: 2026-01-02
description: Μάθετε πώς να εξάγετε DWG ως PDF, να ενεργοποιήσετε τις κρυφές γραμμές
  και να μετατρέψετε DWG σε PDF με το Aspose.CAD για Java σε αυτό το βήμα‑βήμα οδηγό.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Εξαγωγή DWG ως PDF με κρυφές γραμμές – Aspose.CAD για Java
url: /el/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή DWG ως PDF με Κρυφές Γραμμές – Aspose.CAD for Java

## Εισαγωγή

Σε αυτό το tutorial θα μάθετε πώς να **εξάγετε DWG ως PDF** διατηρώντας τις κρυφές γραμμές χρησιμοποιώντας το Aspose.CAD for Java. Είτε χρειάζεστε να **μετατρέψετε DWG σε PDF**, να δημιουργήσετε έναν οδηγό σε στυλ **dwg to pdf tutorial**, είτε απλώς να **αποθηκεύσετε DWG ως PDF** με υποστήριξη κρυφών γραμμών, θα σας καθοδηγήσουμε βήμα προς βήμα. Στο τέλος, θα έχετε μια έτοιμη προς χρήση λύση που μπορείτε να ενσωματώσετε σε οποιοδήποτε έργο Java.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Ενεργοποίηση της απόδοσης κρυφών γραμμών κατά την εξαγωγή DWG σε PDF με το Aspose.CAD for Java.  
- **Ποια κύρια λειτουργία εκτελείται;** `export dwg as pdf`.  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια είναι τα προαπαιτούμενα;** Περιβάλλον ανάπτυξης Java, βιβλιοθήκη Aspose.CAD for Java και αρχεία DWG.  
- **Πόσο χρόνο απαιτεί η υλοποίηση;** Περίπου 10‑15 λεπτά για μια βασική ρύθμιση.

## Τι είναι η “export dwg as pdf”;
Η εξαγωγή ενός αρχείου DWG σε PDF μετατρέπει το διανυσματικό CAD σχέδιο σε μορφή φορητού εγγράφου, διατηρώντας τα επίπεδα, τους τύπους γραμμών και την προαιρετική απόδοση κρυφών γραμμών. Αυτό διευκολύνει την κοινή χρήση σχεδίων CAD με ενδιαφερόμενους που ενδέχεται να μην διαθέτουν λογισμικό CAD.

## Γιατί να ενεργοποιήσετε τις κρυφές γραμμές κατά την εξαγωγή;
Οι κρυφές γραμμές παρέχουν πιο σαφή οπτική αναπαράσταση σύνθετων 3D μοντέλων σε μια 2‑D σελίδα, διασφαλίζοντας ότι τονίζονται μόνο οι ορατές άκρες. Αυτό βελτιώνει την αναγνωσιμότητα και συχνά απαιτείται για τεχνική τεκμηρίωση.

## Προαπαιτούμενα

1. **Aspose.CAD for Java** – κατεβάστε τη βιβλιοθήκη από την επίσημη ιστοσελίδα [εδώ](https://releases.aspose.com/cad/java/).  
2. **Αρχεία DWG** – διατηρήστε τα πηγαία σχέδια DWG αποθηκευμένα σε γνωστό φάκελο.  
3. **Περιβάλλον ανάπτυξης Java** – JDK 8+ και το προτιμώμενο IDE σας (Eclipse, IntelliJ, κλπ.).  

Τώρα που έχετε ρυθμίσει τα πάντα, ας βουτήξουμε στον κώδικα.

## Εισαγωγή Namespaces
Ξεκινήστε εισάγοντας τις απαραίτητες κλάσεις ώστε να μπορείτε να εργαστείτε με εικόνες CAD και επιλογές PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Βήμα 1: Ρύθμιση του Έργου σας

Δημιουργήστε ένα έργο Java και προσθέστε το JAR του Aspose.CAD στο μονοπάτι κατασκευής. Στη συνέχεια ορίστε τον φάκελο που περιέχει τα αρχεία DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Συμβουλή:** Χρησιμοποιήστε απόλυτη διαδρομή ή ρυθμίστε σχετική διαδρομή βάσει του φακέλου πόρων του έργου σας.

## Βήμα 2: Φόρτωση Αρχείου DWG

Φορτώστε το πηγαίο αρχείο DWG σε ένα αντικείμενο `CadImage` ώστε να μπορείτε να το επεξεργαστείτε.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Βήμα 3: Διαμόρφωση Επιλογών Rasterization

Επιλέξτε τα επίπεδα που θέλετε να συμπεριλάβετε και ορίστε το μέγεθος σελίδας ώστε να ταιριάζει με το αρχικό σχέδιο. Εδώ ενεργοποιούμε την απόδοση κρυφών γραμμών καθορίζοντας τη διάταξη.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Βήμα 4: Ορισμός Επιλογών PDF

Ενημερώστε το Aspose.CAD να rasterize τα διανυσματικά δεδομένα σε PDF, χρησιμοποιώντας τη διάταξη “Model” για να διατηρήσει τις κρυφές γραμμές κρυφές.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Βήμα 5: Αποθήκευση Αποτελέσματος

Τέλος, εξάγετε το DWG ως αρχείο PDF. Οι κρυφές γραμμές θα τηρηθούν σύμφωνα με τη διάταξη που ορίσατε.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Κοινό Παράπτωμα:** Η παράλειψη ορισμού της διάταξης σε `"Model"` θα κάνει όλες τις γραμμές (συμπεριλαμβανομένων των κρυφών) να εμφανίζονται στερεές στο PDF.

## Συμπέρασμα

Τώρα έχετε μια πλήρη, έτοιμη για παραγωγή μέθοδο για **εξαγωγή DWG ως PDF** με υποστήριξη κρυφών γραμμών χρησιμοποιώντας το Aspose.CAD for Java. Αυτή η προσέγγιση μπορεί να ενσωματωθεί σε εργαλεία επεξεργασίας δέσμης, web services ή εφαρμογές επιφάνειας εργασίας για αυτοματοποίηση της μετατροπής CAD‑σε‑PDF.

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java με άλλες μορφές αρχείων CAD;
A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD όπως DWG, DXF, DWF και άλλες.

### Q2: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD for Java;
A2: Ναι, μπορείτε να βρείτε τη δωρεάν δοκιμή [εδώ](https://releases.aspose.com/).

### Q3: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD for Java;
A3: Επισκεφθείτε το φόρουμ Aspose.CAD [εδώ](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα.

### Q4: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD for Java;
A4: Ανατρέξτε στην τεκμηρίωση [εδώ](https://reference.aspose.com/cad/java/).

### Q5: Μπορώ να αγοράσω προσωρινή άδεια για το Aspose.CAD for Java;
A5: Ναι, μπορείτε να αποκτήσετε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

### Q6: Λειτουργεί αυτή η μέθοδος επίσης για τη μετατροπή DWG σε PDF σε περιβάλλον server χωρίς UI;
A6: Απόλυτα. Δεδομένου ότι ο κώδικας χρησιμοποιεί μόνο το API του Aspose.CAD, εκτελείται χωρίς εξαρτήσεις UI, καθιστώντας το ιδανικό για αυτοματοποίηση στο server‑side.

---

**Τελευταία ενημέρωση:** 2026-01-02  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}