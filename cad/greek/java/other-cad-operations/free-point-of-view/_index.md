---
date: 2026-01-20
description: Μάθετε πώς να αποδίδετε σχέδια CAD με το Aspose.CAD για Java, να μετατρέπετε
  DXF σε JPEG, να περιστρέφετε την προβολή CAD και να διαχειρίζεστε την άδεια.
linktitle: Free Point of View
second_title: Aspose.CAD Java API
title: Πώς να αποδώσετε CAD – Δωρεάν απόδοση Point of View με το Aspose.CAD για Java
url: /el/java/other-cad-operations/free-point-of-view/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Απεικόνιση Ελεύθερης Προοπτικής με Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το tutorial θα ανακαδίδετε CAD** σχέδια χρησιμοποιώντας το Aspose.CAD για Java, έχοντας πλήρη έλεγχο της γωνίας της κάμερας. Θα περάσουμε από κάθε βήμα—από τη φόρτωση ενός αρχείου CAD, την περιστροφή της προβολής, μέχρι τη μετατροπή ενός αρχείου DXF σε εικόνα JPEG. Στο τέλος θα μπορείτε να δημιουργήσετε μια απόδοση ελεύθερης προοπτικής που μπορεί να αποθηκευτεί ως εικόνα raster υψηλής ανάλυσης, ιδανική για αναφορές, προεπισκοπήσεις στο web ή επεξεργασία downstream.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρειάζεται;** Aspose.CAD για Java  
- **Μπορώ να μετατρέψω DXF σε JPEG;** Ναι, χρησιμοποιώντας `JpegOptions` με  `ObserverPoint` με γωνίες X, Y, Z  
- **Χρειάζομαι άδεια;** Απαιτείται προσωρινή ή πλήρης άδεια Aspose.CAD για παραγωγική χρήση  
- **Ποια έκδοση JDK λειτουργεί;** Java 8 + υποστηρίζεται πλήρως  

## Τι είναι η απεικόνιση ελεύθερης προοπτικής;
Η απεικόνιση ελεύθερης προοπτικής σας επιτρέπει να τοποθετήσετε μια εικονική κάμερα οπουδήποτε γύρω από το μοντέλο CAD, δίνοντάς σας **Δενισμικό CAD** – λειτουργεί έξοδος** – υποστηρίζει JPEG, PNG, BMP και άλλα.  
- **Προγραμματιστικός έλεγχος** – περιστροφή, ζουμ και εξαγωγή όλα από τον κώδικα.  
- **Ανθεκτικές επιλογές αδειοδότησης** – από δωρεάν δοκιμή έως επιχειρηματικές άδειες.

## Προαπαιτούμεναεβαιωθείτε ότι έχετε:

- **Aspose.CAD για Java Library** – κατεβάστε το από το [download link](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK)** – εγκατεστημένο Java 8 ή νεότερο στο σύστημά σας.  

## Εισαγωγή Πακέτων

Προσθέστε τις απαιτούμενες εισαγωγές στην αρχή του αρχείου πηγαίου κώδικα Java:

```java
import com.aspose.cad.fileformats.ObserverPoint;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.ObserverPoint;
```

Αυτές οι κλάσεις σας δίνουν πρόσβαση στη φόρτωση εικόνας, στις ρυθμίσεις rasterization, στην έξοδο JPEG και στη δυνατότητα ορισμού σημείου παρατήρησης (κάμερας).

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ρύθμιση του Καταλόγου Εγγράφων σας
Ορίστε πού θα βρίσκονται τα πηγαία αρχεία CAD και οι εικόνες εξόδου.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Αντικαταστήστε **Your Document Directory** με την απόλυτη διαδρομή στο σύστημά σας.

### Βήμα 2: Φόρτωση του Σχεδίου CAD (load CAD image)
Διαβάστε το αρχείο DXF σε ένα αντικείμενο `Image` ώστε να μπορείτε να το επεξεργαστείτε στη μνήμη.

```java
String sourceFilePath = dataDir + "conic_pyramid.dxf";
Image objImage = Image.load(sourceFilePath);
```

