---
description: Apprenez à convertir les fichiers DWG en PNG et à extraire les objets
  OLE des fichiers DWG à l'aide d'Aspose.CAD pour .NET – un guide rapide axé sur le
  code.
linktitle: Exporting OLE Objects from DWG Files
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Convertir DWG en PNG et exporter les objets OLE - Tutoriel Aspose.CAD
url: /fr/net/advanced-export-techniques/exporting-ole-objects-from-dwg/
weight: 12
---

/main-wrap-class >}} etc remain unchanged.

Now produce translation.

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Exportation d'objets OLE à partir de fichiers DWG - Tutoriel Aspose.CAD

## Introduction

Si vous devez **convertir DWG en PNG** tout en extrayant les objets OLE intégrés, vous êtes au bon endroit. Aspose.CAD pour .NET rend ce processus en deux étapes simple, vous permettant d’automatiser l’extraction et la rasterisation en quelques lignes de C#. Dans les quelques minutes qui suivent, nous parcourrons l’ensemble du flux de travail, de la configuration de votre environnement à l’enregistrement de chaque DWG en PNG contenant les données OLE extraites.

## Réponses rapides
- **Que couvre ce tutoriel ?** Conversion de DWG en PNG et extraction d’objets OLE à l’aide d’Aspose.CAD pour .NET.  
- **Ai‑je besoin d’une licence ?** Une version d’essai gratuite suffit pour le développement ; une licence commerciale est requise pour la production.  
- **Quelles versions de .NET sont prises en charge ?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6+.  
- **Puis‑je traiter plusieurs fichiers DWG en même temps ?** Oui – l’exemple parcourt un tableau de noms de fichiers.  
- **Où trouver plus d’exemples ?** Consultez la documentation officielle d’Aspose.CAD et les liens du forum ci‑dessous.

## Qu’est‑ce que **convert DWG to PNG** ?
Convertir un DWG (dessin AutoCAD) en image PNG rasterise les données vectorielles, ce qui facilite leur affichage ou leur intégration dans des pages web, des rapports ou d’autres applications qui ne supportent pas nativement le format DWG. Lorsque des objets OLE sont présents, ils peuvent être extraits et enregistrés comme actifs séparés pendant la conversion.

## Pourquoi extraire les objets OLE des fichiers CAD ?
De nombreux dessins DWG intègrent des feuilles de calcul, des graphiques ou d’autres documents Office sous forme d’objets OLE. Les extraire vous permet de réutiliser les données d’origine, d’automatiser les rapports ou de migrer le contenu vers des formats plus récents sans perdre les informations intégrées.

## Prérequis

- Bibliothèque Aspose.CAD pour .NET : assurez‑vous que la bibliothèque est installée. Vous pouvez la télécharger depuis la [page de téléchargement Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/).
- Répertoire de documents : créez un répertoire où vos fichiers DWG sont stockés. Remplacez `"Your Document Directory"` dans le fragment de code fourni par le chemin réel.

## Importer les espaces de noms

Dans votre projet .NET, importez les espaces de noms requis :

```csharp
using Aspose.CAD.FileFormats.Cad;
using Aspose.CAD.ImageOptions;
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

## Guide étape par étape

### Étape 1 : Définir le répertoire de documents

```csharp
string MyDir = "Your Document Directory";
```

Remplacez `"Your Document Directory"` par le chemin où vos fichiers DWG sont situés.

### Étape 2 : Lister les fichiers DWG à traiter

```csharp
string[] files = new string[] { "D ZD junior D10m H2m.dwg", "ZD - Senior D6m H2m45.dwg" };
```

### Étape 3 : Configurer les options d’exportation pour la conversion PNG

```csharp
PngOptions pngOptions = new PngOptions { };
CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
pngOptions.VectorRasterizationOptions = rasterizationOptions;
rasterizationOptions.Layouts = new string[] { "Layout1" };
```

Vous pouvez ajuster `CadRasterizationOptions` (par ex., `PageWidth`, `PageHeight`, `BackgroundColor`) pour correspondre à la résolution souhaitée.

### Étape 4 : Parcourir chaque DWG et effectuer la conversion

```csharp
foreach (string file in files)
{
    using (CadImage cadImage = (CadImage)Image.Load(MyDir + file))
    {
        cadImage.Save(MyDir + file + "_out.png", pngOptions);
    }
}
```

Durant cette boucle, la bibliothèque extrait automatiquement les **objets OLE** intégrés à chaque dessin et les inclut dans le PNG généré. Si vous avez besoin des flux OLE bruts, vous pouvez accéder à la collection `cadImage.OleObjects` – une façon pratique de **how to extract ole** les données programmatiquement.

## Problèmes courants & dépannage

- **Nom de mise en page manquant** – Assurez‑vous que la mise en page que vous spécifiez (`"Layout1"` dans l’exemple) existe dans le DWG source ; sinon le rasteriseur revient à l’espace modèle par défaut.
- **Fichiers volumineux provoquant une pression mémoire** – Traitez les fichiers un par un (comme montré) et libérez rapidement les objets `CadImage` avec `using`.
- **Couleurs inattendues** – Définissez `rasterizationOptions.BackgroundColor` pour correspondre à l’arrière‑plan du dessin si la transparence est requise.

## Foire aux questions

### Q1 : Aspose.CAD pour .NET convient‑il aux fichiers CAD junior et senior ?
R1 : Oui, Aspose.CAD pour .NET est polyvalent et peut gérer une large gamme de fichiers CAD, y compris les variantes junior et senior.

### Q2 : Puis‑je personnaliser les options d’exportation pour différentes mises en page ?
R2 : Absolument ! Comme illustré dans le tutoriel, vous pouvez adapter les options d’exportation, y compris les mises en page, selon vos besoins spécifiques.

### Q3 : Où puis‑je trouver la documentation détaillée d’Aspose.CAD pour .NET ?
R3 : Consultez la [documentation Aspose.CAD pour .NET](https://reference.aspose.com/cad/net/) pour des informations approfondies et des exemples.

### Q4 : Existe‑t‑il une version d’essai gratuite ?
R4 : Oui, vous pouvez tester les capacités d’Aspose.CAD pour .NET avec une version d’essai gratuite. Visitez [ce lien](https://releases.aspose.com/) pour commencer.

### Q5 : Comment obtenir du support ou rejoindre la communauté ?
R5 : Pour le support et l’engagement communautaire, rendez‑vous sur le [forum Aspose.CAD](https://forum.aspose.com/c/cad/19).

### Q6 : Comment **extraire OLE à partir de fichiers CAD** sans convertir en PNG ?
R6 : Utilisez la collection `CadImage.OleObjects` après avoir chargé le DWG ; vous pouvez parcourir chaque `OleObject` et enregistrer ses données brutes dans un fichier.

## Conclusion

Vous avez maintenant vu comment **convertir DWG en PNG** tout en **extraitant parfaitement les objets OLE** à l’aide d’Aspose.CAD pour .NET. Cette approche fait gagner du temps, élimine les étapes manuelles de copier‑coller et s’intègre proprement aux pipelines automatisés. N’hésitez pas à expérimenter d’autres formats raster (JPEG, BMP) ou à explorer l’ensemble riche de fonctionnalités de manipulation CAD proposées par Aspose.

---

**Dernière mise à jour :** 2026-03-13  
**Testé avec :** Aspose.CAD 24.11 pour .NET  
**Auteur :** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}