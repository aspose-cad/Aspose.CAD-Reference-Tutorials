---
date: 2026-02-28
description: Μάθετε πώς να δημιουργείτε PDF από DWG, να αποθηκεύετε DWG ως PDF και
  να προσθέτετε κείμενο σε σχέδια DWG με το Aspose.CAD for Java—οδηγός βήμα‑προς‑βήμα.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Δημιουργία PDF από DWG και προσθήκη κειμένου με Aspose.CAD για Java
url: /el/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Δημιουργία PDF από DWG και Προσθήκη Κειμένου με τη χρήση Aspose.CAD for Java

## Εισαγωγή

Αν χρειάζεστε **δημιουργία PDF από DWG** αρχεία ενώ ταυτόχρονα προσθέτετε προσαρμοσμένο κείμενο, βρίσκεστε στο σωστό μέρος. Σε αυτό το tutorial θα περάσουμε από όλη τη διαδικασία — φόρτωση ενός σχεδίου DWG, προσθήκη σχολίου κειμένου και, τέλος, αποθήκευση του αποτελέσματος ως PDF χρησιμοποιώντας το Aspose.CAD for Java. Στο τέλος θα καταλάβετε πώς να **αποθηκεύσετε DWG ως PDF**, να προσαρμόσετε το ύψος του κειμένου και ακόμη να προσθέσετε βασικά σχόλια.

## Γρήγορες Απαντήσεις
- **Μπορώ να μετατρέψω DWG σε PDF με Java;** Ναι, το Aspose.CAD for Java παρέχει ένα απλό API.  
- **Χρειάζομαι άδεια για παραγωγική χρήση;** Απαιτείται εμπορική άδεια· διατίθεται δωρεάν δοκιμαστική έκδοση.  
- **Ποια μέθοδος προσθέτει κείμενο σε DWG;** Χρησιμοποιήστε το αντικείμενο `CadText` και προσθέστε το στο model space.  
- **Μπορώ να ορίσω το ύψος του κειμένου;** Απόλυτα — χρησιμοποιήστε `setTextHeight()` στο αντικείμενο `CadText`.  
- **Είναι το αποτέλεσμα βασισμένο σε διανύσματα;** Όταν οι επιλογές rasterization οριστούν σε `UseObjectColor`, το PDF διατηρεί υψηλής ποιότητας διανυσματικά δεδομένα.

## Τι σημαίνει «δημιουργία PDF από DWG»;
Η δημιουργία PDF από ένα σχέδιο DWG σημαίνει τη μετατροπή της εγγενούς μορφής CAD σε ένα ευρέως υποστηριζόμενο, μόνο για ανάγνωση έγγραφο, διατηρώντας την αρχική γεωμετρία. Αυτή η μετατροπή είναι απαραίτητη όταν πρέπει να μοιραστείτε σχέδια με ενδιαφερόμενους που δεν διαθέτουν λογισμικό CAD.

## Γιατί να χρησιμοποιήσετε Aspose.CAD for Java για τη μετατροπή DWG σε PDF;
Το Aspose.CAD προσφέρει μια λύση καθαρά Java που δεν απαιτεί εξωτερική εγκατάσταση CAD. Υποστηρίζει **convert DWG to PDF**, διατηρεί τη διανυσματική πιστότητα και σας επιτρέπει να προσθέτετε προγραμματιστικά σχόλια όπως κείμενο, διαστάσεις ή προσαρμοσμένα γραφικά πριν από τη μετατροπή.

## Προαπαιτούμενα

Πριν ξεκινήσετε το tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω:

- Aspose.CAD for Java Library: Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη από τη σελίδα [Aspose.CAD for Java page](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK): Βεβαιωθείτε ότι έχετε εγκατεστημένη την πιο πρόσφατη έκδοση του JDK στο σύστημά σας.

- DWG Drawing: Προετοιμάστε ένα αρχείο DWG στο οποίο θέλετε να προσθέσετε κείμενο.

## Εισαγωγή Namespaces

Στον κώδικα Java, εισάγετε τα απαραίτητα namespaces για το Aspose.CAD:

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Τώρα, ας αναλύσουμε το παρεχόμενο απόσπασμα κώδικα σε πολλαπλά βήματα:

