---
date: 2026-03-02
description: Αποκαλύψτε το δυναμικό του Aspose.CAD για Java. Εξαγάγετε εύκολα αντικείμενα
  OLE και **αποθηκεύστε CAD ως PNG**. Κατεβάστε τώρα για απρόσκοπτη διαχείριση δεδομένων
  CAD.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Αποθήκευση CAD ως PNG – Εξαγωγή αντικειμένων OLE χρησιμοποιώντας το Aspose.CAD
  για Java
url: /el/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Αποθήκευση CAD ως PNG – Εξαγωγή αντικειμένων OLE χρησιμοποιώντας το Aspose.CAD για Java

## Εισαγωγή

Στον δυναμικό κόσμο του Computer-Aided Design (CAD), η διαχείριση και εξαγωγή αντικειμένων OLE (Object Linking and Embedding) αποδοτικά—και η δυνατότητα **save CAD as PNG**—είναι κρίσιμη για τις επόμενες διαδικασίες όπως η αναφορά, η προεπισκόπηση στο web ή η αρχειοθέτηση. Το Aspose.CAD for Java παρέχει μια ισχυρή, code‑first λύση που σας επιτρέπει τόσο την εξαγωγή αντικειμένων OLE όσο και τη μετατροπή σχεδίων CAD σε εικόνες PNG υψηλής ποιότητας με λίγες μόνο γραμμές κώδικα.

## Γρήγορες Απαντήσεις
- **What does Aspose.CAD do?** Διαβάζει, επεξεργάζεται και μετατρέπει αρχεία CAD (DWG, DXF, DGN κ.λπ.) χωρίς την ανάγκη εγγενούς λογισμικού CAD.  
- **Can I save CAD as PNG?** Ναι—χρησιμοποιήστε το `PngOptions` μαζί με το `CadRasterizationOptions` για να rasterize οποιαδήποτε διάταξη.  
- **How to export OLE objects?** Φορτώστε το αρχείο CAD με `Image.load` και αποθηκεύστε κάθε διάταξη που περιέχει OLE ως PNG.  
- **Do I need a license?** Διατίθεται δωρεάν δοκιμή· μια εμπορική άδεια αφαιρεί τους περιορισμούς αξιολόγησης.  
- **What Java version is required?** Η Java 8 ή νεότερη υποστηρίζεται πλήρως.

## Τι είναι **save CAD as PNG**;
Η αποθήκευση CAD ως PNG σημαίνει rasterizing διανυσματικών σχεδίων CAD σε εικόνα PNG βασισμένη σε pixel. Αυτή η μετατροπή είναι χρήσιμη όταν χρειάζεστε μια ελαφριά, καθολικά προβολή μορφή για ιστοσελίδες, κινητές εφαρμογές ή τεκμηρίωση.

## Γιατί να χρησιμοποιήσετε το Aspose.CAD για Java για **convert CAD to PNG**;
- **No CAD installation needed** – η βιβλιοθήκη λειτουργεί εξ ολοκλήρου σε Java.  
- **Preserves layout fidelity** – μπορείτε να επιλέξετε συγκεκριμένες διατάξεις, να ελέγξετε το DPI και να διατηρήσετε την ποιότητα των γραμμών.  
- **Batch processing** – επαναλάβετε πάνω σε πολλά αρχεία με έναν απλό βρόχο.  
- **Export OLE objects** – το περιεχόμενο OLE ενσωματωμένο σε αρχεία DWG/DXF αποδίδεται αυτόματα στην έξοδο PNG.

## Προαπαιτούμενα

Πριν βυθιστείτε στο tutorial, βεβαιωθείτε ότι έχετε τα παρακάτω προαπαιτούμενα:

