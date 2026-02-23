---
date: 2026-02-23
description: Apprenez à convertir DWFX en PDF et à enregistrer les fichiers CAD au
  format PDF à l'aide d'Aspose.CAD pour Java. Guide rapide pour ouvrir les fichiers
  DWFX et générer des PDF.
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
title: Convertir DWFX en PDF avec Aspose.CAD pour Java
url: /fr/java/cad-file-manipulation/open-dwfx-file/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWFX en PDF avec Aspose.CAD pour Java

## Introduction

Dans le monde du design en évolution rapide d’aujourd’hui, les développeurs ont souvent besoin de **convertir DWFX en PDF** afin que les dessins CAD puissent être partagés avec des parties prenantes non techniques. Aspose.CAD pour Java rend cette tâche simple, vous permettant d’ouvrir un fichier DWFX, de le rasteriser, et de **sauvegarder le CAD en PDF** avec seulement quelques lignes de code. Dans ce tutoriel, nous parcourrons l’ensemble du processus — de la configuration de votre environnement à la vérification du PDF final — afin que vous puissiez gérer les fichiers DWFX en toute confiance dans vos applications Java.

## Réponses rapides
- **Quel est le but principal de ce guide ?** Montrer comment convertir DWFX en PDF en utilisant Aspose.CAD pour Java.  
- **Quelle bibliothèque est requise ?** Aspose.CAD pour Java (téléchargement depuis le site officiel d’Aspose).  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Puis‑je ouvrir les fichiers DWFX directement ?** Oui, utilisez `Image.load` pour ouvrir les fichiers DWFX.  
- **Quel format de sortie l’exemple produit‑il ?** Un fichier PDF enregistré dans le répertoire de sortie spécifié.

## Qu’est‑ce que la « convertir DWFX en PDF » ?

Convertir DWFX en PDF signifie prendre un dessin DWFX basé sur des vecteurs — couramment utilisé dans les produits Autodesk — et le rendre sous forme de document PDF portable et largement supporté. Cela permet une visualisation, une impression et un partage faciles sans nécessiter de logiciel CAD du côté du destinataire.

## Pourquoi utiliser Aspose.CAD pour Java pour **sauvegarder le CAD en PDF** ?

- **Aucune dépendance externe :** API pure Java, aucune nécessité d’un moteur CAD natif.  
- **Rendu haute fidélité :** Préserve les épaisseurs de ligne, les couleurs et les calques.  
- **Adapté au traitement par lots :** Idéal pour l’automatisation côté serveur ou les services cloud.  
- **Multiplateforme :** Fonctionne sous Windows, Linux et macOS.

## Prérequis

Avant de plonger dans le code, assurez‑vous de disposer de ce qui suit :

- **Aspose.CAD pour Java Library** – Téléchargez‑la depuis la [page de téléchargement d’Aspose.CAD pour Java](https://releases.aspose.com/cad/java/).  
- **Environnement de développement Java** – JDK 8 ou supérieur, avec votre IDE ou outil de construction préféré.  
- **Fichier DWFX** – Un fichier DWFX d’exemple (par ex., `Tyrannosaurus.dwfx`) pour tester la conversion.

## Importer les espaces de noms

Tout d’abord, importez les classes dont nous aurons besoin :

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Comment convertir DWFX en PDF avec Aspose.CAD pour Java

Ci‑dessous, un découpage étape par étape. Chaque étape comprend une courte explication suivie du code exact à exécuter.

### Étape 1 : Charger le fichier DWFX  

```java
String SourceDir = Utils.getDataDir_DWFXDrawings();
String OutputDir = Utils.getDataDir_Output();
String filePath = SourceDir + "Tyrannosaurus.dwfx";

Image cadImageDwf = Image.load(filePath);
```

La méthode `Image.load` lit le fichier DWFX en mémoire, nous fournissant un objet `CadImage` prêt pour la rasterisation.

### Étape 2 : Définir les options de rasterisation  

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());
```

Ces options définissent la taille de la page de sortie, garantissant que le PDF correspond aux dimensions du dessin original.

### Étape 3 : Configurer les options PDF  

```java
PdfOptions CADf = new PdfOptions();
CADf.setVectorRasterizationOptions(rasterizationOptions);
```

Ici, nous associons les paramètres de rasterisation à la configuration d’exportation PDF.

### Étape 4 : Enregistrer en PDF  

```java
cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
```

L’appel à `save` écrit l’image rendue dans un fichier PDF dans le dossier de sortie.

### Étape 5 : Vérifier le succès  

```java
System.out.println("OpenDwfxFile executed successfully");
```

Un simple message console confirme que la conversion s’est terminée sans erreurs.

## Problèmes courants et solutions

| Problème | Cause probable | Solution |
|----------|----------------|----------|
| **Sortie PDF vide** | Largeur/hauteur de rasterisation définie à 0 | Assurez‑vous que `cadImageDwf.getSize()` renvoie des dimensions valides avant de définir les options. |
| **Erreur de mémoire insuffisante** | Fichier DWFX très volumineux | Augmentez la taille du tas JVM (`-Xmx2g`) ou traitez le fichier par sections plus petites. |
| **Polices manquantes** | Police non intégrée dans le DWFX source | Installez les polices requises sur le serveur ou utilisez `CadRasterizationOptions.setFontName` pour spécifier une police de secours. |

## Questions fréquemment posées

### Q1 : Puis‑je utiliser Aspose.CAD pour Java avec d’autres formats de fichiers CAD ?  
R1 : Oui, Aspose.CAD pour Java prend en charge un large éventail de formats CAD, offrant une solution polyvalente aux développeurs.

### Q2 : Un essai gratuit est‑il disponible pour Aspose.CAD pour Java ?  
R2 : Oui, vous pouvez explorer les capacités d’Aspose.CAD pour Java avec un essai gratuit. Visitez [ce lien](https://releases.aspose.com/) pour commencer.

### Q3 : Comment obtenir du support pour Aspose.CAD pour Java ?  
R3 : Rejoignez la communauté Aspose.CAD sur le [forum de support](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide et collaborer.

### Q4 : Des licences temporaires sont‑elles disponibles pour Aspose.CAD pour Java ?  
R4 : Oui, vous pouvez obtenir une licence temporaire pour Aspose.CAD pour Java. Visitez [ce lien](https://purchase.aspose.com/temporary-license/) pour plus de détails.

### Q5 : Où puis‑je trouver la documentation d’Aspose.CAD pour Java ?  
R5 : La documentation complète est disponible [ici](https://reference.aspose.com/cad/java/).

---

**Dernière mise à jour :** 2026-02-23  
**Testé avec :** Aspose.CAD pour Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}