---
date: 2026-05-20
description: Apprenez comment ajouter une image aux fichiers DWG en utilisant Aspose.CAD
  pour Java et également convertir DWG en PDF. Suivez notre guide étape par étape
  pour un développement efficace.
keywords:
- add image to dwg
- convert dwg to pdf
- import image into dwg
- embed raster image dwg
- dwg file operations
linktitle: Importer une image dans un fichier DWG avec Java
schemas:
- author: Aspose
  dateModified: '2026-05-20'
  description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  headline: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  type: TechArticle
- description: Learn how to add image to DWG files using Aspose.CAD for Java and also
    convert DWG to PDF. Follow our step-by-step guide for efficient development.
  name: Add Image to DWG Files Effortlessly Using Aspose.CAD Java
  steps:
  - name: Load the DWG File
    text: First, point to the folder that contains your DWG drawing and load it with
      `Image.load`.
  - name: Define the Raster Image Definition
    text: The `CadRasterImageDef` class defines the external raster image resource
      to be embedded in the drawing.
  - name: Set Insertion Point and Scaling Vectors
    text: The insertion point determines where the lower‑left corner of the image
      will appear. The **U** and **V** vectors control horizontal and vertical scaling.
  - name: Create the CadRasterImage Object
    text: The `CadRasterImage` entity represents a raster picture placed in the DWG
      model space.
  - name: Add the Image to Model Space
    text: Insert the raster image into the `*Model_Space` block, then update the drawing’s
      object collection so the definition is saved.
  - name: Configure PDF Export Options (Optional)
    text: '`PdfOptions` specifies settings for saving a CAD drawing as a PDF file.
      `CadRasterizationOptions` defines how the CAD content is rasterized during PDF
      conversion.'
  - name: Save the Resulting PDF
    text: 'Finally, export the modified drawing as a PDF file. The same `image` instance
      is used, so the PDF reflects the newly added raster image. By following these
      steps, you can **add image to dwg** files quickly and also **save dwg as pdf**
      when needed, covering the most common **dwg file operations** in '
  type: HowTo
