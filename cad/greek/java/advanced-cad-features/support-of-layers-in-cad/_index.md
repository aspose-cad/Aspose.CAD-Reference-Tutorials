---
date: 2025-12-13
description: Μάθετε πώς να αποθηκεύετε CAD ως JPEG σε Java χρησιμοποιώντας το Aspose.CAD,
  να προσθέτετε πολλαπλά στρώματα και να προσαρμόζετε τις διαστάσεις του CAD για ακριβή
  μετατροπή εικόνας.
linktitle: Support of Layers in CAD
second_title: Aspose.CAD Java API
title: Αποθήκευση CAD ως JPEG με υποστήριξη επιπέδων σε Java
url: /el/java/advanced-cad-features/support-of-layers-in-cad/
weight: 18
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση CAD ως JPEG με Υποστήριξη Στρωμάτων σε Java

## Εισαγωγή

Σε αυτό το tutorial θα ανακαλύψετε πώς να **αποθηκεύσετε CAD ως JPEG** εκμεταλλευόμενοι πλήρως την υποστήριξη στρωμάτων στο Aspose.CAD for Java. Τα στρώματα σας επιτρέπουν να απομονώσετε συγκεκριμένα τμήματα ενός σχεδίου, καθιστώντας εύκολη την εξαγωγή μόνο αυτού που χρειάζεστε. Θα περάσουμε βήμα-βήμα από τη ρύθμιση του περιβάλλοντος μέχρι την εξαγωγή ενός JPEG που περιλαμβάνει μόνο τα στρώματα που επιλέγετε.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει “αποθήκευση CAD ως JPEG”;** Μετατρέπει ένα σχέδιο CAD σε μια ραστερική εικόνα JPEG.
- **Μπορώ να συμπεριλάβω μόνο επιλεγμένα στρώματα;** Ναι – χρησιμοποιήστε τη μέθοδο `setLayers` για να καθορίσετε ποια στρώματα θα αποδοθούν.
- **Πώς αλλάζω το μέγεθος της εικόνας;** Ρυθμίστε τα `setPageWidth` και `setPageHeight` στο `CadRasterizationOptions`.
- **Είναι αυτή λύση μόνο για Java;** Το παράδειγμα χρησιμοποιεί Aspose.CAD for Java, αλλά οι ίδιες έννοιες ισχύουν και για άλλες γλώσσες.
- **Χρειάζομαι άδεια;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.

## Προαπαιτούμενα

Πριν ξεκινήσετε, βεβαιωθείτε ότι έχετε τα εξής:

