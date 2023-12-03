---
title: List Layouts in DWG
linktitle: List Layouts in DWG
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/cad-file-manipulation/list-layouts-in-dwg/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.fileformats.cad.CadLayoutDictionary;
import com.aspose.cad.fileformats.cad.cadobjects.CadLayout;


public class ListLayouts {

    public static void main(String[] args) 
    {
       //ExStart:ListLayouts
       String dataDir = "Your Document Directory" + "CADConversion/";
       String sourceFilePath = dataDir + "conic_pyramid.dxf";
     
       Image image = Image.load(sourceFilePath);
       
       CadImage cadImage = (CadImage)image;
       
        CadLayoutDictionary layouts = cadImage.getLayouts();
        for (CadLayout layout : layouts.getValues())
        {
                    
            System.out.println("Layout " +layout.getLayoutName());
        }
       
       //ExEnd:ListLayouts
    }
}

```
