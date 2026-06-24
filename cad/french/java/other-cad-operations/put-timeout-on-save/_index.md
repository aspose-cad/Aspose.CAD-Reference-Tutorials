---
date: 2026-06-19
description: Apprenez à définir un délai d'attente lors de l'enregistrement de dessins
  CAD avec Aspose.CAD pour Java. Améliorez les performances, évitez les blocages et
  exportez les fichiers CAD en PDF efficacement.
keywords:
- how to set timeout
- convert dwg to pdf
- export cad to pdf
linktitle: Définir un délai d'attente à l'enregistrement
schemas:
- author: Aspose
  dateModified: '2026-06-19'
  description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  headline: How to Set Timeout on Save for CAD with Aspose.CAD
  type: TechArticle
- description: Learn how to set timeout on saving CAD drawings with Aspose.CAD for
    Java. Boost performance, avoid hangs, and export CAD to PDF efficiently.
  name: How to Set Timeout on Save for CAD with Aspose.CAD
  steps:
  - name: Set Source and Output Directories
    text: Ensure you have the correct source and output directories for your CAD drawings.
  - name: Create Interruption Token Source
    text: Initialize an interruption token source to manage interruptions during the
      save operation.
  - name: Load CAD Drawing
    text: The `CadImage` class is Aspose.CAD's core object that represents a CAD drawing
      in memory, offering methods for rendering and conversion.
  - name: Configure Rasterization Options
    text: '`CadRasterizationOptions` specifies how the CAD drawing is rasterized into
      an image. Configure rasterization options for the CAD drawing.'
  - name: Configure PDF Options
    text: '`PdfOptions` defines settings for saving a CAD drawing as a PDF document.
      Set up PDF options with vector rasterization options and the interruption token.'
  - name: Save Drawing with Timeout
    text: Save the CAD drawing to a PDF file with the specified timeout.
  - name: Handle Interruption
    text: '`OperationCanceledException` is thrown when a save operation exceeds the
      specified timeout. Create a thread to handle the save operation and interrupt
      it after a specified timeout.'
  type: HowTo
- questions:
  - answer: Yes, wrap each conversion in its own thread with a separate interruption
      token to enforce per‑file time limits.
    question: Can I use this feature to convert DWG to PDF in a batch job?
  - answer: The timeout mechanism is tied to the `InterruptionTokenSource` and works
      with any format that respects the token, including PDF, PNG, and SVG.
    question: Does the timeout work on all output formats?
  - answer: Aspose.CAD automatically discards incomplete output, so you won’t end
      up with corrupted PDFs.
    question: What happens to partially written files after a timeout?
  - answer: Yes, a valid Aspose.CAD license is required for commercial deployments;
      a free trial is available for evaluation.
    question: Is a license required for production use?
  - answer: The official Aspose.CAD documentation provides additional code snippets
      and best‑practice guidelines.
    question: Where can I find more examples of using interruption tokens?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Comment définir un délai d'attente lors de l'enregistrement pour CAD avec Aspose.CAD
url: /fr/java/other-cad-operations/put-timeout-on-save/
weight: 15
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir un délai d'expiration lors de l'enregistrement pour CAD avec Aspose.CAD

## Introduction

Dans ce guide complet, vous apprendrez **comment définir un délai d'expiration** lors de l'enregistrement de dessins CAD à l'aide d'Aspose.CAD pour Java. Appliquer un délai d'expiration empêche les opérations d'enregistrement de longue durée de bloquer votre application, ce qui est particulièrement important lorsque vous devez **exporter CAD vers PDF** ou **convertir DWG en PDF** dans des scénarios de traitement par lots. Aspose.CAD pour Java prend en charge plus de 50 formats CAD et peut gérer des fichiers de plusieurs centaines de pages sans charger le document complet en mémoire, vous offrant des performances prévisibles et une utilisation maîtrisée des ressources.

## Réponses rapides
- **Que fait le délai d'expiration ?** Il interrompt l'opération d'enregistrement après une période spécifiée, libérant le thread et évitant les fuites de ressources.  
- **Quelle classe contrôle le délai d'expiration ?** `InterruptionTokenSource` fournit le jeton d'annulation utilisé par la routine d'enregistrement.  
- **Puis‑je toujours exporter CAD vers PDF après un délai d'expiration ?** Oui – vous pouvez attraper l'exception d'interruption et réessayer ou consigner l'échec.  
- **Ai‑je besoin d'une licence spéciale ?** Une licence Aspose.CAD standard suffit ; la fonctionnalité de délai d'expiration est intégrée.  
- **Cette approche est‑elle thread‑safe ?** Oui, lorsque chaque enregistrement s'exécute dans son propre thread avec son propre jeton.

## Qu'est-ce qu'un délai d'expiration dans les opérations d'enregistrement CAD ?
Un délai d'expiration est une limite de temps configurable qui, lorsqu'elle est dépassée, force le processus d'enregistrement à s'arrêter et lève une exception d'interruption. Cela protège votre application Java des blocages indéfinis causés par des dessins complexes ou des goulets d'étranglement d'E/S.

## Pourquoi définir un délai d'expiration lors de l'enregistrement de fichiers CAD ?
Aspose.CAD peut **convertir DWG en PDF** et **exporter CAD vers PDF** en moins d'une seconde pour les dessins typiques, mais des fichiers extrêmement volumineux ou corrompus peuvent prendre plusieurs minutes. En définissant un délai d'expiration, vous garantissez qu'aucun enregistrement unique ne dépassera, par exemple, 30 secondes, maintenant ainsi la stabilité du débit global du lot et évitant la famine de threads.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d'avoir les prérequis suivants :
- **Aspose.CAD pour Java Library** – Assurez‑vous d'avoir intégré la bibliothèque Aspose.CAD pour Java dans votre projet. Vous pouvez télécharger la bibliothèque depuis le [website](https://releases.aspose.com/cad/java/).
- **Environnement de développement** – Configurez votre environnement de développement Java avec tous les outils et dépendances nécessaires.

