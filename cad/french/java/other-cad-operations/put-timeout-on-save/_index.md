---
title: Délai d'expiration lors de l'enregistrement pour la CAO avec Aspose.CAD
linktitle: Mettre le délai d'attente lors de l'enregistrement
second_title: API Java Aspose.CAD
description: Découvrez comment augmenter les performances de votre application Java avec Aspose.CAD. Mettez un délai d'attente pour l'enregistrement des dessins CAO. Suivez notre guide étape par étape.
weight: 15
url: /fr/java/other-cad-operations/put-timeout-on-save/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Délai d'expiration lors de l'enregistrement pour la CAO avec Aspose.CAD

## Introduction

Bienvenue dans le didacticiel sur la mise en place d'un délai d'attente lors de l'enregistrement à l'aide d'Aspose.CAD pour Java. Dans ce guide, nous vous guiderons tout au long du processus de définition d'un délai d'expiration pour l'enregistrement des dessins CAO afin d'améliorer les performances de votre application. Aspose.CAD for Java est une bibliothèque puissante qui vous permet de travailler de manière transparente avec des fichiers CAO dans vos applications Java.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :
-  Bibliothèque Aspose.CAD pour Java : assurez-vous que la bibliothèque Aspose.CAD pour Java est intégrée à votre projet. Vous pouvez télécharger la bibliothèque à partir du[site web](https://releases.aspose.com/cad/java/).
- Environnement de développement : configurez votre environnement de développement Java avec tous les outils et dépendances nécessaires.

## Importer des packages

Pour commencer, importez les packages requis dans votre projet Java. Ajoutez les lignes suivantes au début de votre fichier Java :

```java
import com.aspose.cad.Image;
import com.aspose.cad.InterruptionTokenSource;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.concurrent.TimeUnit;
```

Maintenant, décomposons l'exemple de code en instructions étape par étape :

## Étape 1 : Définir les répertoires source et de sortie

```java
final String SourceDir = Utils.getDataDir_DWGDrawings();
final String OutputDir = Utils.getDataDir_Output();
```

Assurez-vous que vous disposez des répertoires source et de sortie corrects pour vos dessins CAO.

## Étape 2 : Créer une source de jeton d'interruption

```java
final InterruptionTokenSource source = new com.aspose.cad.InterruptionTokenSource();
```

Initialisez une source de jeton d'interruption pour gérer les interruptions pendant l'opération de sauvegarde.

## Étape 3 : Charger le dessin CAO

```java
final CadImage cadImageBig = (CadImage)Image.load(SourceDir + "Drawing11.dwg");
```

 Chargez le dessin CAO dans un`CadImage` objet.

## Étape 4 : configurer les options de rastérisation

```java
CadRasterizationOptions rasterizationOptionsBig = new CadRasterizationOptions();
rasterizationOptionsBig.setPageWidth(cadImageBig.getSize().getWidth() / 2);
rasterizationOptionsBig.setPageHeight(cadImageBig.getSize().getHeight() / 2);
```

Configurez les options de rastérisation pour le dessin CAO.

## Étape 5 : Configurer les options PDF

```java
final PdfOptions CADfBig = new PdfOptions();
CADfBig.setVectorRasterizationOptions(rasterizationOptionsBig);
CADfBig.setInterruptionToken(source.getToken());
```

Configurez les options PDF avec les options de rastérisation vectorielle et le jeton d'interruption.

## Étape 6 : Enregistrer le dessin avec délai d'attente

```java
cadImageBig.save(OutputDir + "PutTimeoutOnSave_out.pdf", CADfBig);
```

Enregistrez le dessin CAO dans un fichier PDF avec le délai d'expiration spécifié.

## Étape 7 : Gérer les interruptions

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

Créez un thread pour gérer l'opération de sauvegarde et interrompez-la après un délai d'attente spécifié.

## Conclusion

Toutes nos félicitations! Vous avez appris avec succès comment définir un délai d'attente lors de l'enregistrement à l'aide d'Aspose.CAD pour Java. Cette fonctionnalité peut considérablement améliorer l'efficacité de vos applications liées à la CAO.

## FAQ

### Q1 : Comment puis-je télécharger Aspose.CAD pour Java ?

 A1 : Vous pouvez le télécharger à partir du[page des versions](https://releases.aspose.com/cad/java/).

### Q2 : Où puis-je trouver la documentation d'Aspose.CAD pour Java ?

 A2 : Reportez-vous au[Documentation](https://reference.aspose.com/cad/java/) pour des informations complètes.

### Q3 : Existe-t-il un essai gratuit disponible ?

A3 : Oui, vous pouvez bénéficier d'un essai gratuit auprès de[ce lien](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une licence temporaire ?

 A4 : Visite[ici](https://purchase.aspose.com/temporary-license/) pour les détails de la licence temporaire.

### Q5 : Besoin d'aide ou avez des questions ?

 A5 : Rendez-vous au[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le soutien de la communauté.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
