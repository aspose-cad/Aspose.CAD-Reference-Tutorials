---
title: Export IFC to PNG - Aspose.CAD for Java Tutorial
linktitle: Export IFC to PNG - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 18
url: /java/cad-export-options/export-ifc-to-png/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.ifc.IfcImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;


public class ExportIFCToPNG {
     public static void main(String[] args)
     {
        String dataDir = "Your Document Directory" + "ExportingIFC/";
        
        String fileName = dataDir +"example.ifc";
        IfcImage cadImage = (IfcImage)Image.load(fileName);

        CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
        vectorOptions.setPageWidth(1500);
        vectorOptions.setPageHeight(1500);
 
        PngOptions pngOptions = new PngOptions();
        pngOptions.setVectorRasterizationOptions(vectorOptions);
        String outPath = dataDir + "example.png";
        cadImage.save(dataDir, pngOptions);


        
    }
}
```
