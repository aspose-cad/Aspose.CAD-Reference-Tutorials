---
date: 2026-05-04
description: Apprenez à convertir des fichiers PDF CAD en exportant des DGN vers AutoCAD
  PDF à l'aide d'Aspose.CAD pour Java. Guide étape par étape avec taille de PDF personnalisable
  et options.
keywords:
- convert cad pdf
- how to export dgn
- customize pdf size
- aspose cad download
- set pdf options
linktitle: Exportation de DGN au format AutoCAD vers PDF
second_title: Aspose.CAD Java API
title: Convertir PDF CAD – Exportation sans effort de DGN vers PDF AutoCAD avec Aspose.CAD
  pour Java
url: /fr/java/dgn-export-options/exporting-dgn-to-pdf/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir CAD PDF : Exportation sans effort de DGN vers PDF AutoCAD avec Aspose.CAD pour Java

## Introduction

Si vous devez **convertir des PDF CAD** directement à partir de sources DGN, vous êtes au bon endroit. Dans ce tutoriel, nous vous guiderons pas à pas pour utiliser Aspose.CAD pour Java afin d’exporter des fichiers DGN vers un PDF compatible AutoCAD. Vous verrez comment définir des dimensions de page personnalisées, choisir des mises en page spécifiques et affiner la sortie PDF — le tout avec du code clair, étape par étape, que vous pouvez intégrer directement dans votre projet.

## Réponses rapides
- **Que signifie « convertir CAD PDF » ?** Cela désigne la transformation de fichiers sources CAD (comme DGN) en un PDF qui préserve les données vectorielles et la fidélité de la mise en page.  
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD pour Java fournit une version d’essai fiable, sans licence, pour cette tâche.  
- **Ai‑je besoin d’une licence pour le développement ?** Une version d’essai gratuite suffit pour les tests ; une licence commerciale est requise pour la production.  
- **Puis‑je personnaliser la taille du PDF ?** Oui – les `CadRasterizationOptions` vous permettent de définir la largeur, la hauteur et le facteur d’échelle de la page.  
- **Combien de lignes de code sont nécessaires ?** Moins de 20 lignes de code Java pour charger, configurer et enregistrer le PDF.

## Qu’est‑ce que « convertir CAD PDF » ?
Convertir CAD PDF consiste à prendre un dessin CAD natif (par ex., DGN) et à produire un PDF qui conserve les graphiques vectoriels, les calques et les informations de mise en page d’origine. Le PDF résultant peut être visualisé sur n’importe quel appareil sans nécessiter de logiciel CAD, ce qui le rend idéal pour le partage, l’impression ou l’archivage.

## Pourquoi utiliser Aspose.CAD pour Java pour convertir CAD PDF ?
- **Prise en charge complète des formats** – DGN, DWG, DXF et bien d’autres.  
- **Aucune dépendance externe** – Java pur, pas de DLL natives.  
- **Contrôle granulaire** – vous pouvez choisir les mises en page à exporter, définir des tailles de page personnalisées et contrôler la qualité de rasterisation.  
- **Scalable pour les traitements par lots** – chargez et enregistrez des dizaines de fichiers dans une boucle avec un minimum de surcharge.

## Prérequis
Avant de commencer, assurez‑vous de disposer de :

