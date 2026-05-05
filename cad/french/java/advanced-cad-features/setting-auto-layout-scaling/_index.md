---
date: 2026-02-15
description: Apprenez à définir une taille de page personnalisée et à créer un PDF
  à partir de CAD en utilisant Aspose.CAD pour Java. Ce guide étape par étape couvre
  l'exportation de CAD vers PDF avec le redimensionnement automatique de la mise en
  page.
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
title: Définir une taille de page personnalisée – PDF à partir de CAD avec mise à
  l’échelle automatique de la mise en page
url: /fr/java/advanced-cad-features/setting-auto-layout-scaling/
weight: 17
---

 is.

Also need to translate tables content.

Let's produce French translation.

Be careful not to translate URLs, file paths, variable names.

Translate sentences.

Let's craft.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Définir une taille de page personnalisée – Créer un PDF à partir de CAD avec mise à l’échelle automatique du layout

## Introduction

Si vous devez **définir une taille de page personnalisée** tout en **créant un PDF à partir de fichiers CAD** rapidement et avec une mise à l’échelle parfaite, Aspose.CAD for Java répond à vos besoins. La mise à l’échelle automatique du layout ajuste automatiquement les dimensions du layout afin que le PDF résultant apparaisse exactement comme prévu, quel que soit la taille de page CAD d’origine. Dans ce tutoriel, nous parcourrons le processus complet — du chargement d’un fichier DXF à l’exportation d’un PDF — en mettant en avant les capacités **export CAD to PDF** de la bibliothèque et en montrant comment vous pouvez également **convertir DWG en PDF** ou **augmenter la résolution du PDF** lorsque nécessaire.

## Réponses rapides
- **Que fait la mise à l’échelle automatique du layout ?** Elle redimensionne automatiquement les layouts CAD pour qu’ils s’ajustent aux dimensions de la page cible lors de la rasterisation.
- **Quels formats puis‑je convertir ?** Tout format pris en charge par Aspose.CAD (par ex., DXF, DWG, DWF) peut être converti en PDF.
- **Ai‑je besoin d’une licence pour la production ?** Oui, une licence commerciale est requise pour une utilisation autre que l’évaluation.
- **Combien de temps prend la conversion ?** Généralement moins d’une seconde pour des fichiers standards sur du matériel moderne.
- **Puis‑je modifier la taille de la page ?** Oui, vous pouvez définir des dimensions de page personnalisées via `CadRasterizationOptions`.

## Qu’est‑ce que « créer un PDF à partir de CAD » ?

Créer un PDF à partir de CAD consiste à prendre un dessin d’ingénierie vectoriel (DXF, DWG, etc.) et à le rasteriser dans un document PDF. Le PDF conserve la fidélité visuelle du dessin original tout en étant largement visualisable sur n’importe quelle plateforme.

## Pourquoi utiliser la mise à l’échelle automatique du layout ?

- **Sortie cohérente :** Garantit que tous les layouts remplissent la page PDF sans calculs de taille manuels.
- **Gain de temps :** Élimine le besoin d’ajuster manuellement les facteurs de mise à l’échelle pour chaque dessin.
- **Haute qualité :** Conserve le poids des lignes et la précision géométrique pendant la conversion.
- **Flexibilité :** Fonctionne pour **convert dxf to pdf**, **convert dwg to pdf**, et même lorsque vous devez **increase PDF resolution** pour des fichiers prêts à l’impression.

## Prérequis

