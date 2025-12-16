---
date: 2025-12-16
description: Apprenez comment convertir CAD en PNG avec Aspose.CAD pour Java, en couvrant
  l'exportation DWG vers une image, l'enregistrement du CAD au format PNG et les options
  de conversion du CAD en image raster.
linktitle: Convert CAD Drawing to Raster Image Format
second_title: Aspose.CAD Java API
title: Comment convertir un CAD en PNG avec Aspose.CAD pour Java
url: /fr/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment convertir CAD en PNG avec Aspose.CAD pour Java

Dans les flux de travail d'ingénierie modernes, vous devez souvent **convertir CAD en PNG** afin que les dessins puissent être affichés dans les navigateurs, intégrés dans des documents ou partagés avec des parties prenantes qui ne possèdent pas de logiciel CAD. Ce tutoriel vous guide à travers l'ensemble du processus — du chargement d'un fichier CAD à l'exportation d'une image raster PNG de haute qualité — en utilisant la puissante bibliothèque Aspose.CAD pour Java.

## Réponses rapides
- **Quel est le but principal ?** Convertir les dessins CAD en images raster PNG.  
- **Quelle bibliothèque est utilisée ?** Aspose.CAD pour Java.  
- **Ai‑je besoin d’une licence ?** Un essai gratuit est disponible ; une licence est requise pour une utilisation en production.  
- **Puis‑je personnaliser la taille de l’image ?** Oui, utilisez `CadRasterizationOptions` pour définir la largeur et la hauteur.  
- **Formats CAD pris en charge ?** DWG, DXF, DWF et bien d’autres.

## Qu’est‑ce que « convertir CAD en PNG » ?
Convertir CAD en PNG signifie rasteriser le contenu CAD basé sur des vecteurs (DWG, DXF, etc.) en un format d'image basé sur des pixels. PNG conserve la transparence et une qualité sans perte, ce qui le rend idéal pour les aperçus web, la documentation et les rapports.

## Pourquoi convertir CAD en PNG (cad en image raster) ?
- **Visualisation universelle :** PNG fonctionne sur n’importe quel appareil sans visionneurs CAD spéciaux.  
- **Chargement rapide :** Les images raster se chargent instantanément dans les pages web.  
- **Intégration facile :** Insérez des PNG dans des PDF, des documents Word ou des présentations.  
- **Aspect cohérent :** Conservez les épaisseurs de ligne, les couleurs et les calques exactement comme conçus.

## Prérequis
Avant de commencer, assurez‑vous d’avoir :

1. **Environnement de développement Java** – JDK 8 ou version ultérieure installé et configuré.  
2. **Bibliothèque Aspose.CAD** – Téléchargez et ajoutez la bibliothèque à votre projet. Vous pouvez trouver la bibliothèque **[ici](https://releases.aspose.com/cad/java/)**.

## Importer les espaces de noms
Ajoutez les imports requis à votre classe Java afin de pouvoir travailler avec les objets Aspose.CAD.

```java
import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;
```

## Guide étape par étape pour convertir CAD en PNG

### Étape 1 : Charger le dessin CAD
Tout d’abord, chargez le fichier CAD source (DXF, DWG, etc.) en utilisant `Image.load()`.

```java
String dataDir = "Your Document Directory" + "CADConversion/";
String srcFile = dataDir + "conic_pyramid.dxf";
Image image = Image.load(srcFile);
```

> **Astuce :** Conservez vos fichiers CAD dans un dossier dédié (par ex., `CADConversion`) pour éviter les problèmes de chemin.

### Étape 2 : Définir les options de rasterisation (exporter dwg en image)
Définissez la taille de l’image de sortie et les autres paramètres raster.

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(1200);
rasterizationOptions.setPageHeight(1200);
```

Vous pouvez également contrôler la couleur d’arrière‑plan, le mode de rendu des lignes et le DPI ici si nécessaire.

### Étape 3 : Créer les options d’image (enregistrer cad en png)
Créez une instance `PngOptions` et associez‑y les paramètres de rasterisation.

```java
ImageOptionsBase options = new PngOptions();
options.setVectorRasterizationOptions(rasterizationOptions);
```

### Étape 4 : Enregistrer l’image raster (fichier cad en png)
Enfin, écrivez le fichier PNG sur le disque.

```java
image.save(dataDir + "conic_pyramid_raster_image_out.png", options);
```

Le fichier résultant `conic_pyramid_raster_image_out.png` est une représentation PNG haute résolution de votre dessin CAD original.

### Répéter pour d’autres fichiers
Il suffit de modifier `srcFile` pour pointer vers un autre fichier CAD et d’exécuter les mêmes étapes. Le même code fonctionne pour DWG, DWF et les autres formats pris en charge.

## Problèmes courants & solutions
| Problème | Solution |
|----------|----------|
| **Sortie PNG vide** | Vérifiez que le fichier CAD source se charge correctement (`Image.load()` ne doit pas lever d’exception). |
| **Dimensions incorrectes** | Ajustez `PageWidth` / `PageHeight` ou définissez le DPI via `rasterizationOptions.setResolution(...)`. |
| **Couches manquantes** | Assurez‑vous que les calques du fichier CAD ne sont pas masqués ; utilisez `CadRasterizationOptions.setDrawType(CadDrawTypeMode.Vector);`. |
| **Erreurs de licence** | Utilisez un fichier de licence Aspose.CAD valide (`License license = new License(); license.setLicense("Aspose.CAD.lic");`). |

## Questions fréquemment posées

**Q1 : Aspose.CAD est‑il compatible avec tous les formats CAD ?**  
R1 : Aspose.CAD prend en charge un large éventail de formats CAD, dont DWG, DXF, DWF et plus encore. Consultez la **[documentation](https://reference.aspose.com/cad/java/)** pour la liste complète.

**Q2 : Puis‑je personnaliser les options de rasterisation selon mes besoins spécifiques ?**  
R2 : Oui, Aspose.CAD offre une flexibilité dans la définition des options de rasterisation, vous permettant d’adapter la sortie à vos exigences (taille, DPI, couleur d’arrière‑plan, etc.).

**Q3 : Où puis‑je trouver du support pour les questions liées à Aspose.CAD ?**  
R3 : Consultez le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** pour obtenir de l’aide et échanger avec la communauté.

**Q4 : Existe‑t‑il un essai gratuit disponible pour Aspose.CAD pour Java ?**  
R4 : Oui, vous pouvez explorer les fonctionnalités d’Aspose.CAD en obtenant un essai gratuit **[ici](https://releases.aspose.com/)**.

**Q5 : Comment puis‑je acheter Aspose.CAD pour Java ?**  
R5 : Pour acheter Aspose.CAD pour Java, rendez‑vous sur la **[page d’achat](https://purchase.aspose.com/buy)**.

---

**Dernière mise à jour :** 2025-12-16  
**Testé avec :** Aspose.CAD pour Java 24.11 (dernière version au moment de la rédaction)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}