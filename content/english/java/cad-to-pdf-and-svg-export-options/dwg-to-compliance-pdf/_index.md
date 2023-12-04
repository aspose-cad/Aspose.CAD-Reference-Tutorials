---
title: DWG to Compliance PDF
linktitle: DWG to Compliance PDF
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-to-pdf-and-svg-export-options/dwg-to-compliance-pdf/
---

## Complete Source Code
```java

import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfCompliance;
import com.aspose.cad.imageoptions.PdfDocumentOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class DWGToCompliancePDF {

	public static void main(String[] args) {
		
		// The path to the resource directory.
		String dataDir = "Your Document Directory" + "DWGDrawings/";
	    
         	String srcFile = dataDir + "Bottom_plate.dwg";
       		
	
                com.aspose.cad.Image objImage = com.aspose.cad.Image.load(srcFile);
               // Create an instance of PdfOptions
                PdfOptions pdfOptions = new PdfOptions();
                pdfOptions.setVectorRasterizationOptions(new CadRasterizationOptions());

                pdfOptions.setCorePdfOptions(new PdfDocumentOptions());

                pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1a);
                objImage.save(dataDir+"Saved1.pdf", pdfOptions);

                pdfOptions.getCorePdfOptions().setCompliance(PdfCompliance.PdfA1b);
                objImage.save(dataDir+"Saved.pdf", pdfOptions);
	   
        }

    }

```
