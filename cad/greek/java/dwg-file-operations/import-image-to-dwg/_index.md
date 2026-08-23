---
date: 2026-05-20
description: Μάθετε πώς να προσθέσετε εικόνα σε αρχεία DWG χρησιμοποιώντας Aspose.CAD
  για Java και επίσης να μετατρέψετε DWG σε PDF. Ακολουθήστε τον βήμα-βήμα οδηγό μας
  για αποδοτική ανάπτυξη.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Εισαγωγή εικόνας σε αρχείο DWG χρησιμοποιώντας Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Προσθέστε εικόνα σε αρχεία DWG χωρίς κόπο χρησιμοποιώντας Aspose.CAD Java
url: /el/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσθήκη εικόνας σε αρχεία DWG χωρίς κόπο χρησιμοποιώντας το Aspose.CAD Java

Σε σύγχρονες εφαρμογές Java, η **προσθήκη εικόνας σε DWG** είναι συχνή απαίτηση — είτε δημιουργείτε έναν προβολέα CAD, αυτοματοποιείτε ενημερώσεις σχεδίων ή παράγετε τεκμηρίωση. Το Aspose.CAD for Java προσφέρει έναν απλό, υψηλής απόδοσης τρόπο ενσωμάτωσης raster εικόνων απευθείας σε σχέδια DWG χωρίς την ανάγκη πλήρους μηχανής CAD. Σε αυτό το tutorial θα σας καθοδηγήσουμε σε όλη τη διαδικασία, από τη φόρτωση ενός DWG μέχρι την εξαγωγή του αποτελέσματος ως PDF, και θα καλύψουμε επίσης πώς να **εισάγετε εικόνα σε dwg** και **μετατρέψετε dwg σε pdf** σε μια ενιαία ροή εργασίας.

## Γρήγορες Απαντήσεις
- **Ποια βιβλιοθήκη χρειάζομαι;** Aspose.CAD for Java  
- **Μπορώ επίσης να εξάγω σε PDF;** Ναι – use `PdfOptions` with `CadRasterizationOptions`  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή  
- **Ποια έκδοση Java υποστηρίζεται;** Java 8 και νεότερη  
- **Πόσο χρόνο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για μια βασική εισαγωγή εικόνας  

## Τι είναι η “προσθήκη εικόνας σε dwg”;

Η προσθήκη εικόνας σε αρχείο DWG σημαίνει την ενσωμάτωση μιας raster εικόνας (PNG, JPEG κ.λπ.) ως οντότητα **CadRasterImage** μέσα στο μοντέλο του σχεδίου, όπου μπορεί να τοποθετηθεί, κλιμακωθεί και προαιρετικά να περικοπεί όπως κάθε άλλο αντικείμενο CAD. Αποθηκεύεται στον πίνακα αντικειμένων του σχεδίου και εμφανίζεται από τους τυπικούς προβολείς CAD.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD for Java για την προσθήκη εικόνας σε dwg;

Μπορείτε να ενσωματώσετε raster γραφικά σε αρχεία DWG χωρίς εγκατάσταση τρίτου λογισμικού CAD, και το API σας δίνει έλεγχο pixel‑perfect πάνω στο σημείο εισαγωγής, τα διανύσματα κλιμάκωσης και τα όρια περικοπής. Το Aspose.CAD επεξεργάζεται αρχεία έως 2 GB, υποστηρίζει **50+ μορφές εισόδου και εξόδου**, και λειτουργεί σε Windows, Linux και macOS, επιτρέποντάς σας να ενσωματώσετε επεξεργασία CAD σε οποιοδήποτε backend Java.

