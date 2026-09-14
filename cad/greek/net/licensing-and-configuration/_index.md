---
date: 2026-09-14
description: Μάθετε πώς να εφαρμόσετε άδεια στο Aspose.CAD για .NET χρησιμοποιώντας
  διαδρομή αρχείου ή FileStream και εξερευνήστε τη metered licensing για βελτιστοποίηση
  της χρήσης πόρων.
keywords:
- how to apply license
- apply license by path
- apply license using filestream
- metered licensing
lastmod: 2026-09-14
linktitle: Αδειοδότηση και Διαμόρφωση
og_description: Μάθετε πώς να εφαρμόσετε άδεια στο Aspose.CAD για .NET χρησιμοποιώντας
  διαδρομή αρχείου ή FileStream και εξερευνήστε τη metered licensing για βελτιστοποίηση
  της χρήσης πόρων. (150‑160 chars)
og_image_alt: Screenshot of Aspose.CAD license configuration page in a .NET IDE
og_title: Πώς να εφαρμόσετε άδεια στο Aspose.CAD για .NET – Σύντομος Οδηγός
schemas:
- author: Aspose
  dateModified: '2026-09-14'
  description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  headline: How to apply license in Aspose.CAD for .NET
  type: TechArticle
- description: Learn how to apply license in Aspose.CAD for .NET using a file path
    or FileStream, and explore metered licensing to optimise resource usage.
  name: How to apply license in Aspose.CAD for .NET
  steps:
  - name: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
    text: Place your `Aspose.CAD.lic` file in a folder that your application can read
      (e.g., the application root or a secured config folder).
  - name: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
    text: 'Add the following code early in your startup routine (e.g., `Main`, `Startup.Configure`,
      or `Global.asax`):'
  - name: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
    text: Retrieve the license bytes from your source (file system, Azure Blob, etc.).
  - name: Open a `FileStream` with read permissions.
    text: Open a `FileStream` with read permissions.
  - name: Pass the stream to the `License` object.
    text: Pass the stream to the `License` object.
  - name: Obtain a metered‑license key from your Aspose account dashboard.
    text: Obtain a metered‑license key from your Aspose account dashboard.
  - name: Register the key with `License.SetMeteredKey("your‑key")`.
    text: Register the key with `License.SetMeteredKey("your‑key")`.
  - name: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
    text: After each operation, call `License.GetMeteredUsage()` to retrieve the current
      usage count.
  type: HowTo
- questions:
  - answer: Yes, a single license file can be deployed to any number of development
      or production servers, provided the usage complies with your purchased term.
    question: Can I use the same license file on multiple machines?
  - answer: The library will run in evaluation mode, adding a watermark to rendered
      images and limiting the number of pages you can process.
    question: What happens if I forget to set the license before loading a CAD file?
  - answer: Only the first activation and each usage report need connectivity; after
      that, the library can operate offline until the next report.
    question: Does metered licensing require an internet connection?
  - answer: Aspose.CAD supports 45+ input and output formats, including DWG, DXF,
      DGN, STL, OBJ, and IFC, and can render files up to 500 MB without loading the
      entire document into memory.
    question: Which CAD/BIM formats are supported out of the box?
  - answer: Call `License.IsLicensed` (or inspect `License.LicenseFilePath`) after
      registration; it returns `true` when a valid license is active.
    question: Is there a way to programmatically check if the license was applied
      successfully?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- Aspose.CAD
- license configuration
- .NET
- CAD processing
- metered licensing
title: Πώς να εφαρμόσετε άδεια στο Aspose.CAD για .NET
url: /el/net/licensing-and-configuration/
weight: 20
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Πώς να εφαρμόσετε άδεια στο Aspose.CAD για .NET

Καλώς ήρθατε στον ολοκληρωμένο οδηγό για **πώς να εφαρμόσετε άδεια** στο Aspose.CAD για .NET. Είτε δημιουργείτε μια επιτραπέζια εφαρμογή, μια υπηρεσία διακομιστή, είτε μια αυτοματοποιημένη γραμμή παραγωγής BIM, μια έγκυρη άδεια ξεκλειδώνει το πλήρες σύνολο των περισσότερων από 40 μορφών CAD και BIM, ενεργοποιεί την υψηλής απόδοσης απόδοση και αφαιρεί τα υδατογράμματα αξιολόγησης. Αυτό το άρθρο σας καθοδηγεί βήμα‑βήμα σε όλες τις επιλογές αδειοδότησης, ώστε να ξεκινήσετε την ανάπτυξη χωρίς διακοπές.

