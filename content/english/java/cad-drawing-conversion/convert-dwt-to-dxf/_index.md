---
title: Convert DWT to DXF Format Using Java
linktitle: Convert DWT to DXF Format Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 15
url: /java/cad-drawing-conversion/convert-dwt-to-dxf/
---

## Complete Source Code
```java


import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;


public class ConvertDWTToDXF {
    
    public static void main(String[] args){ 
    
    String dataDir = "Your Document Directory" + "DWTDrawings/";  
    
    CadImage cadImage = (CadImage)Image.load(dataDir + "sample.dwt");
    String outFile = dataDir+ "example.dxf";
    cadImage.save(outFile);
    
    }
    
    
}

```
