---
date: 2026-03-05
description: Apprenez à exporter des fichiers dwg en pdf, activer les lignes cachées
  et convertir des DWG en PDF avec Aspose.CAD pour Java dans ce tutoriel étape par
  étape.
linktitle: Export DWG as PDF Using Java
second_title: Aspose.CAD Java API
title: Exporter DWG en PDF avec lignes cachées – Aspose.CAD pour Java
url: /fr/java/cad-text-and-formatting/support-hidden-lines-in-dwg/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export DWG vers PDF avec lignes cachées – Aspose.CAD for Java

## Introduction

Dans ce tutoriel, vous apprendrez comment **exporter dwg vers pdf** tout en conservant les lignes cachées à l’aide d’Aspose.CAD for Java. Que vous ayez besoin de **convertir DWG en PDF**, de créer un guide de type **dwg to pdf tutorial**, ou simplement de **sauvegarder DWG en PDF** avec prise en charge des lignes cachées, nous vous guiderons à chaque étape. À la fin, vous disposerez d’une solution prête à l’emploi que vous pourrez intégrer à n’importe quel projet Java.

## Quick Answers
- **Que couvre ce tutoriel ?** Activation du rendu des lignes cachées lors de l’exportation de DWG vers PDF avec Aspose.CAD for Java.  
- **Quelle opération principale est effectuée ?** `export dwg to pdf`.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise en production.  
- **Quelles sont les prérequis ?** Environnement de développement Java, bibliothèque Aspose.CAD for Java et fichiers DWG.  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour une configuration de base.

## Qu’est‑ce que “export dwg to pdf” ?
Exporter un fichier DWG vers PDF convertit le dessin CAD vectoriel en format de document portable tout en conservant les calques, les types de ligne et le rendu optionnel des lignes cachées. Cela facilite le partage des conceptions CAD avec des parties prenantes qui ne possèdent pas de logiciel CAD.

## Comment activer les lignes cachées lors de l’exportation DWG vers PDF
Les lignes cachées sont contrôlées via le paramètre de mise en page dans les options de rasterisation. En sélectionnant la mise en page **Model**, Aspose.CAD indique au moteur de rendu de traiter les arêtes cachées comme invisibles, vous offrant ainsi une représentation 2‑D nette d’un modèle 3‑D.

## Pourquoi activer les lignes cachées lors de l’exportation ?
Les lignes cachées offrent une représentation visuelle plus claire des modèles 3‑D complexes sur une page 2‑D, en ne mettant en évidence que les arêtes visibles. Cela améliore la lisibilité et est souvent requis pour la documentation d’ingénierie.

## Prérequis

1. **Aspose.CAD for Java** – téléchargez la bibliothèque depuis le site officiel [ici](https://releases.aspose.com/cad/java/).  
2. **Fichiers DWG** – disposez des dessins DWG sources stockés dans un répertoire connu.  
3. **Environnement de développement Java** – JDK 8+ et votre IDE préféré (Eclipse, IntelliJ, etc.).  

Une fois que tout est prêt, passons au code.

## Import Namespaces

Commencez par importer les classes nécessaires afin de travailler avec les images CAD et les options PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;
```

## Étape 1 : Configurer votre projet

Créez un projet Java et ajoutez le JAR Aspose.CAD à votre chemin de construction. Puis définissez le répertoire contenant vos fichiers DWG.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

> **Astuce :** Utilisez un chemin absolu ou configurez un chemin relatif basé sur le dossier des ressources de votre projet.

## Étape 2 : Charger le fichier DWG

Chargez le fichier DWG source dans un objet `CadImage` afin de pouvoir le manipuler.

```java
String sourceFilePath = dataDir + "Bottom_plate.dwg";
String outPath = dataDir + "Bottom_plate.pdf";
CadImage cadImage = (CadImage)Image.load(sourceFilePath);
```

## Étape 3 : Configurer les options de rasterisation

Sélectionnez les calques que vous souhaitez inclure et définissez la taille de page pour correspondre au dessin original. C’est ici que nous activons le rendu des lignes cachées en spécifiant la mise en page.

```java
List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageHeight(cadImage.getHeight());
rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
rasterizationOptions.setLayers(list);
```

## Étape 4 : Définir les options PDF

Indiquez à Aspose.CAD de rasteriser les données vectorielles dans un PDF, en utilisant la mise en page “Model” pour garder les lignes cachées invisibles.

```java
PdfOptions pdfOptions = new PdfOptions();
rasterizationOptions.setLayouts(new String[] { "Model" });
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 5 : Enregistrer le résultat

Enfin, exportez le DWG en fichier PDF. Les lignes cachées seront respectées selon la mise en page que vous avez définie.

```java
cadImage.save(outPath, pdfOptions);
System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
```

> **Erreur fréquente :** Oublier de définir la mise en page sur `"Model"` fera apparaître toutes les lignes (y compris les cachées) en plein trait dans le PDF.

## Problèmes courants et solutions

| Problème | Pourquoi cela se produit | Comment corriger |
|----------|--------------------------|------------------|
| Le PDF montre toutes les lignes en plein trait | Mise en page non définie sur **Model** | Assurez‑vous d’appeler `rasterizationOptions.setLayouts(new String[] { "Model" });` avant l’enregistrement. |
| Calques manquants dans la sortie | Noms de calques incorrects | Vérifiez les noms de calques dans le fichier DWG et faites‑les correspondre exactement dans la `list`. |
| Erreur de mémoire insuffisante sur les gros fichiers | Taille de rasterisation trop grande | Réduisez les dimensions de la page ou traitez le dessin par morceaux si possible. |

## Questions fréquentes

### Q1 : Puis‑je utiliser Aspose.CAD for Java avec d’autres formats de fichiers CAD ?
R1 : Oui, Aspose.CAD prend en charge divers formats CAD tels que DWG, DXF, DWF, et plus encore.

### Q2 : Existe‑t‑il un essai gratuit pour Aspose.CAD for Java ?
R2 : Oui, vous pouvez obtenir l’essai gratuit [ici](https://releases.aspose.com/).

### Q3 : Comment obtenir du support pour Aspose.CAD for Java ?
R3 : Visitez le forum Aspose.CAD [ici](https://forum.aspose.com/c/cad/19) pour le support communautaire.

### Q4 : Où trouver la documentation détaillée d’Aspose.CAD for Java ?
R4 : Consultez la documentation [ici](https://reference.aspose.com/cad/java/).

### Q5 : Puis‑je acheter une licence temporaire pour Aspose.CAD for Java ?
R5 : Oui, vous pouvez obtenir une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

### Q6 : Cette méthode fonctionne‑t‑elle également pour convertir DWG en PDF dans un environnement serveur sans interface graphique ?
R6 : Absolument. Comme le code utilise uniquement l’API Aspose.CAD, il s’exécute sans dépendances UI, ce qui le rend idéal pour l’automatisation côté serveur.

## Conclusion

Vous disposez maintenant d’une méthode complète, prête pour la production, afin d’**exporter dwg vers pdf** avec prise en charge des lignes cachées grâce à Aspose.CAD for Java. Cette approche peut être intégrée à des outils de traitement par lots, des services web ou des applications de bureau pour automatiser la conversion CAD‑vers‑PDF.

---

**Dernière mise à jour :** 2026-03-05  
**Testé avec :** Aspose.CAD for Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}