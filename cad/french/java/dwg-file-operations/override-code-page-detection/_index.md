---
date: 2026-05-20
description: Apprenez comment convertir DWG en PDF tout en contournant la détection
  automatique de la page de code à l'aide d'Aspose.CAD for Java. Comprend les étapes
  d'exportation de DWG vers PDF, des conseils d'encodage et le dépannage.
keywords:
- convert dwg pdf
- export dwg to pdf
- Aspose.CAD Java
linktitle: Contourner la détection automatique de la page de code dans les fichiers
  DWG
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  headline: Convert DWG to PDF – Override Code Page Detection in Java
  type: TechArticle
- description: Learn how to convert DWG to PDF while overriding automatic code page
    detection using Aspose.CAD for Java. Includes export dwg to pdf steps, encoding
    tips, and troubleshooting.
  name: Convert DWG to PDF – Override Code Page Detection in Java
  steps:
  - name: Set Up the Java Project
    text: Create a Maven or Gradle project and add the Aspose.CAD JAR to the classpath.
      This ensures the IDE can resolve the imported classes and that the runtime can
      locate the library.
  - name: Load the DWG File with a Specified Code Page
    text: Tell Aspose.CAD which encoding to use and whether to attempt recovery of
      malformed CIF/MIF data.
  - name: Export the CAD Image to PDF
    text: With the correct code page applied, you can safely export the drawing. The
      `PdfOptions` object lets you fine‑tune the PDF output (compression, rasterization,
      etc.).
  - name: Verify Success
    text: A simple console message confirms that the process completed without exceptions.
      You can repeat these steps for multiple DWG files, adjusting the source path
      and output name as needed.
  type: HowTo
- questions:
  - answer: It forces Aspose.CAD to use a specific character encoding instead of guessing.
    question: What does “override code page” mean?
  - answer: Yes – after setting the correct code page, you can save the CAD image
      as PDF.
    question: Can I export DWG directly to PDF?
  - answer: '`CodePages.Japanese` and `MifCodePages.Japanese` are the right choices.'
    question: Which encoding works for Japanese text?
  - answer: A commercial license is required; a temporary license is available for
      testing.
    question: Do I need a license for production use?
  - answer: Any recent version that supports `LoadOptions` and `PdfOptions`.
    question: What version of Aspose.CAD is needed?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Convertir DWG en PDF – Contourner la détection de la page de code en Java
url: /fr/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PDF – Remplacer la détection de la page de code en Java

Dans ce tutoriel complet, vous apprendrez **comment convertir DWG en PDF** tout en contournant la détection automatique de la page de code qui peut corrompre le texte. Aspose.CAD for Java vous offre un contrôle précis sur l’encodage des caractères, vous permettant de récupérer des données CIF/MIF malformées et de générer une sortie PDF fiable. Que vous construisiez un convertisseur par lots ou que vous ajoutiez le traitement CAD à un service Java plus vaste, les étapes ci‑dessous vous guident à travers l’ensemble du flux de travail — de la configuration du projet à la vérification.

## Réponses rapides
- **Que signifie « override code page » ?** Cela force Aspose.CAD à utiliser un encodage de caractères spécifique au lieu de deviner.  
- **Puis-je exporter DWG directement en PDF ?** Oui – après avoir défini la bonne page de code, vous pouvez enregistrer l’image CAD au format PDF.  
- **Quel encodage fonctionne pour le texte japonais ?** `CodePages.Japanese` et `MifCodePages.Japanese` sont les bons choix.  
- **Ai-je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise ; une licence temporaire est disponible pour les tests.  
- **Quelle version d’Aspose.CAD est nécessaire ?** Toute version récente qui prend en charge `LoadOptions` et `PdfOptions`.

## Qu’est‑ce que « exporter CAD en PDF » ?
Exporter CAD en PDF transforme un dessin DWG basé sur des vecteurs en un document PDF à mise en page fixe, visualisable universellement. La conversion conserve toutes les entités géométriques, les tracés, les calques et le texte intégré, tout en aplatissant le dessin dans un format facilement partageable, imprimable, archivable ou intégrable dans d’autres applications sans nécessiter de logiciel CAD.

## Pourquoi remplacer la détection automatique de la page de code ?
Spécifier manuellement la page de code garantit que les octets de texte sont interprétés correctement, éliminant les caractères illisibles qui apparaissent souvent lorsque l’auto‑détection d’Aspose.CAD devine un encodage hérité erroné. Cela est essentiel pour les scripts non latins tels que le japonais, le cyrillique ou l’arabe, et assure que le PDF exporté correspond au design original.

