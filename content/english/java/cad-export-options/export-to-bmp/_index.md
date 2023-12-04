---
title: Export to BMP - Aspose.CAD for Java Tutorial
linktitle: Export to BMP - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/cad-export-options/export-to-bmp/
---

## Complete Source Code
```java


import com.aspose.cad.Image;
import com.aspose.cad.InterpolationMode;
import com.aspose.cad.SmoothingMode;
import com.aspose.cad.TextRenderingHint;

import com.aspose.cad.imageoptions.BmpOptions;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
//import com.aspose.cad.imageoptions.TypeOfEntities;

public class ExportToBMP {

	public static void main(String[] args) {
		
		
                 // The path to the resource directory.
		String dataDir = "Your Document Directory" + "ExportingCAD/";
                
                String fileName = (dataDir + "site.dwf");
               
            com.aspose.cad.Image image = com.aspose.cad.Image.load(fileName);
        
            BmpOptions bmpOptions = new BmpOptions();
           
            CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
            bmpOptions.setVectorRasterizationOptions(rasterizationOptions);
 
            rasterizationOptions.setPageHeight(500);
            rasterizationOptions.setPageWidth(500);
            rasterizationOptions.setLayouts(new String[] { "Model" });
            // export
            String outPath = dataDir +"site.bmp";
            image.save(outPath, bmpOptions);
          		
	 

}
}

```
