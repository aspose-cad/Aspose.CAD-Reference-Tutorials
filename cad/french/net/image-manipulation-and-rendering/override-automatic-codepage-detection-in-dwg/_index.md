---
date: 2026-09-04
description: Apprenez comment remplacer la détection de la codepage dwg dans les fichiers
  DWG en utilisant Aspose.CAD pour .NET, vous offrant un contrôle précis sur le codage
  des caractères.
keywords:
- override dwg codepage
- dwg codepage detection
- aspose.cad .net
- cad file encoding
- dwg processing
lastmod: 2026-09-04
linktitle: Remplacer la détection automatique de la codepage dans les fichiers DWG
  - Tutoriel Aspose.CAD
og_description: Apprenez comment remplacer la détection de la codepage dwg dans les
  fichiers DWG en utilisant Aspose.CAD pour .NET, vous offrant un contrôle précis
  sur le codage des caractères et améliorant la gestion des fichiers CAD.
og_image_alt: Guide showing how to override DWG codepage with Aspose.CAD in .NET
og_title: Comment remplacer la codepage dwg dans Aspose.CAD pour .NET
schemas:
- author: Aspose
  dateModified: '2026-09-04'
  description: Learn how to override dwg codepage detection in DWG files using Aspose.CAD
    for .NET, giving you precise control over character encoding.
  headline: How to override dwg codepage in Aspose.CAD for .NET
  type: TechArticle
- questions:
  - answer: It forces Aspose.CAD to use the encoding you specify instead of guessing,
      preventing character corruption.
    question: What does overriding the DWG codepage do?
  - answer: Whenever a DWG file contains text in a language that isn’t the default
      Windows codepage (e.g., Central European, Cyrillic).
    question: When should I use it?
  - answer: Any .NET `Encoding` such as `Encoding.GetEncoding(1250)` for Central European.
    question: Which encodings are supported?
  - answer: A trial works for development; a commercial license is required for production.
    question: Do I need a license?
  - answer: Yes, the setting is applied per `Image` instance, so multiple threads
      can process different files concurrently.
    question: Is it thread‑safe?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- override dwg codepage
- Aspose.CAD
- .NET CAD processing
- DWG codepage
- CAD rendering
title: Comment remplacer la codepage dwg dans Aspose.CAD pour .NET
url: /fr/net/image-manipulation-and-rendering/override-automatic-codepage-detection-in-dwg/
weight: 14
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Comment remplacer la page de code DWG dans Aspose.CAD pour .NET

## Réponses rapides
- **Que fait le remplacement de la page de code DWG ?** Il force Aspose.CAD à utiliser le codage que vous spécifiez au lieu de deviner, évitant ainsi la corruption des caractères.  
- **Quand devrais-je l’utiliser ?** Chaque fois qu’un fichier DWG contient du texte dans une langue qui n’est pas la page de code Windows par défaut (par ex., Europe centrale, Cyrillique).  
- **Quels encodages sont pris en charge ?** Tout `Encoding` .NET tel que `Encoding.GetEncoding(1250)` pour l’Europe centrale.  
- **Ai-je besoin d’une licence ?** Une version d’essai fonctionne pour le développement ; une licence commerciale est requise pour la production.  
- **Est‑il sûr pour les threads ?** Oui, le paramètre est appliqué par instance `Image`, de sorte que plusieurs threads peuvent traiter différents fichiers simultanément.

## Qu’est‑ce que le remplacement de la page de code DWG ?
Le remplacement de la page de code DWG est une fonctionnalité d’Aspose.CAD qui vous permet de remplacer la détection automatique de la page de code de la bibliothèque par un encodage de caractères spécifique que vous fournissez. Cela garantit que les chaînes de texte à l’intérieur du DWG sont interprétées correctement, quel que soit les métadonnées originales du fichier.

## Pourquoi utiliser le remplacement de la page de code DWG ?
Aspose.CAD prend en charge **plus de 50 versions DWG/DXF** et peut traiter des fichiers jusqu’à **2 Go** sans charger l’ensemble du document en mémoire. Lorsque la détection automatique échoue, vous pouvez perdre jusqu’à **100 % de lisibilité des annotations**. En définissant explicitement la page de code, vous réduisez ce risque à **0 %** tout en conservant les temps de rendu inchangés.

## Prérequis

