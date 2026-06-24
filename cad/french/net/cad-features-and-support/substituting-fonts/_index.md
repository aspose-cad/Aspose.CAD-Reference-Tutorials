---
date: 2026-03-29
description: Apprenez à remplacer rapidement les polices dans Aspose.CAD pour .NET.
  Ce guide étape par étape vous montre comment définir le nom de police principal
  et personnaliser efficacement les dessins CAD.
linktitle: Substituting Fonts
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment remplacer les polices dans Aspose.CAD pour .NET
url: /fr/net/cad-features-and-support/substituting-fonts/
weight: 17
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment remplacer les polices dans Aspose.CAD pour .NET

## Introduction

Dans le domaine du développement CAD avec .NET, apprendre **comment remplacer les polices** est une compétence cruciale qui peut améliorer considérablement la qualité visuelle de vos dessins. Aspose.CAD pour .NET propose une API simple qui vous permet de **définir le nom de police principal** pour n'importe quel style, rendant la substitution de police globale ou sélective très facile. Dans ce tutoriel, nous parcourrons l'ensemble du processus — du chargement d'un dessin à l'échange de polices, que ce soit globalement ou par nom de style spécifique.

## Réponses rapides
- **Quelle est la classe principale pour la manipulation CAD ?** `Aspose.CAD.Image` (ou son dérivé `CadImage`).
- **Quelle propriété modifie la police ?** `PrimaryFontName` sur `CadStyleTableObject`.
- **Puis‑je remplacer les polices pour tous les styles en même temps ?** Oui, parcourez `cadImage.Styles` et définissez la propriété.
- **Ai‑je besoin d’une licence pour la production ?** Une licence Aspose.CAD valide est requise pour une utilisation hors période d’essai.
- **Versions .NET prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.

## Qu'est-ce que la substitution de police dans le CAD ?
La substitution de police consiste à remplacer la police d'origine utilisée dans un dessin CAD par une autre disponible sur le système cible. Cela est particulièrement utile lorsque la police d'origine est manquante, lorsque vous avez besoin d'un style d'entreprise cohérent, ou lors de la préparation de dessins pour l'impression sur des appareils ne supportant qu'un ensemble limité de polices.

## Pourquoi remplacer les polices avec Aspose.CAD ?
- **Aucune dépendance externe** – la bibliothèque gère le mappage des polices en interne.
- **Fonctionne avec de nombreux formats** – DXF, DWG, DGN, et plus encore.
- **Contrôle programmatique** – automatisez le processus pour des conversions par lots ou des pipelines CI.
- **Préserve la géométrie du dessin** – seule la représentation visuelle du texte change.

## Prérequis

- Connaissances de base en programmation .NET.
- Aspose.CAD pour .NET installé. Si vous ne l’avez pas encore installé, téléchargez‑le [ici](https://releases.aspose.com/cad/net/).
- Un fichier de dessin CAD (DXF, DWG, etc.) pour expérimenter.

## Importer les espaces de noms

Avant de commencer, importez les espaces de noms nécessaires pour accéder aux fonctionnalités Aspose.CAD dans votre application .NET.

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Aspose.CAD;
using Aspose.CAD.FileFormats.Cad.CadTables;
```

## Étape 1 : charger le dessin CAD

Commencez par charger le dessin CAD dans une instance de `CadImage`. Assurez‑vous de fournir le chemin correct vers le répertoire de votre document.

```csharp
string MyDir = "Your Document Directory";
string sourceFilePath = MyDir + "conic_pyramid.dxf";

using (CadImage cadImage = (CadImage)Aspose.CAD.Image.Load(sourceFilePath))
{
    // Your code for further actions goes here
}
```

## Étape 2 : parcourir les styles

Ensuite, parcourez les styles du dessin CAD à l’aide d’une boucle `foreach`. Cela vous permet d’accéder et de manipuler chaque style de police individuellement.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    // Your code for style manipulation goes here
}
```

## Comment définir le nom de police principal pour la substitution de police

La propriété `PrimaryFontName` sur chaque `CadStyleTableObject` contrôle la police utilisée lors du rendu du dessin. En définissant cette propriété, vous remplacez effectivement la police d'origine.

### Étape 3 : substituer les polices globalement

Pour remplacer les polices pour **tous** les styles, définissez la propriété `PrimaryFontName` de chaque style sur le nom de police souhaité, par exemple, `"Arial"`.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    style.PrimaryFontName = "Arial";
}
```

### Étape 4 : substituer la police par nom de style

Si vous ne devez remplacer la police que pour un style spécifique (par ex., le style nommé `"Roman"`), ajoutez une condition à l’intérieur de la boucle.

```csharp
foreach (CadStyleTableObject style in cadImage.Styles)
{
    if (style.StyleName == "Roman")
    {
        style.PrimaryFontName = "Arial";
    }
}
```

## Problèmes courants et dépannage

| Problème | Cause | Correction |
|----------|-------|------------|
| La police ne change pas après l'exécution du code | Le dessin est mis en cache ou ouvert en mode lecture seule | Assurez‑vous d’enregistrer l’image après modification (`cadImage.Save(...)`) ou rechargez le fichier pour vérifier. |
| La police souhaitée n’est pas trouvée sur le système | Police non installée sur la machine exécutant le code | Installez la police TrueType/OpenType requise ou intégrez‑la dans les ressources de l’application. |
| Le texte apparaît illisible | Encodage incorrect ou prise en charge Unicode manquante | Utilisez une police qui supporte le jeu de caractères requis (par ex., Arial Unicode MS). |

## Questions fréquemment posées

**Q : Puis‑je annuler les modifications de police dans Aspose.CAD pour .NET ?**  
R : Oui, vous pouvez revenir en chargeant à nouveau le dessin CAD original ou en conservant une copie de sauvegarde avant d’apporter des modifications.

**Q : Existe‑t‑il d’autres propriétés de police que je peux modifier ?**  
R : Absolument. En plus de `PrimaryFontName`, vous pouvez travailler avec `SecondaryFontName`, `FontFamily` et d’autres attributs liés aux styles pour une personnalisation avancée.

**Q : Aspose.CAD est‑il compatible avec différents formats CAD ?**  
R : Oui, Aspose.CAD prend en charge une large gamme de formats tels que DXF, DWG, DGN, DWF, et plus encore, vous offrant une flexibilité sur tous vos projets.

**Q : Puis‑je automatiser la substitution de police en traitement par lots ?**  
R : Bien sûr. Enveloppez la logique de chargement et de substitution dans une boucle qui parcourt un dossier de fichiers CAD, ou intégrez‑la dans un pipeline CI/CD.

**Q : Où puis‑je trouver un support supplémentaire pour Aspose.CAD pour .NET ?**  
R : Pour un support supplémentaire et des discussions communautaires, visitez le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

---

**Dernière mise à jour :** 2026-03-29  
**Testé avec :** Aspose.CAD pour .NET (dernière version)  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}