---
date: 2025-11-29
description: Apprenez à convertir le DXF en WMF avec Aspose.CAD pour Java, chargez
  le dessin DXF et, éventuellement, utilisez l’exportation Aspose vers PDF. Guide
  étape par étape avec des exemples de code.
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
title: Convertir DXF en WMF à l'aide d'Aspose.CAD en Java
url: /fr/java/additional-features/export-dxf-to-wmf/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DXF en WMF avec Aspose.CAD en Java

## Introduction

Dans ce tutoriel, vous découvrirez comment **convertir DXF en WMF** avec Aspose.CAD pour Java. Que vous ayez besoin d’intégrer des dessins CAD dans un rapport sous Windows ou que vous souhaitiez simplement un format vectoriel léger, la conversion de DXF en WMF est une exigence courante. Nous parcourrons le chargement d’un dessin DXF, la configuration des options de rasterisation, l’enregistrement du résultat au format WMF, et même l’utilisation de l’exportation Aspose vers PDF comme étape optionnelle.

## Réponses rapides
- **Puis-je convertir DXF en WMF avec un essai gratuit ?** Oui – Aspose propose un essai complet de 30 jours.  
- **Quelle version de Java est requise ?** Java 8 ou ultérieure.  
- **Ai-je besoin d’une licence pour exécuter le code ?** Une licence est requise en production ; l’essai fonctionne pour le développement et les tests.  
- **La conversion est‑elle sans perte ?** Les données vectorielles sont préservées ; les options de rasterisation vous permettent de contrôler la résolution.  
- **Puis‑je également exporter le même dessin en PDF ?** Absolument – voir l’étape « Exportation vers PDF » ci‑dessous.

## Qu’est‑ce que « convertir DXF en WMF » ?

Convertir DXF en WMF consiste à prendre un fichier Drawing Exchange Format (DXF) — un format CAD largement utilisé — et à le transformer en Windows Metafile (WMF). WMF est un format d’image vectorielle qui s’intègre parfaitement à Microsoft Office, aux applications Windows et à de nombreux outils de reporting.

## Pourquoi utiliser Aspose.CAD pour Java ?

