---
title: Read XREF Meta Data from DWG Files Using Java
linktitle: Read XREF Meta Data from DWG Files Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/cad-meta-data-and-rendering/read-xref-meta-data/
---

## Complete Source Code
```java

import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.Cad3DPoint;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;

public class ReadXREEFMetaData {

	public static void main(String[] args) {
		
            // The path to the resource directory.
            String dataDir = "Your Document Directory" + "DWGDrawings/";
	    
            CadImage image = (CadImage)Image.load(dataDir+"Bottom_plate.dwg");
            {
                for (CadBaseEntity entity : image.getEntities())
                {
                    if (entity instanceof CadUnderlay)
                    {
                        //XREF entity with metadata
                        Cad3DPoint insertionPoint = ((CadUnderlay) entity).getInsertionPoint();
                        String path = ((CadUnderlay) entity).getUnderlayPath();
                    }
                }
            }	
	
       }
}

```