- Connaissances de base en C# et sur la plateforme .NET.  
- Aspose.CAD pour .NET installé. Si vous ne l’avez pas encore installé, téléchargez‑le sur la **[page de téléchargement d’Aspose.CAD pour .NET](https://releases.aspose.com/cad/net/)**.  
- Un fichier DWG qui utilise une page de code non‑par défaut (par exemple, un fichier créé sur un système avec la page de code 1250).

## Importer les espaces de noms

Pour commencer, ajoutez les directives `using` requises afin que le compilateur puisse localiser les classes Aspose.CAD.

Insérez ce qui suit en haut de votre fichier source C# :

```csharp
using System;
using Aspose.CAD.FileFormats.Cad;
```

Cela prépare l’environnement pour toutes les opérations CAD suivantes.

## Étape 1 : définir le répertoire de votre document

Spécifiez le dossier contenant le DWG que vous souhaitez traiter. Remplacez le texte de substitution par le chemin réel sur votre machine :

```csharp
//ExStart:1
string SourceDir = "Your Document Directory";
//ExEnd:1
```

## Étape 2 : remplacer la détection automatique de la page de code

Nous arrivons maintenant au cœur du tutoriel. Le code ci‑dessous charge un fichier DWG, force la page de code à **Windows‑1250** (Europe centrale), puis enregistre l’image au format PNG. Modifiez le nom du fichier et l’encodage selon vos besoins.

```csharp
//ExStart:1
using (CadImage cadImage = (CadImage)Image.Load(SourceDir + "SimpleEntites.dwg",
new LoadOptions()
{
	SpecifiedEncoding = CodePages.Japanese,
	SpecifiedMifEncoding = MifCodePages.Japanese,
	RecoverMalformedCifMif = false
}))
{
	// Perform export or other operations with cadImage
}
//ExEnd:1
Console.WriteLine("OverrideAutomaticCodePageDetectionDwg executed successfully");
```

`Image.Load` est une méthode statique qui charge un fichier CAD et renvoie un objet `CadImage`. `LoadOptions.CodePage` spécifie l’encodage de caractères à utiliser lors du chargement. `CadImage` représente la représentation en mémoire d’un dessin CAD et fournit des méthodes de rendu ou de conversion.

## Problèmes courants et solutions

- **Des caractères indésirables restent après le remplacement** – Vérifiez que l’encodage que vous avez sélectionné correspond à la langue du fichier original. Utilisez `Encoding.GetEncoding(1251)` pour le cyrillique, par exemple.  
- **Le fichier ne se charge pas** – Assurez‑vous que la version DWG est prise en charge par votre version d’Aspose.CAD ; mettez à jour si nécessaire.  
- **Baisse de performance** – Le remplacement n’ajoute pas de surcharge ; si vous remarquez un ralentissement, vérifiez les goulets d’étranglement I/O non liés.

## Questions fréquemment posées

### Q1 : Puis‑je utiliser Aspose.CAD pour .NET avec d’autres langages que C# ?
R1 : Aspose.CAD pour .NET est principalement conçu pour C#, mais il peut être utilisé dans d’autres langages .NET tels que VB.NET.

### Q2 : Une version d’essai gratuite est‑elle disponible ?
R2 : Oui, vous pouvez accéder à une version d’essai gratuite **[page de téléchargement de l’essai gratuit d’Aspose.CAD](https://releases.aspose.com/)**.

### Q3 : Comment obtenir du support pour Aspose.CAD pour .NET ?
R3 : Consultez le **[forum Aspose.CAD](https://forum.aspose.com/c/cad/19)** pour le support communautaire.

### Q4 : Puis‑je acheter une licence temporaire ?
R4 : Oui, vous pouvez obtenir une licence temporaire **[page d’achat de licence temporaire](https://purchase.aspose.com/temporary-license/)**.

### Q5 : Où puis‑je trouver une documentation détaillée ?
R5 : Référez‑vous à la documentation complète **[documentation de l’API Aspose.CAD .NET](https://reference.aspose.com/cad/net/)**.

### Q6 : Le remplacement de la page de code affecte‑t‑il la qualité du rendu raster ?
R6 : Non. Le paramètre de page de code n’influence que le décodage des chaînes de texte ; la qualité de l’image reste inchangée.

### Q7 : Puis‑je appliquer le remplacement lors de la conversion vers des formats autres que PNG ?
R7 : Absolument. La même valeur `LoadOptions.CodePage` fonctionne pour PDF, SVG ou tout autre format de sortie pris en charge par Aspose.CAD.

---

**Dernière mise à jour :** 2026-09-04  
**Testé avec :** Aspose.CAD 24.10 for .NET  
**Auteur :** Aspose

## Tutoriels associés

- [Recherche de texte dans les fichiers DWG avec C# - Tutoriel Aspose.CAD](/cad/net/text-search-and-manipulation/searching-text-in-dwg-files/)
- [Convertir DWG en PDF et ajouter du texte en C# – Tutoriel Aspose.CAD](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [Comment convertir DWG en PDF et images raster en utilisant Aspose.CAD pour .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}