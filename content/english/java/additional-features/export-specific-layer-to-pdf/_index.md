---
title: Export Specific Layer of DXF Drawing to PDF with Java
linktitle: Export Specific Layer of DXF Drawing to PDF with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 18
url: /java/additional-features/export-specific-layer-to-pdf/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class ExportSpecificLayerOfDXFDrawingToPDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
            String dataDir = "Your Document Directory" + "DXFDrawings/";
            //ExStart:ExportSpecificLayerOfDXFDrawingToPDF
            String srcFile = dataDir + "conic_pyramid.dxf";
            
            Image image = Image.load(srcFile);
	    
            //  Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);
	    // Add desired layers
            List<String> stringList = new ArrayList<>(Arrays.asList("0"));
	     rasterizationOptions.setLayers(stringList);
 

	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();
	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
	    
	    // Export the DXF to PDF
	    image.save(dataDir + "conic_pyramid_layer_out_.pdf", pdfOptions);                
            //ExEnd:ExportSpecificLayerOfDXFDrawingToPDF
	}
}

```
