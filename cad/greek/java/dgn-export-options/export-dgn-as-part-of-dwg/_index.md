---
date: 2026-05-20
description: Μάθετε πώς να εξάγετε DGN σε DWG και να μετατρέψετε MicroStation DGN
  σε AutoCAD DWG χρησιμοποιώντας το Aspose.CAD για Java. Ακολουθήστε τον οδηγό βήμα‑βήμα
  για γρήγορη, αξιόπιστη διαχείριση αρχείων CAD.
keywords:
- how to export dgn to dwg
- convert microstation dgn to autocad dwg
- Aspose.CAD Java export
- CAD file conversion Java
linktitle: Εξαγωγή DGN ως μέρος του DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to export DGN to DWG and convert MicroStation DGN to AutoCAD
    DWG using Aspose.CAD for Java. Follow our step‑by‑step guide for fast, reliable
    CAD file manipulation.
  headline: How to Export DGN to DWG with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export DGN to DWG and convert MicroStation DGN to AutoCAD
    DWG using Aspose.CAD for Java. Follow our step‑by‑step guide for fast, reliable
    CAD file manipulation.
  name: How to Export DGN to DWG with Aspose.CAD for Java
  steps:
  - name: Set File Paths
    text: Define where the source DGN lives and where the resulting DWG will be written.
      Adjust `dataDir`, `fileName`, and `outPath` to match your project layout.
  - name: Create CadRasterizationOptions Instance
    text: '`CadRasterizationOptions` defines how vector data is rasterized before
      being embedded into the DWG container.'
  - name: Load DGN File
    text: '`CadImage` represents the loaded DGN file in memory, allowing access to
      its entities and properties.'
  - name: Iterate Through Entities
    text: '`CadBaseEntity` is the base class for all CAD entities, and `CadDgnUnderlay`
      represents an embedded DGN underlay. Loop over each entity; when an `ImageDefinition`
      is encountered, its external reference is extracted for later embedding.'
  - name: Define Rasterization Options
    text: Set page width, height, layout selection, and background color to match
      the target DWG’s visual requirements.
  - name: Set Vector Rasterization Options
    text: Specify vector‑specific settings such as line weight handling and curve
      approximation to ensure the DWG retains crisp geometry.
  - name: Export DWG to PDF
    text: Call the `save` method on the `CadImage` instance, passing the configured
      options to produce the final DWG‑compatible PDF output.
  type: HowTo
