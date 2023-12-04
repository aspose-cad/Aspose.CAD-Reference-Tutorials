---
title: Convert CAD Layer to Raster Image Format
linktitle: Convert CAD Layer to Raster Image Format
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-drawing-conversion/convert-cad-layer-to-raster-image/
---

## Complete Source Code
```java


import com.aspose.cad.Image;


import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.JpegOptions;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;

public class ConvertCADLayerToRasterImageFormat {
	
	public static void main(String[] args) {
		
		// The path to the resource directory.	        
                String dataDir = "Your Document Directory" + "CADConversion/";
	
        	String srcFile = dataDir + "conic_pyramid.dxf";
		
		// Load a CAD drawing in an instance of Image
		Image image = Image.load(srcFile);

		// Create an instance of CadRasterizationOptions
		CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
		// Set image width & height
		rasterizationOptions.setPageWidth(500);
		rasterizationOptions.setPageHeight(500);

		

                List<String> stringList = new ArrayList<>(Arrays.asList("0"));
		// Add the layer name to the CadRasterizationOptions's layer list
	        rasterizationOptions.setLayers(stringList);
 
		// Create an instance of JpegOptions (or any ImageOptions for raster formats)
		JpegOptions options = new JpegOptions();
		// Set VectorRasterizationOptions property to the instance of CadRasterizationOptions
		options.setVectorRasterizationOptions(rasterizationOptions);
		// Export each layer to JPEG format
		image.save(dataDir + "CADLayersToRasterImageFormats_out_.jpg", options);
                
	}
}

```