1. **Βιβλιοθήκη Aspose.CAD for Java** – κατεβάστε την από την [website](https://releases.aspose.com/cad/java/). Ακολουθήστε τον οδηγό εγκατάστασης για να προσθέσετε τα αρχεία JAR στο classpath του έργου σας.  
2. **Περιβάλλον Ανάπτυξης Java** – εγκατεστημένο πρόσφατο JDK (8 ή νεότερο) στο σύστημά σας.

Τώρα που είμαστε έτοιμοι, ας εξερευνήσουμε τον κώδικα που απαιτείται για **αποθήκευση CAD ως JPEG** με επιλεκτική απόδοση στρωμάτων.

## Εισαγωγή Ονομάτων Χώρων

Ξεκινήστε εισάγοντας τις απαιτούμενες κλάσεις Aspose.CAD και τις τυπικές βοηθητικές κλάσεις της Java:

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
```

## Οδηγός Βήμα‑Βήμα

### Βήμα 1: Ορισμός Διαδρομών Αρχείων

Καθορίστε πού βρίσκεται το αρχείο πηγής DWF και πού θα γραφτεί το αρχείο εξόδου JPEG.

```java
String dataDir = "Your Document Directory" + "DWFDrawings/";
String srcFile = dataDir + "for_layers_test.dwf";
String outFile = dataDir + "for_layers_test.jpg";
```

### Βήμα 2: Φόρτωση της Εικόνας DWF

Χρησιμοποιήστε τη μέθοδο `Image.load` του Aspose.CAD για να διαβάσετε το σχέδιο CAD.

```java
Image image = Image.load(srcFile);
```

### Βήμα 3: Διαμόρφωση Επιλογών Rasterization (Ρύθμιση Διαστάσεων CAD)

Δημιουργήστε ένα αντικείμενο `CadRasterizationOptions` και ορίστε το επιθυμητό μέγεθος εξόδου. Η αλλαγή αυτών των τιμών σας επιτρέπει να **ρυθμίσετε τις διαστάσεις CAD** για το τελικό JPEG.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Βήμα 4: Καθορισμός Στρωμάτων (Προσθήκη Πολλαπλών Στρωμάτων)

Αν θέλετε να αποδώσετε περισσότερα από ένα στρώματα, απλώς προσθέστε τα ονόματά τους στη λίστα. Εδώ ξεκινάμε με ένα μόνο στρώμα που ονομάζεται “LayerA”.

```java
List<String> stringList = new ArrayList<>(Arrays.asList("LayerA"));
rasterizationOptions.setLayers(stringList);
```

*Συμβουλή:* Για **προσθήκη πολλαπλών στρωμάτων**, επεκτείνετε την κλήση `Arrays.asList`, π.χ., `Arrays.asList("LayerA", "LayerB", "LayerC")`.

### Βήμα 5: Διαμόρφωση Επιλογών JPEG (Μετατροπή Εικόνας CAD σε Java)

Συνδέστε τις ρυθμίσεις rasterization με τη μορφή εξόδου JPEG.

```java
JpegOptions jpegOptions = new JpegOptions();
jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Βήμα 6: Εξαγωγή σε JPG (Αποθήκευση CAD ως JPEG)

Τέλος, γράψτε την εικόνα στο δίσκο. Αυτό το βήμα **αποθηκεύει το σχέδιο CAD ως αρχείο JPEG** που περιέχει μόνο τα επιλεγμένα στρώματα.

```java
image.save(outFile, jpegOptions);
```

Ακολουθώντας αυτά τα βήματα, έχετε αποθηκεύσει επιτυχώς **CAD ως JPEG** ελέγχοντας ποια στρώματα εμφανίζονται και προσαρμόζοντας τις διαστάσεις της εικόνας.

## Κοινά Προβλήματα και Λύσεις

| Πρόβλημα | Λύση |
|----------|------|
| **Τα στρώματα δεν εμφανίζονται** | Βεβαιωθείτε ότι τα ονόματα των στρωμάτων ταιριάζουν ακριβώς με αυτά που αποθηκεύονται στο αρχείο DWF (διάκριση πεζών‑κεφαλαίων). |
| **Η εικόνα εξόδου είναι κενή** | Εξασφαλίστε ότι τα `setPageWidth` και `setPageHeight` είναι αρκετά μεγάλα για τις διαστάσεις του σχεδίου. |
| **Εξαίρεση άδειας** | Χρησιμοποιήστε δοκιμαστική άδεια για δοκιμές· αποκτήστε πλήρη άδεια για περιβάλλον παραγωγής. |

## Συχνές Ερωτήσεις

**Ε: Μπορώ να προσθέσω πολλαπλά στρώματα στις επιλογές rasterization;**  
Α: Φυσικά. Επεκτείνετε το `stringList` με επιπλέον ονόματα στρωμάτων, π.χ., `Arrays.asList("LayerA", "LayerB")`.

**Ε: Είναι το Aspose.CAD συμβατό με άλλες μορφές CAD;**  
Α: Ναι, υποστηρίζει DWG, DXF, DWF και πολλές άλλες μορφές.

**Ε: Πώς μπορώ να αλλάξω τις διαστάσεις της εικόνας εξόδου;**  
Α: Τροποποιήστε τα `setPageWidth` και `setPageHeight` στο αντικείμενο `CadRasterizationOptions`.

**Ε: Πού μπορώ να αγοράσω άδεια για το Aspose.CAD;**  
Α: Μπορείτε να εξερευνήσετε τις επιλογές αδειοδότησης [εδώ](https://purchase.aspose.com/buy).

**Ε: Πού μπορώ να βρω υποστήριξη από την κοινότητα;**  
Α: Εγγραφείτε στην κοινότητα Aspose.CAD στο [forum](https://forum.aspose.com/c/cad/19) για βοήθεια και συζητήσεις.

---

**Τελευταία ενημέρωση:** 2025-12-13  
**Δοκιμή με:** Aspose.CAD for Java 24.11  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}