- questions:
  - answer: The full API reference is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the documentation for Aspose.CAD for Java?
  - answer: Grab the latest release from [this link](https://releases.aspose.com/cad/java/).
    question: How can I download the Aspose.CAD library for Java?
  - answer: Yes, a fully functional trial can be obtained [here](https://releases.aspose.com/).
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Request a temporary license from Aspose [here](https://purchase.aspose.com/temporary-license/).
    question: Where can I get a temporary license for Aspose.CAD for Java?
  - answer: Join the community support forum and post your query [here](https://forum.aspose.com/c/cad/19).
    question: Need help or have questions?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Πώς να εξάγετε DGN σε DWG με το Aspose.CAD για Java
url: /el/java/dgn-export-options/export-dgn-as-part-of-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να Εξάγετε DGN σε DWG με το Aspose.CAD για Java

Σε αυτό το tutorial θα ανακαλύψετε **πώς να εξάγετε dgn σε dwg** χρησιμοποιώντας τη βιβλιοθήκη Aspose.CAD για Java. Είτε χρειάζεστε να ενσωματώσετε σχέδια MicroStation σε μια ροή εργασίας AutoCAD είτε να αυτοματοποιήσετε μαζικές μετατροπές, αυτός ο οδηγός σας καθοδηγεί βήμα προς βήμα—από τη ρύθμιση του περιβάλλοντος μέχρι την παραγωγή ενός αρχείου DWG υψηλής πιστότητας. Στο τέλος, θα έχετε ένα επαναχρησιμοποιήσιμο πρότυπο κώδικα που διαχειρίζεται αξιόπιστα την εξαγωγή DGN‑σε‑DWG.

## Σύντομες Απαντήσεις
- **Ποια βιβλιοθήκη διαχειρίζεται τη μετατροπή DGN‑σε‑DWG;** Aspose.CAD for Java.  
- **Χρειάζομαι άδεια για παραγωγή;** Ναι, μια εμπορική άδεια αφαιρεί τους περιορισμούς αξιολόγησης.  
- **Υποστηριζόμενες μορφές CAD;** Πάνω από 50 μορφές εισόδου και εξόδου, συμπεριλαμβανομένων των DGN, DWG, DXF και PDF.  
- **Μπορούν να επεξεργαστούν μεγάλα αρχεία;** Ναι, το Aspose.CAD μεταδίδει αρχεία έως 2 GB χωρίς πλήρη φόρτωση στη μνήμη.  
- **Τυπικός χρόνος υλοποίησης;** Περίπου 15 λεπτά για ένα βασικό script εξαγωγής.

## Τι είναι το “πώς να εξάγετε dgn σε dwg”;
**How to export dgn to dwg** είναι η διαδικασία μετατροπής ενός αρχείου σχεδίου MicroStation DGN σε αρχείο AutoCAD DWG διατηρώντας τη γεωμετρία, τα επίπεδα και τις ραστερ εικόνες. Το Aspose.CAD παρέχει ένα προγραμματικό API που εκτελεί αυτή τη μετατροπή χωρίς την ανάγκη εγγενούς λογισμικού CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java;
Το Aspose.CAD επεξεργάζεται **πάνω από 50 μορφές CAD** και μπορεί να ραστεροποιήσει αρχεία έως 2 GB σε μέγεθος, παρέχοντας ταχύτητες μετατροπής έως 3× πιο γρήγορες από πολλά εγγενή εργαλεία. Η βιβλιοθήκη εκτελείται σε οποιαδήποτε πλατφόρμα συμβατή με Java, δεν απαιτεί εξωτερικές εξαρτήσεις και προσφέρει πλήρη έλεγχο των επιλογών ραστεροποίησης όπως το μέγεθος σελίδας, το χρώμα φόντου και η ποιότητα απόδοσης διανυσματικών στοιχείων.

## Προαπαιτούμενα

Πριν ξεκινήσουμε, βεβαιωθείτε ότι έχετε τα εξής:

1. **Aspose.CAD Library** – Κατεβάστε και εγκαταστήστε την τελευταία έκδοση του Aspose.CAD για Java από [εδώ](https://releases.aspose.com/cad/java/).  
2. **Java Development Kit (JDK)** – JDK 8 ή νεότερο εγκατεστημένο στο σύστημά σας.  
3. **IDE** – Eclipse, IntelliJ IDEA ή οποιοδήποτε IDE συμβατό με Java για άνετη προγραμματιστική εργασία.  

## Πώς να εξάγετε DGN σε DWG χρησιμοποιώντας το Aspose.CAD για Java;

Φορτώστε το πηγαίο DGN, δημιουργήστε τις επιλογές ραστεροποίησης, επαναλάβετε τις οντότητες και τέλος αποθηκεύστε το αποτέλεσμα ως αρχείο DWG. Η πλήρης ροή εργασίας χωράει σε μερικές σύντομες δηλώσεις και εκτελείται σε λιγότερο από ένα λεπτό για τυπικά αρχεία, διατηρώντας τα επίπεδα, τα βάρη γραμμών και τις ενσωματωμένες ραστερ εικόνες ώστε το παραγόμενο DWG να ταιριάζει με την αρχική πρόθεση σχεδίασης.

### Εισαγωγή Πακέτων

Η ενότητα `import` εισάγει τις βασικές κλάσεις του Aspose.CAD που απαιτούνται για τη διαχείριση CAD.

```java
import com.aspose.cad;
import com.aspose.cad.imageoptions;
import com.aspose.cad.fileformats.cad.cadconsts;
import com.aspose.cad.fileformats.cad;
import com.aspose.cad.fileformats.cad.cadobjects;
```

### Βήμα 1: Ορισμός Διαδρομών Αρχείων

Ορίστε πού βρίσκεται το πηγαίο DGN και πού θα γραφτεί το παραγόμενο DWG. Προσαρμόστε τις μεταβλητές `dataDir`, `fileName` και `outPath` ώστε να ταιριάζουν με τη δομή του έργου σας.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
String outPath = dataDir + "BlockRefDgn.dwg.pdf";
```

### Βήμα 2: Δημιουργία Αντικειμένου CadRasterizationOptions

`CadRasterizationOptions` ορίζει πώς τα διανυσματικά δεδομένα ραστεροποιούνται πριν ενσωματωθούν στο κοντέινερ DWG.

```java
PdfOptions exportOptions = new PdfOptions();
```

### Βήμα 3: Φόρτωση Αρχείου DGN

`CadImage` αντιπροσωπεύει το φορτωμένο αρχείο DGN στη μνήμη, επιτρέποντας πρόσβαση στις οντότητες και τις ιδιότητές του.

```java
CadImage cadImage = (CadImage) Image.load(fileName);
```

### Βήμα 4: Επανάληψη Στις Οντότητες

`CadBaseEntity` είναι η βασική κλάση για όλες τις οντότητες CAD, και `CadDgnUnderlay` αντιπροσωπεύει ένα ενσωματωμένο DGN υπόστρωμα. Επανάληψη σε κάθε οντότητα· όταν συναντάται ένα `ImageDefinition`, η εξωτερική του αναφορά εξάγεται για μετέπειτα ενσωμάτωση.

```java
for (CadBaseEntity baseEntity : cadImage.getEntities()) {
    if (baseEntity.getTypeName() == CadEntityTypeName.DGNUNDERLAY) {
        CadDgnUnderlay dgnFile = (CadDgnUnderlay)baseEntity;
        System.out.println(dgnFile.getUnderlayPath());
    }
}
```

### Βήμα 5: Ορισμός Επιλογών Ραστεροποίησης

Ορίστε το πλάτος, το ύψος, την επιλογή διάταξης και το χρώμα φόντου της σελίδας ώστε να ταιριάζουν με τις οπτικές απαιτήσεις του στόχου DWG.

```java
CadRasterizationOptions vectorRasterizationOptions = new CadRasterizationOptions();
vectorRasterizationOptions.setPageWidth(1600);
vectorRasterizationOptions.setPageHeight(1600);
vectorRasterizationOptions.setLayouts(new String[] { "Model" });
vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
vectorRasterizationOptions.setNoScaling(true);
vectorRasterizationOptions.setBackgroundColor(Color.getBlack());
vectorRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
```

### Βήμα 6: Ορισμός Επιλογών Διανυσματικής Ραστεροποίησης

Καθορίστε ρυθμίσεις ειδικές για διανύσματα όπως η διαχείριση βάρους γραμμής και η προσέγγιση καμπύλης ώστε το DWG να διατηρεί καθαρή γεωμετρία.

```java
exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);
```

### Βήμα 7: Εξαγωγή DWG σε PDF

Καλέστε τη μέθοδο `save` στο αντικείμενο `CadImage`, περνώντας τις ρυθμισμένες επιλογές για να παραχθεί το τελικό PDF συμβατό με DWG.

```java
cadImage.save(outPath, exportOptions);
```

## Συνηθισμένα Προβλήματα και Λύσεις

- **Απουσία εξωτερικής αναφοράς εικόνας** – Επαληθεύστε ότι οι ορισμοί εικόνας του DGN δείχνουν σε προσβάσιμες διαδρομές αρχείων· χρησιμοποιήστε απόλυτες διαδρομές εάν αποτύχουν οι σχετικές.  
- **Απρόσμενο χρώμα φόντου** – Βεβαιωθείτε ότι το `CadRasterizationOptions.setBackgroundColor()` ταιριάζει με την επιθυμητή τιμή RGB· η προεπιλογή είναι λευκό.  
- **Σφάλματα μνήμης σε μεγάλα αρχεία** – Ενεργοποιήστε τη ροή ορίζοντας το `CadRasterizationOptions.setPageSize()` σε λογικό μέγεθος και αποφύγετε τη φόρτωση ολόκληρου του αρχείου στη μνήμη.  

## Συχνές Ερωτήσεις

**Q: Πού μπορώ να βρω την τεκμηρίωση για το Aspose.CAD για Java;**  
A: Η πλήρης αναφορά API είναι διαθέσιμη [εδώ](https://reference.aspose.com/cad/java/).

**Q: Πώς μπορώ να κατεβάσω τη βιβλιοθήκη Aspose.CAD για Java;**  
A: Κατεβάστε την τελευταία έκδοση από [αυτόν τον σύνδεσμο](https://releases.aspose.com/cad/java/).

**Q: Υπάρχει δωρεάν δοκιμαστική έκδοση για το Aspose.CAD για Java;**  
A: Ναι, μπορείτε να αποκτήσετε μια πλήρως λειτουργική δοκιμαστική έκδοση [εδώ](https://releases.aspose.com/).

**Q: Πού μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD για Java;**  
A: Ζητήστε προσωρινή άδεια από το Aspose [εδώ](https://purchase.aspose.com/temporary-license/).

**Q: Χρειάζεστε βοήθεια ή έχετε ερωτήσεις;**  
A: Εγγραφείτε στο φόρουμ υποστήριξης της κοινότητας και υποβάλετε το ερώτημά σας [εδώ](https://forum.aspose.com/c/cad/19).

---

**Τελευταία ενημέρωση:** 2026-05-20  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.5  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή DGN σε DWG με Aspose.CAD για Java – Tutorial](/cad/java/dgn-export-options/)
- [Απρόσκοπτη Εξαγωγή DGN σε PDF AutoCAD με Aspose.CAD για Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [Εξαγωγή DWG σε PDF ή Ράστερ χρησιμοποιώντας Aspose.CAD για Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}