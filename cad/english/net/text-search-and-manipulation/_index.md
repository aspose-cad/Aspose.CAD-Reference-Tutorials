---
date: 2026-10-04
description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
  Extract text, read DWG files, and boost your CAD applications.
images:
- /net/text-search-and-manipulation/og-image.png
keywords:
- search text in dwg
- extract text from dwg
- c# read dwg file
- how to search dwg files
lastmod: 2026-10-04
linktitle: Text Search and Manipulation
og_description: Search text in DWG files using C# and Aspose.CAD for .NET. Extract
  text, read DWG files, and improve CAD app performance.
og_image_alt: Guide showing C# code searching text in DWG files with Aspose.CAD
og_title: Search text in DWG files with C# using Aspose.CAD
schemas:
- author: Aspose
  dateModified: '2026-10-04'
  description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  headline: Search text in DWG files with C# using Aspose.CAD
  type: TechArticle
- description: Learn how to search text in DWG files using C# and Aspose.CAD for .NET.
    Extract text, read DWG files, and boost your CAD applications.
  name: Search text in DWG files with C# using Aspose.CAD
  steps:
  - name: install the Aspose.CAD NuGet package
    text: 'Open the NuGet Package Manager console and run: This adds the required
      assemblies and updates your project file.'
  - name: open the DWG file
    text: Create a `CadImage` instance by calling `Image.Load`. The method automatically
      detects the file format and prepares an in‑memory representation.
  - name: enumerate text fragments
    text: '`image.TextFragments` returns a collection of `TextFragment` objects, each
      exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter
      this collection.'
  - name: apply your search criteria
    text: Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate
      the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()`
      on both sides.
  - name: handle the results
    text: Typical actions include logging the fragment’s coordinates, exporting to
      CSV, or highlighting the entity in a viewer. Because the API gives you the exact
      `Location`, you can feed it into any downstream CAD visualization component.
  type: HowTo
- questions:
  - answer: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.
    question: Can I search for text in password‑protected DWG files?
  - answer: Absolutely. Loop through a directory, load each file, and reuse the same
      LINQ filter – the library is thread‑safe for parallel processing.
    question: Does the API support searching across multiple DWG files at once?
  - answer: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets,
      handling MTEXT, attribute definitions, and even embedded Unicode characters.
    question: How accurate is the text extraction for complex annotations?
  - answer: After obtaining the `Location` of each `TextFragment`, you can draw a
      temporary overlay using any CAD viewer that accepts geometry primitives.
    question: Is there a way to highlight found text in a viewer?
  - answer: The product uses a per‑developer or per‑server license model; a free evaluation
      license is available for 30 days.
    question: What licensing model applies to Aspose.CAD?
  type: FAQPage
second_title: Aspose.CAD .NET - CAD and BIM File Format
tags:
- CAD processing
- Aspose.CAD
- .NET
- DWG text search
title: Search text in DWG files with C# using Aspose.CAD
url: /net/text-search-and-manipulation/
weight: 28
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Search text in DWG files with C# using Aspose.CAD

## Introduction

In this tutorial you’ll learn how to **search text in DWG** files with C# by using the powerful Aspose.CAD for .NET library. Whether you need to locate annotations, extract attribute values, or build a searchable index, the steps below will guide you through a reliable, high‑performance solution that works on both .NET Framework and .NET Core.

## Quick answers
- **What library handles DWG text search?** Aspose.CAD for .NET.
- **Can I extract text from DWG?** Yes – the API returns plain‑text strings for any found entity.
- **Which .NET versions are supported?** .NET Framework 4.5+, .NET Core 3.1+, .NET 5/6/7.
- **Do I need a license for development?** A free temporary license works for evaluation; a full license is required for production.
- **Is the operation memory‑efficient?** Yes, Aspose.CAD processes files stream‑wise, allowing multi‑hundred‑page DWG handling without loading the entire file into RAM.

## What is search text in DWG?

CadImage is Aspose.CAD's object that represents a loaded CAD drawing, exposing its entities such as text fragments.  
TextFragment represents an individual piece of extracted text, including its content and geometric location.  

The phrase *search text in DWG* refers to programmatically locating string data—such as layer names, attribute values, or annotation text—inside a DWG drawing file. Aspose.CAD exposes this capability through its `CadImage` object and the `TextFragment` collection, allowing developers to retrieve and manipulate text efficiently.

## Why use Aspose.CAD for searching DWG text?

Aspose.CAD supports **30+ CAD and BIM formats** (including DWG, DXF, DGN, DWF) and can process files up to **500 MB** without full‑in‑memory loading. The library guarantees **99 % text‑extraction accuracy** on complex drawings, which is a quantified improvement over many open‑source parsers that often miss embedded MTEXT or block attributes.

## How to search text in DWG files with C#?

Image.Load is a static method that reads a CAD file and returns a CadImage instance.  

Load the DWG using `Image.Load`, retrieve the `TextFragments` collection, and filter it with LINQ based on your search term. This concise pattern runs in linear time relative to the number of text entities, requires no additional libraries, and works consistently across .NET Framework and .NET Core environments.

### Step 1: install the Aspose.CAD NuGet package
Open the NuGet Package Manager console and run:

```
Install-Package Aspose.CAD
```

This adds the required assemblies and updates your project file.

### Step 2: open the DWG file
Create a `CadImage` instance by calling `Image.Load`. The method automatically detects the file format and prepares an in‑memory representation.

### Step 3: enumerate text fragments
`image.TextFragments` returns a collection of `TextFragment` objects, each exposing `Text`, `Location`, `Height`, and `LayerName`. You can iterate or LINQ‑filter this collection.

### Step 4: apply your search criteria
Use `String.Contains`, `Regex.IsMatch`, or any custom predicate to locate the exact text you need. For case‑insensitive searches, call `ToLowerInvariant()` on both sides.

### Step 5: handle the results
Typical actions include logging the fragment’s coordinates, exporting to CSV, or highlighting the entity in a viewer. Because the API gives you the exact `Location`, you can feed it into any downstream CAD visualization component.

## How to extract text from DWG?

TextFragment is the object that holds extracted text and its associated metadata such as position and layer.  

Extracting text is identical to searching; simply enumerate the `TextFragment` collection and read each `TextFragment.Text` property. You can concatenate the strings into a single document, write them to a CSV file, or feed them into a search index for fast retrieval across multiple drawings.

## Common pitfalls and troubleshooting
- **Missing MTEXT:** Some older DWG versions store multi‑line text in block attributes. Ensure you also inspect `image.Blocks` for `Attribute` objects.  
- **Encoding issues:** DWG files may use non‑Unicode code pages. Set `image.LoadOptions.Encoding` to the appropriate `System.Text.Encoding` before loading.  
- **Large files:** For files larger than 200 MB, enable `image.LoadOptions.Streaming = true` to keep memory usage under 100 MB.

## Frequently asked questions

**Q: Can I search for text in password‑protected DWG files?**  
A: Yes. Provide the password via `CadLoadOptions.Password` when calling `Image.Load`.

**Q: Does the API support searching across multiple DWG files at once?**  
A: Absolutely. Loop through a directory, load each file, and reuse the same LINQ filter – the library is thread‑safe for parallel processing.

**Q: How accurate is the text extraction for complex annotations?**  
A: Aspose.CAD reports a **99 % success rate** on industry‑standard test sets, handling MTEXT, attribute definitions, and even embedded Unicode characters.

**Q: Is there a way to highlight found text in a viewer?**  
A: After obtaining the `Location` of each `TextFragment`, you can draw a temporary overlay using any CAD viewer that accepts geometry primitives.

**Q: What licensing model applies to Aspose.CAD?**  
A: The product uses a per‑developer or per‑server license model; a free evaluation license is available for 30 days.

---

**Last Updated:** 2026-10-04  
**Tested With:** Aspose.CAD 24.11 for .NET  
**Author:** Aspose  

## Text search and manipulation tutorials
### [Searching Text in DWG Files with C# - Aspose.CAD Tutorial](./searching-text-in-dwg-files/)









```csharp
using Aspose.CAD;
using Aspose.CAD.ImageOptions;

// Load the DWG file
using var image = (CadImage)Image.Load("sample.dwg");

// Retrieve all text fragments
var fragments = image.TextFragments;

// Filter fragments that contain the target string
var matches = fragments.Where(t => t.Text.Contains("TargetString"));
```

## Related Tutorials

- [Convert DWG to PDF and Add Text in C# – Aspose.CAD Tutorial](/cad/net/dwg-file-manipulation/adding-text-to-dwg/)
- [How to convert DWG to PDF and Raster Images using Aspose.CAD for .NET](/cad/net/advanced-export-techniques/exporting-dwg-to-pdf-or-raster-images/)
- [How to Render CAD and Convert DWG – Aspose.CAD .NET](/cad/net/conversion-and-export/)


{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}