## Prérequis
- **Environnement de développement Java** – JDK 8+ et votre IDE préféré.  
- **Aspose.CAD for Java** – Téléchargez la bibliothèque depuis le site officiel [here](https://releases.aspose.com/cad/java/).  
- **Fichier d’exemple DWG** – Utilisez le `SimpleEntities.dwg` fourni ou tout autre DWG que vous devez convertir.

## Importer les packages
Les classes `Document`, `LoadOptions` et `PdfOptions` sont le cœur du processus de conversion.

La classe `Document` représente un dessin CAD en mémoire, offrant des méthodes pour charger, manipuler et enregistrer le fichier dans divers formats.  
La classe `LoadOptions` vous permet de spécifier la page de code et les options de récupération lors du chargement d’un fichier DWG.  
La classe `PdfOptions` contrôle les paramètres spécifiques au PDF tels que la compression, la rasterisation et les métadonnées.

Dans votre projet Java, importez les classes Aspose.CAD nécessaires :

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Comment convertir DWG en PDF avec le remplacement de la page de code ?
Chargez le fichier DWG à l’aide de `LoadOptions` pour spécifier la page de code exacte, puis invoquez la méthode `save` sur le `CadImage` résultant avec une instance `PdfOptions` configurée. Cette approche en deux étapes garantit que le texte est interprété correctement et que le PDF généré préserve la fidélité, les calques et la qualité vectorielle du dessin original.

### Étape 1 : Configurer le projet Java
Créez un projet Maven ou Gradle et ajoutez le JAR Aspose.CAD au classpath. Cela permet à l’IDE de résoudre les classes importées et au runtime de localiser la bibliothèque.

### Étape 2 : Charger le fichier DWG avec une page de code spécifiée
Indiquez à Aspose.CAD quel encodage utiliser et s’il faut tenter la récupération des données CIF/MIF malformées.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Étape 3 : Exporter l’image CAD en PDF
Avec la bonne page de code appliquée, vous pouvez exporter le dessin en toute sécurité. L’objet `PdfOptions` vous permet d’ajuster finement la sortie PDF (compression, rasterisation, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Étape 4 : Vérifier le succès
Un simple message console confirme que le processus s’est terminé sans exception.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Vous pouvez répéter ces étapes pour plusieurs fichiers DWG, en ajustant le chemin source et le nom de sortie selon les besoins.

## Problèmes courants et solutions
- **Les caractères indésirables apparaissent toujours :** Vérifiez que le `specifiedEncoding` correspond à la page de code du DWG original. Utilisez un autre enum `CodePages` si nécessaire.  
- **`NullPointerException` sur `cadImage.save` :** Assurez‑vous que le fichier DWG se charge correctement ; vérifiez le chemin et les permissions du fichier.  
- **La taille du PDF est importante :** Activez la compression dans `PdfOptions` (par ex., `pdfOptions.setCompress(true)`) pour réduire la taille du fichier sans perdre de qualité.

## Questions fréquemment posées

**Q1 : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?**  
R1 : Aspose.CAD prend en charge plus de 30 versions DWG, y compris AutoCAD 2018 et les versions antérieures.

**Q2 : Puis‑je utiliser Aspose.CAD pour des projets commerciaux ?**  
R2 : Oui, une licence commerciale est requise pour une utilisation en production. Vous pouvez obtenir une licence [here](https://purchase.aspose.com/buy).

**Q3 : Existe‑t‑il des limitations dans la version d’essai gratuite ?**  
R1 : L’essai impose des restrictions de taille et de fonctionnalités ; consultez la documentation officielle pour plus de détails.

**Q4 : Comment obtenir du support pour Aspose.CAD ?**  
R4 : Visitez la communauté [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

**Q5 : Une licence temporaire est‑elle disponible à des fins de test ?**  
R5 : Oui, une licence temporaire peut être demandée [here](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour** : 2026-05-20  
**Testé avec** : Aspose.CAD for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur** : Aspose

## Tutoriels associés

- [Exporter DWG en PDF et convertir les dessins CAD – Tutoriel Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Exporter une mise en page DWG spécifique en PDF avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Exporter DWG en PDF ou raster avec Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}

{{< blocks/products/products-backtop-button >}}

{{< /blocks/products/pf/main-wrap-class >}}