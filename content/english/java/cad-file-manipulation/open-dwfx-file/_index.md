---
title: Open DWFX File
linktitle: Open DWFX File
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/cad-file-manipulation/open-dwfx-file/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class OpenDwfxFile {
    public static void main(String[] args) {
        //ExStart:1
        String SourceDir = Utils.getDataDir_DWFXDrawings();
        String OutputDir = Utils.getDataDir_Output();
        String filePath = SourceDir + "Tyrannosaurus.dwfx";

        Image cadImageDwf = Image.load(filePath);

        CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();

        rasterizationOptions.setPageWidth(cadImageDwf.getSize().getWidth());
        rasterizationOptions.setPageHeight(cadImageDwf.getSize().getHeight());

        PdfOptions CADf = new PdfOptions();
        CADf.setVectorRasterizationOptions(rasterizationOptions);

        cadImageDwf.save(OutputDir + "OpenDwfxFile_out.pdf", CADf);
        //ExEnd:1
        System.out.println("OpenDwfxFile executed successfully");
    }
}
```
