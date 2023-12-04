---
title: Set Canvas Size and Mode
linktitle: Set Canvas Size and Mode
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 16
url: /java/advanced-cad-features/set-canvas-size-and-mode/
---

## Complete Source Code
```java


import java.awt.Image;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.TiffOptions;

public class SetCanvasSizeAndMode {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";
		
                String srcFile = dataDir + "conic_pyramid.dxf";
	    com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
	    // Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);
            
            rasterizationOptions.setAutomaticLayoutsScaling(true); 
	    
            rasterizationOptions.setNoScaling(true);

	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();

	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

	    // Export CAD to PDF
	    objImage.save(dataDir +"result_out_.pdf", pdfOptions);

	    // Create an instance of TiffOptions
	    TiffOptions tiffOptions = new TiffOptions(TiffExpectedFormat.Default);

	    // Set the VectorRasterizationOptions property
	    tiffOptions.setVectorRasterizationOptions(rasterizationOptions);

	    // Export CAD to TIFF
	    objImage.save(dataDir + "result_out_.tiff", tiffOptions);
		
	}

}

```