> **Συμβουλή:** Αυτό το βήμα δείχνει πώς να *φορτώσετε μια εικόνα CAD*· μπορείτε να αντικαταστήσετε το αρχείο με οποιαδήποτε υποστηριζόμενη μορφή (DWG, DWF κ.λπ.).

### Βήμα 3: Διαμόρφωση Επιλογών Rasterization CAD
Ορίστε το μέγεθοςγαλύτερες διαστάσεις παρέχουν αποτελέσματα υψηλότερης ανάλυσης.

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
cadRasterizationOptions.setPageHeight(1500);
cadRasterizationOptions.setPageWidth(1500);
```

### Βήμα 4: Ρύθμιση Επιλογών JPEG
Συνδέστε τις ρυθμίσεις rasterization με τον κωδικοποιητή JPEG.

```java
JpegOptions options = new JpegOptions();
options.setVectorRasterizationOptions(cadRasterizationOptions);
```

### Βήμα 5: Ορισμός Γωνιών Περιστροφής (rotate CAD view)
Δημιουργήστε ένα `ObserverPoint` για να περιστρέψετε την προβολή γύρω από τους άξονες X, Y και Z.

```java
float xAngle = 10;
float yAngle = 30;
float zAngle = 40;
ObserverPoint obvPoint = new ObserverPoint(xAngle, yAngle, zAngle);
cadRasterizationOptions.setObserverPoint(obvPoint);
```

Ρυθμίστε τις γωνίες ώστε να πετύχετε την επιθυμητή **ελεύθερη προοπτική**. Αυτό αποτελεί τον πυρήνα του *περιστροφής της προβολής CAD*.

### Βήμα 6: Αποθήκευση της Απεικόνισης (convert DXF to JPEG)
Εξάγετε την rasterized εικόνα ως αρχείο JPEG.

```java
objImage.save(dataDir + "FreePointOfView_out.jpeg", options);
```

Το αποτέλεσμα είναι ένα JPEG που αντικατοπτρίζει την περιστραμμένη προοπτική που ορίσατε.

## Κοινά Προβλήματα & Λύσεις
- **Η εικόνα εμφανίζεται κενή** – Βεβαιωθείτε ότι οι γωνίες του παρατηρητή είναι σε λογικό εύρος (0‑90°) και ότι το πηγαίο αρχείο φορτώθηκε σωστά.  
- **Σφάλματα έλλειψης μνήμης** – Μειώστε το `PageHeight`/`PageWidth` ή αυξήστε το μέγεθος heap της JVM (`-Xmx`).  
- **Η άδεια δεν εφαρμόζεται** – Φορτώστε την άδεια Aspose.CAD πριν από οποιαδήποτε κλήση API (`License license = new License(); license.setLicense("Aspose.CAD.lic");`).

## Συχνές Ερωτήσεις

### Q1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java σε πολλαπλές πλατφόρμες;
A1: Ναι, το Aspose.CAD για Java είναι ανεξάρτητο πλατφόρμας και λειτουργεί σε Windows, Linux και macOS.

### Q2: Υπάρχουν επιλογές αδειοδότησης για το Aspose.CAD για Java;
A2: Ναι, μπορείτε να εξερευνήσετε τις **aspose cad licensing** επιλογές και να κάνετε αγορά [εδώ](https://purchase.aspose.com/buy).

### Q3: Διατίθεται δωρεάν δοκιμή;
A3: Ναι, μπορείτε να αποκτήσετε δωρεάν έκδοση δοκιμής [εδώ](https://releases.aspose.com/).

### Q4: Πού μπορώ να βρω υποστήριξη για το Aspose.CAD για Java;
A4: Επισκεφθείτε το [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) για υποστήριξη κοινότητας και συζητήσεις.

### Q5: Πώς μπορώ να αποκτήσω προσωρινή άδεια;
A5: Αποκτήστε προσωρινή άδεια [εδώ](https://purchase.aspose.com/temporary-license/).

## Συμπέρασμα

Μάθατε **πώς να αποδίδετε σχέδια CAD** με ελεύθερη προοπτική χρησιμοποιώντας το Aspose.CAD για Java, πώς να *μετατρέψετε DXF σε JPEG* και πασία.

μέρωση24.12 (τελευταία έκδοση τη στιγμή της συγγραφής)  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}