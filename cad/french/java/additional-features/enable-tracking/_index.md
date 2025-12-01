---
date: 2025-12-01
description: Apprenez à définir la taille de la page PDF, à convertir les fichiers
  DWG en PDF et à activer le suivi des modifications DWG à l'aide d'Aspose.CAD pour
  Java.
language: fr
linktitle: Set PDF Page Size and Track DWG with Java
second_title: Aspose.CAD Java API
title: Définir la taille de la page PDF et suivre le DWG avec Aspose.CAD Java
url: /java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir la taille de la page PDF et suivre les DWG avec Aspose.CAD Java

## Introduction

Lorsque vous collaborez sur des projets CAD, vous devez souvent **définir la taille de la page PDF** pour une mise en page cohérente, **convertir DWG en PDF**, et suivre chaque modification apportée au dessin. Aspose.CAD for Java rend tout cela possible dans un flux de travail unique et simplifié. Dans ce tutoriel, nous parcourrons les étapes exactes pour **définir la taille de la page PDF**, activer le **suivi des modifications DWG**, et exporter le dessin au format PDF — le tout en utilisant Java.

## Réponses rapides
- **Comment définir la taille de la page PDF ?** Utilisez `CadRasterizationOptions.setPageWidth()` et `setPageHeight()` avant l'exportation.  
- **Puis-je suivre les modifications lors de l'exportation ?** Oui – implémentez un `CadRenderHandler` personnalisé pour capturer les résultats du suivi.  
- **Quelle méthode convertit DWG en PDF ?** Appelez `image.save(stream, pdfOptions)` après avoir configuré les options.  
- **Quelles sont les principales conditions préalables ?** JDK, Aspose.CAD for Java, et un dossier contenant des fichiers DWG/DXF.  
- **Une licence est‑elle requise pour la production ?** Oui, une licence valide d'Aspose.CAD est nécessaire pour les déploiements non‑essai.

## Qu’est‑ce que « définir la taille de la page PDF » dans le contexte de l’exportation DWG ?

Définir la taille de la page PDF détermine les dimensions du canevas PDF résultant (largeur × hauteur en pixels). C’est essentiel lorsque vous souhaitez que le dessin exporté s’adapte à une taille de papier ou à une mise en page d’écran spécifique, garantissant que tous les éléments apparaissent exactement où vous les attendez.

## Pourquoi activer le suivi lors de l’exportation de fichiers DWG ?

Le suivi (ou suivi des modifications) enregistre tout problème de rendu, police manquante ou entité non prise en charge qui survient lors de la conversion. En capturant ces informations, vous pouvez :
- Identifier rapidement les problèmes à corriger avant la livraison finale.  
- Fournir des retours clairs aux membres de l’équipe sur ce qui a été modifié ou omis.  
- Maintenir une traçabilité pour les industries fortement réglementées.

## Prérequis

- **Java Development Kit (JDK)** – toute version récente (8+).  
- **Aspose.CAD for Java** – téléchargez depuis la page officielle [Aspose CAD download page](https://releases.aspose.com/cad/java/).  
- **Document Directory** – un dossier contenant les fichiers DWG/DXF que vous souhaitez traiter.

## Importer les espaces de noms

Commencez par importer les classes Aspose.CAD nécessaires ainsi que les classes standard Java I/O.

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

## Étape 1 : Charger le fichier DWG (ou DXF)

Chargez votre dessin source dans un objet `Image`. Ajustez le chemin pour qu’il pointe vers votre propre répertoire.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Étape 2 : Configurer les options d’exportation PDF (y compris la taille de la page)

Ici nous définissons les options PDF et **définissons explicitement la taille de la page PDF** à 800 × 600 pixels. C’est ici que le mot‑clé principal est appliqué.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);   // set PDF page width
cadRasterizationOptions.setPageHeight(600);  // set PDF page height
```

## Étape 3 : Implémenter le suivi

Créez un gestionnaire d’erreurs personnalisé qui recevra les informations de suivi pendant le processus de conversion.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Étape 4 : Exporter en PDF

Avec les options et le gestionnaire de suivi en place, exportez le dessin. Cette étape **convertit DWG en PDF** (ou DXF en PDF dans notre exemple).

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Étape 5 : Classe CadRenderHandler – Capturer les résultats du suivi

La classe `ErrorHandler` étend `CadRenderHandler` et affiche tout problème de rendu survenu lors du **suivi des modifications des fichiers DWG**.

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

## Problèmes courants & comment les résoudre

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Polices manquantes** | Le fichier CAD référence des polices non installées sur le serveur. | Installez les polices requises ou intégrez‑les dans le dessin source. |
| **Entités non prises en charge** | Certaines entités DWG ne sont pas encore supportées par Aspose.CAD. | Utilisez la sortie du suivi pour les identifier et simplifier le dessin. |
| **Taille de page incorrecte** | `setPageWidth/Height` n’a pas été appelé avant l’exportation. | Assurez‑vous que la taille de la page est définie dans `CadRasterizationOptions` comme indiqué ci‑dessus. |

## Questions fréquemment posées

### Q1 : Puis‑je activer le suivi pour d’autres formats de fichiers CAD avec Aspose.CAD for Java ?

R1 : Aspose.CAD prend principalement en charge le suivi pour les fichiers DWG/DXF. Pour d’autres formats, consultez la documentation officielle afin de voir quelles fonctionnalités sont disponibles.

### Q2 : Comment puis‑je gérer des options d’exportation supplémentaires dans Aspose.CAD for Java ?

R2 : La bibliothèque offre de nombreuses options telles que le DPI, la couleur d’arrière‑plan et la rasterisation vectorielle. Explorez‑les dans la [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/).

### Q3 : Existe‑t‑il une version d’essai disponible pour Aspose.CAD for Java ?

R3 : Oui, vous pouvez télécharger une version d’essai gratuite depuis le [Aspose.CAD Free Trial](https://releases.aspose.com/).

### Q4 : Où puis‑je obtenir de l’aide ou discuter des problèmes liés à Aspose.CAD for Java ?

R4 : Le forum communautaire sur le [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) est un excellent endroit pour poser des questions et partager des expériences.

### Q5 : Comment obtenir une licence temporaire pour Aspose.CAD for Java ?

R5 : Suivez les étapes décrites sur la page [Temporary License](https://purchase.aspose.com/temporary-license/) pour demander une licence à durée limitée pour l’évaluation.

### Q6 : Puis‑je **convertir DWG en PDF** tout en préservant les calques ?

R6 : Oui. En configurant `CadRasterizationOptions`, vous pouvez préserver les informations de calque dans le PDF résultant.

### Q7 : Quelle est la meilleure façon d’**exporter DWG en PDF** avec des dimensions de page personnalisées ?

R7 : Définissez la largeur et la hauteur souhaitées à l’aide de `setPageWidth` et `setPageHeight` avant d’appeler `image.save()` – exactement comme démontré à l’Étape 2.

## Conclusion

En suivant les étapes ci‑dessus, vous pouvez **définir la taille de la page PDF**, **convertir DWG en PDF**, et **suivre les modifications des fichiers DWG** à l’aide d’Aspose.CAD for Java. Ce flux de travail vous offre un contrôle complet sur la mise en page du résultat tout en fournissant des diagnostics précieux qui assurent une collaboration CAD fluide et sans erreur. N’hésitez pas à explorer des options de rendu supplémentaires et à intégrer ce code dans des pipelines d’automatisation plus vastes.

---

**Dernière mise à jour :** 2025-12-01  
**Testé avec :** Aspose.CAD for Java 24.12 (latest at time of writing)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}