---
title: Save DXF Files with Java
linktitle: Save DXF Files with Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 20
url: /java/additional-features/save-dxf-files/
---

## Complete Source Code
```java




import com.aspose.cad.Color;
import com.aspose.cad.Image;


import com.aspose.cad.fileformats.cad.CadImage;
import com.aspose.cad.imageoptions.CadRasterizationOptions;
import com.aspose.cad.imageoptions.PdfOptions;
import java.io.File;
public class SaveDXFFiles {
    
public static void main(String[] args){
    //ExStart:SaveDXFFiles

        String dataDir = "Your Document Directory" + "CADConversion/";
        String srcFile = dataDir + "conic_pyramid.dxf";    
        
        CadImage cadImage = (CadImage)Image.load(srcFile);
        cadImage.save(dataDir+"conic.dxf");

//ExEnd:SaveDXFFiles

}

}
```