- questions:
  - answer: Yes, Aspose.CAD for Java works with any IDE that supports JDK 8+, including
      IntelliJ IDEA, Eclipse, and VS Code.
    question: Is Aspose.CAD for Java compatible with all Java development environments?
  - answer: Yes, you can use Aspose.CAD for Java for commercial projects. Visit **[here](https://purchase.aspose.com/buy)**
      for licensing details.
    question: Can I use Aspose.CAD for Java for commercial projects?
  - answer: Yes, you can access the free trial **[here](https://releases.aspose.com/)**.
    question: Is there a free trial available for Aspose.CAD for Java?
  - answer: You can seek support on the **[Aspose.CAD forum](https://forum.aspose.com/c/cad/19)**.
    question: How can I get support for Aspose.CAD for Java?
  - answer: Yes, you can get a temporary license **[here](https://purchase.aspose.com/temporary-license/)**.
    question: Can I obtain a temporary license for Aspose.CAD for Java?
  type: FAQPage
second_title: Aspose.CAD Java API
title: Ajouter une image aux fichiers DWG facilement avec Aspose.CAD Java
url: /fr/java/dwg-file-operations/import-image-to-dwg/
weight: 10
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Ajouter une image aux fichiers DWG facilement avec Aspose.CAD Java

Dans les applications Java modernes, **ajouter une image à un DWG** est une exigence courante—que vous construisiez un visualiseur CAD, automatisiez les mises à jour de dessins ou génériez de la documentation. Aspose.CAD pour Java vous offre une méthode simple et haute performance pour intégrer des images raster directement dans les dessins DWG sans nécessiter un moteur CAD complet. Dans ce tutoriel, nous vous guiderons à travers l’ensemble du processus, du chargement d’un DWG à l’exportation du résultat en PDF, et nous couvrirons également comment **importer une image dans dwg** et **convertir dwg en pdf** dans un flux de travail unique.

## Réponses rapides
- **Quelle bibliothèque faut‑il ?** Aspose.CAD for Java  
- **Puis‑je également exporter en PDF ?** Oui – utilisez `PdfOptions` avec `CadRasterizationOptions`  
- **Ai‑je besoin d’une licence pour le développement ?** Un essai gratuit suffit pour les tests ; une licence commerciale est requise pour la production  
- **Quelle version de Java est prise en charge ?** Java 8 et supérieur  
- **Combien de temps prend l’implémentation ?** Environ 10‑15 minutes pour une importation d’image basique  

## Qu’est‑ce que « ajouter une image à dwg » ?

Ajouter une image à un fichier DWG signifie intégrer une image raster (PNG, JPEG, etc.) en tant qu’entité **CadRasterImage** dans l’espace modèle du dessin, où elle peut être positionnée, mise à l’échelle et éventuellement découpée comme tout autre objet CAD. Elle est stockée dans la table des objets du dessin et affichée par les visualiseurs CAD standards.

## Pourquoi utiliser Aspose.CAD pour Java pour ajouter une image à dwg ?

Vous pouvez intégrer des graphiques raster dans des fichiers DWG sans installer de logiciel CAD tiers, et l’API vous offre un contrôle pixel‑par‑pixel sur le point d’insertion, les vecteurs d’échelle et les limites de découpage. Aspose.CAD traite des fichiers jusqu’à 2 Go, prend en charge **plus de 50 formats d’entrée et de sortie**, et fonctionne sous Windows, Linux et macOS, vous permettant d’intégrer la manipulation CAD dans n’importe quel backend Java.

## Prérequis
- **Aspose.CAD pour Java** – téléchargez le JAR le plus récent depuis le site officiel **[ici](https://releases.aspose.com/cad/java/)**.  
- **Java Development Kit** – JDK 8 ou supérieur, avec votre IDE préféré (IntelliJ IDEA, Eclipse, VS Code, etc.).  
- Une licence **Aspose.CAD** valide pour l’utilisation en production (l’essai fonctionne pour l’expérimentation).  

## Importer les packages
Les importations suivantes apportent les classes essentielles d’Aspose.CAD utilisées pour la manipulation d’images et la conversion PDF.  
```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadDrawTypeMode;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.*;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Guide étape par étape

### Étape 1 : Charger le fichier DWG
Tout d’abord, indiquez le dossier contenant votre dessin DWG et chargez‑le avec `Image.load`.  
```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
String srcFile = dataDir + "Drawing11.dwg";
Image image = Image.load(srcFile);
```

### Étape 2 : Définir la définition de l’image raster
La classe `CadRasterImageDef` définit la ressource d’image raster externe à intégrer dans le dessin.  
```java
CadRasterImageDef cadRasterImageDef = new CadRasterImageDef("road-sign-custom.png", 640, 562);
cadRasterImageDef.setObjectHandle("A3B4");
```

### Étape 3 : Définir le point d’insertion et les vecteurs d’échelle
Le point d’insertion détermine où le coin inférieur gauche de l’image apparaîtra. Les vecteurs **U** et **V** contrôlent le redimensionnement horizontal et vertical.  
```java
Cad3DPoint insertionPoint = new Cad3DPoint(26.77, 22.35);
Cad3DPoint uVector = new Cad3DPoint(0.0061565450840500831, 0);
Cad3DPoint vVector = new Cad3DPoint(0, 0.0061565450840500822);
```

### Étape 4 : Créer l’objet CadRasterImage
L’entité `CadRasterImage` représente une image raster placée dans l’espace modèle du DWG.  
```java
CadRasterImage cadRasterImage = new CadRasterImage(cadRasterImageDef, insertionPoint, uVector, vVector);
cadRasterImage.setImageDefReference("A3B4");
cadRasterImage.setDisplayFlags((short)7);
cadRasterImage.setClippingState((short)0);
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(-0.5, 0.5));
cadRasterImage.getClipBoundaryVertexList().add(new Cad2DPoint(639.5, 561.5));
```

### Étape 5 : Ajouter l’image à l’espace modèle
Insérez l’image raster dans le bloc `*Model_Space`, puis mettez à jour la collection d’objets du dessin afin que la définition soit enregistrée.  
```java
CadImage cadImage = ((CadImage)(image));
cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(cadRasterImage);
CadBaseObject[] objs = cadImage.getObjects();
CadBaseObject[] arr = new CadBaseObject[objs.length + 1];
int ind = 0;
for (CadBaseObject obj : objs)
{
    arr[ind] = obj;
    ind++;
}
arr[ind] = cadRasterImageDef;
cadImage.setObjects(arr);
```

### Étape 6 : Configurer les options d’exportation PDF (facultatif)
`PdfOptions` spécifie les paramètres pour enregistrer un dessin CAD en fichier PDF. `CadRasterizationOptions` définit comment le contenu CAD est rasterisé pendant la conversion PDF.  
```java
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
cadRasterizationOptions.setDrawType(CadDrawTypeMode.UseObjectColor);
cadRasterizationOptions.setPageHeight(1600);
cadRasterizationOptions.setPageWidth(1600);
cadRasterizationOptions.setLayouts(new String[] {"Model"});
```

### Étape 7 : Enregistrer le PDF résultant
Enfin, exportez le dessin modifié en fichier PDF. La même instance `image` est utilisée, de sorte que le PDF reflète la nouvelle image raster ajoutée.  
```java
image.save((srcFile + "_generated.pdf"), pdfOptions);
```

En suivant ces étapes, vous pouvez **ajouter une image aux fichiers dwg** rapidement et également **enregistrer dwg en pdf** lorsque nécessaire, couvrant les opérations **dwg file operations** les plus courantes dans une routine unique et compacte.

## Problèmes courants et solutions
- **Image non affichée** – Vérifiez que le chemin du fichier image (`road-sign-custom.png`) est correct et que les dimensions de l’image correspondent aux valeurs passées à `CadRasterImageDef`.  
- **Échelle incorrecte** – Ajustez les vecteurs U et V ; ils représentent les unités de dessin par pixel.  
- **Le PDF apparaît vide** – Assurez‑vous que `CadRasterizationOptions.setDrawType` est réglé sur `UseObjectColor` ou un autre mode approprié.  

## Questions fréquemment posées

**Q : Aspose.CAD pour Java est‑il compatible avec tous les environnements de développement Java ?**  
A : Oui, Aspose.CAD pour Java fonctionne avec tout IDE supportant JDK 8+, y compris IntelliJ IDEA, Eclipse et VS Code.

**Q : Puis‑je utiliser Aspose.CAD pour Java pour des projets commerciaux ?**  
A : Oui, vous pouvez utiliser Aspose.CAD pour Java pour des projets commerciaux. Consultez **[ici](https://purchase.aspose.com/buy)** pour les détails de licence.

**Q : Existe‑t‑il un essai gratuit disponible pour Aspose.CAD pour Java ?**  
A : Oui, vous pouvez accéder à l’essai gratuit **[ici](https://releases.aspose.com/)**.

**Q : Comment puis‑je obtenir du support pour Aspose.CAD pour Java ?**  
A : Vous pouvez obtenir du support sur le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)**.

**Q : Puis‑je obtenir une licence temporaire pour Aspose.CAD pour Java ?**  
A : Oui, vous pouvez obtenir une licence temporaire **[ici](https://purchase.aspose.com/temporary-license/)**.

**Dernière mise à jour :** 2026-05-20  
**Testé avec :** Aspose.CAD for Java 24.11  
**Auteur :** Aspose  

{{< blocks/products/products-backtop-button >}}

## Tutoriels associés

- [Exporter DWG en PDF ou raster avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)
- [Ajouter des propriétés personnalisées aux fichiers DWG avec Aspose.CAD pour Java](/cad/java/additional-features/add-custom-properties/)
- [Enregistrer CAD en PNG – Convertir un dessin CAD en format d’image raster avec Aspose.CAD pour Java](/cad/java/cad-drawing-conversion/convert-cad-drawing-to-raster-image/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}