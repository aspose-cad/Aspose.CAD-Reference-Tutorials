---
title: Add Custom Properties to DWG Files Using Java
linktitle: Add Custom Properties to DWG Files Using Java
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 10
url: /java/additional-features/add-custom-properties/
---

## Complete Source Code
```java



import com.aspose.cad.Image;

import com.aspose.cad.fileformats.cad.CadImage;

import java.util.Map;

public class AddCustomProperties {
        public static void main(String[] args) {
                //ExStart:1
                String dataDir = "Your Document Directory" + "DXFDrawings/";
                String srcFile = dataDir + "conic_pyramid.dxf";
                String outFile = dataDir + "AddCustomProperties_out.dxf";
                CadImage cadImage = (CadImage)Image.load(srcFile);

                cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_1", "Custom property test 1");
                cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_2", "Custom property test 2");
                cadImage.getHeader().getCustomProperties().put("CUSTOM_PROPERTY_3", "Custom property test 3");

                cadImage.save(outFile);
                //ExEnd:1
                System.out.println("\nAddCustomProperties executed successfully.");
        }
}
```
