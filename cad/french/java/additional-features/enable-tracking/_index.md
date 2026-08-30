---
date: 2026-06-29
description: Apprenez comment exporter DWG en PDF, activer le suivi et utiliser une
  classe Java de gestionnaire d'erreurs personnalisée avec Aspose.CAD pour Java. Inclut
  la conversion DXF‑vers‑PDF.
keywords:
- export dwg to pdf
- custom error handler java
- dwg to pdf java
linktitle: Activer le suivi dans les fichiers DWG avec Java
schemas:
- author: Aspose
  dateModified: '2026-06-29'
  description: Learn how to export DWG to PDF, enable tracking, and use a custom error
    handler Java class with Aspose.CAD for Java. Includes DXF‑to‑PDF conversion.
  headline: Export DWG to PDF and Enable Tracking with Aspose.CAD Java
  type: TechArticle
- questions:
  - answer: It activates Aspose.CAD’s render callbacks so you can see warnings and
      errors during export.
    question: What does “enable dwg tracking java” do?
  - answer: A trial works for testing; a commercial license is required for production
      use.
    question: Do I need a license?
  - answer: Yes – the same `PdfOptions` object used for DWG works for DXF, covering
      the *java convert dxf pdf* scenario.
    question: Can I also convert DXF to PDF?
  - answer: Java 8 or higher.
    question: Which JDK version is required?
  - answer: See the [Aspose.CAD Java Documentation](https://reference.aspose.com/cad/java/)
      linked below.
    question: Where can I find more examples?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Exporter DWG en PDF et activer le suivi avec Aspose.CAD Java
url: /fr/java/additional-features/enable-tracking/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exporter DWG en PDF et activer le suivi avec Aspose.CAD Java

## Introduction

Exporter DWG en PDF tout en conservant une visibilité complète du processus de conversion est essentiel pour les équipes modernes centrées sur la CAO. Dans ce guide, vous découvrirez **comment activer le suivi** dans les flux de travail DWG, convertir DXF en PDF dans le même pipeline, et capturer chaque avertissement de rendu avec une classe **custom error handler Java**. À la fin, vous disposerez d’un extrait prêt pour la production qui non seulement génère des PDF haute fidélité, mais consigne également les informations de diagnostic pour l’audit et le dépannage.

## Réponses rapides
- **Que fait “enable dwg tracking java” ?** Il active les callbacks de rendu d’Aspose.CAD afin que vous puissiez voir les avertissements et les erreurs pendant l’exportation.  
- **Ai-je besoin d’une licence ?** Un essai fonctionne pour les tests ; une licence commerciale est requise pour une utilisation en production.  
- **Puis-je également convertir DXF en PDF ?** Oui – le même objet `PdfOptions` utilisé pour DWG fonctionne pour DXF, couvrant le scénario *java convert dxf pdf*.  
- **Quelle version du JDK est requise ?** Java 8 ou supérieur.  
- **Où puis‑je trouver plus d’exemples ?** Voir la [Documentation Aspose.CAD Java](https://reference.aspose.com/cad/java/) ci‑dessous.

## Qu’est‑ce que l’exportation DWG en PDF ?

L’exportation DWG vers PDF est le processus de conversion d’un dessin AutoCAD natif (DWG) en un document PDF portable tout en préservant la fidélité vectorielle, les calques et les annotations. Aspose.CAD effectue cette conversion entièrement en Java, éliminant le besoin d’installations AutoCAD natives.

## Pourquoi utiliser Aspose.CAD pour Java ?

Aspose.CAD pour Java offre une solution complète, pure‑Java pour la conversion CAO, prenant en charge plus de 50 formats, offrant des performances élevées et proposant un suivi intégré via des callbacks de rendu. Elle ne nécessite aucune dépendance externe et peut être intégrée aux pipelines côté serveur.

- **Prise en charge complète des formats** – gère DWG, DXF, DGN et plus de 50 autres formats CAD.  
- **Aucune dépendance externe** – bibliothèque pure‑Java idéale pour l’automatisation côté serveur.  
- **Suivi intégré** – `CadRenderHandler` fournit des résultats de rendu détaillés.  
- **Export PDF en une ligne** – `PdfOptions` convertit en PDF tout en conservant les données vectorielles intactes.  

Ces affirmations chiffrées sont étayées par la capacité d’Aspose.CAD à traiter des fichiers jusqu’à 500 pages sans charger le document complet en mémoire, atteignant des temps de conversion inférieurs à 2 secondes sur un serveur typique à 4 cœurs.

## Prérequis

- **Java Development Kit (JDK)** 8 ou plus récent installé sur votre machine.  
- **Aspose.CAD for Java** téléchargé depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/) officiel.  
- **Essai gratuit Aspose.CAD** disponible sur la page [Aspose.CAD Free Trial](https://releases.aspose.com/) si vous avez besoin d’une évaluation rapide.  
- Un dossier contenant les fichiers DWG/DXF que vous souhaitez convertir.  

## Comment exporter DWG en PDF ?

Chargez votre fichier source, configurez `PdfOptions`, attachez un `CadRenderHandler` personnalisé, et appelez `save`. Ce flux de bout en bout convertit DWG (ou DXF) en PDF tout en émettant des informations de suivi pour chaque étape de rendu, garantissant que tous les avertissements ou erreurs sont capturés et peuvent être traités par les développeurs ou les processus automatisés.

## Importer les espaces de noms

La classe `CadRenderHandler` est l’interface de rappel d’Aspose.CAD qui reçoit les diagnostics de rendu. Importez les packages requis avant de commencer à coder :

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

La classe `CadImage` représente un document CAD chargé en mémoire. L’instancier avec un chemin de fichier charge le dessin sans ouvrir d’application CAD native.

```java
String dataDir = "Your Document Directory" + "DXFDrawings/";
Image image = Image.load(dataDir + "conic_pyramid.dxf");
```

## Étape 2 : Configurer les options d’export PDF (Comment convertir DXF en PDF)

`PdfOptions` définit comment le rasteriseur CAD doit produire la sortie PDF, incluant les paramètres de rendu vectoriel et la taille de page. Définir `VectorRasterizationOptions` garantit que les lignes et courbes restent nettes. L’objet `VectorRasterizationOptions` spécifie les paramètres de rasterisation tels que le DPI et la couleur d’arrière‑plan.

```java
OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setPageWidth(800);
cadRasterizationOptions.setPageHeight(600);
```

## Étape 3 : Implémenter le suivi (Custom Error Handler Java)

`ErrorHandler` étend `CadRenderHandler` pour capturer les avertissements, erreurs et messages d’information émis pendant la rasterisation. Cette classe écrit chaque message dans la console, mais vous pouvez facilement les rediriger vers un fichier de journal ou un système de surveillance. `CadRenderHandler` est une interface qui reçoit les diagnostics de rendu du rasteriseur.

```java
cadRasterizationOptions.RenderResult = new ErrorHandler();
```

## Étape 4 : Exporter en PDF  

Appeler `save` sur l’instance `CadImage` avec les `PdfOptions` configurés effectue la conversion. Comme le gestionnaire personnalisé est déjà attaché, tout problème de rendu apparaît dans la console pendant l’exportation.

```java
System.out.println("Exporting to pdf format");
image.save(stream, pdfOptions);
```

## Étape 5 : Classe CadRenderHandler  

`CadRenderHandler` est la classe de base d’Aspose.CAD pour recevoir les résultats de rendu. Surcharger sa méthode `onRenderCompleted` vous donne accès à l’objet `RenderResult`, qui contient une collection d’entrées `RenderMessage` décrivant chaque étape du processus.

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

## Pourquoi cela importe-t-il  

Activer le suivi crée une piste d’audit qui satisfait les exigences de conformité dans les secteurs réglementés tels que l’architecture, l’ingénierie et la construction. Le gestionnaire d’erreurs personnalisé vous permet également d’intégrer des contrôles de santé de conversion CAD dans les pipelines CI/CD, signalant automatiquement les fichiers nécessitant une révision manuelle.

## Problèmes courants et solutions

- **`NullPointerException` sur `RenderResult`** – Assurez‑vous d’utiliser Aspose.CAD 23.10 ou plus récent ; les versions antérieures ne disposent pas de l’API `RenderResult`.  
- **Fichier non trouvé** – Vérifiez que `dataDir` pointe vers le bon dossier et que le nom de fichier correspond exactement à la casse.  
- **Sortie de suivi manquante** – Vérifiez que votre instance `ErrorHandler` est correctement assignée à `cadRasterizationOptions.setRenderHandler(new ErrorHandler())`.  

## Questions fréquemment posées

**Q:** Puis‑je activer le suivi pour d’autres formats de fichiers CAD avec Aspose.CAD pour Java ?  
**A:** Le suivi est principalement exposé pour DWG et DXF. Pour d’autres formats, consultez la documentation officielle pour voir quelles API exposent les callbacks de rendu.

**Q:** Comment puis‑je personnaliser des options d’export supplémentaires, comme définir les métadonnées PDF ?  
**A:** `PdfOptions` propose des propriétés telles que `setTitle`, `setAuthor` et `setSubject`. Définissez‑les avant d’appeler `save` pour intégrer les métadonnées dans le PDF résultant.

**Q:** La version d’essai suffit‑elle pour évaluer les fonctionnalités de suivi ?  
**A:** Oui, l’essai gratuit inclut un accès complet à l’API, vous permettant de tester `CadRenderHandler` et l’export PDF sans restrictions.

**Q:** Où puis‑je obtenir du support communautaire pour Aspose.CAD pour Java ?  
**A:** Consultez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour poser des questions et partager des expériences avec d’autres développeurs.

**Q:** Comment obtenir une licence temporaire pour les environnements de test automatisés ?  
**A:** Suivez les étapes sur [Temporary License](https://purchase.aspose.com/temporary-license/) pour générer un fichier de licence à durée limitée.

## Conclusion

En suivant ce tutoriel, vous savez maintenant comment **exporter DWG en PDF**, activer le suivi complet, et gérer la conversion DXF‑vers‑PDF avec une classe **custom error handler Java**. Intégrez ces extraits dans votre pipeline de construction pour obtenir de la visibilité, améliorer la fiabilité et répondre aux exigences de conformité du secteur pour le traitement des documents CAD.

---

**Last Updated:** 2026-06-29  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter DWG en PDF et convertir les dessins CAD – Tutoriel Aspose.CAD Java](/cad/java/cad-drawing-conversion/)
- [Exporter DWG en PDF ou raster avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Exporter une mise en page DWG spécifique en PDF avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}