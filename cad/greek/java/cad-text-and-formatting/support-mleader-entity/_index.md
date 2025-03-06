---
title: Υποστήριξη MLeader Entity για μορφή DWG με Aspose.CAD για Java
linktitle: Υποστήριξη MLEAder Entity για μορφή DWG με Java
second_title: Aspose.CAD Java API
description: Ξεκλειδώστε τη δύναμη του Aspose.CAD για Java με το βήμα προς βήμα εκμάθησή μας για την υποστήριξη οντοτήτων MLeader σε μορφή DWG.
weight: 12
url: /el/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Υποστήριξη MLeader Entity για μορφή DWG με Aspose.CAD για Java

## Εισαγωγή

Στον τομέα του σχεδιασμού με τη βοήθεια υπολογιστή (CAD) με Java, η κατανόηση και η υλοποίηση υποστήριξης για οντότητες MLeader σε μορφή DWG είναι μια πολύτιμη δεξιότητα. Το Aspose.CAD για Java παρέχει μια ισχυρή λύση για τέτοιες εργασίες, προσφέροντας ένα σύνολο ισχυρών εργαλείων και λειτουργιών. Αυτό το σεμινάριο θα σας καθοδηγήσει στη διαδικασία υποστήριξης οντοτήτων MLeader σε αρχεία DWG χρησιμοποιώντας Java με Aspose.CAD.

## Προαπαιτούμενα

Πριν εμβαθύνουμε στο σεμινάριο, βεβαιωθείτε ότι έχετε τις ακόλουθες προϋποθέσεις:

1. Περιβάλλον ανάπτυξης Java: Βεβαιωθείτε ότι έχετε ρυθμίσει ένα περιβάλλον ανάπτυξης Java στο σύστημά σας.

2.  Aspose.CAD Library: Κάντε λήψη και εγκατάσταση της βιβλιοθήκης Aspose.CAD για Java από το[σύνδεσμος λήψης](https://releases.aspose.com/cad/java/).

## Εισαγωγή χώρων ονομάτων

Στο έργο σας Java, εισαγάγετε τους απαραίτητους χώρους ονομάτων για να αξιοποιήσετε αποτελεσματικά τις δυνατότητες του Aspose.CAD. Συμπεριλάβετε τις ακόλουθες γραμμές στον κώδικά σας:

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

Τώρα, ας αναλύσουμε τον κώδικα σε έναν οδηγό βήμα προς βήμα για την υποστήριξη οντοτήτων MLeader για μορφή DWG χρησιμοποιώντας Java με Aspose.CAD.

## 1. Φορτώστε το αρχείο DWG και αποκτήστε πρόσβαση στο CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Επικύρωση οντοτήτων MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Επαληθεύστε το στυλ και τα χαρακτηριστικά του MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Πρόσβαση στα δεδομένα περιβάλλοντος MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Επικύρωση χαρακτηριστικών περιβάλλοντος

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Πρόσβαση στον κόμβο MLeader και στη γραμμή Leader

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. Επικύρωση πρόσθετων χαρακτηριστικών MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Επικύρωση χαρακτηριστικών κειμένου

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Πρόσθετα χαρακτηριστικά MLeader

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## συμπέρασμα

Συγχαρητήρια! Περιηγηθήκατε με επιτυχία στον αναλυτικό οδηγό για την υποστήριξη οντοτήτων MLeader για μορφή DWG χρησιμοποιώντας Java και Aspose.CAD. Αυτή η δυνατότητα ανοίγει πόρτες σε προηγμένους χειρισμούς CAD και βελτιώνει το κιτ εργαλείων ανάπτυξης Java.

## Συχνές ερωτήσεις

### Ε1: Μπορώ να χρησιμοποιήσω το Aspose.CAD για Java με άλλες μορφές CAD;

A1: Ναι, το Aspose.CAD υποστηρίζει διάφορες μορφές CAD πέρα από το DWG, παρέχοντας ευελιξία στα έργα σας.

### Ε2: Πού μπορώ να βρω λεπτομερή τεκμηρίωση για το Aspose.CAD για Java;

 A2: Ανατρέξτε στο[τεκμηρίωση](https://reference.aspose.com/cad/java/) για εις βάθος πληροφορίες σχετικά με τις δυνατότητες του Aspose.CAD.

### Ε3: Υπάρχει διαθέσιμη δωρεάν δοκιμή;

 A3: Ναι, εξερευνήστε τις λειτουργίες από πρώτο χέρι με το[δωρεάν δοκιμή](https://releases.aspose.com/).

### Ε4: Πώς μπορώ να λάβω προσωρινή άδεια χρήσης για το Aspose.CAD;

A4: Λάβετε μια προσωρινή άδεια μέσω[αυτός ο σύνδεσμος](https://purchase.aspose.com/temporary-license/).

### Ε5: Πού μπορώ να αναζητήσω κοινοτική υποστήριξη και βοήθεια;

A5: Επισκεφθείτε το[Φόρουμ Aspose.CAD](https://forum.aspose.com/c/cad/19) για να συνδεθείτε με την κοινότητα και να λάβετε βοήθεια.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
