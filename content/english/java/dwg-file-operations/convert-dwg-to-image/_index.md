---
title: Convert Particular DWG to Image Using Java
linktitle: Convert Particular DWG to Image Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 14
url: /java/dwg-file-operations/convert-dwg-to-image/
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
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.util.ArrayList;
import java.util.Collection;
import java.util.Iterator;
import java.util.List;
import java.util.ListIterator;


public class ParticularDWGToImage {
    
public static void main(String[] args) {

    //ExStart:ParticularDWGToImage
    // The path to the resource directory.
        String dataDir = "Your Document Directory" + "DWGDrawings/";
        String sourceFilePath = dataDir + "visualization_-_conference_room.dwg";

        CadImage cadImage = ((CadImage)(Image.load(sourceFilePath)));

        CadBaseEntity[] entities = cadImage.getEntities();
        
        List<CadBaseEntity> filteredEntities = new ArrayList<CadBaseEntity>();
        for (CadBaseEntity baseEntity : entities) {
        // selection or filtration of entities
        if ((baseEntity.getTypeName() == CadEntityTypeName.TEXT)) {
        filteredEntities.add(baseEntity);
        }

        }
 
    CadBaseEntity[] arr = new CadBaseEntity[filteredEntities.size()];
    cadImage.setEntities(filteredEntities.toArray(arr));
    // Create an instance of CadRasterizationOptions and set its various properties
    CadRasterizationOptions rasterizationOptions = new CadRasterizationOptions();
    rasterizationOptions.setPageWidth(1600);
    rasterizationOptions.setPageHeight(1600);
    // Set Auto Layout Scaling
    rasterizationOptions.setAutomaticLayoutsScaling(true);
    // Create an instance of PdfOptions
    PdfOptions pdfOptions = new PdfOptions();
    // Set the VectorRasterizationOptions property
    pdfOptions.setVectorRasterizationOptions(rasterizationOptions);
    String outFile = dataDir + "result_out_generated.pdf";
    // Export the CAD to PDF
    cadImage.save(outFile, pdfOptions);
     //ExEnd:ParticularDWGToImage
    }
}
```
