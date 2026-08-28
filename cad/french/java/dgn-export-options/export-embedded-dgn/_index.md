---
date: 2026-06-14
description: Apprenez à exporter le CAD en PDF et à convertir le DGN en PDF à l'aide
  d'Aspose.CAD for Java. Guide étape par étape pour les développeurs Java.
keywords:
- export cad to pdf
- convert dwg to pdf
- convert dgn to pdf
- java convert cad pdf
- batch convert dgn pdf
linktitle: Exporter le DGN intégré
schemas:
- author: Aspose
  dateModified: '2026-06-14'
  description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  headline: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  type: TechArticle
- description: Learn how to export CAD to PDF and convert DGN to PDF using Aspose.CAD
    for Java. Step‑by‑step guide for Java developers.
  name: Export CAD to PDF – Export Embedded DGN with Aspose.CAD for Java
  steps:
  - name: Set Up Input and Output Paths
    text: Define the directory that contains your source file and specify the DWG
      that holds the embedded DGN.
  - name: Load DWG File
    text: '`Image` loads the DWG and automatically detects any embedded DGN data,
      exposing it for further processing.'
  - name: Configure Rasterization Options
    text: Select which layout(s) you want to include in the PDF. In this example we
      export only the **Model** layout, which is the most common view for engineering
      drawings.
  - name: Configure PDF Options
    text: Attach the rasterization settings to the PDF export options so that the
      final document respects the chosen layout and DPI.
  - name: Save PDF File
    text: Finally, write the PDF to disk using the configured options. The `save`
      method writes the configured image to the target file format on disk.
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java is a commercial library. You can obtain a license
      from [here](https://purchase.aspose.com/buy).
    question: Can I use Aspose.CAD for Java in a commercial project?
  - answer: Yes, you can access a free trial of Aspose.CAD for Java [here](https://releases.aspose.com/).
    question: Is there a free trial available?
  - answer: You can seek support from the Aspose.CAD community on the [forum](https://forum.aspose.com/c/cad/19).
    question: How can I get support for Aspose.CAD for Java?
  - answer: You can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).
    question: What if I need a temporary license?
  - answer: The documentation is available [here](https://reference.aspose.com/cad/java/).
    question: Where can I find the official documentation?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exporter le CAD en PDF – Exporter le DGN intégré avec Aspose.CAD for Java
url: /fr/java/dgn-export-options/export-embedded-dgn/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter CAD en PDF – Exporter DGN intégré avec Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous découvrirez **comment exporter CAD en PDF** en convertissant un fichier DGN intégré en un document PDF de haute qualité avec Aspose.CAD pour Java. Aspose.CAD est une bibliothèque robuste qui offre aux développeurs Java un contrôle complet sur la manipulation des fichiers CAD, que vous ayez besoin de **convertir DGN en PDF**, **convertir DWG en PDF**, ou simplement de rendre les dessins CAD dans d’autres formats. Suivez le guide étape par étape ci‑dessous, et vous pourrez intégrer cette fonctionnalité dans vos applications en quelques minutes.

## Réponses rapides

- **Que signifie « export CAD to PDF » ?** Il convertit les dessins CAD (DWG, DGN, etc.) en fichiers PDF tout en préservant la qualité vectorielle.  
- **Quelle bibliothèque est utilisée ?** Aspose.CAD for Java.  
- **Ai-je besoin d’une licence ?** Une licence est requise pour la production ; un essai gratuit est disponible.  
- **Quelles sont les principales conditions préalables ?** Environnement de développement Java et le JAR Aspose.CAD pour Java.  
- **Puis-je personnaliser la sortie ?** Oui – vous pouvez sélectionner les mises en page, définir les options de rasterisation et contrôler les paramètres PDF.  

## Qu’est‑ce que « export CAD to PDF » ?

Exporter CAD en PDF convertit un dessin CAD natif (DWG, DGN, etc.) en un fichier PDF qui conserve la géométrie vectorielle originale, les calques et la mise en page, permettant à quiconque de visualiser, imprimer ou partager le design sans logiciel CAD. Cette transformation produit un document indépendant de la plateforme qui apparaît identique à n’importe quel niveau de zoom, ce qui le rend idéal pour la collaboration et l’archivage.

## Pourquoi utiliser Aspose.CAD pour Java pour convertir DGN en PDF ?

Aspose.CAD pour Java fournit une solution pure Java qui élimine le besoin d’outils CAD externes, garantit une fidélité vectorielle exacte dans les PDF résultants, et offre de nombreuses options de configuration telles que la sélection de la mise en page, le contrôle du DPI et l’intégration des polices, ce qui le rend idéal tant pour les conversions simples que pour les tâches à l’échelle de l’entreprise.

- **Aucune dépendance externe** – fonctionne purement en Java sur n’importe quel OS.  
- **Préserve les données vectorielles** – les PDF restent nets à n’importe quel niveau de zoom.  
- **Contrôle fin** – choisissez des mises en page spécifiques, définissez le DPI de rasterisation et intégrez les polices.  
- **Prêt pour l’entreprise** – prend en charge les fichiers jusqu’à **2 GB**, le traitement par lots de milliers de dessins, et une licence flexible.  

## Prérequis

Avant de commencer, assurez-vous de disposer de ce qui suit :

- **Environnement de développement Java** – JDK 8 ou supérieur installé et configuré.  
- **Aspose.CAD pour Java** – téléchargez le dernier JAR depuis [ici](https://releases.aspose.com/cad/java/).  

## Importer les packages

Les instructions `import` importent les classes Aspose.CAD requises dans le scope.  
`Image` est la classe principale qui représente tout fichier CAD rasterisable, tandis que `PdfOptions` et `RasterizationOptions` vous permettent d’ajuster finement la sortie PDF.  
`CadRasterizationOptions` spécifie les paramètres de rasterisation tels que le DPI, la taille de page et la mise en page pour le rendu CAD.

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Comment exporter CAD en PDF avec Aspose.CAD pour Java ?

Le processus commence par charger le fichier DWG contenant le DGN intégré, puis en configurant les paramètres de rasterisation pour définir la résolution et la mise en page de sortie, en attachant ces paramètres à un objet PdfOptions, et enfin en invoquant la méthode save pour générer le PDF. Cette approche garantit des résultats de haute qualité, préservant les vecteurs, avec un code minimal.

Ci‑dessous se trouve un guide clair, numéroté, qui montre exactement comment convertir un fichier DGN intégré (stocké à l’intérieur d’un DWG) en PDF.

### Étape 1 : Configurer les chemins d’entrée et de sortie

Définissez le répertoire contenant votre fichier source et spécifiez le DWG qui contient le DGN intégré.

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "BlockRefDgn.dwg";
```

### Étape 2 : Charger le fichier DWG

`Image` charge le DWG et détecte automatiquement toute donnée DGN intégrée, la rendant disponible pour un traitement ultérieur.

```java
Image objImage = Image.load(fileName);
```

### Étape 3 : Configurer les options de rasterisation

Sélectionnez la ou les mises en page que vous souhaitez inclure dans le PDF. Dans cet exemple, nous exportons uniquement la mise en page **Model**, qui est la vue la plus courante pour les dessins d’ingénierie.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setLayouts(new String[] {"Model"});
```

### Étape 4 : Configurer les options PDF

Attachez les paramètres de rasterisation aux options d’exportation PDF afin que le document final respecte la mise en page et le DPI choisis.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : Enregistrer le fichier PDF

Enfin, écrivez le PDF sur le disque en utilisant les options configurées. La méthode `save` écrit l’image configurée dans le format de fichier cible sur le disque.

```java
objImage.save(dataDir + "BlockRefDgn.pdf", pdfOptions);
```

## Convertir DWG en PDF – une astuce supplémentaire

Si votre fichier source est un DWG simple (sans DGN intégré), vous pouvez réutiliser le même code – il suffit de changer le `fileName` pour pointer vers le DWG que vous souhaitez convertir. Les options de rasterisation et PDF restent identiques, vous offrant un flux de travail cohérent de **convert DWG to PDF**.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| **Sortie PDF vide** | Nom de mise en page incorrect | Vérifiez que le nom de mise en page passé à `setLayouts` correspond exactement à la mise en page du fichier source (sensible à la casse). |
| **Exception de licence** | Utilisation de la version d’essai sans licence | Appliquez une licence Aspose.CAD valide avant de charger l’image (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |
| **Fichier non trouvé** | Chemin `dataDir` incorrect | Utilisez un chemin absolu ou assurez‑vous que le chemin relatif est correct par rapport au répertoire de travail du projet. |
| **Graphiques basse résolution** | Le DPI de rasterisation par défaut est faible | Définissez `rasterizationOptions.setResolution(300)` ou ajustez `setPageWidth/Height` pour augmenter le DPI. |

## Questions fréquentes

**Q : Puis-je utiliser Aspose.CAD pour Java dans un projet commercial ?**  
R : Oui, Aspose.CAD pour Java est une bibliothèque commerciale. Vous pouvez obtenir une licence depuis [ici](https://purchase.aspose.com/buy).

**Q : Une version d’essai gratuite est‑elle disponible ?**  
R : Oui, vous pouvez accéder à une version d’essai gratuite d’Aspose.CAD pour Java [ici](https://releases.aspose.com/).

**Q : Comment obtenir du support pour Aspose.CAD pour Java ?**  
R : Vous pouvez demander du support à la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19).

**Q : Et si j’ai besoin d’une licence temporaire ?**  
R : Vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver la documentation officielle ?**  
R : La documentation est disponible [ici](https://reference.aspose.com/cad/java/).

## Conclusion

Vous avez maintenant appris comment **exporter CAD en PDF**, spécifiquement comment **convertir DGN en PDF** et même **convertir DWG en PDF** en utilisant Aspose.CAD pour Java. En suivant les étapes ci‑dessus, vous pouvez intégrer une conversion CAD‑vers‑PDF fluide dans toute solution basée sur Java, offrant des PDF de haute qualité à vos utilisateurs sans besoin de logiciel CAD supplémentaire.

---

**Dernière mise à jour** : 2026-06-14  
**Testé avec** : Aspose.CAD for Java 24.12  
**Auteur** : Aspose

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter DGN vers DWG avec Aspose.CAD pour Java – Tutoriel](/cad/java/dgn-export-options/)
- [Exportation sans effort de DGN vers PDF AutoCAD avec Aspose.CAD pour Java](/cad/java/dgn-export-options/exporting-dgn-to-pdf/)
- [dwg vers pdf java – Exporter CAD en PDF avec Aspose.CAD](/cad/java/cad-export-options/export-to-pdf/)

{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}