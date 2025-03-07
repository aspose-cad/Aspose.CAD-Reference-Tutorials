---
title: Ajustement de la taille du dessin CAO à l'aide du type d'unité avec Aspose.CAD pour Java
linktitle: Ajustement de la taille du dessin CAO à l'aide du type d'unité
second_title: API Java Aspose.CAD
description: Découvrez la puissance d'Aspose.CAD pour Java pour ajuster facilement la taille des dessins CAO. Suivez notre guide étape par étape pour plus de précision et d’adaptabilité.
weight: 14
url: /fr/java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajustement de la taille du dessin CAO à l'aide du type d'unité avec Aspose.CAD pour Java

## Introduction

Dans le domaine en constante évolution de la conception assistée par ordinateur (CAO), la précision et l’adaptabilité sont primordiales. Une exigence courante consiste à ajuster la taille des dessins CAO en fonction de types d'unités spécifiques. Aspose.CAD pour Java apparaît comme un allié puissant, offrant des capacités transparentes pour manipuler les fichiers CAO par programme.

## Conditions préalables

Avant de plonger dans le didacticiel, assurez-vous que les conditions préalables suivantes sont remplies :

- Environnement de développement Java : assurez-vous que vous disposez d'un environnement de développement Java fonctionnel configuré sur votre ordinateur.

-  Bibliothèque Aspose.CAD pour Java : téléchargez et intégrez la bibliothèque Aspose.CAD dans votre projet Java. Vous pouvez obtenir la bibliothèque[ici](https://releases.aspose.com/cad/java/).

## Importer des espaces de noms

Dans votre code Java, incluez les espaces de noms nécessaires pour accéder aux fonctionnalités d'Aspose.CAD. Ajoutez les importations suivantes :

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, décomposons le processus d'ajustement de la taille du dessin CAO à l'aide du type d'unité en étapes gérables :

## Étape 1 : Définir le répertoire de données

```java
String dataDir = "Your Document Directory" + "CADConversion/";
```

Définissez le chemin du répertoire où se trouvent vos fichiers CAO.

## Étape 2 : Charger le dessin CAO

```java
String sourceFilePath = dataDir + "sample.dwg";
Image image = Image.load(sourceFilePath);
```

 Chargez le dessin CAO à l'aide d'Aspose.CAD`Image` classe.

## Étape 3 : Créer des options BMP

```java
BmpOptions bmpOptions = new BmpOptions();
```

 Instancier le`BmpOptions` classe pour exporter la mise en page CAO au format BMP.

## Étape 4 : configurer les options de rastérisation

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);
```

 Créer une instance de`CadRasterizationOptions` et l'associer au`BmpOptions` pour la rastérisation vectorielle.

## Étape 5 : Définir le type d'unité

```java
cadRasterizationOptions.setUnitType(UnitType.Centimeter);
```

Spécifiez le type d'unité souhaité pour le dessin CAO. Dans cet exemple, nous l'avons défini sur Centimètre.

## Étape 6 : Définir les mises en page

```java
cadRasterizationOptions.setLayouts(new String[] { "Model" });
```

Définissez les mises en page à prendre en compte lors de l'export. Dans ce cas, nous avons sélectionné la disposition "Modèle".

## Étape 7 : Exporter vers BMP

```java
String outPath = sourceFilePath + ".bmp";
image.save(outPath, bmpOptions);
```

Enfin, enregistrez le dessin CAO modifié au format BMP.

## Conclusion

Avec Aspose.CAD pour Java, ajuster la taille des dessins CAO devient un jeu d'enfant. Ce didacticiel vous a guidé tout au long du processus, en soulignant l'importance de chaque étape pour obtenir des résultats précis.

## FAQ

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d’autres langages de programmation ?

A1 : Aspose.CAD prend principalement en charge Java, mais des versions sont disponibles pour d'autres langages comme .NET.

### Q2 : Existe-t-il des options de licence pour Aspose.CAD ?

 A2 : Oui, vous pouvez explorer les options de licence et acheter Aspose.CAD[ici](https://purchase.aspose.com/buy).

### Q3 : Existe-t-il un essai gratuit disponible pour Aspose.CAD ?

 A3 : Bien sûr, vous pouvez accéder à un essai gratuit[ici](https://releases.aspose.com/).

### Q4 : Comment puis-je obtenir de l'assistance pour Aspose.CAD pour Java ?

 A4 : Visitez le forum Aspose.CAD[ici](https://forum.aspose.com/c/cad/19) pour un accompagnement complet.

### Q5 : Puis-je obtenir une licence temporaire pour Aspose.CAD ?

 A5 : Oui, vous pouvez acquérir une licence temporaire[ici](https://purchase.aspose.com/temporary-license/).
{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}