- **Aucune dépendance externe** – Java pur, pas de DLL natives.  
- **Haute fidélité** – préserve les calques, les couleurs et les styles de ligne.  
- **Rasterisation intégrée** – ajuste finement la taille de la page, la résolution et l’arrière‑plan.  
- **Solution tout‑en‑un** – la même API prend également en charge l’exportation vers PDF, PNG, SVG, et plus encore.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Aspose.CAD pour Java** intégré à votre projet. Téléchargez‑le depuis le site officiel : [Aspose.CAD Java download](https://releases.aspose.com/cad/java/).  
- **Répertoire de documents** où vos fichiers DXF sont stockés (par ex., `Your Document Directory/DXFDrawings/`).

## Importer les espaces de noms

Dans votre fichier source Java, importez les classes Aspose.CAD dont vous avez besoin :

```java
import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;
```

## Guide étape par étape

### Étape 1 : Charger le dessin DXF

Tout d’abord, **chargez le dessin DXF** que vous souhaitez convertir. La méthode `Image.load` lit le fichier en mémoire.

```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DXFDrawings/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

### Étape 2 : Configurer les options de rasterisation

Configurez les paramètres de rasterisation qui contrôlent la taille du WMF de sortie. Dans cet exemple, nous utilisons une page de 100 × 100 unités.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(100);
rasterizationOptions.setPageHeight(100);
WmfOptions wmfOptions = new WmfOptions();
```

### Étape 3 : Enregistrer en WMF

Enregistrez maintenant le dessin chargé en fichier WMF en utilisant les options définies ci‑dessus.

```java
cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
```

### Étape 4 : Libérer les ressources

Libérer correctement les ressources évite les fuites de mémoire, surtout lors du traitement de nombreux dessins.

```java
finally
{
  cadImage.dispose();
}
```

### Étape 5 : Optionnel – Exportation Aspose vers PDF

Si vous avez également besoin d’une version PDF du même dessin, Aspose.CAD le fait en une seule ligne.

```java
image.save(dataDir + "conic_pyramid_out_.pdf"); 
```

> **Astuce :** Vous pouvez réutiliser le même objet `CadRasterizationOptions` pour l’exportation PDF en le passant à une instance `PdfOptions`.

## Problèmes courants et solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| **`NullPointerException` sur `cadImage.save`** | Variable `cadImage` non définie (devrait être `image`). | Remplacez `cadImage` par `image` ou renommez la variable de façon cohérente. |
| **Le WMF de sortie est vide** | Taille de page de rasterisation trop petite ou couleur d’arrière‑plan définie sur transparent. | Augmentez `PageWidth`/`PageHeight` ou définissez une couleur d’arrière‑plan via `rasterizationOptions.setBackgroundColor(Color.getWhite());`. |
| **Exception de licence** | Exécution sans licence Aspose valide en production. | Appliquez le fichier de licence au démarrage de l’application : `License license = new License(); license.setLicense("Aspose.Total.Java.lic");`. |

## Conclusion

Vous disposez désormais d’un flux de travail complet et prêt pour la production afin de **convertir DXF en WMF** avec Aspose.CAD pour Java, avec une étape optionnelle pour **l’exportation Aspose vers PDF**. Cette approche vous fournit une sortie vectorielle de haute qualité qui s’intègre parfaitement aux outils de reporting et de documentation sous Windows.

## FAQ

### Q1 : Où puis‑je trouver la documentation Aspose.CAD ?

R1 : Vous pouvez accéder à la documentation [ici](https://reference.aspose.com/cad/java/).

### Q2 : Comment télécharger Aspose.CAD pour Java ?

R2 : Téléchargez la bibliothèque [ici](https://releases.aspose.com/cad/java/).

### Q3 : Une version d’essai gratuite est‑elle disponible ?

R3 : Oui, vous pouvez obtenir un essai gratuit [ici](https://releases.aspose.com/).

### Q4 : Besoin d’options de licence temporaires ?

R4 : Explorez les licences temporaires [ici](https://purchase.aspose.com/temporary-license/).

### Q5 : Où puis‑je obtenir du support ?

R5 : Consultez le forum de support Aspose.CAD [ici](https://forum.aspose.com/c/cad/19).

## Questions fréquemment posées

**Q : Puis‑je convertir de gros fichiers DXF (des centaines de Mo) sans épuiser la mémoire ?**  
**R :** Oui. Chargez le fichier dans un bloc `try‑with‑resources` et libérez rapidement l’objet `Image`. Ajustez `CadRasterizationOptions.setPageWidth/Height` à une taille raisonnable pour limiter la consommation de mémoire.

**Q : La sortie WMF conserve‑t‑elle les informations de calque ?**  
**R :** WMF est un format vectoriel plat, donc la hiérarchie des calques est aplatie, mais les styles de ligne et les couleurs sont préservés.

**Q : Est‑il possible de définir un DPI personnalisé pour le WMF ?**  
**R :** Utilisez `rasterizationOptions.setResolution(300);` pour définir le DPI avant l’enregistrement.

**Q : Puis‑je convertir en lot plusieurs fichiers DXF en une seule exécution ?**  
**R :** Absolument. Parcourez un répertoire, chargez chaque fichier et appliquez la même logique de rasterisation et d’enregistrement.

**Q : Quelles versions de Java sont prises en charge ?**  
**R :** Aspose.CAD pour Java prend en charge Java 8 et ultérieur (y compris Java 11, 17 et les versions LTS plus récentes).

---

**Dernière mise à jour :** 2025-11-29  
**Testé avec :** Aspose.CAD pour Java 24.11  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}