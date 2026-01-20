---
date: 2026-01-20
description: Μάθετε πώς να δημιουργείτε PDF από σχέδια CAD και να προσθέτετε υδατογράφημα
  σε σχέδιο CAD χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθήστε τον οδηγό βήμα‑βήμα
  μας για αδιάλειπτη ενσωμάτωση.
linktitle: Add Watermark
second_title: Aspose.CAD Java API
title: Δημιουργία PDF από CAD και Προσθήκη Υδατοσημάτων – Aspose.CAD για Java
url: /el/java/other-cad-operations/add-watermark/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία PDF από CAD και Προσθήκη Υδατογραφιών – Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το ολοκληρωμένο tutorial θα **δημιουργήσετε PDF από σχέδια CAD** και θα μάθετε **πώς να προσθέσετε υδατογράφημα σε σχέδιο CAD** χρησιμοποιώντας το Aspose.CAD για Java. Είτε χρειάζεστε να χρωματίσετε τα τεχνικά σας σχέδια, να προστατέψετε την πνευματική ιδιοκτησία, είτε απλώς να επισημάνετε ένα σχέδιο, αυτός ο οδηγός σας καθοδηγεί βήμα‑βήμα—from την προετοιμασία του περιβάλλοντος μέχρι την εξαγωγή του τελικού PDF.

## Γρήγορες Απαντήσεις
- **Τι καλύπτει αυτό το tutorial;** Προσθήκη κειμενικού υδατογραφήματος σε αρχείο CAD και εξαγωγή του ως PDF.  
- **Ποια βιβλιοθήκη απαιτείται;** Aspose.CAD για Java (τελευταία έκδοση).  
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 ή νεότερη.  
- **Πόσο διαρκεί η υλοποίηση;** Συνήθως κάτω από 15 λεπτά για ένα βασ## Τι είναι η «δημιουργία PDF από CAD»;

Η δημιουργία DXF κ.λπ.) σε ένα φορητό έγγραφο PDF. Το παραγόμενο PDF διατηρεί την ο σή το λογότυπο της εταιρείας ή μια ειδοποίηση εμπιστευτικότητας.  
- **Έλεγχος έκδοσης:** Σημειώστε σχέδια, αναθεωρήσεις ή κατάσταση «Εμπιστευτικό».  
- **Συμμόρφωση:** Ανταποκριθείτε σε κανονισμούς που απαιτούν σήμανση εγγράφων.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε:

