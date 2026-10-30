---
date: 2026-10-30
description: Μάθετε πώς να αποσυνθέσετε αντικείμενο εισαγωγής CAD σε Java χρησιμοποιώντας
  το Aspose.CAD. Ακολουθήστε αυτόν τον step-by-step οδηγό για να διασπάσετε τα αντικείμενα
  εισαγωγής αποδοτικά.
keywords:
- decompose cad insert
- Aspose.CAD Java
- CAD block extraction
- CAD insert object Java
- CAD entity decomposition
lastmod: 2026-10-30
linktitle: Αποσύνθεση αντικειμένου εισαγωγής CAD με Java
og_description: Μάθετε πώς να αποσυνθέσετε αντικείμενα εισαγωγής CAD χρησιμοποιώντας
  το Aspose.CAD για Java. Αυτό το step-by-step tutorial σας δείχνει πώς να εξάγετε
  block entities αποδοτικά.
og_image_alt: Screenshot of Java code extracting CAD insert objects with Aspose.CAD
og_title: Αποσύνθεση αντικειμένου εισαγωγής CAD με Aspose.CAD σε Java – Quick guide
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to decompose cad insert object in Java using Aspose.CAD.
    Follow this step‑by‑step guide to break down insert objects efficiently.
  headline: Decompose CAD Insert Object with Aspose.CAD In Java
  type: TechArticle
- description: Learn how to decompose cad insert object in Java using Aspose.CAD.
    Follow this step‑by‑step guide to break down insert objects efficiently.
  name: Decompose CAD Insert Object with Aspose.CAD In Java
  steps:
  - name: Set the Resource Directory Path
    text: Define a stable folder that holds all sample drawings. Keeping files in
      a dedicated **DXFDrawings** directory avoids path‑related errors across development
      machines. *Pro tip:* Use `System.getProperty("user.dir")` to build an absolute
      path that works on both Windows and Linux environments.
  - name: Load CAD Image
    text: '`CadImage` is the main class that represents a CAD drawing in memory. When
      you instantiate it with a file path, Aspose.CAD parses the file and builds an
      entity tree ready for traversal. At this point `cadImage` represents the entire
      drawing, including any insert objects it contains.'
  - name: Iterate Through CAD Entities
    text: '`CadEntity` is the base type for every drawable object. By checking the
      entity type you can isolate INSERT objects, fetch their block definitions, and
      then enumerate the inner geometries. `CadBlockEntity` represents a block definition
      that can be referenced by one or more INSERT objects. It contains'
  - name: Dispose of Resources
    text: Aspose.CAD allocates native resources for large drawings. Calling `close()`
      (or using a try‑with‑resources block) releases those handles and prevents memory
      leaks, especially important when processing many files in a batch job.
  type: HowTo
