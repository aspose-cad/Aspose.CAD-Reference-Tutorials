---
date: 2026-01-12
description: Apprenez à exporter des fichiers CAD en PDF tout en surchargeant la détection
  automatique de la page de code dans les fichiers DWG à l’aide d’Aspose.CAD pour
  Java. Gère l’encodage et les CIF/MIF malformés.
linktitle: Override Automatic Code Page Detection in DWG Files
second_title: Aspose.CAD Java API
title: Exporter le CAD en PDF – Contourner la détection automatique de la page de
  code dans les fichiers DWG avec Java
url: /fr/java/dwg-file-operations/override-code-page-detection/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en PDF – Remplacer la détection automatique de la page de code dans les fichiers DWG avec Java

## Introduction

Dans ce guide complet, vous découvrirez **comment exporter CAD en PDF** tout en contournant la détection automatique de la page de code qui peut corrompre le texte dans les fichiers DWG. Aspose.CAD for Java vous offre un contrôle fin sur l’encodage, vous permettant de récupérer des données CIF/MIF malformées et de produire une sortie PDF fiable. Que vous construisiez un convertisseur par lots ou intégriez le traitement CAD dans une application Java plus vaste, les étapes ci-dessous vous guideront à travers l’ensemble du flux de travail.

## Réponses rapides
- **Que signifie «override code page»?** Cela force Aspose.CAD à utiliser un encodage de caractères spécifique au lieu de deviner.
- **Puis‑je exporter un DWG directement en PDF?** Oui – après avoir défini la bonne page de code, vous pouvez enregistrer l'image CAD au format PDF.
- **Quel encodage fonctionne pour le texte japonais ?** `CodePages.Japanese` et `MifCodePages.Japanese` sont les bons choix.
- **Ai‑je besoin d’une licence pour une utilisation en production?** Une licence commerciale est requise; une licence temporaire est disponible pour les tests.
- **Quelle version d'Aspose.CAD est nécessaire ?** Toute version récente qui prend en charge `LoadOptions` et `PdfOptions`.

## Qu'est-ce que « exporter la CAO au format PDF » ?
Exporter CAD en PDF convertit les dessins CAD vectoriels en un format de document à mise en page fixe largement pris en charge. Le PDF résultant préserve les tracés, les calques et le texte tout en facilitant le partage, l’impression ou l’intégration du dessin dans d’autres applications.

## Pourquoi remplacer la détection automatique des pages de codes ?
Les fichiers DWG stockent souvent le texte à l’aide de pages de code héritées. L’auto‑détection d’Aspose.CAD peut mal interpréter ces octets, entraînant des caractères illisibles. En spécifiant manuellement la page de code, vous vous assurez que le texte apparaît exactement comme prévu dans le PDF exporté, notamment pour les scripts non latins tels que le japonais, le cyrillique ou l'arabe.

## Prérequis
- **Environnement de développement Java** – JDK 8+ et votre IDE préféré.
- **Aspose.CAD for Java** – Téléchargez la bibliothèque depuis le site officiel[ici](https://releases.aspose.com/cad/java/).
- **Fichier d’exemple DWG** – Utilisez le `SimpleEntities.dwg` fourni ou tout autre DWG que vous devez convertir.

## Importer des packages
Dans votre projet Java, importez les classes Aspose.CAD nécessaires :

```java
import com.aspose.cad.CodePages;
import com.aspose.cad.Image;
import com.aspose.cad.LoadOptions;
import com.aspose.cad.MifCodePages;
import com.aspose.cad.fileformats.cad.CadImage;
```

## Guide étape par étape

### Étape 1 : Configurer le projet Java
Créez un nouveau projet Maven ou Gradle et ajoutez le JAR Aspose.CAD au classpath. Cette étape garantit que l’IDE ​​peut résoudre les classes importées.

### Étape 2 : Charger le fichier DWG avec une page de codes spécifiée
Indiquez à Aspose.CAD quel encodage utiliser et si vous devez tenter la récupération de données CIF/MIF malformées.

```java
String SourceDir = "Your Document Directory";
String dwgPathToFile = SourceDir + "SimpleEntites.dwg";
LoadOptions opts = new LoadOptions();
opts.setSpecifiedEncoding(CodePages.Japanese);
opts.setSpecifiedMifEncoding(MifCodePages.Japanese);
opts.setRecoverMalformedCifMif(false);
CadImage cadImage = (CadImage) Image.load(dwgPathToFile, opts);
```

### Étape 3 : Exporter l'image CAO au format PDF
Avec la bonne page de code appliqué, vous pouvez exporter le dessin en toute sécurité. L’objet `PdfOptions` vous permet d’ajuster finement la sortie PDF (compression, rastérisation, etc.).

```java
// Perform export or other operations with cadImage
// For example, exporting to PDF
PdfOptions pdfOptions = new PdfOptions();
cadImage.save("output.pdf", pdfOptions);
```

### Étape 4 : Vérifier le succès
Un simple message console confirme que le processus s’est terminé sans exception.

```java
System.out.println("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

Vous pouvez répéter ces étapes pour plusieurs fichiers DWG, en ajustant le chemin source et le nom de sortie selon vos besoins.

## Problèmes courants et solutions
- **Des caractères indésirables apparaissent toujours :** Vérifiez que le `specifiedEncoding` correspond à la page de code originale du DWG. Utilisez une autre énumération `CodePages` si nécessaire.
- **`NullPointerException` sur `cadImage.save`:** Assurez-vous que le fichier DWG se charge correctement ; Vérifiez le chemin et les autorisations du fichier.
- **La taille du PDF est grande :** Activez la compression dans `PdfOptions` (par exemple, `pdfOptions.setCompress(true)`).

## Questions fréquemment posées

**Q1 : Aspose.CAD est-il compatible avec toutes les versions de fichiers DWG ?**
R1 : Aspose.CAD prend en charge un large éventail de versions DWG, y compris AutoCAD 2018 et les versions antérieures.

**Q2 : Puis‑je utiliser Aspose.CAD pour des projets commerciaux ?**
R2 : Oui, une licence commerciale est requise pour une utilisation en production. Vous pouvez obtenir une licence[ici](https://purchase.aspose.com/buy).

**Q3 : Y a‑t‑il des limitations dans la version d’essai gratuite ?**
R3 : L’essai impose des restrictions de taille et de fonctionnalités ; consultez la documentation officielle pour plus de détails.

**Q4 : Comment obtenir du support pour Aspose.CAD ?**
R4 : Visitez la communauté[Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et participer aux discussions.

**Q5 : Une licence temporaire est‑elle disponible à des fins de test?**
R5 : Oui, une licence temporaire peut être demandée[ici](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 12/01/2026

**Testé avec :** Aspose.CAD pour Java 24.11 (dernière version disponible au moment de la rédaction)

**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}