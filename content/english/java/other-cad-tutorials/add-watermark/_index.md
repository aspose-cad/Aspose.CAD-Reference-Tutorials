---
title: Add Watermark - Aspose.CAD for Java Tutorial
linktitle: Add Watermark - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/other-cad-tutorials/add-watermark/
---

## Complete Source Code
```java




import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadMText;
import com.aspose.cad.fileformats.cad.cadobjects.CadText;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;


public class AddWatermark {

    public static void main(String[] args) 
    {
        
        //ExStart:AddWatermark
        String dataDir = "Your Document Directory" + "DWGDrawings/";
        // Path to source file
        String sourceFilePath = dataDir+"Drawing11.dwg";
        
        CadImage cadImage = (CadImage) Image.load(sourceFilePath);
        
        //add new MTEXT
        CadMText watermark = new CadMText();
        watermark.setText("Watermark message");
        watermark.setInitialTextHeight(40);
        watermark.setInsertionPoint(new Cad3DPoint(300, 40));
        watermark.setLayerName("0");
        cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(watermark);
        
        
        
        // or add more simple entity like Text
        CadText text = new CadText();
        text.setDefaultValue("Watermark text");
        text.setTextHeight(40);
        text.setFirstAlignment(new Cad3DPoint(300, 40));
        text.setLayerName("0") ;
        cadImage.getBlockEntities().get_Item("*Model_Space").addEntity(text);
        
        
        
        // export to pdf
        CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
        rasterizationOptions.setPageWidth(1600);
        rasterizationOptions.setPageHeight(1600);
        rasterizationOptions.setLayouts(new String[]{"Model"});
        PdfOptions pdfOptions = new PdfOptions();
        pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
        cadImage.save(dataDir + "AddWatermark_out.pdf", pdfOptions);
        //ExEnd:AddWatermark
    }
}

```
