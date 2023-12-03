---
title: Support for DGN V7 - Aspose.CAD for Java Tutorial
linktitle: Support for DGN V7 - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/other-cad-tutorials/support-for-dgn-v7/
---

## Complete Source Code
```java


import com.aspose.cad.Color;

import java.awt.Image;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.dgn.DgnElementType;
import com.aspose.cad.fileformats.dgn.DgnImage;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.fileformats.dgn.dgnelements.DgnDrawingElementBase;

public class SupportForDGNV7 
{
    public static void main(String[] args)
    {
        // Input and Output file paths
            String dataDir = "Your Document Directory" + "ExportingDGN/";
           //ExStart:SupportForDGNV7   
            String fileName = dataDir + "Nikon_D90_Camera.dgn";
            String outFile  = dataDir + "Nikon_D90_Camera.dgn";
            
            DgnImage objImage = (DgnImage)com.aspose.cad.Image.load(fileName);
            
                PdfOptions options = new PdfOptions();
                CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
                vectorOptions.setPageWidth(1500);
                vectorOptions.setPageHeight(1500);
                vectorOptions.setAutomaticLayoutsScaling(true);
                vectorOptions.setBackgroundColor(Color.getBlack());
                vectorOptions.setLayouts(new String[] { "1", "2", "3", "9" });//only export 4 (1,2,3 and 9) views
                options.setVectorRasterizationOptions(vectorOptions);

                objImage.save(outFile, options);
            
        //ExEnd:SupportForDGNV7
    }
}

```
