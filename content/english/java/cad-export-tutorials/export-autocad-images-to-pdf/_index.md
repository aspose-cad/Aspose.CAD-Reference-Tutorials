---
title: Export AutoCAD Images to PDF - Aspose.CAD for Java Tutorial
linktitle: Export AutoCAD Images to PDF - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/cad-export-tutorials/export-autocad-images-to-pdf/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;

public class Export3DAutoCADImagesToPDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "ExportingCAD/";
		//ExStart:Export3DAutoCADImagesToPDF
                
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image cadImage = Image.load(srcFile);

		CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
		rasterizationOptions.setPageWidth(500);
		rasterizationOptions.setPageHeight(500);
//		rasterizationOptions.setTypeOfEntities(TypeOfEntities.Entities3D);

		rasterizationOptions.setLayouts(new String[] {"Model"});
		PdfOptions pdfOptions = new PdfOptions();
		pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
		cadImage.save(dataDir + "Export3DImagestoPDF_out_.pdf", pdfOptions);
                //ExStart:Export3DAutoCADImagesToPDF

	}

}

```
