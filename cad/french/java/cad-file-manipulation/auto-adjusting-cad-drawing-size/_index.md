---
date: 2025-12-22
description: Apprenez à exporter des dessins CAO et à convertir des fichiers DWG en
  BMP en Java avec Aspose.CAD. Suivez ce guide étape par étape pour une manipulation
  efficace des fichiers CAO.
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
title: Comment exporter un dessin CAO au format BMP en utilisant Aspose.CAD pour Java
url: /fr/java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
weight: 13
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment exporter un dessin CAD au format BMP avec Aspise.CAD pour Java

## Introduction

Si vous cherchez une méthode claire et fiable pour **comment exporter des fichiers CAD** depuis Java, vous êtes au bon endroit. Avec Aspose.CAD pour Java, vous pouvez non seulement ajuster automatiquement les tailles de dessin mais aussi **convert DWG to BMP** en quelques lignes de code seulement. Ce tutoriel vous guide à travers l’ensemble du processus, de la configuration de votre environnement à la génération d’une image BMP qui préserve la mise en page CAD d’origine.

## Réponses rapides
- **What does “how to export cad” mean?** Il s’agit de convertir des fichiers CAD (DWG, DXF, etc.) en un autre format tel que BMP, PNG ou PDF.  
- **Which library handles the conversion?** Aspose.CAD pour Java fournit une API simple pour cette tâche.  
- **Do I need a license?** Une licence temporaire suffit pour les tests ; une licence complète est requise pour la production.  
- **Can I export multiple layouts at once?** Oui – en définissant la propriété `Layouts` vous pouvez spécifier les mises en page à rendre.  
- **Is BMP the only output format?** Non – vous pouvez également exporter en PNG, JPEG, TIFF, et plus encore.

## Qu’est‑ce que “how to export cad” avec Aspose.CAD ?
Exporter un CAD signifie prendre un dessin CAD natif (par ex., un fichier DWG) et le rendre sous forme d’image raster ou d’un autre format vectoriel. Aspose.CAD se charge de toute la lourde tâche : analyse de la structure CAD, rasterisation des entités vectorielles et écriture du résultat dans le format d’image choisi.

## Pourquoi utiliser Aspose.CAD pour Java pour **convert DWG to BMP** ?
- **Aucune dépendance externe** – Java pur, pas de DLL natives.  
- **Prise en charge complète de DWG, DXF, DGN et d’autres formats**.  
- **Contrôle fin** des options de rasterisation telles que la sélection de mise en page, le redimensionnement et la couleur d’arrière‑plan.  
- **Haute performance** adaptée au traitement par lots sur les serveurs.

## Prérequis

Avant de commencer, assurez‑vous de disposer de :

1. **Java Development Kit** – téléchargez‑le [ici](https://www.java.com/en/download/).  
2. **Aspose.CAD pour Java library** – obtenez le dernier JAR [ici](https://releases.aspose.com/cad/java/).  
3. **Sample CAD file** – un fichier DWG (par ex., `sample.dwg`) placé dans le répertoire *document* de votre projet.

## Import Namespaces

Dans votre application Java, incluez les espaces de noms nécessaires pour exploiter les fonctionnalités d’Aspose.CAD. Voici un exemple :

```java

import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, détaillons le processus de **comment exporter des fichiers CAD** en étapes faciles à gérer.

## Guide étape par étape

### Étape 1 : Charger le dessin CAD

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String sourceFilePath = dataDir + "sample.dwg";
Image objImage = Image.load(sourceFilePath);
```

Nous chargeons le fichier DWG source dans un objet `Image`, qui sert de point d’entrée pour toutes les opérations suivantes.

### Étape 2 : Créer `BmpOptions`

```java
BmpOptions bmpOptions = new BmpOptions();
```

`BmpOptions` contiendra les paramètres de rasterisation spécifiques à la sortie BMP.

### Étape 3 : Configurer les paramètres de rasterisation

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

Ici nous associons les options de rasterisation aux options BMP, ce qui nous permet de contrôler la façon dont les entités CAD sont rendues.

### Étape 4 : Définir la (les) mise(s) en page à exporter

```java
cadRasterizationOptions.setLayouts(new String[]{"Model"});
```

La propriété `Layouts` indique à Aspose.CAD quelles mises en page du dessin inclure. Dans la plupart des cas, `"Model"` est la mise en page principale que vous souhaitez convertir.

### Étape 5 : Exporter au format BMP

```java
String outPath = sourceFilePath + ".bmp";
objImage.save(outPath, bmpOptions);
```

L’appel à `save` avec les `BmpOptions` configurées écrit le fichier BMP sur le disque. Cela complète le flux de travail **convert DWG to BMP**.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| L’image de sortie est vide | Nom de mise en page incorrect ou mise en page manquante | Vérifiez que le nom de la mise en page correspond au fichier CAD (par ex., `"Model"`). |
| Résolution faible | DPI par défaut trop bas | Définissez `cadRasterizationOptions.setResolution(300);` avant d’enregistrer. |
| Erreur de mémoire insuffisante pour les gros fichiers | Les dessins volumineux nécessitent plus de heap | Augmentez la taille du heap JVM (`-Xmx2g`) ou traitez les pages individuellement. |

## Questions fréquemment posées

**Q : Aspose.CAD est‑il compatible avec différents formats de fichiers CAD ?**  
R : Oui, Aspose.CAD prend en charge DWG, DXF, DGN et de nombreux autres formats.

**Q : Puis‑je utiliser Aspose.CAD pour des projets commerciaux ?**  
R : Absolument. Achetez une licence [ici](https://purchase.aspose.com/buy) pour une utilisation en production.

**Q : Comment obtenir une licence temporaire pour les tests ?**  
R : Vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je trouver du support communautaire ?**  
R : Rejoignez le forum communautaire Aspose.CAD à l’adresse [forum](https://forum.aspose.com/c/cad/19).

**Q : Existe‑t‑il un essai gratuit d’Aspose.CAD pour Java ?**  
R : Oui, téléchargez l’essai gratuit [ici](https://releases.aspose.com/).

## Conclusion

Dans ce guide, nous avons démontré **comment exporter des fichiers CAD** depuis Java et **convert DWG to BMP** en utilisant Aspose.CAD. En suivant les cinq étapes ci‑dessus, vous pouvez intégrer la conversion CAD‑vers‑image dans n’importe quelle application Java, qu’il s’agisse d’un outil de bureau, d’un service web ou d’un pipeline de traitement par lots. Explorez d’autres formats de sortie (PNG, JPEG, PDF) en changeant simplement la classe d’options, et profitez de l’ensemble riche de fonctionnalités d’Aspose.CAD pour répondre à tous vos besoins de manipulation CAD.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}