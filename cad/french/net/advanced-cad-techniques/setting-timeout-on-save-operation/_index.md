---
date: 2026-03-05
description: Apprenez à définir le délai d’attente lors des opérations d’enregistrement
  lors de la conversion de DWG en PDF avec Aspose.CAD pour .NET. Augmentez l’efficacité
  et le contrôle dans vos applications .NET.
linktitle: Setting Timeout on Save Operation
second_title: Aspose.CAD .NET - CAD and BIM File Format
title: Comment définir un délai d’attente lors de l’opération d’enregistrement - Tutoriel
  Aspose.CAD
url: /fr/net/advanced-cad-techniques/setting-timeout-on-save-operation/
weight: 12
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment définir un délai d'attente sur l'opération d'enregistrement - Tutoriel Aspose.CAD

## Introduction

Dans ce guide, vous apprendrez **comment définir un délai d'attente** sur les opérations d'enregistrement CAD, une technique qui vous aide à éviter que des conversions longues ne deviennent des processus non réactifs. La gestion du délai d'attente est particulièrement utile lorsque vous **convertissez DWG en PDF** ou **exportez des fichiers CAD PDF** dans des travaux batch ou des services web. Aspose.CAD pour .NET fournit une API propre qui vous permet de contrôler l'opération d'enregistrement tout en profitant de son puissant moteur de rasterisation.

## Quick Answers
- **Que contrôle le délai d'attente ?** Il interrompt l'opération d'enregistrement/exportation si elle dure plus longtemps que la période spécifiée.  
- **Quels formats en bénéficient le plus ?** La conversion de gros fichiers DWG en PDF ou en images raster où le temps de traitement peut varier.  
- **Ai-je besoin d'une licence ?** Une licence valide d'Aspose.CAD est requise pour une utilisation en production ; un essai gratuit suffit pour l'évaluation.  
- **Puis-je personnaliser la durée ?** Oui — il suffit de modifier la valeur de `Thread.Sleep` (en millisecondes) pour l'adapter à votre scénario.  
- **Cette approche est‑elle compatible avec l'asynchrone ?** L'exemple utilise `Task.Factory.StartNew`, ce qui facilite son intégration dans des flux de travail async.

## What is “how to set timeout” in the context of CAD saving?
Définir un délai d'attente signifie attacher un `InterruptionToken` aux options d'enregistrement et déclencher une interruption après un intervalle prédéfini. Cela empêche l'opération de rester bloquée indéfiniment, offrant des performances prévisibles et une meilleure gestion des ressources.

## Why use Aspose.CAD to convert DWG to PDF with a timeout?
- **Fiabilité :** Garantit qu'une conversion incontrôlée ne bloquera pas votre service.  
- **Scalabilité :** Vous permet de traiter de nombreux fichiers en parallèle sans craindre qu'un seul fichier n'arrête la chaîne.  
- **Qualité :** Conserve la rasterisation haute fidélité d'Aspose.CAD tout en ajoutant des contrôles de sécurité.

## Prerequisites

Avant de commencer, assurez-vous d'avoir les éléments suivants :

