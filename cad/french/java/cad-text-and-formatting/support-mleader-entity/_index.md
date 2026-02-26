---
date: 2026-01-10
description: Apprenez à lire les fichiers DWG et à créer des entités multileader DWG
  à l’aide d’Aspose.CAD pour Java dans ce tutoriel étape par étape.
linktitle: Support MLeader Entity for DWG Format with Java
second_title: Aspose.CAD Java API
title: Comment lire les fichiers DWG et prendre en charge MLeader avec Aspose.CAD
  pour Java
url: /fr/java/cad-text-and-formatting/support-mleader-entity/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment lire les fichiers DWG et prendre en charge MLeader avec Aspose.CAD pour Java

## Introduction

Si vous devez **lire des fichiers DWG** et travailler avec des entités **multileader DWG** dans une application Java, vous êtes au bon endroit. Aspose.CAD pour Java vous offre une méthode propre et programmatique pour ouvrir des dessins DWG, inspecter les objets MLeader et valider leurs propriétés — le tout sans nécessiter une station de travail CAD complète. Dans ce tutoriel, nous parcourrons chaque étape, du chargement d’un fichier DWG à la confirmation que les données du multileader correspondent au style attendu.

## Réponses rapides
- **Que comprend « comment lire dwg » ?** Charger le DWG avec `Image.load()` et le caster en `CadImage`.
- **Puis‑je créer des entités multileader dwg ?** Oui – vous pouvez ajouter, modifier et valider des objets MLeader en utilisant l’API CadMLeader.
- **Quelle version de la bibliothèque est requise ?** Toute version récente d’Aspose.CAD pour Java (l’API présentée fonctionne avec les builds 2024+).
- **Ai‑je besoin d’une licence pour le développement ?** Une licence temporaire suffit pour les tests ; une licence complète est requise en production.
- **Le code est‑il multiplateforme ?** Absolument – Java fonctionne sous Windows, Linux et macOS.

## Qu’est‑ce que « comment lire dwg » avec Aspose.CAD ?

Lire un fichier DWG signifie convertir le dessin binaire en un objet `CadImage` en mémoire. Une fois cet objet obtenu, vous pouvez parcourir ses entités (lignes, cercles, texte, objets **MLeader**, etc.) et inspecter leurs propriétés.

## Pourquoi prendre en charge les entités MLeader ?

Les objets MLeader (multileader) combinent des lignes de repère avec du texte ou des blocs attachés, ce qui les rend essentiels pour les annotations dans les dessins d’ingénierie. Les prendre en charge vous permet de :

- Vérifier que les annotations respectent les normes de l’entreprise.
- Extraire le texte pour un traitement en aval (par ex., génération de nomenclature).
- Modifier programmatiquement les styles de repère ou remplacer le contenu des blocs.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

