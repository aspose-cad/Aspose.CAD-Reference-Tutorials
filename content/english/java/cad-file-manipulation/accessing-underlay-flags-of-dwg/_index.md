---
title: Accessing Underlay Flags of DWG
linktitle: Accessing Underlay Flags of DWG
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 11
url: /java/cad-file-manipulation/accessing-underlay-flags-of-dwg/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadDgnUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.CadUnderlay;
import com.aspose.cad.fileformats.cad.cadobjects.UnderlayFlags;


public class AccessingUnderlayFlagsofDWG {
    
    public static void main(String[] args) {
		
         
            // The path to the resource directory.
            String dataDir = "Your Document Directory" + "DWGDrawings/";
	   
            // Input file name and path
            String fileName = dataDir + "BlockRefDgn.dwg";
            
            // Load an existing DWG file and convert it into CadImage 
            CadImage image = (CadImage)Image.load(fileName);
            
            // Go through each entity inside the DWG file
                for(CadBaseEntity entity : image.getEntities())
                {
                    // Check if entity is of CadDgnUnderlay type
                    if (entity instanceof CadDgnUnderlay)
                    {
                        // Access different underlay flags 
                        CadUnderlay underlay = (CadUnderlay) entity;
                        System.out.println(underlay.getUnderlayPath());
                        System.out.println(underlay.getUnderlayName());
                        System.out.println(underlay.getInsertionPoint().getX());
                        System.out.println(underlay.getInsertionPoint().getY());
                        System.out.println(underlay.getRotationAngle());
                        System.out.println(underlay.getScaleX());
                        System.out.println(underlay.getScaleY());
                        System.out.println(underlay.getScaleZ());
                        System.out.println((underlay.getFlags() & UnderlayFlags.UnderlayIsOn) == UnderlayFlags.UnderlayIsOn);
                        System.out.println((underlay.getFlags() & UnderlayFlags.ClippingIsOn) == UnderlayFlags.ClippingIsOn);
                        System.out.println((underlay.getFlags() & UnderlayFlags.Monochrome) != UnderlayFlags.Monochrome);
                        break;
                    }
                }
            
	
       }

}

```