## Importer les packages

Pour commencer, importez les packages requis dans votre projet Java. Ajoutez les lignes suivantes au début de votre fichier Java :

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Passons maintenant à l'analyse du code d'exemple étape par étape :

## Comment définir un délai d'expiration lors de l'enregistrement de dessins CAD ?

Chargez votre fichier CAD, créez un `InterruptionTokenSource` avec le délai souhaité, et transmettez le jeton aux options d'enregistrement PDF. Si l'opération dépasse le délai, Aspose.CAD lève une `OperationCanceledException`, que vous pouvez attraper pour gérer l'échec de manière élégante.

### Étape 1 : Définir les répertoires source et de sortie

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Assurez‑vous que les répertoires source et de sortie pour vos dessins CAD sont corrects.

### Étape 2 : Créer une source de jeton d'interruption

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialisez une source de jeton d'interruption pour gérer les interruptions pendant l'opération d'enregistrement.

### Étape 3 : Charger le dessin CAD

La classe `CadImage` est l'objet principal d'Aspose.CAD qui représente un dessin CAD en mémoire, offrant des méthodes de rendu et de conversion.

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

### Étape 4 : Configurer les options de rasterisation

`CadRasterizationOptions` spécifie comment le dessin CAD est rasterisé en image.

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configurez les options de rasterisation pour le dessin CAD.

### Étape 5 : Configurer les options PDF

`PdfOptions` définit les paramètres pour enregistrer un dessin CAD en tant que document PDF.

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configurez les options PDF avec les options de rasterisation vectorielle et le jeton d'interruption.

### Étape 6 : Enregistrer le dessin avec délai d'expiration

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Enregistrez le dessin CAD dans un fichier PDF avec le délai d'expiration spécifié.

### Étape 7 : Gérer l'interruption

`OperationCanceledException` est levée lorsqu'une opération d'enregistrement dépasse le délai spécifié.

```java
java.lang.Thread thread = new java.lang.Thread(new Runnable() {
    @Override
    public void run() {
        try {
            cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
        } catch (Throwable th) {
            System.out.println("interrupted !!!");
        }
    }
});
thread.start();
TimeUnit.SECONDS.sleep(3);
source.interrupt();
thread.join();
```

Créez un thread pour gérer l'opération d'enregistrement et l'interrompre après le délai spécifié.

## Problèmes courants et solutions

- **Délai trop court** – Si vous recevez des interruptions fréquentes, augmentez la valeur du délai pour accueillir des dessins plus volumineux.  
- **InterruptedException non capturée** – Enveloppez toujours l'appel d'enregistrement dans un bloc try‑catch pour `OperationCanceledException` afin d'éviter que l'application ne plante.  
- **Consommation mémoire** – Utilisez `PdfOptions.setVectorRasterizationOptions` pour diffuser la sortie plutôt que de charger le fichier complet en mémoire.

## Questions fréquemment posées

**Q : Puis‑je utiliser cette fonctionnalité pour convertir DWG en PDF dans un travail par lots ?**  
R : Oui, encapsulez chaque conversion dans son propre thread avec un jeton d'interruption distinct afin d'appliquer des limites de temps par fichier.

**Q : Le délai d'expiration fonctionne‑t‑il sur tous les formats de sortie ?**  
R : Le mécanisme de délai d'expiration est lié à `InterruptionTokenSource` et fonctionne avec tout format qui respecte le jeton, y compris PDF, PNG et SVG.

**Q : Que se passe‑t‑il avec les fichiers partiellement écrits après un délai d'expiration ?**  
R : Aspose.CAD supprime automatiquement les sorties incomplètes, vous n'obtiendrez donc pas de PDF corrompu.

**Q : Une licence est‑elle requise pour une utilisation en production ?**  
R : Oui, une licence Aspose.CAD valide est nécessaire pour les déploiements commerciaux ; une version d'essai gratuite est disponible pour l'évaluation.

**Q : Où puis‑je trouver davantage d'exemples d'utilisation des jetons d'interruption ?**  
R : La documentation officielle d'Aspose.CAD fournit des extraits de code supplémentaires et des bonnes pratiques.

## Ressources supplémentaires

- [releases page](https://releases.aspose.com/cad/java/) – Page de téléchargement direct des dernières versions d'Aspose.CAD pour Java.  
- [documentation](https://reference.aspose.com/cad/java/) – Référence API complète et guides développeur.  
- [this link](https://releases.aspose.com/) – Versions générales des produits Aspose.  
- [here](https://purchase.aspose.com/temporary-license/) – Obtenez une licence temporaire pour les tests.  
- [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) – Support communautaire et discussions.

## Conclusion

Vous avez maintenant maîtrisé **comment définir un délai d'expiration** pour l'enregistrement de dessins CAD avec Aspose.CAD pour Java. En intégrant un `InterruptionTokenSource` dans votre flux de travail, vous pouvez **exporter CAD vers PDF** ou **convertir DWG en PDF** de façon fiable sans risquer de longs blocages, gardant ainsi votre application réactive et évolutive.

---

**Dernière mise à jour :** 2026-06-19  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Export Specific DWG Layout to PDF Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-specific-dwg-layout-to-pdf/)
- [Convert DWG to PNG and Other Raster Formats Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/convert-cad-layout-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}