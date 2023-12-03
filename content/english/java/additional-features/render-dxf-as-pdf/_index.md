---
title: Render DXF as PDF Using Java
linktitle: Render DXF as PDF Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 19
url: /java/additional-features/render-dxf-as-pdf/
---

## Complete Source Code
```java


import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class RenderDXFAsPDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "DXFDrawings/";
             //ExStart:RenderDXFAsPDF
		String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image image = Image.load(srcFile);
		
	    // Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setBackgroundColor(Color.getWhite());
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);

	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();
	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

	    // Export the DXF to PDF
	    image.save(dataDir + "conic_pyramid_out_.pdf", pdfOptions);                	
         //ExEnd:RenderDXFAsPDF
	}
	
}

```