## Προαπαιτούμενα
- **Aspose.CAD for Java** – κατεβάστε το τελευταίο JAR από την επίσημη ιστοσελίδα **[here](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 ή νεότερο, με το προτιμώμενο IDE σας (IntelliJ IDEA, Eclipse, VS Code, κλ.).  
- Μία έγκυρη **Aspose.CAD license** για παραγωγική χρήση (η δοκιμαστική έκδοση λειτουργεί για πειραματισμό).  

## Εισαγωγή Πακέτων
Οι παρακάτω εισαγωγές φέρνουν τις απαραίτητες κλάσεις του Aspose.CAD που χρησιμοποιούνται για τη διαχείριση εικόνας και τη μετατροπή σε PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Οδηγός βήμα‑βήμα

### Βήμα 1: Φόρτωση του αρχείου DWG
Πρώτα, εντοπίστε το φάκελο που περιέχει το σχέδιο DWG και φορτώστε το με `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Βήμα 2: Ορισμός του ορισμού Raster Image
Η κλάση `CadRasterImageDef` ορίζει τον εξωτερικό πόρο raster εικόνας που θα ενσωματωθεί στο σχέδιο.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Βήμα 3: Ορισμός σημείου εισαγωγής και διανυσμάτων κλιμάκωσης
Το σημείο εισαγωγής καθορίζει πού θα εμφανιστεί η κάτω‑αριστερή γωνία της εικόνας. Τα διανύσματα **U** και **V** ελέγχουν την οριζόντια και κάθετη κλιμάκωση.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Βήμα 4: Δημιουργία του αντικειμένου CadRasterImage
Η οντότητα `CadRasterImage` αντιπροσωπεύει μια raster εικόνα τοποθετημένη στο μοντέλο του DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Βήμα 5: Προσθήκη της εικόνας στο Model Space
Εισάγετε την raster εικόνα στο μπλοκ `*Model_Space`, έπειτα ενημερώστε τη συλλογή αντικειμένων του σχεδίου ώστε ο ορισμός να αποθηκευτεί.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Βήμα 6: Διαμόρφωση επιλογών εξαγωγής PDF (Προαιρετικό)
`PdfOptions` καθορίζει τις ρυθμίσεις για αποθήκευση ενός σχεδίου CAD ως αρχείο PDF. `CadRasterizationOptions` ορίζει πώς το περιεχόμενο CAD θα rasterαριστεί κατά τη μετατροπή σε PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Βήμα 7: Αποθήκευση του παραγόμενου PDF
Τέλος, εξάγετε το τροποποιημένο σχέδιο ως αρχείο PDF. Η ίδια παρουσία `image` χρησιμοποιείται, έτσι το PDF αντικατοπτρίζει τη νεοεισαγμένη raster εικόνα.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

Ακολουθώντας αυτά τα βήματα, μπορείτε να **προσθέσετε εικόνα σε dwg** αρχεία γρήγορα και επίσης **αποθηκεύσετε dwg ως pdf** όταν χρειάζεται, καλύπτοντας τις πιο συνηθισμένες **λειτουργίες αρχείων dwg** σε μια ενιαία, συμπαγή ρουτίνα.

## Συχνά Προβλήματα και Λύσεις
- **Η εικόνα δεν εμφανίζεται** – Επαληθεύστε ότι η διαδρομή του αρχείου εικόνας (`road-sign-custom.png`) είναι σωστή και ότι οι διαστάσεις της εικόνας ταιριάζουν με τις τιμές που περάστηκαν στο `CadRasterImageDef`.  
- **Λανθασμένη κλιμάκωση** – Προσαρμόστε τα διανύσματα U και V· αντιπροσωπεύουν τις μονάδες σχεδίασης ανά pixel.  
- **Το PDF φαίνεται κενό** – Βεβαιωθείτε ότι το `CadRasterizationOptions.setDrawType` είναι ορισμένο σε `UseObjectColor` ή άλλη κατάλληλη λειτουργία.  

## Συχνές Ερωτήσεις

**Q: Είναι το Aspose.CAD for Java συμβατό με όλα τα περιβάλλοντα ανάπτυξης Java;**  
A: Ναι, το Aspose.CAD for Java λειτουργεί με οποιοδήποτε IDE που υποστηρίζει JDK 8+, συμπεριλαμβανομένων των IntelliJ IDEA, Eclipse και VS Code.

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD for Java για εμπορικά έργα;**  
A: Ναι, μπορείτε να χρησιμοποιήσετε το Aspose.CAD for Java για εμπορικά έργα. Επισκεφθείτε **[here](https://purchase.aspose.com/buy)** για λεπτομέρειες αδειοδότησης.

**Q: Υπάρχει δωρεάν δοκιμαστική έκδοση του Aspose.CAD for Java;**  
A: Ναι, μπορείτε να αποκτήσετε τη δωρεάν δοκιμή **[here](https://releases.aspose.com/)**.

**Q: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD for Java;**  
A: Μπορείτε να ζητήσετε υποστήριξη στο **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.

**Q: Μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD for Java;**  
A: Ναι, μπορείτε να πάρετε προσωρινή άδεια **[here](https://purchase.aspose.com/temporary-license/)**.

**Τελευταία ενημέρωση:** 2026-05-20  
**Δοκιμάστηκε με:** Aspose.CAD for Java 24.11  
**Συγγραφέας:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Σχετικά Μαθήματα

- [Εξαγωγή DWG σε PDF ή Raster χρησιμοποιώντας το Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Προσθήκη προσαρμοσμένων ιδιοτήτων σε αρχεία DWG χρησιμοποιώντας το Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Αποθήκευση CAD ως PNG – Μετατροπή σχεδίου CAD σε μορφή raster εικόνας χρησιμοποιώντας το Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}