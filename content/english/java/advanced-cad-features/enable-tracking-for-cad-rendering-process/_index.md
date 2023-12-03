---
title: Enable Tracking for CAD Rendering Process
linktitle: Enable Tracking for CAD Rendering Process
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/advanced-cad-features/enable-tracking-for-cad-rendering-process/
---

## Complete Source Code
```java


import java.io.FileNotFoundException;
import java.io.FileOutputStream;
import java.io.OutputStream;

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class EnableTrackingForCADRenderingProcess {

	public static void main(String[] args) throws FileNotFoundException {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "CADConversion/";
	//ExStart:EnableTrackingForCADRenderingProcess
                String srcFile = dataDir + "conic_pyramid.dxf";
		
		Image image = Image.load(srcFile);
		
		OutputStream stream = new FileOutputStream(dataDir + "conic_pyramid.pdf");
		PdfOptions pdfOptions = new PdfOptions();
		// Create an instance of CadRasterizationOptions and set its various properties
		CadRasterizationOptions cadRasterizationOptions = new CadRasterizationOptions();
		pdfOptions.setVectorRasterizationOptions(cadRasterizationOptions);
		cadRasterizationOptions.setPageWidth(800);
		cadRasterizationOptions.setPageHeight(600);
		
		image.save(stream, pdfOptions);
		
		System.out.println("Tracking enabled successfully for CAD rendering process.");
	//ExEnd:EnableTrackingForCADRenderingProcess
        }

}

```