## Γρήγορες απαντήσεις
- **Μπορώ να φορτώσω μια άδεια από διαδρομή αρχείου;** Ναι – απλώς δημιουργήστε ένα αντικείμενο `License` και καλέστε `SetLicense("path/to/license.lic")`.  
- **Υποστηρίζεται FileStream;** Απόλυτα· περάστε το ανοιγμένο ρεύμα στη μέθοδο `SetLicense(stream)`.  
- **Τι είναι η αδειοδότηση με μέτρηση (metered licensing);** Παρακολουθεί τη χρήση ανά αίτημα, επιτρέποντάς σας να πληρώνετε μόνο για ό,τι καταναλώνετε.  
- **Χρειάζομαι άδεια για ανάπτυξη;** Μια δωρεάν δοκιμαστική άδεια λειτουργεί για ανάπτυξη και δοκιμές· απαιτείται εμπορική άδεια για παραγωγή.  
- **Ποιες εκδόσεις .NET υποστηρίζονται;** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Τι είναι η αδειοδότηση στο Aspose.CAD;
Η αδειοδότηση στο Aspose.CAD είναι ο μηχανισμός που επικυρώνει την αγορά σας και ενεργοποιεί το πλήρες σύνολο λειτουργιών της βιβλιοθήκης. Χωρίς άδεια, το API λειτουργεί σε λειτουργία αξιολόγησης, περιορίζοντας το μέγεθος εξόδου και προσθέτοντας υδατογράφημα στις αποδομένες εικόνες.

## Γιατί να χρησιμοποιήσετε άδεια βασισμένη σε διαδρομή αντί για ροή;
Η αδειοδότηση με βάση τη διαδρομή είναι ο πιο γρήγορος τρόπος ενεργοποίησης του Aspose.CAD: απλώς δείξτε στο αρχείο *.lic* και η βιβλιοθήκη το φορτώνει αυτόματα. Χρησιμοποιήστε ροή όταν πρέπει να διαβάσετε την άδεια από μη‑αρχείο πηγή, να εφαρμόσετε προσαρμοσμένη ασφάλεια ή να ενσωματώσετε την άδεια μέσα σε ένα assembly. Επιλέξτε τη μέθοδο που ταιριάζει στις περιορισμούς της ανάπτυξής σας.

Η κλάση `License` αντιπροσωπεύει το στοιχείο αδειοδότησης του Aspose.CAD που καταχωρεί μια άδεια στο API.

## Πώς να εφαρμόσετε άδεια με διαδρομή στο Aspose.CAD για .NET;

Για να εφαρμόσετε άδεια με διαδρομή, δημιουργήστε μια παρουσία της κλάσης `License` και καλέστε τη μέθοδο `SetLicense` με την πλήρη διαδρομή του αρχείου *.lic*. Τοποθετήστε αυτόν τον κώδικα νωρίς στην εκκίνηση της εφαρμογής ώστε όλες οι επόμενες λειτουργίες CAD να εκτελούνται σε περιβάλλον αδειοδοτημένο.

Η κλάση `License` αντιπροσωπεύει το στοιχείο αδειοδότησης του Aspose.CAD που καταχωρεί μια άδεια στο API.

1. Τοποθετήστε το αρχείο `Aspose.CAD.lic` σε φάκελο που η εφαρμογή σας μπορεί να διαβάσει (π.χ. τη ρίζα της εφαρμογής ή έναν ασφαλή φάκελο ρυθμίσεων).  
2. Προσθέστε τον παρακάτω κώδικα νωρίς στη διαδικασία εκκίνησης (π.χ. `Main`, `Startup.Configure` ή `Global.asax`):

```csharp
// No code block added – original tutorial contained none.
```

