---
title: Export DXF to WMF Format Using Java
linktitle: Export DXF to WMF Format Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 14
url: /java/additional-features/export-dxf-to-wmf/
---

## Complete Source Code
```java


import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.WmfOptions;

public class ExportDXFToWMF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "DXFDrawings/";
	//ExStart:ExportDXFToWMF
               String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image image = Image.load(srcFile);
		
	        IfcImage cadImage = (IfcImage)Image.load((dataDir +"example.ifc"));
            try
            {
              {
                CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
 
                rasterizationOptions.setPageWidth(100);
                rasterizationOptions.setPageHeight(100);
                WmfOptions wmfOptions = new WmfOptions();
              
                cadImage.save(dataDir+" example.ifc.wmf", wmfOptions);
            }
          }
          finally
          {
            cadImage.dispose();
          
          }

	    // Export the DXF to PDF
	    image.save(dataDir + "conic_pyramid_out_.pdf");                	
	}
	//ExEnd:ExportDXFToWMF
}


```
