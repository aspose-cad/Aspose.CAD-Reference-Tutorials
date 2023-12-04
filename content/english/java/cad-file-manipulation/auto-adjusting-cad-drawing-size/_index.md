---
title: Auto Adjusting CAD Drawing Size
linktitle: Auto Adjusting CAD Drawing Size
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 13
url: /java/cad-file-manipulation/auto-adjusting-cad-drawing-size/
---

## Complete Source Code
```java


import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;

public class AutoAdjustingCADDrawingSize 
{

    public static void main(String[] args) 
    {

        String dataDir = "Your Document Directory" + "CADConversion/";
        // Path to source file
        String sourceFilePath = dataDir+"sample.dwg";

        // Load a CAD drawing in an instance of Image
        com.aspose.cad.Image objImage = com.aspose.cad.Image.load(sourceFilePath);

        // Create an instance of BmpOptions class
        com.aspose.cad.imageoptions.BmpOptions bmpOptions = new com.aspose.cad.imageoptions.BmpOptions();

        // Create an instance of CadRasterizationOptions and set its various properties
        com.aspose.cad.imageoptions.CadRasterizationOptions cadRasterizationOptions = 
                new com.aspose.cad.imageoptions.CadRasterizationOptions();

        bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);

        // Set the layouts property
        cadRasterizationOptions.setLayouts( new String[] { "Model" } );

        // Export layout to BMP format
        String outPath = sourceFilePath + ".bmp";
        objImage.save(outPath, bmpOptions);
   
    }

}

```
