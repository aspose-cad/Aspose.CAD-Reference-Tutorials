---
date: 2026-02-28
description: Apprenez à convertir des fichiers DWG en PDF avec Aspose.CAD pour Java,
  en créant rapidement et avec précision des fichiers conformes aux normes PDF/A1a
  et PDF/A1b.
linktitle: DWG to Compliance PDF
second_title: Aspose.CAD Java API
title: Convertir DWG en PDF (PDF/A1a et A1b) avec Aspose.CAD pour Java
url: /fr/java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
weight: 11
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PDF (PDF/A1a & A1b) avec Aspose.CAD pour Java

## Introduction

Dans les flux de travail modernes d’ingénierie et de conception, **convert DWG to PDF** est une exigence quotidienne pour le partage, l’archivage et la conformité aux formats de documents standard de l’industrie. PDF/A‑1a et PDF/A‑1b sont les normes d’archivage les plus largement acceptées, garantissant que vos dessins s’afficheront de la même manière sur n’importe quel système. Aspose.CAD pour Java rend cette conversion simple, fiable et entièrement programmable. Dans ce tutoriel, vous apprendrez exactement comment convertir des fichiers DWG en PDF conformes PDF/A en quelques lignes de code Java.

## Réponses rapides
- **Quelle bibliothèque gère la conversion ?** Aspose.CAD for Java  
- **Quelles normes PDF/A sont prises en charge ?** PDF/A‑1a et PDF/A‑1b  
- **Ai‑je besoin d’une licence pour les tests ?** Oui – une licence temporaire est disponible auprès d’Aspose.  
- **Quelle est la version minimale de Java ?** Java 8 ou supérieure est recommandée.  
- **Puis‑je traiter par lots plusieurs fichiers DWG ?** Absolument – répétez les étapes pour chaque fichier ou parcourez un dossier.

## Qu’est‑ce que « convertir DWG en PDF » et pourquoi est‑ce important ?
Convertir un dessin DWG en PDF crée un document universellement visualisable tout en préservant la fidélité vectorielle. Lorsque vous choisissez la conformité PDF/A‑1a ou PDF/A‑1b, le fichier intègre également les profils de couleur, les polices et les métadonnées requises pour un archivage à long terme, ce qui est essentiel pour les soumissions réglementaires, la documentation de construction et les livrables client.

## Pourquoi utiliser Aspose.CAD pour Java ?
- **Prise en charge complète des versions DWG** – des anciennes R12 aux dernières versions.  
- **Aucune dépendance externe** – la bibliothèque fonctionne prête à l’emploi, aucun logiciel CAD requis.  
- **Contrôle fin** – vous pouvez définir les options de rasterisation, le DPI, la taille de page et la conformité PDF/A.  
- **Haute performance** – adaptée au traitement par lots de milliers de dessins.

## Prérequis

Avant de commencer, assurez-vous d’avoir :

- Un environnement de développement Java (JDK 8 ou plus récent) avec votre IDE préféré.  
- La bibliothèque Aspose.CAD for Java – téléchargez‑la depuis le [download link](https://releases.aspose.com/cad/java/).  
- Un dossier contenant les dessins DWG que vous souhaitez convertir.

## Importer les espaces de noms

Tout d’abord, importez les classes dont vous avez besoin. Garder les imports en haut du fichier rend le code plus lisible et plus facile à maintenir.

```java
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;
```

## Étape 1 : Définir le répertoire des ressources

Définissez le chemin où se trouvent vos fichiers DWG. Ajustez la chaîne pour qu’elle pointe vers votre répertoire réel.

```java
String dataDir = "Your Document Directory" + "DWGDrawings/";
```

## Étape 2 : Charger le fichier DWG

Utilisez `Image.load` pour lire le fichier DWG en mémoire. Cet objet sera ensuite enregistré en PDF.

```java
String srcFile = dataDir + "Bottom_plate.dwg";
Image objImage = Image.load(srcFile);
```

## Étape 3 : Créer les options PDF

Créez une instance de `PdfOptions` et associez‑lui un objet `CadRasterizationOptions`. Les options de rasterisation vous permettent de contrôler la façon dont les données vectorielles sont rendues dans le PDF.

```java
PdfOptions pdfOptions = new PdfOptions();
pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());
```

## Étape 4 : Définir les options PDF principales (Conformité)

Ici vous indiquez à Aspose.CAD le niveau de conformité PDF/A dont vous avez besoin. L’exemple commence avec PDF/A‑1a.

```java
pdfOptions.setCorePdfOptions(new PdfDocumentOptions());
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
```

## Étape 5 : Enregistrer le PDF avec conformité PDF/A‑1a

Enregistrez maintenant le fichier PDF sur le disque. Le fichier de sortie sera conforme à PDF/A‑1a, prêt pour l’archivage.

```java
objImage.save(dataDir + "Saved1.pdf", pdfOptions);
```

## Étape 6 : Modifier la conformité en PDF/A‑1b et enregistrer à nouveau

Si vous avez besoin de PDF/A‑1b à la place, il suffit de changer le drapeau de conformité et d’enregistrer un second fichier.

```java
pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
objImage.save(dataDir + "Saved.pdf", pdfOptions);
```

> **Astuce :** Encapsulez la logique de conversion dans une méthode réutilisable afin de pouvoir l’appeler pour chaque DWG dans un dossier, réduisant le code répétitif et améliorant la maintenabilité.

## Cas d’utilisation courants

| Scénario | Pourquoi PDF/A ? |
|----------|------------------|
| **Soumissions réglementaires** | Garantit une lisibilité à long terme et une admissibilité légale. |
| **Livrables client** | Les clients peuvent ouvrir le fichier sans aucun logiciel CAD. |
| **Systèmes de gestion documentaire** | Les fichiers PDF/A sont indexés et recherchables dans la plupart des plateformes DMS. |

## Problèmes courants et solutions

- **Polices ou symboles manquants** – Assurez‑vous que le fichier DWG intègre toutes les polices requises, ou définissez `CadRasterizationOptions.setEmbedFonts(true)`.  
- **Taille de fichier importante** – Réduisez le DPI dans les options de rasterisation ou activez la compression via `PdfDocumentOptions.setCompress(true)`.  
- **Licence introuvable** – Appliquez une licence temporaire ou permanente avant la conversion ; sinon vous obtiendrez un filigrane.

## Questions fréquentes

**Q : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?**  
R : Aspose.CAD prend en charge un large éventail de versions DWG, y compris les dernières versions. Consultez la [documentation](https://reference.aspose.com/cad/java/) pour une liste détaillée de compatibilité.

**Q : Puis‑je personnaliser les paramètres de sortie PDF ?**  
R : Absolument ! Des options telles que la taille de page, le DPI, la rasterisation vectorielle et la conformité PDF/A sont toutes configurables via `PdfOptions` et `CadRasterizationOptions`.

**Q : Une licence temporaire est‑elle disponible pour les tests ?**  
R : Oui, vous pouvez obtenir une licence temporaire d’évaluation via [ce lien](https://purchase.aspose.com/temporary-license/).

**Q : Où puis‑je obtenir du support communautaire ?**  
R : Le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19) est un excellent endroit pour poser des questions et partager des expériences.

**Q : Puis‑je essayer Aspose.CAD gratuitement avant d’acheter ?**  
R : Bien sûr ! Téléchargez la version d’essai gratuite depuis [ici](https://releases.aspose.com/) pour explorer l’ensemble complet des fonctionnalités.

---

**Dernière mise à jour :** 2026-02-28  
**Testé avec :** Aspose.CAD for Java 24.11 (latest at time of writing)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}