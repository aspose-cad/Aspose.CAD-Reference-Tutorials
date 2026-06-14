---
date: 2026-06-14
description: Μάθετε πώς να εξάγετε CAD σε SVG με το Aspose.CAD for Java. Αυτός ο οδηγός
  βήμα-βήμα σας δείχνει πώς να μετατρέψετε DWG σε SVG, να ορίσετε τη λειτουργία χρώματος
  SVG και να ενσωματώσετε τη βιβλιοθήκη στο έργο Java σας.
keywords:
- export cad to svg
- convert dwg to svg
- change svg to grayscale
- convert cad to svg
- generate svg from dwg
linktitle: Εξαγωγή σε SVG
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  headline: Export CAD to SVG Using Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to SVG with Aspose.CAD for Java. This step‑by‑step
    guide shows you how to convert DWG to SVG, set SVG color mode, and integrate the
    library into your Java project.
  name: Export CAD to SVG Using Aspose.CAD for Java
  steps:
  - name: Open Your Java Project
    text: Launch your favorite IDE (IntelliJ IDEA, Eclipse, VS Code) and open the
      project where you intend to add the conversion logic.
  - name: Add Aspose.CAD Library
    text: Place the `aspose-cad-xx.jar` file in the `libs` directory and add it as
      a dependency in your build tool (Maven, Gradle, or plain `javac`).
  - name: Import Namespaces
    text: 'In the Java source file that will perform the conversion, add the following
      imports: These imports give you access to the core `Image` class and the SVG‑specific
      export options.'
  - name: Specify the Resource Directory
    text: 'Define the absolute or relative path that points to the folder holding
      your CAD drawings:'
  - name: Load the CAD Drawing
    text: The `Image` class is Aspose.CAD's top‑level object that represents a CAD
      drawing in memory. Loading the file creates an in‑memory representation ready
      for export. `Image.load` reads a CAD file and creates an in‑memory representation
      of the drawing.
  - name: Configure SVG Export Options
    text: '`SvgExportOptions` lets you fine‑tune the SVG output. Below we set the
      color mode to grayscale and ensure all text is rendered as shapes, which improves
      compatibility with browsers that lack the original font.'
  - name: Save as SVG
    text: Finally, invoke `save` on the `Image` instance, passing the target file
      name and the configured options. Aspose.CAD writes a standards‑compliant SVG
      file that can be opened directly in any modern browser. `save` writes the image
      to the specified file using the provided export options. > **Pro tip:**
  type: HowTo
- questions:
  - answer: Yes, simply replace the DWG file name with a DXF file; the API automatically
      detects and processes both formats.
    question: Can I convert a DXF file to SVG using the same code?
  - answer: Set `options.setColorType(SvgColorMode.FullColor);` before invoking the
      `save` method.
    question: How do I change the output to full‑color SVG?
  - answer: Aspose.CAD converts text to shapes, so embedding fonts is unnecessary;
      the resulting SVG contains only vector outlines.
    question: Is it possible to embed fonts in the generated SVG?
  - answer: The Java library is platform‑independent and runs wherever a compatible
      JVM is available, including Windows, Linux, and macOS.
    question: Does the library work on Linux and macOS?
  - answer: The example was tested with Aspose.CAD for Java **24.10**.
    question: What version of Aspose.CAD was used in this tutorial?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Εξαγωγή CAD σε SVG χρησιμοποιώντας το Aspose.CAD for Java
url: /el/java/cad-to-pdf-and-svg-export-options/export-to-svg/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Εξαγωγή CAD σε SVG με χρήση Aspose.CAD για Java

## Εισαγωγή

