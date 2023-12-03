---
title: Enable Tracking in DWG Files Using Java
linktitle: Enable Tracking in DWG Files Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/additional-features/enable-tracking/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.CadRenderResult;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.imageoptions.RenderResult;
import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

/**
 *
 * @author mfazi
 */
public class EnableTracking {
    public static void main(String[] args) throws FileNotFoundException {
        //ExStart:EnableTracking
        
        // The path to the resource directory.
        String dataDir = "Your Document Directory" + "DXFDrawings/";
        
        Image image = Image.load(dataDir + "conic_pyramid.dxf");
        {
            OutputStream stream = new FileOutputStream(dataDir + "output_conic_pyramid.pdf");
            {
                PdfOptions pdfOptions = new PdfOptions();
                CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
                pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
                cadRasterizationOptions.setPageWidth(800);
                cadRasterizationOptions.setPageHeight(600);

                cadRasterizationOptions.RenderResult = new ErrorHandler();

                System.out.println("Exporting to pdf format");
                image.save(stream, pdfOptions);
            }
        }
	//ExEnd:EnableTracking
    }
    //ExStart:CadRenderHandler
    public static class ErrorHandler extends CadRasterizationOptions.CadRenderHandler
    {
        @Override
        public void invoke(CadRenderResult result) {
            System.out.println("Tracking results of exporting");

            if (result.isRenderComplete())
                return;

            System.out.println("Have some problems:");

            int idxError = 1;
            for (RenderResult rr : result.getFailures())
            {
                System.out.printf("{0}. {1}, {2}", idxError, rr.getRenderCode(), rr.getMessage());
                idxError++;
            }
        }
    }
    //ExEnd:CadRenderHandler
    
}

```
