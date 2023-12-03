---
title: Export Specific DXF Layout to Image with Java
linktitle: Export Specific DXF Layout to Image with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 16
url: /java/additional-features/export-specific-layout-to-image/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dwf.whip.objects.DwfWhipLayer;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.dwf.DwfImage;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class ExportSpecificDXFLayoutToImage {

	public static void main(String[] args) {
		//ExStart:ExportSpecificDXFLayoutToImage
		// The path to the resource directory.
            String dataDir = "Your Document Directory" + "DXFDrawings\\";
            
            String srcFile = dataDir + "for_layers_test.dwf";
	
            DwfImage image =(DwfImage)Image.load(srcFile); 
	    
            List<String> layersNames=image.getLayers().getLayersNames();
            
            DwfWhipLayer layer = image.getLayers().getLayerByName("0");
            for (DwfWhipLayer lr : image.getLayers())
            {
                //...
            }
            
		// Create an instance of CadRasterizationOptions and set its various properties
	    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
	    rasterizationOptions.setPageWidth(1600);
	    rasterizationOptions.setPageHeight(1600);  
 
          
            String[] stringArray = Arrays.copyOf(layersNames.toArray(), layersNames.toArray().length, String[].class);
            
            List<String> stringList = Arrays.asList(stringArray);
             // Add desired layers
            rasterizationOptions.setLayers(stringList);

            JpegOptions jpegOptions = new JpegOptions();
            jpegOptions.setVectorRasterizationOptions(rasterizationOptions);
            String output = dataDir+"for_layers_test.jpg";
	    // Export the DXF to Image
            image.save(output, jpegOptions);
	   
            //ExEnd:ExportSpecificDXFLayoutToImage
	}
}

```