- questions:
  - answer: Yes, you can. Purchase a commercial license to remove evaluation restrictions
      and receive priority support. You can buy a license on the [purchase page](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Absolutely. Download the trial from the official release page and start
      experimenting without cost.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: Temporary licenses are provided for 30‑day evaluation periods via the
      [this link](https://purchase.aspose.com/temporary-license/).
    question: How can I obtain a temporary license for Aspose.CAD for Java?
  - answer: The full API reference is available [Aspose.CAD Java API reference](https://reference.aspose.com/cad/java/).
    question: Where can I find detailed documentation for Aspose.CAD for Java?
  - answer: Yes, the Aspose.CAD distribution includes a “DXFDrawings” folder with
      a variety of sample files for testing.
    question: Are there sample drawings I can use to practice?
  type: FAQPage
second_title: Aspose.CAD Java API
tags:
- decompose CAD
- Aspose.CAD
- Java CAD processing
- CAD block extraction
title: Αποσύνθεση αντικειμένου εισαγωγής CAD με Aspose.CAD σε Java
url: /el/java/additional-features/decompose-cad-insert-object/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποσύνθεση αντικειμένου εισαγωγής CAD με Aspose.CAD σε Java

## Εισαγωγή

Σε αυτό το ολοκληρωμένο tutorial θα μάθετε **πώς να αποσυνθέτετε αντικείμενα εισαγωγής cad** με Aspose.CAD για Java. Είτε δημιουργείτε μια εφαρμογή για επιτραπέζιο υπολογιστή, μια υπηρεσία μετατροπής βασισμένη στο cloud, είτε μια αλυσίδα εξαγωγής δεδομένων, η διάσπαση ενός αντικειμένου εισαγωγής στις μεμονωμένες οντότητές του σας επιτρέπει να αναλύετε, να μετασχηματίζετε ή να εξάγετε κάθε μέρος ανεξάρτητα. Θα περάσουμε από όλη τη ροή εργασίας — από την προετοιμασία του περιβάλλοντος ανάπτυξης μέχρι την επανάληψη πάνω στις οντότητες μπλοκ — ώστε να μπορείτε να αρχίσετε να χειρίζεστε αντικείμενα εισαγωγής CAD αμέσως. Το Aspose.CAD είναι μέρος της οικογένειας βιβλιοθηκών Aspose, διαθέσιμο στη [Aspose releases page](https://releases.aspose.com/).

## Γρήγορες απαντήσεις
- **Τι σημαίνει “decompose cad insert object”;** Σημαίνει την εξαγωγή του ορισμού του μπλοκ (insert) και των θυγατρικών οντοτήτων του από ένα σχέδιο CAD.  
- **Ποια βιβλιοθήκη χρειάζομαι;** Aspose.CAD for Java (τελευταία έκδοση).  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμή λειτουργεί για δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποια μορφές CAD υποστηρίζονται;** DXF, DWG, DWF, DGN και περισσότερες από 30 επιπλέον μορφές.  
- **Πόσο διαρκεί η υλοποίηση;** Περίπου 10‑15 λεπτά για μια βασική εξαγωγή.

## Τι είναι η αποσύνθεση cad insert;

Η αποσύνθεση cad insert είναι η διαδικασία εξαγωγής του υποκείμενου ορισμού μπλοκ μιας οντότητας INSERT και απαρίθμησης κάθε γεωμετρικού στοιχείου που περιέχει. Αυτό επιτρέπει λεπτομερή ανάλυση, επιλεκτική μετατροπή ή προσαρμοσμένη απόδοση κάθε στοιχείου. Αποσπώντας γραμμές, τόξα, κείμενο και άλλα πρωτότυπα, αποκτάτε πλήρη προγραμματιστικό έλεγχο του αρχικού μπλοκ.

## Γιατί να χρησιμοποιήσετε Aspose.CAD για Java;

Το Aspose.CAD για Java υποστηρίζει **30+** μορφές CAD εισόδου και εξόδου — συμπεριλαμβανομένων των DWG, DXF, DWF, DGN και PDF — και μπορεί να επεξεργαστεί σχέδια με εκατοντάδες σελίδες χωρίς να φορτώνει ολόκληρο το αρχείο στη μνήμη. Το API λειτουργεί σε οποιαδήποτε πλατφόρμα συμβατή με Java, δεν απαιτεί εγκατάσταση τοπικού CAD και παρέχει καθοριστική απόδοση που κλιμακώνεται γραμμικά με τον αριθμό των οντοτήτων, καθιστώντας το ιδανικό για επεξεργασία παρτίδων ή υπηρεσίες σε πραγματικό χρόνο.

## Προαπαιτούμενα

- **Βιβλιοθήκη Aspose.CAD for Java** – κατεβάστε την τελευταία έκδοση από τη [Aspose.CAD Java download page](https://releases.aspose.com/cad/java/).  
- **Java Development Kit (JDK) 11 ή νεότερο** – η βιβλιοθήκη είναι μεταγλωττισμένη για Java 8+ αλλά το JDK 11 παρέχει μακροπρόθεσμη υποστήριξη.  
- **Ένα IDE** όπως IntelliJ IDEA, Eclipse ή VS Code με επεκτάσεις Java.  
- **Ένας φάκελος με όνομα `DXFDrawings`** που περιέχει δείγματα αρχείων CAD για δοκιμές.

## Εισαγωγή ονοματοχώρων

Εισάγετε τις απαραίτητες κλάσεις Aspose.CAD για εργασία με αρχεία CAD.

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import java.util.ArrayList;
import java.util.List;
```

## Πώς να αποσυνθέσετε αντικείμενο εισαγωγής CAD χρησιμοποιώντας Aspose.CAD για Java;

Φορτώστε το αρχείο CAD, εντοπίστε κάθε οντότητα INSERT, ανακτήστε το σχετικό μπλοκ και, στη συνέχεια, περάστε από κάθε θυγατρική οντότητα. Η πλήρης διαδικασία μπορεί να εκφραστεί σε τέσσερα σύντομα βήματα, και ο κώδικας εκτελείται σε λιγότερο από ένα δευτερόλεπτο για τυπικά αρχεία DXF.

### Βήμα 1: ορίστε τη διαδρομή του φακέλου πόρων

Ορίστε έναν σταθερό φάκελο που περιέχει όλα τα δείγματα σχεδίων. Η διατήρηση των αρχείων σε έναν αφιερωμένο φάκελο **DXFDrawings** αποφεύγει σφάλματα σχετιζόμενα με διαδρομές σε διαφορετικές μηχανές ανάπτυξης.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
```

*Συμβουλή:* Χρησιμοποιήστε `System.getProperty("user.dir")` για να δημιουργήσετε μια απόλυτη διαδρομή που λειτουργεί τόσο σε Windows όσο και σε Linux.

### Βήμα 2: φορτώστε την εικόνα CAD

`CadImage` είναι η κύρια κλάση που αντιπροσωπεύει ένα σχέδιο CAD στη μνήμη. Όταν την δημιουργείτε με μια διαδρομή αρχείου, το Aspose.CAD αναλύει το αρχείο και δημιουργεί ένα δέντρο οντοτήτων έτοιμο για περιήγηση.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
CadImage cadImage =(CadImage) Image.load(srcFile);
```

Σε αυτό το σημείο το `cadImage` αντιπροσωπεύει ολόκληρο το σχέδιο, συμπεριλαμβανομένων τυχόν αντικειμένων εισαγωγής που περιέχει.

### Βήμα 3: επαναλάβετε τις οντότητες CAD

`CadEntity` είναι ο βασικός τύπος για κάθε αντικείμενο που μπορεί να σχεδιαστεί. Ελέγχοντας τον τύπο της οντότητας μπορείτε να απομονώσετε αντικείμενα INSERT, να ανακτήσετε τους ορισμούς των μπλοκ τους και, στη συνέχεια, να απαριθμήσετε τις εσωτερικές γεωμετρίες.

`CadBlockEntity` αντιπροσωπεύει έναν ορισμό μπλοκ που μπορεί να αναφερθεί από ένα ή περισσότερα αντικείμενα INSERT. Περιέχει τη συλλογή των θυγατρικών οντοτήτων που σχηματίζουν το μπλοκ.

```java
for (int i=0; i<cadImage.getEntities().length;i++)
{
    if (cadImage.getEntities()[i].getTypeName() == CadEntityTypeName.INSERT)
    {
        // Retrieve the block entity
        CadBlockEntity block =
            (CadBlockEntity)cadImage.getBlockEntities().get_Item(((CadInsertObject)cadImage.getEntities()[i]).getName());
            
        // Process entities within the block
        for (CadBaseEntity blockChild : block.getEntities())
        {
            // Process each entity within the block
        }
    }
}
```

**Τι συμβαίνει εδώ;**  
- Σαρώνουμε κάθε οντότητα στο σχέδιο.  
- Όταν συναντάμε μια οντότητα τύπου **INSERT**, ανακτούμε το αντίστοιχο `CadBlockEntity`.  
- Ο εσωτερικός βρόχος σας δίνει πρόσβαση σε κάθε θυγατρική οντότητα (γραμμές, τόξα, κύκλους κ.λπ.) μέσα σε αυτό το μπλοκ, αποσυνθέτοντας ουσιαστικά το αντικείμενο εισαγωγής.

### Βήμα 4: απελευθερώστε τους πόρους

Το Aspose.CAD εκχωρεί εγγενείς πόρους για μεγάλα σχέδια. Η κλήση του `close()` (ή η χρήση ενός μπλοκ try‑with‑resources) απελευθερώνει αυτά τα χειριστήρια και αποτρέπει διαρροές μνήμης, κάτι ιδιαίτερα σημαντικό όταν επεξεργάζεστε πολλά αρχεία σε μια παρτίδα.

```java
finally
{
    cadImage.dispose();
}
```

## Συνηθισμένα προβλήματα & συμβουλές

- **Αναφορά σε μηδενικό μπλοκ:** Εάν ένα INSERT αναφέρεται σε ένα μη υπάρχον μπλοκ, το `get_Item` θα επιστρέψει `null`. Προσθέστε έλεγχο null πριν την επεξεργασία.  
- **Απόδοση:** Για πολύ μεγάλα σχέδια, εξετάστε το φιλτράρισμα των οντοτήτων ανά στρώμα ή τύπο πριν την επανάληψη.  
- **Συστήματα συντεταγμένων:** Τα αντικείμενα εισαγωγής μπορεί να έχουν πίνακες μετασχηματισμού· χρησιμοποιήστε `CadInsertObject.getTransform()` εάν χρειάζεστε απόλυτες συντεταγμένες.  
- **Χρήση μνήμης:** Το Aspose.CAD επεξεργάζεται αρχεία με ροή, αλλά η εκχώρηση ενός `CadImage` για ένα DWG 500 σελίδων εξακολουθεί να καταναλώνει ~150 MB RAM. Απελευθερώστε το άμεσα.

## Συμπέρασμα

Σε αυτό το tutorial, εξετάσαμε τη διαδικασία **αποσύνθεσης αντικειμένου εισαγωγής cad** χρησιμοποιώντας το Aspose.CAD για Java. Με το ισχυρό του API, το Aspose.CAD καθιστά εύκολη την εξαγωγή και τη διαχείριση των εσωτερικών οντοτήτων των αντικειμένων εισαγωγής, ανοίγοντας το δρόμο για προσαρμοσμένη ανάλυση, αγωγούς μετατροπής ή οπτικοποιήσεις. Πειραματιστείτε με τον δείγμα κώδικα, προσαρμόστε τους βρόχους στη δική σας επιχειρηματική λογική, και θα έχετε μια σταθερή βάση για οποιαδήποτε εφαρμογή Java που βασίζεται σε CAD.

Εάν αντιμετωπίσετε προκλήσεις ή έχετε ερωτήσεις, μη διστάσετε να επισκεφθείτε το [support forum](https://forum.aspose.com/c/cad/19).

## Συχνές ερωτήσεις

**Q: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java σε εμπορικό έργο;**  
A: Ναι, μπορείτε. Αγοράστε εμπορική άδεια για να αφαιρέσετε περιορισμούς αξιολόγησης και να λάβετε προτεραιότητα στην υποστήριξη. Μπορείτε να αγοράσετε άδεια στη [purchase page](https://purchase.aspose.com/buy).

**Q: Υπάρχει δωρεάν δοκιμή διαθέσιμη για το Aspose.CAD για Java;**  
A: Απόλυτα. Κατεβάστε τη δοκιμή από τη σελίδα επίσημης κυκλοφορίας και ξεκινήστε να πειραματίζεστε χωρίς κόστος.

**Q: Πώς μπορώ να αποκτήσω προσωρινή άδεια για το Aspose.CAD για Java;**  
A: Παρέχονται προσωρινές άδειες για περιόδους αξιολόγησης 30 ημερών μέσω του [this link](https://purchase.aspose.com/temporary-license/).

**Q: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD για Java;**  
A: Η πλήρης αναφορά API είναι διαθέσιμη στο [Aspose.CAD Java API reference](https://reference.aspose.com/cad/java/).

**Q: Υπάρχουν δείγματα σχεδίων που μπορώ να χρησιμοποιήσω για εξάσκηση;**  
A: Ναι, η διανομή του Aspose.CAD περιλαμβάνει έναν φάκελο “DXFDrawings” με ποικιλία δειγμάτων αρχείων για δοκιμές.

---

**Last Updated:** 2026-10-30  
**Tested With:** Aspose.CAD for Java 24.11  
**Author:** Aspose  

## Σχετικά tutorials

- [Πώς να εξάγετε χαρακτηριστικά - Τιμή χαρακτηριστικού μπλοκ από εξωτερική αναφορά χρησιμοποιώντας Aspose.CAD σε Java](/cad/java/advanced-cad-features/extract-block-attribute-value/)
- [Πώς να διαβάσετε αρχεία DWT με Aspose.CAD για Java](/cad/java/advanced-cad-features/reading-dwt-files/)
- [Ορισμός μεγέθους καμβά – Προηγμένα χαρακτηριστικά CAD με Aspose.CAD για Java](/cad/java/advanced-cad-features/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}