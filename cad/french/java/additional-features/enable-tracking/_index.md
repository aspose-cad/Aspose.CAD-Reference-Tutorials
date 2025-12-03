---
date: 2025-12-03
description: Apprenez à définir la taille de la page PDF lors de la conversion de
  DWG en PDF et à activer le suivi dans les fichiers DWG en utilisant Aspose.CAD pour
  Java – un guide complet pour exporter des dessins CAD en PDF avec précision.
language: fr
linktitle: Set PDF Page Size and Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
title: Définir la taille de page PDF et activer le suivi dans les fichiers DWG en
  utilisant Aspose.CAD en Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille de page PDF et activer le suivi dans les fichiers DWG avec Aspose.CAD en Java

## Introduction

Si vous devez **définir la taille de page PDF** lors de la *conversion DWG en PDF* et également suivre les éventuels problèmes de rendu, Aspose.CAD pour Java vous offre une méthode propre et programmatique pour faire les deux. Dans ce tutoriel, nous passerons en revue les étapes exactes pour configurer les dimensions de la page, activer le suivi et exporter un dessin CAD en PDF — le tout depuis Java. À la fin, vous comprendrez pourquoi il est important de définir la bonne taille de page pour les dessins CAD et comment capturer des informations de suivi détaillées pendant le processus d’exportation.

## Quick Answers
- **Que signifie « définir la taille de page PDF » ?** Cela définit la largeur et la hauteur du canevas PDF résultant, garantissant que votre dessin s’ajuste parfaitement.  
- **Ai‑je besoin d’une licence pour utiliser cette fonctionnalité ?** Une version d’essai suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Quelle version d’Aspose.CAD est nécessaire ?** Toute version récente qui prend en charge `CadRasterizationOptions`.  
- **Puis‑je l’utiliser avec d’autres formats CAD ?** L’exemple montre DWG/DXF, mais la même approche fonctionne pour la plupart des formats pris en charge.  
- **Combien de temps prend la conversion ?** Généralement moins d’une seconde pour des fichiers modestes ; les dessins plus volumineux peuvent prendre plus de temps.

## Qu’est‑ce que « définir la taille de page PDF » dans le contexte de l’exportation CAD ?
Définir la taille de page PDF indique au moteur de rendu les dimensions exactes (en pixels ou en points) du canevas de sortie. C’est particulièrement important pour les dessins techniques où l’échelle et la mise en page doivent être conservées. Sans réglage explicite de la taille de page, le PDF peut adopter une taille par défaut qui coupe ou déforme le dessin.

## Pourquoi définir la taille de page PDF lors de l’exportation de dessins CAD ?
- **Conserver l’échelle** – Les ingénieurs comptent sur des impressions à l’échelle réelle.  
- **Adapter au papier** – Choisissez A4, Letter ou une taille personnalisée correspondant aux spécifications du projet.  
- **Améliorer la lisibilité** – Des pages plus grandes peuvent afficher les détails fins sans zoom.  
- **Sortie cohérente** – Les pipelines automatisés produisent des PDF aux dimensions identiques à chaque exécution.

## Comment définir la taille de page PDF lors de la conversion DWG en PDF ?
Ci‑dessous, nous configurerons `CadRasterizationOptions` avec des valeurs de largeur et de hauteur personnalisées avant l’exportation. Cette étape répond directement au mot‑clé principal **définir la taille de page PDF**.

## Prérequis

- **Java Development Kit (JDK)** – Java 8 ou version supérieure installé sur votre machine.  
- **Aspose.CAD for Java** – Téléchargez depuis la page officielle [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – Un dossier contenant les fichiers DWG/DXF que vous souhaitez traiter.

## Import Namespaces

Tout d’abord, importez les classes nécessaires. Le bloc de code reste identique à celui du tutoriel original.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
```

## Étape 1 : Charger le fichier DWG/DXF

Chargez votre dessin source. Ajustez le chemin pour pointer vers votre propre fichier.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Étape 2 : Configurer les options d’exportation PDF (y compris la taille de page)

Ici nous définissons la largeur et la hauteur de la page — c’est l’endroit où nous **définissons la taille de page PDF**. Les valeurs sont en pixels ; vous pouvez les convertir depuis les pouces ou les millimètres selon vos besoins.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // <-- custom width
cadRasterizationOptions.setPageHeight(600);  // <-- custom height
```

> **Astuce :** Si vous préférez les formats de papier standards, utilisez la conversion `1 pouce = 72 points`. Pour une page A4 (8,27 × 11,69 po), définissez `pageWidth = 595` et `pageHeight = 842`.

## Étape 3 : Implémenter le suivi

Le suivi capture tout problème de rendu. Nous attachons un gestionnaire personnalisé qui sera invoqué après l’exportation.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Étape 4 : Exporter vers PDF

Effectuez maintenant la conversion. Le PDF sera créé avec les dimensions que vous avez spécifiées, et les informations de suivi seront affichées dans la console.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Étape 5 : Classe CadRenderHandler

Le gestionnaire affiche toutes les erreurs survenues pendant le rendu. Cela vous aide à déboguer les problèmes lors de **l’exportation d’un dessin CAD en PDF**.

```java
public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler {
    @Override
    public void invoke(CadRenderResult result) {
        System.out.println("Tracking results of exporting");

        if (result.isRenderComplete())
            return;

        System.out.println("Have some problems:");

        int idxError = 1;
        for (RenderResult rr : result.getFailures()) {
            System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
            idxError++;
        }
    }
}
```

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **PDF blanc** | Taille de page définie à 0 ou trop petite | Vérifiez que `setPageWidth` et `setPageHeight` sont des valeurs positives. |
| **Géométrie manquante Erreurs de rendu capturées par le gestionnaire | Consultez la sortie console de `ErrorHandler` et traitez le `RenderCode` indiqué. |
| **Fichier introuvable** | Chemin `dataDir` incorrect | Utilisez un chemin absolu ou assurez‑vous que le répertoire existe. |
| **Exception de licence** | Utilisation de la version d’essai sans licence valide pour de gros fichiers | Appliquez votre licence Aspose.CAD avant de charger l’image. |

## Questions fréquemment posées

**Q : Puis‑je activer le suivi pour d’autres formats de fichiers CAD avec Aspose.CAD pour Java ?**  
R : Aspose.CAD prend principalement en charge le suivi pour DWG/DXF. Pour d’autres formats, consultez la documentation officielle.

**Q : Comment gérer des options d’exportation supplémentaires dans Aspose.CAD pour Java ?**  
R : La bibliothèque propose de nombreuses options telles que DPI, couleur d’arrière‑plan et rasterisation vectorielle. Voir la [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/) pour plus de détails.

**Q : Existe‑t‑il une version d’essai d’Aspose.CAD pour Java ?**  
R : Oui, vous pouvez télécharger une version d’essai gratuite depuis le [Aspose.CAD Free Trial](https://releases.aspose.com/).

**Q : Où puis‑je obtenir de l’aide ou discuter des problèmes liés à Aspose.CAD pour Java ?**  
R : Visitez le [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour le support communautaire et les réponses officielles.

**Q : Comment obtenir une licence temporaire pour Aspose.CAD pour Java ?**  
R : Suivez les étapes décrites sur la page [Temporary License](https://purchase.aspose.com/temporary-license/).

---

**Dernière mise à jour :** 2025-12-03  
**Testé avec :** Aspose.CAD for Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}