## Βήμα 1: Ρύθμιση Καταλόγου Εγγράφου και Διαδρομής Αρχείου DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Βήμα 2: Φόρτωση Εικόνας DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Βήμα 3: Δημιουργία Αντικειμένου CadText (Προσθήκη Κειμένου στο DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Βήμα 4: Προσθήκη Κειμένου στο CadImage (Εισαγωγή Σχολίου)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Βήμα 5: Ρύθμιση PDF Options (Προετοιμασία για δημιουργία PDF από DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Βήμα 6: Διαμόρφωση CadRasterizationOptions (Έλεγχος Απόδοσης PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Βήμα 7: Αποθήκευση Τροποποιημένου DWG ως PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

Ακολουθώντας αυτά τα βήματα, θα μπορείτε να **δημιουργήσετε PDF από DWG**, να προσθέσετε προσαρμοσμένο κείμενο και να ελέγξετε το ύψος του κειμένου — όλα με λίγες γραμμές κώδικα Java.

## Πώς να μετατρέψετε DWG σε PDF με Java σε κλίμακα;
Αν χρειάζεστε **batch convert DWG PDF** αρχεία, τυλίξτε τον παραπάνω κώδικα σε έναν βρόχο που διατρέχει έναν φάκελο με σχέδια DWG. Προσαρμόστε `pageHeight`/`pageWidth` μόνο όταν είναι απαραίτητο για να διατηρήσετε τη χρήση μνήμης χαμηλή, και επαναχρησιμοποιήστε την ίδια παρουσία `PdfOptions` για κάθε αρχείο ώστε να βελτιώσετε την απόδοση.

## Κοινά Προβλήματα & Συμβουλές

- **Το κείμενο δεν εμφανίζεται;** Ελέγξτε ότι οι συντεταγμένες X/Y βρίσκονται εντός των ορίων του σχεδίου και ότι το layer είναι ορατό.
- **Λανθασμένο ύψος κειμένου;** Προσαρμόστε το `setTextHeight()`· η τιμή είναι στη μονάδα του σχεδίου.
- **Το PDF φαίνεται rasterized;** Βεβαιωθείτε ότι το `CadDrawTypeMode.UseObjectColor` είναι ορισμένο για διατήρηση των διανυσματικών πληροφοριών.
- **Απόδοση σε μεγάλα αρχεία;** Αυξήστε `pageHeight`/`pageWidth` μόνο όταν χρειάζεται· μεγαλύτερες τιμές καταναλώνουν περισσότερη μνήμη.

## Συχνές Ερωτήσεις

**Ε: Είναι το Aspose.CAD συμβατό με όλες τις εκδόσεις αρχείων DWG;**  
Α: Το Aspose.CAD υποστηρίζει διάφορες εκδόσεις αρχείων DWG, εξασφαλίζοντας συμβατότητα με ένα ευρύ φάσμα λογισμικού CAD.

**Ε: Μπορώ να προσαρμόσω τη γραμματοσειρά και τη μορφοποίηση του προστιθέμενου κειμένου;**  
Α: Ναι, μπορείτε να προσαρμόσετε τη γραμματοσειρά, το στυλ και άλλες επιλογές μορφοποίησης για το κείμενο που προστίθεται σε αρχεία DWG χρησιμοποιώντας το Aspose.CAD.

**Ε: Υπάρχει δωρεάν δοκιμαστική έκδοση για το Aspose.CAD for Java;**  
Α: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD αποκτώντας δωρεάν δοκιμαστική έκδοση από [εδώ](https://releases.aspose.com/).

**Ε: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD for Java;**  
Α: Ανατρέξτε στην τεκμηρίωση [εδώ](https://reference.aspose.com/cad/java/) για εκτενείς πληροφορίες και παραδείγματα.

**Ε: Πώς μπορώ να λάβω υποστήριξη ή βοήθεια σχετικά με το Aspose.CAD;**  
Α: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για βοήθεια και σύνδεση με την κοινότητα.

---

**Τελευταία Ενημέρωση:** 2026-02-28  
**Δοκιμάστηκε Με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}