---
title: Render DWG Document to Image with Java
linktitle: Render DWG Document to Image with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-meta-data-and-rendering/render-dwg-to-image/
---

## Complete Source Code
```java

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class RenderDWGDocument {

	public static void main(String[] args) {
		
            // The path to the resource directory.
            String dataDir = "Your Document Directory" + "DWGDrawings/";
	    
            String srcFile = dataDir + "visualization_-_conference_room.dwg";
       		
            Image image = Image.load(srcFile);
		
	    // Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);
	    // Specify desired layout name
	    rasterizationOptions.setLayouts(new String[] {"Layout1"});

	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();
	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

	    // Export the DWG to PDF
	    image.save(dataDir + "ExportSpecificLayoutToPDF_out_.pdf", pdfOptions);	
            
            
       }
}

```
