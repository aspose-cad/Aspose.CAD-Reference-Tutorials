---
title: Add Attributes to MText in DWG Files with Java
linktitle: Add Attributes to MText in DWG Files with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 13
url: /java/cad-text-and-formatting/add-attributes-to-mtext/
---

## Complete Source Code
```java


import com.aspose.cad.Color;
import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadconsts.CadEntityTypeName;
import java.util.ArrayList;
import java.util.List;

public class AddAttribMText {

	public static void main(String[] args) 
        {
		
            // The path to the resource directory.
            String dataDir = "Your Document Directory" + "DXFDrawings/";
            
            String srcFile = dataDir + "conic_pyramid.dxf";

            CadImage cadImage =(CadImage) Image.load(srcFile);
            
            List<CadBaseEntity>  mtextList = new ArrayList<CadBaseEntity>();
            List<CadBaseEntity> attribList = new ArrayList<CadBaseEntity>();
            try
            {
                for (CadBaseEntity entity : cadImage.getEntities())
                {
                    if (entity.getTypeName() == CadEntityTypeName.MTEXT)
                    {
                        mtextList.add(entity);
                    }

                    if (entity.getTypeName() == CadEntityTypeName.INSERT)
                    {
                        for (CadBaseEntity childObject : entity.getChildObjects())
                        {
                            if (childObject.getTypeName() == CadEntityTypeName.ATTRIB)
                            {
                                attribList.add(childObject);
                            }
                        }
                    }
                }

                System.out.println("MText Size: "+ mtextList.size());
                System.out.println("Attribute Size: "+ attribList.size());
            }
            finally
            {
                cadImage.dispose();
            }
      
            
      
	
	}
	
}

```
