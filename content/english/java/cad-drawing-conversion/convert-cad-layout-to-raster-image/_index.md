---
title: Convert CAD Layout to Raster Image Format
linktitle: Convert CAD Layout to Raster Image Format
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/cad-drawing-conversion/convert-cad-layout-to-raster-image/
---

## Complete Source Code
```java


import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.fileformats.tiff.enums.TiffExpectedFormat;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.TiffOptions;

public class ConvertCADLayoutToRasterImageFormat {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";

            String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image image = Image.load(srcFile);

		// Create an instance of CadRasterizationOptions
		CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

		// Set page width & height
		rasterizationOptions.setPageWidth(1200);
		rasterizationOptions.setPageHeight(1200);

		// Specify a list of layout names
		rasterizationOptions.setLayouts(new String[] {"Model", "Layout1"});

		// Create an instance of TiffOptions for the resultant image
		ImageOptionsBase options = new TiffOptions(TiffExpectedFormat.Default);

		// Set rasterization options
		options.setVectorRasterizationOptions(rasterizationOptions);

		// Save resultant image
		image.save(dataDir + "conic_pyramid_layoutstorasterimage_out_.tiff", options);

        }

}

```
