---
title: Load DWG File & Access Underlay Flags – Aspose.CAD for Java
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
description: Learn how to load DWG file and extract underlay information with Aspose.CAD for Java – a step‑by‑step guide covering underlay flags.
weight: 11
url: /java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
date: 2025-12-22
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# Load DWG File & Access Underlay Flags – Aspose.CAD for Java

In modern CAD workflows, **loading a DWG file** quickly and pulling out underlay details is a common requirement. Whether you’re building a viewer, automating batch processing, or extracting metadata for GIS integration, Aspose.CAD for Java gives you a clean, code‑first way to do it. In this tutorial we’ll walk through the exact steps to **load DWG file**, iterate its entities, and read the underlay flags that many developers overlook.

## Quick Answers
- **What is the primary class to open a DWG?** `com.aspose.cad.Image.load()` returns a `CadImage`.
- **Which object holds underlay information?** `CadUnderlay` (or its derived types like `CadDgnUnderlay`).
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.
- **Can I process multiple DWG files in a loop?** Yes – just repeat the load‑and‑iterate pattern.
- **Is this approach compatible with Java 11+?** Absolutely, Aspose.CAD supports Java 8 through the latest LTS releases.

## What is “load dwg file” in Aspose.CAD?
`Image.load()` reads the binary DWG content and creates an in‑memory `CadImage` object. From there you can explore layers, blocks, and underlay entities without dealing with the DWG file format yourself.

## Why extract underlay flags from a DWG?
Underlay flags tell you how an external reference (like a DGN or PDF underlay) is positioned, scaled, and rotated inside the drawing. Knowing these values lets you:

- Re‑create the exact visual layout in a custom viewer.
- Convert underlays to native CAD entities for further editing.
- Generate reports that include underlay metadata for compliance or documentation.

## Prerequisites
- **Aspose.CAD Library** – download from the [releases](https://releases.aspose.com/cad/java/) page.
- **Java Development Kit** – JDK 8 or newer.
- **A folder** containing the DWG files you want to analyse. Replace `"Your Document Directory"` in the code with your actual path.

## Import Namespaces

```java
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;
```

## Step‑by‑Step Guide

### Step 1: Set the Resource Directory
```java
// The path to the resource directory.
String dataDir = "Your Document Directory" + "DWGDrawings/";
```
Define where your DWG files live. Using a dedicated folder keeps the sample clean and portable.

### Step 2: Load the DWG File
```java
// Input file name and path
String fileName = dataDir + "BlockRefDgn.dwg";

// Load an existing DWG file and convert it into CadImage 
CadImage image = (CadImage)Image.load(fileName);
```
Here we **load dwg file** `BlockRefDgn.dwg` into a `CadImage` instance, ready for inspection.

### Step 3: Iterate Through DWG Entities
```java
// Go through each entity inside the DWG file
for(CadBaseEntity entity : image.getEntities())
```
The loop walks every entity—lines, circles, blocks, and underlays—so we can pick out the ones we need.

### Step 4: Identify CadDgnUnderlay Entities
```java
// Check if entity is of CadDgnUnderlay type
if (entity instanceof CadDgnUnderlay)
```
Only `CadDgnUnderlay` objects contain the underlay flags we’re after, so we filter for them.

### Step 5: Access Underlay Information
```java
// Access different underlay flags 
CadUnderlay underlay = (CadUnderlay) entity;
System.out.println(underlay.getUnderlayPath());
System.out.println(underlay.getUnderlayName());
// ... (Additional underlay properties)
break;
```
Once we have a `CadUnderlay`, we can read its path, name, insertion point, rotation, scale factors, and the `UnderlayFlags` enum that indicates visibility, clipping, and other rendering options.

## Common Issues & Tips
- **Null underlay path** – Ensure the DWG actually references an external file; otherwise the path will be empty.
- **Unsupported underlay type** – Aspose.CAD currently supports DGN underlays; PDF underlays are not yet exposed via the API.
- **License exceptions** – Running the code without a valid license will add a watermark to any exported images.

## Frequently Asked Questions

**Q: Can I use Aspose.CAD for Java with other CAD file formats?**  
A: Aspose.CAD primarily focuses on the DWG format, but it also supports DXF, DWF, and other CAD formats.

**Q: Is there a trial version available for Aspose.CAD for Java?**  
A: Yes, you can explore the features with a free trial from [here](https://releases.aspose.com/).

**Q: How can I get support or seek assistance with Aspose.CAD for Java?**  
A: Visit the [Aspose.CAD forum](https://forum.aspose.com/c/cad/19) for community support and discussions.

**Q: Are temporary licenses available for Aspose.CAD for Java?**  
A: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

**Q: Where can I find the comprehensive documentation for Aspose.CAD for Java?**  
A: Refer to the [documentation](https://reference.aspose.com/cad/java/) for detailed information.

---

**Last Updated:** 2025-12-22  
**Tested With:** Aspose.CAD 24.12 for Java  
**Author:** Aspose  

{{< /blocks/products/pf/tutorial-page-section >}}

{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}

{{< blocks/products/products-backtop-button >}}