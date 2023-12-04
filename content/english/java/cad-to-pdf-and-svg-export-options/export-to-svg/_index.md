---
title: Export to SVG
linktitle: Export to SVG
second_title: Aspose.CAD Java API
description: 
type: docs
weight: 12
url: /java/cad-to-pdf-and-svg-export-options/export-to-svg/
---

## Complete Source Code
```java
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


import com.aspose.cad.Image;

import com.aspose.cad.imageoptions.SvgOptions;
import com.aspose.cad.imageoptions.svgoptionsparameters.SvgColorMode;


public class ExportToSVG {
    
    public static void main(String[] args){ 
       
        // The path to the resource directory.
       String dataDir = "Your Document Directory" + "DWGDrawings/";
        Image image = Image.load(dataDir + "meshes.dwg");
        {
            SvgOptions options = new SvgOptions();
            options.setColorType(SvgColorMode.Grayscale);
            options.setTextAsShapes(true);
            image.save(dataDir + "meshes.svg");
        }
    
    }
    
}

```
