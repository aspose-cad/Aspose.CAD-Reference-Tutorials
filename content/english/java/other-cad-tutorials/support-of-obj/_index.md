---
title: Support of OBJ - Aspose.CAD for Java Tutorial
linktitle: Support of OBJ - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 19
url: /java/other-cad-tutorials/support-of-obj/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;


public class SupportOfOBJ {
    
     public static void main(String[] args)
    {
        
        String dataDir = "Your Document Directory" + "OBJDrawings/";
        
        Image cadDoc = Image.load(dataDir + "example-580-W.obj");
        CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
        rasterizationOptions.setPageWidth(cadDoc.getSize().getWidth());
        rasterizationOptions.setPageHeight(cadDoc.getSize().getHeight());
        PdfOptions CADf = new PdfOptions();
        CADf.setVectorRasterizationOptions(rasterizationOptions);
        cadDoc.save(dataDir + "example-580-W_custom.pdf", CADf);
        
         
    }

}

```
