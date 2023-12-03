---
title: Adjusting CAD Drawing Size Using Unit Type
linktitle: Adjusting CAD Drawing Size Using Unit Type
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 14
url: /java/cad-file-manipulation/adjusting-cad-drawing-size-using-unit-type/
---

## Complete Source Code
```java


import com.aspose.cad.Image;
import com.aspose.cad.ImageOptionsBase;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;

public class AdjustingCADDrawingSizeUsingUnitType 
{

    public static void main(String[] args) 
    {
       //ExStart:AdjustingCADDrawingSizeUsingUnitType
       String dataDir = "Your Document Directory" + "CADConversion/";
        // Path to source file
        String sourceFilePath = dataDir + "sample.dwg";
            
        // Load a CAD drawing in an instance of Image
      Image image = Image.load(sourceFilePath);
		
        
        // Create an instance of BmpOptions class
        com.aspose.cad.imageoptions.BmpOptions bmpOptions = new com.aspose.cad.imageoptions.BmpOptions();

        // Create an instance of CadRasterizationOptions and set its various properties
        com.aspose.cad.imageoptions.CadRasterizationOptions cadRasterizationOptions = 
                new com.aspose.cad.imageoptions.CadRasterizationOptions();
        
        bmpOptions.setVectorRasterizationOptions(cadRasterizationOptions);

        // Set the UnitType property
        cadRasterizationOptions.setUnitType(com.aspose.cad.imageoptions.UnitType.Centimenter);

        // Set the layouts property
        cadRasterizationOptions.setLayouts( new String[] { "Model" } );
                
        // Export layout to BMP format
        String outPath = sourceFilePath + ".bmp";
        image.save(outPath, bmpOptions);
    //ExEnd:AdjustingCADDrawingSizeUsingUnitType
    }
    

}

```