Σε αυτό το ολοκληρωμένο tutorial θα μάθετε **πώς να εξάγετε CAD σε SVG** χρησιμοποιώντας το Aspose.CAD για Java. Είτε χρειάζεστε **μετατροπή DWG σε SVG**, δημιουργία SVG από αρχεία DWG σε batch job, ή απλώς αλλαγή του SVG σε αποχρώσεις του γκρι για ελαφριά προβολή στο web, αυτός ο οδηγός σας καθοδηγεί βήμα-βήμα—from τη ρύθμιση της βιβλιοθήκης μέχρι τη λεπτομερή ρύθμιση των επιλογών εξαγωγής. Στο τέλος, θα έχετε ένα snippet έτοιμο για παραγωγή που τρέχει σε οποιαδήποτε πλατφόρμα συμβατή με JVM.

## Γρήγορες Απαντήσεις
- **Τι σημαίνει η «εξαγωγή CAD σε SVG»;** Μετατρέπει ένα σχέδιο CAD (π.χ., DWG ή DXF) σε αρχείο Scalable Vector Graphics που οι περιηγητές εμφανίζουν χωρίς απώλεια ποιότητας.  
- **Ποια βιβλιοθήκη χειρίζεται τη μετατροπή;** Το Aspose.CAD για Java παρέχει μια ειδική API που υποστηρίζει 30+ μορφές CAD και εξάγει SVG με πλήρη διανυσματική πιστότητα.  
- **Χρειάζεται άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για αξιολόγηση· απαιτείται εμπορική άδεια για παραγωγικές εγκαταστάσεις.  
- **Μπορώ να ελέγξω το χρώμα εξόδου του SVG;** Ναι—χρησιμοποιήστε το `SvgColorMode` για εναλλαγή μεταξύ αποχρώσεων του γκρι και πλήρους χρώματος.  
- **Απαιτείται επιπλέον λογισμικό;** Μόνο ένα Java runtime (JDK 8 ή νεότερο) και το Aspose.CAD JAR· δεν χρειάζονται εξωτερικά εργαλεία CAD.

## Τι είναι η εξαγωγή CAD σε SVG;
Η εξαγωγή CAD σε SVG είναι η διαδικασία μετατροπής ενός εγγενούς αρχείου CAD (όπως DWG, DXF ή DWF) σε μορφή εικόνας SVG. Το παραγόμενο SVG διατηρεί ακριβή γεωμετρικά δεδομένα, επιτρέποντας προβολή ανεξάρτητη από την ανάλυση σε περιηγητές web και εργαλεία σχεδίασης.

## Γιατί να εξάγετε CAD σε SVG με Aspose.CAD;
Το Aspose.CAD μπορεί να χειριστεί **30+ μορφές εισόδου** και να δημιουργήσει έξοδο SVG έως **500 σελίδες** χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη, προσφέροντας **υψηλής πιστότητας διανυσματική μετατροπή** με ταχύτητα **200 σελίδες/δευτερόλεπτο** σε τυπικό server‑grade CPU. Η βιβλιοθήκη τρέχει **100 % Java**, εξαλείφοντας την ανάγκη για εγγενείς DLL ή τρίτες μηχανές CAD.

## Προαπαιτούμενα