- **Aspose.CAD for .NET** – intégré à votre projet. Vous pouvez le télécharger [here](https://releases.aspose.com/cad/net/).
- **Document Directory** – un dossier où vos fichiers DWG source et les PDFs de sortie seront stockés.

## Import Namespaces

Tout d'abord, importez les espaces de noms qui fournissent les classes dont nous aurons besoin pour la rasterisation, les options PDF et le mécanisme d'interruption.

```csharp
using Aspose.CAD.ImageOptions;
using System;
using System.Threading;
using System.Threading.Tasks;
```

## How to Set Timeout on Save Operation

Voici un guide pas à pas. Chaque étape comprend une brève explication suivie du bloc de code original (inchangé).

### Step 1: Load CAD Drawing

Nous chargeons le fichier DWG source depuis le répertoire désigné. La méthode `Image.Load` renvoie un objet `Image` qui représente le dessin CAD.

```csharp
// Example: Loading CAD Drawing
string SourceDir = "Your Document Directory";
string OutputDir = "Your Document Directory";

using (Image cadDrawing = Image.Load(SourceDir + "Drawing11.dwg"))
{
    // Code for subsequent steps will be placed here
}
```

### Step 2: Configure Rasterization Options

Définissez les options de rasterisation afin que le PDF exporté corresponde aux dimensions du dessin original. C'est ici que vous contrôlez la largeur, la hauteur de la page et d'autres paramètres de rendu.

```csharp
// Example: Configuring Rasterization Options
var rasterizationOptions = new CadRasterizationOptions();
rasterizationOptions.PageWidth = cadDrawing.Size.Width;
rasterizationOptions.PageHeight = cadDrawing.Size.Height;
```

### Step 3: Create PDF Options (Export CAD PDF)

Créez une instance de `PdfOptions` et attachez les paramètres de rasterisation. Cet objet sera passé à la méthode `Save` pour générer une version PDF du fichier DWG.

```csharp
// Example: Creating PDF Options
PdfOptions CADf = new PdfOptions();
CADf.VectorRasterizationOptions = rasterizationOptions;
```

### Step 4: Implement Timeout Mechanism

Nous utilisons `InterruptionTokenSource` pour obtenir un token pouvant interrompre l'opération d'enregistrement. Une tâche en arrière‑plan effectue l'exportation, tandis que le thread principal dort pendant la durée du délai d'attente souhaitée (par ex., 10 seconds). Après le sommeil, nous appelons `Interrupt()` pour annuler l'opération si elle est toujours en cours.

```csharp
// Example: Implementing Timeout Mechanism
using (var its = new InterruptionTokenSource())
{
    CADf.InterruptionToken = its.Token;

    var exportTask = Task.Factory.StartNew(() =>
    {
        cadDrawing.Save(OutputDir + "PutTimeoutOnSave_out.pdf", CADf);
    });

    Thread.Sleep(10000); // Set your desired timeout duration in milliseconds
    its.Interrupt();

    exportTask.Wait();
}
```

### Step 5: Finalize and Confirm

Après l'exportation (ou l'interruption), écrivez un message de confirmation dans la console. Dans une application réelle, vous pourriez journaliser le résultat ou déclencher un événement.

```csharp
// Example: Finalizing and Confirming
Console.WriteLine("PutTimeoutOnSave executed successfully");
```

## Common Issues and Solutions

| Problème | Cause | Solution |
|----------|-------|----------|
| L'exportation se bloque indéfiniment | Aucun token d'interruption attaché | Assurez‑vous que `CADf.InterruptionToken = its.Token;` est défini avant de démarrer la tâche. |
| Le PDF est vide ou corrompu | Chemin du répertoire de sortie incorrect | Vérifiez que `OutputDir` se termine par un séparateur de chemin et que le nom de fichier est valide. |
| Délai d'attente trop court, entraînant un arrêt prématuré | Valeur de `Thread.Sleep` trop basse pour les gros fichiers | Augmentez la durée du sommeil ou calculez un délai d'attente adaptatif en fonction de la taille du fichier. |

## Frequently Asked Questions

**Q1 : Puis‑je personnaliser la durée du délai d'attente ?**  
R : Absolument. Modifiez la valeur passée à `Thread.Sleep` (en millisecondes) pour correspondre à vos attentes de performance.

**Q2 : Existe‑t‑il d'autres options de rasterisation ?**  
R : Oui. `CadRasterizationOptions` propose des propriétés comme `Resolution`, `BackgroundColor` et `DrawType` pour affiner la sortie PDF.

**Q3 : Comment gérer les interruptions dans mon application ?**  
R : Utilisez les classes `InterruptionToken` et `InterruptionTokenSource` comme illustré. Elles offrent un moyen thread‑safe d'interrompre les opérations longues.

**Q4 : Aspose.CAD convient‑il aux fichiers CAD 2D et 3D ?**  
R : Il prend en charge un large éventail de formats 2D et 3D, y compris DWG, DXF, DGN, et plus encore.

**Q5 : Où puis‑je trouver une assistance supplémentaire ou du support communautaire ?**  
R : Consultez le [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) pour des discussions communautaires, des exemples de code et des conseils de dépannage.

## Conclusion

En suivant les étapes ci‑dessus, vous savez maintenant **comment définir un délai d'attente** sur les opérations d'enregistrement CAD, vous permettant de convertir de manière fiable **DWG en PDF** ou **d'exporter des fichiers CAD PDF** sans risquer de processus non réactifs. Intégrez ce modèle dans des convertisseurs batch, des services web ou tout pipeline automatisé où la prévisibilité est importante.

---

**Last Updated:** 2026-03-05  
**Tested With:** Aspose.CAD 24.12 for .NET  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}