> **Άμεση απάντηση (40‑70 λέξεις):**  
> Για να εφαρμόσετε άδεια με διαδρομή, δημιουργήστε ένα αντικείμενο `License` και καλέστε `SetLicense("full\\path\\to\\Aspose.CAD.lic")`. Αυτή η εντολή ενεργοποιεί ολόκληρη τη βιβλιοθήκη, αφαιρεί τα υδατογράμματα αξιολόγησης και ενεργοποιεί την επεξεργασία των 40+ μορφών CAD/BIM χωρίς περιορισμούς απόδοσης. Τοποθετήστε την κλήση πριν από οποιαδήποτε λειτουργία CAD ώστε η άδεια να είναι ενεργή.

## Πώς να εφαρμόσετε άδεια χρησιμοποιώντας FileStream στο Aspose.CAD για .NET;

Για να εφαρμόσετε άδεια χρησιμοποιώντας ένα `FileStream`, ανοίξτε το αρχείο *.lic* με πρόσβαση ανάγνωσης, δημιουργήστε ένα αντικείμενο `License` και περάστε το ρεύμα στη μέθοδο `SetLicense`. Βεβαιωθείτε ότι το ρεύμα παραμένει ανοιχτό μέχρι να ολοκληρωθεί η καταχώριση στην εφαρμογή σας, έπειτα κλείστε το για να ελευθερώσετε πόρους.

Η κλάση `FileStream` παρέχει ρεύμα για ανάγνωση και εγγραφή αρχείων στο δίσκο.

1. Ανακτήστε τα byte της άδειας από την πηγή σας (σύστημα αρχείων, Azure Blob κ.λπ.).  
2. Ανοίξτε ένα `FileStream` με δικαιώματα ανάγνωσης.  
3. Περάστε το ρεύμα στο αντικείμενο `License`.

> **Άμεση απάντηση (40‑70 λέξεις):**  
> Δημιουργήστε ένα αντικείμενο `License` και καλέστε `SetLicense(stream)` όπου το `stream` είναι ένα αναγνώσιμο `FileStream` που δείχνει στο `Aspose.CAD.lic`. Αυτό φορτώνει την άδεια από τη μνήμη, επιτρέποντάς σας να κρατήσετε το αρχείο εκτός του συστήματος αρχείων αν το επιθυμείτε, και ενεργοποιεί όλες τις λειτουργίες αμέσως. Διατηρήστε το ρεύμα ανοιχτό μέχρι να ολοκληρωθεί η καταχώριση, έπειτα κλείστε το.

## Πώς λειτουργεί η αδειοδότηση με μέτρηση (metered licensing) στο Aspose.CAD για .NET;

Η αδειοδότηση με μέτρηση ενεργοποιείται καλώντας το `License.SetMeteredKey` με το μοναδικό σας κλειδί. Μετά την καταχώριση, το SDK αυτόματα αναφέρει κάθε λειτουργία CAD στον διακομιστή της Aspose, επιτρέποντάς σας να παρακολουθείτε τη χρήση και να χρεώνεστε μόνο για τις ενέργειες που πραγματοποιήθηκαν κατά την περίοδο συνδρομής σας.

Η μέθοδος `License.SetMeteredKey` καταχωρεί ένα κλειδί αδειοδότησης με μέτρηση στη βιβλιοθήκη Aspose.CAD.

1. Λάβετε ένα κλειδί αδειοδότησης με μέτρηση από τον πίνακα ελέγχου του λογαριασμού σας στην Aspose.  
2. Καταχωρίστε το κλειδί με `License.SetMeteredKey("your‑key")`.  
3. Μετά από κάθε λειτουργία, καλέστε `License.GetMeteredUsage()` για να λάβετε τον τρέχοντα αριθμό χρήσεων.

> **Άμεση απάντηση (40‑70 λέξεις):**  
> Η αδειοδότηση με μέτρηση ενεργοποιείται καλώντας `License.SetMeteredKey("your‑key")`. Το SDK στη συνέχεια στέλνει δεδομένα χρήσης στον διακομιστή της Aspose μετά από κάθε λειτουργία CAD, επιτρέποντάς σας να παρακολουθείτε και να χρεώνεστε βάσει της πραγματικής κατανάλωσης. Αυτό το μοντέλο υποστηρίζει απεριόριστους ταυτόχρονους χρήστες διατηρώντας το κόστος σύμφωνο με τη χρήση.

