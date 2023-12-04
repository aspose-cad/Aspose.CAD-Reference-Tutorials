---
title: Support for Hidden Lines in DWG Files Using Java
linktitle: Support for Hidden Lines in DWG Files Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-text-and-formatting/support-hidden-lines-in-dwg/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.Arrays;
import java.util.List;


public class SupportForHiddenLines {
    
    public static void main(String[] args) 
        {
	     
	    // The path to the resource directory.
            String dataDir = "Your Document Directory" + "DWGDrawings/";
         
            String sourceFilePath = dataDir + "Bottom_plate.dwg";
            String outPath = dataDir + "Bottom_plate.pdf";
            CadImage cadImage = (CadImage)Image.load(sourceFilePath);
                   
            
            List<String> list = Arrays.asList("Print","L1_RegMark","L2_RegMark");
            CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
            rasterizationOptions.setPageHeight(cadImage.getHeight());
            rasterizationOptions.setPageWidth(cadImage.getWidth()) ;
            rasterizationOptions.setLayers(list);
           


            PdfOptions pdfOptions = new PdfOptions();
            rasterizationOptions.setLayouts(new String[] { "Model" });
            pdfOptions.setVectorRasterizationOptions(rasterizationOptions);

            cadImage.save(outPath, pdfOptions);
            
            System.out.println("\nThe DWG file exported successfully to PDF.\nFile saved at " + dataDir);
                    
            }
      
}

```
