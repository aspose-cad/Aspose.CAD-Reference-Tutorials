---
date: 2026-04-06
description: Apprenez à convertir DWG en PDF et à ajouter du texte personnalisé en
  utilisant C# et Aspose.CAD. Ce guide étape par étape couvre la génération de PDF
  à partir de DWG, l’insertion d’une entité texte et la modification de la police
  du texte DWG.
keywords:
- convert dwg to pdf
- generate pdf from dwg
- insert text entity
- change dwg text font
- aspose cad dwg pdf
linktitle: Ajouter du texte aux fichiers DWG en C#
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG en PDF et ajouter du texte en C# – Tutoriel Aspose.CAD
url: /fr/net/dwg-file-manipulation/adding-text-to-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Convertir DWG en PDF et ajouter du texte en C# – Tutoriel Aspose.CAD

## Introduction

Dans le monde en évolution rapide du CAD et du développement .NET, **convertir DWG en PDF** tout en insérant des annotations personnalisées est une exigence fréquente. Que vous deviez générer des dessins imprimables pour des clients ou intégrer des notes dynamiques directement dans un DWG, Aspose.CAD rend la tâche simple. Dans ce tutoriel, vous apprendrez à **convertir DWG en PDF**, **ajouter une entité texte**, et même **modifier la police du texte DWG** en C#.

## Réponses rapides
- **Quelle bibliothèque est la meilleure pour la conversion DWG‑vers‑PDF ?** Aspose.CAD for .NET  
- **Puis‑je ajouter du texte personnalisé lors de la conversion ?** Oui – créez une entité `CadText` et ajoutez‑la avant l’enregistrement.  
- **Ai‑je besoin d’une licence pour une utilisation en production ?** Une licence commerciale est requise ; un essai gratuit est disponible.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Est‑il possible de changer la police du texte ?** Oui, ajustez les propriétés `CadText` telles que `StyleType` et `TextHeight`.

## Qu’est‑ce que « convertir dwg en pdf » ?

Convertir un fichier DWG en PDF transforme un dessin CAD vectoriel en un document largement partageable et indépendant du dispositif. Le PDF conserve la géométrie et les calques d’origine, tout en vous permettant d’y intégrer des annotations, du texte ou d’autres métadonnées. Aspose.CAD gère automatiquement la rasterisation et le rendu vectoriel, vous n’avez donc pas besoin de logiciel CAD tiers sur le serveur.

## Pourquoi ajouter du texte à un DWG avant la conversion ?

Intégrer du texte directement dans le DWG vous donne un contrôle total sur le placement, le style et l’affectation au calque. Lorsque le fichier est ensuite converti en PDF, le texte apparaît exactement où vous l’avez positionné, préservant l’intention de conception et éliminant le besoin de post‑traitement dans un éditeur PDF.

## Prérequis

Avant de commencer, assurez‑vous d’avoir :

