---
date: 2026-03-02
description: Débloquez le potentiel d'Aspose.CAD pour Java. Exportez facilement les
  objets OLE et **enregistrez le CAD au format PNG**. Téléchargez dès maintenant pour
  une gestion fluide des données CAD.
linktitle: Export OLE Objects from CAD
second_title: Aspose.CAD Java API
title: Enregistrer le CAD au format PNG – Exporter les objets OLE à l'aide d'Aspose.CAD
  pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/export-ole-objects-from-cad/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Enregistrer CAD en PNG – Exporter des objets OLE avec Aspose.CAD pour Java

## Introduction

Dans le monde dynamique de la Conception Assistée par Ordinateur (CAD), gérer et extraire les objets OLE (Object Linking and Embedding) de manière efficace—et pouvoir **enregistrer CAD en PNG**—est essentiel pour les flux de travail en aval tels que les rapports, l’aperçu web ou l’archivage. Aspose.CAD pour Java offre une solution puissante, orientée code, qui vous permet à la fois d’exporter les objets OLE et de convertir les dessins CAD en images PNG de haute qualité en quelques lignes de code.

## Quick Answers
- **Que fait Aspose.CAD ?** Il lit, manipule et convertit les fichiers CAD (DWG, DXF, DGN, etc.) sans nécessiter de logiciel CAD natif.  
- **Puis-je enregistrer CAD en PNG ?** Oui—utilisez `PngOptions` avec `CadRasterizationOptions` pour rasteriser n’importe quelle mise en page.  
- **Comment exporter les objets OLE ?** Chargez le fichier CAD avec `Image.load` et enregistrez chaque mise en page contenant des OLE au format PNG.  
- **Ai-je besoin d’une licence ?** Un essai gratuit est disponible ; une licence commerciale supprime les limitations d’évaluation.  
- **Quelle version de Java est requise ?** Java 8 ou supérieur est entièrement pris en charge.

## Qu’est‑ce que **enregistrer CAD en PNG** ?
Enregistrer CAD en PNG signifie rasteriser les dessins CAD basés sur des vecteurs en une image PNG basée sur des pixels. Cette conversion est utile lorsque vous avez besoin d’un format léger et universellement affichable pour les pages web, les applications mobiles ou la documentation.

## Pourquoi utiliser Aspose.CAD pour Java pour **convertir CAD en PNG** ?
- **Aucune installation CAD requise** – la bibliothèque fonctionne entièrement en Java.  
- **Préserve la fidélité de la mise en page** – vous pouvez choisir des mises en page spécifiques, contrôler le DPI et conserver la qualité des lignes.  
- **Traitement par lots** – parcourez plusieurs fichiers avec une boucle simple.  
- **Exporter les objets OLE** – le contenu OLE intégré dans les fichiers DWG/DXF est automatiquement rendu dans la sortie PNG.

## Prerequisites

- **Environnement Java** – assurez‑vous d’avoir un environnement de développement Java configuré sur votre machine.  
- **Aspose.CAD pour Java** – téléchargez et installez la bibliothèque Aspose.CAD pour Java. Vous pouvez trouver la bibliothèque au [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Fichiers CAD** – préparez les fichiers CAD contenant les objets OLE que vous souhaitez exporter.

## Import Namespaces

Pour commencer, importez les espaces de noms nécessaires dans votre projet Java. Ces espaces de noms fournissent les classes et fonctionnalités essentielles requises pour travailler avec des fichiers CAD à l’aide d’Aspose.CAD.

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

Maintenant, détaillons le processus d’exportation des objets OLE depuis CAD en plusieurs étapes :

## Comment **enregistrer CAD en PNG** et exporter des objets OLE

### Étape 1 : Définir votre répertoire de documents

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

Assurez‑vous de remplacer `"Your Document Directory"` par le chemin du répertoire contenant vos fichiers CAD.

### Étape 2 : Définir les noms de fichiers CAD

```java
String[] files = new String[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

Spécifiez les noms des fichiers CAD que vous souhaitez traiter dans le tableau `files`.

### Étape 3 : Configurer les options d’exportation PNG

```java
PngOptions pngOptions = new PngOptions();
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.setVectorRasterizationOptions(rasterizationOptions);
rasterizationOptions.setLayouts(new String[] { "Layout1" });
```

Configurez les options d’exportation PNG, y compris la rasterisation vectorielle et les paramètres de mise en page. Ces options permettent de **convertir CAD en PNG** avec la qualité souhaitée.

### Étape 4 : Parcourir les fichiers CAD

```java
for(String file : files)
{
    CadImage cadImage = (CadImage)Image.load(dataDir + file);
    cadImage.save(dataDir + file + "_out.png", pngOptions);
}
```

Parcourez chaque fichier CAD spécifié, chargez‑le avec Aspose.CAD et enregistrez les objets OLE sous forme d’images PNG. Cette boucle montre une façon simple de **convertir DWG en PNG** en masse.

## Common Issues and Solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **Sortie PNG vide** | Mauvais nom de mise en page | Vérifiez que le nom de mise en page (`"Layout1"`) existe dans le DWG source. |
| **Graphiques OLE manquants** | Les objets OLE sont stockés dans une mise en page différente | Incluez toutes les mises en page pertinentes dans `rasterizationOptions.setLayouts(...)`. |
| **Erreur de mémoire insuffisante sur les gros fichiers** | Paramètres DPI élevés | Réduisez le DPI via `rasterizationOptions.setResolution(...)` ou traitez les fichiers un par un. |

## Frequently Asked Questions

**Q : Aspose.CAD est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Aspose.CAD prend en charge divers formats CAD, y compris DWG, DXF et DGN. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour la liste complète.

**Q : Puis‑je personnaliser les paramètres d’exportation pour les objets OLE ?**  
R : Oui, Aspose.CAD offre de nombreuses options pour personnaliser les paramètres d’exportation, vous permettant d’adapter la sortie à vos exigences spécifiques.

**Q : Existe‑t‑il un essai gratuit pour Aspose.CAD ?**  
R : Oui, vous pouvez explorer les capacités d’Aspose.CAD en obtenant un essai gratuit [ici](https://releases.aspose.com/).

**Q : Où puis‑je obtenir du support communautaire pour Aspose.CAD ?**  
R : Rejoignez la communauté Aspose.CAD sur le [forum](https://forum.aspose.com/c/cad/19) pour demander de l’aide et partager vos expériences.

**Q : Comment puis‑je acheter une licence pour Aspose.CAD ?**  
R : Visitez la [page d’achat](https://purchase.aspose.com/buy) pour acquérir une licence adaptée à vos besoins de développement.

## Conclusion

Avec ces étapes simples mais puissantes, vous pouvez facilement **enregistrer CAD en PNG** tout en exportant les objets OLE des fichiers CAD à l’aide d’Aspose.CAD pour Java. Cet outil polyvalent permet aux développeurs de gérer les données CAD efficacement, ouvrant de nouvelles possibilités dans le développement d’applications CAD et les flux de travail en aval basés sur des images.

---

**Last Updated:** 2026-03-02  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}