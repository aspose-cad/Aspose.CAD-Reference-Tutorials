---
title: Export to PDF - Aspose.CAD for Java Tutorial
linktitle: Export to PDF - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 13
url: /java/cad-export-options/export-to-pdf/
---

## Complete Source Code
```java


import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;

public class ExportToPDF {

	public static void main(String[] args) {
		
		
                 // The path to the resource directory.
		String dataDir = "Your Document Directory" + "ExportingCAD/";
		//ExStart:ExportToPDF
                String fileName = (dataDir +"site.dwf");
                com.aspose.cad.Image image = com.aspose.cad.Image.load(fileName);
                {
                    PdfOptions pdfOptions = new PdfOptions();
                    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
                    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
 
                    rasterizationOptions.setPageHeight(500);
                    rasterizationOptions.setPageWidth(500);
                    rasterizationOptions.setLayouts(new String[] { "Model" });
                    // export
                    String outPath = dataDir + "site.pdf";
                    image.save(outPath, pdfOptions);
                }		

	 //ExEnd:ExportToPDF
}
}

```
