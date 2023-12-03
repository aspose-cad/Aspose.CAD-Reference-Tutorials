---
title: Export STL to PNG - Aspose.CAD for Java Tutorial
linktitle: Export STL to PNG - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 20
url: /java/other-cad-tutorials/export-stl-to-png/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

   

import com.aspose.cad.Image;

import com.aspose.cad.fileformats.dgn.DgnImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PngOptions;

public class ExportSTLToPNG {
    public static void main(String[] args)
    {
        //ExStart:ExportSTLToPNG
        String dataDir = "Your Document Directory" + "ExportingSTL/";
        String fileName = dataDir + "example.stl";

        CadImage cadImage = (CadImage)Image.load(fileName);
        CadRasterizationOptions vectorOptions = new CadRasterizationOptions();
        vectorOptions.setPageWidth(1500);
        vectorOptions.setPageHeight(1500);
 
        PngOptions pngOptions = new PngOptions();
        //pngOptions.setVectorRasterizationOptions(rasterizationOptions);
        String outPath = dataDir + "galeon.stl.png";
        cadImage.save(outPath, pngOptions);

        //ExEnd:ExportSTLToPNG
    }
}
```
