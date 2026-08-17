---
date: 2026-02-20
description: Apprenez à exporter des PDF AutoCAD à l'aide d'Aspose.CAD pour Java.
  Ce guide étape par étape vous montre comment **convertir DWG en PDF**, **enregistrer
  le CAD au format PDF**, et gérer la licence.
linktitle: Export AutoCAD Images to PDF
second_title: Aspose.CAD Java API
title: Convertir DWG en PDF - Exporter des images AutoCAD en PDF avec Aspose.CAD pour
  Java
url: /fr/java/cad-export-options/export-autocad-images-to-pdf/
weight: 10
---

 Export AutoCAD Images to PDF with Aspose.CAD for Java" etc.

Also translate the table content.

Also translate "Last Updated", "Tested With", "Author".

Make sure to keep markdown formatting.

Let's produce final content.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Export AutoCAD PDF - Exporter des images AutoCAD en PDF avec Aspose.CAD pour Java

## Introduction

Vous cherchez à **convertir DWG en PDF** avec Java ? Ne cherchez plus ! Dans ce tutoriel, nous vous guiderons à travers la conversion d’images AutoCAD en PDF avec Aspose.CAD pour Java, une bibliothèque puissante qui rend le processus de **conversion DWG en PDF** simple et efficace. À la fin, vous saurez comment **enregistrer un CAD en PDF**, appliquer des paramètres de rasterisation personnalisés, et travailler avec une licence Aspose.CAD pour une utilisation en production.

## Réponses rapides
- **Puis-je convertir DWG en PDF avec Java ?** Oui, Aspose.CAD pour Java gère DWG, DXF et de nombreux autres formats.  
- **Ai‑je besoin d’une licence ?** Une **licence Aspose CAD** est requise pour une utilisation illimitée ; une licence temporaire est disponible pour l’évaluation.  
- **Quelle version de Java est prise en charge ?** Java 8+ (la bibliothèque est compatible avec toutes les JDK modernes).  
- **Puis‑je personnaliser la taille de la page PDF ?** Absolument — ajustez `pageWidth` et `pageHeight` dans les options de rasterisation.  
- **La rasterisation 3‑D est‑elle possible ?** Oui, activez `TypeOfEntities.Entities3D` pour un rendu 3‑D complet.

## Qu’est‑ce que **export autocad pdf** ?
Exporter AutoCAD en PDF signifie convertir des dessins CAD vectoriels (DWG, DXF, DWF, etc.) en un document PDF portable tout en préservant les calques, les épaisseurs de ligne et, éventuellement, la géométrie 3‑D. Cela est utile pour partager des conceptions avec des clients, archiver ou imprimer sans nécessiter de logiciel CAD.

## Pourquoi convertir DWG en PDF avec Aspose.CAD pour Java ?
- **Prise en charge complète des formats** – fonctionne avec DWG, DXF, DWF et bien d’autres.  
- **Aucune dépendance externe** – bibliothèque pure Java, sans DLL natives.  
- **Rasterisation de haute qualité** – contrôle du DPI, de la taille de page et de la mise en page, vous permettant de **personnaliser la taille de la page PDF** selon les exigences de votre projet.  
- **Flexibilité de licence** – commencez avec un essai gratuit, puis passez à une **licence Aspose CAD** permanente.  

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Environnement de développement Java** – JDK 8 ou version ultérieure installé.  
- **Bibliothèque Aspose.CAD pour Java** – téléchargez‑la depuis le [lien de téléchargement](https://releases.aspose.com/cad/java/).  
- **Répertoire de documents** – un dossier sur votre machine où les fichiers CAD source et les PDF générés seront stockés.

## Importer les espaces de noms

Dans votre projet Java, importez les classes nécessaires pour travailler avec Aspose.CAD :

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;
```

Passons maintenant au code étape par étape.

## Comment convertir DWG en PDF avec Aspose.CAD pour Java

### Étape 1 : Définir le chemin du répertoire des ressources

```java
String dataDir = "Your Document Directory" + "ExportingCAD/";
```

> **Astuce :** Remplacez `"Your Document Directory"` par le chemin absolu du dossier que vous avez créé dans les prérequis.

### Étape 2 : Charger l’image CAD

```java
String srcFile = dataDir + "conic_pyramid.dxf";
Image cadImage = Image.load(srcFile);
```

> **Pourquoi c’est important :** Charger le fichier CAD dans un objet `Image` vous donne un accès complet au moteur de rasterisation d’Aspose.CAD.

### Étape 3 : Définir les options de rasterisation

```java
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.setPageWidth(500);
rasterizationOptions.setPageHeight(500);
// rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

rasterizationOptions.setLayouts(new String[] {"Model"});
```

- Ajustez `pageWidth` et `pageHeight` pour **personnaliser la taille de la page PDF**.  
- Décommentez la ligne `setTypeOfEntities` si vous avez besoin de **java convert cad pdf** pour les entités 3‑D.  
- L’appel `setLayouts` sélectionne la mise en page à rendre (Model, Layout1, etc.).

### Étape 4 : Configurer les options PDF

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
```

Cela lie les paramètres de rasterisation à la sortie PDF, garantissant que les données vectorielles sont correctement converties.

### Étape 5 : Enregistrer le PDF

```java
cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
```

Le fichier résultant, `Export3DImagestoPDF_out_.pdf`, constitue une **enregistrement cad as pdf** de votre dessin AutoCAD d’origine.

## Problèmes courants & Solutions

| Symptom | Likely Cause | Fix |
|---------|--------------|-----|
| PDF vide | Options de rasterisation non définies ou mise en page incorrecte | Vérifiez que `setLayouts` correspond au nom de la mise en page dans votre fichier CAD. |
| Image basse résolution | `pageWidth`/`pageHeight` trop petites | Augmentez les dimensions ou définissez un DPI plus élevé via `rasterizationOptions.setResolution(...)`. |
| Exception de licence | Aucune licence valide appliquée | Appliquez une **licence Aspose CAD** ou utilisez une licence temporaire pour les tests. |

## Questions fréquentes

### Q1 : Puis‑je utiliser Aspose.CAD pour Java avec d’autres formats de fichiers CAD ?
R1 : Oui, Aspose.CAD prend en charge un large éventail de formats, dont DWG, DWF, DGN, et bien d’autres, vous offrant une grande flexibilité dans vos projets.

### Q2 : Comment obtenir une licence temporaire pour Aspose.CAD pour Java ?
R2 : Visitez [ici](https://purchase.aspose.com/temporary-license/) pour obtenir une licence temporaire d’évaluation.

### Q3 : Existe‑t‑il des options de mise en page pour la rasterisation ?
R3 : Oui, vous pouvez personnaliser les mises en page (par ex., `"Model"`, `"Layout1"`) via la méthode `setLayouts` pour contrôler la vue rendue.

### Q4 : Puis‑je personnaliser la taille du fichier PDF de sortie ?
R4 : Absolument ! Ajustez les paramètres `pageWidth` et `pageHeight` dans les options de rasterisation pour obtenir les dimensions souhaitées.

### Q5 : Où puis‑je obtenir de l’aide ou discuter des problèmes liés à Aspose.CAD pour Java ?
R5 : Rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour un support dédié et des discussions communautaires.

---

**Dernière mise à jour :** 2026-02-20  
**Testé avec :** Aspose.CAD pour Java 24.10  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}