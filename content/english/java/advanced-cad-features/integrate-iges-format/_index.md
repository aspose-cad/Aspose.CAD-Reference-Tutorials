---
title: Integrate IGES Format
linktitle: Integrate IGES Format
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/advanced-cad-features/integrate-iges-format/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;


public class IntegrateIGESFormat {
public static void main(String[] args) 
    {
       
       String dataDir = "Your Document Directory" + "CADConversion/";
       
       String sourceFilePath = dataDir + "figa2.igs";
       String outPath = dataDir +"meshes.pdf";
       
       
       Image igesImage = Image.load(sourceFilePath);
               
       PdfOptions pdf = new PdfOptions();
        CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
        vectorOptions.setPageHeight(1000) ;
        vectorOptions.setPageWidth(1000);
        
        pdf.setVectorRasterizationOptions(vectorOptions);
        
        igesImage.save(outPath, pdf);
       
    }
}

```