1. **Bibliothèque Aspose.CAD for Java** – téléchargez la dernière version depuis la [page de téléchargement](https://releases.aspose.com/cad/java/).  
2. **Répertoire de ressources** – créez un dossier sur votre machine pour stocker les fichiers CAD ; remplacez `"Your Document Directory"` dans le code par ce chemin.  
3. **Fichier CAD d’exemple** – pour ce guide nous utiliserons `conic_pyramid.dxf`, inclus dans le jeu de données d’exemple Aspose.

## Importer les espaces de noms

Tout d’abord, importez les classes requises. Cela nous donne accès aux fonctionnalités de chargement d’image, de rasterisation et d’exportation PDF.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Comment définir une taille de page personnalisée pour le PDF à partir de CAD

Avant de plonger dans le code pas à pas, comprenons pourquoi définir une taille de page personnalisée est important. Lorsque vous **définissez une taille de page personnalisée**, vous contrôlez les dimensions physiques du PDF résultant (par ex., A4, Letter ou une taille sur‑mesure). Cela est essentiel dans les flux de travail d’ingénierie où les dessins doivent correspondre aux normes de feuilles ou lorsque vous devez intégrer le PDF dans des documents plus volumineux.

### Étape 1 : Charger le fichier CAD

Le chargement du fichier source est la première étape de **how to export CAD** vers un document PDF.

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Étape 2 : Créer les options de rasterisation

Définissez les dimensions de la page cible. Vous pouvez également utiliser ce bloc pour **set CAD page size** manuellement si vous préférez un layout personnalisé.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1600);
rasterizationOptions.setPageHeight(1600);
```

### Étape 3 : Activer la mise à l’échelle automatique du layout

Activez la fonctionnalité de mise à l’échelle automatique. C’est le cœur de **how to set scaling** pour une conversion CAD‑to‑PDF.

```java
rasterizationOptions.setAutomaticLayoutsScaling(true);
```

### Étape 4 : Créer les options PDF

Liez les paramètres de rasterisation aux options d’exportation PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 5 : Exporter en PDF

Enfin, enregistrez l’image rendue sous forme de fichier PDF. Cette étape finalise le flux de travail **convert dxf to pdf**.

```java
image.save(dataDir + "result_out_.pdf", pdfOptions);
```

Répétez les étapes ci‑dessus pour tout fichier CAD supplémentaire que vous devez traiter, qu’il s’agisse de **DWG**, **DWF** ou d’autres formats pris en charge.

## Cas d’utilisation courants

| Scénario | Pourquoi définir une taille de page personnalisée ? |
|----------|------------------------------------------------------|
| **Soumission de plans de construction** | Aligne le PDF avec les tailles de feuille standard A1/A2 requises par les autorités réglementaires. |
| **Intégration dans des manuels techniques** | Garantit que le dessin s’adapte à la mise en page prédéfinie du manuel sans mise à l’échelle supplémentaire. |
| **Impression haute résolution** | Vous permet d’augmenter le DPI (par ex., `rasterizationOptions.setResolution(300)`) tout en conservant les dimensions de la page. |

## Problèmes courants & dépannage

| Symptom | Cause probable | Solution |
|---------|----------------|----------|
| PDF vide | Options de rasterisation non définies ou chemin de fichier incorrect | Vérifiez le chemin `srcFile` et assurez‑vous que `setPageWidth/Height` ne sont pas à zéro |
| Mise à l’échelle déformée | `setAutomaticLayoutsScaling` laissé à `false` | Activez la mise à l’échelle automatique ou calculez manuellement le facteur de mise à l’échelle |
| Couches manquantes | Le DXF source contient des entités non prises en charge | Consultez les notes de version d’Aspose.CAD pour les types d’entités supportés |

## Foire aux questions

**Q : Aspose.CAD for Java est‑il compatible avec tous les formats de fichiers CAD ?**  
R : Aspose.CAD for Java prend en charge divers formats CAD, dont DWG, DXF et DWF.

**Q : Puis‑je personnaliser davantage les options de mise à l’échelle ?**  
R : Oui, la classe `CadRasterizationOptions` propose des propriétés pour affiner la mise à l’échelle, le DPI et d’autres paramètres de rasterisation.

**Q : Où puis‑je trouver une documentation supplémentaire pour Aspose.CAD for Java ?**  
R : Consultez la [documentation](https://reference.aspose.com/cad/java/) pour des informations détaillées et des exemples.

**Q : Existe‑t‑il un essai gratuit pour Aspose.CAD for Java ?**  
R : Oui, vous pouvez explorer un [essai gratuit](https://releases.aspose.com/) pour découvrir les capacités d’Aspose.CAD for Java.

**Q : Comment obtenir de l’aide ou participer aux discussions sur Aspose.CAD for Java ?**  
R : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour rejoindre la communauté et demander du support.

**Questions communes supplémentaires**

**Q : Comment convertir un fichier DWG en PDF au lieu de DXF ?**  
R : Le même code fonctionne ; il suffit de changer l’extension du fichier dans `srcFile` en `.dwg`.

**Q : Puis‑je définir un DPI personnalisé pour des PDF à plus haute résolution ?**  
R : Oui, utilisez `rasterizationOptions.setResolution(300);` (ou tout DPI dont vous avez besoin).

**Q : Est‑il possible d’incorporer des polices dans le PDF généré ?**  
R : Aspose.CAD rasterise le dessin, les polices sont donc rendues comme vecteurs ; aucune incorporation de police séparée n’est requise.

## Conclusion

En suivant ce guide, vous savez maintenant comment **définir une taille de page personnalisée** et **créer un PDF à partir de CAD** en utilisant Aspose.CAD for Java avec la mise à l’échelle automatique du layout. Le processus rationalise le flux de travail **export CAD to PDF**, assure une mise à l’échelle cohérente et vous fait gagner un temps de développement précieux. N’hésitez pas à expérimenter avec différentes tailles de page, résolutions et formats CAD pour répondre aux besoins de votre projet, que vous **convertissiez DWG en PDF**, **augmentiez la résolution du PDF** ou construisiez un **java CAD to PDF** batch processor.

---

**Dernière mise à jour :** 2026-02-15  
**Testé avec :** Aspose.CAD for Java 24.12 (latest)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}