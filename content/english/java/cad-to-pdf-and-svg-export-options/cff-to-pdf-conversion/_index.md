---
title: CFF to PDF Conversion - Aspose.CAD for Java Tutorial
linktitle: CFF to PDF Conversion - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 13
url: /java/cad-to-pdf-and-svg-export-options/cff-to-pdf-conversion/
---

## Complete Source Code
```java




import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.PdfOptions;


public class CFFToPDF {

    public static void main(String[] args) 
    {
        
        
        String dataDir = "Your Document Directory" + "CFF/";
        // Path to source file
        String sourceFilePath = dataDir+"WineBottle_Die.cf2";
        
        Image image = Image.load(sourceFilePath);
        {
            PdfOptions options = new PdfOptions();
            image.save(dataDir + "WineBottle_Die_out.pdf",options);
        }
        
        
        
    }
    
}

```