1. **Environnement de développement Java** – JDK 11+ et votre IDE préféré (IntelliJ, Eclipse, VS Code).  
2. **Aspose.CAD pour Java** – Téléchargez le JAR le plus récent depuis le [download link](https://releases.aspose.com/cad/java/).  

## Importer les espaces de noms

Ajoutez les importations suivantes à votre classe Java afin de pouvoir travailler avec les entités DWG et les options de rasterisation :

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

## Comment lire les fichiers DWG avec Aspose.CAD pour Java

### Étape 1 : Charger le fichier DWG et obtenir un `CadImage`

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String file = dataDir + "Multileaders.dwg";
Image image = Image.load(file);
CadImage cadImage = (CadImage) image;
```

### Étape 2 : Valider que le dessin contient des entités MLeader

```java
Assert.areNotEqual(cadImage.getEntities().length, 0);
CadMLeader cadMLeader = (CadMLeader) cadImage.getEntities()[2];
```

### Étape 3 : Vérifier le style MLeader et les attributs de base

```java
Assert.areEqual(cadMLeader.getStyleDescription(), "Standard");
Assert.areEqual(cadMLeader.getLeaderStyleId(), "12E");
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderLineTypeID(), "14");
```

### Étape 4 : Accéder aux données de contexte MLeader (le cœur du multileader)

```java
CadMLeaderContextData context = cadMLeader.getContextData();
```

### Étape 5 : Valider les attributs au niveau du contexte

```java
Assert.areEqual(context.getArrowHeadSize(), 30.0, 0.1);
Assert.areEqual(context.getBasePoint().getX(), 481, 1);
Assert.areEqual(context.getContentScale(), 1.0, 0.01);
Assert.areEqual(context.getDefaultText().getValue(),
    "This is multileader with huge text\\P{\\H1.5x;6666666666666666666666666666\\P}bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
Assert.areEqual(context.hasMText(), true);
```

### Étape 6 : Travailler avec le nœud MLeader et sa ligne de repère

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

### Étape 7 : Valider les attributs supplémentaires du nœud MLeader

```java
Assert.areEqual(Integer.toString(mleaderNode.getBranchIndex()), Integer.toString(0));
Assert.areEqual(mleaderNode.getDogLegLength(), 8.0, 0.1);
Assert.areEqual(context.hasMText(), true);
```

### Étape 8 : Vérifier les propriétés liées au texte

```java
Assert.areEqual(context.getTextAttachmentType().getValue(), (short) 1);
Assert.areEqual(context.getTextBackgroundColor().getValue(), 18);
Assert.areEqual(context.getTextHeight(), 20.0, 0.1);
Assert.areEqual(context.getTextStyleID().getValue(), "11");
Assert.areEqual(context.getTextRotation().getValue(), 0.0, 0.01);
```

### Étape 9 : Examiner les autres attributs MLeader pour assurer la complétude

```java
Assert.areEqual(cadMLeader.getArrowHeadId1(), "639");
Assert.areEqual(cadMLeader.getLeaderType(), 1);
Assert.areEqual(cadMLeader.getBlockContentColor(), 0);
Assert.areEqual(cadMLeader.getLeaderLineColor(), 0);
Assert.areEqual(cadMLeader.getTextHeight(), 1.0, 0.01);
```

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| `ClassCastException` lors du cast d’une entité | L’indice sélectionné n’est pas un objet MLeader. | Vérifiez `cadImage.getEntities()[i] instanceof CadMLeader` avant le cast. |
| Valeurs `null` pour les points de la ligne de repère | Le dessin utilise un style de repère personnalisé non entièrement pris en charge. | Utilisez la dernière version d’Aspose.CAD ou revenez au style par défaut pour les tests. |
| Échecs d’assertion sur des valeurs numériques | Légères différences d’arrondi entre les versions CAD. | Ajustez la tolérance dans `Assert.areEqual(..., delta)` comme indiqué dans les exemples. |

## Questions fréquentes

**Q : Puis‑je utiliser Aspose.CAD pour Java avec d’autres formats CAD ?**  
R : Oui, Aspose.CAD prend en charge DXF, DWF, DGN et plusieurs formats raster en plus du DWG.

**Q : Où puis‑je trouver la documentation détaillée d’Aspose.CAD pour Java ?**  
R : Consultez la [documentation](https://reference.aspose.com/cad/java/) officielle pour les détails de l’API et des exemples de code.

**Q : Existe‑t‑il un essai gratuit ?**  
R : Absolument – vous pouvez télécharger un essai depuis la page [free trial](https://releases.aspose.com/).

**Q : Comment obtenir une licence temporaire pour les tests ?**  
R : Obtenez une licence temporaire via le [temporary license link](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je demander de l’aide à la communauté ?**  
R : Le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) est l’endroit idéal pour poser des questions et partager des solutions.

## Conclusion

Vous disposez maintenant d’un guide complet, de bout en bout, pour **lire des fichiers DWG** et **créer des entités multileader DWG** à l’aide d’Aspose.CAD pour Java. En suivant les étapes ci‑dessus, vous pouvez valider les styles MLeader, extraire les données d’annotation et intégrer le traitement DWG dans n’importe quel flux de travail basé sur Java.

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}

---

**Dernière mise à jour :** 2026-01-10  
**Testé avec :** Aspose.CAD 24.11 pour Java  
**Auteur :** Aspose