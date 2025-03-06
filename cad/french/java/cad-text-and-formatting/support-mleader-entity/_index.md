---
title: Prise en charge de l'entité MLeader pour le format DWG avec Aspose.CAD pour Java
linktitle: Prise en charge de l'entité MLeader pour le format DWG avec Java
second_title: API Java Aspose.CAD
description: Libérez la puissance d'Aspose.CAD pour Java avec notre didacticiel étape par étape sur la prise en charge des entités MLeader au format DWG.
weight: 12
url: /fr/java/cad-text-and-formatting/support-mleader-entity/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Prise en charge de l'entité MLeader pour le format DWG avec Aspose.CAD pour Java

## Introduction

Dans le domaine de la conception assistée par ordinateur (CAO) avec Java, comprendre et mettre en œuvre la prise en charge des entités MLeader au format DWG est une compétence précieuse. Aspose.CAD pour Java fournit une solution robuste pour de telles tâches, offrant un ensemble d'outils et de fonctionnalités puissants. Ce didacticiel vous guidera tout au long du processus de prise en charge des entités MLeader dans les fichiers DWG à l'aide de Java avec Aspose.CAD.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

1. Environnement de développement Java : assurez-vous d'avoir configuré un environnement de développement Java sur votre système.

2.  Bibliothèque Aspose.CAD : téléchargez et installez la bibliothèque Aspose.CAD pour Java à partir du[lien de téléchargement](https://releases.aspose.com/cad/java/).

## Importer des espaces de noms

Dans votre projet Java, importez les espaces de noms nécessaires pour exploiter efficacement les capacités d'Aspose.CAD. Incluez les lignes suivantes dans votre code :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeader;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderContextData;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderLine;
import com.aspose.cad.fileformats.cad.cadobjects.CadMLeaderNode;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

```

Maintenant, décomposons le code en un guide étape par étape pour prendre en charge les entités MLeader pour le format DWG à l'aide de Java avec Aspose.CAD.

## 1. Chargez le fichier DWG et accédez à CadImage

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

## 2. Valider les entités MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### 3. Vérifiez le style et les attributs de MLeader

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

## 4. Accéder aux données contextuelles MLeader

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

## 5. Valider les attributs de contexte

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(), "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

## 6. Accédez au nœud MLeader et à la ligne Leader

```java
CadMLeaderNode mleaderNode = context.getLeaderNode();
Assert.areEqual(mleaderNode.getLastLeaderLinePoint().getX(), 473, 1);

CadMLeaderLine leaderLine = mleaderNode.getLeaderLine();
Assert.areEqual(leaderLine.getBreakEndPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getBreakPointIndex().getValue()), Integer.toString(0));
Assert.areEqual(leaderLine.getBreakStartPoint().toString(), null);
Assert.areEqual(Integer.toString(leaderLine.getLeaderLineIndex().getValue()), Integer.toString(0));
Assert.areEqual(Integer.toString(leaderLine.getLeaderPoints().size()), Integer.toString(4));
```

## 7. Valider les attributs MLeader supplémentaires

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

## 8. Valider les attributs du texte

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

## 9. Attributs supplémentaires de MLeader

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Conclusion

Toutes nos félicitations! Vous avez parcouru avec succès le guide complet sur la prise en charge des entités MLeader pour le format DWG à l'aide de Java et Aspose.CAD. Cette fonctionnalité ouvre les portes à des manipulations CAO avancées et améliore votre boîte à outils de développement Java.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres formats de CAO ?

A1 : Oui, Aspose.CAD prend en charge divers formats de CAO au-delà du DWG, offrant ainsi une polyvalence à vos projets.

### Q2 : Où puis-je trouver une documentation détaillée pour Aspose.CAD pour Java ?

 A2 : Reportez-vous au[Documentation](https://reference.aspose.com/cad/java/) pour un aperçu approfondi des capacités d'Aspose.CAD.

### Q3 : Existe-t-il un essai gratuit disponible ?

 A3 : Oui, explorez les fonctionnalités directement avec le[essai gratuit](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir une licence temporaire pour Aspose.CAD ?

A4 : Obtenez une licence temporaire via[ce lien](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis-je demander le soutien et l’assistance de la communauté ?

A5 : Visitez le[Forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour se connecter avec la communauté et obtenir de l'aide.
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
