---
title: Mesh Support in CAD
linktitle: Mesh Support in CAD
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/advanced-cad-features/mesh-support-in-cad/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;


public class MeshSupport {

    public static void main(String[] args) 
    {
       
       String dataDir = "Your Document Directory" + "CADConversion/";
       
       String sourceFilePath = dataDir +"meshes.dwg";
       String outPath = dataDir + "meshes.pdf";

       CadImage cadImage = (CadImage)Image.load(sourceFilePath);
       
       CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
        rasterizationOptions.setPageWidth(1600);
        rasterizationOptions.setPageHeight(1600);
        rasterizationOptions.setLayouts( new String[] { "Model" });
        
        PdfOptions pdfOptions = new PdfOptions();
        pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
        
        cadImage.save(outPath, pdfOptions);
        
       
    }
}

```
