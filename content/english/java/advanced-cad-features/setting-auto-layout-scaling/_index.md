---
title: Setting Auto Layout Scaling
linktitle: Setting Auto Layout Scaling
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 17
url: /java/advanced-cad-features/setting-auto-layout-scaling/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class SettingAutoLayoutScaling {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";
		//ExStart:SettingAutoLayoutScaling
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image image = Image.load(srcFile);
		
	    // Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);

	    // Set Auto Layout Scaling
	    rasterizationOptions.setAutomaticLayoutsScaling(true);

	    // Create an instance of PdfOptions
	    PdfOptions pdfOptions = new PdfOptions();
	    // Set the VectorRasterizationOptions property
	    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
	    
	    // Export the CAD to PDF
	    image.save(dataDir + "result_out_.pdf", pdfOptions);
            //ExEnd:SettingAutoLayoutScaling
	}

}

```
