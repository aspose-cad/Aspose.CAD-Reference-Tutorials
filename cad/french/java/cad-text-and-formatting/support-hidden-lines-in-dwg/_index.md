---
date: 2026-01-02
description: Apprenez à exporter DWG en PDF, activer les lignes cachées et convertir
  DWG en PDF avec Aspose.CAD pour Java dans ce tutoriel étape par étape.
linktitle: Export DWG as PDF with Hidden Lines Using Java
second_title: Aspose.CAD Java API
title: Exporter DWG en PDF avec lignes cachées – Aspose.CAD pour Java
url: /fr/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportateur DWG en PDF avec lignes cachées – Aspose.CAD pour Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **exporter DWG en PDF** tout en préservant les lignes cachées à l’aide d’Aspose.CAD for Java. Que vous ayez besoin de **convertir DWG en PDF**, de créer un guide de type **dwg to pdf tutoriel**, ou simplement de **sauvegarder DWG en PDF** avec prise en charge des lignes cachées, nous vous accompagnerons étape par étape. À la fin, vous disposez d’une solution prête à l’emploi que vous pourrez intégrer à n’importe quel projet Java.

## Réponses rapides
- **Que couvre ce tutoriel ?** Activation du rendu des lignes cachées lors de l’exportation de DWG en PDF avec Aspose.CAD pour Java.
- **Quelle opération principale est effectuée ?** `exporter le fichier DWG au format PDF`.
- **Dois-je avoir une licence ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production.
- **Quels sont les prérequis ?** Environnement de développement Java, bibliothèque Aspose.CAD for Java et fichiers DWG.
- **Combien de temps prend la mise en œuvre ?** Environ 10 à 15 minutes pour une configuration de base.

## Qu'est-ce que « exporter un fichier DWG au format PDF » ?
Exporter un fichier DWG en PDF convertit le dessin CAD vectoriel en format de document portable tout en conservant les calques, les types de lignes et, éventuellement, le rendu des lignes cachées. Cela facilite le partage des conceptions CAD avec des parties qui ne disposent pas de logiciel CAD.

## Pourquoi activer les lignes cachées lors de l'exportation ?
Les lignes cachées offrent une représentation visuelle plus claire des modèles 3D complexes sur une page 2D, en veillant à ce que seules les arêtes visibles soient mises en avant. Cela améliore la lisibilité et est souvent exigé pour la documentation d’ingénierie.

## Prérequis

1. **Aspose.CAD for Java** – téléchargez la bibliothèque depuis le site officiel [ici](https://releases.aspose.com/cad/java/).
2. **Fichiers DWG** – obtenez des dessins DWG sources stockés dans un répertoire connu.
3. **Environnement de développement Java** – JDK8+ et votre IDE préféré (Eclipse, IntelliJ, etc.).

Maintenant que tout est prêt, passe au code.

## Importer des espaces de noms

Commencez par importer les classes nécessaires afin de travailler avec les images CAD et les options PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Étape 1 : Configurez votre projet

Créez un projet Java et ajoutez le JAR Aspose.CAD à votre chemin de construction. Puis définissez le répertoire contenant vos fichiers DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Conseil de pro :** Utilisez un chemin absolu ou configurez un chemin relatif basé sur le dossier des ressources de votre projet.

## Étape 2 : Charger le fichier DWG

Chargez le fichier DWG source dans un objet `CadImage` afin de pouvoir le manipuler.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Étape 3 : Configurer les options de rastérisation

Sélectionnez les calques à inclure et définissez la taille de page pour correspondre au dessin original. C’est ici que nous activons le rendu des lignes cachées en spécifiant la mise en page.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Étape 4 : Définir les options PDF

Indiquez à Aspose.CAD de rasteriser les données vectorielles dans un PDF, en utilisant la mise en page « Model » pour garder les lignes cachées invisibles.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 5 : Enregistrez le résultat

Enfin, exportez le DWG en fichier PDF. Les lignes cachées seront respectées selon la mise en page que vous avez définie.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Piège commun :** Oublier de définir la mise en page sur `"Model"` entraînera l’affichage de toutes les lignes (y compris les caméras) en traits pleins dans le PDF.

## Conclusion

Vous disposez maintenant d’une méthode complète, prête pour la production, afin de **exporter DWG en PDF** avec prise en charge des lignes cachées en utilisant Aspose.CAD pour Java. Cette approche peut être intégrée à des outils de traitement par lots, des services web ou des applications de bureau pour automatiser la conversion CAD‑vers‑PDF.

## Questions fréquemment posées

### Q1 : Puis-je utiliser Aspose.CAD pour Java avec d'autres formats de fichiers CAO ?
R1 : Oui, Aspose.CAD prend en charge divers formats CAO tels que DWG, DXF, DWF, et plus encore.

### Q2 : Existe-t-il un essai gratuit disponible pour Aspose.CAD pour Java ?
A2 : Oui, vous pouvez trouver l’essai gratuit [ici](https://releases.aspose.com/).

### Q3 : Comment puis-je obtenir du support pour Aspose.CAD pour Java ?
A3 : Visitez le forum Aspose.CAD [ici](https://forum.aspose.com/c/cad/19) pour obtenir de l’aide communautaire.

### Q4 : Où puis-je trouver une documentation détaillée pour Aspose.CAD pour Java ?
A4 : Consultez la documentation [ici](https://reference.aspose.com/cad/java/).

### Q5 : Puis-je acheter une licence temporaire pour Aspose.CAD pour Java ?
A5 : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q6 : Cette méthode fonctionne-t-elle également pour convertir des fichiers DWG en PDF dans un environnement de serveur sans tête ?
R6 : Absolument. Puisque le code utilise uniquement l’API Aspose.CAD, il s’exécute sans aucune dépendance UI, ce qui le rend idéal pour l’automatisation côté serveur.

---

**Dernière mise à jour :** 2026-01-02
**Testé avec :** Aspose.CAD pour Java 24.12
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}