- **Java Environment** – Βεβαιωθείτε ότι έχετε ένα περιβάλλον ανάπτυξης Java εγκατεστημένο στο μηχάνημά σας.  
- **Aspose.CAD for Java** – Κατεβάστε και εγκαταστήστε τη βιβλιοθήκη Aspose.CAD for Java. Μπορείτε να βρείτε τη βιβλιοθήκη στον [download link](https://releases.aspose.com/cad/java/).  
- **CAD Files** – Προετοιμάστε τα αρχεία CAD που περιέχουν αντικείμενα OLE που θέλετε να εξάγετε.

## Εισαγωγή Namespaces

Για να ξεκινήσετε, εισάγετε τα απαραίτητα namespaces στο πρότζεκτ Java σας. Αυτά τα namespaces παρέχουν τις βασικές κλάσεις και λειτουργίες που απαιτούνται για εργασία με αρχεία CAD χρησιμοποιώντας το Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία εξαγωγής αντικειμένων OLE από CAD σε πολλαπλά βήματα:

## Πώς να **save CAD as PNG** και να εξάγετε αντικείμενα OLE

### Βήμα 1: Ορίστε τον Κατάλογο Εγγράφων σας

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Βεβαιωθείτε ότι αντικαθιστάτε `"Your Document Directory"` με τη διαδρομή προς τον κατάλογο που περιέχει τα αρχεία CAD σας.

### Βήμα 2: Ορίστε τα Ονόματα Αρχείων CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Καθορίστε τα ονόματα των αρχείων CAD που θέλετε να επεξεργαστείτε στον πίνακα `files`.

### Βήμα 3: Ορίστε τις Επιλογές Εξαγωγής PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Διαμορφώστε τις επιλογές εξαγωγής PNG, συμπεριλαμβανομένου του rasterization διανυσμάτων και των ρυθμίσεων διάταξης. Αυτές οι επιλογές είναι αυτές που σας επιτρέπουν να **convert CAD to PNG** με την επιθυμητή ποιότητα.

### Βήμα 4: Επανάληψη μέσω Αρχείων CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Επαναλάβετε για κάθε καθορισμένο αρχείο CAD, φορτώστε το χρησιμοποιώντας το Aspose.CAD και αποθηκεύστε τα αντικείμενα OLE ως εικόνες PNG. Αυτός ο βρόχος δείχνει έναν απλό τρόπο να **convert DWG to PNG** μαζικά.

## Συχνά Προβλήματα και Λύσεις

| Πρόβλημα | Αιτία | Λύση |
|----------|-------|------|
| **Blank PNG output** | Ασυμφωνία ονόματος διάταξης | Επαληθεύστε ότι το όνομα διάταξης (`"Layout1"`) υπάρχει στο πηγαίο DWG. |
| **Missing OLE graphics** | Τα αντικείμενα OLE αποθηκεύονται σε διαφορετική διάταξη | Συμπεριλάβετε όλες τις σχετικές διατάξεις στο `rasterizationOptions.setLayouts(...)`. |
| **Out‑of‑memory error on large files** | Ρυθμίσεις υψηλού DPI | Μειώστε το DPI μέσω `rasterizationOptions.setResolution(...)` ή επεξεργαστείτε τα αρχεία ένα προς ένα. |

## Συχνές Ερωτήσεις

**Q: Is Aspose.CAD compatible with all CAD file formats?**  
A: Το Aspose.CAD υποστηρίζει διάφορες μορφές CAD, συμπεριλαμβανομένων των DWG, DXF και DGN. Ανατρέξτε στην [documentation](https://reference.aspose.com/cad/java/) για την πλήρη λίστα.

**Q: Can I customize the export settings for OLE objects?**  
A: Ναι, το Aspose.CAD παρέχει εκτενείς επιλογές προσαρμογής των ρυθμίσεων εξαγωγής, επιτρέποντάς σας να προσαρμόσετε το αποτέλεσμα στις συγκεκριμένες απαιτήσεις σας.

**Q: Is there a free trial available for Aspose.CAD?**  
A: Ναι, μπορείτε να εξερευνήσετε τις δυνατότητες του Aspose.CAD αποκτώντας μια δωρεάν δοκιμή από [εδώ](https://releases.aspose.com/).

**Q: Where can I get community support for Aspose.CAD?**  
A: Ενταχθείτε στην κοινότητα Aspose.CAD στο [forum](https://forum.aspose.com/c/cad/19) για βοήθεια και ανταλλαγή εμπειριών.

**Q: How can I purchase a license for Aspose.CAD?**  
A: Επισκεφθείτε τη [purchase page](https://purchase.aspose.com/buy) για να αποκτήσετε άδεια που ταιριάζει στις ανάγκες ανάπτυξής σας.

## Συμπέρασμα

Με αυτά τα απλά αλλά ισχυρά βήματα, μπορείτε απρόσκοπτα να **save CAD as PNG** ενώ εξάγετε αντικείμενα OLE από αρχεία CAD χρησιμοποιώντας το Aspose.CAD για Java. Αυτό το ευέλικτο εργαλείο ενδυναμώνει τους προγραμματιστές να διαχειρίζονται δεδομένα CAD αποδοτικά, ανοίγοντας νέες δυνατότητες στην ανάπτυξη εφαρμογών CAD και σε downstream ροές εργασίας βασισμένες σε εικόνες.

---

**Τελευταία ενημέρωση:** 2026-03-02  
**Δοκιμή με:** Aspose.CAD for Java 24.12  
**Συγγραφέας:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}