- **Bibliothèque Aspose.CAD** – téléchargez‑la [ici](https://releases.aspose.com/cad/java/).  
- **Répertoire de documents** – un dossier sur votre machine où les fichiers DGN d’entrée et les PDF de sortie seront stockés.

## Importer les packages

Dans votre projet Java, importez les packages nécessaires pour accéder aux fonctionnalités d’Aspose.CAD :

```java
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

Décomposons maintenant l’exemple de code en plusieurs étapes :

## Étape 1 : Définir les chemins de fichiers (comment exporter dgn)

```java
String dataDir = "Your Document Directory" + "ExportingDGN/";
String fileName = dataDir + "Nikon_D90_Camera.dgn";
String outFile  = dataDir + "Nikon_D90_Camera.pdf";
```

Remplacez `"Your Document Directory"` par le chemin réel où se trouvent vos fichiers.

## Étape 2 : Charger l’image DGN

```java
DgnImage objImage = (DgnImage) Image.load(fileName);
```

Chargez le fichier DGN à l’aide d’Aspose.CAD.

## Étape 3 : Définir les options d’exportation PDF (personnaliser la taille du pdf, définir les options pdf)

```java
PdfOptions options = new PdfOptions();
CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
vectorOptions.setPageWidth(1500);
vectorOptions.setPageHeight(1500);
vectorOptions.setAutomaticLayoutsScaling(true);
vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" }); // Export specific views
options.setVectorRasterizationOptions(vectorOptions);
```

Ici nous définissons les options d’exportation PDF, y compris les dimensions de la page, le redimensionnement automatique et les mises en page DGN (vues) que vous souhaitez inclure dans le PDF final.

## Étape 4 : Enregistrer le fichier PDF

```java
objImage.save(outFile, options);
```

Enregistrez le PDF exporté. La méthode `save` applique toutes les options que vous avez configurées à l’étape précédente.

Répétez ces étapes pour chaque fichier DGN supplémentaire que vous souhaitez convertir. Félicitations ! Vous avez réussi à **convertir CAD PDF** en exportant des fichiers DGN au format PDF AutoCAD avec Aspose.CAD pour Java.

## Problèmes courants et solutions
| Problème | Pourquoi cela se produit | Solution |
|----------|--------------------------|----------|
| **Fichier introuvable** | Chemin `dataDir` incorrect | Vérifiez le chemin du dossier et assurez‑vous que le fichier DGN existe. |
| **Pages blanches dans le PDF** | `AutomaticLayoutsScaling` réglé sur `false` ou identifiants de mise en page manquants | Conservez `setAutomaticLayoutsScaling(true)` et vérifiez les noms de mise en page (`"1","2",…`). |
| **Sortie à basse résolution** | DPI de rasterisation par défaut trop bas | Utilisez `vectorOptions.setResolution(300);` pour augmenter la qualité (ajoutez avant `setVectorRasterizationOptions`). |
| **Exception de licence** | Exécution sans licence valide en production | Appliquez une licence temporaire ou achetée comme décrit dans la documentation Aspose. |

## Questions fréquentes (supplémentaires)

**Q : Puis‑je n’exporter qu’une seule mise en page d’un fichier DGN multi‑mise en page ?**  
R : Oui – spécifiez les identifiants de mise en page souhaités dans `vectorOptions.setLayouts(new String[] { "2" });`.

**Q : Est‑il possible d’incorporer des polices dans le PDF résultant ?**  
R : Aspose.CAD intègre automatiquement les polices nécessaires lors de la rasterisation vectorielle ; vous pouvez également contrôler l’incorporation via `PdfOptions` si besoin.

**Q : Comment traiter de nombreux fichiers DGN en lot ?**  
R : Encapsulez les étapes dans une boucle `for` qui itère sur une liste de noms de fichiers, en réutilisant la même instance de `PdfOptions` pour chaque itération.

**Q : La bibliothèque prend‑elle en charge les PDF protégés par mot de passe ?**  
R : Oui – vous pouvez définir un mot de passe sur l’objet `PdfOptions` via `options.setPassword("yourPassword");`.

**Q : Où puis‑je trouver plus d’exemples ?**  
R : La documentation officielle d’Aspose.CAD et le dépôt d’exemples contiennent de nombreux scénarios supplémentaires.

## FAQ's (Original)

### Q1 : Aspose.CAD est‑il compatible avec tous les formats de fichiers CAD ?

R1 : Oui, Aspose.CAD prend en charge un large éventail de formats CAD, assurant une grande polyvalence dans le traitement de différents types de fichiers.

### Q2 : Puis‑je personnaliser les paramètres d’exportation PDF ?

R2 : Absolument. Comme montré dans le tutoriel, vous pouvez ajuster des options telles que les dimensions de page et les mises en page selon vos besoins.

### Q3 : Où puis‑je obtenir un support ou une assistance supplémentaire ?

R3 : Visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) pour le support communautaire et les discussions.

### Q4 : Existe‑t‑il un essai gratuit ?

R4 : Oui, vous pouvez accéder à l’essai gratuit [ici](https://releases.aspose.com/).

### Q5 : Comment obtenir une licence temporaire ?

R5 : Obtenez une licence temporaire [ici](https://purchase.aspose.com/temporary-license/).

## Conclusion

Dans ce tutoriel, nous avons exploré comment **convertir CAD PDF** en tirant parti d’Aspose.CAD pour Java. En quelques lignes de code, vous pouvez charger un dessin DGN, affiner les options d’exportation PDF et générer des PDF de haute qualité prêts à être partagés ou archivés. N’hésitez pas à expérimenter avec différentes tailles de page, mises en page ou traitements par lots pour répondre aux exigences de votre projet.

---

**Dernière mise à jour :** 2026-05-04  
**Testé avec :** Aspose.CAD pour Java 24.12  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}