- **Bibliothèque Aspose.CAD** – téléchargez‑la depuis le [download link](https://releases.aspose.com/cad/net/).  
- **Un environnement .NET fonctionnel** (Visual Studio 2022, .NET 6, ou toute version compatible).  
- **Un dossier pour vos fichiers de test** – nous le désignerons `MyDir` tout au long du guide.

Maintenant, parcourons le processus étape par étape.

## Importer les espaces de noms

Ajoutez les instructions `using` requises afin de pouvoir accéder aux classes Aspose.CAD.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadObjects;
using Aspose.CAD.FileFormats.Cad.CadConsts;
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.FileFormats.Cad.CadObjects.AttEntities;
using Aspose.CAD.ImageOptions;
```

## Étape 1 : charger le fichier DWG

Chargez votre fichier DWG source dans un objet `Image`. Cet objet vous donne accès aux entités CAD sous‑jacentes.

```csharp
string dwgPathToFile = MyDir + "SimpleEntites.dwg";
using (Image image = Image.Load(dwgPathToFile))
{
    // Subsequent steps will be performed inside this block
}
```

## Étape 2 : créer un objet CadText (insérer une entité texte)

La classe `CadText` représente une ligne de texte dans un DWG. Ici, nous définissons son style, sa valeur, sa couleur, son calque et sa position. Ajustez `StyleType` ou `TextHeight` pour **modifier la police du texte DWG**.

```csharp
CadText cadText = new CadText();
cadText.StyleType = "Standard";          // Font/style – change to alter DWG text font
cadText.DefaultValue = "Some custom text";
cadText.ColorId = 256;                    // 256 = ByLayer (you can use a specific ACI color)
cadText.LayerName = "0";
cadText.FirstAlignment.X = 47.90;
cadText.FirstAlignment.Y = 5.56;
cadText.TextHeight = 0.8;                 // Height influences visual size
cadText.ScaleX = 0.0;
```

## Étape 3 : ajouter l’entité texte à l’espace modèle

L’espace modèle du DWG contient la plupart des entités du dessin. En ajoutant notre `CadText` au bloc `*Model_Space`, le texte devient partie intégrante du dessin.

```csharp
CadImage cadImage = (CadImage)image;
cadImage.BlockEntities["*Model_Space"].AddEntity(cadText);
```

## Étape 4 : configurer les options PDF (générer un PDF à partir du DWG)

Configurez les options de rasterisation qui contrôlent la façon dont le DWG est rendu en PDF. Vous pouvez ajuster la taille de page, le type de dessin et la mise en page.

```csharp
PdfOptions pdfOptions = new PdfOptions();
CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
pdfOptions.VectorRasterizationOptions = cadRasterizationOptions;
cadRasterizationOptions.DrawType = CadDrawTypeMode.UseObjectColor;
cadRasterizationOptions.PageHeight = 1600;
cadRasterizationOptions.PageWidth = 1600;
cadRasterizationOptions.Layouts = new string[] { "Model" };
```

## Étape 5 : enregistrer le DWG modifié en PDF

Enfin, exportez le dessin modifié. Le PDF résultant inclut le texte nouvellement inséré.

```csharp
image.Save(MyDir + "SimpleEntites_generated.pdf", pdfOptions);
```

> **Astuce :** Si vous avez besoin d’un PDF à plus haute résolution, augmentez proportionnellement `PageHeight` et `PageWidth`.

## Problèmes courants et solutions

| Problème | Raison | Solution |
|----------|--------|----------|
| Le texte n’apparaît pas dans le PDF | Mauvaise couche ou ID de couleur | Assurez‑vous que `LayerName` existe et que `ColorId` est réglé sur une couleur visible (par ex., 7 pour blanc). |
| Le texte est mal placé | Coordonnées d’alignement incorrectes | Vérifiez les valeurs `FirstAlignment.X/Y` par rapport aux unités du dessin. |
| Le PDF est vide | Options de rasterisation non définies | Définissez `DrawType` sur `UseObjectColor` ou `UseObjectLineWeight`. |

## Questions fréquemment posées (existantes)

### Q1 : Aspose.CAD est‑il compatible avec toutes les versions de fichiers DWG ?

R1 : Aspose.CAD prend en charge un large éventail de versions de fichiers DWG, garantissant la compatibilité avec divers logiciels CAD.

### Q2 : Puis‑je ajouter plusieurs entités texte à un même fichier DWG en utilisant Aspose.CAD ?

R2 : Oui, vous pouvez ajouter plusieurs entités texte à un fichier DWG en répétant le processus décrit dans le tutoriel.

### Q3 : Comment puis‑je changer la police et le style du texte dans Aspose.CAD ?

R3 : Pour modifier la police et le style du texte, ajustez les propriétés de l’objet `CadText` avant de l’ajouter au fichier DWG.

### Q4 : Existe‑t‑il des considérations de licence pour l’utilisation d’Aspose.CAD dans un projet commercial ?

A5 : Oui, assurez‑vous de respecter les conditions de licence d’Aspose.CAD. Consultez [Aspose.CAD Purchase](https://purchase.aspose.com/buy) pour plus de détails.

### Q5 : Où puis‑je obtenir de l’aide ou discuter des questions liées à Aspose.CAD ?

A5 : Visitez le [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour rejoindre la communauté et obtenir du support.

## FAQ supplémentaires

**Q : Comment générer un PDF à partir d’un DWG sans ajouter de texte ?**  
R : Ignorez l’étape de création du `CadText` et configurez directement `PdfOptions` avant d’appeler `image.Save(...)`.

**Q : Puis‑je changer la couleur du texte par programmation ?**  
R : Oui, définissez `cadText.ColorId` sur un numéro de couleur ACI spécifique (par ex., 1 pour rouge).

**Q : Est‑il possible d’insérer du texte multiligne ?**  
R : Utilisez `CadMText` pour des blocs de texte multiligne ; l’approche est similaire à `CadText`.

**Q : Aspose.CAD prend‑il en charge la conversion par lots de plusieurs fichiers DWG ?**  
R : Absolument – parcourez un répertoire de fichiers DWG, appliquez les mêmes étapes et enregistrez chacun en PDF.

## Conclusion

Vous disposez maintenant d’un flux de travail complet, prêt pour la production, pour **convertir DWG en PDF**, **ajouter du texte personnalisé**, et **personnaliser l’apparence du texte** en utilisant C# et Aspose.CAD. Cette technique est idéale pour la génération automatisée de dessins, les pipelines de reporting, ou tout scénario où vous devez enrichir des fichiers CAD à la volée.

---

**Dernière mise à jour :** 2026-04-06  
**Testé avec :** Aspose.CAD 24.11 for .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}