---
date: 2025-12-28
description: Apprenez à créer un PDF à partir de DWG, à enregistrer un DWG en PDF
  et à ajouter du texte aux dessins DWG avec Aspose.CAD pour Java — guide étape par
  étape.
linktitle: Add Text in DWG
second_title: Aspose.CAD Java API
title: Créer un PDF à partir de DWG et ajouter du texte avec Aspose.CAD pour Java
url: /fr/java/cad-text-and-annotation/add-text-in-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un PDF à partir de DWG et ajouter du texte avec Aspose.CAD for Java

## Introduction

Si vous devez **créer un PDF à partir de DWG** tout en insérant du texte personnalisé, vous êtes au bon endroit. Dans ce tutoriel, nous parcourrons l’ensemble du processus : chargement d’un dessin DWG, ajout d’une annotation texte, puis enregistrement du résultat au format PDF à l’aide d’Aspose.CAD for Java. À la fin, vous comprendrez comment **enregistrer DWG en PDF**, personnaliser la hauteur du texte et même ajouter des annotations de base.

## Réponses rapides
- **Puis-je convertir DWG en PDF en Java ?** Oui, Aspose.CAD for Java fournit une API simple.  
- **Ai-je besoin d'une licence pour une utilisation en production ?** Une licence commerciale est requise ; un essai gratuit est disponible.  
- **Quelle méthode ajoute du texte à un DWG ?** Utilisez l'objet `CadText` et ajoutez-le à l'espace modèle.  
- **Puis-je définir la hauteur du texte ?** Absolument — utilisez `setTextHeight()` sur l'instance `CadText`.  
- **Le résultat est-il vectoriel ?** Lorsque les options de rasterisation sont définies sur `UseObjectColor`, le PDF conserve des données vectorielles de haute qualité.

## Prérequis

Avant de plonger dans le tutoriel, assurez‑vous d’avoir les prérequis suivants :

- Bibliothèque Aspose.CAD for Java : téléchargez et installez la bibliothèque depuis la [page Aspose.CAD for Java](https://releases.aspose.com/cad/java/).

- Java Development Kit (JDK) : assurez‑vous d’avoir le dernier JDK installé sur votre système.

- Dessin DWG : préparez un fichier de dessin DWG dans lequel vous souhaitez ajouter du texte.

## Importer les espaces de noms

Dans votre code Java, importez les espaces de noms nécessaires pour Aspose.CAD :

```java
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Maintenant, décomposons l'extrait de code fourni en plusieurs étapes :

## Étape 1 : Configurer le répertoire du document et le chemin du fichier DWG

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String dwgPathToFile = dataDir + "SimpleEntites.dwg";
```

## Étape 2 : Charger l'image DWG

```java
Image image = Image.load(dwgPathToFile);
```

## Étape 3 : Créer l'objet CadText (Ajouter du texte au DWG)

```java
CadText cadText = new CadText();
cadText.setStyleType("Standard");
cadText.setDefaultValue("Some custom text");
cadText.setColorId(256);
cadText.setLayerName("0");
cadText.getFirstAlignment().setX(47.9);
cadText.getFirstAlignment().setY(5.56);
cadText.setTextHeight(0.8);          // set text height in DWG units
cadText.setScaleX(0);
```

## Étape 4 : Ajouter du texte à CadImage (Insérer une annotation)

```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadText);
```

## Étape 5 : Configurer les options PDF (Préparer la création du PDF à partir du DWG)

```java
PdfOptions pdfOptions = new PdfOptions();
```

## Étape 6 : Configurer CadRasterizationOptions (Contrôler le rendu du PDF)

```java
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

## Étape 7 : Enregistrer le DWG modifié en PDF (dwg to pdf java)

```java
image.save(dataDir + "SimpleEntites_generated.dwg.pdf", pdfOptions);
```

En suivant ces étapes, vous pourrez **créer un PDF à partir de DWG**, ajouter du texte personnalisé et contrôler la hauteur du texte — le tout avec seulement quelques lignes de code Java.

## Pourquoi ajouter du texte à un DWG et le convertir en PDF ?

Ajouter du texte directement à un fichier DWG est utile pour :

- **Annoter les conceptions** avec des notes ou des numéros de pièce.
- **Créer une documentation imprimable** où le PDF sert de format en lecture seule, largement supporté.
- **Automatiser le traitement par lots** de grandes bibliothèques CAD sans édition manuelle.

## Problèmes courants et astuces

- **Le texte n'apparaît pas ?** Vérifiez que les coordonnées X/Y sont à l'intérieur des limites du dessin et que le calque est visible.
- **Hauteur du texte incorrecte ?** Ajustez `setTextHeight()` ; la valeur est dans le système d'unités du dessin.
- **Le PDF semble rasterisé ?** Assurez‑vous que `CadDrawTypeMode.UseObjectColor` est défini pour conserver les informations vectorielles.
- **Performance sur de gros fichiers ?** Augmentez `pageHeight`/`pageWidth` uniquement si nécessaire ; des valeurs plus grandes consomment plus de mémoire.

## Questions fréquentes

**Q : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?**  
R : Aspose.CAD prend en charge diverses versions de fichiers DWG, assurant la compatibilité avec un large éventail de logiciels CAD.

**Q : Puis‑je personnaliser la police et le formatage du texte ajouté ?**  
R : Oui, vous pouvez personnaliser la police, le style et d’autres options de formatage du texte ajouté aux fichiers DWG à l’aide d’Aspose.CAD.

**Q : Existe‑t‑il un essai gratuit pour Aspose.CAD for Java ?**  
R : Oui, vous pouvez explorer les fonctionnalités d’Aspose.CAD en obtenant un essai gratuit depuis [ici](https://releases.aspose.com/).

**Q : Où puis‑je trouver la documentation détaillée pour Aspose.CAD for Java ?**  
R : Consultez la documentation [ici](https://reference.aspose.com/cad/java/) pour des informations approfondies et des exemples.

**Q : Comment obtenir du support ou de l’aide avec Aspose.CAD ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour obtenir de l’assistance et rejoindre la communauté.

---

**Dernière mise à jour** : 2025-12-28  
**Testé avec** : Aspose.CAD for Java 24.12  
**Auteur** : Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}