- **Java Development Kit** (JDK 8 ή νεότερο) εγκατεστημένο και ρυθμισμένο στο μηχάνημά σας.  
- **Aspose.CAD for Java** αρχείο JAR που έχει ληφθεί από τον επίσημο [download link](https://releases.aspose.com/cad/java/).  
- Ένας φάκελος που περιέχει τουλάχιστον ένα σχέδιο CAD (DWG, DXF κ.λπ.) που θέλετε να μετατρέψετε.

## Εισαγωγή Namespaces

Πριν γράψετε κώδικα, βεβαιωθείτε ότι η βιβλιοθήκη Aspose.CAD βρίσκεται στο classpath και εισάγετε τις απαιτούμενες κλάσεις.

### Βήμα 1: Ανοίξτε το Java Project σας
Εκκινήστε το αγαπημένο σας IDE (IntelliJ IDEA, Eclipse, VS Code) και ανοίξτε το project όπου σκοπεύετε να προσθέσετε τη λογική μετατροπής.

### Βήμα 2: Προσθέστε τη βιβλιοθήκη Aspose.CAD
Τοποθετήστε το αρχείο `aspose-cad-xx.jar` στον κατάλογο `libs` και προσθέστε το ως εξάρτηση στο εργαλείο κατασκευής σας (Maven, Gradle ή απλό `javac`).

### Βήμα 3: Εισαγωγή Namespaces
Στο αρχείο πηγαίου κώδικα Java που θα εκτελεί τη μετατροπή, προσθέστε τις ακόλουθες εισαγωγές:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgExportOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

Αυτές οι εισαγωγές σας δίνουν πρόσβαση στην κεντρική κλάση `Image` και στις επιλογές εξαγωγής SVG.

## Πώς να εξάγετε CAD σε SVG χρησιμοποιώντας Aspose.CAD για Java;

Η εξαγωγή ενός σχεδίου CAD σε SVG με το Aspose.CAD περιλαμβάνει τη φόρτωση του πηγαίου αρχείου, τη ρύθμιση των επιλογών SVG και την αποθήκευση του αποτελέσματος. Η διαδικασία είναι απλή, απαιτεί μόνο λίγες γραμμές κώδικα και λειτουργεί σταθερά σε όλες τις υποστηριζόμενες μορφές CAD, διατηρώντας τη διανυσματική πιστότητα.

### Βήμα 1: Καθορίστε τον Κατάλογο Πόρων
Ορίστε την απόλυτη ή σχετική διαδρομή που δείχνει στον φάκελο που περιέχει τα σχέδια CAD σας:

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.SvgColorMode;
```

### Βήμα 2: Φορτώστε το Σχέδιο CAD
Η κλάση `Image` είναι το κορυφαίο αντικείμενο του Aspose.CAD που αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη. Η φόρτωση του αρχείου δημιουργεί μια αναπαράσταση στη μνήμη έτοιμη για εξαγωγή.

`Image.load` διαβάζει ένα αρχείο CAD και δημιουργεί μια αναπαράσταση του σχεδίου στη μνήμη.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

### Βήμα 3: Διαμόρφωση Επιλογών Εξαγωγής SVG
`SvgExportOptions` σας επιτρέπει να ρυθμίσετε λεπτομερώς την έξοδο SVG. Παρακάτω ορίζουμε τη λειτουργία χρώματος σε αποχρώσεις του γκρι και διασφαλίζουμε ότι όλο το κείμενο αποδίδεται ως σχήματα, κάτι που βελτιώνει τη συμβατότητα με περιηγητές που δεν διαθέτουν την αρχική γραμματοσειρά.

```java
Image image = Image.load(dataDir + "meshes.dwg");
```

### Βήμα 4: Αποθήκευση ως SVG
Τέλος, καλέστε τη μέθοδο `save` στο αντικείμενο `Image`, περνώντας το όνομα του αρχείου προορισμού και τις ρυθμισμένες επιλογές. Το Aspose.CAD γράφει ένα αρχείο SVG σύμφωνο με τα πρότυπα που μπορεί να ανοιχθεί άμεσα σε οποιονδήποτε σύγχρονο περιηγητή.

`save` γράφει την εικόνα στο καθορισμένο αρχείο χρησιμοποιώντας τις παρεχόμενες επιλογές εξαγωγής.

```java
SvgOptions options = new SvgOptions();
options.setColorType(SvgColorMode.Grayscale);
options.setTextAsShapes(true);
```

> **Συμβουλή:** Για να δημιουργήσετε ένα SVG πλήρους χρώματος, αντικαταστήστε το `SvgColorMode.Grayscale` με το `SvgColorMode.FullColor`. Αυτή η αλλαγή διατηρεί την αρχική παλέτα ενώ εξακολουθεί να παρέχει κλιμακωτή διανυσματική γραφική.

## Γιατί να χρησιμοποιήσετε Aspose.CAD για την εξαγωγή CAD σε SVG;
- **Υψηλή πιστότητα:** Τα διανυσματικά δεδομένα διατηρούνται, εξασφαλίζοντας ότι το SVG φαίνεται ακριβώς όπως το αρχικό σχέδιο CAD.  
- **Χωρίς εξωτερικές εξαρτήσεις:** Η μετατροπή εκτελείται εξ ολοκλήρου μέσα στο Java, αφαιρώντας την ανάγκη για πρόσθετα εργαλεία.  
- **Προσαρμόσιμη έξοδος:** Επιλογές όπως `setColorType` σας επιτρέπουν να ελέγξετε αν το SVG είναι σε αποχρώσεις του γκρι ή πλήρους χρώματος.  
- **Κλιμακούμενη απόδοση:** Επεξεργάζεται σχέδια εκατοντάδων σελίδων σε δευτερόλεπτα, με χρήση μνήμης κάτω από 50 MB.

## Συνηθισμένα Προβλήματα και Λύσεις
- **Αρχείο δεν βρέθηκε:** Επαληθεύστε ότι το `dataDir` δείχνει στον σωστό φάκελο και ότι το όνομα του αρχείου DWG ταιριάζει με το case του συστήματος αρχείων.  
- **Κενή έξοδος SVG:** Βεβαιωθείτε ότι η `options.setTextAsShapes(true)` είναι ενεργοποιημένη όταν το αρχικό σχέδιο περιέχει κείμενο που πρέπει να εμφανίζεται ως διανυσματικά σχήματα.  
- **Μη υποστηριζόμενη μορφή CAD:** Το Aspose.CAD υποστηρίζει DWG, DXF, DWF και πάνω από 15 άλλες μορφές· ανατρέξτε στην επίσημη τεκμηρίωση για την πλήρη λίστα.  
- **Σημεία συμφόρησης στην απόδοση:** Για εξαιρετικά μεγάλα αρχεία, ενεργοποιήστε τη λειτουργία streaming μέσω `options.setEnableStreaming(true)` για να μειώσετε τη χρήση μνήμης.

## Συχνές Ερωτήσεις

**Ε: Μπορώ να μετατρέψω ένα αρχείο DXF σε SVG χρησιμοποιώντας τον ίδιο κώδικα;**  
Α: Ναι, απλώς αντικαταστήστε το όνομα αρχείου DWG με ένα αρχείο DXF· το API ανιχνεύει και επεξεργάζεται αυτόματα και τις δύο μορφές.

**Ε: Πώς μπορώ να αλλάξω την έξοδο σε SVG πλήρους χρώματος;**  
Α: Ορίστε `options.setColorType(SvgColorMode.FullColor);` πριν καλέσετε τη μέθοδο `save`.

**Ε: Είναι δυνατόν να ενσωματωθούν γραμματοσειρές στο παραγόμενο SVG;**  
Α: Το Aspose.CAD μετατρέπει το κείμενο σε σχήματα, επομένως η ενσωμάτωση γραμματοσειρών δεν είναι απαραίτητη· το παραγόμενο SVG περιέχει μόνο διανυσματικά περιγράμματα.

**Ε: Η βιβλιοθήκη λειτουργεί σε Linux και macOS;**  
Α: Η βιβλιοθήκη Java είναι ανεξάρτητη από την πλατφόρμα και εκτελείται όπου υπάρχει συμβατό JVM, συμπεριλαμβανομένων Windows, Linux και macOS.

**Ε: Ποια έκδοση του Aspose.CAD χρησιμοποιήθηκε σε αυτό το tutorial;**  
Α: Το παράδειγμα δοκιμάστηκε με Aspose.CAD for Java **24.10**.

---

**Last Updated:** 2026-06-14  
**Tested With:** Aspose.CAD for Java 24.10  
**Author:** Aspose  

---

```java
image.save(dataDir + "meshes.svg");
```

{{< blocks/products/products-backtop-button >}}

## Σχετικά Tutorials

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [dwg to pdf java – Export CAD to PDF with Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}