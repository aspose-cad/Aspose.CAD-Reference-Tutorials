---
title: Export Specific DXF Layout to PDF with Java
linktitle: Export Specific DXF Layout to PDF with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 17
url: /java/additional-features/export-specific-layout-to-pdf/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class ExportSpecificDXFLayoutToPDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
            String dataDir = "Your Document Directory" + "DXFDrawings/";
            //ExStart:ExportSpecificDXFLayoutToPDF
            String srcFile = dataDir + "conic_pyramid.dxf";
		
            Image image = Image.load(srcFile); 
	    
		// Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);   
	    // Specify desired layout name
	    rasterizationOptions.setLayouts(new String[] {"Model"});
	    
	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();
	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

	    // Export the DXF to PDF
	    image.save(dataDir + "conic_pyramid_layout_out_.pdf", pdfOptions);
            //ExEnd:ExportSpecificDXFLayoutToPDF
	}
}

```
