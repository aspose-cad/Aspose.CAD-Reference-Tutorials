---
date: 2025-12-21
description: Apprenez à convertir DWG en PDF en exportant une mise en page DWG spécifique
  au format PDF à l'aide d'Aspose.CAD pour Java. Suivez ce tutoriel pas à pas de conversion
  DWG en PDF pour optimiser votre flux de travail CAD.
linktitle: Export Specific DWG Layout to PDF
second_title: Aspose.CAD Java API
title: Convertir DWG en PDF – Exporter la mise en page avec Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PDF – Exporter une mise en page spécifique avec Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la Conception Assistée par Ordinateur (CAO), **convertir DWG en PDF** est une exigence fréquente lors du partage de dessins avec des clients, des entrepreneurs ou des parties prenantes non techniques. Aspose.CAD pour Java rend cette conversion simple, et il vous permet même de choisir une seule mise en page d’un fichier DWG contenant plusieurs mises en page. Dans ce tutoriel, nous allons parcourir **comment exporter des mises en page DWG spécifiques vers PDF**, afin que vous puissiez livrer exactement ce dont votre projet a besoin sans pages superflues ni recadrage manuel.

## Réponses rapides
- **Que signifie « convertir DWG en PDF » ?** Cela transforme un dessin DWG en document PDF, en conservant les données vectorielles et la fidélité de la mise en page.  
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD pour Java fournit une API prête à l’emploi.  
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale est requise ; un essai gratuit fonctionne pour l’évaluation.  
- **Puis‑je choisir une seule mise en page ?** Absolument – définissez la propriété `Layouts` sur le nom de la mise en page souhaitée.  
- **Quelle version de Java est prise en charge ?** Java 8 et versions ultérieures sont entièrement compatibles.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8+ et votre IDE préféré.  
- **Bibliothèque Aspose.CAD** – Téléchargez le JAR le plus récent depuis le site officiel **[ici](https://releases.aspose.com/cad/java/)**.  
- **Fichier DWG** – Un dessin contenant au moins une mise en page (par ex. *visualization_-_conference_room.dwg*).  

## Pourquoi exporter une mise en page DWG spécifique vers PDF ?

De nombreux fichiers DWG contiennent plusieurs espaces papier (mises en page). Exporter le fichier entier peut produire un PDF volumineux avec des pages indésirables. Sélectionner une seule mise en page :

- Réduit la taille du fichier.  
- Concentre l’attention du lecteur sur la feuille de dessin pertinente.  
- S’aligne avec les normes de documentation du projet.  

## Guide étape par étape

### Étape 1 : Configurer l’environnement du projet

Créez un nouveau projet Java (Maven, Gradle ou IDE simple) et ajoutez le JAR Aspose.CAD à votre classpath. Vous pouvez le télécharger **[ici](https://releases.aspose.com/cad/java/)**.

### Étape 2 : Importer les packages nécessaires

Ajoutez les espaces de noms Aspose.CAD requis à votre classe Java.

```java
import com.aspose.cad.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

### Étape 3 : Charger le fichier DWG

Indiquez le chemin du DWG que vous souhaitez convertir et chargez‑le dans un objet `Image`.

```java
String srcFile = dataDir + "visualization_-_conference_room.dwg";
Image image = Image.load(srcFile);
```

### Étape 4 : Configurer les options de rasterisation

Définissez la taille de la page et, surtout, la mise en page que vous voulez exporter.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
// Specify desired layout name
rasterizationOptions.setLayouts(new String[] {"Layout1"});
```

### Étape 5 : Définir les options d’exportation PDF

Liez les paramètres de rasterisation à l’exportateur PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 6 : Exporter le DWG en PDF

Enregistrez le résultat sous forme de fichier PDF. La sortie contiendra uniquement **Layout1**, réalisant ainsi une opération propre de **conversion DWG en PDF**.

```java
image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Mise en page introuvable** | Le nom de la mise en page est mal orthographié ou n’existe pas dans le DWG. | Utilisez `image.getLayoutNames()` pour lister les mises en page disponibles, puis choisissez la bonne. |
| **PDF à basse résolution** | `PageWidth`/`PageHeight` sont trop petites. | Augmentez les dimensions (par ex. 2000 × 2000) ou définissez `rasterizationOptions.setResolution(300);`. |
| **Exception de licence** | Exécution sans licence valide dans un environnement non‑essai. | Appliquez votre licence Aspose.CAD avant de charger l’image : `License license = new License(); license.setLicense("Aspose.CAD.lic");`. |

## Questions fréquemment posées

**Q1 : Puis‑je utiliser Aspose.CAD pour Java avec d’autres bibliothèques CAD basées sur Java ?**  
R : Aspose.CAD pour Java est une bibliothèque autonome mais peut être intégrée à d’autres bibliothèques Java pour des fonctionnalités étendues.

**Q2 : Existe‑t‑il des options de licence pour Aspose.CAD ?**  
R : Oui, vous pouvez explorer les options de licence et les détails d’achat **[ici](https://purchase.aspose.com/buy)**.

**Q3 : Comment obtenir une licence temporaire pour Aspose.CAD ?**  
R : Visitez **[ce lien](https://purchase.aspose.com/temporary-license/)** pour demander une licence temporaire.

**Q4 : Où puis‑je trouver du support pour Aspose.CAD ?**  
R : Pour toute question ou assistance, rendez‑vous sur le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**Q5 : Une version d’essai gratuite est‑elle disponible pour Aspose.CAD ?**  
R : Oui, vous pouvez accéder à un essai gratuit **[ici](https://releases.aspose.com/)**.

## Conclusion

En suivant ce **tutoriel dwg to pdf**, vous disposez désormais d’une méthode fiable pour **convertir DWG en PDF** tout en ciblant une seule mise en page. Cette approche économise de l’espace de stockage, accélère le partage de documents et maintient votre flux de travail CAO organisé. N’hésitez pas à expérimenter avec différents paramètres de rasterisation ou à combiner plusieurs mises en page dans un seul PDF au fur et à mesure que votre projet évolue.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2025-12-21  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose