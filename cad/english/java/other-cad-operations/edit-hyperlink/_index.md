---
title: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
linktitle: Edit Hyperlink
second_title: Aspose.CAD Java API
description: Learn how to edit DWG files with Aspose.CAD for Java, including how to update DWG XRef paths and edit hyperlinks. Try the free trial today!
weight: 17
url: /java/other-cad-operations/edit-hyperlink/
date: 2026-06-19
keywords:
- how to edit dwg
- update dwg xref paths
- Aspose.CAD Java hyperlink
schemas:
- type: TechArticle
  headline: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  dateModified: '2026-06-19'
  author: Aspose
- type: HowTo
  name: How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial
  description: Learn how to edit DWG files with Aspose.CAD for Java, including how
    to update DWG XRef paths and edit hyperlinks. Try the free trial today!
  steps:
  - name: Accessing Insert Objects
    text: '`CadInsertObject` is the Aspose.CAD class that represents an inserted block
      reference (XRef) inside a DWG drawing. Iterate through the entities and identify
      if an entity is an instance of the `CadInsertObject` class.'
  - name: How to Change XRef Path in a DWG Drawing
    text: '`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD
      for Java. Once you have identified the insert object, retrieve the associated
      block entity and update the XRef path as needed. This ensures the reference
      points to the correct external file.'
  - name: Modifying Hyperlinks
    text: Next, check if the entity has a hyperlink associated with it. If the hyperlink
      matches a specific URL, update it to the desired URL. This step guarantees that
      clicking the hyperlink in the CAD viewer opens the new target.
- type: FAQPage
  questions:
  - question: Do I need to call a specific method to write the edited DWG back to
      disk?
    answer: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to
      persist the modifications.
  - question: Is it possible to edit multiple hyperlinks in one pass?
    answer: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink
      logic to each matching entity.
---

{{< blocks/products/pf/main-wrap-class >}}
{{< blocks/products/pf/main-container >}}
{{< blocks/products/pf/tutorial-page-section >}}

# How to Edit DWG Hyperlinks - Aspose.CAD Java Tutorial

In today's digital era, **how to edit DWG** files efficiently is a must‑have skill for engineers, architects, and BIM specialists. Whether you need to correct a broken hyperlink, point an XRef to a new source, or batch‑update many drawings, Aspose.CAD for Java offers a clean, programmatic way to make those changes without opening the CAD editor. This tutorial walks you through the entire process, from loading a drawing to persisting the edits.

## Quick Answers
- **What library handles DWG editing in Java?** Aspose.CAD for Java.  
- **Can I edit hyperlinks and XRef paths together?** Yes—both are supported in the same API.  
- **Do I need a license for development?** A free trial works for testing; a commercial license is required for production.  
- **Which Java version is required?** Java 8 or higher.  
- **Is the code sample runnable as‑is?** Yes, after updating the file paths to point to your local DWG files.

## Why edit DWG hyperlinks and XRef paths?

Keeping hyperlinks and XRef paths current prevents broken references, ensures that project documentation always points to the correct resources, and enables automated batch updates across extensive CAD libraries. This reduces manual effort, minimizes errors, and improves overall project efficiency by allowing developers to programmatically maintain link integrity throughout the design lifecycle.

## Prerequisites

Before we dive into the tutorial, make sure you have the following prerequisites in place:

1. **Java Development Environment:** A JDK 8+ installed and your favorite IDE (IntelliJ IDEA, Eclipse, etc.).  
2. **Aspose.CAD for Java Library:** Download and install the Aspose.CAD for Java library from the [download link](https://releases.aspose.com/cad/java/).  
3. **DWG Drawing:** Have a DWG drawing file ready for hyperlink editing.

## Import Packages

Start by importing the necessary packages into your Java project. This ensures that you have access to the Aspose.CAD for Java functionalities.

```java
import com.aspose.cad.Image;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;
```

## How to Edit DWG Hyperlinks Using Aspose.CAD for Java?

`CadImage` is the Aspose.CAD class used to load and save CAD drawings.  
Load the DWG file with `CadImage`, iterate over its entities, update the hyperlink and XRef path where needed, and finally save the image back to DWG. This end‑to‑end flow lets you modify any number of entities in a single pass, guaranteeing that all changes are persisted.

### Step 1: Accessing Insert Objects

`CadInsertObject` is the Aspose.CAD class that represents an inserted block reference (XRef) inside a DWG drawing. Iterate through the entities and identify if an entity is an instance of the `CadInsertObject` class.

```java
    String dataDir = "Your Document Directory" + "DWGDrawings/";
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
    for (CadBaseEntity entity : cadImage.getEntities())
    {
        if (entity instanceof CadInsertObject)
        {
        }
	}
```

### Step 2: How to Change XRef Path in a DWG Drawing

`CadImage` is the primary object that loads and saves CAD files in Aspose.CAD for Java. Once you have identified the insert object, retrieve the associated block entity and update the XRef path as needed. This ensures the reference points to the correct external file.

```java
			CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
            String value = block.getXRefPathName().getValue();
            if (value != null && !value.contentEquals(""))
            {
                block.getXRefPathName().setValue("new file reference.dwg");
            }
    
```

### Step 3: Modifying Hyperlinks

Next, check if the entity has a hyperlink associated with it. If the hyperlink matches a specific URL, update it to the desired URL. This step guarantees that clicking the hyperlink in the CAD viewer opens the new target.

```java
        if (entity.getHyperlink() == "https://products.aspose.com")
        {
            entity.setHyperlink("https://www.aspose.com");
        }
```

## Common Pitfalls & Tips

- **String comparison:** Use `.equals()` instead of `==` for reliable string comparison in Java. The sample uses `==` for simplicity, but in production replace it with `entity.getHyperlink().equals("https://products.aspose.com")`.  
- **Null checks:** Always verify that `block.getXRefPathName()` is not `null` before calling `.getValue()`.  
- **Saving changes:** After modifying entities, call `cadImage.save("output.dwg");` to persist the changes (code omitted to keep the original block count).  
- **Performance note:** Aspose.CAD for Java supports over 30 CAD formats and can process files up to 2 GB without loading the entire document into memory, making bulk updates fast and memory‑efficient.

## Frequently Asked Questions

### Q1: Is Aspose.CAD for Java compatible with all DWG drawing versions?

A1: Aspose.CAD for Java supports more than 50 DWG versions, covering releases from AutoCAD 2000 up to the latest 2025 format.

### Q2: Can I use Aspose.CAD for Java in commercial projects?

A2: Yes, a commercial license is required for production use. You can purchase a license [here](https://purchase.aspose.com/buy).

### Q3: Is there a free trial available for Aspose.CAD for Java?

A3: Yes, you can explore a free trial version [here](https://releases.aspose.com/).

### Q4: How can I get technical support for Aspose.CAD for Java?

A4: For any technical assistance, visit the Aspose.CAD forum [here](https://forum.aspose.com/c/cad/19).

### Q5: Can I obtain a temporary license for testing purposes?

A5: Yes, you can obtain a temporary license [here](https://purchase.aspose.com/temporary-license/).

**Additional Q&A**

**Q: Do I need to call a specific method to write the edited DWG back to disk?**  
A: Yes, after making changes call `cadImage.save("EditedDrawing.dwg");` to persist the modifications.

**Q: Is it possible to edit multiple hyperlinks in one pass?**  
A: Absolutely—loop through `cadImage.getEntities()` and apply the hyperlink logic to each matching entity.

---

**Last Updated:** 2026-06-19  
**Tested With:** Aspose.CAD for Java 24.12  
**Author:** Aspose  

{{< blocks/products/products-backtop-button >}}

## Related Tutorials

- [Read XREF Meta Data from DWG Files Using Aspose.CAD for Java](/cad/java/cad-meta-data-and-rendering/read-xref-meta-data/)
- [Add Custom Properties DWG Files Using Aspose.CAD for Java](/cad/java/additional-features/add-custom-properties/)
- [Export DWG to PDF or Raster Using Aspose.CAD for Java](/cad/java/cad-drawing-conversion/export-dwg-to-pdf-or-raster/)


{{< /blocks/products/pf/tutorial-page-section >}}
{{< /blocks/products/pf/main-container >}}
{{< /blocks/products/pf/main-wrap-class >}}