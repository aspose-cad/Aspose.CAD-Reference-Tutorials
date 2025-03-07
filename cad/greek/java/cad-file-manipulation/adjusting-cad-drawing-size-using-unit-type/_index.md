---
title: Προσαρμογή μεγέθους σχεδίου CAD με χρήση Unit Type με Aspose.CAD για Java
linktitle: Προσαρμογή μεγέθους σχεδίου CAD με χρήση του τύπου μονάδας
second_title: Aspose.CAD Java API
description: Εξερευνήστε τη δύναμη του Aspose.CAD για Java στην προσαρμογή των μεγεθών σχεδίασης CAD χωρίς κόπο. Ακολουθήστε τον βήμα προς βήμα οδηγό μας για ακρίβεια και προσαρμοστικότητα.
weight: 14
url: /el/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Προσαρμογή μεγέθους σχεδίου CAD με χρήση Unit Type με Aspose.CAD για Java

## Εισαγωγή

Στη συνεχώς εξελισσόμενη σφαίρα του Computer-Aided Design (CAD), η ακρίβεια και η προσαρμοστικότητα είναι πρωταρχικής σημασίας. Μια κοινή απαίτηση είναι η προσαρμογή του μεγέθους των σχεδίων CAD με βάση συγκεκριμένους τύπους μονάδων. Το Aspose.CAD για Java αναδεικνύεται ως ένας ισχυρός σύμμαχος, παρέχοντας απρόσκοπτες δυνατότητες χειρισμού αρχείων CAD μέσω προγραμματισμού.

## Προαπαιτούμενα

Πριν ξεκινήσετε το σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

- Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα λειτουργικό περιβάλλον ανάπτυξης Java στον υπολογιστή σας.

-  Aspose.CAD για Java Library: Κατεβάστε και ενσωματώστε τη βιβλιοθήκη Aspose.CAD στο έργο σας Java. Μπορείτε να αποκτήσετε τη βιβλιοθήκη[εδώ](https://releases.aspose.com/cad/java/).

## Εισαγωγή χώρων ονομάτων

Στον κώδικα Java, συμπεριλάβετε τους απαραίτητους χώρους ονομάτων για πρόσβαση στις λειτουργίες Aspose.CAD. Προσθέστε τις ακόλουθες εισαγωγές:

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Τώρα, ας αναλύσουμε τη διαδικασία προσαρμογής του μεγέθους σχεδίου CAD χρησιμοποιώντας τον τύπο μονάδας σε διαχειρίσιμα βήματα:

## Βήμα 1: Ορισμός καταλόγου δεδομένων

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Ορίστε τη διαδρομή για τον κατάλογο όπου βρίσκονται τα αρχεία CAD.

## Βήμα 2: Φόρτωση σχεδίου CAD

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Φορτώστε το σχέδιο CAD χρησιμοποιώντας το Aspose.CAD's`Image` τάξη.

## Βήμα 3: Δημιουργία Επιλογών BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Στιγμιότυπο το`BmpOptions` κλάση για εξαγωγή της διάταξης CAD σε μορφή BMP.

## Βήμα 4: Διαμόρφωση επιλογών ραστεροποίησης

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Δημιουργήστε ένα παράδειγμα του`CadRasterizationOptions` και συσχετίστε το με το`BmpOptions` για διανυσματική ραστεροποίηση.

## Βήμα 5: Ορίστε τον τύπο μονάδας

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Καθορίστε τον επιθυμητό τύπο μονάδας για το σχέδιο CAD. Σε αυτό το παράδειγμα, το έχουμε ορίσει σε Centimeter.

## Βήμα 6: Ορισμός διατάξεων

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Καθορίστε τις διατάξεις που πρέπει να λαμβάνονται υπόψη κατά την εξαγωγή. Σε αυτήν την περίπτωση, έχουμε επιλέξει τη διάταξη "Μοντέλο".

## Βήμα 7: Εξαγωγή σε BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Τέλος, αποθηκεύστε το τροποποιημένο σχέδιο CAD σε μορφή BMP.

## συμπέρασμα

Με το Aspose.CAD για Java, η προσαρμογή των μεγεθών σχεδίων CAD γίνεται παιχνιδάκι. Αυτό το σεμινάριο σας καθοδήγησε στη διαδικασία, τονίζοντας τη σημασία κάθε βήματος για την επίτευξη ακριβών αποτελεσμάτων.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλες γλώσσες προγραμματισμού;

A1: Το Aspose.CAD υποστηρίζει κυρίως Java, αλλά υπάρχουν διαθέσιμες εκδόσεις για άλλες γλώσσες όπως το .NET.

### Ε2: Υπάρχουν επιλογές αδειοδότησης για το Aspose.CAD;

 A2: Ναι, μπορείτε να εξερευνήσετε τις επιλογές αδειοδότησης και να αγοράσετε το Aspose.CAD[εδώ](https://purchase.aspose.com/buy).

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή για το Aspose.CAD;

 A3: Σίγουρα, μπορείτε να έχετε πρόσβαση σε μια δωρεάν δοκιμή[εδώ](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω υποστήριξη για το Aspose.CAD για Java;

 A4: Επισκεφθείτε το φόρουμ Aspose.CAD[εδώ](https://forum.aspose.com/c/cad/19) για ολοκληρωμένη υποστήριξη.

### Ε5: Μπορώ να αποκτήσω μια προσωρινή άδεια για το Aspose.CAD;

 A5: Ναι, μπορείτε να αποκτήσετε μια προσωρινή άδεια[εδώ](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