- **Aspose.CAD για Java** – κατεβάστε το [εδώ](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – την τελευταία έκδοση του JDK εγκατεστημένη στο σύστημά σας.  

## Εισαγωγή Πακέτων

Στο έργο Java, εισάγετε τα απαραίτητα namespaces του Aspose.CAD:

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Πώς να δημιουργήσετε PDF από CAD με υδατογράφημα

### Βήμα 1: Προσθήκη νέου υδατογραφήματος MTEXT

Αρχικά, δημιουργούμε μια οντότητα `MTEXT` που θα λειτουργήσει ως ορατό υδατογράφημα στο σχέδιο.

```java
//add new MTEXT
CadMText watermark = new CadMText();
watermark.setText("Watermark message");
watermark.setInitialTextHeight(40);
watermark.setInsertionPoint(new Cad3DPoint(300, 40));
watermark.setLayerName("0");
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
```

*Συμβουλή:* Προσαρμόστε τις συντεταγμένες του `setInsertionPoint` ώστε να τοποθετήσετε το υδατογράφημα στο πιο κατάλληλο σημείο του layout.

### Βήμα 2: Προσθήκη απλής οντότητας Text (προαιρετικό)

Αν προτιμάτε ένα απλό κειμενικό υδατογράφημα, μπορείτε να προσθέσετε μια οντότητα `Text` αντί για `MTEXT`.

```java
// or add more simple entity like Text
CadText text = new CadText();
text.setDefaultValue("Watermark text");
text.setTextHeight(40);
text.setFirstAlignment(new Cad3DPoint(300, 40));
text.setLayerName("0") ;
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
```

### Βήμα 3: Εξαγωγή του σχεδίου CAD σε PDF

Μετά την ενσωμάτωση του υδατογραφήματος, rasterize το σχέδιο και αποθηκεύστε το ως αρχείο PDF.

```java
// export to pdf
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
rasterizationOptions.setLayouts(new String[]{"Model"});
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);
```

Το `CadRasterizationOptions`γχετε το μέγεθος εξόδου και τη διάταξη, διασφαλίζοντας ότι τοαίνει | Λύση |
|----------|----------------|------|
| Το υδατογράφημα δεν είναι ορατό | Η στρώση μπορεί να είναι κρυφή ή το χρώμα να ταιριίου. | Επαληθεύστε τις συντεταγμένες με `cadImage.getSize()` ή χρησιμοποιήστε `cadImage.getHeader().getLimits()` για ασφαλή όρια. |
| Το αρχείο PDF είναι μεγάλο | Rasterization σεοποιήστε vector rasterization (`rasterizationOptions.setVectorRasterizationOptions(true);`). |

## Συχνές Ερωτήσεις

### Ε1: Το Aspose.CAD είναιτυπα αρχείων CAD;

Α1: Το Aspose.CAD υποστηρίζει διάφορα μορφότυπα CAD, όπως DWG, DXF, DWT και DWF.

### Ε2: Μπορώ να προσαρμόσω την εμφάνιση του κειμένου του υδατογραφήματος;

Α2: Ναι, έχετε πλήρη έλεγχο πάνω στην εμφάνιση του υδατογραφήματος, συμπεριλαμβανομένου του μεγέθους κειμένου, χρώματος και θέσης.

### Ε3: Υπάρχει διαθέσιμη δοκιμαστική έκδοση για το Aspose.CAD για Java;

Α3: Ναι, μπορείτε να κατεβάσετε τη δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD;

Α4: Επισκεφθείτε το [φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για υποστήριξη από την κοινότητα.

### Ε5: Πού μπορώ να βρω την πλήρη τεκμηρίωση για το Aspose.CAD για Java;

Α5: Ανατρέξτε στην [τεκμηρίωση](https://reference.aspose.com/cad/java/) για λεπτομερείς πληροφορίες.

**Πρόσθετες Ερωτήσεις**

**Ε: Μπορώ να προσθέσω υδατογράφημα εικόνας αντί για κείμενο;**  
Α: Ναι. Χρησιμοποιήστε το `CadImage` για να εισάγετε μια εξωτερική εικόνα και προσθέστε τη ως raster οντότητα πριν την εξαγωγή.

**Ε: Πώς εφαρμόζω το ίδιο υδατογράφημα σε πολλά αρχεία CAD σε batch;**  
Α: Τοποθετήστε τον κώδικα δημιουργίας υδατογραφήματος μέσα σε βρόχο που φορτώνει κάθε αρχείο CAD, προσθέτει την οντότητα και αποθηκεύει το PDF.

**Ε: Είναι δυνατόν το PDF να παραμείνει vector‑based αντί για rasterized;**  
Α: Ορίστε `rasterizationOptions.setVectorRasterizationOptions(true);` για να διατηρήσετε τα vector δεδομένα όπου υποστηρίζονται.

## Συμπέρασμα

Τώρα έχετε κατακτήσει πώς να **δημιουργήσετε PDF από σχέδια CAD** και να **προσθέσετε υδατογράφημα σε σχέδιο CAD** χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθώντας αυτά τα βήματα μπορείτε να προστατεύσετε τα σχέδιά σας, να ενισχύσετε το branding και να μοιραστείτε επαγγελματικά PDF με σιγουριά.

---

**Τελευταία ενημέρωση:** 2026-01-20  
**Δοκιμάστηκε με:** Aspose.CAD για Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}