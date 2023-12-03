---
title: Edit Hyperlink - Aspose.CAD for Java Tutorial
linktitle: Edit Hyperlink - Aspose.CAD for Java Tutorial
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 17
url: /java/other-cad-tutorials/edit-hyperlink/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.cadobjects.CadBaseEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadBlockEntity;
import com.aspose.cad.fileformats.cad.cadobjects.CadInsertObject;


public class EditHyperlink {
    
    public static void main(String[] args)
    {
        //ExStart:EditHyperlink
        String dataDir = "Your Document Directory" + "DWGDrawings/";
              
        
        CadImage cadImage = (CadImage)Image.load(dataDir + "AutoCad_Sample.dwg");
        for (CadBaseEntity entity : cadImage.getEntities())
        {
            if (entity instanceof CadInsertObject)
            {
                CadBlockEntity block = cadImage.getBlockEntities().get_Item(((CadInsertObject)entity).getName());
                String value = block.getXRefPathName().getValue();
                if (value != null && !value.contentEquals(""))
                {
                    block.getXRefPathName().setValue("new file reference.dwg");
                }

            }

            if (entity.getHyperlink() == "https://products.aspose.com")
            {
                entity.setHyperlink("https://www.aspose.com");
            }
        }     
        
        
        //ExEnd:EditHyperlink
    }
}

```