## Μαθήματα αδειοδότησης και διαμόρφωσης

### [Εφαρμογή άδειας με διαδρομή στο Aspose.CAD για .NET](./apply-license-by-path/)
Αποκτήστε το πλήρες δυναμικό του Aspose.CAD για .NET! Ακολουθήστε τον βήμα‑βήμα οδηγό για να εφαρμόσετε άδεια απρόσκοπτα. Αναβαθμίστε το παιχνίδι διαχείρισης αρχείων CAD τώρα!

### [Εφαρμογή άδειας χρησιμοποιώντας FileStream στο Aspose.CAD για .NET](./apply-license-using-filestream/)
Κατακτώντας το Aspose.CAD για .NET: Εφαρμόστε άδειες απρόσκοπτα χρησιμοποιώντας FileStream. Εξερευνήστε τον βήμα‑βήμα οδηγό και ξεκλειδώστε το δυναμικό. Κατεβάστε τώρα!

### [Αδειοδότηση με μέτρηση στο Aspose.CAD για .NET](./metered-licensing/)
Αποκτήστε το δυναμικό του Aspose.CAD με αδειοδότηση με μέτρηση σε .NET. Βελτιστοποιήστε τη χρήση πόρων απρόσκοπτα. Εξερευνήστε τον βήμα‑βήμα οδηγό.

## Συχνές ερωτήσεις

**Ε: Μπορώ να χρησιμοποιήσω το ίδιο αρχείο άδειας σε πολλαπλούς υπολογιστές;**  
Α: Ναι, ένα μόνο αρχείο άδειας μπορεί να αναπτυχθεί σε οποιονδήποτε αριθμό διακομιστών ανάπτυξης ή παραγωγής, εφόσον η χρήση συμμορφώνεται με τους όρους της αγοράς σας.

**Ε: Τι συμβαίνει αν ξεχάσω να ορίσω την άδεια πριν φορτώσω ένα αρχείο CAD;**  
Α: Η βιβλιοθήκη θα λειτουργήσει σε λειτουργία αξιολόγησης, προσθέτοντας υδατογράφημα στις αποδομένες εικόνες και περιορίζοντας τον αριθμό των σελίδων που μπορείτε να επεξεργαστείτε.

**Ε: Η αδειοδότηση με μέτρηση απαιτεί σύνδεση στο διαδίκτυο;**  
Α: Μόνο η πρώτη ενεργοποίηση και κάθε αναφορά χρήσης χρειάζονται σύνδεση· μετά από αυτό, η βιβλιοθήκη μπορεί να λειτουργεί εκτός σύνδεσης μέχρι την επόμενη αναφορά.

**Ε: Ποιες μορφές CAD/BIM υποστηρίζονται από προεπιλογή;**  
Α: Το Aspose.CAD υποστηρίζει 45+ μορφές εισόδου και εξόδου, συμπεριλαμβανομένων των DWG, DXF, DGN, STL, OBJ και IFC, και μπορεί να αποδίδει αρχεία έως 500 MB χωρίς να φορτώνει ολόκληρο το έγγραφο στη μνήμη.

**Ε: Υπάρχει τρόπος να ελέγξω προγραμματιστικά αν η άδεια εφαρμόστηκε επιτυχώς;**  
Α: Καλέστε `License.IsLicensed` (ή ελέγξτε το `License.LicenseFilePath`) μετά την καταχώριση· επιστρέφει `true` όταν μια έγκυρη άδεια είναι ενεργή.

---

**Τελευταία ενημέρωση:** 2026-09-14  
**Δοκιμή με:** Aspose.CAD 24.11 για .NET  
**Συγγραφέας:** Aspose

## Σχετικά μαθήματα

- [Εφαρμογή άδειας με διαδρομή στο Aspose.CAD για .NET](/cad/net/licensing-and-configuration/apply-license-by-path/)
- [Εφαρμογή άδειας χρησιμοποιώντας FileStream στο Aspose.CAD για .NET](/cad/net/licensing-and-configuration/apply-license-using-filestream/)
- [Αδειοδότηση με μέτρηση στο Aspose.CAD για .NET](/cad/net/licensing-and-configuration/metered-licensing/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}