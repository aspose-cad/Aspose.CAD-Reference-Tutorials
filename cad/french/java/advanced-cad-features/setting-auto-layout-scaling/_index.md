---
date: 2025-12-10
description: Apprenez à créer un PDF à partir de CAD en utilisant Aspose.CAD pour
  Java avec le redimensionnement automatique de la mise en page. Ce guide étape par
  étape vous montre comment exporter le CAD vers PDF de manière efficace et fiable.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Créer un PDF à partir de CAD – Mise à l’échelle automatique de la mise en page
  avec Aspose.CAD Java
url: /fr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Créer un PDF à partir de CAD – Redimensionnement automatique de la mise en page avec Aspose.CAD Java

## Introduction

Si vous devez **créer un PDF à partir de fichiers CAD** rapidement et avec un redimensionnement parfait, Aspose.CAD pour Java répond à vos besoins. Le redimensionnement automatique de la mise en page ajuste automatiquement les dimensions de la mise en page afin que le PDF résultant apparaisse exactement comme prévu, quelle que soit la taille de la page CAD d'origine. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d'un fichier DXF à l'exportation d'un PDF — tout en mettant en avant les capacités **d'exportation CAD vers PDF** de la bibliothèque.

## Réponses rapides
- **Que fait le redimensionnement automatique de la mise en page ?** Il redimensionne automatiquement les mises en page CAD pour qu'elles s'adaptent aux dimensions de la page cible lors de la rasterisation.
- **Quels formats puis‑je convertir ?** Tout format pris en charge par Aspose.CAD (par ex., DXF, DWG, DWF) peut être converti en PDF.
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale est requise pour une utilisation autre que d'évaluation.
- **Combien de temps prend la conversion ?** Généralement moins d'une seconde pour les fichiers standards sur du matériel moderne.
- **Puis‑je changer la taille de la page ?** Oui, vous pouvez définir des dimensions de page personnalisées via `CadRasterizationOptions`.

## Qu’est‑ce que « créer un PDF à partir de CAD » ?
Créer un PDF à partir de CAD consiste à prendre un dessin d’ingénierie vectoriel (DXF, DWG, etc.) et à le rasteriser dans un document PDF. Le PDF conserve la fidélité visuelle du dessin original tout en étant largement visualisable sur n’importe quelle plateforme.

## Pourquoi utiliser le redimensionnement automatique de la mise en page ?
- **Sortie cohérente :** Garantit que toutes les mises en page remplissent la page PDF sans calculs manuels de taille.
- **Gain de temps :** Élimine le besoin d’ajuster manuellement les facteurs de mise à l’échelle pour chaque dessin.
- **Haute qualité :** Maintient le poids des lignes et la précision géométrique pendant la conversion.

## Prérequis

1. **Bibliothèque Aspose.CAD pour Java** – téléchargez la dernière version depuis la [page de téléchargement](https://releases.aspose.com/cad/java/).  
2. **Répertoire de ressources** – créez un dossier sur votre machine pour stocker les fichiers CAD ; remplacez `"Your Document Directory"` dans le code par ce chemin.  
3. **Fichier CAD d’exemple** – pour ce guide, nous utiliserons `conic_pyramid.dxf`, inclus dans le jeu de données d’exemple Aspose.

## Importer les espaces de noms

Tout d'abord, importez les classes requises. Cela nous donne accès aux fonctions de chargement d’image, de rasterisation et d’exportation PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Étape 1 : Charger le fichier CAD

Le chargement du fichier source est la première étape de **comment exporter CAD** vers un document PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

## Étape 2 : Créer les options de rasterisation

Définissez les dimensions de la page cible. Vous pouvez également utiliser ce bloc pour **définir manuellement la taille de la page CAD** si vous préférez une mise en page personnalisée.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

## Étape 3 : Activer le redimensionnement automatique de la mise en page

Activez la fonctionnalité de mise à l’échelle automatique. C’est le cœur de **comment définir la mise à l’échelle** pour une conversion CAD‑vers‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

## Étape 4 : Créer les options PDF

Liez les paramètres de rasterisation aux options d’exportation PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

## Étape 5 : Exporter vers PDF

Enfin, enregistrez l’image rendue sous forme de fichier PDF. Cette étape finalise le flux de travail **convertir DXF en PDF**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Répétez les étapes ci‑dessus pour tout fichier CAD supplémentaire que vous devez traiter.

## Problèmes courants & Dépannage

| Symptôme | Cause probable | Solution |
|----------|----------------|----------|
| PDF vide en sortie | Options de rasterisation non définies ou chemin de fichier incorrect | Vérifiez le chemin `srcFile` et assurez‑vous que `setPageWidth/Height` ne sont pas à zéro |
| Mise à l’échelle déformée | `setAutomaticLayoutsScaling` laissé à `false` | Activez le redimensionnement automatique ou calculez manuellement le facteur de mise à l’échelle |
| Couches manquantes | Le DXF source contient des entités non prises en charge | Consultez les notes de version d’Aspose.CAD pour les types d’entités supportés |

## FAQ

### Q1 : Aspose.CAD pour Java est‑il compatible avec tous les formats de fichiers CAD ?

R1 : Aspose.CAD pour Java prend en charge divers formats CAD, notamment DWG, DXF et DWF.

### Q2 : Puis‑je personnaliser davantage les options de mise à l’échelle ?

R2 : Oui, la classe `CadRasterizationOptions` offre plusieurs propriétés pour affiner la mise à l’échelle et d’autres paramètres.

### Q3 : Où puis‑je trouver une documentation supplémentaire pour Aspose.CAD pour Java ?

R3 : Consultez la [documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées et des exemples.

### Q4 : Existe‑t‑il un essai gratuit pour Aspose.CAD pour Java ?

R4 : Oui, vous pouvez explorer un [essai gratuit](https://releases.aspose.com/) pour découvrir les capacités d’Aspose.CAD pour Java.

### Q5 : Comment puis‑je obtenir de l’aide ou participer aux discussions sur Aspose.CAD pour Java ?

R5 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour rejoindre la communauté et demander du support.

**Questions supplémentaires fréquentes**

**Q : Comment convertir un fichier DWG en PDF au lieu de DXF ?**  
R : Le même code fonctionne ; il suffit de changer l’extension du fichier dans `srcFile` en `.dwg`.

**Q : Puis‑je définir un DPI personnalisé pour des PDF à plus haute résolution ?**  
R : Oui, utilisez `rasterizationOptions.setResolution(300);` (ou tout DPI dont vous avez besoin).

**Q : Est‑il possible d’incorporer des polices dans le PDF généré ?**  
R : Aspose.CAD rasterise le dessin, les polices sont donc rendues comme vecteurs ; aucune incorporation de police séparée n’est requise.

## Conclusion

En suivant ce guide, vous savez maintenant comment **créer un PDF à partir de fichiers CAD** en utilisant Aspose.CAD pour Java avec le redimensionnement automatique de la mise en page. Le processus rationalise le flux de travail **d'exportation CAD vers PDF**, assure une mise à l’échelle cohérente et vous fait gagner un temps précieux de développement. N’hésitez pas à expérimenter avec différentes tailles de page, résolutions et formats CAD pour répondre aux besoins de votre projet.

---

**Dernière mise à jour :** 2025-12-10  
**Testé avec :** Aspose.CAD pour Java 24.12 (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}