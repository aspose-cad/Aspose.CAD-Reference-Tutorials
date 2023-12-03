---
title: Export DGN as Part of DWG - Aspose.CAD for Java Tutorial
linktitle: Export DGN as Part of DWG - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/dgn-export-tutorials/export-dgn-as-part-of-dwg/
---

## Complete Source Code
```java






public class ExportDGNAsPartofDWG 
{
    public static void main(String[] args)
    {
        //ExStart:ExportDGNAsPartofDWG
        
        // Input and Output file paths
            String dataDir = "Your Document Directory" + "ExportingDGN/";
        // Input and Output file paths
        String fileName = dataDir + "BlockRefDgn.dwg";
        String outPath = dataDir +"BlockRefDgn.dwg.pdf";

        // Create an instance of PdfOptions class as we are exporting the DWG file to PDF format
        com.aspose.cad.imageoptions.PdfOptions exportOptions = new com.aspose.cad.imageoptions.PdfOptions();

        // Load any existing DWG file as image and convert it to CadImage type
        com.aspose.cad.fileformats.cad.CadImage cadImage = (com.aspose.cad.fileformats.cad.CadImage) com.aspose.cad.Image.load(fileName);

        // Go through each entity inside the DWG file
        for (com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity baseEntity : cadImage.getEntities())
        {
            // Check if entity is an image definition
            if (baseEntity.getTypeName() == com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName.DGNUNDERLAY)
            {
                com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay dgnFile = (com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay)baseEntity;

                // Get external reference to object
                System.out.println(dgnFile.getUnderlayPath());
            }
        }

        // Define settings for CadRasterizationOptions object
        com.aspose.cad.imageoptions.CadRasterizationOptions vectorRasterizationOptions = new com.aspose.cad.imageoptions.CadRasterizationOptions();
        vectorRasterizationOptions.setPageWidth(1600);
        vectorRasterizationOptions.setPageHeight(1600);
        vectorRasterizationOptions.setLayouts(new String[] { "Model" });
        vectorRasterizationOptions.setAutomaticLayoutsScaling(false);
        vectorRasterizationOptions.setNoScaling(true);
      
        vectorRasterizationOptions.setBackgroundColor(com.aspose.cad.Color.getBlack());
        vectorRasterizationOptions.setDrawType(com.aspose.cad.fileformats.cad.CadDrawTypeMode.UseObjectColor);

        // Set Vector Rasterization Options
        exportOptions.setVectorRasterizationOptions(vectorRasterizationOptions);

        // Export the DWG to PDF by calling Save method
        cadImage.save(outPath, exportOptions);

        //ExEnd:ExportDGNAsPartofDWG
        
    }
}

```
