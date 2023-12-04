---
title: Export CAD Layouts to PDF - Aspose.CAD for Java Tutorial
linktitle: Export CAD Layouts to PDF - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-export-options/export-cad-layouts-to-pdf/
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

public class ExportCADLayoutsToPDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "ExportingCAD/";
		
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		// Create an instance of CadImage class and load the file.
		Image cadImage = Image.load(srcFile);

		// Create an instance of CadRasterizationOptions class
		CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
		rasterizationOptions.setPageWidth(1600);
		rasterizationOptions.setPageHeight(1600);

		// Set the Entities type property to Entities3D.
//		rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);
                rasterizationOptions.setAutomaticLayoutsScaling(true);
                rasterizationOptions.setNoScaling (false);
		//rasterizationOptions.setScaleMethod(ScaleType.GrowToFit);
		rasterizationOptions.setContentAsBitmap(true);

		// Set Layouts
		rasterizationOptions.setLayouts(new String[] {"Model"});

		// Create an instance of PDF options class
		PdfOptions pdfOptions = new PdfOptions();
		pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

		// Set Graphics options
		rasterizationOptions.getGraphicsOptions().setSmoothingMode(SmoothingMode.HighQuality);
		rasterizationOptions.getGraphicsOptions().setTextRenderingHint(TextRenderingHint.AntiAliasGridFit);
		rasterizationOptions.getGraphicsOptions().setInterpolationMode(InterpolationMode.HighQualityBicubic);

		// Export to PDF by calling the Save method
		cadImage.save(dataDir + "CADLayoutsToPDF_out_.pdf", pdfOptions);
                
	}
}

```
